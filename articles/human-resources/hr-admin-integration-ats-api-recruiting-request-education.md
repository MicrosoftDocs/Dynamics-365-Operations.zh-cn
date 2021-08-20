---
title: 招聘请求教育
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求教育”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 98c1ba139b7685286757d88ebd5cb99dae0573fb1ddd5c2e88eb3479b4283293
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759760"
---
# <a name="recruiting-request-education"></a>招聘请求教育

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“招聘请求教育”实体。

物理名称：mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>说明

描述 RecruitingRequest 的教育要求。

### <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **招聘请求教育实体 ID**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | 只读<br>必填 | 系统生成的招聘请求教育记录的唯一标识符。 |
| **招聘请求 ID**<br>mshr_recruitingrequestid<br>*字符串* | 写入一次<br>必填 | 相关招聘请求的用户可读的唯一标识符。 |
| **招聘请求 ID 值**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmrecruitingrequestentity 的 mshr_hcmrecruitingrequestentityid | 系统生成的相关招聘请求的唯一标识符。 |
| **教育程度 ID**<br>mshr_educationlevelid<br>*字符串* | 写入一次<br>必填 | 所需教育程度。 |
| **教育程度 ID 值**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmeducationlevelentity 的 mshr_hcmeducationlevelentityid | 系统生成的所需教育程度的唯一标识符。 |
| **教育程度描述**<br>mshr_educationleveldescription<br>*字符串* | 只读<br>必填 | 技能所需的教育程度的描述。 |
| **教育学科 ID**<br>mshr_educationdisciplinedescription<br>*字符串* | 写入一次<br>必填 | 教育学科所在的领域。 |
| **教育学科 ID 值**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmeducationdisciplineentity 的 mshr_hcmeducationdisciplineentityid | 系统生成的教育学科所在领域的唯一标识符。 |
| **教育学科描述**<br>mshr_educationdisciplinedescription<br>字符串 | 只读<br>必填 | 教育学科所在领域的描述。 |
| **数据区域 ID**<br>mshr_dataareaid<br>*字符串* | 读/写<br>可选 | 指定法人（公司）。|
| **数据区域 ID 值**<br>_mshr_dataareaid_id_value<br>*GUID* | 只读<br>可选<br>外键：cdm_company 实体的 cdm_companyid | 系统生成的标识法人（公司）的 GUID 值。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 招聘请求值、教育程度 ID 和教育学科 ID 的串联，作为唯一标识记录的另一种方法。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]