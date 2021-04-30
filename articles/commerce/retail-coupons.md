---
title: 设置零售销售优惠券
description: 此主题提供优惠券概览并阐述如何进行设置。
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a4de42c23bf96591d1ac99ed32438fe34a485998
ms.sourcegitcommit: 05868764acd3d77970724a30c49c5ae5ffb6ca5b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906641"
---
# <a name="set-up-coupons-for-retail-sales"></a><span data-ttu-id="d6640-103">设置零售销售优惠券</span><span class="sxs-lookup"><span data-stu-id="d6640-103">Set up coupons for retail sales</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a><span data-ttu-id="d6640-104">优惠券概览</span><span class="sxs-lookup"><span data-stu-id="d6640-104">Overview of coupons</span></span>

<span data-ttu-id="d6640-105">优惠券是用于将折扣添加到交易的代码和条码。</span><span class="sxs-lookup"><span data-stu-id="d6640-105">Coupons are codes and bar codes that are used to add discounts to transactions.</span></span> <span data-ttu-id="d6640-106">每张优惠券可以有多个代码，且每个代码可以有自己的有效日期。</span><span class="sxs-lookup"><span data-stu-id="d6640-106">Each coupon can have multiple codes, and each code can have its own effective dates.</span></span>

<span data-ttu-id="d6640-107">每张优惠券都关联一个折扣。</span><span class="sxs-lookup"><span data-stu-id="d6640-107">Each coupon is related to one discount.</span></span> <span data-ttu-id="d6640-108">与折扣关联的价格组定义可以使用优惠券的客户或优惠券有效的渠道。</span><span class="sxs-lookup"><span data-stu-id="d6640-108">The price groups that are associated with the discount define the customers that can use a coupon or the channels where a coupon is valid.</span></span>

<span data-ttu-id="d6640-109">优惠券基本上是折扣顶部的附加验证。</span><span class="sxs-lookup"><span data-stu-id="d6640-109">Essentially, coupons are additional validation on top of discounts.</span></span> <span data-ttu-id="d6640-110">优惠券提供必需的优惠券代码和条码，以及这些代码的日期范围。</span><span class="sxs-lookup"><span data-stu-id="d6640-110">The coupon provides the coupon codes and bar codes that are required, together with date ranges for those codes.</span></span> <span data-ttu-id="d6640-111">优惠券还提供可选使用限制和客户要求的属性。</span><span class="sxs-lookup"><span data-stu-id="d6640-111">The coupon also provides optional usage limits and customer required properties.</span></span> <span data-ttu-id="d6640-112">折扣提供优惠券对其有效的产品集。</span><span class="sxs-lookup"><span data-stu-id="d6640-112">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="d6640-113">折扣的价格组提供优惠券对其有效的客户、渠道或目录集。</span><span class="sxs-lookup"><span data-stu-id="d6640-113">The price groups for the discount provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

<span data-ttu-id="d6640-114">要创建优惠券，须分开创建折扣和优惠券。</span><span class="sxs-lookup"><span data-stu-id="d6640-114">To create a coupon, you create the discount and the coupon separately.</span></span> <span data-ttu-id="d6640-115">之后可以在 Commerce 中通过选择优惠券页面上的折扣将它们关联。</span><span class="sxs-lookup"><span data-stu-id="d6640-115">You then link them by selecting the discount on the coupon page in Commerce.</span></span>

> [!NOTE]
> <span data-ttu-id="d6640-116">优惠券关联到折扣后，Commerce 折扣页上的多个字段变为只读，因为其由优惠券的设置管理。</span><span class="sxs-lookup"><span data-stu-id="d6640-116">After a coupon is linked to a discount, several fields on the discount page in Commerce become read-only, because they are managed by the coupon's settings.</span></span> <span data-ttu-id="d6640-117">这些字段包括用于状态和标准日期范围的字段。</span><span class="sxs-lookup"><span data-stu-id="d6640-117">These fields include the fields for the status and standard date ranges.</span></span>
> 
> <span data-ttu-id="d6640-118">在呼叫中心渠道中使用优惠券时，您需要选择 **重新计算** 按钮 **（“销售”选项卡 > 计算 > 重新计算）**，以便应用关联到优惠券的折扣。</span><span class="sxs-lookup"><span data-stu-id="d6640-118">While using the coupon in the call center channel, you need to select the **Recalculate** button **(Sell tab > Calculate > Recalculate)** in order for the discount associated to the coupon to get applied.</span></span> <span data-ttu-id="d6640-119">此附加步骤将在以后的版本中删除。</span><span class="sxs-lookup"><span data-stu-id="d6640-119">This additional step will be removed in a future release.</span></span>

### <a name="limited-use-coupons"></a><span data-ttu-id="d6640-120">有限使用的优惠券</span><span class="sxs-lookup"><span data-stu-id="d6640-120">Limited-use coupons</span></span>

<span data-ttu-id="d6640-121">优惠券可以配置为有限使用的优惠券。</span><span class="sxs-lookup"><span data-stu-id="d6640-121">Coupons can be configured as limited-use coupons.</span></span> <span data-ttu-id="d6640-122">使用限制可以按客户或渠道进行配置，或配置为全球限制。</span><span class="sxs-lookup"><span data-stu-id="d6640-122">The usage limit can be defined per customer or channel, or as a global limit.</span></span> <span data-ttu-id="d6640-123">在 POS 中或销售订单录入期间输入或扫描代码或条码时执行此限制。</span><span class="sxs-lookup"><span data-stu-id="d6640-123">This limit is enforced when the code or bar code is entered or scanned in POS or during sales order entry.</span></span>

<span data-ttu-id="d6640-124">此限制按优惠券上的优惠券代码执行。</span><span class="sxs-lookup"><span data-stu-id="d6640-124">The limit is enforced per coupon code on a coupon.</span></span> <span data-ttu-id="d6640-125">例如，具有两个优惠券代码的单次使用优惠券可以使用两次：每个优惠券代码可使用一次。</span><span class="sxs-lookup"><span data-stu-id="d6640-125">For example, a single-use coupon that has two coupon codes can be used two times: one time for each coupon code.</span></span> <span data-ttu-id="d6640-126">优惠券上的每个代码可以单独设置为有效。</span><span class="sxs-lookup"><span data-stu-id="d6640-126">Each code on a coupon can be independently set to active.</span></span>

<span data-ttu-id="d6640-127">优惠券可以跨任何销售渠道使用，但是对于呼叫中心订单，限制使用优惠券只能用于那些呼叫中心的 **订单完成** 设置已启用的呼叫中心订单。</span><span class="sxs-lookup"><span data-stu-id="d6640-127">The coupons can be used across any selling channel however, for call center orders, the limited use coupons can be used for only those call centers orders where the **Order completion** setting on the call center is enabled.</span></span> <span data-ttu-id="d6640-128">如果未启用此设置，呼叫中心订单只能使用非限制使用类型的优惠券。</span><span class="sxs-lookup"><span data-stu-id="d6640-128">If this is not enabled, then only non-limited use type coupons can be used in call center orders.</span></span>

> [!NOTE]
> <span data-ttu-id="d6640-129">优惠券达到使用限制后，系统 *不* 自动将优惠券代码的状态更改为“已用”。</span><span class="sxs-lookup"><span data-stu-id="d6640-129">After a coupon code has reached its usage limit, the system does *not* automatically change the status of the coupon code to “Used".</span></span> <span data-ttu-id="d6640-130">但是，该优惠券代码已达到使用限制，无法使用。</span><span class="sxs-lookup"><span data-stu-id="d6640-130">However that coupon code has reached its usage limit and cannot be used.</span></span> <span data-ttu-id="d6640-131">如果将优惠券代码的状态手动设置为除 **活动** 之外的其他状态，则任何渠道均不可使用此优惠券代码。</span><span class="sxs-lookup"><span data-stu-id="d6640-131">If the status of a coupon code is manually set to anything other than **Active**, then this coupon code cannot be used in any channel.</span></span>  

## <a name="managing-coupons"></a><span data-ttu-id="d6640-132">管理优惠券</span><span class="sxs-lookup"><span data-stu-id="d6640-132">Managing coupons</span></span>

<span data-ttu-id="d6640-133">您必须分开创建折扣和优惠券。</span><span class="sxs-lookup"><span data-stu-id="d6640-133">You must create the discount and the coupon separately.</span></span> <span data-ttu-id="d6640-134">之后可以通过选择优惠券页面上的折扣将它们关联。</span><span class="sxs-lookup"><span data-stu-id="d6640-134">You then link them by selecting the discount on the coupon page.</span></span> <span data-ttu-id="d6640-135">将优惠券关联到折扣后，折扣的多个字段变为只读，因为其由优惠券的设置管理。</span><span class="sxs-lookup"><span data-stu-id="d6640-135">After you link a coupon to a discount, several fields for the discount become read-only, because they are managed by the coupon's settings.</span></span> <span data-ttu-id="d6640-136">这些字段包括用于状态和标准日期范围的字段。</span><span class="sxs-lookup"><span data-stu-id="d6640-136">These fields include the fields for the status and standard date ranges.</span></span>

<span data-ttu-id="d6640-137">优惠券现在基本上是折扣顶部的附加验证。</span><span class="sxs-lookup"><span data-stu-id="d6640-137">Essentially, coupons are now additional validation on top of discounts.</span></span> <span data-ttu-id="d6640-138">优惠券提供优惠券代码和条码以及日期范围、使用限制和客户要求的属性。</span><span class="sxs-lookup"><span data-stu-id="d6640-138">The coupon provides the coupon codes and bar codes, together with date ranges, the usage limits, and the customer required property.</span></span> <span data-ttu-id="d6640-139">折扣提供优惠券对其有效的产品集。</span><span class="sxs-lookup"><span data-stu-id="d6640-139">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="d6640-140">折扣的价格组提供优惠券对其有效的客户、渠道或目录集。</span><span class="sxs-lookup"><span data-stu-id="d6640-140">The discount's price groups provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

## <a name="system-setup-for-coupons"></a><span data-ttu-id="d6640-141">优惠券系统创建</span><span class="sxs-lookup"><span data-stu-id="d6640-141">System setup for coupons</span></span>

<span data-ttu-id="d6640-142">在您可以设置优惠券前，必须先设置优惠券条码和两个优惠券编号规则。</span><span class="sxs-lookup"><span data-stu-id="d6640-142">Before you can set up a coupon, you must set up the coupon bar code and two coupon number sequences.</span></span>

1. <span data-ttu-id="d6640-143">在 **掩码字符** 页，为优惠券代码创建新的掩码字符。</span><span class="sxs-lookup"><span data-stu-id="d6640-143">On the **Mask characters** page, create a new mask character for the coupon code.</span></span> <span data-ttu-id="d6640-144">您可以选择任何未使用的字符。</span><span class="sxs-lookup"><span data-stu-id="d6640-144">You can select any unused character.</span></span>
2. <span data-ttu-id="d6640-145">在 **条码掩码设置** 页，创建一个新的条码掩码。</span><span class="sxs-lookup"><span data-stu-id="d6640-145">On the **Bar code mask setup** page, create a new bar code mask.</span></span> <span data-ttu-id="d6640-146">将 **类型** 字段设置为 **优惠券**。</span><span class="sxs-lookup"><span data-stu-id="d6640-146">Set the **Type** field to **Coupon**.</span></span>
3. <span data-ttu-id="d6640-147">在 **条码设置** 页，创建使用您刚才创建的条码掩码的新条码。</span><span class="sxs-lookup"><span data-stu-id="d6640-147">On the **Bar code setup** page, create a new bar code that uses the bar code mask that you just created.</span></span>
4. <span data-ttu-id="d6640-148">在 **编号规则** 页，创建两个新的编号规则。</span><span class="sxs-lookup"><span data-stu-id="d6640-148">On the **Number sequences** page, create two new number sequences.</span></span> <span data-ttu-id="d6640-149">一个规则用于优惠券代码 ID，另一个规则用于优惠券编号。</span><span class="sxs-lookup"><span data-stu-id="d6640-149">One sequence is for the coupon code ID, and the other sequence is for the coupon number.</span></span> <span data-ttu-id="d6640-150">优惠券代码 ID 是优惠券各优惠券代码的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="d6640-150">The coupon code ID is the unique identifier for each coupon code for a coupon.</span></span> <span data-ttu-id="d6640-151">优惠券编号是优惠券的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="d6640-151">The coupon number is the unique identifier for a coupon.</span></span> <span data-ttu-id="d6640-152">每张优惠券可以有多个触发优惠券的代码和条码。</span><span class="sxs-lookup"><span data-stu-id="d6640-152">Each coupon can have multiple codes and bar codes that trigger the coupon.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6640-153">对于这两种编号规则，必须将 **作用域** 字段设置为 **公司**。</span><span class="sxs-lookup"><span data-stu-id="d6640-153">For both number sequences, you must set the **Scope** field to **Company**.</span></span> <span data-ttu-id="d6640-154">在大多数情况下，都应自动生成两个序列号。</span><span class="sxs-lookup"><span data-stu-id="d6640-154">In most cases, you should automatically generate both sequence numbers.</span></span>

5. <span data-ttu-id="d6640-155">在 **商业参数** 页的 **条码** 选项卡上，选择您之前创建的条码。</span><span class="sxs-lookup"><span data-stu-id="d6640-155">On the **Commerce parameters** page, on the **Bar codes** tab, select the bar code that you created earlier.</span></span>
6. <span data-ttu-id="d6640-156">在 **商业共享参数** 页的 **编号规则** 选项卡上，选择您已为优惠券编号和优惠券代码 ID 创建的编号规则。</span><span class="sxs-lookup"><span data-stu-id="d6640-156">On the **Commerce shared parameters** page, on the **Number sequences** tab, select the number sequences that you created for the coupon number and coupon code ID.</span></span>
7. <span data-ttu-id="d6640-157">您现在可以打开 **优惠券** 页和创建新优惠券。</span><span class="sxs-lookup"><span data-stu-id="d6640-157">You can now open the **Coupons** page and create new coupons.</span></span>

## <a name="the-effect-of-partial-updates-on-coupons"></a><span data-ttu-id="d6640-158">部分更新对优惠券的影响</span><span class="sxs-lookup"><span data-stu-id="d6640-158">The effect of partial updates on coupons</span></span>

<span data-ttu-id="d6640-159">优惠券功能包括多个独特功能。</span><span class="sxs-lookup"><span data-stu-id="d6640-159">Coupon functionality comprises multiple distinct features.</span></span> <span data-ttu-id="d6640-160">商业总部 (HQ) 和渠道可以跨组件部分更新。</span><span class="sxs-lookup"><span data-stu-id="d6640-160">Commerce Headquarters (HQ) and the channel can be partially updated across components.</span></span> <span data-ttu-id="d6640-161">因此，了解部分更新对优惠券功能总体的影响十分重要。</span><span class="sxs-lookup"><span data-stu-id="d6640-161">Therefore, it's important that you understand how partial updates affect coupon functionality as a whole.</span></span>

- <span data-ttu-id="d6640-162">**HQ 被部分更新，但 Commerce Scale Unit 和 POS 不更新。**</span><span class="sxs-lookup"><span data-stu-id="d6640-162">**HQ is partially updated, but Commerce Scale Unit and POS aren't updated.**</span></span> <span data-ttu-id="d6640-163">在 HQ 更新中，优惠券和折扣页更新，商业价格引擎也更新。</span><span class="sxs-lookup"><span data-stu-id="d6640-163">In an HQ update, the coupon and discount pages are updated, and the commerce price engine is also updated.</span></span> <span data-ttu-id="d6640-164">如果两个组件中仅有一个更新，则 Commerce 中的部分页面与价格计算数据不匹配。</span><span class="sxs-lookup"><span data-stu-id="d6640-164">If only one of those two components is updated, some pages in Commerce won't match the price calculation data.</span></span> <span data-ttu-id="d6640-165">因此，在折扣计算期间可能发生意外折扣计算或错误。</span><span class="sxs-lookup"><span data-stu-id="d6640-165">Therefore, unexpected discount calculations or errors might occur during discount calculations.</span></span>
- <span data-ttu-id="d6640-166">**HQ 被更新，但 Commerce Scale Unit 和 POS 不更新 (N-1)。**</span><span class="sxs-lookup"><span data-stu-id="d6640-166">**HQ is updated, but Commerce Scale Unit and POS aren't updated (N-1).**</span></span> <span data-ttu-id="d6640-167">由于并非所有的商店都可以同时更新，因此我们建议您在更新商店前更新 HQ。</span><span class="sxs-lookup"><span data-stu-id="d6640-167">Because not all stores can be updated at the same time, we recommend that you update HQ before you update stores.</span></span> <span data-ttu-id="d6640-168">在 N-1 方案中，与优惠券相关的新功能在尚未更新的商店中不可用。</span><span class="sxs-lookup"><span data-stu-id="d6640-168">In the N-1 scenario, new functionality that is related to coupons won't be available in stores that haven't been updated yet.</span></span> <span data-ttu-id="d6640-169">例如，优惠券功能引入“排除”行。</span><span class="sxs-lookup"><span data-stu-id="d6640-169">For example, the coupon functionality introduces "exclude" lines.</span></span> <span data-ttu-id="d6640-170">如果您对折扣使用排除行，则其不会在运行较早版本的商店中应用这些行。</span><span class="sxs-lookup"><span data-stu-id="d6640-170">If you use exclude lines on a discount, they won't be applied in a store that is running an earlier version.</span></span>
- <span data-ttu-id="d6640-171">**HQ 未被更新，但 Commerce Scale Unit 和 POS 被更新 (N+1)。**</span><span class="sxs-lookup"><span data-stu-id="d6640-171">**HQ isn't updated, but Commerce Scale Unit and POS are updated (N+1).**</span></span> <span data-ttu-id="d6640-172">由于在 Commerce Scale Unit 中更新的价格引擎在价格计算期间可以处理旧折扣代码，因此更新应该对此方案没有功能影响。</span><span class="sxs-lookup"><span data-stu-id="d6640-172">Because the updated price engine in Commerce Scale Unit can handle legacy discount codes during price calculations, the update should have no functional impact in this scenario.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
