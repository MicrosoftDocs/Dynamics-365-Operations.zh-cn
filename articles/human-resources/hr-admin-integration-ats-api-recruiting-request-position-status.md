---
title: 招聘请求职位状态
description: 本主题介绍 Dynamics 365 Human Resources 的招聘请求职位状态选项集。
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051873"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="0ab07-103">招聘请求职位状态</span><span class="sxs-lookup"><span data-stu-id="0ab07-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0ab07-104">本主题介绍 Dynamics 365 Human Resources 的招聘请求职位状态选项集。</span><span class="sxs-lookup"><span data-stu-id="0ab07-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0ab07-105">物理名称：mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="0ab07-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="0ab07-106">此枚举为 RecruitingRequestPosition 实体中招聘请求的每个职位的状态值提供选项集。</span><span class="sxs-lookup"><span data-stu-id="0ab07-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="0ab07-107">值</span><span class="sxs-lookup"><span data-stu-id="0ab07-107">Value</span></span> | <span data-ttu-id="0ab07-108">标签</span><span class="sxs-lookup"><span data-stu-id="0ab07-108">Label</span></span> | <span data-ttu-id="0ab07-109">说明</span><span class="sxs-lookup"><span data-stu-id="0ab07-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0ab07-110">200000000</span><span class="sxs-lookup"><span data-stu-id="0ab07-110">200000000</span></span> | <span data-ttu-id="0ab07-111">公开</span><span class="sxs-lookup"><span data-stu-id="0ab07-111">Open</span></span> | <span data-ttu-id="0ab07-112">招聘请求中的职位空缺，要进行招聘。</span><span class="sxs-lookup"><span data-stu-id="0ab07-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="0ab07-113">这不指示该职位当前没有有效的职位分配。</span><span class="sxs-lookup"><span data-stu-id="0ab07-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="0ab07-114">招聘时该职位上可能有员工。</span><span class="sxs-lookup"><span data-stu-id="0ab07-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="0ab07-115">这仅指示在招聘请求的上下文中该职位可以招聘。</span><span class="sxs-lookup"><span data-stu-id="0ab07-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="0ab07-116">200000001</span><span class="sxs-lookup"><span data-stu-id="0ab07-116">200000001</span></span> | <span data-ttu-id="0ab07-117">已填写</span><span class="sxs-lookup"><span data-stu-id="0ab07-117">Filled</span></span> | <span data-ttu-id="0ab07-118">已选择一名工作人员要分配给该职位。</span><span class="sxs-lookup"><span data-stu-id="0ab07-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="0ab07-119">200000002</span><span class="sxs-lookup"><span data-stu-id="0ab07-119">200000002</span></span> | <span data-ttu-id="0ab07-120">已取消</span><span class="sxs-lookup"><span data-stu-id="0ab07-120">Canceled</span></span> | <span data-ttu-id="0ab07-121">此职位的招聘请求已被取消。</span><span class="sxs-lookup"><span data-stu-id="0ab07-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0ab07-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ab07-122">See also</span></span>

[<span data-ttu-id="0ab07-123">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="0ab07-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0ab07-124">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="0ab07-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]