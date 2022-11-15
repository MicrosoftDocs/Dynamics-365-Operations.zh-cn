---
title: 查看、管理和审核计划订单
description: 本文介绍如何查看、管理和审核计划订单。
author: t-benebo
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a4c3b6c2dd149d3fedf1dc3dc418541961ad1a73
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740950"
---
# <a name="view-manage-and-approve-planned-orders"></a>查看、管理和审核计划订单

[!include [banner](../../includes/banner.md)]

本文介绍如何查看、管理和审核计划订单。

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>查看和管理计划订单

您可以在任何计划订单列表页上查看和管理计划订单。 根据要处理的计划订单的类型，转到以下位置之一：

- 主计划 \> 工作区 \> 主计划
- 主计划 \> 主计划 \> 计划订单
- 生产控制 \> 生产订单 \> 计划生产订单
- 采购 \> 采购订单 \> 计划采购订单
- 库存管理 \> 入站订单 \> 计划转移
- 库存管理 \> 出站订单 \> 计划转移

## <a name="view-and-edit-the-status-of-planned-orders"></a>查看和编辑计划订单的状态

您可以使用每个计划订单的 **状态** 字段来帮助跟踪进度或更改计划订单的处理方式。 提供以下 **状态** 值：

- **未处理** – 当主计划生成计划订单时，它们将获得此状态。 具有此状态的计划订单将在下一次计划运行期间删除。
- **已完成** – 此状态指示计划订单已完成。 如果您决定不确认某一计划订单，可以将其状态手动更改为 *已完成*。 请注意，系统以相同的方式对待 *未处理* 和 *已完成* 状态。
- **已审核** – 此状态指示计划订单已审核，可以确认。 如果要确认计划订单，可将其状态更改为 *已审核*。 如果要保留对计划订单所做的编辑，或者打算确认计划订单，请将其状态更改为 *已审核*。 状态为 *已审核* 的计划订单将被主计划视为固定供应和预期供应。 因此，在之后的主计划运行中不会对其进行修改或删除。 为实现此行为，计划逻辑会在主计划期间将状态为 *已审核* 的计划订单从旧计划版本复制到新计划版本。 请注意，状态为 *已审核* 的计划订单仅在特定主计划内视为供应。

要更改单个计划订单的状态，[打开任何计划订单列表页](#view-planned-orders)，打开订单，然后执行以下步骤之一：

- 在 **常规** 快速选项卡上，更改 **状态** 字段的值。
- 在操作窗格的 **计划订单** 选项卡上，在 **流程** 组中，选择 **更改状态**。
- 在操作窗格上，选择 **审核** 将订单标记为已审核。

要同时更改多个计划订单的状态，[打开任何计划订单列表页](#view-planned-orders)，选中要更改的每个订单的复选框，然后执行以下步骤之一：

- 在操作窗格的 **计划订单** 选项卡上，在 **流程** 组中，选择 **更改状态**。
- 在操作窗格上，选择 **审核** 将订单标记为已审核。

## <a name="approve-planned-orders"></a>审核计划订单

审核计划订单是从计划订单创建确认订单过程中的可选步骤。

下图显示了如何使用分配给每个计划订单的 **状态** 值来实施审核工作流。 要实施审核流程，请按照上一节中所述为每个计划订单手动调整 **状态** 值。

![计划订单流。](media/approved-planned-orders-1.png)

> [!TIP]
> 我们建议您审核所有修改的计划订单。 否则，所做编辑将被下一次计划运行忽略和覆盖。

## <a name="additional-resources"></a>其他资源

- [确定计划订单](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
