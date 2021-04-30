---
title: Dataverse 表
description: Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893392"
---
# <a name="dataverse-tables"></a>Dataverse 表

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。

> [!NOTE]
> Human Resources 实体与 Dataverse 表对应。 有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)

下列 Dataverse 表基于 Human Resources 实体提供。

## <a name="benefit-tables"></a>福利表

| 姓名 | 表 |
| --- | --- |
| 福利计算频率 | cdm_benefitcalculationfrequency |
| 福利计算频率付薪期间 | cdm_benefitcalculationfrequencypayperiod |
| 福利计算比率 | cdm_benefitcalculationrate |
| 福利计算比率详细信息 | cdm_benefitcalculationratedetail |
| 福利选项 | cdm_benefitoption |
| 福利计划 | cdm_benefitplan（未启用自定义字段支持） |
| 福利类型 | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>业务流程任务表

| 姓名 | 表 |
| --- | --- |
| 业务流程日历 | cdm_businessprocesscalendar |
| 业务流程组分配 | cdm_businessprocessgroupassignment |
| 业务流程库任务组 | cdm_businessprocesslibrarytaskgroup |
| 业务流程阶段 | cdm_businessprocessstage |
| 核对清单模板标题 | cdm_businessprocesstemplateheader |
| 核对清单模板任务 | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>薪酬表

| 姓名 | 表 |
| --- | --- |
| 固定薪酬计划 | cdm_compensationfixedplan |
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
| 固定薪酬事件 | cdm_fixedcompensationevent |
| 股份行权规则 | cdm_vestingrule |
| 工作人员固定薪酬 | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>组织表

| 姓名 | 表 |
| --- | --- |
| 部门 | cdm_department |
| 雇用 | cdm_employment |
| 公司 | cdm_company |
| 职位 | cdm_job |
| 工作职能 | cdm_jobfunction |
| 工作职位 | cdm_jobposition |
| 职位类型 | cdm_positiontype |
| 职位工作人员分配 | cdm_positionworkerassignmentmap |
| 工作职位维度 | cdm_jobpositiondimension|
| 工作类型 | cdm_jobtype |
| 语言 | cdm_language |
| 职位 | cdm_title |

> [!NOTE]
> **职位类型**、**职位工作人员分配** 和 **雇用** 的财务维度提供到 Dataverse 的单向集成。 财务维度更新现在不能从 Dataverse 同步到 Human Resources。 

## <a name="leave-and-absence-tables"></a>休假和缺勤表

| 姓名 | 表 |
| --- | --- |
| 休假银行交易记录 | cdm_leavebanktransaction |
| 休假登记 | cdm_leaveenrollment |
| 休假计划 | cdm_leaveplan |
| 休假请求 | cdm_leaverequest |
| 休假请求详细信息 | cdm_leaverequestdetail |
| 休假类型 | cdm_leavetype |
| 休假类型原因代码 | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>工资表

| 姓名 | 表 |
| --- | --- |
| 付薪周期 | cdm_paycycle |
| 付薪期间 | cdm_payperiod |
| 工资单收入代码 | cdm_payrollearningcode |
| 银行帐户付款 | cdm_bankaccountdisbursement |
| 税区 | cdm_taxregion |

## <a name="worker-tables"></a>工作人员表

| 姓名 | 表 |
| --- | --- |
| 工作线程 | cdm_worker |
| 工作人员地址 | cdm_workeraddress |
| 工作人员个人详细信息 | cdm_workerpersonaldetail |
| 工作人员标识号 | cdm_workerpersonidentificationnumber |
| 工作人员标识类型 | cdm_workerpersonidentificationtype |
| 工作日历 | cdm_workcalendar |
| 工作日历天 | cdm_workcalendarday |
| 工作日历的假日 |cdm_workcalendarholiday |
| 工作日历假期行 | cdm_workcalendarholidayline |
| 工作日历时间间隔 | cdm_workcalendartimeinterval（未启用自定义字段支持） |
| 工作人员银行帐户 | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>工作人员设置表

| 姓名 | 表 |
| --- | --- |
| 退伍军人状态 | cdm_veteranstatus |
| 所属种族 | cdm_ethnicorigin |
| 原因代码 | cdm_reasoncode |
| 人员身份证明签发机构 | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>能力表

| 姓名 | 表 |
| --- | --- |
| 技能类型 | cdm_skilltype |

## <a name="table-relationship-models"></a>表关系模型

### <a name="worker"></a>工作线程

![工作线程](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>工作和工作职位

![工作和工作职位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>福利

![福利](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>薪酬

![薪酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>离开

![离开](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>工作日历

![工作日历](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>请参阅

[选择数据集成技术](hr-admin-integration-choose-technology.md)<br>
[配置 Dataverse 集成](hr-admin-integration-common-data-service.md)<br>
[配置 Dataverse 虚拟表](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources 虚拟表常见问题解答](hr-admin-virtual-entity-faq.md)<br>
[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)<br>
[术语更新](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]