---
title: Dynamics 365 Human Resources 新增功能或更改（2021 年 4 月 19 日）
description: 本主题介绍了 2021 年 4 月 19 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改。
author: marcelbf
ms.date: 04/19/2021
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
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8968c9cb849901288d75cd5e539a57faf0045337
ms.sourcegitcommit: e24e335811727c4b12152323b2bcb25495c08c5b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/22/2021
ms.locfileid: "5934884"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Dynamics 365 Human Resources 新增功能或更改（2021 年 4 月 19 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4113。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 平台更新 10.0.17 (41) | -- | [针对 Finance and Operations 应用（2021 年 4 月）的版本 10.0.17 的平台更新](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| 福利管理窗体中的自定义字段支持 | [福利管理中的自定义字段支持](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [福利管理概览](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 552164 | **员工自助服务 > 开设课程** 上的 **已保存视图** 对包含课程安排的课程不起作用 | 如果“开设课程”(ESS) 上使用了“已保存视图”，并且其中一门课程附加了课程安排，视图将不再为该课程显示多个行 |
| 560614 | **福利 > 生活事件选项** 在工具提示文档和代码行为中有差异。 | 更新了 **生活事件选项** 中的工具提示，显示正确的行为。 |
| 560616 | **福利 > 生活事件选项** 在工作人员福利计划中是可编辑的，但更改不受影响。 | 根据工具提示文档，基于依赖方选项，更新了生活事件选项启用或禁用的切换行为。 |
| 565054 | **高级访问** 打开时，无法查看 **未雇用工作人员** 列表内容。 | 此版本解决了 **高级访问** 打开时，只有系统管理员可以查看 **未雇用工作人员** 列表内容的问题。 由于此修复是一项安全更改，因此您需要在“功能管理”中选择加入此功能。 启用此功能后，即使打开了高级访问，那些有权访问窗体的角色也会看到内容。 有关详细信息，请参阅[未雇用工作人员](hr-personnel-workers-without-employment.md)。 |
| 570586 | 当雇用在工作人员的所有休假计划中的最新交易之前结束时，休假申请验证将失败。 | 雇用结束后，休假申请验证没有基于员工休假交易而失败。|
| 570783 | 在 Human Resources 共享参数中启用和禁用跨公司休假将更改在一家公司受雇的员工在休假请求中看到的内容。 | 如果启用或禁用了该参数，在一家公司受雇的员工不会看到申请休息时间的更改。 |
| 572343 | 启用“跨国公司休假视图”功能时，不会显示所需的原因代码。 | 启用跨公司休假功能时，原因代码现在将按预期显示。 |
| 573676 | 无法将 **期间** 添加到 **福利管理 > 链接 > 福利计划**。 | 修复了无法在现有 **福利计划** 窗体上添加或更新 **期间** 的 bug。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 休假和缺勤工作流体验增强 | [休假和缺勤工作流体验增强](https://go.microsoft.com/fwlink/?linkid=2147528) | [申请休假](hr-employee-self-service-request-time-off.md)|
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |
| 平台更新 10.0.18 (42) | 平台更新 10.0.18 计划于 2021 年 5 月 17 日在服务版本中开始推出。 有关详细信息，请参阅 [Finance and Operations 应用版本 10.0.18（2021 年 5 月）的平台更新](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18)。 |
| 福利管理资格规则中的自定义字段支持  | [资格处理的自定义字段支持](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
