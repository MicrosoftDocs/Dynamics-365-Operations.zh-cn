---
title: 创建和编辑销售报价单
description: 该过程演示如何创建和更新销售报价单。
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c15b41a4b0979ec79c8dbd8d88627bffcf6ed3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981224"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="69ef6-103">创建和编辑销售报价单</span><span class="sxs-lookup"><span data-stu-id="69ef6-103">Create and edit sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69ef6-104">该过程演示如何创建和更新销售报价单。</span><span class="sxs-lookup"><span data-stu-id="69ef6-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="69ef6-105">您可以使用演示数据公司 USMF 或您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="69ef6-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="69ef6-106">创建销售报价单</span><span class="sxs-lookup"><span data-stu-id="69ef6-106">Create a sales quotation</span></span>
1. <span data-ttu-id="69ef6-107">转到**导航窗格 > 模块 > 销售和营销 > 销售报价单 > 所有报价单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-107">Go to **Navigation pane > Modules > Sales and marketing > Sales quotations > All quotations**.</span></span>
2. <span data-ttu-id="69ef6-108">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-108">Click **New**.</span></span>
3. <span data-ttu-id="69ef6-109">在**帐户类型**字段中，选择“目标客户”。</span><span class="sxs-lookup"><span data-stu-id="69ef6-109">In the **Account type** field, select 'Prospect'.</span></span>
4. <span data-ttu-id="69ef6-110">在**目标客户**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-110">In the **Prospect** field, enter or select a value.</span></span>
5. <span data-ttu-id="69ef6-111">展开**常规**部分。</span><span class="sxs-lookup"><span data-stu-id="69ef6-111">Expand the **General** section.</span></span> <span data-ttu-id="69ef6-112">由于您选择从“销售和市场营销区域”创建报价单，类型自动设置为“销售报价单”。</span><span class="sxs-lookup"><span data-stu-id="69ef6-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to 'Sales quotation'.</span></span> <span data-ttu-id="69ef6-113">若要创建项目报价，必须从**项目管理和会计**模块访问。</span><span class="sxs-lookup"><span data-stu-id="69ef6-113">To create a quotation for a project you must access it from the **Project management and accounting** module.</span></span>
6. <span data-ttu-id="69ef6-114">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-114">Click **OK**.</span></span> <span data-ttu-id="69ef6-115">报价单行上的字段和操作与销售订单行上的非常类似。</span><span class="sxs-lookup"><span data-stu-id="69ef6-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="69ef6-116">报价单与销售订单一样，在不知道物料编号或在报价单创建过程没有物料编号时可针对特定物料创建，还可针对销售类别创建。</span><span class="sxs-lookup"><span data-stu-id="69ef6-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>     
7. <span data-ttu-id="69ef6-117">在**物料**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-117">In the **Item** field, enter or select a value.</span></span>
8. <span data-ttu-id="69ef6-118">在**站点**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-118">In the **Site** field, type a value.</span></span>
9. <span data-ttu-id="69ef6-119">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="69ef6-119">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="69ef6-120">如果在行上选择该物料的有效贸易协议，适用价格和折扣将会自动复制到报价单行上。</span><span class="sxs-lookup"><span data-stu-id="69ef6-120">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="69ef6-121">确保“单价”字段含有数值，并且您在想要时还可输入折扣值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-121">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span> 
10. <span data-ttu-id="69ef6-122">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-122">Click **Save**.</span></span>
11. <span data-ttu-id="69ef6-123">在**操作窗格**上单击**销售报价单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-123">On the **Action Pane**, click **Sales quotation**.</span></span>
12. <span data-ttu-id="69ef6-124">单击**总计**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-124">Click **Totals**.</span></span>
13. <span data-ttu-id="69ef6-125">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-125">Click **OK**.</span></span>
14. <span data-ttu-id="69ef6-126">选择销售报价单行。</span><span class="sxs-lookup"><span data-stu-id="69ef6-126">Select the sales quotation line.</span></span>
15. <span data-ttu-id="69ef6-127">在**操作窗格**上单击**报价单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-127">On the **Action Pane**, click **Quotation**.</span></span>
16. <span data-ttu-id="69ef6-128">单击**价格模拟**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-128">Click **Price simulation**.</span></span>
    - <span data-ttu-id="69ef6-129">在**运行价格模拟**页，您可以进行试验，根据预期单价、折扣金额、折扣百分比、总金额、毛利或贡献率调整报价单的预期收入或收益率。</span><span class="sxs-lookup"><span data-stu-id="69ef6-129">In the **Run price simulation** page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span> <span data-ttu-id="69ef6-130">在对目标值满意时，应用建议到报价单行中，这会相应更新价格相关的字段。</span><span class="sxs-lookup"><span data-stu-id="69ef6-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    - <span data-ttu-id="69ef6-131">您可以任意创建多个价格模拟。</span><span class="sxs-lookup"><span data-stu-id="69ef6-131">You can create as many price simulations as you wish.</span></span> <span data-ttu-id="69ef6-132">在单击**新建**时，当前报价单行的价格条件会复制到该页面。</span><span class="sxs-lookup"><span data-stu-id="69ef6-132">When you click **New**, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="69ef6-133">然后，您可以修改任何价格相关字段中的值到目标字段中。</span><span class="sxs-lookup"><span data-stu-id="69ef6-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="69ef6-134">任一字段的任何更改会触发所有其他字段的重新计算。</span><span class="sxs-lookup"><span data-stu-id="69ef6-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="69ef6-135">为使系统计算销售毛利和贡献率，必须知道产品的单价。</span><span class="sxs-lookup"><span data-stu-id="69ef6-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="69ef6-136">使用“模拟价格”选项卡，查看原价、建议更改价及其对报价单总价的影响的详细视图。</span><span class="sxs-lookup"><span data-stu-id="69ef6-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span> <span data-ttu-id="69ef6-137">通常，在设为新金额的模拟价应用于报价单行时，系统重新计算并在“单价”字段输入新的数值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="69ef6-138">如果模拟基于新毛利或新贡献率，则仅更新净额字段，且单价字段为空。</span><span class="sxs-lookup"><span data-stu-id="69ef6-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="69ef6-139">在这两种情况下，报价单行上的所有折扣将会在模拟前被删除。</span><span class="sxs-lookup"><span data-stu-id="69ef6-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>
17. <span data-ttu-id="69ef6-140">在**操作窗格**上单击**报价单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-140">On the **Action Pane**, click **Quotation**.</span></span>
18. <span data-ttu-id="69ef6-141">单击**发送报价单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-141">Click **Send quotation**.</span></span>
19. <span data-ttu-id="69ef6-142">在**打印报价单**字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="69ef6-142">Select 'Yes' in the **Print quotation** field.</span></span>
20. <span data-ttu-id="69ef6-143">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-143">Click **OK**.</span></span> <span data-ttu-id="69ef6-144">报表的生成可能需要一分钟。</span><span class="sxs-lookup"><span data-stu-id="69ef6-144">The report may take a minute to generate.</span></span> <span data-ttu-id="69ef6-145">生成报表前不要关闭页面。</span><span class="sxs-lookup"><span data-stu-id="69ef6-145">Don't close the page until it does so.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="69ef6-146">更新销售报价单</span><span class="sxs-lookup"><span data-stu-id="69ef6-146">Update a sales quotation</span></span>
1. <span data-ttu-id="69ef6-147">转到**导航窗格 > 模块 > 销售和营销 > 销售报价单 > 所有报价单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-147">Go to **Navigation pane > Modules > Sales and marketing > Sales quotations > All quotations**.</span></span>
2. <span data-ttu-id="69ef6-148">在**操作窗格**上单击**跟进**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-148">On the **Action Pane**, click **Follow up**.</span></span>
3. <span data-ttu-id="69ef6-149">单击**转换为客户**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-149">Click **Convert to customer**.</span></span>
4. <span data-ttu-id="69ef6-150">在**客户帐户**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-150">In the **Customer account** field, type a value.</span></span>
5. <span data-ttu-id="69ef6-151">单击**确认**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-151">Click **Check**.</span></span> <span data-ttu-id="69ef6-152">确保您看到消息：您输入的帐号可随意使用。</span><span class="sxs-lookup"><span data-stu-id="69ef6-152">Make sure you see a message that the account number you typed in is free to use.</span></span>  
6. <span data-ttu-id="69ef6-153">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-153">Click **OK**.</span></span> <span data-ttu-id="69ef6-154">系统现在为目标客户在报价单上创建了新客户帐户。</span><span class="sxs-lookup"><span data-stu-id="69ef6-154">The system has now created a new customer account for the prospect on the quotation.</span></span>  
7. <span data-ttu-id="69ef6-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="69ef6-155">Close the page.</span></span>
8. <span data-ttu-id="69ef6-156">在**操作窗格**上单击**跟进**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-156">On the **Action Pane**, click **Follow up**.</span></span>
9. <span data-ttu-id="69ef6-157">单击**确认**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-157">Click **Confirm**.</span></span>
10. <span data-ttu-id="69ef6-158">在**原因**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="69ef6-158">In the **Reason** field, enter or select a value.</span></span>
11. <span data-ttu-id="69ef6-159">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-159">Click **OK**.</span></span>
12. <span data-ttu-id="69ef6-160">在**操作窗格**上单击**常规**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-160">On the **Action Pane**, click **General**.</span></span>
13. <span data-ttu-id="69ef6-161">单击**销售订单**。</span><span class="sxs-lookup"><span data-stu-id="69ef6-161">Click **Sales orders**.</span></span>
14. <span data-ttu-id="69ef6-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="69ef6-162">Close the page.</span></span>

