---
title: Dynamics 365 Human Resources 的新增功能或更改（2021 年 7 月 26 日）
description: 本文介绍 2021 年 7 月 26 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c7211135733f45a9841ae5a80607b01999d7c69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870920"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Dynamics 365 Human Resources 的新增功能或更改（2021 年 7 月 26 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 2 概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4384。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 平台 update 10.0.20 | -- | [财务和运营应用版本 10.0.20 的平台更新（2021 年 8 月）](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 |  Description |
| --- | --- | --- |
| 600422 | 工资单地址验证失败，无法准备付款。 | 验证已更新为仅需要一个“工资单居住地址”类型的地址和一个“工资单工作地点”类型的地址。 |
| 601226 | 数据集成问题：工资单集成导出项目没有用于完全推送的选项 | 与 Ceridian DayForce 的工资单集成正在执行增量推送，而不是完全推送。 Ceridian 要求始终完全刷新。 此问题现已修复，数据导出项目中的实体将不再翻转到增量推送。 |
| 602272 | 现在缺少添加到员工自助服务工作区的磁贴，并且无法再将磁贴添加到其中 | 我们已修复员工自助服务的个性化设置问题。 新磁贴可添加到视图中，并且任何现有个性化设置都将对用户可见 |
| 600711 | 为全天休假请求启用了半天定义选择字段 | 此问题现在已修复，只有当员工选择启用了半天定义的休假类型，并且将半天作为所选数额值时才启用半天定义字段 |
| 602208 | 显示工时而不是天的应计费率单位 | 此问题现已修复。 **休假** 窗体将显示 **增长率** 列的正确休假单位（小时或天）。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|
|  让缺勤管理人员能够管理休假 | [让缺勤管理人员能够管理休假](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | 对于此版本，我们将更新缺勤管理人员工作区视图。 有关详细信息，请参阅[配置缺勤管理人员角色](https://go.microsoft.com/fwlink/?linkid=2168107)。|
|  配置每个休假类型的附件要求 | [配置每个休假类型的附件要求](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[配置休假和缺勤类型](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  配置每个休假类型的休假单位 | [配置每个休假类型的休假单位](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[配置休假和缺勤类型](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 使员工能够标记为准备支付 | [使员工能够标记为准备支付](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [准备付款](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>即将推出

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 2 概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 2 波概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
