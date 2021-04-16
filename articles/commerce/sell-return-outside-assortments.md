---
title: 销售和退回不属于商店分类的产品
description: 借助 Dynamics 365 Commerce，您可以销售和退回分类以外的产品。
author: pdp1207
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b6bae9f0d3a236c69ee3ee47226c19c1e1dcaf42
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794035"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="c1ec1-103">销售和退回不属于商店分类的产品</span><span class="sxs-lookup"><span data-stu-id="c1ec1-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1ec1-104">对于任何零售商的一个常见方案是将产品销售给他们的客户或接受客户的退货，即使他们在商店并不存放特定的产品（换言之，该产品未分类到商店）。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="c1ec1-105">下面是一些典型方案：</span><span class="sxs-lookup"><span data-stu-id="c1ec1-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="c1ec1-106">零售商不将它的所有产品存放在特定的商店中。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="c1ec1-107">剩余的产品存储在仓库中。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="c1ec1-108">商店的同事可以协助客户在仓库中搜索或浏览产品，将其添加到购物车，并通过选择交货方法（例如，装运到来自仓库的地址或让客户从当前商店或其他商店提取产品）完成结帐。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="c1ec1-109">零售商不将特定产品存放在商店中，或者在客户访问的商店中没有存货，但在其他商店提供该产品。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="c1ec1-110">商店同事可以协助客户在其他商店中搜索或浏览产品，将其添加到购物车中，并通过选择交货方法完成结帐。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="c1ec1-111">零售商在特定的城市或邮政编码区范围内和附近有许多家商店，并且不想强迫客户将产品退回到购买产品时的同一家商店。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="c1ec1-112">相反，客户可以将产品退回到任何一家商店。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="c1ec1-113">这些常见方案对使用 Commerce 的零售商提供。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="c1ec1-114">借助 Commerce，您可以：</span><span class="sxs-lookup"><span data-stu-id="c1ec1-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="c1ec1-115">搜索或浏览其他商店的产品。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="c1ec1-116">搜索或浏览所有已发布的产品。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="c1ec1-117">创建现金和结转交易记录或客户订单。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="c1ec1-118">选择客户订单的交货选项。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="c1ec1-119">在当前商店或其他商店提取产品。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="c1ec1-120">在当前商店或其他商店取消订单。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="c1ec1-121">在当前商店或其他商店持收据或不持收据退回订单。</span><span class="sxs-lookup"><span data-stu-id="c1ec1-121">Return an order with or without the receipt at the current store or another store.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]