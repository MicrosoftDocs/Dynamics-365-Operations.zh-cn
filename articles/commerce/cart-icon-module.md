---
title: 购物车图标模块
description: 此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261554"
---
# <a name="cart-icon-module"></a><span data-ttu-id="4283d-103">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="4283d-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4283d-104">此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="4283d-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4283d-105">概览</span><span class="sxs-lookup"><span data-stu-id="4283d-105">Overview</span></span>

<span data-ttu-id="4283d-106">购物车图标模块在页面的页眉模块中提供购物车，并显示购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="4283d-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="4283d-107">将鼠标光标悬停在购物车图标上方时，购物车图标模块还会显示购物车摘要（也称为迷你购物车）。</span><span class="sxs-lookup"><span data-stu-id="4283d-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="4283d-108">用户不必导航到购物车页面，迷你购物车就为用户提供购物车中的商品摘要。</span><span class="sxs-lookup"><span data-stu-id="4283d-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="4283d-109">此外，还允许用户在对摘要满意的情况下直接转到结帐页面。</span><span class="sxs-lookup"><span data-stu-id="4283d-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="4283d-110">这样可以减少页面导航次数，加快结帐速度。</span><span class="sxs-lookup"><span data-stu-id="4283d-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="4283d-111">模块属性</span><span class="sxs-lookup"><span data-stu-id="4283d-111">Module properties</span></span>

- <span data-ttu-id="4283d-112">**显示迷你购物车** – 如果为 true，此属性用于启用将鼠标光标悬停在购物车图标上方时显示的购物车摘要（迷你购物车）。</span><span class="sxs-lookup"><span data-stu-id="4283d-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="4283d-113">只有桌面视图端口中才支持此功能。</span><span class="sxs-lookup"><span data-stu-id="4283d-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="4283d-114">向页面添加购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="4283d-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="4283d-115">若要添加购物车图标模块，请参阅[页眉模块](author-header-module.md)。</span><span class="sxs-lookup"><span data-stu-id="4283d-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="4283d-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="4283d-116">Additional resources</span></span>

[<span data-ttu-id="4283d-117">购买框模块</span><span class="sxs-lookup"><span data-stu-id="4283d-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4283d-118">购物车模块</span><span class="sxs-lookup"><span data-stu-id="4283d-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4283d-119">结账模块</span><span class="sxs-lookup"><span data-stu-id="4283d-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4283d-120">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="4283d-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4283d-121">页眉模块</span><span class="sxs-lookup"><span data-stu-id="4283d-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4283d-122">页脚模块</span><span class="sxs-lookup"><span data-stu-id="4283d-122">Footer module</span></span>](author-footer-module.md)
