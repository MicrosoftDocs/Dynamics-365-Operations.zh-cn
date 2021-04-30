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
ms.openlocfilehash: a8c3655e7ff609eedbf92fa90a36b65002f40306
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893464"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="090c7-103">“可雇用的应聘者”的查询示例</span><span class="sxs-lookup"><span data-stu-id="090c7-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="090c7-104">本主题提供 Dynamics 365 Human Resources 中“可雇用的应聘者”实体的示例查询。</span><span class="sxs-lookup"><span data-stu-id="090c7-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="090c7-105">本主题提供了一个示例，演示如何在单个 API 操作中使用 *深插入* 创建新应聘者记录的所有详细信息。</span><span class="sxs-lookup"><span data-stu-id="090c7-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="090c7-106">有关深插入的详细信息，请参阅[在一个操作中创建相关实体记录](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation)。</span><span class="sxs-lookup"><span data-stu-id="090c7-106">For more information about deep inserts, see [Create related entity records in one operation](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="090c7-107">由于与 **mshr_dirpersonentity** 实体之间的关系，**mshr_hcmcandidatetohireentity** 实体是唯一的。</span><span class="sxs-lookup"><span data-stu-id="090c7-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="090c7-108">**mshr_hcmcandidatetohireentity** 上的很多属性（例如，**mshr_firstname**、**mshr_lastname** 和 **mshr_birthdate**）都派生自 **mshr_dirpersonentity** 记录。</span><span class="sxs-lookup"><span data-stu-id="090c7-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="090c7-109">如果在不使用深插入的情况下将新应聘者记录发布到 **mshr_hcmcandidatetohireentity**，您可以直接在 **mshr_hcmcandidatetohireentity** 记录中为这些属性定义值。</span><span class="sxs-lookup"><span data-stu-id="090c7-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="090c7-110">关联的 **mshr_dirpersonentity** 记录将使用属性的定义值隐式创建。</span><span class="sxs-lookup"><span data-stu-id="090c7-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="090c7-111">然后，您可以作为单独的 API 调用创建任何其他相关实体记录（如技能或教育）。</span><span class="sxs-lookup"><span data-stu-id="090c7-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="090c7-112">但是，如果您要使用深插入在一个操作中创建所有相关实体，则必须在该操作的嵌套级别定义特定于 **mshr_dirpersonentity** 实体的属性。</span><span class="sxs-lookup"><span data-stu-id="090c7-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="090c7-113">本示例说明如何在单个 API 操作中使用深插入在三个嵌套级别创建应聘者记录、关联人员记录以及人员的技能和教育情况。</span><span class="sxs-lookup"><span data-stu-id="090c7-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="090c7-114">此示例未包含每个 API 实体的所有属性。</span><span class="sxs-lookup"><span data-stu-id="090c7-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="090c7-115">出于演示目的对其进行了简化。</span><span class="sxs-lookup"><span data-stu-id="090c7-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="090c7-116">**申请**</span><span class="sxs-lookup"><span data-stu-id="090c7-116">**Request**</span></span>

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

<span data-ttu-id="090c7-117">**响应**</span><span class="sxs-lookup"><span data-stu-id="090c7-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="090c7-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="090c7-118">See also</span></span>

[<span data-ttu-id="090c7-119">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="090c7-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]