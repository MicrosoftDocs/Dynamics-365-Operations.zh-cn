---
title: MyLeaveRequests 概览
description: Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115528"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="4fa38-103">MyLeaveRequests 概览</span><span class="sxs-lookup"><span data-stu-id="4fa38-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="4fa38-104">Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。</span><span class="sxs-lookup"><span data-stu-id="4fa38-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="4fa38-105">键</span><span class="sxs-lookup"><span data-stu-id="4fa38-105">Key</span></span>

  | <span data-ttu-id="4fa38-106">属性名称</span><span class="sxs-lookup"><span data-stu-id="4fa38-106">Property Name</span></span> | <span data-ttu-id="4fa38-107">数据类型</span><span class="sxs-lookup"><span data-stu-id="4fa38-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="4fa38-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="4fa38-108">dataAreaId</span></span>    | <span data-ttu-id="4fa38-109">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-109">String</span></span>    |
  | <span data-ttu-id="4fa38-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="4fa38-110">RequestId</span></span>     | <span data-ttu-id="4fa38-111">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-111">String</span></span>    |
  | <span data-ttu-id="4fa38-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="4fa38-112">LeaveType</span></span>     | <span data-ttu-id="4fa38-113">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-113">String</span></span>    |
  | <span data-ttu-id="4fa38-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="4fa38-114">LeaveDate</span></span>     | <span data-ttu-id="4fa38-115">日期</span><span class="sxs-lookup"><span data-stu-id="4fa38-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="4fa38-116">属性</span><span class="sxs-lookup"><span data-stu-id="4fa38-116">Properties</span></span>

  | <span data-ttu-id="4fa38-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="4fa38-117">Property Name</span></span>     | <span data-ttu-id="4fa38-118">数据类型</span><span class="sxs-lookup"><span data-stu-id="4fa38-118">Data Type</span></span> | <span data-ttu-id="4fa38-119">必需</span><span class="sxs-lookup"><span data-stu-id="4fa38-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="4fa38-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="4fa38-120">dataAreaId</span></span>        | <span data-ttu-id="4fa38-121">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-121">String</span></span>    | <span data-ttu-id="4fa38-122">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-122">X</span></span>        |
  | <span data-ttu-id="4fa38-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="4fa38-123">RequestId</span></span>         | <span data-ttu-id="4fa38-124">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-124">String</span></span>    | <span data-ttu-id="4fa38-125">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-125">X</span></span>        |
  | <span data-ttu-id="4fa38-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="4fa38-126">LeaveType</span></span>         | <span data-ttu-id="4fa38-127">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-127">String</span></span>    | <span data-ttu-id="4fa38-128">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-128">X</span></span>        |
  | <span data-ttu-id="4fa38-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="4fa38-129">LeaveDate</span></span>         | <span data-ttu-id="4fa38-130">日期</span><span class="sxs-lookup"><span data-stu-id="4fa38-130">Date</span></span>      | <span data-ttu-id="4fa38-131">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-131">X</span></span>        |
  | <span data-ttu-id="4fa38-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="4fa38-132">ReasonCodeId</span></span>      | <span data-ttu-id="4fa38-133">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-133">String</span></span>    |          |
  | <span data-ttu-id="4fa38-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="4fa38-134">PersonnelNumber</span></span>   | <span data-ttu-id="4fa38-135">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-135">String</span></span>    | <span data-ttu-id="4fa38-136">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-136">X</span></span>        |
  | <span data-ttu-id="4fa38-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="4fa38-137">RequestDate</span></span>       | <span data-ttu-id="4fa38-138">日期</span><span class="sxs-lookup"><span data-stu-id="4fa38-138">Date</span></span>      | <span data-ttu-id="4fa38-139">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-139">X</span></span>        |
  | <span data-ttu-id="4fa38-140">注释</span><span class="sxs-lookup"><span data-stu-id="4fa38-140">Comment</span></span>           | <span data-ttu-id="4fa38-141">字符串</span><span class="sxs-lookup"><span data-stu-id="4fa38-141">String</span></span>    |          |
  | <span data-ttu-id="4fa38-142">状态</span><span class="sxs-lookup"><span data-stu-id="4fa38-142">Status</span></span>            | <span data-ttu-id="4fa38-143">枚举</span><span class="sxs-lookup"><span data-stu-id="4fa38-143">Enum</span></span>      | <span data-ttu-id="4fa38-144">X</span><span class="sxs-lookup"><span data-stu-id="4fa38-144">X</span></span>        |
  | <span data-ttu-id="4fa38-145">时长</span><span class="sxs-lookup"><span data-stu-id="4fa38-145">Amount</span></span>            | <span data-ttu-id="4fa38-146">实数</span><span class="sxs-lookup"><span data-stu-id="4fa38-146">Real</span></span>      |          |
  | <span data-ttu-id="4fa38-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="4fa38-147">HalfDayDefinition</span></span> | <span data-ttu-id="4fa38-148">枚举</span><span class="sxs-lookup"><span data-stu-id="4fa38-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="4fa38-149">行为</span><span class="sxs-lookup"><span data-stu-id="4fa38-149">Actions</span></span>

 | <span data-ttu-id="4fa38-150">操作名称</span><span class="sxs-lookup"><span data-stu-id="4fa38-150">Action Name</span></span>                               | <span data-ttu-id="4fa38-151">说明</span><span class="sxs-lookup"><span data-stu-id="4fa38-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="4fa38-152">submit</span><span class="sxs-lookup"><span data-stu-id="4fa38-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="4fa38-153">提交要由工作流处理的请求。</span><span class="sxs-lookup"><span data-stu-id="4fa38-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4fa38-154">请参阅</span><span class="sxs-lookup"><span data-stu-id="4fa38-154">See also</span></span>

- [<span data-ttu-id="4fa38-155">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="4fa38-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="4fa38-156">身份验证</span><span class="sxs-lookup"><span data-stu-id="4fa38-156">Authentication</span></span>](hr-developer-api-authentication.md)