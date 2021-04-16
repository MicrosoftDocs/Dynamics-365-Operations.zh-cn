---
title: 创建工作订单
description: 本主题介绍如何在资产管理中创建工作订单。
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836726"
---
# <a name="creating-work-orders"></a>创建工作订单

[!include [banner](../../includes/banner.md)]

计划了预防性维护作业之后，接下来需要为这些作业创建工作订单。 您可以使用其中一个维护安排完成此步骤。 维护安排中的计划作业可以采用不同类型，如下表所述。

| 引用类型 | 说明 |
|---|---|
| 维护计划 | 基于 *时间* 或 *计数器* 维护计划类型的预防性维护作业。 |
| 维护阶段 | 其中包含多个需要相似维护类型的资产的预防性维护作业。 |
| 维护请求 | 手动创建的资产的维护或维修请求。 此请求可以转换为工作订单。 |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>根据维护安排创建工作订单

要创建基于维护安排的工作订单，请遵循以下步骤。

1. 打开以下页面之一，具体取决于您要如何为工作订单选择计划项目：

    - 所有维护安排（**资产管理 \> 管理计划 \> 所有维护安排**）
    - 打开维护安排行（**资产管理 \> 管理计划 \> 打开维护安排行**）
    - 打开维护安排池（**资产管理 \> 管理计划 \> 打开维护安排池**）

1. 在网格中，选中要为其创建工作订单的每个计划性维护作业的复选框。 然后，在操作窗格中，选择 **工作订单**。

    **创建工作订单** 对话框将出现。 **维护预测工时数** 字段将显示所选行的预测工时总数。

    ![创建工作订单对话框](media/18-preventive-maintenance.png)

1. 在 **参数** 部分，指定应创建的工作订单的数量。 选择以下选项之一：

    - **每行一个工作订单** – 每个维护安排行创建一个工作订单。
    - **每个以下对象一个工作订单** – 创建将根据您选择此选项时可用的其他选项的设置进行分组的工作订单。

1. 在 **工作订单类型** 字段中，选择要用于所有创建的工作订单的工作订单类型。
1. 选择 **确定** 根据您的设置创建工作订单。

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>对在维护计划运行时自动创建的工作订单行进行分组

使用此功能，您可以根据维护计划，为在系统设置为自动生成工作订单时对单个工作订单下的工作订单行进行分组定义规则。 以前，自动生成的工作订单只能包含一行。 但是，现在您可以按资产、资产类型或功能位置等对工作订单进行分组。 （手动生成的工作订单可能已经通过这种方式完成了分组，如本主题上一节中所述。）

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>为自动生成的工作订单启用分组

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*资产管理*
- **功能名称**：*在运行维护计划时为分组工作订单应用规则*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>为自动生成的工作订单设置分组

要为自动生成的工作订单设置分组，请执行以下步骤。

1. 转到 **资产管理 \> 设置 \> 预防性维护 \> 维护计划**。
1. 对于要在其中生成分组工作订单的每个计划，按照下列步骤操作：

    1. 在列表窗格中选择该计划。
    1. 在 **行** 快速选项卡上，确保选中每行上的 **自动创建** 复选框。

1. 转到 **资产管理 \> 定期 \> 预防性维护 \> 安排维护计划**。
1. 在 **安排维护计划** 对话框中的 **期间** 部分，为计划指定时间范围（查找为之生成工作的计划性维护作业时要提前多长时间）。
1. 将 **从计划自动创建工作订单** 选项设置为 *是*。
1. 在 **工作订单** 部分，选择下列选项之一：

    - **每行一个工作订单** – 每个维护安排行创建一个工作订单。 （此选项提供的功能与 *在运行维护计划时为分组工作订单应用规则* 功能关闭时可用的功能相同。）
    - **每个以下对象一个工作订单** – 创建将根据您选择此选项时可用的其他选项的设置进行分组的工作订单。

1. 如果您希望仅在运行某些维护计划时应用这些选项，在 **要包括的记录** 快速选项卡上，根据需要添加筛选器，就像您可能对 Microsoft Dynamics 365 Supply Chain Management 中的其他批处理作业所做的那样。
1. 在 **在后台运行** 快速选项卡上，根据需要设置批处理和计划选项，就像您可能在 Supply Chain Management 中对其他批处理作业所做的那样。
1. 选择 **确定** 运行和/或计划选定的维护计划。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]