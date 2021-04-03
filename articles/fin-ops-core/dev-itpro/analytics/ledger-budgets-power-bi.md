---
title: 实际与预算 Power BI 内容
description: 此主题描述实际与预算 Power BI 内容。 说明如何访问报表，并提供有关数据模型的信息。
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568565"
---
# <a name="actual-vs-budget-power-bi-content"></a>实际与预算 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题描述 **实际与预算** Microsoft Power BI 内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**实际与预算** Power BI 内容为负责监督组织中的实际与预算绩效的人员而创建。 **实际与预算** Power BI 内容可用于查看您的预算差异。 您可以按科目类别、预算代码、主科目、主科目描述或会计期间分析当前年度的预算，以更好地了解任何差异的原因。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
来自 **实际与预算** Power BI 内容的报表显示在 **分类帐预算和预测** 和 **CFO** 工作区中。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表
下表提供有关在 **实际与预算** Power BI 内容中的每个报表页找到的指标的详细信息。

| 报表                      | 指标                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| 支出 - 实际与预算 | <ul><li>本年支出总额</li><li>本年支出总额预算</li></ul>  |
| 收入 - 实际与预算  | <ul><li>本年收入总额</li><li>本年收入总额预算</li><ul>     |
| 费用                     | <ul><li>本年支出总额</li><li>基于预算的支出目标</li><ul> |
| 收入                     | <ul><li>本年收入总额</li><li>基于预算的收入目标</li><ul>   |
| 净收益                  | <ul><li>本年度净收益</li><li>基于预算的净收益目标</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

| 实体                    | 内容                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| 总帐活动 | 总帐交易金额                                       |
| 预算活动         | 预算登记的交易金额                                      |
| 主科目             | 充当报表筛选依据的主科目                                               |
| 会计日历          | 充当报表筛选依据的会计日历                                            |
| 分类帐                   | 可用于筛选报表到当前分类帐的分类帐              |
| 预算代码              | 充当报表筛选依据的预算代码                                                |
| 法人            | 可用于筛选报表到当前法人的法人 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]