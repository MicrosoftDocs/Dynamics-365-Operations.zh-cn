---
title: "管理仓库工作人员"
description: "本文介绍如何使用 Dynamics 365 for Finance and Operations 帮助监控由您仓库的员工执行的工作。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b91c139987473be65fddf8b05759a5ad6f6c223
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="manage-warehouse-workers"></a>管理仓库工作人员

[!include[banner](../includes/banner.md)]


本文介绍如何使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 帮助监控由您仓库的员工执行的工作。

如果在仓库管理中使用此功能，所有仓库工作人员的操作称作*工作*。 领料、移动和盘点现有库存量等工作使用移动设备记录。 在仓库工作人员可以执行工作之前，他或她必须与人力资源的工作人员关联。 每个**工作人员**帐户可以有多个仓库工作用户与它关联。 这些工作用户可以在不同的仓库工作，并且可具有不同级别的各个移动设备菜单的访问权限。 您可以将仓库工作用户视作所选工作人员的多重登录。 每个工作用户具有默认仓库，并且特定工作流由可用于该工作用户的菜单项显示。 

若要创建新的工作用户，在**工作人员**页面，在**常规**选项卡上，在**仓库**部分单击**工作人员**。 您必须指定用户 ID、用户名、默认仓库和菜单名。 此菜单在该用户登录到仓库移动设备门户时加载，让您定义用户有权访问的菜单项。 

作为每个工作用户设置的一部分，您还可以定义特定流程的工作流。 例如，可以使用**为周期盘点主管**字段指定用户是否可以在盘点操作中处理对周期盘点差异的调整，或者这些调整是否必须由另一个人首先审查。

## <a name="defining-labor-standards"></a>定义人工标准
**人工标准**页让您可以定义系统用于计算特定类型的工作应需要的估计时间的计算方法。 此定义可以在一般级别或特定级别设置。 例如，您可以定义在使用特定领料流程时，按特定单位定义的重量处理销售订单领料应需要的时间。 同时，您可以基于其他计算方法记录已领料的现有库存量的放置操作的时间。 

若要启用您定义的人工标准，则您必须为使用人工标准的每个仓库选择**允许人工标准**选项。

## <a name="monitoring-and-controlling-warehouse-work"></a>监控仓库工作
**所有工作**页让您可以监控和维护计划、进行中和已完成的所有工作。 在此页上，您可以更新不同的流程，如仓库工作用户分配和工作优先级。 您还可以深化到与工作标题和工作行相关的详细信息，以取得对预期或完成的工作流程的了解。 

如果您启用**人工标准**选项，您可以看到该工作的计算出的估计时间。 然后，在处理该工作时，每个工作工序的实际时间也将显示。 这样，您可以将估计时间计算与实际时间比较。 

此外，您可以在规则中使用估计时间来在创建工作时自动拆分工作。 这样，您可以基于完成任务的预期时间进行负载平衡工作。 

用于处理工作项目的时间的分析有助于推动改善仓库工作人员的效率。 以下报表可用于帮助您完成这一分析：

-   **按用户划分的人工** – 此报表基于对照预期时间的实际时间显示工作人员的工作效率。
-   **按工作交易记录类型划分的人工** – 您可以使用此报表调查特定仓库流程的效率低下。 例如，您注意到转移单的领料在本周需要的时间比前一周更长。 那么，您可以使用此信息进行进一步调查。





