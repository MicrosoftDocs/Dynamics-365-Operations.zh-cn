---
title: 为在线订单配置销售税
description: 此主题概述了 Dynamics 365 Commerce 中不同在线订单类型的销售税组选择。
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5801bbfb5b5850cb4c9ae06140bff5adca9b368febdc06d69c538fc49f9ee40a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772953"
---
# <a name="configure-sales-tax-for-online-orders"></a>为在线订单配置销售税

[!include [banner](includes/banner.md)]

本主题提供使用基于目的地或基于客户帐户的税务设置为不同的在线订单类型选择销售税组的概述。 

您可能希望您的电子商务渠道支持在线订单交货或提货等选项。 销售税适用性基于您的在线客户选择的选项。 

## <a name="destination-based-taxes-for-online-orders"></a>在线订单的基于目的地的税务

通常，装运到客户地址的在线订单的税金由目的地定义。 每个销售税组都有一个基于零售目的地的税务配置，在此配置中，您的企业可以通过分层形式定义目的地详细信息，例如国家/地区、省/自治区/直辖市、县和城市。

### <a name="orders-delivered-to-customer-address"></a>交货到客户地址的订单

下达在线订单后，Commerce 税务引擎使用订单中每个明细项的交货地址，按照匹配的基于目的地的税务条件查找销售税组。 例如，对于行项交货地址是到加利福尼亚州旧金山的在线订单，税引擎将查找加利福尼亚的销售税组和销售税代码，然后相应地计算每个行项的税金。

### <a name="order-pick-up-in-store"></a>订单在店内提货

对于指定了店内提货或懒人提货的订单行，将应用所选提货商店的税组。 有关如何为给定商店设置销售税的详细信息，请参阅[为商店设置其他税务选项](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)。

## <a name="customer-account-based-taxes-for-online-orders"></a>在线订单的基于客户帐户的税务

在某些业务场景中，您想要在 Commerce Headquarters 中在特定的客户帐户上配置销售税组。 总部中有两个位置可供您在客户帐户上配置销售税。 若要访问这些位置，您首先需要通过转到 **Retail 和 Commerce \> 客户 \> 所有客户**，然后选择一个客户来转到客户详细信息页面。

可供您为客户帐户配置销售税的两个位置包括：

- 客户详细信息页面的 **发票和交货** 快速选项卡上的 **销售税组**。 
- **管理地址** 页面的 **常规** 快速选项卡上的 **销售税**。 若要从客户详细信息页面中访问，请在 **地址** 快速选项卡下选择特定地址，然后选择 **高级**。

> [!TIP]
> 对于在线客户订单，如果您只想应用基于目的地的税务，而不应用基于客户帐户的税务，请确保客户详细信息页面的 **发票和交货** 快速选项卡上的 **销售税组** 字段为空。 若要确保使用在线渠道注册的新客户不会从默认客户或客户组设置中继承销售税组设置，请确保 **销售税组** 字段对于在线渠道默认客户设置和客户组设置也为空（**Retail 和 Commerce \> 客户 \> 客户组**）。

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>确定基于目的地的税务或基于客户帐户的税务适用性 

下表说明了对在线订单应用基于目的地的税务还是基于客户帐户的税务。 

| 客户类型 | 装运地址                   | 客户 > 发票和交货 > 销售税组？ | 总部中客户帐户上的地址？ | 客户地址 > 高级 > 常规 > 销售税组？                                              | 已应用销售税组      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| 来宾         | 纽约曼哈顿                      | 否（空白）                                                | 否（空白）                              | 否（空白）                                                                                                   | 纽约（基于目的地的税务） |
| 已登录     | 德克萨斯州奥斯汀                          | 否（空白）                                             | 是                               | 否<br/><br/>通过在线渠道添加的新地址。                                                            | 德克萨斯州（基于目的地的税务） |
| 已登录     | 加利福尼亚州旧金山（在商店提货） | 是（纽约）                                            | 不适用                              | 不适用                                                                                                    | 加利福尼亚州（基于目的地的税务） |
| 已登录     | 德克萨斯州休斯敦                         | 是（纽约）                                            | 是                               | 是（纽约）<br/><br/>通过在线渠道添加的新地址和从客户帐户继承的销售税组。 | 纽约（基于客户帐户的税务）  |
| 已登录     | 德克萨斯州奥斯汀                          | 是（纽约）                                            | 是                               | 是（纽约）<br/><br/>通过在线渠道添加的新地址和从客户帐户继承的销售税组。 | 纽约（基于客户帐户的税务）  |
| 已登录     | 佛罗里达州萨拉索塔                       | 是（纽约）                                            | 是                               | 是（华盛顿州）<br/><br/>手动设置为华盛顿州。                                                                          | 华盛顿州（基于客户帐户的税务）  |
| 已登录     | 佛罗里达州萨拉索塔                       | 否（空白）                                                | 是                               | 是（华盛顿州）<br/><br/>手动设置为华盛顿州。                                                                          | 华盛顿州（基于客户帐户的税务）  |

## <a name="additional-resources"></a>其他资源

[基于目的地为在线商店设置税务](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[销售税概览](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[“源”字段中的销售税计算方法](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[ 销售税分配和覆盖](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[全部金额和销售税代码的间隔计算选项](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[免税的计算](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]