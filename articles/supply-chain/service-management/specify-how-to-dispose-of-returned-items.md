---
title: 指定如何处置退回物料
description: 指定如何处置退回物料。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61bff50d55ed4c251918a327f2a033369e731bf0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242365"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>指定如何处置退回物料 

[!include [banner](../includes/banner.md)]


在您处理退货单时，必须指定一个退货原因代码来标识产品被退回的原因。 您还必须指定一个处置代码和处置操作代码来确定该如何处理被退回的产品。

在以下情况下应用处置代码：创建退货单时，登记物料到达或对物料到达执行装箱单更新时，以及结束某一检验单时。

您可以定义为支持业务流程所需的任何处置代码。 下表提供可分配给退回物料处置的一组常用的代码。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>处置类型</p></th>
<th><p>常用代码</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>处置</p></td>
<td><p>SC</p></td>
<td><p>报废/销毁</p></td>
</tr>
<tr class="even">
<td><p>处置</p></td>
<td><p>DC</p></td>
<td><p>捐赠给慈善机构</p></td>
</tr>
<tr class="odd">
<td><p>处置</p></td>
<td><p>TD</p></td>
<td><p>第三方处置</p></td>
</tr>
<tr class="even">
<td><p>处置</p></td>
<td><p>SL</p></td>
<td><p>废物处理</p></td>
</tr>
<tr class="odd">
<td><p>处置</p></td>
<td><p>TS</p></td>
<td><p>第三方销售（二级市场）</p></td>
</tr>
<tr class="even">
<td><p>维修/修改</p></td>
<td><p>RW</p></td>
<td><p>返工</p></td>
</tr>
<tr class="odd">
<td><p>维修/修改</p></td>
<td><p>RF</p></td>
<td><p>再制造/翻新</p></td>
</tr>
<tr class="even">
<td><p>维修/修改</p></td>
<td><p>MD</p></td>
<td><p>修改</p></td>
</tr>
<tr class="odd">
<td><p>维修/修改</p></td>
<td><p>RP</p></td>
<td><p>维修</p></td>
</tr>
<tr class="even">
<td><p>维修/修改</p></td>
<td><p>RV</p></td>
<td><p>退回给供应商</p></td>
</tr>
<tr class="odd">
<td><p>其他</p></td>
<td><p>AI</p></td>
<td><p>按原样使用</p></td>
</tr>
<tr class="even">
<td><p>其他</p></td>
<td><p>RS</p></td>
<td><p>转卖</p></td>
</tr>
<tr class="odd">
<td><p>其他</p></td>
<td><p>EX</p></td>
<td><p>交换</p></td>
</tr>
<tr class="even">
<td><p>其他</p></td>
<td><p>毫秒</p></td>
<td><p>杂项</p></td>
</tr>
</tbody>
</table>


对于您定义的每个处置代码，您必须选择一个处置操作。 处置行为决定处置代码的实际和财务影响。 例如，处置代码确定了被退回物品的实际处理方法，被退回物品所产生的财务影响，以及是否必须将更换物品发送给客户。 您可以根据业务需要定义数目不限的处置代码，但是仅六个预定义的处置操作可供选择。 下表介绍的是处置操作及其定义。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>处置操作</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>贷记</strong></p></td>
<td><p>将物品归入库存并贷记客户。</p></td>
</tr>
<tr class="even">
<td><p><strong>只贷记</strong></p></td>
<td><p>贷记客户，不要求或期待客户退回物品。</p></td>
</tr>
<tr class="odd">
<td><p><strong>报废</strong></p></td>
<td><p>报废物品并贷记客户。</p></td>
</tr>
<tr class="even">
<td><p><strong>更换并贷记</strong></p></td>
<td><p>将物品退回库存，创建更换单并贷记客户。</p></td>
</tr>
<tr class="odd">
<td><p><strong>更换并报废</strong></p></td>
<td><p>报废物品，创建更换单，并且贷记客户。</p></td>
</tr>
<tr class="even">
<td><p><strong>返还客户</strong></p></td>
<td><p>拒绝所退回的物品，并将它退给客户。</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>为检验单选择处置代码

1.  单击 **库存管理** \> **定期** \> **质量管理** \> **检验单**。

2.  对于现有检验单，请从 **概述** 选项卡上的 **处置代码** 字段中选择某一操作。



## <a name="see-also"></a>请参阅

[检验单（窗体）](https://technet.microsoft.com/library/aa554073(v=ax.60))

[处置代码（窗体）](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]