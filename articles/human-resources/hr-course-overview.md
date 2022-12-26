---
title: 课程概述
description: 本文介绍人力资源管理员和经理如何使用课程功能来维护工作人员可以学习的课程的信息。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716330"
---
# <a name="courses-overview"></a>课程概述

Microsoft Dynamics 365 Human Resources 针对您的组织的学习需求提供解决方案。 此解决方案提供两个学习课程路径：*虚拟* 和 *讲师引导*。

*虚拟学习* 是一种通过在线资源提升的学习体验。 在 *讲师引导式培训* 中，由讲师辅助一组工作人员或学员学习培训课程。

在我们的学习模块中，人力资源专业人员、管理员、培训经理和经理可以同时创建两个学习课程路径，然后将其分配给工作人员。

> [!NOTE]
> 要使用虚拟课程，您必须在功能管理中启用 **课程增强** 功能。

## <a name="set-up-virtual-courses"></a>设置虚拟课程

要配置虚拟课程，您必须在功能管理中启用 **课程增强** 功能。 转到 **课程 \> 新建**，将 **虚拟** 选项设置为 **是**。 启用此功能后，需要有课程链接。 **课程状态** 字段将设置为 **打开**。 **允许员工自行注册** 选项将设置为 **是**，但可以设置为 **否**。

在功能管理中启用 **课程增强** 功能后，会发生以下更改：

- 必须为课程分配定义截止日期。
- 需要提供课程链接。
- **员工自助服务** 将在 **课程** 中显示员工概览。 用户可以查看已过期、即将到期和已分配的课程。
- 工作人员可以完成虚拟课程并进行自我证明。

## <a name="set-up-instructor-led-courses"></a>设置讲师引导式课程

讲师引导式课程无需在使用前进行配置。

以下信息是可选的，可以为课程指定。 如果要为课程输入这些信息，应在创建课程记录之前进行设置：

- 课程类型
- 教室组
- 课程组
- 上课地点
- 教室
- 教师
- 课程类型

您可以使用 *课程类型* 根据课程的结构或内容对课程进行分类。 您可以在 **课程类型** 页面创建课程类型。

可以为课程登记的最大和最小参与者人数在 **课程** 页面的 **常规** 快速选项卡中定义。

### <a name="course-setup-type"></a>课程设置类型 

*设置类型* 确定课程结构。 课程有三种设置类型。

| 设置类型 | Description |
|------|--------|
| 标准 | 此设置类型的课程没有每天课程安排。 新建课程时，这是默认设置类型。 |
| 日程 | 选择此设置类型将计划多天课程的每一天的详细信息。 |
| 课程安排 + 会话 | <p>为更复杂的课程选择此设置类型。 例如，您可以将课程日程分为 *轨道* 和 *会话*。</p><ul><li>*轨道* 是课程特定的主题区域。</li><li>*会话* 将轨道划分开来，并且帮助确定与轨道相关的特定流程或技巧。</li></ul> |

### <a name="course-tasks"></a>课程任务

对于每个课程，完成以下任务：

- 登记参与者。
- 指定登记截止日期。
- 定义参与者的最小和最大数目。
- 分配课程所在的地点和教室。
- 为课程参与者推荐旅馆。
- 创建课程描述，可以在 **员工自助服务** 上发布。

> [!NOTE]
> 只有当没有人登记课程时，您才可以删除它。

### <a name="course-statuses"></a>课程状态

下表列出了课程状态以及为每个状态完成的操作。

| Status | 变动 |
|------|--------|
| 创建时间 | <ul><li>输入并修改课程信息。</li><li>将课程状态更改为 **打开**，这样工作人员可以登记该课程。</li></ul> | 
| 已打开 | <ul><li>为课程登记参与者。</li><li>将参与者从课程中移除。</li><li>确认课程的参与者。</li><li>对于状态为 **已确认** 的参与者，将课程状态更改为 **已关闭** 或 **已取消**。</li></ul>|
| 已关闭 | 可以重新打开课程。 |
| 已取消 | 可以重新打开课程。 |

### <a name="course-participants"></a>课程参与者

*课程参与者* 是参加培训课程或活动的工作人员。 仅可为已打开的课程登记参与者。

### <a name="workflow"></a>工作流

通过 **员工自助服务** 页登记课程的员工可以将登记经过审批工作流。 您可以在 **课程** 页的 **常规** 快速选项卡中为课程分配工作流。