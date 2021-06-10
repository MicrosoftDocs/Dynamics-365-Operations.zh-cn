---
title: Dynamics 365 Human Resources（2020 年 2 月 25 日）中的新增功能或更改
description: 本文介绍 2020 年 2 月 25 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d9ff9b524a5812bd309fc33d6aa4ba4a92d687b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051177"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Dynamics 365 Human Resources（2020 年 2 月 25 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.2927。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>启用案例管理导航和数据管理框架 (DMF) 实体 (414754)

此预览功能为案例管理情况增加了导航方式。 可以在 **功能管理** 工作区中启用此预览功能。 这些菜单项在 Dynamics 365 Human Resources 的 **合规性** 工作区中显示。 通过此更改，Human Resources 可以访问：

- 所有案例
- 我的案例
- 我的未结案例
- 我的逾期案例
- 通过工作流分配给我的案例

除了案例的这些新视图，还提供了 **案例详细信息** DMF 实体。

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>在全球通讯簿中启用关系定义 (414762)

全球通讯簿中现在已启用关系。 本周的发布之前，**关系** 速见表显示系统定义的所有关系。 现在您可以在全球通讯簿页面内定义这些关系。

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>职位有活动的薪酬记录时可以删除职位 (414568)

通过此更改，当您尝试删除职位，而一位工作人员有同一个职位的活动薪酬记录时，将显示警告。 如果发生此情况，必须先更新员工的固定薪酬记录，才能删除该职位。

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>绩效审核工作流有时会添加不属于该流程的人员的签核 (414171)

此更改解决了向绩效审核添加更多签核参与者这一问题。

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>在“新建工作人员”对话框中选择后不在 Dataverse 中创建工作人员职位分配 (413479)

此更改解决了通过 **新建工作人员** 对话框雇用新工作人员并为新雇用分配职位时的问题。 现在 Dataverse 中将体现此项职位分配。

## <a name="coming-soon"></a>即将到期

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

在接下来的数周内，所有环境中将支持这些实体更改。 若要手动插入适用于 Human Resources 的最新 Dataverse 解决方案：

1.  转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2.  选择 **环境**。

3.  找到要升级的环境。 这应该对应于 Human Resources 中 **关于** 窗体内 **Common Data Service 信息** 部分中的 **环境名称**。

4.  选择环境以查看环境详细信息。

5.  在顶部的操作栏中选择 **管理解决方案**。 将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。

6.  在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。

7.  选择 **升级** 应用最新解决方案。

## <a name="in-preview"></a>预览模式

以下预览功能已于 2020 年 2 月 3 日可用：

- **休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

- **福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]