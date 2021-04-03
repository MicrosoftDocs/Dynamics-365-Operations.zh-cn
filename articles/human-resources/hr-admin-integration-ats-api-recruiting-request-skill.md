---
title: 招聘请求技能
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求技能”实体。
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
ms.openlocfilehash: b0e6f4d2a38b092eb8460c5f5f4b8b6d290533a8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464662"
---
# <a name="recruiting-request-skill"></a>招聘请求技能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“招聘请求技能”实体。

物理名称：mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>说明

描述 RecruitingRequest 的技能要求。

### <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **招聘请求技能实体 ID**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | 只读<br>必填 | 系统生成的 **招聘请求技能** 记录的唯一标识符。 |
| **招聘请求 ID**<br>mshr_recruitingrequestid<br>*字符串* | 写入一次<br>必填 | 关联招聘请求的用户可读的唯一标识符。 |
| **招聘请求 ID 值**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | 只读<br>必填<br> 外键：mshr_hcmrecruitingrequestentity 实体的 mshr_hcmrecruitingrequestentityid | 系统生成的关联招聘请求的唯一标识符。 |
| **技能 ID**<br>mshr_skillid<br>*字符串*<br> | 写入一次<br>必填 | 所需技能的用户可读的唯一标识符。 |
| **技能 ID 值**<br>_mshr_fk_skill_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmskillentity 实体的 mshr_hcmskillentityid | 系统生成的所需技能的唯一标识符。 |
| **评级级别 ID**<br>mshr_ratinglevelid<br>*字符串* | 写入一次<br>可选 | 基于分配给技能的评级模型为工作选择的所需技能级别值。 |
| **评级级别 ID 值**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmratinglevelentity 实体的 mshr_hcmratinglevelentityid | 系统生成的级别的唯一标识符。 |
| **技能描述**<br>mshr_skilldescription<br>*字符串* | 只读<br>必填 | 技能描述。 |
| **评级级别描述**<br>mshr_ratingleveldescription<br>*字符串* | 只读<br>可选 | 所选技能级别的描述。 |
| **数据区域 ID**<br>mshr_dataareaid<br>*字符串* | 读/写<br>可选 | 指定法人（公司）。 |
| **数据区域 ID 值**<br>_mshr_dataareaid_id_value<br>*GUID* | 只读<br>可选<br>外键：cdm_company 实体的 cdm_companyid | 系统生成的标识法人（公司）的 GUID 值。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 招聘请求值和技能 ID 的串联，作为唯一标识记录的另一种方法。 |
| **评级模型 ID**<br>mshr_ratingmodelid<br>*字符串* | 读/写<br>必填 | 用于对技能评级的评级模型。 |
| **评级模型 ID 值**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmratingmodelentity 实体的 mshr_hcmratingmodelentityid | 系统生成的用于对技能进行评级的评级模型的唯一标识符。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]