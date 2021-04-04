---
title: 在 Microsoft Excel 中将新字段添加到业务文档模板
description: 本主题提供有关如何通过使用业务文档管理功能在 Microsoft Excel 中将新字段添加到业务文档模板的信息。
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6368d763f44c015a6e85652b1880cfd86ff5ba09
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569013"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>在 Microsoft Excel 中将新字段添加到业务文档模板

[!include[banner](../includes/banner.md)]

您可以向用于生成 Microsoft Excel 格式的业务文档的模板添加新字段。 这些字段可以添加为占位符，用于使用来自应用程序的必需信息填充生成的文档。 对于添加的每个字段，还可以指定与数据源的绑定，以指定在使用模板生成业务文档时将在字段中输入哪些应用程序数据。

若要了解有关此功能的详细信息，请完成本主题中的示例。 此示例说明如何更新模板以填充生成的普通发票表单中的字段。

## <a name="configure-business-document-management-to-edit-templates"></a>配置“业务文档管理”以编辑模板

由于业务文档管理 (BDM) 建立在[电子报告 (ER) 概览](general-electronic-reporting.md)框架的基础上，因此必须先配置必需的 ER 和 BDM 参数，然后才能开始使用 BDM。

1.  以系统管理员身份登录到 Microsoft Dynamics 365 Finance 实例。
2.  完成[业务文档管理概述](er-business-document-management.md)主题中示例的以下步骤：

    1.  配置 ER 参数。
    2.  打开 BDM。

现在，您可以开始使用 BDM 编辑业务文档模板了。

## <a name="import-er-solutions-that-contain-a-template"></a>导入包含模板的 ER 解决方案

此过程中的示例使用正式发布的 ER 解决方案。 您必须将此解决方案的 ER 配置导入到您当前的 Finance 实例中。

此解决方案的 **普通发票(Excel)** ER 格式配置包含 Excel 格式的业务文档模板，可以使用 BDM 对其进行编辑。 从 Microsoft Dynamics Lifecycle Service (LCS) 导入此 ER 格式配置的最新版本。 相应的 ER 数据模型和 ER 模型映射配置将自动导入。

有关如何导入 ER 配置的更多信息，请参阅[管理 ER 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。

![LCS 共享资产库页面](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>编辑 ER 解决方案模板

1.  以有权访问 **业务文档管理** 工作区的用户身份登录。
2.  打开 **业务文档管理** 工作区。

    ![业务文档管理工作区](./media/BDM-AddFldExcel-Workspace.png)

3.  在网格中，选择 **普通发票(Excel)** 模板。
4.  在右窗格中，选择 **新建模板** 以创建基于所选模板的新模板。
5.  在 **标题** 字段中，输入 **普通发票 (Excel) Contoso** 作为新模板的标题。
6.  选择 **确定** 以确认开始执行编辑流程。

将出现 BDM 模板编辑器页面。 您可以使用 Microsoft 365 在嵌入式控件中在线编辑所选模板。

![BDM 模板编辑器页面](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>将新字段的标签添加到模板

1.  在 BDM 模板编辑器页面的 Excel 功能区，在 **视图** 选项卡上，选中可编辑 Excel 模板的 **标题和网格线** 复选框。

    ![选中“标题和网格线”复选框](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  选择单元格 **E8:F8**。
3.  在 Excel 功能区的 **主页** 选项卡上，选择 **合并居中**，将选定的单元格合并到新合并的 **E8:F8** 单元格中。
4.  在合并的单元格 **E8:F8** 中，输入 **URL**。
5.  选择合并的单元格 **E7:F7**，选择 **格式刷**，然后选择合并的单元格 **E8:F8** 以与合并的单元格 **E7:F7** 相同的方式设置其格式。

    ![新字段标签已添加到模板](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>设置模板模式以为新字段保留空间

1.  在 BDM 模板编辑器页面上，选择合并的单元格 **G8:H8**。
2.  在 Excel 功能区的 **主页** 选项卡上，选择 **合并居中** 以将选定的单元格合并到新合并的 **G8:H8** 单元格中。
3.  选择合并的单元格 **G7:H7**，选择 **格式刷**，然后选择合并的单元格 **G8:H8** 以与合并的单元格 **G7:H7** 相同的方式设置其格式。

    ![已为新字段保留空间](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  在 **名称** 框字段中，选择 **CompanyInfo**。

    当前 Excel 模板的 **CompanyInfo** 范围包含用于使用作为卖方的当前公司的详细信息填充所生成报表的标头的所有字段。

    ![已选择 CompanyInfo 范围](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>向模板添加新字段

1.  在 **BDM 模板编辑器** 页面上的操作窗格上，选择 **显示格式**。
2.  在 **模板结构** 窗格中，选择 **添加**。

    > [!NOTE]
    > 您必须调整要用作新字段的模板的那一部分。 您已经通过设置合并的单元格 **G8:H8** 的格式进行了此调整。

    ![向模板添加新字段](./media/BDM-AddFldExcel-AddCell.png)

3.  选择 **Excel\单元格** 以在模板中作为单元格添加新字段。

    如果要向模板添加新范围，可以选择 **Excel\范围**。 输入的范围可以包含多个单元格。 您可以稍后添加这些单元格。
    
    请注意，在 **模板结构** 窗格中会自动选择 **CompanyInfo** 模板组件，因为它是当前模板结构中您要添加的字段的最合适的父组件。
    
4.  在 **Excel 范围** 字段中，输入 **CompanyURL_Value**。
5.  选择 **确定**。

    ![CompanyURL_Value 字段已添加到模板结构](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  在 **模板结构** 窗格中，选择省略号按钮 (...)，然后选择 **显示绑定**。

    ![已选择“显示绑定”](./media/BDM-AddFldExcel-ShowBindings.png)

    **模板结构** 窗格现在显示基础 ER 格式中可用的数据源。

7.  选择 **CompanyInfo_Value** 作为您计划绑定到基础 ER 格式的数据源的字段。
8.  在 **模板结构** 窗格的 **数据源** 部分，展开 **模型 \> InvoiceBase \> CompanyInfo**。
9.  在 **CompanyInfo** 下，选择 **WebsiteURI** 项。

    ![已选择 WebsiteURI 项](./media/BDM-AddFldExcel-BindURL.png)

10. 选择 **绑定**。
11. 在 **模板结构** 窗格中，选择 **保存**，然后关闭 BDM 模板编辑器页面。

在 **业务文档管理** 工作区中，右窗格中的 **模板** 选项卡显示更新后的模板。 在网格中，请注意，已编辑模板的 **状态** 字段已更改为 **草稿**，**修订** 字段不再为空。 这些更改表明编辑此模板的过程已经开始。

![已编辑业务文档管理工作区中的模板](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>查看公司设置

1.  转至 **组织管理 \> 组织 \> 法人实体**。
2.  在 **联系信息** 快速选项卡上，确认输入了公司 URL。

![已在法人页面上输入公司 URL](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>生成业务文档以测试更新的模板

1.  在应用程序中，将公司更改为 **USMF**，然后转到 **应收帐款 \> 发票 \> 所有普通发票**。
2.  选择发票 **FTI-00000002**，然后选择 **打印管理**。
3.  在左窗格中，展开 **模块 - 应收帐款 \> 文档 \> 普通发票**。
4.  在 **普通发票** 下，选择 **原始凭证** 级别以指定要处理的发票范围。
5.  在右窗格的 **报表格式** 字段中，为指定的文档级别选择 **普通发票(Excel) Contoso** 模板。

    ![已选择“普通发票(Excel) Contoso”模板](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  按 **Esc** 关闭当前页。
7.  选择 **打印 \> 选定**。
8.  下载生成的文档，然后在 Excel 中打开它。

    ![Excel 中的普通发票](./media/BDM-AddFldExcel-PreviewReport.png)

修改后的模板将用于为所选物料生成普通发票报表。 要分析此报表如何受到模板更改的影响，请在另外一个应用程序会话中更改模板后立即在一个应用程序会话中运行报表。

## <a name="related-links"></a>相关链接

[电子申报 (ER) 概览](general-electronic-reporting.md)

[业务文档管理概览](er-business-document-management.md)

[设计以 OPENXML 格式生成报表的配置](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]