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
# <a name="myleaverequests-overview"></a>MyLeaveRequests 概览

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