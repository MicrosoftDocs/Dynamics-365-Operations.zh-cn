---
title: 更改处理作业的看板规则
description: 该过程旨在更改一个给定看板的惯用看板规则。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba77197f51b871f452c2aa94320aa2a68cf314df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255365"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="8620f-103">更改处理作业的看板规则</span><span class="sxs-lookup"><span data-stu-id="8620f-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8620f-104">该过程旨在更改一个给定看板的惯用看板规则。</span><span class="sxs-lookup"><span data-stu-id="8620f-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="8620f-105">此适用于水平负荷资源以及万一出现故障的情况。</span><span class="sxs-lookup"><span data-stu-id="8620f-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="8620f-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="8620f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8620f-107">该过程是为 lean manufacturing 公司的生产规划人员设计的，为价值流负责。</span><span class="sxs-lookup"><span data-stu-id="8620f-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="8620f-108">复制看板规则</span><span class="sxs-lookup"><span data-stu-id="8620f-108">Copy kanban rule</span></span>
1. <span data-ttu-id="8620f-109">转到“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="8620f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="8620f-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8620f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8620f-111">选择“事件看板规则”000022 至 L0001。</span><span class="sxs-lookup"><span data-stu-id="8620f-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="8620f-112">单击“复制看板规则”。</span><span class="sxs-lookup"><span data-stu-id="8620f-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="8620f-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8620f-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="8620f-114">更改看板规则</span><span class="sxs-lookup"><span data-stu-id="8620f-114">Change kanban rule</span></span>
1. <span data-ttu-id="8620f-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8620f-115">Close the page.</span></span>
2. <span data-ttu-id="8620f-116">转到“看板作业计划”。</span><span class="sxs-lookup"><span data-stu-id="8620f-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="8620f-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8620f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8620f-118">选择看板 000177 行。</span><span class="sxs-lookup"><span data-stu-id="8620f-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="8620f-119">单击“使用备选看板规则”。</span><span class="sxs-lookup"><span data-stu-id="8620f-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="8620f-120">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="8620f-120">Click Next.</span></span>
6. <span data-ttu-id="8620f-121">在“看板规则”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8620f-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="8620f-122">选择之前所创建的看板规则。</span><span class="sxs-lookup"><span data-stu-id="8620f-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="8620f-123">这是看板规则的最高值。</span><span class="sxs-lookup"><span data-stu-id="8620f-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="8620f-124">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="8620f-124">Click Finish.</span></span>
    * <span data-ttu-id="8620f-125">现在该看板作业正在使用另一种看板规则。</span><span class="sxs-lookup"><span data-stu-id="8620f-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="8620f-126">此适用于水平负荷工作单元。</span><span class="sxs-lookup"><span data-stu-id="8620f-126">This can be useful to level load work cells.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]