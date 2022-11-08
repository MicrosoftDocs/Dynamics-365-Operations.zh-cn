---
title: 结帐模块错误参考代码
description: 本文介绍 Microsoft Dynamics 365 Commerce 中面向用户的错误消息中显示的结帐模块错误参考代码。
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728237"
---
# <a name="checkout-module-error-reference-codes"></a>结帐模块错误参考代码

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 中面向用户的错误消息中显示的结帐模块错误代码。

Dynamics 365 Commerce 引入了标准化的错误参考，这些参考可以包含在呈现给在线客户的在线渠道结帐错误中。 在 Commerce 版本 10.0.31 及更高版本中，结帐模块中的错误消息包含错误代码，不会向在线客户显示不必要的信息。 这些错误代码适用于本文详细介绍的错误。

根据遇到的错误，本文中的表包括以下详细信息：

- 导致错误的条件的描述或其他详细信息
- 环境或付款连接器配置中需要考虑的信息
- 如果需要额外帮助，可以在支持案例中引用的信息

## <a name="prerequisites"></a>先决条件

要启用下面列出的结帐模块错误参考代码，在您的站点的站点构建器中，转到 **站点设置 \> 扩展**，在 **购物车和结帐** 部分，选择 **启用增强的在线渠道错误显示消息**。 

## <a name="checkout-module-error-reference-codes"></a>结帐模块错误参考代码

使用下表获取有关客户提供或在线商店中遇到的错误代码参考的更多详细信息。 向右滚动可查看 **错误描述** 列。

| 错误代码 | 动态关联的错误代码 | 错误描述 |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | 无法授权付款。 **TokenizedPaymentCard** 中的卡类型 ID 缺失，或提供的卡类型 ID 不受支持。 |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | 已拒绝。 无法授权付款。 |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | 无法授权付款。 需要客户提供其他信息。 |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | 很抱歉，出现了问题。 我们无法获取卡付款接受结果。 请重试或与您的系统管理员联系。 |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | 无法付款，因为缺少商家付款属性。 请与您的系统管理员联系。 |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | 无法为该操作检索支付方式服务。 请检查所选支付方式的付款方式设置。 |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | 已应用客户帐户付款，但每笔交易只能进行一次付款。 |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | 客户帐户限制与规定数量不同。 请尝试其他付款方式或与客户支持部门联系以获取帮助。 |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | 客户帐户付款超出列出的项的总额。 请稍后重试，或与客户支持部门联系以获取帮助。 |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | 客户帐户付款需要其自己的帐户或支付方式行上匹配的发票金额。 |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | 此时无法处理客户帐户付款 – 已超出下限值。 |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | 此客户不允许分期付款。 |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | 很抱歉，出现了问题。 无法取消付款。 请重试。 |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | 处理付款时出错。 请稍后重试。 |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | 会员付款金额超过了此交易中使用的会员卡允许的金额。 |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | 会员退款金额超过了此交易中使用的会员卡允许的金额。 |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | 未找到会员卡号。 请激活会员卡编号或输入其他卡号，然后重试。 |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | 会员卡号不可用。 请输入其他卡号，然后重试。 |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | 此会员卡无兑换此交易记录的会员积分的资格。 |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | 礼品卡编号遇到错误。 请尝试其他礼品卡，或与客户支持部门联系以获取帮助。 |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | 金额超出礼品卡上的余额。 请输入不同的金额，然后重试。 |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | 交易记录不能包含多个会员付款行。 |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | 付款信息缺失或不正确。 请验证付款信息，然后重试。 |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | 此时无法处理订单。 请稍后重试。 |
| CCR025     | 结帐 API 的前端超时 | 前端操作已超时。请确认订单是否已在 Dynamics 365 Commerce headquarters 中处理。 |
| CCR026     | 原始授权金额更改 | 订单金额已更改，与付款网关处理的原始授权金额不同。 可能是由于优惠券、促销或优惠的时间到期。 |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | 处理付款时出错。 提供给购物车 API 的参考与预期的参考不同（注意结帐过程中可能存在不一致）。 |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | 尝试使用的付款方式遇到错误。 请与支持人员联系以审查您的帐户设置，或使用其他付款方式重试。 |

## <a name="additional-resources"></a>其他资源

[付款常见问题](dev-itpro/payments-retail.md)

[结账模块](add-checkout-module.md)

[付款模块](payment-module.md)
