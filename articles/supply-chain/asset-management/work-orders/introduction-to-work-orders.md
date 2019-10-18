---
title: 工作订单简介
description: 本主题概述资产管理中的工作订单。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875533"
---
# <a name="introduction-to-work-orders"></a>工作订单简介

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

工作订单用于管理维护作业，提供维护作业所需信息和登记维护作业的消耗。 一个工作订单中可以包含一个或多个工作订单作业，并且可以为一个工作订单关联一个或多个资产。 每个工作订单行定义为资产安排的一个维护作业。

可以自动创建工作订单，也可以手动创建：

- 对于基于日历且设置为“自动创建”的维护计划，将自动使用**安排维护计划**窗体。  

- 对于设置为“自动创建”的维护阶段，将自动使用**安排维护阶段**窗体。  

- 基于维护安排（可以是预防性作业或维护请求）创建。  

- 手动创建工作订单。  

- 在**所有维护请求**、**有效维护请求**或**我的功能位置维护请求**中创建工作订单。

>[!NOTE]
>将把与同一个资产关联的工作订单作业关联到同一个项目 ID。

## <a name="all-work-orders"></a>所有工作订单

单击**资产管理** > **常用** > **工作订单** > **所有工作订单**以打开列表。 **所有工作订单**列表中包含所有工作订单，并显示与工作订单有关的部分信息。

![图 1](media/01-work-orders.png)

- 单击**资产管理** > **常用** > **工作订单** > **有效工作订单**可查看有效工作订单的列表。

- 单击**资产管理** > **常用** > **工作订单** > **我的功能位置工作订单维护作业**可查看其中包含在功能位置安装的资产，并且您作为工人（在[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)中设置）关联到的工作订单作业的列表。

- 在**所有工作订单**列表（网格视图）中，单击**工作订单**列中的链接可查看所选记录的详细信息视图。 单击**编辑**按钮以打开来进行编辑。  

- 在详细信息视图中，可查看与工作订单有关的详细信息。  

- 在详细信息视图中，选择**行**链接可查看工作订单作业详细信息，而选择**标题**链接则可查看工作订单详细信息。  

- 屏幕右侧的**相关信息**垂直窗格中包含与工作订单有关的更多信息。 可展开该窗格以查看所选工作订单的相关信息。  


![图 2](media/02-work-orders.png)


操作窗格按钮位于操作窗格上的选项卡中。 下面是与企业资产管理有关的按钮的简短说明：



| 按钮名称                     | 说明                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 编辑​​                            | 编辑所选工作订单。                                                                                                                                                                                                                                           |
| 新                             | 创建新的工作订单。                                                                                                                                                                                                                                                  |
| 删除                          | 删除所选工作订单。                                                                                                                                                                                                                                         |
| 工作订单池                 | 将所选工作订单添加到工作订单池，或从工作订单池中删除工作订单。                                                                                                                                                                                           |
| 调整                          | 调整有关所选工作订单的预计开始和结束时间，服务级别，负责维护工人或负责维护工人组的信息。                                                                                                                                     |
| 相关工作订单              | 创建与所选工作订单作业关联的新工作订单。 如果要登记主工作订单和次级工作订单，这非常有用。                                                                                                                              |
| 复制工作订单                 | 基于现有工作订单创建新的工作订单。                                                                                                                                                                                                                |
| 事件历史记录                   | 查看有关工作订单的登记历史记录。                                                                                                                                                                                                                |
| 工作订单维护作业说明                           | 为工作订单创建描述，或插入注释或注解。 首先单击**添加时间戳**按钮向注释添加您的用户名和时间戳。 将在**工作订单**窗体 > **行详细信息**快速选项卡 > **描述**选项卡中显示注释。 |
| 工具                           | 为工作订单创建所需工具的列表。 工具在**组织管理** > **常用** > **资源** > **资源**中设置为资源。                                                                                                      |
| 维护清单           | 查看与工作订单关联的资产的清单。                                                                                                                                                                                                              |
| 资产故障                     | 查看或登记与资产有关且要用于故障管理的故障信息。                                                                                                                                                                                        |
| 维护停机时间            | 指定工作订单的维护停机时间。                                                                                                                                                                                                                               |
| 条件评估            | 登记工作订单的条件评估度量。                                                                                                                                                                                                             |
| 资产计数器                 | 创建或查看资产的计数器登记。                                                                                                                                                                                                                     |
| 预测                        | 查看或创建工作订单的预测。                                                                                                                                                                                                                               |
| 日记帐                        | 查看或创建工作订单日记帐。 可以从预测复制日记帐行。                                                                                                                                                                                         |
| 项目交易记录            | 查看与为资产创建的工作订单有关的所有已过帐交易记录。                                                                                                                                                                                             |
| 更新工作订单状态                | 更新工作订单生命周期状态。                                                                                                                                                                                                                                                |
| 生命周期状态日志                       | 显示所选工作订单的生命周期状态的日志。                                                                                                                                                                                                                   |
| 资产文档                | 查看附加到与工作订单关联的资产的文档的列表。 这些文档在**资产管理** > **设置** > **资产文档**中设置。                                                                                                 |
| 时间表                        | 安排所选工作订单。                                                                                                                                                                                                                                      |
| 分派            | 将所选工作订单安排给一位工人。                                                                                                                                                                                                                        |
| 删除计划                 | 删除所选工作订单的安排。                                                                                                                                                                                                                          |
| 计划的工作订单维护作业             | 打开**计划的工作订单维护作业**列表页。                                                                                                                                                                                                                             |
| 工作订单采购申请 | 打开**工作订单采购申请**列表页。                                                                                                                                                                                                                 |
| 工作订单采购             | 打开**工作订单采购**列表页。                                                                                                                                                                                                                             |
| 成本控制                    | 比较工作订单的预算成本和实际成本。                                                                                                                                                                                                                |
| 工时控制                    | 比较工作订单的预测工时和实际工时。                                                                                                                                                                                                                |
| 工作订单报告               | 打印工作订单报告。                                                                                                                                                                                                                                                |
| 工作订单消耗量          | 打印消耗报表。                                                                                                                                                                                                                                               |


**工作订单**选项卡 > **项目**组中的按钮与**项目管理与核算**模块中有关预测、日记帐和开票的功能关联。

>[!NOTE]
>通过使用在**资产管理参数**窗体中选择的预测模型运行主计划编制时，可包括为工作订单创建的预测。
