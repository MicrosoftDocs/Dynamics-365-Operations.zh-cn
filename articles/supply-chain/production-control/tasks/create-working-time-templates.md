---
title: 创建工作时间模板
description: 工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920920"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="d0e2b-103">创建工作时间模板</span><span class="sxs-lookup"><span data-stu-id="d0e2b-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0e2b-104">工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="d0e2b-105">该过程说明如何使用对工作时间间隔进行分类的工作时间计划属性定义工作时间模板。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="d0e2b-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d0e2b-107">转到 **工作区 > 资源生命周期管理**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="d0e2b-108">选择 **工作时间模板**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="d0e2b-109">创建工作时间模板</span><span class="sxs-lookup"><span data-stu-id="d0e2b-109">Create working time template</span></span>

1. <span data-ttu-id="d0e2b-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-110">Select **New**.</span></span>
1. <span data-ttu-id="d0e2b-111">在 **工作时间模板** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="d0e2b-112">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="d0e2b-113">展开 **星期一** 部分。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="d0e2b-114">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-114">Select **Add**.</span></span>
1. <span data-ttu-id="d0e2b-115">在 **开始** 字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="d0e2b-116">指定上午开始工作的时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="d0e2b-117">在 **结束** 字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="d0e2b-118">指定工作人员的午餐时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="d0e2b-119">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-119">Select **Add**.</span></span>
1. <span data-ttu-id="d0e2b-120">在 **开始** 字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="d0e2b-121">指定午餐后重新开始工作的时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="d0e2b-122">在 **结束** 字段中，输入一个时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="d0e2b-123">指定工作日结束的时间。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="d0e2b-124">复制工作时间到所有工作日</span><span class="sxs-lookup"><span data-stu-id="d0e2b-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="d0e2b-125">选择 **复制日**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="d0e2b-126">复制星期一的工作时间定义到星期二。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="d0e2b-127">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-127">Select **OK**.</span></span>
1. <span data-ttu-id="d0e2b-128">选择 **复制日**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="d0e2b-129">复制星期一的工作时间定义到星期三。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="d0e2b-130">在 **结束工作日** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="d0e2b-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-131">Select **OK**.</span></span>
1. <span data-ttu-id="d0e2b-132">选择 **复制日**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="d0e2b-133">复制星期一的工作时间定义到星期四。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="d0e2b-134">在 **结束工作日** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="d0e2b-135">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-135">Select **OK**.</span></span>
1. <span data-ttu-id="d0e2b-136">选择 **复制日**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="d0e2b-137">复制星期一的工作时间定义到星期五。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="d0e2b-138">在 **结束工作日** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="d0e2b-139">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="d0e2b-140">定义特殊操作的时隙</span><span class="sxs-lookup"><span data-stu-id="d0e2b-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="d0e2b-141">展开 **星期五** 部分。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="d0e2b-142">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d0e2b-143">在 **属性** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="d0e2b-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d0e2b-145">在 **属性** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="d0e2b-146">标记周末为装货关闭的时间</span><span class="sxs-lookup"><span data-stu-id="d0e2b-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="d0e2b-147">展开 **星期六** 部分。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="d0e2b-148">在 **停止装货** 字段中选择 *是*。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="d0e2b-149">展开 **星期日** 部分。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="d0e2b-150">在 **停止装货** 字段中选择 *是*。</span><span class="sxs-lookup"><span data-stu-id="d0e2b-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]