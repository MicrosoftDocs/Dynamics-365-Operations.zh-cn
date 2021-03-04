---
title: Dynamics 365 Talent - Core HR（2018 年 9 月 10 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460487"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a>Dynamics 365 Talent - Core HR（2018 年 9 月 10 日）中的新增功能或更改

**内部版本 8.1.138.0**

此主题介绍了 Microsoft Dynamics 365 Talent: Core HR 中的新增功能和更改的功能。

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>允许请特定时间段的假（半天）

如果将休假和缺勤设置为以天为单位提交请假，也可以启用半天定义。 然后，当用户提交请假时，可以指定请上半天还是下半天假。

默认情况下，此选项已关闭。 必须在人力资源参数的 **休假和缺勤** 区域中文为要请半天假的员工开启此选项。

此功能的安全权限为“维护人力资源参数”。

## <a name="validation-of-leave-and-absence-entries"></a>验证休假和缺勤条目

根据休假的配置方式，尝试请假时间超过工作日的员工会收到警告消息。 换言之，如果在给定日期请求时间超过一整天，就会予以警告。

此验证始终开启。 只要员工超过了定义的天数阈值，都会在请假时收到警告。

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>工作流中的条件语句的更多字段

已向 Core HR 中的若干工作流的条件语句和占位符添加了更多字段。

已向补偿、离职和转岗工作流添加了以下字段：

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- 位置
- 工会
- 部门
- PositionType
- CompLocation
- 职位
- 工作
- JobType
- JobFamily
- JobFunction

已向职位工作流添加了以下字段：

- 位置
- 工会
- 部门
- PositionType
- CompLocation
- 职位
- 工作
- JobType
- JobFamily
- JobFunction

条件语句和占位符可用于有权配置上面介绍的工作流的所有用户。

## <a name="navigation-to-attract-from-personnel-management"></a>从人员管理导航到 Attract

在人员管理中，如果尚未设置 Attract，**可雇用的应聘者** 部分将指示用户从 Attract 开始，而不是显示消息“我们未找到要在此处显示的任何内容。”

## <a name="other-changes"></a>其他更改

此版本中还包含若干缺陷修复：

- 雇用合同工时，请求/操作页面中的 **补偿** 选项卡应不可用。
- 请求终止过程中，所有必填字段均包含数据之前，不能继续操作。
- 已解决了人员管理分析中的排序和日期显示问题。


[!INCLUDE[footer-include](../includes/footer-banner.md)]