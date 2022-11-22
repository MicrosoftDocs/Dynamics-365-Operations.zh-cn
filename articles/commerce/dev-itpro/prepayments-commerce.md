---
title: Dynamics 365 Commerce 中的预付款
description: 本文概述了 Microsoft Dynamics 365 Commerce 中的预付款交易的处理。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780348"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Dynamics 365 Commerce 中的预付款

[!include[banner](../includes/banner.md)]

本文概述了 Microsoft Dynamics 365 Commerce 中的预付款交易的处理。

Dynamics 365 Commerce 处理应收帐款或 Commerce 中使用的以下付款类型的预付款交易：

- **客户帐户预存款付款** – 客户在销售点 (POS) 支付预存款。 Commerce 作为预付款交易处理预存款付款。 当您过帐交易时，将在 Commerce headquarters 的 **日记帐凭证** 页面创建付款日记帐并过帐。 将自动选中付款日记帐 **付款** 选项卡上的 **预付款日记帐凭证** 复选框。 有关更多信息，包括与目标区域相关的预付款和税务特定信息，请参阅[全球化资源 - 国家/地区特定帮助内容](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content)。
- **有预存款的客户订单** – 客户在 POS 创建客户订单。 客户可以根据在 Commerce headquarters 的 **客户订单** 页面配置的默认预存款百分比（**Commerce 参数 \> 客户订单**）为订单支付预存款。 Commerce 作为预付款交易处理客户订单的预存款付款。 当您过帐交易时，将在 **日记帐凭证** 页面创建付款日记帐并过帐。 将自动选中付款日记帐 **付款** 选项卡上的 **预付款日记帐凭证** 复选框。 付款将完成结算，客户发票将在订单提货或送货时自动开具。
- **呼叫中心销售订单** - 呼叫中心客户服务代表代表客户创建销售订单，在付款捕获期间，**预付款** 属性在付款捕获期间设置为 **是**。

Commerce 执行以下任务来处理预付款：

- **处理客户帐户预存款付款** – 通过使用同步数据的服务，将客户支付的预存款付款转移到 Commerce。 Commerce 为付款创建零售付款交易。 当您过帐零售交易时，会过帐现金日记帐或客户付款日记帐。 将自动选中 Commerce headquarters 中 **日记帐凭证** 页面的 **付款** 选项卡上付款日记帐的 **预付款日记帐凭证** 复选框。 如果付款金额为负数，将无法处理预付款。
- **处理有预存款的客户订单或销售订单** – 客户使用 Commerce Data Exchange: 实时服务支付客户订单所需的预存款。 Commerce 根据客户使用的付款方式创建客户付款日记帐或现金日记帐。 将自动选中 Commerce headquarters 中 **日记帐凭证** 页面的 **付款** 选项卡上日记帐的 **预付款日记帐凭证** 复选框。 如果客户使用多种付款方式进行部分付款，Commerce 会根据所使用的付款方式处理每笔部分付款。

对于信用卡以及具有基础信用卡付款方式的数字钱包，Commerce 会在成功授权后发送“捕获”请求。 （在销售订单开票之前捕获资金。）

如果您取消客户订单，将退还预付款金额，并过帐退款付款日记帐中的预存款金额。 退款金额根据您在过帐退款付款时指定的付款方式计算和过帐。 Commerce 可能会根据您在 Commerce headquarters 中的 **Commerce 参数** 页面上设置的百分比收取取消费用。

如果您退回客户订单，会创建退货单和退款付款日记帐。 当您过帐退货单时，Commerce 会创建客户付款日记帐或现金日记帐，具体取决于客户用于原始交易的付款方式。
