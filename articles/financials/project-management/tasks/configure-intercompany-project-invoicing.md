--- 
title: "配置内部公司项目开票"
description: "此过程显示如何设置贵组织内部两个公司之间的项目开票。"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="5ff27-103">配置内部公司项目开票</span><span class="sxs-lookup"><span data-stu-id="5ff27-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ff27-104">此过程显示如何设置贵组织内部两个公司之间的项目开票。</span><span class="sxs-lookup"><span data-stu-id="5ff27-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="5ff27-105">此任务使用 USSI 数据集。</span><span class="sxs-lookup"><span data-stu-id="5ff27-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="5ff27-106">转到“应付账款”>“供应商”>“所有供应商”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="5ff27-107">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="5ff27-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5ff27-108">在“操作窗格”上单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="5ff27-109">单击“内部公司”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-109">Click Intercompany.</span></span>
5. <span data-ttu-id="5ff27-110">将“有效”设置为“是”以启用内部公司贸易。</span><span class="sxs-lookup"><span data-stu-id="5ff27-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="5ff27-111">在“客户公司”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="5ff27-112">在“我的帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="5ff27-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-113">Click Save.</span></span>
9. <span data-ttu-id="5ff27-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5ff27-114">Close the page.</span></span>
10. <span data-ttu-id="5ff27-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5ff27-115">Close the page.</span></span>
11. <span data-ttu-id="5ff27-116">转至“项目管理和核算”>“设置”>“项目管理和核算参数”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="5ff27-117">单击“内部公司”选项卡。</span><span class="sxs-lookup"><span data-stu-id="5ff27-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="5ff27-118">将滑块移到“是”以启用公司间资源计划编制和工时单。</span><span class="sxs-lookup"><span data-stu-id="5ff27-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="5ff27-119">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="5ff27-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="5ff27-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-120">Click New.</span></span>
16. <span data-ttu-id="5ff27-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="5ff27-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="5ff27-122">在“借人方法人”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="5ff27-123">选中“应计收入”复选框。</span><span class="sxs-lookup"><span data-stu-id="5ff27-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="5ff27-124">在“默认工时单类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="5ff27-125">在“默认费用类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="5ff27-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-126">Click Save.</span></span>
22. <span data-ttu-id="5ff27-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5ff27-127">Close the page.</span></span>
23. <span data-ttu-id="5ff27-128">转到“项目管理与核算”>“设置”>“过帐”>”分类帐记帐设置“。</span><span class="sxs-lookup"><span data-stu-id="5ff27-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="5ff27-129">在“会计科目类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="5ff27-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="5ff27-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-130">Click New.</span></span>
26. <span data-ttu-id="5ff27-131">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="5ff27-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="5ff27-132">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="5ff27-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="5ff27-133">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="5ff27-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-134">Click Save.</span></span>
30. <span data-ttu-id="5ff27-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5ff27-135">Close the page.</span></span>
31. <span data-ttu-id="5ff27-136">转到“项目管理与核算”>“设置”>“价格”>“转让价格”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="5ff27-137">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-137">Click New.</span></span>
33. <span data-ttu-id="5ff27-138">在“有效日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="5ff27-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="5ff27-139">在“借人方法人”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ff27-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="5ff27-140">在“转让价格模型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="5ff27-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="5ff27-141">在“定价”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="5ff27-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="5ff27-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5ff27-142">Click Save.</span></span>


