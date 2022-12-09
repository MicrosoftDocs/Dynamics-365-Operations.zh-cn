---
title: 更新流程
description: Microsoft Dynamics 365 Human Resources 是一款真正的服务型软件 (SaaS)，可为应用程序和平台更改提供连续的非接触式服务更新。
author: twheeloc
ms.date: 12/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 197b3c5717494ab3c80a57cda337a9021293bf73
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819288"
---
# <a name="update-process"></a>更新流程

_**适用于：** 独立基础结构中的 Human Resources_ 

> [!NOTE]
> 从 2022 年 7 月开始，无法在独立的 Human Resources 基础结构中预配新的 Human Resources 环境，因此无法在其中创建新的 Microsoft Dynamics Lifecycle Services (LCS) 项目。 客户可以在财务和运营基础结构上部署 Human Resources 环境。 有关详细信息，请参阅[在财务和运营基础结构中预配 Human Resources](hr-admin-setup-provision-fo.md)。

> [!IMPORTANT]
> 财务和运营应用基础结构上的更新和修补程序流程与 Human Resources 独立更新和修补程序流程不同。 有关更新流程的更多信息，请参阅[移至财务和运营的最新更新的流程](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md)。 有关修补程序的详细信息，请参阅[从 Lifecycle Services (LCS) 下载更新](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md)。 

Microsoft Dynamics 365 Human Resources 是一款真正的服务型软件 (SaaS)，可提供连续的非接触式服务更新。 这些更新包含应用程序和平台更改，通常会对服务进行重大改进，包括监管更新。

## <a name="update-policy"></a>更新策略

更新定期针对所有环境发布。 对 Human Resources 的支持根据 [Microsoft 生命周期策略](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)提供，该策略为支持的可用性提供一致且可预测的指南。

## <a name="release-cadence"></a>发布频率 

Human Resources 更新将自动应用于所有环境。 Human Resources 提供两种类型的发布：

- **服务更新**：服务更新包括发布时适用的平台更新。 除了基于异常的更新之外，定期服务更新会在 Dynamics 365 Finance 平台更新正式发布 (GA) 后进行。 有关平台版本的详细信息，请参阅[平台更新的新增功能或更改](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md)。 更新跨区域在全球分期推出。 有关更新的详细信息，请参阅 [Dynamics 365 Human Resources 的新增功能或更改](hr-admin-whats-new.md)。

- **Dataverse 解决方案更新**：根据需要，这些更新大约每六周进行一次。 这些更新包括 Dataverse 中的新实体和对现有实体的更改。 这些更新与每两周更新发布在相同的区域，需要大约六周时间在所有数据中心完成复制。 解决方案更新可能与每两周服务更新一致，也可能不一致。

> [!NOTE]
> 解决方案更新发布后，将在所有数据中心可用。 如果不想等待更新自动复制，可以在任何数据中心的任何环境中手动应用这些更新。

如果需要，Human Resources 会提供以下类型的修复：

- **修订（修补程序）**：可能随每两周服务更新发布进行或独立进行的缺陷修复

- **紧急修复**：本质上是独立的主动和被动修补程序，可能包括仅配置或代码更改以解决实时的站点问题，可能在每两周服务更新发布之外进行

在内部环境中对发布进行审查、测试和验证。 版本签核后，将被部署到生产中。

## <a name="communications"></a>通信

您可以在以下位置了解 Human Resources 正在开发的功能以及已经发布的功能：

- [Dynamics 365 Human Resources 路线图](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365 版本计划](/dynamics365/release-plans/)

- [Dynamics 365 Human Resources 新增功能或更改](hr-admin-whats-new.md)

- [Lifecycle Services (LCS) 中的问题搜索](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md)（仅适用于平台相关漏洞）

- [Human Resources 博客](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer 社区](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>沙盒环境中的预览功能

您可以先在沙盒环境中验证预览功能，然后再在生产环境中启用。 有关启用功能的详细信息，请参阅[功能管理概述](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在 **功能管理** 工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。

有时，完整功能默认启用，并且无法关闭（例如，功能管理工作区）。

某项功能公开发布后，即可以在生产环境中将其打开或关闭。 **功能管理** 工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

我们强烈建议在沙盒或试用环境中预览功能。 最好将当前生产环境或数据库的副本创建到沙盒环境中，以便您可以利用您的数据获得新功能的完整体验。

有关预配沙盒环境的详细信息，请参阅[预配 Human Resources 项目](hr-admin-setup-provision.md)。 要删除测试环境，请参阅[删除实例](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment)。 

## <a name="report-bugs"></a>报告 bug

在测试预览功能或尝试新功能时，您可能会发现无法正常使用的项目。 请通过 [Microsoft Dynamics 365 支持](https://dynamics.microsoft.com/support/)报告任何一个 bug。

## <a name="see-also"></a>请参阅

[Dynamics 365 和 Power Platform 版本计划](/dynamics365/release-plans)</br>
[Dynamics 365 Human Resource 的新增功能或更改](hr-admin-whats-new.md)</br>
[软件生命周期策略](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
