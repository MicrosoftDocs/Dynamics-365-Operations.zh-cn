--- 
title: "生成和处理客户返点"
description: "该过程会说明如何处理从要求生成到将它们作为应计项目过帐到“应收帐款”的客户返利。"
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 348793abc6d219f38bcdc2629b77343d93927005
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="generate-and-process-customer-rebates"></a><span data-ttu-id="ae96d-103">生成和处理客户返点</span><span class="sxs-lookup"><span data-stu-id="ae96d-103">Generate and process customer rebates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae96d-104">该过程会说明如何处理从要求生成到将它们作为应计项目过帐到“应收帐款”的客户返利。</span><span class="sxs-lookup"><span data-stu-id="ae96d-104">This procedure demonstrates how to process customer rebates from claim generation to the point of passing them as accruals to Accounts receivable.</span></span> <span data-ttu-id="ae96d-105">它会从头至尾引导您完成特定示例，以解释返利行的各种条件如何对将被记入客户帐上的最终金额产生影响。</span><span class="sxs-lookup"><span data-stu-id="ae96d-105">It walks you through a specific example to explain how the various conditions on the rebate lines affect the final amounts that will be credited to the customer.</span></span> <span data-ttu-id="ae96d-106">在开始该指南之前，您需要使用 USMF 公司演示数据，并完成以下任务：(1) 转至“应收帐款参数”页面，并先后展开“价格”选项卡和“价格详情”选项卡，然后检查“启用价格详情”选项是否被设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-106">You need to use the USMF demo data company, and carry out the following tasks before you start the guide: (1) Go to the Accounts receivable parameters page, and expand the Prices tab and then the Price details tab, and check that the Enable price details option is set to Yes.</span></span> <span data-ttu-id="ae96d-107">(2) 转至“返利协议”页面，并选择客户返利协议：USMF-000001.</span><span class="sxs-lookup"><span data-stu-id="ae96d-107">(2) Go to the Rebate agreements page and select the customer rebate agreement: USMF-000001.</span></span> <span data-ttu-id="ae96d-108">如果“工作流审核状态”字段未被设置为“已审核”，您需要单击“操作窗格”上的“验证”，以批准该工作流程。</span><span class="sxs-lookup"><span data-stu-id="ae96d-108">If the Workflow approval status field is not set to Approved, you need click Validation on the Action pane to approve it.</span></span>


## <a name="review-a-customer-rebate-agreement"></a><span data-ttu-id="ae96d-109">审查客户返点协议</span><span class="sxs-lookup"><span data-stu-id="ae96d-109">Review a customer rebate agreement</span></span>
1. <span data-ttu-id="ae96d-110">转至“销售和营销”>“客户返利”>“返利协议”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-110">Go to Sales and marketing > Customer rebates > Rebate agreements.</span></span>
    * <span data-ttu-id="ae96d-111">以下若干步骤用于查看协议 USMF-000001 的条件，</span><span class="sxs-lookup"><span data-stu-id="ae96d-111">The next few steps look at the conditions of agreement USMF-000001.</span></span> <span data-ttu-id="ae96d-112">以便更加轻松地了解如何在过程后续阶段计算客户信用价值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-112">This makes it easier to understand how the customer credit values are calculated later in the procedure.</span></span>  
    * <span data-ttu-id="ae96d-113">协议适用于个别客户，在此示例中是客户 US-009。</span><span class="sxs-lookup"><span data-stu-id="ae96d-113">The agreement is for an individual customer, in this example customer US-009.</span></span>  
    * <span data-ttu-id="ae96d-114">在客户购买特定产品时，可以给予客户返点。</span><span class="sxs-lookup"><span data-stu-id="ae96d-114">Rebates are given to the customer when they purchase a specific product.</span></span> <span data-ttu-id="ae96d-115">在这种情况下，产品的物料编号是 T0020。</span><span class="sxs-lookup"><span data-stu-id="ae96d-115">In this case, the product has item number T0020.</span></span>   
    * <span data-ttu-id="ae96d-116">客户的销售业绩会每周累计，并据此估计返点金额。</span><span class="sxs-lookup"><span data-stu-id="ae96d-116">The customer's sales performance, against which the rebate amounts are estimated, is to be accumulated on a weekly basis.</span></span>  
    * <span data-ttu-id="ae96d-117">“价格源自”的设置是“总额”，这意味着该行的销售额（据此估计要求的付款）未减去行折扣。</span><span class="sxs-lookup"><span data-stu-id="ae96d-117">The setting for “Price taken from” is Gross, which means that line's sales amount on which basis the claim is estimated is not reduced by the line discount.</span></span>  
    * <span data-ttu-id="ae96d-118">“返点换行符类型”字段会显示计算返点的方法。</span><span class="sxs-lookup"><span data-stu-id="ae96d-118">The Rebate line break type field shows the method for calculating rebates.</span></span> <span data-ttu-id="ae96d-119">在这种情况下，销售目标（据此估计返点）被设置为“数量”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-119">In this case, the sales target against which the rebates are to be estimated is set to Quantity.</span></span>   
    * <span data-ttu-id="ae96d-120">协议的行会指定返点金额类型、实际返点价值和阈值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-120">The agreement's lines specify the rebate amount type, the actual rebate value, and the thresholds.</span></span> <span data-ttu-id="ae96d-121">在此示例中，如果每周购买的产品数量下降到 1-50 个单位，客户将有资格获得每个已售单位 20 美元的返点；如果购买数量大于 50 个单位，每个已售单位可以获得 40 美元的返点。</span><span class="sxs-lookup"><span data-stu-id="ae96d-121">In this example, the customer will qualify for a rebate of 20 USD per unit sold, if their weekly purchases of the product fall within 1 to 50 units; and a rebate of 40 USD per unit sold, if they purchase above 50 units.</span></span>  
2. <span data-ttu-id="ae96d-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ae96d-122">Close the page.</span></span>

## <a name="generate-rebate-claims"></a><span data-ttu-id="ae96d-123">生成返点要求</span><span class="sxs-lookup"><span data-stu-id="ae96d-123">Generate rebate claims</span></span>
1. <span data-ttu-id="ae96d-124">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-124">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="ae96d-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-125">Click New.</span></span>
    * <span data-ttu-id="ae96d-126">若要模仿返点要求的生成方式，下一个任务是创建销售订单，其中规定购买特定产品和数量的上述客户将有资格获得返点。</span><span class="sxs-lookup"><span data-stu-id="ae96d-126">To mimic the way in which rebate claims would be generated, the next task is to create a sales order, where the product and quantity will qualify the customer in question for a rebate.</span></span>  
3. <span data-ttu-id="ae96d-127">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-127">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="ae96d-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-128">Click OK.</span></span>
5. <span data-ttu-id="ae96d-129">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-129">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="ae96d-130">将“数量”设置为“40”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-130">Set Quantity to '40'.</span></span>
7. <span data-ttu-id="ae96d-131">单击“销售订单行”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-131">Click Sales order line.</span></span>
8. <span data-ttu-id="ae96d-132">单击“价格详情”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-132">Click Price details.</span></span>
    * <span data-ttu-id="ae96d-133">如果您没有看到此选项，这是因为在开始该指南之前，您没有将“启用价格详情”选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-133">If you don’t see this option, it’s because you didn’t set the Enable price details option to Yes before you started the guide.</span></span>  
9. <span data-ttu-id="ae96d-134">展开“返点”部分。</span><span class="sxs-lookup"><span data-stu-id="ae96d-134">Expand the Rebates section.</span></span>
    * <span data-ttu-id="ae96d-135">“返点”选项卡会列示适用于当前订单行的所有返点协议，并显示估计的返点金额。</span><span class="sxs-lookup"><span data-stu-id="ae96d-135">The Rebates tab lists all the rebate agreements that are applicable to the current order line and shows the estimated rebate amount.</span></span> <span data-ttu-id="ae96d-136">请注意，显示的金额仅表示未来的返利要求可能是多少。</span><span class="sxs-lookup"><span data-stu-id="ae96d-136">Note that the displayed amounts are only indications of what future rebate claims may be.</span></span> <span data-ttu-id="ae96d-137">实际返点金额可能不同，这取决于：客户根据定期返点协议实现的总销售量、客户是否退还所有或部分数量、以及适用的销售订单是否已开具发票。</span><span class="sxs-lookup"><span data-stu-id="ae96d-137">The actual rebate amounts may be different depending on: the total sales volume achieved by the customer under a periodic rebate agreement; whether the customer had returned all or partial quantities; and whether the applicable sales order was invoiced.</span></span>  
10. <span data-ttu-id="ae96d-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ae96d-138">Close the page.</span></span>
11. <span data-ttu-id="ae96d-139">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-139">Click Add line.</span></span>
12. <span data-ttu-id="ae96d-140">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-140">In the Item number field, enter or select a value.</span></span>
13. <span data-ttu-id="ae96d-141">将“数量”设置为“60”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-141">Set Quantity to '60'.</span></span>
14. <span data-ttu-id="ae96d-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-142">Click Save.</span></span>
15. <span data-ttu-id="ae96d-143">在操作窗格上，单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-143">On the Action Pane, click Invoice.</span></span>
16. <span data-ttu-id="ae96d-144">单击“发票”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-144">Click Invoice.</span></span>
17. <span data-ttu-id="ae96d-145">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="ae96d-145">Expand the Parameters section.</span></span>
18. <span data-ttu-id="ae96d-146">在“数量”字段中，选择“所有”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-146">In the Quantity field, select 'All'.</span></span>
19. <span data-ttu-id="ae96d-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-147">Click OK.</span></span>
20. <span data-ttu-id="ae96d-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-148">Click OK.</span></span>

## <a name="process-rebate-claims"></a><span data-ttu-id="ae96d-149">处理返利索赔</span><span class="sxs-lookup"><span data-stu-id="ae96d-149">Process rebate claims</span></span>
1. <span data-ttu-id="ae96d-150">转至“销售和营销”>“客户返利”>“返利”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-150">Go to Sales and marketing > Customer rebates > Rebates.</span></span>
    * <span data-ttu-id="ae96d-151">“返点”页面可以用作工作台，您可以在此审查、批准和处理返点要求。</span><span class="sxs-lookup"><span data-stu-id="ae96d-151">The Rebates page acts a workbench in which you can review, approve, and process rebate claims.</span></span> <span data-ttu-id="ae96d-152">您现在将处理由于为客户 US-009 的销售订单开具发票而创建的要求，该客户是返利协议 USMF-000001 的主体。</span><span class="sxs-lookup"><span data-stu-id="ae96d-152">You’ll now process the claims that were created as a result of invoicing a sales order for customer US-009, who is the subject of the rebate agreement USMF-000001.</span></span>   
    * <span data-ttu-id="ae96d-153">第一行表示 800 美元的返点要求，该金额是基于产品 T0020 的 40 个单位销售量，以及每个单位 20 美元返点计算得出。</span><span class="sxs-lookup"><span data-stu-id="ae96d-153">The first line represents a rebate claim for 800 USD, which is based on the sales of 40 units of product T0020, calculated at 20 USD per unit.</span></span> <span data-ttu-id="ae96d-154">这与返点协议的第一个数量分段条件相匹配。</span><span class="sxs-lookup"><span data-stu-id="ae96d-154">This matches the conditions of the first quantity break in the rebate agreement.</span></span>  
    * <span data-ttu-id="ae96d-155">第二个要求是 2,400 美元，该金额是根据返点协议的第二个数量分段，基于产品 T0020 的 60 个单位销售量，以及每个单位 40 美元返点计算得出的。</span><span class="sxs-lookup"><span data-stu-id="ae96d-155">The second claim is for 2,400 USD, which is based on the sales of 60 units of product T0020, calculated at 40 USD per unit, as per the second quantity break in the agreement.</span></span>  
    * <span data-ttu-id="ae96d-156">这两个要求都处于“待计算”的状态。</span><span class="sxs-lookup"><span data-stu-id="ae96d-156">Both claims are in the “To be calculated” state.</span></span> <span data-ttu-id="ae96d-157">这意味着它们与如下协议相关：定期跟踪客户销售业绩，且必须在各周期内重新计算以说明总销售量。</span><span class="sxs-lookup"><span data-stu-id="ae96d-157">This means that they are associated with an agreement that tracks the customer's sales performance on periodic basis and that they have to be re-calculated to account for the total sales volume within the respective period.</span></span>   
2. <span data-ttu-id="ae96d-158">单击“累计”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-158">Click Cumulate.</span></span>
3. <span data-ttu-id="ae96d-159">在“客户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-159">In the Customer field, enter or select a value.</span></span>
4. <span data-ttu-id="ae96d-160">在“开始日期”字段中，选择今天的日期。</span><span class="sxs-lookup"><span data-stu-id="ae96d-160">In the Start date field, select today's date.</span></span>
5. <span data-ttu-id="ae96d-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-161">Click OK.</span></span>
    * <span data-ttu-id="ae96d-162">作为运行“累计功能”的结果，估计的返点要求金额现已经过调整，以说明相关周期内客户的总销售量高于第一个返点生成时的总销售量。</span><span class="sxs-lookup"><span data-stu-id="ae96d-162">As a result of running the Cumulate function, the estimated claim amount has now been adjusted to account for the fact that the customer's total sales volume in the relevant period is higher than when the first rebate was generated.</span></span> <span data-ttu-id="ae96d-163">更具体而言，由于购买的总数量已达到 100 个单位，客户现在有资格获得每个单位 40 美元的返利（根据返利协议的第二个数量分段），或 400 美元的总返利金额。</span><span class="sxs-lookup"><span data-stu-id="ae96d-163">More specifically, because the total purchased quantity has reached 100 units, the customer now qualifies for 40 USD per unit (as per the agreement's second quantity break), or 400 USD of total rebate amount.</span></span> <span data-ttu-id="ae96d-164">该差异被记录为额外 800 美元的新要求“调整”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-164">The difference is recorded as a new claim "adjustment" for the additional 800 USD.</span></span> <span data-ttu-id="ae96d-165">包括在“累计”更新中的返点要求的状态现在被设置为“已计算”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-165">The status of the rebate claims that were included in the Cumulate update are now set to Calculated.</span></span>   
6. <span data-ttu-id="ae96d-166">在列表中，标记所有行。</span><span class="sxs-lookup"><span data-stu-id="ae96d-166">In the list, mark all rows.</span></span>
7. <span data-ttu-id="ae96d-167">单击“审核”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-167">Click Approve.</span></span>
8. <span data-ttu-id="ae96d-168">单击“流程”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-168">Click Process.</span></span>
9. <span data-ttu-id="ae96d-169">在“客户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ae96d-169">In the Customer field, enter or select a value.</span></span>
10. <span data-ttu-id="ae96d-170">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-170">Click OK.</span></span>
    * <span data-ttu-id="ae96d-171">消息显示返点已成功处理，并且该要求的状态已被更改为“标记”。</span><span class="sxs-lookup"><span data-stu-id="ae96d-171">A message shows that the rebate was processed successfully, and the status of the claims has been changed to Mark.</span></span> <span data-ttu-id="ae96d-172">这意味着，作为返利应计项目日记帐的结果：a) 该要求现已被转移到临时客户余额，以作为扣减项目；b) 返利应计项目帐户已被记入贷方，以表示客户的未来负债；和 c) 返利费用帐户已被记入借方，以承认所发生的与销售相关的成本。</span><span class="sxs-lookup"><span data-stu-id="ae96d-172">This means that as a result of a Rebate accrual journal being posted: a) the claims have now been transferred to the temporary customer balance as deductions; b) the Rebate accrual account has been credited to represent the future liability towards the customer; and c) the Rebate expense account has been debited, in recognition of the cost incurred in connection with the sales.</span></span>   


