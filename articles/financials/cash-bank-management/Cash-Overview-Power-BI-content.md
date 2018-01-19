---
title: "现金概览 Power BI 内容"
description: "此主题介绍现金概览 Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: dfac5fe931cd6932da3a3e851b2578267449ea7b
ms.contentlocale: zh-cn
ms.lasthandoff: 01/19/2018

---

# <a name="cash-overview-power-bi-content"></a><span data-ttu-id="947ae-104">现金概览 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="947ae-104">Cash overview Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="947ae-105">此主题介绍**现金概览** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="947ae-105">This topic describes the **Cash overview** Microsoft Power BI content.</span></span> <span data-ttu-id="947ae-106">它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="947ae-106">It explains how to access the reports that are included in the content, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="947ae-107">概览</span><span class="sxs-lookup"><span data-stu-id="947ae-107">Overview</span></span>

<span data-ttu-id="947ae-108">**现金概览** Power BI 内容面向负责组织中的现金的人员创建。</span><span class="sxs-lookup"><span data-stu-id="947ae-108">The **Cash overview** Power BI content was created for individuals who are responsible for cash in their organization.</span></span> <span data-ttu-id="947ae-109">**现金概览** Power BI 内容提供对您的现金流量的可见性。</span><span class="sxs-lookup"><span data-stu-id="947ae-109">The **Cash overview** Power BI content provides visibility into your cash flow.</span></span> <span data-ttu-id="947ae-110">它还提供预测，可以帮助您做出更好的决策并改进您的现金流量的健康状况。</span><span class="sxs-lookup"><span data-stu-id="947ae-110">It also provides forecasts that can help you make better decisions and therefore improve the health of your cash flow.</span></span> <span data-ttu-id="947ae-111">您可按法人、币种和银行帐户分析现金以更好地了解盈余和赤字。</span><span class="sxs-lookup"><span data-stu-id="947ae-111">You can analyze cash by legal entity, currency, and bank account to get a better understanding of surpluses and shortfalls.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="947ae-112">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="947ae-112">Accessing the Power BI content</span></span>

<span data-ttu-id="947ae-113">来自**现金概览** Power BI 内容的报表显示在**现金概览**和**银行管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="947ae-113">Reports from the **Cash overview** Power BI content are displayed in the **Cash overview** and **Bank management** workspaces.</span></span>

<span data-ttu-id="947ae-114">若要查看带数据的现金流量预测报表，你必须先从“现金和银行管理”区域使用**计算现金流量预测**功能运行预测计算流程。</span><span class="sxs-lookup"><span data-stu-id="947ae-114">To view the Cash flow forecasting reports with data, you must first run the forecast calculation process using the **Calculate cash flow forecasts** function from the Cash and bank management area.</span></span>  <span data-ttu-id="947ae-115">需要为包括在预测中的每个公司完成此操作。</span><span class="sxs-lookup"><span data-stu-id="947ae-115">This needs to be completed for each company included in the forecast.</span></span>  <span data-ttu-id="947ae-116">然后，你需刷新**实体商店**页上的 LedgerCovLiquidityMeasurement 聚合度量。</span><span class="sxs-lookup"><span data-stu-id="947ae-116">You then need to refresh the LedgerCovLiquidityMeasurement aggregate measurement on the **Entity Store** page.</span></span>  

<span data-ttu-id="947ae-117">为了演示目的，你可以从演示数据模块使用**生成数据**页添加现金流量预测演示数据。</span><span class="sxs-lookup"><span data-stu-id="947ae-117">For demonstration purposes, you can add cash flow forecasting demo data using the **Generate data** page from the Demo data module.</span></span>  <span data-ttu-id="947ae-118">此脚本将数据插入到现金流量预测表以快速填充报表所需的信息。</span><span class="sxs-lookup"><span data-stu-id="947ae-118">This script will insert data into the cash flow forecasting tables to quickly populate information necessary for reports.</span></span>  <span data-ttu-id="947ae-119">仅当你在环境上部署演示数据套件模型时，此模块才可用。</span><span class="sxs-lookup"><span data-stu-id="947ae-119">This module is only available if you have the Demo data suite model deployed on the environment.</span></span> 

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="947ae-120">此 Power BI 内容中包含的报表</span><span class="sxs-lookup"><span data-stu-id="947ae-120">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="947ae-121">下表提供有关在**现金概览** Power BI 内容中的每个报表页找到的指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="947ae-121">The following table provides details about the metrics that are found on each report page in the **Cash overview** Power BI content.</span></span>

| <span data-ttu-id="947ae-122">报告</span><span class="sxs-lookup"><span data-stu-id="947ae-122">Report</span></span>                                | <span data-ttu-id="947ae-123">内容</span><span class="sxs-lookup"><span data-stu-id="947ae-123">Contents</span></span> |
|---------------------------------------|----------|
| <span data-ttu-id="947ae-124">现金概览 - 所有公司</span><span class="sxs-lookup"><span data-stu-id="947ae-124">Cash overview – all companies</span></span>         | <ul><li><span data-ttu-id="947ae-125">系统币种的流入量和流出量</span><span class="sxs-lookup"><span data-stu-id="947ae-125">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="947ae-126">预测币种余额</span><span class="sxs-lookup"><span data-stu-id="947ae-126">Forecasted currency balances</span></span></li><li><span data-ttu-id="947ae-127">系统币种的银行总余额</span><span class="sxs-lookup"><span data-stu-id="947ae-127">Total bank balance in system currency</span></span></li><li><span data-ttu-id="947ae-128">按法人分类的余额</span><span class="sxs-lookup"><span data-stu-id="947ae-128">Balance by legal entity</span></span></li><li><span data-ttu-id="947ae-129">银行帐户币种的今日实际余额与预测余额比较</span><span class="sxs-lookup"><span data-stu-id="947ae-129">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="947ae-130">现金概览 - 当前公司</span><span class="sxs-lookup"><span data-stu-id="947ae-130">Cash overview – current company</span></span>       | <ul><li><span data-ttu-id="947ae-131">记帐币种的流入量和流出量</span><span class="sxs-lookup"><span data-stu-id="947ae-131">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="947ae-132">预测币种余额</span><span class="sxs-lookup"><span data-stu-id="947ae-132">Forecasted currency balances</span></span></li><li><span data-ttu-id="947ae-133">记帐币种的银行总余额</span><span class="sxs-lookup"><span data-stu-id="947ae-133">Total bank balance in accounting currency</span></span></li><li><span data-ttu-id="947ae-134">银行帐户币种的今日实际余额与预测余额比较</span><span class="sxs-lookup"><span data-stu-id="947ae-134">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="947ae-135">现金流量预测 - 所有公司</span><span class="sxs-lookup"><span data-stu-id="947ae-135">Cash flow forecast – all companies</span></span>    | <ul><li><span data-ttu-id="947ae-136">系统币种的流入量和流出量</span><span class="sxs-lookup"><span data-stu-id="947ae-136">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="947ae-137">每日预测汇总</span><span class="sxs-lookup"><span data-stu-id="947ae-137">Daily forecast summary</span></span></li><li><span data-ttu-id="947ae-138">预测详细信息</span><span class="sxs-lookup"><span data-stu-id="947ae-138">Forecast details</span></span></li></ul> |
| <span data-ttu-id="947ae-139">现金流量预测 - 公司币种</span><span class="sxs-lookup"><span data-stu-id="947ae-139">Cash flow forecast – currency company</span></span> | <ul><li><span data-ttu-id="947ae-140">记帐币种的流入量和流出量</span><span class="sxs-lookup"><span data-stu-id="947ae-140">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="947ae-141">每日预测汇总</span><span class="sxs-lookup"><span data-stu-id="947ae-141">Daily forecast summary</span></span></li><li><span data-ttu-id="947ae-142">预测详细信息</span><span class="sxs-lookup"><span data-stu-id="947ae-142">Forecast details</span></span></li></ul> |
| <span data-ttu-id="947ae-143">币种预测</span><span class="sxs-lookup"><span data-stu-id="947ae-143">Currency forecast</span></span>                     | <ul><li><span data-ttu-id="947ae-144">预测币种余额</span><span class="sxs-lookup"><span data-stu-id="947ae-144">Forecasted currency balances</span></span></li><li><span data-ttu-id="947ae-145">每日币种汇总</span><span class="sxs-lookup"><span data-stu-id="947ae-145">Daily currency summary</span></span></li><li><span data-ttu-id="947ae-146">预测详细信息</span><span class="sxs-lookup"><span data-stu-id="947ae-146">Forecast details</span></span></li></ul> |
| <span data-ttu-id="947ae-147">银行余额</span><span class="sxs-lookup"><span data-stu-id="947ae-147">Bank balances</span></span>                         | <ul><li><span data-ttu-id="947ae-148">系统币种的银行总余额</span><span class="sxs-lookup"><span data-stu-id="947ae-148">Total bank balance in system currency</span></span></li><li><span data-ttu-id="947ae-149">按法人分类的余额</span><span class="sxs-lookup"><span data-stu-id="947ae-149">Balance by legal entity</span></span></li><li><span data-ttu-id="947ae-150">银行帐户币种的今日实际余额与预测余额比较</span><span class="sxs-lookup"><span data-stu-id="947ae-150">Today’s actual vs forecasted balance in bank account currency</span></span></li><li><span data-ttu-id="947ae-151">按银行帐户分类的余额</span><span class="sxs-lookup"><span data-stu-id="947ae-151">Balance by bank account</span></span></li><li><span data-ttu-id="947ae-152">原币余额</span><span class="sxs-lookup"><span data-stu-id="947ae-152">Balance by currency</span></span></li></ul> |


## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="947ae-153">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="947ae-153">Understanding the data model and entities</span></span>

<span data-ttu-id="947ae-154">下表显示**现金概览** Power BI 内容所基于的实体。</span><span class="sxs-lookup"><span data-stu-id="947ae-154">The following table shows the entities that the **Cash overview** Power BI content is based on.</span></span>

| <span data-ttu-id="947ae-155">实体</span><span class="sxs-lookup"><span data-stu-id="947ae-155">Entity</span></span>                                                                          | <span data-ttu-id="947ae-156">内容</span><span class="sxs-lookup"><span data-stu-id="947ae-156">Contents</span></span> |
|---------------------------------------------------------------------------------|----------|
| <span data-ttu-id="947ae-157">LedgerCovLiquidityMeasurement\_Company</span><span class="sxs-lookup"><span data-stu-id="947ae-157">LedgerCovLiquidityMeasurement\_Company</span></span>                                          | <span data-ttu-id="947ae-158">充当报表筛选依据的公司</span><span class="sxs-lookup"><span data-stu-id="947ae-158">Companies to filter reports by</span></span> |
| <span data-ttu-id="947ae-159">LedgerCovLiquidityMeasurement\_Date</span><span class="sxs-lookup"><span data-stu-id="947ae-159">LedgerCovLiquidityMeasurement\_Date</span></span>                                             | <span data-ttu-id="947ae-160">充当报表筛选依据的日期</span><span class="sxs-lookup"><span data-stu-id="947ae-160">Dates to filter reports by</span></span> |
| <span data-ttu-id="947ae-161">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span><span class="sxs-lookup"><span data-stu-id="947ae-161">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span></span>                          | <span data-ttu-id="947ae-162">实际银行余额与上次预测的银行余额</span><span class="sxs-lookup"><span data-stu-id="947ae-162">Actual bank balance vs last forecasted bank balance</span></span> |
| <span data-ttu-id="947ae-163">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span><span class="sxs-lookup"><span data-stu-id="947ae-163">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span></span>                               | <span data-ttu-id="947ae-164">预测交易记录详细信息</span><span class="sxs-lookup"><span data-stu-id="947ae-164">Forecasted transaction details</span></span> |
| <span data-ttu-id="947ae-165">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span><span class="sxs-lookup"><span data-stu-id="947ae-165">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span></span>    | <span data-ttu-id="947ae-166">使用公司记帐币种的汇总的现金流入量、流出量和余额</span><span class="sxs-lookup"><span data-stu-id="947ae-166">Summarized cash inflows, outflows, and balance using each company’s accounting currency</span></span> |
| <span data-ttu-id="947ae-167">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span><span class="sxs-lookup"><span data-stu-id="947ae-167">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span></span> | <span data-ttu-id="947ae-168">使用系统币种的用于所有公司的汇总的现金流入量、流出量和余额</span><span class="sxs-lookup"><span data-stu-id="947ae-168">Summarized cash inflows, outflows, and balance using the system currency for all companies</span></span> |
| <span data-ttu-id="947ae-169">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span><span class="sxs-lookup"><span data-stu-id="947ae-169">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span></span>            | <span data-ttu-id="947ae-170">使用交易币种的汇总的净交易记录金额和币种余额</span><span class="sxs-lookup"><span data-stu-id="947ae-170">Summarized net transaction amount and balance of currencies using the transaction currency</span></span> |



