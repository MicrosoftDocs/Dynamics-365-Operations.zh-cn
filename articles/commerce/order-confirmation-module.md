---
title: 订单确认模块
description: 此主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698318"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="9fa26-103">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9fa26-104">此主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。</span><span class="sxs-lookup"><span data-stu-id="9fa26-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9fa26-105">概览</span><span class="sxs-lookup"><span data-stu-id="9fa26-105">Overview</span></span>

<span data-ttu-id="9fa26-106">订单确认模块用于在下订单后在订单确认页面中显示确认消息。</span><span class="sxs-lookup"><span data-stu-id="9fa26-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="9fa26-107">订单确认模块显示结帐期间提供的订单确认编号和客户电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="9fa26-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="9fa26-108">当结帐期间下订单时，将把订单确认编号和客户电子邮件地址作为页面 URL 中的查询字符串传递到订单确认页。</span><span class="sxs-lookup"><span data-stu-id="9fa26-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="9fa26-109">订单确认模块将收到此信息，并在订单确认页显示订单状态。</span><span class="sxs-lookup"><span data-stu-id="9fa26-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="9fa26-110">订单确认模块需要此页面上下文才能提供订单状态。</span><span class="sxs-lookup"><span data-stu-id="9fa26-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="9fa26-111">订单确认模块属性</span><span class="sxs-lookup"><span data-stu-id="9fa26-111">Order confirmation module properties</span></span>

| <span data-ttu-id="9fa26-112">属性名称</span><span class="sxs-lookup"><span data-stu-id="9fa26-112">Property name</span></span> | <span data-ttu-id="9fa26-113">值</span><span class="sxs-lookup"><span data-stu-id="9fa26-113">Values</span></span> | <span data-ttu-id="9fa26-114">说明</span><span class="sxs-lookup"><span data-stu-id="9fa26-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="9fa26-115">标题</span><span class="sxs-lookup"><span data-stu-id="9fa26-115">Heading</span></span>       | <span data-ttu-id="9fa26-116">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="9fa26-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="9fa26-117">订单确认模块可以有标题。</span><span class="sxs-lookup"><span data-stu-id="9fa26-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="9fa26-118">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="9fa26-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="9fa26-119">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="9fa26-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="9fa26-120">订单确认页面模块中可以使用的模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="9fa26-121">**建议** – 可将建议模块放到订单确认页中，以便向客户推荐其他产品。</span><span class="sxs-lookup"><span data-stu-id="9fa26-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="9fa26-122">**市场营销** – 市场营销模块可以向订单确认页添加市场营销内容。</span><span class="sxs-lookup"><span data-stu-id="9fa26-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="9fa26-123">创建订单确认页模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="9fa26-124">创建一个名称为**订单确认模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="9fa26-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="9fa26-125">在默认页的**主**插槽中，添加一个订单确认模块。</span><span class="sxs-lookup"><span data-stu-id="9fa26-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="9fa26-126">在订单确认模块中，添加一个建议模块。</span><span class="sxs-lookup"><span data-stu-id="9fa26-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="9fa26-127">保存并预览模板。</span><span class="sxs-lookup"><span data-stu-id="9fa26-127">Save and preview the template.</span></span> <span data-ttu-id="9fa26-128">不应显示此订单确认模块，因为它需要订单确认编号的上下文。</span><span class="sxs-lookup"><span data-stu-id="9fa26-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="9fa26-129">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="9fa26-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="9fa26-130">使用您刚才创建的订单确认模板创建一个名称为**订单确认页**的页面。</span><span class="sxs-lookup"><span data-stu-id="9fa26-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="9fa26-131">向页面大纲添加默认页。</span><span class="sxs-lookup"><span data-stu-id="9fa26-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="9fa26-132">在**页眉**插槽中，添加一个页眉片段。</span><span class="sxs-lookup"><span data-stu-id="9fa26-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="9fa26-133">在**页脚**插槽中，添加一个页脚片段。</span><span class="sxs-lookup"><span data-stu-id="9fa26-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="9fa26-134">在**主**插槽中，添加一个订单确认模块。</span><span class="sxs-lookup"><span data-stu-id="9fa26-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="9fa26-135">在订单确认模块的属性窗格中，添加标题**订单确认**。</span><span class="sxs-lookup"><span data-stu-id="9fa26-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="9fa26-136">在订单确认模块下，添加一个建议模块，然后将其配置为使用**新品**和**最畅销**设置。</span><span class="sxs-lookup"><span data-stu-id="9fa26-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="9fa26-137">保存并预览页面，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="9fa26-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fa26-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="9fa26-138">Additional resources</span></span>

[<span data-ttu-id="9fa26-139">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="9fa26-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9fa26-140">容器模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9fa26-141">购买框模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9fa26-142">购物车模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9fa26-143">结帐模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="9fa26-144">页眉模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="9fa26-145">页脚模块</span><span class="sxs-lookup"><span data-stu-id="9fa26-145">Footer module</span></span>](author-footer-module.md)
