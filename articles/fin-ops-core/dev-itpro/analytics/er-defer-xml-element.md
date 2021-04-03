---
title: 推迟执行 ER 格式的 XML 元素
description: 本主题说明如何推迟执行电子报告 (ER) 格式的 XML 元素。
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f9a19f4ba6bb124de948dcd9e62b258b2178687a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562134"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>推迟执行 ER 格式的 XML 元素

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概览

您可以使用[电子报表 (ER)](general-electronic-reporting.md) 框架的工序设计器，以[配置](./tasks/er-format-configuration-2016-11.md)用于生成 XML 格式出站文档的 ER 解决方案的[格式组件](general-electronic-reporting.md#FormatComponentOutbound)。 配置的格式组件的层次结构由各种类型的格式元素组成。 这些格式元素用于在运行时用所需的信息填充生成的文档。 默认情况下，当您运行 ER 格式时，格式元素的运行顺序与它们在格式层次结构中的显示顺序相同：从上到下一个接一个。 但是，在设计时，您可以更改已配置格式组件的任何 XML 元素的执行顺序。

通过对已配置格式的 XML 元素打开 <a name="DeferredXmlElementExecution"></a>**推迟执行** 选项，可以推迟（延迟）执行该元素。 在这种情况下，该元素只有在其父元素的所有其他元素都已运行后才能运行。

若要了解有关此功能的详细信息，请完成本主题中的示例。

## <a name="limitations"></a>限制

仅为 ER 格式（用于生成 XML 格式的 **出站** 文档）配置的 XML 元素支持 **推迟执行** 选项。

仅位于一个其他 XML 元素中的 XML 元素支持 **推迟执行** 选项。 因此，它不适用于位于其他类型的格式元素中（例如位于 **XML 序列** 元素中）的 XML 元素。

如果 **拆分文件** 选项设置为 **是**，则位于 **通用\\文件** 格式元素中的 XML 元素不支持 **推迟执行** 选项。 有关如何拆分 XML 文件的详细信息，请参阅[基于文件大小和内容数量拆分生成的 XML 文件](er-split-files.md)。

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>示例：推迟执行 ER 格式的 XML 元素

以下步骤说明了具有系统管理员或电子报告职能顾问[角色](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles)的用户如何配置一个 ER 格式，以包含执行顺序与格式层次结构中的执行顺序不同的 XML 元素。

这些步骤可以在 **USMF** 公司内的 Microsoft Dynamics 365 Finance 中执行。

### <a name="prerequisites"></a>先决条件

若要完成本示例，您必须能够用以下角色之一访问 **USMF** 公司的 Finance：

- 电子申报功能顾问
- 系统管理员

如果您尚未完成[推迟执行 ER 格式的序列元素](er-defer-sequence-element.md#Example)主题中的示例，请下载示例 ER 解决方案的以下[配置](general-electronic-reporting.md#Configuration)。

| 内容描述            | 文件名 |
|--------------------------------|-----------|
| ER 数据模型配置    | [Model to learn deferred elements.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER 模型映射配置 | [Mapping to learn deferred elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

在开始之前，您还必须将示例 ER 解决方案的以下配置下载并保存到本地计算机上。

| 内容描述     | 文件名 |
|-------------------------|-----------|
| ER 格式配置 | [Format to learn deferred XML elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>导入示例 ER 配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 选择 **申报配置**。
3. 在 **配置** 页面上，如果 **用于了解推迟的元素的模型** 配置在配置树中不可用，请导入 ER 数据模型配置：

    1. 选择 **交换**，然后选择 **从 XML 文件加载**。
    2. 选择 **浏览**，找到并选择 **Model to learn deferred elements.1.xml** 文件，然后选择 **确定**。

4. 如果 **用于了解推迟的元素的映射** 配置在配置树中不可用，请导入 ER 模型映射配置：

    1. 选择 **交换**，然后选择 **从 XML 文件加载**。
    2. 选择 **浏览**，找到并选择 **Mapping to learn deferred elements.1.1.xml** 文件，然后选择 **确定**。

5. 导入 ER 格式配置：

    1. 选择 **交换**，然后选择 **从 XML 文件加载**。
    2. 选择 **浏览**，找到并选择 **Format to learn deferred XML elements.1.1.xml** 文件，然后选择 **确定**。

6. 在配置树中，展开 **用于了解推迟的元素的模型**。
7. 在配置树中查看导入的 ER 配置的列表。

    ![“配置”页面上导入的 ER 配置](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>激活配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页上的 **配置提供程序** 部分中，确保列出了示例公司 Litware, Inc. (`http://www.litware.com`) 的[配置提供程序](general-electronic-reporting.md#Provider)，并将其标记为活动状态。 如果未列出此配置提供程序，或者未将其标记为活动状态，请按照[创建一个配置提供程序，并标记其为活动状态](./tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。

    ![“本地化配置”页面上的示例公司 Litware, Inc.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>查看导入的模型映射

查看 ER 模型映射组件的设置，该组件配置为根据请求来访问税收交易记录并公开访问的数据。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 选择 **申报配置**。
3. 在 **配置** 页上的配置树中，展开 **用于了解推迟的元素的模型**。
4. 选择 **用于了解推迟的元素的映射** 配置。
5. 选择 **设计器** 来打开映射列表。
6. 选择 **设计器** 查看映射详细信息。
7. 选择 **显示详细信息**。
8. 查看配置为访问税收交易记录的数据源：

    - *表记录* 类型的 **交易记录** 数据源被配置为访问 **TaxTrans** 应用程序表的记录。
    - **计算字段** 类型的 *凭证* 数据源被配置为返回所需的凭证代码（**INV-10000349** 和 **INV-10000350**）作为记录列表。
    - **计算字段** 类型的 *已筛选* 数据源被配置为从 **交易记录** 数据源中仅选择所需凭证的税收交易记录。
    - 为 **已筛选** 数据源添加了 *计算字段* 类型的 **\$TaxAmount** 字段，以显示具有相反符号的税收值。
    - **分组依据** 类型的 *已分组* 数据源被配置为将 **已筛选** 数据源的已筛选税收交易记录分组。
    - **已分组** 数据源的 **TotalSum** 聚合字段被配置为针对该数据源的所有已筛选税收交易记录汇总 **已筛选** 数据源的 **\$TaxAmount** 字段值。

        ![“编辑‘GroupBy’参数”页面上的 TotalSum 聚合字段](./media/ER-DeferredXml-GroupByParameters.png)

9. 查看配置的数据源如何绑定到数据模型，以及它们如何公开访问的数据以使其以 ER 格式可用：

    - **已筛选** 数据源已绑定到数据模型的 **Data.List** 字段。
    - **已筛选** 数据源的 **\$TaxAmount** 字段已绑定到数据模型的 **Data.List.Value** 字段。
    - **已分组** 数据源的 **TotalSum** 字段已绑定到数据模型的 **Data.Summary.Total** 字段。

    ![模型映射设计器页面](./media/ER-DeferredXml-ModelMapping.png)

10. 关闭 **模型映射设计器** 和 **模型映射** 页面。

### <a name="review-the-imported-format"></a>查看导入的格式

1. 在 **配置** 页面上的配置树中，选择 **用于了解延迟 XML 元素的格式** 配置。
2. 选择 **设计器** 查看格式详细信息。
3. 选择 **显示详细信息**。
4. 查看 ER 格式组件的设置，这些设置被配置为以 XML 格式生成出站文档，其中包括税收交易记录的详细信息：

    - **报表\\消息** XML 元素被配置为使用包含嵌套 XML 元素（**标题**、**记录** 和 **汇总**）的单个节点填充出站文档。
    - **报表\\消息\\标题** XML 元素被配置为用单个标题节点填充出站文档，以显示处理的开始日期和时间。
    - **报表\\消息\\记录** XML 元素被配置为用显示单项税收交易记录详细信息的单个记录节点填充出站文档。
    - **报表\\消息\\汇总** XML 元素被配置为用包括已处理税收交易记录中税收值总计的单个汇总节点填充的出站文档。

    ![“格式设计器”页面上的消息 XML 元素和嵌套 XML 元素](./media/ER-DeferredXml-Format.png)

5. 在 **映射** 选项卡上，查看以下详细信息：

    - **报表\\消息\\标题** 元素不必绑定到源即可在出站文档中生成单个节点。
    - **ExecutionDateTime** 属性会生成标题节点的添加日期和时间（包括毫秒）。
    - **报表\\消息\\记录** 元素已绑定到 **model.Data.List** 列表，以为绑定列表中的每条记录生成单个记录节点。
    - **TaxAmount** 属性已绑定到 **model.Data.List.Value**（在相对路径视图中显示为 **\@.Value**）以生成当前税收交易记录的税收值。
    - **RunningTotal** 属性是税收值累计总额的占位符。 当前，此属性没有输出，因为没有为其配置绑定或默认值。
    - **ExecutionDateTime** 属性生成在此报表中处理当前交易时的日期和时间（包括毫秒）。
    - **报表\\消息\\汇总** 元素不必绑定到数据源即可在出站文档中生成单个节点。
    - **TotalTaxAmount** 属性已绑定到 **model.Data.Summary.Total** 以生成已处理税收交易记录的税收值总和。
    - **ExecutionDateTime** 属性会生成汇总节点的添加日期和时间（包括毫秒）。

    ![“格式设计器”页上的“映射”选项卡](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>运行导入的格式

1. 在 **格式设计器** 页上，选择 **运行**。
2. 下载 Web 浏览器提供的文件，然后将其打开以进行检查。

    ![下载的文件](./media/ER-DeferredXml-Run.png)

请注意，汇总节点显示了已处理交易记录的税收值总和。 由于该格式已配置为使用 **model.Data.Summary.Total** 绑定返回此总和，所以通过调用模型映射中 **GroupBy** 类型的 **已分组** 数据源 *TotalSum* 汇总计算了此总和。 为了计算此汇总，模型映射会在 **已筛选** 数据源中选择的所有交易记录上迭代。 通过比较汇总节点和最后一个记录节点的执行时间，可以确定计算总和用了 12 毫秒 (ms)。 通过比较第一个和最后一个记录节点的执行时间，可以确定生成所有记录节点用了 9 ms。 因此，总共需要 21 ms。

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>修改格式，以便根据生成的输出来进行计算

如果交易记录量远大于当前示例中的交易记录量，则计算时间可能会增加并导致性能问题。 通过更改格式设置，可以帮助防止这些性能问题。 因为您访问税收值以将其包括在生成的报表中，所以您可以重复使用此信息来计算税收值。 有关更多信息，请参见[配置格式以进行计数和求和](./tasks/er-format-counting-summing-1.md)。

1. 在 **格式设计师** 页面上的 **格式** 选项卡上，选择格式树中的 **报表** 文件元素。
2. 将 **收集输出详细信息** 选项设置为 **是**。 现在，您可以使用已生成报表的内容作为数据源来配置此格式，该数据源可以通过使用[数据收集](er-functions-category-data-collection.md)类别中的内置 ER 函数来访问。
3. 在 **映射** 选项卡上，选择 **报表\\消息\\记录** XML 元素。
4. 将 **收集的数据密钥名称** 表达式配置为 `WsColumn`。
5. 将 **收集的数据密钥值** 表达式配置为 `WsRow`。

    ![“格式设计器”页面上的记录 XML 元素](./media/ER-DeferredXml-Format3.png)

6. 选择 **报表\\消息\\记录\\TaxAmount** 属性。
7. 将 **收集的数据密钥名称** 表达式配置为 `SummingAmountKey`。

    ![“格式设计器”页面上的 TaxAmount 属性](./media/ER-DeferredXml-Format4.png)

    您可以考虑使用此设置来实现虚拟工作表，其中单元格 A1 的值将附加来自每个已处理税收交易记录的税额值。

8. 选择 **报表\\消息\\记录\\RunningTotal** 属性，然后选择 **编辑公式**。
9. 使用内置 [SUMIF](er-functions-datacollection-sumif.md) ER 函数配置 `SUMIF(SummingAmountKey, WsColumn, WsRow)` 表达式，然后选择 **保存**。

    ![SUMIF 表达式](./media/ER-DeferredXml-FormulaDesigner.png)

10. 关闭 **公式设计器** 页。
11. 选择 **保存**，然后选择 **运行**。
12. 下载并查看 Web 浏览器提供的文件。

    ![下载的文件](./media/ER-DeferredXml-Run1.png)

    最后一个记录节点包含使用生成的输出作为数据源为所有已处理交易记录计算的税值累计总和。 此数据源从报表的开头开始，一直持续到最后一个税收交易记录。 汇总节点包含使用 *GroupBy* 类型数据源在模型映射中计算的所有已处理交易记录的税值总和。 请注意，这些值相等。 因此，可以使用基于输出的求和来代替 **GroupBy**。 通过比较第一个记录节点和汇总节点的执行时间，可以确定生成所有记录节点并进行汇总用了 11 ms。 因此，就生成记录节点和税值总和而言，修改后的格式大约比原始格式快两倍。

13. 选择 **报表\\消息\\汇总\\TotalTaxAmount** 属性，然后选择 **编辑公式**。
14. 输入 `SUMIF(SummingAmountKey, WsColumn, WsRow)` 表达式而不是现有表达式。
15. 选择 **保存**，然后选择 **运行**。
16. 下载并查看 Web 浏览器提供的文件。

    ![下载的文件](./media/ER-DeferredXml-Run2.png)

    请注意，最后一个记录节点中的税收值累计总和现在等于汇总节点上的总和。

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>将基于输出的总和的值放在报表标题中

例如，如果您必须在报表的标题中显示税值总和，则可以修改格式。

1. 在 **格式设计器** 页面的 **格式** 选项卡上，选择 **报表\\消息\\汇总** XML 元素。
2. 选择 **上移**。
3. 选择 **保存**，然后选择 **运行**。
4. 下载并查看 Web 浏览器提供的文件。

    ![下载的文件](./media/ER-DeferredXml-Run3.png)

    请注意，汇总节点中的税收值总和现在等于 0（零），因为此总和现在是基于生成的输出计算的。 生成第一个记录节点时，生成的输出尚不包含具有交易记录明细的记录节点。 您可以配置此格式以延迟执行 **报表\\消息\\汇总** 元素，直到已经为所有税收交易记录运行了 **报表\\消息\\记录** 元素为止。

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>推迟执行汇总 XML 元素，以便使用计算出的总和

1. 在 **格式设计器** 页面的 **格式** 选项卡上，选择 **报表\\消息\\汇总** XML 元素。
2. 将 **推迟执行** 选项设置为 **是**。

    ![“格式设计器”页面上“汇总”XML 元素的推迟执行选项](./media/ER-DeferredXml-Format5.png)

3. 选择 **保存**，然后选择 **运行**。
4. 下载并查看 Web 浏览器提供的文件。

    ![下载的文件](./media/ER-DeferredXml-Run4.png)

    **报表\\消息\\汇总** 元素现在仅在其父元素 **报表\\消息** 下嵌套的所有其他项目运行之后才运行。 因此，它在针对 **model.Data.List** 数据源的所有税收交易记录运行 **报表\\消息\\记录** 元素后运行。 第一个和最后一个记录节点的执行时间以及标题和汇总节点的执行时间揭示了这一事实。

## <a name="additional-resources"></a>其他资源

- [配置格式以执行计数和合计](./tasks/er-format-counting-summing-1.md)
- [跟踪 ER 格式的执行情况以解决性能问题](trace-execution-er-troubleshoot-perf.md)
- [推迟执行 ER 格式的序列元素](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]