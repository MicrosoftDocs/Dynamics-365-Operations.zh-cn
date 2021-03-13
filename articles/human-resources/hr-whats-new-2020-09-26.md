---
title: Dynamics 365 Human Resources 2020 年 9 月 26 日中的新增功能或更改
description: 本主题介绍了 2020 年 9 月 26 日 Microsoft Dynamics 365 Human Resources 中的新增或更改的功能。
author: jcart1106
manager: tfehr
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ac72489c3b2dacfde280606a83221e8514793701
ms.sourcegitcommit: 2190be6c205d7d9e43bdb99b9190cc0112f9f093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5152189"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Dynamics 365 Human Resources 2020 年 9 月 26 日中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。 有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2020 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3589-hf.3。

### <a name="new-features"></a>新功能

此发布通常提供以下功能：

- **平台更新 10.0.13 现在可用**：有关更新的详细信息，请参阅[针对 Finance and Operations 应用（2020 年 10 月）的版本 10.0.13 的平台更新](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13)。

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快向您提供此信息。 本主题可能会进行更新，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 | 说明 |
| --- | --- | --- |
| 469495 | 更新默认财务维度网格和对话框 | 通过 Human Resources 更新财务维度网格和对话框。 |
| 474887 | 休假请求工作项在手动决策中打开错误的链接 | 当工作流配置包含手动决策时，从 **分配给我的工作项** 导航到休假请求将打开错误的链接，显示当前用户创建的空白表单或休假请求，而不是分配给他们进行手动决策的空白表单或休假请求。 |
| 474962 | 休假和缺勤参数实体的字段带有不明确的标签 | 将更新休假和缺勤参数实体标签以使其更清晰。 |
| 481401 | 当应计日期基数在应计开始日期之后和月底时，应计处理将挂起 | 当应计日期基数在应计开始日期之后和月底时，应计处理将更新为没有延迟。 |
| 447167 | 即将过期的记录列表包括空闲工作人员 | **人员管理** 中的 **即将过期的记录** 选项卡中包括了空闲工作人员。 现在，它只包括有效工作人员。 |
| 486840 | 从 **分配给我的工作项** 中打开错误的休假请求 | 从 **分配给我的工作项** 中选择休假请求不再打开分配给当前用户的最新休假请求。 |
| 506868 | 没有为 **工作职位** 实体设置 Dataverse **职务** 字段 | **工作** 和 **工作职位** 实体中的 **职务** 字段显示为未指定。 现在显示 **职务** 字段。 |
| 430359 | 无法访问已分配经理和员工角色的离职清单任务 | 如果具有将来终止日期的工作人员只有员工或经理角色，则无法访问其清单任务。 现在，只有员工或经理角色的用户可以在未来的终止日期访问离职任务。 |
| 458102 | 创建后，新员工未出现在 **工作人员工资单信息** 实体上 | 新员工包括在工作人员工资单信息实体中，而无需在导出实体之前打开该员工的工资单信息。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 中的 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |
| 增强的工作流请求和审批 | [组织和人员管理工作流体验增强](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [用于定位“分配给我的工作项”列表的配置选项](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>即将推出

计划在将来的发布中添加以下新功能：

- [经理自助服务中的自定义链接](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2019 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)。

## <a name="additional-resources"></a>其他资源

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)
[Dynamics 365 Human Resources 2020 年发布波次 2 概述](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[更新流程](hr-admin-setup-update-process.md)
[管理功能](hr-admin-manage-features.md)
