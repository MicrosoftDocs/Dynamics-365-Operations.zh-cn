---
title: 提货信息模块
description: 此主题介绍提货信息模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的结帐页面。
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 063701d5cd5714febeb32907346d9f6e5c2a2ca1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804397"
---
# <a name="pickup-information-module"></a>提货信息模块

[!include [banner](includes/banner.md)]

此主题介绍提货信息模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的结帐页面。

提货信息模块可以在结帐模块中用来显示订单提货信息。 客户可以查看可用的提货日期和时隙，然后选择合适的时间提货。 例如，客户可以选择在 3 月 21 日下午 3 点从旧金山商店提货。

相应商店的提货时隙必须已在 Commerce headquarters 中配置。 有关详细信息，请参阅[创建和更新客户提货时隙](dev-itpro/pickup-timeslots.md)。

如果在结帐页面上创建了提货信息模块，但未为选择提货的商店定义时隙，模块会显示信息，但用户无法选择任何时隙。 时隙是可选的，不是下订单的必需条件。

如果跨多个商店选择了多个要提货的物料，提货信息模块将让用户为每个商店选择一个时隙，前提是时隙可供使用。

> [!NOTE]
> Dynamics 365 Commerce 版本 10.0.15 和更高版本中提供对时隙和结帐提货信息模块的支持。

下图显示了通过结帐页面上的提货信息模块选择时隙的示例。

![结帐页上的提货信息模块的示例](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>模块属性

- **标题** – 输入模块的标题。

## <a name="show-time-slot-information-after-an-order-is-placed"></a>下订单后显示时隙信息

下订单后，可以在[订单确认模块](order-confirmation-module.md)和[订单详细信息模块](account-management.md#order-details-page)查看有关所选时隙的信息。 这两个模块都有 **显示时隙信息** 属性。 必须先将此属性设置为 **True**，模块才能在订购过程中显示所选的时隙。

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>将结帐提货信息模块添加到页面

有关如何将提货信息模块添加到结帐页面以及设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。

下图显示了包括提货行项时隙的电子商务结帐页面的示例。

![包括提货行项时隙的电子商务结帐页面的示例](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>其他资源

[创建和更新客户提货时隙](dev-itpro/pickup-timeslots.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[订单详细信息模块](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]