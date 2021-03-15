---
title: Dynamics 365 Human Resources（2020 年 2 月 18 日）中的新增功能或更改
description: 本文介绍 2020 年 2 月 18 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e087095807f587536f2dad7e65fbc8beaa88878e
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128057"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Dynamics 365 Human Resources（2020 年 2 月 18 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.2903。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="platform-update-32"></a>平台 update 32 

现已推出了平台更新 32。 有关详细信息，请参阅 [Finance and Operations 应用的平台更新 32（2020 年 2 月）的新增功能或更改的功能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)。

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>更改简化的员工窗体中的查看选项时记忆搜索值 (383833)

现在更改查看选项和应用更改时，新的 **工作人员** 窗体将记忆搜索值。

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>预览功能中的薪酬管理摘要磁贴重定向到错误的窗体 (401861)

固定和可变薪酬管理磁贴现在在新的 **工作人员** 窗体中显示正确的记录。 仅适用于简化的员工窗体预览功能。 可以在 **功能管理** 中启用此预览功能。 有关更多信息，请参阅[管理功能](hr-admin-manage-features.md)。

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Dataverse 中某些请假记录的“状态”字段为空 (414915)

此更改更正了 Dataverse中当请假的 **状态** 字段设置为 **审查** 时的问题。 Dataverse 现在可以体现此状态。

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>只能跳过所分配作业的差距分析 (411390)

现在可以对 Human Resources 中定义的任何作业执行技能差距分析。

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>在新环境中，系统币种不能从 Dataverse 同步到 Human Resources (418011)

Dataverse 中的系统币种现在可以同步到 Human Resources。

## <a name="in-preview"></a>预览模式

- [休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [福利管理预览功能](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>即将推出

### <a name="updated-dataverse-solution"></a>更新的 Dataverse 解决方案

一个新的 Dataverse 解决方案很快将推出，其中包含以下更改：

| 说明 | 找零 |
| ----------------------------------------- | --- |
| **工作/职位** 实体更改 | 添加了 **薪酬区域**</br>添加了 **财务维度** |
| **工作人员** 实体更改 | 添加了 **姓名顺序**</br>添加了 **在家工作**</br>添加了 **语言**</br>添加了 **受聘日期**</br>添加了 **周年纪念日日期**</br>添加了 **原始雇用日期** |
| **雇用** 实体更改 | 添加了 **财务维度**</br>添加了 **离职原因**</br>**转变日期** 重命名为 **离职日期**</br>添加了 **试用日期** |
| **工作人员地址** 实体更改 | 添加了 **街道地址**</br>**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用 |
| 新的可变薪酬设置实体 | **可变薪酬计划类型**</br>**薪酬可变计划**</br>**股份行权规则**</br>**可变薪酬计划级别** |
| 新 **工作人员日历雇用** 实体 | 添加了 **工作日历实体** |
| 新 **工资单职位详细信息** 实体 | 添加了 **工资单职位详细信息** |
| 新 **职务** 实体 | 添加了 **职务**。 Human Resources 与 Dataverse 之间的同步流程中将包含新的 **职务** 实体。 其最初不是从 **工作职位** 或 **工作** 实体引用的。 |

## <a name="see-also"></a>请参阅

[Human Resources 新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]