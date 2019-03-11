---
title: 库存对象值
description: 本文提供有关库存对象的值如何计算的信息。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "319124"
---
# <a name="inventory-object-values"></a>库存对象值

[!include [banner](../includes/banner.md)]

本文提供有关库存对象的值如何计算的信息。 

利用名为**实际数量**的新功能，可以查看特定库存对象的值。 

成本对象表示执行库存盘点的实体级别。 有关成本对象的更多信息，请参阅[成本对象](cost-object.md)。 

要查看特定库存对象的值，请在**成本对象**页面上单击**实际数量**。 以下是如何计算库存对象的值： 

Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity 

以下示例显示如何计算库存对象和成本对象的值。 在物料 A 上登记两个产品收据事件：

-   产品收据 1：数量 = 100 pcs.，金额 = $1,000.00，站点 = 1，仓库 =11，批号 = = B1
-   产品收据 2：数量 = 50 pcs.，金额 = $800.00，站点 = 1，仓库 =11，批号 = B2

下表显示成本对象的计算结果。 您可以在**成本对象**页面上查看结果。

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>对象类型</th>
<th>物料编号</th>
<th>站点</th>
<th>数量</th>
<th>库存单位</th>
<th>值</th>
<th>平均单位成本</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>成本对象</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>时间单位</td>
<td><p>$1800.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>

下表显示库存对象的计算结果。 您可以通过在**成本对象**页面上单击**实际数量**来查看结果。

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>对象类型</th>
<th>物料编号</th>
<th>站点</th>
<th>仓库</th>
<th>批号</th>
<th>数量</th>
<th>库存单位</th>
<th>值</th>
<th>平均单位成本</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>库存对象</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>时间单位</td>
<td><p>$1200.00</p></td>
<td><p>$12.00</p></td>
</tr>
<tr class="even">
<td>库存对象</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>时间单位</td>
<td><p>$600.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>其他资源
--------

[成本对象](cost-object.md)

[成本条目](cost-entries.md)

[新增功能和更改的功能](../../fin-and-ops/get-started/whats-new-changed.md)



