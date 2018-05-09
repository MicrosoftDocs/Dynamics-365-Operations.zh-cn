---
title: "设置条码掩码"
description: "此主题介绍如何设置条码掩码字符和条码掩码，以及如何为条码分配条码掩码。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b2799ab1fce629993360c75ff7cfbb308dbd24ed
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-bar-code-masks"></a><span data-ttu-id="7cb89-103">设置条码掩码</span><span class="sxs-lookup"><span data-stu-id="7cb89-103">Set up bar code masks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7cb89-104">此主题介绍如何设置条码掩码字符和条码掩码，以及如何为条码分配条码掩码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-104">This topic describes how to set up bar code mask characters, bar code masks, and how to assign bar code masks to bar codes.</span></span>

<a name="set-up-bar-code-mask-characters"></a><span data-ttu-id="7cb89-105">设置条码掩码字符</span><span class="sxs-lookup"><span data-stu-id="7cb89-105">Set up bar code mask characters</span></span>
-------------------------------

<span data-ttu-id="7cb89-106">条码掩码用于创建条码，以及快速标识扫描到销售点 (POS) 中的条码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-106">Bar code masks are used to create bar codes and to quickly identify bar codes that are scanned into the point of sale (POS).</span></span> <span data-ttu-id="7cb89-107">掩码包含充当占位符的字符，用于表示将创建的条码的格式。</span><span class="sxs-lookup"><span data-stu-id="7cb89-107">Masks are comprised of characters which act as placeholders that indicate the format for the bar codes that will be created.</span></span> <span data-ttu-id="7cb89-108">若要配置条码掩码，需要设置条码掩码字符。</span><span class="sxs-lookup"><span data-stu-id="7cb89-108">To configure a bar code mask, you need to set up bar code mask characters.</span></span> <span data-ttu-id="7cb89-109">转到**零售** &gt; **库存管理** &gt; **条码和标签** &gt; **掩码字符**。</span><span class="sxs-lookup"><span data-stu-id="7cb89-109">Go to **Retail** &gt; **Inventory management** &gt; **Barcodes and labels** &gt; **Mask characters**.</span></span> <span data-ttu-id="7cb89-110">单击**新建**创建条码掩码字符。</span><span class="sxs-lookup"><span data-stu-id="7cb89-110">Click **New** to create bar code mask characters.</span></span> <span data-ttu-id="7cb89-111">可创建掩码字符以表示以下条码数据。</span><span class="sxs-lookup"><span data-stu-id="7cb89-111">Mask characters can be created to indicate the following bar code data.</span></span>

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb89-112">**字段**</span><span class="sxs-lookup"><span data-stu-id="7cb89-112">**Field**</span></span>            | <span data-ttu-id="7cb89-113">**描述**</span><span class="sxs-lookup"><span data-stu-id="7cb89-113">**Description**</span></span>                                                                                                 |
| <span data-ttu-id="7cb89-114">**产品**</span><span class="sxs-lookup"><span data-stu-id="7cb89-114">**Product**</span></span>          | <span data-ttu-id="7cb89-115">产品 ID 的占位符。</span><span class="sxs-lookup"><span data-stu-id="7cb89-115">Placeholder for product ID.</span></span>                                                                                     |
| <span data-ttu-id="7cb89-116">**任意数字**</span><span class="sxs-lookup"><span data-stu-id="7cb89-116">**Any number**</span></span>       | <span data-ttu-id="7cb89-117">用于指定将在条码中硬编码的数字。</span><span class="sxs-lookup"><span data-stu-id="7cb89-117">Used to specify a number that will be hard coded in bar codes.</span></span>                                                  |
| <span data-ttu-id="7cb89-118">**校验位**</span><span class="sxs-lookup"><span data-stu-id="7cb89-118">**Check digit**</span></span>      | <span data-ttu-id="7cb89-119">指示条码掩码中的条码格式使用校验位确认条码的有效性。</span><span class="sxs-lookup"><span data-stu-id="7cb89-119">Indicates that the bar code format in a bar code mask uses a check digit to confirm the validity of a bar code.</span></span> |
| <span data-ttu-id="7cb89-120">**大小位**</span><span class="sxs-lookup"><span data-stu-id="7cb89-120">**Size digit**</span></span>       | <span data-ttu-id="7cb89-121">指示为包含大小的产品变型创建的条码中的大小。</span><span class="sxs-lookup"><span data-stu-id="7cb89-121">Indicates size in a bar code created for a product variant which includes size.</span></span>                                 |
| <span data-ttu-id="7cb89-122">**颜色位**</span><span class="sxs-lookup"><span data-stu-id="7cb89-122">**Color digit**</span></span>      | <span data-ttu-id="7cb89-123">指示为包含颜色的产品变型创建的条码中的颜色。</span><span class="sxs-lookup"><span data-stu-id="7cb89-123">Indicates color in a bar code created for a product variant which includes color.</span></span>                               |
| <span data-ttu-id="7cb89-124">**样式位**</span><span class="sxs-lookup"><span data-stu-id="7cb89-124">**Style digit**</span></span>      | <span data-ttu-id="7cb89-125">指示为包含样式的产品变型创建的条码中的样式。</span><span class="sxs-lookup"><span data-stu-id="7cb89-125">Indicates style in a bar code created for a product variant which includes a style.</span></span>                             |
| <span data-ttu-id="7cb89-126">**EAN 许可证代码**</span><span class="sxs-lookup"><span data-stu-id="7cb89-126">**EAN license code**</span></span> | <span data-ttu-id="7cb89-127">为 EAN 许可证代码颁发的 EAN 许可证的占位符。</span><span class="sxs-lookup"><span data-stu-id="7cb89-127">Placeholder for EAN license issued for EAN license codes.</span></span>                                                       |
| <span data-ttu-id="7cb89-128">**价格**</span><span class="sxs-lookup"><span data-stu-id="7cb89-128">**Price**</span></span>            | <span data-ttu-id="7cb89-129">指示嵌入了价格的条码的间隔。</span><span class="sxs-lookup"><span data-stu-id="7cb89-129">Indicates price for price embedded bar codes.</span></span>                                                                   |
| <span data-ttu-id="7cb89-130">**数量**</span><span class="sxs-lookup"><span data-stu-id="7cb89-130">**Quantity**</span></span>         | <span data-ttu-id="7cb89-131">指示嵌入了数量/随机权重的条码中的数量。</span><span class="sxs-lookup"><span data-stu-id="7cb89-131">Indicates quantity in quantity/random weight embedded bar codes.</span></span>                                                |
| <span data-ttu-id="7cb89-132">**员工**</span><span class="sxs-lookup"><span data-stu-id="7cb89-132">**Employee**</span></span>         | <span data-ttu-id="7cb89-133">指示用于登录条码 POS 的员工 ID 编号的代码段。</span><span class="sxs-lookup"><span data-stu-id="7cb89-133">Indicates bar code segment for employee ID number used for bar code POS login.</span></span>                                  |
| <span data-ttu-id="7cb89-134">**客户**</span><span class="sxs-lookup"><span data-stu-id="7cb89-134">**Customer**</span></span>         | <span data-ttu-id="7cb89-135">指示客户 ID 段。</span><span class="sxs-lookup"><span data-stu-id="7cb89-135">Indicates customer ID segment.</span></span>                                                                                  |
| <span data-ttu-id="7cb89-136">**数据输入**</span><span class="sxs-lookup"><span data-stu-id="7cb89-136">**Data entry**</span></span>       | <span data-ttu-id="7cb89-137">*尚未实现。*</span><span class="sxs-lookup"><span data-stu-id="7cb89-137">*Not yet implemented.*</span></span>                                                                                          |
| <span data-ttu-id="7cb89-138">**折扣代码**</span><span class="sxs-lookup"><span data-stu-id="7cb89-138">**Discount code**</span></span>    | <span data-ttu-id="7cb89-139">从 Dynamics 365 for Retail 2017 年春季版本开始的*折旧*。</span><span class="sxs-lookup"><span data-stu-id="7cb89-139">*Depreciated* as of Dynamics 365 for Retail Spring 2017 release.</span></span> <span data-ttu-id="7cb89-140">以前：指示用于向销售点销售交易记录添加折扣的条码的折扣代码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-140">Previously: Indicates discount code for a bar code that's used to add a discount to a point of sale transaction.</span></span>                                                                   |
| <span data-ttu-id="7cb89-141">**优惠券代码**</span><span class="sxs-lookup"><span data-stu-id="7cb89-141">**Coupon code**</span></span>      | <span data-ttu-id="7cb89-142">指示用于向零售订单添加折扣的条码的优惠券代码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-142">Indicates coupon code for a bar code used to add a discount to a retail order.</span></span> <span data-ttu-id="7cb89-143">它替代折扣代码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-143">This replaced discount code.</span></span>     |
| <span data-ttu-id="7cb89-144">**礼品卡**</span><span class="sxs-lookup"><span data-stu-id="7cb89-144">**Gift card**</span></span>        | <span data-ttu-id="7cb89-145">颁发或使用礼品卡付款时指示礼品卡编号。</span><span class="sxs-lookup"><span data-stu-id="7cb89-145">Indicates a gift card number when issuing or paying by gift card.</span></span>                                               |
| <span data-ttu-id="7cb89-146">**会员卡**</span><span class="sxs-lookup"><span data-stu-id="7cb89-146">**Loyalty card**</span></span>     | <span data-ttu-id="7cb89-147">向交易记录添加会员客户，可在以会员价付款时使用。</span><span class="sxs-lookup"><span data-stu-id="7cb89-147">Adds a loyalty customer to the transaction, and can be used when paying by loyalty.</span></span>                             |

## <a name="define-bar-code-masks"></a><span data-ttu-id="7cb89-148">定义条码掩码</span><span class="sxs-lookup"><span data-stu-id="7cb89-148">Define bar code masks</span></span>
<span data-ttu-id="7cb89-149">为必要的条码掩码指定了条码掩码字符之后，请转至**零售** &gt; **库存管理** &gt; **条码和标签** &gt; **条码掩码设置**。</span><span class="sxs-lookup"><span data-stu-id="7cb89-149">After bar code mask characters are specified for the necessary bar code masks, go to **Retail** &gt; **Inventory management** &gt; **Barcodes and labels** &gt; **Barcode mask setup**.</span></span> <span data-ttu-id="7cb89-150">在此页面中，可以定义使用前面指定的字符的条码掩码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-150">On this page, you can define bar code masks that use the previously specified characters.</span></span> <span data-ttu-id="7cb89-151">这些条码掩码在生成条码时使用，也有助于识别 POS 中扫描的条码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-151">These bar code masks will be used when generating bar codes and will also help to identify bar codes scanned at the POS.</span></span>

1.  <span data-ttu-id="7cb89-152">单击**新建**创建新的条码掩码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-152">Click **New** to create a new bar code mask.</span></span>
2.  <span data-ttu-id="7cb89-153">在**掩码 ID** 和**描述**字段中输入值，然后在**类型**字段中选择条码掩码类型。</span><span class="sxs-lookup"><span data-stu-id="7cb89-153">Enter values in the **Mask ID** and **Description** fields, and then select a bar code mask type in the **Type** field.</span></span>
3.  <span data-ttu-id="7cb89-154">在**常规**部分中，选择**条码标准**字段中选择一个值，然后指定条码前缀（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="7cb89-154">In the **General** section, select a value in the **Bar code standard** field, and then specify the bar code prefix, if one is required.</span></span>
4.  <span data-ttu-id="7cb89-155">在**条码掩码段**部分中，添加将在要创建的条码中使用的条码段。</span><span class="sxs-lookup"><span data-stu-id="7cb89-155">In the **Bar code mask segment** section, add bar code segments that will be used in the bar code to be created.</span></span>

<span data-ttu-id="7cb89-156">例如，若要创建掩码 ID 为“产品”的条码掩码，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7cb89-156">As an example, to create a bar code mask with mask ID 'Product', you'd do the following:</span></span>

1.  <span data-ttu-id="7cb89-157">创建一个新条码掩码，然后选择类型“产品”。</span><span class="sxs-lookup"><span data-stu-id="7cb89-157">Create a new bar code mask and select type ‘Product’.</span></span>
2.  <span data-ttu-id="7cb89-158">选择一个条码标准，如“代码 39”。</span><span class="sxs-lookup"><span data-stu-id="7cb89-158">Select a bar code standard, for example, 'Code 39'.</span></span>
3.  <span data-ttu-id="7cb89-159">提供要用于轻松识别条码的前缀。</span><span class="sxs-lookup"><span data-stu-id="7cb89-159">Provide a prefix to be used to easily identify the bar code.</span></span> <span data-ttu-id="7cb89-160">例如，“22”。</span><span class="sxs-lookup"><span data-stu-id="7cb89-160">For example, ‘22’.</span></span>
4.  <span data-ttu-id="7cb89-161">添加一个掩码段。</span><span class="sxs-lookup"><span data-stu-id="7cb89-161">Add a mask segment.</span></span> <span data-ttu-id="7cb89-162">将选择“产品”掩码段。</span><span class="sxs-lookup"><span data-stu-id="7cb89-162">The ‘Product’ mask segment will be selected.</span></span>
5.  <span data-ttu-id="7cb89-163">为产品段提供长度，如“10”。</span><span class="sxs-lookup"><span data-stu-id="7cb89-163">Provide a length for the product segment, for example, ‘10’.</span></span> <span data-ttu-id="7cb89-164">此长度应匹配商店中常用的产品 ID 的长度。</span><span class="sxs-lookup"><span data-stu-id="7cb89-164">The length should match the length of a product ID commonly used in the store.</span></span> <span data-ttu-id="7cb89-165">将在**常规**部分中的**掩码**下把掩码显示为预览。</span><span class="sxs-lookup"><span data-stu-id="7cb89-165">The mask will be displayed as a preview in the **General** section under **Mask**.</span></span>

## <a name="assign-bar-code-masks-to-bar-codes"></a><span data-ttu-id="7cb89-166">为条码分配条码掩码</span><span class="sxs-lookup"><span data-stu-id="7cb89-166">Assign bar code masks to bar codes</span></span>
<span data-ttu-id="7cb89-167">必须在使用条码之前为其分配条码掩码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-167">Bar codes masks must be assigned to bar codes before they can be used.</span></span> <span data-ttu-id="7cb89-168">继续以前面的示例为例，若要为条码分配条码掩码，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7cb89-168">Continuing with the previous example, to assign the bar code mask to a bar code, do the following:</span></span>

1.  <span data-ttu-id="7cb89-169">转至**组织管理** &gt; **设置** &gt; **条码**。</span><span class="sxs-lookup"><span data-stu-id="7cb89-169">Go to **Organization administration** &gt; **Setup** &gt; **Bar codes**.</span></span> <span data-ttu-id="7cb89-170">单击**新建**创建一个新的条码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-170">Click **New** to create a new bar code.</span></span>
2.  <span data-ttu-id="7cb89-171">在**条码** **设置**和 **设置** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="7cb89-171">Enter values in the **Barcode** **setup** and **Setup **fields.</span></span>
3.  <span data-ttu-id="7cb89-172">在**常规**部分中的**条码类型**字段中，选择“代码 39”。</span><span class="sxs-lookup"><span data-stu-id="7cb89-172">In the **General** section, in the **Bar code type** field, select ‘Code 39’.</span></span> <span data-ttu-id="7cb89-173">在**条码** **ID** 字段中，选择前面创建的“产品”页面。</span><span class="sxs-lookup"><span data-stu-id="7cb89-173">In the **Mask** **ID** field, select the ‘Product’ mask previously created.</span></span>
4.  <span data-ttu-id="7cb89-174">在**大小**下，输入“12”。</span><span class="sxs-lookup"><span data-stu-id="7cb89-174">Under **Size**, enter ‘12’.</span></span>
5.  <span data-ttu-id="7cb89-175">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="7cb89-175">Click **Save**.</span></span>

<span data-ttu-id="7cb89-176">现在可将条码掩码用于为产品创建条码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-176">The bar code mask can now be used to create bar codes for products.</span></span> <span data-ttu-id="7cb89-177">上面的步骤是如何为产品创建条码掩码的示例，但是还说明了如何为其他任何支持的条码类型创建条码掩码。</span><span class="sxs-lookup"><span data-stu-id="7cb89-177">The above steps are examples of how to create bar code masks for products, but they also illustrate how to create bar code masks for any of the other supported bar code types.</span></span> <span data-ttu-id="7cb89-178">应调整条码掩码、类型和长度，以便在您的具体环境中使用。</span><span class="sxs-lookup"><span data-stu-id="7cb89-178">Bar code masks, types, and lengths should be adjusted for use in your specific environment.</span></span>




