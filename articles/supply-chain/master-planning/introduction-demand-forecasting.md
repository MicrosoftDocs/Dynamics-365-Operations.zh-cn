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
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62ee31b7931c6e7d8f54c1efb556a2ba01eb7746
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981442"
---
# <a name="demand-forecasting-overview"></a><span data-ttu-id="b9311-104">需求预测概览</span><span class="sxs-lookup"><span data-stu-id="b9311-104">Demand forecasting overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9311-105">需求预测用于从销售订单预测无关需求并从客户订单的任何解耦点预测相关需求。</span><span class="sxs-lookup"><span data-stu-id="b9311-105">Demand forecasting is used to predict independent demand from sales orders and dependent demand at any decoupling point for customer orders.</span></span> <span data-ttu-id="b9311-106">增强型需求预测缩减规则为批量自定义提供了一个理想的解决方案。</span><span class="sxs-lookup"><span data-stu-id="b9311-106">The enhanced demand forecast reduction rules provide an ideal solution for mass customization.</span></span>

<span data-ttu-id="b9311-107">若要生成基准预测，历史交易记录汇总被传递到在 Azure 上承载的 Microsoft Azure 机器学习。</span><span class="sxs-lookup"><span data-stu-id="b9311-107">To generate the baseline forecast, a summary of historical transactions is passed to Microsoft Azure Machine Learning hosted on Azure.</span></span> <span data-ttu-id="b9311-108">由于此服务不在用户之间共享，其可以轻松地自定义以满足特定于行业的要求。</span><span class="sxs-lookup"><span data-stu-id="b9311-108">Because this service isn't shared among users, it can easily be customized to meet industry-specific requirements.</span></span> <span data-ttu-id="b9311-109">您可以使用 Supply Chain Management 可视化预测、调整预测和查看有关预测准确性的关键绩效指标 (KPI)。</span><span class="sxs-lookup"><span data-stu-id="b9311-109">You can use Supply Chain Management to visualize the forecast, adjust the forecast, and view key performance indicators (KPIs) about forecast accuracy.</span></span>

## <a name="key-features-of-demand-forecasting"></a><span data-ttu-id="b9311-110">需求预测的主要功能</span><span class="sxs-lookup"><span data-stu-id="b9311-110">Key features of demand forecasting</span></span>
<span data-ttu-id="b9311-111">以下是需求预测的一些主要功能：</span><span class="sxs-lookup"><span data-stu-id="b9311-111">Here are some of the main features of demand forecasting:</span></span>

-   <span data-ttu-id="b9311-112">生成基于历史数据的统计基准预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-112">Generate a statistical baseline forecast that is based on historical data.</span></span>
-   <span data-ttu-id="b9311-113">使用一组动态的预测维度。</span><span class="sxs-lookup"><span data-stu-id="b9311-113">Use a dynamic set of forecast dimensions.</span></span>
-   <span data-ttu-id="b9311-114">可视化需求趋势、置信区间和预测调整。</span><span class="sxs-lookup"><span data-stu-id="b9311-114">Visualize demand trends, confidence intervals, and adjustments of the forecast.</span></span>
-   <span data-ttu-id="b9311-115">授权在计划流程中使用的已调整预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-115">Authorize the adjusted forecast to be used in planning processes.</span></span>
-   <span data-ttu-id="b9311-116">删除离群值。</span><span class="sxs-lookup"><span data-stu-id="b9311-116">Remove outliers.</span></span>
-   <span data-ttu-id="b9311-117">创建预测准确性的度量。</span><span class="sxs-lookup"><span data-stu-id="b9311-117">Create measurements of forecast accuracy.</span></span>

## <a name="major-themes-in-demand-forecasting"></a><span data-ttu-id="b9311-118">需求预测的主要主题</span><span class="sxs-lookup"><span data-stu-id="b9311-118">Major themes in demand forecasting</span></span>
<span data-ttu-id="b9311-119">三个主要主题在需求预测中实施：</span><span class="sxs-lookup"><span data-stu-id="b9311-119">Three major themes are implemented in demand forecasting:</span></span>

-   <span data-ttu-id="b9311-120">**模块性** – 需求预测是模块化的和易于配置。</span><span class="sxs-lookup"><span data-stu-id="b9311-120">**Modularity** – Demand forecasting is modular and easy to configure.</span></span> <span data-ttu-id="b9311-121">您可以通过在**贸易** &gt; **库存预测** &gt; **需求预测**更改 Configuration Key 来打开和关闭功能。</span><span class="sxs-lookup"><span data-stu-id="b9311-121">You can turn the functionality on and off by changing the configuration key at **Trade** &gt; **Inventory forecast** &gt; **Demand forecasting**.</span></span>
-   <span data-ttu-id="b9311-122">**Microsoft Stack 的重用** – 机器学习是 Microsoft Cortana 分析套件的一部分，让您可以通过使用算法 R 或 Python 编程语言和简单的拖放界面来迅速轻松地创建预测性分析实验，如需求估计实验。</span><span class="sxs-lookup"><span data-stu-id="b9311-122">**Reuse of the Microsoft stack** – Machine Learning, which is part of the Microsoft Cortana Analytics Suite, lets you quickly and easily create predictive analysis experiments, such as demand estimation experiments, by using algorithms R or Python programming languages and a simple drag-and-drop interface.</span></span>
    -   <span data-ttu-id="b9311-123">您可以下载需求预测实验，更改它们以满足您的业务要求，在 Azure 上作为 Web 服务发布它们，并使用它们生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-123">You can download the Demand forecasting experiments, change them to meet your business requirements, publish them as a web service on Azure, and use them to generate demand forecasts.</span></span> <span data-ttu-id="b9311-124">如果您作为企业级用户购买了生产规划员的 Supply Chain Management 订阅，则可以下载这些实验。</span><span class="sxs-lookup"><span data-stu-id="b9311-124">The experiments are available for download if you've purchased a Supply Chain Management subscription for a production planner as enterprise level user.</span></span>
    -   <span data-ttu-id="b9311-125">您可以从 [Cortana 分析库](https://gallery.cortanaanalytics.com/)下载当前可用的任何需求预测实验。</span><span class="sxs-lookup"><span data-stu-id="b9311-125">You can download any of the currently available demand prediction experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="b9311-126">而需求预测实验将自动与 Supply Chain Management 集成，客户和合作伙伴必须处理从 [Cortana 分析库](https://gallery.cortanaanalytics.com/) 下载的实验的集成。</span><span class="sxs-lookup"><span data-stu-id="b9311-126">Whereas the Demand forecasting experiments are automatically integrated with Supply Chain Management, customers and partners must handle the integration of experiments that they download from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="b9311-127">因此，[Cortana 分析库](https://gallery.cortanaanalytics.com/)的实验不如使用 Finance and Operations 需求预测实验那样简单。</span><span class="sxs-lookup"><span data-stu-id="b9311-127">Therefore, experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) aren't as straightforward to use as the Finance and Operations Demand forecasting experiments.</span></span> <span data-ttu-id="b9311-128">您必须修改实验代码，以便它们使用 Finance and Operations 应用程序编程接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="b9311-128">You must modify the code of the experiments so that they use the Finance and Operations application programming interface (API).</span></span>
    -   <span data-ttu-id="b9311-129">您可以在 Microsoft Azure 机器学习工作室（经典）中创建自己的实验，在 Azure 上作为服务发布，并使用它们生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-129">You can create your own experiments in Microsoft Azure Machine Learning Studio (classic), publish them as services on Azure, and use them to generate demand forecasts.</span></span>
    -   <span data-ttu-id="b9311-130">如果您不需要高性能，或者，如果您不需要处理大量数据，您可以使用机器学习的免费层。</span><span class="sxs-lookup"><span data-stu-id="b9311-130">If you don’t require high performance, or if you don't require that a large amount of data be processed, you can use the Machine Learning free tier.</span></span> <span data-ttu-id="b9311-131">我们建议始终从这一层开始，尤其是在实施和测试阶段。</span><span class="sxs-lookup"><span data-stu-id="b9311-131">We recommend that you always start from this tier, especially during implementation and testing phases.</span></span> <span data-ttu-id="b9311-132">如果您需要高性能和额外存储，您可以使用机器学习的标准层。</span><span class="sxs-lookup"><span data-stu-id="b9311-132">If you require higher performance and additional storage, you can use the Machine Learning standard tier.</span></span> <span data-ttu-id="b9311-133">这一层要求 Azure 订阅并需要其他成本。</span><span class="sxs-lookup"><span data-stu-id="b9311-133">This tier requires an Azure subscription and involves additional costs.</span></span> <span data-ttu-id="b9311-134">有关机器学习定价的详细信息，请参阅[机器学习工作室定价](https://aka.ms/machine-learning-price-info)。</span><span class="sxs-lookup"><span data-stu-id="b9311-134">For details about Machine Learning pricing, see [Machine Learning Studio pricing](https://aka.ms/machine-learning-price-info).</span></span>
-   <span data-ttu-id="b9311-135">**在任何解耦点的预测缩减** – 生成中的需求预测构建此功能，让您可以在任何解耦点预测相关和不相关的需求。</span><span class="sxs-lookup"><span data-stu-id="b9311-135">**Forecast reduction at any decoupling point** – Demand forecasting in builds on this functionality, which lets you forecast both dependent and independent demand at any decoupling point.</span></span>

## <a name="basic-flow-in-demand-forecasting"></a><span data-ttu-id="b9311-136">需求预测的基本流程</span><span class="sxs-lookup"><span data-stu-id="b9311-136">Basic flow in demand forecasting</span></span>
<span data-ttu-id="b9311-137">下图显示需求预测的基本流程。</span><span class="sxs-lookup"><span data-stu-id="b9311-137">The following diagram shows the basic flow in demand forecasting.</span></span> 

<span data-ttu-id="b9311-138">[![需求预测介绍图](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="b9311-138">[![demand forecasting introduction diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span></span>

<span data-ttu-id="b9311-139">需求预测在 Supply Chain Management 中开始生成。</span><span class="sxs-lookup"><span data-stu-id="b9311-139">Demand forecast generation starts in Supply Chain Management.</span></span> <span data-ttu-id="b9311-140">收集 Supply Chain Management 交易记录数据库的历史交易记录数据并填写暂存表。</span><span class="sxs-lookup"><span data-stu-id="b9311-140">Historical transactional data from the Supply Chain Management transactional database is gathered and populates a staging table.</span></span> <span data-ttu-id="b9311-141">此暂存表随后提供给机器学习服务。</span><span class="sxs-lookup"><span data-stu-id="b9311-141">This staging table is later fed to a Machine Learning service.</span></span> <span data-ttu-id="b9311-142">通过执行最小的自定义设置，可以将各个数据源插入到暂存表。</span><span class="sxs-lookup"><span data-stu-id="b9311-142">By performing minimal customization, you can plug various data sources into the staging table.</span></span> <span data-ttu-id="b9311-143">数据源可以包括 Microsoft Excel 文件、逗号分隔值 (CSV) 文件和 Microsoft Dynamics AX 2009 和 Microsoft Dynamics AX 2012 的数据。</span><span class="sxs-lookup"><span data-stu-id="b9311-143">The data sources can include Microsoft Excel files, comma-separated value (CSV) files, and data from Microsoft Dynamics AX 2009 and Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="b9311-144">因此，可以生成考虑在多个系统中分散的历史数据的需求预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-144">Therefore, you can generate demand forecasts that consider historical data that is spread among multiple systems.</span></span> <span data-ttu-id="b9311-145">但是，主数据，例如物料名称和度量单位，在各个数据源中必须是相同的。</span><span class="sxs-lookup"><span data-stu-id="b9311-145">However, the master data, such as item names and units of measure, must be the same across the various data sources.</span></span>

<span data-ttu-id="b9311-146">如果您使用需求预测机器学习实验，它们在五个时间系列预测法中寻找最适合的方法来计算基准预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-146">If you use the Demand forecasting Machine Learning experiments, they look for a best fit among five time series forecasting methods to calculate a baseline forecast.</span></span> <span data-ttu-id="b9311-147">这些预测方法的参数在 Supply Chain Management 中管理。</span><span class="sxs-lookup"><span data-stu-id="b9311-147">The parameters for these forecasting methods are managed in Supply Chain Management.</span></span> 

<span data-ttu-id="b9311-148">预测、历史数据和对之前迭代的需求预测进行的任何更改然后在 Supply Chain Management 中可用。</span><span class="sxs-lookup"><span data-stu-id="b9311-148">The forecasts, historical data, and any changes that were made to the demand forecasts in previous iterations are then available in Supply Chain Management.</span></span> 

<span data-ttu-id="b9311-149">您可以使用 Supply Chain Management 来可视化和修改基准预测。</span><span class="sxs-lookup"><span data-stu-id="b9311-149">You can use Supply Chain Management to visualize and modify the baseline forecasts.</span></span> <span data-ttu-id="b9311-150">手动调整必须授权，然后预测才能用于计划。</span><span class="sxs-lookup"><span data-stu-id="b9311-150">Manual adjustments must be authorized before the forecasts can be used for planning.</span></span>

## <a name="limitations"></a><span data-ttu-id="b9311-151">限制</span><span class="sxs-lookup"><span data-stu-id="b9311-151">Limitations</span></span>
<span data-ttu-id="b9311-152">需求预测是帮助制造行业客户创建预测流程的工具。</span><span class="sxs-lookup"><span data-stu-id="b9311-152">Demand forecasting is a tool that helps customers in the manufacturing industry create forecasting processes.</span></span> <span data-ttu-id="b9311-153">它提供了需求预测解决方案的核心功能，并设计为可以轻松扩展。</span><span class="sxs-lookup"><span data-stu-id="b9311-153">It offers the core functionality of a demand forecasting solution and is designed so that it can easily be extended.</span></span> <span data-ttu-id="b9311-154">需求预测可能对商业、批发、仓库、运输或其他专业服务等行业的客户不是最合适。</span><span class="sxs-lookup"><span data-stu-id="b9311-154">Demand forecasting might not be the best fit for customers in industries such as commerce, wholesale, warehousing, transportation, or other professional services.</span></span>

### <a name="demand-forecast-variant-conversion-limitation"></a><span data-ttu-id="b9311-155">需求预测变型转换限制</span><span class="sxs-lookup"><span data-stu-id="b9311-155">Demand forecast variant conversion limitation</span></span>

<span data-ttu-id="b9311-156">如果库存 UOM 与需求预测 UOM 不同，在生成需求预测时将不完全支持每个变型转换的计量单位 (UOM)。</span><span class="sxs-lookup"><span data-stu-id="b9311-156">Unit of measure (UOM) per variant conversion is not fully supported when generating demand forecast if inventory UOM is different than the demand forecast UOM.</span></span>

<span data-ttu-id="b9311-157">生成预测（**库存 UOM > 需求预测 UOM**）使用产品 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b9311-157">Generating forecast (**Inventory UOM > Demand forecast UOM**) uses product UOM conversion.</span></span> <span data-ttu-id="b9311-158">在为需求预测生成加载历史数据时，即使在变型级别定义了转换，从库存 UOM 转换为需求预测 UOM 时也将始终使用产品级别 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b9311-158">When loading historical data for the demand forecast generation, the product level UOM conversion will be always used when converting from inventory UOM to the demand forecast UOM, even if there are conversions defined on the variant level.</span></span>

<span data-ttu-id="b9311-159">授权预测的第一部分（**需求预测 UOM > 库存 UOM**）使用产品 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b9311-159">The first part of authorizing forecast (**Demand forecast UOM > Inventory UOM**) uses product UOM conversion.</span></span> <span data-ttu-id="b9311-160">授权预测的第二部分（**库存 UOM > 销售 UOM**）使用变型 UOM 转换。</span><span class="sxs-lookup"><span data-stu-id="b9311-160">The second part of authorizing forecast (**Inventory UOM > Sales UOM**) uses the variant UOM conversion.</span></span> <span data-ttu-id="b9311-161">授权所生成的需求预测后，将使用产品级别的 UOM 转换完成从需求预测 UOM 到库存 UOM 的转换。</span><span class="sxs-lookup"><span data-stu-id="b9311-161">When the generated demand forecast is authorized, the conversion to inventory UOM from demand forecast UOM will be done using product level UOM conversion.</span></span> <span data-ttu-id="b9311-162">同时，库存单位和销售 UOM 之间的转换将遵循变型级别定义的转换。</span><span class="sxs-lookup"><span data-stu-id="b9311-162">At the same time, conversion between the inventory unit and the sales UOM will respect the variant level defined conversions.</span></span>

<span data-ttu-id="b9311-163">请注意，需求预测 UOM 不必具有任何特定含义。</span><span class="sxs-lookup"><span data-stu-id="b9311-163">Note that the demand forecast UOM does not have to have any specific meaning.</span></span> <span data-ttu-id="b9311-164">它可以定义为“需求预测单位”。</span><span class="sxs-lookup"><span data-stu-id="b9311-164">It can be defined as “Demand forecast unit”.</span></span> <span data-ttu-id="b9311-165">对于每个产品，您可以使用库存 UOM 将转换定义为 1:1。</span><span class="sxs-lookup"><span data-stu-id="b9311-165">For each of the products, you can define the conversion to be 1:1 with the inventory UOM.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b9311-166">其他资源</span><span class="sxs-lookup"><span data-stu-id="b9311-166">Additional resources</span></span>
--------

[<span data-ttu-id="b9311-167">需求预测设置</span><span class="sxs-lookup"><span data-stu-id="b9311-167">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

[<span data-ttu-id="b9311-168">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="b9311-168">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

[<span data-ttu-id="b9311-169">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="b9311-169">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="b9311-170">授权调整后的预测</span><span class="sxs-lookup"><span data-stu-id="b9311-170">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b9311-171">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="b9311-171">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="b9311-172">在计算需求预测时，需从历史交易记录数据中删除离群值</span><span class="sxs-lookup"><span data-stu-id="b9311-172">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)

[<span data-ttu-id="b9311-173">扩展需求预测功能</span><span class="sxs-lookup"><span data-stu-id="b9311-173">Extend the demand forecasting functionality</span></span>](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



