---
title: 使用 GROUPBY 数据源对记录进行分组和聚合计算
description: 本文介绍如何在电子报告 (ER) 中使用 GROUPBY 类型数据源。
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 0e520705d2441ead5a68ec3284db74999b3d90b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277563"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>使用 GROUPBY 数据源对记录进行分组和聚合计算

[!include[banner](../includes/banner.md)]

在配置 [电子报告 (ER)](general-electronic-reporting.md) 模型映射或格式时，您可以 [添加](#AddMmDataSource2) **GroupBy** 类型的必需数据源。

在设计时，**GroupBy** 数据源被配置为识别以下元素：

- 包含将在运行时分组的记录的[基础数据源](#BaseDataSource)
- 基础数据源的[分组字段](#GroupingFields)，将在运行时用于记录分组
- 指定在运行时将为每个发现的组完成的聚合计算的[聚合函数](#AggregateFunctions)

在运行时，配置的 **GroupBy** 数据源将分组字段中具有相同值的记录分组，然后返回记录列表。 每个记录表示一个组。 对于每个组，数据源将公开初始记录分组依据的字段值、计算的聚合函数的值以及属于该组的基础数据源的记录列表。

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>聚合函数

在运行时，将对每组记录执行每个聚合计算。 此计算通过使用在 **GroupBy** 类型的可编辑数据源中选择用于分组的数据源记录中的单个字段或表达式的值来完成。 当前支持以下聚合函数：

- **AVG** – 此函数返回组中值的平均值。 只能用于数字字段。
- **COUNT** – 此函数返回组中找到的项目数。
- **Min** – 此函数返回组中值中的最小值。
- **Max** – 此函数返回组中值中的最大值。
- **SUM** – 此函数返回组中所有值的总和。 只能用于数字字段。

## <a name="execution-location"></a><a name="ExecutionLocation"></a>执行位置

当您编辑 **GroupBy** 数据源并指定包含必须分组的记录的基础数据源时，系统会自动检测最有效的 [位置](#ExecutionLocation)来执行该 **GroupBy** 数据源。 如果基础数据源 [可查询](er-functions-list-filter.md#usage-notes)（即是否可以在数据库级别运行），应用程序数据库也将被指定为可编辑 **GroupBy** 数据源的执行位置。 否则，应用程序服务器内存将被指定为执行位置。

您可以通过选择适用于配置的数据源的位置手动更改自动检测到的执行位置。 如果所选执行位置不适用，将会在设计时间引发[验证错误](er-components-inspections.md#i5)。

> [!TIP]
> 我们建议您使用数据库位置对公开大量记录的数据源进行分组。

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>内存消耗

默认情况下，如果 **GroupBy** 数据源在内存中运行，应用程序服务器内存将用于将属于每个已发现组的基础数据源的记录存储为单个组的记录。 为帮助减少内存消耗，如果 **GroupBy** 数据源被配置为仅计算聚合函数并且在运行时不使用组的记录，您可以禁止记录存储。 要以这种方式减少内存消耗，请在 **功能管理** 工作区启用 **当记录分组仅用于计算聚合时，降低电子报告中的内存使用量** 功能。

## <a name="alternatives"></a><a name="Alternatives"></a>备选方案

相似的聚合可以使用[不同](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions)类型的数据源或 ER 内置函数计算。

若要了解有关此功能的详细信息，请完成以下示例。

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>示例：使用 GROUPBY 数据源进行聚合计算和记录分组

此示例显示系统管理员或电子报告功能顾问角色的用户如何配置具有 **GROUPBY** 数据源的 ER 模型映射，该数据源用于计算聚合函数和分组记录。 生成内部统计申报时，此模型映射用于打印控制报表。 该报表可让您查看报告的内部统计交易记录。

在 Microsoft Dynamics 365 Finance 中，本示例中的过程可以在 **DEMF** 公司完成。 

### <a name="prepare-sample-data"></a>准备示例数据

确保您在 **内部统计** 页面上有用于报告的内部统计交易。 您必须有不同运输代码的交易记录，因为在此示例中您将按 **传输** 字段对交易记录进行分组。

![在内部统计页面上准备内部统计交易记录。](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>配置 ER 框架

按照[配置电子报告框架](er-quick-start2-customize-report.md#ConfigureFramework)中的步骤设置最低限度的电子报告参数集。 在开始使用 ER 框架设计 ER 模型映射之前，您必须完成此设置。

### <a name="import-the-standard-er-format-configuration"></a>导入标准电子报告格式配置

按照[导入标准电子报告格式配置](er-quick-start2-customize-report.md#ImportERSolution1)中的步骤将标准电子报告配置添加到您当前的 Dynamics 365 Finance 实例。 从存储库导入 **内部统计模型** 配置的版本 1。

### <a name="create-a-custom-data-model-configuration"></a>创建自定义数据模型配置

按照 [添加自定义数据模型配置](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration)中的步骤，手动添加一个新的从导入的 **内部统计模型** 配置派生的 **内部统计模型(Litware)** ER 数据模型配置。

### <a name="configure-a-custom-data-model-component"></a>配置自定义数据模型组件

按照以下步骤对派生的 **内部统计模型(Litware)** 数据模型进行必需的更改，以可以使用它来公开具有所需详细信息的传输代码。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，选择 **内部统计模型(Litware)**。
3. 选择 **设计器**。
4. 在 **数据模型设计器** 页面的模型树中，选择 **内部统计**。
5. 选择 **新建** 为所选 **内部统计** 节点添加新的嵌套节点。 在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 在 **名称** 字段中，输入 **Transport**。
    2. 在 **物料类型** 字段中，选择 **记录列表**。
    3. 选择 **添加** 添加新节点。

6. 选择 **新建** 为您刚才添加的 **传输** 节点添加新的嵌套节点。 在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 在 **名称** 字段中，输入 **Code**。
    2. 在 **物料类型** 字段中，选择 **字符串**。
    3. 选择 **添加** 添加新节点。

7. 选择 **新建** 为 **传输** 节点添加另一个新的嵌套节点。 在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 在 **名称** 字段中，输入 **TotalInvoicedAmount**。
    2. 在 **物料类型** 字段中，选择 **实际**。
    3. 选择 **添加** 添加新节点。

8. 选择 **新建** 为 **传输** 节点添加另一个新的嵌套节点。 在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 在 **名称** 字段中，输入 **NumberOfTransactions**。
    2. 在 **物料类型** 字段中，选择 **整数**。
    3. 选择 **添加** 添加新节点。

9. 选择 **新建** 为 **传输** 节点添加另一个新的嵌套节点。 在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 在 **名称** 字段中，输入 **Transaction**。
    2. 在 **物料类型** 字段中，选择 **记录列表**。
    3. 选择 **添加** 添加新节点。

10. 对于您刚才添加的 **Transaction** 节点，在 **节点** 快速选项卡上，选择 **切换项引用**。
11. 在 **切换项引用** 对话框中，在数据模型树中选择 **CommodityRecord**。 然后选择 **确定**。

![ER 数据模型设计器中配置的数据模型。](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>完成自定义数据模型的设计

按照 [完成数据模型的设计](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration)中的步骤完成派生的 **内部统计模型(Litware)** 数据模型的设计。

### <a name="create-a-new-model-mapping-configuration"></a>创建新模型映射配置

按照 [创建新模型映射配置](er-quick-start1-new-solution.md#CreateModelMapping)中的步骤为派生的 **内部统计模型 (Litware)** 配置手动添加新的 **内部统计示例映射** ER 模型映射配置。

### <a name="add-a-new-model-mapping-component"></a>添加新模型映射组件

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，展开 **内部统计模型** 配置。
3. 选择 **内部统计示例映射** 配置。
4. 选择 **设计器** 来打开映射列表。
5. 选择 **删除** 将现有映射组件删除。
6. 选择 **新建** 添加新的映射组件。
7. 在 **定义** 字段中，选择 **内部统计**。
8. 在 **名称** 字段中输入 **内部统计映射**。
9. 选择 **设计器** 配置新映射。

### <a name="design-the-added-model-mapping-component"></a>设计添加的模型映射组件

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>添加数据源以访问应用程序表

配置数据源以访问包含内部统计交易记录详细信息的应用程序表。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。
2. 在 **数据源** 窗格中，选择 **添加根** 添加将用于访问 **内部统计** 表的新数据源。 **内部统计** 表中的每个记录代表一个内部统计交易记录。
3. 在 **数据源属性** 对话框中，在 **名称** 字段中输入 **Transaction**。
4. 在 **表** 字段中，输入 **内部统计**。
5. 选择 **确定** 添加新数据源。

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>添加数据源以对内部统计交易记录进行分组

配置 **GroupBy** 数据源以对内部统计交易记录进行分组并计算聚合函数。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **函数\\分组依据**。
2. 在 **数据源** 窗格中，选择 **添加根** 添加将用于对内部统计交易记录进行分组并计算聚合函数的新数据源。
3. 在 **数据源属性** 对话框中，在 **名称** 字段中输入 **TransportRecord**。
4. 选择 **编辑分组依据** 配置分组条件。
5. 在 **编辑“分组依据”参数** 页上，在右侧窗格中的数据源列表中，选择 **交易记录** 数据源并将其展开。
6. 选择 **将字段添加到 \> 分组项目** 指示选择 **Transaction** 数据源作为配置的 **GroupBy** 数据源的<a name="BaseDataSource">基础数据源</a>。 **Transaction** 数据源的记录将被分组，该数据源的字段值将用于聚合函数的计算。
7. 选择 **Transaction\Transport** 字段，然后选择 **将字段添加到 \> 已分组字段**，指示基础数据源的 **传输** 字段被选为配置的 **GroupBy** 数据源的<a name="GroupingFields">分组条件</a>。 换言之，**Transaction** 数据源的记录将根据 **传输** 字段的值进行分组。 配置的 **GroupBy** 数据源的每个记录将表示已在基础数据源的记录中找到的一个传输代码。
8. 选择 **Transaction\AmountMST** 字段，然后按照以下步骤操作：

    1. 选择 **将字段添加到 \> 聚合字段** 指示将为此字段计算<a name="AggregateFunctions">聚合函数</a>。
    2. 在 **聚合** 窗格中，在已为所选 **Transaction\AmountMST** 字段添加的记录中，在 **方法** 字段中，选择 **Sum** 函数。
    3. 在 **名称** 可选字段中，输入 **TotalInvoicedAmount**。

    这些设置指定，对于每个传输组，将计算 **Transaction\AmountMST** 字段的总金额。

9. 选择 **Transaction\RecId** 字段，然后按照以下步骤操作：

    1. 选择 **将字段添加到 \> 聚合字段** 指示将为此字段计算聚合函数。
    2. 在 **聚合** 窗格中，在已为所选 **Transaction\RecId** 字段添加的记录中，在 **方法** 字段中，选择 **Count** 函数。
    3. 在 **名称** 可选字段中，输入 **NumberOfTransactions**。

    这些设置指定，对于每个传输组，将计算组中交易记录的数量。

10. 选择 **保存**。
11. 查看可编辑数据源的<a name="ExecutionLocation">执行</a>参数。 请注意，**自动检测** 已在 **执行位置** 字段中自动选择，**执行位置** 字段包含值 **SQL**。 这些设置指定选定的 **Transaction** 基础数据源当前是可查询的，您可以在数据库级别运行可编辑的 **GroupBy** 数据源。
12. 打开 **执行位置** 字段的查找可查看可用值列表。 请注意，您可以选择 **查询** 或 **在内存中** 来强制此 **GroupBy** 数据源在数据库级别或应用程序服务器内存中运行。
13. 选择 **保存**，然后关闭 **编辑“分组依据”参数** 页面。
14. 选择 **确定** 完成 **GroupBy** 数据源的设置。

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>将 GroupBy 数据源与数据模型字段绑定

将配置的数据源与数据模型的字段绑定，来指定在运行时如何使用应用程序数据填充数据模型。

1. 在 **模型映射设计器** 页的 **数据模型** 窗格中，展开 **传输** 节点。
2. 在 **数据源** 窗格中，展开 **TransportRecord** 数据源。
3. 添加绑定以公开已发现传输组的列表：

    1. 在 **数据模型** 窗格中，选择 **传输** 项。
    2. 在 **数据源** 窗格中，选择 **TransportRecord** 数据源。
    3. 选择 **绑定**。

4. 添加绑定以公开每个发现的传输组的传输代码：

    1. 选择 **Transport.Code** 数据模型项。
    2. 选择 **TransportRecord.grouped.TransportMode** 已分组字段。
    3. 选择 **绑定**。

5. 添加绑定以公开每个已发现运输组的已计算聚合函数的值：

    1. 选择 **Transport.NumberOfTransactions** 数据模型项。
    2. 选择 **TransportRecord.aggregated.NumberOfTransactions** 已聚合字段。
    3. 选择 **绑定**。
    4. 选择 **Transport.TotalInvoicedAmount** 数据模型项。
    5. 选择 **TransportRecord.aggregated.TotalInvoicedAmount** 已聚合字段。
    6. 选择 **绑定**。

6. 添加绑定以公开属于每个已发现传输组的交易记录：

    1. 选择 **Transport.Transaction** 数据模型项。
    2. 选择 **TransportRecord.lines** 字段。
    3. 选择 **绑定**。

    您可以继续为 **Transport.Transaction** 数据模型项和 **TransportRecord.lines** 数据源字段的嵌套项配置绑定，以在运行时公开属于每个已发现传输组的内部统计交易记录的详细信息。

![ER 模型映射设计器中配置的模型映射。](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>调试添加的模型映射组件

使用 [ER 数据源调试器](er-debug-data-sources.md)测试配置的模型映射。

1. 在 **模型映射设计器** 页面上，选择 **开始调试**。
2. 在 **调试数据源** 页面，在左侧窗格中，选择 **TransportRecord** 数据源，然后选择 **读取所有记录**。
3. 展开 **TransportRecord** 数据源，然后按照以下步骤操作：

    1. 选择 **TransportRecord.grouped.TransportMode** 数据源。
    2. 选择 **获取值**。 
    3. 选择 **TransportRecord.grouped.NumberOfTransactions** 数据源。
    4. 选择 **获取值**。 
    5. 选择 **TransportRecord.grouped.TotalInvoicedAmount** 数据源。
    6. 选择 **获取值**。 

4. 从右窗格中，选择 **全部展开**。

**TransportRecord** 数据源公开两个记录并提供两个传输代码。 对于每个传输代码，将计算交易记录数和开票总金额。

> [!NOTE]
> 当调用 **GroupBy** 数据源以优化数据库调用时，使用“懒惰读取”方法。 因此，**GroupBy** 数据源中的某些字段值仅在绑定到数据模型字段时才在 ER 数据源调试器中计算。

![“调试数据源”页面上的数据源调试结果。](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>计算组总计值时是否有计算总计的方法？

是。 要计算总计，请配置另一个 **GroupBy** 数据源，将您之前配置的 **GroupBy** 数据源用作基础数据源。 下图显示了 **GroupBy** 类型的 **Totals** 数据源，用于根据 **GroupBy** 类型的 **TransportRecord** 数据源的 **SUM** 聚合计算聚合 **SUM** 函数。

![ER 模型映射设计器中的 Totals 数据源。](./media/er-groupby-data-sources-configure-model-mapping2.png)

下图显示了 **Totals** 数据源调试的结果。

![“调试数据源”页面上的 Totals 数据源调试的结果。](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [调试已执行 ER 格式的数据源以分析数据流和转换](er-debug-data-sources.md)
- [使用电子报告格式的数据收集数据源](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
