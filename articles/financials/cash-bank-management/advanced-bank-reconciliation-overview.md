---
title: "高级银行对帐概览"
description: "本文介绍高级银行对帐流程的流程。 高级银行对帐功能可以导入可从银行交易记录内自动对帐的银行对账单。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ff59250b836a73986848109ce48f843fed1d71a9
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="advanced-bank-reconciliation-overview"></a>高级银行对帐概览

[!include[banner](../includes/banner.md)]


本文介绍高级银行对帐流程的流程。 高级银行对帐功能可以导入可从银行交易记录内自动对帐的银行对账单。

高级银行对帐功能可以导入银行对账单。 导入的银行对账单然后可以自动从银行交易记录内对帐。 这是高级银行对帐流的步骤。

1.  设置银行对账单导入。
    -   通过数据实体框架导入银行对账单。
    -   三种典型的银行对账单构建格式：ISO20022、BAI2 和 MT940。
    -   此功能可以扩展为任意格式。

2.  设置高级银行对帐使用的编号规则，并且定义银行对帐匹配规则。
    -   对帐匹配规则是用于在对帐过程中筛选银行对帐单行和 Microsoft Dynamics 365 for Finance and Operations 银行交易记录行的一组条件。 根据您的业务惯例，您可以设置多个匹配规则以自动化和优化您的对帐流程。

3.  将银行对账单与 Finance and Operations 银行交易记录对帐。
    -   执行自动匹配和创建对帐日记帐。
    -   并行查看银行对账单和 Finance and Operations 银行交易记录。
    -   如果 Finance and Operations 银行交易记录出现在银行对账单中，但不出现在 Finance and Operations 中，则自动过帐这些银行交易记录。
    -   生成对账单。






