---
title: 主计划主页
description: 主计划允许公司确定和平衡原材料和产能的将来需求，以实现公司目标。
author: ChristianRytt
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15fbab7d0260ed714edfbbb5ef54caddb69cae3c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359997"
---
# <a name="master-planning-home-page"></a>主计划主页

[!include [banner](../includes/banner.md)]

在其核心，主计划允许公司确定和平衡原材料和产能的将来需求，以实现公司目标。 主计划评估以下情况：

- 哪些原材料和产能当前可用？
- 完成生产需要哪些原材料和产能？ 例如，必须进行哪些生产、采购、转移或留出安全库存才能完成生产。

主计划使用此信息来计算需求和生成计划订单。

三个主计划流程是：

- **主计划** - 主计划计算净需求。 它基于当前的实际订单，使公司在短期内每日控制库存补货。 描述它的另一个术语是 *净需求计划*。 有关主计划的详细信息，请参阅[主计划概览](master-plans.md)。

- **预测计划** - 预测计划计算总需求。 它基于将来的推测（或预测），让公司可以执行长期的物料和产能规划。 有关详细信息，请参阅[需求预测概览](introduction-demand-forecasting.md)。

- **内部公司主计划** - 内部公司主计划跨法人计算净需求。 它连接公司之间的需求和供应，不仅是短期的固定需求和供应，还有长期的计划（还未确定）需求和供应。 有关详细信息，请参阅[内部公司计划](planning-optimization/Intercompany-planning.md)。

公司可以更改计划的输出。 他们可以运行再生改变、净改变，或二者。 再生计划更新所有需求，而净改变计划只更新在上次计划编制运行后有新需求的项目计划。

主计划编制计划通常涉及短期，可以是从一个星期到六个月的任何时间段。 主计划模块确定将满足当前需求（净需求）的供应（材料）和产能（资源）。 在大多数公司中，这扩展为在要接收的产品中包含最久的累积提前期。

## <a name="learning-map"></a>学习图

下面的学习图显示构成主计划模块框架的主要概念和任务。 单击[快速链接](#quick-links)部分中的链接了解如何使用该模块。

[![主计划的学习图。](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>快速链接

- [主计划概览](master-plans.md)  
- [生成受约束计划](./tasks/constrained-plan.md)
- [创建联产品的物料计划](./tasks/create-material-plan-co-products.md)
- [主计划和多站点功能概览](master-plan-multisite-functionality.md)
- [创建内部公司计划](./tasks/create-intercompany-plan.md)
- [需求预测概览](introduction-demand-forecasting.md)
- [预测缩减参数](reduction-keys.md)

## <a name="additional-resources"></a>其他资源

### <a name="roadmaps"></a>路线图

转到 [Microsoft Dynamics 365 路线图](https://roadmap.dynamics.com/)以了解已发布和正在开发的新功能。

### <a name="blogs"></a>博客

您可以在 [Dynamics AX 制造研发团队博客](/archive/blogs/axmfg/)和 [Dynamics AX 研发团队中的供应链管理博客](https://blogs.msdn.microsoft.com/dynamicsaxscm)中找到有关主计划及其他解决方案的建议、新闻和其他信息。

### <a name="task-guides"></a>任务指南

其他帮助作为任务指南提供。 若要访问任务指南，请单击任何页面上的 **帮助** 按钮。

### <a name="webinars"></a>网络研讨会

[使用 Azure 机器学习进行需求预测](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>技术会议录制

- [扩展需求预测功能](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [主计划 - 有关性能疑难解答的提示和窍门](https://youtu.be/7v8BPmEs9Dg)
- [求助! MRP 太慢！](https://youtu.be/RLXybx20B5o)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]