---
title: "设置 SEPA 直接借记授权单"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>设置 SEPA 直接借记授权单

[!include[banner](../includes/banner.md)]




在客户将已经签署的授权授予债权人的情况下，单一欧元支付区 (SEPA) 直接借记允许债权人从客户的银行帐户中筹集资金。 客户签署的授权允许债权人收取付款，并指示客户方银行支付该收款。 此主题的组织是为了显示 SEPA 直接借记授权单的设置流程。

## <a name="prerequisites"></a>先决条件
下表显示必须先就绪然后才能开始的先决条件。

| 类别       | 先决条件                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 国家/地区 | 法人的主要地址必须在以下国家/地区：奥地利、比利时、德国、西班牙、法国、意大利或荷兰。 |

1. 为直接借记授权设置编号规则。每个直接借记授权必须具有一个独有的编号。 使用“编号规则”****页创建直接借记授权的编号规则。 使用该标识符在“应收帐款参数”****页中将编号规则分配给直接借记授权系统。

2. 为直接借记授权设置应收帐款参数。使用**应收帐款参数**页可以设置直接借记授权的参数。 若要设置参数，请在**直接借记**选项卡上，根据需要更改默认参数。 然后，在**编号规则**选项卡上，用您早先设置的更新编号规则**直接借记授权单 ID**字段。

3. 设置直接借记授权的付款方式。您必须按照付款方式的以下附加步骤进行操作： 您将使用此付款方式查询发票以生成直接借记付款。 使用“付款方式”****页可设置付款方式。 若要设置直接借记授权的付款方式，您必须按照付款方式的以下附加步骤进行操作：

-   在“付款类型”****字段中，选择“电子支付”****。
-   选项：如果您希望您的每位客户具有多个授权，请在**期间**字段中选择**发票**。 将会为每张发票创建单独的付款，而每笔付款使用的都是为发票指定的授权。
-   通过使用直接借记授权单，选择“需要授权单”****选项创建付款。 只有当您在“付款类型”****字段中选择“电子支付”****时，“需要授权单”****才可用。

另请参阅[直接借记概览](sepa-direct-debit-overview.md) 



