---
title: 隐藏订单摘要中的税务细分信息
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中的购物车、结帐、订单确认和订单详细信息页面的订单摘要中隐藏税务分解信息。
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: fe1f6c5875444f4f91ee1dfb01b3fdaa527c52e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881782"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>隐藏订单摘要中的税务细分信息

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中的购物车、结帐、订单确认和订单详细信息页面的订单摘要中隐藏税务分解信息。

默认情况下，Dynamics 365 Commerce 会在购物车、结帐、订单确认和订单详细信息页面的订单摘要中显示税务分解信息。 从 Commerce 版本 10.0.27 开始，Commerce 站点生成器包含一个选项，可让您在订单摘要中隐藏税务分解信息。

下图显示了两个订单摘要的示例。 第一个显示税务分解信息，第二个显示该信息。

![显示和隐藏税务分解信息的购物车的示例。](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - 仅当在 Commerce Headquarters 的 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店** 中将电子商务渠道的 **价格包括销售税** 选项设置为 **是** 时，才可以使用在订单摘要中隐藏税务分解信息的选项。 
> - 默认情况下，在站点生成器中启用了 **在订单摘要中显示税务分解信息** 选项。

## <a name="hide-tax-breakup-information-in-order-summaries"></a>在订单摘要中隐藏税务分解信息

要在订单摘要中隐藏税务分解信息，请执行以下步骤。

1. 在 Commerce 站点生成器中，转到要更新的站点。
1. 转到 **站点设置 \> 扩展**。
1. 清除 **在订单摘要中显示税务分解信息** 复选框。

若要在订单摘要中显示税务分解信息，请选中 **在订单摘要中显示税务分解信息** 复选框。  

下图显示了站点生成器中突出显示并选中的 **在订单摘要中显示税务分解信息** 复选框。

![站点生成器中的“在订单摘要中显示税务分解信息”选项。](media/prices-include-sales-tax-e-Commerce-site-settings.png)

> [!NOTE]
> 如果您有自定义的订单汇总模块，并且不想继承 Commerce 版本 10.0.27 或更高版本中的“在订单摘要中隐藏税务分解信息”功能，请参阅[使用自定义的订单汇总模块时，订单汇总小计不包括费用税](troubleshoot/summary-taxes-custom-modules-10.0.27.md#resolution)。

## <a name="additional-resources"></a>其他资源

[销售税概览](/finance/general-ledger/indirect-taxes-overview)

[配置在线订单的销售税](sales-tax-config.md)

[疑难解答：在线订单的税金计算错误](troubleshoot/tax-miscalculated-online-order.md)
