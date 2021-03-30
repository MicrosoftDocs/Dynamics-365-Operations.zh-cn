---
title: 需求预测概览
description: 需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。 增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。
author: roxanadiaconu
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b285b973f0fee3b253f63f49e3f5b4893d9dd86
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207031"
---
# <a name="demand-forecasting-overview"></a><span data-ttu-id="b016b-104">需求预测概览</span><span class="sxs-lookup"><span data-stu-id="b016b-104">Demand forecasting overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b016b-105">需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。</span><span class="sxs-lookup"><span data-stu-id="b016b-105">Demand forecasting is used to predict independent demand from sales orders and dependent demand at any decoupling point for customer orders.</span></span> <span data-ttu-id="b016b-106">增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。</span><span class="sxs-lookup"><span data-stu-id="b016b-106">The enhanced demand forecast reduction rules provide an ideal solution for mass customization.</span></span>

<span data-ttu-id="b016b-107">若要生成基准预测，历史交易记录汇总被传递到在 Azure 上承载的 Microsoft Azure 机器学习。</span><span class="sxs-lookup"><span data-stu-id="b016b-107">To generate the baseline forecast, a summary of historical transactions is passed to Microsoft Azure Machine Learning hosted on Azure.</span></span> <span data-ttu-id="b016b-108">由于此服务不在用户之间共享，其可以轻松地自定义以满足特定于行业的要求。</span><span class="sxs-lookup"><span data-stu-id="b016b-108">Because this service isn't shared among users, it can easily be customized to meet industry-specific requirements.</span></span> <span data-ttu-id="b016b-109">您可以使用 Supply Chain Management 可视化预测、调整预测和查看有关预测准确性的关键绩效指标 (KPI)。</span><span class="sxs-lookup"><span data-stu-id="b016b-109">You can use Supply Chain Management to visualize the forecast, adjust the forecast, and view key performance indicators (KPIs) about forecast accuracy.</span></span>

> [!NOTE]
> <span data-ttu-id="b016b-110">使用机器学习进行预测生成需要 Microsoft Azure 机器学习工作室（经典）。</span><span class="sxs-lookup"><span data-stu-id="b016b-110">Microsoft Azure Machine Learning Studio (classic) is required for forecast generation with machine learning.</span></span> <span data-ttu-id="b016b-111">自 2021 年 1 月起，它在日本东部、美国中南部、东南亚、美国中西部和西欧推出。</span><span class="sxs-lookup"><span data-stu-id="b016b-111">As of January 2021, it is available in Japan East, South Central US, Southeast Asia, West Central US, and West Europe.</span></span> <span data-ttu-id="b016b-112">有关当前可用性的更新信息，请参阅[按地区划分的 Azure 产品](https://azure.microsoft.com/global-infrastructure/services/?regions=all&products=machine-learning-studio)</span><span class="sxs-lookup"><span data-stu-id="b016b-112">For updated information about current availability, see [Azure Products by Region.](https://azure.microsoft.com/global-infrastructure/services/?regions=all&products=machine-learning-studio)</span></span>

## <a name="key-features-of-demand-forecasting"></a><span data-ttu-id="b016b-113">需求预测的主要功能</span><span class="sxs-lookup"><span data-stu-id="b016b-113">Key features of demand forecasting</span></span>

<span data-ttu-id="b016b-114">以下是需求预测的一些主要功能：</span><span class="sxs-lookup"><span data-stu-id="b016b-114">Here are some of the main features of demand forecasting:</span></span>

- <span data-ttu-id="b016b-115">生成基于历史数据的统计基准预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-115">Generate a statistical baseline forecast that is based on historical data.</span></span>
- <span data-ttu-id="b016b-116">使用一组动态的预测维度。</span><span class="sxs-lookup"><span data-stu-id="b016b-116">Use a dynamic set of forecast dimensions.</span></span>
- <span data-ttu-id="b016b-117">可视化需求趋势、置信区间和预测调整。</span><span class="sxs-lookup"><span data-stu-id="b016b-117">Visualize demand trends, confidence intervals, and adjustments of the forecast.</span></span>
- <span data-ttu-id="b016b-118">授权在计划流程中使用的已调整预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-118">Authorize the adjusted forecast to be used in planning processes.</span></span>
- <span data-ttu-id="b016b-119">删除离群值。</span><span class="sxs-lookup"><span data-stu-id="b016b-119">Remove outliers.</span></span>
- <span data-ttu-id="b016b-120">创建预测准确性的度量。</span><span class="sxs-lookup"><span data-stu-id="b016b-120">Create measurements of forecast accuracy.</span></span>

## <a name="major-themes-in-demand-forecasting"></a><span data-ttu-id="b016b-121">需求预测的主要主题</span><span class="sxs-lookup"><span data-stu-id="b016b-121">Major themes in demand forecasting</span></span>

<span data-ttu-id="b016b-122">三个主要主题在需求预测中实施：</span><span class="sxs-lookup"><span data-stu-id="b016b-122">Three major themes are implemented in demand forecasting:</span></span>

- <span data-ttu-id="b016b-123">**模块性** – 需求预测是模块化的和易于配置。</span><span class="sxs-lookup"><span data-stu-id="b016b-123">**Modularity** – Demand forecasting is modular and easy to configure.</span></span> <span data-ttu-id="b016b-124">您可以通过在 **贸易** &gt; **库存预测** &gt; **需求预测** 更改 Configuration Key 来打开和关闭功能。</span><span class="sxs-lookup"><span data-stu-id="b016b-124">You can turn the functionality on and off by changing the configuration key at **Trade** &gt; **Inventory forecast** &gt; **Demand forecasting**.</span></span>
- <span data-ttu-id="b016b-125">**Microsoft Stack 的重用** – 机器学习是 Microsoft Cortana 分析套件的一部分，让您可以通过使用算法 R 或 Python 编程语言和简单的拖放界面来迅速轻松地创建预测性分析实验，如需求估计实验。</span><span class="sxs-lookup"><span data-stu-id="b016b-125">**Reuse of the Microsoft stack** – Machine Learning, which is part of the Microsoft Cortana Analytics Suite, lets you quickly and easily create predictive analysis experiments, such as demand estimation experiments, by using algorithms R or Python programming languages and a simple drag-and-drop interface.</span></span>
  - <span data-ttu-id="b016b-126">您可以下载需求预测实验，更改它们以满足您的业务要求，在 Azure 上作为 Web 服务发布它们，并使用它们生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-126">You can download the Demand forecasting experiments, change them to meet your business requirements, publish them as a web service on Azure, and use them to generate demand forecasts.</span></span> <span data-ttu-id="b016b-127">如果您作为企业级用户购买了生产规划员的 Supply Chain Management 订阅，则可以下载这些实验。</span><span class="sxs-lookup"><span data-stu-id="b016b-127">The experiments are available for download if you've purchased a Supply Chain Management subscription for a production planner as enterprise-level user.</span></span>
  - <span data-ttu-id="b016b-128">您可以从 [Cortana 分析库](https://gallery.cortanaanalytics.com/)下载当前可用的任何需求预测实验。</span><span class="sxs-lookup"><span data-stu-id="b016b-128">You can download any of the currently available demand prediction experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="b016b-129">而需求预测实验将自动与 Supply Chain Management 集成，客户和合作伙伴必须处理从 [Cortana 分析库](https://gallery.cortanaanalytics.com/) 下载的实验的集成。</span><span class="sxs-lookup"><span data-stu-id="b016b-129">Whereas the Demand forecasting experiments are automatically integrated with Supply Chain Management, customers and partners must handle the integration of experiments that they download from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="b016b-130">因此，[Cortana 分析库](https://gallery.cortanaanalytics.com/)的实验不如使用 Finance and Operations 需求预测实验那样简单。</span><span class="sxs-lookup"><span data-stu-id="b016b-130">Therefore, experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) aren't as straightforward to use as the Finance and Operations Demand forecasting experiments.</span></span> <span data-ttu-id="b016b-131">您必须修改实验代码，以便它们使用 Finance and Operations 应用程序编程接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="b016b-131">You must modify the code of the experiments so that they use the Finance and Operations application programming interface (API).</span></span>
  - <span data-ttu-id="b016b-132">您可以在 Microsoft Azure 机器学习工作室（经典）中创建自己的实验，在 Azure 上作为服务发布，并使用它们生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-132">You can create your own experiments in Microsoft Azure Machine Learning Studio (classic), publish them as services on Azure, and use them to generate demand forecasts.</span></span>
  - <span data-ttu-id="b016b-133">如果您不需要高性能，或者，如果您不需要处理大量数据，您可以使用机器学习的免费层。</span><span class="sxs-lookup"><span data-stu-id="b016b-133">If you don’t require high performance, or if you don't require that a large amount of data be processed, you can use the Machine Learning free tier.</span></span> <span data-ttu-id="b016b-134">我们建议始终从这一层开始，尤其是在实施和测试阶段。</span><span class="sxs-lookup"><span data-stu-id="b016b-134">We recommend that you always start from this tier, especially during implementation and testing phases.</span></span> <span data-ttu-id="b016b-135">如果您需要高性能和额外存储，您可以使用机器学习的标准层。</span><span class="sxs-lookup"><span data-stu-id="b016b-135">If you require higher performance and additional storage, you can use the Machine Learning standard tier.</span></span> <span data-ttu-id="b016b-136">这一层要求 Azure 订阅并需要其他成本。</span><span class="sxs-lookup"><span data-stu-id="b016b-136">This tier requires an Azure subscription and involves additional costs.</span></span> <span data-ttu-id="b016b-137">有关机器学习定价的详细信息，请参阅[机器学习工作室定价](https://aka.ms/machine-learning-price-info)。</span><span class="sxs-lookup"><span data-stu-id="b016b-137">For details about Machine Learning pricing, see [Machine Learning Studio pricing](https://aka.ms/machine-learning-price-info).</span></span>
- <span data-ttu-id="b016b-138">**在任何解耦点的预测缩减** – 生成中的需求预测构建此功能，让您可以在任何解耦点预测相关和不相关的需求。</span><span class="sxs-lookup"><span data-stu-id="b016b-138">**Forecast reduction at any decoupling point** – Demand forecasting in builds on this functionality, which lets you forecast both dependent and independent demand at any decoupling point.</span></span>

## <a name="basic-flow-in-demand-forecasting"></a><span data-ttu-id="b016b-139">需求预测的基本流程</span><span class="sxs-lookup"><span data-stu-id="b016b-139">Basic flow in demand forecasting</span></span>

<span data-ttu-id="b016b-140">下图显示需求预测的基本流程。</span><span class="sxs-lookup"><span data-stu-id="b016b-140">The following diagram shows the basic flow in demand forecasting.</span></span>

<span data-ttu-id="b016b-141">[![需求预测介绍图](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="b016b-141">[![demand forecasting introduction diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span></span>

<span data-ttu-id="b016b-142">需求预测在 Supply Chain Management 中开始生成。</span><span class="sxs-lookup"><span data-stu-id="b016b-142">Demand forecast generation starts in Supply Chain Management.</span></span> <span data-ttu-id="b016b-143">收集 Supply Chain Management 交易记录数据库的历史交易记录数据并填写暂存表。</span><span class="sxs-lookup"><span data-stu-id="b016b-143">Historical transactional data from the Supply Chain Management transactional database is gathered and populates a staging table.</span></span> <span data-ttu-id="b016b-144">此暂存表随后提供给机器学习服务。</span><span class="sxs-lookup"><span data-stu-id="b016b-144">This staging table is later fed to a Machine Learning service.</span></span> <span data-ttu-id="b016b-145">通过执行最小的自定义设置，可以将各个数据源插入到暂存表。</span><span class="sxs-lookup"><span data-stu-id="b016b-145">By performing minimal customization, you can plug various data sources into the staging table.</span></span> <span data-ttu-id="b016b-146">数据源可以包括 Microsoft Excel 文件、逗号分隔值 (CSV) 文件和 Microsoft Dynamics AX 2009 和 Microsoft Dynamics AX 2012 的数据。</span><span class="sxs-lookup"><span data-stu-id="b016b-146">The data sources can include Microsoft Excel files, comma-separated value (CSV) files, and data from Microsoft Dynamics AX 2009 and Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="b016b-147">因此，可以生成考虑在多个系统中分散的历史数据的需求预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-147">Therefore, you can generate demand forecasts that consider historical data that is spread among multiple systems.</span></span> <span data-ttu-id="b016b-148">但是，主数据，例如物料名称和度量单位，在各个数据源中必须是相同的。</span><span class="sxs-lookup"><span data-stu-id="b016b-148">However, the master data, such as item names and units of measure, must be the same across the various data sources.</span></span>

<span data-ttu-id="b016b-149">如果您使用需求预测机器学习实验，它们在五个时间系列预测法中寻找最适合的方法来计算基准预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-149">If you use the Demand forecasting Machine Learning experiments, they look for a best fit among five time series forecasting methods to calculate a baseline forecast.</span></span> <span data-ttu-id="b016b-150">这些预测方法的参数在 Supply Chain Management 中管理。</span><span class="sxs-lookup"><span data-stu-id="b016b-150">The parameters for these forecasting methods are managed in Supply Chain Management.</span></span>

<span data-ttu-id="b016b-151">预测、历史数据和对之前迭代的需求预测进行的任何更改然后在 Supply Chain Management 中可用。</span><span class="sxs-lookup"><span data-stu-id="b016b-151">The forecasts, historical data, and any changes that were made to the demand forecasts in previous iterations are then available in Supply Chain Management.</span></span>

<span data-ttu-id="b016b-152">您可以使用 Supply Chain Management 来可视化和修改基准预测。</span><span class="sxs-lookup"><span data-stu-id="b016b-152">You can use Supply Chain Management to visualize and modify the baseline forecasts.</span></span> <span data-ttu-id="b016b-153">手动调整必须授权，然后预测才能用于计划。</span><span class="sxs-lookup"><span data-stu-id="b016b-153">Manual adjustments must be authorized before the forecasts can be used for planning.</span></span>

## <a name="limitations"></a><span data-ttu-id="b016b-154">限制</span><span class="sxs-lookup"><span data-stu-id="b016b-154">Limitations</span></span>

<span data-ttu-id="b016b-155">需求预测是帮助制造行业客户创建预测流程的工具。</span><span class="sxs-lookup"><span data-stu-id="b016b-155">Demand forecasting is a tool that helps customers in the manufacturing industry create forecasting processes.</span></span> <span data-ttu-id="b016b-156">它提供了需求预测解决方案的核心功能，并设计为可以轻松扩展。</span><span class="sxs-lookup"><span data-stu-id="b016b-156">It offers the core functionality of a demand forecasting solution and is designed so that it can easily be extended.</span></span> <span data-ttu-id="b016b-157">需求预测可能对商业、批发、仓库、运输或其他专业服务等行业的客户不是最合适。</span><span class="sxs-lookup"><span data-stu-id="b016b-157">Demand forecasting might not be the best fit for customers in industries such as commerce, wholesale, warehousing, transportation, or other professional services.</span></span>

### <a name="demand-forecast-variant-conversion-limitation"></a><span data-ttu-id="b016b-158">需求预测变型转换限制</span><span class="sxs-lookup"><span data-stu-id="b016b-158">Demand forecast variant conversion limitation</span></span>

<span data-ttu-id="b016b-159">如果库存 UOM 与需求预测 UOM 不同，在生成需求预测时将不完全支持每个变型转换的计量单位 (UOM)。</span><span class="sxs-lookup"><span data-stu-id="b016b-159">Unit of measure (UOM) per variant conversion is not fully supported when generating demand forecast if inventory UOM is different than the demand forecast UOM.</span></span>

<span data-ttu-id="b016b-160">生成预测（**库存 UOM > 需求预测 UOM**）使用产品 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b016b-160">Generating forecast (**Inventory UOM > Demand forecast UOM**) uses product UOM conversion.</span></span> <span data-ttu-id="b016b-161">在为需求预测生成加载历史数据时，即使在变型级别定义了转换，从库存 UOM 转换为需求预测 UOM 时也将始终使用产品级别 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b016b-161">When loading historical data for the demand forecast generation, the product level UOM conversion will be always used when converting from inventory UOM to the demand forecast UOM, even if there are conversions defined on the variant level.</span></span>

<span data-ttu-id="b016b-162">授权预测的第一部分（**需求预测 UOM > 库存 UOM**）使用产品 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b016b-162">The first part of authorizing forecast (**Demand forecast UOM > Inventory UOM**) uses product UOM conversion.</span></span> <span data-ttu-id="b016b-163">授权预测的第二部分（**库存 UOM > 销售 UOM**）使用变型 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b016b-163">The second part of authorizing forecast (**Inventory UOM > Sales UOM**) uses the variant UOM conversion.</span></span> <span data-ttu-id="b016b-164">授权所生成的需求预测后，将使用产品级别的 UOM 转换完成从需求预测 UOM 到库存 UOM 的转换。</span><span class="sxs-lookup"><span data-stu-id="b016b-164">When the generated demand forecast is authorized, the conversion to inventory UOM from demand forecast UOM will be done using product level UOM conversion.</span></span> <span data-ttu-id="b016b-165">同时，库存单位和销售 UOM 之间的转换将遵循变型级别定义的转换。</span><span class="sxs-lookup"><span data-stu-id="b016b-165">At the same time, conversion between the inventory unit and the sales UOM will respect the variant level defined conversions.</span></span>

<span data-ttu-id="b016b-166">请注意，需求预测 UOM 不必具有任何特定含义。</span><span class="sxs-lookup"><span data-stu-id="b016b-166">Note that the demand forecast UOM does not have to have any specific meaning.</span></span> <span data-ttu-id="b016b-167">它可以定义为“需求预测单位”。</span><span class="sxs-lookup"><span data-stu-id="b016b-167">It can be defined as “Demand forecast unit”.</span></span> <span data-ttu-id="b016b-168">对于每个产品，您可以使用库存 UOM 将转换定义为 1:1。</span><span class="sxs-lookup"><span data-stu-id="b016b-168">For each of the products, you can define the conversion to be 1:1 with the inventory UOM.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b016b-169">其他资源</span><span class="sxs-lookup"><span data-stu-id="b016b-169">Additional resources</span></span>

[<span data-ttu-id="b016b-170">需求预测设置</span><span class="sxs-lookup"><span data-stu-id="b016b-170">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

[<span data-ttu-id="b016b-171">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="b016b-171">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

[<span data-ttu-id="b016b-172">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="b016b-172">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="b016b-173">授权调整后的预测</span><span class="sxs-lookup"><span data-stu-id="b016b-173">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b016b-174">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="b016b-174">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="b016b-175">在计算需求预测时，需从历史交易记录数据中删除离群值</span><span class="sxs-lookup"><span data-stu-id="b016b-175">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)

[<span data-ttu-id="b016b-176">扩展需求预测功能</span><span class="sxs-lookup"><span data-stu-id="b016b-176">Extend the demand forecasting functionality</span></span>](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]