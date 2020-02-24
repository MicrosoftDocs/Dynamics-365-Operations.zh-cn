---
title: 主计划设置向导
description: 此主题介绍用于设置主计划的各种重要策略和参数。
author: t-benebo
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 9d7da31f2df31c7e5cbac73b3232233090ac369e
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031059"
---
# <a name="master-planning-setup-wizard"></a><span data-ttu-id="a04a1-103">主计划设置向导</span><span class="sxs-lookup"><span data-stu-id="a04a1-103">Master planning setup wizard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a04a1-104">本主题提供针对**主计划设置向导**的指南。</span><span class="sxs-lookup"><span data-stu-id="a04a1-104">This topic provides a guide for the **Master planning setup wizard**.</span></span> <span data-ttu-id="a04a1-105">介绍如何计算参数建议，还提供示例来显示不同公司如何根据业务需要设置主计划。</span><span class="sxs-lookup"><span data-stu-id="a04a1-105">It explains how parameter suggestions are calculated and also provides examples that show how different companies set up master planning, based on their business needs.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

<span data-ttu-id="a04a1-106">YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含 [Dynamics 365 Supply Chain Management 中的主计划设置向导](https://youtu.be/c-e6n-8rZb4)视频（上面显示的）。</span><span class="sxs-lookup"><span data-stu-id="a04a1-106">The [Master planning setup wizard in Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


## <a name="specific-requirements-of-your-company"></a><span data-ttu-id="a04a1-107">您的公司的具体要求</span><span class="sxs-lookup"><span data-stu-id="a04a1-107">Specific requirements of your company</span></span>

<span data-ttu-id="a04a1-108">向导的第一页询问公司的具体要求。</span><span class="sxs-lookup"><span data-stu-id="a04a1-108">The first page of the wizard asks about the specific requirements of your company.</span></span> <span data-ttu-id="a04a1-109">您对这些问题的回答不必精确，但是您应该可以提供法人的大致物料和计划订单数量。</span><span class="sxs-lookup"><span data-stu-id="a04a1-109">Your answers to these questions don't have to be exact, but you should be able to provide a rough approximation of the number of items and planned orders that there will be for the legal entity.</span></span> <span data-ttu-id="a04a1-110">您的回答用于配置为法人应用的参数，而不仅是应用于所选主计划的参数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-110">Your answers are used to configure parameters that apply to your legal entity, not just to the master plan that you selected.</span></span> <span data-ttu-id="a04a1-111">以下部分介绍计算的参数和使用的公式。</span><span class="sxs-lookup"><span data-stu-id="a04a1-111">The following sections describe the parameters that are calculated and the formulas that are used.</span></span>

### <a name="number-of-threads"></a><span data-ttu-id="a04a1-112">线程数</span><span class="sxs-lookup"><span data-stu-id="a04a1-112">Number of threads</span></span>

- <span data-ttu-id="a04a1-113">**如果制造任何物料：** 线程数 = 计划订单数 ÷ 1,000</span><span class="sxs-lookup"><span data-stu-id="a04a1-113">**If you manufacture any of the items:** Number of threads = Number of planned orders ÷ 1,000</span></span>
- <span data-ttu-id="a04a1-114">**如果不制造任何物料：** 线程数 = 物料数 ÷ 1,000</span><span class="sxs-lookup"><span data-stu-id="a04a1-114">**If you don't manufacture any of the items:** Number of threads = Number of items ÷ 1,000</span></span>

<span data-ttu-id="a04a1-115">如果计算出的线程数超过可用线程数的 75%，则其超过每位客户的可用线程数的 75%。</span><span class="sxs-lookup"><span data-stu-id="a04a1-115">If the number of threads that is calculated exceeds 75 percent of the available number of threads, it's capped at 75 percent of the number of threads that is available for each customer.</span></span> <span data-ttu-id="a04a1-116">（将为每个客户确定可用线程数。）</span><span class="sxs-lookup"><span data-stu-id="a04a1-116">(The number of available threads will be determined for each customer.)</span></span>

<span data-ttu-id="a04a1-117">有关详细信息，请参阅[线程数](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads)。</span><span class="sxs-lookup"><span data-stu-id="a04a1-117">For more information, see [Number of threads](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).</span></span>

### <a name="bundle-size"></a><span data-ttu-id="a04a1-118">捆绑大小</span><span class="sxs-lookup"><span data-stu-id="a04a1-118">Bundle size</span></span>

<span data-ttu-id="a04a1-119">捆绑大小将设置为 **1**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-119">The bundle size will be set to **1**.</span></span> <span data-ttu-id="a04a1-120">此值通常为最佳值，因为有助于提高主计划的性能。</span><span class="sxs-lookup"><span data-stu-id="a04a1-120">This value is often the best value, because it helps improve the performance of master planning.</span></span>

<span data-ttu-id="a04a1-121">有关详细信息，请参阅[帮助程序任务捆绑中的任务数](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle)。</span><span class="sxs-lookup"><span data-stu-id="a04a1-121">For more information, see [Number of tasks in helper task bundle](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).</span></span>

### <a name="firming-bundle-size"></a><span data-ttu-id="a04a1-122">确认捆绑大小</span><span class="sxs-lookup"><span data-stu-id="a04a1-122">Firming bundle size</span></span>

- <span data-ttu-id="a04a1-123">**如果制造任何物料：** 确认捆绑大小将设置为以下两个值中的较大值：**10** 和捆绑计算结果</span><span class="sxs-lookup"><span data-stu-id="a04a1-123">**If you manufacture any of the items:** The firming bundle size will be set to the larger of these two values: **10** and the bundle calculation</span></span>
- <span data-ttu-id="a04a1-124">**如果不制造任何物料：** 确认捆绑大小将设置为以下两个值中的较大值：**50** 和捆绑计算结果</span><span class="sxs-lookup"><span data-stu-id="a04a1-124">**If you don't manufacture any of the items:** The firming bundle size will be set to the larger of these two values: **50** and the bundle calculation</span></span>

<span data-ttu-id="a04a1-125">捆绑计算结果 =（计划订单数 ×（确认时限 ÷ 覆盖时限）÷ 线程数）÷ 10</span><span class="sxs-lookup"><span data-stu-id="a04a1-125">Bundle calculation = (Number of planned orders × (Firming time fence ÷ Coverage time fence) ÷ Number of threads) ÷ 10</span></span>

### <a name="cache-size"></a><span data-ttu-id="a04a1-126">缓存大小</span><span class="sxs-lookup"><span data-stu-id="a04a1-126">Cache size</span></span>

<span data-ttu-id="a04a1-127">缓存大小将设置为**最大值**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-127">The cache size will be set to **Maximum**.</span></span> <span data-ttu-id="a04a1-128">此值通常为最佳值，因为有助于提高主计划的性能。</span><span class="sxs-lookup"><span data-stu-id="a04a1-128">This value is often the best value, because it helps improve the performance of master planning.</span></span>

<span data-ttu-id="a04a1-129">有关详细信息，请参阅[为作业捆绑中的作业分配时间](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle)。</span><span class="sxs-lookup"><span data-stu-id="a04a1-129">For more information, see [Allocate time to jobs in a job bundle](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).</span></span>

### <a name="manufacturing-setup"></a><span data-ttu-id="a04a1-130">制造设置</span><span class="sxs-lookup"><span data-stu-id="a04a1-130">Manufacturing setup</span></span>

<span data-ttu-id="a04a1-131">如果制造物料，则向导后面将显示**制造设置**页。</span><span class="sxs-lookup"><span data-stu-id="a04a1-131">If you manufacture items, a **Manufacturing setup** page will appear later in the wizard.</span></span>

## <a name="scope-of-the-current-plan"></a><span data-ttu-id="a04a1-132">当前计划的范围</span><span class="sxs-lookup"><span data-stu-id="a04a1-132">Scope of the current plan</span></span>

<span data-ttu-id="a04a1-133">在向导的**当前计划的范围**页，您将回答与主计划中要考虑和计算的各种要求的将来时间范围有关的问题。</span><span class="sxs-lookup"><span data-stu-id="a04a1-133">On the **Scope of the current plan** page of the wizard, you answer questions that are related to how far in the future various requirements will be considered and calculated in master planning.</span></span> <span data-ttu-id="a04a1-134">每个问题询问您是否要使用某项功能，以及如何配置该功能。</span><span class="sxs-lookup"><span data-stu-id="a04a1-134">Each question asks whether you want to use a feature and how you want to configure it.</span></span>

<span data-ttu-id="a04a1-135">例如，对于预测计划功能，向导将询问“是否要在主计划中使用预测计划以便建议计划订单来满足预测的需求?”</span><span class="sxs-lookup"><span data-stu-id="a04a1-135">For example, for the forecast plan feature, the wizard asks, "Do you want to use a forecast plan in master planning so that planned orders will be suggested to fulfill the forecasted demand?"</span></span>

<span data-ttu-id="a04a1-136">选项如下：</span><span class="sxs-lookup"><span data-stu-id="a04a1-136">The following options are available:</span></span>

- <span data-ttu-id="a04a1-137">**否** – 主计划不推荐计划订单来实施预测。</span><span class="sxs-lookup"><span data-stu-id="a04a1-137">**No** – Master planning won't suggest planned orders to fulfill a forecast.</span></span> <span data-ttu-id="a04a1-138">在**主计划**的**时限**选项卡（**主计划 \> 设置 \> 计划 \> 主计划**）选项卡上，向导将把**预测计划(时限)** 选项设置为**是**，将天数设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="a04a1-138">On the **Time fences** tab of the **Master plans** page (**Master planning \> Setup \> Plans \> Master plans**), the wizard will set the **Forecast plan (time fence)** option to **Yes** and set the number of days to **0** (zero).</span></span> <span data-ttu-id="a04a1-139">此设置将覆盖在覆盖范围组中指定的时限。</span><span class="sxs-lookup"><span data-stu-id="a04a1-139">This setup will override the time fence that is specified in the coverage group.</span></span> <span data-ttu-id="a04a1-140">因为天数设置为 **0**（零），则不使用此功能。</span><span class="sxs-lookup"><span data-stu-id="a04a1-140">Because the number of days is set to **0** (zero), the feature won't be used.</span></span>
- <span data-ttu-id="a04a1-141">**是，按照此主计划中的定义** – 字段变得可用，可在其中输入主计划将为计划订单推荐来满足预测的需求的天数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-141">**Yes, as defined in this master plan** – A field becomes available, where you can enter the number of days that master planning will suggest planned orders to fulfill the forecasted demand.</span></span> <span data-ttu-id="a04a1-142">向导将把**预测计划(时限)** 选项设置为**是**，将天数设置为在**主计划**页的**时限**选项卡上**预测计划**字段中输入的天数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-142">The wizard will set the **Forecast plan (time fence)** option to **Yes** and set the number of days to the number of days that is entered in the **Forecast plan** field on the **Time fences** tab of the **Master plans** page.</span></span> <span data-ttu-id="a04a1-143">此设置将覆盖在覆盖范围组中设置的值。</span><span class="sxs-lookup"><span data-stu-id="a04a1-143">This setup will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="a04a1-144">**是，按照覆盖范围中的定义** – 向导将**预测计划(时限)** 选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-144">**Yes, as defined in the coverage** – The wizard will set the **Forecast plan (time fence)** option to **No**.</span></span> <span data-ttu-id="a04a1-145">将使用在覆盖范围组中指定的时限指定为预测计划的时间长短。</span><span class="sxs-lookup"><span data-stu-id="a04a1-145">The time fences that are specified in the coverage group will be used to specify how long you will plan for the forecast.</span></span>

<span data-ttu-id="a04a1-146">此页中的其余问题及其回答采用同一个架构：</span><span class="sxs-lookup"><span data-stu-id="a04a1-146">The remaining questions on this page and their answers follow the same schema:</span></span>

- <span data-ttu-id="a04a1-147">**否** – **预测计划(时限)** 选项将设置为**是**，天数将设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="a04a1-147">**No** – The **Forecast plan (time fence)** option will be set to **Yes**, and the number of days will be set to **0** (zero).</span></span>
- <span data-ttu-id="a04a1-148">**是，按照此主计划中的定义** – **预测计划(时限)** 选项将设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-148">**Yes, as defined in this master plan** – The **Forecast plan (time fence)** option will be set to **Yes**.</span></span> <span data-ttu-id="a04a1-149">将使用您输入的天数，并且该天数将覆盖在覆盖范围组中设置的值。</span><span class="sxs-lookup"><span data-stu-id="a04a1-149">The number of days that you enter will be used and will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="a04a1-150">**是，按照覆盖范围组中的定义** – **预测计划(时限)** 选项将设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-150">**Yes, as defined in the coverage group** – The **Forecast plan (time fence)** option will be set to **No**.</span></span>

<span data-ttu-id="a04a1-151">有关详细信息，请参阅[作业级排产](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。</span><span class="sxs-lookup"><span data-stu-id="a04a1-151">For more information, see [Job scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).</span></span>

## <a name="scheduling-options"></a><span data-ttu-id="a04a1-152">计划编制选项</span><span class="sxs-lookup"><span data-stu-id="a04a1-152">Scheduling options</span></span>

<span data-ttu-id="a04a1-153">仅当对向导第一页上的“是否制造任何计划的物料?”问题回答了**是**，**计划编制选项**页</span><span class="sxs-lookup"><span data-stu-id="a04a1-153">The **Scheduling options** page appears only if you answered **Yes** to the "Do you manufacture any of the items planned?"</span></span> <span data-ttu-id="a04a1-154">才会显示。</span><span class="sxs-lookup"><span data-stu-id="a04a1-154">question on the first page of the wizard.</span></span>

<span data-ttu-id="a04a1-155">您对此页上的第一个问题（“是否需要计划拆分为单个作业的工序?”）的回答决定**主计划**页的**常规**选项卡上的计划编制方法。</span><span class="sxs-lookup"><span data-stu-id="a04a1-155">Your answer to the first question on this page ("Do you need to schedule operations divided into individual jobs?") determines the scheduling method on the **General** tab of the **Master plans** page.</span></span>

- <span data-ttu-id="a04a1-156">**是** – 将使用作业级排产。</span><span class="sxs-lookup"><span data-stu-id="a04a1-156">**Yes** – Job scheduling will be used.</span></span>
- <span data-ttu-id="a04a1-157">**否** – 将使用工序级排产。</span><span class="sxs-lookup"><span data-stu-id="a04a1-157">**No** – Operations scheduling will be used.</span></span>

<span data-ttu-id="a04a1-158">有关详细信息，请参阅[工序级排产](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling)和[作业级排产](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。</span><span class="sxs-lookup"><span data-stu-id="a04a1-158">For more information, see [Operations scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) and [Job scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).</span></span>

## <a name="updates-of-demand-and-supply"></a><span data-ttu-id="a04a1-159">需求和供应的更新</span><span class="sxs-lookup"><span data-stu-id="a04a1-159">Updates of demand and supply</span></span>

<span data-ttu-id="a04a1-160">**需求和供应的更新**页中的问题与确认、行动消息和延迟有关。</span><span class="sxs-lookup"><span data-stu-id="a04a1-160">The questions on the **Updates of demand and supply** page are related to firming, action messages, and delays.</span></span>

<span data-ttu-id="a04a1-161">将根据您的回答和上一个部分中介绍的同一个架构更新主计划设置。</span><span class="sxs-lookup"><span data-stu-id="a04a1-161">The master planning setup will be updated based on your answers, according to the same schema that is described in the previous section:</span></span>

- <span data-ttu-id="a04a1-162">**否** – **主计划**页中的**时限**选项将设置为**是**，天数将设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="a04a1-162">**No** – The **Time fence** option on the **Master plans** page will be set to **Yes**, and the number of days will be set to **0** (zero).</span></span>
- <span data-ttu-id="a04a1-163">**是，按照此主计划中的定义** – **时限**选项将设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-163">**Yes, as defined in this master plan** – The **Time fence** option will be set to **Yes**.</span></span> <span data-ttu-id="a04a1-164">将使用您输入的天数，并且该天数将覆盖在覆盖范围组中设置的值。</span><span class="sxs-lookup"><span data-stu-id="a04a1-164">The number of days that you enter will be used and will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="a04a1-165">**是，按照覆盖范围组中的定义** – **预时限**选项将设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-165">**Yes, as defined in the coverage group** – the **Time fence** option will be set to **No**.</span></span>

<span data-ttu-id="a04a1-166">对于计算的延迟，您对向导中的问题的回答将更新**主计划**页**计算的延迟**选项卡上的相应参数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-166">For calculated delays, your answers to the questions in the wizard will update the corresponding parameters on the **Calculated delays** tab of the **Master plans** page.</span></span>

## <a name="summary-of-your-changes"></a><span data-ttu-id="a04a1-167">您的更改汇总</span><span class="sxs-lookup"><span data-stu-id="a04a1-167">Summary of your changes</span></span>

<span data-ttu-id="a04a1-168">向导的最后一页显示根据您的响应推荐的更改。</span><span class="sxs-lookup"><span data-stu-id="a04a1-168">The last page of the wizard shows the changes that that are recommended based on your responses.</span></span> <span data-ttu-id="a04a1-169">同时显示您的设置（**当前设置**）中的值和向导推荐的值（**新配置**）。</span><span class="sxs-lookup"><span data-stu-id="a04a1-169">It shows both the value in your setup (**Current setup**) and the value that the wizard recommends (**New configuration**).</span></span>

<span data-ttu-id="a04a1-170">也可以修改新配置中的参数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-170">You can also modify the parameters in the new configuration.</span></span> <span data-ttu-id="a04a1-171">参数将拆分为应用于法人的参数和仅应用于所选主计划的参数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-171">The parameters are separated into parameters that apply to your legal entity and parameters that apply only to the master plan that you selected.</span></span> <span data-ttu-id="a04a1-172">若要查看可通过使用此向导更改的所有设置参数，请选择页面底部的**显示所有参数**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-172">To view all the setup parameters that can be changed by using the wizard, select **Show all parameters** at the bottom of the page.</span></span> <span data-ttu-id="a04a1-173">然后可以更改参数。</span><span class="sxs-lookup"><span data-stu-id="a04a1-173">You can then change the parameters.</span></span>

<span data-ttu-id="a04a1-174">最后，在选择**完成**时，将应用新配置。</span><span class="sxs-lookup"><span data-stu-id="a04a1-174">Finally, when you select **Finish**, the new configuration is applied.</span></span> <span data-ttu-id="a04a1-175">如果选择**取消**，则不应用任何更改。</span><span class="sxs-lookup"><span data-stu-id="a04a1-175">If you select **Cancel**, none of the changes are applied.</span></span>

## <a name="examples"></a><span data-ttu-id="a04a1-176">示例</span><span class="sxs-lookup"><span data-stu-id="a04a1-176">Examples</span></span>

<span data-ttu-id="a04a1-177">此部分介绍两家虚构公司的设置，以便显示该设置如何根据各企业的需求而变化。</span><span class="sxs-lookup"><span data-stu-id="a04a1-177">This section describes the setup of two fictional companies to show how the setup can change according to the needs of each business.</span></span>

### <a name="example-1-contoso-manufacturer"></a><span data-ttu-id="a04a1-178">示例 1：Contoso Manufacturer</span><span class="sxs-lookup"><span data-stu-id="a04a1-178">Example 1: Contoso Manufacturer</span></span>

<span data-ttu-id="a04a1-179">Contoso Manufacturer 是一家生产扬声器的制造公司。</span><span class="sxs-lookup"><span data-stu-id="a04a1-179">Contoso Manufacturer is a manufacturing company that produces speakers.</span></span> <span data-ttu-id="a04a1-180">该公司从大量供应商处购买大量用于扬声器成品的原材料和组件。</span><span class="sxs-lookup"><span data-stu-id="a04a1-180">It purchases the various raw materials and components that are used for the final speakers from various suppliers.</span></span> <span data-ttu-id="a04a1-181">下面是它的部分供应和制造特征：</span><span class="sxs-lookup"><span data-stu-id="a04a1-181">Here are some of the characteristics of its supply and manufacturing:</span></span>

- <span data-ttu-id="a04a1-182">公司制造的最终物料采用物料清单 (BOM) 结构。</span><span class="sxs-lookup"><span data-stu-id="a04a1-182">The final items that the company manufactures have a bill of materials (BOM) structure.</span></span>
- <span data-ttu-id="a04a1-183">所有最终物料和组件通过主计划计划。</span><span class="sxs-lookup"><span data-stu-id="a04a1-183">All final items and components are planned by master planning.</span></span> <span data-ttu-id="a04a1-184">不执行手动计划。</span><span class="sxs-lookup"><span data-stu-id="a04a1-184">Manual planning isn't done.</span></span>
- <span data-ttu-id="a04a1-185">将为每个最终物料的生产定义工序的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="a04a1-185">A route of operations is defined for the production of each final item.</span></span>
- <span data-ttu-id="a04a1-186">制造工厂生产最终物料。</span><span class="sxs-lookup"><span data-stu-id="a04a1-186">The manufacturing plant produces the final items.</span></span> <span data-ttu-id="a04a1-187">它定义了一些铣削和钻削机器，用于处理组件。</span><span class="sxs-lookup"><span data-stu-id="a04a1-187">It has a defined number of milling and drilling machines that are used to process the components.</span></span> <span data-ttu-id="a04a1-188">各种组件必须由这些机器处理。</span><span class="sxs-lookup"><span data-stu-id="a04a1-188">The various components must be processed by these machines.</span></span>
- <span data-ttu-id="a04a1-189">有多家供应商。</span><span class="sxs-lookup"><span data-stu-id="a04a1-189">There are many suppliers.</span></span> <span data-ttu-id="a04a1-190">物料的平均提前期为一周。</span><span class="sxs-lookup"><span data-stu-id="a04a1-190">The average lead time for items is one week.</span></span> <span data-ttu-id="a04a1-191">同一家供应商的一组物料的提前期为七周。</span><span class="sxs-lookup"><span data-stu-id="a04a1-191">A group of items from the same supplier will have a lead time of seven weeks.</span></span>

<span data-ttu-id="a04a1-192">在向导中，将为 Contoso Manufacturer 输入以下值：</span><span class="sxs-lookup"><span data-stu-id="a04a1-192">In the wizard, the following values are entered for Contoso Manufacturer:</span></span>

- <span data-ttu-id="a04a1-193">**覆盖范围：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-193">**Coverage:**</span></span>

    - <span data-ttu-id="a04a1-194">**问题**：“是否要指定计划区间的天数？”</span><span class="sxs-lookup"><span data-stu-id="a04a1-194">**Question:** "Do you want to specify the number of days of your planning horizon?"</span></span>
    - <span data-ttu-id="a04a1-195">**回答**：“是，按照覆盖范围组中的定义。”</span><span class="sxs-lookup"><span data-stu-id="a04a1-195">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="a04a1-196">因为物料的提前期相差很大，所以 Contoso 不必将所有物料安排在将来的同一个期间。</span><span class="sxs-lookup"><span data-stu-id="a04a1-196">Because the lead time for items is very different, Contoso doesn't have to plan all the items for the same period in the future.</span></span> <span data-ttu-id="a04a1-197">将为物料创建覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="a04a1-197">Coverage groups for the items are created.</span></span> <span data-ttu-id="a04a1-198">将把提前期相似的物料分派给同一个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="a04a1-198">Items that have a similar lead time are assigned to the same coverage group.</span></span> <span data-ttu-id="a04a1-199">每个覆盖范围组的计划区间（即覆盖时限）大致为提前期加一周的差额。</span><span class="sxs-lookup"><span data-stu-id="a04a1-199">The planning horizon for each coverage group (that is, the coverage time fence) is approximately the lead time plus a margin of one week.</span></span> <span data-ttu-id="a04a1-200">然后，主计划确保根据其提前期提前计划物料。</span><span class="sxs-lookup"><span data-stu-id="a04a1-200">Master planning then makes sure that the items are planned in advance, based on their lead time.</span></span>

    <span data-ttu-id="a04a1-201">因此，将为此示例创建两个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="a04a1-201">Therefore, two coverage groups will be created for this example.</span></span> <span data-ttu-id="a04a1-202">一个覆盖范围组的覆盖时限为两周，另一个的覆盖时限为八周。</span><span class="sxs-lookup"><span data-stu-id="a04a1-202">One coverage group will have a coverage time fence of two weeks, and the other will have a coverage time fence of eight weeks.</span></span>

    <span data-ttu-id="a04a1-203">如果回答选择**是，按照此主计划中的定义**，则输入的天数应该超过所有物料中的最大提前期。</span><span class="sxs-lookup"><span data-stu-id="a04a1-203">If **Yes, as defined in this master plan** is selected as the answer, the number of days that is entered should exceed the longest lead time of all the items.</span></span> <span data-ttu-id="a04a1-204">但是，因为不必将大量物料提前这么久，所以将计算大量计划订单，但是从不使用这些订单。</span><span class="sxs-lookup"><span data-stu-id="a04a1-204">However, because many items don't have to be planned so far in advance, many planned orders will be calculated but never used.</span></span> <span data-ttu-id="a04a1-205">因此，主计划运行时间将增加。</span><span class="sxs-lookup"><span data-stu-id="a04a1-205">Therefore, the master planning runtime will increase.</span></span>

- <span data-ttu-id="a04a1-206">**计划编制：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-206">**Scheduling:**</span></span>

    - <span data-ttu-id="a04a1-207">**问题**：“是否需要计划拆分为单个作业的工序?”</span><span class="sxs-lookup"><span data-stu-id="a04a1-207">**Question:** "Do you need to schedule operations divided into individual jobs?"</span></span>
    - <span data-ttu-id="a04a1-208">**回答**：“是。”</span><span class="sxs-lookup"><span data-stu-id="a04a1-208">**Answer:** "Yes."</span></span>

    <span data-ttu-id="a04a1-209">Contoso Manufacturing 必须计划和安排将对车间执行的单个作业。</span><span class="sxs-lookup"><span data-stu-id="a04a1-209">Contoso Manufacturing must plan and schedule the individual jobs that will be performed on the shop floor.</span></span> <span data-ttu-id="a04a1-210">因此，将使用作业级排产。</span><span class="sxs-lookup"><span data-stu-id="a04a1-210">Therefore, it will use job scheduling.</span></span>

- <span data-ttu-id="a04a1-211">**产能：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-211">**Capacity:**</span></span>

    - <span data-ttu-id="a04a1-212">**问题**：“是否要使用资源的产能进行排产？”</span><span class="sxs-lookup"><span data-stu-id="a04a1-212">**Question:** "Do you want to schedule using the capacity of resources?"</span></span>
    - <span data-ttu-id="a04a1-213">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="a04a1-213">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="a04a1-214">输入了 **10 天**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-214">**10 days** is entered.</span></span>

    <span data-ttu-id="a04a1-215">将限制铣削和钻削机器的数量。</span><span class="sxs-lookup"><span data-stu-id="a04a1-215">The number of milling and drilling machines is limited.</span></span> <span data-ttu-id="a04a1-216">生产计划必须考虑此限制，并根据资源产能及时安排作业。</span><span class="sxs-lookup"><span data-stu-id="a04a1-216">Production planning must take this limitation into account and arrange the jobs in time according to the capacity of the resources.</span></span> <span data-ttu-id="a04a1-217">换句话说，将根据资源的限制重新计划排产的作业。</span><span class="sxs-lookup"><span data-stu-id="a04a1-217">In other words, the jobs that are scheduled will be replanned based on the limitations of the resources.</span></span> <span data-ttu-id="a04a1-218">除了定义的期间，计划还将使用提前期。</span><span class="sxs-lookup"><span data-stu-id="a04a1-218">Planning will use the lead time in addition to the period that is defined.</span></span> <span data-ttu-id="a04a1-219">（计划的生产订单可重叠。）因为物料的生产提前期为七天，所以将考虑主计划在 10 天内的资源产能。</span><span class="sxs-lookup"><span data-stu-id="a04a1-219">(Planned production orders can overlap.) Because the production lead time for the items is seven days, the capacity of the resources for master planning will be considered during 10 days.</span></span>

- <span data-ttu-id="a04a1-220">**先后顺序：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-220">**Sequencing:**</span></span>

    - <span data-ttu-id="a04a1-221">**问题**：“是否要使用产品的顺序值为计划的订单排序？”</span><span class="sxs-lookup"><span data-stu-id="a04a1-221">**Question:** "Do you want to sequence planned orders using the product's sequence values?"</span></span>
    - <span data-ttu-id="a04a1-222">**回答**：“是，按照覆盖范围组中的定义。”</span><span class="sxs-lookup"><span data-stu-id="a04a1-222">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="a04a1-223">将为每个最终物料的生产定义工艺路线。</span><span class="sxs-lookup"><span data-stu-id="a04a1-223">A route is defined for the production of each final item.</span></span> <span data-ttu-id="a04a1-224">因此，主计划将根据定义的工艺路线及时安排订单。</span><span class="sxs-lookup"><span data-stu-id="a04a1-224">Therefore, master planning will schedule the orders in time according to the defined routes.</span></span>

- <span data-ttu-id="a04a1-225">**分解：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-225">**Explosion:**</span></span>

    - <span data-ttu-id="a04a1-226">**问题**：“是否要计划物料清单中所有元素的订单(针对父级和所有子级物料进行计划)?”</span><span class="sxs-lookup"><span data-stu-id="a04a1-226">**Question:** "Do you want to plan orders for all the elements in a Bill of Materials (plan for the parent and all children items)?"</span></span>
    - <span data-ttu-id="a04a1-227">**回答**：“是，按照覆盖范围组中的定义。”</span><span class="sxs-lookup"><span data-stu-id="a04a1-227">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="a04a1-228">必须计划用于生产的所有物料。</span><span class="sxs-lookup"><span data-stu-id="a04a1-228">All the items that are used for the production must be planned.</span></span> <span data-ttu-id="a04a1-229">因为物料的提前期相差极大，所以主计划在使用覆盖范围组时的性能更佳。</span><span class="sxs-lookup"><span data-stu-id="a04a1-229">Because the items have very different lead times, master planning will have better performance when it uses the coverage groups.</span></span> <span data-ttu-id="a04a1-230">而且，可以输入一周的差额，并且可以对与覆盖范围相同的时间进行分解。</span><span class="sxs-lookup"><span data-stu-id="a04a1-230">Again, a margin of one week can be entered, and explosion can be done for the same time as the coverage.</span></span>

### <a name="example-2-contoso-retailer"></a><span data-ttu-id="a04a1-231">示例 2：Contoso Retailer</span><span class="sxs-lookup"><span data-stu-id="a04a1-231">Example 2: Contoso Retailer</span></span>

<span data-ttu-id="a04a1-232">Contoso Retailer 是时尚行业的一家分销公司。</span><span class="sxs-lookup"><span data-stu-id="a04a1-232">Contoso Retailer is a distribution company in the fashion industry.</span></span> <span data-ttu-id="a04a1-233">该公司使用主计划，基于预测销量计算应在何时下达采购订单。</span><span class="sxs-lookup"><span data-stu-id="a04a1-233">It uses master planning to calculate when purchase orders should be placed, based on its forecasted sales.</span></span> <span data-ttu-id="a04a1-234">下面是该公司的部分特征：</span><span class="sxs-lookup"><span data-stu-id="a04a1-234">Here are some of its characteristics:</span></span>

- <span data-ttu-id="a04a1-235">Contoso Retailer 使用需求预测预测销量。</span><span class="sxs-lookup"><span data-stu-id="a04a1-235">Contoso Retailer uses a demand forecast to predict sales.</span></span> <span data-ttu-id="a04a1-236">将根据此预测计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="a04a1-236">Purchase orders will be planned according to the forecast.</span></span>
- <span data-ttu-id="a04a1-237">商店使用补货申请。</span><span class="sxs-lookup"><span data-stu-id="a04a1-237">Stores use requisitions for replenishment.</span></span>
- <span data-ttu-id="a04a1-238">从主仓库到每家商店的提前期为所有物料大约两周。</span><span class="sxs-lookup"><span data-stu-id="a04a1-238">The lead time from the main warehouse to each store is approximately two weeks for all items.</span></span>

<span data-ttu-id="a04a1-239">在向导中，将为 Contoso Retailer 输入以下值：</span><span class="sxs-lookup"><span data-stu-id="a04a1-239">In the wizard, the following values are entered for Contoso Retailer:</span></span>

- <span data-ttu-id="a04a1-240">**预测需求：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-240">**Forecast demand:**</span></span>

    - <span data-ttu-id="a04a1-241">**问题**：“是否要在主计划中使用预测计划以便建议计划订单来满足预测的需求?”</span><span class="sxs-lookup"><span data-stu-id="a04a1-241">**Question:** "Do you want to use a forecast plan in master planning so that planned orders will be suggested to fulfill the forecasted demand?"</span></span>
    - <span data-ttu-id="a04a1-242">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="a04a1-242">**Answer:** "Yes, as defined in this master plan."</span></span>

    <span data-ttu-id="a04a1-243">Contoso 中有一个需求预测，用于预测其销量。</span><span class="sxs-lookup"><span data-stu-id="a04a1-243">Contoso has included a demand forecast to predict its sales.</span></span> <span data-ttu-id="a04a1-244">因此，主计划必须推荐计划订单以实现预测。</span><span class="sxs-lookup"><span data-stu-id="a04a1-244">Therefore, master planning must recommend planned orders to fulfill the forecast.</span></span>

- <span data-ttu-id="a04a1-245">**确认：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-245">**Firming:**</span></span>

    - <span data-ttu-id="a04a1-246">**问题**：“是否希望主计划自动将计划订单确认到订单单据(例如生产或采购订单)?”</span><span class="sxs-lookup"><span data-stu-id="a04a1-246">**Question:** "Do you want master planning to automatically firm planned orders into order documents, for example production or purchase orders?"</span></span>
    - <span data-ttu-id="a04a1-247">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="a04a1-247">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="a04a1-248">输入了 **1 天**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-248">**1 day** is entered.</span></span>

    <span data-ttu-id="a04a1-249">因为 Contoso Retailer 将直接从计划采购订单创建采购订单，所以如果自动确认计划采购订单，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="a04a1-249">Because Contoso Retailer will create purchase orders directly from the planned purchase orders, it's useful if the planned purchase orders are automatically firmed.</span></span> <span data-ttu-id="a04a1-250">因为公司每天运行主计划，所以一天的确认时限将自动确认下一天需要的所有订单。</span><span class="sxs-lookup"><span data-stu-id="a04a1-250">Because the company runs master planning every day, a firming time fence of one day will automatically firm all the orders that are required for the next day.</span></span>

- <span data-ttu-id="a04a1-251">**已审核的申请：**</span><span class="sxs-lookup"><span data-stu-id="a04a1-251">**Approved requisitions:**</span></span>

    - <span data-ttu-id="a04a1-252">**问题**：“是否要包含已审核的零售商店补货申请中的需求？”</span><span class="sxs-lookup"><span data-stu-id="a04a1-252">**Question:** "Do you want to include demand from approved requisitions to replenish retail stores?"</span></span>
    - <span data-ttu-id="a04a1-253">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="a04a1-253">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="a04a1-254">输入了 **1 天**。</span><span class="sxs-lookup"><span data-stu-id="a04a1-254">**1 day** is entered.</span></span>

    <span data-ttu-id="a04a1-255">Contoso 使用其商店的已审核申请创建计划采购订单来为这些商店补货。</span><span class="sxs-lookup"><span data-stu-id="a04a1-255">Contoso uses the approved requisitions from its stores to create planned purchase orders to replenish those stores.</span></span> <span data-ttu-id="a04a1-256">因为每天运行主计划，所以计划中将包含前一天的申请。</span><span class="sxs-lookup"><span data-stu-id="a04a1-256">Because master planning is run every day, the requisitions from the last day will be included in the planning.</span></span>
