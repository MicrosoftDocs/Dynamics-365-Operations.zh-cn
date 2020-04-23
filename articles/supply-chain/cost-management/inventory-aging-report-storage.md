---
title: 库龄报表
description: 本主题介绍使您可以运行库龄报表并使输出以表单和图表形式提供的功能。
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201610"
---
# <a name="inventory-aging-report"></a>库龄报表


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

在 Microsoft Dynamics 365 Supply Chain Management 中，您可以运行**库龄**报表，并使输出以表单和图表形式提供。 在表单中，根据配置的布局动态调整列和聚合余额。 图表提供支持筛选的可视概览，并允许您向下钻取到详细信息。 此外，名为**库龄报表**的数据实体使您可以将**库龄**报表运行的结果导出为 Microsoft Excel 文件或 PDF 文件等格式。

在输出包含很多行的情况下，这种运行**库龄**报表的方法很有用。 例如，如果您有 50,000 个商品和 300 个作为仓库创建的商店，并且您按商品、站点和仓库请求库龄，输出将包含许多行。

## <a name="run-an-inventory-aging-report"></a>运行库龄报表

1. 转到**成本管理 \> 查询和报表 \> 库龄报表存储**。
1. 选择**新建**。
1. 在**流程标识符 – 名称**字段中，输入报表的唯一名称。
1. 选择**标识 – ID** 报表，并根据需要对其进行筛选。

    报表执行始终在批处理作业中完成。

1. 批处理作业完成后，输出将显示在**库龄报表存储**页面上。
1. 要作为具有传统网格布局的表单查看输出，请选择**查看详细信息**。 要以汇总图表形式查看输出，请选择**查看图表**。

    > [!NOTE]
    > 表单将不包括报表布局中定义的小计。

**库龄报表**数据实体使您可以通过将**流程标识符 – 名称**字段的筛选器应用到数据管理支持的任何格式来导出**库龄**报表的输出。
