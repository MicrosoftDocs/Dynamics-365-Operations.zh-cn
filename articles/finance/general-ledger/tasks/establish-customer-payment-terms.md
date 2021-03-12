---
title: 设定客户付款期限
description: 此程序定义了一个现金折扣和到期日期设置。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec16ba09cc7c942119bab1d992856c3ffcd5c628
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968546"
---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="f2cd8-103">设定客户付款期限</span><span class="sxs-lookup"><span data-stu-id="f2cd8-103">Establish customer payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2cd8-104">此程序定义了一个现金折扣和到期日期设置。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="f2cd8-105">此任务指南使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="f2cd8-106">转到 **导航窗格 > 模块 > 应收帐款 > 付款设置 > 付款日**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-106">Go to **Navigation pane > Modules > Accounts receivable > Payments setup > Payment days**.</span></span> <span data-ttu-id="f2cd8-107">**付款期限** 的设置为 **应收帐款** 和 **应付帐款** 共享。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-107">The setup for the **Terms of payment** is shared for **Accounts receivable** and **Accounts payable**.</span></span> <span data-ttu-id="f2cd8-108">如果您在模块中进行定义，其它模板也可以使用这些定义。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="f2cd8-109">对于此任务向导，我在 **应收帐款** 下设置了所有付款期限。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-109">For this task guide, I set up all the terms of payment under **Accounts receivable**.</span></span>
2. <span data-ttu-id="f2cd8-110">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-110">Click **New**.</span></span> <span data-ttu-id="f2cd8-111">如果您的付款期限要求一周中特定的一天（星期一，星期二等）或一个月中特定的一天（5 日，10 日等），请创建付款日。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span> 
3. <span data-ttu-id="f2cd8-112">在 **付款日** 字段中，输入 ID。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-112">In the **Payment day** field, enter an ID.</span></span>
4. <span data-ttu-id="f2cd8-113">在 **描述** 字段中，输入付款日的描述。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-113">In the **Description** field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="f2cd8-114">在 **周/月** 字段中，选择“周”或“月”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-114">In the **Week/Month** field, select either 'Week' or 'Month'.</span></span> <span data-ttu-id="f2cd8-115">如果您要输入一周中的一天，如星期一，请选择“周”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="f2cd8-116">如果要输入一个月中的一天，如 10 日，选择“月”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="f2cd8-117">此示例中，选择“月”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-117">Select Month for this example.</span></span> 
6. <span data-ttu-id="f2cd8-118">在 **日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-118">In the **Day of month** field, enter a date.</span></span> <span data-ttu-id="f2cd8-119">日期应作为数字输入，如“10”而不是“第 10”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span> 
7. <span data-ttu-id="f2cd8-120">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-120">Click **Save**.</span></span>
8. <span data-ttu-id="f2cd8-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-121">Close the page.</span></span>
9. <span data-ttu-id="f2cd8-122">转到 **导航窗格 > 模块 > 应收帐款 > 付款设置 > 付款期限**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-122">Go to **Navigation pane > Modules > Accounts receivable > Payments setup > Terms of payment**.</span></span>
10. <span data-ttu-id="f2cd8-123">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-123">Click **New**.</span></span> <span data-ttu-id="f2cd8-124">付款期用于定义如何计算到期日。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="f2cd8-125">现金打折日期设置在另一个页面进行定义。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-125">The cash discount date setup is defined in a separate page.</span></span> 
11. <span data-ttu-id="f2cd8-126">在 **付款期限** 字段中，输入 ID。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-126">In the **Terms of payment field**, enter an ID.</span></span>
12. <span data-ttu-id="f2cd8-127">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-127">In the **Description** field, enter a description.</span></span>
13. <span data-ttu-id="f2cd8-128">选择 **付款方式**，如货到付款、净额、当前月份等。付款方法用于定义如何开始计算到期日期。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-128">Select a **Payment method** such as COD, Net, Current month, etc. The Payment method is used to define the start of how the due will be calculated.</span></span> <span data-ttu-id="f2cd8-129">例如，如果到期日总是发票日期后的固定月数或天数，将使用净额。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-129">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="f2cd8-130">如果使用货到付款，当收到发票时需要付款，所以将不计算到期日。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-130">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="f2cd8-131">在此任务向导中，选择“当前月份”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-131">Select 'Current month' for this task guide.</span></span>  
14. <span data-ttu-id="f2cd8-132">如果计算中包括了一周中的特定一天或特定一日，请选择一个 **付款日**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-132">Select a **Payment day** if a specific day of the  week or date are included in the calculation.</span></span> <span data-ttu-id="f2cd8-133">根据您的付款期限，您可以以月或天数为单位输入一个数量。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-133">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="f2cd8-134">或者您可以使用 **付款计划** 或 **付款日** 来“添加”到付款方式的结束日期。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-134">Or you can use the **Payment schedule** or **Payment day** to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="f2cd8-135">如果到期日期始终是下个月的 10 号，选择日期为 10 号的 **付款日**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-135">If the due date will always be the 10th of the next month, select a **Payment day** of the 10th.</span></span> 
15. <span data-ttu-id="f2cd8-136">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-136">Click **Save**.</span></span>
16. <span data-ttu-id="f2cd8-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-137">Close the page.</span></span>
17. <span data-ttu-id="f2cd8-138">转到 **应收帐款 > 付款设置 > 现金折扣**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-138">Go to **Accounts receivable > Payments setup > Cash discounts**.</span></span>
18. <span data-ttu-id="f2cd8-139">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-139">Click **New**.</span></span> <span data-ttu-id="f2cd8-140">此页面用于定义如何计算现金折旧日期。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-140">This page is used to define how the cash discount date will be calculated.</span></span> 
19. <span data-ttu-id="f2cd8-141">在 **现金折扣** 字段中，输入 ID。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-141">In the **Cash discount** field, enter an ID.</span></span>
20. <span data-ttu-id="f2cd8-142">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-142">In the **Description** field, enter a description.</span></span>
21. <span data-ttu-id="f2cd8-143">如果分层的现金折旧可用，则选择与这个新的现金折旧相关的 **下一个折旧代码**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-143">If a tiered cash discount is available, select the **Next discount code** that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="f2cd8-144">在 **天数** 字段中，输入用于计算现金折旧的天数。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-144">In the **Days** field, enter the number of days used to calculate the cash dicount date.</span></span> <span data-ttu-id="f2cd8-145">如果选择了 **净额** 原则，天数将被添加到发票日期来计算现金折旧日期。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-145">If **Net** principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="f2cd8-146">在 **折扣百分比** 字段中，输入现金折扣的百分比。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-146">In the **Discount percentage** field, enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="f2cd8-147">在 **客户折扣的主科目** 中，输入客户发票的现金折旧将过帐到的主科目。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-147">In the **Main account for customer discounts**, enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="f2cd8-148">选择 **折旧抵销帐户** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-148">In the **Discount offset accounts** field, select an option.</span></span> <span data-ttu-id="f2cd8-149">如果您选择“发票行上的帐户”，现金折旧将被过帐到供应商发票行的同一资产/费用主要帐户。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-149">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="f2cd8-150">如果您选择“使用供应商发票的主要帐户”，现金折旧将被过帐到您在“供应商的主要帐户”中定义的主要帐户。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-150">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="f2cd8-151">对于本示例，选择“使用供应商发票的主要帐户”。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-151">For this example, select 'Use main account for vendor invoices'.</span></span> 
26. <span data-ttu-id="f2cd8-152">在 **供应商折扣的主科目** 字段中，输入供应商发票的现金折旧将过帐到的主科目。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-152">In the **Main account for vendor discounts** field, enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="f2cd8-153">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2cd8-153">Click **Save**.</span></span>

