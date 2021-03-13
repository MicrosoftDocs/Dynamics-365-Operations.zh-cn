---
title: 可雇用的应聘者
description: 本主题介绍 Dynamics 365 Human Resources 的“可雇用的应聘者”实体。
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
ms.openlocfilehash: eb16f9f46e3f5c58854ec06c3b89ec72dd7bae00
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125729"
---
# <a name="candidate-to-hire"></a>可雇用的应聘者

本主题介绍 Dynamics 365 Human Resources 的“可雇用的应聘者”实体。

物理名称：mshr_hcmcandidatetohireentity

## <a name="description"></a>说明

此实体提供用于在 Dynamics 365 Human Resources 中创建工作人员的应聘者详细信息。 它用于读取所有应聘者记录并创建内部和外部应聘者记录，让您可以为新应聘者创建个人详细信息。

当您创建将在系统中成为新人员记录的外部应聘者记录时，您不能定义发布新应聘者记录的当事方（人员）编号。 新人员实体记录使用新的应聘者记录创建。

创建内部应聘者记录（在公司已有员工记录的职位的应聘者）时，应为应聘者记录上的 mshr_partynumber 属性定义已经存在的人员记录的当事方（人员）编号，而不是定义将用于创建新人员记录的个人信息（如姓名、性别或出生日期）。

## <a name="json-representation"></a>JSON 表示

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **“可雇用的应聘者”实体 ID**<br>mshr_hcmcandidatetohireentityid<br>GUID | 只读<br>必填<br>系统生成 | 系统生成的实体记录的唯一标识符。 |
| **应聘者 ID**<br>mshr_candidateid<br>字符串 | 只读<br>必填<br>系统生成 | 实体的唯一标识符。 |
| **当事方编号**<br>mshr_partynumber<br>字符串 | 只读<br>必填 | 应聘者人员记录的当事方（人员）编号。 |
| **人员 ID 值**<br>_mshr_fk_person_id_value<br>GUID | 只读<br>必填<br>外键：mshr_direpersonentity 的 mshr_dirpersonentityid | 系统生成的应聘者的当事方（人员）记录的唯一标识符。 |
| **当事方类型**<br>mshr_partytype<br>mshr_dirpartytype 选项集 | 只读<br>必填 | 记录的当事方类型，在 mshr_dirpartytype 选项集中定义。 对于此实体，类型始终为“人员”。 |
| **招聘请求 ID**<br>mshr_recruitingrequestid<br>字符串 | 写入一次<br>可选 | 引用此应聘者满足的招聘请求。 |
| **招聘请求 ID 值**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | 读/写<br>可选<br>外键：mshr_hcmrecruitingrequestentity 的 mshr_hcmrecruitingrequestentityid | 系统生成的应聘者满足的招聘请求的唯一标识符。 |
| **职位 ID**<br>mshr_positionid<br>字符串 | 读/写<br>可选 | 应聘者被作为考虑对象的职位的 ID。 |
| **职位 ID 值**<br>_mshr_fk_position_if_value<br>GUID | 只读<br>可选<br>外键：mshr_hcmpositionv2entity 的 mshr_hcmpositionv2entityid | 应聘者被作为考虑对象的职位的系统生成标识符。 |
| **名**<br>mshr_firstname<br>字符串 | 读/写<br>必填 | 应聘者的名字。 |
| **中间名**<br>mshr_middlename<br>字符串 | 读/写<br>可选 | 应聘者的中间名。 |
| **姓氏前缀**<br>mshr_lastnameprefix<br>字符串 | 读/写<br>可选 | 应聘者的姓氏前缀。 |
| **姓**<br>mshr_lastname<br>字符串 | 读/写<br>可选 | 应聘者的姓氏。 |
| **性**<br>mshr_gender<br>mshr_hcmpersongender 选项集 | 读/写<br>可选 | 应聘者的性别。 |
| **出生日期**<br>mshr_birthdate<br>DateTime | 读/写<br>可选 | 应聘者的出生日期。 |
| **国籍国家/地区代码**<br>mshr_citizenshipcountrycode<br>字符串 | 读/写<br>可选 | 指定应聘者的国籍国家/地区。 有效的国家/地区代码在 mshr_logisticaddresscountryregionentity 中。 |
| **退伍军人状态 ID**<br>mshr_veteranstatusid<br>字符串 | 读/写<br>可选 | 指示应聘者的退伍军人状态。 |
| **退伍军人状态 ID 值**<br>_mshr_fk_veteranstatus_id_value<br>GUID | 只读<br>可选<br>外键：mshr_hcmveteranstatusentity 的 mshr_hcmveteranstatusentityid | 系统生成的退伍军人状态实体记录的唯一标识符。 |
| **兵役开始日期**<br>mshr_militaryservicestartdate<br>DateTime | 读/写<br>可选 | 应聘者服兵役的开始日期。 |
| **兵役结束日期**<br>mshr_militaryserviceenddate<br>DateTime | 读/写<br>可选 | 应聘者服兵役的结束日期。 |
| **是伤残退伍军人**<br>mshr_isdisabledveteran<br>mshr_noyes 选项集 | 读/写<br>可选 | 指示应聘者是否有伤残退伍军人状态。 |
| **可用性日期**<br>mshr_availabilitydate<br>DateTime | 读/写<br>可选 | 应聘者可以上班的最早日期。 |
| **是否愿意重新定位**<br>mshr_iswillingtorelocate<br>mshr_noyes 选项集 | 读/写<br>可选 | 指示应聘者是否愿意调整职位。 |
| **注释**<br>mshr_comments<br>字符串 | 读/写<br>可选 | 招聘人员或招聘经理使用的注释。 |
| **应用程序集成结果**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult 选项集 | 读/写<br>必填 | 应聘者在与集成相关的招聘流程中的状态。 |
| **不雇用原因码 ID**<br>mshr_donothirereasoncodeid<br>字符串 | 读/写<br>可选 | 当状态（应用程序集成结果）设置为“不雇用”时，视需要提供的原因代码。 |
| **原因代码 ID 值**<br>_mshr_fk_reasoncode_id_value<br>GUID | 只读<br>可选<br>外键：mshr_hcmreasoncodeentity 实体的 mshr_hcmreasoncodeentityid | 系统生成的 **不雇用** 原因代码的唯一标识符。 |
| **数据区域 ID**<br>mshr_dataareaid<br>字符串 | 读/写<br>可选 |  指定法人（公司）。 |
| **数据区域 ID 值**<br>_mshr_dataareaid_id_value<br>GUID | 只读<br>可选<br>外键：cdm_company 实体的 cdm_companyid | 系统生成的标识法人（公司）的 GUID 值。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
