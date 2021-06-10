---
title: 人员证书
description: 本主题介绍 Dynamics 365 Human Resources 的“人员证书”实体。
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055188"
---
# <a name="person-certificate"></a>人员证书

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员证书”实体。

物理名称：mshr_hcmpersoncertificateentity

## <a name="description"></a>说明

此实体描述应聘者的专业证书。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员证书实体 ID**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | 只读<br>必填 | 系统生成的人员证书实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 应聘者的当事方（人员）ID。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的当事方（人员）实体记录的标识符。 |
| **证书类型 ID**<br>mshr_certificatetypeid<br>*字符串* | 读/写<br>必填 |  Human Resources 中定义的证书类型的标识符。 |
| **证书类型 ID 值**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmcertificatetypeentity 的 mshr_hcmcertificatetypeentityid | 系统生成的关联实体中证书类型的唯一标识符。 |
| **开始日期**<br>mshr_startdate<br>*日期/时间* | 读/写<br>必填 | 颁发证书的日期。 |
| **结束日期**<br>mshr_enddate<br>*日期/时间* | 读/写<br>可选 | 证书到期的日期。 |
| **说明**<br>mshr_notes<br>*字符串* | 读/写<br>可选 | 招聘经理和招聘人员使用的说明。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 |  用作实体记录的标识符的字段。 当事方编号、证书类型 ID 和开始日期的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]