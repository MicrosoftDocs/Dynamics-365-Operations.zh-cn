---
title: 支持 ER 数据模型的参数化调用
description: 本主题介绍了如何实现电子申报 (ER) 数据模型的参数化调用。
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419464"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>支持 ER 数据模型的参数化调用

[!include [banner](../includes/banner.md)]

若要生成业务文档，请配置包含以下 ER 组件的[电子申报 (ER)](general-electronic-reporting.md) 解决方案：

- **[格式](er-overview-components.md#format-component)** - 此组件指定业务文档的结构。
- **格式映射** - 此组件控制运行时填写业务文档的方式。
- **[模型映射](er-overview-components.md#model-mapping-component)** - 此组件指定数据从应用程序提取到格式映射中的内容。
- **[数据模型](er-overview-components.md#data-model-component)** - 此组件在各个组件之间传递信息。

运行 ER 格式时，从根格式元素开始运行每个格式元素。 每当运行的格式元素包含数据源[绑定](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents)时，都会运行数据源以提供预期数据并使用它填写格式元素。 调用 *模型* 类型的数据源后，将根据模型映射设置调用适当的模型映射以从应用程序中提取数据。

以前，无法对这些模型映射调用进行参数化，因此无法使其依赖于所运行格式的逻辑。 仅支持以下数据流。

<table>
<tbody>
<tr align="center">
<td>
<b>格式</b><br>
格式元素<br>
&nbsp;
</td>
<td>
<i>绑定</i><br>
&gt;&nbsp;请求&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;&lt;
</td>
<td><b>格式映射</b><br>
数据源<br>
&nbsp;
</td>
<td>
<i>数据模型</i><br>
&gt;&nbsp;请求&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;&lt;
</td>
<td>
<b>模型映射</b><br>
数据源<br>
&nbsp;
</td>
<td>
<i>绑定</i><br>
&gt;&nbsp;请求&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;&lt;
</td>
<td>
<b>表</b><br>
记录<br>
字段
</td>
</tr>
</tbody>
</table>

但是，在版本 10.0.15 及更高版本中，您可以配置仅在提供所配置参数的值时才能调用的数据模型字段。 从格式组件配置和调用此类字段时，必须在格式绑定中提供所需的参数作为调用的参数。 在这些情况下，可以根据特定于格式的值指定参数的值。 因此，您可以使用 **动态运行时参数化** 进行数据模型调用以支持以下数据流。

<table>
<tbody>
<tr align="center">
<td>
<b>格式</b><br>
格式元素 1<br>
<br>
格式元素 2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>绑定</i><br>
&gt;&nbsp;请求&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;请求&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>格式映射</b><br>
数据源 1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>数据模型</i><br>
&gt;&nbsp;field1&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;值&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>模型映射</b><br>
数据源 1<br>
<br>
数据源 2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>绑定</i><br>
&gt;&nbsp;请求&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;请求&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;值&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>表&nbsp;1</b><br>
记录&nbsp;1<br>
字段&nbsp;1<br>
<b>表&nbsp;2</b><br>
记录&nbsp;2<br>
字段&nbsp;2
</td>
</tr>
</tbody>
</table>

新功能允许您对 [*记录*](er-formula-supported-data-types-composite.md#record)或 [*记录列表*](er-formula-supported-data-types-composite.md#record-list)类型的任何数据模型字段的调用进行参数化。 数据模型字段的参数支持以下数据类型：

- [Boolean](er-formula-supported-data-types-primitive.md#boolean)
- [集装箱](er-formula-supported-data-types-composite.md#container)
- [日期](er-formula-supported-data-types-primitive.md#date)
- [日期时间](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [整数](er-formula-supported-data-types-primitive.md#integer)
- [实数](er-formula-supported-data-types-primitive.md#real)
- [字符串](er-formula-supported-data-types-primitive.md#string)

您可以指定数据模型字段的每个参数，并且可以为数据模型字段提供参数，作为已定义数据类型的单个值和此类值的 [*列表*](er-formula-supported-data-types-composite.md#record-list)。

> [!NOTE]
> 不支持数据模型字段参数的默认值。 如果您将参数添加到数据模型中的字段，并且该数据模型的版本已经发布，则必须将所有相应的模型映射和格式[重定](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)为该模型的新版本，因为该数据模型更改无法向后兼容。

您可以配置参数化数据模型字段以使模型映射调用特定于格式。 此方法可以帮助您减少必须为单个数据模型的许多格式配置的模型映射数。 您还可以使用此方法来提高格式的执行性能并减少生成业务文档所需的时间。 若要了解有关此功能的详细信息，请完成本主题中的示例。

## <a name="example-use-parameterized-calls-of-er-data-models"></a>示例：使用 ER 数据模型的参数化调用

以下步骤说明了系统管理员或电子申报开发人员角色的用户如何设计一个包含数据模型、模型映射和格式 ER 组件的 ER 解决方案，通过为调用提供参数（其值是在运行时使用运行格式的公式计算出来的），这些组件被配置为从格式调用模型映射。 

这些步骤可以在 **DEMF** 公司完成。 无需进行任何代码修改。 

在此示例中，将为示例公司 **Litware, Inc.** 创建所需 ER [配置](general-electronic-reporting.md#Configuration)。 确保为 ER 框架列出了 **Litware, Inc.** (`http://www.litware.com`) 示例公司的配置提供程序，并且它被标记为 **活动**。 如果未列出此配置提供程序，或者未将其标记为 **活动** 状态，请按照[创建一个配置提供程序，并标记其为活动状态](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。

### <a name="business-scenario"></a>业务方案

您有一个 ER 解决方案，其中包含一种格式，您可以运行该格式以生成用于审计目的的电子单据。 此格式包含的税务交易与销售订单和采购订单相关，并且具有所需的详细信息，例如交易日期和税值。 在新会计年度，此单据的结构已更改。 您现在必须提交一个扩展单据，其中包含在生成的报表上显示其交易的所有当事方（客户和供应商）的其他详细信息（名称）。 因此，您必须修改 ER 解决方案，以便它生成符合此新要求的单据。

### <a name="configure-the-er-framework"></a>配置 ER 框架

按照[配置电子报告框架](er-quick-start2-customize-report.md#ConfigureFramework)中的步骤设置最低限度的电子报告参数集。 在开始使用 ER 框架设计新 ER 解决方案之前，您必须完成此设置。

### <a name="design-a-domain-specific-data-model"></a>设计域特定数据模型

您必须创建一个包含所需数据模型组件的新 ER 配置。 此数据模型将在以后您设计 ER 格式以生成审核报表时用作数据源。

按照以下步骤从 Microsoft 提供的 XML 文件导入所需的数据模型。

1. 下载 [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在 **配置** 页上的操作窗格中，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Sample audit model.version.1.xml** 文件。
6. 选择 **确定** 导入配置。

    ![“配置”页面上导入的 ER 数据模型配置。](./media/er-data-model-parameterized-calls-imported-model.png)

下图显示了 **数据模型设计器** 页上可编辑版本的已配置数据模型。

![数据模型设计器页面上 ER 数据模型的结构。](./media/er-data-model-parameterized-calls-model1.png)

当前，该模型旨在仅公开具有所需详细信息的税务交易。

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>为配置的数据模型设计模型映射

作为电子报告开发人员角色的用户，您必须为示例审核数据模型创建一个新的 ER 配置，其中包含模型映射组件。 此组件实现为 Microsoft Dynamics 365 Finance 配置的数据模型，并且特定于该应用。 您必须配置模型映射组件来指定必须用于在运行时使用应用程序数据填充配置的数据模型的应用程序对象。 要完成此任务，您必须了解税业务域的数据结构在 Finance 中是如何实现的。

按照以下步骤从 Microsoft 提供的 XML 文件导入所需的模型映射。

1. 下载 [Sample audit model mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在 **配置** 页上的操作窗格中，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Sample audit model mapping.version.1.1.xml** 文件。
6. 选择 **确定** 导入配置。

    ![“配置”页面上导入的 ER 模型映射配置。](./media/er-data-model-parameterized-calls-imported-mapping.png)

下图显示了 **模型映射设计器** 页面上配置的模型映射的可编辑版本。

![模型映射设计器页面上 ER 模型映射的结构。](./media/er-data-model-parameterized-calls-mapping1.png)

当前，该模型映射旨在公开具有所需详细信息的税务交易。 它使用配置的 `TaxTrans` 和 `TaxTrans` ER 数据源从 `TaxTransFiltered` 应用程序表中提取此信息。

### <a name="design-a-new-format"></a>设计新格式

作为电子报告功能顾问角色的用户，您必须创建一个新的 ER 配置，其中包含格式组件。 您必须配置格式组件，才能用包含所有必需详细信息的税务交易填写生成的报表。

按照以下步骤从 Microsoft 提供的 XML 文件导入所需的格式。

1. 下载 [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在 **配置** 页上的操作窗格中，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Sample audit format.version.1.1.xml** 文件。
6. 选择 **确定** 导入配置。

    ![“配置”页面上导入的 ER 格式配置。](./media/er-data-model-parameterized-calls-imported-format.png)

下图显示了 **格式设计器** 页面上配置的格式的可编辑版本。

![格式设计器页面上 ER 格式的结构。](./media/er-data-model-parameterized-calls-format1.png)

ER 格式配置为以逗号分隔值 (CSV) 格式的文本文件形式生成报表。

### <a name="run-the-imported-format"></a>运行导入的格式

1. 在 **配置** 页面上，选择 **示例审核格式** 配置，然后在操作窗格上选择 **运行**。
2. 在 **电子报表参数** 对话框的 **要包括的记录** 选项卡上，选择 **筛选器**。
3. 指定条件以选择 **PIV-110000004** 和 **INV-10000001** 凭证的税务交易。
4. 选择 **确定**。
5. 选择 **确定**。
6. 查看包含所选凭证的税务交易的已生成单据。

    ![带税务交易的已生成单据的预览。](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>调整导入的 ER 解决方案

根据新要求，您必须提交的单据必须包含其交易包含在内的客户和供应商的名称。 因此，您必须修改导入的 ER 解决方案，以便它生成符合此新要求的单据。

决定您希望如何对导入的 ER 组件进行所需的修改。

显而易见的方法是实施以下修改：

- 在数据模型中，添加 *字符串* 类型的新 `Transaction.Party.Name` 数据模型字段。
- 在模型映射中，使用可用的表关系配置新数据模型字段的绑定，以访问 `DirPartyTable` 应用程序表的相关记录，并从中提取 `Name` 字段的值。

尽管此方法将起作用，但它可能会在 SQL 数据库中导致性能问题，因为 `TaxTrans` 是交易表，因此可能包含大量记录。 在这种情况下，`DirPartyTable` 的调用次数必须等于 `TaxTrans` 表中可能导致性能问题的记录数。

或者，您可以进行以下修改：

- 在数据模型中，添加新 `Party` 根和新 `Party.Name` 字段。
- 在模型映射中，添加一个新的数据源，该数据源将加入表关系中使用的所有表记录，以从 `DirPartyTable` 表开始访问 `TaxTrans` 应用程序表的相关记录。

虽然此方法将起作用，但它可能会导致一些内存消耗问题。 即使将新 [JOIN](er-join-data-sources.md) 数据源作为对应用程序数据库的单个 SQL 请求运行来防止数据库性能问题，也必须将结果提取到应用程序服务器的内存中。 因为记录的数量和这些记录中的字段数量会很大，所以这种方法可能会导致内存消耗非常大。 甚至可能会引发内存不足运行时异常。

当运行格式在内存中收集将在已生成报表中显示的所有税务交易的客户和供应商唯一标识代码时，您可以实施修改。 因为只应该保留唯一代码，所以最终的代码集不会大到影响内存消耗。 然后，将代码集传递到模型映射，作为 *模型* 类型数据源的另一调用的参数。 基于该调用，模型映射将运行一个新 ER 数据源，该数据源向应用程序数据库发出单个 SQL 请求，以从 `DirPartyTable` 表中仅提取其代码出现在所提供的一组数据中的各当事方记录。

### <a name="adjust-the-imported-data-model"></a>调整导入的数据模型

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的左侧窗格的配置树中，选择 **示例审核模型**。
3. 在 **版本** 快速选项卡上，选择状态为 **[草稿](general-electronic-reporting.md#component-versioning)** 的版本 **2**。
4. 选择 **配置组件** 快速选项卡。
5. 选择 **设计器** 以打开要编辑的数据模型。
6. 在 **数据模型** 页面上，请确保已选择 `Root` 字段，然后选择 **新建**。
7. 在下拉对话框中，执行以下步骤：

    1. 在 **新节点作为** 字段组中，选择 **活动节点的子节点** 选项。
    2. 在 **名称** 字段中，输入 **当事方**。
    3. 在 **物料类型** 字段中，选择 **记录列表**。
    4. 选择 **添加** 以完成添加新字段的操作。

8. 确保选择了 `Root.Party` 字段，然后在 **节点** 选项卡上，选择 **参数**。
9. 在 **参数** 对话框中，执行以下步骤：

    1. 在 **参数** 选项卡上，选择 **新建**。
    2. 在 **名称** 字段中，输入 **PartyRefRecId**。
    3. 在 **类型** 字段中，选择 **Int64**。
    4. 选择 **列表** 复选框。
    5. 选择 **确定** 以完成输入参数的操作。

    > [!NOTE]
    > 您刚才将 `Root.Party` 数据模型字段配置为在 **PartyRefRecId** 参数中提供值时调用的字段。 此值必须存在于包含 *Int64* 数据类型的 `Value` 字段的记录列表中。

    ![参数对话框。](./media/er-data-model-parameterized-calls-model2a.png)

10. 请确保仍然选择 `Root.Party` 字段，然后选择 **新建**。
11. 在下拉对话框中，执行以下步骤：

    1. 在 **新节点作为** 字段组中，选择 **活动节点的子节点** 选项。
    2. 在 **名称** 字段中，输入 **名称**。
    3. 在 **物料类型** 字段中，选择 **字符串**。
    4. 选择 **添加** 以完成添加新字段的操作。

12. 选择 **保存**，然后关闭 **数据模型** 页面。

    ![“数据模型设计器”页面上已调整 ER 数据模型的结构。](./media/er-data-model-parameterized-calls-model2b.png)

13. 在 **版本** 快速选项卡上，针对版本 **2**，选择 **更改状态** \> **完成**。 然后选择 **确定**。

    > [!NOTE]
    > 您的数据模型更改存储在 **示例审核模型** 数据模型组件的第二修订版中，该组件位于 **示例审核模型** ER 配置的第二个版本中。

![“配置”页面上更新的 ER 数据模型配置。](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>调整导入的模型映射

1. 在 **配置** 页的左侧窗格的配置树中，展开 **示例审核模型**。
2. 选择 **示例审核模型映射**，然后在 **版本** 快速选项卡上，选择基于第一个数据模型版本（版本 **1.2**）且状态为 **草稿** 的第二个映射版本。
3. 选择 **重定基本版本**。
4. 在 **目标版本** 字段中，保留 **示例审核模型** 基本模型的版本 **2**。
5. 选择 **确定** 以重定模型映射并将其与最近的数据模型更改保持一致。

    请注意，可编辑模型映射的版本号已从 **1.2** 更改为 **2.2**，以指示第二个模型版本当前用作基础版本。

6. 选择 **设计器**。
7. 在 **模型到数据源映射** 页面上，选择当前模型映射的 **设计器**。
8. 按照这些步骤添加新数据源以访问 `DirPartyTable` 应用程序表：

    1. 在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations \> 表记录**。
    2. 在 **数据源** 窗格中，选择 **添加根**。
    3. 在 **名称** 字段中，输入 **PartyTable**。
    4. 在 **表** 字段中，输入 **DirPartyTable**。
    5. 选择 **确定** 以完成添加新数据源的操作。

9. 根据提供的记录标识代码列表，按照以下步骤添加新数据源以请求 `DirPartyTable` 记录：

    1. 在 **数据源类型** 窗格中，选择 **常规 \> 空容器**。
    2. 在 **数据源** 窗格中，选择 **添加根**。
    3. 在 **名称** 字段中，输入 **数据**。
    4. 选择 **确定** 以完成添加新数据源的操作。
    5. 在 **数据源** 窗格中，选择 **数据** 数据源。
    6. 在 **数据源类型** 窗格中，选择 **函数 \> 计算字段**。
    7. 在 **数据源** 窗格中选择 **添加**。
    8. 在 **名称** 字段中，输入 **DirParty**。
    9. 选择 **编辑公式**。
    10. 在 **公式设计器** 页面上，选择 **参数**。
    11. 在 **参数** 对话框中，执行以下步骤：

        1. 在 **参数** 选项卡上，选择 **新建**。
        2. 在 **名称** 字段中，输入 **DirPartyId**。
        3. 在 **类型** 字段中，选择 **Int64**。
        4. 选择 **列表** 复选框。
        5. 选择 **确定**。

        > [!NOTE]
        > 您刚才配置了此计算字段，以便它在运行时接受单个参数的自变量，该参数配置为具有 *Int64* 类型的单个 `Value` 字段的记录列表。

    12. 在 **公式** 字段中，输入下面的表达式：

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > 您刚才将 `DirParty` 计算字段配置为仅获取 `DirPartyTable` 记录，其中记录标识代码包含在 `DirPartyId` 列表中，该列表在调用 `DirParty` 字段时作为参数提供。

        ![从“公式设计器”页面上的应用程序表中获取当事方名称的公式。](./media/er-data-model-parameterized-calls-formula1.png)

    13. 选择 **保存**，然后关闭 **公式设计器** 页面。
    14. 选择 **保存**，然后选择 **确定** 以完成添加新数据源的操作。

10. 按照以下步骤将新数据源绑定到新数据模型字段，以便使用数据模型公开当事方名称：

    1. 在 **数据模型** 窗格中，选择 `Root.Party` 数据模型字段。
    2. 在 **数据模型** 窗格中，选择 **编辑**。
    3. 在 **公式设计器** 页面的 **公式** 字段中，输入表达式 `Data.DirParty(PartyRefRecId)`。
    4. 选择 **保存**，然后关闭 **公式设计器** 页面。

        > [!NOTE]
        > 您刚才将绑定配置为调用配置的 `Data.DirParty` 数据源，并提供调用 `Root.Party` 数据模型字段时以此格式指定的记录标识代码列表。

    5. 在 **数据模型** 窗格中，选择 `Root.Party.Name` 数据模型字段。
    6. 在 **数据模型** 窗格中，选择 **编辑**。
    7. 在 **公式设计器** 页面上的 **数据源** 窗格中，展开 **数据 \> DirParty**，然后选择 **名称**。
    8. 选择 **添加数据源**。
    9. 选择 **保存**，然后关闭 **公式设计器** 页面。

    ![“模型映射设计器”页面上已调整 ER 模型映射的结构。](./media/er-data-model-parameterized-calls-mapping2.png)

11. 选择 **保存**，然后关闭 **模型映射设计器** 页面。
12. 关闭 **模型到数据源映射** 页。
13. 在 **版本** 快速选项卡上，针对版本 **2.2**，选择 **更改状态 \> 完成**。 然后选择 **确定**。

### <a name="adjust-the-imported-format"></a>调整导入的格式

1. 在 **配置** 页上，选择 **示例审核格式**。
2. 在 **版本** 快速选项卡上，选择状态为 **草稿** 的版本 **1.2**。
3. 选择 **重定基本版本**。
4. 在 **目标版本** 字段中，保留 **示例审核模型** 基本模型的版本 **2**。
5. 选择 **确定** 以重定格式并将其与最近的数据模型更改保持一致。
6. 选择 **设计器**。
7. 在 **格式设计器** 页上，在左窗格中的格式结构树中，选择 **展开/折叠**。
8. 按照以下步骤添加新格式元素，以收集其交易在所生成报表中呈现的当事方的记录标识代码。

    1. 在格式结构树中，选择 **Report.Row.Trans** 序列元素。
    2. 选择 **添加**。
    3. 在 **添加** 对话框中，选择 **数据源 \> 项**。
    4. 在 **组件属性** 对话框的 **名称** 字段中，输入 **ID**。
    5. 在 **数据类型** 字段中，选择 **Int64**。
    6. 选择 **确定**。

    > [!NOTE]
    > **数据源 \> 项** 元素仅可用于在运行格式范围内执行内部计算和数据转换。 因此，通过添加此格式元素，您不会更改生成的文档的内容。

9. 按照这些步骤添加新格式元素以在生成的报表上输入当事方名称：

    1. 选择 **Report.Row** 序列元素。
    2. 选择 **添加**。
    3. 在 **添加** 对话框中，选择 **文本 \> 序列**。
    4. 在 **组件属性** 对话框的 **名称** 字段中，输入 **当事方**。
    5. 选择 **确定**。
    6. 选择 **Report.Row.Party** 序列元素。
    7. 选择 **添加**。
    8. 在 **添加** 对话框中，选择 **文本 \> 字符串**。
    9. 在 **组件属性** 对话框的 **名称** 字段中，输入 **名称**。
    10. 选择 **确定**。

10. 按照以下步骤添加新数据源，以收集其交易在所生成报表中呈现的当事方的记录标识代码：

    1. 在 **映射** 选项卡上，选择 **添加根**。
    2. 在 **添加数据源** 对话框中，选择 **函数 \> 数据集合**。
    3. 在 **数据集合数据源属性** 对话框中，在 **名称** 字段中输入 **PartyIds**。
    4. 在 **物料类型** 字段中，选择 **Int64**。
    5. 选择 **确定**。

11. 按照以下步骤添加新绑定，以收集其交易在所生成报表中呈现的当事方的记录标识代码：

    1. 在格式结构树中，选择 **Report.Row.Trans.Id** 数据项元素。
    2. 选择 **编辑公式**。
    3. 在 **公式设计器** 页面上，输入表达式 `PartyIds.Collect(model.Transaction.Party.RecId)`。
    4. 选择 **保存**，然后关闭 **公式设计器** 页面。

12. 按照这些步骤添加新绑定以在生成的报表上输入当事方名称：

    1. 在格式结构树中，选择 **Report.Party** 序列元素。
    2. 选择 **编辑公式**。
    3. 在 **公式设计器** 页面上，输入表达式 `model.Party(PartyIds.Result)`。
    4. 选择 **保存**，然后关闭 **公式设计器** 页面。
    5. 在格式结构树中，选择 **Report.Party.Name** 序列元素。
    6. 在 **映射** 选项卡上，选择 `model.Party.Name` 数据模型字段。
    7. 选择 **绑定**。

    ![“格式设计器”页面上调整的 ER 格式的结构。](./media/er-data-model-parameterized-calls-format2.png)

13. 选择 **保存**，然后关闭 **格式设计器** 页面。
14. 关闭 **模型到数据源映射** 页。
15. 在 **版本** 快速选项卡上，针对版本 **2.2**，选择 **更改状态** \> **完成**。 然后选择 **确定**。

### <a name="run-the-adjusted-format"></a>运行调整的格式

1. 在 **配置** 页面上，选择 **示例审核格式**，然后在操作窗格上选择 **运行**。
2. 在 **电子报表参数** 对话框的 **要包括的记录** 选项卡上，选择 **筛选器**。
3. 指定条件以选择 **PIV-110000004** 和 **INV-10000001** 凭证的税务交易。
4. 选择 **确定**。
5. 选择 **确定**。
6. 查看生成的单据，其中包含所选凭证的税务交易以及相应客户和供应商的名称。

    ![带税务交易和当事方名称的已生成单据的预览。](./media/er-data-model-parameterized-calls-output2.png)

7. 转到 **应付帐款** \> **供应商** \> **所有供应商**，并查看所选 **PIV-110000004** 凭证的详细信息，包括供应商名称。

    ![查看“所有供应商”和“发票日记帐”页面上的采购凭证详细信息。](./media/er-data-model-parameterized-calls-review1.gif)

8. 转到 **应收帐款** \> **客户** \> **所有客户**，并查看所选 **INV-10000001** 凭证的详细信息，包括客户名称。

    ![查看“所有客户”和“已过帐销售税”页面上的销售凭证详细信息。](./media/er-data-model-parameterized-calls-review2.gif)

有关此 ER 解决方案的此执行的更多详细信息，请使用 ER 内置的[性能跟踪](trace-execution-er-troubleshoot-perf.md)分析器。

## <a name="additional-resources"></a>其他资源

- [支持对计算字段类型的 ER 数据源执行参数化调用](er-calculated-field-type.md)
- [跟踪电子申报格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)
- [使用电子报告格式的数据收集数据源](er-data-collection-data-sources.md)
- [ValueInLarge ER 函数](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
