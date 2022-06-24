---
title: 工资单固定薪酬计划
description: 本文提供 Dynamics 365 Human Resources 中工资单固定薪酬计划实体的详细信息和示例查询。
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909837"
---
# <a name="payroll-fixed-compensation-plan"></a>工资单固定薪酬计划


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的工资单固定薪酬计划实体。

### <a name="description"></a>说明

该实体提供为员工的给定职位分配的固定薪酬计划。

物理名称：mshr_payrollfixedcompensationplanentity。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **计划 ID**</br>mshr_planid</br>*字符串* | 只读 | 指定薪酬计划。  |
| **人员编号**</br>mshr_personnelnumber</br>*字符串* | 只读 | 员工的唯一人员编号。 |
| **付薪比率**</br>mshr_payrate</br>*十进制* | 只读 | 在固定薪酬计划中定义的付薪比率。 |
| **职位 ID**</br>mshr_positionid</br>*字符串* | 只读 | 与员工和固定薪酬计划登记关联的职位 ID。 |
| **生效日期**</br>mshr_validfrom</br>*日期/时间偏移* |  只读 | 员工固定薪酬有效的开始日期。  |
| **失效日期**</br>mshr_validto</br>*日期/时间偏移* | 只读 | 员工固定薪酬有效的结束日期。 |
| **付薪频率**</br>mshr_payfrequency</br>*字符串* | 只读 | 给定付薪比率的[薪酬付薪频率](hr-admin-integration-payroll-api-compensation-pay-frequency.md)的 ID。 |
| **货币**</br>mshr_currency</br>*字符串* | 只读 | 针对固定薪酬计划定义的货币。 |
| **工资单固定薪酬计划实体**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识薪酬计划的 GUID 值。 |

## <a name="relations"></a>关系

|属性值 | 相关实体 | 导航属性 | 集合类型 |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**响应**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
