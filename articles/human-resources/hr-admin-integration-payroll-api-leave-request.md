---
title: 休假请求
description: 本主题提供 Dynamics 365 Human Resources 中休假请求实体的详细信息和示例查询。
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
ms.openlocfilehash: 0f14c143a59553786fe85284c128cec80905810b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067671"
---
# <a name="leave-request"></a>休假请求


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的休假请求实体。

### <a name="description"></a>说明

该实体提供休假请求的信息。

物理名称：mshr_essleaverequestentity。

## <a name="properties"></a>属性

| 属性</br>**物理名称**</br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **请求 ID**</br>mshr_requestid</br>*字符串* | 只读 | 请求 ID。 |
| **休假类型 ID**</br>mshr_leavetypeid</br>*字符串* | 只读 | 休假类型 ID。 |
| **日期**</br>mshr_leavedate</br>*日期/时间偏移* | 只读 | 休假请求的日期。 |
| **金额**</br>mshr_amount</br>*十进制* | 只读 | 休假请求金额。 |
| **半天类型**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition 选项集* | 只读 | 半天休假的类型。 |
| **注释**</br>mshr_comment</br>*字符串* | 只读 | 请求的注释。 |
| **状态**</br>mshr_status</br>*mshr_status 选项集* | 只读 | 请求的状态。 |
| **日期**</br>mshr_requestdate</br>*日期/时间偏移* | 只读 | 请求的日期。 |
| **人员编号**</br>mshr_personnelnumber</br>*字符串* | 只读 | 员工的唯一人员编号。 |
| **原因代码 ID**</br>mshr_reasoncodeid</br>*字符串* | 只读 | 原因代码 ID。 |
| **数据区域 ID**</br>mshr_dataareaid</br>*字符串* | 只读 | 指定法人（公司）。 |
| **主要字段**</br>mshr_primaryfield</br>*GUID* | 只读</br>系统生成的 | |
| **休假类型实体**</br>mshr_essleaverequestentityid</br>*GUID* | 系统生成的 | 系统生成的用于唯一标识休假请求的 GUID 值。 |

## <a name="example-query"></a>示例查询

**请求**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**响应**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
