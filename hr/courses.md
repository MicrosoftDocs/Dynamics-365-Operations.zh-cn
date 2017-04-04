---
title: "设置培训课程"
description: "人力资源管理员和经理可以使用课程功能维护有关为工作人员提供的培训的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: aa97950a22572fb4c934687b550c13dcc8acce0d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-training-courses"></a>设置培训课程

人力资源管理员和经理可以使用课程功能维护有关为工作人员提供的培训的信息。

 <a name="set-up-prerequisites"></a> 设置先决条件
---------------------

以下信息是必需的，而且必须在创建课程之前设置。
-   **课程类型**

以下信息是可以为课程指定的可选信息。 如果您知道您将为课程输入此信息，则应在创建课程记录之前设置此信息。
-   **教室组**
-   **课程组**
-   **上课地点**
-   **教室**
-   **教师**

## <a name="course-types"></a>课程类型
您可以使用课程类型根据课程结构或内容对课程进行分类。 您可以在“课程类型”****页上创建课程类型。 创建课程记录时，必须选择课程类型。

## <a name="course-setup-type"></a>课程设置类型
下表列出了课程的三种设置类型。 设置类型确定课程结构。

<table>
<thead>
<tr class="header">
<th>设置类型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>标准</strong></td>
<td>为没有日程安排的课程选择此类型。 新建课程时，这是默认设置类型。</td>
</tr>
<tr class="even">
<td><strong>课程安排</strong></td>
<td>选择此类型以规划多天课程的每一天的详细信息。</td>
</tr>
<tr class="odd">
<td><strong>课程安排 + 会话</strong></td>
<td>为更复杂的课程选择此类型。 例如，您可以将课程日程分为轨道和会话。
<ul>
<li>“班组”<strong></strong>– 班组是课程特定的主题区域。</li>
<li>“学期”<strong></strong>– 学期将班组划分开来，并且帮助确定与轨道相关的特定流程或技巧。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>课程任务
对于每个课程，都可以完成以下任务。
-   登记参与者
-   指定登记截止日期
-   定义参与者的最小和最大数目
-   分配课程所在的地点和教室
-   为课程参与者推荐旅馆
-   创建课程描述，然后您可以在员工自助服务上进行建议

  >**注释**可以删除课程，只有当任何人都为其登记。 
    
## <a name="course-statuses"></a>课程状态
下表列出了可能的课程状态，以及在课程具有特定状态时您可以完成的操作。

<table>
<thead>
<tr class="header">
<th>状态</th>
<th>行为</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>已创建</strong></td>
<td><ul>
<li>输入并修改课程信息。</li>
<li>将课程状态更改为“打开”<strong></strong>，这样工作人员可以登记该课程。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>打开</strong></td>
<td><ul>
<li>为课程登记参与者。</li>
<li>将参与者从课程中移除。</li>
<li>确认课程的参与者。</li>
<li>将课程状态更改为“已关闭”<strong></strong>或“已取消”<strong></strong>。</li>
<li>为状态为“已确认”<strong></strong>的参与者规划调查表。</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>已关闭</strong></td>
<td>可以重新打开课程。</td>
</tr>
<tr class="even">
<td><strong>已取消</strong></td>
<td>可以重新打开课程。</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>课程参与者
课程参与者有工作人员、申请者或参加培训课程或事件的承包商。 仅可为开放式课程登记参与者。 可以为课程登记的参与者最大和最小人数在“课程”****页上的“常规”****快速选项卡中进行了定义。

<a name="workflow"></a>工作流
--------

通过登记课程的员工** **员工自助服务页可为其登记将通过工作流以供审核。  工作流可以分配给** **的"常规"选项卡上 FastTab 一课程在课程** **页。




