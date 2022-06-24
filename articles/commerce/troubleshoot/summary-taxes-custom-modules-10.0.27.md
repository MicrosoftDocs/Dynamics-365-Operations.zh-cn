---
title: 使用自定义订单摘要模块时，订单摘要小计不包括费用中的税费
description: 本文提供了故障排除指南，在您使用自定义的订单汇总模块，并且订单汇总小计在“价格包括销售税”方案中不包括费用税时，此指导可提供帮助。
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848829"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>使用自定义订单摘要模块时，订单摘要小计不包括费用中的税费

本文提供了故障排除指南，在您使用自定义的订单汇总模块，并且订单汇总小计在“价格包括销售税”方案中不包括费用税时，此指导可提供帮助。

## <a name="description"></a>Description

从 Microsoft Dynamics 365 Commerce 版本 10.0.27 开始，已对“价格包括销售税”方案进行了以下更改，以在订单汇总模块中跨电子商务站点页面提供一致的体验。

- 已添加以下两个新字段：**TaxOnShippingCharge** 和 **TaxOnNonShippingCharges**。
- 在“价格包括销售税”方案中，**GetSalesOrderBySalesId** 和 **GetSalesOrderByTransactionId** 应用编程接口 (API) 具有以下字段的准确值：

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

但是，如果您使用的是自定义的订单汇总模块，则这些更改可能会影响订单汇总小计值，因为未包括费用税。

## <a name="resolution"></a>解决方法

如果您使用的是自定义的订单汇总模块，并且不想继承对 Commerce 版本 10.0.27 及更高版本中的“价格包括销售税”方案所做的更改，请按照此部分中的说明进行操作。

通过恢复为 **salesTransaction.SubtotalAmount** 和 **salesTransaction.SubtotalAmountWithoutTax** 字段的先前（版本 10.0.27 之前）订单汇总行为，您可以恢复为在小计金额（**SubtotalAmount** 和 **SubtotalAmountWithoutTax**）中包含总费用税额（**TaxOnShippingCharge** 和 **TaxOnNonShippingCharges**）。

若要恢复为以前的订单汇总行为，请按照以下步骤进行操作。

1. 在 Commerce headquarters 中，打开 Commerce 参数页面（**Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**）。
1. 在左侧导航窗格中，选择 **配置参数**。
1. 添加以下配置参数，并将每个参数的值设置为 **true**：

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> 如果您以前使用过 **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** 配置参数，并且要对 **order.NetAmountWithoutTax** 属性保留相同的行为，那么您还应添加 **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** 配置参数，并将其值设置为 **true**。

## <a name="additional-resources"></a>其他资源

[隐藏订单摘要中的税务细分信息](../hide-taxes-breakup.md)
