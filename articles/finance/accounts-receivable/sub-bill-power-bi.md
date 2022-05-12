---
title: 订阅计费 Power BI 内容
description: 此主题介绍订阅计费 Microsoft Power BI 内容中包含的内容。
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: fad96bdaf60e7772e9ea1ff937435b0274303505
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645382"
---
# <a name="subscription-billing-power-bi-content"></a>订阅计费 Power BI 内容

[!include[banner](../includes/banner.md)]

此主题介绍订阅计费 Microsoft Power BI 内容中包含的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。 

## <a name="overview"></a>概述

已为订阅计费记帐员和经理创建了订阅计费 Power BI 内容。 它提供关键的订阅计费指标，例如计费计划的每月经常性收入 (MRR)，以及延期计划的递减余额和瀑布图信息。 它使用来自计费计划和延期计划的数据来提供经常性收入和收入的概览。

Power BI 内容具有以下三个选项卡，这些选项卡总共提供四个分析报告： 

- **分析 - MRR** - 此选项卡提供 **每月定期计费** 报告和 **计费计划详细信息** 报告。
- **分析 - 瀑布图** - 此选项卡提供 **收入瀑布图** 报告。
- **分析 - 递减余额** - 此选项卡提供 **递减余额** 报告。

## <a name="view-data-on-the-analytical-reports"></a>查看分析报告上的数据

在您可以查看分析报告上的数据之前，您必须运行一个为每个报告生成报告数据的定期流程。 必须生成报告所需的这些数据，因为它未直接存储在数据库中。 

1. 转到 **订阅计费 \> 定期合同计费 \> 定期任务 \> MRR 分析报告批处理**，并按照以下步骤操作：

    1. 输入不超过三年的日期范围。
    2. 可选：设置定期批处理作业以定期刷新数据。
    3. 选择 **确定**。

2. 批处理作业运行完后，请转到 **系统管理 \> 设置 \> 实体存储**，并刷新 **MRR 报告** 聚合度量。 
3. 转到 **订阅计费 \> 收入和支出延期 \> 定期任务 \> 瀑布图分析报告批处理**，并按照以下步骤操作：

    1. 输入相隔不超过 26 个期间的开始日期和结束日期。 
    2. 如果要查看当前期间中过去期间的预测金额，请将 **预测当前期间中的过去金额** 选项设置为 **是**。
    3. 可选：设置定期批处理作业以定期刷新数据。
    4. 选择 **确定**。 

4. 批处理作业运行完后，请转到 **系统管理 \> 设置 \> 实体存储**，并刷新 **瀑布图报告** 聚合度量。
5. 转到 **订阅计费 \> 收入和支出延期 \> 定期任务 \> 余额递减法分析报表批处理**，并按照以下步骤操作：

    1. 输入相隔不超过 26 个期间的开始日期和结束日期。 
    2. 如果要查看当前期间中过去期间的预测金额，请将 **预测当前期间中的过去金额** 选项设置为 **是**。
    3. 可选：设置定期批处理作业以定期刷新数据。
    4. 选择 **确定**。

6. 批处理作业运行完后，请转到 **系统管理 \> 设置 \> 实体存储**，并刷新 **递减余额报告** 聚合度量。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

**预订计费** 工作区中会显示预订计费 Power BI 内容。
