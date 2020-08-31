---
title: 礼品卡模块
description: 此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661234"
---
# <a name="gift-card-module"></a>礼品卡模块

[!include [banner](includes/banner.md)]

此主题介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

礼品卡是一种常见付款方式，可在结帐模块中使用礼品卡模块接受礼品卡。 礼品卡模块支持 Dynamics 365、SVS 和 Givex 礼品卡。 SVS 和 Givex 礼品卡通过 Adyen 支付方兑换。

有关支持外部礼品卡（如 SVS 和 Givex）的详细信息，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)

下图显示了结帐页上的礼品卡模块的示例。

![礼品卡模块示例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>模块属性

- **显示其他字段** - 此属性定义除了礼品卡编号（默认始终显示），还应该显示礼品卡的哪些字段。 例如，某些礼品卡支持显示个人标识号 (PIN)，其他则支持显示 PIN 和到期日期。 错误，还可以将此属性设置为“无”，这将仅显示礼品卡编号，不显示其他字段。

支持的值：
-   PIN
-   到期日期
-   PIN 和到期日期 
-   None

## <a name="site-settings-for-gift-card-modules"></a>礼品卡模块的站点设置

在 Commerce 站点构建器中**站点设置 \> 扩展**下，有一个礼品卡模块设置，名称为**支持的礼品卡类型**。 此设置支持三个值：
- **Dynamics 365 礼品卡** - 如果应用此设置，则礼品卡模块仅允许兑换 Dynamics 365 礼品卡。 此设置仅支持 e-Commerce 站点中的已登录用户。
- **SVS 和 Givex 礼品卡** - 如果应用此设置，则礼品卡模块仅允许兑换 SVS 和 Givex 礼品卡。 此设置支持 e-Commerce 站点中的已登录用户和匿名用户。
- **Dynamics 365、SVS 和 Givex 礼品卡** - 如果应用此设置，则礼品卡模块允许兑换 Dynamics 365、SVS 和 Givex 礼品卡。 此设置仅支持 e-Commerce 站点中的已登录用户。

## <a name="add-a-gift-card-module-to-a-page"></a>向页面添加礼品卡模块

有关如何向结帐页添加礼品卡模块和设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结帐模块](add-checkout-module.md)

[付款模块](payment-module.md)

[装运地址模块](ship-address-module.md)

[交货选项模块](delivery-options-module.md)

[订单详细信息模块](order-confirmation-module.md)

[对外部礼品卡的支持](./dev-itpro/gift-card.md)
