---
title: "需求预测概览"
description: "需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。 增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86f2f556d1b2d8711e7419b4e85904e297097380
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="demand-forecasting-overview"></a>需求预测概览

[!include[banner](../includes/banner.md)]


需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。 增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。

若要生成基准预测，历史交易记录汇总被传递到在 Azure 上承载的 Microsoft Azure 机器学习服务。 由于此服务不在用户之间共享，其可以轻松地自定义以满足特定于行业的要求。 您可以使用 Dynamics 365 for Operations 可视化预测、调整预测和查看有关预测准确性的关键绩效指标 (KPI)。

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

-   **模块性** – 需求预测是模块化的和易于配置。 您可以通过在**贸易** &gt; **库存预测** &gt; **需求预测**更改 Configuration Key 来打开和关闭功能。
-   **Microsoft 堆栈的重用** – Microsoft 在 2015 年 2 月启动机器学习平台。 机器学习现在是 Microsoft Cortana 分析套件的一部分，让您可以通过使用算法 R 或 Python 编程语言和简单的拖放界面来迅速轻松地创建预测性分析实验，如需求估计实验。
    -   您可以下载 Dynamics 365 for Operations 需求预测实验，更改它们以满足您的业务要求，在 Azure 上作为 Web 服务发布它们，并使用它们生成需求预测。 如果您作为企业级用户购买了生产规划员的 Dynamics 365 for Operations 订阅，则可以下载这些实验。
    -   您可以从 [Cortana 分析库](https://gallery.cortanaanalytics.com/)下载当前可用的任何需求预测实验。 而 Dynamics 365 for Operations 需求预测实验将自动与 Dynamics 365 for Operations 集成，客户和合作伙伴必须处理从 [Cortana 分析库](https://gallery.cortanaanalytics.com/)下载的实验的集成。 因此，[Cortana 分析库](https://gallery.cortanaanalytics.com/)的实验不如使用 Dynamics 365 for Operations 需求预测实验那样简单。 您必须修改实验代码，以便它们使用 Dynamics 365 for Operations 应用程序编程接口 (API)。
    -   您可以在 Microsoft Azure 机器学习工作室中创建自己的实验，在 Azure 上作为服务发布，并使用它们生成需求预测。
    -   如果您不需要高性能，或者，如果您不需要处理大量数据，您可以使用机器学习的免费层。 我们建议始终从这一层开始，尤其是在实施和测试阶段。 如果您需要高性能和额外存储，您可以使用机器学习的标准层。 这一层要求 Azure 订阅并需要其他成本。 有关机器学习定价的详细信息，请参阅 <http://aka.ms/machine-learning-price-info>。
-   **在任何解耦点的预测缩减** – Dynamics 365 for Operations 中的需求预测构建此功能，让您可以在任何解耦点预测相关和不相关的需求。

## <a name="basic-flow-in-demand-forecasting"></a>需求预测的基本流程
下图显示需求预测的基本流程。 

[![需求预测介绍图](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

需求预测生成在 Dynamics 365 for Operations 中开始。 收集 Dynamics 365 for Operations 交易记录数据库的历史交易记录数据并填写暂存表。 此暂存表随后提供给机器学习服务。 通过执行最小的自定义设置，可以将各个数据源插入到暂存表。 数据源可以包括 Microsoft Excel 文件、逗号分隔值 (CSV) 文件和 Microsoft Dynamics AX 2009 和 Microsoft Dynamics AX 2012 的数据。 因此，可以生成考虑在多个系统中分散的历史数据的需求预测。 但是，主数据，例如物料名称和度量单位，在各个数据源中必须是相同的。

如果您使用 Dynamics 365 for Operations 需求预测机器学习实验，它们在五个时间系列预测法中寻找最适合的方法来计算基准预测。 这些预测方法的参数在 Dynamics 365 for Operations 中管理。 

预测、历史数据和对之前迭代的需求预测进行的任何更改然后在 Dynamics 365 for Operations 中可用。 

您可以使用 Dynamics 365 for Operations 来可视化和修改基准预测。 手动调整必须授权，然后预测才能用于计划。

## <a name="limitations"></a>限制
Dynamics 365 for Operations 中的需求预测是帮助制造行业客户创建预测流程的工具。 它提供了需求预测解决方案的核心功能，并设计为可以轻松扩展。 需求预测可能对零售、批发、仓库、运输或其他专业服务等行业的客户不是最合适。

<a name="see-also"></a>请参阅
--------

[需求预测设置](demand-forecasting-setup.md)

[生成统计基准预测](generate-statistical-baseline-forecast.md)

[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)

[授权调整后的需求预测](authorize-adjusted-forecast.md)

[监控预测准确性](monitor-forecast-accuracy.md)

[在计算需求预测时，需从历史交易记录数据中删除离群值](remove-historical-outliers-calculating-demand-forecast.md)




