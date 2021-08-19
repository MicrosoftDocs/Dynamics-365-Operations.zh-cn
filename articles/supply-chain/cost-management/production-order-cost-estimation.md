---
title: 生产订单成本估计
description: 本文提供有关生产成本估计的信息。 生产成本估计提供按计划的生产订单数量生产一个物料的预计材料和产能消耗成本。
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5debf62a3a0fc3ae8828473d7dd593c690e298712e5ed696077db1562796943
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724908"
---
# <a name="production-order-cost-estimation"></a>生产订单成本估计

[!include [banner](../includes/banner.md)]

本文提供有关生产成本估计的信息。 生产成本估计提供按计划的生产订单数量生产一个物料的预计材料和产能消耗成本。 

在您创建生产订单后，必须估计生产成本。 目的是估计生产流程的物料和工艺路线消耗量，因为这些预估用作后续的排产和生产流程的基础。

## <a name="production-cost-estimation"></a>生产成本估计
生产成本估计基于以下信息：

-   生产订单中的数量
-   生产物料清单 (BOM) 的组件
-   生产工艺路线中的工艺路线工序
-   应用于组件和工序的间接成本
-   截至计算日期的有效成本数据

如果生产物料清单中存在虚拟行物料，这些计算反映虚拟的组件和工艺路线工序。 您可以使用估计任务重新计算估计成本，以便它们反映更新的信息。 例如，更新后的信息可以更改为生产订单数量、生产物料清单中的组件、生产工艺路线中的工艺路线工序、适用于这些组件和工序的间接成本或者截至重新计算日期的有效成本数据中的变化。 计算估计成本还基于成本加上加价方法为生产物流建议销售价格。 估计成本计算可选择是否应用于参考订单，参考订单反映链接到该生产订单的其他生产订单。

## <a name="view-the-estimated-costs"></a>查看估计成本
在运行估计后，您可以查看 **价格计算** 页上的结果。 估计将计算以下值：

-   **生产成本** – 生产成本是估计的顶行。 它显示执行生产订单的整个成本以及生产的总销售价。 它是预估上的所有成本行之和。
-   **工艺路线或资源成本** – 工艺路线或资源成本是生产工序的成本。 它们包括诸如设置时间、运行时间和开销等元素成本。
-   **材料成本** – 材料成本是需要用于生产物料的物料清单组件的成本和价格。 这些成本以前已确立并输入到系统中。

## <a name="other-uses-of-cost-estimation"></a>成本估计的其他用途
成本估计还提供以下信息：

-   有意义的报价单
-   订单利润的估计
-   原材料使用的估计
-   来自以前生产的成本信息的比较
-   预算和预测信息
-   维持特定成本所需的生产规模的估计






[!INCLUDE[footer-include](../../includes/footer-banner.md)]