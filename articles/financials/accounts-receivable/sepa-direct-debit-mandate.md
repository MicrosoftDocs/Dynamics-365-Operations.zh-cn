---
title: "设置 SEPA 直接借记授权单"
description: "在客户将已经签署的授权授予债权人的情况下，单一欧元支付区 (SEPA) 直接借记允许债权人从客户的银行帐户中筹集资金。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 242d6d3d517ad5190b96ace36bd585a5769ae994
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-sepa-direct-debit-mandate"></a>设置 SEPA 直接借记授权单

[!include [banner](../includes/banner.md)]

在客户将已经签署的授权授予债权人的情况下，单一欧元支付区 (SEPA) 直接借记允许债权人从客户的银行帐户中筹集资金。 客户签署的授权允许债权人收取付款，并指示客户方银行支付该收款。 此主题的组织是为了显示 SEPA 直接借记授权单的设置流程。

## <a name="prerequisites"></a>先决条件
下表显示必须先就绪然后才能开始的先决条件。

| 类别       | 先决条件                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 国家/地区 | 法人的主要地址必须在以下国家/地区：奥地利、比利时、德国、西班牙、法国、意大利或荷兰。 |

1. 为直接借记授权设置编号规则。每个直接借记授权必须具有一个独有的编号。 使用**编号规则**页创建直接借记授权的编号规则。 使用该标识符在**应收账款参数**页中将编号规则分配给直接借记授权系统。

2. 为直接借记授权设置应收账款参数。使用**应收账款参数**页可以设置直接借记授权的参数。 若要设置参数，请在**直接借记**选项卡上，根据需要更改默认参数。 然后，在**编号规则**选项卡上，用您早先设置的更新编号规则**直接借记授权单 ID**字段。

3. 设置直接借记授权的付款方式。您必须按照付款方式的以下附加步骤进行操作： 您将使用此付款方式查询发票以生成直接借记付款。 使用**付款方式**页可设置付款方式。 若要设置直接借记授权的付款方式，您必须按照付款方式的以下附加步骤进行操作：

-   在**付款类型**字段中，选择**电子支付**。
-   选项：如果您希望您的每位客户具有多个授权，请在**期间**字段中选择**发票**。 将会为每张发票创建单独的付款，而每笔付款使用的都是为发票指定的授权。
-   通过使用直接借记授权单，选择**需要授权单**选项创建付款。 只有当您在**付款类型**字段中选择**电子支付**时，**需要授权单**才可用。

其他资源

[直接借记概览](sepa-direct-debit-overview.md) 

[为客户创建直接借记授权单](tasks/create-direct-debit-mandate-customer.md) 


