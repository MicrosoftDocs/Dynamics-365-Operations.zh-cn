---
title: 实际与预算 Power BI 内容
description: 此主题描述实际与预算 Power BI 内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6a185da5055741ac30c7e237ef72d07084644651
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685264"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="1eeee-104">实际与预算 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="1eeee-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1eeee-105">此主题描述 **实际与预算** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="1eeee-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="1eeee-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="1eeee-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="1eeee-107">概览</span><span class="sxs-lookup"><span data-stu-id="1eeee-107">Overview</span></span>

<span data-ttu-id="1eeee-108">**实际与预算** Power BI 内容为负责监督组织中的实际与预算绩效的人员而创建。</span><span class="sxs-lookup"><span data-stu-id="1eeee-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="1eeee-109">**实际与预算** Power BI 内容可用于查看您的预算差异。</span><span class="sxs-lookup"><span data-stu-id="1eeee-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="1eeee-110">您可以按科目类别、预算代码、主科目、主科目描述或会计期间分析当前年度的预算，以更好地了解任何差异的原因。</span><span class="sxs-lookup"><span data-stu-id="1eeee-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="1eeee-111">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="1eeee-111">Accessing the Power BI content</span></span>
<span data-ttu-id="1eeee-112">来自 **实际与预算** Power BI 内容的报表显示在 **分类帐预算和预测** 和 **CFO** 工作区中。</span><span class="sxs-lookup"><span data-stu-id="1eeee-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="1eeee-113">此 Power BI 内容中包含的报表</span><span class="sxs-lookup"><span data-stu-id="1eeee-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="1eeee-114">下表提供有关在 **实际与预算** Power BI 内容中的每个报表页找到的指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1eeee-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="1eeee-115">报表</span><span class="sxs-lookup"><span data-stu-id="1eeee-115">Report</span></span>                      | <span data-ttu-id="1eeee-116">指标</span><span class="sxs-lookup"><span data-stu-id="1eeee-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeee-117">支出 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="1eeee-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="1eeee-118">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="1eeee-118">Total expenses this year</span></span></li><li><span data-ttu-id="1eeee-119">本年支出总额预算</span><span class="sxs-lookup"><span data-stu-id="1eeee-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="1eeee-120">收入 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="1eeee-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="1eeee-121">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="1eeee-121">Total revenue this year</span></span></li><li><span data-ttu-id="1eeee-122">本年收入总额预算</span><span class="sxs-lookup"><span data-stu-id="1eeee-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="1eeee-123">费用</span><span class="sxs-lookup"><span data-stu-id="1eeee-123">Expense</span></span>                     | <ul><li><span data-ttu-id="1eeee-124">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="1eeee-124">Total expenses this year</span></span></li><li><span data-ttu-id="1eeee-125">基于预算的支出目标</span><span class="sxs-lookup"><span data-stu-id="1eeee-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="1eeee-126">收入</span><span class="sxs-lookup"><span data-stu-id="1eeee-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="1eeee-127">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="1eeee-127">Total revenue this year</span></span></li><li><span data-ttu-id="1eeee-128">基于预算的收入目标</span><span class="sxs-lookup"><span data-stu-id="1eeee-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="1eeee-129">净收益</span><span class="sxs-lookup"><span data-stu-id="1eeee-129">Net income</span></span>                  | <ul><li><span data-ttu-id="1eeee-130">本年度净收益</span><span class="sxs-lookup"><span data-stu-id="1eeee-130">Net income this year</span></span></li><li><span data-ttu-id="1eeee-131">基于预算的净收益目标</span><span class="sxs-lookup"><span data-stu-id="1eeee-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="1eeee-132">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="1eeee-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="1eeee-133">实体</span><span class="sxs-lookup"><span data-stu-id="1eeee-133">Entity</span></span>                    | <span data-ttu-id="1eeee-134">内容</span><span class="sxs-lookup"><span data-stu-id="1eeee-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1eeee-135">总帐活动</span><span class="sxs-lookup"><span data-stu-id="1eeee-135">General Ledger Activities</span></span> | <span data-ttu-id="1eeee-136">总帐交易金额</span><span class="sxs-lookup"><span data-stu-id="1eeee-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="1eeee-137">预算活动</span><span class="sxs-lookup"><span data-stu-id="1eeee-137">Budget Activities</span></span>         | <span data-ttu-id="1eeee-138">预算登记的交易金额</span><span class="sxs-lookup"><span data-stu-id="1eeee-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="1eeee-139">主科目</span><span class="sxs-lookup"><span data-stu-id="1eeee-139">Main Accounts</span></span>             | <span data-ttu-id="1eeee-140">充当报表筛选依据的主科目</span><span class="sxs-lookup"><span data-stu-id="1eeee-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="1eeee-141">会计日历</span><span class="sxs-lookup"><span data-stu-id="1eeee-141">Fiscal Calendars</span></span>          | <span data-ttu-id="1eeee-142">充当报表筛选依据的会计日历</span><span class="sxs-lookup"><span data-stu-id="1eeee-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="1eeee-143">分类帐</span><span class="sxs-lookup"><span data-stu-id="1eeee-143">Ledgers</span></span>                   | <span data-ttu-id="1eeee-144">可用于筛选报表到当前分类帐的分类帐</span><span class="sxs-lookup"><span data-stu-id="1eeee-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="1eeee-145">预算代码</span><span class="sxs-lookup"><span data-stu-id="1eeee-145">Budget Codes</span></span>              | <span data-ttu-id="1eeee-146">充当报表筛选依据的预算代码</span><span class="sxs-lookup"><span data-stu-id="1eeee-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="1eeee-147">法人</span><span class="sxs-lookup"><span data-stu-id="1eeee-147">Legal Entities</span></span>            | <span data-ttu-id="1eeee-148">可用于筛选报表到当前法人的法人</span><span class="sxs-lookup"><span data-stu-id="1eeee-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
