---
title: 创建团队日历
description: 在 Dynamics 365 Human Resources 中查看和创建团队日历。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0679a69b4d607f9d466474026d5dd0ceef0dad6f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692189"
---
# <a name="view-team-and-company-calendars"></a>查看团队和公司日历

>[!Important]
>本主题中提到的功能目前对独立 Dynamics 365 Human Resources 上的客户可用。 在 Finance 版本 10.0.26 之后，部分或全部功能将作为未来版本的一部分在 Finance 基础结构上提供。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 Dynamics 365 Human Resources 中查看团队和公司日历。 团队日历仅显示在行层次结构中定义的直接下属。

## <a name="view-your-team-calendar-as-an-employee"></a>以员工身份查看团队日历

- 在 **员工自助服务** 工作区，选择 **摘要** 下的 **团队缺勤日历**。

## <a name="view-your-team-calendar-as-a-manager"></a>以经理身份查看团队日历

1. 在 **员工自助服务** 工作区中，选择 **我的团队**。

2. 选择 **休假和缺勤**，然后选择 **查看经理缺勤日历**。

经理也可以从 **我的团队的待处理休息请求**、**批准的休息时间** 和 **休息时间请求** 访问团队日历。 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>以缺勤管理人员身份查看缺勤管理人员日历

> [!NOTE]
> 要查看缺勤管理人员日历，您必须先在功能管理中打开 **(预览)管理休假的缺勤管理人员** 功能。 有关如何打开预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

缺勤管理人员角色的用户可以在日历中查看休假请求。 按照以下步骤访问休假日历。

1. 在 **员工自助服务** 工作区中，选择 **休假管理**，然后选择 **缺勤管理人员日历**。

2. 在 **日期** 字段中，输入所需日期。

3. 根据需要更新视图选项。

缺勤管理人员日历显示在休假层次结构中向缺勤管理人员报告工作的员工的所有记录。

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

**休假和缺勤参数** 页面中的日历配置决定可用视图选项。

还可以按经理或部门筛选日历。 主要职位分配确定设置了这些筛选器时显示的员工。 

> [!IMPORTANT]
> 您可以在功能管理中打开 **跨公司休假视图** 功能。 然后，您必须在 **人力资源共享参数** 页启用该功能以在日历中显示法人筛选器。 有关详细信息，请参阅[配置休假和缺勤参数](hr-leave-and-absence-parameters.md)。
> 
> 您可以按法人筛选日历。 要查看所有员工，无论是哪个法人，先清除筛选器字段，然后选择 **Enter**。 

有关日历设置的信息，请参阅[配置日历参数](hr-leave-and-absence-parameters.md?configure-calendar-parameters)。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
