---
title: 人员地址
description: 本主题介绍 Dynamics 365 Human Resources 的“人员地址”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e16966c30ccfadd69e3d53f1259fa7167896e6d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798145"
---
# <a name="person-address"></a>人员地址

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员地址”实体。

物理名称：mshr_hcmpersonaddressentities

## <a name="description"></a>说明

此实体包含应聘者记录的邮寄地址列表。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员地址实体 ID**<br>mshr_hcmpersonaddressentityid<br>*字符串* | 只读<br>必填 | 系统生成的实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 关联当事方（人员）记录的 ID。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的当事方（人员）实体记录的标识符。 |
| **位置 ID**<br>mshr_locationid<br>*字符串* | 读/写<br>必填 | 地址记录的位置 ID。 在 mshr_logisticspostaladdresslocationcdsentity 实体中设置。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 应聘者地址的描述。 |
| **角色**<br>mshr_roles<br>*字符串* | 读/写<br>必填 | 为此地址分配的角色。 可以分配多个角色。 每个角色应以分号分隔。 有效值包含在 mshr_logisticslocationroleentity 实体中。 |
| **街道**<br>mshr_street<br>*字符串* | 读/写<br>可选 | 街道编号。 |
| **市**<br>mshr_city<br>*字符串* | 读/写<br>可选 | 地址的城市。 在 mshr_logisticsaddresscityentity 实体中设置。 |
| **州或省/自治区/直辖市**<br>mshr_state<br>*字符串* | 读/写<br>可选 | 地址所在的省/市/自治区。 在 mshr_logisticsaddressstateentity 实体中设置。 |
| **县**<br>mshr_county<br>*字符串* | 读/写<br>可选 | 地址的县。 在 mshr_logisticsaddresscountyentity 实体中设置。 |
| **邮政编码**<br>mshr_zipcode<br>*字符串* | 读/写<br>可选 | 地址对应的邮政编码。 在 mshr_logisticsaddresspostalcodeentity 实体中设置。 |
| **国家/地区 ID**<br>mshr_countryregionid<br>*字符串* | 读/写<br>可选 | 地址所在的国家或地区。 |
| **国家/地区 ID 值**<br>_mshr_fk_countriregion_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_logisticsaddresscountryregionentity 的 mshr_logisticaddresscountryregionentityid | 系统生成的地址中国家/地区的唯一标识符。 |
| **是否为主要**<br>mshr_isprimary<br>*mshr_noyes 选项集* | 读/写<br>必填 | 标识此地址是否是所定义角色的人员的主要地址。 |
| **私人**<br>mshr_isprivate<br>*mshr_noyes 选项集* | 读/写<br>必填 | 标识此地址是否为该人员的私人地址。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录的主要标识符的字段。 当事方编号和位置 ID 的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]