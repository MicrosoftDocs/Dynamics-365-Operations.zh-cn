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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417389"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="74d52-103">MyLeaveRequests 概览</span><span class="sxs-lookup"><span data-stu-id="74d52-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="74d52-104">Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。</span><span class="sxs-lookup"><span data-stu-id="74d52-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="74d52-105">键</span><span class="sxs-lookup"><span data-stu-id="74d52-105">Key</span></span>

  | <span data-ttu-id="74d52-106">属性名称</span><span class="sxs-lookup"><span data-stu-id="74d52-106">Property Name</span></span> | <span data-ttu-id="74d52-107">数据类型</span><span class="sxs-lookup"><span data-stu-id="74d52-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="74d52-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="74d52-108">dataAreaId</span></span>    | <span data-ttu-id="74d52-109">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-109">String</span></span>    |
  | <span data-ttu-id="74d52-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="74d52-110">RequestId</span></span>     | <span data-ttu-id="74d52-111">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-111">String</span></span>    |
  | <span data-ttu-id="74d52-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="74d52-112">LeaveType</span></span>     | <span data-ttu-id="74d52-113">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-113">String</span></span>    |
  | <span data-ttu-id="74d52-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="74d52-114">LeaveDate</span></span>     | <span data-ttu-id="74d52-115">日期</span><span class="sxs-lookup"><span data-stu-id="74d52-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="74d52-116">属性</span><span class="sxs-lookup"><span data-stu-id="74d52-116">Properties</span></span>

  | <span data-ttu-id="74d52-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="74d52-117">Property Name</span></span>     | <span data-ttu-id="74d52-118">数据类型</span><span class="sxs-lookup"><span data-stu-id="74d52-118">Data Type</span></span> | <span data-ttu-id="74d52-119">必需</span><span class="sxs-lookup"><span data-stu-id="74d52-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="74d52-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="74d52-120">dataAreaId</span></span>        | <span data-ttu-id="74d52-121">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-121">String</span></span>    | <span data-ttu-id="74d52-122">X</span><span class="sxs-lookup"><span data-stu-id="74d52-122">X</span></span>        |
  | <span data-ttu-id="74d52-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="74d52-123">RequestId</span></span>         | <span data-ttu-id="74d52-124">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-124">String</span></span>    | <span data-ttu-id="74d52-125">X</span><span class="sxs-lookup"><span data-stu-id="74d52-125">X</span></span>        |
  | <span data-ttu-id="74d52-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="74d52-126">LeaveType</span></span>         | <span data-ttu-id="74d52-127">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-127">String</span></span>    | <span data-ttu-id="74d52-128">X</span><span class="sxs-lookup"><span data-stu-id="74d52-128">X</span></span>        |
  | <span data-ttu-id="74d52-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="74d52-129">LeaveDate</span></span>         | <span data-ttu-id="74d52-130">日期</span><span class="sxs-lookup"><span data-stu-id="74d52-130">Date</span></span>      | <span data-ttu-id="74d52-131">X</span><span class="sxs-lookup"><span data-stu-id="74d52-131">X</span></span>        |
  | <span data-ttu-id="74d52-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="74d52-132">ReasonCodeId</span></span>      | <span data-ttu-id="74d52-133">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-133">String</span></span>    |          |
  | <span data-ttu-id="74d52-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="74d52-134">PersonnelNumber</span></span>   | <span data-ttu-id="74d52-135">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-135">String</span></span>    | <span data-ttu-id="74d52-136">X</span><span class="sxs-lookup"><span data-stu-id="74d52-136">X</span></span>        |
  | <span data-ttu-id="74d52-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="74d52-137">RequestDate</span></span>       | <span data-ttu-id="74d52-138">日期</span><span class="sxs-lookup"><span data-stu-id="74d52-138">Date</span></span>      | <span data-ttu-id="74d52-139">X</span><span class="sxs-lookup"><span data-stu-id="74d52-139">X</span></span>        |
  | <span data-ttu-id="74d52-140">注释</span><span class="sxs-lookup"><span data-stu-id="74d52-140">Comment</span></span>           | <span data-ttu-id="74d52-141">字符串</span><span class="sxs-lookup"><span data-stu-id="74d52-141">String</span></span>    |          |
  | <span data-ttu-id="74d52-142">状态</span><span class="sxs-lookup"><span data-stu-id="74d52-142">Status</span></span>            | <span data-ttu-id="74d52-143">枚举</span><span class="sxs-lookup"><span data-stu-id="74d52-143">Enum</span></span>      | <span data-ttu-id="74d52-144">X</span><span class="sxs-lookup"><span data-stu-id="74d52-144">X</span></span>        |
  | <span data-ttu-id="74d52-145">时长</span><span class="sxs-lookup"><span data-stu-id="74d52-145">Amount</span></span>            | <span data-ttu-id="74d52-146">实数</span><span class="sxs-lookup"><span data-stu-id="74d52-146">Real</span></span>      |          |
  | <span data-ttu-id="74d52-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="74d52-147">HalfDayDefinition</span></span> | <span data-ttu-id="74d52-148">枚举</span><span class="sxs-lookup"><span data-stu-id="74d52-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="74d52-149">行为</span><span class="sxs-lookup"><span data-stu-id="74d52-149">Actions</span></span>

 | <span data-ttu-id="74d52-150">操作名称</span><span class="sxs-lookup"><span data-stu-id="74d52-150">Action Name</span></span>                               | <span data-ttu-id="74d52-151">说明</span><span class="sxs-lookup"><span data-stu-id="74d52-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="74d52-152">submit</span><span class="sxs-lookup"><span data-stu-id="74d52-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="74d52-153">提交要由工作流处理的请求。</span><span class="sxs-lookup"><span data-stu-id="74d52-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="74d52-154">请参阅</span><span class="sxs-lookup"><span data-stu-id="74d52-154">See also</span></span>

- [<span data-ttu-id="74d52-155">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="74d52-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="74d52-156">身份验证</span><span class="sxs-lookup"><span data-stu-id="74d52-156">Authentication</span></span>](hr-developer-api-authentication.md)