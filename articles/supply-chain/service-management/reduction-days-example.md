---
title: 缩减天数示例
description: 缩减天数示例。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e588273244c88ffa208e88b66800dc7ce20d68
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674804"
---
# <a name="reduction-days-example"></a>缩减天数示例

[!include [banner](../includes/banner.md)]

您已经为客户的维护预订创建了预订交易记录，如下表中所述。

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>开始日期</p></th>
<th><p>结束日期</p></th>
<th><p>预订</p></th>
<th><p>预订类型</p></th>
<th><p>项目</p></th>
<th><p>类别</p></th>
<th><p>销售币种</p></th>
<th><p>销售价</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011 年 3 月 1 日</p></td>
<td><p>2011 年 3 月 31 日</p></td>
<td><p>NR-2</p></td>
<td><p><strong>常规</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>欧元</p></td>
<td><p>200.00</p></td>
</tr>
</tbody>
</table>

客户报告不需要两天（3 月 10 日和 3 月 11 日）的服务覆盖范围。 您同意缩减这两天的预订。

您如下表中所述，创建类型为 **缩减天数** 的新交易记录。

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>开始日期</p></th>
<th><p>结束日期</p></th>
<th><p>预订</p></th>
<th><p>预订类型</p></th>
<th><p>项目</p></th>
<th><p>类别</p></th>
<th><p>销售币种</p></th>
<th><p>销售价</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011 年 3 月 10 日</p></td>
<td><p>2011 年 3 月 11 日</p></td>
<td><p>NR-2</p></td>
<td><p><strong>缩减天数</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>欧元</p></td>
<td><p>-12.90</p></td>
</tr>
</tbody>
</table>

在给 2011 年 3 月的交易记录开票时，EUR 200 的销售价将减少 EUR 12.90。 因此，预测交易记录的应计费金额是 EUR 187.10，并且按 EUR 187.10 的合计对这两个交易记录开票。

## <a name="see-also"></a>请参阅

[缩减预订费用天数](reduce-the-days-on-subscription-fees.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]