---
title: 中国的物料清单比较
description: 本主题提供了有关中国的物料清单比较的信息。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBOMComparison_CN
audience: Application User
ms.reviewer: kfend
ms.custom: 268584
ms.assetid: e399ab34-4bfa-4b6d-a956-d425c1395ea3
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c9c7d4ff228a4c5326f6181e5c3655b39a55e81576f257b225f1d3f0526f5c6e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717459"
---
# <a name="bill-of-materials-comparison-for-china"></a>中国的物料清单比较

[!include [banner](../includes/banner.md)]

本主题提供了有关中国的物料清单比较的信息。

产品可以通过其物料清单 (BOM) 的多个版本伴随超过其生命周期的过程，因为许多产品要重新设计或修改到满足不断变化的需求。 一般来说，物料清单的成本通常反映生产的实际成本并用于组件和材料中的派生，以及直接和间接的创建最终产品的成本。 物料清单的价格可以手动分配，或者通过累计产品的制造或构造期间产生的成本计算。 使用 **物料清单比较** 可以比较组件数量和库存成本或不同物料清单版本之间的组件的最新采购价。 还可以通过物料清单比较执行以下任务：

-   为现有产品创建新的物料清单，并将早期版本作为这个新物料清单的基础。
-   在一组相似的产品中比较并显示组件的差异。
-   回答有关产品差异和使用的客户查询。
-   在工业和制造环境中维护准确的库存记录。
-   维护准确的运营和个人记录以及精确数据。
-   快速响应以更改生产级别和要求。
-   控制库存水平。
-   标识和减少过时部分的库存。
-   降低总体的制造成本。
-   提高设计和构造流程。
-   通过自定义和不同预算级别的流程来满足客户的需求。
-   基于实际经验生成概念估计或客户询价。

## <a name="example"></a>示例
下表显示如何完成物料清单比较。 在此示例中，产品 FG001 和 FG003，每个都具有一个有效的物料清单与有两个有效物料清单的产品 FG002 进行比较。 该报告列出物料清单版本中的每个组件，显示相应单位中的组件数量，并显示库存成本或最新采购价。

| 产品 | 物料清单     | 站点   | 组件 | 已 | 单位 | 成本      |
|---------|---------|--------|------------|----------|------|-----------|
| FG001   | FG001V1 |        | MT001      | 2        | 时间单位  | 20.00 美元 |
|         |         |        | MT002      | 3        | 厘米   | 10.00 美元 |
|         |         |        | MT005      | 3        | 千克   | 32.00 美元 |
| FG002   | FG002V1 |        | MT001      | 1        | 时间单位  | 50.00 美元 |
|         |         |        | MT003      | 1        | 时间单位  | 12.00 美元 |
|         |         |        | MT005      | 1        | 千克   | 10.00 美元 |
|         | FG002V2 | 站点 1 | MT002      | 3        | 厘米   | 30.00 美元 |
|         |         |        | MT004      | 2        | “盒”  | 32.00 美元 |
|         |         |        | MT005      | 1        | 千克   | 10.00 美元 |
| FG003   | FG003V1 |        | MT003      | 4        | 时间单位  | 30.00 美元 |
|         |         |        | MT004      | 2        | “盒”  | 23.00 美元 |
|         |         |        | MT005      | 3        | 千克   | 18.00 美元 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]