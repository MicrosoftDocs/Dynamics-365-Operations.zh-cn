---
title: 交货选项模块
description: 此主题介绍交货选项模块，说明如何在 Microsoft Dynamics 365 Commerce 中配置该模块。
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
ms.openlocfilehash: f9e8df576efd1e58fde235828823f31e87ed58bf
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410652"
---
# <a name="delivery-options-module"></a>交货选项模块

[!include [banner](includes/banner.md)]

此主题介绍交货选项模块，说明如何在 Microsoft Dynamics 365 Commerce 中配置该模块。

## <a name="overview"></a>概览

交货选项模块使客户可以为在线订单选择交货方式，如装运或提货。 需要装运地址来确定交货方式。 如果更改装运地址，则必须重新检索交货选项。 如果订单中仅包含将在商店提货的项，则自动隐藏此模块。

有关如何配置交货方式的信息，请参阅[在线渠道设置](channel-setup-online.md)和[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。

每种交货方式都可能收取相关费用。 有关如何为在线商店配置费用的详细信息，请参阅[全渠道高级自动收费](omni-auto-charges.md)。

在 Commerce 版本 10.0.13 中，交货选项模块已更新，可以支持 **不按比例分配的标题费用** 和 **作为行费用装运** 功能。 如果关闭了按比例分配，预期电子商务工作流将不允许为购物车中的商品提供混合交货方式（即某些商品被选出进行装运，其他商品则被选为采用提货方式）。 **不按比例分配的标题费用** 功能需要在 Commerce headquarters 中打开 **支持在渠道中进行一致的交货方式处理** 标记。 打开该标记后，装运费用将在标题级别或行级别应用，具体取决于 Commerce headquarters 中的配置。

Fabrikam 主题支持混合交货方式，有些商品被选出进行装运，其他商品则被选为采用提货方式。 在此模式下，将为选出采用装运交货方式的所有商品按比例分配装运费用。 要能使用混合交货方式，必须首先在 Commerce headquarters 中配置 **按比例分配的标题费用** 功能。 有关此配置的详细信息，请参阅[按比例分配标题费用以匹配销售行](pro-rate-charges-matching-lines.md)。

如果在行项应用装运费用，可以在每一项的购物车行上显示这些费用。 此功能需要同时为购物车模块和结帐模块打开 **在行项上显示装运费用** 属性。 有关详细信息，请参阅[购物车模块](add-cart-module.md)和[结帐模块](add-checkout-module.md)。

下图显示了结帐页上的交货选项模块的示例。

![结帐页上的交货选项模块的示例](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>交货选项模块属性

| 属性 | 值 | 说明 |
|----------|--------|-------------|
| 标题 | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 交货选项模块的可选标题。 |
| 自定义 CSS 类名称 | 文本 | 将用于呈现此模块的自定义级联样式表 (CSS) 类名称（如果适用）。 |
| 筛选交货模式选项 | **不筛选** 或 **非装运方式** | 指定交货选项模块是否应筛选掉所有非装运交货方式的值。 |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>向结帐页添加交货选项模块和设置必需的属性

交货选项模块只能添加到结帐模块。 有关如何配置交货选项模块并将其添加到结帐页的详细信息，请参阅[结帐模块](add-checkout-module.md)。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[付款模块](payment-module.md)

[收货地址模块](ship-address-module.md)

[提货信息模块](pickup-info-module.md)

[订单详细信息模块](order-confirmation-module.md)

[礼品卡模块](add-giftcard.md)

[在线渠道设置](channel-setup-online.md)

[全渠道高级自动费用](omni-auto-charges.md)

[按比例分配标题费用以匹配销售行](pro-rate-charges-matching-lines.md)

[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]