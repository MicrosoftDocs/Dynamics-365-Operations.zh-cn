---
title: 更新业务文档模板的结构
description: 本主题说明如何通过使用“业务文档管理”功能更新业务文档模板的结构。
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
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
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd279b28c43e22bec6bf814845fe97828bc96d81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681320"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="c9275-103">更新业务文档模板的结构</span><span class="sxs-lookup"><span data-stu-id="c9275-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c9275-104">在 [业务文档管理](er-business-document-management.md)模板编辑器的 **摸板结构** 窗格中，可以通过在 Microsoft Excel 中向模板[添加新字段](er-bdm-add-field-to-excel-template.md)来修改业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="c9275-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="c9275-105">然后，在 Dynamics 365 Finance 中自动更新模板的结构，以使其反映您在 **模板结构** 窗格中进行的更改。</span><span class="sxs-lookup"><span data-stu-id="c9275-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="c9275-106">您还可以通过使用 Office 365 在线功能修改模板。</span><span class="sxs-lookup"><span data-stu-id="c9275-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="c9275-107">例如，您可以将新的命名项目（例如图片或形状）添加到可编辑工作表中。</span><span class="sxs-lookup"><span data-stu-id="c9275-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="c9275-108">在这种情况下，模板的结构不会在 Finance 中自动更新，并且您添加的项目不会出现在 **模板结构** 窗格中。</span><span class="sxs-lookup"><span data-stu-id="c9275-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="c9275-109">通过选择模板编辑器页面中的 **更新结构**，在 Finance 中更新摸板结构。</span><span class="sxs-lookup"><span data-stu-id="c9275-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="c9275-110">有关此功能的详细信息，请完成以下示例。</span><span class="sxs-lookup"><span data-stu-id="c9275-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="c9275-111">示例：更新业务文档模板的结构</span><span class="sxs-lookup"><span data-stu-id="c9275-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="c9275-112">此示例显示在 Office Online 中修改了模板之后，系统管理员如何在 Finance 中更新业务文档模板的结构。</span><span class="sxs-lookup"><span data-stu-id="c9275-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="c9275-113">以下各节说明了其中涉及的步骤。</span><span class="sxs-lookup"><span data-stu-id="c9275-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="c9275-114">准备要编辑的业务文档模板</span><span class="sxs-lookup"><span data-stu-id="c9275-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="c9275-115">完成[业务文档管理概述](er-business-document-management.md)中的以下过程。</span><span class="sxs-lookup"><span data-stu-id="c9275-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="c9275-116">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="c9275-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="c9275-117">导入 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="c9275-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="c9275-118">启用业务文档管理</span><span class="sxs-lookup"><span data-stu-id="c9275-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="c9275-119">配置参数</span><span class="sxs-lookup"><span data-stu-id="c9275-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="c9275-120">编辑业务文档模板</span><span class="sxs-lookup"><span data-stu-id="c9275-120">Edit a business document template</span></span>

1. <span data-ttu-id="c9275-121">在 **业务文档管理** 工作区中，选择 **新建文档**。</span><span class="sxs-lookup"><span data-stu-id="c9275-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="c9275-122">在 **创建新模板** 页面上，选择 **普通发票(ER 示例)(Excel)** 模板。</span><span class="sxs-lookup"><span data-stu-id="c9275-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="c9275-123">选择 **创建文档**。</span><span class="sxs-lookup"><span data-stu-id="c9275-123">Select **Create document**.</span></span>
4. <span data-ttu-id="c9275-124">在 **标题** 字段中，输入 **FTI sample Litware**。</span><span class="sxs-lookup"><span data-stu-id="c9275-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="c9275-125">选择 **确定** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="c9275-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9275-126">如果您尚未登录 Office Online，将把您[定向到 Office 365 登录页面](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page)。</span><span class="sxs-lookup"><span data-stu-id="c9275-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span></span> <span data-ttu-id="c9275-127">要返回 Finance 环境，请在浏览器中选择 **后退** 按钮。</span><span class="sxs-lookup"><span data-stu-id="c9275-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="c9275-128">将打开新模板，以便在模板编辑器页面上的 Excel Online 嵌入式控件中进行编辑。</span><span class="sxs-lookup"><span data-stu-id="c9275-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="c9275-129">[![使用业务文档管理工作区开始编辑业务文档模板](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="c9275-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="c9275-130">查看可编辑模板的当前结构</span><span class="sxs-lookup"><span data-stu-id="c9275-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="c9275-131">在 Excel Online 中的功能区上 **视图** 选项卡中 **显示** 组内，选择 **网格线**。</span><span class="sxs-lookup"><span data-stu-id="c9275-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="c9275-132">在可编辑模板中，选择模板标题上方的矩形。</span><span class="sxs-lookup"><span data-stu-id="c9275-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="c9275-133">这个矩形是一张名为 **rptHeaderCompLogo** 的图片。</span><span class="sxs-lookup"><span data-stu-id="c9275-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="c9275-134">如果 **模板结构** 窗格已隐藏，请选择 **显示结构**。</span><span class="sxs-lookup"><span data-stu-id="c9275-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="c9275-135">在 **模板结构** 窗格中，展开 **报表 \> 发票 \> rptHeader \> rptHeaderPart1**。</span><span class="sxs-lookup"><span data-stu-id="c9275-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="c9275-136">请注意，在 Finance 中的模板结构中，**rptHeaderCompLogo** 项表示为 **报表 \> 发票 \> rptHeader \> rptHeaderPart1** 的一个子项。</span><span class="sxs-lookup"><span data-stu-id="c9275-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="c9275-137">[![使用业务文档管理工作区查看可编辑模板的当前结构](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="c9275-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="c9275-138">通过删除图片更新业务文档模板的结构</span><span class="sxs-lookup"><span data-stu-id="c9275-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="c9275-139">在 Excel Online 中的可编辑模板中，选择 **rptHeaderCompLogo** 图片。</span><span class="sxs-lookup"><span data-stu-id="c9275-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="c9275-140">请按照以下步骤之一从可编辑模板中删除所选图片：</span><span class="sxs-lookup"><span data-stu-id="c9275-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="c9275-141">选择键盘上的 **Delete** 键。</span><span class="sxs-lookup"><span data-stu-id="c9275-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="c9275-142">选择并按住（或右键单击）图片，然后选择 **剪切**。</span><span class="sxs-lookup"><span data-stu-id="c9275-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9275-143">**rptHeaderCompLogo** 项现在仍然留在 Finance 中的模板结构中，虽然 Excel 模板中不再包含此图片。</span><span class="sxs-lookup"><span data-stu-id="c9275-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="c9275-144">选择 **更新结构** 同步 Excel 和 Finance 中的可编辑模板结构。</span><span class="sxs-lookup"><span data-stu-id="c9275-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="c9275-145">在 **模板结构** 窗格中，展开 **报表 \> 发票 \> rptHeader \> rptHeaderPart1**。</span><span class="sxs-lookup"><span data-stu-id="c9275-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="c9275-146">请注意，Finance 中的模板结构中不再包含 **rptHeaderCompLogo** 项。</span><span class="sxs-lookup"><span data-stu-id="c9275-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="c9275-147">[![使用业务文档管理工作区从业务文档模板删除图片](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="c9275-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="c9275-148">通过添加图片更新业务文档模板的结构</span><span class="sxs-lookup"><span data-stu-id="c9275-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="c9275-149">在 Excel Online 中的功能区上 **插入** 选项卡中 **示意图** 组内，选择 **图片**。</span><span class="sxs-lookup"><span data-stu-id="c9275-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="c9275-150">选择 **选择文件**，浏览到要添加的图像，选择它，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c9275-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="c9275-151">选择 **插入**。</span><span class="sxs-lookup"><span data-stu-id="c9275-151">Select **Insert**.</span></span>
4. <span data-ttu-id="c9275-152">移动新图片，直到到达正确位置。</span><span class="sxs-lookup"><span data-stu-id="c9275-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="c9275-153">默认情况下，Excel 会为该图片命名。</span><span class="sxs-lookup"><span data-stu-id="c9275-153">By default, Excel names the picture.</span></span> <span data-ttu-id="c9275-154">例如，它可能将此图片命名为 **Picture 2**。</span><span class="sxs-lookup"><span data-stu-id="c9275-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="c9275-155">选择 **更新结构** 同步 Excel 和 Finance 中的可编辑模板结构。</span><span class="sxs-lookup"><span data-stu-id="c9275-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="c9275-156">在 **模板结构** 窗格中，展开 **报表 \> 发票 \> rptHeader \> rptHeaderPart1**。</span><span class="sxs-lookup"><span data-stu-id="c9275-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="c9275-157">请注意，Finance 中的模板结构中现在包含这个新图片，形式为一个项。</span><span class="sxs-lookup"><span data-stu-id="c9275-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="c9275-158">[![使用业务文档管理工作区向业务文档模板添加图片](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="c9275-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="c9275-159">相关链接</span><span class="sxs-lookup"><span data-stu-id="c9275-159">Related links</span></span>

[<span data-ttu-id="c9275-160">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="c9275-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="c9275-161">业务文档管理概览</span><span class="sxs-lookup"><span data-stu-id="c9275-161">Business document management overview</span></span>](er-business-document-management.md)
