---
title: Dynamics 365 Human Resources 中的新增功能或更改（2021 年 5 月 3 日）
description: 本文介绍 2021 年 5 月 3 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df8bd0277e4f27c23ba25c886d12f589913e5d46
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066214"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Dynamics 365 Human Resources 中的新增功能或更改（2021 年 5 月 3 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4140。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 创建生活事件时添加信息栏。 | - | 创建生活事件时，信息栏会显示一条消息，指示创建的生活事件的类型。

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 |  Description |
| --- | --- | --- |
| 559312 |  为员工创建固定薪酬计划时未显示级别。 |  如果用户所在的时区与公司所在的时区之间存在时区不匹配，无法读取工作的薪酬级别。 此查询已更新为根据 UTC 时间进行提取。 |
| 573676  | 无法在 **福利计划** 窗体中添加新期间。 | 更新了此窗体，可以在 **福利计划** 中的 **期间** 快速选项卡下启用 **新建** 按钮。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 休假和缺勤工作流体验增强 | [休假和缺勤工作流体验增强](https://go.microsoft.com/fwlink/?linkid=2147528) | [申请休假](hr-employee-self-service-request-time-off.md)|
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|
| 休假应计交易记录审计 | - | [休假应计交易记录审计](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 平台更新 10.0.18 (42) | 平台更新 10.0.18 计划于 2021 年 5 月 17 日在服务版本中开始推出。 有关详细信息，请参阅[财务和运营应用版本 10.0.18 的平台更新（2021 年 5 月）](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18)。 |
| 福利管理资格规则中的自定义字段支持  | [资格处理的自定义字段支持](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

