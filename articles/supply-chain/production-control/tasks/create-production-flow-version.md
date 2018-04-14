--- 
title: "创建生产流版本"
description: "该过程主要讲述创建新的生产流版本。"
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0e2e99bc1132f50bca4e6c21abccdc685658a178
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="128c8-103">创建生产流版本</span><span class="sxs-lookup"><span data-stu-id="128c8-103">Create a production flow version</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="128c8-104">该过程主要讲述创建新的生产流版本。</span><span class="sxs-lookup"><span data-stu-id="128c8-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="128c8-105">对于该过程，必须定义的 lean manufacturing 生产参数和上课时间的度量单位。</span><span class="sxs-lookup"><span data-stu-id="128c8-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="128c8-106">您还需要定义价值流和生产组。</span><span class="sxs-lookup"><span data-stu-id="128c8-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="128c8-107">若要了解更多 lean manufacturing 中生产流程和活动，请参阅 Microsoft Dynamics AX 的 Lean manufacturing 白皮书。</span><span class="sxs-lookup"><span data-stu-id="128c8-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="128c8-108">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="128c8-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="128c8-109">创建生产流</span><span class="sxs-lookup"><span data-stu-id="128c8-109">Create a production flow</span></span>
1. <span data-ttu-id="128c8-110">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="128c8-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="128c8-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="128c8-111">Click New.</span></span>
3. <span data-ttu-id="128c8-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="128c8-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="128c8-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="128c8-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="128c8-114">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="128c8-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="128c8-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="128c8-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="128c8-116">选择值类型价值流图的运营单位。</span><span class="sxs-lookup"><span data-stu-id="128c8-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="128c8-117">价值流是跨越价值流的所有活动和流程的运营单位。</span><span class="sxs-lookup"><span data-stu-id="128c8-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="128c8-118">在此阶段，运营单位限制为法人实体，但不具有进一步功能。</span><span class="sxs-lookup"><span data-stu-id="128c8-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="128c8-119">在“生产组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="128c8-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="128c8-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="128c8-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="128c8-121">为生产流选择生产组。</span><span class="sxs-lookup"><span data-stu-id="128c8-121">Select a production group for the production flow.</span></span> <span data-ttu-id="128c8-122">生产组允许为生产流程定义材料、人工和 WIP 帐户。</span><span class="sxs-lookup"><span data-stu-id="128c8-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="128c8-123">要将核算生产环境与生产流相联系，必须选择生产组。</span><span class="sxs-lookup"><span data-stu-id="128c8-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="128c8-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="128c8-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="128c8-125">创建生产流版本</span><span class="sxs-lookup"><span data-stu-id="128c8-125">Create a production flow version</span></span>
1. <span data-ttu-id="128c8-126">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="128c8-126">Click Add.</span></span>
2. <span data-ttu-id="128c8-127">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="128c8-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="128c8-128">如果需要，请定义版本的“到期日期”。</span><span class="sxs-lookup"><span data-stu-id="128c8-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="128c8-129">您可以在任意指定时间更新它，即便为活动版本。</span><span class="sxs-lookup"><span data-stu-id="128c8-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="128c8-130">您可以使用它来计划逐步淘汰一个版本。</span><span class="sxs-lookup"><span data-stu-id="128c8-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="128c8-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="128c8-131">Click OK.</span></span>
4. <span data-ttu-id="128c8-132">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="128c8-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="128c8-133">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="128c8-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="128c8-134">决定“改变单位产品生产时间”。</span><span class="sxs-lookup"><span data-stu-id="128c8-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="128c8-135">在“平均单位产品生产时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="128c8-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="128c8-136">定义版本的“平均单位产品生产时间”。</span><span class="sxs-lookup"><span data-stu-id="128c8-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="128c8-137">对于生产流版本的间隔控制，定义所针对的单位产品生产时间。</span><span class="sxs-lookup"><span data-stu-id="128c8-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="128c8-138">单位产品为每个时间周期内生产的的产品数量。</span><span class="sxs-lookup"><span data-stu-id="128c8-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="128c8-139">在本例中，单位产品生产时间为每 10 件 0.2 小时。</span><span class="sxs-lookup"><span data-stu-id="128c8-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="128c8-140">工作时间为 8 小时，所对应的日产能为 400 件。</span><span class="sxs-lookup"><span data-stu-id="128c8-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="128c8-141">在“每周期数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="128c8-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="128c8-142">定义“平均单位产品生产时间”周期的数量。</span><span class="sxs-lookup"><span data-stu-id="128c8-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="128c8-143">切换“版本详细信息”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="128c8-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="128c8-144">在“最小单位产品生产时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="128c8-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="128c8-145">定义最小单位产品生产时间。</span><span class="sxs-lookup"><span data-stu-id="128c8-145">Define the minimum takt time.</span></span> <span data-ttu-id="128c8-146">最小单位产品生产时间必须为小于或等于平均单位产品生产时间。</span><span class="sxs-lookup"><span data-stu-id="128c8-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="128c8-147">在“最大单位产品生产时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="128c8-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="128c8-148">最大单位产品生产时间必须为大于或等于“平均单位产品生产时间”。</span><span class="sxs-lookup"><span data-stu-id="128c8-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="128c8-149">在“实际周期期间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="128c8-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="128c8-150">在“周期”中，输入实际的周期天数。</span><span class="sxs-lookup"><span data-stu-id="128c8-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="128c8-151">实际周期为从实际分钟数向后计算实际周期时间的合并工作天数。</span><span class="sxs-lookup"><span data-stu-id="128c8-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="128c8-152">可以随时更改该值，且该值只能用来计算实际周期时间。</span><span class="sxs-lookup"><span data-stu-id="128c8-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="128c8-153">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="128c8-153">Click Save.</span></span>


