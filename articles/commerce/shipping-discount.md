---
title: 装运折扣
description: 本文介绍了 Microsoft Dynamics 365 Commerce 中的装运折扣功能以及使用这些功能所需的设置。
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346377"
---
# <a name="shipping-discount"></a>装运折扣

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍了 Microsoft Dynamics 365 Commerce 中的装运折扣功能以及使用这些功能所需的设置。

免费或折扣装运是影响客户在线购买决定的一个因素。 为了增加每笔交易的收入，很多零售商使用免费装运福利来激励客户增大购物车容量。

Commerce 支持装运折扣功能，当交易中合格商品的总销售额满足特定条件时，零售商可以为特定送货方式配置装运费用的折扣百分比。 使用装运折扣功能的示例场景如“花费 $50 或以上即可享受免费隔夜送货”。

## <a name="prerequisites"></a>先决条件

Commerce 的[全渠道高级自动收费](/dynamics365/unified-operations/retail/omni-auto-charges)功能支持装运折扣功能。 要使装运折扣功能正常工作，您必须在 Commerce headquarters 中在 **Commerce 参数** 页面的 **客户订单** 选项卡上启用 **使用高级自动费用** 配置。 零售商可以使用高级自动费用功能来设置各种类型的费用，如处理、安装和处置。

装运折扣仅应用于装运费用。 因此，零售商必须指定哪些费用是装运费用。 要指定装运费用，在 Commerce headquarters 中，转到 **渠道设置 \> 费用 \> 费用代码**，将所需费用的 **装运费用** 选项设置为 **是**。

![将费用指定为装运费用。](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>配置

装运折扣功能基于层级，仅支持 **折扣比率** 计算类型。 要设置装运折扣，在 Commerce headquarters 中，转到 **定价和折扣 \> 装运阈值折扣**。 然后，您可以指定折扣应用的交货方式，定义一个或多个金额阈值，并为每个阈值设置折扣百分比。 您还可以将类别或产品列表配置为合格项目。 这样，当定价引擎评估交易总额是否达到阈值时，只会计算交易中这些项目的销售额。

> [!NOTE]
> 与其他折扣类型不同，装运折扣不会创建折扣行。 而是直接编辑装运费用，并将折扣名称追加到费用描述中。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
