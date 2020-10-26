---
title: 连接试验和编辑变体
description: 本主题介绍了如何将第三方服务中的试验连接到 Dynamics 365 Commerce，以及如何编辑试验的变体。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930150"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="0284d-103">连接试验和编辑变体</span><span class="sxs-lookup"><span data-stu-id="0284d-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="0284d-104">本主题介绍了如何在 Commerce 中连接试验和更改您的变体，以使其与您的假设相符。</span><span class="sxs-lookup"><span data-stu-id="0284d-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so they align with your hypothesis.</span></span> <span data-ttu-id="0284d-105">下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="0284d-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0284d-106">其他步骤在单独的主题中介绍。</span><span class="sxs-lookup"><span data-stu-id="0284d-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="0284d-107">[![试验用户旅程 - 连接和编辑](./media/experimentation_connect_edit.svg)](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0284d-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="0284d-108">在第三方服务中[设置试验](experimentation-setup.md)后，您将在 Dynamics 365 Commerce 中连接试验和编辑试验变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="0284d-109">计划注意事项</span><span class="sxs-lookup"><span data-stu-id="0284d-109">Planning considerations</span></span>

<span data-ttu-id="0284d-110">在 Commerce 中连接试验之前，您需要做出一些可能影响 Commerce 管理内容的方式的决定。</span><span class="sxs-lookup"><span data-stu-id="0284d-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="0284d-111">确定试验范围</span><span class="sxs-lookup"><span data-stu-id="0284d-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="0284d-112">连接试验时，系统会提示您定义试验范围。</span><span class="sxs-lookup"><span data-stu-id="0284d-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="0284d-113">试验定义为**部分**范围或**整个**范围。</span><span class="sxs-lookup"><span data-stu-id="0284d-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="0284d-114">如果您要在页面的特定部分进行试验，则选择**部分**。</span><span class="sxs-lookup"><span data-stu-id="0284d-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="0284d-115">如果选择此选项，必须标识试验中包括哪些模块。</span><span class="sxs-lookup"><span data-stu-id="0284d-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="0284d-116">对默认页面或片段中与试验无关的部分所做的更改会在变体之间自动同步。</span><span class="sxs-lookup"><span data-stu-id="0284d-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="0284d-117">如果您要在整个页面或片段上进行试验，则选择**整个**。</span><span class="sxs-lookup"><span data-stu-id="0284d-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="0284d-118">将创建默认页面或片段的单独副本。</span><span class="sxs-lookup"><span data-stu-id="0284d-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="0284d-119">您无需选择试验中包括哪些模块，因为整个编辑界面都可以更改。</span><span class="sxs-lookup"><span data-stu-id="0284d-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="0284d-120">您可以根据需要添加、删除和重新排序模块。</span><span class="sxs-lookup"><span data-stu-id="0284d-120">You can add, delete, and re-order modules as needed.</span></span> <span data-ttu-id="0284d-121">但是，如果对与试验相关联的默认页面或片段进行了任何更改，则必须在所有变体之间手动同步这些更改。</span><span class="sxs-lookup"><span data-stu-id="0284d-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="0284d-122">如果您将试验与使用布局的页面相关联，则只能将试验的范围设置为**整个**。</span><span class="sxs-lookup"><span data-stu-id="0284d-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="0284d-123">决定是否要计划发布试验的时间</span><span class="sxs-lookup"><span data-stu-id="0284d-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="0284d-124">如果您想要计划将试验发布到活动站点的时间，请确保在连接试验*之前*，要与试验关联的内容在发布组中可用。</span><span class="sxs-lookup"><span data-stu-id="0284d-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="0284d-125">有关发布组的详细信息，请参考[使用发布组](publish-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="0284d-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="0284d-126">连接试验</span><span class="sxs-lookup"><span data-stu-id="0284d-126">Connect your experiment</span></span>
<span data-ttu-id="0284d-127">若要连接试验，您将启动**连接试验**向导。</span><span class="sxs-lookup"><span data-stu-id="0284d-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="0284d-128">该向导将引导您完成连接试验所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="0284d-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="0284d-129">完成向导后，您的试验已连接，变体已创建并可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="0284d-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

1. <span data-ttu-id="0284d-130">若要启动向导，请在站点构建器中选择**试验**选项卡，然后选择**连接**。</span><span class="sxs-lookup"><span data-stu-id="0284d-130">To launch the wizard, select the **Experiments** tab in site builder and then select **Connect**.</span></span> <span data-ttu-id="0284d-131">或者，可以从页面或片段编辑器中访问该向导。</span><span class="sxs-lookup"><span data-stu-id="0284d-131">Alternatively, the wizard can be accessed from a page or fragment editor.</span></span> <span data-ttu-id="0284d-132">在编辑模式下，在命令栏中选择**连接试验**。</span><span class="sxs-lookup"><span data-stu-id="0284d-132">In edit mode, select **Connect experiment** in the command bar.</span></span>

> [!NOTE]
> <span data-ttu-id="0284d-133">一个页面一次只能连接到一个试验。</span><span class="sxs-lookup"><span data-stu-id="0284d-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="0284d-134">若要将页面连接到其他试验，请首先删除该页面当前连接到的试验。</span><span class="sxs-lookup"><span data-stu-id="0284d-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="0284d-135">选择您要在其上运行试验的页面或片段。</span><span class="sxs-lookup"><span data-stu-id="0284d-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="0284d-136">根据您在上述[确定试验范围](#determine-the-scope-of-your-experiment)部分中做出的选择，将试验范围设置为**部分**或**整个**。</span><span class="sxs-lookup"><span data-stu-id="0284d-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="0284d-137">如果要在整个页面或片段上进行试验，则必须启用**在页面或片段上试验**功能标志。</span><span class="sxs-lookup"><span data-stu-id="0284d-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="0284d-138">有关详细信息，请参考 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)主题。</span><span class="sxs-lookup"><span data-stu-id="0284d-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="0284d-139">在向导的最后一步中，选择**生成变体并退出向导**。</span><span class="sxs-lookup"><span data-stu-id="0284d-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="0284d-140">为试验创建了变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="0284d-141">编辑变体</span><span class="sxs-lookup"><span data-stu-id="0284d-141">Edit your variations</span></span>
<span data-ttu-id="0284d-142">退出向导时，将为您创建变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="0284d-143">接下来，您将编辑变体，以便它们反映您需要在试验假设中验证的选择。</span><span class="sxs-lookup"><span data-stu-id="0284d-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="0284d-144">选择与您在上述[确定试验范围](#determine-the-scope-of-your-experiment)部分中为试验选择的范围相对应的以下过程之一。</span><span class="sxs-lookup"><span data-stu-id="0284d-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="0284d-145">编辑具有部分范围的试验的变体</span><span class="sxs-lookup"><span data-stu-id="0284d-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="0284d-146">如果您在**连接试验**向导中将试验的范围定义为**部分**，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0284d-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="0284d-147">在编辑器视图中，使用命令栏下方的变体下拉菜单，基于您的原始假设编辑每个变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="0284d-148">您可能还想通过使变体之一保持不变来建立控件或基本变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="0284d-149">选择要在其上进行试验的模块，选择省略号 (...)，然后选择**添加到试验**。</span><span class="sxs-lookup"><span data-stu-id="0284d-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="0284d-150">编辑具有整个范围的试验的变体</span><span class="sxs-lookup"><span data-stu-id="0284d-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="0284d-151">如果您在**连接试验**向导中将试验的范围定义为**整个**，在编辑器视图中时，使用命令栏下方的变体下拉菜单根据您的原始假设编辑每个变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="0284d-152">在任何一种情况下，您可能还想通过使变体之一保持不变来建立控件或基本变体。</span><span class="sxs-lookup"><span data-stu-id="0284d-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="0284d-153">上一步</span><span class="sxs-lookup"><span data-stu-id="0284d-153">Previous step</span></span>
[<span data-ttu-id="0284d-154">设置试验</span><span class="sxs-lookup"><span data-stu-id="0284d-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="0284d-155">后续步骤</span><span class="sxs-lookup"><span data-stu-id="0284d-155">Next step</span></span>
[<span data-ttu-id="0284d-156">预览和发布试验</span><span class="sxs-lookup"><span data-stu-id="0284d-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
