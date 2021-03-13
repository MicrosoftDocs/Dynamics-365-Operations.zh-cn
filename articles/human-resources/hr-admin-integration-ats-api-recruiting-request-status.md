---
title: 招聘请求状态
description: 本主题介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125946"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="474e0-103">招聘请求状态</span><span class="sxs-lookup"><span data-stu-id="474e0-103">Recruiting request status</span></span>

<span data-ttu-id="474e0-104">本主题介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。</span><span class="sxs-lookup"><span data-stu-id="474e0-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="474e0-105">物理名称：mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="474e0-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="474e0-106">此枚举为 RecruitingRequest 的状态值提供选项集。</span><span class="sxs-lookup"><span data-stu-id="474e0-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="474e0-107">值</span><span class="sxs-lookup"><span data-stu-id="474e0-107">Value</span></span> | <span data-ttu-id="474e0-108">标签</span><span class="sxs-lookup"><span data-stu-id="474e0-108">Label</span></span> | <span data-ttu-id="474e0-109">说明</span><span class="sxs-lookup"><span data-stu-id="474e0-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="474e0-110">200000000</span><span class="sxs-lookup"><span data-stu-id="474e0-110">200000000</span></span> | <span data-ttu-id="474e0-111">草案</span><span class="sxs-lookup"><span data-stu-id="474e0-111">Draft</span></span> | <span data-ttu-id="474e0-112">请求处于草稿状态，尚未准备好进行有效招聘。</span><span class="sxs-lookup"><span data-stu-id="474e0-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="474e0-113">200000001</span><span class="sxs-lookup"><span data-stu-id="474e0-113">200000001</span></span> | <span data-ttu-id="474e0-114">正在审核</span><span class="sxs-lookup"><span data-stu-id="474e0-114">In Review</span></span> | <span data-ttu-id="474e0-115">请求已提交，正在传送以通过工作流进行审批。</span><span class="sxs-lookup"><span data-stu-id="474e0-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="474e0-116">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="474e0-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="474e0-117">200000002</span><span class="sxs-lookup"><span data-stu-id="474e0-117">200000002</span></span> | <span data-ttu-id="474e0-118">待处理</span><span class="sxs-lookup"><span data-stu-id="474e0-118">Pending</span></span> | <span data-ttu-id="474e0-119">请求正在等待工作流操作。</span><span class="sxs-lookup"><span data-stu-id="474e0-119">The request is pending workflow action.</span></span> <span data-ttu-id="474e0-120">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="474e0-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="474e0-121">200000003</span><span class="sxs-lookup"><span data-stu-id="474e0-121">200000003</span></span> | <span data-ttu-id="474e0-122">已取消</span><span class="sxs-lookup"><span data-stu-id="474e0-122">Canceled</span></span> | <span data-ttu-id="474e0-123">已取消请求。</span><span class="sxs-lookup"><span data-stu-id="474e0-123">The request has been canceled.</span></span> <span data-ttu-id="474e0-124">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="474e0-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="474e0-125">200000004</span><span class="sxs-lookup"><span data-stu-id="474e0-125">200000004</span></span> | <span data-ttu-id="474e0-126">已拒绝</span><span class="sxs-lookup"><span data-stu-id="474e0-126">Denied</span></span> | <span data-ttu-id="474e0-127">请求已被拒绝。</span><span class="sxs-lookup"><span data-stu-id="474e0-127">The request has been denied.</span></span> <span data-ttu-id="474e0-128">仅在工作流启用时可用。</span><span class="sxs-lookup"><span data-stu-id="474e0-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="474e0-129">200000005</span><span class="sxs-lookup"><span data-stu-id="474e0-129">200000005</span></span> | <span data-ttu-id="474e0-130">可用</span><span class="sxs-lookup"><span data-stu-id="474e0-130">Active</span></span> | <span data-ttu-id="474e0-131">任何工作流均已完成并获得批准，请求已准备好可以进行有效招聘。</span><span class="sxs-lookup"><span data-stu-id="474e0-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="474e0-132">200000006</span><span class="sxs-lookup"><span data-stu-id="474e0-132">200000006</span></span> | <span data-ttu-id="474e0-133">已结</span><span class="sxs-lookup"><span data-stu-id="474e0-133">Closed</span></span> | <span data-ttu-id="474e0-134">招聘请求已关闭。</span><span class="sxs-lookup"><span data-stu-id="474e0-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="474e0-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="474e0-135">See also</span></span>

[<span data-ttu-id="474e0-136">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="474e0-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="474e0-137">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="474e0-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
