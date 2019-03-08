---
title: 生产订单成本分析
description: 本文提供有关可为已完成和当前生产订单执行的成本分析的信息。 您可以使用价格计算页或成本预估和成本计算报表分析估计成本和实际成本。 您可以查看有关每个组件物料的估计和实际成本（和数量）、工艺路线工序以及间接成本的信息。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f027d6521d5f57a7e2d2cac1bed8dc08ae9f20f1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "353555"
---
# <a name="production-order-cost-analysis"></a>生产订单成本分析

[!include [banner](../includes/banner.md)]

本文提供有关可为已完成和当前生产订单执行的成本分析的信息。 您可以使用价格计算页或成本预估和成本计算报表分析估计成本和实际成本。 您可以查看有关每个组件物料的估计和实际成本（和数量）、工艺路线工序以及间接成本的信息。

生产订单的实际成本基于报告的物料消耗量和工艺路线工序。 您可以访问有关**生产过帐**页中生产订单的报告的物料消耗量、工艺路线工序和间接成本的详细交易记录。

## <a name="variance-analysis-for-a-completed-production-order"></a>已完成生产订单的差异分析
差异反映生产物料的报告的生产活动和标准成本的计算之间的比较。 该差异不反映与生产订单的估计成本的比较。 报告的生产活动包含物料消耗量和工艺路线工序，以及关联的直接成本和报告完成的数量。 计算差异的以下四种类型：

-   批次规模差异
-   生产数量差异
-   生产价差异
-   生产替代差异

在该生产订单结束时，下图为物料的成本记录内生成订单的实际成本和计算的成本之间的差异显示帐户的四个差异。 

![计入已完成生产订单差异的差异](./media/control.jpg) 

可以通过使用**差异**页或**生产差异**报表分析生产差异。 使用显示选项卡按物料和运营资源，或按成本组查看详细差异。 库存参数中的成本细分策略确定是否按成本组跟踪差异。 您还可以使用**单个**、**多个**和**总计**显示选项查看汇总的差异。 有关详细差异的信息可以帮助您理解每个差异的来源。 为了在结束生产订单前预测差异，应分析在**成本预估和成本计算**报表中提供的详细信息。

## <a name="cost-analysis-for-current-production-orders"></a>当前生产订单的成本分析
单独的报表提供与各个交易记录类型有关的信息。 使用这些报表可以分析报告的生产活动的成本。 只为状态为**已开始**或**完工入库**的当前生产订单显示信息。

-   **在途原材料** − 该报表列出根据截至指定交易记录日期的当前生产订单报告的领料单交易记录。 该报表指示发货的组件的数量以及各个交易记录的成本额。 为单个组件物料使用选择条件。 例如，您可以根据适用生产订单打印与组件的发货数量有关的信息。 发货数量不按照父物料的完工入库数量进行更新。 因此，进行中的原材料的实际数量可能会被高估。
-   **在制品** − 该报表列出根据截至指定交易记录日期的当前生产订单报告的工艺路线交易记录（或作业）。 该报表指示为每个交易记录报告的工时、金额和数量（完好数量和残次数量）。 它还包括诸如工序编号、工序 ID 和工序资源等信息。 而且，该报表还根据生产订单显示所有交易记录的总时间和金额，以及完工入库数量。
-   **未入帐间接成本** − 该报表针对生产订单列出了已发生的间接成本。 此数据是基于工艺路线工序的已报告消耗和截止指定交易记录日期的组件。 该报表指示间接成本的类型（附加费或费用）、间接成本的成本计算单代码和每个交易记录的成本额。 该报表不提供有关导致间接成本的工艺卡或领料单交易记录的信息。
-   **进行中的生产的成本计算** − 该报表针对截至指定交易记录日期的生产订单，列出组合的物料消耗量、工艺路线工序和间接成本。
-   **在制的成品** − 该报表列出截至指定的交易记录日期的当前生产订单和完工入库交易记录。


<a name="additional-resources"></a>其他资源
--------

[生产差异的常见来源](common-sources-of-production-variances.md)



