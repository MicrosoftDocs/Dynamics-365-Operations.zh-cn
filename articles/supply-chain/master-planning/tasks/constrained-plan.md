---
title: 生成受约束计划
description: 此主题介绍如何创建涉及物料和产能限制的计划。
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808008"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="9b749-103">生成受约束计划</span><span class="sxs-lookup"><span data-stu-id="9b749-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b749-104">此主题介绍如何创建涉及物料和产能限制的计划。</span><span class="sxs-lookup"><span data-stu-id="9b749-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="9b749-105">计划确保，在制造物料可用且资源未超额认购之前，不进行生产。</span><span class="sxs-lookup"><span data-stu-id="9b749-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="9b749-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="9b749-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9b749-107">此程序是专为生产规划员设计的。</span><span class="sxs-lookup"><span data-stu-id="9b749-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="9b749-108">设置约束计划</span><span class="sxs-lookup"><span data-stu-id="9b749-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="9b749-109">在主页中，选择 **主计划** 工作区。</span><span class="sxs-lookup"><span data-stu-id="9b749-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="9b749-110">选择工作区最右侧链接列表中的 **主计划**。</span><span class="sxs-lookup"><span data-stu-id="9b749-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="9b749-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9b749-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="9b749-112">示例：**StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="9b749-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="9b749-113">在 **有限产能** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b749-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="9b749-114">在 **有限产能时限** 字段中，输入 `30`。</span><span class="sxs-lookup"><span data-stu-id="9b749-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="9b749-115">展开 **按天计算的时限** 部分。</span><span class="sxs-lookup"><span data-stu-id="9b749-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="9b749-116">在 **产能** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b749-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="9b749-117">在 **产能计划时限（以天为单位）** 字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="9b749-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="9b749-118">示例: `60`</span><span class="sxs-lookup"><span data-stu-id="9b749-118">Example: `60`</span></span>  
9. <span data-ttu-id="9b749-119">在 **计划延迟** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b749-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="9b749-120">在 **计划延迟时限（以天为单位）** 字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="9b749-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="9b749-121">示例: `60`</span><span class="sxs-lookup"><span data-stu-id="9b749-121">Example: `60`</span></span> 
11. <span data-ttu-id="9b749-122">展开 **计算的延迟** 部分。</span><span class="sxs-lookup"><span data-stu-id="9b749-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="9b749-123">在所有 **添加计算的延迟到需求日期** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b749-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="9b749-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b749-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="9b749-125">创建约束计划</span><span class="sxs-lookup"><span data-stu-id="9b749-125">Create a constrained plan</span></span>
1. <span data-ttu-id="9b749-126">选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="9b749-126">Select **Run**.</span></span>
2. <span data-ttu-id="9b749-127">在 **主计划** 字段中，输入或选择要为其设置约束的计划。</span><span class="sxs-lookup"><span data-stu-id="9b749-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="9b749-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b749-128">Select **OK**.</span></span>
4. <span data-ttu-id="9b749-129">选择 **计划订单**。</span><span class="sxs-lookup"><span data-stu-id="9b749-129">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]