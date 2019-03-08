---
title: 设置汇票
description: 此主题描述设置汇票的步骤。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cda597b1d99e99ac5c5c396bcfcec9c0712f0eb1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "344700"
---
# <a name="set-up-bills-of-exchange"></a>设置汇票

[!include [banner](../includes/banner.md)]

此主题描述设置汇票的步骤。

汇票是来自客户的手写或电子形式的订单，它指定其他方（通常是银行）应向公司支付指示的金额。 在您使用汇票作为针对销售订单发票或普通发票的付款时，您贷记该客户帐户。 该贷记由汇票担保，直到客户向银行支付汇票。 您通常将在到期日期通过汇票结算发票。 在您收到来自承兑汇票的银行的通知后，就可以关闭该汇票。 您可以在以下时间之一通过您的银行支取汇票：

-   到期日期。 此方法也称作“托收汇款”。
-   在到期日期前，通常在为客户设置的付款期限指定的折扣日期。 当您过账交易记录时，将折扣金额过账到支出科目。 剩余金额时之于您的负债（直到银行从客户接收了付款）。 此方法也称作“折扣汇款”。

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>设置汇票的过帐模板

使用**客户过帐模板**页面设置过帐模板，以便用于汇票、拒付的汇票、托收汇款和折扣汇款。 在**汇总科目**字段中，选择要将汇票金额过帐到的汇总科目。 根据汇款交易记录的类型借记或贷记此账户：
-   对于汇票，在过帐汇票时借记此帐户，在过帐折扣汇款或托收汇款时贷记此帐户。
-   对于拒付汇票，在过帐拒付汇票时借记此帐户。
-   对于托收汇款，在过帐托收汇款时借记此帐户。
-   对于折扣汇款，在过帐折扣汇款时借记此帐户。

在**结算科目**字段中，选择要将汇票金额过帐到的现金帐户。 在结算汇票时借记此帐户。 在**销售税预付款**字段中，选择在汇票用于预付时要将增值税金额过帐到的汇总科目。 在**折扣负债科目**段中，选择您要将折旧汇款的折扣金额过账到的账户。 在过帐折扣汇款时贷记此帐户。

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>为汇票设置应收账款参数

在**应收账款参数**页，在**分类帐和销售税**选项卡上输入汇票的默认过帐模板。在**编号规则**选项卡上定义编号规则。

## <a name="set-up-journal-names-for-bills-of-exchange"></a>设置汇票的日志名称


在**日记帐名称**页面中，至少创建五个要用于汇票的日志名称。 下面是日记帐类型：
-   **客户签发汇票** – 为签发汇票日记帐创建日记帐名称。
-   **客户拒付汇票** – 为拒付汇票日记帐创建日记帐名称。
-   **客户重新签发汇票** – 为重新签发汇票日记帐创建日记帐名称。
-   **客户银行汇款** – 为汇款日记帐创建日记帐名称。
-   **客户结算汇票** – 为结算汇票日记帐创建日记帐名称。

在每个汇票日记帐的日记帐凭证页上，在**汇票**选项卡上输入有关汇票的信息。在过帐汇票日志行后，可以在**汇票日记帐查询**页面和**汇票统计信息**页面中看到这些行。

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>设置汇票的付款方式

在**付款方式**页面中，为汇票至少设置一种付款方式。 如果您与多家银行有业务往来，则设置的付款方式应该与每家银行需要的汇票汇款格式相符。

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>设置汇票的付款费用

汇款付款是与客户付款收取过程有关的费用。 每个付款费用可以与多个付款费用设置行关联。 可使用设置行可以控制如何计算付款费用的默认金额。 例如，您可以针对付款方法、付款说明、币种和时段创建设置行。 也可以为基于日期间隔的百分比或金额创建设置行。 例如，可以设置基于逾期时间长度的利息百分比。 如果银行为不同的汇款类型（例如**征收**或**折扣**）收取不同的费用，则为各汇款类型设置单独的付款费用行。

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>为银行汇款文件设置汇款费用

在**银行帐户**页面中，您可以设置银行向生成的每个汇款文件收取的汇款费用。 在汇款已确认并且实收费用额已知时，过帐汇款费用。 汇款费用不同于付款费用，后者将从客户收取并且附加到日志行。

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>设置汇票的单据版式

在**银行帐户**页面中，单击**设置**，然后指定将为其生成打印的汇票单据的各个银行帐户所需的单据版式。

## <a name="set-up-customers-for-bills-of-exchange"></a>为汇票设置客户

在**客户**页面中的**付款默认值**选项卡上，对于同意通过使用汇票支付的每个客户，您可以设置汇票的默认付款方式。





