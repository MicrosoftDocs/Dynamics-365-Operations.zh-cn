--- 
title: "创建联产品的物料计划"
description: "生产规划员为属于配方联产品的物料规划物料要求。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="c727f-103">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="c727f-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c727f-104">生产规划员为属于配方联产品的物料规划物料要求。</span><span class="sxs-lookup"><span data-stu-id="c727f-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="c727f-105">使用 USP2 公司演示数据创建此过程。</span><span class="sxs-lookup"><span data-stu-id="c727f-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="c727f-106">创建联产品的要求</span><span class="sxs-lookup"><span data-stu-id="c727f-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="c727f-107">转到“默认仪表板”。</span><span class="sxs-lookup"><span data-stu-id="c727f-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="c727f-108">点击“销售订单处理和查询”。</span><span class="sxs-lookup"><span data-stu-id="c727f-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="c727f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c727f-109">Click New.</span></span>
4. <span data-ttu-id="c727f-110">单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="c727f-110">Click Sales order.</span></span>
5. <span data-ttu-id="c727f-111">在“客户帐户”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c727f-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="c727f-112">示例：US-001</span><span class="sxs-lookup"><span data-stu-id="c727f-112">Example: US-001</span></span>  
6. <span data-ttu-id="c727f-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c727f-113">Click OK.</span></span>
7. <span data-ttu-id="c727f-114">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c727f-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c727f-115">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="c727f-115">Example: P6003</span></span>  
8. <span data-ttu-id="c727f-116">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c727f-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c727f-117">示例：50000</span><span class="sxs-lookup"><span data-stu-id="c727f-117">Example: 50000</span></span>  
9. <span data-ttu-id="c727f-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c727f-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="c727f-119">创建联产品的物料计划</span><span class="sxs-lookup"><span data-stu-id="c727f-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="c727f-120">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="c727f-120">Click Master planning.</span></span>
2. <span data-ttu-id="c727f-121">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="c727f-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c727f-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c727f-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c727f-123">示例：主计划</span><span class="sxs-lookup"><span data-stu-id="c727f-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="c727f-124">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="c727f-124">Click Run.</span></span>
5. <span data-ttu-id="c727f-125">展开或折叠包含部分的“记录”。</span><span class="sxs-lookup"><span data-stu-id="c727f-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="c727f-126">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="c727f-126">Click Filter.</span></span>
7. <span data-ttu-id="c727f-127">在列表中，选择“字段 = 物料编号”的行。</span><span class="sxs-lookup"><span data-stu-id="c727f-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="c727f-128">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c727f-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="c727f-129">示例：P6003</span><span class="sxs-lookup"><span data-stu-id="c727f-129">Example: P6003</span></span>  
9. <span data-ttu-id="c727f-130">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c727f-130">Click OK.</span></span>
10. <span data-ttu-id="c727f-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c727f-131">Click OK.</span></span>
11. <span data-ttu-id="c727f-132">单击“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="c727f-132">Click Planned orders.</span></span>
12. <span data-ttu-id="c727f-133">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="c727f-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c727f-134">例如，使用值“P6000”在“物料编号”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="c727f-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="c727f-135">根据配方物料筛选，即含有您已创建销售订单的物料的联产品的配方物料。</span><span class="sxs-lookup"><span data-stu-id="c727f-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="c727f-136">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c727f-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c727f-137">选择筛选器返回的任何行。</span><span class="sxs-lookup"><span data-stu-id="c727f-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="c727f-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c727f-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c727f-139">展开或折叠“限定”部分。</span><span class="sxs-lookup"><span data-stu-id="c727f-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="c727f-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c727f-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c727f-141">计划订单受到联产品销售订单的限定。</span><span class="sxs-lookup"><span data-stu-id="c727f-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="c727f-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c727f-142">Close the page.</span></span>


