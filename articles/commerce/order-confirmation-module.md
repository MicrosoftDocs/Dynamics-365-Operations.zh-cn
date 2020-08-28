---
title: 订单详细信息模块
description: 此主题介绍订单详细信息模块和如何在 Microsoft Dynamics 365 Commerce 中使用该模块。
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661164"
---
# <a name="order-details-module"></a><span data-ttu-id="efe48-103">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="efe48-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="efe48-104">此主题介绍订单详细信息模块和如何在 Microsoft Dynamics 365 Commerce 中使用该模块。</span><span class="sxs-lookup"><span data-stu-id="efe48-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="efe48-105">概览</span><span class="sxs-lookup"><span data-stu-id="efe48-105">Overview</span></span>

<span data-ttu-id="efe48-106">下订单之后，将使用订单详细信息模块显示订单确认详细信息。</span><span class="sxs-lookup"><span data-stu-id="efe48-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="efe48-107">它显示订单确认 ID、订单联系人信息和其他订单详细信息，例如购买的商品、付款信息和装运方式。</span><span class="sxs-lookup"><span data-stu-id="efe48-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="efe48-108">订单详细信息模块属性</span><span class="sxs-lookup"><span data-stu-id="efe48-108">Order details module properties</span></span>

| <span data-ttu-id="efe48-109">属性名称</span><span class="sxs-lookup"><span data-stu-id="efe48-109">Property name</span></span>  | <span data-ttu-id="efe48-110">值</span><span class="sxs-lookup"><span data-stu-id="efe48-110">Values</span></span> | <span data-ttu-id="efe48-111">说明</span><span class="sxs-lookup"><span data-stu-id="efe48-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="efe48-112">标题</span><span class="sxs-lookup"><span data-stu-id="efe48-112">Heading</span></span>        | <span data-ttu-id="efe48-113">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="efe48-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="efe48-114">订单详细信息模块可以有标题。</span><span class="sxs-lookup"><span data-stu-id="efe48-114">The order details module can have a heading.</span></span> <span data-ttu-id="efe48-115">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="efe48-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="efe48-116">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="efe48-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="efe48-117">联系人号码</span><span class="sxs-lookup"><span data-stu-id="efe48-117">Contact number</span></span> | <span data-ttu-id="efe48-118">文本</span><span class="sxs-lookup"><span data-stu-id="efe48-118">Text</span></span> | <span data-ttu-id="efe48-119">可以为与订单相关的问题提供联系人号码。</span><span class="sxs-lookup"><span data-stu-id="efe48-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="efe48-120">订单详细信息页面中可以使用的模块</span><span class="sxs-lookup"><span data-stu-id="efe48-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="efe48-121">创建订单详细信息页面时，除了订单详细信息模块外，您还可以添加其他相关模块。</span><span class="sxs-lookup"><span data-stu-id="efe48-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="efe48-122">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="efe48-122">Here are some examples:</span></span>

- <span data-ttu-id="efe48-123">**建议模块** – 可将建议模块放到订单详细信息页中，以便向客户推荐其他产品。</span><span class="sxs-lookup"><span data-stu-id="efe48-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="efe48-124">**市场营销模块** – 可以将任何市场营销模块添加到订单详细信息页面以显示市场营销内容。</span><span class="sxs-lookup"><span data-stu-id="efe48-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="efe48-125">向页面添加订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="efe48-125">Add an order details module to a page</span></span>

<span data-ttu-id="efe48-126">若要向新页面添加订单详细信息模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="efe48-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="efe48-127">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="efe48-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="efe48-128">在**新建模板**对话框的**模板名称**下，输入名称**订单详细信息模板**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="efe48-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="efe48-129">在**正文**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="efe48-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="efe48-130">在**添加模块**对话框中，选择**默认页面**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="efe48-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="efe48-131">在**默认页**模块的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="efe48-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="efe48-132">在**添加模块**对话框中，选择**订单详细信息**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="efe48-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="efe48-133">选择**保存**，然后选择**预览**预览模板。</span><span class="sxs-lookup"><span data-stu-id="efe48-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="efe48-134">不会显示此订单详细信息模块，因为它需要订单确认编号的上下文。</span><span class="sxs-lookup"><span data-stu-id="efe48-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="efe48-135">选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="efe48-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="efe48-136">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="efe48-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="efe48-137">在**选择模板**对话框中，选择**订单详细信息模板**。</span><span class="sxs-lookup"><span data-stu-id="efe48-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="efe48-138">在**页面名称**下，输入**订单详细信息页面**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="efe48-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="efe48-139">在**默认页**模块的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="efe48-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="efe48-140">在**添加模块**对话框中，选择**订单详细信息**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="efe48-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="efe48-141">在订单详细信息模块的属性窗格中，选择铅笔符号旁边的**标题**。</span><span class="sxs-lookup"><span data-stu-id="efe48-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="efe48-142">在**标题**对话框的**标题文本**字段中，输入标题文本**订单详细信息**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="efe48-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="efe48-143">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="efe48-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="efe48-144">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="efe48-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efe48-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="efe48-145">Additional resources</span></span>

[<span data-ttu-id="efe48-146">购物车模块</span><span class="sxs-lookup"><span data-stu-id="efe48-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="efe48-147">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="efe48-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="efe48-148">结帐模块</span><span class="sxs-lookup"><span data-stu-id="efe48-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="efe48-149">付款模块</span><span class="sxs-lookup"><span data-stu-id="efe48-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="efe48-150">装运地址模块</span><span class="sxs-lookup"><span data-stu-id="efe48-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="efe48-151">交货选项模块</span><span class="sxs-lookup"><span data-stu-id="efe48-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="efe48-152">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="efe48-152">Gift card module</span></span>](add-giftcard.md)
