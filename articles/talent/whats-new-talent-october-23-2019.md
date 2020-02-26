---
title: Dynamics 365 Talent（2019 年 10 月 23 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68e3f428215bdc4f9a4ce0dd69cfd4482c72fbf3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006256"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Dynamics 365 Talent（2019 年 10 月 23 日）中的新增功能或更改

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2569。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Finance and Operations 应用平台更新 30

有关详细信息，请参阅 [Finance and Operations 应用的平台更新 30（2019 年 11 月）的新增功能或更改的功能](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30)。

### <a name="remove-benefits-open-enrollment-preview-feature"></a>删除福利开放登记预览功能

连同我们在[Core HR 的战略投资推动卓越运营](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)博客文章中宣布的消息，Microsoft 将在 2019 年 10 月 18 日的公开预览中删除福利开放登记功能。 将来会发布新功能。 当前处于公共预览的福利开放登记功能的生产使用将不受支持。

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>再次选择“工作人员”窗体上的国家/地区时出错 (350294)

在本周的发布中，在**工作人员**窗体上选择国家/地区时出现的问题已更正。

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>当“不允许手动输入”设置为 true 时，财务维度值默认为“组合显示”字段 (340097)

进行此更改后，当设置财务维度并使用不允许手动输入选项时，系统会将维度值默认为正确的**组合显示**字段。

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>新的关系类型应该添加到个人联系人窗体中的“关系”查找中 (347691)

此版本包含一些新功能，可以在**关系类型**表中添加新的关系类型，并在个人联系人的关系查找中反映这些更改。

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>自定义字段中的其他列表值未反映在 Common Data Service 中 (379599)

在本周的发布中，将新列表值添加到已经与 Common Data Service 同步的现有自定义字段中，新的领料单值现在将在对实体应用更改后出现。

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>在“雇用条款”页面上，选择“在 Excel 中打开”后，显示所有员工的雇用条款 (348073)

在此版本中，只有选定员工的雇用条款将在 Excel 中打开。 所有公司安全性也已实现。

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Common Data Service 中缺少“工作日历假期”实体和“工作日历”实体之间的关联 (324178)

此关系已在此版本中添加。 此更改将使员工的工作日显示在 PowerApps 中。 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>使用具有可配置层次结构的员工自助服务工作流时出错 (370132)

在此版本中，可以更好的传达如何配置使用可配置层次结构的工作流。 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>系统允许创建“可用于分配”日期早于“启用”日期的新位置 (340103)

当**可用于分配**日期在该位置的**启用**日期之前时，此更改将显示警告。

## <a name="coming-soon"></a>即将到期

### <a name="print-performance-reviews"></a>打印绩效复查

请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。

### <a name="feature-management-workspace"></a>“功能管理”工作区

每个版本中都会增加和更新功能。 功能管理体验提供一个工作区，可在其中查看各版本已交付的功能的列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。

要了解有关功能管理带来的更改的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。
