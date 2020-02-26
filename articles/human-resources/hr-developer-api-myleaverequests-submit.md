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
# <a name="submit-a-leave-request-to-workflow"></a>将请假申请提交至工作流

在 Microsoft Dynamics 365 Human Resources 中，您可以使用 MyLeaveRequests submit() 应用程序编程接口 (API) 向工作流提交休假请求。 此 API 在 MyLeaveRequests OData 实体上作为操作公开。

## <a name="prerequisites"></a>先决条件

休假请求必须保存在数据库中，并且必须可以通过 MyLeaveRequests 实体进行检索。

## <a name="permissions"></a>权限

调用此 API 需要下列权限之一。 有关权限以及如何选择权限的详细信息，请参阅[身份验证](hr-developer-api-authentication.md)。

| 权限类型                    | 权限（从最低权限到最高权限） |
|------------------------------------|--------------------------------------------------------|
| 委托（工作或学校帐户） | user\_impersonation                                    |

## <a name="https-request"></a>HTTPS 请求

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

此请求符合 OData 标准。 {requestId}、{leaveType}、{leaveDate} 和 {dataArea} 参数引用构成 MyLeaveRequests 实体的组合自然键的字段。

> [!NOTE]
> 虽然 MyLeaveRequests 实体的字段引用休假请求中的单独一行，但调用提交 API 会将整个休假请求（所有行）都提交到工作流。

### <a name="request-headers"></a>请求标题

| ​页眉         | Value                     |
|----------------|---------------------------|
| 授权  | 不记名 {token}（必需） |
| 内容类型   | application/json          |

### <a name="request-body"></a>请求正文

不要为此方法提供请求正文。

### <a name="response"></a>响应

成功的响应永远是 **204 无内容**响应。

未经授权的调用方将收到 **401 未授权**或 **403 已禁止**响应。

如果提交未成功（例如，由于验证），响应将为 **500 服务器错误**，响应正文将包括包含更多详细信息的 JSON 对象。

## <a name="example"></a>示例

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

## <a name="validation-and-error-messages"></a>验证和错误消息

作为对提交 API 的调用的一部分，Human Resources 在提交之前执行业务逻辑验证，以确保休假请求处于有效状态，可以提交。 如果验证失败，您可能会在响应中收到以下错误消息：

 - 此请求将使“{LeaveTypeId}”余额小于 {date} 所允许的最低余额。
 - 无法提交“已完成”状态的休息时间请求。
 - 未进行任何更改，无法提交或保存请求。 请添加或更新金额或休假类型，然后重试。
 - 输入的休息时间请求有一天或多天的日期和休假类型与现有的待处理请求相同。 请撤回现有请求，进行更改。
 - 原因代码“{ReasonCodeId}”不适用于请求中的任何休假类型。
 - 休假类型“{LeaveTypeId}”需要有原因代码。 请选择适当的类型和原因代码。
 - 休息时间未成功提交。 休息时间已另存为草稿请求。

## <a name="see-also"></a>请参阅

- [MyLeaveRequests 概览](hr-developer-api-myleaverequests-overview.md)
- [身份验证](hr-developer-api-authentication.md)