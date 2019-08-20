---
title: SEPA 直接借记概览
description: 单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。 国内和跨境付款之间不存在差异。 SEPA 包含 28 个欧盟 (EU) 成员国，以及冰岛、列支敦斯登、挪威、瑞士、摩纳哥和圣马力诺。 SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。 最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcb7585d344988e00093231f785c1a746226e4e0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836628"
---
# <a name="sepa-direct-debit-overview"></a>SEPA 直接借记概览

[!include [banner](../includes/banner.md)]

单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。 国内和跨境付款之间不存在差异。 SEPA 包含 28 个欧盟 (EU) 成员国，以及冰岛、列支敦斯登、挪威、瑞士、摩纳哥和圣马力诺。 SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。 最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>SEPA 直接借记的目标是什么？
---------------------------------------

在向债权人授予客户已签署授权的情况下，SEPA 直接借记允许债权人从客户的银行帐户中筹集资金。 客户签署授权允许债权人收取付款并指示客户的银行支付该收款。 

SEPA 直接借记第一次创建了一种可以用于 32 个 SEPA 国家/地区中国内和跨境欧元直接借记的付款工具。 

可采用两种方案：SEPA 核心直接借记方案和 SEPA 企业到企业 (B2B) 直接借记方案。 两种方案使用相同的文件格式。

## <a name="what-is-the-core-direct-debit-scheme"></a>什么是核心直接借记方案？
SEPA 核心直接借记方案是基本方案。 它具有以下属性：
-   资金以欧元转帐（即便是银行帐户可能以其他币种存有资金)。
-   客户和债权人必须各自持有位于 SEPA 中信用机构的帐户。
-   客户必须授予该债权人一份已签署的授权。
-   在最后启动收款的 36 个月之后授权到期。
-   只要授权有效或在最后收款之后的至少 14 个月里，债权人必须保存授权。
-   该方案可以用于单个（一次性）收款或重复直接借记收款。
-   客户在其帐户借记后长达八周内具有接收退款“不受质询”的权利。

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>什么是 SEPA 企业到企业 (B2B) 直接借记方案？
SEPA B2B 直接借记方案应用于企业到企业的交易记录以及在 SEPA 核心直接借记方案上设置。 主要差异在于：
-   在客户为私人个体（消费者）时，不允许 SEPA B2B 直接借记方案。
-   该客户没有资格获取已授权交易记录的退款。
-   客户银行必须根据授权信息对收款进行验证，以确保该收款为授权的。 客户银行和客户必须同意针对每个直接借记执行验证。
-   该方案提供较短的时间线用于呈现直接借记及缩短返还周期。

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>我能将 COR1 方案用于直接借记授权单吗？
是。 您可以在奥地利、比利时、德国、法国、意大利、西班牙和荷兰对 SEPA 直接借记授权单使用 COR1 方案。 该方案提供针对直接借记收款为债权人提供短时提前通知。

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>什么是国际银行帐号 (IBAN) 和银行标识符代码 (BIC)?
国际银行帐号 (IBAN) 和银行标识符代码 (BIC) 用于标识在 32 个 SEPA 国家/地区的任何帐户。 在“SWIFT 代码”字段中输入 BIC，在“IBAN”字段中输入 IBAN。 这两个字段位于“银行帐户”页中的“银行帐户”选项卡上的“附加标识”快速选项卡上。 这对于债权人的银行帐户和客户的银行帐户皆适用。

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>我在何处输入债权人标识符（直接借记 ID）?
在 SEPA 中，每个债权人由唯一的标识符确定债权人。 此标识符允许客户和客户银行筛选每个直接借记，然后根据客户说明处理或拒绝该直接借记。 债权人必须通过其银行申请此标识符。 在“直接借记 ID”中针对法人的银行帐户输入此标识符。

## <a name="what-are-mandates"></a>什么是授权？
客户签署授权允许债权人收取付款并指示客户的银行支付该收款。 客户可以以纸质或电子形式签发授权。 默认情况下，在最后启动直接借记的 36 个月之后该授权到期。

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>我在何处指定 SEPA 直接借记文件格式 (ISO 20022)?
SEPA 数据格式基于 ISO 20022 消息标准。 当您配置应收账款的付款方式时，您将选中“一般电子申报”复选框并选择 SEPA 直接借记格式作为导出格式配置。 当您在客户付款日记帐中生成一个付款文件时，您使用该付款方式。

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>我可以生成哪种格式的 SEPA 直接借记付款文件？
可以按照以下格式为 SEPA 直接借记生成电子付款文件：
-   针对比利时、德国、西班牙、法国、意大利和荷兰按 ISO 20022 PAIN.008.001.02 XML 文件格式生成 SEPA 直接借记付款文件。
-   针对奥地利按 PAIN.008.001.02 XML 文件格式生成 SEPA 直接借记付款文件，针对德国按照 PAIN.008.003.02 XML 文件格式生成 SEPA 直接借记付款文件。

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>如何使用 SEPA 直接借记退款和还款？
在两个 SEPA 直接借记方案中，客户具有某些退款权限。 在到期日期后的八周内，允许客户撤消任何已授权的交易记录，而不必说明原因。 在未授权的交易记录情况下，该时间延长至到期日期的 13 个月之后。 通过使用“客户交易记录”页中的“取消付款”按钮手动完成撤消任何已执行的付款。





