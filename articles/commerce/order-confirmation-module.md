---
title: 订单确认模块
description: 本主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中使用它们。
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972727"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="33b0d-103">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33b0d-104">本主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中使用它们。</span><span class="sxs-lookup"><span data-stu-id="33b0d-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="33b0d-105">概览</span><span class="sxs-lookup"><span data-stu-id="33b0d-105">Overview</span></span>

<span data-ttu-id="33b0d-106">下订单之后，将使用订单确认模块显示订单确认详细信息。</span><span class="sxs-lookup"><span data-stu-id="33b0d-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="33b0d-107">它显示订单确认 ID、订单联系人信息和其他订单详细信息，例如购买的物料、付款信息、提货选项和装运方式。</span><span class="sxs-lookup"><span data-stu-id="33b0d-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="33b0d-108">订单确认模块属性</span><span class="sxs-lookup"><span data-stu-id="33b0d-108">Order confirmation module properties</span></span>

| <span data-ttu-id="33b0d-109">属性名称</span><span class="sxs-lookup"><span data-stu-id="33b0d-109">Property name</span></span>  | <span data-ttu-id="33b0d-110">值</span><span class="sxs-lookup"><span data-stu-id="33b0d-110">Values</span></span> | <span data-ttu-id="33b0d-111">说明</span><span class="sxs-lookup"><span data-stu-id="33b0d-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="33b0d-112">标题</span><span class="sxs-lookup"><span data-stu-id="33b0d-112">Heading</span></span>        | <span data-ttu-id="33b0d-113">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="33b0d-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="33b0d-114">订单确认模块可以有标题。</span><span class="sxs-lookup"><span data-stu-id="33b0d-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="33b0d-115">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="33b0d-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="33b0d-116">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="33b0d-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="33b0d-117">联系人号码</span><span class="sxs-lookup"><span data-stu-id="33b0d-117">Contact number</span></span> | <span data-ttu-id="33b0d-118">文本</span><span class="sxs-lookup"><span data-stu-id="33b0d-118">Text</span></span> | <span data-ttu-id="33b0d-119">可以为与订单相关的问题提供联系人号码。</span><span class="sxs-lookup"><span data-stu-id="33b0d-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="33b0d-120">显示提货时隙信息</span><span class="sxs-lookup"><span data-stu-id="33b0d-120">Show pickup timeslot information</span></span> | <span data-ttu-id="33b0d-121">真或假</span><span class="sxs-lookup"><span data-stu-id="33b0d-121">True or False</span></span> | <span data-ttu-id="33b0d-122">此属性在 Dynamics 365 Commerce 10.0.15 及更高版本中提供。</span><span class="sxs-lookup"><span data-stu-id="33b0d-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="33b0d-123">当为 true 时，将显示为提货物料提供的提货时隙信息</span><span class="sxs-lookup"><span data-stu-id="33b0d-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="33b0d-124">订单确认页面上可以使用的模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="33b0d-125">创建订单确认页面时，除了订单确认模块外，您还可以添加其他相关模块。</span><span class="sxs-lookup"><span data-stu-id="33b0d-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="33b0d-126">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="33b0d-126">Here are some examples:</span></span>

- <span data-ttu-id="33b0d-127">**建议模块** – 可将建议模块添加到订单确认页面，以便向客户推荐其他产品。</span><span class="sxs-lookup"><span data-stu-id="33b0d-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="33b0d-128">**市场营销模块** – 可以将任何市场营销模块添加到订单确认页面以显示市场营销内容。</span><span class="sxs-lookup"><span data-stu-id="33b0d-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="33b0d-129">向页面添加订单确认模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="33b0d-130">若要向新页面添加订单确认模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="33b0d-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="33b0d-131">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="33b0d-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="33b0d-132">在 **新建模板** 对话框的 **模板名称** 下，输入名称 **订单确认模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="33b0d-133">在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33b0d-134">在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33b0d-135">在 **默认页** 模块的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33b0d-136">在 **添加模块** 对话框中，选择 **订单确认** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33b0d-137">选择 **保存**，然后选择 **预览** 预览模板。</span><span class="sxs-lookup"><span data-stu-id="33b0d-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="33b0d-138">不显示此订单确认模块，因为它需要订单确认编号的上下文。</span><span class="sxs-lookup"><span data-stu-id="33b0d-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="33b0d-139">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="33b0d-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="33b0d-140">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="33b0d-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="33b0d-141">在 **选择模板** 对话框中，选择 **订单确认模板**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="33b0d-142">在 **页面名称** 下，输入 **订单确认页面**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="33b0d-143">在 **默认页** 模块的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33b0d-144">在 **添加模块** 对话框中，选择 **订单确认** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33b0d-145">在订单确认模块的属性窗格中，选择铅笔符号旁边的 **标题**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="33b0d-146">在 **标题** 对话框的 **标题文本** 字段中，输入标题文本 **订单确认**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33b0d-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="33b0d-147">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="33b0d-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="33b0d-148">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="33b0d-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33b0d-149">其他资源</span><span class="sxs-lookup"><span data-stu-id="33b0d-149">Additional resources</span></span>

[<span data-ttu-id="33b0d-150">购物车模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="33b0d-151">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="33b0d-152">结帐模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="33b0d-153">付款模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="33b0d-154">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="33b0d-155">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="33b0d-156">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="33b0d-157">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="33b0d-157">Gift card module</span></span>](add-giftcard.md)
