---
title: 在工作分解结构模板中设置角色
description: 本主题介绍如何在工作分解结构模板中设置角色信息。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760486"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>在工作分解结构模板中设置角色

[!include [banner](../includes/banner.md)]

项目经理可以设置在创建新项目的工作分解结构 (WBS) 时可以应用的 WBS 模板。 项目经理可以在创建模板时添加角色。 使用以下过程将角色分配到 WBS 模板。 

1. 选择**项目管理与核算** > **设置** > **项目** > **工作分解结构模板**。
2. 选择所选 WBS 模板的**详细信息**。
3. 选择列表中的某一任务，然后在**角色**字段中，选择要分配给任务的角色。

## <a name="work-with-a-wbs"></a>使用 WBS

您可以创建新的 WBS，也可以从现有的 WBS 模板复制 WBS。 项目经理可以通过在 WBS 上将角色分配给新任务来轻松管理资源。 角色可以在获取资源后替换，或者在确定执行任务的确认资源后替换。 此灵活性让项目经理可以执行以下任务：

- 确定 WBS 工作包所需的资源的数量。
- 评估项目成本。
- 确定初步预算。
- 基于角色和资源估计活动持续时间。
- 基于可用项目信息制定某些项目管理计划。

附加选项已添加到 WBS 中以便更好地使用资源功能。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>选项</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>资源分配</td>
<td>在 WBS 中查看任务的分配资源、日期、工时数和预订类型。</td>
</tr>
<tr class="even">
<td>自动生成团队</td>
<td>通过使用与任务关联的角色自动添加计划资源。 Finance 通过使用基于角色的多条件决策分析来自动建议计划资源。 在 WBS 中为任务设置角色和工作量（工时）后，并且在发布结构之后，选择<strong>自动生成团队</strong>。 所需计划资源数量将添加到 WBS 和<strong>项目和团队计划编制</strong>选项卡。</td>
</tr>
<tr class="odd">
<td>资源（下拉列表）</td>
<td>在<strong>启动资源分配</strong>页上，您可以基于指定的持续时间选择要硬性预订或软性预订的资源。 您可以调整视图设置来查看和设置资源活动的持续时间。 您可以使用以下选项在工作包级别选择和分配资源：
<ul>
<li><strong>接受</strong> – 确认对分配给任务的资源的更改。</li>
<li><strong>取消</strong> – 取消对分配给任务的资源的更改。</li>
<li><strong>自动分配</strong> - 自动选择具有匹配角色的可用雇用资源并分配到所选任务。</li>
</ul></td>
</tr>
</tbody>
</table>

1. 在**所有项目**页上，选择 **XYZ 升级第 2 阶段**项目。
2. 选择**计划** > **活动** > **工作分解结构**。
3. 选择**新建**将以下一级活动添加到 WBS：

    - 启动
    - 计划
    - 正在执行
    - 监控和控制
    - 期结

4. 设置日期和工作量（工时），如以下插图所示。

    [![设置日期和工作量](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. 选择**启动**任务行，然后在**角色**字段中，选择**高级项目经理**。
6. 选择**发布**。
7. 在同一行的**资源**字段中，选择 **Daniel Goldschmidt**，然后选择**接受**。
8. 选择**计划**任务行，然后在**角色**字段中，选择**业务分析员**。
9. 选择**发布**，然后选择**自动生成团队**。
10. 在出现的消息框中选择**是**。
11. 在**资源**字段中，确认值为**业务分析员 1**。
12. 对于**业务分析员 1** 资源，打开查找，并选择**启动资源分配**。 然后为任务选择一个工作人员。
13. 选择**软性分配** &gt; **全部产能**。

    > [!NOTE] 
    > 您不会收到指定资源现在是 2 的警告，因为资源数量仍为 1。

14. 在**工作分解结构**页上，在 WBS 中验证资源分配，然后选择**保存**。
