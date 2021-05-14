---
title: 创建联产品的物料计划
description: 生产规划员为属于配方联产品的物料规划物料要求。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920721"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="81a1a-103">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="81a1a-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81a1a-104">生产规划员为属于配方联产品的物料规划物料要求。</span><span class="sxs-lookup"><span data-stu-id="81a1a-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="81a1a-105">使用 USP2 公司演示数据创建此过程。</span><span class="sxs-lookup"><span data-stu-id="81a1a-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="81a1a-106">创建联产品的要求</span><span class="sxs-lookup"><span data-stu-id="81a1a-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="81a1a-107">转到 **销售和市场营销 \> 工作区 \> 销售订单处理和查询**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="81a1a-108">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-108">Select **New**.</span></span>
1. <span data-ttu-id="81a1a-109">选择 **销售订单**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="81a1a-110">在 **客户帐户** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="81a1a-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="81a1a-111">示例：US-001</span><span class="sxs-lookup"><span data-stu-id="81a1a-111">Example: US-001</span></span>  
1. <span data-ttu-id="81a1a-112">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-112">Select **OK**.</span></span>
1. <span data-ttu-id="81a1a-113">在 **项目编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="81a1a-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="81a1a-114">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="81a1a-114">Example: P6003</span></span>  
1. <span data-ttu-id="81a1a-115">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="81a1a-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="81a1a-116">示例：50000</span><span class="sxs-lookup"><span data-stu-id="81a1a-116">Example: 50000</span></span>  
1. <span data-ttu-id="81a1a-117">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="81a1a-118">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="81a1a-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="81a1a-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="81a1a-119">Close the page.</span></span>
1. <span data-ttu-id="81a1a-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="81a1a-120">Close the page.</span></span>
1. <span data-ttu-id="81a1a-121">选择 **主计划**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="81a1a-122">在 **计划** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="81a1a-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="81a1a-123">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="81a1a-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="81a1a-124">示例：主计划</span><span class="sxs-lookup"><span data-stu-id="81a1a-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="81a1a-125">选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-125">Select **Run**.</span></span>
1. <span data-ttu-id="81a1a-126">展开或折叠 **要包括的记录** 部分。</span><span class="sxs-lookup"><span data-stu-id="81a1a-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="81a1a-127">选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-127">Select **Filter**.</span></span>
1. <span data-ttu-id="81a1a-128">在列表中，选择 **字段** = *物料编号* 的行。</span><span class="sxs-lookup"><span data-stu-id="81a1a-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="81a1a-129">在 **条件** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="81a1a-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="81a1a-130">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="81a1a-130">Example: P6003</span></span>  
1. <span data-ttu-id="81a1a-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-131">Select **OK**.</span></span>
1. <span data-ttu-id="81a1a-132">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-132">Select **OK**.</span></span>
1. <span data-ttu-id="81a1a-133">选择 **计划订单**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="81a1a-134">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="81a1a-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="81a1a-135">例如，使用值“P6000”在 **物料编号** 字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="81a1a-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="81a1a-136">根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。</span><span class="sxs-lookup"><span data-stu-id="81a1a-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="81a1a-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="81a1a-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="81a1a-138">选择筛选器返回的任何行。</span><span class="sxs-lookup"><span data-stu-id="81a1a-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="81a1a-139">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="81a1a-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="81a1a-140">展开 **限定标准** 部分。</span><span class="sxs-lookup"><span data-stu-id="81a1a-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="81a1a-141">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="81a1a-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="81a1a-142">计划订单受到联产品销售订单的限定。</span><span class="sxs-lookup"><span data-stu-id="81a1a-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="81a1a-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="81a1a-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="81a1a-144">为联产品创建第二个要求</span><span class="sxs-lookup"><span data-stu-id="81a1a-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="81a1a-145">转到 **销售和市场营销 \> 工作区 \> 销售订单处理和查询**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="81a1a-146">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-146">Select **New**.</span></span>
1. <span data-ttu-id="81a1a-147">选择 **销售订单**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="81a1a-148">在 **客户帐户** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="81a1a-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="81a1a-149">示例：US-001</span><span class="sxs-lookup"><span data-stu-id="81a1a-149">Example: US-001</span></span>  
1. <span data-ttu-id="81a1a-150">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-150">Select **OK**.</span></span>
1. <span data-ttu-id="81a1a-151">在 **项目编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="81a1a-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="81a1a-152">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="81a1a-152">Example: P6003</span></span>  
1. <span data-ttu-id="81a1a-153">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="81a1a-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="81a1a-154">示例：50000</span><span class="sxs-lookup"><span data-stu-id="81a1a-154">Example: 50000</span></span>  
1. <span data-ttu-id="81a1a-155">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="81a1a-156">为联产品创建第二个物料计划</span><span class="sxs-lookup"><span data-stu-id="81a1a-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="81a1a-157">在 **计划** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="81a1a-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="81a1a-158">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="81a1a-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="81a1a-159">示例：主计划</span><span class="sxs-lookup"><span data-stu-id="81a1a-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="81a1a-160">选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-160">Select **Run**.</span></span>
4. <span data-ttu-id="81a1a-161">展开或折叠 **要包括的记录** 部分。</span><span class="sxs-lookup"><span data-stu-id="81a1a-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="81a1a-162">选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-162">Select **Filter**.</span></span>
6. <span data-ttu-id="81a1a-163">在列表中，选择 **字段** = *物料编号* 的行。</span><span class="sxs-lookup"><span data-stu-id="81a1a-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="81a1a-164">在 *条件* 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="81a1a-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="81a1a-165">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="81a1a-165">Example: P6003</span></span>  
8. <span data-ttu-id="81a1a-166">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-166">Select **OK**.</span></span>
9. <span data-ttu-id="81a1a-167">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-167">Select **OK**.</span></span>
10. <span data-ttu-id="81a1a-168">选择 **计划订单**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="81a1a-169">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="81a1a-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="81a1a-170">例如，使用值“P6000”在 **物料编号** 字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="81a1a-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="81a1a-171">根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。</span><span class="sxs-lookup"><span data-stu-id="81a1a-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="81a1a-172">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="81a1a-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="81a1a-173">选择筛选器返回的任何行。</span><span class="sxs-lookup"><span data-stu-id="81a1a-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="81a1a-174">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="81a1a-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="81a1a-175">展开或折叠 **限定标准** 部分。</span><span class="sxs-lookup"><span data-stu-id="81a1a-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="81a1a-176">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="81a1a-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="81a1a-177">计划订单受到联产品销售订单的限定。</span><span class="sxs-lookup"><span data-stu-id="81a1a-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="81a1a-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="81a1a-178">Close the page.</span></span>
17. <span data-ttu-id="81a1a-179">选择 **主计划**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="81a1a-180">转到 **主计划 \> 设置 \> 主计划参数**。</span><span class="sxs-lookup"><span data-stu-id="81a1a-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="81a1a-181">在 **禁用所有计划流程** 字段中选择 *否*。</span><span class="sxs-lookup"><span data-stu-id="81a1a-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="81a1a-182">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="81a1a-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]