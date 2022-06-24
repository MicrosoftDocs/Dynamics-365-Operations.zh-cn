---
title: 人员姓名历史记录
description: 本文提供 Dynamics 365 Human Resources 中“人员姓名历史记录”实体的详细信息和示例查询。
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875762"
---
# <a name="person-name-history"></a>人员姓名历史记录


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的“人员姓名历史记录”实体。

物理名称：mshr_dirpersonnamehistoricalentity。

### <a name="description"></a>说明

此实体提供有关给定人员名称历史记录的信息。

> [!IMPORTANT] 
> **FirstName**、**MiddleName**、**LastName**、**NameValidFrom** 和 **NameValidTo** 字段在“工资单员工”实体上不再可用。 它们已被删除，以确保只有一个日期有效的数据源支持该实体。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **名**</br>mshr_firstname</br>*字符串* | 只读 | 名。 |
| **姓氏前缀**</br>mshr_lastnameprefix</br>*字符串* | 只读 | 姓前缀。 |
| **姓**</br>mshr_lastname</br>*字符串* | 只读 | 姓。 |
| **中间名**</br>mshr_middlename</br>*字符串* | 只读 | 中间名。 |
| **失效日期**</br>mshr_validto</br>*字符串* | 只读 | 姓名有效的结束日期。 |
| **当事方编号**</br>mshr_partynumber</br>*字符串* | 只读 | 用户可读的系统生成的人员的唯一标识符。 |
| **主要字段**</br>mshr_primaryfield</br>*字符串* | 只读 | 记录的唯一标识符。 |
| **人员姓名历史记录实体 ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识记录的全局唯一标识符 (GUID) 值。 |

## <a name="relations"></a>关系

| 属性值 | 相关实体 | 导航属性 | 集合类型 |
| --- | --- | --- | --- |
| 不适用 | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | 不适用 | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>工资单员工的示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**响应**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
