# [ADO.NET](index.md)
# [ADO.NET 新增功能](whats-new.md)
# [ADO.NET 概述](ado-net-overview.md)
## [ADO.NET 体系结构](ado-net-architecture.md)
## [ADO.NET 技术选项和准则](ado-net-technology-options-and-guidelines.md)
## [LINQ 和 ADO.NET](linq-and-ado-net.md)
## [.NET framework 数据提供程序](data-providers.md)
## [ADO.NET 数据集](ado-net-datasets.md)
## [在 ADO.NET 中的并行执行](side-by-side-execution.md)
## [ADO.NET 代码示例](ado-net-code-examples.md)
# [保证 ADO.NET 应用程序的安全](securing-ado-net-applications.md)
## [安全性概述](security-overview.md)
## [安全数据访问](secure-data-access.md)
## [保护客户端应用程序](secure-client-applications.md)
## [代码访问安全性和 ADO.NET](code-access-security.md)
## [隐私和数据安全](privacy-and-data-security.md)
# [ADO.NET 中的数据类型映射](data-type-mappings-in-ado-net.md)
## [SQL Server 数据类型映射](sql-server-data-type-mappings.md)
## [OLE DB 数据类型映射](ole-db-data-type-mappings.md)
## [ODBC 数据类型映射](odbc-data-type-mappings.md)
## [Oracle 数据类型映射](oracle-data-type-mappings.md)
## [浮点数字](floating-point-numbers.md)
# [在 ADO.NET 中检索和修改数据](retrieving-and-modifying-data.md)
## [连接到数据源](connecting-to-a-data-source.md)
### [建立连接](establishing-the-connection.md)
### [连接事件](connection-events.md)
## [连接字符串](connection-strings.md)
### [连接字符串生成器](connection-string-builders.md)
### [连接字符串和配置文件](connection-strings-and-configuration-files.md)
### [连接字符串语法](connection-string-syntax.md)
### [保护连接信息](protecting-connection-information.md)
## [连接池](connection-pooling.md)
### [SQL Server 连接池 (ADO.NET)](sql-server-connection-pooling.md)
### [OLE DB、 ODBC 和 Oracle 连接池](ole-db-odbc-and-oracle-connection-pooling.md)
## [命令和参数](commands-and-parameters.md)
### [执行命令](executing-a-command.md)
### [配置参数和参数数据类型](configuring-parameters-and-parameter-data-types.md)
### [使用 Commandbuilder 生成命令](generating-commands-with-commandbuilders.md)
### [从数据库获取单一值](obtaining-a-single-value-from-a-database.md)
### [使用命令修改数据](using-commands-to-modify-data.md)
#### [更新数据源中的数据](updating-data-in-a-data-source.md)
#### [执行目录操作](performing-catalog-operations.md)
## [Dataadapter 和 Datareader](dataadapters-and-datareaders.md)
### [使用 DataReader 检索数据](retrieving-data-using-a-datareader.md)
### [从 DataAdapter 填充数据集](populating-a-dataset-from-a-dataadapter.md)
### [DataAdapter 参数](dataadapter-parameters.md)
### [将现有约束添加到数据集](adding-existing-constraints-to-a-dataset.md)
### [DataAdapter 数据表和 DataColumn 映射](dataadapter-datatable-and-datacolumn-mappings.md)
### [通过查询结果分页](paging-through-a-query-result.md)
### [使用 DataAdapter 更新数据源](updating-data-sources-with-dataadapters.md)
### [处理 DataAdapter 事件](handling-dataadapter-events.md)
### [使用 Dataadapter 执行批处理操作](performing-batch-operations-using-dataadapters.md)
## [事务和并发性](transactions-and-concurrency.md)
### [本地事务](local-transactions.md)
### [分布式的事务](distributed-transactions.md)
### [System.Transactions 与 SQL Server 的集成](system-transactions-integration-with-sql-server.md)
### [开放式并发](optimistic-concurrency.md)
## [检索标识或自动编号值](retrieving-identity-or-autonumber-values.md)
## [检索二进制数据](retrieving-binary-data.md)
## [使用存储过程修改数据](modifying-data-with-stored-procedures.md)
## [检索数据库架构信息](retrieving-database-schema-information.md)
### [GetSchema 和架构集合](getschema-and-schema-collections.md)
### [架构限制](schema-restrictions.md)
### [通用架构集合](common-schema-collections.md)
### [SQL Server 架构集合](sql-server-schema-collections.md)
### [Oracle 架构集合](oracle-schema-collections.md)
### [ODBC 架构集合](odbc-schema-collections.md)
### [OLE DB 架构集合](ole-db-schema-collections.md)
## [DbProviderFactories](dbproviderfactories.md)
### [工厂模型概述](factory-model-overview.md)
### [获取 DbProviderFactory](obtaining-a-dbproviderfactory.md)
### [DbConnection、 DbCommand 和 DbException](dbconnection-dbcommand-and-dbexception.md)
### [使用 DbDataAdapter 修改数据](modifying-data-with-a-dbdataadapter.md)
## [在 ADO.NET 中的数据跟踪](data-tracing.md)
## [性能计数器](performance-counters.md)
## [异步编程](asynchronous-programming.md)
## [SqlClient 流支持](sqlclient-streaming-support.md)
## [LINQ to DataSet](linq-to-dataset.md)
### [入门](getting-started-linq-to-dataset.md)
#### [LINQ to DataSet 概述](linq-to-dataset-overview.md)
#### [数据加载到数据集](loading-data-into-a-dataset.md)
#### [下载示例数据库](downloading-sample-databases-linq-to-dataset.md)
#### [如何： 在 Visual Studio 中创建 LINQ to DataSet 项目](how-to-create-a-linq-to-dataset-project-in-vs.md)
### [编程指南](programming-guide-linq-to-dataset.md)
#### [在 LINQ to DataSet 查询](queries-in-linq-to-dataset.md)
#### [查询数据集](querying-datasets-linq-to-dataset.md)
##### [单表查询](single-table-queries-linq-to-dataset.md)
##### [跨表查询](cross-table-queries-linq-to-dataset.md)
##### [查询类型化数据集](querying-typed-datasets.md)
#### [比较 Datarow](comparing-datarows-linq-to-dataset.md)
#### [从查询创建数据表](creating-a-datatable-from-a-query-linq-to-dataset.md)
#### [如何： 实现 CopyToDataTable<T>泛型类型 T 不是 DataRow](implement-copytodatatable-where-type-not-a-datarow.md)
#### [泛型字段和 SetField 方法](generic-field-and-setfield-methods-linq-to-dataset.md)
#### [数据绑定和 LINQ to DataSet](data-binding-and-linq-to-dataset.md)
##### [创建 DataView 对象](creating-a-dataview-object-linq-to-dataset.md)
##### [使用 DataView 进行筛选](filtering-with-dataview-linq-to-dataset.md)
##### [使用 DataView 进行排序](sorting-with-dataview-linq-to-dataset.md)
##### [查询在 DataView 中的 DataRowView 集合](querying-the-datarowview-collection-in-a-dataview.md)
##### [DataView 性能](dataview-performance.md)
##### [如何： 将 DataView 对象绑定到 Windows 窗体 DataGridView 控件](how-to-bind-a-dataview-object-to-a-winforms-datagridview-control.md)
#### [调试 LINQ to DataSet 查询](debugging-linq-to-dataset-queries.md)
#### [安全性](security-linq-to-dataset.md)
#### [LINQ to DataSet 示例](linq-to-dataset-examples.md)
##### [查询表达式示例](query-expression-examples-linq-to-dataset.md)
###### [投影](query-expression-syntax-examples-projection-linq-to-dataset.md)
###### [限制](query-expression-syntax-examples-restriction-linq-to-dataset.md)
###### [分区](query-expression-syntax-examples-partitioning.md)
###### [排序](query-expression-syntax-examples-ordering-linq-to-dataset.md)
###### [元素运算符](query-expression-syntax-examples-element-operators.md)
###### [聚合运算符](query-expression-syntax-examples-aggregate-operators.md)
###### [联接运算符](query-expression-syntax-examples-join-operators.md)
##### [基于方法的查询示例](method-based-query-examples-linq-to-dataset.md)
###### [投影](method-based-query-syntax-examples-projection.md)
###### [分区](method-based-query-syntax-examples-partitioning-linq.md)
###### [排序](method-based-query-syntax-examples-ordering-linq-to-dataset.md)
###### [集运算符](method-based-query-syntax-examples-set-operators.md)
###### [转换运算符](method-based-query-syntax-examples-conversion-operators.md)
###### [元素运算符](method-based-query-syntax-examples-element-operators.md)
###### [聚合运算符](method-based-query-syntax-examples-aggregate-operators.md)
###### [Join](method-based-query-syntax-examples-join-linq-to-dataset.md)
##### [数据集特定的运算符示例](dataset-specific-operator-examples-linq-to-dataset.md)
# [实体数据模型](entity-data-model.md)
## [实体数据模型关键概念](entity-data-model-key-concepts.md)
## [实体数据模型： 命名空间](entity-data-model-namespaces.md)
## [实体数据模型： 基元数据类型](entity-data-model-primitive-data-types.md)
## [实体数据模型： 继承](entity-data-model-inheritance.md)
## [关联端](association-end.md)
## [关联端重数](association-end-multiplicity.md)
## [关联集](association-set.md)
## [关联集端](association-set-end.md)
## [关联类型](association-type.md)
## [复杂类型](complex-type.md)
## [实体容器](entity-container.md)
## [实体键](entity-key.md)
## [实体集](entity-set.md)
## [实体类型](entity-type.md)
## [facet](facet.md)
## [外键属性](foreign-key-property.md)
## [模型声明函数](model-declared-function.md)
## [模型定义函数](model-defined-function.md)
## [导航属性](navigation-property.md)
## [属性](property.md)
## [引用完整性约束](referential-integrity-constraint.md)
# [Oracle 和 ADO.NET](oracle-and-adonet.md)
## [系统要求](system-requirements-for-the-dotnet-data-provider-for-oracle.md)
## [Oracle Bfile](oracle-bfiles.md)
## [Oracle Lob](oracle-lobs.md)
## [Oracle REF Cursor](oracle-ref-cursors.md)
### [REF CURSOR 示例](ref-cursor-examples.md)
### [OracleDataReader 中的 REF CURSOR 参数](ref-cursor-parameters-in-an-oracledatareader.md)
### [从使用 OracleDataReader 的多个 REF Cursor 中检索数据](retrieving-data-from-multiple-ref-cursors.md)
### [填充数据集使用一个或多个 REF Cursor](filling-a-dataset-using-one-or-more-ref-cursors.md)
## [OracleTypes](oracletypes.md)
## [Oracle 序列](oracle-sequences.md)
## [Oracle 数据类型映射](oracle-data-type-mappings.md)
## [Oracle 分布式事务](oracle-distributed-transactions.md)
# [ADO.NET 实体框架](ef/)
# [SQL Server 和 ADO.NET](sql/)
# [数据集、数据表和数据视图](dataset-datatable-dataview/)
