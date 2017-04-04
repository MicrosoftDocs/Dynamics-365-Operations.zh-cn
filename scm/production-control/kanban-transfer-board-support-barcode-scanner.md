---
title: "转移看板条码扫描仪的板；客户都支持"
description: "看板转移面板支持从小组件条码扫描器到选择、开始、完成和清空看板作业的扫描器输入。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f393efaf011de103fc172af625816eef5915c642
ms.lasthandoff: 03/31/2017


---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>转移看板条码扫描仪的板；客户都支持

看板转移面板支持从小组件条码扫描器到选择、开始、完成和清空看板作业的扫描器输入。

<a name="registration-modes"></a>登记模式
------------------

在**扫描仪登记**快速选项卡中，您可以选择登记模式，其控制您扫描看板卡号或在“看板卡号”字段中手动输入该编号的操作。
| 设置登记模式 | 描述                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| 启动                 | 将看板转移作业登记为进行中。                                                 |
| 已完成              | 将看板转移作业登记为已完成。                                                   |
| 空                 | 将由看板卡引用的物料处理单元登记为空。              |
| 选择                | 登记看板卡号并在看板列表中自动选择引用的作业。 |

 
<a name="registration-mode-select"></a>登记模式选择
------------------------

当你使用"条码读取器选择作业时，看板面板查看的模式更改。 在此模式中，以下条件适用：

-   仅显示扫描的看板作业。
-   所选作业的详细信息显示在**详细信息**快速选项卡中。
-   **消息**快速选项卡只为所选作业显示消息。
-   您可以通过使用操作窗格上提供的功能更改作业的状态。 看板转移面板在此时间只显示单个作业。
-   您可以通过依次单击手动更新在作业列表的信息 (Shift+F5 **刷新**) 在操作窗格。 在刷新信息后，作业筛选器的完整结果再次将显示。

## <a name="job-status-and-possible-actions"></a>作业状态和可能的操作
所选作业的状态和事件看板的任何限定作业的状态确定是否可以进一步处理作业。 下表显示有关这些状态和任务的信息：
-   可用与作业或可用于作业引用的处理单元的状态。
-   您可为作业执行的每个任务。

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>作业类型</th>
<th>作业状态或处理单元状态</th>
<th>更新领料单</th>
<th>启动</th>
<th>更新登记</th>
<th>已完成</th>
<th>空</th>
<th>创建事件看板</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>转移</td>
<td><ul>
<li>未计划</li>
<li>无限定的作业或限定的作业已完成</li>
</ul></td>
<td>是</td>
<td>是</td>
<td>是</td>
<td>是</td>
<td>否</td>
<td>是</td>
</tr>
<tr class="even">
<td>转移</td>
<td><ul>
<li>未计划</li>
<li>限定的作业未完成</li>
</ul></td>
<td>是</td>
<td>否</td>
<td>是</td>
<td>否</td>
<td>否</td>
<td>否</td>
</tr>
<tr class="odd">
<td>转移</td>
<td>进行中</td>
<td>是</td>
<td>否</td>
<td>是</td>
<td>是</td>
<td>否</td>
<td>否</td>
</tr>
<tr class="even">
<td>转移</td>
<td>已完成</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>是</td>
<td>否</td>
</tr>
<tr class="odd">
<td>转换或处理</td>
<td>空</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
</tr>
<tr class="even">
<td>转换或处理</td>
<td>找不到看板卡</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
</tr>
<tr class="odd">
<td>转换或处理</td>
<td>找到看板卡，但为分配给看板。</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
</tr>
<tr class="even">
<td>处理</td>
<td><ul>
<li>未计划</li>
<li>已准备</li>
<li>进行中</li>
</ul></td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
</tr>
<tr class="odd">
<td>处理</td>
<td>已完成</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
<td>否</td>
</tr>
</tbody>
</table>




