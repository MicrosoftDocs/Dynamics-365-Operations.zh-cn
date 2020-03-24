---
title: MyLeaveRequests 概览
description: Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092029"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="5cdc0-103">MyLeaveRequests 概览</span><span class="sxs-lookup"><span data-stu-id="5cdc0-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="5cdc0-104">Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。</span><span class="sxs-lookup"><span data-stu-id="5cdc0-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="5cdc0-105">键</span><span class="sxs-lookup"><span data-stu-id="5cdc0-105">Key</span></span>

  | <span data-ttu-id="5cdc0-106">属性名称</span><span class="sxs-lookup"><span data-stu-id="5cdc0-106">Property Name</span></span> | <span data-ttu-id="5cdc0-107">数据类型</span><span class="sxs-lookup"><span data-stu-id="5cdc0-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="5cdc0-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5cdc0-108">dataAreaId</span></span>    | <span data-ttu-id="5cdc0-109">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-109">String</span></span>    |
  | <span data-ttu-id="5cdc0-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="5cdc0-110">RequestId</span></span>     | <span data-ttu-id="5cdc0-111">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-111">String</span></span>    |
  | <span data-ttu-id="5cdc0-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5cdc0-112">LeaveType</span></span>     | <span data-ttu-id="5cdc0-113">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-113">String</span></span>    |
  | <span data-ttu-id="5cdc0-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5cdc0-114">LeaveDate</span></span>     | <span data-ttu-id="5cdc0-115">日期</span><span class="sxs-lookup"><span data-stu-id="5cdc0-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="5cdc0-116">属性</span><span class="sxs-lookup"><span data-stu-id="5cdc0-116">Properties</span></span>

  | <span data-ttu-id="5cdc0-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="5cdc0-117">Property Name</span></span>     | <span data-ttu-id="5cdc0-118">数据类型</span><span class="sxs-lookup"><span data-stu-id="5cdc0-118">Data Type</span></span> | <span data-ttu-id="5cdc0-119">必需</span><span class="sxs-lookup"><span data-stu-id="5cdc0-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="5cdc0-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5cdc0-120">dataAreaId</span></span>        | <span data-ttu-id="5cdc0-121">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-121">String</span></span>    | <span data-ttu-id="5cdc0-122">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-122">X</span></span>        |
  | <span data-ttu-id="5cdc0-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="5cdc0-123">RequestId</span></span>         | <span data-ttu-id="5cdc0-124">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-124">String</span></span>    | <span data-ttu-id="5cdc0-125">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-125">X</span></span>        |
  | <span data-ttu-id="5cdc0-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5cdc0-126">LeaveType</span></span>         | <span data-ttu-id="5cdc0-127">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-127">String</span></span>    | <span data-ttu-id="5cdc0-128">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-128">X</span></span>        |
  | <span data-ttu-id="5cdc0-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5cdc0-129">LeaveDate</span></span>         | <span data-ttu-id="5cdc0-130">日期</span><span class="sxs-lookup"><span data-stu-id="5cdc0-130">Date</span></span>      | <span data-ttu-id="5cdc0-131">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-131">X</span></span>        |
  | <span data-ttu-id="5cdc0-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="5cdc0-132">ReasonCodeId</span></span>      | <span data-ttu-id="5cdc0-133">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-133">String</span></span>    |          |
  | <span data-ttu-id="5cdc0-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="5cdc0-134">PersonnelNumber</span></span>   | <span data-ttu-id="5cdc0-135">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-135">String</span></span>    | <span data-ttu-id="5cdc0-136">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-136">X</span></span>        |
  | <span data-ttu-id="5cdc0-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="5cdc0-137">RequestDate</span></span>       | <span data-ttu-id="5cdc0-138">日期</span><span class="sxs-lookup"><span data-stu-id="5cdc0-138">Date</span></span>      | <span data-ttu-id="5cdc0-139">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-139">X</span></span>        |
  | <span data-ttu-id="5cdc0-140">注释</span><span class="sxs-lookup"><span data-stu-id="5cdc0-140">Comment</span></span>           | <span data-ttu-id="5cdc0-141">字符串</span><span class="sxs-lookup"><span data-stu-id="5cdc0-141">String</span></span>    |          |
  | <span data-ttu-id="5cdc0-142">状态</span><span class="sxs-lookup"><span data-stu-id="5cdc0-142">Status</span></span>            | <span data-ttu-id="5cdc0-143">枚举</span><span class="sxs-lookup"><span data-stu-id="5cdc0-143">Enum</span></span>      | <span data-ttu-id="5cdc0-144">X</span><span class="sxs-lookup"><span data-stu-id="5cdc0-144">X</span></span>        |
  | <span data-ttu-id="5cdc0-145">时长</span><span class="sxs-lookup"><span data-stu-id="5cdc0-145">Amount</span></span>            | <span data-ttu-id="5cdc0-146">实数</span><span class="sxs-lookup"><span data-stu-id="5cdc0-146">Real</span></span>      |          |
  | <span data-ttu-id="5cdc0-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="5cdc0-147">HalfDayDefinition</span></span> | <span data-ttu-id="5cdc0-148">枚举</span><span class="sxs-lookup"><span data-stu-id="5cdc0-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="5cdc0-149">行为</span><span class="sxs-lookup"><span data-stu-id="5cdc0-149">Actions</span></span>

 | <span data-ttu-id="5cdc0-150">操作名称</span><span class="sxs-lookup"><span data-stu-id="5cdc0-150">Action Name</span></span>                               | <span data-ttu-id="5cdc0-151">说明</span><span class="sxs-lookup"><span data-stu-id="5cdc0-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="5cdc0-152">submit</span><span class="sxs-lookup"><span data-stu-id="5cdc0-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="5cdc0-153">提交要由工作流处理的请求。</span><span class="sxs-lookup"><span data-stu-id="5cdc0-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5cdc0-154">请参阅</span><span class="sxs-lookup"><span data-stu-id="5cdc0-154">See also</span></span>

- [<span data-ttu-id="5cdc0-155">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="5cdc0-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="5cdc0-156">身份验证</span><span class="sxs-lookup"><span data-stu-id="5cdc0-156">Authentication</span></span>](hr-developer-api-authentication.md)