--- 
title: "定义物料的覆盖规则"
description: "创建此程序的演示数据公司是 USMF。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 443347fd3042184a6be3a025b99f33dff56df79c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="f5fa5-103">定义物料的覆盖规则</span><span class="sxs-lookup"><span data-stu-id="f5fa5-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5fa5-104">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f5fa5-105">该过程会显示如何创建覆盖范围规则，以及覆写特定物料的覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="f5fa5-106">它也显示了如何确定默认库存设置。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="f5fa5-107">创建覆盖范围组</span><span class="sxs-lookup"><span data-stu-id="f5fa5-107">Create a coverage group</span></span>
1. <span data-ttu-id="f5fa5-108">转至“覆盖范围组”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="f5fa5-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-109">Click New.</span></span>
3. <span data-ttu-id="f5fa5-110">在“覆盖范围组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="f5fa5-111">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f5fa5-112">在“日历”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="f5fa5-113">选择总体规划用于创建本组内物料的补货建议的日历。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="f5fa5-114">在“覆盖范围代码”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="f5fa5-115">选择“该过程适用的要求”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="f5fa5-116">在“覆盖时限（以天为单位）”字段中，输入“90”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="f5fa5-117">对于该项目，主计划将创建未来 90 天的附属建议。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="f5fa5-118">在“负天数”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="f5fa5-119">在“正天数”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="f5fa5-120">展开或折叠“其他”部分。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="f5fa5-121">在“添加到需求日期的收货宽限期”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="f5fa5-122">例如，如果将收货宽限期设置为 1 天，并且一个采购订行计划在 5 月 15 日收货，则总体规划会将调整后的收货日期计算为 5 月 16 日。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="f5fa5-123">在“从需求日期中减去的发货宽限期”字段中，输入"1"。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="f5fa5-124">例如，如果将安全宽限期设置为 1 天，并且一个销售订行计划在 5 月 15 日交货，则主计划编制将调整后的交货日期计算为 5 月 14 日。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="f5fa5-125">在“再订购宽限期添加到物料提前期”字段中，输入"1"。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="f5fa5-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="f5fa5-127">创建新产品</span><span class="sxs-lookup"><span data-stu-id="f5fa5-127">Create a new product</span></span>
1. <span data-ttu-id="f5fa5-128">转至“产品发布”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-128">Go to Released products.</span></span>
2. <span data-ttu-id="f5fa5-129">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-129">Click New.</span></span>
3. <span data-ttu-id="f5fa5-130">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="f5fa5-131">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="f5fa5-132">在“物料模型组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f5fa5-133">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f5fa5-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f5fa5-135">在“物料组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f5fa5-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f5fa5-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f5fa5-138">在“存储维度组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f5fa5-139">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="f5fa5-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f5fa5-141">在“跟踪维度组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f5fa5-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f5fa5-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f5fa5-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="f5fa5-145">设置默认订单设置</span><span class="sxs-lookup"><span data-stu-id="f5fa5-145">Setup default order settings</span></span>
1. <span data-ttu-id="f5fa5-146">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="f5fa5-147">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-147">Click Default order settings.</span></span>
3. <span data-ttu-id="f5fa5-148">在“采购站点”字段中，键入在创建采购订单时的默认站点。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="f5fa5-149">在“仓库站点”字段中，键入存储物料的站点。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="f5fa5-150">展开或折叠“库存”部分。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="f5fa5-151">设置多个为“10”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="f5fa5-152">设置最小值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-152">Set Min.</span></span> <span data-ttu-id="f5fa5-153">订单量为“10”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="f5fa5-154">设置最大值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-154">Set Max.</span></span> <span data-ttu-id="f5fa5-155">订单量为“100”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="f5fa5-156">设置标准订单量为“10”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="f5fa5-157">在“采购提前期”字段中，输入数值。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="f5fa5-158">选中或取消选中“工作日”复选框。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="f5fa5-159">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-159">Click Save.</span></span>
13. <span data-ttu-id="f5fa5-160">在“默认订单类型”字段中选择“采购订单”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="f5fa5-161">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-161">Click Save.</span></span>
15. <span data-ttu-id="f5fa5-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-162">Close the page.</span></span>
    * <span data-ttu-id="f5fa5-163">关闭“默认订单设置”页面。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="f5fa5-164">向覆盖范围组中添加物料</span><span class="sxs-lookup"><span data-stu-id="f5fa5-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="f5fa5-165">展开或折叠“计划”部分。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="f5fa5-166">在“覆盖范围组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f5fa5-167">在列表中，找到您创建的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="f5fa5-168">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="f5fa5-169">创建物料覆盖范围规则</span><span class="sxs-lookup"><span data-stu-id="f5fa5-169">Create item coverage rules</span></span>
1. <span data-ttu-id="f5fa5-170">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="f5fa5-171">单击“物料覆盖范围”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-171">Click Item coverage.</span></span>
3. <span data-ttu-id="f5fa5-172">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-172">Click New.</span></span>
4. <span data-ttu-id="f5fa5-173">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-173">Click the General tab.</span></span>
5. <span data-ttu-id="f5fa5-174">选中覆写“覆盖范围组”设置标题上的选择框。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="f5fa5-175">在“覆盖时限（以天为单位）”字段中，输入“60”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="f5fa5-176">尽管物料覆盖范围组要求的物料需提前 90 天做计划，此物料只需提前 60 天做计划。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-176">Although items in coverage group Requirement are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="f5fa5-177">在“负天数”字段中，输入“2”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="f5fa5-178">在“正天数”字段中，输入“2”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="f5fa5-179">单击“提前期”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="f5fa5-180">选中“采购标题”上的选择框。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="f5fa5-181">在“采购时间”字段中，输入“5”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="f5fa5-182">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f5fa5-182">Click Save.</span></span>


