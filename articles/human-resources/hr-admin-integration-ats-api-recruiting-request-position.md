---
title: 招聘请求职位
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求职位”实体。
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
ms.openlocfilehash: 01d73d390f72343c7498ccbb99838d38be45a19e
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126018"
---
# <a name="recruiting-request-position"></a>招聘请求职位

本主题介绍 Dynamics 365 Human Resources 的“招聘请求职位”实体。

物理名称：mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>说明

描述要为招聘请求填补的职位。 向招聘请求添加职位是可选的。 职位的属性是只读的，因为职位属性在招聘请求中与在职位主记录中应该不会不同。 如果需要更改属性，应在将职位添加到招聘请求中之前在职位主记录上进行。

### <a name="json-representation"></a>JSON 表示
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **招聘请求职位实体 ID**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | 只读<br>必填 |    系统生成的招聘请求职位记录的标识符。 |
| **招聘请求 ID**<br>mshr_recruitingrequestid<br>*字符串* | 写入一次<br>必填 | 招聘请求的用户可读的唯一标识符。 |
| **招聘请求 ID 值**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmrecruitingrequestentity 实体的 mshr_hcmrecruitingrequestentityid | 系统生成的要将职位分配到的招聘请求的标识符。 |
| **职位 ID**<br>mshr_positionid<br>*字符串* | 写入一次<br>必填 | 职位的用户可读的唯一标识符。 |
| **职位 ID 值**<br>_mshr_fk_position_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmpositionv2entity 实体的 mshr_hcmpositionv2entityid | 系统生成的职位的标识符。 |
| **说明**<br>mshr_description<br>*字符串* | 只读<br>必填 | 职位描述。 |
| **职位类型 ID**<br>mshr_positiontypeid<br>*字符串* | 只读<br>可选 | 此职位的职位类型的用户可读的唯一标识符。 |
| **职位类型 ID 值**<br>_mshr_fk_positiontype_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmpositiontypeentity 实体的 mshr_hcmpositiontypeentityid | 系统生成的此职位的职位类型的唯一标识符。 |
| **状态**<br>mshr_status<br>*RecruitingRequestPositionStatus* 选项集 | 读/写<br>必填 | 招聘请求的职位的状态。 |
| **部门编号**<br>mshr_departmentnumber<br>*字符串* | 只读<br>可选<br> | 职位的部门编号。 |
| **部门 ID 值**<br>_mshr_fk_department_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_omdepartmententity 实体的 mshr_omdepartmententityid | 系统生成的职位的部门的唯一标识符。 |
| **直接上级职位 ID**<br>mshr_reportstopositionid<br>*字符串* | 只读<br>必填 | 招聘的职位在组织层次结构中向其报告的职位的用户可读 ID。 |
| **直接上级职位 ID 值**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmpositionv2entity 实体的 mshr_hcmpositionv2entityid | 系统生成的招聘的职位向其报告的职位的 ID。 |
| **直接上级人员编号**<br>mshr_reportstopersonnelnumber<br>*字符串* | 只读<br>必填 | 雇用的应聘者将向其报告的工作人员的工作人员 ID。 |
| **直接上级工作人员 ID 值**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmworkerbaseentity 实体的 mshr_hcmworkerbaseentityid | 系统生成的雇用的应聘者将向其报告的工作人员的 ID。 |
| **财务维度**<br>mshr_financialdimension<br>*字符串* | 只读<br>可选 | 分配给职位的财务维度（例如，成本中心）。 财务维度按法人为每个职位分配。 可通过 mshr_dimattributeomcostcenterentity 实体访问维度中定义的成本中心。 |
| **数据区域 ID**<br>mshr_dataareaid<br>*字符串* | 读/写<br>可选 | 指定招聘请求职位的法人（公司）。 |
| **数据区域 ID 值**<br>_mshr_dataareaid_id_value<br>*GUID* | 只读<br>可选<br>外键：cdm_company 实体的 cdm_companyid | 系统生成的标识招聘请求职位的法人（公司）的 GUID 值。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 招聘请求值和职位 ID 的串联，作为唯一标识记录的另一种方法。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]