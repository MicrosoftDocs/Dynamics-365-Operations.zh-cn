---
title: 工作订单简介
description: 本主题概述资产管理中的工作订单。
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3891ea08a484950d8fef57d6229117e90ed93a92ab800f9de3ad82db3aff956d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754696"
---
# <a name="introduction-to-work-orders"></a>工作订单简介

[!include [banner](../../includes/banner.md)]



工作订单用于管理维护作业，提供维护作业所需信息和登记维护作业的消耗。 每个工作订单中可以包含一个或多个工作订单作业，并且可以为每个工作订单关联一个或多个资产。 每个工作订单作业定义为资产安排的一个维护作业。

可以通过以下方式创建工作订单：

- 对于基于日历且打开了“自动创建”设置的维护计划，通过自动使用[安排维护计划](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md)。

- 对于打开了“自动创建”设置的维护阶段，通过自动使用[安排维护阶段](../preventive-and-reactive-maintenance/maintenance-rounds.md)。

- 对于预防性维护作业或维护请求，通过[维护安排](../preventive-and-reactive-maintenance/maintenance-schedule.md)。

- 手动

- 从 **所有维护请求**、**有效维护请求** 或 **我的功能位置维护请求** 页面。

>[!NOTE]
>将把与同一个资产关联的工作订单作业关联到同一个项目 ID。

## <a name="all-work-orders"></a>所有工作订单

选择 **资产管理** > **常用** > **工作订单** > **所有工作订单** 打开 **所有工作订单** 列表页。 此页显示所有工作订单和与每个工作订单有关的一些信息。

下图显示了 **所有工作订单** 列表页的示例。

![图 1.](media/01-work-orders.png)

要查看只有有效工作订单的列表，请选择 **资产管理** > **常用** > **工作订单** > **有效工作订单**。 

要查看其中包含在功能位置安装的资产，并且您作为工作人员关联到的工作订单作业的列表，请选择 **资产管理** > **常用** > **工作订单** > **我的功能位置工作订单维护作业**。 （工作人员和功能位置之间的关系在 **工作人员** 页面设置。 有关详细信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。）

您可以通过以下几种方式使用 **所有工作订单** 页面：

- 在网格视图中的 **工作订单** 列选择链接可以显示所选记录的详细信息视图。 然后，您可以选择 **编辑** 打开记录进行编辑。

- 在详细信息视图中，可查看与工作订单有关的详细信息。  

- 在详细信息视图中，选择 **行** 选项卡可查看工作订单作业的详细信息，而选择 **标题** 选项卡则可查看工作订单的详细信息。  

- 展开页面右侧的 **相关信息** 窗格，可以查看与所选工作订单相关的其他信息。

下图显示了 **所有工作订单** 详细信息视图的示例。

![图 2.](media/02-work-orders.png)


操作窗格上的按钮排列在选项卡上。 下表简述与资产管理有关的按钮：



| 按钮名称                     | 说明                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 编辑​​                            | 编辑所选工作订单。                                                                                                                                                                                                                                           |
| 新                             | 创建新的工作订单。                                                                                                                                                                                                                                                  |
| Delete                          | 删除所选工作订单。                                                                                                                                                                                                                                         |
| 工作订单池                 | 将所选工作订单添加到工作订单池，或从工作订单池中删除工作订单。                                                                                                                                                                                           |
| 调整                          | 调整有关所选工作订单的预计开始和结束时间，服务级别，负责维护工人或负责维护工人组的信息。                                                                                                                                     |
| 相关工作订单              | 创建与所选工作订单作业关联的新工作订单。 如果要登记主工作订单和次级工作订单，这非常有用。                                                                                                                              |
| 复制工作订单                 | 创建基于现有工作订单的新工作订单。                                                                                                                                                                                                               |
| 事件历史记录                   | 查看工作订单的登记历史记录。                                                                                                                                                                                                                |
| 工作订单维护作业说明                           | 为工作订单创建描述，或插入与其相关的注释或注解。 首先，选择 **添加时间戳** 向注释添加您的用户名和时间戳。 注释在 **工作订单** 页面的 **行明细** 快速选项卡上的 **描述** 选项卡上显示。         |
| 工具                           | 为工作订单创建所需工具的列表。 工具在 **组织管理** > **资源** > **资源** 中设置为资源。                                                                                                      |
| 维护清单           | 查看与工作订单关联的资产的清单。                                                                                                                                                                                                              |
| 资产故障                     | 查看或登记资产的故障信息。 此信息供故障管理使用。                                                                                                                                                                                      |
| 维护停机时间            | 指定工作订单的维护停机时间。                                                                                                                                                                                                                               |
| 条件评估            | 登记工作订单的条件评估度量。                                                                                                                                                                                                             |
| 资产计数器                 | 创建或查看资产的计数器登记。                                                                                                                                                                                                                     |
| 预测                        | 查看或创建工作订单的预测。                                                                                                                                                                                                                               |
| 日记帐                        | 查看或创建工作订单日记帐。 可以从预测复制日记帐行。                                                                                                                                                                                         |
| 项目交易记录            | 查看与为资产创建的工作订单有关的所有已过帐交易记录。                                                                                                                                                                                             |
| 更新工作订单状态           | 更新工作订单生命周期状态。                                                                                                                                                                                                                                                |
| 生命周期状态日志                      | 查看日志，其中显示所选工作订单的生命周期状态。                                                                                                                                                                                                                   |
| 资产文档                | 查看附加到与工作订单关联的资产的文档的列表。 这些文档在 **资产管理** > **设置** > **资产文档** 中设置。                                                                                                 |
| 时间表                        | 安排所选工作订单。                                                                                                                                                                                                                                      |
| 分派            | 将所选工作订单安排给一位工人。                                                                                                                                                                                                                        |
| 删除计划                 | 删除所选工作订单的安排。                                                                                                                                                                                                                          |
| 计划的工作订单维护作业             | 打开 **计划的工作订单维护作业** 列表页。                                                                                                                                                                                                                             |
| 工作订单采购申请 | 打开 **工作订单采购申请** 列表页。                                                                                                                                                                                                                 |
| 工作订单采购             | 打开 **工作订单采购** 列表页。                                                                                                                                                                                                                             |
| 成本控制                    | 比较工作订单的预算成本和实际成本。                                                                                                                                                                                                                |
| 工时控制                    | 比较工作订单的预测工时和实际工时。                                                                                                                                                                                                                |
| 工作订单报告               | 打印工作订单报告。                                                                                                                                                                                                                                                |
| 工作订单消耗量          | 打印消耗报表。                                                                                                                                                                                                                                               |


“操作窗格”的 **工作订单** 选项卡上 **项目** 组中的按钮与 **项目管理与核算** 模块中的预测、日记帐和开票功能关联。

>[!NOTE]
>要包括在运行主计划编制时在工作订单上创建的预测，请使用在 **资产管理参数** 页面上选择的预测模型。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]