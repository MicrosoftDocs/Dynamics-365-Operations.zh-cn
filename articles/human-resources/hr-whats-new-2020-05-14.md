---
title: Dynamics 365 Human Resources（2020 年 5 月 14 日）中的新增功能或更改
description: 此主题介绍了 2020 年 5 月 14 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e70d8fc62150d68503552754e94c7130d8960c76
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802351"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Dynamics 365 Human Resources（2020 年 5 月 14 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。 更改适用于内部版本号 8.1.3244。 某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。

## <a name="platform-changes"></a>平台变更

本周的发布中包含平台变更。 有关详细信息，请参阅 [Finance and Operations 应用版本 10.0.10（2020 年 5 月）的平台更新](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34)。 此发布中包含所保存视图的缺陷修复和更改。
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>确保 Dataverse 选择列表与休假枚举一致 (436343)

Dataverse 选择列表现在与休假枚举一致。

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>允许用户根据请求量配置请假工作流 (300044)

用户可根据请求量配置请假工作流。
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>启用高级安全后，新工作窗体通过“视图”菜单显示数据 (403185)

此发布中解决了启用高级访问且其他公司的工作人员可访问时，如何通过法人功能查看工作人员。

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>允许为一个计划或一家公司运行应计休假 (318844)

通过此更改，可以为一家公司或一个计划运行应计。
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>通过“招聘的工作人员”窗体显示职位的全职等效 (FTE) (414658)

为休假类型启用 FTE 选项之后，工作人员职位的 FTE 值决定工作人员的假期额度费率。 此字段现在包含在 **招聘的工作人员** 窗体和 **成批登记** 对话框中。

## <a name="add-leave-balance-expiration-batch-job-431266"></a>添加休假余额到期批处理作业 (431266)

现在可执行每日运行的新批处理作业。 当到期日期变为当前时，将导致剩余休假余额减少。

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>使用工作人员个人联系人实体导出员工的个人联系人不导出类型为父关系的个人联系人 (345893)

**工作人员个人联系人** 数据实体（DMF 中为 **HcmPersonalContactPersonEntity**，OData 中则为 **PersonalContactPerson**）无法导出关系类型为 **父** 的个人联系人。 为此更改后创建的个人联系人解决了此问题。 后续发布中将解决类型为 **父** 的现有个人联系人。

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>当其标记为休假和缺勤并启用了简化员工窗体时，不同方案中将显示原因代码 (434163)

如果启用了简化员工输入，此更改将原因代码限制为仅休假和缺勤代码。

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>预览功能“将来为员工分配休假计划”显示错误 (433555)

此更改更正了为休假计划分配了两个休假类型且您尝试分派员工时的错误。

## <a name="getting-started-banner-appears-for-all-users-441731"></a>为所有用户显示开始横幅 (441731)

进行此更改后，将对非系统管理员或数据管理管理员用户隐藏开始横幅。 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Human Resources 中Dataverse 工作人员地址实体在日期时间有效日期方面的工作方式不同 (425071)

特定方案中，此更改让地址信息根据地址日期保持一致。

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>无法向批准的请假添加附件 (425407)

在本周的发布中，不必更改请假即可向批准的请假添加附件。

## <a name="in-preview"></a>预览模式

## <a name="leave-suspension"></a>休假暂停

可在 Human Resources 中暂停员工的休假和缺勤。 暂停休假将停止所选休假类型的休假应计。 如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。 有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>更新用户体验以表明应计已暂停 (429550)

用户体验现在表明计划已暂停应计。

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>暂停指定休假类型的休假应计 (272447)

在此版本中，HR 可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。 无薪假可以是一种类型，但不是必须的。 您可以根据其他休假类型暂停任何休假。

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>可用于暂停应计的 DMF 实体 (429549)

DMF 实体现在可用于暂停应计。

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>将原因代码添加到应计暂停 (429547)

原因代码已添加到应计暂停。

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>开始从人力资源参数转换到休假和缺勤参数

此版本开始将人力资源参数与休假和缺勤参数进行合并。

## <a name="carry-forward-rules"></a>结转规则

可为转移了结转调整的结转余额指定结转休假类型。 例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。 有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]