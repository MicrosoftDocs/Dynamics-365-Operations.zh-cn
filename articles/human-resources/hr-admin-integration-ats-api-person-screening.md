---
title: 人员筛选
description: 本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。
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
ms.openlocfilehash: 5129348f928fd709a5fabe73917522799a2d47e0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066285"
---
# <a name="person-screening"></a>人员筛选


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。

物理名称：mshr_hcmpersonscreeningentity

## <a name="description"></a>说明

此实体描述应聘者已通过或必须通过才能被雇用的筛选。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员筛选实体 ID**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | 只读<br>必填<br>系统生成 | 人员筛选记录的唯一主要标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 与应聘者关联的当事方（人员）编号。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的当事方（人员）实体记录的标识符。 |
| **筛选类型 ID**<br>mshr_screeningtypeid<br>*字符串* | 读/写<br>必填<br>外键：ScreeningType | Human Resources 中定义的筛选类型的标识符。 |
| **筛选类型 ID 值**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmscreeningtypeentity 的 mshr_hcmscreeningtypeentityid | 系统生成的关联实体中筛选类型记录的标识符。 |
| **需求截止日期**<br>mshr_requiredby<br>*日期/时间* | 读/写<br>可选 | 要求在此之前完成筛选的日期。 |
| **状态**<br>mshr_status<br>*mshr_hcmcompletionstatus 选项集*<br>读/写<br>必填 | 提供用于筛选的应聘者状态。 |
| **完成日期**<br>mshr_completeddate<br>*日期/时间* | 读/写<br>可选 | 筛选完成的日期。 |
| **说明**<br>mshr_note<br>*字符串* | 读/写<br>可选 | 招聘经理和招聘人员使用的说明。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
