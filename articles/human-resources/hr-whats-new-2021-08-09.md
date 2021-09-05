---
title: Dynamics 365 Human Resources 2021 年 8 月 9 日版本的新增功能或更改
description: 此主题介绍了 2021 年 8 月 9 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: marcelbf
ms.date: 08/09/2021
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
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f515b614aedce3d58994bf21104ada25702a71e
ms.sourcegitcommit: fc19ee0aba2a6174fef305d151f1eb23ca6c0346
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7385692"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Dynamics 365 Human Resources 2021 年 8 月 9 日版本的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Microsoft Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 2 概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4393。

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 | 说明 |
| --- | --- | --- |
| 558385 | 如果为默认指定人员开启了 **自动选择指定人员** 选项，则不会选中默认指定人员。 | 此问题现已修复。 如果开启了 **Human Resources 共享参数** 页面中的 **自动选择指定人员** 选项，将自动选中多个默认指定人员。 |
| 589617 | 如果限制为只有特定公司才能访问，则 **休假** 页面中的 **可购买** 和 **可出售** 余额为空白。 | 此问题现已修复。 如果将用户限制给特定公司，则 **休假** 页面将显示 **可购买** 和 **可出售** 余额。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关如何开启或关闭的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|
| 让缺勤管理人员能够管理休假 | [让缺勤管理人员能够管理休假](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | 在此版本中，我们将更新缺勤管理人员工作区视图。 有关详细信息，请参阅[配置缺勤管理人员角色](https://go.microsoft.com/fwlink/?linkid=2168107)。 |
| 配置每个休假类型的附件要求 | [配置每个休假类型的附件要求](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[配置休假和缺勤类型](https://go.microsoft.com/fwlink/?linkid=2168108)|
| 配置每个休假类型的休假单位 | [配置每个休假类型的休假单位](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[配置休假和缺勤类型](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 使员工能够标记为准备支付 | [使员工能够标记为准备支付](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [准备付款](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>即将推出

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 2 概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

| 功能 | 明细 |
| --- | --- |
| 平台更新 10.0.21 (45) | 计划于 2021 年 10 月 4 日在服务版本中开始推出 平台更新 10.0.21。 有关详细信息，请参阅 [Finance and Operations 应用版本 10.0.21（2021 年 10 月）的平台更新](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21)。 |

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 2 波概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
