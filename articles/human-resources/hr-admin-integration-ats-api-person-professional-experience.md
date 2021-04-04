---
title: 人员专业经验
description: 本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5672e32b157b46b6863f06fea123fd3d6a3d96d2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466416"
---
# <a name="person-professional-experience"></a>人员专业经验

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。

物理名称：mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>说明

此实体描述应聘者的专业经验或工作经历。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **人员专业经验实体 ID**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | 只读<br>必填 | 系统生成的实体记录的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>*字符串* | 读/写<br>必填 | 应聘者的人员记录的唯一标识符。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_dirpersonentity 的 mshr_dirpersonentityid | 系统生成的人员实体记录的唯一标识符。 |
| **雇主职位**<br>mshr_employerposition<br>*字符串* | 读/写<br>必填 | 应聘者受雇期间担任的职务。 |
| **雇主名称**<br>mshr_employername<br>*字符串* | 读/写<br>必填 | 雇主的名称。 |
| **雇主位置**<br>mshr_employerlocation<br>*字符串* | 读/写<br>可选 | 雇主所在的位置。 最大长度：60。 未定义或要求特定格式。 |
| **电话**<br>mshr_phone<br>*字符串* | 读/写<br>可选 | 雇主的电话号码。 |
| **URL**<br>mshr_url<br>*字符串* | 读/写<br>可选 | 雇主网站的 URL。 |
| **开始日期**<br>mshr_startdate<br>*日期/时间* | 读/写<br>必填 | 应聘者受雇用的开始日期。 |
| **结束日期**<br>mshr_enddate<br>*日期/时间* | 读/写<br>可选 | 应聘者受雇用的结束日期，如果应聘者仍在此工作，则为 null。 |
| **允许联系雇主**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno 选项集* | 读/写<br>可选 | 表示应聘者是否允许与以前的雇主联系。 |
| **说明**<br>mshr_note<br>*字符串* | 读/写<br>可选 | 招聘人员和招聘经理使用的说明。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 只读<br>必填 | 用作实体记录的主要标识符的字段。 当事方编号、开始日期、雇主职位和雇主名称的组合。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]