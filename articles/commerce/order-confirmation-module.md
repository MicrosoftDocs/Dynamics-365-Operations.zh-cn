---
title: 订单详细信息模块
description: 此主题介绍订单详细信息模块和如何在 Microsoft Dynamics 365 Commerce 中使用该模块。
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026009"
---
# <a name="order-details-module"></a><span data-ttu-id="1bf64-103">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1bf64-104">此主题介绍订单详细信息模块和如何在 Microsoft Dynamics 365 Commerce 中使用该模块。</span><span class="sxs-lookup"><span data-stu-id="1bf64-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1bf64-105">概览</span><span class="sxs-lookup"><span data-stu-id="1bf64-105">Overview</span></span>

<span data-ttu-id="1bf64-106">下订单之后，将使用订单详细信息模块显示订单确认详细信息。</span><span class="sxs-lookup"><span data-stu-id="1bf64-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="1bf64-107">它显示订单确认 ID、订单联系人信息和其他订单详细信息，例如购买的商品、付款信息和装运方式。</span><span class="sxs-lookup"><span data-stu-id="1bf64-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="1bf64-108">订单确认模块属性</span><span class="sxs-lookup"><span data-stu-id="1bf64-108">Order confirmation module properties</span></span>

| <span data-ttu-id="1bf64-109">属性名称</span><span class="sxs-lookup"><span data-stu-id="1bf64-109">Property name</span></span>  | <span data-ttu-id="1bf64-110">值</span><span class="sxs-lookup"><span data-stu-id="1bf64-110">Values</span></span> | <span data-ttu-id="1bf64-111">说明</span><span class="sxs-lookup"><span data-stu-id="1bf64-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1bf64-112">标题</span><span class="sxs-lookup"><span data-stu-id="1bf64-112">Heading</span></span>        | <span data-ttu-id="1bf64-113">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="1bf64-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1bf64-114">订单确认模块可以有标题。</span><span class="sxs-lookup"><span data-stu-id="1bf64-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="1bf64-115">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="1bf64-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="1bf64-116">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="1bf64-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="1bf64-117">联系人号码</span><span class="sxs-lookup"><span data-stu-id="1bf64-117">Contact number</span></span> | <span data-ttu-id="1bf64-118">文本</span><span class="sxs-lookup"><span data-stu-id="1bf64-118">Text</span></span> | <span data-ttu-id="1bf64-119">可以为与订单相关的问题提供联系人号码。</span><span class="sxs-lookup"><span data-stu-id="1bf64-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="1bf64-120">订单详细信息页面中可以使用的模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="1bf64-121">创建订单详细信息页面时，除了订单详细信息模块外，您还可以添加其他相关模块。</span><span class="sxs-lookup"><span data-stu-id="1bf64-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="1bf64-122">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="1bf64-122">Here are some examples:</span></span>

- <span data-ttu-id="1bf64-123">**建议模块** – 可将建议模块放到订单详细信息页中，以便向客户推荐其他产品。</span><span class="sxs-lookup"><span data-stu-id="1bf64-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="1bf64-124">**市场营销模块** – 可以将任何市场营销模块添加到订单详细信息页面以显示市场营销内容。</span><span class="sxs-lookup"><span data-stu-id="1bf64-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="1bf64-125">创建订单详细信息页模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-125">Create an order details page module</span></span>

1. <span data-ttu-id="1bf64-126">创建一个名称为**订单详细信息模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="1bf64-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="1bf64-127">在默认页的**主**插槽中，添加一个订单详细信息模块。</span><span class="sxs-lookup"><span data-stu-id="1bf64-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="1bf64-128">在订单详细信息模块中，添加一个建议模块。</span><span class="sxs-lookup"><span data-stu-id="1bf64-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="1bf64-129">保存并预览模板。</span><span class="sxs-lookup"><span data-stu-id="1bf64-129">Save and preview the template.</span></span> <span data-ttu-id="1bf64-130">不会显示此订单详细信息模块，因为它需要订单确认编号的上下文。</span><span class="sxs-lookup"><span data-stu-id="1bf64-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="1bf64-131">编辑完模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="1bf64-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="1bf64-132">使用您刚才创建的订单详细信息模板创建一个名称为**订单详细信息页**的页面。</span><span class="sxs-lookup"><span data-stu-id="1bf64-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="1bf64-133">向页面大纲添加默认页。</span><span class="sxs-lookup"><span data-stu-id="1bf64-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="1bf64-134">在**页眉**插槽中，添加一个页眉片段。</span><span class="sxs-lookup"><span data-stu-id="1bf64-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="1bf64-135">在**页脚**插槽中，添加一个页脚片段。</span><span class="sxs-lookup"><span data-stu-id="1bf64-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="1bf64-136">在**主**插槽中，添加一个订单详细信息模块。</span><span class="sxs-lookup"><span data-stu-id="1bf64-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="1bf64-137">在订单详细信息模块的属性窗格中，添加标题**订单详细信息**。</span><span class="sxs-lookup"><span data-stu-id="1bf64-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="1bf64-138">在订单详细信息模块下，添加一个建议模块，然后将其配置为使用**新品**和**最畅销**设置。</span><span class="sxs-lookup"><span data-stu-id="1bf64-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="1bf64-139">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="1bf64-139">Save and preview the page.</span></span>
1. <span data-ttu-id="1bf64-140">编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="1bf64-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bf64-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="1bf64-141">Additional resources</span></span>

[<span data-ttu-id="1bf64-142">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="1bf64-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1bf64-143">容器模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1bf64-144">购买框模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1bf64-145">购物车模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1bf64-146">结帐模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1bf64-147">页眉模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1bf64-148">页脚模块</span><span class="sxs-lookup"><span data-stu-id="1bf64-148">Footer module</span></span>](author-footer-module.md)
