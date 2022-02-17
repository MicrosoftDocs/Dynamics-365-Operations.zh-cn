---
title: 招聘请求位置
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求位置”实体。
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
ms.openlocfilehash: 4dbc676e25c1ec24350607b10787924b0738e102
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069163"
---
# <a name="recruiting-request-location"></a>招聘请求位置


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“招聘请求位置”实体。

物理名称：mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>说明

定义为招聘的员工雇用后的工作位置的位置列表。 这些是跨法人创建的位置。

### <a name="json-representation"></a>JSON 表示

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **位置 ID**<br>mshr_locationid<br>*字符串* | 写入一次<br>必填 | 系统生成的用户可读的招聘位置的标识符。 |
| **招聘请求位置**<br>mshr_recruitingrequestlocationid<br>*字符串* | 写入一次<br>必填 | 用户定义的招聘位置的唯一标识符。 |
| **招聘请求位置实体 ID**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | 只读<br>必填 | 系统生成的招聘请求位置记录的唯一标识符。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 位置的描述。 |
| **国家/地区 ID**<br>mshr_countryregionid<br>*字符串* | 只读<br>可选 | 指定应聘者的国籍国家或地区。 |
| **国家/地区 ID 值**<br>_mshr_fk_countriregion_id_value<br>*GUID* | 只读<br>可选<br>外键：mshr_logisticsaddresscountryregionentity 的 mshr_logisticaddresscountryregionentityid | 系统生成的地址中国家/地区的唯一标识符。 |
| **邮政编码**<br>mshr_zipcode<br>*字符串* | 只读<br>可选 | 邮政编码。 |
| **街道**<br>mshr_street<br>*字符串* | 只读<br>可选 | 街道地址。 |
| **市**<br>mshr_city<br>*字符串* | 只读<br>可选 | 城市。 |
| **州或省/自治区/直辖市**<br>mshr_state<br>*字符串* | 只读<br>可选 | 州或省/自治区/直辖市。 |
| **县**<br>mshr_county<br>*字符串* | 只读<br>可选 | 县。 |
| **电话**<br>mshr_telephone<br>*字符串* | 读/写<br>可选 | 位置的电话号码。 |
| **电子邮件**<br>mshr_email<br>*字符串* | 读/写<br>可选 | 电子邮件地址。 |
| **InternetAddress**<br>mshr_internetaddress<br>*字符串* | 读/写<br>可选 | 位置网站的 URL。 |
| **数据区域 ID**<br>mshr_dataareaid<br>*字符串* | 读/写<br>可选 | 指定法人（公司）。 |
| **数据区域 ID 值**<br>_mshr_dataareaid_id_value<br>*GUID* | 只读<br>可选<br>外键：cdm_company 实体的 cdm_companyid | 系统生成的标识法人（公司）的 GUID 值。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
