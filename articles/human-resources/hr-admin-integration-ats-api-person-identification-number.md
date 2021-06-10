---
title: 人员标识号
description: 本主题介绍 Dynamics 365 Human Resources 的“人员标识号”实体。
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
ms.openlocfilehash: ef33e3922ca676b1312a3d60ae07aa2fe2828056
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055164"
---
# <a name="person-identification-number"></a>人员标识号

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员标识号”实体。

物理名称：mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>说明

此实体描述应聘者的标识号。 它让 API 使用者可以将标识号（如社会安全号或护照号）写入应聘者记录。 标识号显示在工作人员记录上，但不显示在应聘者记录上。 集成应用程序可以将值写入 Human Resources 数据库，但是在创建应聘者的工作人员记录之前，这些号码在 Human Resources 中不可见。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员标识号实体 ID**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | 只读<br>必填<br>系统生成 | 人员标识号记录的唯一主要标识符。 |
| **分录类型**<br>mshr_entrytype<br>*字符串* | 读/写<br>可选 | 引用标识号条目类型的自由值。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>可选 | 标识号的描述。 |
| **到期日期**<br>mshr_expirationdate<br>*日期/时间* | 读/写<br>可选 | 标识号或关联文档的到期日期。 |
| **是否为主要**<br>mshr_isprimary<br>*mshr_noyes 选项集* | 读/写<br>可选 | 定义标识号是否是此标识类型的人员的主要记录。 |
| **标识号**<br>mshr_identificationnumber<br>*字符串* | 读/写<br>必填 | 标识号。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 拥有标识号的当事方（人员）的标识符。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 实体的 mshr_dirpersonentityid | 当事方（人员）的唯一标识符。 |
| **标识类型 ID**<br>mshr_identificationtypeid<br>*字符串* | 读/写<br>必填 | 标识号的类型。 |
| **标识类型 ID 值**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmidentificationtypeentity 实体的 mshr_hcmidentificationtypeentityid | 系统生成的标识类型的唯一标识符。 |
| **签发机构 ID**<br>mshr_issuingagencyid<br>*字符串* | 读/写<br>可选 | 发放标识号的机构或组织。 |
| **签发机构 ID 值**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_hcmissuingagencyentity 实体的 mshr_hcmissuingagencyentityid | 系统生成的发放标识号的机构的唯一标识符。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录的标识符的字段。 当事方编号、标识类型 ID 和标识号的组合。 |
| **签发日期**<br>mshr_issuedate<br>*日期* | 读/写<br>可选 | 发放标识号的日期。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]