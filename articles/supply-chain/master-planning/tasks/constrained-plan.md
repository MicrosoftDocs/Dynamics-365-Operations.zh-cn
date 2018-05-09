--- 
title: "生成受约束计划"
description: "此过程显示如何创建涉及物料和产能限制的计划。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f612836ea1756dee149db6310f4b3afe386c3222
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="aa11a-103">生成受约束计划</span><span class="sxs-lookup"><span data-stu-id="aa11a-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa11a-104">此过程显示如何创建涉及物料和产能限制的计划。</span><span class="sxs-lookup"><span data-stu-id="aa11a-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="aa11a-105">计划确保，在制造物料可用且资源未超额认购之前，不进行生产。</span><span class="sxs-lookup"><span data-stu-id="aa11a-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="aa11a-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="aa11a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aa11a-107">此程序是专为生产规划员设计的。</span><span class="sxs-lookup"><span data-stu-id="aa11a-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="aa11a-108">设置约束计划</span><span class="sxs-lookup"><span data-stu-id="aa11a-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="aa11a-109">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-109">Click Master planning.</span></span>
2. <span data-ttu-id="aa11a-110">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-110">Click Master plans.</span></span>
3. <span data-ttu-id="aa11a-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="aa11a-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa11a-112">示例：StaticPlan</span><span class="sxs-lookup"><span data-stu-id="aa11a-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="aa11a-113">在“有限产能”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="aa11a-114">在“有限产能时限”字段中，输入“30“。</span><span class="sxs-lookup"><span data-stu-id="aa11a-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="aa11a-115">可以在天数部分，扩展时限。</span><span class="sxs-lookup"><span data-stu-id="aa11a-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="aa11a-116">在“产能”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="aa11a-117">在“产能计划时限（以天为单位）”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="aa11a-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="aa11a-118">示例：60</span><span class="sxs-lookup"><span data-stu-id="aa11a-118">Example: 60</span></span>  
9. <span data-ttu-id="aa11a-119">在“计划延迟”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="aa11a-120">在“计划延迟时限（以天为单位）”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="aa11a-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="aa11a-121">示例：60</span><span class="sxs-lookup"><span data-stu-id="aa11a-121">Example: 60</span></span>  
11. <span data-ttu-id="aa11a-122">展开“计算的延迟”部分。</span><span class="sxs-lookup"><span data-stu-id="aa11a-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="aa11a-123">在“添加计算的延迟到需求日期”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="aa11a-124">在“添加计算的延迟到需求日期”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="aa11a-125">在“添加计算的延迟到需求日期”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="aa11a-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="aa11a-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="aa11a-127">创建约束计划</span><span class="sxs-lookup"><span data-stu-id="aa11a-127">Create a constrained plan</span></span>
1. <span data-ttu-id="aa11a-128">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-128">Click Run.</span></span>
2. <span data-ttu-id="aa11a-129">在“主计划”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="aa11a-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="aa11a-130">选择您设置约束的计划。</span><span class="sxs-lookup"><span data-stu-id="aa11a-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="aa11a-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-131">Click OK.</span></span>
    * <span data-ttu-id="aa11a-132">这可能需要花费一段时间。</span><span class="sxs-lookup"><span data-stu-id="aa11a-132">This may take a while.</span></span>  
4. <span data-ttu-id="aa11a-133">单击“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="aa11a-133">Click Planned orders.</span></span>


