---
title: 设置培训课程
description: 人力资源管理员和经理可以使用课程功能维护有关为工作人员提供的培训的信息。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 83f88d17c744bb53dad975b77d169a09375d20d1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "859682"
---
# <a name="set-up-training-courses"></a>设置培训课程

[!include [banner](includes/banner.md)]

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
您可以使用课程类型根据课程结构或内容对课程进行分类。 您可以在**课程类型**页上创建课程类型。 创建课程记录时，必须选择课程类型。

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
<li><strong>班组</strong>– 班组是课程特定的主题区域。</li>
<li><strong>学期</strong>– 学期将班组划分开来，并且帮助确定与轨道相关的特定流程或技巧。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>课程任务
对于每个课程，都可以完成以下任务。
- 登记参与者
- 指定登记截止日期
- 定义参与者的最小和最大数目
- 分配课程所在的地点和教室
- 为课程参与者推荐旅馆
- 创建课程描述，然后您可以在员工自助服务上进行建议

  >**注意** 只有当没有人登记课程时，您才可以删除它。 

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
<li>将课程状态更改为<strong>打开</strong>，这样工作人员可以登记该课程。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>打开</strong></td>
<td><ul>
<li>为课程登记参与者。</li>
<li>将参与者从课程中移除。</li>
<li>确认课程的参与者。</li>
<li>将课程状态更改为<strong>已关闭</strong>或<strong>已取消</strong>。</li>
<li>为状态为<strong>已确认</strong>的参与者规划调查表。</li>
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
课程参与者有工作人员、申请者或参加培训课程或事件的承包商。 仅可为开放式课程登记参与者。 可以为课程登记的参与者最大和最小人数在**课程**页上的**常规**快速选项卡中进行了定义。

<a name="workflow"></a>工作流
--------

通过**工自助服务**页登记课程的员工可以让其注册工作流传送以供审核。  工作流可以分配到**课程**页上的**常规**快速选项卡中的课程。





