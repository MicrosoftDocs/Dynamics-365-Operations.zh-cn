---
title: 管理生产中的转包工作
description: 本文说明如何在 Dynamics 365 Supply Chain Management 中管理已转包工序。 换言之，说明供应商如何管理分配给资源的生产工序。
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup, ProdBOMVendorListPagePreviewPane, ProdBOMVendor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0021d409f9f4a9b36effbd80a99766812572d5b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863786"
---
# <a name="manage-subcontracting-work-in-production"></a>管理生产中的转包工作

[!include [banner](../includes/banner.md)]

本文说明如何在 Dynamics 365 Supply Chain Management 中管理已转包工序。 换言之，说明供应商如何管理分配给资源的生产工序。

在[生产流程](production-process-overview.md)中，可以由供应商拥有或管理的资源完成工作。 通常，供应商资源用于平衡超过了公司自身资源可用产能的定期超额需求。 供应商还可以以较低的价格提供特定[资源产能](resource-capabilities.md)或资源。  

根据生产流程中使用的供应商资源，[工艺路线](routes-operations.md)通常有额外的物流要求，因为必须首先将物料和半成品运输到供应商的站点。 然后，必须将已转包工序的结果运输到分配给下一道工序的位置或产品仓库。  

使用了转包工序或活动时，将影响工序的所有阶段，从生产、成本计算预测、计划和安排中需要的工序的定义，到物料、半成品和产品的物流管理。 最后，这些资源还需要自己的成本核算和成本控制流程。  

对于内部资源，通常分配一个期间的固定成本率。 比较而言，已转包资源的成本基于相关服务的采购价。 服务定义为另一件产品，用于推动指定的已转包工序的采购流程。  

目前，Supply Chain Management 中没有明确的半成品概念。 对于需要多道工序以将原料转化为成品的生产订单，产品将仅在最后一道工序中过帐回库存。 早期工序生成的半成品计入在制品 (WIP)，但不在库存中过帐或跟踪。 尽管可以将工艺路线和物料清单 (BOMs) 拆分为多个小单元，此方法却会增加必须管理的产品、物料清单和工艺路线的数量。  

可通过两种方法为生产工序的转包工作建模。 这些方法的不同之处在于：为转包流程的建模方式、半成品在流程中的表示方式，以及成本的控制方式。

-   生产订单或批次订单中工艺路线工序的转包
    -   服务产品必须是贮存的产品，并且必须属于物料清单。
    -   此方法支持先进先出 (FIFO) 或标准成本。
    -   半成品在流程中表示为服务产品。
    -   成本控制将与已转包工作关联的成本分配给物料成本。
-   精益生产流中的生产流活动的转包
    -   此服务是非贮存服务产品，不属于物料清单。
    -   此方法将采购协议用作服务协议。
    -   此方法使用倒冲成本计算法。
    -   此方法允许聚合的异步采购。 （物料流独立于采购流程。）
    -   成本控制在自己的成本细分块中分配已转包工作。

## <a name="subcontracting-of-route-operations"></a>工艺路线工序的转包
若要将工艺路线工序的转包用于生产或批次订单，必须将用于采购服务的服务产品定义为 **服务** 类型的产品。 此外，还必须拥有 **库存策略** 下的 **贮存的产品** 选项设置为 **是** 的物料模型组。 此选项定义产品在产品收据上是否记为库存（**贮存的产品** = **是**），或者产品是否记为损益科目的开支（**贮存的产品** = **否**）。 尽管此行为可能貌似矛盾，却基于以下事实：只有拥有此策略的产品才将创建可在成本控制中用于计算计划成本并在生产订单结束时确定实际成本的库存交易记录。  

若要在计划和成本计算中考虑服务，必须将服务添加到物料清单。 物料清单行的类型必须为 **供应商**，并且必须分配给为其分配了服务的工艺路线工序。 此工艺路线工序必须有指向类型为 **供应商** 且将工艺和相关服务连接到相应供应商帐户的资源的成本计算资源和资源要求。  

使用此配置时，将根据生产订单的估计情况为相关服务产品创建采购订单。 服务的采购订单用作已转包工序的定位点。 可以通过生产控件中 **已转包工作** 列表页管理已转包工作。 已转包工作用于装运原料，最终将半成品装运到供应商来为工序做准备。 还用于在物料到达时接收已转包工序产生的产品，其中服务产品用于标识半成品的到达。 收到采购订单行时，将把生产工序更新为已完成。  

一个生产订单可以有多道工序，并且可以将每道工序分配给不同供应商。 因此，端到端生产订单可能触发多个采购订单。

## <a name="subcontracting-of-production-flow-activities"></a>生产流活动的转包
[lean manufacturing](lean-manufacturing-overview.md) 解决方案将转包工作建模为与[生产流](tasks/create-production-flow-version.md)活动有关的服务（任务指南一文）。 因此，这种类型的转包也称为[基于活动的转包](activity-based-subcontracting.md)。 已引入了名称为 **直接外包** 的一种特殊成本组类型，并且转包服务不属于成品的物料清单 (BOM)。 使用 lean manufacturing 时，所有活动都由可与一个或多个生产流活动关联的看板定义。 因此，该说明听起来就像生产订单的说明。 但是，虽然生产订单始终必须以产品结束，您可以创建看板来提供半成品。 无需引入新产品和物料清单级别。  

由于看板规则可能变化很大，您可以为生产流中的相同产品的不同供应变型建模。 使用 lean subcontracting 时，将把物料流和财务流严格分开。 所有物料流均由看板活动表示。 可以根据生产流中的看板作业状态，自动执行服务产品的采购订单和这些服务的收据过帐。 即使在创建采购订单之前，也可以启动和完成看板作业。 可通过期间和服务聚合转包票据（服务的采购订单和采购收据）。 因此，可以将采购票据和行的数量保持为较少，甚至在重复性极高且供应商通过一个流提供已转包服务的工序中也不例外。

### <a name="modeling-subcontracting-in-a-production-flow"></a>为生产流中的转包建模

在[精益生产流](lean-manufacturing-modeling-lean-organization.md)中，当流程活动分配给只有一个供应商资源的工作单元（资源组）时，可将该流程活动定义为已转包。 转包了工作单元时，必须将相关流程活动链接到包含服务项和服务价格的活动采购协议行。 活动的服务协议也定义看板作业的产品数量与产生的服务数量之间的计算比率。 可以选择基于作业数量、为作业报告的优质产品数量还是产品总数（此总数包含报废的产品）计算服务数量。  

也可以将转移活动定义为已转包。 为转移活动中的装运选择负责方时，明确执行此定义。 选择 **发货人** 或 **接收人** 时，如果相应源或目标仓库是供应商管理的仓库，则将活动视为已转包。 选择 **承运人** 时，始终转包活动。 与已转包流程活动一样，必须先将已转包转移活动连接到服务协议，才能激活生产流。

### <a name="backflush-costing"></a>倒冲成本计算

转包工作的成本会计已完全集成到 lean manufacturing 解决方案的成本计算（倒冲成本计算法）。 过帐了服务的采购订单收据或执行了开票时，将把服务的成本分配给生产流。 对于倒冲成本计算法，通过将所接收产品标准成本的转包块抵销实际接收和开票服务数量，计算已转包服务的差异。

## <a name="material-supply-for-subcontracted-operations"></a>已转包工序的物料供应
必须将半成品和其他相关物料转移到实际开展工作的位置。 使用已转包工序和活动时，此转移通常与到供应商运营站点的额外运输有关。 通过将物料清单中的物料分配给已转包工序，声明必须将物料暂存到所分配资源的资源组输入位置中。 然后，主计划或精细补货将物料供应给该位置。  

若要为供应商站点的库存建模，行业最佳实践是定义供应商管理的仓库。 可以通过创建新仓库和分配供应商帐户，轻松定义供应商管理的仓库。 若要记录必须在执行工序之前将物料转移到供应商，应将供应商管理的仓库分配给包含资源的资源组的输入仓库。  

若要在此仓库补充物料，可以使用多个策略。

-   转移单
-   转移日记帐
-   提领看板
-   供应商位置的直接采购

半成品是此规则的例外。 若要转移半成品，只能使用以下选项：

-   对于生产和批次订单，只能通过使用 **已转包工作** 列表页中的领料单日记帐，以逻辑方式转移半成品。 此日记帐将创建可用于把半成品和原料转移到供应商的交货通知票据。
-   对于生产流中的已转包工序，将由供应商位置的提款或生产看板的收据记录半成品的转移。 若要为显式转移活动建模，可以以额外的转移活动结束生产看板。

**注释：** 一个生产订单的生产工艺路线不能跨多个站点。 此规则也适用于已转包工作。 因此，必须在与工艺路线中所用内部资源相同的站点中定义表示供应商所管理位置的仓库。 尽管生产流可以跨站点，但不能将半成品从一个站点运输到另一个站点，因为该工序表示了成本上下文的变化。  

通常，直接将已转包资源组的输出仓库和位置分配给工艺路线或生产流中工序下一步骤的仓库和位置。 此设置有助于减少产品的作业报告量或必须建模的额外转移工序的数量。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]