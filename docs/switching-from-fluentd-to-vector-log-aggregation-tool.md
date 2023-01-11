# 从 FluentD 切换到矢量日志聚合工具

> 原文：<https://devops.com/switching-from-fluentd-to-vector-log-aggregation-tool/>

日志文件对于[数据分析](https://devops.com/?s=DataOps)过程极其重要，因为它们包含有关操作系统、应用程序、服务器或设备内的使用模式、活动和操作的基本信息。这些数据与组织中的许多使用案例相关，包括资源管理、应用程序故障排除、法规遵从性、SIEM 以及业务分析和营销洞察。为了管理这些用例创建的日志并利用这些丰富的数据，日志聚合工具使组织能够系统地收集和标准化日志文件。然而，选择正确的工具可能相当具有挑战性。

这个博客将详细介绍和比较流行的开源日志聚合工具 fluentD 和 Vector。

### 流体配置和效率计算

当使用像 Kubernetes 这样的编排工具来部署容器或其他 API 资源时，需要一个日志聚合器来存储云平台中的 pod 或节点日志。对于特定的需求，fluentD 被用作日志聚合器工具，以将 K8s pod 日志推送到云存储桶，其示例配置如下所示:

```
<match kubernetes.**>

@type <cloud platform name>

project <project name in cloud platform>

keyfile <credential json to access the cloud storage> bucket <cloud storage bucket name> object_key_format <name for the file to be used>

path <file prefix/path where the file have to be stored>

<buffer tag,time>

@type file

path /var/log/fluent/gcs timekey 1m timekey_wait 30 timekey_use_utc true flush_thread_count 16 flush_at_shutdown true flush_mode interval flush_interval 1 chunk_limit_size 10MB retry_max_interval 30 retry_wait 60

</buffer> <format>

@type json </format>

</match>
```

使用该系统，fluentD 仅将总日志的 47.62%推送到云存储。由于损失超过 50%，因此对配置进行了更改。在大多数变化中，效率在 40%到 50%之间，一整天的最高效率平均为 67%。下面是所做的一些更改，以及推送到云存储的日志的百分比:

```
<buffer tag,time> @type file

path /var/log/fluent/gcs timekey 1m timekey_wait 30 timekey_use_utc true flush_thread_count 16 flush_at_shutdown true retry_max_interval 60 retry_wait 30

</buffer> Efficiency:- 46.32%

<buffer tag,time> @type file

path /var/log/fluent/gcs timekey 1m timekey_wait 30 timekey_use_utc true flush_thread_count 16 flush_at_shutdown true

</buffer> Efficiency:- 49.89%

<buffer tag,time>

@type file

path /var/log/fluent/gcs timekey 10m timekey_wait 0 timekey_use_utc true flush_at_shutdown true

</buffer> Efficiency:- 37%

<buffer tag,time> @type file

path /var/log/fluent/gcs timekey 30 timekey_wait 0 timekey_use_utc true flush_thread_count 15 flush_at_shutdown true

</buffer> Efficiency:- 60.88%

<buffer tag,time> @type file

path /var/log/fluent/gcs timekey 1 timekey_wait 0 timekey_use_utc true flush_thread_count 16 flush_at_shutdown true flush_mode immediate

</buffer> Efficiency:- 66.77%
```

### 向量部署、配置和最终效率

为了进一步改进这一点，还考虑了 Datadog 的开源矢量工具。该工具适用于配置与 fluentD 相似的 K8s 设置，安装在节点中。

Helm 命令用于在其虚拟机中克隆官方存储库；如下所述更改了配置，并将其作为代理安装。Vector 有两种工作模式:代理和聚合器。代理是将日志/事件从源推到目的地的普通模式，而聚合器用于转换和传送由其他代理收集的数据(在本例中是 Vector)。

该工具的安装需要本地机器中的 Helm 存储库来获取源代码。因此，在 K8s 集群中安装 Vector 之前，以下命令按顺序运行:

```
helm repo add vector https://helm.vector.dev (Adding vector repo to helm list)

helm repo update (Updating the helm repos)

helm fetch –untar vector/vector . (command to clone the repository to local machine)

Configuration:-

data_dir: /vector-data-dir

sources:

<Custom source id>:

type: kubernetes_logs (because we are using kubernetes as our source)

exclude_paths_glob_patterns: <Array of directories which has be excluded when collecting the logs from the nodes> (Optional)

sinks:

<Custom sink id>:

type: <Destination cloud storage>

inputs: <Array of source id’s from where log has to be pushed>

bucket: <Bucket name of cloud storage>

key_prefix: <Path inside the bucket where the logs has to collected> (Optional) encoding:

codec: <Encoding of the log file> (Optional) Command to install the Vector:-

helm install vector . –namespace vector
```

在开发环境中部署 Vector 并进行测试后，效率大约为 100%,损失可以忽略不计。然后切换到 Vector 并部署到生产环境中。Vector 每秒可以传送 100，000 个事件或日志，与其他日志聚合工具相比，这是一个非常高的吞吐率。即使在 Kubernetes 生产集群中，Vector 也能够实现 99.98-100%的效率。

要了解更多关于 [DataOps](https://www.sigmoid.com/data-devops/) 如何通过实时日志记录和监控实现高性能数据管道，请观看本视频[。](https://www.youtube.com/watch?v=BvfmPFtAKyo)