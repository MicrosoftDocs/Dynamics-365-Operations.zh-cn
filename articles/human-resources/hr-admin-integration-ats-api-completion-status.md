---
title: 完成状态
description: 本主题介绍 Dynamics 365 Human Resources 的完成状态选项集。
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468195"
---
# <a name="completion-status"></a><span data-ttu-id="81e8c-103">完成状态</span><span class="sxs-lookup"><span data-stu-id="81e8c-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="81e8c-104">本主题介绍 Dynamics 365 Human Resources 的完成状态选项集。</span><span class="sxs-lookup"><span data-stu-id="81e8c-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="81e8c-105">物理名称：mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="81e8c-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="81e8c-106">此枚举为应聘者筛选提供状态值选项集。</span><span class="sxs-lookup"><span data-stu-id="81e8c-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="81e8c-107">值</span><span class="sxs-lookup"><span data-stu-id="81e8c-107">Value</span></span> | <span data-ttu-id="81e8c-108">标签</span><span class="sxs-lookup"><span data-stu-id="81e8c-108">Label</span></span> | <span data-ttu-id="81e8c-109">说明</span><span class="sxs-lookup"><span data-stu-id="81e8c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="81e8c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="81e8c-110">200000000</span></span> | <span data-ttu-id="81e8c-111">未完成</span><span class="sxs-lookup"><span data-stu-id="81e8c-111">Not Complete</span></span> | <span data-ttu-id="81e8c-112">应聘者尚未完成筛选。</span><span class="sxs-lookup"><span data-stu-id="81e8c-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="81e8c-113">200000001</span><span class="sxs-lookup"><span data-stu-id="81e8c-113">200000001</span></span> | <span data-ttu-id="81e8c-114">通过</span><span class="sxs-lookup"><span data-stu-id="81e8c-114">Pass</span></span> | <span data-ttu-id="81e8c-115">应聘者已通过筛选。</span><span class="sxs-lookup"><span data-stu-id="81e8c-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="81e8c-116">200000002</span><span class="sxs-lookup"><span data-stu-id="81e8c-116">200000002</span></span> | <span data-ttu-id="81e8c-117">失败</span><span class="sxs-lookup"><span data-stu-id="81e8c-117">Fail</span></span> | <span data-ttu-id="81e8c-118">应聘者未通过筛选。</span><span class="sxs-lookup"><span data-stu-id="81e8c-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="81e8c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="81e8c-119">See also</span></span>

[<span data-ttu-id="81e8c-120">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="81e8c-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="81e8c-121">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="81e8c-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]