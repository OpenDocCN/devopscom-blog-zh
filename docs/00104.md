# MongoDB 复制专业提示:报告实例

> 原文：<https://devops.com/mongodb-replication-pro-tips/>

任何有 DevOps 文化，有 MongoDB 支持的应用程序的商店都使用副本集…不仅仅是生产应用程序，还包括那些仍处于原型阶段的应用程序。复制对于正常运行时间至关重要，因此您的运营团队在整个项目开发过程中一直与您的开发人员合作，并且您没有推迟复制策略，直到您有了可运行的应用程序。

您也没有忽略对报告需求的规划。众所周知，除了运行您的应用程序，您还需要获得用户行为、一般使用和其他特定业务指标的分析。您不能只对您的实时数据库运行报告，(原因我将在下面详述，以防您还不清楚)。在您的 DevOps 车间中，开发人员和管理员在项目开始时讨论了隔离报告任务的计划，以便它们不会干扰生产任务。

## 使报告读数远离生产

将报告查询限制到专用节点是一个典型的例子，在整个 [MongoDB 复制文档](http://docs.mongodb.org/manual/core/replication-introduction/)中都有使用。报告不需要写入，并允许最终一致的数据。如果每日摘要来自几秒钟或几分钟的陈旧数据，则不会受到影响。如果您的计数遗漏了一些操作，并且一些计数略有偏差，这不会改变用户行为报告的基本含义。

但是为什么利用这一点如此重要呢？

## 旁白:混合生产和分析的问题

如果对你来说这已经是显而易见的，跳过这一部分。如果你想了解一些背景，请继续阅读。

考虑工作集，MongoDB 在任何给定的时间跨度内读写整个数据库的子集。您的生产环境将有一组活动用户，与他们的数据相关的文档将是操作系统试图保存在物理内存中的内容。

(不要让您的工作集超过 RAM！如果要去那里，你需要[分片](http://docs.mongodb.org/manual/core/sharding-introduction/)，所以容量规划很关键。但那是另外一课。使用 MongoDB 的[免费监控服务](http://mms.mongodb.com/?pk_campaign=devops-com-replication-protips-4-14&pk_kwd=)监控您的实例，并参加[即将举行的容量规划网络研讨会](https://www.mongodb.com/webinar/ops-series-capacity-april-2014?pk_campaign=devops-com-replication-protips-4-14&pk_kwd=)。)

即使您的数据库是可用内存大小的数百或数千倍，如果您已经很好地规划了模式和索引，MongoDB 也会高效地运行，因为工作集之外的数据可以在磁盘上保持不变。随着用户变得空闲，他们的文档将不再使用，他们占用的 RAM 将可用于容纳新的活跃用户的文档。

但是，报告作业读取大范围的数据，不会重复访问相同的数据，并且每个报告任务可能会处理完全不同的数据集。在任何一个相当大的数据库中，这意味着这些作业需要不断地从 RAM 中弹出最近使用过的文档，以便为读取新文档腾出空间。如果您在支持生产工作负载的同一个实例上运行这些作业，您的报告作业将与您的生产应用争夺 RAM 空间，不断排出您的实时用户数据，同时您的应用不断重新加载这些数据。恭喜你，你造出了一台打谷机。

## 具有专用报告实例的副本集

通过利用[隐藏副本集成员](http://docs.mongodb.org/manual/core/replica-set-hidden-member/)，或者[标签集](http://docs.mongodb.org/manual/tutorial/configure-replica-set-tag-sets/)与[读取偏好](http://docs.mongodb.org/manual/core/read-preference/)，您可以在 MongoDB 复制之上构建专用的报告节点。第一种方法更简单，第二种更灵活。

### 查看 MongoDB 副本集

[MongoDB 副本集](http://docs.mongodb.org/manual/core/replication-introduction/)通过将数据复制到一个副本集中的所有节点，并向客户端提供无缝故障转移，创造了持续正常运行时间。它们包含一个允许写入的主节点，而其余的是只读辅助节点。它们自己管理哪个是主要的，[在条件需要时举行选举来决定哪个节点应该是主要的](http://docs.mongodb.org/manual/core/replica-set-elections/)。副本集应该包含奇数个成员，以便在没有联系的情况下进行快速选举。

从根本上说，不可到达的机器是否停机或网络是否已被分区是不可知的，因此，如果副本集中的大多数节点脱机(比方说，3 个成员集中的 2 个)，即使健康的主节点仍然存在，它也会降级为只读的辅助节点。如果不这样做，可能会导致多台机器在网络分区的情况下宣称自己是主机器，并导致可怕的数据不一致。

因此，一个副本集至少包含 3 个成员，提供一个*机器故障的容错能力。*

## 报告实例，隐藏成员

副本集的隐藏成员被配置为`priority: 0`，以防止它们被选为主要成员，并被配置为`hidden: true`，以防止连接到副本集的客户端将读取路由到副本集，即使它们指定了读取首选项`secondary`。

要读取这个隐藏成员，您将使用一个独立的连接，而不是`MongoReplicaSetClient`类型，并指定`slave_ok`。

### 隐藏成员设置

我们可以使用 mongo shell 来隐藏现有副本集的成员:

```
# connect to primary directly
Kusanagi:~ avery$ mongo --port 29019
MongoDB shell version: 2.4.3
connecting to: 127.0.0.1:29019/test

// using my local replica set playground
PRIMARY> conf = rs.config()
{
    "_id" : "test",
    "version" : 21,
    "members" : [
        {
            "_id" : 0,
            "host" : "Kusanagi.local:29017",
        },
        {
            "_id" : 1,
            "host" : "Kusanagi.local:29018",
        },
        {
            "_id" : 2,
            "host" : "Kusanagi.local:29019",
        }
    ]
}

// we'll use members[1], the instance on port 29018
PRIMARY> conf.members[1].priority = 0
PRIMARY> conf.members[1].hidden = true
PRIMARY> conf.version += 1
PRIMARY> rs.reconfig(conf)
Tue Apr  1 12:24:34.045 DBClientCursor::init call() failed
Tue Apr  1 12:24:34.046 trying reconnect to 127.0.0.1:29019
Tue Apr  1 12:24:34.047 reconnect 127.0.0.1:29019 ok
reconnected to server after rs command (which is normal)
```

草薙. local:29018 现已隐藏。它将像往常一样继续复制并在选举中投票，但连接到副本集的客户端将永远不会读取它，即使草薙. local:29019 被删除:

```
irb(main):012:0> rs = Mongo::MongoReplicaSetClient.new(["Kusanagi.local:29017", "Kusanagi.local:29018", "Kusanagi.local:29019"])
=> <Mongo::MongoReplicaSetClient:0x3fe06e4fe564 @seeds=[["Kusanagi.local", 29017], ["Kusanagi.local", 29018], ["Kusanagi.local", 29019]] @connected=true>
irb(main):013:0> rs.primary
=> ["Kusanagi.local", 29017]
irb(main):014:0> rs.secondaries
=> #<Set: {}>
# an empty set -- as far as this connection is concerned, there are no secondaries.
```

报告代码应该是这样的(在 Ruby 中):

```
require 'mongo'
reporting = Mongo::MongoClient.new("Kusanagi.local", "29018", slave_ok: true)

# error checking goes here

reporting['my_application']['users'].aggregate(...)
```

### 考虑

使用隐藏成员是为专用工作负荷(如报告)设置实例的最简单方法，但是:

#### 紧急情况下无法读取隐藏成员

副本集中有两个普通成员和一个隐藏成员，写入容错与常规的 3 成员集相同。但是，如果您失去两个节点，您的生产应用程序将无法正常降级到只读模式，因为您的隐藏成员将不允许副本集客户端读取。如果您只是喜欢隐藏成员的简单性，并且成本不是问题，请使用 5 成员集(隐藏一个成员)来代替。

#### 不能使用副本集的包装代码

许多团队创建特定于应用程序的包装器，将基础设施知识添加到 MongoDB 驱动程序提供的客户机中。由于您需要用一个独立的连接来处理您的报告实例，您将无法重用这项投资，这将使您很难过。

## 报告实例，标记成员

将报告查询路由到专用节点的更复杂但灵活的方法是使用标记和读取首选项。

与隐藏成员一样，将一个成员设置为`priority: 0`，但不要将其设置为隐藏。相反，分配一个标签`use: reporting`:

```
PRIMARY> conf = rs.config()
{
    "_id" : "test",
    "version" : 21,
    "members" : [
        {
            "_id" : 0,
            "host" : "Kusanagi.local:29017",
        },
        {
            "_id" : 1,
            "host" : "Kusanagi.local:29018",
        },
        {
            "_id" : 2,
            "host" : "Kusanagi.local:29019",
        }
    ]
}

// we'll use members[1], the instance on port 29018
PRIMARY> conf.members[1].priority = 0
PRIMARY> conf.members[1].tags = { "use": "reporting" }
PRIMARY> conf.version += 1
PRIMARY> rs.reconfig(conf)
[...]
```

和以前一样，草薙. local:29018 永远不会成为初选；但是，在其他两台机器变得不可访问的情况下，您的应用程序将能够向报告服务器发出读取请求。不言而喻，在这样的事件中你的报道应该被暂停。

您的报告代码将如下所示(这次用 Python 编写):

```
from pymongo import MongoReplicaSetClient
from pymongo.read_preferences import ReadPreference

rep_set = MongoReplicaSetClient(
    'Kusanagi.local:29017,Kusanagi.local:29018,Kusanagi.local:29019',
    replicaSet = 'test',
    read_preference = ReadPreference.SECONDARY,
    tag_sets = [{'use':'reporting'}]
)
# check to ensure we're not running reporting against the sole remaining secondary
if rep_set.primary is not None:
    rep_set.my_application.users.aggregate(...)
```

上面只会向标记为`use: reporting`的辅助节点发送报告查询，如果没有可用的主节点，它会阻止运行。实际上，如果您找不到主要事件，您应该抛出异常并在升级代码中处理它们！更好的是，您的监控可以设置运行时可用的值，以便您可以分支，例如，`reporting_system.ok()`。

### 好处和注意事项

使用标签和读取首选项允许一定程度的灵活性，这是隐藏成员所不能实现的。

#### 可以很容易地添加报告实例

因为您的连接代码是声明性的，而不是特定于特定主机的，所以要为报告作业添加更多节点，只需添加并标记它们，如下所示:

```
PRIMARY> rs.add({_id:3, host:"Kusanagi.local:29020", priority:0, tags:{'use':'reporting'}})
```

您现有的代码将利用新的容量，副本集将继续运行*,而不会触发选举和断开您的客户机。*

#### 可以移动或删除报告实例

如果您需要在紧要关头向其他作业提供读取带宽，可以移动甚至删除报告标记。像这样的重新配置将触发一次选举，并断开您所有客户端的连接，但这并不比任何其他选项更糟糕。**注意:通过将生产读取分布到辅助节点来增加一般容量是一种反模式。这只是应急措施。**

#### 一些驱动程序需要手动同步

例如，Ruby 驱动程序(从 1.9.2 开始)不刷新它的副本集视图，除非客户端被[明确初始化为用`refresh_mode: :sync`刷新](http://api.mongodb.org/ruby/1.9.2/Mongo/MongoReplicaSetClient.html#initialize-instance_method)。检查您的驱动程序文档。

## 结论

自从 MongoDB 之前推出以来，简单的复制设置一直是我最喜欢的操作方面之一，当时它使 MySQL 复制看起来像是石器时代的东西。当时还有点粗糙，但已经真正形成了自己的风格。无论您使用标记集还是隐藏成员，在 MongoDB 的复制特性上构建报告基础设施都可以简化操作，让您专注于构建优秀的应用程序。