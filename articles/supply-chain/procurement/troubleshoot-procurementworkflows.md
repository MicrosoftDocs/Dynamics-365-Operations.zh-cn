---
title: 采购工作流故障排除
description: 本主题介绍如何解决使用采购工作流时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423424"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>采购工作流故障排除

本主题介绍如何解决使用采购工作流时可能遇到的问题。

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>更改后将采购订单重新提交到工作流时出错：“激活更改管理后，仅允许在“草稿”状态下对采购订单 X 进行更改”

仅当在您请求更改之前采购订单处于 *已确认* 状态时，才会发生此问题。 如果您在采购订单处于 *已批准* 状态时请求更改，工作流可以成功处理。

### <a name="error-description"></a>错误描述

更改后重新提交采购订单时，工作流中发生以下错误：

> 已停止(错误): X++ 异常：在以下位置激活更改管理时，仅允许在“草稿”状态下对采购订单 PO0000569 进行更改<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>解决问题

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

此问题将通过[此 Microsoft 知识库 (KB) 文章](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138)解决。

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>一个或多个会计分配分配过多或分配不足。

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>如果在打开了更改管理的采购订单上取消了剩余交货量，采购订单将进入“已确认”状态。

### <a name="issue-description"></a>问题描述

对于需要接受更改管理的采购订单，如果请求的唯一更改是取消一个或多个行上的剩余交货量，该采购订单在获得批准后将直接进入 *已确认* 状态，不会创建日记帐。

### <a name="issue-resolution"></a>解决问题

取消剩余交货量不会影响确认日记帐的内容。 此功能应在部分接收行时使用，剩余数量应在与供应商确认采购订单后，在流程步骤中取消。

如果这应该反映在采购订单确认中，数量应在采购订单行上调整，以要求进行确认。 或者，如果行上未进行任何接收，可以删除数量。 在这种情况下，将需要重新确认。

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>取消的采购订单将显示在“采购订单准备”工作区的草稿列表中。

### <a name="issue-description"></a>问题描述

取消处于 *已确认* 状态的采购订单后，取消的采购订单仍会出现在 **采购订单准备** 工作区中的草稿采购订单列表中。

### <a name="issue-resolution"></a>解决问题

仅需要接受更改管理的采购订单会发生此问题。 发生这种情况是因为取消被认为是必须进行审批的更改。 审批可以由系统自动完成。 因此，流程是将取消的采购订单提交到审批工作流，让它可以进入 *已批准* 状态。 此时，采购订单将不再出现在 **采购订单准备** 工作区中的草稿采购订单列表中。

