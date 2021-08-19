---
title: Dynamics 365 Human Resources 中的新增功能或更改（2021 年 2 月 22 日）
description: 此主题介绍 2021 年 2 月 22 日 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 379a902489bdccdfa3490a830cc3b0bbf7639e7f0b62079a3ff3a999b0a7c412
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721551"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Dynamics 365 Human Resources 中的新增功能或更改（2021 年 2 月 22 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3988。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 的 Dynamics 365 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 529994 | 在 **工作人员** 窗体上修改 **称作** 字段未触发 Dataverse 更新 | 修复了当 **工作人员** 窗体上的 **称作** 字段更新时，Dataverse 不更新的问题。 |
| 532651 | 薪酬分析 PBI 报表在为所有公司计算指标时不使用货币转换 | 修复了薪酬分析 PBI 报表不能正确进行货币转换的问题。 |
| 552226 | 生活事件处理多次关闭和重新打开单个生活事件的计划  | 修复了问题：员工在多个法人中，在生活事件发生时，为员工所在的每个法人生成生活事件记录。 处理生活事件时，必须选择要处理的法人。 但是，此处理逻辑并不会自行约束为此法人。 而是为所有法人进行处理，关闭和重新打开所选法人中的计划。 此操作会让一个生活事件在同一个法人中多次处理，导致多次关闭/重新打开受该生活事件影响的每个计划。 |
| 518064 | 当多个依赖方被标记为默认指定人员时，在合格计划中只选择了一个依赖方 | 修复了不能在合格计划中自动选择多个默认指定人员的问题。 您现在还可以为个人联系人指定主要受益人。 如果有多个受益人，主要受益人在合格计划中列为 100%。 |
| 552365 | 升级到平台更新 40 后，提供您自己的数据库 (BYOD) 导出作业失败 | 修复了将平台更新 40 应用于环境后 BYOD 导出失败的问题。 |
| 547123 | 限制在仪表板上的“待办事宜”列表中查询的任务数 | 现在，“待办事宜”列表中显示的任务数限制为 15，以修复由于尝试加载过多任务而导致的性能问题。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 经理跨公司查看休假 | [经理跨公司查看员工休假](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [配置休假和缺勤参数](./hr-leave-and-absence-parameters.md) |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 限制员工编辑业务联系人详细信息 | [限制员工编辑业务联系人详细信息](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse 术语更新

自 2020 年 11 月起，Common Data Service 已重命名为 [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro)。 请参阅 Power Apps 博客上的[正式公告](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)了解详细信息。 随此名称更改，Dataverse 中的一些术语已经更新。 例如，*实体* 现在更新为 *表*，*字段* 现在更新为 *列*。 有关详细信息，请参阅[术语更新](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)。

在此版本中，与 Dynamics 365 Human Resources 和 Dataverse 集成相关的术语已在整个应用程序中进行了更新，以反映这些更改。 例如，**Common Data Service 集成** 窗体现在是 **Microsoft Dataverse 集成**。

要了解有关 Dynamics 365 Human Resources 与 Microsoft Dataverse 集成的详细信息，请参阅[配置 Microsoft Dataverse 集成](./hr-admin-integration-common-data-service.md)和[配置 Microsoft Dataverse 虚拟表](./hr-admin-integration-common-data-service-virtual-entities.md)。

## <a name="updates-to-service-deployment"></a>服务部署更新

从 2021 年 2 月 22 日版本开始，我们正在调整区域服务更新部署。 调整将包括轮换全球区域接收 Human Resources 服务更新的顺序，以及对更新阶段之间的等待时间进行修改。 这些更改让我们更加符合安全部署实践 (SDP) 的做法，以提高服务的稳定性、质量和可支持性。

我们将继续遵循两周的部署频率。 但是，客户可能会注意到，更新通常在两周周期的不同日期（与以前版本相比）应用到他们的 Human Resources 环境。

有关服务更新流程的详细信息，请参阅[更新流程](./hr-admin-setup-update-process.md)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]