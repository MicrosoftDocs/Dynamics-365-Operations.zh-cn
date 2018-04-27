---
title: "调整现有库存量成本价值"
description: "使用”现有库存量调整“页调整库存结转流程运行后的现有库存量数量的成本价值。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 21942f7aa57d21f70e3014051c42328164b750a3
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="adjust-on-hand-inventory-cost-values"></a>调整现有库存量成本价值

[!INCLUDE [banner](../includes/banner.md)]

使用”现有库存量调整“页调整库存结转流程运行后的现有库存量数量的成本价值。

您可以使用**现有库存量调整**页调整库存结转流程运行后的现有库存量数量的成本价值。 **注意：**若要打开**现有库存量调整**页，在**结转与调整**页上，选择已完成的库存结转流程的记录，然后单击**调整** &gt; **现有**。 **示例：**您在 2 月份具有以下交易记录：

-   2 月 1 日：以 10.00 美元的成本有数量为 2 的库存财务收货
-   2 月 5 日：以 13.00 美元的成本有数量为 1 的库存财务收货
-   2 月 19 日：以 11.00 美元的移动平均成本有数量为 1 的库存财务发货

此物料以先进先出 (FIFO) 库存模型设置，并在 2 月 28 日结转库存。 11.00 美元的财务发货交易记录将对照 2 月 1 日的财务收货结算，并将做 1.00 美元的调整。 以下库存收货将包含未结库存数量：

-   2 月 1 日：成本为 10 美元的数量 1
-   2 月 5 日：成本为 13.00 美元的数量 1

若要将这两个物料的成本设置为 USD 15.00，请使用现有量调整选项来调整截至最后库存结转期间的未结现有数量。 **注意：**现有量调整交易记录的过帐日期将是上一次库存结转的日期。 不能修改此日期。

