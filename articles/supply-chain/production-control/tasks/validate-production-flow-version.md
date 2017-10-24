--- 
title: "验证生产流和版本"
description: "该过程显示如何创建新的生产流以及 lean manufacturing 的第一个版本。"
author: ChristianRytt
manager: AnnBe
ms.date: 02/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7fb52291f15bfe9063b2a9d4a572dcdc44286402
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="93e0a-103">验证生产流和版本</span><span class="sxs-lookup"><span data-stu-id="93e0a-103">Validate a production flow and version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93e0a-104">该过程显示如何创建新的生产流以及 lean manufacturing 的第一个版本。</span><span class="sxs-lookup"><span data-stu-id="93e0a-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="93e0a-105">先决条件：必须定义 Lean manufacturing 的生产参数以及类别时间的度量单位。</span><span class="sxs-lookup"><span data-stu-id="93e0a-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="93e0a-106">您需要定义“价值流”和“生产组”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="93e0a-107">请参阅 Lean manufacturing 白皮书，以了解生产流和活动的概念。</span><span class="sxs-lookup"><span data-stu-id="93e0a-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="93e0a-108">该过程在演示数据中使用的是 USMF 法人。</span><span class="sxs-lookup"><span data-stu-id="93e0a-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="93e0a-109">但是，如果已配置 Lean manufacturing 的法人，则可使用其他法人。</span><span class="sxs-lookup"><span data-stu-id="93e0a-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="93e0a-110">创建生产流</span><span class="sxs-lookup"><span data-stu-id="93e0a-110">Create a production flow</span></span>
1. <span data-ttu-id="93e0a-111">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="93e0a-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-112">Click New.</span></span>
3. <span data-ttu-id="93e0a-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="93e0a-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="93e0a-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="93e0a-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="93e0a-115">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="93e0a-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="93e0a-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="93e0a-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93e0a-117">价值流是跨越价值流的所有活动和流程的运营单位。</span><span class="sxs-lookup"><span data-stu-id="93e0a-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="93e0a-118">在此阶段，运营单位限制为法人实体，但不具有进一步功能。</span><span class="sxs-lookup"><span data-stu-id="93e0a-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="93e0a-119">在“生产组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="93e0a-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="93e0a-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="93e0a-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93e0a-121">生产组允许为生产流程定义材料、人工和 WIP 帐户。</span><span class="sxs-lookup"><span data-stu-id="93e0a-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="93e0a-122">要将核算生产环境与生产流相联系，必须选择生产组。</span><span class="sxs-lookup"><span data-stu-id="93e0a-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="93e0a-123">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="93e0a-124">创建生产流版本</span><span class="sxs-lookup"><span data-stu-id="93e0a-124">Create a production flow version</span></span>
1. <span data-ttu-id="93e0a-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-125">Click Add.</span></span>
2. <span data-ttu-id="93e0a-126">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="93e0a-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="93e0a-127">您可以在指定时间更新该版本，甚至是有效版本的“到期日期”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="93e0a-128">使用该版本的到期日期，以作出版本淘汰计划。</span><span class="sxs-lookup"><span data-stu-id="93e0a-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="93e0a-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-129">Click OK.</span></span>
4. <span data-ttu-id="93e0a-130">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="93e0a-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="93e0a-131">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="93e0a-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="93e0a-132">选择“单位产品生产时间单位”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="93e0a-133">在“平均单位产品生产时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="93e0a-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="93e0a-134">对于生产流版本的间隔控制，定义所针对的单位产品生产时间。</span><span class="sxs-lookup"><span data-stu-id="93e0a-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="93e0a-135">单位产品为每个时间周期内生产的产品数量。</span><span class="sxs-lookup"><span data-stu-id="93e0a-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="93e0a-136">在给定示例中，单位产品生产时间为每 10 件 0.2 小时。</span><span class="sxs-lookup"><span data-stu-id="93e0a-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="93e0a-137">工作时间为 8 小时，所对应的日产能为 400 件。</span><span class="sxs-lookup"><span data-stu-id="93e0a-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="93e0a-138">在“每周期数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="93e0a-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="93e0a-139">展开或折叠“版本详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="93e0a-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="93e0a-140">在“最小单位产品生产时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="93e0a-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="93e0a-141">最小单位产品生产时间必须为小于或等于平均单位产品生产时间。</span><span class="sxs-lookup"><span data-stu-id="93e0a-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="93e0a-142">在“最大单位产品生产时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="93e0a-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="93e0a-143">最大单位产品生产时间必须为大于或等于“平均单位产品生产时间”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="93e0a-144">在“期间”中输入实际周期时间的天数</span><span class="sxs-lookup"><span data-stu-id="93e0a-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="93e0a-145">实际周期为从实际分钟数向后计算实际周期时间的合并工作天数。</span><span class="sxs-lookup"><span data-stu-id="93e0a-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="93e0a-146">可以随时更改该值，且该值只能用来计算实际周期时间。</span><span class="sxs-lookup"><span data-stu-id="93e0a-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="93e0a-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="93e0a-147">Click Save.</span></span>

