---
title: 创建普通发票模板
description: 此过程说明如何创建普通发票模板。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8281de3cb336d9392a6a97f98e51a2a139a384c5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189123"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="d466d-103">创建普通发票模板</span><span class="sxs-lookup"><span data-stu-id="d466d-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d466d-104">对于本演练，请使用 USMF 演示公司数据。</span><span class="sxs-lookup"><span data-stu-id="d466d-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="d466d-105">该过程由负责管理和处理“应收账款”发票的用户负责。</span><span class="sxs-lookup"><span data-stu-id="d466d-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="d466d-106">创建模板</span><span class="sxs-lookup"><span data-stu-id="d466d-106">Create a template</span></span>

1. <span data-ttu-id="d466d-107">转到“应收账款”>“发票”>“循环发票”>“普通发票模板”。</span><span class="sxs-lookup"><span data-stu-id="d466d-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="d466d-108">使用此窗体创建普通发票模板，可包括发票行、费用、会计分配模板和分类帐户信息。</span><span class="sxs-lookup"><span data-stu-id="d466d-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="d466d-109">单击“新建”，创建新的普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="d466d-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="d466d-110">在“模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d466d-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="d466d-111">“模板名称”为一个普通发票模板的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="d466d-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="d466d-112">两个模板不能具有相同的“模板名称”。</span><span class="sxs-lookup"><span data-stu-id="d466d-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="d466d-113">在“描述”字段中，输入模板组描述。</span><span class="sxs-lookup"><span data-stu-id="d466d-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="d466d-114">展开“发票行”的选项卡。</span><span class="sxs-lookup"><span data-stu-id="d466d-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="d466d-115">在“描述”字段中，输入发票行描述。</span><span class="sxs-lookup"><span data-stu-id="d466d-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="d466d-116">在“主要帐户”字段中，选择一个收入帐户。</span><span class="sxs-lookup"><span data-stu-id="d466d-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="d466d-117">您可以在选择的客户抵消交易帐户，来确定客户过帐模板页的发票总额。</span><span class="sxs-lookup"><span data-stu-id="d466d-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="d466d-118">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d466d-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d466d-119">当前发票行的销售税组，是客户帐户的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="d466d-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="d466d-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d466d-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d466d-121">在“物料税务组”字段中，选择当前发票行的物料销售税额。</span><span class="sxs-lookup"><span data-stu-id="d466d-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="d466d-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d466d-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d466d-123">在“单位价格”字段中，输入或查看发票行的每计价单位的价格。</span><span class="sxs-lookup"><span data-stu-id="d466d-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="d466d-124">此金额乘以“数量”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="d466d-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="d466d-125">在普通发票模板上添加新行。</span><span class="sxs-lookup"><span data-stu-id="d466d-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="d466d-126">在“描述”字段中，输入发票行描述。</span><span class="sxs-lookup"><span data-stu-id="d466d-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="d466d-127">在“主要帐户”字段中，选择一个收入帐户。</span><span class="sxs-lookup"><span data-stu-id="d466d-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="d466d-128">您可以在选择的客户抵消交易帐户，来确定客户过帐模板页的发票总额。</span><span class="sxs-lookup"><span data-stu-id="d466d-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="d466d-129">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d466d-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d466d-130">当前发票行的销售税组，是客户帐户的默认销售税组。</span><span class="sxs-lookup"><span data-stu-id="d466d-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="d466d-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d466d-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d466d-132">在“物料销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d466d-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d466d-133">当前发票行的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="d466d-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="d466d-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d466d-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d466d-135">输入或查看发票行的单位数。</span><span class="sxs-lookup"><span data-stu-id="d466d-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="d466d-136">该数字乘以“单位价格”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="d466d-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="d466d-137">输入或查看发票行的单位价格。</span><span class="sxs-lookup"><span data-stu-id="d466d-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="d466d-138">该金额乘以“数量”字段中的值来确定发票行金额。</span><span class="sxs-lookup"><span data-stu-id="d466d-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="d466d-139">查看和修改单独行和所有子行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="d466d-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="d466d-140">会计分配定义如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。</span><span class="sxs-lookup"><span data-stu-id="d466d-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="d466d-141">更新已选发票行的会计分配。</span><span class="sxs-lookup"><span data-stu-id="d466d-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="d466d-142">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="d466d-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="d466d-143">将普通发票保存为模板</span><span class="sxs-lookup"><span data-stu-id="d466d-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="d466d-144">也可以将现有普通发票保存为模板。</span><span class="sxs-lookup"><span data-stu-id="d466d-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="d466d-145">从“发票”选项卡选择“保存到模板”时，请为模板提供名称和说明。</span><span class="sxs-lookup"><span data-stu-id="d466d-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="d466d-146">如果有同名模板，将看到通知，说明已存在该名称的模板。</span><span class="sxs-lookup"><span data-stu-id="d466d-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="d466d-147">仍然可以单击“确定”替换该模板。</span><span class="sxs-lookup"><span data-stu-id="d466d-147">You can still click on Ok to replace it.</span></span> 
