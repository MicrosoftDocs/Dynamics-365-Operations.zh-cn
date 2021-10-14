---
title: 福利管理工作区
description: 本主题将介绍 Dynamics 365 Human Resources 中的福利管理工作区。
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6cc1432e108c74706dea124a62024272e65b6c1
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512465"
---
# <a name="benefits-management-workspace"></a>福利管理工作区

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

本主题将介绍 Dynamics 365 Human Resources 中的 **福利管理** 工作区。

> [!NOTE]
> 要查看 **福利管理** 工作区，必须首先在“功能管理”中启用 **(预览)福利管理工作区** 功能。 有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。<br><br>![启用福利管理工作区。](./media/hr-benefits-management-workspace-enable.png)

**福利管理** 工作区为您提供需要您注意的福利项目的快速视图。 在此页上，您可以看到：

- 等待操作的项目的总计
- 有未确认选择的工作人员
- 最近在福利中登记的工作人员
- 有将来生活事件的工作人员
- 未登记的新雇员
- 有活动生活事件的工作人员
- 有打开的登记但未选择任何计划的工作人员

![福利管理工作区。](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>查看操作项

您可以通过选择磁贴或选项卡来查看操作项。如果选择选项卡，您可以从工作区页面查看和选择工作人员。

![操作项。](./media/hr-benefits-management-workspace-action-items.png)

如果选择磁贴，转到该区域的页面。 例如，选择这些磁贴中的任意一个将显示 **工作人员福利计划** 页，该页面已针对您需要执行操作的员工进行了筛选：

- **未确认的选择**
- **打开没有已签出计划的许可登记表**
- **登记的福利**
- **新雇员未登记**

![工作人员福利计划。](./media/hr-benefits-management-workspace-plans.png)

选择 **活动生活事件** 或 **将来生活事件** 会将您带到活动或将来生活事件的列表。

![生命事件。](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>正在处理

要处理登记资格、生活事件或比率更改更新，请在导航栏上选择适当的项目。

![处理中。](./media/hr-benefits-management-workspace-processing.png)

要查看处理结果，在页面上选择 **处理结果**。

![流程结果。](./media/hr-benefits-management-workspace-process-results.png)

有关福利处理的详细信息，请参阅：

- [处理登记资格](hr-benefits-process-enrollment-eligibility.md)
- [处理生活事件更改](hr-benefits-process-life-event-changes.md)
- [处理生活事件资格](hr-benefits-process-life-event-eligibility.md)
- [处理生活事件](hr-benefits-process-life-events.md)
- [处理费率更改](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>更改期间

要查看不同的福利期间，从 **期间** 下拉列表中选择期间。

![更改期间。](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>“开放登记”选项卡

您可以通过选择磁贴或选项卡来查看操作项。如果选择选项卡，您可以在工作区页面上查看和选择工作人员。
**开放登记** 选项卡会为开放登记流程提供关键指标。 

将在 **登记开始日期** 之前 30 天显示有关开放登记的信息。 **福利管理** > **链接** > **期间** 中 **期间** 设置内的 **登记开始日期** 字段中定义了此日期。  若要更改此设置，请转到 **人力资源共享参数** > **福利管理** > **开放登记选项**，并更新 **相关数目** 字段。  

**开放登记** 选项卡上会提供以下信息：
 - 尚未启动开放登记流程的员工
 - 正在进行选举的员工
 - 已完成选举程序的员工
 - 未确认的选择

**汇总磁贴**

- **未启动** - **未启动** 磁贴显示尚未启动登记流程的员工计数。 **未启动** 磁贴是一个筛选列表，它仅显示在开放登记计划期间未选择、放弃或查看任何计划的员工。 强制计划被忽略，并且不包括在内，因为默认情况下为员工选择了这些计划。  您可以在此磁贴上向后钻取，以在 **工作人员福利计划** 页面上查看尚未启动公开登记流程的员工列表。

  > [!NOTE]
  > 如果您不想跟踪 **计划类型** 的公开登记进度，则可以转到 **福利管理** > **链接** > **员工自助服务参数** > **福利计划磁贴设置**，并更新 **跟踪公开登记进度** 字段，从而将其排除。  例如，您可能已创建了 **计划类型** = **其他** 的计划。 这些计划可能是您不希望跟踪其登记进度的可选计划。 如果未选择此计划类型，则在 **公开登记** 选项卡上跟踪登记进度或完成时，将忽略这些类型的计划。此设置适用于为所有期间和法人选择的计划类型。

- **进行中** - **进行中** 磁贴提供了正在进行选举的员工计数。 **进行中** 磁贴是一个筛选列表，该列表仅显示至少具有一个放弃或选择的计划的员工。 强制计划被忽略，并且不包括在内，因为默认情况下为员工选择了这些计划。 您可以从此磁贴中向后钻取，以在 **工作人员福利计划批量更新** 页上查看所选择和放弃的计划。

- **已登记福利** - **已登记福利** 磁贴提供了完全登记福利的员工人数。 **已登记福利** 磁贴是一个筛选列表，显示了已选择或放弃所有计划的员工。 查询将排除在 **员工自助服务参数** 页面上未跟踪的开放登记计划。 您可以从此磁贴中向后钻取，以查看 **工作人员福利计划** 页面上的员工列表。

- **未确认的选择** - **未确认的选择** 磁贴显示已选择或放弃计划且需要确认这些计划的员工计数。 您可以从此磁贴中向后钻取，以显示 **工作人员福利计划批量更新** 页面。

**活动**

- **未启动** - **未启动** 选项卡显示尚未启动登记流程的员工列表。 **未启动** 磁贴是一个筛选列表，它显示在开放登记计划期间未选择、放弃或查看任何计划的员工。 强制计划被忽略，并且不包括在内，因为默认情况下为员工选择了这些计划。 您可以深入了解工作人员以显示 **工作人员福利计划详细信息** 页。

- **正在进行选举** - **正在进行选举** 选项卡提供了正在进行选举的员工列表。 **正在进行选举** 是一个筛选列表，该列表显示至少具有一个放弃或选择的计划的员工。 强制计划被忽略，并且不包括在内，因为默认情况下为员工选择了这些计划。 您可以深入了解工作人员以显示 **工作人员福利计划详细信息** 页。

## <a name="view-more-options"></a>查看更多选项

要查看更多信息以及/或者其他操作，请选择 **链接**。

![链接。](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>请参阅

[福利管理概览](hr-benefits-management-overview.md)
