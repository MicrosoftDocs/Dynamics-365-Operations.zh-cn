---
title: 开始使用计划优化
description: 本主题说明如何开始使用计划优化功能。
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423444"
---
# <a name="get-started-with-planning-optimization"></a>开始使用计划优化

[!include [banner](../../includes/banner.md)]

正如[之前宣布](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios)的那样，计划优化计划替换现有的内置主计划引擎。

如果当前使用内置的主计划引擎，则应该立即开始计划迁移到计划优化。 立即开始迁移过程非常重要，因为强制执行弃用操作可能会影响您的操作。 为了避免在最后强制执行弃用时出现问题，我们强烈建议您在 2020 年 12 月 1 日之前完成迁移。 

计划优化功能当前不支持 Supply Chain Management 中内置的计划引擎中提供的所有功能。 因此，重要的是要评估计划优化中当前可用的功能集是否满足您的要求。 计划优化功能当前在 Dynamics Lifecycle Services (LCS) 中默认未启用，因此您有机会在启用该功能之前进行评估。

> [!NOTE]
> 如果您的主计划流程不包括生产（主计划生成的计划生产订单）并且您需要版本 10.0.15 以上的内置主计划引擎，则需要在迁移到计划优化过程中请求一个例外。 从版本 10.0.16 开始，当运行内置主计划而不生成计划生产订单时，环境中将显示一条错误。 应该将计划优化用于在主计划期间不生成计划生产订单的所有新部署。 运行内置主计划引擎而不生成计划生产订单的现有环境的所有者将收到一封邮件，其中包含有关例外流程的详细信息。 我们建议您与合作伙伴一起评估和计划迁移到计划优化。

在打开计划优化之前，强烈建议您评估计划优化拟合分析的结果。 有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。

### <a name="availability"></a>可用性
Planning Optimization 当前在以下 Azure 地域中可用：美国、加拿大、欧洲、英国和澳大利亚。 如果您尝试从其他地理区域安装加载项，则 LCS 将显示一条消息，指明不支持该地理区域。

请注意，Planning Optimization 不支持 Dynamics 365 Supply Chain Management 的本地部署。

### <a name="licensing"></a>许可授权

如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。

### <a name="install-the-add-in"></a>安装加载项

若要使用计划优化，请安装 Dynamics 365 Supply Chain Management 的计划优化加载项。 您可以从 LCS 项目访问加载项，然后从 Supply Chain Management 用户界面 (UI) 启用计划优化功能。

> [!NOTE]
> Planning Optimization 的要求是：支持 LCS 的第 2 层或更高层高可用性环境（不是 OneBox 环境），并且具有 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本。 如果您尝试在 OneBox 环境中安装加载项，则安装将无法完成，因此您需要取消安装。

1. 登录到 LCS，然后打开所需的环境。
1. 转到 **完整详细信息**。
1. 向下滚动到 **环境加载项** 快速选项卡。
1. 选择 **安装新加载项**。
1. 选择 **计划优化**。
1. 按照安装指南操作，并同意条款和条件。
1. 选择 **安装**。
1. 在 **环境加载项** 快速选项卡上，您应该看到正在安装计划优化。
1. 几分钟后 **正在安装** 应会改为 **已安装**（您可能需要刷新页面）。 安装后，您就可以在 Dynamics 365 Supply Chain Management 中激活计划优化了。

安装计划优化加载项的主要目的是连接服务和环境。 因此，无论在环境之间移动任何代码，都必须在将使用计划优化的每个环境上分别安装该加载项。

### <a name="planning-optimization-integration"></a>计划优化集成

要配置是否应将计划优化加载项用于主计划，请转到 **主计划** \> **设置** \> **计划优化参数**。

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

**使用计划优化** 选项的设置确定哪个计划引擎用于主计划：

- **是** – 计划优化用于主计划。
- **否** – 内置 Supply Chain Management 计划引擎用于主计划。

> [!NOTE]
> 如果在 **使用计划优化** 选项设置为 **是** 的情况下触发了为内置 Supply Chain Management 计划引擎创建的现有计划批处理作业，这些作业将失败。

### <a name="integration-with-the-setup"></a>与设置集成

如果打开了计划优化，则使用计划优化加载项来完成主计划。 在这种情况下，主计划结果和功能会受到影响。

## <a name="additional-resources"></a>其他资源

[预览条款和条件](https://go.microsoft.com/fwlink/?linkid=2015274)

[计划优化概览](planning-optimization-overview.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[将筛选器应用于计划](plan-filters.md)

[取消计划作业](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]