---
title: 创建联产品的物料计划
description: 生产规划员为属于配方联产品的物料规划物料要求。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209666"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7a3da-103">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="7a3da-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a3da-104">生产规划员为属于配方联产品的物料规划物料要求。</span><span class="sxs-lookup"><span data-stu-id="7a3da-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="7a3da-105">使用 USP2 公司演示数据创建此过程。</span><span class="sxs-lookup"><span data-stu-id="7a3da-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7a3da-106">创建联产品的要求</span><span class="sxs-lookup"><span data-stu-id="7a3da-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="7a3da-107">转到“默认仪表板”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="7a3da-108">点击“销售订单处理和查询”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="7a3da-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-109">Click New.</span></span>
4. <span data-ttu-id="7a3da-110">单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-110">Click Sales order.</span></span>
5. <span data-ttu-id="7a3da-111">在“客户帐户”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="7a3da-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="7a3da-112">示例：US-001</span><span class="sxs-lookup"><span data-stu-id="7a3da-112">Example: US-001</span></span>  
6. <span data-ttu-id="7a3da-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-113">Click OK.</span></span>
7. <span data-ttu-id="7a3da-114">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="7a3da-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7a3da-115">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="7a3da-115">Example: P6003</span></span>  
8. <span data-ttu-id="7a3da-116">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7a3da-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="7a3da-117">示例：50000</span><span class="sxs-lookup"><span data-stu-id="7a3da-117">Example: 50000</span></span>  
9. <span data-ttu-id="7a3da-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7a3da-119">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="7a3da-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="7a3da-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7a3da-120">Close the page.</span></span>
2. <span data-ttu-id="7a3da-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7a3da-121">Close the page.</span></span>
3. <span data-ttu-id="7a3da-122">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-122">Click Master planning.</span></span>
4. <span data-ttu-id="7a3da-123">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7a3da-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7a3da-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a3da-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a3da-125">示例：主计划</span><span class="sxs-lookup"><span data-stu-id="7a3da-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="7a3da-126">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-126">Click Run.</span></span>
7. <span data-ttu-id="7a3da-127">展开或折叠包含部分的“记录”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="7a3da-128">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-128">Click Filter.</span></span>
9. <span data-ttu-id="7a3da-129">在列表中，选择“字段 = 物料编号”的行。</span><span class="sxs-lookup"><span data-stu-id="7a3da-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="7a3da-130">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="7a3da-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="7a3da-131">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="7a3da-131">Example: P6003</span></span>  
11. <span data-ttu-id="7a3da-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-132">Click OK.</span></span>
12. <span data-ttu-id="7a3da-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-133">Click OK.</span></span>
13. <span data-ttu-id="7a3da-134">单击“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-134">Click Planned orders.</span></span>
14. <span data-ttu-id="7a3da-135">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="7a3da-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7a3da-136">例如，使用值“P6000”在“物料编号”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="7a3da-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7a3da-137">根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。</span><span class="sxs-lookup"><span data-stu-id="7a3da-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="7a3da-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7a3da-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7a3da-139">选择筛选器返回的任何行。</span><span class="sxs-lookup"><span data-stu-id="7a3da-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="7a3da-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a3da-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="7a3da-141">展开或折叠“限定”部分。</span><span class="sxs-lookup"><span data-stu-id="7a3da-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="7a3da-142">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a3da-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a3da-143">计划订单受到联产品销售订单的限定。</span><span class="sxs-lookup"><span data-stu-id="7a3da-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="7a3da-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7a3da-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7a3da-145">创建联产品的要求</span><span class="sxs-lookup"><span data-stu-id="7a3da-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="7a3da-146">转到“默认仪表板”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="7a3da-147">点击“销售订单处理和查询”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="7a3da-148">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-148">Click New.</span></span>
4. <span data-ttu-id="7a3da-149">单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-149">Click Sales order.</span></span>
5. <span data-ttu-id="7a3da-150">在“客户帐户”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="7a3da-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="7a3da-151">示例：US-001</span><span class="sxs-lookup"><span data-stu-id="7a3da-151">Example: US-001</span></span>  
6. <span data-ttu-id="7a3da-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-152">Click OK.</span></span>
7. <span data-ttu-id="7a3da-153">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="7a3da-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7a3da-154">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="7a3da-154">Example: P6003</span></span>  
8. <span data-ttu-id="7a3da-155">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7a3da-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="7a3da-156">示例：50000</span><span class="sxs-lookup"><span data-stu-id="7a3da-156">Example: 50000</span></span>  
9. <span data-ttu-id="7a3da-157">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7a3da-158">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="7a3da-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="7a3da-159">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7a3da-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="7a3da-160">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a3da-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a3da-161">示例：主计划</span><span class="sxs-lookup"><span data-stu-id="7a3da-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="7a3da-162">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-162">Click Run.</span></span>
4. <span data-ttu-id="7a3da-163">展开或折叠包含部分的“记录”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="7a3da-164">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-164">Click Filter.</span></span>
6. <span data-ttu-id="7a3da-165">在列表中，选择“字段 = 物料编号”的行。</span><span class="sxs-lookup"><span data-stu-id="7a3da-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="7a3da-166">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="7a3da-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="7a3da-167">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="7a3da-167">Example: P6003</span></span>  
8. <span data-ttu-id="7a3da-168">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-168">Click OK.</span></span>
9. <span data-ttu-id="7a3da-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-169">Click OK.</span></span>
10. <span data-ttu-id="7a3da-170">单击“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-170">Click Planned orders.</span></span>
11. <span data-ttu-id="7a3da-171">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="7a3da-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7a3da-172">例如，使用值“P6000”在“物料编号”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="7a3da-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7a3da-173">根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。</span><span class="sxs-lookup"><span data-stu-id="7a3da-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="7a3da-174">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7a3da-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7a3da-175">选择筛选器返回的任何行。</span><span class="sxs-lookup"><span data-stu-id="7a3da-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="7a3da-176">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a3da-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7a3da-177">展开或折叠“限定”部分。</span><span class="sxs-lookup"><span data-stu-id="7a3da-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="7a3da-178">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a3da-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a3da-179">计划订单受到联产品销售订单的限定。</span><span class="sxs-lookup"><span data-stu-id="7a3da-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="7a3da-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7a3da-180">Close the page.</span></span>
17. <span data-ttu-id="7a3da-181">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-181">Click Master planning.</span></span>
18. <span data-ttu-id="7a3da-182">转到“主计划”>“设置”>“主计划参数”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="7a3da-183">在“禁用所有计划过程”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="7a3da-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="7a3da-184">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7a3da-184">Close the page.</span></span>

