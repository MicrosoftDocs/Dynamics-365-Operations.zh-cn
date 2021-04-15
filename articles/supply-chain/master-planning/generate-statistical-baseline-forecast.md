---
title: 生成统计基准预测
description: 此主题提供有关用于需求预测计算的参数和筛选器的信息。
author: roxanadiaconu
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 562cf07348e77d9c2f169e31a852843bea10fcc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816500"
---
# <a name="generate-a-statistical-baseline-forecast"></a><span data-ttu-id="15515-103">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="15515-103">Generate a statistical baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15515-104">此主题提供有关用于需求预测计算的参数和筛选器的信息。</span><span class="sxs-lookup"><span data-stu-id="15515-104">This topic provides information about the parameters and filters that are used in the calculation of demand forecasting.</span></span> 

<span data-ttu-id="15515-105">在您创建基准预测时，必须首先指定在计算中使用的参数和筛选器。</span><span class="sxs-lookup"><span data-stu-id="15515-105">When you create a baseline forecast, you must first specify the parameters and filters that are used in the calculation.</span></span> <span data-ttu-id="15515-106">例如，您可以创建基于指定公司和所选物料组去年、下个月的交易数据来估计需求的基准预测。</span><span class="sxs-lookup"><span data-stu-id="15515-106">For example, you can create a baseline forecast that estimates demand based on transaction data from the past year for a specific company, for the coming month, and for a selected group of items.</span></span> 

<span data-ttu-id="15515-107">若要生成需求预测，转到 **主计划 &gt; 预测 &gt; 需求预测 &gt; 生成统计基线预测**。</span><span class="sxs-lookup"><span data-stu-id="15515-107">To generate a demand forecast, go to **Master planning &gt; Forecasting &gt; Demand forecasting &gt; Generate statistical baseline forecast**.</span></span> 

<span data-ttu-id="15515-108">预测时段可以在预测生成时选择。</span><span class="sxs-lookup"><span data-stu-id="15515-108">The forecast bucket can be selected at forecast generation time.</span></span> <span data-ttu-id="15515-109">可用值：天、周和月。</span><span class="sxs-lookup"><span data-stu-id="15515-109">The available values are: Day, Week, and Month.</span></span> 

<span data-ttu-id="15515-110">要为其生成预测的时段的数目在 **预测区间** 字段中设置。</span><span class="sxs-lookup"><span data-stu-id="15515-110">The number of buckets to generate a forecast for is set in the **Forecast horizon** field.</span></span> 

<span data-ttu-id="15515-111">在将预测策略设置为 **复制历史需求** 时，忽略历史区间的结束。</span><span class="sxs-lookup"><span data-stu-id="15515-111">When the forecast strategy is set to **Copy over historical demand**, the end of the historical horizon is ignored.</span></span> <span data-ttu-id="15515-112">此系统将在 **预测区间** 字段中指定的时段的数量复制到预测需求，从在 **历史区间** 下的 **开始日期** 字段中设置的日期开始。</span><span class="sxs-lookup"><span data-stu-id="15515-112">The system copies the number of buckets specified in the **Forecast horizon** field to the forecast demand, starting from the date set in the **From date** field under **Historical horizon**.</span></span> <span data-ttu-id="15515-113">通过复制某一日期前推的历史需求，生产计划人员可以通过两种方式为下一个季度制定计划：</span><span class="sxs-lookup"><span data-stu-id="15515-113">By copying historical demand from a certain date forward, production planners can make the plan for the next quarter in two ways:</span></span>

-   <span data-ttu-id="15515-114">通过复制去年相同季度的需求。</span><span class="sxs-lookup"><span data-stu-id="15515-114">By copying the demand from the same quarter last year.</span></span>
-   <span data-ttu-id="15515-115">通过复制上一个季度的需求。</span><span class="sxs-lookup"><span data-stu-id="15515-115">By copying the demand from the previous quarter.</span></span>

<span data-ttu-id="15515-116">为了避免生产计划的混淆，特定预测时段数目可以锁定。</span><span class="sxs-lookup"><span data-stu-id="15515-116">To prevent confusion in the production plans, a certain number of forecast buckets can be frozen.</span></span> <span data-ttu-id="15515-117">此数目在字段 **锁定时限** 中设置。</span><span class="sxs-lookup"><span data-stu-id="15515-117">This number is set in the **Freeze time fence** field.</span></span> <span data-ttu-id="15515-118">在 **调整后的需求预测** 页上，锁定时段的单元格将禁用，以给予不应更改的那些值以直观显示。</span><span class="sxs-lookup"><span data-stu-id="15515-118">On the **Adjusted demand forecast** page, the cells for the frozen buckets are disabled, to give a visual indication that those values should not be changed.</span></span> 

<span data-ttu-id="15515-119">基准需求预测的开始日期不必为当前日期或未来日期。</span><span class="sxs-lookup"><span data-stu-id="15515-119">The start date for the baseline demand forecast doesn’t have to be the current date or a date in the future.</span></span> <span data-ttu-id="15515-120">若要设置不同的开始日期，请使用 **基准预测开始日期 - 开始日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="15515-120">To set a different start date, use the **Baseline forecast start date - From date** field.</span></span> <span data-ttu-id="15515-121">例如，在六月，用户可以生成明年的预测。</span><span class="sxs-lookup"><span data-stu-id="15515-121">For example, in June, users can generate a forecast for the next year.</span></span> <span data-ttu-id="15515-122">由于历史需求的结束和基准的开始之间的预测时段缺少，预测可能不准确。</span><span class="sxs-lookup"><span data-stu-id="15515-122">Because the forecast buckets between the end of historical demand and the start of the baseline are missing, the predictions might not be accurate.</span></span> <span data-ttu-id="15515-123">如果您使用需求预测服务，您可以有四种方法填补缺失。</span><span class="sxs-lookup"><span data-stu-id="15515-123">If you are using the Demand forecasting service, there are four ways in which you can fill in the missing gaps.</span></span> <span data-ttu-id="15515-124">您可以通过在 **需求预测参数** 页上设置 MISSING\_VALUE\_SUBSTITUTION 参数来选择需要的方法。</span><span class="sxs-lookup"><span data-stu-id="15515-124">You can choose the method that you want by setting the MISSING\_VALUE\_SUBSTITUTION parameter on the **Demand forecasting parameters** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="15515-125">只有历史数据开始日期与结束日期之间的数据之差才支持替换缺少值。</span><span class="sxs-lookup"><span data-stu-id="15515-125">Missing value substitution only works for the gaps in data in between the start and end dates for historical data.</span></span> <span data-ttu-id="15515-126">不会在最后一个物理数据点之前或之后填充数据，而是仅充当实际现有数据点之间的外延。</span><span class="sxs-lookup"><span data-stu-id="15515-126">It will not fill in data before or after the last physical data point, it only acts as extrapolation between actual existing data points.</span></span> 

<span data-ttu-id="15515-127">**基准预测开始日期**  -  **开始日期** 字段必须设置为预测时段的开始，例如，在美国，如果预测时段是周则为星期日。</span><span class="sxs-lookup"><span data-stu-id="15515-127">The **Baseline forecast start date** - **From date** field has to be set to the beginning of a forecast bucket, for example, in the United States, a Sunday if the forecasting bucket is the week.</span></span> <span data-ttu-id="15515-128">此系统自动调整 **基准预测开始日期**  -  **开始日期** 字段为与预测时段的开始匹配。</span><span class="sxs-lookup"><span data-stu-id="15515-128">The system automatically adjusts the **Baseline forecast start date** - **From date** field to match the beginning of a forecast bucket.</span></span> 

<span data-ttu-id="15515-129">**基准预测开始日期**  -  **开始日期** 字段可以设置为过去的日期。</span><span class="sxs-lookup"><span data-stu-id="15515-129">The **Baseline forecast start date** - **From date** field can be set to a date in in the past.</span></span> <span data-ttu-id="15515-130">换言之，可以生成过去的需求预测。</span><span class="sxs-lookup"><span data-stu-id="15515-130">In other words, it is possible to generate a demand forecast in the past.</span></span> <span data-ttu-id="15515-131">这很有用，因为它允许用户调整预测服务参数，以便过去生成的统计预测与实际历史需求匹配。</span><span class="sxs-lookup"><span data-stu-id="15515-131">This is useful, because it lets users adjust the forecast service parameters so that the statistical forecast generated in the past matches the actual historical demand.</span></span> <span data-ttu-id="15515-132">用户然后可以继续使用这些参数设置来生成将来的统计基准预测。</span><span class="sxs-lookup"><span data-stu-id="15515-132">Users can then continue using these parameter settings to generate a statistical baseline forecast for the future.</span></span> 

<span data-ttu-id="15515-133">如果选中 **转移对需求预测进行的手动调整** 复选框，在以前需求预测迭代进行的手动调整可以自动应用于新的基准预测。</span><span class="sxs-lookup"><span data-stu-id="15515-133">Manual adjustments made in previous demand forecasting iterations can be automatically applied to the new baseline forecast if the **Transfer manual adjustments to the demand forecas** t check box is selected.</span></span> <span data-ttu-id="15515-134">如果清除此复选框，手动调整不添加到基准预测 – 但它们不删除。</span><span class="sxs-lookup"><span data-stu-id="15515-134">If the check box is cleared, the manual adjustments are not added to the baseline forecast – but they are not deleted.</span></span> <span data-ttu-id="15515-135">对预测进行的手动调整只能在预测导入时删除，方法是通过清除 **保存对基准需求预测进行的手动调整** 复选框。</span><span class="sxs-lookup"><span data-stu-id="15515-135">Manual adjustments made to a forecast can be deleted only at forecast import time, by clearing the **Save the manual adjustments made to the baseline demand forecast** check box.</span></span> <span data-ttu-id="15515-136">手动调整在授权时保存。</span><span class="sxs-lookup"><span data-stu-id="15515-136">Manual adjustments are saved at authorization time.</span></span> <span data-ttu-id="15515-137">因此，如果用户对预测进行手动调整，但不授权预测返回 Supply Chain Management，则更改将丢失。</span><span class="sxs-lookup"><span data-stu-id="15515-137">Therefore, if a user makes manual adjustments to the forecast, but doesn’t authorize the forecast back to Supply Chain Management, the changes are lost.</span></span> <span data-ttu-id="15515-138">有关手动调整以及它们的工作方式的详细信息，请参阅[授权已调整的预测](authorize-adjusted-forecast.md)。</span><span class="sxs-lookup"><span data-stu-id="15515-138">For more information about manual adjustments and how they work, see [Authorize an adjusted forecast](authorize-adjusted-forecast.md).</span></span> 

<span data-ttu-id="15515-139">需求预测生成可以有名称和注释以帮助用户确定已生成的预测。</span><span class="sxs-lookup"><span data-stu-id="15515-139">A demand forecast generation can have a name and comments to help users identify the forecast that has been generated.</span></span> <span data-ttu-id="15515-140">这些值在 **统计基准预测生成历史记录** 页的预测生成历史记录中可见。</span><span class="sxs-lookup"><span data-stu-id="15515-140">These values are visible in forecast generation history on the **Statistical baseline forecast generation history** page.</span></span> 

<span data-ttu-id="15515-141">内部公司计划组、物料分配参数和其他筛选器可以在预测生成时应用。</span><span class="sxs-lookup"><span data-stu-id="15515-141">The intercompany planning group, item allocation keys, and other filters can be applied at forecast generation time.</span></span> <span data-ttu-id="15515-142">它们可用于提高绩效或将数据拆分为可管理的区块。</span><span class="sxs-lookup"><span data-stu-id="15515-142">These can be used to improve performance or to split the data into manageable chunks.</span></span> <span data-ttu-id="15515-143">不过，请注意，需求预测没有为不与内部公司计划组关联的任何物料分配参数的成员生成，即使物料分配参数在查询中选择。</span><span class="sxs-lookup"><span data-stu-id="15515-143">However, note that a demand forecast is not generated for the members of any item allocation key that is not associated with an intercompany planning group, even if the item allocation key is selected in the query.</span></span> 

> [!TIP]
> <span data-ttu-id="15515-144">在某些情况下，在生成需求预测时，用户可能会收到错误消息，或预测生成在没有会话日志的情况下完成。</span><span class="sxs-lookup"><span data-stu-id="15515-144">Sometimes users might receive errors while generating a demand forecast, or forecast generation is completed with no session log.</span></span> <span data-ttu-id="15515-145">这可能由于之前用于预测生成的查询中的残余数据而发生。</span><span class="sxs-lookup"><span data-stu-id="15515-145">This can happen because of leftover data in the query that was previously used for forecast generation.</span></span> <span data-ttu-id="15515-146">为了解决此问题，单击 **选择** 打开 **查询** 页，选择 **重置**，然后重新生成基准预测。</span><span class="sxs-lookup"><span data-stu-id="15515-146">To resolve this issue, click **Select** to open the **Query** page, select **Reset**, and then regenerate the baseline forecast.</span></span> 

<span data-ttu-id="15515-147">如果没有为大物料组生成预测，但是，例如，一次为一个物料或一个物料分配参数生成，那么为了达到更好的效果，您可以选中 **主计划 - 设置 - 需求预测**  -  **需求预测参数 - Azure 机器学习** 选项卡上的 **使用请求响应模式** 复选框。</span><span class="sxs-lookup"><span data-stu-id="15515-147">If the forecast is not generated for a big set of items, but, for example, for one item or one item allocation key at a time, then in order to get better performance, you can select the **Use request response mode** check box on the **Master planning - Setup - Demand forecasting** - **Demand forecasting parameters - Azure Machine Learning** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="15515-148">看起来可能平稳的预测可能是较长历史时间范围（最少 3 个时间段以选出模式，如 3 年的月预测）的历史数据的结果。</span><span class="sxs-lookup"><span data-stu-id="15515-148">A potentially flat looking forecast can be due to the historical data that has to be of a longer historical timeframe (a minimum 3 of time periods in order to pick out patterns, such as 3 years with monthly forecast).</span></span> <span data-ttu-id="15515-149">若要获取更好的结果，可以尝试更改时间范围的粒度或扩大时间范围。</span><span class="sxs-lookup"><span data-stu-id="15515-149">To get a better result, you can try changing the granularity of the time range or increase the time range.</span></span>

<a name="additional-resources"></a><span data-ttu-id="15515-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="15515-150">Additional resources</span></span>
--------

- [<span data-ttu-id="15515-151">需求预测设置</span><span class="sxs-lookup"><span data-stu-id="15515-151">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

- [<span data-ttu-id="15515-152">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="15515-152">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

- [<span data-ttu-id="15515-153">授权调整后的预测</span><span class="sxs-lookup"><span data-stu-id="15515-153">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]