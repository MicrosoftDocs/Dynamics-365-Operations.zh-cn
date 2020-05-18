---
title: 取消计划作业
description: 本主题说明如何取消使用“计划优化”功能的活动计划作业。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323454"
---
# <a name="cancel-a-planning-job"></a>取消计划作业

[!include [banner](../../includes/banner.md)]

在 Microsoft Dynamics 365 Supply Chain Management 中，您可以取消使用“计划优化”功能的活动计划作业。 如果在直接从用户界面（而不是后台）触发了计划优化作业后在对话框中选择**取消**，不会取消该计划优化作业。 即使收到“已取消操作”之类警告，您仍然需要通过以下步骤通过计划优化取消计划作业。


要取消活动的计划作业，请按照下列步骤操作。 

> [!NOTE]
> 仅活动作业可以取消。

1. 转到**主计划 \> 设置 \> 计划**。
2. 为计划运行选择适当的计划。
3. 选择**历史记录**。
4. 选择要取消的计划作业。
5. 选择**取消**。

作业状态将为**正在取消**，直到计划优化服务确认该作业已被取消。 然后，状态将更改为**已取消**。

> [!NOTE]
> 要查看状态更改，您必须通过选择**刷新**按钮刷新页面。

## <a name="additional-resources"></a>其他资源

[计划优化概览](planning-optimization-overview.md)

[开始使用计划优化](get-started.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[将筛选器应用于计划](plan-filters.md)
