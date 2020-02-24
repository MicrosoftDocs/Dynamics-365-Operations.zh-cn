---
title: 配置与 Finance 的集成
description: 本文介绍可用于从 Dynamics 365 Human Resources 和 Dynamics 365 Finance 集成的功能。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2e7070f627654c9eb889f3e0ee27e37681db0502
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008195"
---
# <a name="configure-integration-with-finance"></a>配置与 Finance 的集成

本文介绍可用于从 Dynamics 365 Human Resources 和 Dynamics 365 Finance 集成的功能。 [数据集成器](https://docs.microsoft.com/powerapps/administrator/data-integrator)随附的“Human Resources 到 Finance”模板可实现工作、职位和工作人员的数据流。 数据从 Human Resources 流向 Finance。 此模板不提供数据从 Finance 流回 Human Resources 的功能。 

![Human Resources 到 Finance 集成流](./media/TalentFinOpsFlow.png)

“Human Resources 到 Finance”解决方案提供以下类型的数据同步。 

- 在 Human Resources 中维护工作，并将其从 Human Resources 同步到 Finance。
- 在 Human Resources 中维护职位和职位分配，并将其从 Human Resources 同步到 Finance。
- 在 Human Resources 中维护雇用，并将其从 Human Resources 同步到 Finance。
- 在 Human Resources 中维护工作人员和工作人员地址，并将其从 Human Resources 同步到 Finance。

## <a name="system-requirements-for-human-resources"></a>Human Resources 的系统要求
此集成解决方案需要以下版本的 Human Resources 和 Finance： 
- Common Data Service 上的 Dynamics 365 Human Resources。
- Dynamics 365 Finance 版本 7.2 及更高版本。

## <a name="template-and-tasks"></a>模板和任务

若要访问模板，请执行以下操作。
1. 打开 [Power Apps 管理中心](https://admin.powerapps.com/)。 
1. 选择**项目**，然后在右上角，选择**新项目**以选择公共模板。 您需要为要集成到 Finance 中的每个法人创建一个新项目。

以下模板用于将 Human Resources 中的记录与 Finance 同步。

- **数据集成中的模板名称：** Human Resources（Human Resources Common Data Service 到 Finance）

  > [!NOTE]
  > 任务名称包含每个应用程序中使用的实体。 源 (Human Resources) 在左侧，目标 (Finance and Operations) 在右侧。

以下基础任务用于将 Human Resources 中的记录与 Finance 同步。
- 工作职能到补偿工作职能
- 部门到运营单位
- 工作类型到补偿工作类型
- 工作到工作
- 工作到工作详细信息
- 职位类型到职位类型
- 工作职位到基本职位
- 工作职位到职位详细信息
- 工作职位到职位持续时间
- 工作职位到职位层次结构
- 工作人员到工作人员
- 雇用到雇用
- 雇用到雇用详细信息
- 职位工作人员分配到职位工作人员分配
- 工作人员地址到工作人员邮寄地址 V2

## <a name="template-mappings"></a>模板映射

### <a name="job-functions-to-compensation-job-function"></a>工作职能到补偿工作职能

| Common Data Service 实体（源）                 | Finance and Operations 实体（目标） |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Function Name)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>部门到运营单位

| Common Data Service 实体（源）                           | Finance and Operations 实体（目标） |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>工作类型到补偿工作类型

| Common Data Service 实体（源）                   | Finance and Operations 实体（目标） |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>工作到工作

| Common Data Service 实体（源）                                           | Finance and Operations 实体（目标）           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>工作到工作详细信息

| Common Data Service 实体（源）                                             | Finance and Operations 实体（目标） |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Job Type (Job Type Name))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Job Function (Job Function Name)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid To)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Default Fulltime Equivalent)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>职位类型到职位类型

| Common Data Service 实体（源）                       | Finance and Operations 实体（目标） |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>工作职位到基本职位

| Common Data Service 实体（源）                           | Finance and Operations 实体（目标） |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>工作职位到职位详细信息

| Common Data Service 实体（源）                                                      | Finance and Operations 实体（目标）       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (Job Position Number)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Job (Name))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (Department (Department Number)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Position Type (Name))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Available for Assignment)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (Valid From)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (Valid To)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Fulltime Equivalent)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>工作职位到职位持续时间

| Common Data Service 实体（源）                             | Finance and Operations 实体（目标） |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (Calculated Activation) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (Calculated Retirement) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hiearchies"></a>工作职位到职位层次结构

| Common Data Service 实体（源）                                                                           | Finance and Operations 实体（目标） |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Valid From)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid   To)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>工作人员到工作人员
| Common Data Service 实体（源）                           | Finance and Operations 实体（目标）       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>雇用到雇用

| Common Data Service 实体（源）                                             | Finance and Operations 实体（目标） |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>雇用到雇用详细信息

| Common Data Service 实体（源）                                             | Finance and Operations 实体（目标）   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Valid   To)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>职位工作人员分配到职位工作人员分配

| Common Data Service 实体（源）                                             | Finance and Operations 实体（目标）   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (Job Position Number)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Valid   To)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>工作人员地址到工作人员邮寄地址 V2

| Common Data Service 实体（源）                                             | Finance and Operations 实体（目标）   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>集成注意事项
从 Human Resources 到 Finance 集成数据时，集成将尝试根据 ID 匹配记录。 如果发生匹配，Finance 中的数据将被 Human Resources 中的值覆盖。 但是，如果逻辑上这些记录是不同的，但根据各自的编号规则在 Human Resources 或 Finance 中生成了相同的 ID，则可能发生问题。

可能发生这种情况的区域是“工作人员”和“职位”区域，前者使用人员编号进行匹配。 工作不使用编号规则。 结果，如果 Human Resources 和 Finance 中同时存在同一个工作 ID，Human Resources 信息将覆盖 Dynamics 365 Finance 信息。 

为防止出现重复 ID 问题，您可以在[编号规则](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json)中添加前缀，或在编号规则中设置一个超出其他系统范围的开始编号。 

用于工作人员地址的位置 ID 不是编号规则的一部分。 将工作人员地址从 Human Resources 集成到 Finance 时，如果 Finance 中已经存在该工作人员地址，则可能会创建重复的地址记录。 

下图显示了数据集成器中的模板映射的一个示例。 

![模板映射](./media/IntegrationMapping.png)


