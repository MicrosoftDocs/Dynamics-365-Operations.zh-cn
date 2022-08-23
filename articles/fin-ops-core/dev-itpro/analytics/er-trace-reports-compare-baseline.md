---
title: 跟踪生成的报表结果并将其与基准值进行比较
description: 本文介绍如何将生成的电子报告 (ER) 报表的结果与基准报表值进行比较。
author: kfend
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: f37405b548a321735abdd73da5c7cf3f4b00ff01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278757"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>跟踪生成的报表结果并将其与基准值进行比较。

[!include[banner](../includes/banner.md)]

可跟踪用于生成传出电子单据的电子申报 (ER) 格式的结果。 如果开启了跟踪生成（通过使用 **以调试模式运行** ER 用户参数），只要运行 ER 报表，都将在 ER 格式执行日志中生成一条新的跟踪记录。 生成的每条记录中包含以下详细信息：

- 验证规则生成的所有警告
- 验证规则生成的所有错误
- 生成的所有以跟踪记录附件形式存储的文件

可存储任何 ER 格式的单个基准申请表文件。 如果文件描述运行的报表的结果，则视为基准文件。 如果开启跟踪生成后运行的 ER 格式有基准文件，除了之前提到的详细信息，跟踪还将存储生成的电子单据与这个基准文件的比较结果。 只需单击一次，就还可以以单个 zip 文件的形式获取生成的电子单据及其基准文件。 然后可以通过使用 WinDiff 之类外部工具执行详细比较。

可以评估跟踪以分析生成的电子单据中是否包含预期内容。 当代码库已更改时（如当您迁移到了应用程序的新实例，安装了修补程序包或部署了代码修改时），可以在用户接受测试 (UAT) 环境中执行此项评估。 这样就可以确保评估不会影响 所用 ER 报表的执行。 对于许多 ER 报表来说，可以以无人值守模式执行评估。

若要了解此项功能，请播放 **ER 生成报表和比较结果（第 1 部分）** 和 **ER 生成报表和比较结果（第 2 部分）** 任务指南，这些指南属于 **7.5.4.3 测试 IT 服务/解决方案 (10679)** 业务流程，可以从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。 这些任务指南可以引导您完成配置 ER 框架以使用基准文件评估生成的电子单据这一过程。

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>示例：跟踪生成的报告结果并与基准值进行比较

此过程介绍如何配置 ER 框架以收集有关 ER 格式执行情况的信息，然后评估这些执行的结果。 此项评估中，将把生成的文档与其基准文件进行比较。 在此示例中，将为示例公司 Litware 公司创建所需 ER 配置。 此过程针对向其分配了系统管理员角色或电子申报开发人员角色的用户。 可使用任何数据集完成这些步骤。

为了完成此示例中的步骤，您必须首先在 RCS 中完成[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页 **配置提供程序** 部分中，验证是否列出了示例公司 Litware, Inc. 的配置提供程序，以及其是否标记为 **有效**。 如果没有看到此配置提供程序，请执行[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤。

### <a name="configure-document-management-parameters"></a>配置文档管理参数

1. 转到 **组织管理** \> **文档管理** \> **文档类型**，然后创建新文档类型存储基准文件。
2. 在 **类** 字段中，输入 **附加文件**。
3. 在 **组** 字段中，输入 **文件**。

![文档类型页面。](media/GER-BaselineSample-SetupDocumentType.PNG "“文档类型”页的屏幕截图")

> [!NOTE]
> 必须为计划用于 ER 基准功能的每个数据集配置同名新文档类型。

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>配置 ER 参数以开始使用基准功能

1. 在 **电子申报** 工作区的 **相关链接** 部分中，选择 **电子申报参数**。

    ![电子报告工作区。](media/GER-BaselineSample-ERWorkspace.PNG "“电子申报”工作区的屏幕截图")

2. 在 **附件** 选项卡上的 **基准** 字段中，输入或选择刚才创建的文档类型。

    ![“电子报告参数”页面的“附件”选项卡。](media/GER-BaselineSample-ERParameters.PNG "“电子申报”参数的屏幕截图")

3. 选择 **保存**，然后关闭 **电子申报参数** 页。

### <a name="add-a-new-er-model-configuration"></a>添加新 ER 模型配置

1. 在 **电子申报** 工作区的 **配置** 部分中，选择 **申报配置** 磁贴。
2. 在操作窗格中选择 **创建配置**。
3. 在下拉对话框的 **名称** 字段中，输入 **用于了解 ER 基准的模型**。
4. 选择 **创建配置** 以确认创建新的 ER 数据模型条目。

![“创建配置”对话框，添加新电子报告模型配置。](media/GER-BaselineSample-ModelAdd.PNG "“创建配置”下拉对话框的屏幕截图")

### <a name="design-a-data-model"></a>设计数据模型

1. 在 **配置** 页的操作窗格上，选择 **设计器**。
2. 选择 **新建**。
3. 在下拉对话框的 **名称** 字段中，输入 **根**。
4. 选择 **添加**。
5. 选择 **根引用**。
6. 选择 **确定**，然后选择 **保存**。
7. 关闭 **模型设计器** 页。
8. 选择 **更改状态**。
9. 选择 **完成**，然后选择 **确定**。

![配置页面。](media/GER-BaselineSample-ModelComplete.PNG "配置页的屏幕截图")

### <a name="add-a-new-er-format-configuration"></a>添加新 ER 格式配置

1. 在 **配置** 页的操作窗格上，选择 **创建配置**。
2. 在下拉对话框中的 **新建** 字段组中，选择 **基于数据模型“用于了解 ER 基准的模型”的格式** 选项。
3. 在 **名称** 字段中，输入 **用于了解 ER 基准的格式**。
4. 选择 **创建配置** 以确认创建新的 ER 格式条目。

![“创建配置”对话框，添加新电子报告格式配置。](media/GER-BaselineSample-FormatAdd.PNG "“创建配置”下拉对话框的屏幕截图")

### <a name="design-a-format"></a>设计格式

对于此示例，将创建简单的 ER 格式以生成 XML 文档。

1. 在 **配置** 页的操作窗格上，选择 **设计器**。
2. 选择 **添加根**。
3. 在下拉对话框中，执行以下步骤：

    1. 在树中，选择 **常见\\文件**。
    2. 在 **名称** 字段中，输入 **输出**。
    3. 选择 **确定**。

4. 选择 **添加**。
5. 在下拉对话框中，执行以下步骤：

    1. 在树中，选择 **XML\\元素**。
    2. 在 **名称** 字段中，输入 **文档**。
    3. 选择 **确定**。

6. 在树中，选择 **输出\\文档**。
7. 选择 **添加**。
8. 在下拉对话框中，执行以下步骤：

    1. 在树结构中，选择 **XML\\属性**。
    2. 在 **名称** 字段中，输入 **ID**。
    3. 选择 **确定**。

    ![“格式设计器”页面，在树中选择的 XML 属性。](media/GER-BaselineSample-FormatLayoutDesign.PNG "“格式设计器”页的屏幕截图")

9. 在 **映射** 选项卡上，选择 **删除**。
10. 选择 **添加根**。
11. 在下拉对话框的树中，选择 **常规\\用户输入参数**，然后执行以下步骤：

    1. 在 **名称** 字段中，输入 **ID**。
    2. 在 **标签** 字段中，输入 **输入 ID**。
    3. 选择 **确定**。

12. 在树中，选择 **输出\\文档\\Id**。
13. 选择 **绑定**，然后选择 **保存**。

![“格式设计器”页面，“映射”选项卡。](media/GER-BaselineSample-FormatMappingDesign.PNG "“格式设计器”页的屏幕截图")

配置的格式将根据设计的结构生成 XML 文件。 此 XML 中包含 **根** 元素，该元素的 **ID** 属性设置为用户在“ER 运行时”对话框中输入的值。

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>为设计的 ER 格式生成新的基准文件

1. 在 **配置** 页的 **版本** 快速选项卡上，选择 **运行**。
2. 在 **输入 ID** 字段中，输入 **1**。
3. 选择 **确定**。

    ![电子报表参数对话框。](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "“电子报表参数”对话框的屏幕截图")

4. 保存生成的 **out.Admin.xml** 文件的本地副本，以便后面将其用作此 ER 格式的基准。

    ![有关“配置”页面上生成文件的通知。](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "有关“配置”页上生成的文件的通知的屏幕截图")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>配置 ER 参数以使用基准功能

1. 在 **配置** 页操作窗格中的 **配置** 选项卡上，选择 **用户参数**。
2. 将 **以调试模式运行** 选项设置为 **是**。
3. 选择 **确定**。

![“用户参数”对话框。](media/GER-BaselineSample-ERUserParameters.PNG "“用户参数”对话框的屏幕截图")

### <a name="add-a-new-baseline-for-designed-er-format"></a>为设计的 ER 格式添加新基准

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在操作窗格上，选择 **基准**。

    ![“配置”页面上的“基准”按钮。](media/GER-BaselineSample-OpenBaselinePage.PNG "“配置”页上的“基准”按钮的屏幕截图")

3. 在操作窗格上，选择 **新建**。
4. 选择之前设计的 **用于了解 ER 基准的格式** ER 格式。
5. 选择 **保存**。

![“电子报告格式基准”页面。](media/GER-BaselineSample-AddBaseline.PNG "“电子申报格式基准”页的屏幕截图")

将为 **用于了解 ER 基准的格式** 格式的基准。

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>为添加的基准配置基准规则

1. 在 **电子申报格式基准** 页的操作窗格上，选择 **附件** 按钮（回形针符号）。
2. 在操作窗格上，选择 **新建** \> **文件**。 在 ER 参数中，之前应该已将 **文件** 文档类型选择为用于存储基准文件的文档格式。
3. 选择 **浏览**，然后选择您之前在运行配置的 ER 格式时生成的 **out.Admin.xml** 文件。

    ![“附件”页面。](media/GER-BaselineSample-UploadBaselineFile.PNG "附件页的屏幕截图")

4. 关闭 **附件** 页。
5. 在 **基准** 快速选项卡上，选择 **新建**。
6. 在 **名称** 字段中，输入 **基准 1**。
7. 在 **文件组件名称** 字段中，输入或选择 **输出**。 此值指示将把配置的基准与使用 **输出** 格式元素生成的文件进行比较。
8. 在 **文件名掩码** 字段中，输入 **\*.xml**。

    > [!NOTE]
    > 可定义文件名掩码。 如果定义文件名掩码，则仅当生成的输出文件的名称满足此掩码，才会使用基准记录评估生成的输出。

9. 如果仅当已登录特定公司的用户运行 **用于了解 ER 基准的格式** ER 格式时才应使用配置的基准，则在 **公司** 字段中选择这些公司。
10. 在 **基准** 字段中，输入或选择 **out.Admin** 附件。
11. 选择 **保存**。

![“电子报告格式基准”页面，选择了基准的“基准”快速选项卡。](media/GER-BaselineSample-SetupBaselineLine.PNG "“电子申报格式基准”页的屏幕截图")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>运行设计的 ER 格式和检查日志以分析结果

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在树中，展开 **用于了解 ER 基准的模型**，然后选择 **用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。
3. 在 **版本** 快速选项卡上，选择 **运行**。
4. 在 **输入 ID** 字段中，输入 **1**。
5. 选择 **确定**。
6. 转到 **组织管理** \> **电子申报** \> **配置调试日志**。

    ![具有同等基准的“电子报告运行日志”页面。](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "“电子申报运行日志”页的屏幕截图")

    > [!NOTE]
    > 执行日志中包含有关所生成文件与所配置基准的比较结果的信息。 在此示例中，日志指示生成的文件和基准相等。

7. 选择 **全部删除**。

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>运行设计的 ER 格式和检查日志以分析结果

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在树中，展开 **用于了解 ER 基准的模型**，然后选择 **用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。
3. 在 **版本** 快速选项卡上，选择 **运行**。
4. 在 **输入 ID** 字段中，输入 **2**。
5. 选择 **确定**。
6. 转到 **组织管理** \> **电子申报** \> **配置调试日志**。

    ![具有不同基准的“电子报告运行日志”页面。](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "“电子申报运行日志”页的屏幕截图")

    > [!NOTE]
    > 执行日志中包含有关所生成文件与所配置基准的比较结果的信息。 在此示例中，日志指示生成的文件和基准不同。

7. 选择 **比较**。

> [!NOTE]
> 将以 zip 文件的形式提供生成的文件和基准文件。 可使用 WinDiff 之类外部比较工具比较文件和检查不同之处。

## <a name="additional-resources"></a>其他资源

- [配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
