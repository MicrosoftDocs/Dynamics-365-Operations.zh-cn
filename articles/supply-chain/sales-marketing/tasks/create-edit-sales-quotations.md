--- 
title: "创建和编辑销售报价单"
description: "该过程演示如何创建和更新销售报价单。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f56b495131836689395a2124d5a834579e1646b7
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="8d0d2-103">创建和编辑销售报价单</span><span class="sxs-lookup"><span data-stu-id="8d0d2-103">Create and edit sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d0d2-104">该过程演示如何创建和更新销售报价单。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="8d0d2-105">您可以使用演示数据公司 USMF 或您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="8d0d2-106">创建销售报价单</span><span class="sxs-lookup"><span data-stu-id="8d0d2-106">Create a sales quotation</span></span>
1. <span data-ttu-id="8d0d2-107">转到“销售和市场营销”>“销售报价单”>“所有报价单”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="8d0d2-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-108">Click New.</span></span>
3. <span data-ttu-id="8d0d2-109">在“帐户类型”字段中，选择“目标客户”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="8d0d2-110">在“目标客户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="8d0d2-111">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-111">Expand the General section.</span></span>
    * <span data-ttu-id="8d0d2-112">由于您选择从“销售和市场营销区域”创建报价单，类型自动设置为“销售报价单”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="8d0d2-113">若要创建项目报价，必须从“项目管理和会计模块”访问。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="8d0d2-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-114">Click OK.</span></span>
    * <span data-ttu-id="8d0d2-115">报价单行上的字段和操作与销售订单行上的非常类似。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="8d0d2-116">报价单与销售订单一样，在不知道物料编号或在报价单创建过程没有物料编号时可针对特定物料创建，还可针对销售类别创建。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="8d0d2-117">在“物料”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="8d0d2-118">在“物料”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="8d0d2-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-119">Close the page.</span></span>
10. <span data-ttu-id="8d0d2-120">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8d0d2-121">如果在行上选择该物料的有效贸易协议，适用价格和折扣将会自动复制到报价单行上。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="8d0d2-122">确保“单价”字段含有数值，并且您在想要时还可输入折扣值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="8d0d2-123">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-123">Click Save.</span></span>
12. <span data-ttu-id="8d0d2-124">在操作窗格上单击“销售报价单”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="8d0d2-125">单击“总计”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-125">Click Totals.</span></span>
14. <span data-ttu-id="8d0d2-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-126">Click OK.</span></span>
15. <span data-ttu-id="8d0d2-127">单击“销售报价单行”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="8d0d2-128">单击“价格”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-128">Click Prices.</span></span>
    * <span data-ttu-id="8d0d2-129">在“运行价格模拟”页，您可以进行试验，根据预期单价、折扣金额、折扣百分比、总金额、毛利或贡献率调整报价单的预期收入或收益率。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="8d0d2-130">在对目标值满意时，应用建议到报价单行中，这会相应更新价格相关的字段。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="8d0d2-131">您可以任意创建多个价格模拟。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="8d0d2-132">在单击“新建”时，当前报价单行的价格条件会复制到该页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="8d0d2-133">然后，您可以修改任何价格相关字段中的值到目标字段中。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="8d0d2-134">任一字段的任何更改会触发所有其他字段的重新计算。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="8d0d2-135">为使系统计算销售毛利和贡献率，必须知道产品的单价。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="8d0d2-136">使用“模拟价格”选项卡，查看原价、建议更改价及其对报价单总价的影响的详细视图。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="8d0d2-137">通常，在设为新金额的模拟价应用于报价单行时，系统重新计算并在“单价”字段输入新的数值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="8d0d2-138">如果模拟基于新毛利或新贡献率，则仅更新净额字段，且单价字段为空。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="8d0d2-139">在这两种情况下，报价单行上的所有折扣将会在模拟前被删除。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="8d0d2-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-140">Close the page.</span></span>
18. <span data-ttu-id="8d0d2-141">在操作窗格上，单击“报价单”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="8d0d2-142">单击“发送报价单”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-142">Click Send quotation.</span></span>
20. <span data-ttu-id="8d0d2-143">在“打印报价单”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="8d0d2-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-144">Click OK.</span></span>
    * <span data-ttu-id="8d0d2-145">报表的生成可能需要一分钟。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-145">The report may take a minute to generate.</span></span> <span data-ttu-id="8d0d2-146">生成报表前不要关闭页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="8d0d2-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="8d0d2-148">更新销售报价单</span><span class="sxs-lookup"><span data-stu-id="8d0d2-148">Update a sales quotation</span></span>
1. <span data-ttu-id="8d0d2-149">在操作窗格上，单击“跟进”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="8d0d2-150">单击“转换为客户”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="8d0d2-151">在“客户帐户”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="8d0d2-152">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-152">Click Check.</span></span>
    * <span data-ttu-id="8d0d2-153">确保您看到消息：您输入的帐号可随意使用。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="8d0d2-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-154">Click OK.</span></span>
    * <span data-ttu-id="8d0d2-155">系统现在为目标客户在报价单上创建了新客户帐户。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="8d0d2-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-156">Close the page.</span></span>
7. <span data-ttu-id="8d0d2-157">在操作窗格上，单击“跟进”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="8d0d2-158">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-158">Click Confirm.</span></span>
9. <span data-ttu-id="8d0d2-159">在“原因”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="8d0d2-160">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-160">Click OK.</span></span>
11. <span data-ttu-id="8d0d2-161">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="8d0d2-162">单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-162">Click Sales orders.</span></span>
13. <span data-ttu-id="8d0d2-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8d0d2-163">Close the page.</span></span>


