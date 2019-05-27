---
title: 创建催款单序列
description: 使用此任务指南创建收款单序列。
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567421"
---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="4a106-103">创建催款单序列</span><span class="sxs-lookup"><span data-stu-id="4a106-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a106-104">使用此任务指南创建收款单序列。</span><span class="sxs-lookup"><span data-stu-id="4a106-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="4a106-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="4a106-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="4a106-106">转到“信用征收”>“设置”>“设置收款单序列”。</span><span class="sxs-lookup"><span data-stu-id="4a106-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="4a106-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4a106-107">Click New.</span></span>
3. <span data-ttu-id="4a106-108">在“收款单序列”字段中，输入要代表序列的序列 ID。</span><span class="sxs-lookup"><span data-stu-id="4a106-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="4a106-109">将使用该 ID 设置过帐模板。</span><span class="sxs-lookup"><span data-stu-id="4a106-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="4a106-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a106-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4a106-111">付款期限是可选的。</span><span class="sxs-lookup"><span data-stu-id="4a106-111">The terms of payment is optional.</span></span> <span data-ttu-id="4a106-112">如果您在此处输入一个值，则收款单费用发票将使用这些付款期限，而非客户所保留的付款期限。</span><span class="sxs-lookup"><span data-stu-id="4a106-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="4a106-113">在“收款单代码”字段中，选择您想要发送的第一个收款单代码。</span><span class="sxs-lookup"><span data-stu-id="4a106-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="4a106-114">根据发票上的截止日期、您在“天数”字段中输入的宽限期值以及您在此行中输入的其它信息创建第一个收款单。</span><span class="sxs-lookup"><span data-stu-id="4a106-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="4a106-115">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a106-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4a106-116">该费用的币种默认为客户币种。</span><span class="sxs-lookup"><span data-stu-id="4a106-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="4a106-117">此币种代码可以不同于发票币种。</span><span class="sxs-lookup"><span data-stu-id="4a106-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="4a106-118">单击“添加”，添加下一个被发送至序列的收款单</span><span class="sxs-lookup"><span data-stu-id="4a106-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="4a106-119">在大多数情况下，第一个收款单仅是警告。</span><span class="sxs-lookup"><span data-stu-id="4a106-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="4a106-120">您可以根据需要添加费用。</span><span class="sxs-lookup"><span data-stu-id="4a106-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="4a106-121">在“收款单代码”字段中，选择下一个被发送至序列的收款单。</span><span class="sxs-lookup"><span data-stu-id="4a106-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="4a106-122">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a106-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="4a106-123">在“主帐单”字段中，选择用于费用的收入帐户。</span><span class="sxs-lookup"><span data-stu-id="4a106-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="4a106-124">在将收款单过帐时输入要收取的费用。</span><span class="sxs-lookup"><span data-stu-id="4a106-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="4a106-125">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="4a106-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="4a106-126">如果销售税额必须计算在费用中，请选择物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="4a106-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="4a106-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4a106-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4a106-128">在收款单寄出前，输入所需的最小逾期余额。</span><span class="sxs-lookup"><span data-stu-id="4a106-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="4a106-129">输入您所允许的宽限天数。</span><span class="sxs-lookup"><span data-stu-id="4a106-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="4a106-130">这是一个在截止日期后收款单可以生成的天数。</span><span class="sxs-lookup"><span data-stu-id="4a106-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="4a106-131">用于计算的截止日期取决于收款单在收款单序列的位置：   ⦁    收款单 1 的宽限期与发票上的截止日期相关。</span><span class="sxs-lookup"><span data-stu-id="4a106-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="4a106-132">⦁ 根据在“应收账款参数”页“更新收款单代码”字段中的选择，收款单 2 的宽限期和更高状态与以前的收款单过帐或打印的日期相关。</span><span class="sxs-lookup"><span data-stu-id="4a106-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="4a106-133">单击“添加”，在序列中添加最后一个收款单。</span><span class="sxs-lookup"><span data-stu-id="4a106-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="4a106-134">您最多可为收款单序列添加五个收款单代码。</span><span class="sxs-lookup"><span data-stu-id="4a106-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="4a106-135">在“收款单代码”字段中，选择下一个被发送至序列的收款单。</span><span class="sxs-lookup"><span data-stu-id="4a106-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="4a106-136">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a106-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="4a106-137">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="4a106-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="4a106-138">在“费用币种”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4a106-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="4a106-139">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="4a106-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="4a106-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4a106-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="4a106-141">在“最小的逾期余额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4a106-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="4a106-142">在“天数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4a106-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="4a106-143">选中该复选框，以阻止客户进一步交货和开票。</span><span class="sxs-lookup"><span data-stu-id="4a106-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="4a106-144">若要解锁帐户，则在客户页的“开票和交货暂停”字段中选择“不”。</span><span class="sxs-lookup"><span data-stu-id="4a106-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="4a106-145">展开“注意”快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="4a106-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="4a106-146">输入显示在所选收款单代码的收款单文本。</span><span class="sxs-lookup"><span data-stu-id="4a106-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="4a106-147">您可以应用注释框上方的“翻译菜单”将此文本翻译为多种语言。</span><span class="sxs-lookup"><span data-stu-id="4a106-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  

