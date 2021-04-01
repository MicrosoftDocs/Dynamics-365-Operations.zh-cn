---
title: 为在线订单配置销售税
description: 此主题概述了 Dynamics 365 Commerce 中不同在线订单类型的销售税组选择。
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254833"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="259b9-103">为在线订单配置销售税</span><span class="sxs-lookup"><span data-stu-id="259b9-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="259b9-104">此主题概述了不同在线订单类型的销售税组选择。</span><span class="sxs-lookup"><span data-stu-id="259b9-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="259b9-105">您的电子商务渠道可能希望支持在线订单交货或提货等选项。</span><span class="sxs-lookup"><span data-stu-id="259b9-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="259b9-106">销售税的适用性基于您的在线用户选择的选项。</span><span class="sxs-lookup"><span data-stu-id="259b9-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="259b9-107">当站点客户选择在线购买商品并将其装运到某个地址时，销售税根据客户的装运地址税组设置确定。</span><span class="sxs-lookup"><span data-stu-id="259b9-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="259b9-108">当客户选择在商店提取购买的商品时，销售税根据提货商店的税组设置确定。</span><span class="sxs-lookup"><span data-stu-id="259b9-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="259b9-109">装运到客户地址的订单</span><span class="sxs-lookup"><span data-stu-id="259b9-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="259b9-110">通常，装运到客户地址的在线订单的税金由目的地定义。</span><span class="sxs-lookup"><span data-stu-id="259b9-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="259b9-111">每个销售税组有一个基于零售目的地的税金配置，在此配置中，您的企业可以通过分层形式定义目的地详细信息，如国家/地区、省/自治区/直辖市、县和城市。</span><span class="sxs-lookup"><span data-stu-id="259b9-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="259b9-112">下达在线订单后，Commerce 税引擎使用订单中每个行项的交货地址，按照匹配的基于目的地的税收标准查找销售税组。</span><span class="sxs-lookup"><span data-stu-id="259b9-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="259b9-113">例如，对于行项交货地址是到加利福尼亚州旧金山的在线订单，税引擎将查找加利福尼亚的销售税组和销售税代码，然后相应地计算每个行项的税金。</span><span class="sxs-lookup"><span data-stu-id="259b9-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="259b9-114">基于客户的税组</span><span class="sxs-lookup"><span data-stu-id="259b9-114">Customer-based tax groups</span></span>

<span data-ttu-id="259b9-115">在 Commerce headquarters 中，有两个地方可以配置客户税组：</span><span class="sxs-lookup"><span data-stu-id="259b9-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="259b9-116">**客户配置文件**</span><span class="sxs-lookup"><span data-stu-id="259b9-116">**Customer's profile**</span></span>
- <span data-ttu-id="259b9-117">**客户装运地址**</span><span class="sxs-lookup"><span data-stu-id="259b9-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="259b9-118">如果客户配置文件配置了税组</span><span class="sxs-lookup"><span data-stu-id="259b9-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="259b9-119">Headquarters 中的客户配置文件记录可能已经配置了销售税组，但是，对于在线订单，在客户配置文件中配置的销售税组不会被税引擎使用。</span><span class="sxs-lookup"><span data-stu-id="259b9-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="259b9-120">如果客户装运地址配置了税组</span><span class="sxs-lookup"><span data-stu-id="259b9-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="259b9-121">如果客户的装运地址记录配置了税组，当在线订单（或行项）装运到客户的装运地址时，客户地址记录中配置的税组会被税引擎用来计算税金。</span><span class="sxs-lookup"><span data-stu-id="259b9-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="259b9-122">为客户的装运地址记录配置税组</span><span class="sxs-lookup"><span data-stu-id="259b9-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="259b9-123">要在 Commerce headquarters 中为客户的装运地址记录配置税组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="259b9-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="259b9-124">转到 **所有顾客**，然后选择所需的客户。</span><span class="sxs-lookup"><span data-stu-id="259b9-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="259b9-125">在 **地址** 快速选项卡上，选择所需的地址，然后选择 **更多选项 \> 高级**。</span><span class="sxs-lookup"><span data-stu-id="259b9-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="259b9-126">在 **管理地址** 页上的 **常规** 选项卡下，根据需要设置销售税值。</span><span class="sxs-lookup"><span data-stu-id="259b9-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="259b9-127">税组使用订单行的交货地址定义，基于目的地的税金在税组中配置。</span><span class="sxs-lookup"><span data-stu-id="259b9-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="259b9-128">有关详细信息，请参阅[设置基于目的地的在线商店税金](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)。</span><span class="sxs-lookup"><span data-stu-id="259b9-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="259b9-129">订单在店内提货</span><span class="sxs-lookup"><span data-stu-id="259b9-129">Order pickup in store</span></span>

<span data-ttu-id="259b9-130">对于指定了店内提货或路边提货的订单行，将应用所选提货商店的税组。</span><span class="sxs-lookup"><span data-stu-id="259b9-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="259b9-131">有关如何为给定商店配置税组的详细信息，请参阅[设置商店的其他税金选项](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)。</span><span class="sxs-lookup"><span data-stu-id="259b9-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="259b9-132">当订单行是在商店提货时，客户地址的税金设置（如果已设置）将被税引擎忽略，将应用提货商店的税金配置。</span><span class="sxs-lookup"><span data-stu-id="259b9-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="259b9-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="259b9-133">Additional resources</span></span>

[<span data-ttu-id="259b9-134">销售税概览</span><span class="sxs-lookup"><span data-stu-id="259b9-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="259b9-135">“源”字段中的销售税计算方法</span><span class="sxs-lookup"><span data-stu-id="259b9-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="259b9-136"> 销售税分配和覆盖</span><span class="sxs-lookup"><span data-stu-id="259b9-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="259b9-137">全部金额和销售税代码的间隔计算选项</span><span class="sxs-lookup"><span data-stu-id="259b9-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="259b9-138">免税的计算</span><span class="sxs-lookup"><span data-stu-id="259b9-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]