--- 
title: "在发票日记帐中记录供应商发票"
description: "此任务指南将显示如何记录与采购订单无关的供应商发票。"
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="14a46-103">在发票日记帐中记录供应商发票</span><span class="sxs-lookup"><span data-stu-id="14a46-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14a46-104">此任务指南将显示如何记录与采购订单无关的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="14a46-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="14a46-105">此类型发票的示例包括货物供应或服务的费用。</span><span class="sxs-lookup"><span data-stu-id="14a46-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="14a46-106">此记录使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="14a46-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="14a46-107">转到“应付账款”>“工作区”>“供应商发票条目”。</span><span class="sxs-lookup"><span data-stu-id="14a46-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="14a46-108">单击“新发票日记帐”。</span><span class="sxs-lookup"><span data-stu-id="14a46-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="14a46-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="14a46-109">Click New.</span></span>
4. <span data-ttu-id="14a46-110">在“名称”字段中，输入日记帐名称或单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="14a46-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="14a46-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="14a46-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="14a46-112">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="14a46-112">Click Lines.</span></span>
    * <span data-ttu-id="14a46-113">在“日期”字段中，输入要更新总帐的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="14a46-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="14a46-114">在“帐户”字段中，指定供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="14a46-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="14a46-115">在“发票”字段中，输入发票编号。</span><span class="sxs-lookup"><span data-stu-id="14a46-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="14a46-116">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="14a46-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="14a46-117">在“信用”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="14a46-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="14a46-118">在“抵销帐户”字段中，输入科目编号或单击下拉按钮以打开查找</span><span class="sxs-lookup"><span data-stu-id="14a46-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="14a46-119">销售税组将会根据供应商帐户默认显示。</span><span class="sxs-lookup"><span data-stu-id="14a46-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="14a46-120">物料销售税组将默认为“抵销帐户”字段中指定的主科目信息。</span><span class="sxs-lookup"><span data-stu-id="14a46-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="14a46-121">“到期日期”将根据“付款期限”计算。</span><span class="sxs-lookup"><span data-stu-id="14a46-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="14a46-122">现金折扣将默认为供应商帐户信息。</span><span class="sxs-lookup"><span data-stu-id="14a46-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="14a46-123">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="14a46-123">Click Post.</span></span>
13. <span data-ttu-id="14a46-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14a46-124">Close the page.</span></span>


