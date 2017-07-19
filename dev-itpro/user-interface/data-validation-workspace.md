---
title: "数据验证工作区"
description: "数据验证核对清单工作区可以跟踪跨公司、区域和人员的数据验证流程。 核对清单可以在新实现期间、升级后或迁移后使用。"
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e105c4b171979a03c20718c1fa9d558c921cd704
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017

---

# <a name="data-validation-workspace"></a>数据验证工作区

[!include[banner](../includes/banner.md)]


此主题提供**数据验证核对清单工作区**和相关配置的概览。

## <a name="data-validation-checklist-workspace"></a>数据验证核对清单工作区

**数据验证核对清单**工作区可以跟踪跨公司、区域和人员的数据验证流程。 核对清单可以在新实现期间、升级后或迁移后使用。 根据**数据验证核对清单**工作区的视图，您将看到数据验证项目的所有任务和状态，或仅分配给您的任务。

首先必须在该工作区顶部选择一个数据验证项目。 然后按所选数据验证项目筛选该工作区中显示的所有数据。

### <a name="summary-tiles"></a>汇总磁贴

**汇总**磁贴为您提供流程概览以及帮助您跟踪数据验证流程的指示器。 您可以查看该流程的所有剩余任务、已完成任务、正在进行的任务和尚未开始的任务。 此信息针对包含在所选数据验证项目内的所有公司。

### <a name="tasks-and-status-section"></a>任务和状态部分

在**任务和状态**部分，总体数据验证项目的状态以不同的方式显示：按法人、区域和任务列表显示的状态。 您可以选择筛选器以查看特定公司的状态。 每个状态选项卡同时按已完成百分比和剩余任务数量提供细分。

最后一个卡针对详细任务列表。 此列表显示完整的任务列表。
可以通过多种方式筛选任务列表。 单击**编辑任务**更改任务的状态或分配任务。 单击**附件**查看任务的附件。

任务名称是链接至 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 页面的超链接，用户必须进入该页面完成工作。 您可以在从**配置数据验证项目**窗体编辑或创建任务时使用**菜单项名称**字段设置此超链接。

可通过使用**附件**操作将文件、注释、图像和 URL 附加到任务。 例如，您可以附加为任务打印的报表文件。 如果有附件，任务的**附件**列中将显示一个图标。

任务完成后，将使用完成该任务的工作人员的名称自动填充**完成人**选项。 任务标记为已完成时，**完成日期**字段将自动更新为当前日期和时间。

### <a name="configure-data-validation-project-page"></a>配置数据验证项目页

在您可以使用**数据验证核对清单**工作区之前，必须使用**配置数据验证项目**页配置流程。 （单击**工作区** \> **数据验证核对清单** \> **配置数据验证项目**。）

### <a name="task-areas"></a>任务区域

您使用任务区域将数据验证任务分组到您的组织中的逻辑所有权区域。 例如，应付帐款、应收帐款或总帐可以使用为任务区域。

**菜单项名称**与任务工作关联，可用于从工作区中的任务链接直接访问关联页面。 例如，要为应付帐款运行**应付帐款帐龄**报表的数据验证任务可以链接到**应付帐款帐龄报表**页。

