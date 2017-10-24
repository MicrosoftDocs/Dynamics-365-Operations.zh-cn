--- 
title: "使用模板创建日记帐条目"
description: "已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。"
author: aprilolson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 055fe129b9fc9cf50e1d9e1a5b4cb77285f20c92
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-journal-entry-using-a-template"></a><span data-ttu-id="ccb2e-103">使用模板创建日记帐条目</span><span class="sxs-lookup"><span data-stu-id="ccb2e-103">Create a journal entry using a template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccb2e-104">已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="ccb2e-105">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="ccb2e-106">”总帐“>”日记帐分录“>”普通日记帐“。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-106">General ledger > Journal entries > General journals.</span></span> <span data-ttu-id="ccb2e-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-107">Click New.</span></span>
    * <span data-ttu-id="ccb2e-108">此程序开始时需要创建和过帐日记帐凭证，但所有以前已过帐的日记帐凭证可以保存为模板。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
2. <span data-ttu-id="ccb2e-109">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-109">In the Name field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ccb2e-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-110">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ccb2e-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ccb2e-112">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-112">Click Lines.</span></span>
6. <span data-ttu-id="ccb2e-113">为帐户类型输入一个帐户。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-113">Enter an account for the Account type.</span></span>
7. <span data-ttu-id="ccb2e-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-114">In the Description field, type a value.</span></span>
8. <span data-ttu-id="ccb2e-115">在“借项”字段中，输入一个金额。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-115">Enter an amount in the Debit field.</span></span>
9. <span data-ttu-id="ccb2e-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-116">Click New.</span></span>
10. <span data-ttu-id="ccb2e-117">为帐户类型输入一个不同的帐户。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-117">Enter a different account for the Account type.</span></span>
11. <span data-ttu-id="ccb2e-118">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-118">In the Description field, type a value.</span></span>
12. <span data-ttu-id="ccb2e-119">在“借项”字段中，输入一个金额。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-119">Enter an amount in the Debit field.</span></span>
13. <span data-ttu-id="ccb2e-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-120">Click New.</span></span>
14. <span data-ttu-id="ccb2e-121">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-121">In the Account field, specify the desired values.</span></span>
15. <span data-ttu-id="ccb2e-122">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-122">In the Description field, type a value.</span></span>
16. <span data-ttu-id="ccb2e-123">在“贷项”字段中输入一个金额以使凭证试算平衡。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-123">Enter an amount in the Credit field to balance the voucher.</span></span>
17. <span data-ttu-id="ccb2e-124">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-124">Click Post.</span></span>
18. <span data-ttu-id="ccb2e-125">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-125">Click Functions.</span></span>
19. <span data-ttu-id="ccb2e-126">单击“保存凭证模板”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-126">Click Save voucher template.</span></span>
20. <span data-ttu-id="ccb2e-127">此程序使用百分比模板类型。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-127">This procedure assumes a Percent Template type.</span></span> <span data-ttu-id="ccb2e-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-128">Click OK.</span></span>
    * <span data-ttu-id="ccb2e-129">•百分比：凭证中的金额会被转换为百分比系数，当选择了凭证模板时，这允许应用任何金额。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-129">• Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>  <span data-ttu-id="ccb2e-130">•金额：将存储和应用实际金额。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-130">• Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="ccb2e-131">单击“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-131">Click General journals.</span></span>
22. <span data-ttu-id="ccb2e-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-132">Click New.</span></span>
23. <span data-ttu-id="ccb2e-133">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-133">In the Name field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="ccb2e-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="ccb2e-135">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-135">Click Lines.</span></span>
26. <span data-ttu-id="ccb2e-136">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-136">Click Functions.</span></span>
27. <span data-ttu-id="ccb2e-137">单击“选择凭证模板”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-137">Click Select voucher template.</span></span>
28. <span data-ttu-id="ccb2e-138">查找您之前创建的模板。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-138">Find the template that you created earlier.</span></span> <span data-ttu-id="ccb2e-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-139">Click OK.</span></span>
    * <span data-ttu-id="ccb2e-140">如果存在其它模板，您可能需要单击“上一步”，然后选择正确的模板。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-140">You may need to click Previous step and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="ccb2e-141">在“金额”字段中，输入要应用于凭证的金额。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-141">In the Amount field, enter the amount to be applied to the voucher.</span></span>
    * <span data-ttu-id="ccb2e-142">仅当凭证模板是百分比类型时才会显示金额字段。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-142">The amount field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="ccb2e-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-143">Click OK.</span></span>


