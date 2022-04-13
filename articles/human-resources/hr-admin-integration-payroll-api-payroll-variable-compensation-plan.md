---
title: 工资单可变薪酬计划
description: 本主题提供 Dynamics 365 Human Resources 中工资单可变薪酬计划实体的详细信息和示例查询。
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5cc9e02ff2dd49e2eb0c8131fcff2eca4b9c3b1
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533638"
---
# <a name="payroll-variable-compensation-plan"></a>工资单可变薪酬计划


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的工资单可变薪酬计划实体。

### <a name="description"></a>说明

该实体提供为员工的给定职位分配的可变薪酬计划。

物理名称：mshr_payrollvariablecompensationawardentity。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员编号**</br>mshr_personnelnumber</br>*字符串* | 只读 | 员工的唯一人员编号。  |
| **奖励日期**</br>mshr_awarddate</br>*日期/时间偏移* | 只读 | 奖励的日期。 |
| **奖励类型**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType 选项集](hr-admin-integration-payroll-api-award-type.md)* | 只读 | 为可变薪酬计划定义的奖励的类型。 |
| **货币**</br>mshr_unitcurrencycode</br>*字符串* | 只读 |为可变薪酬计划定义的货币。   |
| **固定薪酬计划 ID**</br>mshr_fixedplanid</br>*字符串* | 只读 | 用作奖励计算基准的固定薪酬计划。 |
| **单位值**</br>mshr_awardamount</br>*十进制* | 只读 | 单位的值 |
| **流程类型**</br>mshr_processtype</br>*[mshr_hrmCompProcessType 选项集](hr-admin-integration-payroll-api-process-type.md)* | 只读 | 流程类型。 |
| **可变薪酬计划类型**</br>字符串</br>*mshr_typeid* | 只读 | 可变薪酬计划的类型。 |
| **可变薪酬计划 ID**</br>字符串</br>*mshr_planid* | 只读 | 可变薪酬计划的 ID。 |
| **单位数量**</br>十进制</br>*mshr_numberofunits* | 只读 | 奖励的单位数量。 |
| **主要字段**</br>mshr_primaryfield</br>*GUID* | 只读</br>系统生成。 | |
| **工资单可变薪酬计划实体**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识薪酬计划的 GUID 值。 |

## <a name="relations"></a>关系 

|属性值 | 相关实体 | 导航属性 | 集合类型 |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**响应**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
