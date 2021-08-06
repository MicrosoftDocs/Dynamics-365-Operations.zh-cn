---
title: Dynamics 365 Human Resources 中的新增功能或更改（2021 年 5 月 20 日）
description: 此主题介绍了 2021 年 5 月 20 日 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: marcelbf
ms.date: 05/20/2021
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
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c7b7f71cf084a05bb0278f5df4ddb022ef3d640f
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560042"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Dynamics 365 Human Resources 中的新增功能或更改（2021 年 5 月 20 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4189。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 平台更新 10.0.18 (42) | -- | [针对 Finance and Operations 应用（2021 年 5 月）的版本 10.0.18 的平台更新](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Microsoft Teams 的 Human Resources 应用现在支持半天定义和休假日拆分功能 | -- | [管理 Teams 中的休假申请](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 |  说明 |
| --- | --- | --- |
| 583776 | 大量员工登记休假计划导致重复记录错误 | 此 bug 已在最新版本中修复，大量休假计划登记现在应可以成功处理。 |
| 582263 | 无法一次为所有工作人员运行生活事件处理 | 当 **工作人员** 字段留空以进行生活事件处理时，会处理所有工作人员的事件。 |
| 558383 | 主要受益人未在没有选择默认指定人时标记为 100% | Bug 已经修复，用户现在只需选择主要受益人切换。|
| 509404 | 部门人数分析未考虑部门之间的员工流动 |此分析已经更新，现在包括部门之间的员工转移|
| 579420 | 锁定网格中的列功能不应该可用 | **锁定网格中的列** 功能在 Human Resources 中不可用，但在功能管理中可用。 此功能已从要启用的功能列表中删除。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理资格规则中的自定义字段支持 | [资格处理的自定义字段支持](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[配置资格规则](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 休假和缺勤工作流体验增强 | [休假和缺勤工作流体验增强](https://go.microsoft.com/fwlink/?linkid=2147528) | [申请休假](hr-employee-self-service-request-time-off.md)|
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|
| 休假应计交易记录审计 | - | [休假应计交易记录审计](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
|  让缺勤管理人员能够管理休假 | [让缺勤管理人员能够管理休假](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
