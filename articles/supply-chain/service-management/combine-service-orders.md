---
title: 合并服务订单
description: 可以合并服务订单。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676766"
---
# <a name="combine-service-orders"></a>合并服务订单   

[!include [banner](../includes/banner.md)]


当您在 **服务协议** 窗体中自动创建服务订单行时，您可以选择以下选项之一以指定您如何对它们进行分组：

  - **按服务协议**

  - **按服务任务**

  - **按员工**

  - **按服务对象**

## <a name="example"></a>示例

您创建了开始日期为 2007 年 3 月 31 日的服务协议。 在 **合并服务订单** 字段中，指定 **按服务对象**。 然后您创建了以下服务协议行：

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>协议行号</p></th>
<th><p>交易记录类型</p></th>
<th><p>说明</p></th>
<th><p>间期</p></th>
<th><p>服务对象</p></th>
<th><p>入职日期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>工时</strong></p></td>
<td><p>SAL1</p></td>
<td><p>每周</p></td>
<td><p>X-1</p></td>
<td><p>2007 年 4 月 1 日</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>工时</strong></p></td>
<td><p>SAL2</p></td>
<td><p>每两周</p></td>
<td><p>X-2</p></td>
<td><p>2007 年 4 月 1 日</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>工时</strong></p></td>
<td><p>SAL3</p></td>
<td><p>每周</p></td>
<td><p>X-2</p></td>
<td><p>2007 年 4 月 1 日</p></td>
</tr>
</tbody>
</table>


您未指定任何服务协议行的时间范围。 因此，服务订单行将不从它们所在的计算日移动。

接着，您从 **创建服务订单** 窗体生成了从 2007 年 4 月 1 日到 2007 年 4 月 30 日的服务订单行。

总共创建了 10 个服务订单。 因为您选择的组合设置为 **按服务对象**，创建的所有服务订单将只包含具有一个特定服务对象的服务订单行。 从该服务协议生成并具有相同服务日期和对象的服务订单行被组合为同一个服务订单。


> [!NOTE]
> <P>在此示例中，在<STRONG>服务管理参数</STRONG>窗体中指定的日历没有休息日。</P>



可以根据您在服务协议行上指定的任意时间范围将服务订单行的附加组合为服务订单。

## <a name="see-also"></a>请参阅

[自动创建服务订单](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]