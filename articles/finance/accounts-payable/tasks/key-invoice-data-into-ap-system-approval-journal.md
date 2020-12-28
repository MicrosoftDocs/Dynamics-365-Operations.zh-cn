---
title: 使用审核日记帐将发票数据键入应付帐款
description: 此主题介绍如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788397b5c9a3f42e373f7cdad256c1ee3d058e57
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440590"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="b9614-103">使用审核日记帐将发票数据键入应付帐款</span><span class="sxs-lookup"><span data-stu-id="b9614-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9614-104">此主题介绍如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。</span><span class="sxs-lookup"><span data-stu-id="b9614-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="b9614-105">创建并过帐发票</span><span class="sxs-lookup"><span data-stu-id="b9614-105">Create and post and invoice</span></span>
1. <span data-ttu-id="b9614-106">在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票登记簿**。</span><span class="sxs-lookup"><span data-stu-id="b9614-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="b9614-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b9614-107">Select **New**.</span></span>
3. <span data-ttu-id="b9614-108">选择您想要使用的发票登记簿名称。</span><span class="sxs-lookup"><span data-stu-id="b9614-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="b9614-109">单击 **行**，以打开登记簿和输入费用行。</span><span class="sxs-lookup"><span data-stu-id="b9614-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="b9614-110">选择某一供应商。</span><span class="sxs-lookup"><span data-stu-id="b9614-110">Select a vendor.</span></span> <span data-ttu-id="b9614-111">例如，输入或选择 `US-104`。</span><span class="sxs-lookup"><span data-stu-id="b9614-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="b9614-112">在 **发票** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b9614-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="b9614-113">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b9614-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="b9614-114">在 **信用** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="b9614-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="b9614-115">在 **审核人** 字段中，从下拉菜单中选择一个审核人。</span><span class="sxs-lookup"><span data-stu-id="b9614-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="b9614-116">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="b9614-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="b9614-117">审核发票</span><span class="sxs-lookup"><span data-stu-id="b9614-117">Approve an invoice</span></span>
1. <span data-ttu-id="b9614-118">在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票审核**。</span><span class="sxs-lookup"><span data-stu-id="b9614-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="b9614-119">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b9614-119">Select **New**.</span></span>
3. <span data-ttu-id="b9614-120">选择您想要使用的发票审核日记帐的名称。</span><span class="sxs-lookup"><span data-stu-id="b9614-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="b9614-121">选择 **行**，以显示可以选择要审核发票的页面。</span><span class="sxs-lookup"><span data-stu-id="b9614-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="b9614-122">选择 **查找凭证**，以显示可供审核的所有发票。</span><span class="sxs-lookup"><span data-stu-id="b9614-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="b9614-123">标记您创建的发票，然后单击 **选择**。</span><span class="sxs-lookup"><span data-stu-id="b9614-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="b9614-124">选中后，您选择的以上凭证将移动到此列表中。</span><span class="sxs-lookup"><span data-stu-id="b9614-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="b9614-125">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9614-125">Select **OK**.</span></span>
8. <span data-ttu-id="b9614-126">单击 **帐号** 字段，以添加费用帐户到发票中。</span><span class="sxs-lookup"><span data-stu-id="b9614-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="b9614-127">输入一个帐号，并关闭该字段。</span><span class="sxs-lookup"><span data-stu-id="b9614-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="b9614-128">例如，输入 `600120`。</span><span class="sxs-lookup"><span data-stu-id="b9614-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="b9614-129">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="b9614-129">Select **Post**.</span></span>
11. <span data-ttu-id="b9614-130">选择 **凭证** 查看已过帐条目。</span><span class="sxs-lookup"><span data-stu-id="b9614-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="b9614-131">发票待定审核帐户被冲销，并替换成实际费用帐户。</span><span class="sxs-lookup"><span data-stu-id="b9614-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

