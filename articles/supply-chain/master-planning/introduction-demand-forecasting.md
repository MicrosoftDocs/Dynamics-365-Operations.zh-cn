---
title: "需求预测概览"
description: "需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。 增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5a651fcd386e9f976559a1fc540c5d9191ab632b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="demand-forecasting-overview"></a><span data-ttu-id="7ecd6-104">需求预测概览</span><span class="sxs-lookup"><span data-stu-id="7ecd6-104">Demand forecasting overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7ecd6-105">需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-105">Demand forecasting is used to predict independent demand from sales orders and dependent demand at any decoupling point for customer orders.</span></span> <span data-ttu-id="7ecd6-106">增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-106">The enhanced demand forecast reduction rules provide an ideal solution for mass customization.</span></span>

<span data-ttu-id="7ecd6-107">若要生成基准预测，历史交易记录汇总被传递到在 Azure 上承载的 Microsoft Azure 机器学习服务。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-107">To generate the baseline forecast, a summary of historical transactions is passed to a Microsoft Azure Machine Learning service that is hosted on Azure.</span></span> <span data-ttu-id="7ecd6-108">由于此服务不在用户之间共享，其可以轻松地自定义以满足特定于行业的要求。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-108">Because this service isn't shared among users, it can easily be customized to meet industry-specific requirements.</span></span> <span data-ttu-id="7ecd6-109">您可以使用 Finance and Operations 可视化预测、调整预测和查看有关预测准确性的关键绩效指标 (KPI)。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-109">You can use Finance and Operations to visualize the forecast, adjust the forecast, and view key performance indicators (KPIs) about forecast accuracy.</span></span>

## <a name="key-features-of-demand-forecasting"></a><span data-ttu-id="7ecd6-110">需求预测的主要功能</span><span class="sxs-lookup"><span data-stu-id="7ecd6-110">Key features of demand forecasting</span></span>
<span data-ttu-id="7ecd6-111">以下是需求预测的一些主要功能：</span><span class="sxs-lookup"><span data-stu-id="7ecd6-111">Here are some of the main features of demand forecasting:</span></span>

-   <span data-ttu-id="7ecd6-112">生成基于历史数据的统计基准预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-112">Generate a statistical baseline forecast that is based on historical data.</span></span>
-   <span data-ttu-id="7ecd6-113">使用一组动态的预测维度。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-113">Use a dynamic set of forecast dimensions.</span></span>
-   <span data-ttu-id="7ecd6-114">可视化需求趋势、置信区间和预测调整。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-114">Visualize demand trends, confidence intervals, and adjustments of the forecast.</span></span>
-   <span data-ttu-id="7ecd6-115">授权在计划流程中使用的已调整预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-115">Authorize the adjusted forecast to be used in planning processes.</span></span>
-   <span data-ttu-id="7ecd6-116">删除离群值。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-116">Remove outliers.</span></span>
-   <span data-ttu-id="7ecd6-117">创建预测准确性的度量。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-117">Create measurements of forecast accuracy.</span></span>

## <a name="major-themes-in-demand-forecasting"></a><span data-ttu-id="7ecd6-118">需求预测的主要主题</span><span class="sxs-lookup"><span data-stu-id="7ecd6-118">Major themes in demand forecasting</span></span>
<span data-ttu-id="7ecd6-119">三个主要主题在需求预测中实施：</span><span class="sxs-lookup"><span data-stu-id="7ecd6-119">Three major themes are implemented in demand forecasting:</span></span>

-   <span data-ttu-id="7ecd6-120">**模块性** – 需求预测是模块化的和易于配置。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-120">**Modularity** – Demand forecasting is modular and easy to configure.</span></span> <span data-ttu-id="7ecd6-121">您可以通过在**贸易** &gt; **库存预测** &gt; **需求预测**更改 Configuration Key 来打开和关闭功能。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-121">You can turn the functionality on and off by changing the configuration key at **Trade** &gt; **Inventory forecast** &gt; **Demand forecasting**.</span></span>
-   <span data-ttu-id="7ecd6-122">**Microsoft 堆栈的重用** – Microsoft 在 2015 年 2 月启动机器学习平台。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-122">**Reuse of the Microsoft stack** – Microsoft launched the Machine Learning platform in February 2015.</span></span> <span data-ttu-id="7ecd6-123">机器学习现在是 Microsoft Cortana 分析套件的一部分，让您可以通过使用算法 R 或 Python 编程语言和简单的拖放界面来迅速轻松地创建预测性分析实验，如需求估计实验。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-123">Machine Learning, which is now part of the Microsoft Cortana Analytics Suite, lets you quickly and easily create predictive analysis experiments, such as demand estimation experiments, by using algorithms R or Python programming languages and a simple drag-and-drop interface.</span></span>
    -   <span data-ttu-id="7ecd6-124">您可以下载 Finance and Operations 需求预测实验，更改它们以满足您的业务要求，在 Azure 上作为 Web 服务发布它们，并使用它们生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-124">You can download the Finance and Operations Demand forecasting experiments, change them to meet your business requirements, publish them as a web service on Azure, and use them to generate demand forecasts.</span></span> <span data-ttu-id="7ecd6-125">如果您作为企业级用户购买了生产规划员的 Finance and Operations 订阅，则可以下载这些实验。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-125">The experiments are available for download if you've purchased a Finance and Operations subscription for a production planner as enterprise level user.</span></span>
    -   <span data-ttu-id="7ecd6-126">您可以从 [Cortana 分析库](https://gallery.cortanaanalytics.com/)下载当前可用的任何需求预测实验。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-126">You can download any of the currently available demand prediction experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="7ecd6-127">而 Finance and Operations 需求预测实验将自动与 Finance and Operations 集成，客户和合作伙伴必须处理从 [Cortana 分析库](https://gallery.cortanaanalytics.com/) 下载的实验的集成。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-127">Whereas the Finance and Operations Demand forecasting experiments are automatically integrated with Finance and Operations, customers and partners must handle the integration of experiments that they download from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="7ecd6-128">因此，[Cortana 分析库](https://gallery.cortanaanalytics.com/) 的实验不如使用 Finance and Operations 需求预测实验那样简单。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-128">Therefore, experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) aren't as straightforward to use as the Finance and Operations Demand forecasting experiments.</span></span> <span data-ttu-id="7ecd6-129">您必须修改实验代码，以便它们使用 Finance and Operations 应用程序编程接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-129">You must modify the code of the experiments so that they use the Finance and Operations application programming interface (API).</span></span>
    -   <span data-ttu-id="7ecd6-130">您可以在 Microsoft Azure 机器学习工作室中创建自己的实验，在 Azure 上作为服务发布，并使用它们生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-130">You can create your own experiments in Microsoft Azure Machine Learning Studio, publish them as services on Azure, and use them to generate demand forecasts.</span></span>
    -   <span data-ttu-id="7ecd6-131">如果您不需要高性能，或者，如果您不需要处理大量数据，您可以使用机器学习的免费层。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-131">If you don’t require high performance, or if you don't require that a large amount of data be processed, you can use the Machine Learning free tier.</span></span> <span data-ttu-id="7ecd6-132">我们建议始终从这一层开始，尤其是在实施和测试阶段。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-132">We recommend that you always start from this tier, especially during implementation and testing phases.</span></span> <span data-ttu-id="7ecd6-133">如果您需要高性能和额外存储，您可以使用机器学习的标准层。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-133">If you require higher performance and additional storage, you can use the Machine Learning standard tier.</span></span> <span data-ttu-id="7ecd6-134">这一层要求 Azure 订阅并需要其他成本。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-134">This tier requires an Azure subscription and involves additional costs.</span></span> <span data-ttu-id="7ecd6-135">有关机器学习定价的详细信息，请参阅 <http://aka.ms/machine-learning-price-info>。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-135">For details about Machine Learning pricing, see <http://aka.ms/machine-learning-price-info>.</span></span>
-   <span data-ttu-id="7ecd6-136">**在任何解耦点的预测缩减** – Finance and Operations 中的需求预测构建此功能，让您可以在任何解耦点预测相关和不相关的需求。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-136">**Forecast reduction at any decoupling point** – Demand forecasting in Finance and Operations builds on this functionality, which lets you forecast both dependent and independent demand at any decoupling point.</span></span>

## <a name="basic-flow-in-demand-forecasting"></a><span data-ttu-id="7ecd6-137">需求预测的基本流程</span><span class="sxs-lookup"><span data-stu-id="7ecd6-137">Basic flow in demand forecasting</span></span>
<span data-ttu-id="7ecd6-138">下图显示需求预测的基本流程。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-138">The following diagram shows the basic flow in demand forecasting.</span></span> 

<span data-ttu-id="7ecd6-139">[![需求预测介绍图](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="7ecd6-139">[![demand forecasting introduction diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span></span>

<span data-ttu-id="7ecd6-140">需求预测生成在 Finance and Operations 中开始。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-140">Demand forecast generation starts in Finance and Operations.</span></span> <span data-ttu-id="7ecd6-141">收集 Finance and Operations 交易记录数据库的历史交易记录数据并填写暂存表。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-141">Historical transactional data from the Finance and Operations transactional database is gathered and populates a staging table.</span></span> <span data-ttu-id="7ecd6-142">此暂存表随后提供给机器学习服务。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-142">This staging table is later fed to a Machine Learning service.</span></span> <span data-ttu-id="7ecd6-143">通过执行最小的自定义设置，可以将各个数据源插入到暂存表。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-143">By performing minimal customization, you can plug various data sources into the staging table.</span></span> <span data-ttu-id="7ecd6-144">数据源可以包括 Microsoft Excel 文件、逗号分隔值 (CSV) 文件和 Microsoft Dynamics AX 2009 和 Microsoft Dynamics AX 2012 的数据。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-144">The data sources can include Microsoft Excel files, comma-separated value (CSV) files, and data from Microsoft Dynamics AX 2009 and Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="7ecd6-145">因此，可以生成考虑在多个系统中分散的历史数据的需求预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-145">Therefore, you can generate demand forecasts that consider historical data that is spread among multiple systems.</span></span> <span data-ttu-id="7ecd6-146">但是，主数据，例如物料名称和度量单位，在各个数据源中必须是相同的。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-146">However, the master data, such as item names and units of measure, must be the same across the various data sources.</span></span>

<span data-ttu-id="7ecd6-147">如果您使用 Finance and Operations 需求预测机器学习实验，它们在五个时间系列预测法中寻找最适合的方法来计算基准预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-147">If you use the Finance and Operations Demand forecasting Machine Learning experiments, they look for a best fit among five time series forecasting methods to calculate a baseline forecast.</span></span> <span data-ttu-id="7ecd6-148">这些预测方法的参数在 Finance and Operations 中管理。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-148">The parameters for these forecasting methods are managed in Finance and Operations.</span></span> 

<span data-ttu-id="7ecd6-149">预测、历史数据和对之前迭代的需求预测进行的任何更改然后在 Finance and Operations 中可用。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-149">The forecasts, historical data, and any changes that were made to the demand forecasts in previous iterations are then available in Finance and Operations.</span></span> 

<span data-ttu-id="7ecd6-150">您可以使用 Finance and Operations 来可视化和修改基准预测。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-150">You can use Finance and Operations to visualize and modify the baseline forecasts.</span></span> <span data-ttu-id="7ecd6-151">手动调整必须授权，然后预测才能用于计划。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-151">Manual adjustments must be authorized before the forecasts can be used for planning.</span></span>

## <a name="limitations"></a><span data-ttu-id="7ecd6-152">限制</span><span class="sxs-lookup"><span data-stu-id="7ecd6-152">Limitations</span></span>
<span data-ttu-id="7ecd6-153">Finance and Operations 中的需求预测是帮助制造行业客户创建预测流程的工具。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-153">Demand forecasting in Finance and Operations is a tool that helps customers in the manufacturing industry create forecasting processes.</span></span> <span data-ttu-id="7ecd6-154">它提供了需求预测解决方案的核心功能，并设计为可以轻松扩展。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-154">It offers the core functionality of a demand forecasting solution and is designed so that it can easily be extended.</span></span> <span data-ttu-id="7ecd6-155">需求预测可能对零售、批发、仓库、运输或其他专业服务等行业的客户不是最合适。</span><span class="sxs-lookup"><span data-stu-id="7ecd6-155">Demand forecasting might not be the best fit for customers in industries such as retail, wholesale, warehousing, transportation, or other professional services.</span></span>

<a name="see-also"></a><span data-ttu-id="7ecd6-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="7ecd6-156">See also</span></span>
--------

[<span data-ttu-id="7ecd6-157">需求预测设置</span><span class="sxs-lookup"><span data-stu-id="7ecd6-157">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

[<span data-ttu-id="7ecd6-158">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="7ecd6-158">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

[<span data-ttu-id="7ecd6-159">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="7ecd6-159">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="7ecd6-160">授权调整后的需求预测</span><span class="sxs-lookup"><span data-stu-id="7ecd6-160">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="7ecd6-161">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="7ecd6-161">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="7ecd6-162">在计算需求预测时，需从历史交易记录数据中删除离群值</span><span class="sxs-lookup"><span data-stu-id="7ecd6-162">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



