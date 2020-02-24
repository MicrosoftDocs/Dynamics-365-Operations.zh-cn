---
title: 将请假申请提交至工作流
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008270"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="d0674-102">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="d0674-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="d0674-103">在 Microsoft Dynamics 365 Human Resources 中，您可以使用 MyLeaveRequests submit() 应用程序编程接口 (API) 向工作流提交休假请求。</span><span class="sxs-lookup"><span data-stu-id="d0674-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="d0674-104">此 API 在 MyLeaveRequests OData 实体上作为操作公开。</span><span class="sxs-lookup"><span data-stu-id="d0674-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d0674-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="d0674-105">Prerequisites</span></span>

<span data-ttu-id="d0674-106">休假请求必须保存在数据库中，并且必须可以通过 MyLeaveRequests 实体进行检索。</span><span class="sxs-lookup"><span data-stu-id="d0674-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="d0674-107">权限</span><span class="sxs-lookup"><span data-stu-id="d0674-107">Permissions</span></span>

<span data-ttu-id="d0674-108">调用此 API 需要下列权限之一。</span><span class="sxs-lookup"><span data-stu-id="d0674-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d0674-109">有关权限以及如何选择权限的详细信息，请参阅[身份验证](hr-developer-api-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="d0674-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="d0674-110">权限类型</span><span class="sxs-lookup"><span data-stu-id="d0674-110">Permission type</span></span>                    | <span data-ttu-id="d0674-111">权限（从最低权限到最高权限）</span><span class="sxs-lookup"><span data-stu-id="d0674-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="d0674-112">委托（工作或学校帐户）</span><span class="sxs-lookup"><span data-stu-id="d0674-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d0674-113">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="d0674-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="d0674-114">HTTPS 请求</span><span class="sxs-lookup"><span data-stu-id="d0674-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="d0674-115">此请求符合 OData 标准。</span><span class="sxs-lookup"><span data-stu-id="d0674-115">The request conforms to OData standards.</span></span> <span data-ttu-id="d0674-116">{requestId}、{leaveType}、{leaveDate} 和 {dataArea} 参数引用构成 MyLeaveRequests 实体的组合自然键的字段。</span><span class="sxs-lookup"><span data-stu-id="d0674-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="d0674-117">虽然 MyLeaveRequests 实体的字段引用休假请求中的单独一行，但调用提交 API 会将整个休假请求（所有行）都提交到工作流。</span><span class="sxs-lookup"><span data-stu-id="d0674-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="d0674-118">请求标题</span><span class="sxs-lookup"><span data-stu-id="d0674-118">Request headers</span></span>

| <span data-ttu-id="d0674-119">​页眉</span><span class="sxs-lookup"><span data-stu-id="d0674-119">Header</span></span>         | <span data-ttu-id="d0674-120">Value</span><span class="sxs-lookup"><span data-stu-id="d0674-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="d0674-121">授权</span><span class="sxs-lookup"><span data-stu-id="d0674-121">Authorization</span></span>  | <span data-ttu-id="d0674-122">不记名 {token}（必需）</span><span class="sxs-lookup"><span data-stu-id="d0674-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="d0674-123">内容类型</span><span class="sxs-lookup"><span data-stu-id="d0674-123">Content-Type</span></span>   | <span data-ttu-id="d0674-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d0674-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="d0674-125">请求正文</span><span class="sxs-lookup"><span data-stu-id="d0674-125">Request body</span></span>

<span data-ttu-id="d0674-126">不要为此方法提供请求正文。</span><span class="sxs-lookup"><span data-stu-id="d0674-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="d0674-127">响应</span><span class="sxs-lookup"><span data-stu-id="d0674-127">Response</span></span>

<span data-ttu-id="d0674-128">成功的响应永远是 **204 无内容**响应。</span><span class="sxs-lookup"><span data-stu-id="d0674-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="d0674-129">未经授权的调用方将收到 **401 未授权**或 **403 已禁止**响应。</span><span class="sxs-lookup"><span data-stu-id="d0674-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="d0674-130">如果提交未成功（例如，由于验证），响应将为 **500 服务器错误**，响应正文将包括包含更多详细信息的 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="d0674-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="d0674-131">示例</span><span class="sxs-lookup"><span data-stu-id="d0674-131">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="d0674-132">验证和错误消息</span><span class="sxs-lookup"><span data-stu-id="d0674-132">Validation and error messages</span></span>

<span data-ttu-id="d0674-133">作为对提交 API 的调用的一部分，Human Resources 在提交之前执行业务逻辑验证，以确保休假请求处于有效状态，可以提交。</span><span class="sxs-lookup"><span data-stu-id="d0674-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="d0674-134">如果验证失败，您可能会在响应中收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="d0674-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="d0674-135">此请求将使“{LeaveTypeId}”余额小于 {date} 所允许的最低余额。</span><span class="sxs-lookup"><span data-stu-id="d0674-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="d0674-136">无法提交“已完成”状态的休息时间请求。</span><span class="sxs-lookup"><span data-stu-id="d0674-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="d0674-137">未进行任何更改，无法提交或保存请求。</span><span class="sxs-lookup"><span data-stu-id="d0674-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="d0674-138">请添加或更新金额或休假类型，然后重试。</span><span class="sxs-lookup"><span data-stu-id="d0674-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="d0674-139">输入的休息时间请求有一天或多天的日期和休假类型与现有的待处理请求相同。</span><span class="sxs-lookup"><span data-stu-id="d0674-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="d0674-140">请撤回现有请求，进行更改。</span><span class="sxs-lookup"><span data-stu-id="d0674-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="d0674-141">原因代码“{ReasonCodeId}”不适用于请求中的任何休假类型。</span><span class="sxs-lookup"><span data-stu-id="d0674-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="d0674-142">休假类型“{LeaveTypeId}”需要有原因代码。</span><span class="sxs-lookup"><span data-stu-id="d0674-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="d0674-143">请选择适当的类型和原因代码。</span><span class="sxs-lookup"><span data-stu-id="d0674-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="d0674-144">休息时间未成功提交。</span><span class="sxs-lookup"><span data-stu-id="d0674-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="d0674-145">休息时间已另存为草稿请求。</span><span class="sxs-lookup"><span data-stu-id="d0674-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0674-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0674-146">See also</span></span>

- [<span data-ttu-id="d0674-147">MyLeaveRequests 概览</span><span class="sxs-lookup"><span data-stu-id="d0674-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="d0674-148">身份验证</span><span class="sxs-lookup"><span data-stu-id="d0674-148">Authentication</span></span>](hr-developer-api-authentication.md)