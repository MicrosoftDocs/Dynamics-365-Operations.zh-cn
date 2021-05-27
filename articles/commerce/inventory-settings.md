---
title: 应用库存设置
description: 本主题介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: ae0195f63b123a345b0cdcd4976bfd25b3b3d6d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019070"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="9b147-103">应用库存设置</span><span class="sxs-lookup"><span data-stu-id="9b147-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="9b147-104">本主题介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。</span><span class="sxs-lookup"><span data-stu-id="9b147-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9b147-105">库存设置指定在将产品添加到购物车之前是否应该检查库存。</span><span class="sxs-lookup"><span data-stu-id="9b147-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="9b147-106">另外还定义与库存相关的促销消息，如“有存货”和“仅剩几个”。</span><span class="sxs-lookup"><span data-stu-id="9b147-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="9b147-107">这些设置可确保如果库存不足就不能购买产品。</span><span class="sxs-lookup"><span data-stu-id="9b147-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="9b147-108">Dynamics 365 Commerce 提供对产品现有量的估计。</span><span class="sxs-lookup"><span data-stu-id="9b147-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="9b147-109">有关如何计算估计现有量的信息，请参阅[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="9b147-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="9b147-110">在 Commerce 站点构建器中，可以为产品或类别定义库存阈值和范围。</span><span class="sxs-lookup"><span data-stu-id="9b147-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="9b147-111">它们确定库存是分类为有存货、低库存还是库存不足。</span><span class="sxs-lookup"><span data-stu-id="9b147-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="9b147-112">有关详细信息，请参阅[配置库存缓冲区和库存级别](inventory-buffers-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="9b147-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9b147-113">对库存阈值和范围的支持在 Dynamics 365 Commerce 10.0.12 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="9b147-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="9b147-114">库存设置</span><span class="sxs-lookup"><span data-stu-id="9b147-114">Inventory settings</span></span>

<span data-ttu-id="9b147-115">在 Commerce 中，库存设置在站点构建器中的 **站点设置 \> 扩展 \> 库存管理** 处定义。</span><span class="sxs-lookup"><span data-stu-id="9b147-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="9b147-116">有五种库存设置，其中一种已过时（已弃用）：</span><span class="sxs-lookup"><span data-stu-id="9b147-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="9b147-117">**在应用中启用存货检查** – 此设置打开产品库存检查。</span><span class="sxs-lookup"><span data-stu-id="9b147-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="9b147-118">然后，商店模块中的购买框、购物车和提货将检查产品库存，并且仅在有库存时允许将产品添加到购物车中。</span><span class="sxs-lookup"><span data-stu-id="9b147-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="9b147-119">**库存级别确定条件** – 此设置定义如何计算库存级别。</span><span class="sxs-lookup"><span data-stu-id="9b147-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="9b147-120">可用值为 **总可用量**、**实际可用量** 和 **库存不足阈值**。</span><span class="sxs-lookup"><span data-stu-id="9b147-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="9b147-121">在 Commerce 中，可以为每个产品和类别定义库存阈值和范围。</span><span class="sxs-lookup"><span data-stu-id="9b147-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="9b147-122">库存 API 返回 **总可用量** 属性和 **实际可用量** 属性的产品库存信息。</span><span class="sxs-lookup"><span data-stu-id="9b147-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="9b147-123">零售商决定是应该使用 **总可用量** 还是 **实际可用量** 值来确定库存盘点，以及有存货和库存不足状态的相应范围。</span><span class="sxs-lookup"><span data-stu-id="9b147-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="9b147-124">**库存级别确定条件** 设置的 **库存不足阈值** 值是旧的（旧版）已过时的值。</span><span class="sxs-lookup"><span data-stu-id="9b147-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="9b147-125">选择它后，库存盘点将根据 **总可用量** 值的结果确定，但阈值由稍后介绍的 **库存不足阈值** 数字设置定义。</span><span class="sxs-lookup"><span data-stu-id="9b147-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="9b147-126">此阈值设置将应用于整个电子商务站点的所有产品。</span><span class="sxs-lookup"><span data-stu-id="9b147-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="9b147-127">如果库存低于阈值数字，则视为产品库存不足。</span><span class="sxs-lookup"><span data-stu-id="9b147-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="9b147-128">否则，视为有存货。</span><span class="sxs-lookup"><span data-stu-id="9b147-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="9b147-129">**库存不足阈值** 值的能力是有限的，我们不建议您在版本 10.0.12 及更高版本中使用它。</span><span class="sxs-lookup"><span data-stu-id="9b147-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="9b147-130">**多个仓库的库存级别** – 此设置可以针对默认仓库或多个仓库计算库存级别。</span><span class="sxs-lookup"><span data-stu-id="9b147-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="9b147-131">**基于单个仓库** 选项将基于默认仓库计算库存级别。</span><span class="sxs-lookup"><span data-stu-id="9b147-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="9b147-132">或者，电子商务站点可以指向多个仓库以推进履行。</span><span class="sxs-lookup"><span data-stu-id="9b147-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="9b147-133">在这种情况下，**基于装运和提货仓库的聚合** 选项用于指示存货可用性。</span><span class="sxs-lookup"><span data-stu-id="9b147-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="9b147-134">例如，当客户购买物料并选择“装运”作为交货方式时，可以从履行组中具有可用库存的任何仓库装运物料。</span><span class="sxs-lookup"><span data-stu-id="9b147-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="9b147-135">如果履行组中的任何可用装运仓库有库存，产品详细信息页 (PDP) 将为装运显示“有存货”消息。</span><span class="sxs-lookup"><span data-stu-id="9b147-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="9b147-136">**多个仓库的库存级别** 设置从 Commerce 版本 10.0.19 开始可用。</span><span class="sxs-lookup"><span data-stu-id="9b147-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="9b147-137">如果要从旧版本的 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="9b147-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="9b147-138">有关说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="9b147-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="9b147-139">**库存范围** – 此设置定义在站点模块上显示消息的库存范围。</span><span class="sxs-lookup"><span data-stu-id="9b147-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="9b147-140">仅当为 **库存级别确定条件** 选择了 **总可用量** 值或 **实际可用量** 值时，此设置才适用。</span><span class="sxs-lookup"><span data-stu-id="9b147-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="9b147-141">可用值有 **所有**、**低库存和库存不足** 和 **库存不足**。</span><span class="sxs-lookup"><span data-stu-id="9b147-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="9b147-142">选择 **所有** 时，将显示所有库存范围的消息，从有存货（“有货”消息）到库存不足（“库存不足”消息）。</span><span class="sxs-lookup"><span data-stu-id="9b147-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="9b147-143">选择 **低库存和库存不足** 时，将显示除有存货（“有货”消息）以外的所有库存范围的消息。</span><span class="sxs-lookup"><span data-stu-id="9b147-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="9b147-144">选择 **库存不足** 时，将仅显示“库存不足”消息。</span><span class="sxs-lookup"><span data-stu-id="9b147-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="9b147-145">**库存不足阈值** – 这是一个旧的数字设置，只有在为 **库存级别确定条件** 设置选择了 **库存不足阈值** 值时才会生效。</span><span class="sxs-lookup"><span data-stu-id="9b147-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="9b147-146">这些设置在 Dynamics 365 Commerce 10.0.12 版本中提供。</span><span class="sxs-lookup"><span data-stu-id="9b147-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="9b147-147">如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="9b147-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="9b147-148">有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="9b147-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="9b147-149">使用库存设置的模块</span><span class="sxs-lookup"><span data-stu-id="9b147-149">Modules that use inventory settings</span></span>

<span data-ttu-id="9b147-150">购买框、愿望列表、商店选择器、购物车和购物车图标模块使用库存设置显示库存范围和消息。</span><span class="sxs-lookup"><span data-stu-id="9b147-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="9b147-151">在下图的示例中，PDP 显示有存货（“可用”）消息。</span><span class="sxs-lookup"><span data-stu-id="9b147-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![显示有存货消息的 PDP 模块的示例](./media/pdp-InStock.png)

<span data-ttu-id="9b147-153">在下图的示例中，PDP 显示有“库存不足”消息。</span><span class="sxs-lookup"><span data-stu-id="9b147-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![显示库存不足消息的 PDP 模块的示例](./media/pdp-outofstock.png)

<span data-ttu-id="9b147-155&quot;>在下图的示例中，购物车显示有存货（“可用”）消息。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;9b147-155&quot;>In the example in the following illustration, a cart is showing an in-stock (&quot;Available") message.</span></span>

![显示有存货消息的购物车模块的示例](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="9b147-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="9b147-157">Additional resources</span></span>

[<span data-ttu-id="9b147-158">模块库概述</span><span class="sxs-lookup"><span data-stu-id="9b147-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9b147-159">配置库存缓冲区和库存级别</span><span class="sxs-lookup"><span data-stu-id="9b147-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="9b147-160">购物车模块</span><span class="sxs-lookup"><span data-stu-id="9b147-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9b147-161">购买框模块</span><span class="sxs-lookup"><span data-stu-id="9b147-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9b147-162">帐户管理页面和模块</span><span class="sxs-lookup"><span data-stu-id="9b147-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="9b147-163">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="9b147-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="9b147-164">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="9b147-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
