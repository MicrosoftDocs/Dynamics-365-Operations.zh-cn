---
title: 服务状态和进度字段交互
description: 在“服务订单”窗体中，标题上的“进度”字段反映整个服务订单的状态，而“状态”报告各个服务订单行的状态。
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
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677637"
---
# <a name="service-status-and-progress-field-interaction"></a>服务状态和进度字段交互

[!include [banner](../includes/banner.md)]

在 **服务订单** 窗体中，服务订单标题上的 **进度** 字段反映整个服务订单的状态，而 **状态** 报告各个服务订单行的状态。

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>进度</p></th>
<th><p>行 1 状态</p></th>
<th><p>行 2 状态</p></th>
<th><p>行 3 状态</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>进行中</strong></p></td>
<td><p><strong>已创建</strong></p></td>
<td><p><strong>已创建</strong></p></td>
<td><p><strong>已创建</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>进行中</strong></p></td>
<td><p><strong>已取消</strong></p></td>
<td><p><strong>已创建</strong></p></td>
<td><p><strong>已创建</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>进行中</strong></p></td>
<td><p><strong>已创建</strong></p></td>
<td><p><strong>已取消</strong></p></td>
<td><p><strong>已过帐</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>已取消</strong></p></td>
<td><p><strong>已取消</strong></p></td>
<td><p><strong>已取消</strong></p></td>
<td><p><strong>已取消</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>已过帐</strong></p></td>
<td><p><strong>已过帐</strong></p></td>
<td><p><strong>已过帐</strong></p></td>
<td><p><strong>已过帐</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>已过帐</strong></p></td>
<td><p><strong>已过帐</strong></p></td>
<td><p><strong>已取消</strong></p></td>
<td><p><strong>已取消</strong></p></td>
</tr>
</tbody>
</table>

如果所有行都具有 **已创建** 状态，则服务订单的进度为进行中。如果有些行具有 **已取消** 状态或 **已过帐** 状态，则其进度仍为进行中。

如果服务订单中的所有行都标记为 **已过帐**，则状态订单的进度为 **已过帐**。 如果有些行的状态为 **已过帐**，而有些行的状态为 **已取消**，则进度仍为 **已过帐**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
