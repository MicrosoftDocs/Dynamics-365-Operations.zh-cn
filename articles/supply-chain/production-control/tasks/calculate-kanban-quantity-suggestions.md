---
title: 计算看板数量建议
description: 此过程重点是通过使用看板数量计算，优化特定看板规则的看板大小和数量。
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 540dd32c5da5859ef5e69f55d6806eada90bc840
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "348978"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="f59c1-103">计算看板数量建议</span><span class="sxs-lookup"><span data-stu-id="f59c1-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f59c1-104">此过程重点是通过使用看板数量计算，优化特定看板规则的看板大小和数量。</span><span class="sxs-lookup"><span data-stu-id="f59c1-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="f59c1-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f59c1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f59c1-106">此程序是专为价值流经理设计的。</span><span class="sxs-lookup"><span data-stu-id="f59c1-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="f59c1-107">这是您完成“添加新看板数量计算策略到看到规则”这一过程的先决条件。</span><span class="sxs-lookup"><span data-stu-id="f59c1-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="f59c1-108">创建看板数量计算</span><span class="sxs-lookup"><span data-stu-id="f59c1-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="f59c1-109">转到“生产控制”>“定期任务”>“看板数量计算”>“计算看板数量”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="f59c1-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-110">Click New.</span></span>
3. <span data-ttu-id="f59c1-111">在“名称”字段中，键入“Speaker2016”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="f59c1-112">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f59c1-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f59c1-113">选择您在“添加新看板数量计算策略到看板规则”这一过程中创建的策略。</span><span class="sxs-lookup"><span data-stu-id="f59c1-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="f59c1-114">例如，Speaker2016。</span><span class="sxs-lookup"><span data-stu-id="f59c1-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="f59c1-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f59c1-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f59c1-116">在“规则有效截止日期”字段，设置日期和时间为“2012-12-17T08:00:00”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="f59c1-117">此日期用作确定要包括在看板数量计算中的固定看板规则基础。</span><span class="sxs-lookup"><span data-stu-id="f59c1-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="f59c1-118">在“已履行需求期间开始日期”字段，设置日期和时间为“2012-11-17T09:00:00”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="f59c1-119">包括过去需求交易记录以计算看板数量的开始日期。</span><span class="sxs-lookup"><span data-stu-id="f59c1-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="f59c1-120">在“已履行需求期间结束日期”字段，设置日期和时间为“2012-12-17T07:59:59”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="f59c1-121">包括过去需求交易记录以计算看板数量的截止日期。</span><span class="sxs-lookup"><span data-stu-id="f59c1-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="f59c1-122">在“需求期间开始日期”字段，设置日期和时间为“2012-12-17T08:00:00”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="f59c1-123">包括当前需求交易记录以计算固定看板数量的开始日期。</span><span class="sxs-lookup"><span data-stu-id="f59c1-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="f59c1-124">在“需求期间结束日期”字段，设置日期和时间为“2013-01-16T07:59:59”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="f59c1-125">包括当前需求交易记录以计算看板数量的截止日期。</span><span class="sxs-lookup"><span data-stu-id="f59c1-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="f59c1-126">生成看板数量方案</span><span class="sxs-lookup"><span data-stu-id="f59c1-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="f59c1-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-127">Click Save.</span></span>
2. <span data-ttu-id="f59c1-128">单击“生成”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-128">Click Generate.</span></span>
    * <span data-ttu-id="f59c1-129">这将生成 000020 看板规则的看板数量方案行。</span><span class="sxs-lookup"><span data-stu-id="f59c1-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="f59c1-130">运行看板数量计算</span><span class="sxs-lookup"><span data-stu-id="f59c1-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="f59c1-131">单击“计算”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-131">Click Calculate.</span></span>
    * <span data-ttu-id="f59c1-132">此计算看板数量方案。</span><span class="sxs-lookup"><span data-stu-id="f59c1-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="f59c1-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-133">Click OK.</span></span>
3. <span data-ttu-id="f59c1-134">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f59c1-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f59c1-135">请注意，建议的看板数量为 2。</span><span class="sxs-lookup"><span data-stu-id="f59c1-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="f59c1-136">更改产品数量并重新计算</span><span class="sxs-lookup"><span data-stu-id="f59c1-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="f59c1-137">将产品数量设置为“5”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="f59c1-138">单击“计算”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-138">Click Calculate.</span></span>
3. <span data-ttu-id="f59c1-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-139">Click OK.</span></span>
    * <span data-ttu-id="f59c1-140">请注意，如果看板数量为 5，建议更改为 4。</span><span class="sxs-lookup"><span data-stu-id="f59c1-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="f59c1-141">这由实际产品数量低引起，我们需要更多看板来满足需求。</span><span class="sxs-lookup"><span data-stu-id="f59c1-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="f59c1-142">更新看板规则</span><span class="sxs-lookup"><span data-stu-id="f59c1-142">Update kanban rule</span></span>
1. <span data-ttu-id="f59c1-143">在“规则生效日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f59c1-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="f59c1-144">将“规则有效截止日期”设置为未来日期。</span><span class="sxs-lookup"><span data-stu-id="f59c1-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="f59c1-145">例如，今天 + 一年。</span><span class="sxs-lookup"><span data-stu-id="f59c1-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="f59c1-146">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-146">Click Update.</span></span>
3. <span data-ttu-id="f59c1-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-147">Click OK.</span></span>
4. <span data-ttu-id="f59c1-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f59c1-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="f59c1-149">验证看板规则的更改</span><span class="sxs-lookup"><span data-stu-id="f59c1-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="f59c1-150">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="f59c1-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f59c1-151">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f59c1-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f59c1-152">选择在上一子任务中创建的看板规则。</span><span class="sxs-lookup"><span data-stu-id="f59c1-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="f59c1-153">这应该是按编号排序的列表中的第一个看板规则。</span><span class="sxs-lookup"><span data-stu-id="f59c1-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="f59c1-154">切换“详细信息”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="f59c1-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="f59c1-155">请注意，生效日期指规则在此日期前未生效。</span><span class="sxs-lookup"><span data-stu-id="f59c1-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="f59c1-156">切换“数量”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="f59c1-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="f59c1-157">请注意，这是您在看板数量计算中输入的默认数量。</span><span class="sxs-lookup"><span data-stu-id="f59c1-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="f59c1-158">请注意，这是来自看板数量计算的固定看板数量 4.</span><span class="sxs-lookup"><span data-stu-id="f59c1-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="f59c1-159">单击“列表面板”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f59c1-159">Click the ListPanel tab.</span></span>

