---
title: 休假类型
description: 本文提供 Dynamics 365 Human Resources 中休假类型实体的详细信息和示例查询。
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893777"
---
# <a name="leave-type"></a>休假类型


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的休假类型实体。

### <a name="description"></a>Description

该实体提供给定休假类型的信息。

物理名称：mshr_essleavetypeentity。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **休假类型 ID**</br>mshr_leavetypeid</br>*字符串* | 只读 | 休假类型 ID。 |
| **说明**</br>mshr_description</br>*字符串* | 只读 | 休假类型的描述。 |
| **类别**</br>mshr_category</br>*mshr_LeaveTypeCategory 选项集* | 只读 | 休假类型类别。 |
| **需要原因代码**</br>mshr_isreasoncoderequired</br>*mshr_NoYes 选项集* | 只读 | 定义休假类型是否需要原因代码。 |
| **休假单位**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit 选项集* | 只读 | 此休假类型的单位。 |
| **启用半天**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes 选项集* | 定义是否为休假类型启用半天。 |
| **数据区域 ID**</br>mshr_dataareaid_id</br>*字符串* | 只读 | 指定法人（公司）。 |
| **休假类型实体**</br>mshr_essleavetypeentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识休假类型的 GUID 值。 |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**响应**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
