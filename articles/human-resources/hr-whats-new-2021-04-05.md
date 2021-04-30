---
title: Dynamics 365 Human Resources 中的新增功能或更改（2021 年 4 月 5 日）
description: 本主题介绍了 2021 年 4 月 5 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改。
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ffb1d8966cb7e41a7032c6d4449b9e332c0e4703
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890593"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Dynamics 365 Human Resources 中的新增功能或更改（2021 年 4 月 5 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4074。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 限制员工编辑业务联系人详细信息 | [限制员工编辑业务联系人详细信息](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [限制对个人信息的编辑](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 550852 | **审批** 按钮不会验证在 **审查** 窗体上设置的必填字段。 | 当您将 **审查** 窗体上的某个字段设置为必填字段，并为经理角色发布更改时，窗体不会按预期验证。 |
| 559564 | 固定薪酬更改的历史工作人员操作会使解雇用户遇到错误。 | 离职员工薪酬的工作人员操作会产生错误。 员工解雇后，解雇前的提升员工操作会产生错误。 |
| 560074 | 雇用类别下拉列表未筛选 **工作人员类型**，并显示员工和合同工的类别。 | 在 **员工** 窗体上，**雇用类别** 下拉列表应基于员工的工作人员类型显示员工或合同工类别。 |
| 567388 | 新创建的员工的某些信息不会立即同步到 Dataverse 中的 **cdm_worker** 表。 | 创建新员工记录时，新记录将同步到 Dataverse 中的 **cdm_worker** 表，但并非所有属性都将包含在 Dataverse 记录中。 |
| 563837 | 将显示在 Human Resources 中不可用的功能。 | 功能管理中将显示多个不适用于 Human Resources 的功能。 现在，这些功能已从可在 Human Resources 中启用的功能列表中删除。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |
| 平台更新 10.0.17 (41) | 平台更新 10.0.17 计划于 2021 年 4 月 19 日在下一个版本中开始推出。 有关详细信息，请参阅 [Finance and Operations 应用的版本 10.0.17（2021 年 4 月）的平台更新](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md)。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]