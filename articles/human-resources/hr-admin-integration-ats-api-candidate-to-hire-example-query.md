---
title: “可雇用的应聘者”的查询示例
description: 本主题提供 Dynamics 365 Human Resources 中“可雇用的应聘者”实体的示例查询。
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
ms.openlocfilehash: ea6fc745ffb5892a32196394cb28cb5e646b7639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795061"
---
# <a name="example-query-for-candidate-to-hire"></a>“可雇用的应聘者”的查询示例

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题提供 Dynamics 365 Human Resources 中“可雇用的应聘者”实体的示例查询。

本主题提供了一个示例，演示如何在单个 API 操作中使用 *深插入* 创建新应聘者记录的所有详细信息。 有关深插入的详细信息，请参阅[在一个操作中创建相关实体记录](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation)。

由于与 **mshr_dirpersonentity** 实体之间的关系，**mshr_hcmcandidatetohireentity** 实体是唯一的。 **mshr_hcmcandidatetohireentity** 上的很多属性（例如，**mshr_firstname**、**mshr_lastname** 和 **mshr_birthdate**）都派生自 **mshr_dirpersonentity** 记录。 如果在不使用深插入的情况下将新应聘者记录发布到 **mshr_hcmcandidatetohireentity**，您可以直接在 **mshr_hcmcandidatetohireentity** 记录中为这些属性定义值。 关联的 **mshr_dirpersonentity** 记录将使用属性的定义值隐式创建。 然后，您可以作为单独的 API 调用创建任何其他相关实体记录（如技能或教育）。

但是，如果您要使用深插入在一个操作中创建所有相关实体，则必须在该操作的嵌套级别定义特定于 **mshr_dirpersonentity** 实体的属性。

本示例说明如何在单个 API 操作中使用深插入在三个嵌套级别创建应聘者记录、关联人员记录以及人员的技能和教育情况。

> [!NOTE]
> 此示例未包含每个 API 实体的所有属性。 出于演示目的对其进行了简化。

**申请**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**响应**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]