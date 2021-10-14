---
title: 对基准预测进行手动调整
description: 本主题介绍如何手动调整基准预测和查看预测的详细信息。
author: ChristianRytt
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37d78e97a6c7f9152ab0b893a35a3ae70d5adabc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579632"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>对基准预测进行手动调整

[!include [banner](../includes/banner.md)]

本主题介绍如何手动调整基准预测和查看预测的详细信息。 

在进行手动调整之前，务需您理解各个页上的若干概念。

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>“调整后的需求预测”页上的网格
**调整后的需求预测** 页包括具有以下结构的网格：

-   第一列显示为其生成预测的物料、物料分配参数、公司等。 该页的副标题提供在网格中显示的当前预测维度的描述。 例如，如果该页的副标题是 **公司/站点/物料分配参数**，且网格中的行标题是 **USMF / 1 / D\_Alloc**，则该行显示 USMF 公司的预测、站点 1 和 **D\_Alloc** 物料分配参数。
-   随后的列表示为其生成预测的预测时段。 每一列标题是列显示的预测时段的第一个日期。
-   这些单元格中的值表示该特定预测时段的一个物料的预测、物料分配参数等。

## <a name="forecast-aggregation-and-de-aggregation"></a>预测合并和取消合并
该页的副标题显示预测合并的级别。 

例如，如果页的副标题是 **公司/站点/分配参数/物料编号/颜色/尺寸/配置/样式**，则没有预测合并，并且预测在物料及其维度级别显示。 若要更改合并，请使用 **更改预测维度** 页，可以从应用程序菜单打开。 

若要修改预测，单击可用的任何单元格，并键入已调整的预测值。 编辑后的单元格将立即变为粗体，指示它显示的预测不是需求预测服务创建的预测，不过已进行手动调整。 

如果您更改合并以使页显示更多聚合数据，可以使用 **需求预测行** 页查看构成聚合预测的单独预测行。 

例如，您在物料级别生成了预测，不过，您知道由于促销或其他类似的事件，此物料的需求在所有站点都将增加。 在这种情况下，您可以在 **更改预测维度** 页设置合并为 **公司/物料分配参数/物料**。 您可以为在 **调整后的需求预测** 网格中的所有站点的物料调整全局预测。 若要查看跨所有站点的更改的效果，请打开 **需求预测行** 页。 在此页，您将看到每个站点的物料、经调整的预测数量和原始预测数量在一行。 

在聚合级别进行预测数量调整时，M此系统使用加权分配在创建合并的行中分配更改。 

您还可以在 **需求预测行** 页进行手动调整，方法是通过修改取消合并网格中的 **总数量** 值或 **数量** 单元格。

## <a name="viewing-details-of-the-forecast"></a>查看预测详细信息
您可以打开 **需求预测详细信息** 页查看有关预测的更多信息。 

**需求预测详细信息** 页以图形和表格式显示以下信息：

-   预测所基于的历史需求。
-   主计划使用的当前预测。
-   新的需求预测值和按其手动调整的金额。
-   预测值的置信区间。
-   用于生成预测的预测模型。 如果您正在查看聚合数据，您将看到用于所有聚合时间系列的所有方法的列表。
-   内部模型准确性 (MAPE)。 有关预测准确性的详细信息，请参阅[监控预测准确性](monitor-forecast-accuracy.md)。

**注意：**

-   如果从“功能管理”启用 **根据需求预测详细信息选择预测模型**，您将能够选择要包含在 **需求预测详细信息** 页上的历史预测的预测模型。
-   显示在该页的 **预测** 部分中的置信区间表示置信区间上限和置信区间下限之间的差异。 要查看上限和下限的值，将鼠标悬停在 **以图形方式表示的历史需求和预测** 部分的图表上。
-   如果您使用需求预测 Microsoft Azure 机器学习，您可以指定生成的预测应具有的可信度百分比。 置信区间包含一系列用作良好的需求预测估计的值。 可信度百分比 95% 表示需求预测有 5% 的几率超出置信区间范围。

您还可以手动调整 **需求预测详细信息** 页上的预测，方法是通过修改 **预测** 部分的 **预测** 行中的值。

## <a name="additional-resources"></a>其他资源

[监控预测准确性](monitor-forecast-accuracy.md)

[生成统计基准预测](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]