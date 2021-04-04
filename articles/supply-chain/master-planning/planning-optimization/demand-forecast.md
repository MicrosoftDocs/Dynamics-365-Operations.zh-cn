---
title: 具有需求预测的主计划
description: 本主题介绍如何使用计划优化在主计划期间包括需求预测。
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7bd1268893d0869d2414b944493c8b8859f27abc
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501118"
---
# <a name="master-planning-with-demand-forecasts"></a><span data-ttu-id="de885-103">具有需求预测的主计划</span><span class="sxs-lookup"><span data-stu-id="de885-103">Master planning with demand forecasts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de885-104">您可以将需求预测与计划优化一起使用，以在主计划中考虑预期需求。</span><span class="sxs-lookup"><span data-stu-id="de885-104">You can use a demand forecast together with Planning Optimization to account for expected demand in your master planning.</span></span> <span data-ttu-id="de885-105">您可以使用 Microsoft Dynamics 365 Supply Chain Management 中的需求预测功能手动创建、导入或生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-105">You can manually create a demand forecast, import it, or generate it by using the demand forecasting functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="de885-106">有关需求预测的详细信息，请参阅[需求预测概述](../introduction-demand-forecasting.md)。</span><span class="sxs-lookup"><span data-stu-id="de885-106">For more information about demand forecasting, see [Demand forecasting overview](../introduction-demand-forecasting.md).</span></span>

> [!NOTE]
> <span data-ttu-id="de885-107">计划优化不支持单独的预测计划。</span><span class="sxs-lookup"><span data-stu-id="de885-107">Separate forecast planning isn't supported with Planning Optimization.</span></span> <span data-ttu-id="de885-108">因此，在使用计划优化时，**主计划参数** 页面上的 **当前预测计划** 设置无效。</span><span class="sxs-lookup"><span data-stu-id="de885-108">Therefore, the **Current forecast plan** setting on the **Master planning parameters** page has no effect when you use Planning Optimization.</span></span>

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a><span data-ttu-id="de885-109">设置主计划以包括需求预测</span><span class="sxs-lookup"><span data-stu-id="de885-109">Set up a master plan to include a demand forecast</span></span>

<span data-ttu-id="de885-110">若要配置主计划以使其包括需求预测，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="de885-110">To configure a master plan so that it includes a demand forecast, follow these steps.</span></span>

1. <span data-ttu-id="de885-111">转到 **主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="de885-111">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="de885-112">选择一个现有计划，或创建新计划。</span><span class="sxs-lookup"><span data-stu-id="de885-112">Select an existing plan, or create a new plan.</span></span>
1. <span data-ttu-id="de885-113">在 **常规** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="de885-113">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="de885-114">**预测模型** – 选择要应用的预测模型。</span><span class="sxs-lookup"><span data-stu-id="de885-114">**Forecast model** – Select the forecast model to apply.</span></span> <span data-ttu-id="de885-115">当为当前主计划生成供应建议时，将考虑该模型。</span><span class="sxs-lookup"><span data-stu-id="de885-115">This model will be considered when a supply suggestion is generated for the current master plan.</span></span>
    - <span data-ttu-id="de885-116">**包括需求预测** – 将此选项设置为 *是* 以在当前主计划中包括需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-116">**Include demand forecast** – Set this option to *Yes* to include the demand forecast in the current master plan.</span></span> <span data-ttu-id="de885-117">如果设置为 *否*，需求预测交易将不包含在主计划中。</span><span class="sxs-lookup"><span data-stu-id="de885-117">If you set it to *No*, demand forecast transactions won't be included in the master plan.</span></span>
    - <span data-ttu-id="de885-118">**用于减少预测需求的方法** – 选择应用于减少预测需求的方法。</span><span class="sxs-lookup"><span data-stu-id="de885-118">**Method used to reduce forecast requirements** – Select the method that should be used to reduce forecast requirements.</span></span> <span data-ttu-id="de885-119">有关详细信息，请参阅本主题后面的[预测缩减参数](#reduction-keys)部分。</span><span class="sxs-lookup"><span data-stu-id="de885-119">For more information, see the [Forecast reduction keys](#reduction-keys) section later in this topic.</span></span>

1. <span data-ttu-id="de885-120">在 **时限（天）** 快速选项卡上，您可以设置以下字段来指定包括需求预测的期间：</span><span class="sxs-lookup"><span data-stu-id="de885-120">On the **Time fence in days** FastTab, you can set the following fields to specify the period that the demand forecast is included during:</span></span>

    - <span data-ttu-id="de885-121">**预测计划** – 将此选项设置为 *是* 以替代源自各个覆盖范围组的预测计划时限。</span><span class="sxs-lookup"><span data-stu-id="de885-121">**Forecast plan** – Set this option to *Yes* to override the forecast plan time fence that originates from the individual coverage groups.</span></span> <span data-ttu-id="de885-122">设置为 *否* 以使用来自当前主计划的各个覆盖范围组中的值。</span><span class="sxs-lookup"><span data-stu-id="de885-122">Set it to *No* to use the values from the individual coverage groups for the current master plan.</span></span>
    - <span data-ttu-id="de885-123">**预测时段** – 如果您将 **预测计划** 选项设置为 *是*，请指定应该应用需求预测的天数（从今天开始）。</span><span class="sxs-lookup"><span data-stu-id="de885-123">**Forecast time period** – If you set the **Forecast plan** option to *Yes*, specify the number of days (from today's date) that the demand forecast should be applied.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de885-124">计划优化尚不支持 **预测计划** 设置。</span><span class="sxs-lookup"><span data-stu-id="de885-124">The **Forecast plan** setting isn't yet supported with Planning Optimization.</span></span>

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a><span data-ttu-id="de885-125">设置覆盖范围组以包括需求预测</span><span class="sxs-lookup"><span data-stu-id="de885-125">Set up a coverage group to include a demand forecast</span></span>

<span data-ttu-id="de885-126">若要配置覆盖范围组以使其包括需求预测，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="de885-126">To configure a coverage group so that it includes a demand forecast, follow these steps.</span></span>

1. <span data-ttu-id="de885-127">转到 **主计划 \> 设置 \> 计划 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="de885-127">Go to **Master planning \> Setup \> Plans \> Coverage groups**.</span></span>
1. <span data-ttu-id="de885-128">选择一个现有覆盖范围组，或创建新组。</span><span class="sxs-lookup"><span data-stu-id="de885-128">Select an existing coverage group, or create a new group.</span></span>
1. <span data-ttu-id="de885-129">在 **其他** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="de885-129">On the **Other** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="de885-130">**预测计划时限** – 输入应该应用需求预测的天数（从今天开始）。</span><span class="sxs-lookup"><span data-stu-id="de885-130">**Forecast plan time fence** – Enter the number of days (from today's date) that the demand forecast should be applied for.</span></span> <span data-ttu-id="de885-131">可以使用主计划上的 **预测计划** 选项替代此值，如上一部分所述。</span><span class="sxs-lookup"><span data-stu-id="de885-131">This value can be overridden by using the **Forecast plan** option on the master plan, as described in the previous section.</span></span>
    - <span data-ttu-id="de885-132">**缩减参数** – 选择要应用的缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-132">**Reduction key** – Select the reduction key to apply.</span></span> <span data-ttu-id="de885-133">有关详细信息，请参阅本主题后面的[创建和设置预测缩减参数](#create-reduction-key)和[使用缩减参数](#use-reduction-key)部分。</span><span class="sxs-lookup"><span data-stu-id="de885-133">For more information, see the [Create and set up a forecast reduction key](#create-reduction-key) and [Use a reduction key](#use-reduction-key) sections later in this topic.</span></span>
    - <span data-ttu-id="de885-134">**预测减少依据** – 对于 **用于减少预测需求的方法** 字段设置为 *交易 - 缩减参数* 或 *交易 - 动态期间* 的主计划，指定哪些交易应减少预测。</span><span class="sxs-lookup"><span data-stu-id="de885-134">**Reduce forecast by** – For master plans where the **Method used to reduce forecast requirements** field is set to *Transactions - reduction key* or *Transactions - dynamic period*, specify which transactions should reduce the forecast.</span></span> <span data-ttu-id="de885-135">选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="de885-135">Select one of the following values:</span></span>

        - <span data-ttu-id="de885-136">**所有交易** – 所有交易都应减少预测。</span><span class="sxs-lookup"><span data-stu-id="de885-136">**All transactions** – All transactions should reduce the forecast.</span></span>
        - <span data-ttu-id="de885-137">**订单** – 仅销售订单应减少预测。</span><span class="sxs-lookup"><span data-stu-id="de885-137">**Orders** – Only sales orders should reduce the forecast.</span></span>

        > [!NOTE]
        > <span data-ttu-id="de885-138">如果选择 *所有交易*，在相同的库存维度上具有需求和供应的交易将视为中性，并将在预测减少期间忽略。</span><span class="sxs-lookup"><span data-stu-id="de885-138">If you select *All transactions*, transactions that have both demand and supply in the same inventory dimensions are considered neutral and are ignored during the forecast reduction.</span></span> <span data-ttu-id="de885-139">例如，如果计划维度设置为仅站点（而不是仓库），将忽略站点 1，仓库 11 和站点 1，仓库 13 之间的转移单，并且不会减少剩余需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-139">For example, if the planning dimension is set to site only, not warehouse, a transfer order between site 1, warehouse 11, and site 1, warehouse 13, will be ignored and won't reduce the remaining demand forecast.</span></span>

    - <span data-ttu-id="de885-140">**包括内部公司订单** – 如果在减少预测时应包括内部公司订单，将此选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="de885-140">**Include intercompany orders** – Set this option to *Yes* if intercompany orders should be included when the forecast is reduced.</span></span> <span data-ttu-id="de885-141">否则，将其设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="de885-141">Otherwise, set it to *No*.</span></span>
    - <span data-ttu-id="de885-142">**在需求预测中包括客户预测** – 指定是否应在整个预测中包括客户预测。</span><span class="sxs-lookup"><span data-stu-id="de885-142">**Include customer forecast in the demand forecast** – Specify whether a customer forecast should be included in the overall forecast.</span></span> <span data-ttu-id="de885-143">此选项确定实际需求如何减少预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-143">This option determines how actual demand reduces the forecasted demand.</span></span> <span data-ttu-id="de885-144">您可以使用它确保主计划涵盖特定客户采购的物料供应。</span><span class="sxs-lookup"><span data-stu-id="de885-144">You can use it to ensure that master planning covers the supply of items that are purchased by specific customers.</span></span>

        - <span data-ttu-id="de885-145">将此选项设置为 *是* 以在整个预测中包括客户预测。</span><span class="sxs-lookup"><span data-stu-id="de885-145">Set this option to *Yes* to include a customer forecast in the overall forecast.</span></span> <span data-ttu-id="de885-146">在这种情况下，实际客户需求会同时减少客户预测和整个预测。</span><span class="sxs-lookup"><span data-stu-id="de885-146">In this case, actual customer demand reduces both the customer forecast and the overall forecast.</span></span> <span data-ttu-id="de885-147">主计划将生成计划订单以仅涵盖整个预测数量。</span><span class="sxs-lookup"><span data-stu-id="de885-147">Master planning generates planned orders to cover only the overall forecast quantity.</span></span>
        - <span data-ttu-id="de885-148">如果您不希望在整个预测中包括客户预测，将此选项设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="de885-148">Set this option to *No* if you don't want to include a customer forecast in the overall forecast.</span></span> <span data-ttu-id="de885-149">在这种情况下，实际客户需求仅减少客户预测。</span><span class="sxs-lookup"><span data-stu-id="de885-149">In this case, actual customer demand reduces only the customer forecast.</span></span> <span data-ttu-id="de885-150">主计划将生成计划订单，以涵盖整个预测数量和每个客户数量的预测。</span><span class="sxs-lookup"><span data-stu-id="de885-150">Master planning generates planned orders to cover both the overall forecast quantity and the forecast for each customer quantity.</span></span>

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a><span data-ttu-id="de885-151">预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-151">Forecast reduction keys</span></span>

<span data-ttu-id="de885-152">此部分提供有关用于减少预测需求的不同方法的信息。</span><span class="sxs-lookup"><span data-stu-id="de885-152">This section provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="de885-153">其中包括每种方法的结果的示例。</span><span class="sxs-lookup"><span data-stu-id="de885-153">It includes examples of the results of each method.</span></span> <span data-ttu-id="de885-154">还介绍如何创建、设置和使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-154">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="de885-155">一些方法使用预测缩减参数缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-155">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="de885-156">用于缩减预测需求的方法</span><span class="sxs-lookup"><span data-stu-id="de885-156">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="de885-157">向主计划添加预测时，可以选择包含实际需求时如何缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-157">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span> <span data-ttu-id="de885-158">请注意，主计划中不包含过去的预测要求，即当天以前的所有预测要求。</span><span class="sxs-lookup"><span data-stu-id="de885-158">Note that master planning excludes forecast requirements from the past, which means all forecast requirements before today's date.</span></span>

<span data-ttu-id="de885-159">若要在主计划中添加预测并选择用于缩减预测需求的方法，请转到 **主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="de885-159">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="de885-160">在 **预测模型** 字段中，选择一个预测模型。</span><span class="sxs-lookup"><span data-stu-id="de885-160">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="de885-161">在 **用于减少预测需求的方法** 字段中，选择一个方法。</span><span class="sxs-lookup"><span data-stu-id="de885-161">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="de885-162">选项如下：</span><span class="sxs-lookup"><span data-stu-id="de885-162">The following options are available:</span></span>

- <span data-ttu-id="de885-163">None</span><span class="sxs-lookup"><span data-stu-id="de885-163">None</span></span>
- <span data-ttu-id="de885-164">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-164">Percent – reduction key</span></span>
- <span data-ttu-id="de885-165">交易 – 缩减参数（计划优化尚不支持）</span><span class="sxs-lookup"><span data-stu-id="de885-165">Transactions – reduction key (not yet supported with Planning Optimization)</span></span>
- <span data-ttu-id="de885-166">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="de885-166">Transactions – dynamic period</span></span>

<span data-ttu-id="de885-167">以下部分提供有关每个选项的详细信息。</span><span class="sxs-lookup"><span data-stu-id="de885-167">The following sections provide more information about each option.</span></span>

#### <a name="none"></a><span data-ttu-id="de885-168">无</span><span class="sxs-lookup"><span data-stu-id="de885-168">None</span></span>

<span data-ttu-id="de885-169">如果您选择 **无**，则在主计划编制期间不缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-169">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="de885-170">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="de885-170">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="de885-171">这些计划订单中维持建议的数量，不考虑其他类型的需求。</span><span class="sxs-lookup"><span data-stu-id="de885-171">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="de885-172">例如，如果下达销售订单，主计划将创建更多计划订单以供给销售订单。</span><span class="sxs-lookup"><span data-stu-id="de885-172">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="de885-173">将不缩减预测需求的数量。</span><span class="sxs-lookup"><span data-stu-id="de885-173">The quantity of the forecast requirements isn't reduced.</span></span>

#### <a name="percent--reduction-key"></a><span data-ttu-id="de885-174">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-174">Percent – reduction key</span></span>

<span data-ttu-id="de885-175">如果选择 **百分比 - 缩减参数**，则根据百分比和缩减参数定义的百分比和期间来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-175">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="de885-176">在此案例中，主计划创建计划订单，在此类订单中，数量的计算方法是预测数量 × 各期间的缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-176">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="de885-177">如果有其他类型的需求，主计划还将创建计划订单以满足该需求。</span><span class="sxs-lookup"><span data-stu-id="de885-177">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

##### <a name="example-percent--reduction-key"></a><span data-ttu-id="de885-178">示例：百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-178">Example: Percent – reduction key</span></span>

<span data-ttu-id="de885-179">此示例显示由缩减参数如何根据由缩减参数定义的百分比和期间缩减需求预测要求。</span><span class="sxs-lookup"><span data-stu-id="de885-179">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="de885-180">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-180">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="de885-181">月</span><span class="sxs-lookup"><span data-stu-id="de885-181">Month</span></span>    | <span data-ttu-id="de885-182">需求预测</span><span class="sxs-lookup"><span data-stu-id="de885-182">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="de885-183">一月</span><span class="sxs-lookup"><span data-stu-id="de885-183">January</span></span>  | <span data-ttu-id="de885-184">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-184">1,000</span></span>           |
| <span data-ttu-id="de885-185">二月</span><span class="sxs-lookup"><span data-stu-id="de885-185">February</span></span> | <span data-ttu-id="de885-186">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-186">1,000</span></span>           |
| <span data-ttu-id="de885-187">三月</span><span class="sxs-lookup"><span data-stu-id="de885-187">March</span></span>    | <span data-ttu-id="de885-188">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-188">1,000</span></span>           |
| <span data-ttu-id="de885-189">四月</span><span class="sxs-lookup"><span data-stu-id="de885-189">April</span></span>    | <span data-ttu-id="de885-190">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-190">1,000</span></span>           |

<span data-ttu-id="de885-191">在 **缩减参数** 页上，设置以下行。</span><span class="sxs-lookup"><span data-stu-id="de885-191">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="de885-192">找零</span><span class="sxs-lookup"><span data-stu-id="de885-192">Change</span></span> | <span data-ttu-id="de885-193">单位</span><span class="sxs-lookup"><span data-stu-id="de885-193">Unit</span></span>  | <span data-ttu-id="de885-194">百分比</span><span class="sxs-lookup"><span data-stu-id="de885-194">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="de885-195">1</span><span class="sxs-lookup"><span data-stu-id="de885-195">1</span></span>      | <span data-ttu-id="de885-196">月</span><span class="sxs-lookup"><span data-stu-id="de885-196">Month</span></span> | <span data-ttu-id="de885-197">100</span><span class="sxs-lookup"><span data-stu-id="de885-197">100</span></span>     |
| <span data-ttu-id="de885-198">2</span><span class="sxs-lookup"><span data-stu-id="de885-198">2</span></span>      | <span data-ttu-id="de885-199">月</span><span class="sxs-lookup"><span data-stu-id="de885-199">Month</span></span> | <span data-ttu-id="de885-200">75</span><span class="sxs-lookup"><span data-stu-id="de885-200">75</span></span>      |
| <span data-ttu-id="de885-201">3</span><span class="sxs-lookup"><span data-stu-id="de885-201">3</span></span>      | <span data-ttu-id="de885-202">月</span><span class="sxs-lookup"><span data-stu-id="de885-202">Month</span></span> | <span data-ttu-id="de885-203">50</span><span class="sxs-lookup"><span data-stu-id="de885-203">50</span></span>      |
| <span data-ttu-id="de885-204">4</span><span class="sxs-lookup"><span data-stu-id="de885-204">4</span></span>      | <span data-ttu-id="de885-205">月</span><span class="sxs-lookup"><span data-stu-id="de885-205">Month</span></span> | <span data-ttu-id="de885-206">25</span><span class="sxs-lookup"><span data-stu-id="de885-206">25</span></span>      |

<span data-ttu-id="de885-207">将缩减参数分配给物料的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="de885-207">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="de885-208">然后在 **主计划** 页的 **用于缩减预测需求的方法** 字段中，选择 **百分比 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="de885-208">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="de885-209">在此案例中，如果在 1 月 1 日运行预测计划编制，则将根据您在 **缩减参数** 页上设置的百分比来消耗销售预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-209">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="de885-210">以下需求数量将转移到主计划。</span><span class="sxs-lookup"><span data-stu-id="de885-210">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="de885-211">月</span><span class="sxs-lookup"><span data-stu-id="de885-211">Month</span></span>                | <span data-ttu-id="de885-212">计划订单数量</span><span class="sxs-lookup"><span data-stu-id="de885-212">Planned order quantity</span></span> | <span data-ttu-id="de885-213">计算</span><span class="sxs-lookup"><span data-stu-id="de885-213">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="de885-214">一月</span><span class="sxs-lookup"><span data-stu-id="de885-214">January</span></span>              | <span data-ttu-id="de885-215">0</span><span class="sxs-lookup"><span data-stu-id="de885-215">0</span></span>                      | <span data-ttu-id="de885-216">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="de885-216">= 0% × 1,000</span></span>   |
| <span data-ttu-id="de885-217">二月</span><span class="sxs-lookup"><span data-stu-id="de885-217">February</span></span>             | <span data-ttu-id="de885-218">250</span><span class="sxs-lookup"><span data-stu-id="de885-218">250</span></span>                    | <span data-ttu-id="de885-219">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="de885-219">= 25% × 1,000</span></span>  |
| <span data-ttu-id="de885-220">三月</span><span class="sxs-lookup"><span data-stu-id="de885-220">March</span></span>                | <span data-ttu-id="de885-221">500</span><span class="sxs-lookup"><span data-stu-id="de885-221">500</span></span>                    | <span data-ttu-id="de885-222">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="de885-222">= 50% × 1,000</span></span>  |
| <span data-ttu-id="de885-223">四月</span><span class="sxs-lookup"><span data-stu-id="de885-223">April</span></span>                | <span data-ttu-id="de885-224">750</span><span class="sxs-lookup"><span data-stu-id="de885-224">750</span></span>                    | <span data-ttu-id="de885-225">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="de885-225">= 75% × 1,000</span></span>  |
| <span data-ttu-id="de885-226">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="de885-226">May through December</span></span> | <span data-ttu-id="de885-227">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-227">1,000</span></span>                  | <span data-ttu-id="de885-228">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="de885-228">= 100% × 1,000</span></span> |

#### <a name="transactions--reduction-key"></a><span data-ttu-id="de885-229">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-229">Transactions – reduction key</span></span>

<span data-ttu-id="de885-230">如果选择 **交易记录 - 缩减参数**，则通过在缩减参数定义的期间内发生的交易记录来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-230">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

##### <a name="example-transactions--reduction-key"></a><span data-ttu-id="de885-231">示例：交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-231">Example: Transactions – reduction key</span></span>

<span data-ttu-id="de885-232">此示例显示如何实际订单，这将在由缩减参数和缩减需求预测要求定义的期间发生。</span><span class="sxs-lookup"><span data-stu-id="de885-232">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="de885-233">对于本示例，在 **主计划** 页的 **用于缩减预测需求的方法** 字段中，选择 **交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="de885-233">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="de885-234">1 月 1 日存在以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="de885-234">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="de885-235">月</span><span class="sxs-lookup"><span data-stu-id="de885-235">Month</span></span>    | <span data-ttu-id="de885-236">订购的份数</span><span class="sxs-lookup"><span data-stu-id="de885-236">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="de885-237">一月</span><span class="sxs-lookup"><span data-stu-id="de885-237">January</span></span>  | <span data-ttu-id="de885-238">956</span><span class="sxs-lookup"><span data-stu-id="de885-238">956</span></span>                      |
| <span data-ttu-id="de885-239">二月</span><span class="sxs-lookup"><span data-stu-id="de885-239">February</span></span> | <span data-ttu-id="de885-240">1,176</span><span class="sxs-lookup"><span data-stu-id="de885-240">1,176</span></span>                    |
| <span data-ttu-id="de885-241">三月</span><span class="sxs-lookup"><span data-stu-id="de885-241">March</span></span>    | <span data-ttu-id="de885-242">451</span><span class="sxs-lookup"><span data-stu-id="de885-242">451</span></span>                      |
| <span data-ttu-id="de885-243">四月</span><span class="sxs-lookup"><span data-stu-id="de885-243">April</span></span>    | <span data-ttu-id="de885-244">119</span><span class="sxs-lookup"><span data-stu-id="de885-244">119</span></span>                      |

<span data-ttu-id="de885-245">如果您使用上一个示例中使用的同一个每月 1,000 份需求预测，将向主计划转移以下需求数量。</span><span class="sxs-lookup"><span data-stu-id="de885-245">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="de885-246">月</span><span class="sxs-lookup"><span data-stu-id="de885-246">Month</span></span>                | <span data-ttu-id="de885-247">所需的份数</span><span class="sxs-lookup"><span data-stu-id="de885-247">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="de885-248">一月</span><span class="sxs-lookup"><span data-stu-id="de885-248">January</span></span>              | <span data-ttu-id="de885-249">44</span><span class="sxs-lookup"><span data-stu-id="de885-249">44</span></span>                        |
| <span data-ttu-id="de885-250">二月</span><span class="sxs-lookup"><span data-stu-id="de885-250">February</span></span>             | <span data-ttu-id="de885-251">0</span><span class="sxs-lookup"><span data-stu-id="de885-251">0</span></span>                         |
| <span data-ttu-id="de885-252">三月</span><span class="sxs-lookup"><span data-stu-id="de885-252">March</span></span>                | <span data-ttu-id="de885-253">549</span><span class="sxs-lookup"><span data-stu-id="de885-253">549</span></span>                       |
| <span data-ttu-id="de885-254">四月</span><span class="sxs-lookup"><span data-stu-id="de885-254">April</span></span>                | <span data-ttu-id="de885-255">881</span><span class="sxs-lookup"><span data-stu-id="de885-255">881</span></span>                       |
| <span data-ttu-id="de885-256">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="de885-256">May through December</span></span> | <span data-ttu-id="de885-257">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-257">1,000</span></span>                     |

#### <a name="transactions--dynamic-period"></a><span data-ttu-id="de885-258">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="de885-258">Transactions – dynamic period</span></span>

<span data-ttu-id="de885-259">如果选择 **交易记录 - 动态期间**，将按动态期间进行的实际订单交易记录缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-259">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="de885-260">动态期间涵盖当前预测日期，并在下一预测开始时结束。</span><span class="sxs-lookup"><span data-stu-id="de885-260">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="de885-261">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="de885-261">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="de885-262">但是，下达实际订单交易记录时，将缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-262">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="de885-263">实际交易记录占用部分预测需求。</span><span class="sxs-lookup"><span data-stu-id="de885-263">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="de885-264">在使用此选项时，会发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="de885-264">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="de885-265">将不需要或不使用缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-265">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="de885-266">如果完全缩减预测，则当前预测的预测需求变为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="de885-266">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="de885-267">如果没有将来的预测，则最后一个输入的预测的预测需求会缩减。</span><span class="sxs-lookup"><span data-stu-id="de885-267">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="de885-268">时限包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="de885-268">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="de885-269">正天数包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="de885-269">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="de885-270">如果实际订单交易记录超过预测的需求，则其余的交易记录不会前进到下一预测期间。</span><span class="sxs-lookup"><span data-stu-id="de885-270">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

##### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="de885-271">示例 1：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="de885-271">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="de885-272">下面是一个简单示例，该示例显示 **交易记录 - 动态期间** 方法的工作原理。</span><span class="sxs-lookup"><span data-stu-id="de885-272">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="de885-273">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-273">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="de885-274">日期</span><span class="sxs-lookup"><span data-stu-id="de885-274">Date</span></span>       | <span data-ttu-id="de885-275">需求预测</span><span class="sxs-lookup"><span data-stu-id="de885-275">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="de885-276">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="de885-276">January 1</span></span>  | <span data-ttu-id="de885-277">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-277">1,000</span></span>           |
| <span data-ttu-id="de885-278">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="de885-278">February 1</span></span> | <span data-ttu-id="de885-279">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-279">1,000</span></span>             |

<span data-ttu-id="de885-280">还将创建以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="de885-280">You also create the following sales orders.</span></span>

| <span data-ttu-id="de885-281">日期</span><span class="sxs-lookup"><span data-stu-id="de885-281">Date</span></span>        | <span data-ttu-id="de885-282">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="de885-282">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="de885-283">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="de885-283">January 15</span></span>  | <span data-ttu-id="de885-284">200</span><span class="sxs-lookup"><span data-stu-id="de885-284">200</span></span>                  |
| <span data-ttu-id="de885-285">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="de885-285">February 15</span></span> | <span data-ttu-id="de885-286">400</span><span class="sxs-lookup"><span data-stu-id="de885-286">400</span></span>                  |

<span data-ttu-id="de885-287">在此案例中，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="de885-287">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="de885-288">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="de885-288">Demand forecast date</span></span> | <span data-ttu-id="de885-289">数量</span><span class="sxs-lookup"><span data-stu-id="de885-289">Quantity</span></span> | <span data-ttu-id="de885-290">摘要</span><span class="sxs-lookup"><span data-stu-id="de885-290">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="de885-291">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="de885-291">January 1</span></span>            | <span data-ttu-id="de885-292">800</span><span class="sxs-lookup"><span data-stu-id="de885-292">800</span></span>      | <span data-ttu-id="de885-293">预测需求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="de885-293">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="de885-294">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="de885-294">January 15</span></span>           | <span data-ttu-id="de885-295">200</span><span class="sxs-lookup"><span data-stu-id="de885-295">200</span></span>      | <span data-ttu-id="de885-296">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="de885-296">Sales orders requirements</span></span>             |
| <span data-ttu-id="de885-297">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="de885-297">February 1</span></span>           | <span data-ttu-id="de885-298">600</span><span class="sxs-lookup"><span data-stu-id="de885-298">600</span></span>      | <span data-ttu-id="de885-299">预测需求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="de885-299">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="de885-300">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="de885-300">February 15</span></span>          | <span data-ttu-id="de885-301">400</span><span class="sxs-lookup"><span data-stu-id="de885-301">400</span></span>      | <span data-ttu-id="de885-302">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="de885-302">Sales orders requirements</span></span>             |

##### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="de885-303">示例 2：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="de885-303">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="de885-304">在大多数情况下，会设置系统以使交易记录在特定预测期间减少需求预测：周、月，等等。</span><span class="sxs-lookup"><span data-stu-id="de885-304">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="de885-305">这些期间是在缩减参数中定义的。</span><span class="sxs-lookup"><span data-stu-id="de885-305">These periods are defined in the reduction key.</span></span> <span data-ttu-id="de885-306">但是，两个需求预测行之间的时间还可 *提示* 期间。</span><span class="sxs-lookup"><span data-stu-id="de885-306">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="de885-307">对于此示例，将为以下日期和数量创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-307">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="de885-308">日期</span><span class="sxs-lookup"><span data-stu-id="de885-308">Date</span></span>       | <span data-ttu-id="de885-309">需求预测</span><span class="sxs-lookup"><span data-stu-id="de885-309">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="de885-310">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="de885-310">January 1</span></span>  | <span data-ttu-id="de885-311">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-311">1,000</span></span>           |
| <span data-ttu-id="de885-312">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="de885-312">January 5</span></span>  | <span data-ttu-id="de885-313">500</span><span class="sxs-lookup"><span data-stu-id="de885-313">500</span></span>             |
| <span data-ttu-id="de885-314">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="de885-314">January 12</span></span> | <span data-ttu-id="de885-315">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-315">1,000</span></span>           |

<span data-ttu-id="de885-316">请注意，在此预测中，预测日期之间没有清晰的间隔。</span><span class="sxs-lookup"><span data-stu-id="de885-316">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="de885-317">第一个和第二个日期之间的间隔为四天，第二个和第三个日期之间的间隔为七天。</span><span class="sxs-lookup"><span data-stu-id="de885-317">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="de885-318">这些间隔就是动态期间。</span><span class="sxs-lookup"><span data-stu-id="de885-318">These spans are the dynamic periods.</span></span>

<span data-ttu-id="de885-319">还将创建以下销售订单行。</span><span class="sxs-lookup"><span data-stu-id="de885-319">You also create the following sales order lines.</span></span>

| <span data-ttu-id="de885-320">日期</span><span class="sxs-lookup"><span data-stu-id="de885-320">Date</span></span>                             | <span data-ttu-id="de885-321">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="de885-321">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="de885-322">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="de885-322">December 15 in the previous year</span></span> | <span data-ttu-id="de885-323">500</span><span class="sxs-lookup"><span data-stu-id="de885-323">500</span></span>                  |
| <span data-ttu-id="de885-324">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="de885-324">January 3</span></span>                        | <span data-ttu-id="de885-325">100</span><span class="sxs-lookup"><span data-stu-id="de885-325">100</span></span>                  |
| <span data-ttu-id="de885-326">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="de885-326">January 10</span></span>                       | <span data-ttu-id="de885-327">200</span><span class="sxs-lookup"><span data-stu-id="de885-327">200</span></span>                  |

<span data-ttu-id="de885-328">在此案例中，将以下面的方式缩减预测：</span><span class="sxs-lookup"><span data-stu-id="de885-328">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="de885-329">因为第一个销售订单不在任何期间，因此不会缩减任何预测。</span><span class="sxs-lookup"><span data-stu-id="de885-329">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="de885-330">因为第二个销售订单是从 1 月 1 日到 1 月 5 日，因此它会将 1 月 1 日的预测缩减 100。</span><span class="sxs-lookup"><span data-stu-id="de885-330">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="de885-331">因为第三个销售订单是从 5 月 5 日到 5 月 12 日，因此它会将 5 月 5 日的预测缩减 200。</span><span class="sxs-lookup"><span data-stu-id="de885-331">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="de885-332">因此，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="de885-332">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="de885-333">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="de885-333">Demand forecast date</span></span>             | <span data-ttu-id="de885-334">数量</span><span class="sxs-lookup"><span data-stu-id="de885-334">Quantity</span></span> | <span data-ttu-id="de885-335">摘要</span><span class="sxs-lookup"><span data-stu-id="de885-335">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="de885-336">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="de885-336">December 15 in the previous year</span></span> | <span data-ttu-id="de885-337">500</span><span class="sxs-lookup"><span data-stu-id="de885-337">500</span></span>      | <span data-ttu-id="de885-338">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="de885-338">Sales order requirements</span></span>                                            |
| <span data-ttu-id="de885-339">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="de885-339">January 1</span></span>                        | <span data-ttu-id="de885-340">900</span><span class="sxs-lookup"><span data-stu-id="de885-340">900</span></span>      | <span data-ttu-id="de885-341">预测需求期间 1 月 1 日到 1 月 5 日 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="de885-341">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="de885-342">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="de885-342">January 3</span></span>                        | <span data-ttu-id="de885-343">100</span><span class="sxs-lookup"><span data-stu-id="de885-343">100</span></span>      | <span data-ttu-id="de885-344">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="de885-344">Sales order requirements</span></span>                                            |
| <span data-ttu-id="de885-345">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="de885-345">January 5</span></span>                        | <span data-ttu-id="de885-346">300</span><span class="sxs-lookup"><span data-stu-id="de885-346">300</span></span>      | <span data-ttu-id="de885-347">预测需求期间 1 月 5 日到 1 月 10 日 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="de885-347">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="de885-348">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="de885-348">January 12</span></span>                       | <span data-ttu-id="de885-349">1,000</span><span class="sxs-lookup"><span data-stu-id="de885-349">1,000</span></span>    | <span data-ttu-id="de885-350">预测需求期间 1 月 12 日到月底</span><span class="sxs-lookup"><span data-stu-id="de885-350">Forecast requirements period January 12 to end</span></span>                      |

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a><span data-ttu-id="de885-351">创建和设置预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-351">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="de885-352">用于缩减预测需求的 **交易记录 - 缩减参数** 和 **百分比- 缩减参数** 方法中使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-352">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="de885-353">若要创建和设置缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="de885-353">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="de885-354">转到 **主计划 \> 设置 \> 覆盖范围 \> 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="de885-354">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="de885-355">选择 **新建** 创建缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-355">Select **New** to create a reduction key.</span></span>
3. <span data-ttu-id="de885-356">在 **缩减参数** 字段中，输入预测缩减参数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="de885-356">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="de885-357">然后在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="de885-357">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="de885-358">定义期间和每个期间中的缩减参数百分比：</span><span class="sxs-lookup"><span data-stu-id="de885-358">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="de885-359">**生效日期** 字段指示开始创建期间的日期。</span><span class="sxs-lookup"><span data-stu-id="de885-359">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="de885-360">如果 **使用生效日期** 选项设置为 **是**，期间将在生效日期开始。</span><span class="sxs-lookup"><span data-stu-id="de885-360">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="de885-361">如果设置为 **否**，期间将在运行主计划的日期开始。</span><span class="sxs-lookup"><span data-stu-id="de885-361">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="de885-362">定义应进行预测缩减的期间。</span><span class="sxs-lookup"><span data-stu-id="de885-362">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="de885-363">为具体期间指定应缩减预测需求的百分比。</span><span class="sxs-lookup"><span data-stu-id="de885-363">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="de885-364">您可以输入正值以减少需求，或输入负值增加需求。</span><span class="sxs-lookup"><span data-stu-id="de885-364">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a><span data-ttu-id="de885-365">使用一个缩减参数</span><span class="sxs-lookup"><span data-stu-id="de885-365">Use a reduction key</span></span>

<span data-ttu-id="de885-366">必须为物料的覆盖范围组分配预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="de885-366">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="de885-367">若要为物料的覆盖范围组分配缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="de885-367">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="de885-368">转至 **主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="de885-368">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="de885-369">在 **其他** 快速选项卡上的 **缩减参数** 字段中，选择缩减参数分配给覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="de885-369">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="de885-370">缩减参数然后运用于属于该覆盖范围组的所有物料。</span><span class="sxs-lookup"><span data-stu-id="de885-370">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="de885-371">在主计划编制期间，若要使用缩减参数计算预测缩减，必须在设置预测计划或主计划时定义此设置。</span><span class="sxs-lookup"><span data-stu-id="de885-371">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="de885-372">转至以下位置之一：</span><span class="sxs-lookup"><span data-stu-id="de885-372">Go to one of the following locations:</span></span>

    - <span data-ttu-id="de885-373">**主计划 \> 设置 \> 计划 \> 预测计划**</span><span class="sxs-lookup"><span data-stu-id="de885-373">**Master planning \> Setup \> Plans \> Forecast plans**</span></span>
    - <span data-ttu-id="de885-374">**主计划 \> 设置 \> 计划 \> 主计划**</span><span class="sxs-lookup"><span data-stu-id="de885-374">**Master planning \> Setup \> Plans \> Master plans**</span></span>

4. <span data-ttu-id="de885-375">在 **预测计划** 或 **主计划** 页面 **常规** 快速选项卡上的 **用于减少预测需求的方法** 字段中，选择 **百分比 - 缩减参数** 或 **交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="de885-375">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

### <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="de885-376">按交易记录缩减预测</span><span class="sxs-lookup"><span data-stu-id="de885-376">Reduce a forecast by transactions</span></span>

<span data-ttu-id="de885-377">如果用于缩减预测需求的方法选择 **交易记录 - 缩减参数** 或 **交易记录 - 动态期间**，则可指定哪些交易记录缩减预测。</span><span class="sxs-lookup"><span data-stu-id="de885-377">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="de885-378">如果所有交易记录均应缩减预测，请在 **覆盖范围组** 页面 **其他** 快速选项卡上的 **预测减少依据** 字段中选择 **所有交易记录**，如果只有销售订单才应缩减预测，请选择 **订单**。</span><span class="sxs-lookup"><span data-stu-id="de885-378">On the **Coverage groups** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="forecast-models-and-submodels"></a><span data-ttu-id="de885-379">预测模型和子模型</span><span class="sxs-lookup"><span data-stu-id="de885-379">Forecast models and submodels</span></span>

<span data-ttu-id="de885-380">本节介绍如何创建预测模型以及如何通过设置子模型来合并多个预测模型。</span><span class="sxs-lookup"><span data-stu-id="de885-380">This section describes how to create forecast models and how to combine multiple forecast models by setting up submodels.</span></span>

<span data-ttu-id="de885-381">*预测模型* 对特定的预测进行命名和标识。</span><span class="sxs-lookup"><span data-stu-id="de885-381">A *forecast model* names and identifies a specific forecast.</span></span> <span data-ttu-id="de885-382">创建预测模型后，可以向其添加预测行。</span><span class="sxs-lookup"><span data-stu-id="de885-382">After you've created the forecast model, you can add forecast lines to it.</span></span> <span data-ttu-id="de885-383">要为多个物料添加预测行，使用 **需求预测行** 页。</span><span class="sxs-lookup"><span data-stu-id="de885-383">To add forecast lines for multiple items, use the **Demand forecast lines** page.</span></span> <span data-ttu-id="de885-384">要为特定的选定物料添加预测行，使用 **已发布产品** 页。</span><span class="sxs-lookup"><span data-stu-id="de885-384">To add forecast lines for a specific selected item, use the **Released products** page.</span></span>

<span data-ttu-id="de885-385">预测模型可以包括来自其他预测模型的预测。</span><span class="sxs-lookup"><span data-stu-id="de885-385">A forecast model can include forecasts from other forecast models.</span></span> <span data-ttu-id="de885-386">要实现此目的，将其他预测模型添加为父预测模型的 *子模型*。</span><span class="sxs-lookup"><span data-stu-id="de885-386">To achieve this result, you add other forecast models as *submodels* of a parent forecast model.</span></span> <span data-ttu-id="de885-387">必须先创建每个相关模型，然后才能将其添加为父预测模型的子模型。</span><span class="sxs-lookup"><span data-stu-id="de885-387">You must create each relevant model before you can add it as a submodel of a parent forecast model.</span></span>

<span data-ttu-id="de885-388">生成的结构将为您提供一种控制预测的有效方法，因为它让您可以合并（聚合）来自多个预测的输入。</span><span class="sxs-lookup"><span data-stu-id="de885-388">The resulting structure gives you a powerful way to control forecasts, because it lets you combine (aggregate) the input from multiple individual forecasts.</span></span> <span data-ttu-id="de885-389">因此，从计划的角度，很容易合并预测来进行模拟。</span><span class="sxs-lookup"><span data-stu-id="de885-389">Therefore, from a planning point of view, it's easy to combine forecasts for simulations.</span></span> <span data-ttu-id="de885-390">例如，您可以基于定期预测与春季促销预测的组合来设置模拟。</span><span class="sxs-lookup"><span data-stu-id="de885-390">For example, you might set up a simulation that is based on the combination of a regular forecast with the forecast for a spring promotion.</span></span>

### <a name="submodel-levels"></a><span data-ttu-id="de885-391">子模型级别</span><span class="sxs-lookup"><span data-stu-id="de885-391">Submodel levels</span></span>

<span data-ttu-id="de885-392">可以添加到父预测模型的子模型的数量没有限制。</span><span class="sxs-lookup"><span data-stu-id="de885-392">There is no limit on the number of submodels that can be added to a parent forecast model.</span></span> <span data-ttu-id="de885-393">但是，结构只能有一个级别。</span><span class="sxs-lookup"><span data-stu-id="de885-393">However, the structure can be only one level deep.</span></span> <span data-ttu-id="de885-394">换言之，作为另一个预测模型的子模型的预测模型不能有自己的子模型。</span><span class="sxs-lookup"><span data-stu-id="de885-394">In other words, a forecast model that is a submodel of another forecast model can't have its own submodels.</span></span> <span data-ttu-id="de885-395">将子模型添加到预测模型时，系统会检查该预测模型是否已经是另一个预测模型的子模型。</span><span class="sxs-lookup"><span data-stu-id="de885-395">When you add submodels to a forecast model, the system checks whether that forecast model is already a submodel of another forecast model.</span></span>

<span data-ttu-id="de885-396">如果主计划遇到有自己的子模型的子模型，您会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="de885-396">If master planning encounters a submodel that has its own submodels, you receive an error message.</span></span>

#### <a name="submodel-levels-example"></a><span data-ttu-id="de885-397">子模型级别示例</span><span class="sxs-lookup"><span data-stu-id="de885-397">Submodel levels example</span></span>

<span data-ttu-id="de885-398">预测模型 A 有子模型预测模型 B。</span><span class="sxs-lookup"><span data-stu-id="de885-398">Forecast model A has forecast model B as a submodel.</span></span> <span data-ttu-id="de885-399">因此，预测模型 B 不能有自己的子模型。</span><span class="sxs-lookup"><span data-stu-id="de885-399">Therefore, forecast model B can't have its own submodels.</span></span> <span data-ttu-id="de885-400">如果您尝试将子模型添加到预测模型 B，会收到以下错误消息：“预测模型 B 是模型 A 的子模型。”</span><span class="sxs-lookup"><span data-stu-id="de885-400">If you try to add a submodel to forecast model B, you receive the following error message: "Forecast model B is a submodel for model A."</span></span>

### <a name="aggregating-forecasts-across-forecast-models"></a><span data-ttu-id="de885-401">跨预测模型聚合预测</span><span class="sxs-lookup"><span data-stu-id="de885-401">Aggregating forecasts across forecast models</span></span>

<span data-ttu-id="de885-402">在同一天发生的预测行将跨其预测模型及其子模型聚合。</span><span class="sxs-lookup"><span data-stu-id="de885-402">Forecast lines that occur on the same day will be aggregated across their forecast model and its submodels.</span></span>

#### <a name="aggregation-example"></a><span data-ttu-id="de885-403">聚合示例</span><span class="sxs-lookup"><span data-stu-id="de885-403">Aggregation example</span></span>

<span data-ttu-id="de885-404">预测模型 A 有预测模型 B 和 C 两个子模型。</span><span class="sxs-lookup"><span data-stu-id="de885-404">Forecast model A has forecast models B and C as submodels.</span></span>

- <span data-ttu-id="de885-405">预测模型 A 包括 6 月 15 日 2 件 (pcs) 的需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-405">Forecast model A includes a demand forecast for 2 pieces (pcs) on June 15.</span></span>
- <span data-ttu-id="de885-406">预测模型 B 包括 6 月 15 日 3 pcs 的需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-406">Forecast model B includes a demand forecast for 3 pcs on June 15.</span></span>
- <span data-ttu-id="de885-407">预测模型 C 包括 6 月 15 日 4 pcs 的需求预测。</span><span class="sxs-lookup"><span data-stu-id="de885-407">Forecast model C includes a demand forecast for 4 pcs on June 15.</span></span>

<span data-ttu-id="de885-408">生成的需求预测将是 6 月 15 日 9 pcs (2 + 3 + 4) 的一个需求。</span><span class="sxs-lookup"><span data-stu-id="de885-408">The resulting demand forecast will be a single demand for 9 pcs (2 + 3 + 4) on June 15.</span></span>

> [!NOTE]
> <span data-ttu-id="de885-409">每个子模型使用自己的参数，而不是父预测模型的参数。</span><span class="sxs-lookup"><span data-stu-id="de885-409">Each submodel uses its own parameters, not the parameters of the parent forecast model.</span></span>

### <a name="create-a-forecast-model"></a><span data-ttu-id="de885-410">创建预测模型</span><span class="sxs-lookup"><span data-stu-id="de885-410">Create a forecast model</span></span>

<span data-ttu-id="de885-411">若要创建预测模型，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="de885-411">To create a forecast model, follow these steps.</span></span>

1. <span data-ttu-id="de885-412">转到 **主计划 \> 设置 \> 需求预测 \> 预测模型**。</span><span class="sxs-lookup"><span data-stu-id="de885-412">Go to **Master planning \> Setup \> Demand forecasting \> Forecast models**.</span></span>
1. <span data-ttu-id="de885-413">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="de885-413">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="de885-414">为新的预测模型设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="de885-414">Set the following fields for the new forecast model:</span></span>

    - <span data-ttu-id="de885-415">**模型** – 为模型输入唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="de885-415">**Model** – Enter a unique identifier for the model.</span></span>
    - <span data-ttu-id="de885-416">**名称** – 为模型输入描述性名称。</span><span class="sxs-lookup"><span data-stu-id="de885-416">**Name** – Enter a descriptive name for the model.</span></span>
    - <span data-ttu-id="de885-417">**已停止** – 通常，您应将此选项设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="de885-417">**Stopped** – Usually, you should set this option to *No*.</span></span> <span data-ttu-id="de885-418">仅当要阻止编辑分配到模型的所有预测行时再将其设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="de885-418">Set it to *Yes* only if you want to prevent editing of all forecast lines that are assigned to the model.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de885-419">**包括在现金流量预测中** 字段和 **项目** 快速选项卡上的字段不会与主计划关联。</span><span class="sxs-lookup"><span data-stu-id="de885-419">The **Include in cash flow forecasts** field and the fields on the **Project** FastTab aren't related to master planning.</span></span> <span data-ttu-id="de885-420">因此，您可以在此上下文中忽略它们。</span><span class="sxs-lookup"><span data-stu-id="de885-420">Therefore, you can ignore them in this context.</span></span> <span data-ttu-id="de885-421">仅在使用 **项目管理和会计** 模块的预测时，才必须考虑它们。</span><span class="sxs-lookup"><span data-stu-id="de885-421">You must consider them only when you work with forecasts for the **Project management and accounting** module.</span></span>

### <a name="assign-submodels-to-a-forecast-model"></a><span data-ttu-id="de885-422">将子模型分配到预测模型</span><span class="sxs-lookup"><span data-stu-id="de885-422">Assign submodels to a forecast model</span></span>

<span data-ttu-id="de885-423">要将子模型分配到预测模型，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="de885-423">To assign submodels to a forecast model, follow these steps.</span></span>

1. <span data-ttu-id="de885-424">转到 **库存管理 \> 设置 \> 预测 \> 预测模型**。</span><span class="sxs-lookup"><span data-stu-id="de885-424">Go to **Inventory management \> Setup \> Forecast \> Forecast models**.</span></span>
1. <span data-ttu-id="de885-425">在列表窗格中，选择要为其设置子模型的预测模型。</span><span class="sxs-lookup"><span data-stu-id="de885-425">In the list pane, select the forecast model to set up a submodel for.</span></span>
1. <span data-ttu-id="de885-426">在 **子模型** 快速选项卡上，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="de885-426">On the **Submodel** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="de885-427">在新行中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="de885-427">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="de885-428">**子模型** – 选择要添加为子模型的预测模型。</span><span class="sxs-lookup"><span data-stu-id="de885-428">**Submodel** – Select the forecast model to add as a submodel.</span></span> <span data-ttu-id="de885-429">此预测模型必须已经存在，并且不能有自己的任何子模型。</span><span class="sxs-lookup"><span data-stu-id="de885-429">This forecast model must already exist, and it must not have any submodels of its own.</span></span>
    - <span data-ttu-id="de885-430">**名称** – 为子模型输入描述性名称。</span><span class="sxs-lookup"><span data-stu-id="de885-430">**Name** – Enter a descriptive name for the submodel.</span></span> <span data-ttu-id="de885-431">例如，此名称可以指示子模型与父预测模型的关系。</span><span class="sxs-lookup"><span data-stu-id="de885-431">For example, this name might indicate the submodel's relation to the parent forecast model.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

