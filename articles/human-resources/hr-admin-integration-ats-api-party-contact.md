---
title: 当事方联系人
description: 本主题介绍 Dynamics 365 Human Resources 的“当事方联系人”实体。
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
ms.openlocfilehash: d77f5ebb52c14759918178194fc08b63d27db1f0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798193"
---
# <a name="party-contact"></a>当事方联系人

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“当事方联系人”实体。

物理名称：mshr_dirpartycontactentities

## <a name="description"></a>说明

此实体描述应聘者的联系信息，包括电话、电子邮件和社交媒体帐户。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **当事方联系人实体 ID**<br>mshr_dirpartycontactentityid<br>*字符串* | 只读<br>必填 | 系统生成的实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 关联当事方（人员）记录的 ID。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的当事方（人员）实体记录的标识符。 |
| **位置 ID**<br>mshr_locationid<br>*字符串* | 读/写<br>必填 | 地址记录的位置 ID。 在 mshr_logisticspostaladdresslocationcdsentity 实体中设置。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 联系人详细信息的描述。 |
| **类型**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype 选项集* | 读/写<br>必填 | 联系人详细信息类型。 |
| **国家/地区代码**<br>mshr_countryregioncode<br>*字符串* | 读/写<br>可选 | 地址所在的国家或地区。 |
| **定位符**<br>mshr_locator<br>*字符串* | 读/写<br>可选 | 联系人详细信息。 例如，如果类型是 **电子邮件地址**，此字段则包含应聘者的电子邮件地址。 |
| **定位符扩展**<br>mshr_locatorextension<br>*字符串* | 读/写<br>可选 | 定位符扩展。 例如，如果类型是 **电话**，此属性则包含电话号码分机。 |
| **移动**<br>mshr_ismobile<br>*mshr_noyes 选项集* | 读/写<br>必填 | 指定电话是否为手机号码。 |
| **即时消息**<br>mshr_isinstantmessage<br>*mshr_noyes 选项集* | 读/写<br>必填 | 指定是否为电话启用即时消息。 |
| **是否为主要**<br>mshr_isprimary<br>*mshr_noyes 选项集* | 读/写<br>必填 | 确定联系人类型的主要联系人。 每个联系人类型只能有一个主要记录。 |
| **专用**<br>mshr_isprivate<br>*mshr_noyes 选项集* | 读/写<br>必填 | 标识此地址是否为该人员的私人地址。 |
| **目的**<br>mshr_purpose<br>*字符串* | 读/写<br>可选 | 联系人详细信息的目的/角色。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录的主要标识符的字段。 当事方编号、类型、描述和定位符的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]