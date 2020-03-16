---
title: 计划优化拟合分析
description: 本主题说明如何根据计划优化功能的能力来验证当前的设置和数据。
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 25f3b39d0e6e88eb3f042ab93773e9724528ab0f
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076170"
---
# <a name="planning-optimization-fit-analysis"></a>计划优化拟合分析

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

要查看您当前的设置和数据与计划优化功能之间的兼容性，请转到**主计划** \> **设置** \> **计划优化拟合分析**，然后选择**运行分析**。 如果分析发现任何不一致之处，则会在同一页面上列出。 （分析可能需要几分钟运行。）

> [!NOTE]
> 如果发现不一致，您仍然可以使用计划优化。 拟合分析的结果仅显示计划服务不支持您当前设置的地方。 换言之，它们显示某些流程可能被忽略或不被支持的地方。

## <a name="analysis-results-example-1"></a>分析结果：示例 1

- **功能：** 生产
- **问题：** BOM 级别大于零的物料：56
- **说明：** 拟合分析发现有 56 个物料的物料清单 (BOM) 设置用于生产。 由于当前版本的计划优化不支持生产，因此计划优化将生成计划采购订单，而不是计划生产订单。 它还将显示警告，列出受影响的物料。

### <a name="analysis-results-example-2"></a>分析结果：示例 2

- **功能：** 操作
- **问题：** 启用了操作计算的覆盖范围组：6
- **说明：** 拟合分析发现了六个启用了操作计算的覆盖范围组。 由于当前版本的计划优化不支持操作，因此在主计划期间将不会生成任何操作。

## <a name="related-resources"></a>相关资源

[计划优化概述](planning-optimization-overview.md)

[开始使用计划优化](get-started.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[将筛选器应用于计划](plan-filters.md)

[取消计划作业](cancel-planning-job.md)
