---
title: 现金流预测(预览版)
description: 本主题描述现金流预测功能。
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f4b48122ea54c201888d71afb5fb731ebcab230d
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638768"
---
# <a name="cash-flow-forecast-preview"></a>现金流预测(预览版)

[!include [banner](../includes/banner.md)]

现金流对任何业务都至关重要。 即使盈利的公司如果不保持现金流来满足眼前的需求，他们也可能面临破产。 Finance insights 中的现金流预测功能可帮助公司有效地监控和管理其现金余额。 此功能使用机器学习来帮助企业比以前更准确地预测现金流。 还可以帮助经理制定决策，以根据其当前的现金状况来优化商机。 

对于大多数公司而言，管理现金流和进行现金流预测是一个繁琐、重复且手动的过程。 大多数公司依靠的 Microsoft Excel 解决方案的复杂程度各异。 准确预测现金流的挑战包括：

- 决策者无法使用数据，因为数据分散在多个地方，包括： 
  - 会计或企业资源计划系统
  - 财务计划软件
  - Excel
  - 其他软件应用程序 
- 预测基于每个领域或部门内“孤岛”中的内部知识。
- 财务实现后，衡量现金流预测的准确性不确定且困难。
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>现金流预测功能的详细信息
现金流预测功能包括以下功能。 

- 轻松将来自外部系统的现金流数据集成到 Dynamics 365 Finance 中。 现金流预测也可以使用数据导入-导出框架。 该框架使与 Excel OData 的集成变得容易。 您还可以合并来自多个来源的数据以创建全面的现金流解决方案。 

- 介绍智能现金头寸。 根据客户的付款行为创建现金头寸，以预测公司何时可以期望现金进入其帐户。 它还分析了付款供应商的历史模式，以预测何时可能会支付将来的发票和订单。 

- 通过与 AI Builder 的自动集成使用时间序列预测，引入了用于长期预测的智能现金流预测。

- 提供保存特定现金流头寸或预测，对其进行编辑，然后轻松地将其与实际财务状况进行比较和衡量预测性能的功能。

- 通过快照比较启用假设分析。 例如，您可以创建代表快照的最乐观、最悲观和最现实的快照，然后比较并查看差异。

- 提供查看法人中多种货币的现金流预测以及筛选和查看与银行帐户相关的现金流的功能。 

- 使您可以筛选和查看与财务维度相关的银行帐户。

Dynamics 365 Finance 中的现金流预测功能将使您的组织能够将繁琐、复杂但重复的现金流预测转换为简单的自动化流程。 自动化现金流预测的最繁琐的方面，使您可以专注于关键决策，以实现期望的业务成果。

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>设置现金流预测的维度
**现金流预测设置** 页上的一个新选项卡可让您控制使用财务维度在 **现金流预测** 工作区中进行筛选。 仅当启用现金流预测功能后，此选项卡才会出现。 

在 **维度** 选项卡上，从要用于筛选的维度列表中进行选择，然后使用箭头键将其移至右侧列。 只能选择两个维度来筛选现金流预测数据。 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
