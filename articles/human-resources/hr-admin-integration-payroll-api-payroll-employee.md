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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768183"
---
# <a name="payroll-employee"></a>工资单员工

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的工资单员工实体。

物理名称：mshr_payrollemployeeentity。

### <a name="description"></a>说明

该实体提供有关员工的信息。 在使用此实体之前，您必须设置[工资单集成参数](hr-admin-integration-payroll-api-parameters.md)。

>[!IMPORTANT] 
>**FirstName**、**MiddleName**、**LastName**、**NameValidFrom** 和 **NameValidTo** 字段在此实体上不再可用。 这将确保只有一个日期有效的数据源支持此实体。
>这些字段将在平台更新 43 中发布的 **DirPersonNameHistoricalEntity** 上可用。 **人员** 字段上存在从 **PayrollEmployeeEntity** 到 **DirPersonNameHistoricalEntity** 的 OData 关系。 

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员编号**<br>mshr_personnelnumber<br>*字符串* | 只读 | 员工的唯一人员编号。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>系统生成的 |  |
| **法人 ID**<br>mshr_legalentityID<br>*字符串* | 只读 | 指定法人（公司）。 |
| **性**<br>mshr_gender<br>[mshr_hcmpersongender 选项集](hr-admin-integration-payroll-api-gender.md) | 只读 | 员工的性别。 |
| **工资单员工实体 ID**<br>mshr_payrollemployeeentityid<br>*GUID* | 必填<br>系统生成的 | 系统生成的用于唯一标识员工的 GUID 值。 |
| **雇用开始日期**<br>mshr_employmentstartdate<br>*日期/时间偏移* | 只读 | 员工受雇用的开始日期。 |
| **标识类型 ID**<br>mshr_identificationtypeid<br>*字符串* |只读 | 针对员工定义的标识类型。 |
| **雇佣结束日期**<br>mshr_employmentenddate<br>*日期/时间偏移* | 只读 |员工受雇用的结束日期。  |
| **数据区域 ID**<br>mshr_dataareaid_id<br>*GUID* | 只读 <br>系统生成的 | 系统生成的标识法人（公司）的 GUID 值。 |
| **失效日期**<br>mshr_namevalidto<br>*日期/时间偏移* |  只读 | 员工信息有效的结束日期。 |
| **出生日期**<br>mshr_birthdate<br>*日期/时间偏移* | 只读 | 员工的出生日期 |
| **标识号**<br>mshr_identificationnumber<br>*字符串* | 只读 |针对员工定义的标识号。  |

## <a name="example-query-for-payroll-employee"></a>工资单员工的示例查询

**请求**

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
## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
