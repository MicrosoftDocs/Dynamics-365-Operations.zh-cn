---
title: "为制造物料摊销固定成本"
description: "制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75c0f5bcff0aae63aa8c7dae9b0767f8c7e6a81c
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>为制造物料摊销固定成本

[!include [banner](../includes/banner.md)]

制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。 

成本计算批次规模的概念用于在制造物料的计算成本中摊销这些固定成本。 此概念具有若干同义词，其中之一是会计批次规模。 摊销固定成本的概念也具有若干同义词，其中之一是成比例固定成本。

制造物料的成本计算批次规模数量用于物料清单 (BOM) 计算中。 该数量取决于您是如何启动和执行物料清单计算的，如下所示：

-   物料的物料清单计算中的默认计算数量 − 该物料的标准订单数量（用于库存）充当成本计算批次规模，但该默认值可以是更高的数量，以便反映该物料的订单数量倍数。 可以在该物料的默认订单设置或特定于站点的订单设置内定义其标准订单数量和倍数。
-   物料的物料清单计算中的指定计算数量 − 该指定的计算数量充当物料的成本计算批次规模。 该计算数量最初使用该物料的标准订单数量，但默认值可被手动覆盖。 指定的计算数量为指定的物料和具有生产的一种物料清单行类型的制造组件显示成本计算批次规模。 原因在于，假定精确数量生产制造组件。 具有物料的物料清单行类型的其他制造组件的成本计算批次规模将反映其标准订单数量。
-   物料的物料清单计算中指定的按订单生产计算数量 − 该指定的计算数量在物料清单计算使用按订单生产分解模式时充当该物料及其制造组件的成本计算批次规模。 假定按精确数量生产制造组件，就像具有生产的物料清单行类型的制造组件。
-   特定于订单的物料清单计算中的指定计算数量 − 可为销售订单、销售报价单或服务订单上的行项执行特定于订单的物料清单计算。 该指定的计算数量使用原始行项上的数量，但是可以覆盖该默认数量。 您可以选择特定于订单的物料清单计算是使用按订单生产还是多级分解模式。

制造物料的摊销固定成本的计算出的金额称作费用。






