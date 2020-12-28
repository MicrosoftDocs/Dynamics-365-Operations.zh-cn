---
title: 在 Microsoft Excel 中将新字段添加到业务文档模板
description: 本主题提供有关如何通过使用业务文档管理功能在 Microsoft Excel 中将新字段添加到业务文档模板的信息。
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: fcfbcb021b192cef75d59b0db1796e994f3dc27d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681367"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="807a0-103">在 Microsoft Excel 中将新字段添加到业务文档模板</span><span class="sxs-lookup"><span data-stu-id="807a0-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="807a0-104">您可以向用于生成 Microsoft Excel 格式的业务文档的模板添加新字段。</span><span class="sxs-lookup"><span data-stu-id="807a0-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="807a0-105">这些字段可以添加为占位符，用于使用来自应用程序的必需信息填充生成的文档。</span><span class="sxs-lookup"><span data-stu-id="807a0-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="807a0-106">对于添加的每个字段，还可以指定与数据源的绑定，以指定在使用模板生成业务文档时将在字段中输入哪些应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="807a0-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="807a0-107">若要了解有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="807a0-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="807a0-108">此示例说明如何更新模板以填充生成的普通发票表单中的字段。</span><span class="sxs-lookup"><span data-stu-id="807a0-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="807a0-109">配置“业务文档管理”以编辑模板</span><span class="sxs-lookup"><span data-stu-id="807a0-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="807a0-110">由于业务文档管理 (BDM) 建立在[电子报告 (ER) 概览](general-electronic-reporting.md)框架的基础上，因此必须先配置必需的 ER 和 BDM 参数，然后才能开始使用 BDM。</span><span class="sxs-lookup"><span data-stu-id="807a0-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="807a0-111">以系统管理员身份登录到 Microsoft Dynamics 365 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="807a0-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="807a0-112">完成[业务文档管理概述](er-business-document-management.md)主题中示例的以下步骤：</span><span class="sxs-lookup"><span data-stu-id="807a0-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="807a0-113">配置 ER 参数。</span><span class="sxs-lookup"><span data-stu-id="807a0-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="807a0-114">打开 BDM。</span><span class="sxs-lookup"><span data-stu-id="807a0-114">Turn on BDM.</span></span>

<span data-ttu-id="807a0-115">现在，您可以开始使用 BDM 编辑业务文档模板了。</span><span class="sxs-lookup"><span data-stu-id="807a0-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="807a0-116">导入包含模板的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="807a0-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="807a0-117">此过程中的示例使用正式发布的 ER 解决方案。</span><span class="sxs-lookup"><span data-stu-id="807a0-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="807a0-118">您必须将此解决方案的 ER 配置导入到您当前的 Finance 实例中。</span><span class="sxs-lookup"><span data-stu-id="807a0-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="807a0-119">此解决方案的 **普通发票(Excel)** ER 格式配置包含 Excel 格式的业务文档模板，可以使用 BDM 对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="807a0-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="807a0-120">从 Microsoft Dynamics Lifecycle Service (LCS) 导入此 ER 格式配置的最新版本。</span><span class="sxs-lookup"><span data-stu-id="807a0-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="807a0-121">相应的 ER 数据模型和 ER 模型映射配置将自动导入。</span><span class="sxs-lookup"><span data-stu-id="807a0-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="807a0-122">有关如何导入 ER 配置的更多信息，请参阅[管理 ER 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="807a0-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS 共享资产库页面](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="807a0-124">编辑 ER 解决方案模板</span><span class="sxs-lookup"><span data-stu-id="807a0-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="807a0-125">以有权访问 **业务文档管理** 工作区的用户身份登录。</span><span class="sxs-lookup"><span data-stu-id="807a0-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="807a0-126">打开 **业务文档管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="807a0-126">Open the **Business document management** workspace.</span></span>

    ![业务文档管理工作区](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="807a0-128">在网格中，选择 **普通发票(Excel)** 模板。</span><span class="sxs-lookup"><span data-stu-id="807a0-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="807a0-129">在右窗格中，选择 **新建模板** 以创建基于所选模板的新模板。</span><span class="sxs-lookup"><span data-stu-id="807a0-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="807a0-130">在 **标题** 字段中，输入 **普通发票 (Excel) Contoso** 作为新模板的标题。</span><span class="sxs-lookup"><span data-stu-id="807a0-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="807a0-131">选择 **确定** 以确认开始执行编辑流程。</span><span class="sxs-lookup"><span data-stu-id="807a0-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="807a0-132">将出现 BDM 模板编辑器页面。</span><span class="sxs-lookup"><span data-stu-id="807a0-132">The BDM template editor page appears.</span></span> <span data-ttu-id="807a0-133">您可以使用 Microsoft 365 在嵌入式控件中在线编辑所选模板。</span><span class="sxs-lookup"><span data-stu-id="807a0-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM 模板编辑器页面](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="807a0-135">将新字段的标签添加到模板</span><span class="sxs-lookup"><span data-stu-id="807a0-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="807a0-136">在 BDM 模板编辑器页面的 Excel 功能区，在 **视图** 选项卡上，选中可编辑 Excel 模板的 **标题和网格线** 复选框。</span><span class="sxs-lookup"><span data-stu-id="807a0-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![选中“标题和网格线”复选框](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="807a0-138">选择单元格 **E8:F8**。</span><span class="sxs-lookup"><span data-stu-id="807a0-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="807a0-139">在 Excel 功能区的 **主页** 选项卡上，选择 **合并居中**，将选定的单元格合并到新合并的 **E8:F8** 单元格中。</span><span class="sxs-lookup"><span data-stu-id="807a0-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="807a0-140">在合并的单元格 **E8:F8** 中，输入 **URL**。</span><span class="sxs-lookup"><span data-stu-id="807a0-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="807a0-141">选择合并的单元格 **E7:F7**，选择 **格式刷**，然后选择合并的单元格 **E8:F8** 以与合并的单元格 **E7:F7** 相同的方式设置其格式。</span><span class="sxs-lookup"><span data-stu-id="807a0-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![新字段标签已添加到模板](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="807a0-143">设置模板模式以为新字段保留空间</span><span class="sxs-lookup"><span data-stu-id="807a0-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="807a0-144">在 BDM 模板编辑器页面上，选择合并的单元格 **G8:H8**。</span><span class="sxs-lookup"><span data-stu-id="807a0-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="807a0-145">在 Excel 功能区的 **主页** 选项卡上，选择 **合并居中** 以将选定的单元格合并到新合并的 **G8:H8** 单元格中。</span><span class="sxs-lookup"><span data-stu-id="807a0-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="807a0-146">选择合并的单元格 **G7:H7**，选择 **格式刷**，然后选择合并的单元格 **G8:H8** 以与合并的单元格 **G7:H7** 相同的方式设置其格式。</span><span class="sxs-lookup"><span data-stu-id="807a0-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![已为新字段保留空间](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="807a0-148">在 **名称** 框字段中，选择 **CompanyInfo**。</span><span class="sxs-lookup"><span data-stu-id="807a0-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="807a0-149">当前 Excel 模板的 **CompanyInfo** 范围包含用于使用作为卖方的当前公司的详细信息填充所生成报表的标头的所有字段。</span><span class="sxs-lookup"><span data-stu-id="807a0-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![已选择 CompanyInfo 范围](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="807a0-151">向模板添加新字段</span><span class="sxs-lookup"><span data-stu-id="807a0-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="807a0-152">在 **BDM 模板编辑器** 页面上的操作窗格上，选择 **显示格式**。</span><span class="sxs-lookup"><span data-stu-id="807a0-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="807a0-153">在 **模板结构** 窗格中，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="807a0-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="807a0-154">您必须调整要用作新字段的模板的那一部分。</span><span class="sxs-lookup"><span data-stu-id="807a0-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="807a0-155">您已经通过设置合并的单元格 **G8:H8** 的格式进行了此调整。</span><span class="sxs-lookup"><span data-stu-id="807a0-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![向模板添加新字段](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="807a0-157">选择 **Excel\单元格** 以在模板中作为单元格添加新字段。</span><span class="sxs-lookup"><span data-stu-id="807a0-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="807a0-158">如果要向模板添加新范围，可以选择 **Excel\范围**。</span><span class="sxs-lookup"><span data-stu-id="807a0-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="807a0-159">输入的范围可以包含多个单元格。</span><span class="sxs-lookup"><span data-stu-id="807a0-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="807a0-160">您可以稍后添加这些单元格。</span><span class="sxs-lookup"><span data-stu-id="807a0-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="807a0-161">请注意，在 **模板结构** 窗格中会自动选择 **CompanyInfo** 模板组件，因为它是当前模板结构中您要添加的字段的最合适的父组件。</span><span class="sxs-lookup"><span data-stu-id="807a0-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="807a0-162">在 **Excel 范围** 字段中，输入 **CompanyURL_Value**。</span><span class="sxs-lookup"><span data-stu-id="807a0-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="807a0-163">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="807a0-163">Select **OK**.</span></span>

    ![CompanyURL_Value 字段已添加到模板结构](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="807a0-165">在 **模板结构** 窗格中，选择省略号按钮 (...)，然后选择 **显示绑定**。</span><span class="sxs-lookup"><span data-stu-id="807a0-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![已选择“显示绑定”](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="807a0-167">**模板结构** 窗格现在显示基础 ER 格式中可用的数据源。</span><span class="sxs-lookup"><span data-stu-id="807a0-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="807a0-168">选择 **CompanyInfo_Value** 作为您计划绑定到基础 ER 格式的数据源的字段。</span><span class="sxs-lookup"><span data-stu-id="807a0-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="807a0-169">在 **模板结构** 窗格的 **数据源** 部分，展开 **模型 \> InvoiceBase \> CompanyInfo**。</span><span class="sxs-lookup"><span data-stu-id="807a0-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="807a0-170">在 **CompanyInfo** 下，选择 **WebsiteURI** 项。</span><span class="sxs-lookup"><span data-stu-id="807a0-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![已选择 WebsiteURI 项](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="807a0-172">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="807a0-172">Select **Bind**.</span></span>
11. <span data-ttu-id="807a0-173">在 **模板结构** 窗格中，选择 **保存**，然后关闭 BDM 模板编辑器页面。</span><span class="sxs-lookup"><span data-stu-id="807a0-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="807a0-174">在 **业务文档管理** 工作区中，右窗格中的 **模板** 选项卡显示更新后的模板。</span><span class="sxs-lookup"><span data-stu-id="807a0-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="807a0-175">在网格中，请注意，已编辑模板的 **状态** 字段已更改为 **草稿**，**修订** 字段不再为空。</span><span class="sxs-lookup"><span data-stu-id="807a0-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="807a0-176">这些更改表明编辑此模板的过程已经开始。</span><span class="sxs-lookup"><span data-stu-id="807a0-176">These changes indicate that the process of editing this template has been started.</span></span>

![已编辑业务文档管理工作区中的模板](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="807a0-178">查看公司设置</span><span class="sxs-lookup"><span data-stu-id="807a0-178">Review company settings</span></span>

1.  <span data-ttu-id="807a0-179">转至 **组织管理 \> 组织 \> 法人实体**。</span><span class="sxs-lookup"><span data-stu-id="807a0-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="807a0-180">在 **联系信息** 快速选项卡上，确认输入了公司 URL。</span><span class="sxs-lookup"><span data-stu-id="807a0-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![已在法人页面上输入公司 URL](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="807a0-182">生成业务文档以测试更新的模板</span><span class="sxs-lookup"><span data-stu-id="807a0-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="807a0-183">在应用程序中，将公司更改为 **USMF**，然后转到 **应收帐款 \> 发票 \> 所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="807a0-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="807a0-184">选择发票 **FTI-00000002**，然后选择 **打印管理**。</span><span class="sxs-lookup"><span data-stu-id="807a0-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="807a0-185">在左窗格中，展开 **模块 - 应收帐款 \> 文档 \> 普通发票**。</span><span class="sxs-lookup"><span data-stu-id="807a0-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="807a0-186">在 **普通发票** 下，选择 **原始凭证** 级别以指定要处理的发票范围。</span><span class="sxs-lookup"><span data-stu-id="807a0-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="807a0-187">在右窗格的 **报表格式** 字段中，为指定的文档级别选择 **普通发票(Excel) Contoso** 模板。</span><span class="sxs-lookup"><span data-stu-id="807a0-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![已选择“普通发票(Excel) Contoso”模板](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="807a0-189">按 **Esc** 关闭当前页。</span><span class="sxs-lookup"><span data-stu-id="807a0-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="807a0-190">选择 **打印 \> 选定**。</span><span class="sxs-lookup"><span data-stu-id="807a0-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="807a0-191">下载生成的文档，然后在 Excel 中打开它。</span><span class="sxs-lookup"><span data-stu-id="807a0-191">Download the generated document, and open it in Excel.</span></span>

    ![Excel 中的普通发票](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="807a0-193">修改后的模板将用于为所选物料生成普通发票报表。</span><span class="sxs-lookup"><span data-stu-id="807a0-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="807a0-194">要分析此报表如何受到模板更改的影响，请在另外一个应用程序会话中更改模板后立即在一个应用程序会话中运行报表。</span><span class="sxs-lookup"><span data-stu-id="807a0-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="807a0-195">相关链接</span><span class="sxs-lookup"><span data-stu-id="807a0-195">Related links</span></span>

[<span data-ttu-id="807a0-196">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="807a0-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="807a0-197">业务文档管理概览</span><span class="sxs-lookup"><span data-stu-id="807a0-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="807a0-198">设计以 OPENXML 格式生成报表的配置</span><span class="sxs-lookup"><span data-stu-id="807a0-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
