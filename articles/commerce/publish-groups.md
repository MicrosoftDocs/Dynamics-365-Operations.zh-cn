---
title: 使用发布组
description: 本主题介绍 Microsoft Dynamics 365 Commerce 中的发布组功能。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 374a6c7dd33440903babbc8232f580ac2b68df82
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003157"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="9d0e7-103">使用发布组</span><span class="sxs-lookup"><span data-stu-id="9d0e7-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9d0e7-104">本主题介绍 Microsoft Dynamics 365 Commerce 中的发布组功能。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9d0e7-105">概览</span><span class="sxs-lookup"><span data-stu-id="9d0e7-105">Overview</span></span>

<span data-ttu-id="9d0e7-106">电子商务网站全年会不断更新新内容。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="9d0e7-107">更新通常是围绕繁忙的电子商务活动（如假期、季节性市场营销活动或促销启动）成批发布。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="9d0e7-108">这些更新通常要求在单个操作中同时筹划、验证和发布网站内容组（例如，页面、图像、片段和模板）。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="9d0e7-109">将项目分组为一起发布项目的逻辑集（每个集都有自己的生命周期）的能力，将为站点作者提供许多好处。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="9d0e7-110">在 Commerce 中，这些逻辑集称为发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="9d0e7-111">他们使站点作者可以将更新集作为自己的可配置、可测试且可发布的实体进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="9d0e7-112">作者可以在筹划好的发布组中预览更新，而不会影响活动站点或其他独立的发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="9d0e7-113">然后，作者可以计划发布操作，以将发布组中的所有项目同时发布到活动站点。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="9d0e7-114">对于许多会通过基于活动的站点更新里程碑获得可观年度收入的企业级公司来说，能够对要发布的更新进行分组、预览和计划非常重要。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="9d0e7-115">公司可能会因无法顺利进行的缓慢或无效的内容发布而产生成本。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="9d0e7-116">发布组有助于确保活动启动能够得到按时地安排、验证和发布。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="9d0e7-117">无论是大是小，发布组都会提供宝贵的工具集，可帮助作者安排和简化正在进行的站点更新任务。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="9d0e7-118">何时使用发布组</span><span class="sxs-lookup"><span data-stu-id="9d0e7-118">When to use publish groups</span></span>

<span data-ttu-id="9d0e7-119">任何时候当您必须筹划多个文档并要一起发布时，都可以使用发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="9d0e7-120">例如，如果您的网站每个季节更新一次内容，则可以为这些季节性市场营销活动创建发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="9d0e7-121">您的“秋季季节性更新”发布组可以包含新的季节性图像、带有季节性市场营销消息的片段、包含季节性产品集合的页面，或其他季节性网站更新。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="9d0e7-122">发布组的一个优点是您可以并行筹划进行多个更新。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="9d0e7-123">例如，在“秋季季节性更新”发布组更新之后不久，可能会有特定假期周末的内容更新。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="9d0e7-124">在这种情况下，您可以在筹划后续的“秋季假期更新”发布组的内容的同时，筹划“秋季季节性更新”发布组的内容。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="9d0e7-125">每个发布组包含其自己的一组独特页面、图像、片段、模板等。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="9d0e7-126">您可以在并发时间线上独立地筹划、预览和验证这两个发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="9d0e7-127">然后可以计划让每个发布组在特定日期和时间在您的站点上线。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="9d0e7-128">打开发布组功能</span><span class="sxs-lookup"><span data-stu-id="9d0e7-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="9d0e7-129">发布组功能是可选的，要使用，必须自行为站点打开。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="9d0e7-130">要在 Commerce 创作工具中打开站点的发布组功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="9d0e7-131">在左侧导航窗格中，选择**站点设置**将其展开。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="9d0e7-132">在**站点设置**下，选择**功能**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="9d0e7-133">将**发布组**选项设置为**开**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="9d0e7-134">创建发布组</span><span class="sxs-lookup"><span data-stu-id="9d0e7-134">Create a publish group</span></span>

<span data-ttu-id="9d0e7-135">要在 Commerce 创作工具中为站点创建发布组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="9d0e7-136">在左侧导航窗格中，选择**发布组**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="9d0e7-137">在顶部命令栏中，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="9d0e7-138">在**创建发布组**对话框中，在**发布组名称**下，输入一个描述性名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="9d0e7-139">然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="9d0e7-140">设置发布组创作上下文</span><span class="sxs-lookup"><span data-stu-id="9d0e7-140">Set the publish group authoring context</span></span>

<span data-ttu-id="9d0e7-141">在 Commerce 中，默认的创作上下文是活动站点上下文。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="9d0e7-142">活动站点创作上下文是默认视图，您无需使用发布组即可在其中直接查看和更改网站。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="9d0e7-143">它代表对站点的已发布版本的最新的直接更新。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="9d0e7-144">如果左侧导航窗格中**发布组**下的上下文控件显示名称**活动站点**，说明您正在活动站点创作上下文中工作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="9d0e7-145">**活动站点**是上下文控件的默认名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="9d0e7-146">否则，上下文控件将显示发布组的名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="9d0e7-147">要在发布组中工作，必须为其切换到发布组创作上下文。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="9d0e7-148">若要设置发布组上下文，请按照下列步骤之一进行操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="9d0e7-149">在左侧导航窗格中，直接在**发布组**下选择上下文控件，然后在显示的选项列表中选择发布组的名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="9d0e7-150">上下文控件已被重命名，显示发布组的名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="9d0e7-151">在左侧导航窗格中，选择**发布组**，然后，在**发布组**下，选择发布组的名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="9d0e7-152">上下文控件已被重命名，显示发布组的名称。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="9d0e7-153">设置发布组创作上下文后，您将在预览和编辑站点内容时在该发布组上下文中工作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="9d0e7-154">若要返回到默认的活动站点创作上下文，请选择上下文控件，然后选择**活动站点**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="9d0e7-155">将页面或其他项目添加到发布组</span><span class="sxs-lookup"><span data-stu-id="9d0e7-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="9d0e7-156">选择发布组创作上下文，并且左侧导航窗格中的上下文控件显示其名称之后，您可以像在默认活动站点上下文中一样创建内容。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="9d0e7-157">您还可以从其他发布组或活动站点上下文添加现有页面或其他项目。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="9d0e7-158">要将现有页面复制到发布组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="9d0e7-159">选择要从其复制的创作上下文，然后在左侧导航窗格中选择**页面**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="9d0e7-160">选择要添加到发布组的页面。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="9d0e7-161">在命令栏中，选择**复制到发布组**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="9d0e7-162">在**选择发布组**对话框中，选择要添加页面的发布组，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="9d0e7-163">您可以使用相同的基本步骤来创建自定义的产品页面、URL、模板、布局、片段和媒体库资产，或将这些类型的现有项目添加到发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="9d0e7-164">验证发布组</span><span class="sxs-lookup"><span data-stu-id="9d0e7-164">Validate a publish group</span></span>

<span data-ttu-id="9d0e7-165">为确保发布组内容中的所有依赖项都符合要求并且所有验证都能够通过，您可以在计划发布操作之前运行验证来发现必须解决的所有问题。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="9d0e7-166">若要在计划之前验证发布组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="9d0e7-167">在左侧导航窗格中，选择**发布组**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="9d0e7-168">选择要验证的发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="9d0e7-169">在命令栏中，选择**验证**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="9d0e7-170">验证对发布组中的所有内容运行。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="9d0e7-171">将阻止发布操作成功的任何问题都会显示在将出现在右上角的通知框中。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="9d0e7-172">计划发布组时，将始终自动运行验证。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="9d0e7-173">但是，命令栏中的**验证**按钮很有用，因为它有助于发现在尝试计划发布组上线之前必须解决的问题。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="9d0e7-174">计划发布组上线</span><span class="sxs-lookup"><span data-stu-id="9d0e7-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="9d0e7-175">若要计划发布组在您的站点上线，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="9d0e7-176">在左侧导航窗格中，选择**发布组**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="9d0e7-177">在**发布组**下，选择要计划的发布组。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="9d0e7-178">在命令栏中，选择**编辑计划**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="9d0e7-179">将显示**编辑计划**对话框。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="9d0e7-180">选择发布组应该上线的日期和时间，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="9d0e7-181">要取消对发布组的计划，请遵循相同步骤，但是在**编辑计划**对话框中选择**取消发布组计划**。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="9d0e7-182">很大的发布组在计划的发布时间到达时可能需要一到两分钟才能发布。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="9d0e7-183">请注意，发布操作不是即时的，较小的发布组将发布得更快。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="9d0e7-184">发布组常见问题</span><span class="sxs-lookup"><span data-stu-id="9d0e7-184">Publish groups FAQ</span></span>

<span data-ttu-id="9d0e7-185">**一个发布组中可以有多少个项目？**</span><span class="sxs-lookup"><span data-stu-id="9d0e7-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="9d0e7-186">当前，每个发布组限制为 2,000 个项目。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="9d0e7-187">请注意，很大的发布组在计划的发布时间到达时可能需要几分钟才能发布。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="9d0e7-188">**发布组是否像软件开发术语中的代码“分支”？**</span><span class="sxs-lookup"><span data-stu-id="9d0e7-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="9d0e7-189">是，也不是。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-189">Yes and no.</span></span> <span data-ttu-id="9d0e7-190">发布组可以被视为站点的分支版本。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="9d0e7-191">这样看，它们的确像分支。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-191">In that way, they do act like branches.</span></span> <span data-ttu-id="9d0e7-192">但是，没有在单个项目级别的合并概念。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="9d0e7-193">最后发布的项目会覆盖以前存在的项目，最新的发布操作始终会取代之前的发布操作。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="9d0e7-194">**我可以计划两个发布组同时上线吗？**</span><span class="sxs-lookup"><span data-stu-id="9d0e7-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="9d0e7-195">编号</span><span class="sxs-lookup"><span data-stu-id="9d0e7-195">No.</span></span> <span data-ttu-id="9d0e7-196">出于性能和冲突原因，系统将强制您将计划的发布组的上线错开，中间至少间隔五分钟。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="9d0e7-197">**我可以使用发布组计划折扣和产品更新等全渠道后勤办公室项目吗？**</span><span class="sxs-lookup"><span data-stu-id="9d0e7-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="9d0e7-198">当前，发布组功能仅支持网站内容。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="9d0e7-199">但是，Microsoft 意识到与后勤办公室促销场景集成，对于全渠道市场活动启动的协调和自动化可能很有价值。</span><span class="sxs-lookup"><span data-stu-id="9d0e7-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d0e7-200">其他资源</span><span class="sxs-lookup"><span data-stu-id="9d0e7-200">Additional resources</span></span>

[<span data-ttu-id="9d0e7-201">添加内容的方法</span><span class="sxs-lookup"><span data-stu-id="9d0e7-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="9d0e7-202">页面模型词汇表</span><span class="sxs-lookup"><span data-stu-id="9d0e7-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="9d0e7-203">文档状态和生命周期</span><span class="sxs-lookup"><span data-stu-id="9d0e7-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="9d0e7-204">使用模块</span><span class="sxs-lookup"><span data-stu-id="9d0e7-204">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="9d0e7-205">使用片段</span><span class="sxs-lookup"><span data-stu-id="9d0e7-205">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="9d0e7-206">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="9d0e7-206">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9d0e7-207">自定义站点导航</span><span class="sxs-lookup"><span data-stu-id="9d0e7-207">Customize site navigation</span></span>](customize-site-navigation.md)
