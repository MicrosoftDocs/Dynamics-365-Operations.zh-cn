---
title: "单个凭证和货币重估升级"
description: "某些组织输入的日记帐中包含有多位客户或供应商的单一凭证，并且还运行应收账款或应付账款外币重估流程。 此主题描述这些组织在升级到 Microsoft Dynamics 365 for Operations 版本 1611 时应执行的步骤。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>单个凭证和货币重估升级

[!INCLUDE [banner](../includes/banner.md)]

某些组织输入的日记帐中包含有多位客户或供应商的单一凭证，并且还运行应收账款或应付账款外币重估流程。 此主题描述这些组织在升级到 Microsoft Dynamics 365 for Operations 版本 1611 时应执行的步骤。

升级到 Microsoft Dynamics 365 for Operations 版本 1611 时，请执行以下步骤。

1.  升级到 Dynamics 365 for Operations 之前，请为应收账款和应付账款运行外币重估流程。 将**方法**字段设置为**发票日期**。 将创建一条重估交易记录，用于冲销上一笔外币重估。 因此，将以原始会计币种计算这笔未结交易记录的价值。
2.  升级到 Dynamics 365 for Operations 版本 1611。
3.  再次运行应付账款和应收账款外币重估流程。 此时，将**方法**字段设置为**标准**。 将根据当前汇率创建一条新的重估交易记录。 此交易记录记录或有利润/损失和正确的汇总会计科目。





