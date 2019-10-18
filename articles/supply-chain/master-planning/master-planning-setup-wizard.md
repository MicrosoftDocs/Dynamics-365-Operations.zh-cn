---
title: 主计划设置向导
description: 此主题介绍用于设置主计划的各种重要策略和参数。
author: t-benebo
manager: AnnBe
ms.date: 08/05/2019
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
ms.openlocfilehash: 0310ac55d35421d8ad9080739fc5a393660ce520
ms.sourcegitcommit: 261dc882710f29303b14f9be8a26d71d85d25345
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2019
ms.locfileid: "1999526"
---
# <a name="master-planning-setup-wizard"></a><span data-ttu-id="81be2-103">主计划设置向导</span><span class="sxs-lookup"><span data-stu-id="81be2-103">Master planning setup wizard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81be2-104">本主题提供针对**主计划设置向导**的指南。</span><span class="sxs-lookup"><span data-stu-id="81be2-104">This topic provides a guide for the **Master planning setup wizard**.</span></span> <span data-ttu-id="81be2-105">介绍如何计算参数建议，还提供示例来显示不同公司如何根据业务需要设置主计划。</span><span class="sxs-lookup"><span data-stu-id="81be2-105">It explains how parameter suggestions are calculated and also provides examples that show how different companies set up master planning, based on their business needs.</span></span>

## <a name="specific-requirements-of-your-company"></a><span data-ttu-id="81be2-106">您的公司的具体要求</span><span class="sxs-lookup"><span data-stu-id="81be2-106">Specific requirements of your company</span></span>

<span data-ttu-id="81be2-107">向导的第一页询问公司的具体要求。</span><span class="sxs-lookup"><span data-stu-id="81be2-107">The first page of the wizard asks about the specific requirements of your company.</span></span> <span data-ttu-id="81be2-108">您对这些问题的回答不必精确，但是您应该可以提供法人的大致物料和计划订单数量。</span><span class="sxs-lookup"><span data-stu-id="81be2-108">Your answers to these questions don't have to be exact, but you should be able to provide a rough approximation of the number of items and planned orders that there will be for the legal entity.</span></span> <span data-ttu-id="81be2-109">您的回答用于配置为法人应用的参数，而不仅是应用于所选主计划的参数。</span><span class="sxs-lookup"><span data-stu-id="81be2-109">Your answers are used to configure parameters that apply to your legal entity, not just to the master plan that you selected.</span></span> <span data-ttu-id="81be2-110">以下部分介绍计算的参数和使用的公式。</span><span class="sxs-lookup"><span data-stu-id="81be2-110">The following sections describe the parameters that are calculated and the formulas that are used.</span></span>

### <a name="number-of-threads"></a><span data-ttu-id="81be2-111">线程数</span><span class="sxs-lookup"><span data-stu-id="81be2-111">Number of threads</span></span>

- <span data-ttu-id="81be2-112">**如果制造任何物料：** 线程数 = 计划订单数 ÷ 1,000</span><span class="sxs-lookup"><span data-stu-id="81be2-112">**If you manufacture any of the items:** Number of threads = Number of planned orders ÷ 1,000</span></span>
- <span data-ttu-id="81be2-113">**如果不制造任何物料：** 线程数 = 物料数 ÷ 1,000</span><span class="sxs-lookup"><span data-stu-id="81be2-113">**If you don't manufacture any of the items:** Number of threads = Number of items ÷ 1,000</span></span>

<span data-ttu-id="81be2-114">如果计算出的线程数超过可用线程数的 75%，则其超过每位客户的可用线程数的 75%。</span><span class="sxs-lookup"><span data-stu-id="81be2-114">If the number of threads that is calculated exceeds 75 percent of the available number of threads, it's capped at 75 percent of the number of threads that is available for each customer.</span></span> <span data-ttu-id="81be2-115">（将为每个客户确定可用线程数。）</span><span class="sxs-lookup"><span data-stu-id="81be2-115">(The number of available threads will be determined for each customer.)</span></span>

<span data-ttu-id="81be2-116">有关详细信息，请参阅[线程数](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads)。</span><span class="sxs-lookup"><span data-stu-id="81be2-116">For more information, see [Number of threads](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).</span></span>

### <a name="bundle-size"></a><span data-ttu-id="81be2-117">捆绑大小</span><span class="sxs-lookup"><span data-stu-id="81be2-117">Bundle size</span></span>

<span data-ttu-id="81be2-118">捆绑大小将设置为 **1**。</span><span class="sxs-lookup"><span data-stu-id="81be2-118">The bundle size will be set to **1**.</span></span> <span data-ttu-id="81be2-119">此值通常为最佳值，因为有助于提高主计划的性能。</span><span class="sxs-lookup"><span data-stu-id="81be2-119">This value is often the best value, because it helps improve the performance of master planning.</span></span>

<span data-ttu-id="81be2-120">有关详细信息，请参阅[帮助程序任务捆绑中的任务数](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle)。</span><span class="sxs-lookup"><span data-stu-id="81be2-120">For more information, see [Number of tasks in helper task bundle](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).</span></span>

### <a name="firming-bundle-size"></a><span data-ttu-id="81be2-121">确认捆绑大小</span><span class="sxs-lookup"><span data-stu-id="81be2-121">Firming bundle size</span></span>

- <span data-ttu-id="81be2-122">**如果制造任何物料：** 确认捆绑大小将设置为以下两个值中的较大值：**10** 和捆绑计算结果</span><span class="sxs-lookup"><span data-stu-id="81be2-122">**If you manufacture any of the items:** The firming bundle size will be set to the larger of these two values: **10** and the bundle calculation</span></span>
- <span data-ttu-id="81be2-123">**如果不制造任何物料：** 确认捆绑大小将设置为以下两个值中的较大值：**50** 和捆绑计算结果</span><span class="sxs-lookup"><span data-stu-id="81be2-123">**If you don't manufacture any of the items:** The firming bundle size will be set to the larger of these two values: **50** and the bundle calculation</span></span>

<span data-ttu-id="81be2-124">捆绑计算结果 =（计划订单数 ×（确认时限 ÷ 覆盖时限）÷ 线程数）÷ 10</span><span class="sxs-lookup"><span data-stu-id="81be2-124">Bundle calculation = (Number of planned orders × (Firming time fence ÷ Coverage time fence) ÷ Number of threads) ÷ 10</span></span>

### <a name="cache-size"></a><span data-ttu-id="81be2-125">缓存大小</span><span class="sxs-lookup"><span data-stu-id="81be2-125">Cache size</span></span>

<span data-ttu-id="81be2-126">缓存大小将设置为**最大值**。</span><span class="sxs-lookup"><span data-stu-id="81be2-126">The cache size will be set to **Maximum**.</span></span> <span data-ttu-id="81be2-127">此值通常为最佳值，因为有助于提高主计划的性能。</span><span class="sxs-lookup"><span data-stu-id="81be2-127">This value is often the best value, because it helps improve the performance of master planning.</span></span>

<span data-ttu-id="81be2-128">有关详细信息，请参阅[为作业捆绑中的作业分配时间](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle)。</span><span class="sxs-lookup"><span data-stu-id="81be2-128">For more information, see [Allocate time to jobs in a job bundle](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).</span></span>

### <a name="manufacturing-setup"></a><span data-ttu-id="81be2-129">制造设置</span><span class="sxs-lookup"><span data-stu-id="81be2-129">Manufacturing setup</span></span>

<span data-ttu-id="81be2-130">如果制造物料，则向导后面将显示**制造设置**页。</span><span class="sxs-lookup"><span data-stu-id="81be2-130">If you manufacture items, a **Manufacturing setup** page will appear later in the wizard.</span></span>

## <a name="scope-of-the-current-plan"></a><span data-ttu-id="81be2-131">当前计划的范围</span><span class="sxs-lookup"><span data-stu-id="81be2-131">Scope of the current plan</span></span>

<span data-ttu-id="81be2-132">在向导的**当前计划的范围**页，您将回答与主计划中要考虑和计算的各种要求的将来时间范围有关的问题。</span><span class="sxs-lookup"><span data-stu-id="81be2-132">On the **Scope of the current plan** page of the wizard, you answer questions that are related to how far in the future various requirements will be considered and calculated in master planning.</span></span> <span data-ttu-id="81be2-133">每个问题询问您是否要使用某项功能，以及如何配置该功能。</span><span class="sxs-lookup"><span data-stu-id="81be2-133">Each question asks whether you want to use a feature and how you want to configure it.</span></span>

<span data-ttu-id="81be2-134">例如，对于预测计划功能，向导将询问“是否要在主计划中使用预测计划以便建议计划订单来满足预测的需求?”</span><span class="sxs-lookup"><span data-stu-id="81be2-134">For example, for the forecast plan feature, the wizard asks, "Do you want to use a forecast plan in master planning so that planned orders will be suggested to fulfill the forecasted demand?"</span></span>

<span data-ttu-id="81be2-135">选项如下：</span><span class="sxs-lookup"><span data-stu-id="81be2-135">The following options are available:</span></span>

- <span data-ttu-id="81be2-136">**否** – 主计划不推荐计划订单来实施预测。</span><span class="sxs-lookup"><span data-stu-id="81be2-136">**No** – Master planning won't suggest planned orders to fulfill a forecast.</span></span> <span data-ttu-id="81be2-137">在**主计划**的**时限**选项卡（**主计划 \> 设置 \> 计划 \> 主计划**）选项卡上，向导将把**预测计划(时限)** 选项设置为**是**，将天数设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="81be2-137">On the **Time fences** tab of the **Master plans** page (**Master planning \> Setup \> Plans \> Master plans**), the wizard will set the **Forecast plan (time fence)** option to **Yes** and set the number of days to **0** (zero).</span></span> <span data-ttu-id="81be2-138">此设置将覆盖在覆盖范围组中指定的时限。</span><span class="sxs-lookup"><span data-stu-id="81be2-138">This setup will override the time fence that is specified in the coverage group.</span></span> <span data-ttu-id="81be2-139">因为天数设置为 **0**（零），则不使用此功能。</span><span class="sxs-lookup"><span data-stu-id="81be2-139">Because the number of days is set to **0** (zero), the feature won't be used.</span></span>
- <span data-ttu-id="81be2-140">**是，按照此主计划中的定义** – 字段变得可用，可在其中输入主计划将为计划订单推荐来满足预测的需求的天数。</span><span class="sxs-lookup"><span data-stu-id="81be2-140">**Yes, as defined in this master plan** – A field becomes available, where you can enter the number of days that master planning will suggest planned orders to fulfill the forecasted demand.</span></span> <span data-ttu-id="81be2-141">向导将把**预测计划(时限)** 选项设置为**是**，将天数设置为在**主计划**页的**时限**选项卡上**预测计划**字段中输入的天数。</span><span class="sxs-lookup"><span data-stu-id="81be2-141">The wizard will set the **Forecast plan (time fence)** option to **Yes** and set the number of days to the number of days that is entered in the **Forecast plan** field on the **Time fences** tab of the **Master plans** page.</span></span> <span data-ttu-id="81be2-142">此设置将覆盖在覆盖范围组中设置的值。</span><span class="sxs-lookup"><span data-stu-id="81be2-142">This setup will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="81be2-143">**是，按照覆盖范围中的定义** – 向导将**预测计划(时限)** 选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="81be2-143">**Yes, as defined in the coverage** – The wizard will set the **Forecast plan (time fence)** option to **No**.</span></span> <span data-ttu-id="81be2-144">将使用在覆盖范围组中指定的时限指定为预测计划的时间长短。</span><span class="sxs-lookup"><span data-stu-id="81be2-144">The time fences that are specified in the coverage group will be used to specify how long you will plan for the forecast.</span></span>

<span data-ttu-id="81be2-145">此页中的其余问题及其回答采用同一个架构：</span><span class="sxs-lookup"><span data-stu-id="81be2-145">The remaining questions on this page and their answers follow the same schema:</span></span>

- <span data-ttu-id="81be2-146">**否** – **预测计划(时限)** 选项将设置为**是**，天数将设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="81be2-146">**No** – The **Forecast plan (time fence)** option will be set to **Yes**, and the number of days will be set to **0** (zero).</span></span>
- <span data-ttu-id="81be2-147">**是，按照此主计划中的定义** – **预测计划(时限)** 选项将设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="81be2-147">**Yes, as defined in this master plan** – The **Forecast plan (time fence)** option will be set to **Yes**.</span></span> <span data-ttu-id="81be2-148">将使用您输入的天数，并且该天数将覆盖在覆盖范围组中设置的值。</span><span class="sxs-lookup"><span data-stu-id="81be2-148">The number of days that you enter will be used and will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="81be2-149">**是，按照覆盖范围组中的定义** – **预测计划(时限)** 选项将设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="81be2-149">**Yes, as defined in the coverage group** – The **Forecast plan (time fence)** option will be set to **No**.</span></span>

<span data-ttu-id="81be2-150">有关详细信息，请参阅[作业级排产](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。</span><span class="sxs-lookup"><span data-stu-id="81be2-150">For more information, see [Job scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).</span></span>

## <a name="scheduling-options"></a><span data-ttu-id="81be2-151">计划编制选项</span><span class="sxs-lookup"><span data-stu-id="81be2-151">Scheduling options</span></span>

<span data-ttu-id="81be2-152">仅当对向导第一页上的“是否制造任何计划的物料?”问题回答了**是**，**计划编制选项**页</span><span class="sxs-lookup"><span data-stu-id="81be2-152">The **Scheduling options** page appears only if you answered **Yes** to the "Do you manufacture any of the items planned?"</span></span> <span data-ttu-id="81be2-153">才会显示。</span><span class="sxs-lookup"><span data-stu-id="81be2-153">question on the first page of the wizard.</span></span>

<span data-ttu-id="81be2-154">您对此页上的第一个问题（“是否需要计划拆分为单个作业的工序?”）的回答决定**主计划**页的**常规**选项卡上的计划编制方法。</span><span class="sxs-lookup"><span data-stu-id="81be2-154">Your answer to the first question on this page ("Do you need to schedule operations divided into individual jobs?") determines the scheduling method on the **General** tab of the **Master plans** page.</span></span>

- <span data-ttu-id="81be2-155">**是** – 将使用作业级排产。</span><span class="sxs-lookup"><span data-stu-id="81be2-155">**Yes** – Job scheduling will be used.</span></span>
- <span data-ttu-id="81be2-156">**否** – 将使用工序级排产。</span><span class="sxs-lookup"><span data-stu-id="81be2-156">**No** – Operations scheduling will be used.</span></span>

<span data-ttu-id="81be2-157">有关详细信息，请参阅[工序级排产](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling)和[作业级排产](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。</span><span class="sxs-lookup"><span data-stu-id="81be2-157">For more information, see [Operations scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) and [Job scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).</span></span>

## <a name="updates-of-demand-and-supply"></a><span data-ttu-id="81be2-158">需求和供应的更新</span><span class="sxs-lookup"><span data-stu-id="81be2-158">Updates of demand and supply</span></span>

<span data-ttu-id="81be2-159">**需求和供应的更新**页中的问题与确认、行动消息和延迟有关。</span><span class="sxs-lookup"><span data-stu-id="81be2-159">The questions on the **Updates of demand and supply** page are related to firming, action messages, and delays.</span></span>

<span data-ttu-id="81be2-160">将根据您的回答和上一个部分中介绍的同一个架构更新主计划设置。</span><span class="sxs-lookup"><span data-stu-id="81be2-160">The master planning setup will be updated based on your answers, according to the same schema that is described in the previous section:</span></span>

- <span data-ttu-id="81be2-161">**否** – **主计划**页中的**时限**选项将设置为**是**，天数将设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="81be2-161">**No** – The **Time fence** option on the **Master plans** page will be set to **Yes**, and the number of days will be set to **0** (zero).</span></span>
- <span data-ttu-id="81be2-162">**是，按照此主计划中的定义** – **时限**选项将设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="81be2-162">**Yes, as defined in this master plan** – The **Time fence** option will be set to **Yes**.</span></span> <span data-ttu-id="81be2-163">将使用您输入的天数，并且该天数将覆盖在覆盖范围组中设置的值。</span><span class="sxs-lookup"><span data-stu-id="81be2-163">The number of days that you enter will be used and will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="81be2-164">**是，按照覆盖范围组中的定义** – **预时限**选项将设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="81be2-164">**Yes, as defined in the coverage group** – the **Time fence** option will be set to **No**.</span></span>

<span data-ttu-id="81be2-165">对于计算的延迟，您对向导中的问题的回答将更新**主计划**页**计算的延迟**选项卡上的相应参数。</span><span class="sxs-lookup"><span data-stu-id="81be2-165">For calculated delays, your answers to the questions in the wizard will update the corresponding parameters on the **Calculated delays** tab of the **Master plans** page.</span></span>

## <a name="summary-of-your-changes"></a><span data-ttu-id="81be2-166">您的更改汇总</span><span class="sxs-lookup"><span data-stu-id="81be2-166">Summary of your changes</span></span>

<span data-ttu-id="81be2-167">向导的最后一页显示根据您的响应推荐的更改。</span><span class="sxs-lookup"><span data-stu-id="81be2-167">The last page of the wizard shows the changes that that are recommended based on your responses.</span></span> <span data-ttu-id="81be2-168">同时显示您的设置（**当前设置**）中的值和向导推荐的值（**新配置**）。</span><span class="sxs-lookup"><span data-stu-id="81be2-168">It shows both the value in your setup (**Current setup**) and the value that the wizard recommends (**New configuration**).</span></span>

<span data-ttu-id="81be2-169">也可以修改新配置中的参数。</span><span class="sxs-lookup"><span data-stu-id="81be2-169">You can also modify the parameters in the new configuration.</span></span> <span data-ttu-id="81be2-170">参数将拆分为应用于法人的参数和仅应用于所选主计划的参数。</span><span class="sxs-lookup"><span data-stu-id="81be2-170">The parameters are separated into parameters that apply to your legal entity and parameters that apply only to the master plan that you selected.</span></span> <span data-ttu-id="81be2-171">若要查看可通过使用此向导更改的所有设置参数，请选择页面底部的**显示所有参数**。</span><span class="sxs-lookup"><span data-stu-id="81be2-171">To view all the setup parameters that can be changed by using the wizard, select **Show all parameters** at the bottom of the page.</span></span> <span data-ttu-id="81be2-172">然后可以更改参数。</span><span class="sxs-lookup"><span data-stu-id="81be2-172">You can then change the parameters.</span></span>

<span data-ttu-id="81be2-173">最后，在选择**完成**时，将应用新配置。</span><span class="sxs-lookup"><span data-stu-id="81be2-173">Finally, when you select **Finish**, the new configuration is applied.</span></span> <span data-ttu-id="81be2-174">如果选择**取消**，则不应用任何更改。</span><span class="sxs-lookup"><span data-stu-id="81be2-174">If you select **Cancel**, none of the changes are applied.</span></span>

## <a name="examples"></a><span data-ttu-id="81be2-175">示例</span><span class="sxs-lookup"><span data-stu-id="81be2-175">Examples</span></span>

<span data-ttu-id="81be2-176">此部分介绍两家虚构公司的设置，以便显示该设置如何根据各企业的需求而变化。</span><span class="sxs-lookup"><span data-stu-id="81be2-176">This section describes the setup of two fictional companies to show how the setup can change according to the needs of each business.</span></span>

### <a name="example-1-contoso-manufacturer"></a><span data-ttu-id="81be2-177">示例 1：Contoso Manufacturer</span><span class="sxs-lookup"><span data-stu-id="81be2-177">Example 1: Contoso Manufacturer</span></span>

<span data-ttu-id="81be2-178">Contoso Manufacturer 是一家生产扬声器的制造公司。</span><span class="sxs-lookup"><span data-stu-id="81be2-178">Contoso Manufacturer is a manufacturing company that produces speakers.</span></span> <span data-ttu-id="81be2-179">该公司从大量供应商处购买大量用于扬声器成品的原材料和组件。</span><span class="sxs-lookup"><span data-stu-id="81be2-179">It purchases the various raw materials and components that are used for the final speakers from various suppliers.</span></span> <span data-ttu-id="81be2-180">下面是它的部分供应和制造特征：</span><span class="sxs-lookup"><span data-stu-id="81be2-180">Here are some of the characteristics of its supply and manufacturing:</span></span>

- <span data-ttu-id="81be2-181">公司制造的最终物料采用物料清单 (BOM) 结构。</span><span class="sxs-lookup"><span data-stu-id="81be2-181">The final items that the company manufactures have a bill of materials (BOM) structure.</span></span>
- <span data-ttu-id="81be2-182">所有最终物料和组件通过主计划计划。</span><span class="sxs-lookup"><span data-stu-id="81be2-182">All final items and components are planned by master planning.</span></span> <span data-ttu-id="81be2-183">不执行手动计划。</span><span class="sxs-lookup"><span data-stu-id="81be2-183">Manual planning isn't done.</span></span>
- <span data-ttu-id="81be2-184">将为每个最终物料的生产定义工序的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="81be2-184">A route of operations is defined for the production of each final item.</span></span>
- <span data-ttu-id="81be2-185">制造工厂生产最终物料。</span><span class="sxs-lookup"><span data-stu-id="81be2-185">The manufacturing plant produces the final items.</span></span> <span data-ttu-id="81be2-186">它定义了一些铣削和钻削机器，用于处理组件。</span><span class="sxs-lookup"><span data-stu-id="81be2-186">It has a defined number of milling and drilling machines that are used to process the components.</span></span> <span data-ttu-id="81be2-187">各种组件必须由这些机器处理。</span><span class="sxs-lookup"><span data-stu-id="81be2-187">The various components must be processed by these machines.</span></span>
- <span data-ttu-id="81be2-188">有多家供应商。</span><span class="sxs-lookup"><span data-stu-id="81be2-188">There are many suppliers.</span></span> <span data-ttu-id="81be2-189">物料的平均提前期为一周。</span><span class="sxs-lookup"><span data-stu-id="81be2-189">The average lead time for items is one week.</span></span> <span data-ttu-id="81be2-190">同一家供应商的一组物料的提前期为七周。</span><span class="sxs-lookup"><span data-stu-id="81be2-190">A group of items from the same supplier will have a lead time of seven weeks.</span></span>

<span data-ttu-id="81be2-191">在向导中，将为 Contoso Manufacturer 输入以下值：</span><span class="sxs-lookup"><span data-stu-id="81be2-191">In the wizard, the following values are entered for Contoso Manufacturer:</span></span>

- <span data-ttu-id="81be2-192">**覆盖范围：**</span><span class="sxs-lookup"><span data-stu-id="81be2-192">**Coverage:**</span></span>

    - <span data-ttu-id="81be2-193">**问题**：“是否要指定计划区间的天数？”</span><span class="sxs-lookup"><span data-stu-id="81be2-193">**Question:** "Do you want to specify the number of days of your planning horizon?"</span></span>
    - <span data-ttu-id="81be2-194">**回答**：“是，按照覆盖范围组中的定义。”</span><span class="sxs-lookup"><span data-stu-id="81be2-194">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="81be2-195">因为物料的提前期相差很大，所以 Contoso 不必将所有物料安排在将来的同一个期间。</span><span class="sxs-lookup"><span data-stu-id="81be2-195">Because the lead time for items is very different, Contoso doesn't have to plan all the items for the same period in the future.</span></span> <span data-ttu-id="81be2-196">将为物料创建覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="81be2-196">Coverage groups for the items are created.</span></span> <span data-ttu-id="81be2-197">将把提前期相似的物料分派给同一个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="81be2-197">Items that have a similar lead time are assigned to the same coverage group.</span></span> <span data-ttu-id="81be2-198">每个覆盖范围组的计划区间（即覆盖时限）大致为提前期加一周的差额。</span><span class="sxs-lookup"><span data-stu-id="81be2-198">The planning horizon for each coverage group (that is, the coverage time fence) is approximately the lead time plus a margin of one week.</span></span> <span data-ttu-id="81be2-199">然后，主计划确保根据其提前期提前计划物料。</span><span class="sxs-lookup"><span data-stu-id="81be2-199">Master planning then makes sure that the items are planned in advance, based on their lead time.</span></span>

    <span data-ttu-id="81be2-200">因此，将为此示例创建两个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="81be2-200">Therefore, two coverage groups will be created for this example.</span></span> <span data-ttu-id="81be2-201">一个覆盖范围组的覆盖时限为两周，另一个的覆盖时限为八周。</span><span class="sxs-lookup"><span data-stu-id="81be2-201">One coverage group will have a coverage time fence of two weeks, and the other will have a coverage time fence of eight weeks.</span></span>

    <span data-ttu-id="81be2-202">如果回答选择**是，按照此主计划中的定义**，则输入的天数应该超过所有物料中的最大提前期。</span><span class="sxs-lookup"><span data-stu-id="81be2-202">If **Yes, as defined in this master plan** is selected as the answer, the number of days that is entered should exceed the longest lead time of all the items.</span></span> <span data-ttu-id="81be2-203">但是，因为不必将大量物料提前这么久，所以将计算大量计划订单，但是从不使用这些订单。</span><span class="sxs-lookup"><span data-stu-id="81be2-203">However, because many items don't have to be planned so far in advance, many planned orders will be calculated but never used.</span></span> <span data-ttu-id="81be2-204">因此，主计划运行时间将增加。</span><span class="sxs-lookup"><span data-stu-id="81be2-204">Therefore, the master planning runtime will increase.</span></span>

- <span data-ttu-id="81be2-205">**计划编制：**</span><span class="sxs-lookup"><span data-stu-id="81be2-205">**Scheduling:**</span></span>

    - <span data-ttu-id="81be2-206">**问题**：“是否需要计划拆分为单个作业的工序?”</span><span class="sxs-lookup"><span data-stu-id="81be2-206">**Question:** "Do you need to schedule operations divided into individual jobs?"</span></span>
    - <span data-ttu-id="81be2-207">**回答**：“是。”</span><span class="sxs-lookup"><span data-stu-id="81be2-207">**Answer:** "Yes."</span></span>

    <span data-ttu-id="81be2-208">Contoso Manufacturing 必须计划和安排将对车间执行的单个作业。</span><span class="sxs-lookup"><span data-stu-id="81be2-208">Contoso Manufacturing must plan and schedule the individual jobs that will be performed on the shop floor.</span></span> <span data-ttu-id="81be2-209">因此，将使用作业级排产。</span><span class="sxs-lookup"><span data-stu-id="81be2-209">Therefore, it will use job scheduling.</span></span>

- <span data-ttu-id="81be2-210">**产能：**</span><span class="sxs-lookup"><span data-stu-id="81be2-210">**Capacity:**</span></span>

    - <span data-ttu-id="81be2-211">**问题**：“是否要使用资源的产能进行排产？”</span><span class="sxs-lookup"><span data-stu-id="81be2-211">**Question:** "Do you want to schedule using the capacity of resources?"</span></span>
    - <span data-ttu-id="81be2-212">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="81be2-212">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="81be2-213">输入了 **10 天**。</span><span class="sxs-lookup"><span data-stu-id="81be2-213">**10 days** is entered.</span></span>

    <span data-ttu-id="81be2-214">将限制铣削和钻削机器的数量。</span><span class="sxs-lookup"><span data-stu-id="81be2-214">The number of milling and drilling machines is limited.</span></span> <span data-ttu-id="81be2-215">生产计划必须考虑此限制，并根据资源产能及时安排作业。</span><span class="sxs-lookup"><span data-stu-id="81be2-215">Production planning must take this limitation into account and arrange the jobs in time according to the capacity of the resources.</span></span> <span data-ttu-id="81be2-216">换句话说，将根据资源的限制重新计划排产的作业。</span><span class="sxs-lookup"><span data-stu-id="81be2-216">In other words, the jobs that are scheduled will be replanned based on the limitations of the resources.</span></span> <span data-ttu-id="81be2-217">除了定义的期间，计划还将使用提前期。</span><span class="sxs-lookup"><span data-stu-id="81be2-217">Planning will use the lead time in addition to the period that is defined.</span></span> <span data-ttu-id="81be2-218">（计划的生产订单可重叠。）因为物料的生产提前期为七天，所以将考虑主计划在 10 天内的资源产能。</span><span class="sxs-lookup"><span data-stu-id="81be2-218">(Planned production orders can overlap.) Because the production lead time for the items is seven days, the capacity of the resources for master planning will be considered during 10 days.</span></span>

- <span data-ttu-id="81be2-219">**先后顺序：**</span><span class="sxs-lookup"><span data-stu-id="81be2-219">**Sequencing:**</span></span>

    - <span data-ttu-id="81be2-220">**问题**：“是否要使用产品的顺序值为计划的订单排序？”</span><span class="sxs-lookup"><span data-stu-id="81be2-220">**Question:** "Do you want to sequence planned orders using the product's sequence values?"</span></span>
    - <span data-ttu-id="81be2-221">**回答**：“是，按照覆盖范围组中的定义。”</span><span class="sxs-lookup"><span data-stu-id="81be2-221">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="81be2-222">将为每个最终物料的生产定义工艺路线。</span><span class="sxs-lookup"><span data-stu-id="81be2-222">A route is defined for the production of each final item.</span></span> <span data-ttu-id="81be2-223">因此，主计划将根据定义的工艺路线及时安排订单。</span><span class="sxs-lookup"><span data-stu-id="81be2-223">Therefore, master planning will schedule the orders in time according to the defined routes.</span></span>

- <span data-ttu-id="81be2-224">**分解：**</span><span class="sxs-lookup"><span data-stu-id="81be2-224">**Explosion:**</span></span>

    - <span data-ttu-id="81be2-225">**问题**：“是否要计划物料清单中所有元素的订单(针对父级和所有子级物料进行计划)?”</span><span class="sxs-lookup"><span data-stu-id="81be2-225">**Question:** "Do you want to plan orders for all the elements in a Bill of Materials (plan for the parent and all children items)?"</span></span>
    - <span data-ttu-id="81be2-226">**回答**：“是，按照覆盖范围组中的定义。”</span><span class="sxs-lookup"><span data-stu-id="81be2-226">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="81be2-227">必须计划用于生产的所有物料。</span><span class="sxs-lookup"><span data-stu-id="81be2-227">All the items that are used for the production must be planned.</span></span> <span data-ttu-id="81be2-228">因为物料的提前期相差极大，所以主计划在使用覆盖范围组时的性能更佳。</span><span class="sxs-lookup"><span data-stu-id="81be2-228">Because the items have very different lead times, master planning will have better performance when it uses the coverage groups.</span></span> <span data-ttu-id="81be2-229">而且，可以输入一周的差额，并且可以对与覆盖范围相同的时间进行分解。</span><span class="sxs-lookup"><span data-stu-id="81be2-229">Again, a margin of one week can be entered, and explosion can be done for the same time as the coverage.</span></span>

### <a name="example-2-contoso-retailer"></a><span data-ttu-id="81be2-230">示例 2：Contoso Retailer</span><span class="sxs-lookup"><span data-stu-id="81be2-230">Example 2: Contoso Retailer</span></span>

<span data-ttu-id="81be2-231">Contoso Retailer 是时尚行业的一家分销公司。</span><span class="sxs-lookup"><span data-stu-id="81be2-231">Contoso Retailer is a distribution company in the fashion industry.</span></span> <span data-ttu-id="81be2-232">该公司使用主计划，基于预测销量计算应在何时下达采购订单。</span><span class="sxs-lookup"><span data-stu-id="81be2-232">It uses master planning to calculate when purchase orders should be placed, based on its forecasted sales.</span></span> <span data-ttu-id="81be2-233">下面是该公司的部分特征：</span><span class="sxs-lookup"><span data-stu-id="81be2-233">Here are some of its characteristics:</span></span>

- <span data-ttu-id="81be2-234">Contoso Retailer 使用需求预测预测销量。</span><span class="sxs-lookup"><span data-stu-id="81be2-234">Contoso Retailer uses a demand forecast to predict sales.</span></span> <span data-ttu-id="81be2-235">将根据此预测计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="81be2-235">Purchase orders will be planned according to the forecast.</span></span>
- <span data-ttu-id="81be2-236">零售商店使用补货申请。</span><span class="sxs-lookup"><span data-stu-id="81be2-236">Retail stores use requisitions for replenishment.</span></span>
- <span data-ttu-id="81be2-237">从主仓库到每家商店的提前期为所有物料大约两周。</span><span class="sxs-lookup"><span data-stu-id="81be2-237">The lead time from the main warehouse to each store is approximately two weeks for all items.</span></span>

<span data-ttu-id="81be2-238">在向导中，将为 Contoso Retailer 输入以下值：</span><span class="sxs-lookup"><span data-stu-id="81be2-238">In the wizard, the following values are entered for Contoso Retailer:</span></span>

- <span data-ttu-id="81be2-239">**预测需求：**</span><span class="sxs-lookup"><span data-stu-id="81be2-239">**Forecast demand:**</span></span>

    - <span data-ttu-id="81be2-240">**问题**：“是否要在主计划中使用预测计划以便建议计划订单来满足预测的需求?”</span><span class="sxs-lookup"><span data-stu-id="81be2-240">**Question:** "Do you want to use a forecast plan in master planning so that planned orders will be suggested to fulfill the forecasted demand?"</span></span>
    - <span data-ttu-id="81be2-241">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="81be2-241">**Answer:** "Yes, as defined in this master plan."</span></span>

    <span data-ttu-id="81be2-242">Contoso 中有一个需求预测，用于预测其销量。</span><span class="sxs-lookup"><span data-stu-id="81be2-242">Contoso has included a demand forecast to predict its sales.</span></span> <span data-ttu-id="81be2-243">因此，主计划必须推荐计划订单以实现预测。</span><span class="sxs-lookup"><span data-stu-id="81be2-243">Therefore, master planning must recommend planned orders to fulfill the forecast.</span></span>

- <span data-ttu-id="81be2-244">**确认：**</span><span class="sxs-lookup"><span data-stu-id="81be2-244">**Firming:**</span></span>

    - <span data-ttu-id="81be2-245">**问题**：“是否希望主计划自动将计划订单确认到订单单据(例如生产或采购订单)?”</span><span class="sxs-lookup"><span data-stu-id="81be2-245">**Question:** "Do you want master planning to automatically firm planned orders into order documents, for example production or purchase orders?"</span></span>
    - <span data-ttu-id="81be2-246">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="81be2-246">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="81be2-247">输入了 **1 天**。</span><span class="sxs-lookup"><span data-stu-id="81be2-247">**1 day** is entered.</span></span>

    <span data-ttu-id="81be2-248">因为 Contoso Retailer 将直接从计划采购订单创建采购订单，所以如果自动确认计划采购订单，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="81be2-248">Because Contoso Retailer will create purchase orders directly from the planned purchase orders, it's useful if the planned purchase orders are automatically firmed.</span></span> <span data-ttu-id="81be2-249">因为公司每天运行主计划，所以一天的确认时限将自动确认下一天需要的所有订单。</span><span class="sxs-lookup"><span data-stu-id="81be2-249">Because the company runs master planning every day, a firming time fence of one day will automatically firm all the orders that are required for the next day.</span></span>

- <span data-ttu-id="81be2-250">**已审核的申请：**</span><span class="sxs-lookup"><span data-stu-id="81be2-250">**Approved requisitions:**</span></span>

    - <span data-ttu-id="81be2-251">**问题**：“是否要包含已审核的零售商店补货申请中的需求？”</span><span class="sxs-lookup"><span data-stu-id="81be2-251">**Question:** "Do you want to include demand from approved requisitions to replenish retail stores?"</span></span>
    - <span data-ttu-id="81be2-252">**回答**：“是，按照此主计划中的定义”。</span><span class="sxs-lookup"><span data-stu-id="81be2-252">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="81be2-253">输入了 **1 天**。</span><span class="sxs-lookup"><span data-stu-id="81be2-253">**1 day** is entered.</span></span>

    <span data-ttu-id="81be2-254">Contoso 使用其零售商店的已审核申请创建计划采购订单来为这些商店补货。</span><span class="sxs-lookup"><span data-stu-id="81be2-254">Contoso uses the approved requisitions from its retail stores to create planned purchase orders to replenish those stores.</span></span> <span data-ttu-id="81be2-255">因为每天运行主计划，所以计划中将包含前一天的申请。</span><span class="sxs-lookup"><span data-stu-id="81be2-255">Because master planning is run every day, the requisitions from the last day will be included in the planning.</span></span>
