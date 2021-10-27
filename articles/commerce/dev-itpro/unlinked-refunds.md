---
title: 使用面向 Adyen 的 Dynamics 365 Commerce Payment Connector 处理非关联退款
description: 本主题介绍了使用面向 Adyen 的 Microsoft Dynamics 365 Payment Connector 时非关联退款的操作方式。
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c137dcf7d35031a293c88d8c4f5dc1e5f3d9e2f9
ms.sourcegitcommit: a21a664cd35b95c8600c5af0aac588a64e892902
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2021
ms.locfileid: "7623913"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>使用面向 Adyen 的 Dynamics 365 Commerce Payment Connector 处理非关联退款

[!include [banner](../includes/banner.md)]

本主题介绍了使用[面向 Adyen 的 Microsoft Dynamics 365 Payment Connector](adyen-connector.md) 时非关联退款的操作方式。 它还审查了在销售点 (POS) 或呼叫中心针对新付款方式处理退款的能力。

面向 Adyen 的 Dynamics 365 Payment Connector 支持使用不同于用于原始交易的付款方式处理退款的功能。 虽然我们建议您使用[关联退款](linked-refunds.md)根据提供的原始付款方式处理退款，但在某些情况下需要向其他付款方式退款。 例如，用于原始付款的卡现在可能已过期或丢失，或者用户可能已取消该卡。

## <a name="prerequisites"></a>先决条件

必须先满足以下先决条件，面向 Adyen 的 Dynamics 365 Payment Connector 才能处理非关联退款：

- 设置[付款方式](../payment-methods.md)。
- 设置[全渠道付款](../omni-channel-payments.md)。

## <a name="additional-configuration"></a>其他配置

适用于 Adyen 的 Dynamics 365 Payment Connector 提供下节中所介绍的每种受支持退款方案的现成实施。 未使用面向 Adyen 的 Dynamics 365 Payment Connector 的现成实现功能的客户必须设置支持信用卡标志的连接器。

## <a name="supported-refund-scenarios"></a>支持退款方案

Dynamics 365 Commerce 支持对先前批准和确认的交易进行退款。 退款可以包括交易的全额退款或部分退款。 退款不能超过原始付款授权全额。 非关联退款仅在 POS 和呼叫中心受支持。

## <a name="enable-unlinked-refunds-functionality"></a>启用非关联退款功能

要在 Commerce Headquarters 中启用非关联退款功能，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**。
1. 在 **全渠道付款** 选项卡中，将 **使用全渠道付款** 选项设置为 **是**。

### <a name="supported-payment-method-variants"></a>支持的付款方式变型

以下付款方式变型支持现成的非关联退款：

- 卡
- 电子钱包

并非所有付款方式变型都支持非关联退款。 下表提供了一系列通用付款方式，并显示每种方法对关联和非关联退款的支持能力。

| 付款方式        | 关联退款 | 非关联退款 |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | 是           | 是             |
| amexconsumer          | 是           | 是             |
| amexcorporate         | 是           | 是             |
| amexdebit             | 是           | 是             |
| amexprepaid           | 是           | 是             |
| amexprepaidreloadable | 是           | 是             |
| amexsmallbusiness     | 是           | 是             |
| discover              | 是           | 是             |
| maestro               | 是           | 是             |
| maestrouk             | 是           | 是             |
| mc                    | 是           | 是             |
| mcalphabankbonus      | 是           | 是             |
| mcprepaidanonymous    | 是           | 是             |
| visa                  | 是           | 是             |
| visaalphabankbonus    | 是           | 是             |
| visacheckout          | 是           | 是             |
| visadankort           | 是           | 是             |
| visahipotecario       | 是           | 是             |
| visasaraivacard       | 是           | 是             |
| vpay                  | 是           | 是             |
| givex                 | **否**        | 是             |
| svs                   | **否**        | 是             |
| cup                   | 是           | 是             |
| diners                | 是           | 是             |
| interac               | **否**        | 是             |
| jcb                   | 是           | 是             |
| jcb_applepay          | 是           | 是             |
| unionpay              | 是           | 是             |

### <a name="process-an-unlinked-refund-in-pos"></a>在 POS 中处理非关联退款

客户可以在允许的退货期内将物品退还给 POS 收银员并拥有有效收据。 在处理退款期间，**退货付款** 对话框包含 **选择付款方式** 选项。 然后，收银员可以在支持的退款付款方式（卡和钱包）中选择付款方式。

### <a name="process-an-unlinked-refund-in-call-center"></a>在呼叫中心处理非关联退款

在呼叫中心针对订单处理非关联退款时，呼叫中心员工会选择与原始付款方式不同的付款方式。 然后系统会提示员工获取管理员替代个人标识号 (PIN)。 在处理不同的付款方式以进行退款之前，需要 PIN。

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>为呼叫中心设置管理员替代 PIN

若要在 Commerce Headquarters 中为呼叫中心设置管理员替代 PIN，请按照以下步骤操作。

1. 转到 **Retail 和 Commerce Channel \> 渠道设置 \> 呼叫中心设置**，或搜索“替代权限”。
1. 选择允许其具有非关联退款处理权限的角色。
1. 在 **退款** 快速选项卡上，将 **允许替代付款** 选项设置为 **是**。

## <a name="additional-resources"></a>其他资源

[面向 Adyen 的 Dynamics 365 Payment Connector](adyen-connector.md)

[以前批准和确认的交易的关联退款](linked-refunds.md)
