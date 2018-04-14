--- 
title: "配置成本控制工作区参数"
description: "此过程用于配置“成本控制”工作区，以便组织中各级经理可洞察自己的成本对象，如成本中心和产品组。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1d2448642b0f60f8c060b3fd3e04b22e269814d4
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="fd609-103">配置成本控制工作区参数</span><span class="sxs-lookup"><span data-stu-id="fd609-103">Configure cost control workspace parameters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd609-104">此过程用于配置“成本控制”工作区，以便组织中各级经理可洞察自己的成本对象，如成本中心和产品组。</span><span class="sxs-lookup"><span data-stu-id="fd609-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="fd609-105">USP2 演示公司用于创建此录制。</span><span class="sxs-lookup"><span data-stu-id="fd609-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="fd609-106">转至“成本核算”>“设置”>“成本控制工作区配置”。</span><span class="sxs-lookup"><span data-stu-id="fd609-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="fd609-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="fd609-107">Click New.</span></span>
3. <span data-ttu-id="fd609-108">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fd609-109">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fd609-110">在“已发布”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fd609-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="fd609-111">如果将此选项设置为“是”，为其分配了以下角色之一的用户可查看“成本控制”工作区中的报表：成本核算经理、成本会计师、成本核算师和成本对象总监。</span><span class="sxs-lookup"><span data-stu-id="fd609-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="fd609-112">如果将此选项设置为“否”，只有为其分配了以下角色之一的用户可查看“成本控制”工作区中的报表：成本核算经理、成本会计师或成本核算师。</span><span class="sxs-lookup"><span data-stu-id="fd609-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="fd609-113">展开“数据筛选”部分。</span><span class="sxs-lookup"><span data-stu-id="fd609-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="fd609-114">在“成本控制单元”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="fd609-115">在“预算原始版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="fd609-116">在“成本元素维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="fd609-117">在“成本对象维度层次结构”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="fd609-118">展开“分配计算记录”部分。</span><span class="sxs-lookup"><span data-stu-id="fd609-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="fd609-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="fd609-119">Click New.</span></span>
13. <span data-ttu-id="fd609-120">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="fd609-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="fd609-121">在“会计日历期间”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="fd609-122">在“实际版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="fd609-123">展开“每列的会计期间”部分。</span><span class="sxs-lookup"><span data-stu-id="fd609-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="fd609-124">在“当前期间”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fd609-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="fd609-125">展开“为成本显示的列”部分。</span><span class="sxs-lookup"><span data-stu-id="fd609-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="fd609-126">在“固定成本”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fd609-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="fd609-127">在“可变成本”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fd609-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="fd609-128">在“总成本”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fd609-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="fd609-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fd609-129">Click Save.</span></span>
23. <span data-ttu-id="fd609-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fd609-130">Close the page.</span></span>
24. <span data-ttu-id="fd609-131">转至“成本核算”>“工作区”>“成本控制”。</span><span class="sxs-lookup"><span data-stu-id="fd609-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="fd609-132">选择报表以查看所选会计期间的固定成本、可变成本、总成本和未分类的成本。</span><span class="sxs-lookup"><span data-stu-id="fd609-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="fd609-133">在“会计日历期间”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="fd609-134">在“成本对象维度层次结构节点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fd609-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fd609-135">选择“成本对象维度层次结构”之后，展开“成本元素维度层次结构”以查看所需成本值。</span><span class="sxs-lookup"><span data-stu-id="fd609-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="fd609-136">例如，可以将层次结构展开到“制造开销”以查看值。</span><span class="sxs-lookup"><span data-stu-id="fd609-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  


