---
title: "库存日记帐"
description: "本文介绍如何使用库存日记帐过帐实际库存交易记录的不同类型。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 968bf9a243d0c0cc9f0dfec474cb207ca32f9eeb
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-journals"></a>库存日记帐

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


本文介绍如何使用库存日记帐过帐实际库存交易记录的不同类型。

Microsoft Dynamics 365 for Finance and Operations 中的库存日记帐用于过帐多种类型的实际库存交易记录，如发货和收货的过帐、库存变动、物料清单的创建，以及实际库存的对帐。 所有这些库存日记帐以相同的方式被使用，不过，它们划分为不同类型。

## <a name="types-of-inventory-journals"></a>库存日记帐的类型
提供以下库存日记帐类型：

-   移动
-   库存调整
-   转移
-   物料清单
-   物料到达
-   生产输入
-   正在盘点
-   标签盘点

### <a name="movement"></a>移动

当您使用一个库存变动日记帐时，您可以在添加库存时向物料中添加成本，不过，您必须通过在创建日记帐时指定总帐对方科目，手动将附加成本分配给特定的总帐科目。 如果您想要将物料支出分配给不同部门，或者，如果要针对支出用途从库存中删除物料，则此库存日记帐类型很有用。

### <a name="inventory-adjustment"></a>库存调整

当您使用库存调整日记帐时，您可以在添加库存时向物料中添加成本。 附加成本将基于物料组过帐模板的设置，自动过帐到特定总帐科目。 在物料应保留其值默认总帐对方科目时，使用此库存日记帐类型将收益和损失更新到库存数量。 在过帐库存调整日记帐时，将过帐库存收货或发货、更改库存值，并创建分录。

### <a name="transfer"></a>转移

您可以使用转移日记帐在库存位置、批次或产品变型之间转移物料而不关联任何成本影响。 例如，您可以将物料在同一公司内从一个仓库转移到另一个仓库。 在您使用转移日记帐时，必须指定“从”和“到”库存维度（例如，对于站点和仓库）。 已定义库存维度的现有库存量相应更改。 库存转移反映物料的即时移动。 中转库存不被跟踪。 如果必须跟踪中转库存，则应使用转移单。 在过帐转移日记帐时，将为每个日记帐行创建两个库存交易记录：

-   “从”位置的库存发货
-   “到”位置的库存收货

### <a name="bom"></a>物料清单

当您将物料清单报告为已完工入库时，可以创建物料清单日记帐。 通过使用物料清单日志，您可以直接过帐物料清单。 此过帐生成产品的的库存收货，以及关联的物料清单以及物料清单中包括的产品的库存发货。 此库存日记帐类型在不需要工艺路线的简单或大量生产方案中十分有用。

### <a name="item-arrival"></a>物料到达

您可以使用物料到达日记帐登记物料收货（例如，从采购订单）。 可以从**“到达概览”**页上创建到达日记帐，作为到达管理的一部分，也可以手动从**“物料到达”**页创建日记帐条目。 如果您启用物料到达日志名称检查领料库位，Finance and Operations 会查找接收物料的库位，如果存在空间，则会为新进物料生成库位目标。

### <a name="production-input"></a>生产输入

生产输入日记帐的工作方式类似于物料到达日记帐，但用于生产订单。

### <a name="counting"></a>正在盘点

盘点日记帐能让您纠正为物料或物料组登记的现有库存量，然后过帐实际盘点，因此，您可以进行为对帐差异而需要的调整。 您可以将盘点策略与盘点组关联，以帮助对具有多种特征的物料进行分组，因此，这些物料可以包括到盘点日记帐中。 例如，您可以设置盘点组以盘点具有特定频率的物料，或在存货下跌到特定级别时盘点物料。 有关如何定义盘点组的信息，请参阅[定义库存盘点流程（任务指南）](tasks/define-inventory-counting-processes.md)。

### <a name="tag-counting"></a>标签盘点

标签盘点日记帐用于将带编号的标签分配给盘点批次。 标记应包含标记编号、物料编号和物料数量。 为了帮助确保标记只使用一次，并且所有标记都被使用，每个物料编号应该有唯一的一组标记，其具有自己的编号规则。 可以为每个标记设置三种状态值：

-   **已使用** – 为此标签计数物料编号。
-   **已失效** – 为此标签使物料编号失效。
-   **缺失** – 此标签缺失物料编号。

过帐标签盘点日记帐时，基于标签盘点日记帐行创建新的盘点日记帐。 有关标签盘点的详细信息，请参阅[库存标签盘点](inventory-tag-counting.md)。

## <a name="working-with-journals"></a>使用日志
一个用户一次只能访问一个日志。 如果若干用户必须同时访问日记帐创建日记帐行，则该用户必须选择当前不用于避免覆盖信息。 在多个部门使用同一日记帐类型的情况下，创建多个日记帐名称（例如，每个部门一个）很有用。 它还可用于划分日记帐，以便每个过帐例程都输入到它自己的唯一库存日记帐中。 对于与库存交易记录相关联的过帐例程，为期间库存调整创建一个日志，为库存盘点创建另一个日志。

## <a name="posting-journal-lines"></a>记帐日志行
您可以在任何时间过帐您创建的日记帐行，直到您锁定了来自附加交易记录的物料。 在日记帐中输入的数据保留在该日记帐中，即使您关闭该日记帐而不过帐这些行。

