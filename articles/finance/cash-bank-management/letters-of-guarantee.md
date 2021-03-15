---
title: 保函
description: 本文提供有关保函的信息。 在保函中，如果银行客户之一拖欠某人员的付款或合同，银行同意向该人员支付特定金额。
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: roschlom
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b86ccc46475babb302cdbf82f5c99c26e2091501
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978781"
---
# <a name="letters-of-guarantee"></a>保函

[!include [banner](../includes/banner.md)]

本文提供有关保函的信息。 在保函中，如果银行客户之一拖欠某人员的付款或合同，银行同意向该人员支付特定金额。 

信用保证书是由银行（保人）支付金钱到某人（受益人）的协议，如果银行的客户（主要的）在付款或合同默认为受益人。 保函是不可转移的。 它们仅适用于协议中指定的受益人。 依据协议持续时间，主要客户可以请求增减信用保证书的值。 

若要结算信用保证书，受益人必须在到期日期之前提交原始信用保证书和通知主要客户默认的银行。 根据保函条款，银行然后由于受益人的帐户支付金额。 银行预留付款的百分比作为毛利。 百分比在协议条款审核并指定。 

您可以创建代码跟踪保函的用途。 当保函取消时，您还可以指定可与保函关联的原因。 您可以在 **付款目的代码** 和 **银行原因** 页查看目的代码和银行原因。 

您可以使用 **保函** 页完成以下任务：

-   创建正确的分类帐条目并消除手动输入。
-   记录所有货币性和非货币性交易记录和跟踪保函余额。
-   记录和跟踪保函状态和到期。
-   生成列出了各个持有信用保证书的银行的报表。

下表介绍了您可以在保函中执行的操作。

| 行为              | 用途                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| 提交至银行      | 提交信用保证书申请给银行。                                                                       |
| 从银行收到   | 在银行同意已提交的申请后，从银行托收信用保证书。                            |
| 给予受益人 | 在您从银行收到信用保证书后，提供信用保证书给受益人。              |
| 增加值      | 如果同意受益人和主要审核，则增加货币值。                                                  |
| 减少值      | 如果同意受益人和主要审核，则减少货币值。                                                  |
| 扩展              | 在您提供信用保证书给受益人后，如果需要扩展，扩展有效期。 |
| 取消              | 在保函请求的用途不再适用时，取消协议。                  |
| 清偿           | 在受益人显示信用保证书到银行后，清除信用保证书。                      |


有关详细信息，请参阅以下主题：

[保函交易记录](tasks/letter-guarantee-transaction.md)

[设置保函的银行设施和过帐模板](tasks/set-up-bank-facilities-posting-profiles.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]