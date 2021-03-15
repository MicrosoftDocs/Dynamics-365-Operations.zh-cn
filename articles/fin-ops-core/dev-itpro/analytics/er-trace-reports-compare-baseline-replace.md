---
title: 对跟踪所生成 ER 报表结果并与基准值比较的改进
description: 本主题介绍 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.3（2019 年 6 月）中对 ER 基准功能的改进。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1c00a5d9e2804f6ec0f6cb4c544029a1235ee58d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093996"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>对跟踪所生成 ER 报表结果并与基准值比较的改进

[!include[banner](../includes/banner.md)]

本主题介绍已对电子申报 (ER) 框架基准功能所做的第一组改进。 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.3（2019 年 6 月）及更高版本中包含这些改进。

## <a name="automate-the-setting-of-baseline-rules"></a>自动执行基准规则的设置

[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题介绍如何配置 ER 框架以收集有关 ER 格式执行情况的信息和评估这些执行的结果。 本主题中的示例显示必须完成的步骤。

下面是其中的部分步骤：

- 运行 ER 格式以生成出站文件并存储在本地。
- 将本地存储的文件作为为 ER 格式添加的基准的附件添加。
- 为添加的基准配置基准规则。 此配置中包含以下步骤：

    - 指定用于生成出站文件的 ER 格式元素。
    - 选择引用生成的出站文件的附件。

> [!NOTE]
> 这些步骤必须手动执行，即使可以使用新的 ER 功能自动执行这些步骤也不例外。 若要了解有关此功能的详细信息，请完成以下示例。

## <a name="example-automate-the-setting-of-baseline-rules"></a>示例：自动执行基准规则的设置

若要完成此示例中的步骤，必须先完成前面的“为设计的 ER 格式添加新基准”部分[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题中的示例的步骤。

### <a name="review-added-baseline"></a>查看添加的基准

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 选择 **基准**。

    > [!NOTE]
    > 仅当为当前公司开启了 **以调试模式运行** ER 用户参数，操作窗格上的 **基准** 按钮才可用。

已为所选 **用于了解 ER 基准的格式** 格式添加了基准，但是尚未为此基准添加基准规则。

![“电子报告格式基准”页，还没有规则](media/GER-BaselineSample-AddBaseline2.PNG "“电子申报格式基准”页的屏幕截图")

### <a name="make-a-new-baseline-rule"></a>新建基准规则

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在树中，展开 **用于了解 ER 基准的模型**。
3. 在树中，选择 **用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。
4. 在 **版本** 快速选项卡上，选择 **运行**。
5. 在 **输入 ID** 字段中，输入 **1**。
6. 将 **创建基准文件** 选项设置为 **是**。
7. 选择 **确定**。
8. 选择 **基准**。

    ![“电子报告格式基准”页，选择了基准](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "“电子申报格式基准”页的屏幕截图")

    已将生成的出站文件自动附加到执行的 ER 格式的基准。 基准规则已自动添加到此基准，其中还包含对附加的文件的引用。

9. 在 **名称** 字段中，输入 **基准 1**。
10. 在 **文件名掩码** 字段中，输入 **.xml**。
11. 选择 **保存**。

### <a name="run-the-format"></a>运行格式

现在已准备就绪，可以从“运行设计的 ER 格式和检查日志以分析结果”部分开始，完成[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题中的示例中的步骤。

> [!NOTE]
> 在 **基准** 快速选项卡上删除自动添加的基准规则时，不会自动删除引用的附件。

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>配置基准，使其忽略持续改变的 ER 输出部分

如果已将 ER 格式设计为包含运行该格式时更改的信息，需要此格式才能使用 ER 基准功能将生成的结果与基准值进行比较。 例如，此信息可能是处理日期和时间，或不同格式中生成的文档的唯一标识符（全局唯一标识符 \[GUID\] 等）。 可通过新的 ER 功能配置基准规则，以便在为了将基准值与 ER 格式的执行结果进行比较而运行格式时忽略该格式的可更改元素。 若要了解有关此功能的详细信息，请完成以下示例。

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>示例：配置基准，使其忽略持续改变的 ER 输出部分

若要完成此示例中的步骤，必须先完成[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题中的示例的步骤。

### <a name="modify-a-configured-er-format"></a>修改配置的 ER 格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在树中，展开 **用于了解 ER 基准的模型**。
3. 在树中，选择 **用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。
4. 选择 **设计器**。
5. 在树中，选择 **输出\\文档**。
6. 选择 **添加**。
7. 在下拉对话框中的树中，选择 **XML\\属性**。
8. 在 **名称** 字段中，输入 **ProcessingDateTime**。
9. 选择 **确定**。
10. 在 **映射** 选项卡上的树中，选择 **输出\\文档\\ProcessingDateTime**。
11. 选择 **编辑公式**。
12. 在 **公式** 字段中，输入下面的表达式：**DATETIMEFORMAT(NOW(), "O")**
13. 选择 **保存**，然后选择 **测试**。
14. 再次选择 **测试** 重新测试配置的表达式。

    ![公式设计器页](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "“公式设计器”页的屏幕截图")

    > [!NOTE]
    > **测试结果** 选项卡显示配置的表达式只要被调用，都会返回不同的日期和时间值。

15. 关闭 **公式设计器** 页，然后选择 **保存**。

    ![“格式设计器”页面](media/GER-BaselineSample-FormatMappingDesign2.PNG "“格式设计器”页的屏幕截图")

16. 关闭 **格式设计器** 页。

### <a name="remove-an-existing-baseline-rule"></a>删除现有基准规则

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 选择 **基准**。
3. 在基准列表中，选择为 **用于了解 ER 基准的格式** 格式配置的基准。
4. 在 **基准** 快速选项卡上，选择 **删除** 以删除前面配置的基准规则。

![“电子报告格式基准”页，已删除](media/GER-BaselineSample-AddBaseline3.PNG "“电子申报格式基准”页的屏幕截图")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>为设计的 ER 格式的绑定定义替换项

1. 在 **配置** 页的 **替换** 快速选项卡上，选择 **选择组件**。
2. 在格式组件树中，展开 **输出**，展开 **输出\\文档**，然后选中 **输出\\文档\\ProcessingDateTime** 的复选框。
3. 选择 **确定**。

![“电子报告格式基准”页，组件](media/GER-BaselineSample-AddBaseline4.PNG "“电子申报格式基准”页的屏幕截图")

已将选择的 ER 格式组件添加到了 **替换** 快速选项卡上的组件列表中。 以调试模式运行基本 ER 格式时，将把该格式每个组件的绑定替换为 **绑定** 列中的绑定。 若要更改 **替换** 快速选项卡上列出的组件的默认绑定，请选择 **编辑**。

### <a name="make-a-new-baseline-rule"></a>新建基准规则

执行本主题前文“示例：自动执行基准规则的设置”部分中的步骤。 将有一个通知警告您已使用基准设置生成了出站文件，并且已强制替换了格式绑定。

![“配置”页上的通知](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "“配置”页上的通知的屏幕截图")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>禁止显示有关替换格式绑定的警告

通过设置特定 ER 参数，可禁止显示用于警示更换格式绑定的通知。 使用 Regression Suite Automation Tool 以无人值守模式替换格式绑定时，此项禁止显示可能很有用。 在此情况下，可以将警告视为正在运行的测试用例失败。

1. 在 **配置** 页操作窗格中的 **配置** 选项卡上，选择 **用户参数**。
2. 将 **禁止显示基准警告** 选项设置为 **是**，然后选择 **确定**。

### <a name="review-the-generated-baseline-file"></a>检查生成的基准文件

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 选择 **基准**。
3. 选择 **附件**。
    > [!NOTE]
    > 生成的文件中包含来自添加的基准规则中配置的绑定，而不是来自格式的绑定的处理日期和时间文本 (**"#"**)。
    
4. 关闭 **附件** 页。

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>运行设计的 ER 格式和检查日志以分析结果

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在树中，展开 **用于了解 ER 基准的模型**。
3. 在树中，选择 **用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。
4. 在 **版本** 快速选项卡上，选择 **运行**。
5. 在 **输入 ID** 字段中，键入 **1**。
6. 选择 **确定**。
7. 转到 **组织管理** \> **电子申报** \> **配置调试日志**。

执行日志中包含有关所生成文件与所配置基准的比较结果的信息。 此日志指示生成的文件与基准相等，即使执行的格式中包含绑定以在出站文件中输入持续改变的日期和时间值。

> [!NOTE]
> 尽管已通过用于强制替换格式的绑定的基准设置生成了出站文件，您仍然不会收到有关替换的警告。

## <a name="exchange-baseline-settings-between-environments"></a>在环境之间交换基准设置

### <a name="export-baseline-settings"></a>导出基准设置

可通过新的 ER 功能将所选 ER 格式的基准设置从当前环境导出并作为 XML 文件存储。 

若要导出基准设置，请在 **电子申报格式基准** 页上选择 **导出**。

### <a name="import-baseline-settings"></a>导入基线设置

可将导出的基准设置导入到其他环境中。 首先必须将该环境作为 ER 格式导入。 然后可以导入基准设置。

若要从本地存储的 XML 文件导入基准设置，请在 **电子申报格式基准** 页上选择 **导入**，然后选择 **浏览** 以选择该 XML 文件。

![导入基线设置对话框](media/GER-BaselineSample-ImportBaseline1.PNG "“导入基准设置”对话框的屏幕截图")

若要基于当前文档管理设置和所选文档类型从 Microsoft SharePoint Server 中存储的 XML 文件导入基准设置，请在 **电子申报格式基准** 页上选择 **从来源导入**。 然后选择文档类型和 XML 文件。 必须提前配置访问 SharePoint 文件夹所需文档类型。

![“从来源导入”对话框](media/GER-BaselineSample-ImportBaseline2.PNG "“从来源导入”对话框的屏幕截图")

> [!NOTE]
> 可使用任务录制器录制在 **从来源导入** 对话框中选择所需文档类型和文件名的步骤。 这样就可以将所需基准设置保存在 SharePoint Server 上，然后在使用 Regression Suite Automation Tool 运行自动化任务时通过播放任务录制自动导入。

## <a name="additional-resources"></a>其他资源

- [跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)
- [任务录制器资源](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]