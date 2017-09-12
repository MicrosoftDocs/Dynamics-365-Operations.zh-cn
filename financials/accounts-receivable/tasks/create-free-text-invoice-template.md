--- 
title: "创建普通发票模板"
description: "此记录使用 USMF 公司演示。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="74051-103">创建普通发票模板</span><span class="sxs-lookup"><span data-stu-id="74051-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74051-104">此记录使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="74051-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="74051-105">该记录由负责管理和处理“应收帐款”发票的用户负责。</span><span class="sxs-lookup"><span data-stu-id="74051-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="74051-106">转到“应收帐款”>“发票”>“循环发票”>“普通发票模板”。</span><span class="sxs-lookup"><span data-stu-id="74051-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="74051-107">使用此窗体创建普通发票模板，可包括发票行、费用、会计分配模板和分类帐户信息。</span><span class="sxs-lookup"><span data-stu-id="74051-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="74051-108">单击“新建”，创建新的普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="74051-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="74051-109">在“模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="74051-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="74051-110">“模板名称”为一个普通发票模板的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="74051-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="74051-111">两个模板不能具有相同的“模板名称”。</span><span class="sxs-lookup"><span data-stu-id="74051-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="74051-112">在“描述”字段中，输入模板组描述。</span><span class="sxs-lookup"><span data-stu-id="74051-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="74051-113">展开“发票行”的选项卡。</span><span class="sxs-lookup"><span data-stu-id="74051-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="74051-114">在“描述”字段中，输入发票行描述。</span><span class="sxs-lookup"><span data-stu-id="74051-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="74051-115">在“主要帐户”字段中，选择一个收入帐户。</span><span class="sxs-lookup"><span data-stu-id="74051-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="74051-116">您可以在选择的客户抵消交易帐户，来确定客户过帐模板页的发票总额。</span><span class="sxs-lookup"><span data-stu-id="74051-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="74051-117">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="74051-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="74051-118">当前发票行的销售税组，是客户帐户的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="74051-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="74051-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="74051-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="74051-120">在“物料税务组”字段中，选择当前发票行的物料销售税额。</span><span class="sxs-lookup"><span data-stu-id="74051-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="74051-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="74051-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="74051-122">在“单位价格”字段中，输入或查看发票行的每计价单位的价格。</span><span class="sxs-lookup"><span data-stu-id="74051-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="74051-123">此金额乘以“数量”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="74051-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="74051-124">在普通发票模板上添加新行。</span><span class="sxs-lookup"><span data-stu-id="74051-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="74051-125">在“描述”字段中，输入发票行描述。</span><span class="sxs-lookup"><span data-stu-id="74051-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="74051-126">在“主要帐户”字段中，选择一个收入帐户。</span><span class="sxs-lookup"><span data-stu-id="74051-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="74051-127">您可以在选择的客户抵消交易帐户，来确定客户过帐模板页的发票总额。</span><span class="sxs-lookup"><span data-stu-id="74051-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="74051-128">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="74051-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="74051-129">当前发票行的销售税组，是客户帐户的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="74051-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="74051-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="74051-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="74051-131">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="74051-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="74051-132">当前发票行的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="74051-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="74051-133">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="74051-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="74051-134">输入或查看发票行的单位数。</span><span class="sxs-lookup"><span data-stu-id="74051-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="74051-135">该数字乘以“单位价格”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="74051-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="74051-136">输入或查看发票行的单位价格。</span><span class="sxs-lookup"><span data-stu-id="74051-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="74051-137">该金额乘以“数量”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="74051-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="74051-138">查看和修改单独行和所有子行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="74051-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="74051-139">会计分配定义如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。</span><span class="sxs-lookup"><span data-stu-id="74051-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="74051-140">更新已选发票行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="74051-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="74051-141">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="74051-141">Click Close.</span></span>


