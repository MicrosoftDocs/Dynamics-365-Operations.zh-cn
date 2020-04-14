---
title: 更新流程
description: Microsoft Dynamics 365 Human Resources 是一款真正的服务型软件 (SaaS)，可为应用程序和平台更改提供连续的非接触式服务更新。
author: andreabichsel
manager: AnnBe
ms.date: 02/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 424027e82717b8636d59289b28978d6ce3c6db4d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154497"
---
# <a name="update-process"></a>更新流程

Microsoft Dynamics 365 Human Resources 是一款真正的服务型软件 (SaaS)，可提供连续的非接触式服务更新。 这些更新包含应用程序和平台更改，通常会对服务进行重大改进，包括监管更新。

## <a name="update-policy"></a>更新策略

更新定期针对所有环境发布。 对 Human Resources 的支持根据 [Microsoft 生命周期策略](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)提供，该策略为支持的可用性提供一致且可预测的指南。

## <a name="release-cadence"></a>发布频率

Human Resources 更新将自动应用于所有环境。 Human Resources 提供两种类型的发布：

- **服务更新**：每两周更新一次，其中包括缺陷修复和新功能。 服务更新在发布时还包括适用的平台更新。 要了解何时发布平台更新，请参阅[表 3：平台发布](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)。 每两周更新跨区域在全球分期推出。 有关每两周更新的详细信息，请参阅 [Dynamics 365 Human Resources 的新增功能或更改](hr-admin-whats-new.md)。

    除非另有说明，否则所有受支持的数据中心都会每两周更新一次。 每两周更新中包括美国、澳大利亚、欧洲、英国、亚洲和加拿大地区。 

- **Common Data Service 解决方案更新**：根据需要，这些更新大约每六周进行一次。 这些更新包括 Common Data Service 中的新实体和对现有实体的更改。 这些更新与每两周更新发布在相同的区域，需要大约六周时间在所有数据中心完成复制。 解决方案更新可能与每两周服务更新一致，也可能不一致。

> [!NOTE]
> 解决方案更新发布后，将在所有数据中心可用。 如果不想等待更新自动复制，可以在任何数据中心的任何环境中手动应用这些更新。

如果需要，Human Resources 还会提供以下类型的修复：

- **修订（修补程序）**：可能随每两周服务更新发布进行或独立进行的缺陷修复

- **紧急修复**：本质上是独立的主动和被动修补程序，可能包括仅配置或代码更改以解决实时的站点问题，可能在每两周服务更新发布之外进行

在内部环境中对发布进行审查、测试和验证。 版本签核后，将被部署到生产中。

## <a name="release-cadence-exceptions-in-2020"></a>2020 年的发布频率例外情况

以下日期是常规发布计划的例外情况：

| 日期 | 说明 |
| --- | --- |
| 11 月 23 日所在周 | 无更新 |
| 12 月 14 日所在周 | 仅次要更新 |
| 12 月 21 日所在周 | 无更新 |
| 12 月 28 日所在周 | 无更新 |

## <a name="communications"></a>通信

您可以在以下位置了解 Human Resources 正在开发的功能以及已经发布的功能：

- [Dynamics 365 Human Resources 路线图](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365 版本计划](https://docs.microsoft.com/dynamics365/release-plans/)

- [Dynamics 365 Human Resources 新增功能或更改](hr-admin-whats-new.md)

- [Lifecycle Services (LCS) 中的问题搜索](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs)（仅适用于平台相关漏洞）

- [Human Resources 博客](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer 社区](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>沙盒环境中的预览功能

您可以先在沙盒环境中验证预览功能，然后再在生产环境中启用。 有关启用功能的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在功能管理工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。

有时，完整功能默认启用，并且无法关闭（例如，功能管理工作区）。

某项功能公开发布后，即可以在生产环境中将其打开或关闭。 功能管理工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

我们强烈建议在沙盒或试用环境中预览功能。 最好将当前生产环境或数据库的副本创建到沙盒环境中，以便您可以利用您的数据获得新功能的完整体验。

有关预配沙盒环境的详细信息，请参阅[预配 Human Resources 项目](hr-admin-setup-provision.md)。 要删除测试环境，请参阅[删除实例](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment)。 

## <a name="report-bugs"></a>报告 bug

在测试预览功能或尝试新功能时，您可能会发现无法正常使用的项目。 请通过 [Microsoft Dynamics 365 支持](https://dynamics.microsoft.com/support/)报告任何一个 bug。

## <a name="see-also"></a>请参阅

[Dynamics 365 和 Power Platform 版本计划](https://docs.microsoft.com/dynamics365/release-plans)</br>
[Dynamics 365 Human Resource 的新增功能或更改](hr-admin-whats-new.md)</br>
[软件生命周期策略](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

