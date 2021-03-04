---
title: 为在线订单配置销售税
description: 此主题概述了 Dynamics 365 Commerce 中不同在线订单类型的销售税组选择。
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530189"
---
# <a name="configure-sales-tax-for-online-orders"></a>为在线订单配置销售税

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

此主题概述了不同在线订单类型的销售税组选择。 

您的电子商务渠道可能希望支持在线订单交货或提货等选项。 销售税的适用性基于您的在线用户选择的选项。 当站点客户选择在线购买商品并将其装运到某个地址时，销售税根据客户的装运地址税组设置确定。 当客户选择在商店提取购买的商品时，销售税根据提货商店的税组设置确定。 

## <a name="orders-shipped-to-a-customer-address"></a>装运到客户地址的订单 

通常，装运到客户地址的在线订单的税金由目的地定义。 每个销售税组有一个基于零售目的地的税金配置，在此配置中，您的企业可以通过分层形式定义目的地详细信息，如国家/地区、省/自治区/直辖市、县和城市。 下达在线订单后，Commerce 税引擎使用订单中每个行项的交货地址，按照匹配的基于目的地的税收标准查找销售税组。 例如，对于行项交货地址是到加利福尼亚州旧金山的在线订单，税引擎将查找加利福尼亚的销售税组和销售税代码，然后相应地计算每个行项的税金。  

## <a name="customer-based-tax-groups"></a>基于客户的税组

在 Commerce headquarters 中，有两个地方可以配置客户税组：

- **客户配置文件**
- **客户装运地址**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>如果客户配置文件配置了税组

Headquarters 中的客户配置文件记录可能已经配置了销售税组，但是，对于在线订单，在客户配置文件中配置的销售税组不会被税引擎使用。 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>如果客户装运地址配置了税组

如果客户的装运地址记录配置了税组，当在线订单（或行项）装运到客户的装运地址时，客户地址记录中配置的税组会被税引擎用来计算税金。

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>为客户的装运地址记录配置税组

要在 Commerce headquarters 中为客户的装运地址记录配置税组，请按照下列步骤操作。

1. 转到 **所有顾客**，然后选择所需的客户。 
1. 在 **地址** 快速选项卡上，选择所需的地址，然后选择 **更多选项 \> 高级**。 
1. 在 **管理地址** 页上的 **常规** 选项卡下，根据需要设置销售税值。

> [!NOTE]
> 税组使用订单行的交货地址定义，基于目的地的税金在税组中配置。 有关详细信息，请参阅[设置基于目的地的在线商店税金](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)。

## <a name="order-pickup-in-store"></a>订单在店内提货

对于指定了店内提货或路边提货的订单行，将应用所选提货商店的税组。 有关如何为给定商店配置税组的详细信息，请参阅[设置商店的其他税金选项](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)。

> [!NOTE]
> 当订单行是在商店提货时，客户地址的税金设置（如果已设置）将被税引擎忽略，将应用提货商店的税金配置。 

## <a name="additional-resources"></a>其他资源

[销售税概览](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[“源”字段中的销售税计算方法](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ 销售税分配和覆盖](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[全部金额和销售税代码的间隔计算选项](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[免税的计算](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]