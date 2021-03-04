---
title: Dynamics 365 Human Resources（2020 年 3 月 10 日）中的新增功能或更改
description: 本文介绍 2020 年 3 月 10 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526898"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Dynamics 365 Human Resources（2020 年 3 月 10 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.2985。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="cant-access-skill-gap-analysis-report-394460"></a>不能访问技能差距分析报表 (394460)

Dynamics 365 Human Resources 中不支持此报表。 已删除了用于打印 SSRS 报表的菜单项。

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>访问“开始”页时显示不正确的消息 (417950)

进行此更改之后，如果您无权访问窗体，安全措施将隐藏此菜单项。

## <a name="streamlined-task-maintenance-for-employees-380538"></a>简化了员工的任务维护 (380538)

工作人员任务维护窗体列出了员工在入职、离职、转移和业务流程中的所有任务。 您可以删除，重新分配或更新任务状态。

示例：Benjamin Martin 是福利管理员。 员工入职期间，将创建任务以供 Benjamin 检查新员工选择的福利。 Benjamin 有自己已完成的过去任务和需要其完成的未来任务。 Benjamin 决定离开公司，因此需要重新分配或删除他的任务。 可通过（**工作人员** 窗体的操作窗格中的）任务维护窗体将 Benjamin 的所有任务重新分配给其他工作人员或将其删除。  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service 现已可用，并具有以下更改：

| 说明 | 找零 |
| --- | --- |
| **工作/职位** 实体更改 | <ul><li>添加了 **薪酬区域**</li>|
| 添加了 **工作职位维度** 实体 | <ul><li>添加了 **财务维度**</li>
| **工作人员** 实体更改 | <ul><li>添加了 **姓名顺序**</li><li>添加了 **在家工作**</li><li>添加了 **语言**</li><li>添加了 **受聘日期**</li><li>添加了 **周年纪念日日期**</li><li>添加了 **原始雇用日期**</li></ul> |
| **雇用** 实体更改 | <ul><li>添加了 **财务维度**</li><li>添加了 **离职原因**</li><li>**转变日期** 重命名为 **离职日期**</li><li>添加了 **试用日期**</li></ul> |
| **工作人员地址** 实体更改 | <ul><li>添加了 **街道地址**</li><li>**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用</li></ul> |
| 新的可变薪酬设置实体 | <ul><li>**可变薪酬计划类型**</li><li>**薪酬可变计划**</li><li>**股份行权规则**</li><li>**可变薪酬计划级别**</li></ul> |
| 新 **工作人员日历雇用** 实体 | <ul><li>添加了 **工作日历实体**</li></ul> |
| 新 **工资单职位详细信息** 实体 | <ul><li>添加了 **工资单职位详细信息**</li></ul> |
| 新 **职务** 实体 | <ul><li>添加了 **职务**</li></ul> 新的 **职务** 实体位于 Common Data Service 中，但是此时不是从 **工作职位** 或 **工作** 实体引用的。 |

> [!NOTE]
> 职位和雇用的财务维度为从 Human Resources 到 Common Data Service 的更新提供单向集成。 财务维度更新现在不从 Common Data Service 同步到 Human Resources。

在接下来的数周内，所有环境中将支持这些实体更改。 若要手动插入适用于 Human Resources 的最新 Common Data Service 解决方案：

1.  转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2.  选择 **环境**。

3.  找到要升级的环境。 此环境应该对应于 Human Resources 中 **关于** 窗体内 **Common Data Service 信息** 部分中的 **环境名称**。

4.  选择环境以查看环境详细信息。

5.  在顶部的操作栏中选择 **管理解决方案**。 将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。

6.  在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。

7.  选择 **升级** 应用最新解决方案。

## <a name="in-preview"></a>预览模式

以下预览功能于 2020 年 2 月 3 日可用：

- **休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

- **福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。

## <a name="coming-soon"></a>即将推出

### <a name="platform-update-33"></a>平台 update 33

- 整页应用（预览）- 此预览功能需要您启用“已保存的视图”功能，其允许将 Power Apps 和第三方应用通过仪表板作为整页体验添加。

- 已保存的视图（预览）- 此预览功能启用已保存的视图，这是对个性化子系统的显著增强。 此功能让用户每页可以有多组命名的个性化设置。 也可以将视图发布给安全角色。

- 经过优化的“之一”筛选体验 - 此功能启用了优化的“之一”筛选体验，可以更轻松地输入多个筛选器值，提供更简单的机制来删除单个或所有筛选器值，并可更紧凑直观地以可视化方式呈现筛选器值。

- “推荐”字段 - 用户通常需要向网格或页面添加字段。 因为可用字段太多，这可能很难。 此功能让系统基于其他用户在类似方案中最常添加的字段显示一组推荐字段，而不必在大型列表中进行搜索。

- 网格中的粘滞默认操作 - 此功能确保网格中的默认操作链接到网格中的特定列，而不管是否移动或隐藏了该列。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]