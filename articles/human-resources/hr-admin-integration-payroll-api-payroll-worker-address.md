---
title: 工资单工作人员地址
description: 本主题提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。
author: jcart
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020697"
---
# <a name="payroll-worker-address"></a>工资单工作人员地址

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **市**<br>mshr_city<br>*字符串* | 只读<br>必填 | 针对地址定义的城市。   |
| **人员编号**<br>mshr_personnelnumber<br>*字符串* | 只读<br>必填 | 员工的唯一人员编号。  |
| **国家/地区**<br>mshr_countryregionid<br>*字符串* | 只读<br>必填 | 针对地址定义的国家/地区  |
| **生效日期**<br>mshr_postaladdressvalidfrom<br>*日期/时间偏移* | 只读 <br>必填 | 地址有效的开始日期。 |
| **工作地址**<br>mshr_isworkedinaddressbr>*Int32* | 只读<br>必填 | 表示地址是否是员工的工作地址。 |
| **县**<br>mshr_county<br>*字符串* | 只读<br>必填 | 针对地址定义的县。  |
| **工资单工作人员地址 ID**<br>mshr_payrollworkeraddressentityid<br>*GUID* | 必填<br>系统生成的 | 系统生成的用于唯一标识地址的 GUID 值。  |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 |  |
| **街道**<br>mshr_street<br>*字符串* | 只读<br>必填 | 针对地址定义的街道。 |
| **失效日期**<br>mshr_postaladdressvalidto<br>*日期/时间偏移* | 只读 <br>必填 | 地址有效的结束日期。  |
| **位置 ID**<br>mshr_locationidbr>*String* | 只读 <br>必填 | 地址的 ID。  |
| **邮政编码**<br>mshr_zipcode<br>*字符串* | 只读 <br>必填 |针对员工定义的标识号。  |
| **家庭地址**<br>mshr_islivedinaddressbr>*String* | 只读<br>必填 | 表示地址是否是员工的家庭地址。 |
| **州或省/自治区/直辖市**<br>mshr_state<br>*字符串* | 只读<br>必填 | 针对地址定义的省/自治区/直辖市。  |

## <a name="example-query"></a>示例查询

**申请**

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
