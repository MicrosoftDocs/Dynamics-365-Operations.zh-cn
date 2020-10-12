---
title: 付款模块
description: 此主题介绍付款模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818318"
---
# <a name="payment-module"></a>付款模块

[!include [banner](includes/banner.md)]

此主题介绍付款模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

## <a name="overview"></a>概览

付款模块使客户可以使用信用卡或借记卡支付订单。 此模块的付款集成由适用于 Adyen 的 Dynamics 365 付款连接器提供。 有关如何设置和配置付款连接器的详细信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)。

付款模块将通过 Adyen 提供的付款信息托管在 HTML 内联框架 (iframe) 中。 付款模块与 Commerce Scale Unit 交互来检索 Adyen 付款信息。 作为 Commerce Scale Unit 交互的一部分，支付模块可以允许在 iframe 中或作为单独的模块提供账单地址信息。 在 Fabrikam 主题中，账单地址显示在单独的模块中。 此方法具有更大的格式灵活性，因为可以呈现地址行，使其类似于装运地址的行。

付款模块还使登录客户可以保存其付款信息。 付款信息和账单地址通过 Adyen 付款连接器保存和管理。

付款模块包含会员积分或礼品卡未覆盖的所有订单费用。 如果订单总计已完全由会员积分或礼品卡积分覆盖，付款模块将被隐藏，客户可以不使用付款模块下订单。

Adyen 付款连接器还支持强大客户身份验证 (SCA)。 欧盟 (EU) 付款服务规定 2.0 (PSD2.0) 的一部分要求在线购物者在使用电子付款方式时，必须在其在线购物体验之外进行身份验证。 在结帐流中，客户将被重定向到他们的银行站点。 然后，在进行身份验证之后，它们将被重定向回 Commerce 结帐流。 在此重定向过程中，客户在结帐流中输入的信息（例如，装运地址、交货选项、礼品卡信息和会员信息）将保持不变。 必须先在 Commerce headquarters 中为 SCA 配置付款连接器，然后才能打开此功能。 有关详细信息，请参阅[使用 Adyen 的强大客户身份验证](adyen_redirect.md)。

下图显示了结帐页面上的礼品卡、会员和付款模块的示例。

![结帐页面上的礼品卡、会员和付款模块的示例](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>付款模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题 | 标题文本 | 付款模块的可选标题。 |
| iframe 的高度 | 像素 | iframe 高度（以像素为单位）。 可以根据需要调整此高度。 |
| 显示帐单地址 | **True** 或 **False** | 如果将此属性设置为 **True**，账单地址将由 Adyen 在付款模块 iframe 中提供。 如果设置为 **False**，Adyen 将不会提供账单地址，Commerce 用户必须配置一个模块来在结帐页面上显示账单地址。 |
| 付款方式覆盖 | 级联样式表 (CSS) 代码 | 由于付款模块托管在 iframe 中，因此样式功能有限。 您可以使用此属性来实现某些样式。 要覆盖站点样式，必须粘贴 CSS 代码作为此属性的值。 站点构建器 CSS 覆盖和样式不适用于此模块。 |

## <a name="billing-address"></a>帐单地址

付款模块使客户可以在付款信息中提供账单地址。 它还使他们可以将装运地址用作账单地址，从而使结帐流更加轻松快捷。 如果将**显示账单地址**属性设置为 **False**，应在结帐页面上配置付款模块。

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>向结帐页面添加付款模块和设置必需的属性

付款模块只能添加到结帐模块。 有关如何为结帐页面配置付款模块的详细信息，请参阅[结帐模块](add-checkout-module.md)。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结帐模块](add-checkout-module.md)

[收货地址模块](ship-address-module.md)

[交付选项模块](delivery-options-module.md)

[订单详细信息模块](order-confirmation-module.md)

[礼品卡模块](add-giftcard.md)

[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)

[使用 Adyen 的强大客户身份验证](adyen_redirect.md)
