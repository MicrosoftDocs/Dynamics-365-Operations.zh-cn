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
ms.openlocfilehash: 349479d9e77861b54d879bcfd93f7af0e38cff95
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069824"
---
# <a name="payroll-position-job"></a>工资单职位工作


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的工资单职位工作实体。

### <a name="description"></a>说明

该实体为给定的固定薪酬计划提供职位和工作之间的关系。

物理名称：mshr_payrollpositionjobentity。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **职位 ID**</br>mshr_positionid</br>*字符串* | 只读 | 职位的 ID。 |
| **生效日期**</br>mshr_validto</br>*日期/时间偏移* | 只读 | 职位和工作关系生效的开始日期。 |
| **失效日期**</br>mshr_validto</br>*日期/时间偏移* | 只读 | 职位和工作关系有效的结束日期。 |
| **工作 ID**</br>mshr_jobid</br>*字符串* | 只读 | 工作的 ID。 |
| **主要字段**</br>mshr_primaryfield</br>*字符串* | 系统生成的 | 主要字段。 |
| **工资单职位工作实体 ID**</br>mshr_payrollpositionjobentityid</br>*GUID* | 系统生成。 | 系统生成的用于唯一标识作业的全局唯一标识符 (GUID) 值。 |

## <a name="relations"></a>关系

| 属性值 | 相关实体 | 导航属性 | 集合类型 |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | 不适用 |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

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
