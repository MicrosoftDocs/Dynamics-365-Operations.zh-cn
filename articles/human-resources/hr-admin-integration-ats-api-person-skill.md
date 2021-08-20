---
title: 人员技能
description: 本主题介绍 Dynamics 365 Human Resources 的“人员技能”实体。
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
ms.openlocfilehash: d2721e3eace401537e85e57b5895d508317e6c4b71d481d15ff176b786a937e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756188"
---
# <a name="person-skill"></a>人员技能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员技能”实体。

物理名称：mshr_hcmpersonskillentity

## <a name="description"></a>说明

此实体描述应聘者的技能。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员技能实体 ID**<br>mshr_hcmpersonskillentityid<br>*GUID* | 只读<br>必填 | 系统生成的实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 |   关联当事方（人员）记录的 ID。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的当事方（人员）实体记录的标识符。 |
| **认证人**<br>mshr_certifier<br>*字符串* | 读/写<br>可选 | 证明此技能的工作人员的人员编号。 |
| **认证人 ID 值**<br>_mshr_fk_certifier_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmworkerentity 的 mshr_hcmworkerentityid | 系统生成的证明技能的工作人员的工人记录的唯一标识符。 |
| **技能 ID**<br>mshr_skillid<br>*字符串* | 读/写<br>必填 | Human Resources 中定义的技能的标识符。 |
| **技能 ID 值**<br>_mshr_fk_skill_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmskillentity 的 mshr_hcmskillentityid | 系统生成的所选技能的标识符。 |
| **年资**<br>mshr_yearsofexperience<br>*十进制* | 读/写<br>可选 | 应聘者具有此技能的年资。 |
| **评级 ID**<br>mshr_ratingid<br>*字符串* | 读/写<br>必填 | 评级级别类型。 对于此实体，值为 **技能**。 |
| **级别类型**<br>mshr_leveltype<br>*mshr_hrmskillleveltype 选项集* | 读/写<br>必填 | 分配给技能的级别的类型分类。 |
| **级别 ID**<br>mshr_levelid<br>*字符串* | 读/写<br>必填 | 应聘者对此技能所具有的评级级别的 ID。 |
| **评级级别 ID 值**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmratinglevelentity 的 mshr_hcmratinglevelentityid | 系统生成的评级级别的标识符。 |
| **级别日期**<br>mshr_leveldate<br>*日期/时间* | 读/写<br>必填 | 对应聘者进行技能评级的日期。 |
| **评级级别主考人**<br>mshr_ratinglevelexaminer<br>*字符串* | 读/写<br>可选 | 对应聘者进行评级的工作人员的人员编号。 |
| **评级级别主考人 ID 值**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmworkerentity 的 mshr_hcmworkerentityid | 系统生成的检查应聘者技能级别的工作人员的标识符。 |
| **已验证**<br>mshr_verified<br>*mshr_noyes 选项集* | 读/写<br>必填 | 指示评估的技能级别是否已得到验证。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录的标识符的字段。 当事方编号、级别类型、技能 ID 和级别日期的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]