---
title: 配置人工和支出的标准成本
description: 本主题介绍如何为项目的人工和费用设置标准价。
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185397"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="204d6-103">配置人工和支出的标准成本</span><span class="sxs-lookup"><span data-stu-id="204d6-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="204d6-104">本主题介绍如何为项目的人工和费用设置标准价。</span><span class="sxs-lookup"><span data-stu-id="204d6-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="204d6-105">此任务使用 USSI 数据集。</span><span class="sxs-lookup"><span data-stu-id="204d6-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="204d6-106">在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 成本价(工时)**。</span><span class="sxs-lookup"><span data-stu-id="204d6-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="204d6-107">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="204d6-107">Select **New**.</span></span>
3. <span data-ttu-id="204d6-108">在**生效日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="204d6-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="204d6-109">在**成本价**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="204d6-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="204d6-110">可为项目类别设置标准成本价，也可以按照工作人员编号、项目编号、类别、日期以及它们的任何组合来设置成本价。</span><span class="sxs-lookup"><span data-stu-id="204d6-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="204d6-111">应用的成本价是最能提供详细信息的成本价。</span><span class="sxs-lookup"><span data-stu-id="204d6-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="204d6-112">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="204d6-112">Select **Save**.</span></span>
6. <span data-ttu-id="204d6-113">在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 销售价(工时)**。</span><span class="sxs-lookup"><span data-stu-id="204d6-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="204d6-114">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="204d6-114">Select **New**.</span></span>
8. <span data-ttu-id="204d6-115">在**生效日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="204d6-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="204d6-116">在**有效**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="204d6-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="204d6-117">在**定价**字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="204d6-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="204d6-118">可以根据工时交易记录或按项目类别设置标准销售价。</span><span class="sxs-lookup"><span data-stu-id="204d6-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="204d6-119">也可以按工作人员编号、项目编号、类别、交易记录日期或其中任一组合设置销售价。</span><span class="sxs-lookup"><span data-stu-id="204d6-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="204d6-120">实际销售价是工作人员在“工时”日记帐中输入交易记录时应用的价格，它是具有最高详细级别的销售价。</span><span class="sxs-lookup"><span data-stu-id="204d6-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="204d6-121">例如，如果同时设置了一般销售价和工作人员特定的销售价，将使用工作人员特定的销售价。</span><span class="sxs-lookup"><span data-stu-id="204d6-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="204d6-122">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="204d6-122">Select **Save**.</span></span>
12. <span data-ttu-id="204d6-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="204d6-123">Close the page.</span></span>
13. <span data-ttu-id="204d6-124">在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 成本价(支出)**。</span><span class="sxs-lookup"><span data-stu-id="204d6-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="204d6-125">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="204d6-125">Select **New**.</span></span>
15. <span data-ttu-id="204d6-126">在**生效日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="204d6-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="204d6-127">在**成本价**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="204d6-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="204d6-128">可以填写多个字段，但是要保存记录，至少必须填写该字段。</span><span class="sxs-lookup"><span data-stu-id="204d6-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="204d6-129">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="204d6-129">Select **Save**.</span></span>
18. <span data-ttu-id="204d6-130">在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 销售价(支出)**。</span><span class="sxs-lookup"><span data-stu-id="204d6-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="204d6-131">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="204d6-131">Select **New**.</span></span>
20. <span data-ttu-id="204d6-132">在**生效日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="204d6-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="204d6-133">在**有效**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="204d6-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="204d6-134">在**定价**字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="204d6-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="204d6-135">工作人员在费用日记帐凭证中输入交易记录时使用的实际销售价是最详细的销售价。</span><span class="sxs-lookup"><span data-stu-id="204d6-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="204d6-136">例如，如果同时设置了日记帐和工作人员特定的销售价，将使用工作人员特定的销售价。</span><span class="sxs-lookup"><span data-stu-id="204d6-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="204d6-137">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="204d6-137">Select **Save**.</span></span>

