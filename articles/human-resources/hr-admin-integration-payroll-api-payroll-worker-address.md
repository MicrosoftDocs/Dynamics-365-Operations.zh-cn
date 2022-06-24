---
title: 工资单工作人员地址
description: 本文提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。
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
ms.openlocfilehash: 683994b24113b8c2017f1bb3c1055e7e0f0eb75e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901109"
---
# <a name="payroll-worker-address"></a>工资单工作人员地址


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的工资单工作人员地址实体。

物理名称：mshr_payrollworkeraddressentity。

### <a name="description"></a>说明

该实体为给定员工提供工资单居住地址和工资单工作地点。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员编号**</br>mshr_personnelnumber</br>*字符串* | 只读 | 员工的唯一人员编号。 |
| **位置 ID**</br>mshr_locationidbr>*String* | 只读 | 地址的 ID。 |
| **家庭地址**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes 选项集](hr-admin-integration-payroll-api-no-yes.md)* | 只读 | 一个指示地址是否为员工居住地的值。 |
| **工作地址** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes 选项集](hr-admin-integration-payroll-api-no-yes.md)* | 只读 | 一个指示地址是否为员工工作场所的值。 |
| **国家/地区**</br>mshr_countryregionid</br>*字符串* | 只读</br>必需 | 为地址定义的国家或地区。 |
| **邮政编码**</br>mshr_zipcode<br>*字符串* | 只读 | 针对员工定义的标识号。 |
| **街道**</br>mshr_street</br>*字符串* | 只读 | 针对地址定义的街道。 |
| **城市**</br>mshr_city</br>*字符串* | 只读 | 针对地址定义的城市。 |
| **州或省/自治区/直辖市**</br>mshr_state</br>*字符串* | 只读 | 为地址定义的省/市/自治区。 |
| **县**</br>mshr_county</br>*字符串* | 只读 | 针对地址定义的国家/地区。 |
| **生效日期**</br>mshr_postaladdressvalidfrom</br>*日期/时间偏移* | 只读 | 地址生效的开始日期。 |
| **失效日期**</br>mshr_postaladdressvalidto</br>*日期/时间偏移* | 只读 | 地址有效的结束日期。 |
| **主要字段**</br>mshr_primaryfield</br>*字符串* | 只读 | 主要字段。 |
| **工资单工作人员地址 ID**</br>mshr_payrollworkeraddressentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识地址的全局唯一标识符 (GUID) 值。 |

## <a name="relations"></a>关系

| 属性值 | 相关实体 | 导航属性 | 集合类型 |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**响应**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
