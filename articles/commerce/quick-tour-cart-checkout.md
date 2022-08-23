---
title: 购物车和结帐页面概览
description: 本文概述 Microsoft Dynamics 365 Commerce 中的购物车和结帐页。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: c2fad50b58db8213ecc246376e28b2ae43f77a08
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286430"
---
# <a name="cart-and-checkout-pages-overview"></a>购物车和结帐页面概览

[!include [banner](includes/banner.md)]

本文概述 Microsoft Dynamics 365 Commerce 中的购物车和结帐页。

电子商务网站的购物车页显示客户已添加到购物车的所有商品。 购物车页是使用购物车模块生成的。 购物车模块是承载展示购物车中的商品所需全部模块的容器。 购物车模块也可以使用其他模块显示订单汇总和已经为客户订单应用的任何促销代码。

电子商务网站的结帐页提供分步流，供客户输入下订单所需全部信息。 结帐模块中可以包含用于处理装运地址、装运方式、记帐信息、订单摘要和与客户订单有关的其他信息的模块。

## <a name="cart-page"></a>购物车页

购物车页充当购物袋，其中包含已添加到购物车的所有商品。

下图显示使用模块库和“Fabrikam”主题生成的购物车页的示例。

![购物车页面的示例。](./media/cart2.PNG)

购物车页的主体显示客户已添加到购物车的所有商品。 将显示所有适用的折扣。 这些折扣包括复合折扣。 例如，“买 3 件打九折”或“买一瓶和一个背包打九折”。 订单汇总模块显示应用折扣、运费、税等后的应付金额。 还有一个促销代码模块，供客户应用或删除促销代码。

客户可匿名或作为已登录用户购物。 如果客户已登录，则购物车中的商品将保留到下个会话。 因此，客户可以从多个设备继续购物。

客户可从购物车继续结帐。 客户可以以访客用户或已登录用户的身份开始结帐。

有关如何制作购物车页的信息，请参阅[向页面添加购物车模块](add-cart-module.md)。

## <a name="checkout-page"></a>结帐页

结帐页是客户输入下订单所需信息时所在位置。

下图显示使用模块库生成的结帐页的示例。

![结帐页面的示例。](./media/Checkout.PNG)

结帐页的主题是收集所有订单信息的位置。 此信息包括装运地址、交货选项和付款信息。 结帐采用分步流程，因为必须按照特定顺序输入要处理的信息。 例如，必须先输入装运地址，才能计算装运成本和为付款授权。

### <a name="shipping-address"></a>装运地址

如果必须装运商品，则需要装运地址。 可以在 Dynamics 365 Commerce 中为每个区域设置配置装运地址格式。 例如，如果要将商品运到美国，则装运地址必须包含街道地址、州和邮政编码。 将为装运地址字段执行一些基本输入验证，如验证字母数字字符、最大长度和数字。 虽然不验证地址是否有效，但可以使用自定义的第三方服务进行此项验证。

装运地址应用于购物车中所有选择了“装运”选项的商品。 如果使用模块库中提供的结帐流程，则不能将单件购物车商品装运到不同地址。 如果需要此功能，可以通过自定义结帐模块来实施。

提供装运地址之后，将显示 Dynamics 365 Commerce 在线商店中的可用装运方式。 可以在 Commerce 中配置装运方式及其支持的地址。

### <a name="payment"></a>付款

结帐流程中的下一步是付款。 在电子商务中，可使用多种付款方式下订单，如信用卡、礼品卡和积分。 也可以使用这些付款方式的组合。 可能需要更多信息，具体取决于所用付款方式。 例如，信用卡付款需要结算地址。 信用卡付款通过使用 Adyen 付款连接器处理。

#### <a name="loyalty-points"></a>会员积分

结帐流程中，会员计划成员客户和积攒了积分的客户可以兑换这些积分来支付订单。 仅当客户当前拥有会员资格时，才会显示积分模块。 此模块对非会员和访客用户隐藏。

#### <a name="gift-cards"></a>礼品卡

模块库支持为订单兑换内部礼品卡。 客户必须先登录，才能应用内部礼品卡。 为了提高安全，我们建议您为内部礼品卡使用个人标识号 (PIN) 来自定义流程。

### <a name="signed-in-and-guest-users"></a>已登录用户和访客用户

客户可以以访客用户或已登录用户的身份完成结帐流程。 如果客户登录，将自动检索帐户信息，如保存的装运地址和保存的信用卡详细信息。

### <a name="order-summary"></a>订单汇总

结帐显示购物车中的明细商品的汇总，所以客户可以在下订单前验证订单。 结帐流程中不能编辑明细商品。 但是，提供了购物车链接，以防用户回去编辑明细商品。

客户提供装运和记帐信息之后，订单汇总体现应用积分、礼品卡和其他付款后的应付金额。

### <a name="order-confirmation-and-email"></a>订单确认和电子邮件

客户下订单时，将提供确认编号。 此时，付款已获得授权，但未扣费。 仅当订单已履行（即已装运或已提货），才会对付款扣费。

创建订单之后，将向客户发送订单确认电子邮件。

有关如何制作结帐页的详细信息，请参阅[向页面添加结帐模块](add-checkout-module.md)。

## <a name="additional-resources"></a>其他资源

[主页概览](quick-tour-home-page.md)

[产品详细信息页面概览](quick-tour-pdp.md)

[帐户管理页面概览](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
