---
title: 生成统计基准预测
description: 本文提供有关用于需求预测计算的参数和筛选器的信息。
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f2ccb8c0b4d7c4755e0b8dc66539e165265090
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "326415"
---
# <a name="generate-a-statistical-baseline-forecast"></a><span data-ttu-id="53b1c-103">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="53b1c-103">Generate a statistical baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53b1c-104">本文提供有关用于需求预测计算的参数和筛选器的信息。</span><span class="sxs-lookup"><span data-stu-id="53b1c-104">This article provides information about the parameters and filters that are used in the calculation of demand forecasting.</span></span> 

<span data-ttu-id="53b1c-105">在您创建基准预测时，必须首先指定在计算中使用的参数和筛选器。</span><span class="sxs-lookup"><span data-stu-id="53b1c-105">When you create a baseline forecast, you must first specify the parameters and filters that are used in the calculation.</span></span> <span data-ttu-id="53b1c-106">例如，您可以创建基于指定公司和所选物料组去年、下个月的交易数据来估计需求的基准预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-106">For example, you can create a baseline forecast that estimates demand based on transaction data from the past year for a specific company, for the coming month, and for a selected group of items.</span></span> 

<span data-ttu-id="53b1c-107">若要生成需求预测，转到**主计划 &gt; 预测 &gt; 需求预测 &gt; 生成统计基线预测**。</span><span class="sxs-lookup"><span data-stu-id="53b1c-107">To generate a demand forecast, go to **Master planning &gt; Forecasting &gt; Demand forecasting &gt; Generate statistical baseline forecast**.</span></span> 

<span data-ttu-id="53b1c-108">预测时段可以在预测生成时选择。</span><span class="sxs-lookup"><span data-stu-id="53b1c-108">The forecast bucket can be selected at forecast generation time.</span></span> <span data-ttu-id="53b1c-109">可用值：天、周和月。</span><span class="sxs-lookup"><span data-stu-id="53b1c-109">The available values are: Day, Week, and Month.</span></span> 

<span data-ttu-id="53b1c-110">要为其生成预测的时段的数目在**预测区间**字段中设置。</span><span class="sxs-lookup"><span data-stu-id="53b1c-110">The number of buckets to generate a forecast for is set in the **Forecast horizon** field.</span></span> 

<span data-ttu-id="53b1c-111">在将预测策略设置为**复制历史需求**时，忽略历史区间的结束。</span><span class="sxs-lookup"><span data-stu-id="53b1c-111">When the forecast strategy is set to **Copy over historical demand**, the end of the historical horizon is ignored.</span></span> <span data-ttu-id="53b1c-112">此系统将在**预测区间**字段中指定的时段的数量复制到预测需求，从在**历史区间**下的**开始日期**字段中设置的日期开始。</span><span class="sxs-lookup"><span data-stu-id="53b1c-112">The system copies the number of buckets specified in the **Forecast horizon** field to the forecast demand, starting from the date set in the **From date** field under **Historical horizon**.</span></span> <span data-ttu-id="53b1c-113">通过复制某一日期前推的历史需求，生产计划人员可以通过两种方式为下一个季度制定计划：</span><span class="sxs-lookup"><span data-stu-id="53b1c-113">By copying historical demand from a certain date forward, production planners can make the plan for the next quarter in two ways:</span></span>

-   <span data-ttu-id="53b1c-114">通过复制去年相同季度的需求。</span><span class="sxs-lookup"><span data-stu-id="53b1c-114">By copying the demand from the same quarter last year.</span></span>
-   <span data-ttu-id="53b1c-115">通过复制上一个季度的需求。</span><span class="sxs-lookup"><span data-stu-id="53b1c-115">By copying the demand from the previous quarter.</span></span>

<span data-ttu-id="53b1c-116">为了避免生产计划的混淆，特定预测时段数目可以锁定。</span><span class="sxs-lookup"><span data-stu-id="53b1c-116">To prevent confusion in the production plans, a certain number of forecast buckets can be frozen.</span></span> <span data-ttu-id="53b1c-117">此数目在字段**锁定时限**中设置。</span><span class="sxs-lookup"><span data-stu-id="53b1c-117">This number is set in the **Freeze time fence** field.</span></span> <span data-ttu-id="53b1c-118">在**调整后的需求预测**页上，锁定时段的单元格将禁用，以给予不应更改的那些值以直观显示。</span><span class="sxs-lookup"><span data-stu-id="53b1c-118">On the **Adjusted demand forecast** page, the cells for the frozen buckets are disabled, to give a visual indication that those values should not be changed.</span></span> 

<span data-ttu-id="53b1c-119">基准需求预测的开始日期不必为当前日期或未来日期。</span><span class="sxs-lookup"><span data-stu-id="53b1c-119">The start date for the baseline demand forecast doesn’t have to be the current date or a date in the future.</span></span> <span data-ttu-id="53b1c-120">若要设置不同的开始日期，请使用**基准预测开始日期 - 开始日期**字段。</span><span class="sxs-lookup"><span data-stu-id="53b1c-120">To set a different start date, use the **Baseline forecast start date - From date** field.</span></span> <span data-ttu-id="53b1c-121">例如，在六月，用户可以生成明年的预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-121">For example, in June, users can generate a forecast for the next year.</span></span> <span data-ttu-id="53b1c-122">由于历史需求的结束和基准的开始之间的预测时段缺少，预测可能不准确。</span><span class="sxs-lookup"><span data-stu-id="53b1c-122">Because the forecast buckets between the end of historical demand and the start of the baseline are missing, the predictions might not be accurate.</span></span> <span data-ttu-id="53b1c-123">如果您使用 Microsoft Dynamics 365 for Finance and Operations 需求预测服务，您可以有四种方法填补缺失。</span><span class="sxs-lookup"><span data-stu-id="53b1c-123">If you are using the Microsoft Dynamics 365 for Finance and Operations Demand forecasting service, there are four ways in which you can fill in the missing gaps.</span></span> <span data-ttu-id="53b1c-124">您可以通过在**需求预测参数**页上设置 MISSING\_VALUE\_SUBSTITUTION 参数来选择需要的方法。</span><span class="sxs-lookup"><span data-stu-id="53b1c-124">You can choose the method that you want by setting the MISSING\_VALUE\_SUBSTITUTION parameter on the **Demand forecasting parameters** page.</span></span> 

<span data-ttu-id="53b1c-125">**基准预测开始日期**  -  **开始日期**字段必须设置为预测时段的开始，例如，在美国，如果预测时段是周则为星期日。</span><span class="sxs-lookup"><span data-stu-id="53b1c-125">The **Baseline forecast start date** - **From date** field has to be set to the beginning of a forecast bucket, for example, in the United States, a Sunday if the forecasting bucket is the week.</span></span> <span data-ttu-id="53b1c-126">此系统自动调整**基准预测开始日期**  -  **开始日期**字段为与预测时段的开始匹配。</span><span class="sxs-lookup"><span data-stu-id="53b1c-126">The system automatically adjusts the **Baseline forecast start date** - **From date** field to match the beginning of a forecast bucket.</span></span> 

<span data-ttu-id="53b1c-127">**基准预测开始日期**  -  **开始日期**字段可以设置为过去的日期。</span><span class="sxs-lookup"><span data-stu-id="53b1c-127">The **Baseline forecast start date** - **From date** field can be set to a date in in the past.</span></span> <span data-ttu-id="53b1c-128">换言之，可以生成过去的需求预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-128">In other words, it is possible to generate a demand forecast in the past.</span></span> <span data-ttu-id="53b1c-129">这很有用，因为它允许用户调整预测服务参数，以便过去生成的统计预测与实际历史需求匹配。</span><span class="sxs-lookup"><span data-stu-id="53b1c-129">This is useful, because it lets users tweak the forecast service parameters so that the statistical forecast generated in the past matches the actual historical demand.</span></span> <span data-ttu-id="53b1c-130">用户然后可以继续使用这些参数设置来生成将来的统计基准预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-130">Users can then continue using these parameter settings to generate a statistical baseline forecast for the future.</span></span> 

<span data-ttu-id="53b1c-131">如果选中**转移对需求预测进行的手动调整**复选框，在以前需求预测迭代进行的手动调整可以自动应用于新的基准预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-131">Manual adjustments made in previous demand forecasting iterations can be automatically applied to the new baseline forecast if the **Transfer manual adjustments to the demand forecas**t check box is selected.</span></span> <span data-ttu-id="53b1c-132">如果清除此复选框，手动调整不添加到基准预测 – 但它们不删除。</span><span class="sxs-lookup"><span data-stu-id="53b1c-132">If the check box is cleared, the manual adjustments are not added to the baseline forecast – but they are not deleted.</span></span> <span data-ttu-id="53b1c-133">对预测进行的手动调整只能在预测导入时删除，方法是通过清除**保存对基准需求预测进行的手动调整**复选框。</span><span class="sxs-lookup"><span data-stu-id="53b1c-133">Manual adjustments made to a forecast can be deleted only at forecast import time, by clearing the **Save the manual adjustments made to the baseline demand forecast** check box.</span></span> <span data-ttu-id="53b1c-134">手动调整在授权时保存。</span><span class="sxs-lookup"><span data-stu-id="53b1c-134">Manual adjustments are saved at authorization time.</span></span> <span data-ttu-id="53b1c-135">因此，如果用户对预测进行手动调整，但不授权预测返回 Finance and Operations，则更改将丢失。</span><span class="sxs-lookup"><span data-stu-id="53b1c-135">Therefore, if a user makes manual adjustments to the forecast, but doesn’t authorize the forecast back to Finance and Operations, the changes are lost.</span></span> <span data-ttu-id="53b1c-136">有关手动调整以及它们的工作方式的详细信息，请参阅[授权已调整的预测](authorize-adjusted-forecast.md)。</span><span class="sxs-lookup"><span data-stu-id="53b1c-136">For more information about manual adjustments and how they work, see [Authorizing the adjusted forecast](authorize-adjusted-forecast.md).</span></span> 

<span data-ttu-id="53b1c-137">需求预测生成可以有名称和注释以帮助用户确定已生成的预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-137">A demand forecast generation can have a name and comments to help users identify the forecast that has been generated.</span></span> <span data-ttu-id="53b1c-138">这些值在**统计基准预测生成历史记录**页的预测生成历史记录中可见。</span><span class="sxs-lookup"><span data-stu-id="53b1c-138">These values are visible in forecast generation history on the **Statistical baseline forecast generation history** page.</span></span> 

<span data-ttu-id="53b1c-139">内部公司计划组、物料分配参数和其他筛选器可以在预测生成时应用。</span><span class="sxs-lookup"><span data-stu-id="53b1c-139">The intercompany planning group, item allocation keys, and other filters can be applied at forecast generation time.</span></span> <span data-ttu-id="53b1c-140">它们可用于提高绩效或将数据拆分为可管理的区块。</span><span class="sxs-lookup"><span data-stu-id="53b1c-140">These can be used to improve performance or to split the data into manageable chunks.</span></span> <span data-ttu-id="53b1c-141">不过，请注意，需求预测没有为不与内部公司计划组关联的任何物料分配参数的成员生成，即使物料分配参数在查询中选择。</span><span class="sxs-lookup"><span data-stu-id="53b1c-141">However, note that a demand forecast is not generated for the members of any item allocation key that is not associated with an intercompany planning group, even if the item allocation key is selected in the query.</span></span> 

<span data-ttu-id="53b1c-142">**提示**：在某些情况下，在生成需求预测时，用户可能会收到错误消息，或预测生成在没有会话日志的情况下完成。</span><span class="sxs-lookup"><span data-stu-id="53b1c-142">**Tip**: Sometimes users might receive errors while generating a demand forecast, or forecast generation is completed with no session log.</span></span> <span data-ttu-id="53b1c-143">这可能由于之前用于预测生成的查询中的残余数据而发生。</span><span class="sxs-lookup"><span data-stu-id="53b1c-143">This can happen because of leftover data in the query that was previously used for forecast generation.</span></span> <span data-ttu-id="53b1c-144">为了修复此问题，单击**选择**打开**查询**页，单击**重置**，然后重新生成基准预测。</span><span class="sxs-lookup"><span data-stu-id="53b1c-144">To fix this issue, click **Select** to open the **Query** page, click **Reset**, and then regenerate the baseline forecast.</span></span> 

<span data-ttu-id="53b1c-145">如果没有为大物料组生成预测，但是，例如，一次为一个物料或一个物料分配参数生成，那么为了达到更好的效果，您可以选中**主计划 - 设置 - 需求预测**  -  **需求预测参数 - Azure 机器学习**选项卡上的**使用请求响应模式**复选框。</span><span class="sxs-lookup"><span data-stu-id="53b1c-145">If the forecast is not generated for a big set of items, but, for example, for one item or one item allocation key at a time, then in order to get better performance, you can select the **Use request response mode** check box on the **Master planning - Setup - Demand forecasting** - **Demand forecasting parameters - Azure Machine Learning** tab.</span></span>

<a name="additional-resources"></a><span data-ttu-id="53b1c-146">其他资源</span><span class="sxs-lookup"><span data-stu-id="53b1c-146">Additional resources</span></span>
--------

[<span data-ttu-id="53b1c-147">需求预测设置</span><span class="sxs-lookup"><span data-stu-id="53b1c-147">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

[<span data-ttu-id="53b1c-148">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="53b1c-148">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="53b1c-149">授权调整后的需求预测</span><span class="sxs-lookup"><span data-stu-id="53b1c-149">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)



