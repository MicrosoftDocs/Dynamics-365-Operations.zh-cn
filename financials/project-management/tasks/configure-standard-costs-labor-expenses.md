--- 
title: "配置人工和支出的标准成本"
description: "此过程显示如何为项目的人工和费用设置标准价。"
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="b8af3-103">配置人工和支出的标准成本</span><span class="sxs-lookup"><span data-stu-id="b8af3-103">Configure standard costs for labor and expenses</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8af3-104">此过程显示如何为项目的人工和费用设置标准价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="b8af3-105">此任务使用 USSI 数据集。</span><span class="sxs-lookup"><span data-stu-id="b8af3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b8af3-106">转至“项目管理与核算 > 设置 > 价格 > 成本价(工时)”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="b8af3-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-107">Click New.</span></span>
3. <span data-ttu-id="b8af3-108">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b8af3-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="b8af3-109">在“成本价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b8af3-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="b8af3-110">可为项目类别设置标准成本价，也可以按照工作人员编号、项目编号、类别、日期以及它们的任何组合来设置成本价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="b8af3-111">应用的成本价是最能提供详细信息的成本价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="b8af3-112">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-112">Click Save.</span></span>
6. <span data-ttu-id="b8af3-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b8af3-113">Close the page.</span></span>
7. <span data-ttu-id="b8af3-114">转至“项目管理与核算 > 设置 > 价格 > 销售价(工时)”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="b8af3-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-115">Click New.</span></span>
9. <span data-ttu-id="b8af3-116">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b8af3-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="b8af3-117">在“有效”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b8af3-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="b8af3-118">在“定价”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="b8af3-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="b8af3-119">可以根据工时交易记录或按项目类别设置标准销售价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="b8af3-120">也可以按工作人员编号、项目编号、类别、交易记录日期或其中任一组合设置销售价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="b8af3-121">实际销售价是工作人员在“工时”日记帐中输入交易记录时应用的价格，它是具有最高详细级别的销售价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b8af3-122">例如，如果同时设置了一般销售价和工作人员特定的销售价，将使用工作人员特定的销售价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="b8af3-123">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-123">Click Save.</span></span>
13. <span data-ttu-id="b8af3-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b8af3-124">Close the page.</span></span>
14. <span data-ttu-id="b8af3-125">转至“项目管理与核算 > 设置 > 价格 > 销售价(费用)”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="b8af3-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-126">Click New.</span></span>
16. <span data-ttu-id="b8af3-127">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b8af3-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="b8af3-128">在“成本价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b8af3-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="b8af3-129">可以填写多个字段，但是要保存记录，至少必须填写该字段。</span><span class="sxs-lookup"><span data-stu-id="b8af3-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="b8af3-130">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-130">Click Save.</span></span>
19. <span data-ttu-id="b8af3-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b8af3-131">Close the page.</span></span>
20. <span data-ttu-id="b8af3-132">转至“项目管理与核算 > 设置 > 价格 > 销售价(费用)”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="b8af3-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-133">Click New.</span></span>
22. <span data-ttu-id="b8af3-134">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b8af3-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="b8af3-135">在“有效”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b8af3-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="b8af3-136">在“定价”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="b8af3-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="b8af3-137">工作人员在费用日记帐凭证中输入交易记录时使用的实际销售价是最详细的销售价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b8af3-138">例如，如果同时设置了日记帐和工作人员特定的销售价，将使用工作人员特定的销售价。</span><span class="sxs-lookup"><span data-stu-id="b8af3-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="b8af3-139">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b8af3-139">Click Save.</span></span>


