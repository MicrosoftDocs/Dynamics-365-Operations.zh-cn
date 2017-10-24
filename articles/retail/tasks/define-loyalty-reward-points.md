--- 
title: "定义会员奖励分"
description: "此程序会逐步演示如何定义会员奖励积分。"
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05237a0ba3aa785432c8b1fc36284a47f9aabd4a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="fd36e-103">定义会员奖励分</span><span class="sxs-lookup"><span data-stu-id="fd36e-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fd36e-104">此程序会逐步演示如何定义会员奖励积分。</span><span class="sxs-lookup"><span data-stu-id="fd36e-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="fd36e-105">在设置会员计划之前，您应设置会员奖励积分。</span><span class="sxs-lookup"><span data-stu-id="fd36e-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="fd36e-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="fd36e-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="fd36e-107">转至“零售和商业”>“客户”>“会员”>“会员奖励积分”。</span><span class="sxs-lookup"><span data-stu-id="fd36e-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="fd36e-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="fd36e-108">Click New.</span></span>
3. <span data-ttu-id="fd36e-109">在“奖励积分 ID”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="fd36e-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="fd36e-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fd36e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fd36e-111">在“奖励积分类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="fd36e-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="fd36e-112">如果您想要将奖励积分舍入到最近的整数，请选择“数量”。</span><span class="sxs-lookup"><span data-stu-id="fd36e-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="fd36e-113">如果您想要根据币种舍入规则对奖励积分进行舍入，请选择“金额”。</span><span class="sxs-lookup"><span data-stu-id="fd36e-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="fd36e-114">如果您选择“数量”，请跳过此程序的下一步。</span><span class="sxs-lookup"><span data-stu-id="fd36e-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="fd36e-115">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fd36e-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="fd36e-116">对于金额类型奖励积分，发放的所有积分都将拥有选定的币种。</span><span class="sxs-lookup"><span data-stu-id="fd36e-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="fd36e-117">对于数量类型奖励积分，此字段不适用，跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="fd36e-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="fd36e-118">选中或取消选中“可兑换”复选框。</span><span class="sxs-lookup"><span data-stu-id="fd36e-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="fd36e-119">在“兑换排名”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fd36e-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="fd36e-120">在两个或多个可兑换的奖励积分可用于支付产品货款时，使用兑换排名。</span><span class="sxs-lookup"><span data-stu-id="fd36e-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="fd36e-121">如果两个奖励积分拥有相同的兑换排名，则使用需要较少积分数的奖励积分。</span><span class="sxs-lookup"><span data-stu-id="fd36e-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="fd36e-122">在“到期时间值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fd36e-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="fd36e-123">奖励积分将在积分发放的指定天数、月数或年数之后过期。</span><span class="sxs-lookup"><span data-stu-id="fd36e-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="fd36e-124">值为“0”意味着会员奖励积分将永不过期。</span><span class="sxs-lookup"><span data-stu-id="fd36e-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="fd36e-125">在“到期时间单位”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="fd36e-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="fd36e-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fd36e-126">Click Save.</span></span>


