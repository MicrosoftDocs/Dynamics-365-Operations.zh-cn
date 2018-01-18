---
title: "创建零售销售优惠券"
description: "此主题提供零售优惠券概览并阐述如何进行设置。"
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 8e0ef5e6170987b1d78e43823bc132fe9a4c6a02
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="create-coupons-for-retail-sales"></a><span data-ttu-id="3ef20-103">创建零售销售优惠券</span><span class="sxs-lookup"><span data-stu-id="3ef20-103">Create coupons for retail sales</span></span>

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a><span data-ttu-id="3ef20-104">优惠券概览</span><span class="sxs-lookup"><span data-stu-id="3ef20-104">Overview of coupons</span></span>

<span data-ttu-id="3ef20-105">优惠券是用于将零售折扣添加到交易的代码和条码。</span><span class="sxs-lookup"><span data-stu-id="3ef20-105">Coupons are codes and bar codes that are used to add retail discounts to transactions.</span></span> <span data-ttu-id="3ef20-106">每张优惠券可以有多个代码，且每个代码可以有自己的有效日期。</span><span class="sxs-lookup"><span data-stu-id="3ef20-106">Each coupon can have multiple codes, and each code can have its own effective dates.</span></span> 

<span data-ttu-id="3ef20-107">每张优惠券都关联一个零售折扣。</span><span class="sxs-lookup"><span data-stu-id="3ef20-107">Each coupon is related to one retail discount.</span></span> <span data-ttu-id="3ef20-108">与折扣关联的价格组定义可以使用优惠券的客户或优惠券有效的渠道。</span><span class="sxs-lookup"><span data-stu-id="3ef20-108">The price groups that are associated with the discount define the customers that can use a coupon or the channels where a coupon is valid.</span></span> 

<span data-ttu-id="3ef20-109">优惠券基本上是零售折扣顶部的附加验证。</span><span class="sxs-lookup"><span data-stu-id="3ef20-109">Essentially, coupons are additional validation on top of retail discounts.</span></span> <span data-ttu-id="3ef20-110">优惠券提供必需的优惠券代码和条码，以及这些代码的日期范围。</span><span class="sxs-lookup"><span data-stu-id="3ef20-110">The coupon provides the coupon codes and bar codes that are required, together with date ranges for those codes.</span></span> <span data-ttu-id="3ef20-111">优惠券还提供可选使用限制和客户要求的属性。</span><span class="sxs-lookup"><span data-stu-id="3ef20-111">The coupon also provides optional usage limits and customer required properties.</span></span> <span data-ttu-id="3ef20-112">折扣提供优惠券对其有效的产品集。</span><span class="sxs-lookup"><span data-stu-id="3ef20-112">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="3ef20-113">折扣的价格组提供优惠券对其有效的客户、渠道或目录集。</span><span class="sxs-lookup"><span data-stu-id="3ef20-113">The price groups for the discount provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

<span data-ttu-id="3ef20-114">要创建优惠券，须分开创建折扣和优惠券。</span><span class="sxs-lookup"><span data-stu-id="3ef20-114">To create a coupon, you create the discount and the coupon separately.</span></span> <span data-ttu-id="3ef20-115">然后通过选择 Microsoft Dynamics 365 for Retail 优惠券页面的折扣进行关联。</span><span class="sxs-lookup"><span data-stu-id="3ef20-115">You then link them by selecting the discount on the coupon page in Microsoft Dynamics 365 for Retail.</span></span> 

> [!NOTE]
> <span data-ttu-id="3ef20-116">优惠券关联到折扣后，Microsoft Dynamics 365 for Retail 折扣页上的多个字段变为只读，因为其由优惠券的设置管理。</span><span class="sxs-lookup"><span data-stu-id="3ef20-116">After a coupon is linked to a discount, several fields on the discount page in Microsoft Dynamics 365 for Retail become read-only, because they are managed by the coupon’s settings.</span></span> <span data-ttu-id="3ef20-117">这些字段包括用于状态和标准日期范围的字段。</span><span class="sxs-lookup"><span data-stu-id="3ef20-117">These fields include the fields for the status and standard date ranges.</span></span>

### <a name="limited-use-coupons"></a><span data-ttu-id="3ef20-118">有限使用的优惠券</span><span class="sxs-lookup"><span data-stu-id="3ef20-118">Limited-use coupons</span></span>

<span data-ttu-id="3ef20-119">优惠券可以配置为有限使用的优惠券。</span><span class="sxs-lookup"><span data-stu-id="3ef20-119">Coupons can be configured as limited-use coupons.</span></span> <span data-ttu-id="3ef20-120">使用限制可以按客户或渠道进行配置，或配置为全球限制。</span><span class="sxs-lookup"><span data-stu-id="3ef20-120">The usage limit can be defined per customer or channel, or as a global limit.</span></span> <span data-ttu-id="3ef20-121">在 POS 中或销售订单录入期间输入或扫描代码或条码时执行此限制。</span><span class="sxs-lookup"><span data-stu-id="3ef20-121">This limit is enforced when the code or bar code is entered or scanned in POS or during sales order entry.</span></span> <span data-ttu-id="3ef20-122">当关联优惠券的订单完成时，优惠券记录为已使用。</span><span class="sxs-lookup"><span data-stu-id="3ef20-122">A coupon is recorded as used when an order is completed that has the coupon associated with it.</span></span>

<span data-ttu-id="3ef20-123">此限制按优惠券上的优惠券代码执行。</span><span class="sxs-lookup"><span data-stu-id="3ef20-123">The limit is enforced per coupon code on a coupon.</span></span> <span data-ttu-id="3ef20-124">例如，具有两个优惠券代码的单次使用优惠券可以使用两次：每个优惠券代码可使用一次。</span><span class="sxs-lookup"><span data-stu-id="3ef20-124">For example, a single-use coupon that has two coupon codes can be used two times: one time for each coupon code.</span></span> <span data-ttu-id="3ef20-125">优惠券上的每个代码可以单独设置为有效。</span><span class="sxs-lookup"><span data-stu-id="3ef20-125">Each code on a coupon can be independently set to active.</span></span>

## <a name="managing-coupons"></a><span data-ttu-id="3ef20-126">管理优惠券</span><span class="sxs-lookup"><span data-stu-id="3ef20-126">Managing coupons</span></span>

<span data-ttu-id="3ef20-127">您必须分开创建折扣和优惠券。</span><span class="sxs-lookup"><span data-stu-id="3ef20-127">You must create the discount and the coupon separately.</span></span> <span data-ttu-id="3ef20-128">之后可以通过选择优惠券页面上的折扣将它们关联。</span><span class="sxs-lookup"><span data-stu-id="3ef20-128">You then link them by selecting the discount on the coupon page.</span></span> <span data-ttu-id="3ef20-129">将优惠券关联到折扣后，折扣的多个字段变为只读，因为其由优惠券的设置管理。</span><span class="sxs-lookup"><span data-stu-id="3ef20-129">After you link a coupon to a discount, several fields for the discount become read-only, because they are managed by the coupon's settings.</span></span> <span data-ttu-id="3ef20-130">这些字段包括用于状态和标准日期范围的字段。</span><span class="sxs-lookup"><span data-stu-id="3ef20-130">These fields include the fields for the status and standard date ranges.</span></span>  

<span data-ttu-id="3ef20-131">优惠券现在基本上是零售折扣顶部的附加验证。</span><span class="sxs-lookup"><span data-stu-id="3ef20-131">Essentially, coupons are now additional validation on top of retail discounts.</span></span> <span data-ttu-id="3ef20-132">优惠券提供优惠券代码和条码以及日期范围、使用限制和客户要求的属性。</span><span class="sxs-lookup"><span data-stu-id="3ef20-132">The coupon provides the coupon codes and bar codes, together with date ranges, the usage limits, and the customer required property.</span></span> <span data-ttu-id="3ef20-133">折扣提供优惠券对其有效的产品集。</span><span class="sxs-lookup"><span data-stu-id="3ef20-133">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="3ef20-134">折扣的价格组提供优惠券对其有效的客户、渠道或目录集。</span><span class="sxs-lookup"><span data-stu-id="3ef20-134">The discount's price groups provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

## <a name="system-setup-for-coupons"></a><span data-ttu-id="3ef20-135">优惠券系统创建</span><span class="sxs-lookup"><span data-stu-id="3ef20-135">System setup for coupons</span></span> 

<span data-ttu-id="3ef20-136">在您可以设置优惠券前，必须先设置优惠券条码和两个优惠券编号规则。</span><span class="sxs-lookup"><span data-stu-id="3ef20-136">Before you can set up a coupon, you must set up the coupon bar code and two coupon number sequences.</span></span> 

1.  <span data-ttu-id="3ef20-137">在**掩码字符**页，为优惠券代码创建新的掩码字符。</span><span class="sxs-lookup"><span data-stu-id="3ef20-137">On the **Mask characters** page, create a new mask character for the coupon code.</span></span> <span data-ttu-id="3ef20-138">您可以选择任何未使用的字符。</span><span class="sxs-lookup"><span data-stu-id="3ef20-138">You can select any unused character.</span></span>
2.  <span data-ttu-id="3ef20-139">在**条码掩码设置**页，创建一个新的条码掩码。</span><span class="sxs-lookup"><span data-stu-id="3ef20-139">On the **Bar code mask setup** page, create a new bar code mask.</span></span> <span data-ttu-id="3ef20-140">将**类型**字段设置为**优惠券**。</span><span class="sxs-lookup"><span data-stu-id="3ef20-140">Set the **Type** field to **Coupon**.</span></span>
3.  <span data-ttu-id="3ef20-141">在**条码设置**页，创建使用您刚才创建的条码掩码的新条码。</span><span class="sxs-lookup"><span data-stu-id="3ef20-141">On the **Bar code setup** page, create a new bar code that uses the bar code mask that you just created.</span></span>
4.  <span data-ttu-id="3ef20-142">在**编号规则**页，创建两个新的编号规则。</span><span class="sxs-lookup"><span data-stu-id="3ef20-142">On the **Number sequences** page, create two new number sequences.</span></span> <span data-ttu-id="3ef20-143">一个规则用于优惠券代码 ID，另一个规则用于优惠券编号。</span><span class="sxs-lookup"><span data-stu-id="3ef20-143">One sequence is for the coupon code ID, and the other sequence is for the coupon number.</span></span> <span data-ttu-id="3ef20-144">优惠券代码 ID 是优惠券各优惠券代码的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3ef20-144">The coupon code ID is the unique identifier for each coupon code for a coupon.</span></span> <span data-ttu-id="3ef20-145">优惠券编号是优惠券的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3ef20-145">The coupon number is the unique identifier for a coupon.</span></span> <span data-ttu-id="3ef20-146">每张优惠券可以有多个触发优惠券的代码和条码。</span><span class="sxs-lookup"><span data-stu-id="3ef20-146">Each coupon can have multiple codes and bar codes that trigger the coupon.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ef20-147">对于这两种编号规则，必须将**作用域**字段设置为**公司**。</span><span class="sxs-lookup"><span data-stu-id="3ef20-147">For both number sequences, you must set the **Scope** field to **Company**.</span></span> <span data-ttu-id="3ef20-148">在大多数情况下，都应自动生成两个序列号。</span><span class="sxs-lookup"><span data-stu-id="3ef20-148">In most cases, you should automatically generate both sequence numbers.</span></span>

5.  <span data-ttu-id="3ef20-149">在**零售共享参数**页的**条码**选项卡上，选择您之前创建的条码。</span><span class="sxs-lookup"><span data-stu-id="3ef20-149">On the **Retail shared parameters** page, on the **Bar codes** tab, select the bar code that you created earlier.</span></span>
6.  <span data-ttu-id="3ef20-150">在**零售参数**页的**编号规则**选项卡上，选择您已为优惠券编号和优惠券代码 ID 创建的编号规则。</span><span class="sxs-lookup"><span data-stu-id="3ef20-150">On the **Retail parameters** page, on the **Number sequences** tab, select the number sequences that you created for the coupon number and coupon code ID.</span></span>
7.  <span data-ttu-id="3ef20-151">您现在可以打开**优惠券**页和创建新优惠券。</span><span class="sxs-lookup"><span data-stu-id="3ef20-151">You can now open the **Coupons** page and create new coupons.</span></span>

## <a name="the-effect-of-partial-updates-on-coupons"></a><span data-ttu-id="3ef20-152">部分更新对优惠券的影响</span><span class="sxs-lookup"><span data-stu-id="3ef20-152">The effect of partial updates on coupons</span></span>

<span data-ttu-id="3ef20-153">优惠券功能包括 Dynamics 365 for Retail 中的多个独特功能。</span><span class="sxs-lookup"><span data-stu-id="3ef20-153">Coupon functionality comprises multiple distinct features in Dynamics 365 for Retail.</span></span> <span data-ttu-id="3ef20-154">Microsoft Dynamics 365 for Retail 总部 (HQ) 和渠道可以跨组件部分更新。</span><span class="sxs-lookup"><span data-stu-id="3ef20-154">Microsoft Dynamics 365 for Retail headquarters (HQ) and the channel can be partially updated across components.</span></span> <span data-ttu-id="3ef20-155">因此，了解部分更新对优惠券功能总体的影响十分重要。</span><span class="sxs-lookup"><span data-stu-id="3ef20-155">Therefore, it's important that you understand how partial updates affect coupon functionality as a whole.</span></span>

- <span data-ttu-id="3ef20-156">**HQ 被部分更新，但 Retail 服务器和 POS 不更新。**</span><span class="sxs-lookup"><span data-stu-id="3ef20-156">**HQ is partially updated, but Retail server and POS aren't updated.**</span></span> <span data-ttu-id="3ef20-157">在 HQ 更新中，优惠券和折扣页更新，零售价格引擎也更新。</span><span class="sxs-lookup"><span data-stu-id="3ef20-157">In an HQ update, the coupon and discount pages are updated, and the retail price engine is also updated.</span></span> <span data-ttu-id="3ef20-158">如果两个组件中仅有一个更新，则 Retail 中的部分页面与价格计算数据不匹配。</span><span class="sxs-lookup"><span data-stu-id="3ef20-158">If only one of those two components is updated, some pages in Retail won’t match the price calculation data.</span></span> <span data-ttu-id="3ef20-159">因此，在折扣计算期间可能发生意外折扣计算或错误。</span><span class="sxs-lookup"><span data-stu-id="3ef20-159">Therefore, unexpected discount calculations or errors might occur during discount calculations.</span></span>
- <span data-ttu-id="3ef20-160">**HQ 更新，但 Retail 服务器和 POS 不更新 (N-1)。**</span><span class="sxs-lookup"><span data-stu-id="3ef20-160">**HQ is updated, but Retail server and POS aren't updated (N-1).**</span></span> <span data-ttu-id="3ef20-161">由于并非所有的零售商店可以同时更新，因此我们建议您在更新零售商店前更新 HQ。</span><span class="sxs-lookup"><span data-stu-id="3ef20-161">Because not all retail stores can be updated at the same time, we recommend that you update HQ before you update retail stores.</span></span> <span data-ttu-id="3ef20-162">在 N-1 方案中，与优惠券相关的新功能在尚未更新的商店中不可用。</span><span class="sxs-lookup"><span data-stu-id="3ef20-162">In the N-1 scenario, new functionality that is related to coupons won't be available in stores that haven’t been updated yet.</span></span> <span data-ttu-id="3ef20-163">例如，优惠券功能引入“排除”行。</span><span class="sxs-lookup"><span data-stu-id="3ef20-163">For example, the coupon functionality introduces “exclude” lines.</span></span> <span data-ttu-id="3ef20-164">如果您对折扣使用排除行，则其不会应用在运行较早版本的零售商店中。</span><span class="sxs-lookup"><span data-stu-id="3ef20-164">If you use exclude lines on a discount, they won't be applied in a retail store that is running an earlier version.</span></span>
- <span data-ttu-id="3ef20-165">**HQ 不更新，但 Retail 服务器和 POS 更新 (N+1)。**</span><span class="sxs-lookup"><span data-stu-id="3ef20-165">**HQ isn't updated, but Retail server and POS are updated (N+1).**</span></span> <span data-ttu-id="3ef20-166">由于在 Retail 服务器中更新的价格引擎在价格计算期间可以处理旧折扣，因此更新应该对此方案没有功能影响。</span><span class="sxs-lookup"><span data-stu-id="3ef20-166">Because the updated price engine in Retail server can handle legacy discount codes during price calculations, the update should have no functional impact in this scenario.</span></span>

