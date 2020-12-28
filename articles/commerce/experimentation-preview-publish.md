---
title: 预览和发布试验
description: 本主题介绍了如何从 Dynamics 365 Commerce 中预览和发布试验。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "4410624"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="bc045-103">预览和发布试验</span><span class="sxs-lookup"><span data-stu-id="bc045-103">Preview and publish an experiment</span></span>

<span data-ttu-id="bc045-104">本主题介绍了如何在[连接试验和编辑变体](experimentation-connect-edit.md)之后在 Dynamics 365 Commerce 中预览和发布试验。</span><span class="sxs-lookup"><span data-stu-id="bc045-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="bc045-105">下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="bc045-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bc045-106">其他步骤在单独的主题中介绍。</span><span class="sxs-lookup"><span data-stu-id="bc045-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="bc045-107">[![试验用户旅程 - 预览和发布](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bc045-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="bc045-108">预览试验变体</span><span class="sxs-lookup"><span data-stu-id="bc045-108">Preview your experiment variations</span></span>
<span data-ttu-id="bc045-109">您可以预览变体并继续进行编辑，直到它们实现您的预期效果。</span><span class="sxs-lookup"><span data-stu-id="bc045-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="bc045-110">若要在 Commerce 站点构建器中预览试验变体，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="bc045-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bc045-111">从命令栏下方的变体下拉菜单中，选择要预览的内容。</span><span class="sxs-lookup"><span data-stu-id="bc045-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="bc045-112">在命令栏中，选择 **预览**。</span><span class="sxs-lookup"><span data-stu-id="bc045-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="bc045-113">显示内容发布时的预览情况。</span><span class="sxs-lookup"><span data-stu-id="bc045-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="bc045-114">若要预览其他变体，请从变体下拉菜单中选择它，然后再次选择 **预览**。</span><span class="sxs-lookup"><span data-stu-id="bc045-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="bc045-115">发布试验</span><span class="sxs-lookup"><span data-stu-id="bc045-115">Publish your experiment</span></span>
<span data-ttu-id="bc045-116">如果您没有使用发布组来计划试验上线的时间，并且想立即发布，请在命令栏中选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="bc045-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="bc045-117">将发布属于该试验的所有变体。</span><span class="sxs-lookup"><span data-stu-id="bc045-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="bc045-118">如果页面上有取消发布的 URL，必须首先发布该 URL，否则它将对您的网站用户不可见。</span><span class="sxs-lookup"><span data-stu-id="bc045-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="bc045-119">有关详细信息，请参阅[保存、预览和发布页面](save-preview-publish-page.md)。</span><span class="sxs-lookup"><span data-stu-id="bc045-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="bc045-120">使用发布组计划试验上线的时间</span><span class="sxs-lookup"><span data-stu-id="bc045-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="bc045-121">可以使用发布组计划发布在站点构建器中创建的变体。</span><span class="sxs-lookup"><span data-stu-id="bc045-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="bc045-122">在发布组中，您可以通过选择左侧导航窗格中的 **试验** 将页面或片段连接到试验。</span><span class="sxs-lookup"><span data-stu-id="bc045-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="bc045-123">您也可以通过选择 **页面** 或 **片段** 并按照[连接试验和编辑变体](experimentation-connect-edit.md)中的说明来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="bc045-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="bc045-124">有关发布组的信息，请参阅[使用发布组](publish-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="bc045-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="bc045-125">当使用发布组进行试验时，有一些需要注意的重要考虑事项。</span><span class="sxs-lookup"><span data-stu-id="bc045-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="bc045-126">当您将运行了试验的页面或片段添加到发布组时，该试验将从发布组的页面或片段中删除。</span><span class="sxs-lookup"><span data-stu-id="bc045-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="bc045-127">连接到活动站点中的页面的试验不适用于发布组中的页面，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="bc045-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="bc045-128">同样，在活动站点中运行了试验的页面也不适用于发布组中的其他试验，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="bc045-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="bc045-129">当您发布或计划发布组时，发布组中的所有内容都将发布，而不管是否有与发布组关联的试验。</span><span class="sxs-lookup"><span data-stu-id="bc045-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="bc045-130">由于发布组在发布到活动站点后仍会继续存在，因此发布组中的试验也将继续存在。</span><span class="sxs-lookup"><span data-stu-id="bc045-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="bc045-131">因此，您将无法将其他试验与同一页面或片段相关联。</span><span class="sxs-lookup"><span data-stu-id="bc045-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="bc045-132">为了避免此限制，请删除具有持续性试验的所有发布组。</span><span class="sxs-lookup"><span data-stu-id="bc045-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="bc045-133">同样，如果您要删除的试验不仅在活动站点中，也存在于发布组中，请先将其从发布组中删除。</span><span class="sxs-lookup"><span data-stu-id="bc045-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="bc045-134">上一步</span><span class="sxs-lookup"><span data-stu-id="bc045-134">Previous step</span></span>
[<span data-ttu-id="bc045-135">连接和编辑试验</span><span class="sxs-lookup"><span data-stu-id="bc045-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="bc045-136">后续步骤</span><span class="sxs-lookup"><span data-stu-id="bc045-136">Next step</span></span>
[<span data-ttu-id="bc045-137">运行和监视试验</span><span class="sxs-lookup"><span data-stu-id="bc045-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
