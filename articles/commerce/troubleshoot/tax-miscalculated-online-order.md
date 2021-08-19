---
title: 在线订单的税金计算错误
description: 本主题提供了故障排除指南，当在线订单上的税金计算错误或未正确设置销售行上的税组时，此指南可以提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e51ae789dad2c7b5118be2cf8a88f4e4090a8c74c8259b4eaaddad1a134af80a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715252"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>在线订单的税金计算错误

[!include [banner](../../includes/banner.md)]

本主题提供了故障排除指南，当在线订单上的税金计算错误或未正确设置销售行上的税组时，此指南可以提供帮助。

## <a name="description"></a>说明

下达电子商务订单时，税额计算错误，或未正确设置销售行上的税组。

## <a name="resolution"></a>解决方法

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>在 Commerce Headquarters 中配置零售商店的销售税

要在 Commerce Headquarters 中配置零售商店的销售税，请按照下列步骤操作。

1. 转至 **Retail 和 Commerce \> 渠道 \> 所有商店**。
1. 选择要为其配置销售税的商店。
1. 在 **常规** 快速选项卡上，在 **销售税** 部分，配置商店的销售税信息。

> [!NOTE]
> 对于从商店取货，税组来自选择要取货的商店。 有关详细信息，请参阅[设置商店的其他税金选项](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)。

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>在 Commerce Headquarters 中配置客户地址的相应销售税

要在 Commerce Headquarters 中配置客户地址的相应销售税，请按照下列步骤操作。

1. 转到 **应付帐款 \> 客户 \> 所有客户**。
1. 选择要为其配置销售税的客户。
1. 在 **地址** 快速选项卡上，选择要为其配置销售税的地址，再选择 **更多选项**，然后选择 **高级**。
1. 在 **常规** 快速选项卡上，选择 **税组**。
1. 在 **销售税** 字段中，输入合适的值。

> [!NOTE]
> 对于涉及客户地址上的销售税的装运，该行的收货地址确定该行的税组。 如果客户要送货到具有已配置税组的现有地址，则将使用现有税组。 默认情况下，地址在创建时没有税组。

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>在 Commerce Headquarters 中配置一般销售税组

要在 Commerce Headquarters 中配置一般销售税组，请按照下列步骤操作。

1. 转到 **税 \> 间接税 \> 销售税 \> 销售税组**。
1. 在左侧导航栏中，选择要配置的税组。
1. 在 **基于零售目的地的税** 快速选项卡上，为销售税组配置税。

> [!NOTE]
> 对于涉及客户地址上的销售税的装运，该行的交货地址以及为税组配置的基于目的地的税将确定税组。 有关详细信息，请参阅[设置基于目的地的在线商店税金](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)。

## <a name="additional-resources"></a>其他资源

[配置在线订单的销售税](../sales-tax-config.md)