---
title: 设计 ER 格式以使用页面页眉或页脚中的嵌入图像生成采用 Excel 格式的报表
description: 本主题说明如何使用电子报告 (ER) 生成具有在页面页眉或页脚中嵌入的图像和形状的业务文档。
author: NickSelin
ms.date: 06/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e67c10ecb9f297d1855a55431cd07c53ee87d40a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361373"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>设计 ER 格式以使用页面页眉或页脚中的嵌入图像生成采用 Excel 格式的报表

[!include[banner](../includes/banner.md)]

本主题说明系统管理员或电子报告功能顾问角色的用户如何执行以下任务：

- 配置[电子报告 (ER)](general-electronic-reporting.md) 框架的参数。
- 基于 Microsoft Excel 格式中的[模板](er-fillable-excel.md#excel-file-component)，导入 Microsoft [提供](general-electronic-reporting.md#Provider)的并用于生成[普通发票](../../../finance/accounts-receivable/create-free-text-invoice-new.md)的 ER [配置](general-electronic-reporting.md#Configuration)。
- 创建 Microsoft 提供的标准 ER 格式配置的[自定义（派生）](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization)版本。
- 修改自定义 ER 格式配置，以便它生成在页脚中具有公司徽标图像的普通发票报表。

本主题中的过程可以在 **USMF** 公司完成。 无需进行编码。 在开始之前，请下载并保存以下文件。

| 说明        | 文件名 |
|--------------------|-----------|
| 公司徽标图像 | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>内容

- [配置法人](#ConfigureLegalEntity)
- [配置 ER 框架](#ConfigureFramework)

    - [配置 ER 参数](#ConfigureParameters)
    - [激活 ER 配置提供程序](#ActivateProvider)

        - [查看 ER 配置提供程序列表](#ReviewProvidersList)
        - [添加新 ER 配置提供程序](#AddProvider)
        - [激活新 ER 配置提供程序](#ActivateAddedProvider)

- [导入标准 ER 格式配置](#ImportERSolution1)

    - [导入标准 ER 配置](#ImportERFormat)
    - [查看导入的 ER 配置](#ReviewImportedERSolution)

- [使用标准 ER 格式打印普通发票](#PrintInvoice1)

    - [设置打印管理](#ConfigurePrintManagement1)
    - [打印普通发票](#ProcessInvoice1)

- [自定义标准 ER 格式](#CustomizeProvidedFormat)

    - [创建自定义格式](#DeriveProvidedFormat)
    - [编辑自定义格式](#ConfigureDerivedFormat)
    - [将自定义格式标记为可运行](#MarkFormatRunnable)

- [使用自定义 ER 格式打印普通发票](#PrintInvoice2)

    - [设置打印管理](#ConfigurePrintManagement2)
    - [打印普通发票](#ProcessInvoice2)

- [其他资源](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>配置法人

1. 转到 **组织管理** \> **组织** \> **法人**。
2. 在 **法人** 页面上的 **报表公司徽标图像** 快速选项卡上，选择 **更改**。
3. 在 **选择要上传的图像文件** 对话框中，选择 **浏览**，然后选择之前下载的 **Company logo.png** 文件。
4. 选择 **保存**，然后关闭 **法人** 页面。

![在法人页面上选择的公司徽标图像。](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>配置 ER 框架

作为电子申报功能顾问角色的用户，您必须至少配置一小组 ER 参数，才能开始使用 ER 框架设计标准 ER 格式的自定义版本。

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>配置 ER 参数

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **电子申报参数**。
3. 在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。
4. 在 **附件** 选项卡上，设置以下参数：

    - 在 **配置** 字段中，选择 **USMF** 公司的 **文件** 类型。
    - 在 **作业存档**、**临时**、**基准** 和 **其他** 字段中，选择 **文件** 类型。

有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>激活 ER 配置提供程序

将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。 在 **电子申报** 工作区中激活的 ER 配置提供程序用于此目的。 因此，必须先在 **电子申报** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。

> [!NOTE]
> ER 配置仅可以由配置负责人编辑。 必须先在 **电子报告** 工作区中激活相应的 ER 配置提供程序，才能编辑 ER 配置。

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>查看 ER 配置提供程序列表

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序表** 页面中，每条提供程序记录都有唯一名称和 URL。 查看此页面的内容。 如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#AddProvider)。

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>添加新 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序** 页面上，选择 **新建**。
4. 在 **名称** 字段中，输入 **Litware, Inc.**
5. 在 **Internet 地址** 字段中，输入 `https://www.litware.com`。
6. 选择 **保存**。

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>激活新 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴，然后选择 **设置有效**。

有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>导入标准 ER 格式配置

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>导入标准 ER 配置

若要向当前 Dynamics 365 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)中导入这些配置。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 以查看 **Microsoft** 提供程序的存储库列表。
3. 在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。 如果提示您进行授权以连接到 [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md)，请按照授权说明进行操作。
4. 在 **配置存储库** 页面上，在左侧窗格的配置树中，选择 **普通发票 (Excel)** 格式配置。
5. 在 **版本** 快速选项卡上，选择所选 ER 格式配置的最新版本（例如 **240.112**）。
6. 选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。

![在“配置存储库”页面上导入标准 ER 配置。](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> 如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 Microsoft Dynamics Lifecycle Services (LCS)[ 下载配置](download-electronic-reporting-configuration-lcs.md)。

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>查看导入的 ER 配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页的左侧窗格的配置树中，展开 **发票模型**。
4. 除了所选的 **普通发票 (Excel)** ER 格式，还导入了其他必需的 ER 配置。 请确保配置树中有以下 ER 配置：

    - **发票模型** – 此配置中包含[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于表示开票业务域的数据结构。
    - **发票模型映射** – 此配置中包含[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于描述如何在运行时使用应用程序数据填充数据模型。
    - **普通发票 (Excel)** – 此配置中包含[格式](general-electronic-reporting.md#FormatComponentOutbound)和格式映射 ER 组件。 格式组件基于 Excel 格式的模板指定报表布局。 格式映射组件包含模型数据源，并指定如何在运行时使用此数据源填充报告布局。

![“配置”页面上导入的 ER 配置。](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>使用标准 ER 格式打印普通发票

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>设置打印管理

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，选择 **FTI-00000002** 发票，然后在操作窗格上，在 **发票** 选项卡的 **打印管理** 组中，选择 **打印管理**。
3. 在 **打印管理设置** 页面上，在左侧的树中，展开 **模块 - 应收帐款 \> 文档 \> 普通发票**，然后选择 **原始 \<Default\>** 项。
4. 在 **报表格式** 字段中，选择 **普通发票 (Excel)**。
5. 选择 **Esc** 键以退出 **打印管理设置** 页面并返回到 **普通发票** 页面。

![打印管理设置页面上标准 ER 格式的普通发票的打印管理设置。](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>打印普通发票

1. 在 **普通发票** 页面上，确保仍然选择 **FTI-00000002** 发票，然后在操作窗格上，在 **发票** 选项卡的 **文档** 组中，选择 **打印** \> **已选择**。
2. 下载 Excel 格式的生成发票，然后打开它进行预览。
3. 请注意，根据提供的 ER 格式的 Excel 模板的结构，生成发票的页面页脚包含有关当前页码和报表中总页数的信息。

![生成的普通发票。](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>自定义标准 ER 格式

对于本部分中的示例，您可以使用 Microsoft 提供的 ER 配置来生成 Excel 格式的普通发票。 但是，您必须添加自定义以将公司徽标图像放置在生成发票的页面页脚中。

在此情况下，作为 Litware, Inc. 的代表，您必须创建（派生）基于 Microsoft 提供的 **普通发票 (Excel)** 配置的新 ER 格式配置。

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>创建自定义格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型**，然后选择 **普通发票 (Excel)**。 Litware, Inc. 将此 ER 格式配置的导入版本（例如 **240.112**）用作自定义版本的基础。
3. 选择 **创建配置**，以打开下拉对话框。 使用此对话框创建自定义付款格式的新配置。
4. 在 **新建** 字段组中，选择 **从名称派生：普通发票 (Excel)，Microsoft** 选项。
5. 在 **名称** 字段中，输入 **普通发票 (Excel) 自定义**。
6. 选择 **创建配置**。

![在“创建配置”下拉对话框中为自定义付款格式创建配置。](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

创建版本 240.112.1 的 **普通发票 (Excel) 自定义** ER 格式配置。 此版本的 [状态](general-electronic-reporting.md#component-versioning)为 **草稿**，可以编辑。 自定义 ER 格式的当前内容与 Microsoft 提供的格式的内容匹配。

![在“配置”页面上创建的 ER 格式配置的新版本。](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>编辑自定义格式

配置您的自定义格式，以便在报表的每一页的页脚中放置公司徽标图像。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **付款模型**，然后选择 **普通发票 (Excel) 自定义**。
3. 在 **版本** 快速选项卡上，选择所选配置的版本 **240.112.1**。
4. 选择 **设计器**。
5. 在 **格式设计器** 页面中，选择 **显示详细信息** 查看有关格式元素的详细信息。
6. 展开并查看以下元素：

    - **Excel** 类型的 **普通发票** 元素。 此元素用于生成 Excel 工作簿格式的发票。
    - **工作表** 类型的 **普通发票 \\ 发票** 元素。 此元素用于生成已生成 Excel 工作簿的工作表。
    - **页脚** 类型的 **普通发票 \\ 发票 \\ 页脚** 元素。 此元素用于填充发票页脚。

7. 选择 **普通发票 \\ 发票 \\ 页脚** 元素。

    ![ER 操作设计器中的页脚元素。](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > 生成发票的每个页面页脚都包含有关当前页码和报表中总页数的信息。 如您所见，**普通发票 \\ 发票 \\ 页脚** 元素不包含子元素。 因此，要使用的 Excel 模板配置为在每个报表的页脚中心显示分页详细信息。

8. 选择 **添加**，然后选择要添加的格式元素的 **Excel \\ 图片** 类型：

    1. 在 **对齐方式** 字段中，选择 **右对齐**。
    2. 在 **缩放高度** 字段中，选择 **相对**。
    3. 在 **缩放百分比** 字段中，输入 **70**。
    4. 选择 **确定**。

        > [!NOTE]
        > **Excel \\ 图片** 元素用于添加公司徽标图像并将其对齐到页面页脚的右侧。

    ![“组件属性”对话框中图片元素的属性。](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. 在左侧的格式结构树中，选择刚刚添加的 **图片** 元素，然后在 **映射** 选项卡上，展开 **模型** 数据源。
10. 展开 **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo**，然后选择 **model.InvoiceBase.CompanyInfo.Logo** 数据源字段。 [容器](er-formula-supported-data-types-composite.md#container)类型的数据源字段将公司徽标图像公开为媒体内容。
11. 选择 **绑定**。 现在，**图片** 格式元素与 **model.InvoiceBase.CompanyInfo.Logo** 数据源字段绑定在一起。 因此，在运行时，公司徽标图像将放置在生成发票的页脚中。

    ![在 ER 操作设计器中与 model.InvoiceBase.CompanyInfo.Logo 数据源字段绑定在一起的图片格式元素。](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. 选择 **保存**，然后关闭 **设计器** 页面。

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>将自定义格式标记为可运行

因为已创建自定义格式的第一个版本，并且其状态为 **草稿**，因此您可以运行格式以进行测试。 若要运行此报表，请使用引用自定义 ER 格式的付款方式处理供应商付款。 默认情况下，从应用程序调用 ER 格式时，仅 [考虑](general-electronic-reporting.md#component-versioning)状态为 **已完成** 或 **已共享** 的版本。 此行为有助于避免使用未完成设计的 ER 格式。 但是，对于测试运行，可以强制应用程序使用状态为 **草稿** 的 ER 格式版本。 因此，如果需要进行任何修改，可以调整当前格式版本。 有关详细信息，请参阅[适用性](electronic-reporting-destinations.md#applicability)。

要使用 ER 格式的草稿版本，必须显式标记 ER 格式。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。
4. 选择 **编辑** 以使当前页面可编辑，然后在左侧窗格的配置树中，选择 **普通发票 (Excel) 自定义**。
5. 将 **运行草稿** 选项设置为 **是**。

![在“配置”页面上将自定义格式标记为可运行。](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>使用自定义 ER 格式打印普通发票

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>设置打印管理

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，选择 **FTI-00000002** 发票，然后在操作窗格上，在 **发票** 选项卡的 **打印管理** 组中，选择 **打印管理**。
3. 在 **打印管理设置** 页面上，在左侧的树中，展开 **模块 - 应收帐款** \> **文档** \> **普通发票**，然后选择 **原始** **\<Default\>** 项。
4. 在 **报表格式** 字段中，选择 **普通发票 (Excel) 自定义**。
5. 选择 **Esc** 以退出 **打印管理设置** 页面并返回到 **普通发票** 页面。

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>打印普通发票

1. 在 **普通发票** 页面上，确保仍然选择 **FTI-00000002** 发票，然后在操作窗格上，在 **发票** 选项卡的 **文档** 组中，选择 **打印** \> **已选择**。
2. 下载 Excel 格式的生成发票，然后打开它进行预览。
3. 请注意，根据自定义 ER 格式的结构，除了有关报表分页的信息，生成发票的页面页脚还包含公司徽标图像。

![页面页脚中具有公司徽标图像的生成普通发票。](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>其他资源

- [设计配置以生成 Excel 格式的文档](er-fillable-excel.md)
- [使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)
