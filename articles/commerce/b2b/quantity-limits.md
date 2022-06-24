---
title: 设置 B2B 电子商务站点的产品数量限制
description: 本文介绍如何为企业到企业 (B2B) 电子商务站点设置产品数量限制。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 034441f8f712c676dbcc89f0009361d0a4a65721
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876997"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>设置 B2B 电子商务站点的产品数量限制

[!include [banner](../../includes/banner.md)]

本文介绍如何为企业到企业 (B2B) 电子商务站点设置产品数量限制。

大多数产品都有一个定义其分组的度量单位。 分组将影响产品的销售方式。 有些产品可能还有额外的数量分组。 此分组确定产品是单个还是多个出售，以及是否有必须遵循的最小或最大订购数量限制。

数量限制功能可确保将 Microsoft Dynamics 365 Commerce 中配置的最小、最大、多个和标准数量（在默认订单设置或 Commerce 站点构建器站点设置中）应用于在电子商务站点上下的客户订单。 销售点 (POS) 和呼叫中心当前不支持产品数量限制。

很多零售商提供客户订单（也称特殊订单）选项，以满足各种产品和履行要求。 下面是一些典型方案：

- 客户希望特定变型的产品能够以几个的倍数销售。
- 客户希望从非购买产品的商店或位置取货。 但是，商店的包装标准不同于在线销售分配的包装标准。
- 客户想要购买限量版产品，该产品对可购买件数有最大数量限制。

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>在 Commerce headquarters 中打开默认订单设置功能

您必须先在 Commerce headquarters 中启用默认订单设置功能，然后才能够设置产品数量限制。

要打开默认订单设置功能，请按照下列步骤操作。

1. 转到 **系统管理 \> 工作区 \> 功能管理**。
1. 找到并选择 **在客户订单中支持站点和默认订单设置** 功能。
1. 在右窗格的底部，选择 **立即启用**。 

## <a name="define-quantity-settings"></a>定义数量设置 

您可以在 **默认订单设置** 页面上定义数量设置。

要定义数量设置，请执行以下步骤。 

1. 转到产品 **Retail 和 Commerce \> 产品和类别 \> 按类别发布的产品**。
1. 选择一个已发布产品。
1. 在操作窗格上，在 **管理库存** 选项卡上的 **订单设置** 组中，选择 **默认订单设置**。 
1. 在 **默认订单设置** 页上的 **销售订单** 快速选项卡上，在 **销售数量** 部分，设置产品销售数量：

    - **倍数** – 产品可以其倍数购买的数量。
    - **最小订单数量** – 必须购买的最少产品数量。
    - **最大订单数量** – 可以购买的最多产品数量。
    - **标准订单数量** – 选择产品时自动输入的默认数量。

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>在 Commerce 站点构建器中打开 B2B 订单数量限制功能

要在 Commerce 站点构建器中打开 B2B 订单数量限制功能，请按照以下步骤操作。

1. 转到 **站点设置 \> 扩展**
1. 在 **启用订单数量限制** 下，在下拉菜单中选择 **为 B2B 客户启用**。 

> [!NOTE] 
> 更新的站点构建器设置仅在更新 app.settings.json 文件后才会生效。 有关详细信息，请参阅 [SDK 和模块库更新](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

## <a name="additional-resources"></a>其他资源

[建立 B2B 电子商务站点](set-up-b2b-site.md)

[使用客户层次结构管理 B2B 业务合作伙伴](partners-customer-hierarchies.md)

[在 B2B 电子商务站点上管理业务合作伙伴用户](manage-b2b-users.md)

[配置 B2B 电子商务站点的客户帐户付款方式](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
