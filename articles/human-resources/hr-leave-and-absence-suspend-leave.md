---
title: 暂停休假
description: 可以在 Dynamics 365 Human Resources 中暂停员工的休假。
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805252"
---
# <a name="suspend-leave"></a>暂停休假

>[!Important]
>本文中提到的功能目前对独立 Dynamics 365 Human Resources 上的客户可用。 在 Finance 版本 10.0.26 之后，部分或全部功能将作为未来版本的一部分在 Finance 基础结构上提供。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

可以暂停员工的休假，以便停止处理所选休假类型的休假应计。

## <a name="suspend-leave-and-absence-for-an-employee"></a>暂停员工的休假和缺勤

1. 在员工的记录上，选择 **休假**。

2. 选择 **暂停休假**。

3. 选择 **新建**。

4. 在 **暂停休假假期额度记录** 对话框中，选择暂停的 **休假类型** 和 **开始日期** 与 **结束日期**。

5. （可选）也可以为暂停添加 **注释**。 

如果在已暂停员工的休假时处理应计项目，则不会为暂停该团队休假类型执行累积。

> [!NOTE]
> 休假申请将暂停休息时间申请，但休息时间申请不会暂停休假申请。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)
- [配置休假和缺勤类型](hr-leave-and-absence-types.md)
- [累积休假和缺勤计划](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
