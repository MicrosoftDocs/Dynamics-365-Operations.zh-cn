---
title: 人员筛选
description: 本文介绍 Dynamics 365 Human Resources 的“人员筛选”实体。
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831882"
---
# <a name="person-screening"></a>人员筛选


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的“人员筛选”实体。

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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | Description |
| --- | --- | --- |
| **说明**<br>mshr_note<br>*字符串* | 读/写<br>可选 | 招聘经理和招聘人员使用的说明。 |
| **需求截止日期**<br>mshr_requiredby<br>*日期/时间* | 读/写<br>可选 | 要求在此之前完成筛选的日期。 |
| **状态**<br>mshr_status<br>*mshr_hcmcompletionstatus 选项集*|读/写<br>必填 | 提供用于筛选的应聘者状态。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 与应聘者关联的当事方（人员）编号。 |
| **筛选类型 ID**<br>mshr_screeningtypeid<br>*字符串* | 读/写<br>必填<br>外键：ScreeningType | Human Resources 中定义的筛选类型的标识符。 |
| **筛选类型 ID 值**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmscreeningtypeentity 的 mshr_hcmscreeningtypeentityid | 系统生成的关联实体中筛选类型记录的标识符。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* |  只读<br>必填 | 用作实体记录的标识符的字段。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的当事方（人员）实体记录的标识符。 |
| **人员筛选实体 ID**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | 只读<br>必填<br>系统生成| 人员筛选记录的唯一主要标识符。 |
| **完成日期**<br>mshr_completeddate<br>*日期/时间* | 读/写<br>可选 | 筛选完成的日期。 |


## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
