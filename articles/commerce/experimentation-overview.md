---
title: Dynamics 365 Commerce 中的试验
description: 通过试验，可以在站点构建器中创建、编辑和管理页面布局和内容处理。 为电子商务页面和页面中的实体启用了端到端试验支持。
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
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "4410625"
---
# <a name="experimentation-in-dynamics-365-commerce"></a><span data-ttu-id="607e9-104">Dynamics 365 Commerce 中的试验</span><span class="sxs-lookup"><span data-stu-id="607e9-104">Experimentation in Dynamics 365 Commerce</span></span>
<span data-ttu-id="607e9-105">使用 Dynamics 365 Commerce 中的试验以验证有关您的电子商务页面有效性的假设，并以数据驱动的信心做出决策。</span><span class="sxs-lookup"><span data-stu-id="607e9-105">Use experimentation in Dynamics 365 Commerce to validate hypotheses about the effectiveness of your e-Commerce pages and make decisions with data-driven confidence.</span></span> <span data-ttu-id="607e9-106">Commerce 支持在页面、模块和片段上进行 A/B 测试，并使您能够度量建议的更改对网站的影响。</span><span class="sxs-lookup"><span data-stu-id="607e9-106">Commerce supports A/B testing on pages, modules, and fragments and enables you to measure the impact of proposed changes to your website.</span></span>

<span data-ttu-id="607e9-107">您可以在 Commerce 站点构建器中创建、编辑和管理页面和内容处理（称为 **变体**）。</span><span class="sxs-lookup"><span data-stu-id="607e9-107">You can create, edit, and manage page and content treatments known as **variations** in Commerce site builder.</span></span> <span data-ttu-id="607e9-108">Commerce 与第三方服务集成，可用于创建试验和处理分配。</span><span class="sxs-lookup"><span data-stu-id="607e9-108">Commerce integrates with third-party services that you can use to create experiments and treatment assignments.</span></span> <span data-ttu-id="607e9-109">在 Commerce 中捕获的实时事件流可启用在第三方服务中定义试验结果的分析。</span><span class="sxs-lookup"><span data-stu-id="607e9-109">Real-time event streams captured in Commerce enable the analytics that define the experiment results in the third-party service.</span></span> <span data-ttu-id="607e9-110">然后，您可以利用这些分析来帮助支持或驳倒您的假设。</span><span class="sxs-lookup"><span data-stu-id="607e9-110">You can then leverage these analytics to help support or refute your hypothesis.</span></span>

## <a name="set-up-prerequisites"></a><span data-ttu-id="607e9-111"> 设置先决条件</span><span class="sxs-lookup"><span data-stu-id="607e9-111">Set up prerequisites</span></span>
1. <span data-ttu-id="607e9-112">**获取正确的 Commerce 版本** - 将您的模块库、在线渠道可扩展性软件开发工具包 (SDK) 和 Commerce Scale Unit 升级到 Commerce 版本 10.0.13 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="607e9-112">**Get the correct version of Commerce** - Upgrade your module library, online channel extensibility software development kit (SDK), and Commerce Scale Unit to Commerce version 10.0.13 or later.</span></span>
1. <span data-ttu-id="607e9-113">**设置试验连接器** - 试验连接器允许 Commerce 与第三方服务连接，以检索试验列表并确定何时向用户展示试验。</span><span class="sxs-lookup"><span data-stu-id="607e9-113">**Set up an experimentation connector** - An experimentation connector allows Commerce to connect with third-party services to retrieve the list of experiments and determine when to show an experiment to a user.</span></span> <span data-ttu-id="607e9-114">您可以从 [AppSource](https://appsource.microsoft.com) 中购买第三方连接器。</span><span class="sxs-lookup"><span data-stu-id="607e9-114">You can purchase a third-party connector from [AppSource](https://appsource.microsoft.com).</span></span> <span data-ttu-id="607e9-115">请按照发布者提供的安装说明操作。</span><span class="sxs-lookup"><span data-stu-id="607e9-115">Follow the setup instructions provided by the publisher.</span></span> <span data-ttu-id="607e9-116">您也可以使用 Commerce 的示例测试连接器来测试试验工作流，而无需配置外部服务。</span><span class="sxs-lookup"><span data-stu-id="607e9-116">You can alternatively use the sample test connector from Commerce to test the experimentation workflow without needing to configure an external service.</span></span> <span data-ttu-id="607e9-117">有关详细信息，请参阅[配置和启用连接器](e-commerce-extensibility/connectors.md)。</span><span class="sxs-lookup"><span data-stu-id="607e9-117">For more information, see [Configure and enable connectors](e-commerce-extensibility/connectors.md).</span></span> 
1. <span data-ttu-id="607e9-118">**在 Commerce 中打开试验功能标志** - 您可以通过转到 **租户设置 > 功能** 在租户级别上启用试验，如果是在站点级别上启用，则转到 **站点设置 > 功能**。</span><span class="sxs-lookup"><span data-stu-id="607e9-118">**Turn on the experimentation feature flags in Commerce** - You can enable experimentation at the tenant level by going to **Tenant Settings > Features** or at the site level at **Site Settings > Features**.</span></span>
    - <span data-ttu-id="607e9-119">启用 **试验** 标志以创建页面内模块的试验变体，而不会影响或复制不属于试验的其他内容。</span><span class="sxs-lookup"><span data-stu-id="607e9-119">Enable the **Experimentation** flag to create experiment variations of modules within a page without affecting or copying other content that isn't part of the experiment.</span></span> <span data-ttu-id="607e9-120">这样可以确保试验外部正在进行的内容更新在试验生命周期中保持同步。</span><span class="sxs-lookup"><span data-stu-id="607e9-120">This ensures that ongoing content updates outside the experiment stay in sync during the experiment lifecycle.</span></span> <span data-ttu-id="607e9-121">禁用此标志将阻止向用户显示所有试验，并删除站点构建器中的所有编辑功能。</span><span class="sxs-lookup"><span data-stu-id="607e9-121">Disabling this flag stops all experiments from being shown to users and removes all editing functions within site builder.</span></span>
    - <span data-ttu-id="607e9-122">启用 **在页面或片段上试验** 标志以在页面或片段上运行试验。</span><span class="sxs-lookup"><span data-stu-id="607e9-122">Enable the **Experiment on pages or fragments** flag to run experiments on a page or fragment.</span></span> <span data-ttu-id="607e9-123">这将为页面或片段中的所有模块创建整个页面或片段的完整实例副本。</span><span class="sxs-lookup"><span data-stu-id="607e9-123">This creates a full instance copy of the entire page or fragment for all modules within the page or fragment.</span></span> <span data-ttu-id="607e9-124">当您要测试全面的内容更改，或者不需要在各个实例之间同步正在进行的内容更改时，请使用此模式。</span><span class="sxs-lookup"><span data-stu-id="607e9-124">Use this mode when you want to test comprehensive content changes, or where synchronizing ongoing content changes across instances isn't a concern.</span></span> <span data-ttu-id="607e9-125">禁用此标志可防止在页面和片段上创建和编辑新试验。</span><span class="sxs-lookup"><span data-stu-id="607e9-125">Disabling this flag prevents creation and editing of new experiments on pages and fragments.</span></span>
    > [!NOTE]
    > <span data-ttu-id="607e9-126">若要使 **在页面或片段上试验** 功能生效，还必须启用 **试验** 标志。</span><span class="sxs-lookup"><span data-stu-id="607e9-126">The **Experimentation** flag must also be enabled for the **Experiment on pages or fragments** functionality to work.</span></span>
    
## <a name="experimentation-lifecycle"></a><span data-ttu-id="607e9-127">试验生命周期</span><span class="sxs-lookup"><span data-stu-id="607e9-127">Experimentation lifecycle</span></span>
<span data-ttu-id="607e9-128">设置试验，创建变体和运行试验是一个迭代过程。</span><span class="sxs-lookup"><span data-stu-id="607e9-128">Setting up an experiment, creating variations, and running an experiment is an iterative process.</span></span> <span data-ttu-id="607e9-129">下图说明了 Commerce 和第三方服务中的试验生命周期。</span><span class="sxs-lookup"><span data-stu-id="607e9-129">The diagram below illustrates the experimentation lifecycle in Commerce and the third-party service.</span></span> 

<span data-ttu-id="607e9-130">[ ![试验生命周期](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="607e9-130">[ ![Experimentation lifecycle](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span></span>

<span data-ttu-id="607e9-131">若要了解有关试验过程中每个步骤的详细信息，请参考以下主题。</span><span class="sxs-lookup"><span data-stu-id="607e9-131">To learn more about each step in the experimentation process, refer to the following topics.</span></span>
- [<span data-ttu-id="607e9-132">标识假设并确定试验指标</span><span class="sxs-lookup"><span data-stu-id="607e9-132">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md)
- [<span data-ttu-id="607e9-133">设计试验</span><span class="sxs-lookup"><span data-stu-id="607e9-133">Set up an experiment</span></span>](experimentation-setup.md)
- [<span data-ttu-id="607e9-134">连接和编辑试验</span><span class="sxs-lookup"><span data-stu-id="607e9-134">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
- [<span data-ttu-id="607e9-135">预览并发布试验</span><span class="sxs-lookup"><span data-stu-id="607e9-135">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
- [<span data-ttu-id="607e9-136">运行和监视试验</span><span class="sxs-lookup"><span data-stu-id="607e9-136">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
- [<span data-ttu-id="607e9-137">加入变量并完成试验</span><span class="sxs-lookup"><span data-stu-id="607e9-137">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)

> [!NOTE]
> <span data-ttu-id="607e9-138">若要了解试验在生命周期中的位置，请选择站点构建器的左侧导航窗格中的 **试验**。</span><span class="sxs-lookup"><span data-stu-id="607e9-138">To learn where an experiment is in the lifecycle, select **Experiments** in the left navigation pane of site builder.</span></span> <span data-ttu-id="607e9-139">将显示试验列表，其中包含 Commerce 和第三方服务中每个试验的状态。</span><span class="sxs-lookup"><span data-stu-id="607e9-139">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service.</span></span> <span data-ttu-id="607e9-140">有关详细信息，请参阅[查看试验的状态](experimentation-status.md)。</span><span class="sxs-lookup"><span data-stu-id="607e9-140">For more information, see [Review the status of an experiment](experimentation-status.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="607e9-141">后续步骤</span><span class="sxs-lookup"><span data-stu-id="607e9-141">Next step</span></span>
[<span data-ttu-id="607e9-142">标识假设并确定试验的成功指标</span><span class="sxs-lookup"><span data-stu-id="607e9-142">Identify a hypothesis and determine success metrics for an experiment</span></span>](experimentation-identify.md) 
