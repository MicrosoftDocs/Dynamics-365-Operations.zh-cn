---
title: Dynamics 365 Human Resources（2020 年 3 月 24 日）中的新增功能或更改
description: 本文介绍 2020 年 3 月 24 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 03/24/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 22c5e83a7f180a340e98b81a197daa95d3569cc3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463686"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Dynamics 365 Human Resources（2020 年 3 月 24 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.3073。 某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Human Resources 环境限制现在基于更新的许可 (394595)

Lifecycle Services (LCS) 中每个项目的环境数量限制已更改。 先前的限制是两个环境。 现在，您可以在 LCS 中为 Human Resources 创建的生产环境和沙盒环境的数量限制基于更新的许可。 现在，您可以根据购买的许可证数量，为每个 LCS 项目创建所需数量的环境。 2020 年 2 月 1 日更新的新许可允许客户购买其他环境。 有关其他环境的许可要求的详细信息，请参阅 [Dynamics 365 许可指南](https://dynamics.microsoft.com/pricing/#HumanResources)。

## <a name="platform-changes"></a>平台变更

- 整页应用（预览）- 此预览功能需要您启用“已保存的视图”功能，其允许将 Power Apps 和第三方应用通过仪表板作为整页体验添加。

- 已保存的视图（预览）- 此预览功能启用已保存的视图，这将为个性化子系统提供显著的增强。 此功能让用户每页可以有多组命名的个性化设置。 也可以将视图发布给安全角色。

- 经过优化的“之一”筛选体验 - 此功能启用了优化的“之一”筛选体验，可以更轻松地输入多个筛选器值，提供更简单的机制来删除单个或所有筛选器值，并可更紧凑直观地以可视化方式呈现筛选器值。

- “推荐”字段 - 用户通常需要向网格或页面添加字段。 因为可用字段太多，这可能很难。 此功能让系统基于其他用户在类似方案中最常添加的字段显示一组推荐字段，而不必在大型列表中进行搜索。

- 网格中的粘滞默认操作 - 此功能确保网格中的默认操作链接到网格中的特定列，而不管是否移动或隐藏了该列。

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>无法为创建的没有应计但已启用“多个休假类型”功能的计划调整休假余额 (419635)

通过此更改，您可以为创建的已在功能管理中启用了多个休假类型（预览功能）的休假计划调整余额。

## <a name="in-preview"></a>预览模式

以下预览功能已于 2020 年 2 月 3 日可用：

- **休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

- **福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse 现已可用，并具有以下更改：

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
| 新 **职务** 实体 | <ul><li>添加了 **职务**</li></ul>新的 **职务** 实体位于 Dataverse 中，但是此时不是从 **工作职位** 或 **工作** 实体引用的。 |

> [!NOTE]
> 职位和雇用的财务维度为从 Human Resources 到 Dataverse 的更新提供单向集成。 财务维度更新现在不从 Dataverse 同步到 Human Resources。

在接下来的数周内，所有环境中将支持这些实体更改。 若要手动插入适用于 Human Resources 的最新 Dataverse 解决方案：

1.  转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2.  选择 **环境**。

3.  找到要升级的环境。 此环境应该对应于 Human Resources 中 **关于** 窗体内 **Common Data Service 信息** 部分中的 **环境名称**。

4.  选择环境以查看环境详细信息。

5.  在顶部的操作栏中选择 **管理解决方案**。 将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。

6.  在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。

7.  选择 **升级** 应用最新解决方案。

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint 预览在某些环境下不起作用

如果 SharePoint 中存储的文档的文档预览不起作用，请尝试以下过程：

1. 验证管理员用户帐户是否具有与用户记录关联的电子邮件。 可在 **用户** 页面查看这些信息。 如果未设置电子邮件，则需要使用 OData Excel 加载项添加电子邮件和提供程序。 默认情况下，Excel 设计中不显示电子邮件地址。 您需要编辑 Excel 设计，添加所有字段，然后应用并刷新。 完成这些步骤后，您可以更新管理员帐户。

2. 管理员帐户具有关联的电子邮件帐户后，使用管理员凭据登录到 Human Resources。

3. 访问 SharePoint 中的附件启动文档预览。

4. 使用有权访问附件的另一个用户帐户登录，然后验证预览是否按预期工作。

## <a name="coming-soon"></a>即将推出

## <a name="new-production-release-cadence"></a>新产品发布频率

从 4 月开始，Human Resources 的发布频率将从每周更新变为每两周更新。 为了确保符合安全部署实践，并在服务中保持高标准的稳定性和可靠性，将为期两周把服务更新部署到所有区域。 将部署更多测试和监视人员，以验证流程各个阶段是否成功部署。 有关发布频率的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

## <a name="known-issues"></a>已知问题

## <a name="employment-detail-entity"></a>雇用详细信息实体

已经更新了 **雇用详细信息** 实体的以下字段：**付款频率**、**雇用类别 ID**、**雇用类型**、**雇用类型ID** 和 **福利雇用状态**。 这些字段的设置数据依赖于功能管理中启用的福利管理。 不应在 **雇用详细信息** 实体中填充或更新这些字段，因为将导致导入期间出错。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]