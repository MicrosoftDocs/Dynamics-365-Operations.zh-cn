---
title: 应用库存设置
description: 本主题介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2c44eb5ece74de15e22180abc6d9d0448ab401b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798881"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="23d6d-103">应用库存设置</span><span class="sxs-lookup"><span data-stu-id="23d6d-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23d6d-104">本主题介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。</span><span class="sxs-lookup"><span data-stu-id="23d6d-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="23d6d-105">库存设置指定在将产品添加到购物车之前是否应该检查库存。</span><span class="sxs-lookup"><span data-stu-id="23d6d-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="23d6d-106">另外还定义与库存相关的促销消息，如“有存货”和“仅剩几个”。</span><span class="sxs-lookup"><span data-stu-id="23d6d-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="23d6d-107">这些设置可确保如果库存不足就不能购买产品。</span><span class="sxs-lookup"><span data-stu-id="23d6d-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="23d6d-108">Dynamics 365 Commerce 提供对产品现有量的估计。</span><span class="sxs-lookup"><span data-stu-id="23d6d-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="23d6d-109">有关如何计算估计现有量的信息，请参阅[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="23d6d-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="23d6d-110">在 Commerce 站点构建器中，可以为产品或类别定义库存阈值和范围。</span><span class="sxs-lookup"><span data-stu-id="23d6d-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="23d6d-111">它们确定库存是分类为有存货、低库存还是库存不足。</span><span class="sxs-lookup"><span data-stu-id="23d6d-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="23d6d-112">有关详细信息，请参阅[配置库存缓冲区和库存级别](inventory-buffers-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="23d6d-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="23d6d-113">对库存阈值和范围的支持在 Dynamics 365 Commerce 10.0.12 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="23d6d-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="23d6d-114">库存设置</span><span class="sxs-lookup"><span data-stu-id="23d6d-114">Inventory settings</span></span>

<span data-ttu-id="23d6d-115">在 Commerce 中，库存设置在站点构建器中的 **站点设置 \> 扩展 \> 库存管理** 处定义。</span><span class="sxs-lookup"><span data-stu-id="23d6d-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="23d6d-116">有四种库存设置，其中一种已过时（已弃用）：</span><span class="sxs-lookup"><span data-stu-id="23d6d-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="23d6d-117">**在应用中启用存货检查** – 此设置打开产品库存检查。</span><span class="sxs-lookup"><span data-stu-id="23d6d-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="23d6d-118">然后，商店模块中的购买框、购物车和提货将检查产品库存，并且仅在有库存时允许将产品添加到购物车中。</span><span class="sxs-lookup"><span data-stu-id="23d6d-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="23d6d-119">**库存级别确定条件** – 此设置定义如何计算库存级别。</span><span class="sxs-lookup"><span data-stu-id="23d6d-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="23d6d-120">可用值为 **总可用量**、**实际可用量** 和 **库存不足阈值**。</span><span class="sxs-lookup"><span data-stu-id="23d6d-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="23d6d-121">在 Commerce 中，可以为每个产品和类别定义库存阈值和范围。</span><span class="sxs-lookup"><span data-stu-id="23d6d-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="23d6d-122">库存 API 返回 **总可用量** 属性和 **实际可用量** 属性的产品库存信息。</span><span class="sxs-lookup"><span data-stu-id="23d6d-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="23d6d-123">零售商决定是应该使用 **总可用量** 还是 **实际可用量** 值来确定库存盘点，以及有存货和库存不足状态的相应范围。</span><span class="sxs-lookup"><span data-stu-id="23d6d-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="23d6d-124">**库存级别确定条件** 设置的 **库存不足阈值** 值是旧的（旧版）已过时的值。</span><span class="sxs-lookup"><span data-stu-id="23d6d-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="23d6d-125">选择它后，库存盘点将根据 **总可用量** 值的结果确定，但阈值由稍后介绍的 **库存不足阈值** 数字设置定义。</span><span class="sxs-lookup"><span data-stu-id="23d6d-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="23d6d-126">此阈值设置将应用于整个电子商务站点的所有产品。</span><span class="sxs-lookup"><span data-stu-id="23d6d-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="23d6d-127">如果库存低于阈值数字，则视为产品库存不足。</span><span class="sxs-lookup"><span data-stu-id="23d6d-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="23d6d-128">否则，视为有存货。</span><span class="sxs-lookup"><span data-stu-id="23d6d-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="23d6d-129">**库存不足阈值** 值的能力是有限的，我们不建议您在版本 10.0.12 及更高版本中使用它。</span><span class="sxs-lookup"><span data-stu-id="23d6d-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="23d6d-130">**库存范围** – 此设置定义在站点模块上显示消息的库存范围。</span><span class="sxs-lookup"><span data-stu-id="23d6d-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="23d6d-131">仅当为 **库存级别确定条件** 选择了 **总可用量** 值或 **实际可用量** 值时，此设置才适用。</span><span class="sxs-lookup"><span data-stu-id="23d6d-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="23d6d-132">可用值有 **所有**、**低库存和库存不足** 和 **库存不足**。</span><span class="sxs-lookup"><span data-stu-id="23d6d-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="23d6d-133">选择 **所有** 时，将显示所有库存范围的消息，从有存货（“有货”消息）到库存不足（“库存不足”消息）。</span><span class="sxs-lookup"><span data-stu-id="23d6d-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="23d6d-134">选择 **低库存和库存不足** 时，将显示除有存货（“有货”消息）以外的所有库存范围的消息。</span><span class="sxs-lookup"><span data-stu-id="23d6d-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="23d6d-135">选择 **库存不足** 时，将仅显示“库存不足”消息。</span><span class="sxs-lookup"><span data-stu-id="23d6d-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="23d6d-136">**库存不足阈值** – 这是一个旧的数字设置，只有在为 **库存级别确定条件** 设置选择了 **库存不足阈值** 值时才会生效。</span><span class="sxs-lookup"><span data-stu-id="23d6d-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="23d6d-137">这些设置在 Dynamics 365 Commerce 10.0.12 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="23d6d-137">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="23d6d-138">如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="23d6d-138">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="23d6d-139">有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="23d6d-139">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="23d6d-140">使用库存设置的模块</span><span class="sxs-lookup"><span data-stu-id="23d6d-140">Modules that use inventory settings</span></span>

<span data-ttu-id="23d6d-141">购买框、愿望列表、商店选择器、购物车和购物车图标模块使用库存设置显示库存范围和消息。</span><span class="sxs-lookup"><span data-stu-id="23d6d-141">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="23d6d-142">下图显示了产品详细信息页面 (PDP) 的示例，该页面显示有存货（“有货”）消息。</span><span class="sxs-lookup"><span data-stu-id="23d6d-142">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![显示有存货消息的 PDP 模块的示例](./media/pdp-InStock.png)

<span data-ttu-id="23d6d-144">下图显示了显示“库存不足”消息的 PDP 示例。</span><span class="sxs-lookup"><span data-stu-id="23d6d-144">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![显示库存不足消息的 PDP 模块的示例](./media/pdp-outofstock.png)

<span data-ttu-id="23d6d-146&quot;>下图显示了显示有存货（“有货”）消息的购物车的示例。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;23d6d-146&quot;>The following image shows an example of a cart that is showing an in-stock (&quot;Available") message.</span></span>

![显示有存货消息的购物车模块的示例](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="23d6d-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="23d6d-148">Additional resources</span></span>

[<span data-ttu-id="23d6d-149">模块库概述</span><span class="sxs-lookup"><span data-stu-id="23d6d-149">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="23d6d-150">配置库存缓冲区和库存级别</span><span class="sxs-lookup"><span data-stu-id="23d6d-150">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="23d6d-151">购物车模块</span><span class="sxs-lookup"><span data-stu-id="23d6d-151">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="23d6d-152">购买框模块</span><span class="sxs-lookup"><span data-stu-id="23d6d-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="23d6d-153">帐户管理页面和模块</span><span class="sxs-lookup"><span data-stu-id="23d6d-153">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="23d6d-154">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="23d6d-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="23d6d-155">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="23d6d-155">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
