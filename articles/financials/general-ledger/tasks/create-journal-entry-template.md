---
title: 使用模板创建日记帐分录
description: 已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: babbc5ee067743d368680970556f8e5d3d8585f0
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916136"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="a289b-103">使用模板创建日记帐分录</span><span class="sxs-lookup"><span data-stu-id="a289b-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a289b-104">已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。</span><span class="sxs-lookup"><span data-stu-id="a289b-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="a289b-105">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="a289b-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="a289b-106">转到**导航窗格 > 模块 > 总帐 > 日记帐条目 > 普通日记帐**。</span><span class="sxs-lookup"><span data-stu-id="a289b-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="a289b-107">在**操作窗格**中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a289b-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="a289b-108">此程序开始时需要创建和过帐日记帐凭证，但所有以前已过帐的日记帐凭证可以保存为模板。</span><span class="sxs-lookup"><span data-stu-id="a289b-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="a289b-109">在**名称**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a289b-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a289b-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a289b-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a289b-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a289b-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a289b-112">单击**行**。</span><span class="sxs-lookup"><span data-stu-id="a289b-112">Click **Lines**.</span></span>
7. <span data-ttu-id="a289b-113">在**帐户类型**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="a289b-114">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="a289b-115">在**借方**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="a289b-116">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a289b-116">Click **New**.</span></span>
11. <span data-ttu-id="a289b-117">在**帐户类型**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="a289b-118">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="a289b-119">在**借方**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="a289b-120">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a289b-120">Click **New**.</span></span>
14. <span data-ttu-id="a289b-121">在**帐户**字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="a289b-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="a289b-122">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a289b-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="a289b-123">在**贷项**字段中，键入一个值以使凭证试算平衡。</span><span class="sxs-lookup"><span data-stu-id="a289b-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="a289b-124">在**操作窗格**上，单击**过帐**。</span><span class="sxs-lookup"><span data-stu-id="a289b-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="a289b-125">单击**功能**。</span><span class="sxs-lookup"><span data-stu-id="a289b-125">Click **Functions**.</span></span>
19. <span data-ttu-id="a289b-126">单击**保存凭证**模板。</span><span class="sxs-lookup"><span data-stu-id="a289b-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="a289b-127">此程序使用**百分比模板**类型。</span><span class="sxs-lookup"><span data-stu-id="a289b-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="a289b-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a289b-128">Click OK.</span></span>
    - <span data-ttu-id="a289b-129">百分比：凭证中的金额会被转换为百分比系数，当选择了凭证模板时，这允许应用任何金额。</span><span class="sxs-lookup"><span data-stu-id="a289b-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="a289b-130">金额：将存储和应用实际金额。</span><span class="sxs-lookup"><span data-stu-id="a289b-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="a289b-131">单击**普通日记帐**。</span><span class="sxs-lookup"><span data-stu-id="a289b-131">Click **General journals**.</span></span>
22. <span data-ttu-id="a289b-132">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a289b-132">Click **New**.</span></span>
23. <span data-ttu-id="a289b-133">在**名称**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a289b-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="a289b-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a289b-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="a289b-135">单击**行**。</span><span class="sxs-lookup"><span data-stu-id="a289b-135">Click **Lines**.</span></span>
26. <span data-ttu-id="a289b-136">单击**功能**。</span><span class="sxs-lookup"><span data-stu-id="a289b-136">Click **Functions**.</span></span>
27. <span data-ttu-id="a289b-137">单击**选择凭证模板**。</span><span class="sxs-lookup"><span data-stu-id="a289b-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="a289b-138">查找您之前创建的模板。</span><span class="sxs-lookup"><span data-stu-id="a289b-138">Find the template that you created earlier.</span></span> <span data-ttu-id="a289b-139">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a289b-139">Click **OK**.</span></span> <span data-ttu-id="a289b-140">如果存在其它模板，您可能需要单击**上一步**，然后选择正确的模板。</span><span class="sxs-lookup"><span data-stu-id="a289b-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="a289b-141">在**金额**字段中，输入要应用于凭证的金额。</span><span class="sxs-lookup"><span data-stu-id="a289b-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="a289b-142">仅当凭证模板是百分比类型时才会显示**金额**字段。</span><span class="sxs-lookup"><span data-stu-id="a289b-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="a289b-143">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a289b-143">Click **OK**.</span></span>

