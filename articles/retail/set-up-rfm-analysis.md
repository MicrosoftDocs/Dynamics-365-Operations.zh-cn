---
title: "设置 RFM 分析"
description: "本主题解释了如何设置客户的 Recency、频率和货币 (RFM) 分析。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e11ec02d7392601b22e17384a4dbf620b79df035
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-rfm-analysis"></a>设置 RFM 分析

[!include[banner](includes/banner.md)]


本主题解释了如何设置客户的 Recency、频率和货币 (RFM) 分析。

Recency、频率和货币 (RFM) 分析是一个您的组织用来评估由客户购买生成的数据的市场营销工具。 在设置了 RFM 分析后，客户在购买时会被分配计算过的 RFM 得分。 RFM 得分可以是一个三位等级，也可以是一个总数，具体取决于您的组织如何配置了 RFM 分析。 如果您的组织使用三位数等级的得分，则第一位数为客户的 Recency 等级（客户最近从您的组织进行购买的频率）。 第二位数为客户的频率等级（客户从您的组织进行购买的频率）。 第三位数为客户的货币等级（客户在从您的组织进行购买时花费的货币量）。 例如，您的组织设置 1 至 5 的等级，其中 5 是最高等级。 在此情况下，客户等级 535 可告知您有关客户的以下信息：

-   **Recency 等级 5** – 客户最近进行了购买。
-   **频率等级 3** – 客户从您的组织购买产品的频率中等。
-   **货币等级 5** – 在客户购买时，支出了一大笔钱。

如果您的组织使用总分数，则将各个等级加起来。 对于同一示例，客户具有等级 13 (5 + 3 + 5)。




