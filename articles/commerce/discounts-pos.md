---
title: 在 POS 中显示折扣
description: 此主题说明 Microsoft Dynamics 365 Commerce 如何帮助销售助理了解促销和如何将其用于交叉销售和向上销售动态。
author: ShalabhjainMSFT
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: a9fd5a90d59ec329f8d4a2515e657fb822c098b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792839"
---
# <a name="show-discounts-in-pos"></a>在 POS 中显示折扣

[!include [banner](includes/banner.md)]

促销在促使客户做出购买决定时起着重要作用。 例如，节假日可能为零售商带来最高的销售额，因为整个零售市场到处都是诱人的促销和折扣。 如果商店助理了解并理解可用促销，可以轻松利用这些促销交叉销售和向上销售商品。 此主题说明 Microsoft Dynamics 365 Commerce 如何帮助销售助理了解促销和如何将其用于交叉销售和向上销售动态。

## <a name="learn-about-store-discounts"></a>了解商店折扣

Commerce 中有一项操作，名称为“查看所有折扣”。 此操作显示商店中当前正在实施的所有折扣。 可以将“查看所有折扣”操作映射到 销售点 (POS) 中的按钮，而该按钮可以添加到 **欢迎** 页或 **交易记录** 页。 下图显示打开的 **所有折扣** 页的示例。

![“所有折扣”页](./media/View_all_discounts.png "“所有折扣”页")

为了显示折扣，系统将查找与下面的一个或多个条件匹配的所有折扣：

- 折扣的价格组与商店的价格组匹配。
- 折扣的价格组映射到隶属或会员计划。
- 折扣的价格组映射到与商店关联的目录。

**所有折扣** 页仅显示基于优惠券的部分折扣，因为零售商通常会对特定客户创建成千上万的优惠券和相应折扣，而此页不应显示特定于客户的折扣。 仅当在每个优惠券页眉中开启了 **应用但不使用优惠券代码** 选项时才显示基于优惠券的折扣。 在此情况下，收银员应用优惠券时不必输入或扫描任何优惠券代码或条形码。

如果开启了 **应用但不使用优惠券** 选项，则可使用多种方案。 例如，收银员可以为了安抚客户或因为产品有瑕疵，向客户提供额外折扣。 不必向收银员分发印刷的优惠券代码或条形码。 相反，收银员可以选择 **应用优惠券** 按钮。 然后将把优惠券自动应用于交易。 如果一个优惠券页眉有多个优惠券，系统将自动选择交易记录中的第一个有效优惠券。

销售助理还可以在 **所有折扣** 页中按关键字搜索折扣。 关键字搜索在包含折扣名称和折扣描述的字段中进行。 销售助理还可以根据折扣是否需要优惠券代码来筛选折扣。

## <a name="cross-sell-and-upsell-by-using-discounts"></a>使用折扣交叉销售和向上销售

多行折扣（如数量折扣、组合购买折扣和阈值折扣）非常适合刺激客户购买更多产品以享受更大折扣。 因此，也有助于增加客户购物车的大小和提高零售商的收入。 可以在电子商务网站、社交媒体和店内标语中公布这些折扣。

但是，即使使用了所有这些宣传方式，客户也可能错过享受促销的机会。 为了方便销售助理了解哪些促销适用于选定的行，或者甚至适用于整个购物车，零售商可以将 **“查看可用折扣”** 操作的按钮添加到 **交易** 页上的按钮网格中。 这样，销售助理可以选择一个交易行，然后选择按钮以显示可用于所选行的所有折扣。 销售助理还可以选择另一个选项卡以显示适用于整个交易的折扣。 务必注意，**查看可用折扣** 不会显示已在销售行应用的折扣，因为折扣信息已显示在销售行上。 此方案的目的是仅显示尚未应用的折扣。 例外情况是基于标记为“应用但不使用优惠券代码”的优惠券应用的折扣。 这使销售助理可以轻松删除他们已应用的优惠券。

**所有折扣** 页面仅显示不与任何已应用折扣竞争的折扣。 此行为有助于确保在销售助理向客户介绍折扣，并且客户执行了所需操作（例如，客户多购买一件商品以享受 10% 的折扣）时，将该折扣应用于交易。 仅在启用了 **应用但不使用优惠券代码** 选项时，才会显示基于优惠券的折扣。

在所有折扣的优先级相同，折扣并发模式为 **复合型**，并且折扣并发模式设置为 **最优价格和复合位于优先级中，请勿跨多个优先级进行复合** 这样的简单方案中,**所有折扣** 页显示产品的所有可用折扣，因为所有折扣均为复合型，并且彼此不冲突。

下图显示的逻辑决定高级方案（如折扣并发模式为 **最佳价格** 或 **排除**，并且使用了两个或更多优先级）中显示哪些折扣。 在这些方案中，将根据折扣并发控件设置为 **最优价格和复合位于优先级中，请勿跨多个优先级进行复合** 还是 **最优价格仅位于优先级中，请始终跨多个优先级进行复合** 进一步影响显示的折扣。

下图显示当折扣并发控件设置为 **最优价格和复合位于优先级中，请勿跨多个优先级进行复合** 时使用的逻辑。

![“最优价格和复合位于优先级中，请勿跨多个优先级进行复合”的逻辑](./media/Model_1.png "“最优价格和复合位于优先级中，请勿跨多个优先级进行复合”的逻辑")。

下图显示当折扣并发控件设置为 **最优价格仅位于优先级中，请始终跨多个优先级进行复合** 时使用的逻辑。

![“最优价格仅位于优先级中，请始终跨多个优先级进行复合”的逻辑](./media/Model_2.png "“最优价格仅位于优先级中，请始终跨多个优先级进行复合”的逻辑")。


[!INCLUDE[footer-include](../includes/footer-banner.md)]