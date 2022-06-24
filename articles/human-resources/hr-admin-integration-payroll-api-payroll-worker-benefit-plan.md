---
title: 工资单工作人员福利计划
description: 本文提供 Dynamics 365 Human Resources 中工资单工作人员福利计划实体的详细信息和示例查询。
author: twheeloc
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef45855d9e60131ac065ae6e2769b71ae3f69537
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902276"
---
# <a name="payroll-worker-benefit-plan"></a>工资单工作人员福利计划


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的工资单工作人员福利计划实体。

物理名称：mshr_payrollworkerbenefitplanentities。

### <a name="description"></a>说明

此实体提供有关给定工作人员福利计划的信息。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员编号**</br>mshr_personnelnumber</br>*字符串* | 只读</br>必填 | 员工的唯一人员编号。 |
| **法人 ID**</br>mshr_legalentityID</br>*字符串* | 只读 | 指定法人（公司）。 |
| **期间 ID**</br>mshr_periodid</br>*字符串* | 只读 | 期间的标识符。 |
| **计划 ID**</br>mshr_planid</br>*字符串* | 只读 | 计划的标识符。 |
| **覆盖范围选项**</br>mshr_coverageoptionid</br>*字符串* | 只读 | 覆盖范围选项的标识。 |
| **扣缴开始日期**</br>mshr_deductionstartdatetime</br>*日期/时间偏移* | 只读 | 扣缴开始日期。 |
| **扣缴结束日期**</br>mshr_deductionenddatetime</br>*日期/时间偏移* | 只读 | 扣缴结束日期。 |
| **状态**</br>mshr_status</br>*[福利员工计划状态选项集](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | 只读 | 福利计划的状态。 |
| **生效日期**</br>mshr_validfrom</br>*日期/时间偏移* | 只读 | 此记录的生效时间。 |
| **失效日期**</br>mshr_validto</br>*日期/时间偏移* |  只读 | 此记录的失效时间。 |
| **计划类型 ID**</br>mshr_plantypeid</br>*字符串* | 只读 | 计划类型的标识符。 |
| **计划类型代码**</br>mshr_plantypecode</br>*[福利计划类型覆盖范围选项集](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | 只读 | 计划类型的详细说明。 |
| **付薪期间数**</br>mshr_payperiod</br>*整数* | 只读 | 代表福利提供商或员工的支付频率的支付期间数。 此数字将用于计算员工的年度福利薪金金额。 |
| **员工金额**</br>mshr_amountemployee</br>*十进制* | 只读 | 员工金额或百分比。 |
| **雇主金额**</br>mshr_amountemployer</br>*十进制* | 只读 | 雇主金额或百分比。 |
| **主要字段**</br>mshr_primaryfield</br>*字符串* | 系统生成的 | 主要字段。 |
| **工作人员 ID 值** </br>_mshr_fk_worker_id_value</br>*GUID* | 外键：mshr_hcmworkerbaseentity 实体的 mshr_hcmworkerbaseentityid。 | 系统生成的工作人员的唯一标识符。 |
| **期间 ID 值**</br> _mshr_fk_period_id_value</br>*GUID* | 外键：mshr_benefitperiodentity 实体的 mshr_benefitperiodentityid。 | 系统生成的期间的唯一标识符。 |
| **计划 ID 值**</br> _mshr_fk_plan_id_value</br>*GUID* | 外键：mshr_benefitplanentity 实体的 mshr_benefitplanentityid。 | 系统生成的计划的唯一标识符。 |
| **计划类型 ID 值**</br> _mshr_fk_plantype_id_value</br>*GUID* | 外键：mshr_benefitplantypeentity 实体的 mshr_benefitplantypeentityid。 | 系统生成的计划的唯一标识符。 |
| **覆盖范围选项 ID 值**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | 外键：mshr_benefitcoverageoptionentity 实体的 mshr_benefitcoverageoptionentityid。 | 系统生成的计划的唯一标识符。 |
| **工资单工作人员福利计划实体 ID 值**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | 只读 </br> 系统生成的 | 系统生成的记录的唯一标识符。 |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>工资单工作人员福利计划的查询示例

**请求**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**响应**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
