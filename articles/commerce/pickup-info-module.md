---
title: 提货信息模块
description: 此主题介绍提货信息模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的结帐页面。
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 61b97d72b6a397737c10476cd6c02764e60f10b1
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665340"
---
# <a name="pickup-information-module"></a><span data-ttu-id="32670-103">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="32670-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32670-104">此主题介绍提货信息模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的结帐页面。</span><span class="sxs-lookup"><span data-stu-id="32670-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="32670-105">提货信息模块可以在结帐模块中用来显示订单提货信息。</span><span class="sxs-lookup"><span data-stu-id="32670-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="32670-106">客户可以查看可用的提货日期和时隙，然后选择合适的时间提货。</span><span class="sxs-lookup"><span data-stu-id="32670-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="32670-107">例如，客户可以选择在 3 月 21 日下午 3 点从旧金山商店提货。</span><span class="sxs-lookup"><span data-stu-id="32670-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="32670-108">相应商店的提货时隙必须已在 Commerce headquarters 中配置。</span><span class="sxs-lookup"><span data-stu-id="32670-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="32670-109">有关详细信息，请参阅[创建和更新客户提货时隙](dev-itpro/pickup-timeslots.md)。</span><span class="sxs-lookup"><span data-stu-id="32670-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="32670-110">如果在结帐页面上创建了提货信息模块，但未为选择提货的商店定义时隙，模块会显示信息，但用户无法选择任何时隙。</span><span class="sxs-lookup"><span data-stu-id="32670-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="32670-111">时隙是可选的，不是下订单的必需条件。</span><span class="sxs-lookup"><span data-stu-id="32670-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="32670-112">如果跨多个商店选择了多个要提货的物料，提货信息模块将让用户为每个商店选择一个时隙，前提是时隙可供使用。</span><span class="sxs-lookup"><span data-stu-id="32670-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="32670-113">Dynamics 365 Commerce 版本 10.0.15 和更高版本中提供对时隙和结帐提货信息模块的支持。</span><span class="sxs-lookup"><span data-stu-id="32670-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="32670-114">下图显示了通过结帐页面上的提货信息模块选择时隙的示例。</span><span class="sxs-lookup"><span data-stu-id="32670-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![结帐页上的提货信息模块的示例](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="32670-116">模块属性</span><span class="sxs-lookup"><span data-stu-id="32670-116">Module properties</span></span>

- <span data-ttu-id="32670-117">**标题** – 输入模块的标题。</span><span class="sxs-lookup"><span data-stu-id="32670-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="32670-118">下订单后显示时隙信息</span><span class="sxs-lookup"><span data-stu-id="32670-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="32670-119">下订单后，可以在[订单确认模块](order-confirmation-module.md)和[订单详细信息模块](account-management.md#order-details-page)查看有关所选时隙的信息。</span><span class="sxs-lookup"><span data-stu-id="32670-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="32670-120">这两个模块都有 **显示时隙信息** 属性。</span><span class="sxs-lookup"><span data-stu-id="32670-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="32670-121">必须先将此属性设置为 **True**，模块才能在订购过程中显示所选的时隙。</span><span class="sxs-lookup"><span data-stu-id="32670-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="32670-122">将结帐提货信息模块添加到页面</span><span class="sxs-lookup"><span data-stu-id="32670-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="32670-123">有关如何将提货信息模块添加到结帐页面以及设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="32670-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="32670-124">下图显示了包括提货行项时隙的电子商务结帐页面的示例。</span><span class="sxs-lookup"><span data-stu-id="32670-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![包括提货行项时隙的电子商务结帐页面的示例](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="32670-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="32670-126">Additional resources</span></span>

[<span data-ttu-id="32670-127">创建和更新客户提货时隙</span><span class="sxs-lookup"><span data-stu-id="32670-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="32670-128">结帐模块</span><span class="sxs-lookup"><span data-stu-id="32670-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="32670-129">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="32670-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="32670-130">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="32670-130">Order details module</span></span>](account-management.md)
