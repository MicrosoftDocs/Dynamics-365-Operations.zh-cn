---
title: 编辑 Dynamics 365 Talent - Onboard 中的入职指南和模板
description: 本主题说明如何将活动和其他信息添加到 Microsoft Dynamics 365 Talent - Onboard 中的入职指南和模板。
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460465"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="d53d3-103">编辑入职指南和模板</span><span class="sxs-lookup"><span data-stu-id="d53d3-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d53d3-104">在 Microsoft Dynamics 365 Talent: Onboard 中创建入职指南或模板后，您必须添加介绍、活动、联系人和资源。</span><span class="sxs-lookup"><span data-stu-id="d53d3-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="d53d3-105">Onboard 允许您在入职指南中包含丰富的内容，包括：</span><span class="sxs-lookup"><span data-stu-id="d53d3-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="d53d3-106">YouTube 视频</span><span class="sxs-lookup"><span data-stu-id="d53d3-106">YouTube videos</span></span>
- <span data-ttu-id="d53d3-107">Microsoft Sway 演示文稿</span><span class="sxs-lookup"><span data-stu-id="d53d3-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="d53d3-108">Microsoft PowerApps 应用</span><span class="sxs-lookup"><span data-stu-id="d53d3-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="d53d3-109">Microsoft Stream 视频</span><span class="sxs-lookup"><span data-stu-id="d53d3-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="d53d3-110">Microsoft Forms 表单</span><span class="sxs-lookup"><span data-stu-id="d53d3-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="d53d3-111">包含 Web 内容的 iframe</span><span class="sxs-lookup"><span data-stu-id="d53d3-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="d53d3-112">编辑从模板导入的介绍或活动</span><span class="sxs-lookup"><span data-stu-id="d53d3-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="d53d3-113">如果您从模板创建入职指南，或者将活动从一个模板导入另一个模板，您会注意到导入活动上有一个 **锁定** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d53d3-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="d53d3-114">这些称为 *托管活动*。</span><span class="sxs-lookup"><span data-stu-id="d53d3-114">These are called *managed activities*.</span></span>

<span data-ttu-id="d53d3-115">[![托管活动](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="d53d3-116">选择托管活动时，您可以在活动顶部看到源模板。</span><span class="sxs-lookup"><span data-stu-id="d53d3-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="d53d3-117">[![托管活动源](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="d53d3-118">如果您在模板中编辑活动，Onboard 会将更改推送到基于该模板的所有模板和未发送的指南。</span><span class="sxs-lookup"><span data-stu-id="d53d3-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="d53d3-119">如果您根据编辑的模板选择未发送的指南，然后选择指南中的 **活动** 选项卡，您将看到指南已更改的通知。</span><span class="sxs-lookup"><span data-stu-id="d53d3-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="d53d3-120">要消除通知，请选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="d53d3-121">[![更改通知](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="d53d3-122">您会在更新的活动旁边看到一个黑点。</span><span class="sxs-lookup"><span data-stu-id="d53d3-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="d53d3-123">[![已更改活动](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="d53d3-124">除了在活动的右侧部分添加受托人、到期日期或其他信息外，您无法编辑原始模板之外的托管活动。</span><span class="sxs-lookup"><span data-stu-id="d53d3-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="d53d3-125">如果要编辑托管活动，或者如果您不希望活动从其来源模板接收更新，请选择该活动的 **锁定** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d53d3-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="d53d3-126">**锁定** 按钮将消失。</span><span class="sxs-lookup"><span data-stu-id="d53d3-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="d53d3-127">该活动将不再由原始模板管理，并且将不再从该模板接收更新。</span><span class="sxs-lookup"><span data-stu-id="d53d3-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="d53d3-128">您对活动所做的更新不会影响原始模板。</span><span class="sxs-lookup"><span data-stu-id="d53d3-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="d53d3-129">如果您从指南中删除活动并从该指南的模板中推送更改，则该活动将在指南中保持删除状态。</span><span class="sxs-lookup"><span data-stu-id="d53d3-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="d53d3-130">联系人和资源不受模板管理。</span><span class="sxs-lookup"><span data-stu-id="d53d3-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="d53d3-131">此外，还不管理部分，因此，如果您在模板中添加或编辑部分，则不会将更改推送到使用该模板的任何指南或模板。</span><span class="sxs-lookup"><span data-stu-id="d53d3-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="d53d3-132">如果向模板添加新活动，则会基于该模板将新活动推送到指南和模板，并在顶部显示新活动。</span><span class="sxs-lookup"><span data-stu-id="d53d3-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="d53d3-133">从另一个模板导入活动</span><span class="sxs-lookup"><span data-stu-id="d53d3-133">Import activities from another template</span></span>

<span data-ttu-id="d53d3-134">您可以将一个或多个模板中的活动导入指南或模板。</span><span class="sxs-lookup"><span data-stu-id="d53d3-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="d53d3-135">选择要编辑的指南或模板。</span><span class="sxs-lookup"><span data-stu-id="d53d3-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="d53d3-136">选择 **活动** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d53d3-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="d53d3-137">在右侧部分中选择 **导入** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d53d3-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="d53d3-138">[![导入活动](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="d53d3-139">要在浏览器的新选项卡中预览任务，请选择任意模板上的 **在新选项卡中打开** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d53d3-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="d53d3-140">[![导入活动](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="d53d3-141">将所需模板拖放到指南模板中要显示活动的位置。</span><span class="sxs-lookup"><span data-stu-id="d53d3-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="d53d3-142">继续编辑指南或模板。</span><span class="sxs-lookup"><span data-stu-id="d53d3-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="d53d3-143">导入的活动将包含 **锁定** 按钮，表示这些活动由您从中导入活动的模板管理。</span><span class="sxs-lookup"><span data-stu-id="d53d3-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="d53d3-144">当您对导入的模板进行更改时，这些活动将在您将其导入的模板中更新。</span><span class="sxs-lookup"><span data-stu-id="d53d3-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="d53d3-145">但是，更改不会自动推送到从向其导入的模板创建的任何指南。</span><span class="sxs-lookup"><span data-stu-id="d53d3-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="d53d3-146">将更改从模板推送到其他模板或指南</span><span class="sxs-lookup"><span data-stu-id="d53d3-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="d53d3-147">如果编辑包含其他模板或指南使用的活动的模板，如果希望更改出现在其他模板或指南中，则必须推送更改。</span><span class="sxs-lookup"><span data-stu-id="d53d3-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="d53d3-148">如果您不确定模板的活动是否在其他模板或指南中使用，请选择 **使用位置** 选项卡查看这些活动的显示位置。</span><span class="sxs-lookup"><span data-stu-id="d53d3-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="d53d3-149">[![查看指南和模板活动的使用位置](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="d53d3-150">推送更改：</span><span class="sxs-lookup"><span data-stu-id="d53d3-150">To push your changes:</span></span>

1. <span data-ttu-id="d53d3-151">选择 **保存** 按钮保存更改。</span><span class="sxs-lookup"><span data-stu-id="d53d3-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="d53d3-152">如果不这样做，系统将提示您在下一步中保存更改。</span><span class="sxs-lookup"><span data-stu-id="d53d3-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="d53d3-153">选择 **推送这些更改**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="d53d3-154">添加或编辑介绍</span><span class="sxs-lookup"><span data-stu-id="d53d3-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="d53d3-155">在 **介绍** 选项卡上，输入指南的标题和开场白消息。</span><span class="sxs-lookup"><span data-stu-id="d53d3-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="d53d3-156">要使用示例文本，请选择 **使用此消息**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="d53d3-157">[![Onboard 模板中的“介绍”选项卡](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="d53d3-158">使用格式按钮根据需要调出文本，或添加图像或链接。</span><span class="sxs-lookup"><span data-stu-id="d53d3-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="d53d3-159">选择 **保存** 保存您的工作。</span><span class="sxs-lookup"><span data-stu-id="d53d3-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="d53d3-160">添加或编辑活动</span><span class="sxs-lookup"><span data-stu-id="d53d3-160">Add or edit activities</span></span>

1. <span data-ttu-id="d53d3-161">在 **活动** 选项卡上，将项目从右侧拖动到编辑区域。</span><span class="sxs-lookup"><span data-stu-id="d53d3-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="d53d3-162">要将指南安排到各个部分，请将 **新部分** 项目拖动到编辑区域，然后输入部分的名称和可选描述。</span><span class="sxs-lookup"><span data-stu-id="d53d3-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="d53d3-163">将新部分添加到入职指南或模板</span><span class="sxs-lookup"><span data-stu-id="d53d3-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="d53d3-164">要为新雇员添加要完成的活动，请将 **新活动** 项目拖到编辑区域，然后输入活动的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="d53d3-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="d53d3-165">将新活动添加到入职指南或模板</span><span class="sxs-lookup"><span data-stu-id="d53d3-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="d53d3-166">为您的入职指南添加丰富的内容：</span><span class="sxs-lookup"><span data-stu-id="d53d3-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="d53d3-167">要添加 YouTube 视频，请将 **YouTube** 项目拖至编辑区域，输入活动的名称和描述，然后输入 YouTube 视频的 URL。</span><span class="sxs-lookup"><span data-stu-id="d53d3-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="d53d3-168">要添加 Sway 演示文稿或新闻稿，请将 **Sway** 项目拖到编辑区域，输入活动的名称和描述，然后输入 Sway 演示文稿或新闻稿的嵌入 URL。</span><span class="sxs-lookup"><span data-stu-id="d53d3-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="d53d3-169">要添加 Microsoft Power Apps 应用，请将 **Power Apps** 项目拖动到编辑区域，输入活动的名称和描述，然后选择 Power Apps 应用或输入 Power Apps 应用 ID。</span><span class="sxs-lookup"><span data-stu-id="d53d3-169">To add a Microsoft Power Apps app, drag the **Power Apps** item to the editing area, enter a name and description for the activity, and either select the Power Apps app or enter the Power Apps app ID.</span></span>
    - <span data-ttu-id="d53d3-170">要添加 Microsoft Stream 视频，请将 **Microsoft Stream** 项目拖到编辑区域，输入活动的名称和描述，然后输入 Microsoft Stream 视频的 URL。</span><span class="sxs-lookup"><span data-stu-id="d53d3-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="d53d3-171">要添加 Microsoft Forms 表单，请将 **Microsoft Forms** 项目拖到编辑区域，输入活动的名称和描述，输入 Microsoft Forms 表单的 URL，并指定屏幕区域的大小。</span><span class="sxs-lookup"><span data-stu-id="d53d3-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="d53d3-172">要添加包含 Web 内容的 iframe，请将 **Web 内容(iframe)** 项目拖到编辑区域，输入活动的名称和描述，输入 Web 内容的 URL，并指定 屏幕区域的大小。</span><span class="sxs-lookup"><span data-stu-id="d53d3-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="d53d3-173">将丰富内容添加到入职指南或模板</span><span class="sxs-lookup"><span data-stu-id="d53d3-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="d53d3-174">可选：在每个活动右侧的区域中，将活动分配给特定的人员或角色、添加到期日期和联系人、分配类别颜色。</span><span class="sxs-lookup"><span data-stu-id="d53d3-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="d53d3-175">将活动分配给人员或角色时，会为每个人创建一个任务。</span><span class="sxs-lookup"><span data-stu-id="d53d3-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="d53d3-176">此任务显示在 Onboard 上的 **任务** 菜单中。</span><span class="sxs-lookup"><span data-stu-id="d53d3-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="d53d3-177">[![在入职指南或模板中分配活动](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="d53d3-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="d53d3-178">选择 **保存** 保存您的工作。</span><span class="sxs-lookup"><span data-stu-id="d53d3-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="d53d3-179">要删除活动或部分，请选择活动或部分右上角的 **删除** 按钮（垃圾桶符号）。</span><span class="sxs-lookup"><span data-stu-id="d53d3-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="d53d3-180">要重新排列活动和部分，请将它们拖动到新位置。</span><span class="sxs-lookup"><span data-stu-id="d53d3-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="d53d3-181">添加或编辑联系人</span><span class="sxs-lookup"><span data-stu-id="d53d3-181">Add or edit contacts</span></span>

<span data-ttu-id="d53d3-182">您可以添加可以从第一天起帮助您的新雇员取得成功的联系人。</span><span class="sxs-lookup"><span data-stu-id="d53d3-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="d53d3-183">这些联系人可以是招聘人员、团队成员、入职联系人、指导者、管理员和 IT 支持人员。</span><span class="sxs-lookup"><span data-stu-id="d53d3-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="d53d3-184">在 **联系人** 选项卡上，选择 **新联系人**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="d53d3-185">在 **添加团队成员** 对话框中，输入联系人的姓名或电子邮件地址，输入说明联系人如何帮助新雇员的简短说明，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="d53d3-186">将联系人添加到入职指南或模板</span><span class="sxs-lookup"><span data-stu-id="d53d3-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="d53d3-187">或者，您可以在 **建议** 下选择一个或多个联系人。</span><span class="sxs-lookup"><span data-stu-id="d53d3-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="d53d3-188">选择 **保存** 保存您的工作。</span><span class="sxs-lookup"><span data-stu-id="d53d3-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="d53d3-189">要删除联系人，请选择联系人右侧的 **删除** 按钮（垃圾桶符号）。</span><span class="sxs-lookup"><span data-stu-id="d53d3-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="d53d3-190">要编辑联系人，请选择联系人右侧的 **编辑** 按钮（铅笔符号）。</span><span class="sxs-lookup"><span data-stu-id="d53d3-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="d53d3-191">添加或编辑资源</span><span class="sxs-lookup"><span data-stu-id="d53d3-191">Add or edit resources</span></span>

<span data-ttu-id="d53d3-192">您可以将有用的文件、地图和链接添加到入职指南的 **资源** 部分。</span><span class="sxs-lookup"><span data-stu-id="d53d3-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="d53d3-193">在 **资源** 选项卡上，选择 **新资源**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="d53d3-194">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d53d3-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="d53d3-195">要添加文件，请选择 **文件** 选项卡，然后将文件拖到指定区域。</span><span class="sxs-lookup"><span data-stu-id="d53d3-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="d53d3-196">（或者，单击该区域中的任意位置以浏览计算机上的文件，或选择 **浏览 OneDrive**。）输入文件的名称，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="d53d3-197">要添加链接，请选择 **链接** 选项卡，输入链接的名称和地址，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="d53d3-198">要添加地图，请选择 **地图** 选项卡，输入地图的名称和地址，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d53d3-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="d53d3-199">Onboard 将包含您指定的地址的地图。</span><span class="sxs-lookup"><span data-stu-id="d53d3-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="d53d3-200">将资源添加到入职指南或模板</span><span class="sxs-lookup"><span data-stu-id="d53d3-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="d53d3-201">选择 **保存** 保存您的工作。</span><span class="sxs-lookup"><span data-stu-id="d53d3-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="d53d3-202">要删除资源，请选择资源右侧的 **删除** 按钮（垃圾桶符号）。</span><span class="sxs-lookup"><span data-stu-id="d53d3-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="d53d3-203">要编辑联系人，请选择资源右侧的 **编辑** 按钮（铅笔符号）。</span><span class="sxs-lookup"><span data-stu-id="d53d3-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d53d3-204">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d53d3-204">Next steps</span></span>

- [<span data-ttu-id="d53d3-205">与其他参与者共享内容</span><span class="sxs-lookup"><span data-stu-id="d53d3-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="d53d3-206">查看任务和入职员工的状态</span><span class="sxs-lookup"><span data-stu-id="d53d3-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="d53d3-207">在 Onboard 中创建招聘团队</span><span class="sxs-lookup"><span data-stu-id="d53d3-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="d53d3-208">请参阅</span><span class="sxs-lookup"><span data-stu-id="d53d3-208">See also</span></span>

- [<span data-ttu-id="d53d3-209">试用或购买 Onboard 应用</span><span class="sxs-lookup"><span data-stu-id="d53d3-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="d53d3-210">Dynamics 365 Talent 新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="d53d3-210">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="d53d3-211">发布计划</span><span class="sxs-lookup"><span data-stu-id="d53d3-211">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="d53d3-212">获取 Microsoft Dynamics 365 Talent 支持</span><span class="sxs-lookup"><span data-stu-id="d53d3-212">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
