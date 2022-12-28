---
title: 配置与 Dataverse 表的集成
description: 本文介绍 Microsoft Dynamics 365 Human Resources 与 Dataverse 之间的集成。
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838619"
---
# <a name="configure-integration-with-dataverse-tables"></a>配置与 Dataverse 表的集成

>[!Important]
>本文中说明的功能当前对财务和运营基础结构上的 Dynamics 365 Human Resources 客户可用。 


要将 Microsoft Dynamics 365 Human Resources 与 Dataverse 集成，您可以使用[数据集成器](/powerapps/administrator/data-integrator)。 “Human Resources 到 Dataverse”模板使工作、职位、员工和其他人的数据能够从 Human Resources 流入 Dataverse，并从 Dataverse 流入 Human Resources，从而在两个系统中创建写入。

## <a name="system-requirements-for-human-resources"></a>Human Resources 的系统要求

此集成解决方案需要以下版本的 Human Resources 和 Dynamics 365 Finance： 

- Dynamics 365 Finance 版本 7.2 及更高版本
- 其中已创建数据库并允许使用 Dynamics 365 应用的 Dynamics CRM 环境

## <a name="template-and-tasks"></a>模板和任务

按照以下步骤访问“Human Resources 到 Finance”模板。

1. 打开 [Power Apps 管理中心](https://admin.powerapps.com/)。 
2. 在您的环境下，选择 **Dynamics 365 应用**，然后选择工具栏上的 **应用源** 。
3. 安装模板，请搜索“双重写入 Human Resources”，或直接转到以下地址：<https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>。
3. 安装完成后，打开 Dynamics 365 Finance。
4. 打开 **数据管理** 工作区。 
5. 选择 **双重写入**。 
6. 执行用于为您组织中的至少一家公司链接您的环境的过程。 
7. 设置完指向您的 Dataverse 环境的链接后，选择 **应用解决方案**。 解决方案已应用，映射已安装到集成器应用中。

## <a name="template-mappings"></a>模板映射

在以下模板映射表中，任务名称指明每个应用程序中使用的实体。 Finance 在左边， Dataverse 在右边。

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>银行帐户支付（双重写入）到银行帐户支付

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| 金额                         | cdm\_amount                                         |
| PRIORITY                       | cdm\_disbursementpriority                           |
| PERSONNELNUMBER                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| REMAINDER                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>福利计算比率详细信息（双重写入）到福利计算比率详细信息

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| EFFECTIVE                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| EXPIRATION                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| 名称                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>福利计算比率标头到福利计算比率

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| 名称                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>福利选项到福利选项

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>福利类型到福利类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| 描述                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>业务日历到业务流程日历

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| 名称                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>业务流程到业务流程标头

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| 名称                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| 状态                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>业务流程库任务组到业务流程库任务组

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| 名称                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>业务流程阶段到业务流程阶段

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| 名称                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>业务流程任务到业务流程任务

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| INSTRUCTIONS                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| 名称                           | cdm\_name                                           |
| 状态                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>业务流程模板到核对清单模板标题

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| 名称                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| PERSONNELNUMBER                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>业务流程模板任务到核对清单模板任务

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| 名称                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| 描述                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| INSTRUCTIONS                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>计算频率到福利计算频率

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>计算频率付薪期间到福利计算频率付薪期间

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>日历到工作日历

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>薪酬固定操作表到固定薪酬事件

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ACTION                         | cdm\_name                                           |
| ACTIVE                         | cdm\_isactive                                       |
| 描述                    | cdm\_description                                    |
| 类型                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>薪酬固定计划到薪酬固定计划

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PLAN                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| 类型                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| 币种                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>薪酬网格到薪酬网格

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| 类型                           | cdm\_type                                           |
| 币种                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>薪酬工作职能到工作职能

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| 描述                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>薪酬工作类型到工作类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>薪酬付薪频率到薪酬付薪频率

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| PERIOD                         | cdm\_period                                         |
| 描述                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>薪酬地区到薪酬区域

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| 位置                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>可变薪酬计划 V2 到可变薪酬计划

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| 描述                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>可变薪酬类型到可变薪酬计划类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| 类型                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>薪酬股份行权规则到股份行权规则

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| 注释                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>部门 V2 到部门

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| 名称                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>双重写入税区到税区

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| CITY                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| COUNTY                         | cdm\_county                                         |
| STATE                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>双重写入工作人员标识到工作人员标识号

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>薪酬结构到薪酬结构

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 金额                         | cdm\_amount                                         |
| GRID                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>收入代码到工资单收入代码

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>员工固定薪酬到工作人员固定薪酬

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| 类型                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| PLAN                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| ACTION                         | cdm\_eventid.cdm\_name                               |
| STEP                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>每个公司的雇用到雇用

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>所属种族到所属种族

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| 描述                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>业务流程组分配到组分配

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 名称                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>标识类型到工作人员标识类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>签发机构到人员身份证明签发机构

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 电子邮件                          | cdm\_email                                          |
| EXTENSION                      | cdm\_extension                                      |
| FAX                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| 名称                           | cdm\_description                                    |
| PAGER                          | cdm\_pager                                          |
| 短信                            | cdm\_sms                                            |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>工作职位双重写入到工作职位

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| ACTIVATION                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| 描述                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| 退休                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>工作双重写入到工作

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>语言代码到语言

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| 描述                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>休假和缺勤银行交易记录 V2 到休假银行交易记录

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 金额                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>休假和缺勤登记 V2 到休假登记

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>休假和缺勤计划 V2 到休假计划

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| 名称                           | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>休假和缺勤类型到休假类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| 类型                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>休假和缺勤类型原因代码到休假类型原因代码

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>休假请求详细信息到休假请求详细信息

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 金额                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| 类型                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>休假请求标题到休假请求

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| 状态                         | cdm\_status                                         |
| COMMENT                        | cdm\_comment                                        |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>级别到薪酬级别

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 类型                           | cdm\_type                                           |
| 描述                    | cdm\_description                                    |
| LEVEL                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>入职流程标题到入职流程标题

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>付薪周期到付薪周期

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>付薪期间到付薪期间

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| 状态                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>职位的工资单明细到工资单职位详细信息

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>职位默认维度双重写入到工作职位维度

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>职位类型到职位类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| CLASSIFICATION                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>职位工作人员分配 V2 到职位工作人员分配

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>原因代码到原因代码

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>参考点设置行（双重写入）到薪酬参考点设置行

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| 描述                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>参考点设置到薪酬参考点设置

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| 类型                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>技能类型到技能类型

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| 描述                    | cdm\_description                                    |

### <a name="titles-to-title"></a>标题到标题

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>可变薪酬级别 V2 到可变薪酬计划级别

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>退伍军人身份到退伍军人身份

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| 描述                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>工作日历注册到工作日历注册

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| PERSONNELNUMBER                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>工作日历假日到工作日历假日

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ID                             | cdm\_name                                           |
| 描述                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>工作日历假日行到工作日历假日行

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| 名称                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>工作人员到工作人员

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| GENDER                         | cdm\_gender                                         |
| BIRTHDATE                      | cdm\_birthdate                                      |
| 名称                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>工作人员银行帐户到工作人员银行帐户

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| 电子邮件                          | cdm\_email                                          |
| EXTENSION                      | cdm\_extension                                      |
| FAX                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| 名称                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>工作人员个人详细信息到工作人员个人详细信息

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| BIRTHDATE                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| GENDER                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| EDUCATION                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>工作人员邮寄地址双重写入到工作人员地址

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| EFFECTIVE                      | cdm\_effectivedate                                  |
| EXPIRATION                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>工作时间到工作日历时间间隔

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>工作时间到工作日历日

| 财务实体                 | Dataverse 表                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>集成注意事项

- 对任一系统中的数据所做的所有更改都将由另一个系统进行验证。 如果发生故障，数据将不会写入任何一个系统。 
- 所有写入都受数据默认设置的约束（如果自定义逻辑出现在 Finance 中）。
- 双重写入集成器应用使用集成键在两个系统之间进行映射。 有时，很难选择正确的集成键，尤其是当多个集成键满足要求时。 为帮助做出此选择，下表列出了建议的映射集成键。

| Dataverse 表                          | 集成密钥 |
|------------------------------------------|------------------|
| 银行帐户付款                | cdm\_bankaccountid.cdm\_accountidentification、cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber、cdm\_companyid.cdm\_companycode |
| 福利计算频率            | cdm\_name |
| 福利计算频率付薪期间 | cdm\_payperiodid.cdm\_periodstartdate、cdm\_payperiodid.cdm\_paycycleid.cdm\_name、cdm\_benefitcalculationfrequencyid.cdm\_name |
| 福利计算比率                 | cdm\_name |
| 福利计算比率详细信息          | cdm\_workerdeduction、cdm\_effective、cdm\_calculationrateid.cdm\_name |
| 福利选项                           | cdm\_name |
| 福利类型                             | cdm\_name |
| 业务流程日历                | cdm\_name |
| 业务流程组分配        | cdm\_name |
| 业务流程标头                  | cdm\_processid |
| 业务流程库任务组      | cdm\_processtype、cdm\_name |
| 业务流程阶段                   | cdm\_name、cdm\_businessprocesstype、cdm\_companyid.cdm\_companycode |
| 业务流程任务                    | cdm\_taskid |
| 业务单位                            | |
| 核对清单模板标题                | cdm\_businessprocesstype、cdm\_name、cdm\_genericsubtype |
| 核对清单模板任务                  | cdm\_taskid |
| 公司                                  | cdm\_companycode |
| 固定薪酬计划                  | cdm\_name、cdm\_company.cdm\_companycode |
| 薪酬网格                        | cdm\_name、cdm\_companyid.cdm\_companycode |
| 薪酬级别                       | cdm\_name |
| 薪酬付薪频率               | cdm\_name、cdm\_companyid.cdm\_companycode |
| 薪酬参考点设置       | cdm\_name、cdm\_companyid.cdm\_companycode |
| 薪酬参考点设置行  | cdm\_name、cdm\_referencepointsetupid.cdm\_name、cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| 薪酬区域                      | cdm\_name |
| 薪酬结构                   | cdm\_compensationlevelid.cdm\_name、cdm\_referencepointid.cdm\_name、cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name、cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode、cdm\_companyid.cdm\_companycode、cdm\_compensationgridid.cdm\_name、cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| 可变薪酬计划               | cdm\_name、cdm\_companyid.cdm\_companycode |
| 可变薪酬计划级别         | cdm\_companyid.cdm\_companycode、cdm\_compensationvariableplanid.cdm\_name、cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode、cdm\_compensationlevelid.cdm\_name |
| 可变薪酬计划类型          | cdm\_name、cdm\_companyid.cdm\_companycode |
| 币种                                 | isocurrencycode |
| 部门                               | cdm\_departmentnumber |
| 雇用                               | cdm\_employmentstartdate、cdm\_workerid.cdm\_workernumber、cdm\_companyid.cdm\_companycode |
| 所属种族                            | cdm\_name |
| 固定薪酬事件                 | cdm\_name、cdm\_companyid.cdm\_companycode |
| 职务                                      | cdm\_name |
| 工作职能                             | cdm\_name |
| 工作职位                             | cdm\_jobpositionnumber |
| 工作职位维度                   | cdm\_jobpositionid.cdm\_jobpositionnumber、cdm\_companyid.cdm\_companycode |
| 工作类型                                 | cdm\_name |
| 语言                                 | cdm\_name |
| 休假银行交易记录                   | cdm\_transactiondate、cdm\_transactiontype、cdm\_transactionnumber、cdm\_leavetypeid.cdm\_type、cdm\_leavetypeid.cdm\_companyid.cdm\_companycode、cdm\_companyid.cdm\_companycode、cdm\_workerid.cdm\_workernumber |
| 休假登记                         | cdm\_startdate、cdm\_leaveplanid.cdm\_name、cdm\_leaveplanid.cdm\_companyid.cdm\_companycode、cdm\_companyid.cdm\_companycode、cdm\_workerid.cdm\_workernumber |
| 休假计划                               | cdm\_name、cdm\_companyid.cdm\_companycode |
| 休假请求                            | cdm\_leaverequestnumber、cdm\_companyid.cdm\_companycode |
| 休假请求详细信息                     | cdm\_leavedate、cdm\_leavetypeid.cdm\_type、cdm\_leavetypeid.cdm\_companyid.cdm\_companycode、cdm\_leaverequestid.cdm\_leaverequestnumber、cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| 休假类型                               | cdm\_type、cdm\_companyid.cdm\_companycode |
| 休假类型原因代码                   | cdm\_reasoncodeid.cdm\_name、cdm\_typeid.cdm\_type、cdm\_typeid.cdm\_companyid.cdm\_companycode |
| 入职流程标头                   | cdm\_processheaderid.cdm\_processid |
| 组织                             | |
| 付薪周期                                | cdm\_name |
| 付薪期间                               | cdm\_periodstartdate、cdm\_paycycleid.cdm\_name、cdm\_periodenddate |
| 工资单收入代码                     | cdm\_name |
| 工资单职位详细信息                  | cdm\_validfrom、cdm\_validto、cdm\_position.cdm\_jobpositionnumber |
| 人员身份证明签发机构     | cdm\_name |
| 职位类型                            | cdm\_name |
| 职位工作人员分配               | cdm\_validfrom、cdm\_jobpositionid.cdm\_jobpositionnumber |
| 原因代码                              | cdm\_name |
| 技能类型                               | cdm\_name |
| 税区                               | cdm\_stateorprovince、cdm\_name、cdm\_countryorregion、cdm\_county、cdm\_city |
| 团队                                     | azureactivedirectoryobjectid、membershiptype |
| 标题                                    | cdm\_name |
| 用户                                     | azureactivedirectoryobjectid |
| 股份行权规则                             | cdm\_name、cdm\_companyid.cdm\_companycode |
| 退伍军人状态                           | cdm\_name |
| 工作日历                            | cdm\_name、cdm\_companyid.cdm\_companycode |
| 工作日历天                        | cdm\_calendardate、cdm\_companyid.cdm\_companycode、cdm\_workcalendarid.cdm\_name、cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| 工作日历登记                 | cdm\_employmentid.cdm\_employmentstartdate、cdm\_employmentid.cdm\_workerid.cdm\_workernumber、cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| 工作日历的假日                    | cdm\_name |
| 工作日历假期行               | cdm\_holidaydate、cdm\_workcalendarholidayid.cdm\_name |
| 工作日历时间间隔              | cdm\_starttime、cdm\_workcalendardayid.cdm\_calendardate、cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode、cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name、cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode、cdm\_companyid.cdm\_companycode、cdm\_workcalendarid.cdm\_name、cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| 工作人员                                   | cdm\_workernumber |
| 工作人员地址                           | cdm\_addressnumber、cdm\_addresstype、cdm\_workerid.cdm\_workernumber |
| 工作人员银行帐户                      | cdm\_accountidentification、cdm\_workerid.cdm\_workernumber |
| 工作人员固定薪酬                | cdm\_linenumber、cdm\_effectivedate、cdm\_companyid.cdm\_companycode、cdm\_positionid.cdm\_jobpositionnumber、cdm\_workerid.cdm\_workernumber、cdm\_eventid.cdm\_name、cdm\_eventid.cdm\_companyid.cdm\_companycode、cdm\_planid.cdm\_name、cdm\_planid.cdm\_company.cdm\_companycode |
| 工作人员标识号      | cdm\_identificationnumber、cdm\_workerid.cdm\_workernumber、cdm\_identificationtypeid.cdm\_name |
| 工作人员标识类型        | cdm\_name |
| 工作人员个人详细信息                   | cdm\_workerid.cdm\_workernumber |
