---
title: 创建团队日历
description: 在 Dynamics 365 Human Resources 中查看和创建团队日历。
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ca7ccb7959eab6f8a9bdc0292e28c3126cb0364c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466440"
---
# <a name="view-team-and-company-calendars"></a>查看团队和公司日历

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 Dynamics 365 Human Resources 中查看团队和公司日历。 团队日历仅显示在行层次结构中定义的直接下属。

## <a name="view-your-team-calendar-as-an-employee"></a>以员工身份查看团队日历

1. 在 **员工自助服务** 工作区，选择 **摘要** 下的 **团队缺勤日历**。

## <a name="view-your-team-calendar-as-a-manager"></a>以经理身份查看团队日历

1. 在 **员工自助服务** 工作区中，选择 **我的团队**。

2. 选择 **休假和缺勤**，然后选择 **查看经理缺勤日历**。

经理也可以从 **我的团队的待处理休息请求**、**批准的休息时间** 和 **休息时间请求** 访问团队日历。 

## <a name="view-a-company-calendar"></a>查看公司日历

具有人力资源角色的人员可以查看公司日历。 公司日历显示所有员工。 默认情况下，日历显示今天的日期加上 28 天，但您可以更改日期范围。 您还可以按 **姓名**、**人员编号** 和 **休假类型** 筛选日历。

1. 在 **休假和缺勤** 工作区中，选择 **链接**。

2. 选择 **休假和缺勤日历**。

人力资源角色也可以从 **休假和缺勤请求**、**批准的休息时间** 和 **休息时间请求** 访问公司日历。 

日历现在包含更多筛选器和选项。 所有日历都包含以下对象的视图选项：

- 审核的请求
- 待定请求
- 已请假的员工
- 无请假的员工
- 员工生日
- 休假请求 
- 休假申请

“休假和缺勤”参数中的日历配置决定可用视图选项。

还可以按经理或部门筛选日历。 主要职位分配确定设置了这些筛选器时显示的员工。 

>[!IMPORTANT]
>跨公司查看休假和缺勤当前处于预览状态。 您需要在 **沙盒** 环境中启用它。 有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。<br><br>
>然后，您必须在 **Human Resources 共享参数** 中启用该功能以在日历中显示法人筛选器。 有关详细信息，请参阅[配置休假和缺勤参数](hr-leave-and-absence-parameters.md)。<br><br>
>您可以按法人筛选日历。 如果要查看所有员工，不论其法人如何，请清除筛选器框并选择 Enter 键。 

有关日历设置的信息，请参阅[配置日历参数](hr-leave-and-absence-parameters.md?configure-calendar-parameters)。



[!INCLUDE[footer-include](../includes/footer-banner.md)]