---
title: 创建工作时间模板
description: 工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f41ae891625fea77eed6650a5bc1fb800a08ee8f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210701"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="e08a2-103">创建工作时间模板</span><span class="sxs-lookup"><span data-stu-id="e08a2-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e08a2-104">工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="e08a2-105">该过程说明如何使用对工作时间间隔进行分类的工作时间计划属性定义工作时间模板。</span><span class="sxs-lookup"><span data-stu-id="e08a2-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="e08a2-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="e08a2-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="e08a2-107">转到“所有工作区”>“资源周期管理”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="e08a2-108">单击“工作时间模板”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="e08a2-109">创建工作时间模板</span><span class="sxs-lookup"><span data-stu-id="e08a2-109">Create working time template</span></span>
1. <span data-ttu-id="e08a2-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-110">Click New.</span></span>
2. <span data-ttu-id="e08a2-111">在“工作时间模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e08a2-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="e08a2-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e08a2-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e08a2-113">展开“星期一”部分。</span><span class="sxs-lookup"><span data-stu-id="e08a2-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="e08a2-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-114">Click Add.</span></span>
6. <span data-ttu-id="e08a2-115">在“开始”字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="e08a2-116">指定上午开始工作的时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="e08a2-117">在“结束”字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="e08a2-118">指定工作人员的午餐时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="e08a2-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-119">Click Add.</span></span>
9. <span data-ttu-id="e08a2-120">在“开始”字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="e08a2-121">指定午餐后重新开始工作的时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="e08a2-122">在“结束”字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="e08a2-123">指定工作日结束的时间。</span><span class="sxs-lookup"><span data-stu-id="e08a2-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="e08a2-124">复制工作时间到所有工作日</span><span class="sxs-lookup"><span data-stu-id="e08a2-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="e08a2-125">单击“复制此日”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-125">Click Copy day.</span></span>
    * <span data-ttu-id="e08a2-126">复制星期一的工作时间定义到星期二。</span><span class="sxs-lookup"><span data-stu-id="e08a2-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="e08a2-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-127">Click OK.</span></span>
3. <span data-ttu-id="e08a2-128">单击“复制此日”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-128">Click Copy day.</span></span>
    * <span data-ttu-id="e08a2-129">复制星期一的工作时间定义到星期三。</span><span class="sxs-lookup"><span data-stu-id="e08a2-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="e08a2-130">在“结束工作日”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="e08a2-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="e08a2-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-131">Click OK.</span></span>
6. <span data-ttu-id="e08a2-132">单击“复制此日”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-132">Click Copy day.</span></span>
    * <span data-ttu-id="e08a2-133">复制星期一的工作时间定义到星期四。</span><span class="sxs-lookup"><span data-stu-id="e08a2-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="e08a2-134">在“结束工作日”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="e08a2-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="e08a2-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-135">Click OK.</span></span>
9. <span data-ttu-id="e08a2-136">单击“复制此日”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-136">Click Copy day.</span></span>
    * <span data-ttu-id="e08a2-137">复制星期一的工作时间定义到星期五。</span><span class="sxs-lookup"><span data-stu-id="e08a2-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="e08a2-138">在“结束工作日”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="e08a2-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="e08a2-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="e08a2-140">定义特殊操作的时隙</span><span class="sxs-lookup"><span data-stu-id="e08a2-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="e08a2-141">展开“星期五”部分。</span><span class="sxs-lookup"><span data-stu-id="e08a2-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="e08a2-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e08a2-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e08a2-143">在“属性”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e08a2-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="e08a2-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e08a2-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e08a2-145">在“属性”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e08a2-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="e08a2-146">标记周末为装货关闭的时间</span><span class="sxs-lookup"><span data-stu-id="e08a2-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="e08a2-147">展开“星期六”部分。</span><span class="sxs-lookup"><span data-stu-id="e08a2-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="e08a2-148">在“停止装货”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="e08a2-149">展开“星期日”部分。</span><span class="sxs-lookup"><span data-stu-id="e08a2-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="e08a2-150">在“停止装货”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e08a2-150">Select Yes in the Closed for pickup field.</span></span>

