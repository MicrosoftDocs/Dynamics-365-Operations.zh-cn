---
title: Dynamics 365 Human Resources 的新增功能或更改，2021 年 1 月 28 日
description: 此主题介绍了 2021 年 1 月 28 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: marcelbf
manager: tfehr
ms.date: 01/28/2021
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
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b4739b5b1b6c61e829dd931ba8d4c9e0e49c8aed
ms.sourcegitcommit: fb335954f73eaa2233ef6fb1e7fab1ece3c50756
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2021
ms.locfileid: "5081283"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Dynamics 365 Human Resources 的新增功能或更改，2021 年 1 月 28 日

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.3906。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 将福利原因代码集成到 **人事管理** 工作区 | -- | [设置原因代码](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。


| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 539456 | **只显示缺勤(不包含详细信息)** 参数启用时日历在悬浮文本中显示休假类型。 | 当 **只显示缺勤(不包含详细信息)** 选项启用后，请求的日期现在将悬浮显示。 |
| 528907 | 在员工角色上授予对法人的访问权限导致经理无法在“员工自助服务”的 **我的团队** 区域查看员工的休假余额活动。 |设置此选项现在将允许经理继续查看休假余额活动。 |
| 526280 | HcmWorkerEntity、HcmEmployeeEntity 和 HcmContractorEntity 上的权限错误。 | 由于 NationalityCountryRegion 字段上的权限错误，具有非系统管理员角色的用户无法导出列出的实体。 用户将继续需要以下特权来导出此信息：HcmWorkerEntityMaintain、HcmWorkerEntityView、HcmEmployeeEntityMaintain、HcmEmployeeEntityMaintain、HcmEmployeeEntityView、HcmContractorEntityMaintain 和 HCMContractorEntityView。 |
| 542147 | 通过“员工自助服务”添加银行帐户时 **银行帐号** 和 **银行代号** 字段变为必填字段。 | 我们已经修复了添加银行帐户详细信息时员工需要输入 **银行帐号** 和 **银行代号** 字段的错误。 保存新的银行帐户信息时，这些字段不再是必填字段。 |
| 543641 | 电子报告中未填充邮政编码。 | 修复了保险范围代码 L 到 Q 的 ACA 报告中未填充邮政编码的 bug。 |
| 545402 | 为 UserBranding.js 文件添加路由更改来删除 404 错误。 | 用户应该不会再在控制台中看到 404 错误。 |

## <a name="in-preview"></a>预览模式   

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| Microsoft Teams 中的 Human Resources 应用 | [Microsoft Teams 中的员工休假和缺勤体验](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[管理 Teams 中的休假申请](hr-teams-leave-app.md) |
| 经理跨公司查看休假 | [经理跨公司查看员工休假](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [配置休假和缺勤参数](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 福利登记的电子邮件确认 | 当员工从员工自助服务中的福利登记体验中签出时，此功能将提供向他们发送确认电子邮件的选项。 此功能将于 2 月 1 日可用。 有关详细信息，请参阅[配置每个公司的福利管理参数](hr-benefits-setup-parameters-per-company.md)。 |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse 术语更新

自 2020 年 11 月起，Common Data Service 已重命名为 [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)。 请参阅 Power Apps 博客上的[正式公告](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)了解详细信息。 连同此名称更改一起，Dataverse 中的一些术语已经更新。 例如，*实体* 现在更新为 *表*，*字段* 现在更新为 *列*。 有关详细信息，请参阅[术语更新](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)。

在此版本中，与 Dynamics 365 Human Resources 和 Dataverse 集成相关的术语已在整个应用程序中进行了更新，以反映这些更改。 例如，**Common Data Service 集成** 窗体现在是 **Microsoft Dataverse 集成**。

要了解有关 Dynamics 365 Human Resources 与 Microsoft Dataverse 集成的详细信息，请参阅[配置 Microsoft Dataverse 集成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service)和[配置 Microsoft Dataverse 虚拟表](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)
