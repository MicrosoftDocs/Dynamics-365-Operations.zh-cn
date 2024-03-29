---
title: 比较物料价格存储报表
description: 了解如何生成比较物料价格存储报表，然后浏览和/或导出结果。
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c6373679299b68413d75236ca8cc18ceba03e091
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334976"
---
# <a name="compare-item-prices-storage-report"></a>比较物料价格存储报表

[!include [banner](../includes/banner.md)]

本文说明如何运行 **比较物料价格存储** 报表并以数字方式提供输出，可以是 Dynamics 365 Supply Chain Management 中的交互式页面，也可以是多种格式中任何一种的导出文档。

在浏览器中查看此报表时，将根据配置的布局动态调整列和聚合余额。 可以对结果排序，进行过滤，以及向下钻取到数据中，等等。

报告结果存储在 **比较物料价格** 数据实体中，可用于过滤结果并将其导出为 CSV 或 Microsoft Excel 之类格式。

如果输出中包含多行，**比较物料价格存储** 报表非常有用。 例如，如果成本计算版本中有 40,000 个以上的物料的物料价格未决，则输出将包含多行。

## <a name="turn-the-compare-item-prices-storage-feature-on-or-off"></a>打开或关闭比较物料价格存储功能

要使用此功能，必须为您的系统打开它。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.29，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *比较物料价格存储* 功能来打开或关闭此功能。

## <a name="generate-a-compare-item-prices-storage-report"></a>生成比较物料价格存储报表

请执行以下步骤生成并存储 **比较物料价格存储** 报表：

1. 转到 **成本管理 > 查询和报表 > 预先确定的成本报表 > 比较物料价格存储**。

1. 选择 **新建** 打开 **比较物料价格** 窗格。 设置以下选项以定义要在报表中比较的价格：

    - 在 **参数** 快速选项卡上，为报表提供唯一 **名称**，并使用 **要比较的未决价格** 和 **用于比较的价格** 部分中的字段定义要比较的价格和日期。
    - 在 **要包括的记录** 快速选项卡上，设置筛选器和约束以定义要在报表中包括的数据。
    - 在 **在后台运行** 快速选项卡上，设置报表的生成方式、时间和频率。
    > [!NOTE]
    > 此报告始终作为批处理作业的一部分执行。

1. 选择 **确定** 应用设置并关闭窗格。

1. 批处理作业完成后，它将列在 **比较物料价格存储** 页中。 您可能需要刷新页面才能查看此报表。

## <a name="explore-the-compare-item-prices-storage-report"></a>浏览比较物料价格存储报表

生成报表后，随时可以查看和浏览报表，如下所示：

1. 转到 **成本管理 > 查询和报表 > 预先确定的成本报表 > 比较物料价格存储**。

1. 从列表中选择报表。

1. 执行以下选项之一：

    - 选择 **概览** 获取报表结果的概览。
    - 选择 **查看详细信息** 获取更详细的报表视图

1. 所选视图打开之后，可执行以下操作：

    - 选择几乎任何标题以按照该列中的值对表进行排序或筛选，就像在 Supply Chain Management 中对大多数标准窗体的处理一样。 请注意，不能对 **单价净额变化百分比** 列进行排序或筛选，因为这是计算字段。
    - 选择 **维度显示** 打开一个窗格，可在其中选择窗体中要包含哪些维度列。 如果要保存这些设置，以便保留到下次打开报表时，请将 **保存设置** 设置为 **是**。 选择 **确定** 应用设置并关闭。
    - 选择窗体中的任何行，然后选择 **查看详细信息** 查看有关所选物料的详细信息。 您将可以从此处向下钻取到数据。
    - 选择窗体中的任何行，然后选择 **查看对比图** 查看结果的交互式图形表示，因为它们与您的所选物料有关。 可以通过选择图表中的各种图形元素和图例浏览这些结果。
    - 选择窗体中的任何行，然后选择 **查看计算详细信息** 查看有关与所选物料相关的计算的详细信息。 您将可以从此处向下钻取到数据。

## <a name="export-the-compare-item-prices-storage-report"></a>导出比较物料价格存储报表

生成的所有报表都存储在 **比较物料价格** 数据实体中。 可使用 Supply Chain Management 的标准数据管理功能将此实体中的数据导出到任何支持的数据格式，包括 CSV 或 Microsoft Excel。

下面是如何导出 **比较物料价格存储** 报表的示例：

1. 转到 **系统管理 > 工作区 > 数据管理**。

1. 选择 **数据管理** 部分中的 **导出** 按钮。

1. 将打开 **导出** 页面，用于设置导出作业。 首先为作业提供 **组名称**。

1. 在 **选定实体** 部分中，选择 **添加实体** 打开一个对话框，可在其中设置以下选项：

    - **实体名称** - 选择 **比较物料价格**。
    - **目标数据格式** - 选择要导出到的格式。

1. 选择 **添加** 添加新行，然后选择 **关闭** 关闭对话框。

1. 通常一次导出一个报表。 方法是，为刚才添加到 **查询** 窗格中的行设置 **筛选器**。 这样就可以定义导出中要包含 **比较物料价格** 实体中的哪些报表。 设置以下筛选选项以导出单个报表：

    - 在 **范围** 选项卡中，选择 **添加** 添加新行。
    - 将 **表** 设置为 **比较物料价格**。
    - 将 **派生表** 设置为 **比较物料价格**。
    - 将 **字段** 设置为要充当筛选依据的字段。 通常使用 **执行名称** 或 **执行时间**。
    - 将 **条件** 设置为要查找的所选字段中的值（报表的名称或生成时间）。
    - 如有必要，向 **范围** 表添加更多行，直到唯一确定了要查找的报表。

1. 选择 **确定** 保存设置并关闭。

1. 选择 **保存** 则保存导出设置。

1. 打开 **导出选项** 选项卡，然后选择 **立即导出** 生成导出文件。

1. 将打开 **执行摘要** 页，可在其中查看导出作业的状态和导出的实体的列表。 选择 **实体处理状态** 区域中列出的 **比较物料价格** 实体，然后选择 **下载文件** 下载从该实体导出的数据。

有关如何使用数据管理导出数据的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]