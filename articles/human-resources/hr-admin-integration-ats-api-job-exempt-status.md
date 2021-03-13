---
title: 工作免除情况
description: 本主题介绍 Dynamics 365 Human Resources 的工作免除情况选项集。
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125561"
---
# <a name="job-exempt-status"></a><span data-ttu-id="aa45a-103">工作免除情况</span><span class="sxs-lookup"><span data-stu-id="aa45a-103">Job exempt status</span></span>

<span data-ttu-id="aa45a-104">本主题介绍 Dynamics 365 Human Resources 的工作免除情况选项集。</span><span class="sxs-lookup"><span data-stu-id="aa45a-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="aa45a-105">物理名称：cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="aa45a-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="aa45a-106">此枚举为 FLSA 工作免除情况值指定选项集。</span><span class="sxs-lookup"><span data-stu-id="aa45a-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="aa45a-107">在现有 cdm_jobexemptstatus 选项集中提供。</span><span class="sxs-lookup"><span data-stu-id="aa45a-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="aa45a-108">值</span><span class="sxs-lookup"><span data-stu-id="aa45a-108">Value</span></span> | <span data-ttu-id="aa45a-109">标签</span><span class="sxs-lookup"><span data-stu-id="aa45a-109">Label</span></span> | <span data-ttu-id="aa45a-110">说明</span><span class="sxs-lookup"><span data-stu-id="aa45a-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aa45a-111">200000000</span><span class="sxs-lookup"><span data-stu-id="aa45a-111">200000000</span></span> | <span data-ttu-id="aa45a-112">豁免</span><span class="sxs-lookup"><span data-stu-id="aa45a-112">Exempt</span></span> | <span data-ttu-id="aa45a-113">工作根据 FLSA 准则确定免除情况。</span><span class="sxs-lookup"><span data-stu-id="aa45a-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="aa45a-114">200000001</span><span class="sxs-lookup"><span data-stu-id="aa45a-114">200000001</span></span> | <span data-ttu-id="aa45a-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="aa45a-115">NonExempt</span></span> | <span data-ttu-id="aa45a-116">工作根据 FLSA 准则为不免除状态。</span><span class="sxs-lookup"><span data-stu-id="aa45a-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="aa45a-117">200000002</span><span class="sxs-lookup"><span data-stu-id="aa45a-117">200000002</span></span> | <span data-ttu-id="aa45a-118">不适用</span><span class="sxs-lookup"><span data-stu-id="aa45a-118">Does Not Apply</span></span> | <span data-ttu-id="aa45a-119">FLSA 状态准则不适用于此工作。</span><span class="sxs-lookup"><span data-stu-id="aa45a-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa45a-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="aa45a-120">See also</span></span>

[<span data-ttu-id="aa45a-121">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="aa45a-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="aa45a-122">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="aa45a-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
