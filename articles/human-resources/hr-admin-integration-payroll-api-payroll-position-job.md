---
title: 工资单职位工作
description: 本主题提供 Dynamics 365 Human Resources 中工资单职位工作实体的详细信息和示例查询。
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722623"
---
# <a name="payroll-position-job"></a>工资单职位工作

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的工资单职位工作实体。

### <a name="description"></a>说明

该实体为给定的固定薪酬计划提供职位和工作之间的关系。

物理名称：mshr_payrollpositionjobentity。

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **工作 ID**<br>mshr_jobid<br>*字符串* | 只读<br>必填 |工作的 ID。 |
| **生效日期**<br>mshr_validto<br>*日期/时间偏移* | 只读 <br>必填 | 职位和工作关系有效的开始日期。 |
| **失效日期**<br>mshr_validto<br>*日期/时间偏移* | 只读 <br>必填 | 职位和工作关系有效的结束日期。  |
| **职位 ID**<br>mshr_positionid<br>*字符串* | 只读<br>必填 | 职位的 ID。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 必填<br>系统生成的 |  |
| **职位工作 ID 值**<br>_mshr_fk_positionjob_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_payrollpositionjobentity 的 mshr_PayrollPositionJobEntity |与职位关联的工作的 ID。|
| **固定薪酬计划 ID 值**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_payrollfixedcompensationplanentity 的 mshr_FixedCompPlan_id  | 与职位关联的固定薪酬计划的 ID。 |
| **工资单职位工作实体 ID**<br>mshr_payrollpositionjobentityid<br>*GUID* | 必填<br>系统生成。 | 系统生成的用于唯一标识工作的 GUID 值。  |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**响应**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
