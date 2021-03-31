---
title: 付款模块
description: 此主题介绍付款模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: anupamar-ms
manager: annbe
ms.date: 11/18/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d9c0956e30d413f5ae695cf75b06fb58711b2944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222481"
---
# <a name="payment-module"></a>付款模块

[!include [banner](includes/banner.md)]

此主题介绍付款模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

付款模块使客户可以使用信用卡或借记卡支付订单。 此模块的付款集成由适用于 Adyen 的 Dynamics 365 付款连接器提供。 有关如何设置和配置付款连接器的详细信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)。  

从 Commerce 版本 10.0.14 开始，付款模块还与适用于 PayPal 的 Dynamics 365 Payment Connector 集成，以允许客户使用 PayPal 支付订单。 有关如何设置和配置适用于 PayPal 的 Dynamics 365 Payment Connector 的详细信息，请参阅[适用于 PayPal 的 Dynamics 365 Payment Connector](paypal.md)。 

## <a name="dynamics-365-payment-connector-for-adyen"></a>适用于 Adyen 的 Dynamics 365 付款连接器 

付款模块将通过 Adyen 提供的付款信息托管在 HTML 内联框架 (iframe) 中。 付款模块与 Commerce Scale Unit 交互来检索 Adyen 付款信息。 作为 Commerce Scale Unit 交互的一部分，支付模块可以允许通过 Adyen 在 iframe 中或作为单独的模块提供账单地址信息。 在 Fabrikam 主题中，账单地址作为单独的模块启用。 此方法具有更大的格式灵活性，因为可以呈现地址行，使其类似于装运地址的行。

付款模块还使登录客户可以保存其付款信息。 付款信息和账单地址通过 Adyen 付款连接器保存和管理。

付款模块包含会员积分或礼品卡未覆盖的所有订单费用。 如果订单总计已完全由会员积分或礼品卡积分覆盖，付款模块将被隐藏，客户可以不使用付款模块下订单。

Adyen 付款连接器还支持强大客户身份验证 (SCA)。 欧盟 (EU) 修订的付款服务规定 (PSD2) 的一部分要求在线购物者在使用电子付款方式时，必须在其在线购物体验之外进行身份验证。 在结帐流中，客户将重定向到其银行站点，然后在进行身份验证后，他们将重定向回 Commerce 结帐流。 在此重定向过程中，客户在结帐流中输入的信息（例如，装运地址、交货选项、礼品卡信息和会员信息）将保持不变。 必须先在 Commerce 总部中为 SCA 配置付款连接器，然后才能打开 Adyen Payment Connector。 有关详细信息，请参阅[使用 Adyen 的强大客户身份验证](adyen_redirect.md)。 此功能已在 Commerce 版本 10.0.12 中启用。

> [!NOTE]
> 对于 Adyen 付款连接器，仅在将 Adyen URL 添加到您的站点的允许列表时，才能显示付款模块中的 iframe 模块。 若要完成此步骤，请将 **\*.adyen.com** 添加到您的站点的内容安全策略的 **child-src**、**connect-src**、**img-src**、**script-src** 和 **style-src** 指令。 有关详细信息，请参阅[管理内容安全策略](manage-csp.md)。 

下图显示结帐页面上的礼品卡、会员和 Adyen 付款模块的示例。

![结帐页面上的礼品卡、会员和 Adyen 付款模块的示例](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>适用于 PayPal 的 Dynamics 365 Payment Connector

从 Commerce 版本 10.0.14 开始，付款模块还与适用于 PayPal 的 Dynamics 365 Payment Connector 集成。 有关如何设置和配置此付款连接器的详细信息，请参阅[适用于 PayPal 的 Dynamics 365 Payment Connector](paypal.md)。
 
在结帐页面上，可以同时配置 Adyen 和 PayPal 连接器。 付款模块已通过附加属性增强，有助于确定应使用的连接器。 有关详细信息，请参阅下表中的 **支持的支付方式** 和 **为主付款** 模块属性。
  
当付款模块配置为使用 PayPal Payment Connector 时，结帐页面上将显示 PayPal 按钮。 当付款模块由客户调用时，将显示包含 PayPal 信息的 iframe。 客户可以登录并在此 iframe 中提供其 PayPal 信息，以完成其交易。 当客户选择使用 PayPal 付款时，将通过 PayPal 收取订单上的余额。

PayPal Payment Connector 不需要账单地址模块，因为所有与账单相关的信息都由 PayPal 在其 iframe 中处理。 但是，需要装运地址和交货选项模块。

下图显示结帐页面上两个付款模块的示例，一个配置有 Adyen Payment Connector，另一个配置有 PayPal Payment Connector。
![结帐页面上的 Adyen 付款和 PayPal 模块的示例](./media/ecommerce-paypal.png)

下图显示使用 PayPal 按钮调用的 PayPal iframe 的示例。 
![结帐页面上的 Paypal iframe 的示例](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>付款模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题 | 标题文本 | 付款模块的可选标题。 |
| iframe 的高度 | 像素 | iframe 高度（以像素为单位）。 可以根据需要调整此高度。 |
| 显示帐单地址 | **True** 或 **False** | 如果将此属性设置为 **True**，账单地址将由 Adyen 在付款模块 iframe 中提供。 如果设置为 **False**，Adyen 将不会提供账单地址，Commerce 用户必须配置一个模块以在结帐页面上显示账单地址。 对于 PayPal Payment Connector，此字段没有影响，因为账单地址已在 PayPal 中完全处理。 |
| 付款方式覆盖 | 级联样式表 (CSS) 代码 | 由于付款模块托管在 iframe 中，因此样式功能有限。 您可以使用此属性来实现某些样式。 要覆盖站点样式，必须粘贴 CSS 代码作为此属性的值。 站点构建器 CSS 覆盖和样式不适用于此模块。 |
|支持的支付方式| 字符串| 如果配置了多个付款连接器，应提供在 Commerce 总部付款连接器配置中定义的受支持的支付方式字符串（请参见下图）。 如果为空白，则默认为 Adyen Payment Connector。 Commerce 版本 10.0.14 中已添加。|
|为主付款|  **True** 或 **False** | 如果为 **True**，将在结帐页面上从主付款连接器中生成任何错误消息。 如果同时配置了 Adyen Payment Connector 和 PayPal Payment Connector，请将 Adyen 设置为 **True**，已在 Commerce 版本 10.0.14 中添加它。|

下图显示在 Commerce 总部的付款连接器配置中 **支持的支付方式** 值设置为“PayPal”的示例。
![Commerce 总部中支持的支付方式的示例](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>帐单地址

如果 Adyen Payment Connector 账单地址行与站点其余部分的外观不完全匹配，则可以在结帐页面上使用账单地址模块。 

如果付款模块与 Adyen Payment Connector 集成，若要在结帐页面上使用账单地址模块，请将 **显示账单地址** 属性设置为 **False**，以便可以使用专用的账单地址模块，而不是默认的 Adyen 账单地址。 在这种情况下，站点作者应在结帐页面上包括账单地址模块。 Adyen Payment Connector 还允许将装运地址用作账单地址，以最大程度地减少站点用户的操作步骤。

与付款模块类似，在 Commerce 版本 10.0.14 中，**支持的支付方式** 属性已添加到账单地址模块。 此属性的值应与付款模块中提供的值相同，以确保它们可以一起使用。 对于 Adyen Payment Connector，付款模块和账单地址模块都应将此值保留为空白（默认状态）。 对于 PayPal 连接器，不需要专用的账单地址模块。 对于其他类型的付款连接器，应按照 Commerce 总部中的配置提供字符串。

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>向结帐页面添加付款模块和设置必需的属性

付款模块只能添加到结帐模块。 有关如何为结帐页面配置付款模块的详细信息，请参阅[结帐模块](add-checkout-module.md)。

如果同时需要 Adyen Payment Connector 和 PayPal Payment Connector，将这两个模块添加到付款部分。 确保已为 PayPal 配置 **支持的支付方式** 属性值，对于 Adyen 则保留为空白。 另外，对于 Adyen，将 **为主付款** 属性设置为 **True**。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结帐模块](add-checkout-module.md)

[收货地址模块](ship-address-module.md)

[交付选项模块](delivery-options-module.md)

[提货信息模块](pickup-info-module.md)

[订单详细信息模块](order-confirmation-module.md)

[礼品卡模块](add-giftcard.md)

[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)

[适用于 PayPal 的 Dynamics 365 Payment Connector](paypal.md)

[使用 Adyen 的强大客户身份验证](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]