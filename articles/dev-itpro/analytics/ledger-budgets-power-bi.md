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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849421"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="4aa65-104">实际与预算 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="4aa65-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aa65-105">此主题描述**实际与预算** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="4aa65-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="4aa65-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="4aa65-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="4aa65-107">概览</span><span class="sxs-lookup"><span data-stu-id="4aa65-107">Overview</span></span>

<span data-ttu-id="4aa65-108">**实际与预算** Power BI 内容为负责监督组织中的实际与预算绩效的人员而创建。</span><span class="sxs-lookup"><span data-stu-id="4aa65-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="4aa65-109">**实际与预算** Power BI 内容可用于查看您的预算差异。</span><span class="sxs-lookup"><span data-stu-id="4aa65-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="4aa65-110">您可以按科目类别、预算代码、主科目、主科目描述或会计期间分析当前年度的预算，以更好地了解任何差异的原因。</span><span class="sxs-lookup"><span data-stu-id="4aa65-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="4aa65-111">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="4aa65-111">Accessing the Power BI content</span></span>
<span data-ttu-id="4aa65-112">来自**实际与预算** Power BI 内容的报表显示在**分类帐预算和预测**和 **CFO** 工作区中。</span><span class="sxs-lookup"><span data-stu-id="4aa65-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="4aa65-113">此 Power BI 内容中包含的报表</span><span class="sxs-lookup"><span data-stu-id="4aa65-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="4aa65-114">下表提供有关在**实际与预算** Power BI 内容中的每个报表页找到的指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4aa65-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="4aa65-115">报表</span><span class="sxs-lookup"><span data-stu-id="4aa65-115">Report</span></span>                      | <span data-ttu-id="4aa65-116">指标</span><span class="sxs-lookup"><span data-stu-id="4aa65-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa65-117">支出 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="4aa65-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="4aa65-118">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="4aa65-118">Total expenses this year</span></span></li><li><span data-ttu-id="4aa65-119">本年支出总额预算</span><span class="sxs-lookup"><span data-stu-id="4aa65-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="4aa65-120">收入 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="4aa65-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="4aa65-121">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="4aa65-121">Total revenue this year</span></span></li><li><span data-ttu-id="4aa65-122">本年收入总额预算</span><span class="sxs-lookup"><span data-stu-id="4aa65-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="4aa65-123">费用</span><span class="sxs-lookup"><span data-stu-id="4aa65-123">Expense</span></span>                     | <ul><li><span data-ttu-id="4aa65-124">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="4aa65-124">Total expenses this year</span></span></li><li><span data-ttu-id="4aa65-125">基于预算的支出目标</span><span class="sxs-lookup"><span data-stu-id="4aa65-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="4aa65-126">收入</span><span class="sxs-lookup"><span data-stu-id="4aa65-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="4aa65-127">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="4aa65-127">Total revenue this year</span></span></li><li><span data-ttu-id="4aa65-128">基于预算的收入目标</span><span class="sxs-lookup"><span data-stu-id="4aa65-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="4aa65-129">净收益</span><span class="sxs-lookup"><span data-stu-id="4aa65-129">Net income</span></span>                  | <ul><li><span data-ttu-id="4aa65-130">本年度净收益</span><span class="sxs-lookup"><span data-stu-id="4aa65-130">Net income this year</span></span></li><li><span data-ttu-id="4aa65-131">基于预算的净收益目标</span><span class="sxs-lookup"><span data-stu-id="4aa65-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="4aa65-132">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="4aa65-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="4aa65-133">实体</span><span class="sxs-lookup"><span data-stu-id="4aa65-133">Entity</span></span>                    | <span data-ttu-id="4aa65-134">内容</span><span class="sxs-lookup"><span data-stu-id="4aa65-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4aa65-135">总帐活动</span><span class="sxs-lookup"><span data-stu-id="4aa65-135">General Ledger Activities</span></span> | <span data-ttu-id="4aa65-136">总帐交易金额</span><span class="sxs-lookup"><span data-stu-id="4aa65-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="4aa65-137">预算活动</span><span class="sxs-lookup"><span data-stu-id="4aa65-137">Budget Activities</span></span>         | <span data-ttu-id="4aa65-138">预算登记的交易金额</span><span class="sxs-lookup"><span data-stu-id="4aa65-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="4aa65-139">主科目</span><span class="sxs-lookup"><span data-stu-id="4aa65-139">Main Accounts</span></span>             | <span data-ttu-id="4aa65-140">充当报表筛选依据的主科目</span><span class="sxs-lookup"><span data-stu-id="4aa65-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="4aa65-141">会计日历</span><span class="sxs-lookup"><span data-stu-id="4aa65-141">Fiscal Calendars</span></span>          | <span data-ttu-id="4aa65-142">充当报表筛选依据的会计日历</span><span class="sxs-lookup"><span data-stu-id="4aa65-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="4aa65-143">分类帐</span><span class="sxs-lookup"><span data-stu-id="4aa65-143">Ledgers</span></span>                   | <span data-ttu-id="4aa65-144">可用于筛选报表到当前分类帐的分类帐</span><span class="sxs-lookup"><span data-stu-id="4aa65-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="4aa65-145">预算代码</span><span class="sxs-lookup"><span data-stu-id="4aa65-145">Budget Codes</span></span>              | <span data-ttu-id="4aa65-146">充当报表筛选依据的预算代码</span><span class="sxs-lookup"><span data-stu-id="4aa65-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="4aa65-147">法人</span><span class="sxs-lookup"><span data-stu-id="4aa65-147">Legal Entities</span></span>            | <span data-ttu-id="4aa65-148">可用于筛选报表到当前法人的法人</span><span class="sxs-lookup"><span data-stu-id="4aa65-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
