---
title: 业务文档管理中的 Microsoft Office 样式用户界面
description: 本主题说明如何在电子报告 (ER) 框架的业务文档管理功能中使用新用户界面。
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881028"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="890c9-103">业务文档管理中的 Microsoft Office 样式用户界面</span><span class="sxs-lookup"><span data-stu-id="890c9-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="890c9-104">业务文档管理使业务用户可以使用 Microsoft 365 服务或相应的 Microsoft Office 桌面应用程序来编辑业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="890c9-105">编辑可能包括设计更改或新部署，或者用户可能会添加占位符以包含其他数据，而不必更改源代码。</span><span class="sxs-lookup"><span data-stu-id="890c9-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="890c9-106">有关如何使用业务文档管理的更多信息，请参见[业务文档管理概述](er-business-document-management.md)。</span><span class="sxs-lookup"><span data-stu-id="890c9-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="890c9-107">新用户界面 (UI) 更清晰，使用起来更舒适。</span><span class="sxs-lookup"><span data-stu-id="890c9-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="890c9-108">**业务文档** 区域仅显示当前提供商可用的模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="890c9-109">在上一个 UI 中，**模板** 选项卡列出了可用于任何提供商的所有模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="890c9-110">它还显示了由具有相同角色的任何用户创建和编辑的所有模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="890c9-111">您可以使用 **新建文档** 按钮以其他提供商提供的电子报告 (ER) 格式配置创建和编辑模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="890c9-112">在本主题的示例中，提供者是 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="890c9-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="890c9-113">或者，您可以通过以 Excel 格式上传自己的模板来创建模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="890c9-114">[使用业务文档管理创建新业务文档](https://youtu.be/gAIYl-mM_pw)视频（如上所示）包含在 YouTube 上可用的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="890c9-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="890c9-115">使业务文档管理中的新文档 UI 可用</span><span class="sxs-lookup"><span data-stu-id="890c9-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="890c9-116">要开始使用业务文档管理中的新文档 UI，必须打开 **功能管理** 工作区中的 **类似于 Office 的业务文档管理 UI 体验** 功能。</span><span class="sxs-lookup"><span data-stu-id="890c9-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="890c9-117">请按照以下步骤为所有法人启用此功能。</span><span class="sxs-lookup"><span data-stu-id="890c9-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="890c9-118">在 **功能管理** 工作区中的 **所有** 选项卡上，选择列表中的 **类似于 Office 的业务文档管理 UI 体验** 功能。</span><span class="sxs-lookup"><span data-stu-id="890c9-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="890c9-119">选择 **立即启用** 以打开所选功能。</span><span class="sxs-lookup"><span data-stu-id="890c9-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="890c9-120">刷新页面以访问新功能。</span><span class="sxs-lookup"><span data-stu-id="890c9-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="890c9-121">编辑其他提供商拥有的模板</span><span class="sxs-lookup"><span data-stu-id="890c9-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="890c9-122">在 **业务文档管理** 工作区中，选择 **新建文档**。</span><span class="sxs-lookup"><span data-stu-id="890c9-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![业务文档管理工作区](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="890c9-124">在 **选择** 选项卡上，选择要用作模板的文档，然后选择 **创建文档**。</span><span class="sxs-lookup"><span data-stu-id="890c9-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![业务文档对话框](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="890c9-126">在此新对话框内的 **标题** 字段中，根据需要更改标题。</span><span class="sxs-lookup"><span data-stu-id="890c9-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="890c9-127">标题文本用于命名自动创建的新 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="890c9-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="890c9-128">此配置 (**Customer FTI report (GER) Copy**) 的草稿版本将包含编辑的模板，并且将用于为当前用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="890c9-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="890c9-129">将使用来自基本 ER 格式配置的原始模板为每个其他用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="890c9-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="890c9-130">在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。</span><span class="sxs-lookup"><span data-stu-id="890c9-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="890c9-131">在 **注释** 字段中，更新有关将自动创建的可编辑模板的修订注解。</span><span class="sxs-lookup"><span data-stu-id="890c9-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="890c9-132">选择 **确定** 以确认开始执行编辑流程。</span><span class="sxs-lookup"><span data-stu-id="890c9-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![文档创建对话框](./media/BDM_overview_new_template3.png)

<span data-ttu-id="890c9-134">**新建文件** 按钮用于以其他提供商提供的 ER 格式配置创建和编辑模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="890c9-135">在本示例中，提供商是 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="890c9-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="890c9-136">当您选择 **新建文档** 时，您可以查看当前提供商和其他提供商拥有的所有模板。</span><span class="sxs-lookup"><span data-stu-id="890c9-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="890c9-137">选择模板后，将打开它进行编辑。</span><span class="sxs-lookup"><span data-stu-id="890c9-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="890c9-138">然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。</span><span class="sxs-lookup"><span data-stu-id="890c9-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="890c9-139">上传使用现有 Excel 格式的模板</span><span class="sxs-lookup"><span data-stu-id="890c9-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="890c9-140">在上传模板之前，请按照以下步骤提供所需信息。</span><span class="sxs-lookup"><span data-stu-id="890c9-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="890c9-141">在 **业务文档管理** 工作区中，选择 **新建文档**。</span><span class="sxs-lookup"><span data-stu-id="890c9-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![业务文档管理工作区](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="890c9-143">在 **创建新模板** 页面上，在 **上传** 选项卡的 **模板** 选项卡上，选择 **浏览** 以查找并选择要用作模板的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="890c9-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="890c9-144">在 **模板** 部分中，将自动填写 **标题** 和 **描述** 字段。</span><span class="sxs-lookup"><span data-stu-id="890c9-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="890c9-145">它们指定自动创建的新 ER 格式配置的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="890c9-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="890c9-146">可以根据需要编辑这些字段。</span><span class="sxs-lookup"><span data-stu-id="890c9-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="890c9-147">在 **文档类型** 部分中，在 **名称** 字段中，指定业务文档的类型。</span><span class="sxs-lookup"><span data-stu-id="890c9-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="890c9-148">该值将用于搜索正确的数据源（即 ER 模型配置）。</span><span class="sxs-lookup"><span data-stu-id="890c9-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![模板选项卡](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="890c9-150">在 **数据源** 选项卡上，在 **筛选器** 快速选项卡上，选择 **应用筛选器**。</span><span class="sxs-lookup"><span data-stu-id="890c9-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="890c9-151">在 **数据源** 部分中，自动填写 **名称** 字段，或者您可以手动选择值。</span><span class="sxs-lookup"><span data-stu-id="890c9-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="890c9-152">您可以使用筛选器按名称、描述、国家/地区代码和业务文档类型搜索适当的数据源名称。</span><span class="sxs-lookup"><span data-stu-id="890c9-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![数据源选项卡](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="890c9-154">**筛选器** 快速选项卡用于搜索正确的数据源（即 ER 模型配置）。</span><span class="sxs-lookup"><span data-stu-id="890c9-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="890c9-155">您可以编辑所有筛选器字段，以找到最适合您上传的文档的数据源。</span><span class="sxs-lookup"><span data-stu-id="890c9-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="890c9-156">使用 **筛选器** 快速选项卡上的条件作为 **OR** 条件。</span><span class="sxs-lookup"><span data-stu-id="890c9-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="890c9-157">在 **映射** 选项卡上，选择 **自动检测**。</span><span class="sxs-lookup"><span data-stu-id="890c9-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="890c9-158">自动填写 **根定义** 字段，或者您可以手动选择值。</span><span class="sxs-lookup"><span data-stu-id="890c9-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="890c9-159">此选项卡显示模板和模型中元素的最终映射。</span><span class="sxs-lookup"><span data-stu-id="890c9-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![映射选项卡](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="890c9-161">**模板结构** 部分中的映射使用用户语言的数据源和模板的单元格名称中的标签或描述的完全匹配。</span><span class="sxs-lookup"><span data-stu-id="890c9-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="890c9-162">选择 **创建文档** 以确认您要创建模板并开始编辑流程。</span><span class="sxs-lookup"><span data-stu-id="890c9-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="890c9-163">有关更多信息，请参见[业务文档管理概述](er-business-document-management.md)。</span><span class="sxs-lookup"><span data-stu-id="890c9-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="890c9-164">如果电子报告中没有提供商，您可以创建一个。</span><span class="sxs-lookup"><span data-stu-id="890c9-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="890c9-165">如果没有活动的提供商，您可以进行选择以激活一个。</span><span class="sxs-lookup"><span data-stu-id="890c9-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="890c9-166">若要创建提供商，请在 **名称** 字段中更改提供商的名称，在 **Internet 地址** 字段中更新新提供商的 Internet 地址，然后选择 **确定** 以确认。</span><span class="sxs-lookup"><span data-stu-id="890c9-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![在 BDM 中创建新的提供商](./media/bdm_create_provider.png)
    
- <span data-ttu-id="890c9-168">若要激活现有提供商，请在 **配置提供商** 字段中选择提供商的名称，然后选择 **确定** 以将提供商设置为活动状态。</span><span class="sxs-lookup"><span data-stu-id="890c9-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![在 BDM 中激活提供商](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="890c9-170">每个 BDM 模板都将该提供商引用为配置的作者。</span><span class="sxs-lookup"><span data-stu-id="890c9-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="890c9-171">这就是为什么模板需要活动的提供商。</span><span class="sxs-lookup"><span data-stu-id="890c9-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
