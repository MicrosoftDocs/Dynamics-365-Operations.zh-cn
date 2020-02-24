---
title: MyLeaveRequests 概览
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008219"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="258e9-102">MyLeaveRequests 概览</span><span class="sxs-lookup"><span data-stu-id="258e9-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="258e9-103">Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。</span><span class="sxs-lookup"><span data-stu-id="258e9-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="258e9-104">键</span><span class="sxs-lookup"><span data-stu-id="258e9-104">Key</span></span>

  | <span data-ttu-id="258e9-105">属性名称</span><span class="sxs-lookup"><span data-stu-id="258e9-105">Property Name</span></span> | <span data-ttu-id="258e9-106">数据类型</span><span class="sxs-lookup"><span data-stu-id="258e9-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="258e9-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="258e9-107">dataAreaId</span></span>    | <span data-ttu-id="258e9-108">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-108">String</span></span>    |
  | <span data-ttu-id="258e9-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="258e9-109">RequestId</span></span>     | <span data-ttu-id="258e9-110">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-110">String</span></span>    |
  | <span data-ttu-id="258e9-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="258e9-111">LeaveType</span></span>     | <span data-ttu-id="258e9-112">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-112">String</span></span>    |
  | <span data-ttu-id="258e9-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="258e9-113">LeaveDate</span></span>     | <span data-ttu-id="258e9-114">日期</span><span class="sxs-lookup"><span data-stu-id="258e9-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="258e9-115">属性</span><span class="sxs-lookup"><span data-stu-id="258e9-115">Properties</span></span>

  | <span data-ttu-id="258e9-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="258e9-116">Property Name</span></span>     | <span data-ttu-id="258e9-117">数据类型</span><span class="sxs-lookup"><span data-stu-id="258e9-117">Data Type</span></span> | <span data-ttu-id="258e9-118">必需</span><span class="sxs-lookup"><span data-stu-id="258e9-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="258e9-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="258e9-119">dataAreaId</span></span>        | <span data-ttu-id="258e9-120">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-120">String</span></span>    | <span data-ttu-id="258e9-121">X</span><span class="sxs-lookup"><span data-stu-id="258e9-121">X</span></span>        |
  | <span data-ttu-id="258e9-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="258e9-122">RequestId</span></span>         | <span data-ttu-id="258e9-123">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-123">String</span></span>    | <span data-ttu-id="258e9-124">X</span><span class="sxs-lookup"><span data-stu-id="258e9-124">X</span></span>        |
  | <span data-ttu-id="258e9-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="258e9-125">LeaveType</span></span>         | <span data-ttu-id="258e9-126">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-126">String</span></span>    | <span data-ttu-id="258e9-127">X</span><span class="sxs-lookup"><span data-stu-id="258e9-127">X</span></span>        |
  | <span data-ttu-id="258e9-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="258e9-128">LeaveDate</span></span>         | <span data-ttu-id="258e9-129">日期</span><span class="sxs-lookup"><span data-stu-id="258e9-129">Date</span></span>      | <span data-ttu-id="258e9-130">X</span><span class="sxs-lookup"><span data-stu-id="258e9-130">X</span></span>        |
  | <span data-ttu-id="258e9-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="258e9-131">ReasonCodeId</span></span>      | <span data-ttu-id="258e9-132">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-132">String</span></span>    |          |
  | <span data-ttu-id="258e9-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="258e9-133">PersonnelNumber</span></span>   | <span data-ttu-id="258e9-134">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-134">String</span></span>    | <span data-ttu-id="258e9-135">X</span><span class="sxs-lookup"><span data-stu-id="258e9-135">X</span></span>        |
  | <span data-ttu-id="258e9-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="258e9-136">RequestDate</span></span>       | <span data-ttu-id="258e9-137">日期</span><span class="sxs-lookup"><span data-stu-id="258e9-137">Date</span></span>      | <span data-ttu-id="258e9-138">X</span><span class="sxs-lookup"><span data-stu-id="258e9-138">X</span></span>        |
  | <span data-ttu-id="258e9-139">注释</span><span class="sxs-lookup"><span data-stu-id="258e9-139">Comment</span></span>           | <span data-ttu-id="258e9-140">字符串</span><span class="sxs-lookup"><span data-stu-id="258e9-140">String</span></span>    |          |
  | <span data-ttu-id="258e9-141">状态</span><span class="sxs-lookup"><span data-stu-id="258e9-141">Status</span></span>            | <span data-ttu-id="258e9-142">枚举</span><span class="sxs-lookup"><span data-stu-id="258e9-142">Enum</span></span>      | <span data-ttu-id="258e9-143">X</span><span class="sxs-lookup"><span data-stu-id="258e9-143">X</span></span>        |
  | <span data-ttu-id="258e9-144">时长</span><span class="sxs-lookup"><span data-stu-id="258e9-144">Amount</span></span>            | <span data-ttu-id="258e9-145">实数</span><span class="sxs-lookup"><span data-stu-id="258e9-145">Real</span></span>      |          |
  | <span data-ttu-id="258e9-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="258e9-146">HalfDayDefinition</span></span> | <span data-ttu-id="258e9-147">枚举</span><span class="sxs-lookup"><span data-stu-id="258e9-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="258e9-148">行为</span><span class="sxs-lookup"><span data-stu-id="258e9-148">Actions</span></span>

 | <span data-ttu-id="258e9-149">操作名称</span><span class="sxs-lookup"><span data-stu-id="258e9-149">Action Name</span></span>                               | <span data-ttu-id="258e9-150">说明</span><span class="sxs-lookup"><span data-stu-id="258e9-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="258e9-151">submit</span><span class="sxs-lookup"><span data-stu-id="258e9-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="258e9-152">提交要由工作流处理的请求。</span><span class="sxs-lookup"><span data-stu-id="258e9-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="258e9-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="258e9-153">See also</span></span>

- [<span data-ttu-id="258e9-154">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="258e9-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="258e9-155">身份验证</span><span class="sxs-lookup"><span data-stu-id="258e9-155">Authentication</span></span>](hr-developer-api-authentication.md)