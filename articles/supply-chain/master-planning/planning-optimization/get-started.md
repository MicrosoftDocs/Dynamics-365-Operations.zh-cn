---
title: 开始使用计划优化
description: 本主题说明如何开始使用计划优化功能。
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
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
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076124"
---
# <a name="get-started-with-planning-optimization"></a>开始使用计划优化

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

计划优化功能当前不支持 Microsoft Dynamics 365 Supply Chain Management 内置的计划引擎中提供的所有功能。 因此，重要的是要评估计划优化中当前可用的功能集是否满足您的要求。 默认情况下，Dynamics Lifecycle Services (LCS) 中默认不启用计划优化功能。 因此，您有机会在启用之前进行评估。

最终，计划优化将取代现有的内置 Supply Chain Management 计划引擎。

在打开计划优化之前，强烈建议您评估计划优化拟合分析的结果。 有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。

### <a name="licensing"></a>许可授权

如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。

### <a name="install-the-add-in"></a>安装加载项

若要使用计划优化，请安装 Dynamics 365 Supply Chain Management 的计划优化加载项。 您可以从 LCS 项目访问加载项，然后从 Supply Chain Management 用户界面 (UI) 启用计划优化功能。

> [!NOTE]
> 计划优化的要求是 LCS 通过 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本实现了高可用性环境（而不是 OneBox 环境）。

1. 登录到 LCS，然后打开所需的环境。
1. 转到**完整详细信息**。
1. 向下滚动到**环境加载项**快速选项卡。
1. 选择**安装新加载项**。
1. 选择**计划优化**。
1. 按照安装指南操作，并同意条款和条件。
1. 选择**安装**。
1. 在**环境加载项**快速选项卡上，您应该看到正在安装计划优化。
1. 几分钟后**正在安装**应会改为**已安装**（您可能需要刷新页面）。 安装后，您就可以在 Dynamics 365 Supply Chain Management 中激活计划优化了。

### <a name="planning-optimization-integration"></a>计划优化集成

要配置是否应将计划优化加载项用于主计划，请转到**主计划** \> **设置** \> **计划优化参数**。

#### <a name="connection-status"></a>连接状态

连接状态指示 Supply Chain Management 和计划优化服务之间的连接的当前状态。 下表显示可能的值。

| 连接状态 | 说明 | 是否可以使用计划优化？ |
|---|---|---|
| 已连接 | 已在计划优化服务和 Supply Chain Management 之间建立连接。 | 是 |
| 正在启用连接 | 当前正在处理打开计划优化服务连接的请求。 | 否 |
| 已断开连接 | 没有与计划优化服务的连接。 可以从 LCS 打开连接，如本主题前面所述。 | 否 |
| 正在禁用连接 | 当前正在处理关闭计划优化服务连接的请求。 | 否 |
| 正在获取状态 | 系统正在等待来自计划优化服务的状态信息。 | 否 |

#### <a name="the-use-planning-optimization-option"></a>“使用计划优化”选项

**使用计划优化**选项的设置确定哪个计划引擎用于主计划：

- **是** – 计划优化用于主计划。
- **否** – 内置 Supply Chain Management 计划引擎用于主计划。

> [!NOTE]
> 如果在**使用计划优化**选项设置为**是**的情况下触发了为内置 Supply Chain Management 计划引擎创建的现有计划批处理作业，这些作业将失败。

### <a name="integration-with-the-setup"></a>与设置集成

如果打开了计划优化预览，则使用计划优化加载项来完成主计划。 在这种情况下，主计划结果和功能会受到影响。

## <a name="related-resources"></a>相关资源

[预览条款和条件](https://go.microsoft.com/fwlink/?linkid=2015274)

[计划优化概述](planning-optimization-overview.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[将筛选器应用于计划](plan-filters.md)

[取消计划作业](cancel-planning-job.md)
