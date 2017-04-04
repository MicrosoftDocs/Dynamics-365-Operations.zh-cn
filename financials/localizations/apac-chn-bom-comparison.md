---
title: "针对中国的比较物料清单"
description: "此主题提供有关针对中国比较物料清单的信息。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 268584
ms.assetid: e399ab34-4bfa-4b6d-a956-d425c1395ea3
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 94932de5b8074134d5d2dfe06abaaa1a554d1611
ms.lasthandoff: 03/31/2017


---

# <a name="bill-of-materials-comparison-for-china"></a>针对中国的比较物料清单

此主题提供有关针对中国比较物料清单的信息。

因为许多产品将重新设计或修改满足需求，更改产品可由其物料清单 (BOM) 中伴随若干版本在其生命周期中。 除了直接和间接成本。创建最终产品，一般来说，物料清单的成本反映实际成本和来自使用的组件和材料，派生。 物料清单的价格可以手动分配，或者它可以通过标记产品在计算的制造时或构造的已发生成本。 **使用物料清比较**比较页面组件数量和库存成本或组件的最新采购价，在不同物料清单版本中。 物料清单还比较可以执行以下任务：

-   创建现有的产品创建新的物料清，并基于新的物料清早期版本。
-   在一组相似的产品中比较并显示组件的差异。
-   回答有关产品差异和使用的客户查询。
-   在工业和制造环境中维护准确的库存记录。
-   将准确运营和个人记录精确，并且维护数据。
-   快速响应以更改生产级别和要求。
-   控制库存水平。
-   标识和缩小过时部件库存。
-   降低总体的制造成本。
-   提高设计和构造流程。
-   通过自定义客户要求设计和流程与预算在不同级别。
-   生成基于实际经验的概念评估询价或客户。

## <a name="example"></a>示例
下表显示如何完成物料清单进行比较。 在此示例中 FG001、产品和 FG003，每种具有有效物料清单和 FG002 产品，有两个有效物料清单，比较。 报告列出物料清单版本、显示组件数量。的相应单位和显示的每一构成库存成本或最新采购价。

| 产品 | 物料清单     | 站点   | 组件 | 已 | 单位 | 成本      |
|---------|---------|--------|------------|----------|------|-----------|
| FG001   | FG001V1 |        | MT001      | 2        | 时间单位  | USD 20.00 |
|         |         |        | MT002      | 3        | 厘米   | USD 10.00 |
|         |         |        | MT005      | 3        | 千克   | USD 32.00 |
| FG002   | FG002V1 |        | MT001      | 1        | 时间单位  | USD 50.00 |
|         |         |        | MT003      | 1        | 时间单位  | USD 12.00 |
|         |         |        | MT005      | 1        | 千克   | USD 10.00 |
|         | FG002V2 | 站点 1 | MT002      | 3        | 厘米   | USD 30.00 |
|         |         |        | MT004      | 2        | “盒”  | USD 32.00 |
|         |         |        | MT005      | 1        | 千克   | USD 10.00 |
| FG003   | FG003V1 |        | MT003      | 4        | 时间单位  | USD 30.00 |
|         |         |        | MT004      | 2        | “盒”  | USD 23.00 |
|         |         |        | MT005      | 3        | 千克   | USD 18.00 |




