---
title: “提货”选项没有出现在购物车或产品详细信息页面上
description: 本文提供了故障排除指南，可以在购物车页面或产品详细信息页面上未显示店内提货选项时提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 85d102d3442e19377912cb9562010778a0575db8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284595"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>“提货”选项没有出现在购物车或产品详细信息页面上

[!include [banner](../../includes/banner.md)]

本文提供了故障排除指南，可以在购物车页面或产品详细信息页面上未显示店内提货选项时提供帮助。

## <a name="description"></a>说明

**提货** 选项没有出现在购物车页面或产品详细信息页面上。

下图显示了一个包括 **提货** 按钮的页面示例。

![“提货”按钮。](media/pickup-button-missing.jpg)

## <a name="resolution"></a>解决方法

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>在 Commerce 站点构建器中启用 BOPIS 扩展

要在 Commerce 站点构建器中启用“线上购买，店内提货”(BOPIS) 扩展，请按照下列步骤操作。

1. 选择您的站点。
1. 选择 **站点设置**，然后选择 **扩展**。
1. 确保已清除 **禁用 BOPIS** 选项。

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>在 Commerce Headquarters 中配置交付方式

要在 Commerce Headquarters 中配置交付方式，请按照下列步骤操作。

1. 转到 **采购 \> 设置 \> 交付方式**。
1. 确保已创建 **客户提货** 交付方式，并为其分配了产品和地址。
1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数**。
1. 在左侧导航栏中，选择 **客户订单**。
1. 确保已正确配置 **提货交货方式**。

### <a name="configure-customer-orders-payments"></a>配置客户订单付款

要在 Commerce Headquarters 中配置客户订单付款，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数**。
1. 在左侧导航栏中，选择 **客户订单**。
1. 在 **付款** 快速选项卡上，请确保 **付款条款** 和 **付款方式** 字段设置正确。

## <a name="additional-resources"></a>其他资源

[配置 BOPIS](../cpe-bopis.md)

[为客户订单启用多种提货交货方式](../multiple-pickup-modes.md)

[全渠道 Commerce 订单付款](../dev-itpro/commerce-payments.md)

[商店选择器模块](../store-selector.md)
