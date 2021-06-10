---
title: 工资单员工
description: 本主题提供 Dynamics 365 Human Resources 中工资单员工实体的详细信息和示例查询。
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
ms.openlocfilehash: 87efbf7063de373e1e0b844ff1b942cdaab4a021
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055044"
---
# <a name="payroll-employee"></a>工资单员工

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题提供 Dynamics 365 Human Resources 中工资单员工实体的详细信息和示例查询。

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员编号**<br>mshr_personnelnumber<br>*字符串* | 只读<br>必填 | 员工的唯一人员编号。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 必填<br>系统生成的 |  |
| **姓**<br>mshr_lastname<br>*字符串* | 只读<br>必填 | 员工姓氏。 |
| **法人 ID**<br>mshr_legalentityID<br>*字符串* | 只读<br>必填 | 指定法人（公司）。 |
| **生效日期**<br>mshr_namevalidfrom<br>*日期/时间偏移* | 只读 <br>必填 | 员工信息有效的开始日期。  |
| **性**<br>mshr_gender<br>*Int32* | 只读<br>必填 | 员工的性别。 |
| **工资单员工实体 ID**<br>mshr_payrollemployeeentityid<br>*GUID* | 必填<br>系统生成的 | 系统生成的用于唯一标识员工的 GUID 值。 |
| **雇用开始日期**<br>mshr_employmentstartdate<br>*日期/时间偏移* | 只读<br>必填 | 员工受雇用的开始日期。 |
| **标识类型 ID**<br>mshr_identificationtypeid<br>*字符串* |只读<br>必填 | 针对员工定义的标识类型。 |
| **雇佣结束日期**<br>mshr_employmentenddate<br>*日期/时间偏移* | 只读<br>必填 |员工受雇用的结束日期。  |
| **数据区域 ID**<br>mshr_dataareaid_id<br>*GUID* | 必填 <br>系统生成的 | 系统生成的标识法人（公司）的 GUID 值。 |
| **失效日期**<br>mshr_namevalidto<br>*日期/时间偏移* |  只读<br>必填 | 员工信息有效的结束日期。 |
| **出生日期**<br>mshr_birthdate<br>*日期/时间偏移* | 只读 <br>必填 | 员工的出生日期 |
| **标识号**<br>mshr_identificationnumber<br>*字符串* | 只读 <br>必填 |针对员工定义的标识号。  |
| **名**<br>mshr_firstname<br>*字符串* | 只读<br>必填 | 员工名字。 |
| **中间名**<br>mshr_middlename<br>*字符串* | 只读<br>必填 |员工中间名。  |

## <a name="example-query-for-payroll-employee"></a>工资单员工的示例查询

**申请**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**响应**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
