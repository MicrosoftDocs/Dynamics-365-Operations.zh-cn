---
title: 可视化和协作执行
description: 本文介绍如何监控需求驱动型材料要求计划 (DDMRP) 分离点、缓冲区、计划订单和历史记录。
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740815"
---
# <a name="visual-and-collaborative-execution"></a>可视化和协作执行

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

本文介绍如何监控需求驱动型材料要求计划 (DDMRP) 分离点、缓冲区、计划订单和历史记录。

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>目视跟踪所选物料的缓冲区和数量

在 Microsoft Dynamics 365 Supply Chain Management 中，您可以目视跟踪任何所选已发布产品的缓冲区、现有数量和净流级别如何随时间发生变化。 按照以下步骤打开和查看图表。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择设置为分离点的已发布物料。 （有关详细信息，请参阅[库存定位](ddmrp-inventory-positioning.md)。）
1. 在操作窗格上，在 **计划** 选项卡上，选择 **物料覆盖范围**。
1. 在 **物料覆盖范围** 页面上，选择创建分离点的物料覆盖范围记录。 （此记录将显示为创建分离点而设置的覆盖范围组的名称。）
1. 选择 **现有量** 选项卡。此选项卡包含一个图表，其中显示了随时间变化的现有数量，以及每次运行主计划时针对特定期间记录的现有量水平值。 该选项卡还包括一个表，此表显示每个记录的现有量水平属于以下哪个类别：

    - **极低** - 小于该期间最小值的一半。
    - **低** - 介于最小值和最小值的一半之间。
    - **平均现有量** - 介于最小值和最小值加绿色区域之间。
    - **高于平均值** - 高于平均值。

    ![“现有量”选项卡上的历史现有量水平。](media/ddmrp-on-hand-graph.png "“现有量”选项卡上的历史现有量水平")

    > [!NOTE]
    > **现有量** 选项卡上使用的颜色所表示的范围不同于 **缓冲区值** 选项卡上使用的相似颜色所表示的范围。

1. 若要查看缓冲区值随时间变化情况，以及它们与现有量和净流水平的比较情况，请选择 **缓冲区值** 选项卡。

    ![“缓冲区值”选项卡上的历史现有量和净流水平。](media/ddmrp-buffer-values-graph.png "“缓冲区值”选项卡上的历史现有量和净流水平")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>跟踪所有分离点的状态和计划订单

**需求驱动型 MRP** 工作区提供了多种工具，以及关键绩效指标 (KPI) 和分离点物料及相关计划订单的状态概览。 若要打开它，请转到 **主计划 \> 工作区 \> 需求驱动型 MRP**。

![需求驱动型 MRP 工作区。](media/ddmrp-workspace.png "需求驱动型 MRP 工作区")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>获取分离点和计划订单的概览

除了 **需求驱动型 MRP** 工作区之外，Supply Chain Management 还提供了多个页面，您可以在其中查看有关 DDMRP 设置、分离点和计划订单的信息。 其中一些页面还提供了操作窗格上的方便按钮，可让您管理缓冲区、运行主计划以及打开其他相关视图。

- 若要按净流水平查看分离点状态，请转到 **主计划 \> 主计划 \> DDMRP \> 按净流显示的分离点状态**。
- 若要按现有量库存水平查看分离点状态，请转到 **主计划 \> 主计划 \> DDMRP \> 按现有量显示的分离点状态**。
- 若要查看分离点的计划订单，请转到 **主计划 \> 主计划 \> DDMRP \> 分离点的计划订单**。
- 若要查看分离的提前期，请转到 **主计划 \> 主计划 \> DDMRP \> 分离的提前期**。

## <a name="clean-up-decoupling-point-buffer-values"></a>清除分离点缓冲区值

随着时间的推移，您的系统将生成大量与正在进行的缓冲区计算相关的历史数据。 此历史数据将导致您的数据量增加，最终可能会影响您的系统性能。 因此，我们建议您偶尔清理旧的分离点缓冲区值。

> [!WARNING]
> 清理作业将删除历史缓冲区值设置和历史现有量/净流信息。 此操作不可逆。

按照以下步骤清理分离点缓冲区值。

1. 转到 **主计划 \> 主计划 \> DDMRP \> 清理分离点缓冲区值**。
1. 在 **清理分离点缓冲区值** 对话框中，设置以下字段：

    - **删除过去几天的记录(天)** - 以天为单位指定要保留的最晚记录的年限。 将删除早于此值的所有分离点缓冲区值记录。
    - **主计划** - 选择包含应该受此清理影响的物料的主计划。 应用您在此对话框中指定的 **筛选器** 设置后，清理将应用于计划中的所有物料。

1. 要限制此批处理作业运行所应针对的记录集，请在 **要包括的记录** 快速选项卡上选择 **筛选器** 以打开 **查询** 对话框。 此对话框的工作方式与其用于 Supply Chain Management 中其他类型的[后台作业](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)时一样。
1. 在 **在后台运行** 快速选项卡上，指定执行清理的方式、时间和频率。 这些字段的工作方式与它们用于 Supply Chain Management 中其他类型的[后台作业](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)时一样。
1. 选择 **确定** 以将新作业添加到要执行的批处理队列。
