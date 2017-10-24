---
title: "供应商发票日记帐和发票审核日记帐的默认对方科目"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>供应商发票日记帐和发票审核日记帐的默认对方科目

[!include[banner](../includes/banner.md)]




在以下供应商发票日记帐页中使用默认的对方帐户：

-   发票日记帐
-   发票审核日记帐

使用下表帮助您决定应为发票日记帐分配的默认科目。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>在此设置默认帐户</th>
<th>在此提供默认帐户</th>
<th>此选项如何影响处理</th>
<th>您应该在何时使用此选项</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>供应商组</strong> – 在<strong>默认帐户设置</strong>页上为供应商组设置默认对方科目，此页可以从<strong>供应商组</strong>页打开。</td>
<td><ul>
<li>供应商帐户</li>
<li>没有为供应商帐户指定默认帐户情况下的供应商组中的供应商帐户的日记帐条目</li>
</ul></td>
<td>供应商组的默认对方科目在<strong>默认帐户设置</strong>页上显示为供应商的默认对方科目。 您可以从列表页<strong>所有供应商</strong>打开此页。</td>
<td>如果随着时间的推移，您通常为同一供应商组的同类物品付款，则使用此选项。</td>
</tr>
<tr class="even">
<td><strong>供应商帐户</strong> – 在<strong>默认帐户设置</strong>页上为供应商帐户设置默认帐户，此页可以从<strong>供应商</strong>页打开。</td>
<td>供应商帐户的日记帐条目</td>
<td>供应商帐户的默认对方科目显示为供应商帐户的日记帐条目的默认抵销帐户。</td>
<td>如果随着时间的推移，您通常为同一供应商的同类物品付款，则使用此选项。</td>
</tr>
<tr class="odd">
<td><strong>日记帐名称</strong> – 在<strong>日记帐名称</strong>页设置日记帐的默认对方科目。 选择<strong>固定对方科目</strong>选项。 请注意，如果日记帐名称的日记帐类型为<strong>发票登记簿</strong>或<strong>审核</strong>，您则不能在日记帐名称指定默认对方科目。</td>
<td><ul>
<li>使用日记帐名称的日记帐标题</li>
<li>使用日记帐名称的日记帐中的日记帐条目</li>
</ul></td>
<td>如果选择<strong>日记帐名称</strong>页中的<strong>固定对方科目</strong>选项，则供应商或供应商组的默认对方科目被日记帐名称的对方科目覆盖。</td>
<td>使用此选项为计入到特定帐户的特定成本和费用设置日记帐，无论供应商属于哪个供应商或供应商组。</td>
</tr>
<tr class="even">
<td><strong>日记帐名称</strong> – 在<strong>日记帐名称</strong>页设置日记帐的默认对方科目。 清除<strong>固定对方科目</strong>选项。 请注意，如果日记帐名称的日记帐类型为<strong>发票登记簿</strong>或<strong>审核</strong>，您则不能在日记帐名称指定默认对方科目。</td>
<td><ul>
<li>日记帐标题</li>
<li>使用日记帐名称的日记帐中的日记帐条目</li>
</ul></td>
<td>在日记帐标题页中使用这些默认条目，日记帐标题页中的对方科目在日记帐凭证页中用作默认条目。 只要默认科目不是为供应商帐户设置的，就使用<strong>日记帐名称</strong>页中的默认科目。</td>
<td>当未分配默认的供应商对方科目时，使用此选项设置所使用的默认科目。</td>
</tr>
<tr class="odd">
<td><strong>日记帐标题</strong> – 在日记帐凭证页中为日记帐设置默认对方科目用作默认条目。 请注意，如果日记帐名称的日记帐类型为<strong>发票登记簿</strong>或<strong>审核</strong>，您则不能在日记帐标题指定默认对方科目。</td>
<td>日记帐中的日记帐条目</td>
<td>日记帐的默认对方科目在日记帐凭证页中用作默认条目。</td>
<td>如果日记帐中的大多数条目拥有相同的对方科目，则使用此选项帮助提高输入数据的速度。</td>
</tr>
</tbody>
</table>






