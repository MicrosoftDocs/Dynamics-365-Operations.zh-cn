---
title: 评级级别
description: 本文介绍 Dynamics 365 Human Resources 的“评级级别”实体。
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
ms.openlocfilehash: dcd366632456c186eca9682d79a0c8690772e8bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893865"
---
# <a name="rating-level"></a>评级级别


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的“评级级别”实体。

物理名称：mshr_hcmratinglevelentity

## <a name="description"></a>说明

此实体提供可用的技能评级级别。 评级级别在所有法人中应用。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **评级级别实体 ID**<br>mshr_hcmratinglevelentityid<br>*GUID* | 只读<br>必填<br>系统生成 | 系统生成的级别的唯一标识符。 |
| **评级级别 ID**<br>mshr_ratinglevelid<br>*字符串* | 读/写<br>必填 | 级别的用户可读的唯一标识符。 |
| **评级模型 ID**<br>mshr_ratingmodelid<br>*字符串* | 读/写<br>必填 | 评级级别所属的评级模型。 |
| **评级模型实体 ID**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_hcmratingmodelentity 的 mshr_hcmratingmodelentityid | 系统生成的评级级别所属的评级模型的标识符。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 评级级别的描述。 |
| **系数**<br>mshr_factor<br>*整数* | 读/写<br>必填 | 评级级别的系数。 在比较具有不同评级级别数的项时，系数用于使分数标准化。 此值必须是 0 到 9 之间的一个整数。 |
| **注意**<br>mshr_note<br>*字符串* | 读/写<br>可选 | 与评级级别关联的所有说明。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录的标识符的字段。 评级级别 ID 和评级模型 ID 的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
