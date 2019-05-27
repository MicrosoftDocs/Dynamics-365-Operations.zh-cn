---
title: 收入报表财务报表
description: 本文介绍默认收入报表。 还介绍此报表的关联构建块。
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9105e1de86ed2834b04f75c7d08c4021402bcfda
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549142"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="3f231-104">收入报表财务报表</span><span class="sxs-lookup"><span data-stu-id="3f231-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f231-105">本文介绍默认收入报表。</span><span class="sxs-lookup"><span data-stu-id="3f231-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="3f231-106">还介绍此报表的关联构建块。</span><span class="sxs-lookup"><span data-stu-id="3f231-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="3f231-107">默认收入报表</span><span class="sxs-lookup"><span data-stu-id="3f231-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="3f231-108">默认报表</span><span class="sxs-lookup"><span data-stu-id="3f231-108">Default report</span></span>             | <span data-ttu-id="3f231-109">作用</span><span class="sxs-lookup"><span data-stu-id="3f231-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f231-110">收入报表 – 默认</span><span class="sxs-lookup"><span data-stu-id="3f231-110">Income Statement – Default</span></span> | <span data-ttu-id="3f231-111">提供组织当前期间以及本年迄今收益率的视图。</span><span class="sxs-lookup"><span data-stu-id="3f231-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="3f231-112">构建基块</span><span class="sxs-lookup"><span data-stu-id="3f231-112">Building blocks</span></span>
<span data-ttu-id="3f231-113">收入报表财务报表使用以下构建基块。</span><span class="sxs-lookup"><span data-stu-id="3f231-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="3f231-114">默认报表</span><span class="sxs-lookup"><span data-stu-id="3f231-114">Default report</span></span>             | <span data-ttu-id="3f231-115">行定义</span><span class="sxs-lookup"><span data-stu-id="3f231-115">Row definition</span></span>                     | <span data-ttu-id="3f231-116">列定义</span><span class="sxs-lookup"><span data-stu-id="3f231-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="3f231-117">收入报表 - 默认</span><span class="sxs-lookup"><span data-stu-id="3f231-117">Income Statement - Default</span></span> | <span data-ttu-id="3f231-118">收入报表汇总 - 默认</span><span class="sxs-lookup"><span data-stu-id="3f231-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="3f231-119">定期和 YTD - 默认</span><span class="sxs-lookup"><span data-stu-id="3f231-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="3f231-120">行定义</span><span class="sxs-lookup"><span data-stu-id="3f231-120">Row definition</span></span>

<span data-ttu-id="3f231-121">行定义，收入报表汇总 – 默认，包含每个传统收入报表部分的一个部分。</span><span class="sxs-lookup"><span data-stu-id="3f231-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="3f231-122">主科目类别维度用于创建此行定义。</span><span class="sxs-lookup"><span data-stu-id="3f231-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="3f231-123">因此，任何人都可以生成报表，而不必进行任何修改。</span><span class="sxs-lookup"><span data-stu-id="3f231-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="3f231-124">列定义</span><span class="sxs-lookup"><span data-stu-id="3f231-124">Column Definition</span></span>

<span data-ttu-id="3f231-125">列定义包含不同的列类型以提供不同级别的详细信息和财务数据。</span><span class="sxs-lookup"><span data-stu-id="3f231-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="3f231-126">**定期和 YTD – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="3f231-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="3f231-127">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="3f231-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="3f231-128">**FD** – 当前期间的财务数据</span><span class="sxs-lookup"><span data-stu-id="3f231-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="3f231-129">**FD** – 本年迄今的财务数据</span><span class="sxs-lookup"><span data-stu-id="3f231-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="3f231-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="3f231-130">Additional resources</span></span>
--------

[<span data-ttu-id="3f231-131">财务申报</span><span class="sxs-lookup"><span data-stu-id="3f231-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="3f231-132">查看财务报表</span><span class="sxs-lookup"><span data-stu-id="3f231-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="3f231-133">Dynamics 财务申报博客</span><span class="sxs-lookup"><span data-stu-id="3f231-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



