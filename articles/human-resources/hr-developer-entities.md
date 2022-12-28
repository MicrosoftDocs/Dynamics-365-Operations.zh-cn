---
title: Dataverse 表
description: Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838574"
---
# <a name="dataverse-tables"></a>Dataverse 表


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。

> [!NOTE]
> Human Resources 实体与 Dataverse 表对应。 有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)

下列 Dataverse 表基于 Human Resources 实体提供。

有关已知问题的更多信息，请参阅 [Lifecycle Services (LCS) 中的问题搜索](/dev-itpro/lifecycle-services/issue-search-lcs)。

## <a name="benefit-tables"></a>福利表

| Name | 表 | 已知问题  | Status |
| --- | --- |    --------|----------  |
| 福利计算频率 | cdm_benefitcalculationfrequency |     |     |
| 福利计算频率付薪期间 | cdm_benefitcalculationfrequencypayperiod |     |     |
| 福利计算比率 | cdm_benefitcalculationrate |    |     |
| 福利计算比率详细信息 | cdm_benefitcalculationratedetail |753225 | 已解析  |
| 福利选项 | cdm_benefitoption |    |     |
| 福利计划 | cdm_benefitplan（未启用自定义字段支持） |    |     |
| 福利类型 | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>业务流程任务表

| Name | 表 |已知问题  | Status |
| --- | --- |   --------|----------   |
| 业务流程日历 | cdm_businessprocesscalendar | 751867 | 已解析 |
| 业务流程组分配 | cdm_businessprocessgroupassignment | 751869  751863 | 可用|
| 业务流程库任务组 | cdm_businessprocesslibrarytaskgroup |751866 | 已关闭 |
| 业务流程阶段 | cdm_businessprocessstage |      |     |
| 核对清单模板标题 | cdm_businessprocesstemplateheader |     |     |
| 核对清单模板任务 | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>薪酬表

| Name | 表 |已知问题  | Status |
| --- | --- | ----------      | -------    |
| 固定薪酬计划 | cdm_compensationfixedplan |754453 | 已关闭 |
| 薪酬网格 | cdm_compensationgrid |             |     |
| 薪酬级别 | cdm_compensationlevel |           |     |
| 薪酬付薪频率 | cdm_compensationpayfrequency |                  |     |
| 薪酬参考点设置 | cdm_compensationreferencepointsetup |               |     |
| 薪酬参考点设置行 | cdm_compensationreferencepointsetupline |             |     |
| 薪酬区域 | cdm_compensationregion |                   |     |
| 薪酬结构 | cdm_compensationstructure |    754456        | 已关闭    |
| 可变薪酬计划 | cdm_compensationvariableplan |               |     |
| 可变薪酬计划级别 | cdm_compensationvariableplanlevel |                |     |
| 可变薪酬计划类型 | cdm_compensationvariableplantype |               |     |
| 固定薪酬事件 | cdm_fixedcompensationevent |               |     |
| 股份行权规则 | cdm_vestingrule |              |     |
| 工作人员固定薪酬 | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>组织表

| Name | 表 |已知问题  | Status |
| --- | --- | ----------      | -------    |
| 部门 | cdm_department |  752194    | 已关闭    |
| 雇用 | cdm_employment | 762414  |  已关闭  |
| 公司 | cdm_company |  |     |
| 职务 | cdm_job |  |     |
| 工作职能 | cdm_jobfunction |        |     |
| 工作职位 | cdm_jobposition | 752214      | 已关闭    |
| 职位类型 | cdm_positiontype |            |     |
| 职位工作人员分配 | cdm_positionworkerassignmentmap | 752224    |  已关闭   |
| 工作职位维度 | cdm_jobpositiondimension|       |     |
| 工作类型 | cdm_jobtype |      |     |
| 语言 | cdm_language |        |     |
| 职位 | cdm_title |       |     |

> [!NOTE]
> **职位类型**、**职位工作人员分配** 和 **雇用** 的财务维度提供到 Dataverse 的单向集成。 财务维度更新现在不能从 Dataverse 同步到 Human Resources。 

## <a name="leave-and-absence-tables"></a>休假和缺勤表

| Name | 表 | 已知问题  | Status |
| --- | --- |   ----------      | -------    |
| 休假银行交易记录 | cdm_leavebanktransaction |  752252    |    已解析 |
| 休假登记 | cdm_leaveenrollment |  752934    |已关闭     |
| 休假计划 | cdm_leaveplan |   752232   |   已关闭  |
| 休假请求 | cdm_leaverequest | 753207     | 已关闭    |
| 休假请求详细信息 | cdm_leaverequestdetail | 753207     |   已关闭  |
| 休假类型 | cdm_leavetype |      |     |
| 休假类型原因代码 | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>只有在使用 **功能管理** 的 Microsoft Dynamics 365 Finance 中启用了 **在单个休假计划上配置多个休假类型** 功能时，使用 Dataverse 休假表和缺勤表的双重写入集成才可用。 

## <a name="payroll-tables"></a>工资表

| Name | 表 |已知问题  | Status |
| --- | --- |  ----------      | -------    |
| 付薪周期 | cdm_paycycle |    |     |
| 付薪期间 | cdm_payperiod |          |     |
| 工资单收入代码 | cdm_payrollearningcode |   754458        |   已关闭  |
| 银行帐户付款 | cdm_bankaccountdisbursement |    751904     |   已关闭  |
| 税区 | cdm_taxregion |          |     |

## <a name="worker-tables"></a>工作人员表

| Name | 表 |已知问题  | Status |
| --- | --- |----------      | -------    |
| 工作人员 | cdm_worker |    751906    |    已关闭 |
| 工作人员地址 | cdm_workeraddress |   754465     |已关闭     |
| 工作人员个人详细信息 | cdm_workerpersonaldetail |   751906     |   已关闭  |
| 工作人员标识号 | cdm_workerpersonidentificationnumber |  766704      |   已关闭  |
| 工作人员标识类型 | cdm_workerpersonidentificationtype |        |     |
| 工作日历 | cdm_workcalendar |        |     |
| 工作日历天 | cdm_workcalendarday |        |     |
| 工作日历的假日 |cdm_workcalendarholiday |        |     |
| 工作日历假期行 | cdm_workcalendarholidayline |        |     |
| 工作日历时间间隔 | cdm_workcalendartimeinterval（未启用自定义字段支持） |        |     |
| 工作人员银行帐户 | cdm_workerbankaccount |        |     |

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

![工作人员。](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>工作和工作职位

![工作和工作职位。](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>福利

![福利。](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>薪酬

![薪酬。](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>休假

![休假。](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>工作日历

![工作日历。](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>请参阅

[选择数据集成技术](hr-admin-integration-choose-technology.md)<br>
[配置 Dataverse 集成](hr-admin-integration-common-data-service.md)<br>
[配置 Dataverse 虚拟表](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources 虚拟表常见问题解答](hr-admin-virtual-entity-faq.md)<br>
[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)<br>
[术语更新](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
