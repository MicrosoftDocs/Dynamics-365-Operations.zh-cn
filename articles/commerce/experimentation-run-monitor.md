---
title: 运行和监视试验
description: 本主题介绍了如何在第三方服务中运行和监视试验。 它还介绍了如何在试验开始后更改变体。
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
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930147"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="041ec-104">运行和监视试验</span><span class="sxs-lookup"><span data-stu-id="041ec-104">Run and monitor an experiment</span></span>

<span data-ttu-id="041ec-105">本主题介绍了如何在第三方应用中运行和监视试验，以及如何更改变体（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="041ec-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="041ec-106">在完成本主题中的步骤之前，您需要在 Commerce 中[发布](experimentation-preview-publish.md)试验。</span><span class="sxs-lookup"><span data-stu-id="041ec-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="041ec-107">下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="041ec-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="041ec-108">其他步骤在单独的主题中介绍。</span><span class="sxs-lookup"><span data-stu-id="041ec-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="041ec-109">[![试验用户旅程 - 运行和监视](./media/experimentation_run_monitor.svg)](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="041ec-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="041ec-110">发布变体后，完成在 Commerce 中运行试验所需的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="041ec-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="041ec-111">下一步是确定在每个用户请求页面时向他们显示哪个变体。</span><span class="sxs-lookup"><span data-stu-id="041ec-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="041ec-112">第三方服务可以做出决定，但是首先您必须在服务中激活试验。</span><span class="sxs-lookup"><span data-stu-id="041ec-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="041ec-113">由于激活试验的步骤因服务而异，因此您需要按照服务或提供商提供的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="041ec-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="041ec-114">如果未激活试验，用户将仅看到页面的默认版本 - 不显示任何变体。</span><span class="sxs-lookup"><span data-stu-id="041ec-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="041ec-115">您需要保持试验运行足够长的时间以收集数据，从而得到统计上有效的结果。</span><span class="sxs-lookup"><span data-stu-id="041ec-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="041ec-116">在运行试验时，使用第三方服务监视与试验相关的数据和分析。</span><span class="sxs-lookup"><span data-stu-id="041ec-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="041ec-117">调整您的变体</span><span class="sxs-lookup"><span data-stu-id="041ec-117">Adjust your variations</span></span>
<span data-ttu-id="041ec-118">如果出于任何原因需要修改变体，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="041ec-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="041ec-119">如果您对 Commerce 或第三方服务中的实时试验进行了更改，则结果可能会受到重大影响。</span><span class="sxs-lookup"><span data-stu-id="041ec-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="041ec-120">考虑继续完成试验，然后为重大更改创建新的试验。</span><span class="sxs-lookup"><span data-stu-id="041ec-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="041ec-121">在站点构建器中，转到**试验**选项卡，然后选择试验。</span><span class="sxs-lookup"><span data-stu-id="041ec-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="041ec-122">从下拉菜单中选择要更新的变体。</span><span class="sxs-lookup"><span data-stu-id="041ec-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="041ec-123">进行所需更改，然后预览和发布变体。</span><span class="sxs-lookup"><span data-stu-id="041ec-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="041ec-124">有关详细信息，请参阅[预览和发布试验](experimentation-preview-publish.md)。</span><span class="sxs-lookup"><span data-stu-id="041ec-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="041ec-125">转到第三方服务以进行与试验设置相关的任何更改。</span><span class="sxs-lookup"><span data-stu-id="041ec-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="041ec-126">上一步</span><span class="sxs-lookup"><span data-stu-id="041ec-126">Previous step</span></span>
[<span data-ttu-id="041ec-127">预览和发布试验</span><span class="sxs-lookup"><span data-stu-id="041ec-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="041ec-128">后续步骤</span><span class="sxs-lookup"><span data-stu-id="041ec-128">Next step</span></span>
[<span data-ttu-id="041ec-129">促进变体和完成试验</span><span class="sxs-lookup"><span data-stu-id="041ec-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
