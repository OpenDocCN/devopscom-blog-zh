# Redis 实验室扩展了内存数据库的范围

> 原文：<https://devops.com/redis-labs-extends-reach-of-in-memory-database/>

在其在线 [RedisConf 2021](https://redislabs.com/redisconf/) 活动中，Redis 实验室今天详细介绍了该公司的内存数据库将如何用于驱动实时应用程序，这些应用程序是大多数数字业务转型计划的核心。

Redis Labs 首席技术官兼联合创始人 Yiftach Shoolman 表示，Redis Labs 努力的核心是四项举措，以取代组织过去用来驱动面向批处理的应用程序流程的遗留数据库。

第三季度，Redis 数据库的[7.0 版将推出 redist，它提供了一个基于 Raft 共识算法的模块，使多个 Redis 服务器能够被一个应用程序使用，就好像它们是一个单一的、容错的逻辑集群。Shoolman 说，这种能力将使 IT 团队能够将 Redis 服务器分布在更靠近分布式应用程序使用数据的地方，而不会导致数据库之间的任何冲突。](https://www.businesswire.com/news/home/20210420005398/en/Redis-Labs-Ushers-the-Real-Time-Era-with-Redis-as-a-Data-Platform)

与此同时，Redis 正在扩展其主动-主动技术，使集成数据模型的部署方式允许分布式应用程序尽可能靠近数据的创建和消费点。

最后，RediSearch 正在更新，以包括对使用嵌套文档模型的 JSON 应用程序中的索引功能的支持，而 RedisAI 功能将为人工智能(AI)应用程序添加一个推理引擎，该引擎可以用作一个功能库，通过它可以管理应用程序中 AI 模型的部署。Shoolman 指出，这种方法也有望显著提高人工智能应用的整体性能。

历史上，Redis 内存数据库因其为开发人员提供的缓存功能而闻名。然而，Shoolman 指出，使用 Redis 数据库的组织中有 66%将它用于其他用例。Shoolman 补充说，随着通常配置有自己的数据库的微服务变得越来越普遍，内存数据库平台的采用只会增加。

这些微服务中有许多是在数字业务转型项目的背景下使用的。组织逐渐认识到的问题是，大多数流程需要近乎实时地运行。Shoolman 说，这一要求最终将推动更多的组织部署基于分布式数据库运行在内存中的[数据库](https://devops.com/?s=database)，该数据库对应用程序来说是一个逻辑实体。

Redis 的核心是一个数据存储，它支持字符串、散列、列表、集合、带有范围查询的排序集合、位图、超级日志、地理空间索引和流等结构。在其他功能中，它包括对内置复制、Lua 脚本、事务和不同级别的持久性的支持。该公司声称，核心 Redis 数据库在过去九年中已被下载了 150 万次。

在此基础上，Redis 实验室提供了在大规模应用环境中部署和管理 Redis 的工具。最近，Redis Labs [筹集了额外的 1 亿美元融资](https://redislabs.com/press/redis-labs-110-million-series-g-led-by-tiger-global/)，使其估值超过 20 亿美元。该公司现在声称拥有 8，000 多名付费客户，过去三年的销售复合年增长率为 54%。

很难说 Redis 数据存储会在多大程度上取代传统的数据库平台。然而，有一件事是肯定的，内存中运行着更多的数据库，在许多情况下，不再需要传统的关系数据库。