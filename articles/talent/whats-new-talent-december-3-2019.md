---
title: Dynamics 365 Talent（2019 年 12 月 3 日）中的新增功能或更改
description: 本文介绍 Microsoft Dynamics 365 Talent 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528685"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Dynamics 365 Talent（2019 年 12 月 3 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Talent 中的新增功能或更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2646。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="feature-management-workspace"></a>“功能管理”工作区

**功能管理** 工作区提供了每个版本提供的功能列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。 有关功能管理的更多信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。

所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。 主要功能通常在预览期之后的每年 10 月和 4 月公开发布。 在 **功能管理** 工作区中看到新功能后，即可将其打开。 有些功能可能默认已启用。
 
有时，完整功能默认启用，并且无法关闭（例如，**功能管理** 工作区）。
 
某项功能公开发布后，即可以在生产环境中将其打开或关闭。 **功能管理** 工作区指示何时将强制使用某项预览功能。 此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。 您无法关闭强制功能。 在强制使用之前，您可以在所有环境中打开和关闭功能。

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>添加批处理作业历史记录清理的自动计划 (332528)

进行此更改后，**批处理作业历史记录** 每天晚上运行，并删除 30 天以上的批处理作业历史记录项目。

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>当标识号长度与标识类型不匹配时，Talent 不响应工作人员的操作 (390971)

此版本更正了当标识号长度与标识类型内的定义不匹配时出现的问题。 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>固定薪酬不随着职位详细信息的更改更新级别 (348085)

在本周的发布中，**薪酬开始日期** 确定为员工创建新的固定薪酬记录时在该日期与职位关联的作业。

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>当仅应为“工作人员”或“合同工”时，“工作人员、员工和合同工”列表都显示为“工作人员”类型 (384473)

此更改将准确反映输入的工作人员（合同工或员工）的类型。

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>新雇员操作的电子邮件通知由于安全策略不包含姓名信息 (383402)

此更改更正了启用高级安全性后，工作流占位符内的“姓”或“姓氏”字段中显示的信息。

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>系统允许同一天有两个全天休假请求 (379284)

进行此更改后，您将无法对同一天发出两个休假请求。 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>地址更改列表应按生效日期排序 (352798)

进行此更改后，地址更改列表现在按 **生效日期** 排序。

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>休假请求应允许在 Talent 中从 Common Data Service 删除 (376999)

通过此更改，可以从 Common Data Service 中删除草稿和已取消的休假请求，然后从 Talent 中删除。

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>将相同的收入代码分配给员工时，允许删除收入代码 (371792)

在此版本中，必须先从员工删除收入代码，然后再从系统中删除收入代码。

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>具有两个审核阶段的休假和缺勤工作流无法完成 (391116)

通过此更改，当为请求配置了多个审核阶段时，休假和缺勤工作流将继续执行所有步骤。

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>在 Talent 中更新或输入后，发布日期不同步到 Common Data Service (397361)

此更改更正了 **人员标识** 记录的发布日期不同步到 Talent 中的 Common Data Service 的问题。

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>将经理分配到职位时出现层次结构循环引用错误 (386659)

此更改更正了在将新经理分配到职位时出现循环引用错误的特殊情况。

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>现在支持自定义字段的 Common Data Service 实体

以下 Common Data Service 实体现在支持自定义字段：

| 姓名 | 实体 |
| --- | --- |
| 银行帐户付款 | cdm_bankaccountdisbursement |
| 福利计算频率 | cdm_benefitcalculationfrequency |
| 福利计算频率付薪期间 | cdm_benefitcalculationfrequencypayperiod |
| 福利计算比率 | cdm_benefitcalculationrate |
| 福利计算比率详细信息 | cdm_benefitcalculationratedetail |
| 福利选项 | cdm_benefitoption |
| 福利计划 | cdm_benefitplan（未启用自定义字段支持） |
| 福利类型 | cdm_benefittype |
| 业务流程日历 | cdm_businessprocesscalendar |
| 业务流程组分配 | cdm_businessprocessgroupassignment |
| 业务流程库任务组 | cdm_businessprocesslibrarytaskgroup |
| 业务流程阶段 | cdm_businessprocessstage |
| 核对清单模板标题 | cdm_businessprocesstemplateheader |
| 核对清单模板任务 | cdm_businessprocesstemplatetask |
| 公司 | cdm_company |
| 薪酬固定计划 | cdm_compensationfixedplan |
| 薪酬网格 | cdm_compensationgrid |
| 薪酬级别 | cdm_compensationlevel |
| 薪酬付薪频率 | cdm_compensationpayfrequency |
| 薪酬参考点设置 | cdm_compensationreferencepointsetup |
| 薪酬参考点设置行 | cdm_compensationreferencepointsetupline |
| 薪酬区域 | cdm_compensationregion |
| 薪酬结构 | cdm_compensationstructure |
| 可变薪酬计划 | cdm_compensationvariableplan |
| 可变薪酬计划级别 | cdm_compensationvariableplanlevel |
| 可变薪酬计划类型 | cdm_compensationvariableplantype |
| 部门 | cdm_department |
| 雇用 | cdm_employment |
| 所属种族 | cdm_ethnicorigin |
| 固定薪酬事件 | cdm_fixedcompensationevent |
| 职位 | cdm_job |
| 工作职能 | cdm_jobfunction |
| 工作职位 | cdm_jobposition |
| 工作类型 | cdm_jobtype |
| 语言 | cdm_language |
| 休假银行交易记录 | cdm_leavebanktransaction |
| 休假登记 | cdm_leaveenrollment |
| 休假计划 | cdm_leaveplan |
| 休假请求 | cdm_leaverequest |
| 休假请求详细信息 | cdm_leaverequestdetail |
| 休假类型 | cdm_leavetype |
| 休假类型原因代码 | cdm_leavetypereasoncode |
| 付薪周期 | cdm_paycycle |
| 付薪期间 | cdm_payperiod |
| 工资单收入代码 | cdm_payrollearningcode |
| 人员标识颁发机构 | cdm_personidentificationissuingagency |
| 职位类型 | cdm_positiontype |
| 职位工作人员分配 | cdm_positionworkerassignmentmap |
| 原因代码 | cdm_reasoncode |
| 技能类型 | cdm_skilltype |
| 税区 | cdm_taxregion |
| 股份行权规则 | cdm_vestingrule |
| 退伍军人身份 | cdm_veteranstatus |
| 工作日历 | cdm_workcalendar |
| 工作日历天 | cdm_workcalendarday |
| 工作日历的假日 |cdm_workcalendarholiday |
| 工作日历假期行 | cdm_workcalendarholidayline |
| 工作日历时间间隔 | cdm_workcalendartimeinterval（未启用自定义字段支持） |
| 工作线程 | cdm_worker |
| 工作人员地址 | cdm_workeraddress |
| 工作人员银行帐户 | cdm_workerbankaccount |
| 工作人员固定薪酬 | cdm_workerfixedcompensation |
| 工作人员个人详细信息 | cdm_workerpersonaldetail |
| 工作人员标识号 | cdm_workerpersonidentificationnumber |
| 工作人员标识类型 | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>预览模式

仅在 **沙盒** 环境中才能使用预览功能。

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。
