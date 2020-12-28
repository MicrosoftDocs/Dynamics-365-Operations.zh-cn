---
title: 装运地址模块
description: 此主题介绍装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
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
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410647"
---
# <a name="shipping-address-module"></a>装运地址模块

[!include [banner](includes/banner.md)]

此主题介绍装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

## <a name="overview"></a>概览

装运地址模块使客户可以在结帐流中添加或选择订单的装运地址。 如果客户已登录，则显示以前为该客户保存的所有地址，然后客户可以在其中进行选择。 客户也可以添加新地址。 装运地址模块用于订单中需要装运的所有项。

装运地址格式可以在 Commerce headquarters 中为每个国家或地区定义，然后装运地址模块强制执行特定于国家/地区的规则。

当客户在结帐流中输入装运地址时，他们可以选择将地址保存为主要地址。 仅当客户登录后才显示此选项。

虽然装运地址模块不提供地址验证，但是可以通过自定义设置来实现此功能。

下图显示了结帐页上的新装运地址模块的示例。

![结帐页上的装运地址模块的示例](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题 | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 装运地址模块的可选标题。 |
| 显示地址类型 | **True** 或 **False** | 如果将此可选属性设置为 **True**，地址类型（如 **住宅** 或 **企业**）将显示。 如果未指定地址类型，地址将自动保存为 **类型**=**其他**。 |

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
