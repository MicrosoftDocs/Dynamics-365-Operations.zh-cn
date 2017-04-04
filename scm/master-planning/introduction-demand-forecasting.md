---
title: "需求预测概览"
description: "需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。 增强的需求预测规则缩减为自定义一个质量提供有用的解决方案。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>需求预测概览

需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。 增强的需求预测规则缩减为自定义一个质量提供有用的解决方案。

若要生成基准预测，历史交易记录汇总被传递到在 Azure 上承载的 Microsoft Azure 机器学习服务。 由于此服务不在用户之间共享，其可以轻松地自定义以满足特定于行业的要求。 您可以使用 Dynamics 365。工序可直观预测，该调整预测和显示有关预测准确性的关键绩效指标 (KPI)。

## <a name="key-features-of-demand-forecasting"></a>需求预测的主要功能
以下是需求预测的一些主要功能：

-   生成基于历史数据的统计基准预测。
-   使用一组动态的预测维度。
-   可视化需求趋势、置信区间和预测调整。
-   授权在计划流程中使用的已调整预测。
-   删除离群值。
-   创建预测准确性的度量。

## <a name="major-themes-in-demand-forecasting"></a>需求预测的主要主题
三个主要主题在需求预测中实施：

-   **模块性** – 需求预测是模块化的和易于配置。 你可以通过更改 Configuration Key 打开和关闭功能在贸易** &gt; ** **库存预测** &gt; ** **需求预测。
-   ** Microsoft 的一堆重用** – Microsoft 在 2015 年 2 月启动机器学习平台。 使用机器学习，则算法 R 或 Python 编程语言和简单的拖放界面，现在为 Microsoft Cortana 逻辑分析方法套件的一部分，可以轻松快捷地创建预期分析测试需求，例如估计，测试。
    -   您可以将工序需求预测测试的 Dynamics 365，更改其满足您的业务要求，为其发布 Azure 的一个网站和服务使用它们生成需求预测。 如果您购买了预订的 Dynamics 365 生产工序计划表的级别为企业用户，测试可以下载。
    -   您可以从 [Cortana 分析库](https://gallery.cortanaanalytics.com/)下载当前可用的任何需求预测实验。 而工序需求预测测试的 Dynamics 365 自动集成。工序的 Dynamics 365，客户和合作伙伴必须下载处理则从测试的集成 Cortana 逻辑分析方法库 [] (https://gallery.cortanaanalytics.com/)。 因此，从测试的 [Cortana 逻辑分析方法库] (https://gallery.cortanaanalytics.com/) 不相同的直接使用 Dynamics "为 https://gallery.cortanaanalytics.com/)。工序需求预测测试。 必须修改的测试代码，以使工序应用程序编程接口 (API) 使用 Dynamics (API)。
    -   您可以在 Microsoft Azure 机器学习工作室中创建自己的实验，在 Azure 上作为服务发布，并使用它们生成需求预测。
    -   如果您不需要高性能，或者，如果您不需要处理大量数据，您可以使用机器学习的免费层。 我们建议始终从这一层开始，尤其是在实施和测试阶段。 如果您需要高性能和额外存储，您可以使用机器学习的标准层。 这一层要求 Azure 订阅并需要其他成本。 有关机器学习定价的详细信息，请参阅 <http://aka.ms/machine-learning-price-info>。
-   **在任何离散的积分的预测**缩减–需求预测。工序的 Dynamics 365 功能{{在此：on}}内部版本，以便您预测相关且独立任何在需求分解的起始点。

## <a name="basic-flow-in-demand-forecasting"></a>需求预测的基本流程
下图显示需求预测的基本流程。 

[![需求预测介绍图] (。/media/demand 预测 Introduction.png)](。/media/demand 预测 introduction.png)

Dynamics 中 365 的需求预测生成开始的工序。 从 Dynamics 365 的历史交易记录数据工序可处理的数据库收集和已填充：时，会升级表。 此表升级后提供对机器学习服务。 通过执行最小的自定义内容，可以插入到暂存不同数据源表。 数据源可以提供包含 Microsoft Excel 文件、逗号分隔值 (CSV) 文件和数据并做出中从 Microsoft Dynamics AX (CSV) 和 Microsoft Dynamics AX 2009。 因此，可以生成多数据历史考虑在系统中分配的需求预测。 但是，主数据，例如物料名称和度量单位，在各个数据源中必须是相同的。

如果您为工序需求预测测试使用机器学习 Dynamics 365，则查找一特定合身在五个时间数列预测"法计算基准中预测。 这些方法预测的参数。工序的 Dynamics 365 管理。 

预测、历史数据和对上面的迭代的需求预测的任何更改将可在 Dynamics 365。工序。 

您可以使用 Dynamics 365。工序可直观和修改基线预测。 手动调整必须授权，然后预测才能用于计划。

## <a name="limitations"></a>限制
Dynamics 中 365 的需求预测的工序是帮助制造行业的客户创建预测流程的工具。 它提供需求预测解决方案的核心功能和设计，以便可以轻松地是扩展的。 不要求预测可能尤其合身行业的 (例如"零售")，批发，仓库中，运输，或者其他专业服务。

<a name="see-also"></a>请参阅
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


