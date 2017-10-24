---
title: "按库存维度跟踪移动平均成本"
description: "库存维度组附加到每个库存物料。 因此，基于选择的在财务上正跟踪的库存维度，计算某一物料的经常性平均成本价。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a88ec380810a9a2d7048d5a8773ebb5960e4cf86
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>按库存维度跟踪移动平均成本

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


库存维度组附加到每个库存物料。 因此，基于选择的在财务上正跟踪的库存维度，计算某一物料的经常性平均成本价。

库存维度有三种类型：产品，存储区和跟踪。 产品维度包括配置、大小和颜色。 产品维度始终在财务上跟踪。 存储和跟踪维度包括站点、仓库、库位、库存状态、牌照、批处理号和序列号。 您可以决定在财务上跟踪哪一存储和跟踪维度。 

**示例 1** 

如果按仓库从财务上跟踪附加到物料的存储维度组，则将为每个仓库都计算移动平均成本价。 以下采购订单已开票：

-   数量为 2 且成本价为 USD 10.00 的采购订单已为仓库 GW 开票。
-   数量为 3 且成本价为 USD 12.00 的采购订单已为仓库 GW 开票。
-   数量为 5 且成本价为 USD 15.00 的采购订单已为仓库 MW 开票。

仓库 GW 的移动平均成本价为 USD 11.20，并且，仓库 MW 的移动平均成本价为 USD 15.00。 为仓库 GW 过帐销售订单发票。 库存和所售货物成本的价值（在执行库存结转前并且未标记）将是 USD 11.20。 为仓库 MW 过帐另一个销售订单。 库存和所售货物成本的价值（在执行库存结转前并且未标记）将是 USD 15.00。 

**示例 2**如果附加到物料的存储维度组按仓库从财务上跟踪，并按批号从财务上跟踪跟踪维度组，则为每个批次计算移动平均成本价。 

**注意：**我们建议您始终查看正在跟踪的所有财务维度的成本价。 以下采购订单已开票：

-   数量为 2 且成本价为 USD 10.00 的采购订单已为仓库 GW 和批处理 AAA 开票。
-   数量为 3 且成本价为 USD 12.00 的采购订单已为仓库 GW 和批处理 AAA 开票。
-   数量为 2 且成本价为 USD 15.00 的采购订单已为仓库 GW 和批处理 BBB 开票。

仓库 GW 和批处理 AAA 的移动平均成本价为 USD 11.20，并且，仓库 GW 和批处理 BBB 的移动平均成本价为 USD 15.00。




