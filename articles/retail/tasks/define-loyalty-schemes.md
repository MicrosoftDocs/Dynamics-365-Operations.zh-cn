--- 
title: "定义会员方案"
description: "此程序会逐步演示如何定义会员方案。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 203f952eb9cf346cf5e8c97f9dab874d536e2e24
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="define-loyalty-schemes"></a><span data-ttu-id="73499-103">定义会员方案</span><span class="sxs-lookup"><span data-stu-id="73499-103">Define loyalty schemes</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="73499-104">此程序会逐步演示如何定义会员方案。</span><span class="sxs-lookup"><span data-stu-id="73499-104">This procedure walks through how to define a loyalty scheme.</span></span> <span data-ttu-id="73499-105">会员方案是会员计划的奖励获得和兑换规则。</span><span class="sxs-lookup"><span data-stu-id="73499-105">Loyalty schemes are reward earning and redeeming rules for a loyalty program.</span></span> <span data-ttu-id="73499-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="73499-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="73499-107">转至“零售和商业”>“客户”>“会员”>“会员方案”。</span><span class="sxs-lookup"><span data-stu-id="73499-107">Go to Retail and commerce > Customers > Loyalty > Loyalty schemes.</span></span>
2. <span data-ttu-id="73499-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="73499-108">Click New.</span></span>
3. <span data-ttu-id="73499-109">在“方案 ID”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="73499-109">In the Scheme ID field, type a value.</span></span>
4. <span data-ttu-id="73499-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="73499-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="73499-111">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="73499-111">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73499-112">您可以为某一会员计划设置多个会员方案。</span><span class="sxs-lookup"><span data-stu-id="73499-112">You can have multiple loyalty schemes for a loyalty program.</span></span> <span data-ttu-id="73499-113">会员方案可以用于所有渠道，或仅用于某一渠道子集。</span><span class="sxs-lookup"><span data-stu-id="73499-113">Loyalty schemes can be for all channels or only a sub-set of channels.</span></span>  
6. <span data-ttu-id="73499-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="73499-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="73499-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="73499-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="73499-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="73499-116">Click Save.</span></span>
9. <span data-ttu-id="73499-117">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="73499-117">Click Add line.</span></span>
10. <span data-ttu-id="73499-118">在“活动类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="73499-118">In the Activity type field, select an option.</span></span>
    * <span data-ttu-id="73499-119">如果您希望客户基于其花费的金额获得奖励，选择“按金额购买产品”。</span><span class="sxs-lookup"><span data-stu-id="73499-119">Select Purchase products by amount if you want customers to earn rewards based on how much they spend.</span></span> <span data-ttu-id="73499-120">如果您希望客户基于其购买的产品数量获得奖励，选择“按数量购买产品”。</span><span class="sxs-lookup"><span data-stu-id="73499-120">Select Purchase products by quantity if you want customers to earn rewards based on how many products they buy.</span></span>  <span data-ttu-id="73499-121">如果您希望客户获得每个销售交易的奖励，而不考虑购买什么或花费多少金额，请选择“销售交易记录计数”。</span><span class="sxs-lookup"><span data-stu-id="73499-121">Select Sales transaction count if you want customers to earn rewards for each sales transaction, regardless of what or how much is purchased.</span></span>  
    * <span data-ttu-id="73499-122">选择类别。</span><span class="sxs-lookup"><span data-stu-id="73499-122">Select a category.</span></span> <span data-ttu-id="73499-123">类别将会限制此获得规则适用于哪些产品。</span><span class="sxs-lookup"><span data-stu-id="73499-123">The category will limit which products this earning rule applies to.</span></span>  
    * <span data-ttu-id="73499-124">如果您希望该获得规则适用于所有客户，则将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="73499-124">If you want the earning rule to apply to all products, leave this field blank.</span></span>  
11. <span data-ttu-id="73499-125">在“活动金额/数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="73499-125">In the Activity amount/quantity field, enter a number.</span></span>
    *  <span data-ttu-id="73499-126">对于“销售交易记录计数”活动类型，您应始终使用值“1.0”。</span><span class="sxs-lookup"><span data-stu-id="73499-126">For activity type Sales transaction count, you should always use a value of '1.0'.</span></span> <span data-ttu-id="73499-127">对于“按金额购买”或“按数量购买”活动类型，低于输入值的任何交易都不会触发获得规则。</span><span class="sxs-lookup"><span data-stu-id="73499-127">For activity types of Purchase by amount or Purchase by quantity, any transaction that is less than the value entered will not trigger the earning rule.</span></span> <span data-ttu-id="73499-128">例如，如果活动类型是“按金额购买”，并且您输入“10.00”，则“9.00”的销售交易不会获得此获得规则的奖励。</span><span class="sxs-lookup"><span data-stu-id="73499-128">For example, if the activity type is Purchase by amount, and you enter '10.00', then a sales transaction for '9.00' will not earn rewards for this earning rule.</span></span>  
12. <span data-ttu-id="73499-129">在“活动货币”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="73499-129">In the Activity currency field, type a value.</span></span>
13. <span data-ttu-id="73499-130">在“奖励积分 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="73499-130">In the Reward point ID field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="73499-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="73499-131">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="73499-132">在“奖励积分”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="73499-132">In the Reward points field, enter a number.</span></span>
    * <span data-ttu-id="73499-133">金额类型奖励积分将记录已获得的小数点形式的积分量。</span><span class="sxs-lookup"><span data-stu-id="73499-133">Amount type reward points will record earned amounts with decimals.</span></span> <span data-ttu-id="73499-134">例如，如果获得规则规定每花费 1 加拿大元即可获得 1 分奖励积分，且客户花费 1.25 加拿大元，则该客户将获 1.25 分奖励积分。</span><span class="sxs-lookup"><span data-stu-id="73499-134">For example, if the earning rule states 1 reward point earned for every 1 Canadian Dollar spent, and the customer spends 1.25 Canadian Dollars, then the customer will earn 1.25 reward points.</span></span> <span data-ttu-id="73499-135">数量类型奖励积分将记录已获得的整数形式的积分量。</span><span class="sxs-lookup"><span data-stu-id="73499-135">Quantity type reward points will record earned amounts in integers.</span></span> <span data-ttu-id="73499-136">使用示例，其中获得规则规定每花费 1 加拿大元即可获得 1 分奖励积分，且客户花费 1.25 加拿大元，则该客户将获 1.0 分奖励积分。</span><span class="sxs-lookup"><span data-stu-id="73499-136">Using the example where the earning rule states 1 reward point earned for every 1 Canadian Dollar spent, and the customer spends 1.25 Canadian Dollars, then the customer will earn 1.0 reward points.</span></span>  
16. <span data-ttu-id="73499-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="73499-137">Click Save.</span></span>
17. <span data-ttu-id="73499-138">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="73499-138">Click Add line.</span></span>
    * <span data-ttu-id="73499-139">兑换规则在使用会员付款方式时使用。</span><span class="sxs-lookup"><span data-stu-id="73499-139">Redemption rules are used when the loyalty payment method is used.</span></span>  
18. <span data-ttu-id="73499-140">在“奖励积分 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="73499-140">In the Reward point ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73499-141">仅显示可兑换的奖励积分。</span><span class="sxs-lookup"><span data-stu-id="73499-141">Only redeemable reward points are shown.</span></span>  
19. <span data-ttu-id="73499-142">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="73499-142">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="73499-143">在“奖励积分”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="73499-143">In the Reward points field, enter a number.</span></span>
21. <span data-ttu-id="73499-144">在“兑换类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="73499-144">In the Redemption type field, select an option.</span></span>
    * <span data-ttu-id="73499-145">选择“按金额付款”会导致“金额或数量”字段被视为一个币值。</span><span class="sxs-lookup"><span data-stu-id="73499-145">Selecting Payment by amount causes the Amount or quantity field to be treated as a currency value.</span></span> <span data-ttu-id="73499-146">在这种情况下，按付款币种单位使用的奖励积分金额是一个固定比率。</span><span class="sxs-lookup"><span data-stu-id="73499-146">In this case, the amount of reward points used per currency unit of payment is a fixed ratio.</span></span> <span data-ttu-id="73499-147">选择“按数量付款”会导致“金额或数量”字段被视为一个数量值。</span><span class="sxs-lookup"><span data-stu-id="73499-147">Selecting Payment by quantity causes the Amount or quantity field to be treated as a quantity value.</span></span> <span data-ttu-id="73499-148">在这种情况下，按物料数量使用的奖励积分金额是一个固定比率，但是，如果在数量相同的情况下，附赠会员奖励积分的物料支付价格有所不同，则货币金额会各不相同。</span><span class="sxs-lookup"><span data-stu-id="73499-148">In this case, the amount of reward points used per item quantity is a fixed ratio, however, the amount in currency can vary if the price of items paid for with loyalty reward points varies for the same quantity.</span></span> <span data-ttu-id="73499-149">只有在启用“俄罗斯”国家/地区的特定功能配置密钥，且 POS 功能配置文件拥有“RU”这一 ISO 代码时，会员积分折扣的兑换类型才有效。</span><span class="sxs-lookup"><span data-stu-id="73499-149">Redemption type of Loyalty points discount is only valid when the 'Russia' Country/Regional specific features configuration key is enabled, and the POS functionality profiles has an ISO code of 'RU'.</span></span>  
    * <span data-ttu-id="73499-150">选择类别。</span><span class="sxs-lookup"><span data-stu-id="73499-150">Select a category.</span></span> <span data-ttu-id="73499-151">类别将会限制此兑换规则适用于哪些产品。</span><span class="sxs-lookup"><span data-stu-id="73499-151">The category will limit which products this redemption rule applies to.</span></span>  
    * <span data-ttu-id="73499-152">如果您希望该兑换规则适用于所有客户，则将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="73499-152">If you want the redemption rule to apply to all products, leave this field blank.</span></span>  
22. <span data-ttu-id="73499-153">在“金额或数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="73499-153">In the Amount or quantity field, enter a number.</span></span>
23. <span data-ttu-id="73499-154">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="73499-154">In the Currency field, type a value.</span></span>
24. <span data-ttu-id="73499-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="73499-155">Click Save.</span></span>
25. <span data-ttu-id="73499-156">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="73499-156">Click Add line.</span></span>
    * <span data-ttu-id="73499-157">从可用的组织节点列表中选择一个或多个节点，并通过单击两个列表之间的箭头，将它们移到选定组织节点列表中。</span><span class="sxs-lookup"><span data-stu-id="73499-157">Select one or more nodes from the Available organization nodes list and move them to the Selected organization nodes list by clicking the arrow between the two lists.</span></span>  
26. <span data-ttu-id="73499-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="73499-158">Click OK.</span></span>
27. <span data-ttu-id="73499-159">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="73499-159">Click Save.</span></span>
    * <span data-ttu-id="73499-160">但凡要更改会员方案的渠道，您必须运行“处理会员方案”。</span><span class="sxs-lookup"><span data-stu-id="73499-160">Anytime you change the channels for a loyalty scheme, you must run Process loyalty schemes.</span></span> <span data-ttu-id="73499-161">如此，渠道将会获得更新的会员方案。</span><span class="sxs-lookup"><span data-stu-id="73499-161">That way, the channels will get updated loyalty schemes.</span></span>  


