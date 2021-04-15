---
title: “提货”选项没有出现在购物车或产品详细信息页面上
description: 本主题提供了故障排除指南，可以在购物车页面或产品详细信息页面上未显示店内提货选项时提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46eeed18bb547035603d7e9a01e8f131a2393f01
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801619"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="2df82-103">“提货”选项没有出现在购物车或产品详细信息页面上</span><span class="sxs-lookup"><span data-stu-id="2df82-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2df82-104">本主题提供了故障排除指南，可以在购物车页面或产品详细信息页面上未显示店内提货选项时提供帮助。</span><span class="sxs-lookup"><span data-stu-id="2df82-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="2df82-105">说明</span><span class="sxs-lookup"><span data-stu-id="2df82-105">Description</span></span>

<span data-ttu-id="2df82-106">**提货** 选项没有出现在购物车页面或产品详细信息页面上。</span><span class="sxs-lookup"><span data-stu-id="2df82-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="2df82-107">下图显示了一个包括 **提货** 按钮的页面示例。</span><span class="sxs-lookup"><span data-stu-id="2df82-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![“提货”按钮](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="2df82-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="2df82-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="2df82-110">在 Commerce 站点构建器中启用 BOPIS 扩展</span><span class="sxs-lookup"><span data-stu-id="2df82-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="2df82-111">要在 Commerce 站点构建器中启用“线上购买，店内提货”(BOPIS) 扩展，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2df82-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2df82-112">选择您的站点。</span><span class="sxs-lookup"><span data-stu-id="2df82-112">Select your site.</span></span>
1. <span data-ttu-id="2df82-113">选择 **站点设置**，然后选择 **扩展**。</span><span class="sxs-lookup"><span data-stu-id="2df82-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="2df82-114">确保已清除 **禁用 BOPIS** 选项。</span><span class="sxs-lookup"><span data-stu-id="2df82-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="2df82-115">在 Commerce Headquarters 中配置交付方式</span><span class="sxs-lookup"><span data-stu-id="2df82-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="2df82-116">要在 Commerce Headquarters 中配置交付方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2df82-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2df82-117">转到 **采购 \> 设置 \> 交付方式**。</span><span class="sxs-lookup"><span data-stu-id="2df82-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="2df82-118">确保已创建 **客户提货** 交付方式，并为其分配了产品和地址。</span><span class="sxs-lookup"><span data-stu-id="2df82-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="2df82-119">转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数**。</span><span class="sxs-lookup"><span data-stu-id="2df82-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="2df82-120">在左侧导航栏中，选择 **客户订单**。</span><span class="sxs-lookup"><span data-stu-id="2df82-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="2df82-121">确保已正确配置 **提货交货方式**。</span><span class="sxs-lookup"><span data-stu-id="2df82-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="2df82-122">配置客户订单付款</span><span class="sxs-lookup"><span data-stu-id="2df82-122">Configure customer orders payments</span></span>

<span data-ttu-id="2df82-123">要在 Commerce Headquarters 中配置客户订单付款，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2df82-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2df82-124">转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数**。</span><span class="sxs-lookup"><span data-stu-id="2df82-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="2df82-125">在左侧导航栏中，选择 **客户订单**。</span><span class="sxs-lookup"><span data-stu-id="2df82-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="2df82-126">在 **付款** 快速选项卡上，请确保 **付款条款** 和 **付款方式** 字段设置正确。</span><span class="sxs-lookup"><span data-stu-id="2df82-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2df82-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="2df82-127">Additional resources</span></span>

[<span data-ttu-id="2df82-128">配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="2df82-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="2df82-129">为客户订单启用多种提货交货方式</span><span class="sxs-lookup"><span data-stu-id="2df82-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="2df82-130">全渠道 Commerce 订单付款</span><span class="sxs-lookup"><span data-stu-id="2df82-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="2df82-131">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="2df82-131">Store selector module</span></span>](../store-selector.md)
