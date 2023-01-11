# 从微软 Azure 到 AWS 上的雪花的数据库迁移:第 2 部分

> 原文：<https://devops.com/database-migration-from-microsoft-azure-to-snowflake-on-aws-part-2/>

在这个博客系列的 [第一部分](https://devops.com/database-migration-from-microsoft-azure-to-snowflake-on-aws-part-1/) 中，我们通过利用 Azure 数据工厂、调整数据工厂管道的性能、 u 调用拼花文件和增加计算能力来查看我们的迁移方法。

在这篇博客中，我们将探讨迁移过程中遇到的一些挑战、节约成本的措施以及我们的数据验证方法。

## 遇到的挑战

*   如果列名包含空格或特殊字符，则表的数据工厂导出失败。在这种情况下，列名使用别名(用下划线代替空格),查询方法用作源。
*   列数据类型“Geography”的数据工厂导出失败，必须转换为 *varchar* ，然后导出到 Blob。
*   SQL server 中的一些列名是 Snowflake 中的关键字，这不允许它迁移。例如，“LOCALTIME”在 SQL 中是一个列名，但在 Snowflake 中也是一个关键字，在创建 Snowflake 表时使用引号作为转义符("")来表示。
*   在摄取到雪花的过程中，平面文件以表命名，根据名称模式列出文件。例如，如果我们想列出表名为 test_1 的文件，雪花将列出所有以名称 test_1 开头的文件。务必确保每个文件名都是唯一的。
*   如果要接收的文件与表不符，Snowflake 不会返回任何错误消息或警告。它只是接收文件，并在没有找到列映射的地方放置 NULL。
*   创建表时，如果列名有空格，则使用转义字符，以便保留相同的空格。但是对于这种列的摄取，平面文件中的列映射将与源查询中使用的别名相同。
*   Snowflake 不支持触发器和计算列，在创建表时必须将其删除。
*   此外，雪花模式中不存在的数据类型必须更改，记住数据的正确性。

## 节约成本的行动

*   使用拼花文件有助于实现高达 75%的压缩率。800GB 的数据在多个文件中被压缩到 234GB，从而降低了 Blobs 的存储成本。
*   详细的概念验证和分析发现，雪花摄入对于小型中型餐桌和中型大型餐桌来说是最佳的，这样可以控制雪花的成本。
*   由于使用了 Azure VM 的计算能力，自托管 IR 节省了数据管道运营成本。

## 成本估算

![](img/9f9bf56617f427674e8f4cb9eee7bf61.png)

![](img/4905edf22edf0605c41d3dea06ab3eea.png)

## 数据有效性

该项目的关键部分是确保在迁移过程中维护数据的完整性和正确性。作为标准 [数据操作](https://www.sigmoid.com/data-devops/) 最佳实践的一部分，执行了彻底的数据验证活动，以确保数据保持有意义，并继续用于推动业务决策。

数据验证的方法有两种:

在第一种方法中，列出了 SQL server 中属于 [db 迁移](https://www.sigmoid.com/cloud-migration/) 的所有不同数据类型，并针对每种数据类型在一行中随机采样。从雪花中获取相同的行并进行匹配。

![](img/25243128231fdcb60a12a7d71a02066f.png)

**基于数据类型的表格列表**

`select table_catalog,table_schema,table_name,COLUMN_NAME,* from
INFORMATION_SCHEMA.COLUMNS
where DATA_TYPE = 'money' and TABLE_NAME not like 'sys%'`

在此验证过程中发现了如下所示的问题，并针对该数据类型的所有实例进行了更正。

![](img/bd93dbe8551e46f8302e8f20d5c5ce85.png)

第二种方法包括编写一个自动化脚本，它实现了以下结果(更多细节可以在 [这里](https://github.com/AmolGawas/DataValidation_SnowFlake.git) )找到:

*   脚本触及了每个数据库的每个表
*   从两侧随机抽取一组五个记录并进行匹配
*   如果这些表是空的，则被记录为没有记录的表
*   如果样本集与脚本不匹配，它会与样本集争论，并一次一列地对它们进行排序。如果样本与脚本匹配，就会被记录下来。这种争论解决了前 n 列有重复记录的情况
*   任何失败的验证尝试都可以在生成的日志报告中看到:

开始对表:Test1 进行验证

—-->表 Test1 的验证通过

开始对表:Test2 进行验证

—-->表 Test2 的验证通过

开始对表:Test3 进行验证

—-->表中有 0 条记录

开始对表:Test4 进行验证

—-->表 Test4 的验证失败

开始对表:Test5 进行验证

—-->表 Test5 的验证通过

============报告=============

#扫描的表总数:5

包含 0 条记录的表数:1

#通过:3

失败次数:1

#百分比 60.5556123