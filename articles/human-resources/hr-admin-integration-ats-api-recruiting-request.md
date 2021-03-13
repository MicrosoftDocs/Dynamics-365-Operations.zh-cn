---
title: 招聘请求
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求”实体。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 572ee0755e331d19b41442e3614effb92db95a92
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125417"
---
# <a name="recruiting-request"></a>招聘请求

本主题介绍 Dynamics 365 Human Resources 的“招聘请求”实体。

物理名称：mshr_hcmrecruitingrequestentity

### <a name="description"></a>说明

描述招聘工作的请求。

### <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **招聘请求 ID**<br>mshr_recruitingrequestid<br>*字符串* | 只读<br>必填<br>系统生成 | HR 应用程序中显示的请求的用户可读的唯一标识符。 编号规则。 |
| **招聘请求实体 ID**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | 只读<br>必填<br>系统生成 | 系统生成的用于唯一标识招聘请求的 GUID 值。 |
| **数据区域 ID**<br>mshr_dataareaid<br>*字符串* | 读/写<br>可选<br> | 指定招聘请求的法人（公司）。 |
| **数据区域 ID 值**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | 只读<br>可选<br>外键：cdm_company 实体的 cdm_companyid | 系统生成的标识招聘请求的法人（公司）的 GUID 值。 |
| **招聘经理人员编号**<br>mshr_hiringmanagerpersonnelnumber<br>*字符串* | 读/写<br>可选 | 与此招聘请求关联的招聘经理的人员编号。 |
| **招聘经理 ID 值**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmworkerbaseentity 实体的 mshr_hcmworkerbaseentityid | 系统生成的用于标识与招聘请求关联的经理的 GUID 值。 |
| **招聘人员方编号**<br>mshr_recruiterpartynumber<br>*字符串* | 读/写<br>可选 | 为请求选择的招聘人员的人员（当事方）编号。 |
| **招聘人员 ID 值**<br>_mshr_fk_recruiter_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_dirpersonentity 实体的 mshr_dirpersonentityid | 系统生成的用于标识与招聘请求关联的招聘人员的 GUID 值。 |
| **状态**<br>mshr_status<br>*RecruitingRequestStatus* 选项集 | 读/写<br>必填<br> | 指示招聘请求的状态。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 描述请求。 |
| **招聘请求位置 ID**<br>mshr_recruitingrequestlocationid<br>*字符串* | 读/写<br>可选 | 与此请求关联的工作位置的用户可读的唯一标识符。 |
| **招聘位置 ID 值**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmrecruitingrequestlocationentity 实体的 mshr_hcmrecruitingrequestlocationentityid | 系统生成的用于标识为请求选择的招聘请求位置的 GUID 值。 |
| **注释**<br>mshr_comments<br>*字符串* | 读/写<br>可选 | 供招聘经理和招聘人员使用的关于请求的注释。 |
| **工作 ID**<br>mshr_jobid<br>*字符串* | 写入一次<br>必填 |   由与此请求关联的所有职位共享的工作的用户可读唯一标识符。 |
| **工作 ID 值**<br>_mshr_fk_job_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmjobentity 实体的 mshr_hcmjobentityid | 系统生成的由与招聘请求关联的所有职位共享的工作的唯一标识符。 |
| **职务 ID**<br>mshr_titleid<br>*字符串* | 只读<br>必填 | 与此请求关联的职务的用户可读的唯一标识符。 |
| **职务 ID 值**<br>_mshr_fk_title_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmtitleentity 实体的 mshr_hcmtitleid | 系统生成的为招聘请求选择的工作的职务的唯一标识符。 |
| **工作职能 ID**<br>mshr_jobfunctionid<br>*字符串* | 只读<br>必填<br>外键：mshr_hcmjobfunctionentity 实体的 mshr_jobfunctionid | 与此请求关联的工作职能的用户可读的唯一标识符。 |
| **默认全职等效**<br>mshr_defaultfulltimeequivalency<br>*双精度* | 只读<br>必填 | 工作的全职等效值，其中 1.0 表示全职工作人员。 |
| **监管工作类别**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory* 选项集 | 只读<br>可选 | 为工作选择的工作职能的 EEO 工作类别。 有效值包含在 HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) 选项集中。 |
| **工作类型 ID**<br>mshr_jobtypeid<br>*字符串* | 只读<br>可选 | 与职位关联的工作的类型。 工作类型是用户定义的值，在 mshr_hcmjobtypeentity 实体中提供。 |
| **工作类型 ID 值**<br>_mshr_fk_jobtype_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmjobtypenentity 实体的 mshr_hcmjobtypeentityid | 系统生成的与招聘请求的工作关联的工作类型的唯一标识符。 |
| **免税状态**<br>mshr_exemptstatus<br>*JobExemptStatus* 选项集 | 只读<br>可选 | 基于工作类型的 FLSA 免除情况。 |
| **估计的开始日期**<br>mshr_estimatedstartdate<br>*日期* | 读/写<br>必填 | 应聘者将开始工作的估计日期。 |
| **外部描述**<br>mshr_externaldescription<br>*字符串* | 读/写<br>可选 | 面向应聘者的工作/职位描述。 | 薪酬低阈值<br>mshr_compensationlowthreshold<br>*双精度* | 读/写<br>可选 | 薪酬级别的下限。 |
| **薪酬控制点**<br>mshr_compensationcontrolpoint<br>*双精度* | 读/写<br>可选 | 薪酬级别的控制点。 |
| **薪酬高阈值**<br>mshr_compensationhighthreshold<br>*双精度* | 读/写<br>可选 | 薪酬级别的上限。 |
| **薪酬级别**<br>mshr_compensationlevelid<br>*字符串* | 读/写<br>可选 | 工作的薪酬级别。 工作可以设置多个薪酬级别。 此属性指示为此请求选择的工作薪酬级别。 |
| **工作薪酬 ID**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmjobcompensationentity 实体的 mshr_hcmjobcompensationentityid | 系统生成的与招聘请求的工作关联的薪酬级别的唯一标识符。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)
