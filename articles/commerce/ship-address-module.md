---
title: 收货地址模块
description: 本文介绍装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 48e6909b4dac9722830a83ec3a63a58876768d7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274997"
---
# <a name="shipping-address-module"></a>收货地址模块

[!include [banner](includes/banner.md)]

本文描述装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

装运地址模块使客户可以在结帐流中添加或选择订单的装运地址。 如果客户已登录，则显示以前为该客户保存的所有地址，然后客户可以在其中进行选择。 客户也可以添加新地址。 装运地址模块用于订单中需要装运的所有项。

装运地址格式可以在 Commerce headquarters 中为每个国家或地区定义，然后装运地址模块强制执行特定于国家/地区的规则。

当客户在结帐流中输入装运地址时，他们可以选择将地址保存为主要地址。 仅当客户登录后才显示此选项。

虽然装运地址模块不提供地址验证，但是可以通过自定义设置来实现此功能。

下图显示了结帐页上的新装运地址模块的示例。

![结帐页面上的装运地址模块的示例。](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题 | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 装运地址模块的可选标题。 |
| 显示地址类型 | **True** 或 **False** | 如果将此可选属性设置为 **True**，地址类型（如 **住宅** 或 **企业**）将显示。 如果未指定地址类型，地址将自动保存为 **类型**=**其他**。 |
| 启用自动建议| **True** 或 **False** | 如果将此可选属性设置为 **真**，系统会提供自动地址建议。 这些建议由必应地图提供支持。 有关如何为您的站点设置必应地图集成的信息，请参阅[商店选择器模块](store-selector.md)。 从 Commerce 版本 10.0.15 起提供此功能。|
|自动建议选项| 数字| 如果启用了自动地址建议，则可以指定其他选项，例如应提供的最大建议数量。|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>向结帐页添加装运地址模块和设置必需的属性

装运地址模块只能添加到结帐模块。 有关如何配置装运地址模块并将其添加到结帐页的详细信息，请参阅[结帐模块](add-checkout-module.md)。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结帐模块](add-checkout-module.md)

[付款模块](payment-module.md)

[交付选项模块](delivery-options-module.md)

[提货信息模块](pickup-info-module.md)

[订单详细信息模块](order-confirmation-module.md)

[礼品卡模块](add-giftcard.md)

[商店选择器模块](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
