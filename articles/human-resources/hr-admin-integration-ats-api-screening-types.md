---
title: 筛选类型
description: 本主题介绍 Dynamics 365 Human Resources 的“筛选类型”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb99c2fb57df883ab376c7f6aab547073bd0ff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058288"
---
# <a name="screening-types"></a>筛选类型

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“筛选类型”实体。

物理名称：mshr_hcmscreeningtypeentity

## <a name="description"></a>说明

此实体描述公司为入职前和持续的员工筛选流程设置的筛选类型。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **筛选类型实体 ID**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | 只读<br>必填<br>系统生成 | 筛选类型记录的唯一主要标识符。 |
| **筛选类型 ID**<br>mshr_screeningtypeid<br>*字符串* | 读/写<br>必填 | 用户定义的筛选类型的唯一标识符。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 筛选类型的描述。 |
| **频率单位**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit 选项集* | 读/写<br>必填 | 描述必须为分配的人员完成的筛选的频率。 |
| **生成来源**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom 选项集* | 读/写<br>必填 | 如果频率值是“一次性”以外的任何值，GenerateFrom 值将确定开始计算下一个筛选事件的日期。 |
| **频率间隔**<br>mshr_frequencyinterval<br>*整数* | 读/写<br>必填 | 如果频率值是“一次性”以外的任何值，您必须为每个筛选事件之间的时间单位定义一个间隔。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]