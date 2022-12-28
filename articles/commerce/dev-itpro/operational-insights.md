---
title: 设置操作见解
description: 本文介绍如何在  Microsoft Dynamics 365 Commerce 中设置和使用操作见解功能。
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832114"
---
# <a name="set-up-operational-insights"></a>设置操作见解

[!include [banner](../includes/banner.md)]

本文介绍如何在  Microsoft Dynamics 365 Commerce 中设置和使用操作见解功能。

操作见解是一项 Dynamics 365 Commerce 功能，旨在通过将遥测数据直接发送到客户拥有的 Application Insights 帐户，让客户更好地了解其服务运行状况和业务功能。

通过在 Commerce headquarters 中为您的环境启用操作见解，您可以从 Commerce Scale Unit (CSU) 和您的销售点 (POS) 设备收集经过策划的事件列表。 这些事件可以帮助您更好地了解系统的性能，并让您监控关键的技术和业务指标。

即使您不想一直收集此遥测数据，您也可以通过对特定环境快速启用或禁用收集来获益。 这样，遥测可以帮助您在开发或生产过程中进行故障排除或调试。

## <a name="access-logs-in-application-insights"></a>在 Application Insights 中访问日志

要通过 Application Insights 访问 Commerce CSU 和 POS 组件的诊断事件日志，请完成本节中的过程。

### <a name="minimum-version-requirements-for-csu"></a>CSU 的最低版本要求

CSU 具有以下最低版本要求：

- 10.0.23（Retail Server 版本 9.33.22062.15 及更高版本）
- 10.0.24（Retail Server 版本 9.34.22062.14 及更高版本）
- 10.0.25（Retail Server 版本 9.35.22062.13 及更高版本）
- 10.0.26 及更高版本（所有版本）

### <a name="enable-diagnostic-events-in-application-insights"></a>在 Application Insights 中启用诊断事件

> [!IMPORTANT]
> 如果您之前使用的是操作见解的预览版，则必须通过以下过程来启用操作见解。 这样，您可以确保能够继续安全可靠地访问事件。

要启用 Commerce 组件诊断事件，您必须拥有一个 Application Insights 帐户。 您可以使用现有帐户或[创建新帐户](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource)。 出于数据隐私原因，我们建议您为生产、沙盒和开发环境使用单独的 Application Insights 帐户。 创建帐户后，您必须在 Headquarters 中启用 **操作见解** 功能。

要在 Application Insights 中启用诊断事件，请执行以下步骤。

1. 在 Headquarters 中，打开 **功能管理** 工作区，并启用 **操作见解** 功能。
1. 转到 **系统管理 \> 设置 \> 操作见解**。
1. 在 **配置** 选项卡上，将 **商务渠道事件** 选项设置为 **是**。
1. 在 **环境** 选项卡上，针对您计划在其中使用 Application Insights 的每个环境输入 **LCS 环境 ID** 和 **环境模式** 的值 您可以在 Microsoft Dynamics Lifecycle Services 中针对该环境在 **环境详细信息** 页上查找每个环境的环境 ID。 需要执行此步骤，以在执行数据库复制操作时帮助防止诊断事件被无意中发送到不正确的环境。
1. 在 **Application Insights 注册表** 选项卡上，指定 Application Insights **检测密钥** 值，和您计划在其中使用每个 Application Insights 帐户的环境的相应 **环境模式** 值。
1. 完成上述配置后，您必须运行 **CDX 作业 1110** 作业。 您可以等待此作业按其自己的计划运行，也可以手动运行。
1. 在 Lifecycle Services 中，转到 **环境详细信息 \> 商业 \> 管理**，选择一个 CSU 实例，然后选择 **重新启动**。 为 CSU 重复这一步骤。
1. 对计划使用 Application Insights 的每个环境重复上述步骤。

> [!NOTE]
> - Operational Insights 中的遥测事件可能会发生变化。 我们建议您使用操作见解事件自行进行初步分析和故障排除，而不是定义仪表板或警报。 如果您将事件用于自助故障排除之外的其他目的，我们建议您在每次 CSU/POS 发布后验证和更新您的查询。
> - 从 Commerce 版本 10.0.29 开始，本节中的过程还允许将 POS 操作见解事件流式传输到您的 Application Insights 帐户。 如需了解更多信息，请参阅 [POS 操作见解 – 事件和查询](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf)。

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>使用 DLLHost.exe.config 文件控制 POS 操作见解事件

要使用 DLLHost.exe.config 文件控制 POS 操作见解事件，请按照下列步骤操作。

1. 在文本编辑器中，打开 **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker** 中的 **DLLHost.exe.config** 文件。
1. 在 **diagnosticsSection** 部分，删除类名称为 **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger** 的接收器 XML 元素。
1. 保存此文件。

### <a name="disable-diagnostic-events-in-application-insights"></a>在 Application Insights 中禁用诊断事件

> [!IMPORTANT]
> 如果要禁用诊断事件并且不再将它们发送到 Application Insights，则必须完成以下过程。 您不能只在功能管理中禁用该功能。

要在 Application Insights 中禁用诊断事件，请执行以下步骤。

1. 在 Headquarters 中，转到 **系统管理 \> 操作见解**。
1. 在 **配置** 选项卡上，将 **商务渠道事件** 选项设置为 **否**。
1. 完成上述配置后，您必须运行 **CDX 作业 1110** 作业。 您可以等待此作业按其自己的计划运行，也可以手动运行此作业。
1. 在 Lifecycle Services 中，转到 **环境详细信息 \> 商业 \> 管理**，选择一个 CSU 实例，然后选择 **重新启动**。 为 CSU 重复这一步骤。
1. 对计划关闭 Application Insights 的每个环境重复上述步骤。

要针对单个环境禁用诊断事件，请在 **操作见解** 页面的 **Application Insights 注册表** 选项卡上删除检测密钥。 然后完成上述过程的步骤 3 和 4。

> [!NOTE]
> 在 Commerce 版本 10.0.29 及更高版本中，本节中的这些步骤还会禁止将 POS 操作见解事件流式传输到您的 Application Insights 帐户。 
