---
title: 配置电子报告格式以使用每个法人指定的参数
description: 本文说明如何配置电子报告 (ER) 格式以使用每个法人指定的参数。
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eb44422c4cdcc87989cdfb28dcd7d5cfea9002eb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858819"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>配置 ER 格式以使用每个法人指定的参数

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>概览

在您将要设计的许多电子报告 (ER) 格式中，您必须使用一组特定于您实例的每个法人的值（例如，用于筛选税收交易记录的一组税码）来筛选数据。 当前，以 ER 格式配置这种类型的筛选时，在 ER 格式的表达式中使用依赖于法人的值（例如，税码）来指定数据筛选规则。 因此，将 ER 格式设为特定于法人，要生成所需的报表，必须为必须运行 ER 格式的每个法人创建原始 ER 格式的派生副本。 必须对每种派生的 ER 格式进行编辑，以将特定于法人的值引入其中，每当原始（基本）版本更新，从测试环境中导出并在必须部署用于生产用途时导入到生产环境中等情况下，都将重定基本值。 因此，出于以下几个原因，此类已配置的 ER 解决方案的维护复杂且耗时：

-   法人越多，必须维护的 ER 格式配置就越多。
-   维护 ER 配置需要业务用户具有 ER 知识。

ER 应用程序特定的参数功能使高级用户可以以 ER 格式配置数据筛选，使其基于一组抽象规则。 可以将这组规则配置为可以使用 ER 格式的数据源。 然后，业务用户可以使用基于相应 ER 格式的设置，以及将由 ER 格式的数据源访问的当前法人数据自动生成的用户界面 (UI)，来指定 ER 框架之外的实际规则。 可以从 Dynamics 365 Finance (Finance) 实例的当前法人导出为 ER 格式指定的规则集。 然后可以将其导入与同一 ER 格式的一组规则相同的 Finance 实例或不同实例的另一个法人。

## <a name="prerequisites"></a>先决条件

要完成本文中的示例，您必须有权访问为与以下角色之一的 Finance 相同的租户预配的 Regulatory Configuration Services (RCS) 实例：

- 电子申报开发人员
- 电子申报功能顾问
- 系统管理员

我们建议您完成[支持对计算字段类型的 ER 数据源的参数化调用](er-calculated-field-type.md)一文中的步骤。 如果您已经完成了这些步骤，则可以跳过后面的 **将 ER 配置导入 RCS** 部分中的步骤。

## <a name="import-er-configurations-into-rcs"></a>将 ER 配置导入 RCS

下载并本地存储以下 ER 配置。

| **内容描述**                        | **文件名**                                        |
|------------------------------------------------|------------------------------------------------------|
| 示例 **ER 数据模型** 配置文件    | [用于了解参数化调用的模型.版本.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| 示例 **ER 元数据** 配置文件      | [用于了解参数化调用的元数据.版本.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| 示例 **ER 模型映射** 配置文件 | [用于了解参数化调用的映射.版本.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| 示例 **ER 格式** 配置             | [用于了解参数化调用的格式.版本.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

接下来，登录到您的 RCS 实例。

在此示例中，您将为 Litware, Inc 示例公司创建一个配置。 在完成此过程之前，必须完成 RCS 中[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)一文中的步骤。

1.  在默认仪表板中，选择 **电子申报**。
2.  选择 **申报配置**。
3.  按照以下顺序将您先前下载的 ER 配置导入到 RCS 中：数据模型、元数据、模型映射、格式。 对于每个 ER 配置，请按照下列步骤操作：

    1.  选择 **交换**。
    2.  选择 **从 XML 文件加载**。
    3.  选择 **浏览** 以 XML 格式选择所需 ER 配置的文件。
    4.  选择 **确定**。

## <a name="review-the-er-solution-that-is-provided"></a>查看提供的 ER 解决方案

1.  在配置树中，展开 **用于了解参数化调用的模型** 项的目录。
2.  选择 **用于了解参数化调用的格式** 项。
3.  选择 **设计器**。
4.  选择 **展开/折叠**。

    **用于了解参数化调用的格式** ER 格式旨在生成 XML 格式的税报表，其显示多个征税级别（正常、减税和免税）。 每个级别都有不同数量的详细信息。

    ![多种级别的 ER 格式，用于学习参数化调用的格式。](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  在 **映射** 选项卡上，展开 **模型**、**数据** 和 **汇总** 项目。

    **Model.Data.Summary** 数据源返回税收交易记录的列表。 这些交易记录按税码进行汇总。 对于此数据源，已配置 **Model.Data.Summary.Level** 计算字段以返回每个汇总记录的征税级别的代码。 对于在运行时可以从 **Model.Data.Summary** 数据源中检索到的任何税码，计算字段将作为文本值返回征税级别代码（**正常**、**减税**、**免税** 或 **其他**）。 **Model.Data.Summary.Level** 计算字段用于筛选 **Model.Data.Summary** 数据源的记录，并通过使用 **Model.Data2.Level1**、**Model.Data2.Level2** 和 **Model.Data2.Level3** 字段来在表示征税级别的每个 XML 元素中输入筛选后的数据。

    ![税务交易的 Model.Data.Summary 数据源列表。](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    已配置 **Model.Data.Summary.Level** 计算字段，使其包含 ER 表达式。 税码（**VAT19**、**InVAT19**、**VAT7**、**InVAT7**、**THIRD** 和 **InVAT0**）将硬编码到此配置中。 因此，此 ER 格式取决于配置了这些税码的法人。

    ![具有硬编码税码的 Model.Data.Summary.Level 计算字段。](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    要为每个法人支持一组不同的税码，您必须执行以下步骤：

    - 为每个法人创建 ER 格式的派生版本。
    - 根据法人设置，在 **Model.Data.Summary.Level** 计算字段中更新税码。

6.  关闭 **格式设计器** 页。

## <a name="create-a-derived-format"></a>创建派生格式

接下来，您将使用 ER 应用程序特定的参数功能，以单个 ER 格式为每个法人支持一组不同的税码。

1.  在配置树中，展开 **用于了解参数化调用的模型** 项的目录。
2.  选择 **用于了解参数化调用的格式** 项。
3.  选择 **创建配置**。
4.  选择 **从以下名称派生: 用于了解参数化调用的格式，Microsoft** 选项。
5.  在 **名称** 字段中，输入 **用于了解如何查找 LE 数据的格式**。
6.  选择 **创建配置**。

## <a name="configure-a-derived-format"></a>配置派生格式

### <a name="add-a-format-enumeration"></a>添加格式枚举

接下来，您将添加一个新的 ER 格式枚举。 此格式枚举的值将提供给业务用户，业务用户将为 ER 格式中使用的各个征税级别指定与法人相关的税码集。

1.  选择 **设计器**。
2.  选择 **格式枚举**。
3.  选择 **添加**。
4.  在 **名称** 字段中，输入 **征税级别列表**。
5.  选择 **保存**。
6.  在 **格式枚举值** 选项卡上，选择 **添加**。
7.  在 **名称** 字段中，输入 **正常税收**。
8.  再次选择 **添加**。
9.  在 **名称** 字段中，输入 **减税**。
10. 再次选择 **添加**。
11. 在 **名称** 字段中，输入 **免税**。
12. 再次选择 **添加**。
13. 在 **名称** 字段中，输入 **其他**。

    ![格式枚举页面上的新记录。](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    由于业务用户可能使用不同的语言来指定与法人相关的税码集，因此我们建议您将此枚举的值翻译为在 Finance 中为那些用户配置为首选语言的语言。

14. 选择 **免税** 记录。
15. 单击 **标签** 字段。
16. 选择 **翻译**。
17. 在 **文本翻译** 窗格中的 **标签 ID** 字段中，输入 **LBL_LEVELENUM_NO**。
18. 在 **语言为默认语言的文本** 字段中，输入 **免税**。
19. 在 **语言** 字段中，选择 **DE**。
20. 在 **已翻译的文本** 字段中，输入 **keine Besteuerung**。
21. 选择 **翻译**。

    ![文本翻译滑出。](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. 选择 **保存**。
23. 关闭 **格式枚举** 页。

### <a name="add-a-new-lookup-data-source"></a>添加新的查找数据源

接下来，您将添加一个新的数据源，以指定业务用户将如何指定与法人相关的规则，以为每个汇总的交易记录识别正确的征税级别。

1.  在 **映射** 选项卡上，选择 **添加**。
2.  选择 **格式枚举\查找**。

    您刚刚确定，业务用户为征税级别识别指定的每个规则将返回 ER 格式枚举的值。 请注意，除了 **格式枚举** 块外，还可以在 **数据模型** 和 **Dynamics 365 for Operations** 块下访问 **查找** 数据源类型。 因此，ER 数据模型枚举和应用程序枚举可用于指定为该类型的数据源返回的值的类型。 若要了解有关 **查找** 数据源的详细信息，请参阅[配置查找数据源以使用 ER 应用程序特定的参数功能](er-lookup-data-sources.md)。
    
3.  在 **名称** 字段中，输入 **选择器**。
4.  在 **格式枚举** 字段中，选择 **征税级别列表**。

    您指定，对于此数据源中指定的每个规则，商务用户必须选择 **征税级别列表** 格式枚举的值之一作为返回值。
    
5.  选择 **编辑查找**。
6.  选择 **列**。
7.  展开 **模型** 项。
8.  展开 **数据** 项。
9.  展开 **税务** 项。
10. 选择 **Model.Data.Tax.Code** 项。
11. 选择 **添加** 按钮（向右箭头）。

    ![列滑出。](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    您刚才指定了，对于此数据源中指定的用于征税级别识别的每个规则，业务用户必须选择一个税码作为条件。 业务用户可以选择的税码列表将由 **Model.Data.Tax** 数据源返回。 因为此数据源包含 **名称** 字段，所以将在呈现给业务用户的查找中为每个税码值显示税码的名称。
    
12. 选择 **确定**。

    ![查找设计器页面。](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    业务用户可以添加多个规则作为此数据源的记录。 每个记录将由一个行代码编号。 规则将按照行号增加的顺序进行评估。

    因为您选择了 **税码** 字段作为此查找数据源中规则的条件，并且由于 **税码** 被设置为 **字符串** 数据类型的字段，所以将在运行时对每个规则进行评估，方法是将传递给数据源的税码与数据源的记录中定义的税码进行比较。

    找到满足配置条件的规则时，此数据源将返回在 **查找结果** 字段中定义的规则的查找值。 如果未找到任何规则，则会引发异常以通知用户当前数据源无法返回正确的值。

13. 选择 **保存**。
14. 关闭 **查找设计器** 页。
15. 选择 **确定**。

    请注意，您添加了一个新的数据源，该数据源将返回征税级别作为任何税码的 **征税级别列表** 格式枚举的值，该税码将作为 **字符串** 数据类型的 **代码** 参数的参数传递给数据源。
    
    ![具有新数据源的格式设计器页面。](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    对已配置规则的评估取决于为定义这些规则的条件而选择的字段的数据类型。 当您选择一个配置为 **数字** 或 **日期** 数据类型的字段的字段时，条件将不同于先前针对 **字符串** 数据类型描述的条件。 对于 **数字** 和 **日期** 字段，必须将规则指定为值的范围。 当传递到数据源的值在配置的范围内时，将认为规则的条件已满足。
    
    下图显示了此类设置的示例。 除了 **字符串** 数据类型的 **Model.Data.Tax.Code** 字段外，**实数** 数据类型的 **Model.Tax.Summary.Base** 字段用于指定查找数据源的条件。
    
    ![具有其他列的查找设计器页面。](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    因为为此查询数据源选择了 **Model.Data.Tax.Code** 和 **Model.Tax.Summary.Base** 字段，所以将以以下方式配置此数据源的每个规则：
    
    -   在显示的列表中，必须选择 **征税级别列表** 格式枚举的值作为返回值。
    -   必须输入税码作为此规则的条件。 仅适用于 **Model.Data.Tax** 数据源提供的税码。
    -   必须将税金基准额的最小值和最大值输入为此规则的条件。

    这是在运行时如何评估此数据源的每个规则的方法：
    -   传递给此数据源的 **字符串** 数据类型的代码是否等于规则的税码？
    -   传递给此数据源的 **实数** 数据类型的值是否在特定的最小值和最大值之间？

    当两个条件都满足时，将认为规则适用。

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>翻译添加的查找数据源的标签

因为业务用户可能使用不同的语言来指定与法人相关的税码集，所以我们建议您翻译添加的任何查找数据源的标签，以便在相应页面上以每个用户的首选语言显示。

1.  选择 **Model.Data.Selector** 数据源。
2.  选择 **编辑**。
3.  单击 **标签** 字段。
4.  选择 **翻译**。
5.  在 **文本翻译** 窗格中的 **标签 ID** 字段中，输入 **LBL_SELECTOR_DS**。
6.  在 **语言为默认语言的文本** 字段中，输入 **按税码选择征税级别**。
7.  在 **语言** 字段中，选择 **DE**。
8.  在 **已翻译的文本** 字段中，输入 **Steuerebene für Steuerkennzeichen auswählen**。
9.  选择 **翻译**。
10. 选择 **确定**。

    ![数据源属性滑出。](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>添加一个新字段以使用配置的查找

1.  展开 **Model.Data** 项。
2.  选择 **Model.Data.Summary** 项。
3.  选择 **添加**。
4.  选择 **Functions/Calculated field**。
5.  在 **名称** 字段中，输入 **LevelByLookup**。
6.  选择 **编辑公式**。
7.  在 **公式字段** 中，输入 **Model.Selector(Model.Data.Summary.Code)**.
8.  选择 **保存**。

    ![将 Model.Selector(Model.Data.Summary.Code) 添加到公式设计器页面。](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  关闭 **公式编辑器** 页。
10. 选择 **确定**。

    ![添加了新公式的格式设计器页面。](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    请注意，您添加的 **LevelByLookup** 计算字段将返回征税级别，作为每个汇总的税收交易记录的 **征税级别列表** 格式枚举的值。 记录的税码将传递到 **Model.Selector** 查找数据源，此数据源的规则集将用于选择正确的征税级别。

### <a name="add-a-new-format-enumeration-based-data-source"></a>添加新的基于格式枚举的数据源

接下来，您将添加一个新数据源，该数据源引用您之前添加的格式枚举。 稍后将在 ER 格式表达式中使用此数据源的值。

1.  选择 **添加根**。
2.  选择 **格式枚举\枚举**。
3.  在 **名称** 字段中，输入 **TaxationLevel**。
4.  在 **格式枚举** 字段中，选择 **征税级别列表**。
5.  选择 **保存**。

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>修改现有字段以开始使用查找

接下来，您将修改现有的计算字段，以使其使用配置的查找数据源根据税码返回正确的征税级别值。

1.  选择 **Model.Data.Summary.Level** 项。
2.  选择 **编辑**。
3.  选择 **编辑公式**。

    请注意，**Model.Data.Summary.Level** 字段的当前表达式包括以下硬编码的税码：
    
    CASE（@.Code、“VAT19”、“Regular”、“InVAT19”、“Regular”、“VAT7”、“Reduced”、“InVAT7”、“Reduced”、“THIRD”、“None”、“InVAT0”、“None”、“Other”）

4.  在 **公式** 字段中，输入 **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**。

    ![ER 操作设计器页面。](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    请注意，**Model.Data.Summary.Level** 字段的表达式现在将基于当前记录的税码和商务用户在 **Model.Data.Selector** 查找数据源中配置的规则集返回征税级别。
    
5.  选择 **保存**。
6.  关闭 **公式设计器** 页。
7.  选择 **确定**。
8.  选择 **保存**。
9.  关闭 **格式设计器** 页。

## <a name="complete-the-draft-version-of-a-derived-format"></a>完成派生格式的草稿版本

1.  在 **版本** 快速选项卡上，选择 **更改状态**。
2.  选择 **完成**。
3.  选择 **确定**。

## <a name="export-completed-version-of-modified-format"></a>导出修改后格式的完整版本

1.  在配置树中，选择 **用于了解如何查找 LE 数据的格式** 项目。
2.  在 **版本** 快速选项卡上，选择状态为 **已完成** 的记录。
3.  选择 **交换**。
4.  选择 **导出为 XML 文件**。
5.  选择 **确定**。
6.  Web 浏览器下载 **Format to learn how to look up LE data.xml** 文件。 将此文件存储在本地。

对 **用于了解如何查找 LE 数据的格式** 的父项重复本部分中的步骤，并在本地存储以下文件：

-   Format to learn parameterized calls.xml
-   Mapping to learn parameterized calls.xml
-   Model to learn parameterized calls.xml

若要了解如何使用已配置的 **用于了解如何查找 LE 数据的格式** ER 格式来设置法人相关的税码集，以按不同征税级别筛选税收交易，请完成[为每个法人设置 ER 格式的参数](er-app-specific-parameters-set-up.md)一文中的步骤。

## <a name="additional-resources"></a>其他资源

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[为每个法人设置电子报告格式的参数](er-app-specific-parameters-set-up.md)

[配置查找数据源以使用 ER 应用程序特定的参数功能](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
