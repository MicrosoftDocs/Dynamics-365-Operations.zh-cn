---
title: "项目的采购订单"
description: "本文介绍您可用于为项目创建采购订单的不同方法。 使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。"
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a>项目的采购订单

[!include [banner](../includes/banner.md)]

本文介绍您可用于为项目创建采购订单的不同方法。 使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。

在 Microsoft Dynamics 365 for Finance and Operations 中，您可以使用多种方法创建项目的采购订单。 使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。

### <a name="methods-for-creating-a-purchase-order"></a>创建采购订单的方法

您可以使用以下方法之一在“项目”管理与核算中创建一个采购订单。 采购订单的目的是确定采购订单的消耗时间，并随之确定对项目物料计费的时间。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>方法</th>
<th>用途</th>
<th>物料的消耗</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>直接从项目创建采购订单</td>
<td>使用此方法以针对项目的消耗量从外部供应商采购物料。 可以通过两种方法创建采购订单：
<ul>
<li>从项目本身出发。 在这种情况下，已经为采购订单定义项目。</li>
<li>通过导航到项目采购订单。 您必须选择要为其创建采购订单的供应商和项目。</li>
</ul></td>
<td>更新供应商发票时消耗物料。</td>
</tr>
<tr class="even">
<td>根据销售订单创建采购订单。</td>
<td>如果您从项目创建销售订单，可以使用此方法采购物料。</td>
<td>为客户的销售订单开票后消耗物料。</td>
</tr>
<tr class="odd">
<td>根据物料需求创建采购订单。</td>
<td>如果您从项目创建物料需求，可以使用此方法采购物料。</td>
<td>更新物料需求装箱单时消耗物料。</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> 更新供应商发票或装箱单时，系统将提示您根据物料需求更新该装箱单。

有关详细信息，请参阅[根据物料需求接收采购订单上的物料](tasks/receive-items-purchase-order-item-requirement.md)。


