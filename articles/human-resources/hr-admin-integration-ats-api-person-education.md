---
title: 人员教育
description: 本主题介绍 Dynamics 365 Human Resources 的“人员教育”实体。
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
ms.openlocfilehash: c04a9c973e5a93b716889bdc0bb5f59ff5bbdd7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053747"
---
# <a name="person-education"></a>人员教育

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员教育”实体。

物理名称：mshr_hcmpersoneducationentity

## <a name="description"></a>说明

此实体包含作为应聘者的人员的教育历史。 教育将与个人记录关联，以让教育在除应聘者记录（工作人员、合同工等）之外还可与该人员创建的任何其他角色关联。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员教育实体 ID**<br>mshr_hcmpersoneducationentityid<br>*GUID* | 只读<br>必填 | 系统生成的人员教育实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 应聘者的当事方（人员）记录的唯一标识符。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的应聘者的人员记录的唯一标识符。 |
| **信用基础**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis 选项集* | 读/写<br>可选 | 教育程度的信用基础。 |
| **已完成信用数**<br>mshr_creditscompleted<br>*十进制* | 读/写<br>可选 | 教育已完成的信用数。 |
| **已获得信用数**<br>mshr_creditsearned<br>*十进制* | 读/写<br>可选 | 正在进行的学位的教育记录所获得的信用数。 |
| **所需信用数**<br>mshr_creditsneeded<br>*十进制* | 读/写<br>可选 | 正在进行的学位所需的信用数。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>可选 | 应聘者学位的描述。 |
| **教育程度 ID**<br>mshr_educationlevelid<br>*字符串* | 读/写<br>可选 | 教育程度的 ID。 | 
| **教育程度 ID 值**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmeducationdegreeentity 实体的 mshr_hcmeducationdegreeentityid | 系统生成的教育程度记录的标识符。 此标识符提供为组织定义的学位和教育程度。 |
| **教育学科 ID**<br>mshr_educationdisciplineid<br>*字符串* | 读/写<br>必填<br>外键：EducationDiscipline | 教育学科的 ID。 |
| **教育学科 ID 值**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmeducationdisciplineentity 的 mshr_hcmeducationdisciplineentityid | 系统生成的教育记录的教育学科的唯一标识符。 |
| **辅助强调**<br>mshr_secondaryemphasis<br>*字符串* | 读/写<br>可选 | 获得学位的辅助强调信息。 |
| **教育机构 ID**<br>mshr_educationinstitutionid<br>*字符串* | 读/写<br>可选 | 加入的教育机构的 ID。 |
| **教育机构 ID 值**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmeducationinstitutionentity 的 mshr_hcmeducationinstitutionentityid | 系统生成的教育机构的标识符。 |
| **开始日期**<br>mshr_startdate<br>*日期/时间* | 读/写<br>可选 | 所获得学位的教育的开始日期。 |
| **结束日期**<br>mshr_enddate<br>*日期/时间* | 读/写<br>必填 | 发放凭据的日期。 |
| **持续期**<br>mshr_duration<br>*十进制* | 读/写<br>可选 | 教育记录的持续时间。 |
| **持续时间单位**<br>mshr_durationunit<br>*mshr_periodunit 选项集* | 读/写<br>可选 | 与教育记录的持续时间关联的时间单位。 |
| **年级平均成绩**<br>mshr_gradepointaverage<br>*十进制* | 读/写<br>可选 | 学位获得的年级平均成绩。 |
| **年级量表**<br>mshr_gradescale<br>*字符串* | 读/写<br>可选 | 用于年级平均成绩的量表。 |
| **说明**<br>mshr_notes<br>*字符串* | 读/写<br>可选 | 招聘人员和招聘经理使用的说明。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录另一个主要标识符的字段。 当事方编号、教育学科 ID、教育机构 ID 和教育程度 ID 的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]