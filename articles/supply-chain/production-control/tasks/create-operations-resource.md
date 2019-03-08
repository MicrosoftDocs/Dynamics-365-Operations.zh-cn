---
title: 创建运营资源
description: 运营资源执行项目或生产流程的活动。
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9d8f13e29ea813eb9721ddca795b67837e2aa5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "350059"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="183d9-103">创建运营资源</span><span class="sxs-lookup"><span data-stu-id="183d9-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="183d9-104">运营资源执行项目或生产流程的活动。</span><span class="sxs-lookup"><span data-stu-id="183d9-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="183d9-105">此过程显示您如何定义运营资源。</span><span class="sxs-lookup"><span data-stu-id="183d9-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="183d9-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="183d9-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="183d9-107">转到“资源”。</span><span class="sxs-lookup"><span data-stu-id="183d9-107">Go to Resources.</span></span>
2. <span data-ttu-id="183d9-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="183d9-108">Click New.</span></span>
3. <span data-ttu-id="183d9-109">在“资源”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="183d9-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="183d9-111">定义产能和消耗参数</span><span class="sxs-lookup"><span data-stu-id="183d9-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="183d9-112">展开“操作”部分。</span><span class="sxs-lookup"><span data-stu-id="183d9-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="183d9-113">在“废料百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="183d9-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="183d9-114">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="183d9-115">指定定义如何计算设置成本的成本类别。</span><span class="sxs-lookup"><span data-stu-id="183d9-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="183d9-116">在“运行时间类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="183d9-117">指定定义如何计算运行时间成本的成本类别。</span><span class="sxs-lookup"><span data-stu-id="183d9-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="183d9-118">在“质量类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="183d9-119">指定定义如何计算基于输出数量的资源成本的成本类别。</span><span class="sxs-lookup"><span data-stu-id="183d9-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="183d9-120">在“产能单位”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="183d9-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="183d9-121">指定表示运营资源的产能的单位。</span><span class="sxs-lookup"><span data-stu-id="183d9-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="183d9-122">在“产能”字段中，输入数字。</span><span class="sxs-lookup"><span data-stu-id="183d9-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="183d9-123">在“效率百分比”字段中，输入数字。</span><span class="sxs-lookup"><span data-stu-id="183d9-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="183d9-124">指定您期望的运营资源效率。</span><span class="sxs-lookup"><span data-stu-id="183d9-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="183d9-125">效率百分比调整运营资源的生成量，并影响为该资源预留的时间。</span><span class="sxs-lookup"><span data-stu-id="183d9-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="183d9-126">在“操作安排百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="183d9-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="183d9-127">指定您想要在运营计划中使用的运营资源的最大产能百分比。</span><span class="sxs-lookup"><span data-stu-id="183d9-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="183d9-128">在“有限产能”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="183d9-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="183d9-129">如果运营资源应根据可用的实际产能安排，以及如果应该考虑现有产能保留，将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="183d9-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="183d9-130">如果此选项设置为“否”，则运营资源假定为无限产能，并且可能会超额订购资源。</span><span class="sxs-lookup"><span data-stu-id="183d9-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="183d9-131">在“瓶颈资源”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="183d9-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="183d9-132">定义工作时间</span><span class="sxs-lookup"><span data-stu-id="183d9-132">Define working times</span></span>
1. <span data-ttu-id="183d9-133">展开“日历”部分。</span><span class="sxs-lookup"><span data-stu-id="183d9-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="183d9-134">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="183d9-134">Click Add.</span></span>
3. <span data-ttu-id="183d9-135">在“日历”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="183d9-136">指定定义资源产能（按小时计算）的工作日历。</span><span class="sxs-lookup"><span data-stu-id="183d9-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="183d9-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="183d9-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="183d9-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="183d9-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="183d9-139">定义资源功能</span><span class="sxs-lookup"><span data-stu-id="183d9-139">Define resource capabilities</span></span>
1. <span data-ttu-id="183d9-140">展开“功能”部分。</span><span class="sxs-lookup"><span data-stu-id="183d9-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="183d9-141">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="183d9-141">Click Add.</span></span>
    * <span data-ttu-id="183d9-142">功能是运营资源执行特定活动的能力。</span><span class="sxs-lookup"><span data-stu-id="183d9-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="183d9-143">计划编制引擎通过将每一活动的资源要求与可用运营资源的功能匹配来分配资源。</span><span class="sxs-lookup"><span data-stu-id="183d9-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="183d9-144">在“功能”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="183d9-145">在“水平”字段，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="183d9-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="183d9-146">指定资源处理该功能的熟练程度。</span><span class="sxs-lookup"><span data-stu-id="183d9-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="183d9-147">在“优先”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="183d9-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="183d9-148">指定该功能相关的运营资源的优先级。</span><span class="sxs-lookup"><span data-stu-id="183d9-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="183d9-149">在按优先级进行计划编制时，首先选择最高优先级的（数值最小）的运营资源。</span><span class="sxs-lookup"><span data-stu-id="183d9-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="183d9-150">分配资源给资源组</span><span class="sxs-lookup"><span data-stu-id="183d9-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="183d9-151">展开“资源组”部分。</span><span class="sxs-lookup"><span data-stu-id="183d9-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="183d9-152">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="183d9-152">Click Add.</span></span>
    * <span data-ttu-id="183d9-153">资源组定义运营资源的站点、生产单位和仓库环境。</span><span class="sxs-lookup"><span data-stu-id="183d9-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="183d9-154">运营资源只有在分配至资源组时，以及只有在资源组所在的站点时才可安排计划。</span><span class="sxs-lookup"><span data-stu-id="183d9-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="183d9-155">在“资源组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="183d9-156">在“输入位置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="183d9-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="183d9-157">指定运营资源调用物料的仓库位置。</span><span class="sxs-lookup"><span data-stu-id="183d9-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

