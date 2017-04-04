---
title: "库存值对象"
description: "本文提供有关库存对象的值如何计算的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>库存值对象

本文提供有关库存对象的值如何计算的信息。 

将命名的新功能**实际数量**能让您看到特定对象库存的值。 成本对象表示执行库存盘点的实体级别。 有关成本对象的更多信息，请参阅[成本对象](cost-object.md)。 若要查看某个特定库存的值)，请单击**实际数量** **在成本对象**的页面。 这是库存对象的如何计算值：库存对象。值=成本对象。平均库存单位成本×对象。以下示例显示数量库存对象和成本的对象如何计算值。 在物料 A 上登记两个产品收据事件：

-   产品收据 1:数量= 100 台计算机。个人，金额=根据，站点= 1，=11，仓库不批次。 B1 =
-   产品收据 2:数量= 50 台计算机。个人，金额= $800.00，站点= 1，=11，仓库不批次。 =格

下表显示成本对象的计算结果。 您可以在**“成本对象”**页面上查看结果。

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

下表显示库存对象的计算结果。 您可以通过在**“成本对象”**页面上单击**“实际数量”**来查看结果。

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



<a name="see-also"></a>请参阅
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[新增功能和更改在 Microsoft Dynamics AX ISS] (-新更改的/dynamics365/operations/dev-itpro/get-started/what)


