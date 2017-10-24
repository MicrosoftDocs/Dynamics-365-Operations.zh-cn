--- 
title: "使用审核日记帐将发票数据键入应付账款"
description: "此任务指南将显示如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。"
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="8289a-103">使用审核日记帐将发票数据键入应付账款</span><span class="sxs-lookup"><span data-stu-id="8289a-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8289a-104">此任务指南将显示如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。</span><span class="sxs-lookup"><span data-stu-id="8289a-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="8289a-105">创建并过帐发票</span><span class="sxs-lookup"><span data-stu-id="8289a-105">Create and post and invoice</span></span>
1. <span data-ttu-id="8289a-106">转到“应付账款”>“发票”>“发票登记簿”。</span><span class="sxs-lookup"><span data-stu-id="8289a-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="8289a-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8289a-107">Click New.</span></span>
3. <span data-ttu-id="8289a-108">选择您想要使用的发票登记簿名称。</span><span class="sxs-lookup"><span data-stu-id="8289a-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="8289a-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8289a-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8289a-110">单击“行”，以打开登记簿和输入费用行。</span><span class="sxs-lookup"><span data-stu-id="8289a-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="8289a-111">选择某一供应商。</span><span class="sxs-lookup"><span data-stu-id="8289a-111">Select a vendor.</span></span> <span data-ttu-id="8289a-112">例如，输入或选择 US-104</span><span class="sxs-lookup"><span data-stu-id="8289a-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="8289a-113">在“发票”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="8289a-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="8289a-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8289a-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="8289a-115">在“信用”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="8289a-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="8289a-116">在“审核人”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="8289a-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8289a-117">突出显示一个审核人，然后单击“选择”以选择该审核人。</span><span class="sxs-lookup"><span data-stu-id="8289a-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="8289a-118">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="8289a-118">Click Post.</span></span>
13. <span data-ttu-id="8289a-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8289a-119">Close the page.</span></span>
14. <span data-ttu-id="8289a-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8289a-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="8289a-121">审核发票</span><span class="sxs-lookup"><span data-stu-id="8289a-121">Approve an invoice</span></span>
1. <span data-ttu-id="8289a-122">转到“应付账款”>“发票”>“发票审核”。</span><span class="sxs-lookup"><span data-stu-id="8289a-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="8289a-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8289a-123">Click New.</span></span>
3. <span data-ttu-id="8289a-124">选择您想要使用的发票审核日记帐的名称。</span><span class="sxs-lookup"><span data-stu-id="8289a-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="8289a-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8289a-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8289a-126">单击“行”，以显示可以选择要审核发票的页面。</span><span class="sxs-lookup"><span data-stu-id="8289a-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="8289a-127">选择“查找凭证”，以显示可供审核的所有发票。</span><span class="sxs-lookup"><span data-stu-id="8289a-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="8289a-128">标记您创建的发票。</span><span class="sxs-lookup"><span data-stu-id="8289a-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="8289a-129">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="8289a-129">Click Select.</span></span>
    * <span data-ttu-id="8289a-130">选中后，您选择的以上凭证将移动到此列表中。</span><span class="sxs-lookup"><span data-stu-id="8289a-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="8289a-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8289a-131">Click OK.</span></span>
10. <span data-ttu-id="8289a-132">单击“帐号”字段，以添加费用帐户到发票中。</span><span class="sxs-lookup"><span data-stu-id="8289a-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="8289a-133">输入一个帐号，并关闭该字段。</span><span class="sxs-lookup"><span data-stu-id="8289a-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="8289a-134">例如，输入 600120。</span><span class="sxs-lookup"><span data-stu-id="8289a-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="8289a-135">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="8289a-135">Click Post.</span></span>
13. <span data-ttu-id="8289a-136">单击“凭证”查看已过帐条目。</span><span class="sxs-lookup"><span data-stu-id="8289a-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="8289a-137">发票待定审核帐户被冲销，并替换成实际费用帐户。</span><span class="sxs-lookup"><span data-stu-id="8289a-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

