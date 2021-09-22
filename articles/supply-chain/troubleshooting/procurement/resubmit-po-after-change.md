---
title: 更改后将采购订单重新提交到工作流时出错
description: 更改后将采购订单重新提交到工作流时出错
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475735"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>更改后将采购订单重新提交到工作流时出错


## <a name="symptoms"></a>故障特征

更改后重新提交采购订单时，工作流中发生以下错误：

> 已停止(错误): X++ 异常：在以下位置激活更改管理时，仅允许在“草稿”状态下对采购订单 PO0000569 进行更改<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

仅当在您请求更改之前采购订单处于 *已确认* 状态时，才会发生此问题。 如果您在采购订单处于 *已批准* 状态时请求更改，工作流可以成功处理。

## <a name="resolution"></a>解决方法

发生此问题可能是由于采购订单分配不一致。

要解决此问题并将采购订单重置为 *草稿* 状态，请转到 **采购 \> 定期任务 \> 清除 \> 采购订单分配重置**。 有关详细信息，请参阅以下博客文章：[解决 Dynamics 365 Supply Chain Management 中的采购订单分配错误](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)。

此问题将通过[此 Microsoft 知识库 (KB) 文章](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138)解决。
