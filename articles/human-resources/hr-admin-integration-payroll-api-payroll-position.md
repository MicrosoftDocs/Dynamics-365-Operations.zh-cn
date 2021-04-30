---
title: 职位的工资单详细信息
description: 本主题提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881932"
---
# <a name="payroll-position"></a>工资单职位

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **年度常规时间(小时)**<br>annualregularhours<br>*十进制* | 只读<br>必填 | 在职位上定义的年度常规小时。  |
| **工资单职位详细信息实体 ID**<br>payrollpositiondetailsentityid<br>*GUID* | 必填<br>系统生成。 | 系统生成的用于唯一标识职位的 GUID 值。  |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 必填<br>系统生成的 |  |
| **职位工作 ID 值**<br>_mshr_fk_positionjob_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_payrollpositionjobentity 的 mshr_PayrollPositionJobEntity |与职位关联的工作的 ID。|
| **固定薪酬计划 ID 值**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_payrollfixedcompensationplanentity 的 mshr_FixedCompPlan_id  | 与职位关联的固定薪酬计划的 ID。 |
| **付薪周期 ID**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 在职位上定义的付薪周期。 |
| **由法人支付**<br>paidbylegalentity<br>*字符串* | 只读<br>必填 | 在负责签发付款的职位上定义的法人。 |
| **职位 ID**<br>mshr_positionid<br>*字符串* | 只读<br>必填 | 职位的 ID。 |
| **失效日期**<br>validto<br>*日期/时间偏移* | 只读<br>必填 |位置详细信息有效的开始日期。  |
| **生效日期**<br>validfrom<br>*日期/时间偏移* | 只读<br>必填 |位置详细信息有效的结束日期。  |

**查询**

**申请**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**响应**

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
