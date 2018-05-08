---
title: "直接交货"
description: "本文提供有关直接交运的信息。 直接交运是直接从供应商发送到您的客户的交货。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1f2cdae674dc88a4d533258e24b1ecf7ec4cf55b
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="direct-deliveries"></a>直接交货

[!include [banner](../includes/banner.md)]

本文提供有关直接交运的信息。 直接交运是直接从供应商发送到您的客户的交货。

直接交运节省交货时间并减少与存储库存关联的成本，因为您直接向客户发运，无需在您的仓库中存储产品。  

您可以从**销售订单**页创建直接交运。 首先，创建销售订单和订单行。 然后在操作窗格上，在**销售订单**选项卡，选择**直接交运**。 最后，指定必须处理为直接交运的行。 现在即在直接交运销售订单行及其相应的采购订单行之间创建了一个链接。  

**注意：**如果订购数量的一部分已交货，则必须拆分剩余数量。 创建必须直接交运的数量新行，从原始行的数量中减去此数量。 例如，如果原始数量为 15，而发货的数量为 5，则必须为剩余数量 10 创建新行，然后根据此数额减少原始数量。  

在您在销售订单行和采购订单行之间创建直接交运链接后，可以通过使用装箱单更新销售订单。 从采购订单运行装箱单更新或发票更新。 您必须从**销售订单**页更新销售订单发票。 更新发票不会造成销售订单的数量超过登记为已接收的数量。 例如，销售订单行都有 10 件，不过通过装箱单只从销售订单行更新 5 件。 如果选择**列表**中的**全部**，当您对销售订单进行发票更新时，使用装箱单，因此，只有已实际接收的物料更新发票。 不会更新整个销售订单行。

## <a name="delivery-date"></a>交货日期
在您更新销售订单行上的**要求接收日期**字段时，也更新相应采购订单行上的**交货日期**字段。 相似地，在您更新采购订单行上的**已确认**字段时，也更新相应销售订单行上的**已确认的接收日期**和**已确认的装运日期**字段。

## <a name="delivery-address"></a>交货地址
通常情况下，采购订单的交货地址是公司的地址。 但是，在您创建直接交运时，输入客户的地址将作为交货地址。 如果您为**直接交运**交货类型的采购订单行更改交货地址，则也更新相应销售订单行的交货地址。 与此相似，如果您更改销售订单行上的交货地址，则也会更新采购订单行上的交货地址。

## <a name="deleting-order-lines"></a>删除订单行
如果您尝试删除交货类型为**直接交运**的某一销售订单行，消息框指出多个采购订单行已附加到该行。 如果该销售订单行已部分交货，则您不能删除该销售订单行或其附加的采购订单行。

## <a name="warehouse"></a>仓库
在您创建直接交运时，销售的物料永远不会实际到达您的仓库。 不过，您仍必须在销售订单行指定仓库。 相似地，领料要求可能在物料的物料模型组中指定。 但是，由于物料永远不会实际到达您的仓库，在销售订单为直接交运时，会忽略这些需求。




