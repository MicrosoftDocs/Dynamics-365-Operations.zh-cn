---
title: 创建替换看板规则
description: 此过程介绍在特定日期将现有看板规则替换为新看板规则。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ded10b0972f07f4f86ee32cee596c5e30b15ebd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843761"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="774fc-103">创建替换看板规则</span><span class="sxs-lookup"><span data-stu-id="774fc-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="774fc-104">此过程介绍在特定日期将现有看板规则替换为新看板规则。</span><span class="sxs-lookup"><span data-stu-id="774fc-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="774fc-105">在生产流或补货规则的更改需要协调和计划时这很有用。</span><span class="sxs-lookup"><span data-stu-id="774fc-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="774fc-106">用于创建过程的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="774fc-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="774fc-107">当他们为更改的生产流或新补货规则准备生产时，该过程面向工艺工程师和价值流经理。</span><span class="sxs-lookup"><span data-stu-id="774fc-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="774fc-108">此任务使用新规则替换看板规则 000022，并且将新规则的最大数量从 48 增加到 100。</span><span class="sxs-lookup"><span data-stu-id="774fc-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="774fc-109">选择要替换的看板规则</span><span class="sxs-lookup"><span data-stu-id="774fc-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="774fc-110">转到“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="774fc-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="774fc-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="774fc-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="774fc-112">选择看板规则 000022。</span><span class="sxs-lookup"><span data-stu-id="774fc-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="774fc-113">创建替换看板规则</span><span class="sxs-lookup"><span data-stu-id="774fc-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="774fc-114">单击“替换看板规则”。</span><span class="sxs-lookup"><span data-stu-id="774fc-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="774fc-115">在“有效日期”字段中输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="774fc-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="774fc-116">选择未来的一个日期，例如从现在起一个星期。</span><span class="sxs-lookup"><span data-stu-id="774fc-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="774fc-117">这是新看板规则生效并取代旧看板规则的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="774fc-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="774fc-118">如果看板规则更改生产流的路径，可以选择另一活动。</span><span class="sxs-lookup"><span data-stu-id="774fc-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="774fc-119">在此过程中，我们将保持活动不改变。</span><span class="sxs-lookup"><span data-stu-id="774fc-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="774fc-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="774fc-120">Click OK.</span></span>
    * <span data-ttu-id="774fc-121">请注意，将创建新的看板规则来替换看板规则 000022。</span><span class="sxs-lookup"><span data-stu-id="774fc-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="774fc-122">生效日期根据您替换看板规则时选择的日期设置。</span><span class="sxs-lookup"><span data-stu-id="774fc-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="774fc-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="774fc-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="774fc-124">选择替换的看板规则 000022。</span><span class="sxs-lookup"><span data-stu-id="774fc-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="774fc-125">请注意，替换的看板规则具有与到期日期相同的日期，因为这是它将到期的日期。</span><span class="sxs-lookup"><span data-stu-id="774fc-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="774fc-126">在列表中，选择第一行 。</span><span class="sxs-lookup"><span data-stu-id="774fc-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="774fc-127">选择列表顶部的新看板规则。</span><span class="sxs-lookup"><span data-stu-id="774fc-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="774fc-128">这是看板规则编号最高的看板规则。</span><span class="sxs-lookup"><span data-stu-id="774fc-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="774fc-129">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="774fc-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="774fc-130">单击看板规则编号打开该看板规则。</span><span class="sxs-lookup"><span data-stu-id="774fc-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="774fc-131">修改替换看板规则的最大数量</span><span class="sxs-lookup"><span data-stu-id="774fc-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="774fc-132">设置最大数量为 '100'。</span><span class="sxs-lookup"><span data-stu-id="774fc-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="774fc-133">展开“数量”快速选项卡查看“最大数量”字段。</span><span class="sxs-lookup"><span data-stu-id="774fc-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="774fc-134">更改最大数量为 100 可以最多处理 100 个看板。</span><span class="sxs-lookup"><span data-stu-id="774fc-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="774fc-135">这是该任务的最后一步。</span><span class="sxs-lookup"><span data-stu-id="774fc-135">This is the last step in this task.</span></span>  

