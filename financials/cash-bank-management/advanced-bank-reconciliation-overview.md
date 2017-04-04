---
title: "高级银行对帐概览"
description: "本文介绍高级银行对帐流程的流程。 高级银行对帐功能可以导入可从银行交易记录内自动对帐的银行对帐单。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>高级银行对帐概览

本文介绍高级银行对帐流程的流程。 高级银行对帐功能可以导入可从银行交易记录内自动对帐的银行对帐单。

高级银行对帐功能可以导入银行对帐单。 导入的银行对帐单然后可以自动从银行交易记录内对帐。 这是高级银行对帐流的步骤。

1.  设置银行对帐单导入。
    -   通过数据实体框架导入银行对帐单。
    -   三种典型的银行对帐单构建格式：ISO20022、BAI2 和 MT940。
    -   此功能可以扩展为任意格式。

2.  设置高级银行对帐使用的编号规则，并且定义银行对帐匹配规则。
    -   对帐对于的规则是用于在对帐过程中筛选银行对帐单对报表行和 Microsoft Dynamics 365 工序银行交易记录行的一组条件。 根据您的商业惯例，您可以设置多个匹配的规则同时自动化和优化您的对帐过程。

3.  银行对帐单对帐的银行交易工序记录的 Dynamics 365。
    -   执行自动匹配和创建对帐日记帐。
    -   并排显示银行对帐单和 Dynamics 365 工序银行交易记录。
    -   自动过帐工序记录的银行交易 Dynamics 365，如果它们在银行对帐单，但不希望显示在工序的 Dynamics 365。
    -   生成对帐单。




