---
title: 设计 ER 配置以填写 PDF 模板
description: 本主题介绍如何设计电子申报 (ER) 格式以填写 PDF 模板。
author: NickSelin
manager: AnnBe
ms.date: 04/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 13744df950040056ba03a3847d84f93e266ea6c3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181442"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>设计 ER 配置以填写 PDF 模板

[!include[banner](../includes/banner.md)]

本主题中的过程为示例，用于演示**系统管理员**角色或**电子申报开发人员**角色的用户如何通过将可填写 PDF 文档用作报表模板来配置用于生成 PDF 文件格式报表的电子申报 (ER) 格式。 Dynamics 365 Finance 或 Regulatory Configuration Services (RCS) 的任何公司都可以执行这些步骤。

## <a name="prerequisites"></a>先决条件

首先，您必须具有下列访问权限类型之一，具体取决于您用于完成本主题中的过程的服务。

- 访问 Finance 的以下其中一个角色：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 访问 RCS 的以下其中一个角色：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

还必须完成[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。

最后，必须从 [CustomerSource](https://go.microsoft.com/fwlink/?linkid=874111) 下载下列文件。

| 内容描述                       | 文件名                                     |
|-------------------------------------------|-----------------------------------------------|
| 报表第一页的模板 | [IntrastatReportTemplate1.pdf](https://mbs.microsoft.com/Files/public/CS)                  |
| 报表其他页的模板    | [IntrastatReportTemplate2.pdf](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatReportTemplate2.pdf)                  |
| 示例 ER 格式 - PDF                          | [Intrastat report (PDF).version.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatreportPDFversion11.xml)        |
| 示例 ER 格式 - Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatimportfromExcelversion11.xml) |
| 示例数据集                            | [Intrastat sample data.xlsx](https://mbs.microsoft.com/Files/public/CS/AX/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>设计 ER 格式配置

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>访问 Microsoft 提供的配置列表

1. 转到**组织管理 \> 工作区 \> 电子申报**。
2. 确保提供商 **Litware 公司**可用且标记为有效。
3. 在 **Microsoft** 提供商的磁贴中，选择**存储库**。

    > [!NOTE]
    > 如果已存在类型为 **LCS** 的存储库，请跳过此过程的其余步骤。

4. 选择**添加**。
5. 在下拉对话框中的**配置存储库类型**字段组中，选择 **LCS** 选项。
6. 选择**创建存储库**。
7. 选择**确定**。

### <a name="get-the-model-configurations-provided-by-microsoft"></a>获取 Microsoft 提供的模型配置

1. 在**配置存储库**页左侧，选择**显示筛选器**按钮（漏洞符号）。
2. 在**类型**字段中添加 **LCS** 值的筛选器，然后使用**开头为**运算符。
3. 选择**应用**。
4. 选择**打开**。
5. 在树中，选择**内部统计模型**。
6. 在**版本**快速选项卡中，选择版本 **1**。

    > [!NOTE]
    > 如果**版本**快速选项卡上的**导入**按钮不可用，请跳过此过程中的其余步骤。

7. 选择**导入**。
8. 选择**是**确认导入所选版本的**内部统计模型**模型配置。

### <a name="create-a-new-format-configuration"></a>创建新的格式配置

1. 在**电子申报**工作区中，选择**报告配置**磁贴。
2. 在树中，选择**内部统计模型**。
3. 选择**创建配置**。

    > [!NOTE]
    > 如果**创建配置**按钮不可用，必须在可从**电子申报**工作区打开的**电子申报参数**页中开启设计模式。

4. 在下拉对话框中的**新建**字段组中，选择**基于数据模型内部统计的格式**选项。
5. 在**名称** 字段中，输入 **Intrastat report (PDF)**。
6. 在**说明**字段中，输入 **PDF 格式的内部统计报表**。

    > [!NOTE]
    > 将自动输入有效配置提供商。 此提供商可以维护此配置。 尽管其他提供商可以使用此配置，但不能对其进行维护。

7. 可选：在**格式类型**字段中，可选择电子文档的具体格式。 如果选择 **PDF**，设计时，ER Operations 设计器将仅提供仅适用于以 PDF 格式生成的文档的格式元素（**PDF\文件**、**PDF\PDF 合并器**等）。 如果将此字段留空，将在设计时添加第一个格式元素期间在 ER Operations 设计器中指定电子文档的格式。 例如，如果添加 **Excel\File** 作为第一个格式元素，ER Operations 设计器将仅提供仅适用于以 Excel 格式生成的文档的格式元素（**Excel\单元格**、**Excel\区域**等）。 格式。
8. 选择**创建配置**。

将创建新的 ER 格式配置。 可使用此配置的草稿版本来存储为了生成 PDF 格式的电子文档而设计的 ER 格式组件。

### <a name="design-the-format-of-an-electronic-document"></a>设计电子单据的格式

接下来，在创建的 ER 格式配置中，将设计用于生成 PDF 格式的**内部统计控件**报表的 ER 格式。 此报表第一页显示报表摘要和报告的外贸交易记录的详细信息。 其他页必须仅显示报告的外贸交易记录的详细信息。 由于生成的报表页必须采用不同布局，所以将在 ER 格式中使用 PDF 格式的两个不同模板。

在任何 PDF 查看器中，打开下载的 PDF 模板。 请注意，每个模板中包含多个必须填写的字段。 在每个模板中，外贸交易记录的详细信息表示为 42 行，每行九个字段。 行号在每个字段名称的默认显示（如**日期 1**…**日期 42** 和 **商品 1**…**商品 42**）。

下图显示报表第一页的 PDF 模板。

![模板 1](media/rcs-ger-filloutpdf-template1.png)

下图显示报表其他页的 PDF 模板。

![模板 2](media/rcs-ger-filloutpdf-template2.png)

1. 在**配置**页上，选择**设计器**。
2. 选择**添加根**。
3. 在下拉对话框中的树中，选择 **PDF \> PDF 合并器**。

    如果格式的根元素选择 **PDF 合并器**元素，则在运行时生成的所有 PDF 文档都将合并为一个最终的 PDF 文档。 如果仅需要一个 PDF 模板来使用您设计的 ER 格式生成需要的所有文档，根元素可选择 **PDF 文件**。

4. 在**名称**字段中，输入**输出**。
5. 在**语言首选项**字段中，选择**用户首选项**。 将使用运行报表的用户的首选语言生成报表。
6. 在**区域性首选项**字段中，选择**用户首选项**。 将根据运行报表的用户的首选区域设置来设置报表页中显示的值和日期。
7. 选择**确定**。
8. 在操作窗格上的**导入**选项卡上，选择**从 PDF 导入**。

    将可填写 PDF 文档作为此 ER 格式的模板导入时，将根据导入的 PDF 文档的结构以设计的格式自动创建所有必需的 ER 格式元素（**PDF 文件**、**字段组**和**字段**元素）。

9. 选择**浏览**。 导航到并选择之前作为先决条件下载的 **IntrastatReportTemplate1.pdf** 文件。
10. 选择**确定**。

    将加载所选文件，并填写**从 PDF 导入**对话框中的**模板**字段。

11. 将**组字段**选项设置为**是**。 如果所选 PDF 文档中包含任何字段组，将使用这些字段组来为创建的 ER 格式元素分组。 将为此目的创建一个**字段组**格式元素。

    如果此选项设置为**否**，将把所需 ER 格式元素创建为创建的 **PDF 文件**格式元素下嵌套的元素的简单列表。

12. 选择**确定**。

    ![“从 PDF 导入”对话框](media/rcs-ger-filloutpdf-importtemplate.png)

13. 在树中，展开**输出**。

    请注意，已自动创建了 **PDF 文件**组件来管理运行时生成的报表的第一页的创建。

14. 在树中，展开**输出 \> PDF 文件**。

    请注意，已根据前面导入的可填写 PDF 文档的结构使用此 Er 格式自动创建了结构化的格式元素列表。

15. 在树中，选择**输出 \> PDF 文件**。
16. 在**名称**字段中，输入**第 1 页**。

    此格式将用于生成**内部统计控件**报表的第一页。 此页将显示报表摘要和外贸交易记录的详细信息。

    如果使**语言首选项**字段留空，**PDF 合并器**父元素的**语言首选项**设置将决定通过使用此格式元素生成的报表的语言。 可选择其他值替换父元素的设置。

    如果使**区域性首选项**字段留空，**PDF 合并器**父元素的**区域性首选项**设置将决定通过使用此格式元素生成的报表的语言。 区域设置决定报表页中的值和日期的格式。 可选择其他值替换父元素的设置。

17. 在操作窗格中，选择**导入**选项卡。请注意，**从 PDF 更新**按钮已变为可用于所选格式元素 **PDF 文件**。

    可使用此按钮将更新后的 PDF 模板导入到编辑后的格式。 导入更新后的 PDF 模板时，将相应更改格式元素列表：

    - 对于更新后的 PDF 模板中的任何新字段，将使用编辑后的 ER 格式创建新的格式元素。
    - 如果更新后的 PDF 模板中不再包含与编辑后的 ER 格式的任何现有格式元素对应的字段，将从 ER 格式删除这些格式元素。

18. 在**格式**选项卡中，选择**附件**。

    请注意，导入的 PDF 文档已附加到编辑后的 ER 格式。

    ![PDF 附件预览](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. 继续设计此格式，方法是导入第二个 PDF 模板，向数据源添加必要的绑定等。
20. 选择**保存**。
21. 关闭该页面。
22. 选择**删除**。
23. 选择**是**。

若要了解如何使用 **PDF 合并器**、**PDF 文件**、**字段组**和**字段**格式元素生成 PDF 格式的文档，可导入和分析示例 ER 格式。

### <a name="import-the-format-configuration"></a>导入格式配置

接下来，将导入之前下载的示例 ER 格式以生成 PDF 格式的**内部统计控件**报表。 报表第一页显示报表摘要和报告的外贸交易记录的详细信息。 其他页必须仅显示报告的外贸交易记录的详细信息。

1. 在**配置**页中，选择**交换 \> 从 XML 文件加载**。
2. 选择**浏览**。 导航到并选择之前作为先决条件下载的 **Intrastat report (PDF).version.1.1.xml** 文件。
3. 选择**确定**。

## <a name="analyze-the-format-configuration"></a>分析格式配置

### <a name="format-layout"></a>格式布局

1. 在**配置**页上的树中，选择**内部统计模型 \> 内部统计报表 (PDF)**。
2. 选择**设计器**。
3. 选择**显示详细信息**。
4. 在树中，展开**输出：PDF 合并器**。

    请注意，此 ER 格式中包含两个 **PDF 文件**元素，其中每个使用一个不同的 PDF 模板。 一个模板用于生成 PDF 格式的报表第一页，另一个模板用于生成其他页。

5. 在树中，展开**输出：PDF 合并器 \> 第 1 页：PDF 文件 (IntrastatReportTemplate1)**。
6. 在树中，展开**输出：PDF 合并器 \> 第 N 页：PDF 文件 (IntrastatReportTemplate2)**。

    请注意，由于这两个 PDF 模板的内容不同，所以这两个 **PDF 文件**元素的嵌套格式元素的结构也不同。

### <a name="format-mapping"></a>格式映射

1. 在**格式设计器**页中，选择**映射**选项卡。
2. 在树中，展开**分页 \> 页面**。

    ![其中展开了模型树的配方设计器页](media/rcs-ger-filloutpdf-reviewformat.png)

    注意以下详细信息：

    - **PDF 文件**类型的**输出 \> 第 1 页**格式元素为绑定到任何数据源，并且此格式元素的 **Enabled** 表达式为空。 因此，运行时生成单个 PDF 文档期间，**IntrastatReportTemplate1** PDF 模板仅填充一次。
    - **PDF 文件**类型的**输出 \> 第 N 页**格式元素绑定到**记录列表**类型的 **Paging.PageN** 数据源，并且此格式元素的 **Enabled** 表达式为空。 因此，运行时生成单个 PDF 文档期间，将为绑定的记录列表中的每个记录填充 **IntrastatReportTemplate2** PDF 模板。
    - 因为**第 1 页：PDF 文件**和**第 N 页：PDF 文件**格式元素是**输出：PDF 合并器**格式元素的子代，所以将把填写的所有 PDF 文档合并为一个最终的 PDF 文档。
    - **Paging.Page1** 和 **Paging.PageN** 数据源配置为 **Paging.Pages** 数据源中的记录的筛选器。 配置此数据源是为了将整组外贸交易记录拆分为批次。 每个批次最多包含 42 条记录。 下面的 ER 表达式用于将交易记录拆分为批次：

        SPLITLIST(Totals.CommodityRecord,42)

    - **Paging.Pages** 数据源中包含 **Paging.Pages.Enumerated** 元素，用于返回批次中包含的每个记录的详细信息。 这些详细信息中包含该记录在当前批次（**Paging.Pages.Enumerated.Number** 字段）中的序号。 **Paging.Pages.Enumerated.Number** 字段在 **PDF 字段**格式元素的 **Name** 表达式中用于动态生成基于批次中的交易记录号的字段名。 然后将生成的字段名用于填写所用 PDF 模板中的正确 PDF 字段。
    - **PDF 组**类型的**输出 \> 第 N 页 \> 详细信息 2** 格式元素绑定到**记录列表**类型的 **Paging.PageN.Enumerated** 数据源（如果使用的是**相对路径**视图模式，则为 **\@.Enumerated**）。 因此，在运行时，将为绑定的记录列表中的每个记录填写此 PDF 组的嵌套元素。 这样，最终在为 **Paging.PageN.Enumerated** 列表的 42 个记录中的第 N 个填写以下 PDF 字段时，将生成单个 PDF 行：日期 N、方向 N、商品 N 等。因此，在这方面，此**字段组**格式元素的行为类似 **XML \> 序列**和**文本 \> 序列**格式元素的行为类似。

3. 在树中，展开**输出 \> 第 N 页\> 详细信息 2**。
4. 在树中，选择**输出 \> 第 N 页\> 详细信息 2 \> PageFooter**。

    请注意，此格式元素的**名称**属性定义为 **PageFooter**。 另请注意，格式元素的 **Name** 表达式为空。

5. 在树中，选择**输出 \> 第 N 页\> 详细信息 2 \> Correction 1**。

    请注意，此格式元素的**名称**属性定义为 **Correction 1**。 另请注意，格式元素的 **Name** 表达式定义为 **Paging.FldName("Correction",\@.Number)**。

![其中选择了映射的格式设计器](media/rcs-ger-filloutpdf-reviewformat2.png)

请注意，**字段**格式元素用于填写定义为 **PDF 文件**格式父元素的模板的可填写 PDF 文档的单个字段。 **PDF 文件**格式元素或其嵌套元素（如果有任何嵌套元素）的绑定指定在相应 PDF 字段中输入的值。 **字段**格式元素的不同属性可用于指定单个格式元素填充哪个 PDF 字段：

- **格式**选项卡上的格式元素的 **Name** 属性
- **映射**选项卡上的格式元素的 **Name** 表达式

因为这两个属性是**字段**格式元素的可选属性，所以将把下列规则应用于目标 PDF 字段：

- 如果 **Name** 属性为空，而 **Name** 表达式在运行时返回空字符串，则在运行时引发异常以通知用户在正用于填写 PDF 文档的 PDF 模板中无法找到 PDF 字段。
- 如果定义了 **Name** 属性，并且 **Name** 表达式为空，则将填写与格式元素的 **Name** 属性同名的 PDF 字段。
- 如果定义了 **Name** 属性，并且配置了 **Name** 表达式，则将填写与格式元素的 **Name** 表达式返回的值同名的 PDF 字段。

> [!NOTE]
> 可按照下面的方法选择的内容填写 PDF 复选框：
>
> - 如果相应的**字段**格式元素绑定到值为 **True** 的**布尔值**数据类型的数据源字段
> - 如果相应的**字段**格式元素中包含绑定到文本值为 **1**、**True** 或 **Yes** 的数据源字段的嵌套**字符串**格式元素

## <a name="run-the-format-configuration"></a>运行格式配置

### <a name="import-the-format-configuration"></a>导入格式配置

接下来，将加载**内部统计（从 Excel 导入）** 示例 ER 格式。 此格式用于解析用户选择来模拟外贸交易记录的 Microsoft Excel 工作簿。

1. 在**配置**页中，选择**交换 \> 从 XML 文件加载**。
2. 选择**浏览**。 导航到并选择之前作为先决条件下载的 **Intrastat (import from Excel).version.1.1.xml** 文件。
3. 选择**确定**。
4. 在树中，选择**内部统计模型 \> 内部统计（从 Excel 导入）**。
5. 选择**编辑**。
6. 将**模型映射的默认值**选项设置为**是**。

    > [!NOTE]
    > 如果之前将**内部统计模型**配置或**内部统计模型**配置下嵌套的另一个配置的**模型映射的默认值**选项设置为**是**，请将此选项设置为**否**。

    如果**模型映射的默认值**选项设置为**是**，则将导入的**内部统计（从 Excel 导入）** ER 格式指定为**内部统计报表 (PDF)** 格式配置的默认数据源。 然后，在运行**内部统计报表 (PDF)** 格式配置时，**内部统计（从 Excel 导入）** ER 格式解析的 Excel 工作簿的内容将模拟必须报告的外贸交易记录。 下图显示了一个 Excel 工作簿的示例。

    ![包含示例数据的 Excel 工作簿](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>运行格式配置

1. 在**配置**页上的树中，选择**内部统计模型 \> 内部统计报表 (PDF)**。
2. 选择**运行**。
3. 选择**浏览**。 导航到并选择之前作为先决条件下载的 **Intrastat sample data.xlsx** 文件。
4. 选择**确定**。
5. 在**报表方向**字段中，选择**双向**以填写来自生成的 PDF 报表中导入的 Excel 工作簿内的所有交易记录。
6. 选择**确定**。
7. 查看生成的 PDF 文档。

下图显示生成的报表的第一页的示例。

![生成的报表的第一页](media/rcs-ger-filloutpdf-generatedreport.png)

下图显示生成的报表的另一页的示例。

![生成的报表的另一页](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a>其他资源

- [ER 设计以 OPENXML 格式生成报表的配置](tasks/er-design-reports-openxml-2016-11.md)
- [设计 ER 配置以生成 Microsoft Word 格式的报表](tasks/er-design-configuration-word-2016-11.md)
