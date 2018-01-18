---
title: "创建零售销售优惠券"
description: "此主题提供零售优惠券概览并阐述如何进行设置。"
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e05361bf865e44ba6073198fba94d7102b1ed19
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="create-coupons-for-retail-sales"></a>创建零售销售优惠券

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>优惠券概览

优惠券是用于将零售折扣添加到交易的代码和条码。 每张优惠券可以有多个代码，且每个代码可以有自己的有效日期。 

每张优惠券都关联一个零售折扣。 与折扣关联的价格组定义可以使用优惠券的客户或优惠券有效的渠道。 

优惠券基本上是零售折扣顶部的附加验证。 优惠券提供必需的优惠券代码和条码，以及这些代码的日期范围。 优惠券还提供可选使用限制和客户要求的属性。 折扣提供优惠券对其有效的产品集。 折扣的价格组提供优惠券对其有效的客户、渠道或目录集。

要创建优惠券，须分开创建折扣和优惠券。 然后通过选择 Microsoft Dynamics 365 for Retail 优惠券页面的折扣进行关联。 

> [!NOTE]
> 优惠券关联到折扣后，Microsoft Dynamics 365 for Retail 折扣页上的多个字段变为只读，因为其由优惠券的设置管理。 这些字段包括用于状态和标准日期范围的字段。

### <a name="limited-use-coupons"></a>有限使用的优惠券

优惠券可以配置为有限使用的优惠券。 使用限制可以按客户或渠道进行配置，或配置为全球限制。 在 POS 中或销售订单录入期间输入或扫描代码或条码时执行此限制。 当关联优惠券的订单完成时，优惠券记录为已使用。

此限制按优惠券上的优惠券代码执行。 例如，具有两个优惠券代码的单次使用优惠券可以使用两次：每个优惠券代码可使用一次。 优惠券上的每个代码可以单独设置为有效。

## <a name="managing-coupons"></a>管理优惠券

您必须分开创建折扣和优惠券。 之后可以通过选择优惠券页面上的折扣将它们关联。 将优惠券关联到折扣后，折扣的多个字段变为只读，因为其由优惠券的设置管理。 这些字段包括用于状态和标准日期范围的字段。  

优惠券现在基本上是零售折扣顶部的附加验证。 优惠券提供优惠券代码和条码以及日期范围、使用限制和客户要求的属性。 折扣提供优惠券对其有效的产品集。 折扣的价格组提供优惠券对其有效的客户、渠道或目录集。

## <a name="system-setup-for-coupons"></a>优惠券系统创建 

在您可以设置优惠券前，必须先设置优惠券条码和两个优惠券编号规则。 

1.  在**掩码字符**页，为优惠券代码创建新的掩码字符。 您可以选择任何未使用的字符。
2.  在**条码掩码设置**页，创建一个新的条码掩码。 将**类型**字段设置为**优惠券**。
3.  在**条码设置**页，创建使用您刚才创建的条码掩码的新条码。
4.  在**编号规则**页，创建两个新的编号规则。 一个规则用于优惠券代码 ID，另一个规则用于优惠券编号。 优惠券代码 ID 是优惠券各优惠券代码的唯一标识符。 优惠券编号是优惠券的唯一标识符。 每张优惠券可以有多个触发优惠券的代码和条码。

    > [!NOTE]
    > 对于这两种编号规则，必须将**作用域**字段设置为**公司**。 在大多数情况下，都应自动生成两个序列号。

5.  在**零售共享参数**页的**条码**选项卡上，选择您之前创建的条码。
6.  在**零售参数**页的**编号规则**选项卡上，选择您已为优惠券编号和优惠券代码 ID 创建的编号规则。
7.  您现在可以打开**优惠券**页和创建新优惠券。

## <a name="the-effect-of-partial-updates-on-coupons"></a>部分更新对优惠券的影响

优惠券功能包括 Dynamics 365 for Retail 中的多个独特功能。 Microsoft Dynamics 365 for Retail 总部 (HQ) 和渠道可以跨组件部分更新。 因此，了解部分更新对优惠券功能总体的影响十分重要。

- **HQ 被部分更新，但 Retail 服务器和 POS 不更新。** 在 HQ 更新中，优惠券和折扣页更新，零售价格引擎也更新。 如果两个组件中仅有一个更新，则 Retail 中的部分页面与价格计算数据不匹配。 因此，在折扣计算期间可能发生意外折扣计算或错误。
- **HQ 更新，但 Retail 服务器和 POS 不更新 (N-1)。** 由于并非所有的零售商店可以同时更新，因此我们建议您在更新零售商店前更新 HQ。 在 N-1 方案中，与优惠券相关的新功能在尚未更新的商店中不可用。 例如，优惠券功能引入“排除”行。 如果您对折扣使用排除行，则其不会应用在运行较早版本的零售商店中。
- **HQ 不更新，但 Retail 服务器和 POS 更新 (N+1)。** 由于在 Retail 服务器中更新的价格引擎在价格计算期间可以处理旧折扣，因此更新应该对此方案没有功能影响。

