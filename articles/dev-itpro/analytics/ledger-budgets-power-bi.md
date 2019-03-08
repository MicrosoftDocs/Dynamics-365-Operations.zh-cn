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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c801544e9e37a528203f5a1730aa8cb526d63dbf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "343481"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="b9b48-104">实际与预算 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="b9b48-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9b48-105">此主题描述**实际与预算** Microsoft Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="b9b48-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="b9b48-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="b9b48-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b9b48-107">概览</span><span class="sxs-lookup"><span data-stu-id="b9b48-107">Overview</span></span>

<span data-ttu-id="b9b48-108">**实际与预算** Power BI 内容为负责监督组织中的实际与预算绩效的人员而创建。</span><span class="sxs-lookup"><span data-stu-id="b9b48-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="b9b48-109">**实际与预算** Power BI 内容可用于查看您的预算差异。</span><span class="sxs-lookup"><span data-stu-id="b9b48-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="b9b48-110">您可以按科目类别、预算代码、主科目、主科目描述或会计期间分析当前年度的预算，以更好地了解任何差异的原因。</span><span class="sxs-lookup"><span data-stu-id="b9b48-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b9b48-111">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="b9b48-111">Accessing the Power BI content</span></span>
<span data-ttu-id="b9b48-112">来自**实际与预算** Power BI 内容的报表显示在**分类帐预算和预测**和 **CFO** 工作区中。</span><span class="sxs-lookup"><span data-stu-id="b9b48-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b9b48-113">此 Power BI 内容中包含的报表</span><span class="sxs-lookup"><span data-stu-id="b9b48-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="b9b48-114">下表提供有关在**实际与预算** Power BI 内容中的每个报表页找到的指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b9b48-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="b9b48-115">报表</span><span class="sxs-lookup"><span data-stu-id="b9b48-115">Report</span></span>                      | <span data-ttu-id="b9b48-116">指标</span><span class="sxs-lookup"><span data-stu-id="b9b48-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b48-117">支出 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="b9b48-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="b9b48-118">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="b9b48-118">Total expenses this year</span></span></li><li><span data-ttu-id="b9b48-119">本年支出总额预算</span><span class="sxs-lookup"><span data-stu-id="b9b48-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="b9b48-120">收入 - 实际与预算</span><span class="sxs-lookup"><span data-stu-id="b9b48-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="b9b48-121">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="b9b48-121">Total revenue this year</span></span></li><li><span data-ttu-id="b9b48-122">本年收入总额预算</span><span class="sxs-lookup"><span data-stu-id="b9b48-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="b9b48-123">费用</span><span class="sxs-lookup"><span data-stu-id="b9b48-123">Expense</span></span>                     | <ul><li><span data-ttu-id="b9b48-124">本年支出总额</span><span class="sxs-lookup"><span data-stu-id="b9b48-124">Total expenses this year</span></span></li><li><span data-ttu-id="b9b48-125">基于预算的支出目标</span><span class="sxs-lookup"><span data-stu-id="b9b48-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="b9b48-126">收入</span><span class="sxs-lookup"><span data-stu-id="b9b48-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="b9b48-127">本年收入总额</span><span class="sxs-lookup"><span data-stu-id="b9b48-127">Total revenue this year</span></span></li><li><span data-ttu-id="b9b48-128">基于预算的收入目标</span><span class="sxs-lookup"><span data-stu-id="b9b48-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="b9b48-129">净收益</span><span class="sxs-lookup"><span data-stu-id="b9b48-129">Net income</span></span>                  | <ul><li><span data-ttu-id="b9b48-130">本年度净收益</span><span class="sxs-lookup"><span data-stu-id="b9b48-130">Net income this year</span></span></li><li><span data-ttu-id="b9b48-131">基于预算的净收益目标</span><span class="sxs-lookup"><span data-stu-id="b9b48-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="b9b48-132">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="b9b48-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="b9b48-133">实体</span><span class="sxs-lookup"><span data-stu-id="b9b48-133">Entity</span></span>                    | <span data-ttu-id="b9b48-134">内容</span><span class="sxs-lookup"><span data-stu-id="b9b48-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b9b48-135">总帐活动</span><span class="sxs-lookup"><span data-stu-id="b9b48-135">General Ledger Activities</span></span> | <span data-ttu-id="b9b48-136">总帐交易金额</span><span class="sxs-lookup"><span data-stu-id="b9b48-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="b9b48-137">预算活动</span><span class="sxs-lookup"><span data-stu-id="b9b48-137">Budget Activities</span></span>         | <span data-ttu-id="b9b48-138">预算登记的交易金额</span><span class="sxs-lookup"><span data-stu-id="b9b48-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="b9b48-139">主科目</span><span class="sxs-lookup"><span data-stu-id="b9b48-139">Main Accounts</span></span>             | <span data-ttu-id="b9b48-140">充当报表筛选依据的主科目</span><span class="sxs-lookup"><span data-stu-id="b9b48-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="b9b48-141">会计日历</span><span class="sxs-lookup"><span data-stu-id="b9b48-141">Fiscal Calendars</span></span>          | <span data-ttu-id="b9b48-142">充当报表筛选依据的会计日历</span><span class="sxs-lookup"><span data-stu-id="b9b48-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="b9b48-143">分类帐</span><span class="sxs-lookup"><span data-stu-id="b9b48-143">Ledgers</span></span>                   | <span data-ttu-id="b9b48-144">可用于筛选报表到当前分类帐的分类帐</span><span class="sxs-lookup"><span data-stu-id="b9b48-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="b9b48-145">预算代码</span><span class="sxs-lookup"><span data-stu-id="b9b48-145">Budget Codes</span></span>              | <span data-ttu-id="b9b48-146">充当报表筛选依据的预算代码</span><span class="sxs-lookup"><span data-stu-id="b9b48-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="b9b48-147">法人</span><span class="sxs-lookup"><span data-stu-id="b9b48-147">Legal Entities</span></span>            | <span data-ttu-id="b9b48-148">可用于筛选报表到当前法人的法人</span><span class="sxs-lookup"><span data-stu-id="b9b48-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
