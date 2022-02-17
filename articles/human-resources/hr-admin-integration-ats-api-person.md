---
title: 人员
description: 本主题介绍 Dynamics 365 Human Resources 的“人员”实体。
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
ms.openlocfilehash: 728e383be44949ec7f1e51feb5157c61679b3e7b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068651"
---
# <a name="person"></a>人员


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员”实体。

物理名称：mshr_dirpersonentity

### <a name="description"></a>说明

此实体为作为应聘者的个人提供个人信息。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员实体 ID**<br>mshr_dirpersonentityid<br>*GUID* | 只读<br>必填<br>系统生成 | 系统生成的实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 只读<br>必填<br>系统生成 | 用户可读的系统生成的人员的唯一标识符。  |
| **姓名**<br>mshr_name<br>*字符串* | 只读<br>必填 | 此字段值是按照 **姓名顺序显示为** 字段中定义的顺序的名字、中间名、姓氏前缀和姓氏的串联。 |
| **别名**<br>mshr_namealias<br>*字符串* | 读/写<br>可选 | 可以为该人员提供的别名。 |
| **称作**<br>mshr_knownas<br>*字符串* | 读/写<br>可选 | 通常被称为另一个名字时可以用于该人员的名字。 |
| **语言 ID**<br>mshr_languageid<br>*字符串* | 读/写<br>可选 | 人员的主要语言的语言 ID，以 ISO 639-1 格式定义。 |
| **通讯簿**<br>mshr_addressbooks<br>*字符串* | 读/写<br>可选 | 人员可能被分配到的通讯簿。 已为组织设置的通讯簿在 mshr_diraddressbooksentity 实体中列出。 |
| **周年纪念日**<br>mshr_anniversaryday<br>*Int* | 读/写<br>可选 | 该人员周年纪念日的那一天。 |
| **周年纪念月份**<br>mshr_anniversarymonth<br>*mshr_monthsofyear 选项集* | 读/写<br>可选 | 该人员周年纪念日所在的月份。 |
| **周年纪念年份**<br>mshr_anniversaryyear<br>*Int* | 读/写<br>可选 | 该人员周年纪念日所在的年份。 |
| **出生日**<br>mshr_birthday<br>*Int* | 读/写<br>可选 | 该人员出生日期的那一天。 |
| **出生月份**<br>mshr_birthmonth<br>*mshr_monthsofyear 选项集* | 读/写<br>可选 | 该人员出生日期所在的月份。 |
| **出生年份**<br>mshr_birthyear<br>*Int* | 读/写<br>可选 | 该人员出生日期所在的年份。 |
| **子女姓名**<br>mshr_childrennames<br>*字符串* | 读/写<br>可选 | 该人员子女姓名的字符串。 不需要界定。 |
| **性**<br>mshr_gender<br>*mshr_hcmpersongender 选项集* | 读/写<br>可选 | 人员的性别。 |
| **爱好**<br>mshr_hobbies<br>*字符串* | 读/写<br>可选 | 此人的爱好。 |
| **缩写**<br>mshr_initials<br>*字符串* | 读/写<br>可选 | 该人员姓名的缩写。 |
| **婚姻状况**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus 选项集* | 读/写<br>可选 | 该人员的婚姻状况。 |
| **语音名字**<br>mshr_phoneticfirstname<br>*字符串* | 读/写<br>可选 | 该人员名字的语音发音。 |
| **语音姓氏**<br>mshr_phoneticlastname<br>*字符串* | 读/写<br>可选 | 该人员姓氏的语音发音。 |
| **语音中间名**<br>mshr_phoneticmiddlename<br>*字符串* | 读/写<br>可选 | 该人员姓氏的语音发音。 |
| **人称后缀**<br>mshr_personalsuffix<br>*字符串* | 读/写<br>可选 | 该人员的人称后缀。 有效值在 mshr_dirnameaffixentity 实体中，其中 mshr_type 为 Suffix (200000001)。 |
| **称谓**<br>mshr_personaltitle<br>*字符串* | 读/写<br>可选 | 该人员的称谓。 有效值在 mshr_dirnameaffixentity 实体中，其中 mshr_type 为 Title (200000000)。
| **职称后缀**<br>mshr_professionalsuffix<br>*字符串* | 读/写<br>可选 | 职称后缀。 |
| **职称**<br>mshr_professionaltitle<br>*字符串* | 读/写<br>可选 | 职称。 |
| **完整主要地址**<br>mshr_fullprimaryaddress<br>*字符串* | 读/写<br>可选 | 该人员的完整主要地址，主要地址字段的串联。 |
| **地址 - 城市**<br>mshr_addresscity<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的城市。 在 mshr_logisticsaddresscityentity 实体中设置。 |
| **地址国家/地区**<br>mshr_addresscountryregionid<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的国家/地区。 有效值在 mshr_logisticsaddresscountryregionentity 实体中。 |
| **地址国家/地区 ISO 代码**<br>mshr_addresscountryregionisocode<br>*字符串* | 读/写<br>可选 | 该人员主要地址中的国家/地区的 ISO 代码。 |
| **地址县**<br>mshr_addresscounty<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的县。 在 mshr_logisticsaddresscountyentity 实体中设置。 |
| **地址地区名称**<br>mshr_addressdistrictname<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的地区。 在 mshr_logisticsaddressdistrictentity 实体中设置。 |
| **地址纬度**<br>mshr_addresslatitude<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的纬度。 |
| **地址位置 ID**<br>mshr_addresslocationid<br>*字符串* | 读/写<br>可选 | 该人员主要地址中的位置的唯一标识符。 有效值在 mshr_logisticspostaladdresslocationcdsentity 实体中。 |
| **地址位置角色**<br>mshr_addresslocationroles<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的位置角色。 在 mshr_logisticslocationrolecdsentity 实体中设置。 |
| **地址经度**<br>mshr_addresslongitude<br>*字符串* |  读/写<br>可选 | 该人员的主要地址中的经度。 |
| **地址州或省/自治区/直辖市**<br>mshr_addressstate<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的州或省/自治区/直辖市。 在 mshr_logisticsaddressstateentity 实体中设置。 |
| **地址街道**<br>mshr_addressstreet<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的街道地址。 |
| **地址生效日期**<br>mshr_addressvalidfrom<br>*日期* | 读/写<br>可选 | 该人员的主要地址开始有效的日期。 |
| **地址失效日期**<br>mshr_addressvalidto<br>*日期* | 读/写<br>可选 | 该人员的主要地址失效的日期。 |
| **地址邮政编码**<br>mshr_addresszipcode<br>*字符串* | 读/写<br>可选 | 该人员的主要地址中的邮政编码。 在 mshr_logisticsaddresspostalcodeentity 实体中设置。 |
| **私人地址**<br>mshr_addressisprivate<br>*mshr_noyes 选项集* | 读/写<br>可选 | 确定人员的主要地址是否与组织中的其他人共享。 |
| **地址描述**<br>mshr_addressdescription<br>*字符串* | 读/写<br>可选 | 该人员的主要地址的描述。 |
| **主要联系电子邮件**<br>mshr_primarycontactemail<br>*字符串* | 读/写<br>可选 | 该人员的主要电子邮件地址。 |
| **主要联系电子邮件描述**<br>mshr_primarycontactemaildescription<br>*字符串* | 读/写<br>可选 | 为主要电子邮件地址提供的描述。 |
| **主要联系电子邮件是 IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes 选项集* | 读/写<br>可选 | 确定主要电子邮件地址是否可用于发送即时消息。 |
| **主要联系电子邮件用途**<br>mshr_primarycontactemailpurpose<br>*字符串* | 读/写<br>可选 | 主要电子邮件地址的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **主要联系传真**<br>mshr_primarycontactfax<br>*字符串* | 读/写<br>可选 | 主要传真号。 |
| **主要联系传真描述**<br>mshr_primarycontactfaxdescription<br>*字符串* | 读/写<br>可选 | 为主要传真号提供的描述。 |
| **主要联系传真分机**<br>mshr_primarycontactfaxextension<br>*字符串* | 读/写<br>可选 | 主要传真号的分机。 |
| **主要联系传真用途**<br>mshr_primarycontactfaxpurpose<br>*字符串* | 读/写<br>可选 | 主要传真号的用途。 在 ogisticslocationroleentity 实体中设置。
| **主要联系电话**<br>mshr_primarycontactphone<br>*字符串* | 读/写<br>可选 | 主电话号码。 |
| **主要联系电话描述**<br>mshr_primarycontactphonedescription<br>*字符串* | 读/写<br>可选 | 为主要电话号码提供的描述。 |
| **主要联系电话分机**<br>mshr_primarycontactphoneextension<br>*字符串* | 读/写<br>可选 | 主要电话号码的分机。 |
| **主要联系电话是移动电话**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes 选项集* | 读/写<br>可选 | 确定主要电话号码是否是移动电话。 |
| **主要联系电话用途**<br>mshr_primarycontactphonepurpose<br>*字符串* | 读/写<br>可选 | 主要电话号码的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **主要联系电报**<br>mshr_primarycontacttelex<br>*字符串* | 读/写<br>可选 | 主要电报号码。 |
| **主要联系电报描述**<br>mshr_primarycontacttelexdescription<br>*字符串* | 读/写<br>可选 | 为人员的主要电报号码提供的描述。 |
| **主要联系电报用途**<br>mshr_primarycontacttelexpurpose<br>*字符串* | 读/写<br>可选 | 该人员的主要电报号码的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **主要联系 URL**<br>mshr_primarycontacturl<br>*字符串* | 读/写<br>可选 | 主要 URL。 |
| **主要联系 URL 描述**<br>mshr_primarycontacturldescription<br>*字符串* | 读/写<br>可选 | 为该人员的主要 URL 提供的描述。 |
| **主要联系 URL 用途**<br>mshr_primarycontacturldescription<br>*字符串* | 读/写<br>可选 | 人员的主要 URL 的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **主要联系 Facebook**<br>mshr_primarycontactfacebook<br>*字符串* | 读/写<br>可选 | 主要 Facebook 帐户。 使用用户 ID 标识。 |
| **主要联系 Facebook 描述**<br>mshr_primarycontactfacebookdescription<br>*字符串* | 读/写<br>可选 | 为该人员的主要 Facebook 帐户提供的描述。 |
| **主要联系 Facebook 是私人帐户**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes 选项集* | 读/写<br>可选 | 确定主要 Facebook 帐户是否对其他用户可见。 |
| **主要联系 Facebook 用途**<br>mshr_primarycontactfacebookpurpose<br>*字符串* | 读/写<br>可选 | 人员的主要 Facebook 帐户的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **主要联系 LinkedIn**<br>mshr_primarycontactlinkedin<br>*字符串* | 读/写<br>可选 | 主要 LinkedIn 帐户。 使用用户名标识。 |
| **主要联系 LinkedIn 描述**<br>mshr_primarycontactlinkedindescription<br>*字符串* | 读/写<br>可选 | 为该人员的主要 LinkedIn 帐户提供的描述。 |
| **主要联系 LinkedIn 是私人帐户**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes 选项集* | 读/写<br>可选 | 确定人员的主要 LinkedIn 帐户信息是否与其他用户共享。 |
| **主要联系 LinkedIn 用途**<br>mshr_primarycontactlinkedinpurpose<br>*字符串* | 读/写<br>可选 | 人员的主要 LinkedIn 帐户的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **主要联系 Twitter**<br>mshr_primarycontacttwitter<br>*字符串* | 读/写<br>可选 | 人员的主要 Twitter 帐户。 使用“@用户名”标识。 |
| **主要联系 Twitter 描述**<br>mshr_primarycontacttwitterdescription<br>*字符串* | 读/写<br>可选 | 为该人员的主要 Twitter 帐户提供的描述。 |
| **主要联系 Twitter 是私人帐户**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes 选项集* | 读/写<br>可选 | 确定人员的主要 Twitter 帐户信息是否与其他用户共享。 |
| **主要联系 Twitter 用途**<br>mshr_primarycontacttwitterpurpose<br>*字符串* | 读/写<br>可选 | 人员的主要 Twitter 帐户的用途。 在 ogisticslocationroleentity 实体中设置。 |
| **当事方类型**<br>mshr_partytype<br>*字符串* | 读/写<br>可选 | 人员的当事方类型。 将一直是应聘者的 **人员**。 |
| **姓名顺序显示为**<br>mshr_namesequencedisplayas<br>*字符串* | 读/写<br>可选 | 串联人员的姓名属性以形成 Name (mshr_name) 属性值所采用的顺序。 |
| **名**<br>mshr_firstname<br>*字符串* | 读/写<br>必填 | 人员的名字。 |
| **中间名**<br>mshr_middlename<br>*字符串* | 读/写<br>可选 | 人员的中间名。 |
| **姓氏前缀**<br>mshr_lastnameprefix<br>*字符串* | 读/写<br>可选 | 人员姓氏的前缀。 |
| **姓**<br>mshr_lastname<br>*字符串* | 读/写<br>可选 | 人员的姓氏。 |
| **电子位置 ID**<br>mshr_electroniclocationid<br>*字符串* | 读/写<br>可选 | 人员的电子位置的 ID。 |
| **地址时区**<br>mshr_addresstimezone<br>*Int* | 读/写<br>可选 | 该人员的主要地址中的时区。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
