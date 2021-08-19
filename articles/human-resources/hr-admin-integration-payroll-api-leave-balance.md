---
title: 休假余额
description: 本主题提供 Dynamics 365 Human Resources 中休假余额实体的详细信息和示例查询。
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab136e9b40de280387dc3c5207a08a6bb357941feb3a8c736d9671f7850f2bf8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782675"
---
# <a name="leave-balance"></a>休假余额

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的休假余额实体。

### <a name="description"></a>说明

该实体为给定员工提供每种休假类型的休假余额。

物理名称：mshr_essleavebalanceentities。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员编号**</br>mshr_personnelnumber</br>*字符串* | 只读 | 员工的唯一人员编号。 |
| **当前余额**</br>mshr_balanceavailable</br>*十进制* | 只读 | 员工的当前余额。 |
| **类型**</br>mshr_balanceavailable</br>*字符串* | 只读 | 休假类型 ID。 |
| **增长率**</br>mshr_accrualratedescription</br> | 只读 | 假期额度费率。 |
| **上次结转的金额**</br>mshr_lastcarryforwardamount</br>*十进制* | 只读 | 上次结转的金额。 |
| **本年度所用**</br>mshr_takenthisyear</br>*十进制* | 只读 | 本年已休假期。 |
| **本年度总计**</br>mshr_totalthisyear</br>*十进制* | 只读 | 本年总金额。 |
| **数据区域 ID**</br>mshr_dataareaid_id</br>*字符串* | 只读 | 指定法人（公司）。 |
| **主要字段**</br>mshr_primaryfield</br>*GUID* | 只读</br>系统生成的 | |
| **休假类型 ID**</br>_mshr_fk_leavetype_id_value</br>*GUID* | 只读</br>外键：mshr_essleavetypeentity 实体的 mshr_essleavetypeentityid  | 休假类型 ID |
| **休假余额实体**</br>mshr_essleavebalanceentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识余额的 GUID 值。 |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**响应**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
