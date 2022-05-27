---
title: MyLeaveRequests 概览
description: Microsoft Dynamics 365 Human Resources 中的 MyLeaveRequests 实体提供休假请求的列表。
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717046"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests 概览


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
