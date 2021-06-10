---
title: 招聘请求状态
description: 本主题介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059176"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="d421f-103">招聘请求状态</span><span class="sxs-lookup"><span data-stu-id="d421f-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d421f-104">本主题介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。</span><span class="sxs-lookup"><span data-stu-id="d421f-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d421f-105">物理名称：mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="d421f-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="d421f-106">此枚举为 RecruitingRequest 的状态值提供选项集。</span><span class="sxs-lookup"><span data-stu-id="d421f-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="d421f-107">值</span><span class="sxs-lookup"><span data-stu-id="d421f-107">Value</span></span> | <span data-ttu-id="d421f-108">标签</span><span class="sxs-lookup"><span data-stu-id="d421f-108">Label</span></span> | <span data-ttu-id="d421f-109">说明</span><span class="sxs-lookup"><span data-stu-id="d421f-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d421f-110">200000000</span><span class="sxs-lookup"><span data-stu-id="d421f-110">200000000</span></span> | <span data-ttu-id="d421f-111">草案</span><span class="sxs-lookup"><span data-stu-id="d421f-111">Draft</span></span> | <span data-ttu-id="d421f-112">请求处于草稿状态，尚未准备好进行有效招聘。</span><span class="sxs-lookup"><span data-stu-id="d421f-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="d421f-113">200000001</span><span class="sxs-lookup"><span data-stu-id="d421f-113">200000001</span></span> | <span data-ttu-id="d421f-114">正在审核</span><span class="sxs-lookup"><span data-stu-id="d421f-114">In Review</span></span> | <span data-ttu-id="d421f-115">请求已提交，正在传送以通过工作流进行审批。</span><span class="sxs-lookup"><span data-stu-id="d421f-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="d421f-116">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="d421f-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d421f-117">200000002</span><span class="sxs-lookup"><span data-stu-id="d421f-117">200000002</span></span> | <span data-ttu-id="d421f-118">待处理</span><span class="sxs-lookup"><span data-stu-id="d421f-118">Pending</span></span> | <span data-ttu-id="d421f-119">请求正在等待工作流操作。</span><span class="sxs-lookup"><span data-stu-id="d421f-119">The request is pending workflow action.</span></span> <span data-ttu-id="d421f-120">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="d421f-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d421f-121">200000003</span><span class="sxs-lookup"><span data-stu-id="d421f-121">200000003</span></span> | <span data-ttu-id="d421f-122">已取消</span><span class="sxs-lookup"><span data-stu-id="d421f-122">Canceled</span></span> | <span data-ttu-id="d421f-123">已取消请求。</span><span class="sxs-lookup"><span data-stu-id="d421f-123">The request has been canceled.</span></span> <span data-ttu-id="d421f-124">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="d421f-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d421f-125">200000004</span><span class="sxs-lookup"><span data-stu-id="d421f-125">200000004</span></span> | <span data-ttu-id="d421f-126">已拒绝</span><span class="sxs-lookup"><span data-stu-id="d421f-126">Denied</span></span> | <span data-ttu-id="d421f-127">请求已被拒绝。</span><span class="sxs-lookup"><span data-stu-id="d421f-127">The request has been denied.</span></span> <span data-ttu-id="d421f-128">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="d421f-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="d421f-129">200000005</span><span class="sxs-lookup"><span data-stu-id="d421f-129">200000005</span></span> | <span data-ttu-id="d421f-130">可用</span><span class="sxs-lookup"><span data-stu-id="d421f-130">Active</span></span> | <span data-ttu-id="d421f-131">任何工作流均已完成并获得批准，请求已准备好可以进行有效招聘。</span><span class="sxs-lookup"><span data-stu-id="d421f-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="d421f-132">200000006</span><span class="sxs-lookup"><span data-stu-id="d421f-132">200000006</span></span> | <span data-ttu-id="d421f-133">已结</span><span class="sxs-lookup"><span data-stu-id="d421f-133">Closed</span></span> | <span data-ttu-id="d421f-134">招聘请求已关闭。</span><span class="sxs-lookup"><span data-stu-id="d421f-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d421f-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="d421f-135">See also</span></span>

[<span data-ttu-id="d421f-136">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="d421f-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d421f-137">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="d421f-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]