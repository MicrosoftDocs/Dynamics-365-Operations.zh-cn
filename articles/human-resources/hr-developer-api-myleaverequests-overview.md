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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465502"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="a1b21-103">MyLeaveRequests 概览</span><span class="sxs-lookup"><span data-stu-id="a1b21-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a1b21-104">Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。</span><span class="sxs-lookup"><span data-stu-id="a1b21-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="a1b21-105">键</span><span class="sxs-lookup"><span data-stu-id="a1b21-105">Key</span></span>

  | <span data-ttu-id="a1b21-106">属性名称</span><span class="sxs-lookup"><span data-stu-id="a1b21-106">Property Name</span></span> | <span data-ttu-id="a1b21-107">数据类型</span><span class="sxs-lookup"><span data-stu-id="a1b21-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="a1b21-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="a1b21-108">dataAreaId</span></span>    | <span data-ttu-id="a1b21-109">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-109">String</span></span>    |
  | <span data-ttu-id="a1b21-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="a1b21-110">RequestId</span></span>     | <span data-ttu-id="a1b21-111">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-111">String</span></span>    |
  | <span data-ttu-id="a1b21-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="a1b21-112">LeaveType</span></span>     | <span data-ttu-id="a1b21-113">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-113">String</span></span>    |
  | <span data-ttu-id="a1b21-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="a1b21-114">LeaveDate</span></span>     | <span data-ttu-id="a1b21-115">日期</span><span class="sxs-lookup"><span data-stu-id="a1b21-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="a1b21-116">属性</span><span class="sxs-lookup"><span data-stu-id="a1b21-116">Properties</span></span>

  | <span data-ttu-id="a1b21-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="a1b21-117">Property Name</span></span>     | <span data-ttu-id="a1b21-118">数据类型</span><span class="sxs-lookup"><span data-stu-id="a1b21-118">Data Type</span></span> | <span data-ttu-id="a1b21-119">必需</span><span class="sxs-lookup"><span data-stu-id="a1b21-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="a1b21-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="a1b21-120">dataAreaId</span></span>        | <span data-ttu-id="a1b21-121">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-121">String</span></span>    | <span data-ttu-id="a1b21-122">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-122">X</span></span>        |
  | <span data-ttu-id="a1b21-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="a1b21-123">RequestId</span></span>         | <span data-ttu-id="a1b21-124">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-124">String</span></span>    | <span data-ttu-id="a1b21-125">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-125">X</span></span>        |
  | <span data-ttu-id="a1b21-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="a1b21-126">LeaveType</span></span>         | <span data-ttu-id="a1b21-127">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-127">String</span></span>    | <span data-ttu-id="a1b21-128">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-128">X</span></span>        |
  | <span data-ttu-id="a1b21-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="a1b21-129">LeaveDate</span></span>         | <span data-ttu-id="a1b21-130">日期</span><span class="sxs-lookup"><span data-stu-id="a1b21-130">Date</span></span>      | <span data-ttu-id="a1b21-131">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-131">X</span></span>        |
  | <span data-ttu-id="a1b21-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="a1b21-132">ReasonCodeId</span></span>      | <span data-ttu-id="a1b21-133">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-133">String</span></span>    |          |
  | <span data-ttu-id="a1b21-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="a1b21-134">PersonnelNumber</span></span>   | <span data-ttu-id="a1b21-135">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-135">String</span></span>    | <span data-ttu-id="a1b21-136">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-136">X</span></span>        |
  | <span data-ttu-id="a1b21-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="a1b21-137">RequestDate</span></span>       | <span data-ttu-id="a1b21-138">日期</span><span class="sxs-lookup"><span data-stu-id="a1b21-138">Date</span></span>      | <span data-ttu-id="a1b21-139">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-139">X</span></span>        |
  | <span data-ttu-id="a1b21-140">注释</span><span class="sxs-lookup"><span data-stu-id="a1b21-140">Comment</span></span>           | <span data-ttu-id="a1b21-141">字符串</span><span class="sxs-lookup"><span data-stu-id="a1b21-141">String</span></span>    |          |
  | <span data-ttu-id="a1b21-142">状态</span><span class="sxs-lookup"><span data-stu-id="a1b21-142">Status</span></span>            | <span data-ttu-id="a1b21-143">枚举</span><span class="sxs-lookup"><span data-stu-id="a1b21-143">Enum</span></span>      | <span data-ttu-id="a1b21-144">X</span><span class="sxs-lookup"><span data-stu-id="a1b21-144">X</span></span>        |
  | <span data-ttu-id="a1b21-145">时长</span><span class="sxs-lookup"><span data-stu-id="a1b21-145">Amount</span></span>            | <span data-ttu-id="a1b21-146">实数</span><span class="sxs-lookup"><span data-stu-id="a1b21-146">Real</span></span>      |          |
  | <span data-ttu-id="a1b21-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="a1b21-147">HalfDayDefinition</span></span> | <span data-ttu-id="a1b21-148">枚举</span><span class="sxs-lookup"><span data-stu-id="a1b21-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="a1b21-149">行为</span><span class="sxs-lookup"><span data-stu-id="a1b21-149">Actions</span></span>

 | <span data-ttu-id="a1b21-150">操作名称</span><span class="sxs-lookup"><span data-stu-id="a1b21-150">Action Name</span></span>                               | <span data-ttu-id="a1b21-151">说明</span><span class="sxs-lookup"><span data-stu-id="a1b21-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="a1b21-152">submit</span><span class="sxs-lookup"><span data-stu-id="a1b21-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="a1b21-153">提交要由工作流处理的请求。</span><span class="sxs-lookup"><span data-stu-id="a1b21-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a1b21-154">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1b21-154">See also</span></span>

- [<span data-ttu-id="a1b21-155">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="a1b21-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="a1b21-156">身份验证</span><span class="sxs-lookup"><span data-stu-id="a1b21-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]