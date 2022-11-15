---
title: 开始使用主计划
description: 本文说明如何开始使用 Dynamics 365 Supply Chain Management 中的主计划功能。
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 958de3f9ae6ead6cb6914bd3b7a4560e768013ab
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740321"
---
# <a name="get-started-with-master-planning"></a>开始使用主计划

[!include [banner](../../includes/banner.md)]

Supply Chain Management 中的主计划由 Dynamics 365 Supply Chain Management 的名为“计划优化加载项”的外部服务提供。 本主题介绍如何获取和设置该服务。

## <a name="availability"></a>可用性

Planning Optimization 当前在以下 Azure 地域中可用：美国、加拿大、巴西、欧洲、法国、英国、澳大利亚、亚太、日本和印度。 如果您尝试从其他地理区域安装加载项，则 LCS 将显示一条消息，指明不支持该地理区域。 有关 Azure 地区和相关区域的详细信息，请参阅 [Azure 地区](https://azure.microsoft.com/global-infrastructure/geographies/#geographies)。

请注意，Planning Optimization 不支持 Dynamics 365 Supply Chain Management 的本地部署。

## <a name="licensing"></a>许可授权

如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。

## <a name="install-and-enable-planning-optimization"></a>安装和启用计划优化

若要使用计划优化，您必须确保系统具备所有先决条件，然后启用其许可证密钥并安装 Dynamics 365 Supply Chain Management 的计划优化加载项。

### <a name="prerequisites"></a>先决条件

在安装计划优化加载项之前，必须满足以下先决条件：

- 您必须是在支持 LCS 的第 2 层或更高层高可用性环境（不是 OneBox 环境）中运行 Supply Chain Management，并且具有 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本。 如果您尝试在 OneBox 环境中安装加载项，则安装将无法完成，因此您需要取消安装。

- 您的系统必须已针对 Power Platform 集成进行设置。 有关详细信息，请参阅 [Microsoft Power Platform 与财务和运营应用的集成](../../../fin-ops-core/dev-itpro/power-platform/overview.md)。

### <a name="enable-the-planning-optimization-license"></a>启用计划优化许可证

要使用计划优化，您必须启用它的配置键。 为此：

1. 将您的系统置于维护模式下，如[维护模式](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
1. 转到 **系统管理 \> 设置 \> 许可证配置**。
1. 在 **配置键** 选项卡上，选中 **计划优化** 的复选框。
1. 关闭维护模式，如[维护模式](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。

### <a name="install-the-planning-optimization-add-in"></a>安装计划优化加载项

您必须从 LCS 项目安装此加载项，然后从 Supply Chain Management 用户界面启用计划优化功能。

安装计划优化加载项：

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

## <a name="integrate-planning-optimization-with-your-system"></a>将计划优化与系统集成

要配置是否应将计划优化加载项用于主计划，请转到 **主计划** \> **设置** \> **计划优化参数**。

### <a name="connection-status"></a>连接状态

连接状态指示 Supply Chain Management 和计划优化服务之间的连接的当前状态。 下表显示可能的值。

| 连接状态 | 说明 | 是否可以使用计划优化？ |
|---|---|---|
| 已连接 | 已在计划优化服务和 Supply Chain Management 之间建立连接。 | 是 |
| 正在启用连接 | 当前正在处理打开计划优化服务连接的请求。 | 否 |
| 已断开连接 | 没有与计划优化服务的连接。 可以从 LCS 打开连接，如本文前面所述。 | 否 |
| 正在禁用连接 | 当前正在处理关闭计划优化服务连接的请求。 | 否 |
| 正在获取状态 | 系统正在等待来自计划优化服务的状态信息。 | 否 |

### <a name="the-use-planning-optimization-option"></a>“使用计划优化”选项

**使用计划优化** 选项的设置确定哪个计划引擎用于主计划：

- **是** – 计划优化用于主计划。
- **否** – 已弃用的主计划引擎用于主计划。

此设置适用于所有法人（公司）。 无法在某些法人中使用计划优化，也无法在其他法人中使用已弃用的主计划引擎。

> [!NOTE]
> 如果在 **使用计划优化** 选项设置为 **是** 的情况下触发了为已弃用的主计划引擎创建的现有计划批处理作业，这些作业将失败。

### <a name="integration-with-the-setup"></a>与设置集成

如果打开了计划优化，则使用计划优化加载项来完成主计划。 在这种情况下，主计划结果和功能会受到影响。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
