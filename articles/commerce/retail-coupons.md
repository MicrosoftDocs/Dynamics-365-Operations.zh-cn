---
title: 设置零售销售优惠券
description: 此主题提供优惠券概览并阐述如何进行设置。
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a4de42c23bf96591d1ac99ed32438fe34a485998
ms.sourcegitcommit: 05868764acd3d77970724a30c49c5ae5ffb6ca5b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906641"
---
# <a name="set-up-coupons-for-retail-sales"></a>设置零售销售优惠券

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>优惠券概览

优惠券是用于将折扣添加到交易的代码和条码。 每张优惠券可以有多个代码，且每个代码可以有自己的有效日期。

每张优惠券都关联一个折扣。 与折扣关联的价格组定义可以使用优惠券的客户或优惠券有效的渠道。

优惠券基本上是折扣顶部的附加验证。 优惠券提供必需的优惠券代码和条码，以及这些代码的日期范围。 优惠券还提供可选使用限制和客户要求的属性。 折扣提供优惠券对其有效的产品集。 折扣的价格组提供优惠券对其有效的客户、渠道或目录集。

要创建优惠券，须分开创建折扣和优惠券。 之后可以在 Commerce 中通过选择优惠券页面上的折扣将它们关联。

> [!NOTE]
> 优惠券关联到折扣后，Commerce 折扣页上的多个字段变为只读，因为其由优惠券的设置管理。 这些字段包括用于状态和标准日期范围的字段。
> 
> 在呼叫中心渠道中使用优惠券时，您需要选择 **重新计算** 按钮 **（“销售”选项卡 > 计算 > 重新计算）**，以便应用关联到优惠券的折扣。 此附加步骤将在以后的版本中删除。

### <a name="limited-use-coupons"></a>有限使用的优惠券

优惠券可以配置为有限使用的优惠券。 使用限制可以按客户或渠道进行配置，或配置为全球限制。 在 POS 中或销售订单录入期间输入或扫描代码或条码时执行此限制。

此限制按优惠券上的优惠券代码执行。 例如，具有两个优惠券代码的单次使用优惠券可以使用两次：每个优惠券代码可使用一次。 优惠券上的每个代码可以单独设置为有效。

优惠券可以跨任何销售渠道使用，但是对于呼叫中心订单，限制使用优惠券只能用于那些呼叫中心的 **订单完成** 设置已启用的呼叫中心订单。 如果未启用此设置，呼叫中心订单只能使用非限制使用类型的优惠券。

> [!NOTE]
> 优惠券达到使用限制后，系统 *不* 自动将优惠券代码的状态更改为“已用”。 但是，该优惠券代码已达到使用限制，无法使用。 如果将优惠券代码的状态手动设置为除 **活动** 之外的其他状态，则任何渠道均不可使用此优惠券代码。  

## <a name="managing-coupons"></a>管理优惠券

您必须分开创建折扣和优惠券。 之后可以通过选择优惠券页面上的折扣将它们关联。 将优惠券关联到折扣后，折扣的多个字段变为只读，因为其由优惠券的设置管理。 这些字段包括用于状态和标准日期范围的字段。

优惠券现在基本上是折扣顶部的附加验证。 优惠券提供优惠券代码和条码以及日期范围、使用限制和客户要求的属性。 折扣提供优惠券对其有效的产品集。 折扣的价格组提供优惠券对其有效的客户、渠道或目录集。

## <a name="system-setup-for-coupons"></a>优惠券系统创建

在您可以设置优惠券前，必须先设置优惠券条码和两个优惠券编号规则。

1. 在 **掩码字符** 页，为优惠券代码创建新的掩码字符。 您可以选择任何未使用的字符。
2. 在 **条码掩码设置** 页，创建一个新的条码掩码。 将 **类型** 字段设置为 **优惠券**。
3. 在 **条码设置** 页，创建使用您刚才创建的条码掩码的新条码。
4. 在 **编号规则** 页，创建两个新的编号规则。 一个规则用于优惠券代码 ID，另一个规则用于优惠券编号。 优惠券代码 ID 是优惠券各优惠券代码的唯一标识符。 优惠券编号是优惠券的唯一标识符。 每张优惠券可以有多个触发优惠券的代码和条码。

    > [!NOTE]
    > 对于这两种编号规则，必须将 **作用域** 字段设置为 **公司**。 在大多数情况下，都应自动生成两个序列号。

5. 在 **商业参数** 页的 **条码** 选项卡上，选择您之前创建的条码。
6. 在 **商业共享参数** 页的 **编号规则** 选项卡上，选择您已为优惠券编号和优惠券代码 ID 创建的编号规则。
7. 您现在可以打开 **优惠券** 页和创建新优惠券。

## <a name="the-effect-of-partial-updates-on-coupons"></a>部分更新对优惠券的影响

优惠券功能包括多个独特功能。 商业总部 (HQ) 和渠道可以跨组件部分更新。 因此，了解部分更新对优惠券功能总体的影响十分重要。

- **HQ 被部分更新，但 Commerce Scale Unit 和 POS 不更新。** 在 HQ 更新中，优惠券和折扣页更新，商业价格引擎也更新。 如果两个组件中仅有一个更新，则 Commerce 中的部分页面与价格计算数据不匹配。 因此，在折扣计算期间可能发生意外折扣计算或错误。
- **HQ 被更新，但 Commerce Scale Unit 和 POS 不更新 (N-1)。** 由于并非所有的商店都可以同时更新，因此我们建议您在更新商店前更新 HQ。 在 N-1 方案中，与优惠券相关的新功能在尚未更新的商店中不可用。 例如，优惠券功能引入“排除”行。 如果您对折扣使用排除行，则其不会在运行较早版本的商店中应用这些行。
- **HQ 未被更新，但 Commerce Scale Unit 和 POS 被更新 (N+1)。** 由于在 Commerce Scale Unit 中更新的价格引擎在价格计算期间可以处理旧折扣代码，因此更新应该对此方案没有功能影响。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
