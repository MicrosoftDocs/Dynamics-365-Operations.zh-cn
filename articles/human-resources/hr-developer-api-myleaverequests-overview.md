---
title: MyLeaveRequests 概览
description: Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 724c4c91e38bb8ac9fe1fd0794dc5a79b2435472
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339731"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests 概览

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供系统中的休假请求列表，其范围（限制）为查询该实体的当前用户可以访问的请求。

## <a name="key"></a>键

  | 属性名称 | 数据类型 |
  |---------------|-----------|
  | dataAreaId    | 字符串    |
  | RequestId     | 字符串    |
  | LeaveType     | 字符串    |
  | LeaveDate     | 日期      |
  
## <a name="properties"></a>属性

  | 属性名称     | 数据类型 | 必需 |
  |-------------------|-----------|----------|
  | dataAreaId        | 字符串    | X        |
  | RequestId         | 字符串    | X        |
  | LeaveType         | 字符串    | X        |
  | LeaveDate         | 日期      | X        |
  | ReasonCodeId      | 字符串    |          |
  | PersonnelNumber   | 字符串    | X        |
  | RequestDate       | 日期      | X        |
  | 注释           | 字符串    |          |
  | 状态            | 枚举      | X        |
  | 时长            | 实数      |          |
  | HalfDayDefinition | 枚举      |          |

## <a name="actions"></a>行为

 | 操作名称                               | 说明                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [submit](hr-developer-api-myleaverequests-submit.md)   | 提交要由工作流处理的请求。 |

## <a name="see-also"></a>请参阅

- [将请假申请提交至工作流](hr-developer-api-myleaverequests-submit.md)
- [身份验证](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]