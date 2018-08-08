--- 
title: "创建普通发票模板"
description: "此过程说明如何创建普通发票模板。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 91f2ec2f8ab21616c6a1b886ee89d6faf84023e4
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="05e47-103">创建普通发票模板</span><span class="sxs-lookup"><span data-stu-id="05e47-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05e47-104">对于本演练，请使用 USMF 演示公司数据。</span><span class="sxs-lookup"><span data-stu-id="05e47-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="05e47-105">该过程由负责管理和处理“应收账款”发票的用户负责。</span><span class="sxs-lookup"><span data-stu-id="05e47-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="05e47-106">创建模板</span><span class="sxs-lookup"><span data-stu-id="05e47-106">Create a template</span></span>

1. <span data-ttu-id="05e47-107">转到“应收账款”>“发票”>“循环发票”>“普通发票模板”。</span><span class="sxs-lookup"><span data-stu-id="05e47-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="05e47-108">使用此窗体创建普通发票模板，可包括发票行、费用、会计分配模板和分类帐户信息。</span><span class="sxs-lookup"><span data-stu-id="05e47-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="05e47-109">单击“新建”，创建新的普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="05e47-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="05e47-110">在“模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="05e47-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="05e47-111">“模板名称”为一个普通发票模板的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="05e47-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="05e47-112">两个模板不能具有相同的“模板名称”。</span><span class="sxs-lookup"><span data-stu-id="05e47-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="05e47-113">在“描述”字段中，输入模板组描述。</span><span class="sxs-lookup"><span data-stu-id="05e47-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="05e47-114">展开“发票行”的选项卡。</span><span class="sxs-lookup"><span data-stu-id="05e47-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="05e47-115">在“描述”字段中，输入发票行描述。</span><span class="sxs-lookup"><span data-stu-id="05e47-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="05e47-116">在“主要帐户”字段中，选择一个收入帐户。</span><span class="sxs-lookup"><span data-stu-id="05e47-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="05e47-117">您可以在选择的客户抵消交易帐户，来确定客户过帐模板页的发票总额。</span><span class="sxs-lookup"><span data-stu-id="05e47-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="05e47-118">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="05e47-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="05e47-119">当前发票行的销售税组，是客户帐户的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="05e47-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="05e47-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="05e47-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="05e47-121">在“物料税务组”字段中，选择当前发票行的物料销售税额。</span><span class="sxs-lookup"><span data-stu-id="05e47-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="05e47-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="05e47-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="05e47-123">在“单位价格”字段中，输入或查看发票行的每计价单位的价格。</span><span class="sxs-lookup"><span data-stu-id="05e47-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="05e47-124">此金额乘以“数量”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="05e47-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="05e47-125">在普通发票模板上添加新行。</span><span class="sxs-lookup"><span data-stu-id="05e47-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="05e47-126">在“描述”字段中，输入发票行描述。</span><span class="sxs-lookup"><span data-stu-id="05e47-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="05e47-127">在“主要帐户”字段中，选择一个收入帐户。</span><span class="sxs-lookup"><span data-stu-id="05e47-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="05e47-128">您可以在选择的客户抵消交易帐户，来确定客户过帐模板页的发票总额。</span><span class="sxs-lookup"><span data-stu-id="05e47-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="05e47-129">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="05e47-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="05e47-130">当前发票行的销售税组，是客户帐户的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="05e47-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="05e47-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="05e47-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="05e47-132">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="05e47-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="05e47-133">当前发票行的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="05e47-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="05e47-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="05e47-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="05e47-135">输入或查看发票行的单位数。</span><span class="sxs-lookup"><span data-stu-id="05e47-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="05e47-136">该数字乘以“单位价格”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="05e47-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="05e47-137">输入或查看发票行的单位价格。</span><span class="sxs-lookup"><span data-stu-id="05e47-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="05e47-138">该金额乘以“数量”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="05e47-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="05e47-139">查看和修改单独行和所有子行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="05e47-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="05e47-140">会计分配定义如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。</span><span class="sxs-lookup"><span data-stu-id="05e47-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="05e47-141">更新已选发票行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="05e47-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="05e47-142">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="05e47-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="05e47-143">将普通发票保存为模板</span><span class="sxs-lookup"><span data-stu-id="05e47-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="05e47-144">也可以将现有普通发票保存为模板。</span><span class="sxs-lookup"><span data-stu-id="05e47-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="05e47-145">从“发票”选项卡选择“保存到模板”时，请为模板提供名称和说明。</span><span class="sxs-lookup"><span data-stu-id="05e47-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="05e47-146">如果有同名模板，将看到通知，说明已存在该名称的模板。</span><span class="sxs-lookup"><span data-stu-id="05e47-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="05e47-147">仍然可以单击“确定”替换该模板。</span><span class="sxs-lookup"><span data-stu-id="05e47-147">You can still click on Ok to replace it.</span></span> 

