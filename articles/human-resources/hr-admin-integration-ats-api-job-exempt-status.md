---
title: 工作免除情况
description: 本主题介绍 Dynamics 365 Human Resources 的工作免除情况选项集。
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
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798289"
---
# <a name="job-exempt-status"></a><span data-ttu-id="0482b-103">工作免除情况</span><span class="sxs-lookup"><span data-stu-id="0482b-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0482b-104">本主题介绍 Dynamics 365 Human Resources 的工作免除情况选项集。</span><span class="sxs-lookup"><span data-stu-id="0482b-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0482b-105">物理名称：cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="0482b-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="0482b-106">此枚举为 FLSA 工作免除情况值指定选项集。</span><span class="sxs-lookup"><span data-stu-id="0482b-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="0482b-107">在现有 cdm_jobexemptstatus 选项集中提供。</span><span class="sxs-lookup"><span data-stu-id="0482b-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="0482b-108">值</span><span class="sxs-lookup"><span data-stu-id="0482b-108">Value</span></span> | <span data-ttu-id="0482b-109">标签</span><span class="sxs-lookup"><span data-stu-id="0482b-109">Label</span></span> | <span data-ttu-id="0482b-110">说明</span><span class="sxs-lookup"><span data-stu-id="0482b-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0482b-111">200000000</span><span class="sxs-lookup"><span data-stu-id="0482b-111">200000000</span></span> | <span data-ttu-id="0482b-112">豁免</span><span class="sxs-lookup"><span data-stu-id="0482b-112">Exempt</span></span> | <span data-ttu-id="0482b-113">工作根据 FLSA 准则确定免除情况。</span><span class="sxs-lookup"><span data-stu-id="0482b-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="0482b-114">200000001</span><span class="sxs-lookup"><span data-stu-id="0482b-114">200000001</span></span> | <span data-ttu-id="0482b-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="0482b-115">NonExempt</span></span> | <span data-ttu-id="0482b-116">工作根据 FLSA 准则为不免除状态。</span><span class="sxs-lookup"><span data-stu-id="0482b-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="0482b-117">200000002</span><span class="sxs-lookup"><span data-stu-id="0482b-117">200000002</span></span> | <span data-ttu-id="0482b-118">不适用</span><span class="sxs-lookup"><span data-stu-id="0482b-118">Does Not Apply</span></span> | <span data-ttu-id="0482b-119">FLSA 状态准则不适用于此工作。</span><span class="sxs-lookup"><span data-stu-id="0482b-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0482b-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="0482b-120">See also</span></span>

[<span data-ttu-id="0482b-121">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="0482b-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0482b-122">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="0482b-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]