---
title: 定义会员计划
description: 此程序会显示如何设置一个带有两个会员层级的会员计划。
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e57bb9c9e3348f2a9853dfda1351a8a75261beb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "355303"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="509c4-103">定义会员计划</span><span class="sxs-lookup"><span data-stu-id="509c4-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="509c4-104">此程序会显示如何设置一个带有两个会员层级的会员计划。</span><span class="sxs-lookup"><span data-stu-id="509c4-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="509c4-105">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="509c4-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="509c4-106">转至“零售和商业”></span><span class="sxs-lookup"><span data-stu-id="509c4-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="509c4-107">>“会员计划”。</span><span class="sxs-lookup"><span data-stu-id="509c4-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="509c4-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="509c4-108">Click New.</span></span>
3. <span data-ttu-id="509c4-109">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="509c4-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="509c4-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="509c4-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="509c4-111">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="509c4-111">Click Add line.</span></span>
6. <span data-ttu-id="509c4-112">在“水平”字段，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="509c4-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="509c4-113">在“层”字段中，输入会员层级的名称。</span><span class="sxs-lookup"><span data-stu-id="509c4-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="509c4-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="509c4-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="509c4-115">在“日期区间”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="509c4-116">此日期区间应延展到未来。</span><span class="sxs-lookup"><span data-stu-id="509c4-116">This date interval should extend into the future.</span></span> <span data-ttu-id="509c4-117">例如，如果黄金层级选择的日期区间为一年，所有符合该黄金层级的客户可以获得一年分配给该层的奖励。</span><span class="sxs-lookup"><span data-stu-id="509c4-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="509c4-118">如果在该层级的客户重新符合黄金层级，则该客户层状态到期日期延伸到另一年，开始日期从客户重新符合黄金层级计算。</span><span class="sxs-lookup"><span data-stu-id="509c4-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="509c4-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="509c4-120">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="509c4-120">Click Add line.</span></span>
12. <span data-ttu-id="509c4-121">在“水平”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="509c4-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="509c4-122">在“层”字段中，输入会员层级的名称。</span><span class="sxs-lookup"><span data-stu-id="509c4-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="509c4-123">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="509c4-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="509c4-124">在“日期区间”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="509c4-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="509c4-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="509c4-126">Click Save.</span></span>
18. <span data-ttu-id="509c4-127">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="509c4-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="509c4-128">层级规则定义了在符合该层级的时间内需要获得的最小奖励积分数。</span><span class="sxs-lookup"><span data-stu-id="509c4-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="509c4-129">切换“层规则”部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="509c4-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="509c4-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="509c4-130">Click New.</span></span>
    * <span data-ttu-id="509c4-131">您可以为每个层级设置多个层级规则。</span><span class="sxs-lookup"><span data-stu-id="509c4-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="509c4-132">例如，您可以设置三个不同的条件来获得一个层级：每个月花费 500 美元，一年花费 1000 美元和一年拥有 20 个交易。</span><span class="sxs-lookup"><span data-stu-id="509c4-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="509c4-133">为此，您需要创建三个层级规则。</span><span class="sxs-lookup"><span data-stu-id="509c4-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="509c4-134">在“奖励积分”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="509c4-135">这应是不可兑换的会员奖励积分。</span><span class="sxs-lookup"><span data-stu-id="509c4-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="509c4-136">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="509c4-137">在“发放的最小点数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="509c4-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="509c4-138">如果通过参与该计划，所有客户均可轻松符合最低层级，则输入 0。</span><span class="sxs-lookup"><span data-stu-id="509c4-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="509c4-139">在“评估日期区间”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="509c4-140">此日期区间应延展到过去。</span><span class="sxs-lookup"><span data-stu-id="509c4-140">This date interval should extend into the past.</span></span> <span data-ttu-id="509c4-141">将仅使用在此日期区间内获得的积分来计算是否达到最小发放积分值。</span><span class="sxs-lookup"><span data-stu-id="509c4-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="509c4-142">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="509c4-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="509c4-143">Click Save.</span></span>
27. <span data-ttu-id="509c4-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="509c4-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="509c4-145">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="509c4-145">Click New.</span></span>
29. <span data-ttu-id="509c4-146">在“奖励积分”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="509c4-147">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="509c4-148">在“发放的最小点数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="509c4-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="509c4-149">在“评估日期区间”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="509c4-150">此日期区间应延展到过去。</span><span class="sxs-lookup"><span data-stu-id="509c4-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="509c4-151">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="509c4-152">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="509c4-152">Click Save.</span></span>
35. <span data-ttu-id="509c4-153">单击“价格组”。</span><span class="sxs-lookup"><span data-stu-id="509c4-153">Click Price groups.</span></span>
    * <span data-ttu-id="509c4-154">如果您想要给予会员客户折扣，</span><span class="sxs-lookup"><span data-stu-id="509c4-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="509c4-155">您需要将一个或多个价格组分配给会员计划，并将多个价格组分配给折扣。</span><span class="sxs-lookup"><span data-stu-id="509c4-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="509c4-156">最佳做法是不要在不同实体类型之间混合价格组。</span><span class="sxs-lookup"><span data-stu-id="509c4-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="509c4-157">例如，不要将同一价格组用于会员折扣和渠道折扣。</span><span class="sxs-lookup"><span data-stu-id="509c4-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="509c4-158">在“价格组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="509c4-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="509c4-159">页面顶部价格组链接用于会员计划。</span><span class="sxs-lookup"><span data-stu-id="509c4-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="509c4-160">“计划层”快速选项卡中的价格组链接仅供特定会员层级使用。</span><span class="sxs-lookup"><span data-stu-id="509c4-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="509c4-161">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="509c4-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="509c4-162">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="509c4-162">Click Save.</span></span>
39. <span data-ttu-id="509c4-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="509c4-163">Close the page.</span></span>
40. <span data-ttu-id="509c4-164">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="509c4-164">Click Save.</span></span>

