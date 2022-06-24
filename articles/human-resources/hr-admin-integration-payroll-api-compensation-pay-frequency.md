---
title: 薪酬付薪频率
description: 本文提供 Dynamics 365 Human Resources 中薪酬付薪频率实体的详细信息和示例查询。
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9afe27776797b2355a32226bbd7fa514b5c5d962
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894605"
---
# <a name="compensation-pay-frequency"></a>薪酬付薪频率


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 中的薪酬付薪频率实体。

物理名称：mshr_hcmpayrateconversionentity。

### <a name="description"></a>说明

此实体提供有关给定薪酬付薪频率的付薪比率转换的信息。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **年度付薪比率转换**</br>mshr_annualconversionfactor</br>*小数* | 只读 | 付款频率的年度换算系数。 |
| **说明**</br>mshr_description</br>*字符串* | 只读 | 转换率的描述。 |
| **小时付薪比率转换**</br>mshr_hourlyconversionfactor</br>*小数* | 只读 | 付款频率的小时换算系数。 |
| **每月付薪比率转换**</br>mshr_monthlyconversionfactor</br>*小数* | 只读 | 付款频率的每月换算系数。 |
| **付薪比率转换**</br>mshr_payrateconversion</br>*字符串* | 只读 | 用于标识转化率的唯一字符串。 |
| **期间余额**</br>mshr_period</br>*期间选项集* | 只读 | 给定付薪比率转换的主期间。 |
| **每周付薪比率转换**</br>mshr_weeklyconversionfactor</br>*小数* | 只读 | 付款频率的每周换算系数。 |
| **数据区域 ID**</br>mshr_dataareaid</br>*字符串* | 只读 | 法人（公司）。 |
| **薪酬付薪频率实体 ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识记录的全局唯一标识符 (GUID) 值。 |

## <a name="example-query-for-payroll-employee"></a>工资单员工的示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**响应**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
