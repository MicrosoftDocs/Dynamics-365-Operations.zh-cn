---
title: 职位的工资单详细信息
description: 本文提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。
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
ms.openlocfilehash: ac36b0386312e1631528b8ab5976db2cb3924caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904121"
---
# <a name="payroll-position"></a>工资单职位


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 中的工资单职位实体。

物理名称：mshr_payrollpositionentity。

### <a name="description"></a>说明

该实体为给定员工提供与职位相关的信息。

物理名称：mshr_payrollpositionentity。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **职位 ID**</br>mshr_positionid</br>*字符串* | 只读 | 职位的 ID。 |
| **付薪周期 ID**</br>mshr_paycycleid</br>*字符串* | 只读 | 针对职位定义的付薪周期。 |
| **年度常规时间(小时)**</br>annualregularhours</br>*小数* | 只读 | 针对职位上定义的年度常规小时。 |
| **由法人支付**</br>paidbylegalentity</br>*字符串* | 只读 | 针对负责签发付款的职位定义的法人。 |
| **失效日期**</br>validto</br>*日期/时间偏移* | 只读 | 位置详细信息有效的结束日期。 |
| **生效日期**</br>validfrom</br>*日期/时间偏移* | 只读 | 职位详细信息生效的开始日期。 |
| **主要字段**</br>mshr_primaryfield</br>*字符串* | 系统生成的 | 主要字段。 |
| **工资单职位详细信息实体 ID**</br>payrollpositiondetailsentityid</br>*GUID* | 必需</br>系统生成。 | 系统生成的用于唯一标识职位的全局唯一标识符 (GUID) 值。 |

## <a name="relations"></a>关系

| 属性值 | 相关实体 | 导航属性 | 集合类型 |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | 不适用 |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | 不适用 |

## <a name="example-query"></a>示例查询

**请求**

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

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
