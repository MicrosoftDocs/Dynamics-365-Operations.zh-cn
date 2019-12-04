---
title: 取消计划作业
description: 本主题说明如何取消使用“计划优化”功能的活动计划作业。
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773912"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a>取消计划作业

在 Microsoft Dynamics 365 Supply Chain Management 中，您可以取消使用“计划优化”功能的活动计划作业。

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

## <a name="related-resources"></a>相关资源

[计划优化概述](planning-optimization-overview.md)

[开始使用计划优化](get-started.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[将筛选器应用于计划](plan-filters.md)
