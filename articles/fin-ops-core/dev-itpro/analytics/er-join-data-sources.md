---
title: 在 ER 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据
description: 本主题介绍如何在电子申报 (ER) 中使用 JOIN 类型数据源。
author: NickSelin
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: e872ff38d2115273fe76f5a2f54197c55cc7a2e0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565533"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>在电子申报 (ER) 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据

[!include[banner](../includes/banner.md)]

在配置电子申报 (ER) 模型映射或格式时，您可以 [添加](#review) **Join** 类型的必需数据源。 在设计时，将 **Join** 数据源配置为一组数据源，每个数据源都返回记录列表。 对于除第一个数据源外的每个数据源，您都需要定义必要条件以联接当前和先前数据源的记录。 在运行时，配置的 **Join** 类型的数据源[返回](#executeERformat)包含嵌套数据源记录中字段的记录的单个联接列表。

当前支持以下联接类型：

- 外部（左）联接：
    - 联接第一个（最左侧）数据源的所有记录，然后联接根据第二个（最右侧）数据源的配置条件记录进行的任何匹配。
- 内部（右）联接：
    - 仅联接第一个（最左侧）数据源的记录，并仅联接根据配置的条件相互匹配的第二个（最右侧）数据源的记录。

在配置的 **Join** 数据源中，当所有数据源均为 **表记录** 类型时，可以使用单个 SQL 语句[在数据库级别执行](#analyze) Join 数据源的执行。 此语句将减少数据库调用的次数，从而提高模型映射的性能。 否则，将在内存中执行 **Join 数据** 源。

> [!NOTE]
> 目前尚不支持在 ER 表达式中使用 **VALUEIN** 函数来指定联接类型为 Join 的数据源中的记录的条件。 有关此函数的更多详细信息，请访问[电子申报中的配方设计器](general-electronic-reporting-formula-designer.md)页面。

若要了解有关此功能的详细信息，请完成本主题中的示例。

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>示例：在 ER 模型映射中使用 JOIN 数据源

以下步骤说明了系统管理员或电子申报开发人员如何配置电子申报 (ER) 模型映射，以通过使用 **Join** 类型的数据源来一次从多个应用程序表中获取数据，从而提高数据访问性能。 Dynamics 365 Finance 或 Regulatory Configuration Services (RCS) 的任何公司都可以执行这些步骤。

### <a name="prerequisites"></a>先决条件

要完成本主题中的示例，您必须有权使用以下服务之一（具体取决于哪个服务用于完成这些步骤）：

**访问 Finance 的以下其中一个角色：**

- 电子申报开发人员
- 电子申报功能顾问
- 系统管理员

**访问 RCS 的以下其中一个角色：**

- 电子申报开发人员
- 电子申报功能顾问
- 系统管理员

您还必须首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。

事先，您还必须从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=000000)下载并在本地保存以下示例 ER 配置文件：

| **内容描述**  | **文件名**   |
|--------------------------|-----------------|
| 示例 **ER 数据模型** 配置文件，用作示例的数据源。| [Model to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| 示例 **ER 模型映射** 配置文件，为示例实现 ER 数据模型。 | [Mapping to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| 示例 **ER 格式** 配置文件。 此文件介绍用于为示例填充 ER 格式组件的数据。 | [Format to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>启用配置提供程序

1. 在 Web 浏览器的第一个会话中访问 Finance 或 RCS。
2. 转到 **组织管理 \> 工作区 \> 电子申报**。
3. 在 **本地化配置** 页上的 **配置提供程序** 部分中，确保列出了示例公司 [Litware, Inc.](http://www.litware.com) 的配置提供程序，并将其标记为 **活动状态**。 如果没有看到此配置提供程序，请执行[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。

    ![电子申报工作区](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>导入示例 ER 配置文件

1. 选择 **申报配置**。
2. 导入 ER 数据模型配置文件。
    1. 选择 **交换**。
    2. 选择 **从 XML 文件加载**。
    3. 选择 **浏览** 找到 **Model to learn JOIN data sources.version.1.1.xml** 文件。
    4. 选择 **确定**。
3. 导入 ER 模型映射配置文件。
    1. 选择 **交换**。
    2. 选择 **从 XML 文件加载**。
    3. 选择 **浏览** 找到 **Mapping to learn JOIN data sources.version.1.1.xml** 文件。
    4. 选择 **确定**。
4. 导入 ER 格式配置文件。
    1. 选择 **交换**。
    2. 选择 **从 XML 文件加载**。
    3. 选择 **浏览** 找到 **Format to learn JOIN data sources.version.1.1.xml** 文件。
    4. 选择 **确定**。
5. 在配置树中，展开 **用于了解 JOIN 数据源的模型** 项目以及其他模型项目（如果有）。
6. 观察树中的 ER 配置列表以及 **版本** 快速选项卡上的版本详细信息 – 它们将用作示例报表的数据源。

    ![电子申报配置页面](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>打开执行跟踪选项

1. 选择 **配置**。
2. 选择 **用户参数**。
3. 设置执行跟踪参数，如下面的屏幕截图所示。

    ![电子申报用户参数页面](./media/GER-JoinDS-Parameters.PNG)

    启用这些参数后，对于导入的 ER 格式文件的每次执行，都会生成执行跟踪。 使用生成的执行跟踪的详细信息，您可以分析 ER 格式和 ER 模型映射组件的执行。 请访问[跟踪 ER 格式的执行情况以解决性能问题](trace-execution-er-troubleshoot-perf.md)页面，了解有关 ER 执行跟踪功能的更多详细信息。

### <a name="review-er-model-mapping-part-1"></a>查看 ER 模型映射（第 1 部分）

查看 ER 模型映射组件的设置。 该组件配置为访问有关 ER 配置版本、配置详细信息和配置提供程序的信息，而无需使用 **Join** 类型的数据源。

1. 选择 **用于了解 JOIN 数据源的映射** 配置。
2. 选择 **设计器** 来打开映射列表。
3. 选择 **设计器** 查看映射详细信息。
4. 选择 **显示详细信息**。
5. 在配置树中，展开 **Set1** 和 **Set1.Details** 数据模型项目：

    1. 绑定 **Details: Record list = Versions** 表示 **Set1.Details** 项目已绑定到返回 **ERSolutionVersionTable** 表的记录的 **Versions** 数据源。 此表的每个记录代表一个单独版本的 ER 配置。 此表的内容显示在 **配置** 页面上的 **版本** 快速选项卡中。
    2. 绑定 **ConfigurationVersion: String = @.PublicVersionNumber** 表示每个 ER 配置版本的公共版本的值均取自 **ERSolutionVersionTable** 表的 **PublicVersionNumber** 字段，并放置到 **ConfigurationVersion** 项目中。
    3. 绑定 **ConfigurationTitle: String = @.'>Relations'.Solution.Name** 表示 ER 配置的名称取自 **ERSolutionTable** 表的 **名称** 字段，该表通过使用 **ERSolutionVersionTable** 和 **ERSolutionTable** 表之间的多对一关系 (**'>Relations'**) 评估。 当前应用程序实例的 ER 配置的名称显示在 **配置** 页面上的配置树中。
    4. 绑定 **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** 意味着具有当前配置的配置提供程序的名称取自 **ERVendorTable** 表的 **名称** 字段，该表通过使用 **ERSolutionTable** 和 **ERVendorTable** 表之间的多对一关系进行评估。 ER 配置提供程序的名称显示在 **配置** 页面上的配置树中，位于每个配置的页标题上。 ER 配置提供程序的完整列表可在 **组织管理 \> 电子申报 \> 配置提供程序** 表页面上找到。

    ![ER 模型映射设计器页面](./media/GER-JoinDS-Set1Review.PNG)

6. 在配置树中，展开 **Set1.Summary** 数据模型项目：

    1. 绑定 **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** 表示 **Set1.Summary.VersionsNumber** 项目绑定到 **GroupBy** 类型的 **VersionsSummary** 数据源的 **VersionsNumber** 合并字段，该类型配置为通过 **Versions** 数据源返回 **ERSolutionVersionTable** 表的记录数。

    ![GROUPBY 数据源参数页面](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. 关闭该页面。

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a>查看 ER 模型映射（第 2 部分）

查看 ER 模型映射组件的设置。 该组件配置为使用 **Join** 类型的数据源访问有关 ER 配置版本、配置详细信息和配置提供程序的信息。

1. 在配置树中，展开 **Set2** 和 **Set2.Details** 数据模型项目。 绑定 **Details: Record list = Details** 表示 **Set2.Details** 项目绑定到配置为 **Join** 类型的数据源的 **Details** 数据源。

    ![ER 模型映射设计器页面](./media/GER-JoinDS-Set2Review.PNG)

    可以通过选择 **Functions\Join** 数据源来添加 **Join** 数据源：

    ![ER 模型映射设计器页面](./media/GER-JoinDS-AddJoinDS.PNG)

2. 选择 **Details** 数据源。
3. 在 **数据源** 窗格中选择 **编辑**。
4. 选择 **编辑联接**。
5. 选择 **显示详细信息**。

    ![JOIN 数据源参数页面](./media/GER-JoinDS-JoinDSEditor.PNG)

    此页面用于设计 **Join 类型** 的必需数据源。 在运行时，此数据源将从 **联接列表** 网格中的数据源创建记录的单个联接列表。 记录的联接将从作为第一个网格的网格中的 **ConfigurationProviders** 数据源开始（它的 **类型** 列为空白）。 因此，将根据每个其他数据源在此网格中的顺序将其记录联接到父数据源的记录。 每个联接的数据源都必须配置为嵌套在目标数据源下的数据源（`1Versions` 数据源嵌套在 `1Configurations` 数据源下；`1Configurations` 数据源嵌套在 **ConfigurationProviders** 数据源下）。 每个配置的数据源都必须包含联接条件。 在此 **Join** 的数据源中，定义了以下联接：

    - **ConfigurationProviders** 数据源的每条记录（在 **ERVendorTable** 表中介绍）仅与 **1Configurations** 数据源的记录（在 **ERSolutionTable** 表中介绍）连接，从而在 **SolutionVendor** 和 **RecId** 字段中具有相同的值。 **内联接** 类型用于此连接，以及用于匹配记录的以下条件：

    FILTER（Configurations，Configurations.SolutionVendor = ConfigurationProviders.RecId）

    - **1Configurations** 数据源的每条记录（在 **ERSolutionTable** 表中介绍）仅与 **1Versions** 数据源的记录（在 **ERSolutionVersionTable** 表中介绍）连接，从而在 **Solution** 和 **RecId** 字段中具有相同的值。 **内联接** 类型用于此连接以及用于匹配记录的以下条件：

    FILTER（ConfigurationVersions，ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId）

    - **执行** 选项配置为 **查询**，这意味着此联接数据源将在运行时在数据库级别作为直接 SQL 调用执行。

    对于联接表示应用程序表的数据源的记录，可以使用除描述这些表之间的 AOT 关系中现有字段以外的其他字段对来指定联接条件。 还可以将此类型的联接配置为在数据库级别执行。

6. 关闭该页面。
7. 选择 **取消**。
8. 在配置树中，展开 **Set2.Summary** 数据模型项目：

    - 绑定 **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** 表示 **Set2.Summary.VersionsNumber** 项目绑定到 **GroupBy** 类型的 **DetailsSummary** 数据源的 **VersionsNumber** 合并字段，该类型配置为返回 **Join** 类型的 **Details** 数据源的联接记录数。
    - **执行** 位置选项配置为 **查询**，这意味着此 **GroupBy** 数据源将在运行时在数据库级别作为直接 SQL 调用运行。 能够实现此行为是因为 **Join** 类型的基础数据源 **Details** 被配置为在数据库级别执行。

    ![GROUPBY 数据源参数页面](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. 关闭该页面。
10. 选择 **取消**。

### <a name="execute-er-format"></a><a name="executeERformat"></a> 执行 ER 格式

1. 使用与第一个会话相同的凭据和公司，在 Web 浏览器的第二个会话中访问 Finance 或 RCS。
2. 转到 **组织管理 \> 电子申报 \> 配置**。
3. 展开 **用于了解 JOIN 数据源的模型** 配置。
4. 选择 **用于了解 JOIN 数据源的格式** 配置。
5. 选择 **设计器**。
6. 选择 **显示详细信息**。
7. 选择 **映射**。
8. 选择 **展开/折叠**。

    此格式用于为 ER 配置的每个版本使用新行填充生成的文本文件（**版本** 顺序）。 每个生成的行将包含拥有当前配置的配置提供程序的名称、配置名称和配置版本，并以分号分隔。 生成文件的最后一行将包含已发现的 ER 配置的版本数（**摘要** 顺序）。

    ![ER 格式设计器页面](./media/GER-JoinDS-FormatReview.PNG)

    **Data** 和 **Summary** 数据源用于将配置版本详细信息填充到生成的文件中：

    - 在运行 ER 格式时，运行时在用户对话框页面上为 **Selector** 数据源选择 **否** 时，将使用来自 **Set1** 数据模型的信息。
    - 运行时在用户对话框页面上为 **Selector** 数据源选择 **是** 时，将使用来自 **Set2** 数据模型的信息。

    ![ER 格式设计器页面](./media/GER-JoinDS-FormatMappingReview.PNG)

9. 选择 **运行**。
10. 在对话框页面上，在 **使用 JOIN 数据源** 字段中选择 **否**。
11. 选择 **确定**。
12. 查看生成的文件。

    ![ER 用户对话框页面](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>分析 ER 格式执行跟踪

1. 在 Finance 或 RCS 的第一个会话中，选择 **设计器**。
2. 选择 **性能跟踪**。
3. 在 **性能跟踪** 网格中，选择使用当前模型映射组件的 ER 格式的最新执行跟踪的最上面那条记录。
4. 选择 **确定**。

    执行统计信息会通知您有关应用程序表的重复调用：

    - **ERSolutionTable** 被调用的次数与您在 **ERSolutionVersionTable** 表中的配置版本记录相同，而为提高性能，此类调用的次数可以适时减少。
    - 对于 **ERSolutionVersionTable** 表中发现的每个配置版本记录，两次调用了 **ERVendorTable**，此类调用的次数也可以减少。

    ![ER 模型映射设计器页面](./media/GER-JoinDS-Set1Run2.PNG)

5. 关闭该页面。

### <a name="execute-er-format"></a>执行 ER 格式

1. 切换到包含 Finance 或 RCS 的第二个会话的 Web 浏览器选项卡。
2. 选择 **运行**。
3. 在对话框页面上，在 **使用 JOIN 数据源** 字段中选择 **是**。
4. 选择 **确定**。
5. 查看生成的文件。

    ![ER 用户对话框页面](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a>分析 ER 格式执行跟踪

1. 在 Finance 或 RCS 的第一个会话中，选择 **设计器**。
2. 选择 **性能跟踪**。
3. 在 **性能跟踪** 网格中，选择表示使用当前模型映射组件的 ER 格式的最新执行跟踪的最上面那条记录。
4. 选择 **确定**。

    统计信息会通知您以下内容：

    - 已调用一次应用程序数据库，以从 **ERVendorTable**、**ERSolutionTable** 和 **ERSolutionVersionTable** 表中获取记录来访问必填字段。

    ![ER 模型映射设计器页面](./media/GER-JoinDS-Set2Run2.PNG)

    - 已调用一次应用程序数据库，以使用在 **Details** 数据源中配置的联接来计算配置版本数。

    ![ER 模型映射设计器页面](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>限制

从本主题的示例中可以看到，可以利用多个数据源构建 **JOIN** 数据源，前者描述了最终必须连接的记录的各个数据集。 您可以使用内置的 ER [FILTER](er-functions-list-filter.md) 函数来配置这些数据源。 当您配置数据源以使其在 **JOIN** 数据源之外被调用时，您可以将公司范围用作数据选择条件的一部分。 **JOIN** 数据源的初始实现不支持这种类型的数据源。 例如，在 **JOIN** 数据源的执行范围内调用基于 [FILTER](er-functions-list-filter.md) 的数据源时，如果被调用的数据源包含公司范围，并将其作为数据选择条件的一部分，则会发生异常。

在 Microsoft Dynamics 365 Finance 版本 10.0.12（2020 年 8 月）中，可以将公司范围用作在基于 [FILTER](er-functions-list-filter.md) 的数据源中进行数据选择的部分条件，这些数据源在 **JOIN** 数据源的执行范围内被调用。 由于应用程序 [查询](../dev-ref/xpp-library-objects.md#query-object-model)生成器限制的缘故，仅对 **JOIN** 数据源的第一个数据源支持公司范围。

### <a name="example"></a>示例

例如，您必须对应用程序数据库进行单次调用，才能获取多个公司的外贸交易列表，以及这些交易中引用的库存项目的详细信息。

在这种情况下，您可以在 ER 模型映射中配置以下项目：

- 表示 **Intrastat** 表的 **内部统计** 根数据源。
- 表示 **InventTable** 表的 **项目** 根数据源。
- **公司** 根数据源，它返回必须在其中访问交易的公司（在此示例中为 **DEMF** 和 **GBSI**）列表。 公司代码可从 **Companies.Code** 字段获得。
- 具有 `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))` 表达式的 **X1** 根数据源。 作为数据选择条件的一部分，此表达式包含公司范围 `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)` 的定义。
- 作为 **X1** 数据源的嵌套项的 **X2** 数据源。 它包括 `FILTER (Items, Items.ItemId = X1.ItemId)` 表达式。

最后，您可以配置 **JOIN** 数据源，其中 **X1** 是第一个数据源，**X2** 是第二个数据源。 您可以将 **查询** 指定为 **执行** 选项，以强制 ER 作为直接 SQL 调用在数据库级别运行此数据源。

在[跟踪](trace-execution-er-troubleshoot-perf.md) ER 执行情况期间运行配置的数据源时，以下语句在 ER 模型映射设计器中显示为 ER 性能跟踪的一部分。

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> 如果运行已配置的 **JOIN** 数据源，以便该数据源包含数据选择条件，并且这些数据选择条件具有已执行 **JOIN** 数据源的其他数据源的公司范围，则会出现错误。

## <a name="additional-resources"></a>其他资源

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[跟踪 ER 格式的执行情况以解决性能问题](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]