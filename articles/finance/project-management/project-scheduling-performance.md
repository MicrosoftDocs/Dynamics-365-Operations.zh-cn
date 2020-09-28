---
title: 项目资源计划性能
description: 此主题介绍如何提高大量项目的资源计划性能。
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760489"
---
# <a name="project-resource-scheduling-performance"></a>项目资源计划性能

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


当项目数量上千时，可能发生与资源计划有关的性能问题。 为了提高资源计划性能，提供了一项功能，供用户减少启动资源可用性窗体所用时间。 特别是，其去除了资源产能汇总同步流程，而是使用 **ResProjectResource** 表加快资源查找速度。 请注意，将不再使用 **ResRollup** 表。

> [!IMPORTANT]
> 如果需要依赖资源产能汇总同步流程或 **ResProjectResource** 表，请勿使用此功能。

## <a name="enable-resource-scheduling-performance-enhancement"></a>启用资源计划性能增强
若要启用资源计划性能增强，请完成以下步骤。

1. 转到**功能管理** > **所有**，然后在功能列表中找到**启用项目资源计划性能增强功能**。
2. 选择**立即启用**。

> [!NOTE]
> 如果在此列表中找不到该功能，请选择**检查更新**刷新列表。

3. 刷新浏览器，然后转到**项目管理与核算** > **定期** > **项目资源** > **同步所有公司的资源日历产能**。
4. 将**删除现有产能记录**设置为**是**以删除之前的数据。 如果要生成增量数据，请将其设置为**否**。
5. 在**期间代码**字段中，选择应生成数据的期间。 如果选择期间代码，则无需定义开始日期和结束日期。
6. 如果让**期间代码**字段保留为空，请选择特定的开始日期和结束日期以生成数据。
7. 选择**确定**。

 > [!NOTE]
 > 这将在您的环境中所有公司内把常规数据分发给 **ResCalendarCapacity** 表，以便只需在一个法人中运行批处理作业。 需要此批处理作业中的数据，才能通过关联的日历计算资源产能。

8. 转到**项目管理与核算** > **定期** > **项目资源** > **填充所有公司的项目资源**，然后选择**确定**。 这是 **ResProjectResource**、**ResCalendarDateTimeRange** 和 **ResEffectiveDateTimeRange** 表中常规数据的数据更新脚本。 还将更新 **PSAPRojSchedRole.RootActivity** 字段的值。 如果不运行，在尝试执行资源计划操作时，将收到警告。
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>关闭资源计划性能增强

1. 转到**功能管理** > **所有**，然后搜索**启用项目资源计划性能增强功能**。
2. 选择功能，然后选择**禁用**按钮。
3. 刷新浏览器。
4. 转到**目管理与核算** > **定期** > **产能同步** > **同步资源产能汇总**。
5. 在**产能汇总同步**页面中，将**删除现有产能记录**设置为**是**以删除之前的数据。 如果要生成增量数据，请将其设置为**否**。
6. 在**期间代码**字段中，选择应生成数据的期间。 如果选择期间代码，则无需定义开始日期和结束日期。
7. 如果让**期间代码**字段保留为空，请选择特定的开始日期和结束日期以生成数据。
8. 选择**确定**。

> [!NOTE]
> 这将在您的环境中所有公司内把常规数据分发给 **ResRollup** 表，以便只需在一个法人中运行批处理作业。 所有**资源可用性**视图都需要此批处理作业。 如果未运行此批处理作业，将即时生成 **ResRollup** 数据，这可能需要一些时间。
