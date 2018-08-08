--- 
title: "创建普通发票"
description: "本文说明如何创建普通发票。"
author: mikefalkner
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
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="d2f35-103">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="d2f35-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2f35-104">本文说明如何创建普通发票。</span><span class="sxs-lookup"><span data-stu-id="d2f35-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="d2f35-105">对于本流程，使用了 USMF 演示公司数据。</span><span class="sxs-lookup"><span data-stu-id="d2f35-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="d2f35-106">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="d2f35-106">Create a free text invoice</span></span>

1. <span data-ttu-id="d2f35-107">转到“应收账款”>“发票”>“所有普通发票”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="d2f35-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-108">Click New.</span></span>
3. <span data-ttu-id="d2f35-109">在“客户帐户”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d2f35-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="d2f35-110">发票帐户将默认为用于客户帐户的同一帐户。</span><span class="sxs-lookup"><span data-stu-id="d2f35-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="d2f35-111">如果发票未过帐，会计状态最开始为“进行中”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="d2f35-112">发票过帐后，将分配发票编号。</span><span class="sxs-lookup"><span data-stu-id="d2f35-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="d2f35-113">如果您使用 SEPA 授权，当您选择客户帐户时，直接借记授权将自动填充授权。</span><span class="sxs-lookup"><span data-stu-id="d2f35-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="d2f35-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d2f35-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d2f35-115">在“主科目”字段中，指定没有维度的帐号。</span><span class="sxs-lookup"><span data-stu-id="d2f35-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="d2f35-116">您还可以为主科目输入一个或多个字符，并使用查找功能查找科目。</span><span class="sxs-lookup"><span data-stu-id="d2f35-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="d2f35-117">您稍后将在此指南输入维度。</span><span class="sxs-lookup"><span data-stu-id="d2f35-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="d2f35-118">展开“行明细”快速选项卡，以便您可以将维度添加到主科目。</span><span class="sxs-lookup"><span data-stu-id="d2f35-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="d2f35-119">单击“财务维度行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d2f35-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="d2f35-120">这些维度仅适用于所选行。</span><span class="sxs-lookup"><span data-stu-id="d2f35-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="d2f35-121">销售税组将从客户处填充信息。</span><span class="sxs-lookup"><span data-stu-id="d2f35-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="d2f35-122">如果客户没有销售税组，则使用主科目的销售税组信息。</span><span class="sxs-lookup"><span data-stu-id="d2f35-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="d2f35-123">物料销售税组根据主科目填充。</span><span class="sxs-lookup"><span data-stu-id="d2f35-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="d2f35-124">如果主科目没有物料销售税组，则使用“总帐中销售税参数”中的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="d2f35-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="d2f35-125">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d2f35-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d2f35-126">数量为可选项。</span><span class="sxs-lookup"><span data-stu-id="d2f35-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="d2f35-127">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d2f35-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="d2f35-128">单位价格为可选项。</span><span class="sxs-lookup"><span data-stu-id="d2f35-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="d2f35-129">此金额计算为数量乘以单位价格。</span><span class="sxs-lookup"><span data-stu-id="d2f35-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="d2f35-130">不过，您可以覆盖计算值，另外输入一个金额。</span><span class="sxs-lookup"><span data-stu-id="d2f35-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="d2f35-131">单击“销售税”查看为您的发票计算的销售税。</span><span class="sxs-lookup"><span data-stu-id="d2f35-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="d2f35-132">在此页查看销售税金额，您也可以在“调整”选项卡上覆盖这些金额。</span><span class="sxs-lookup"><span data-stu-id="d2f35-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="d2f35-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-133">Click OK.</span></span>
12. <span data-ttu-id="d2f35-134">单击“费用”，以添加费用到您的发票中。</span><span class="sxs-lookup"><span data-stu-id="d2f35-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="d2f35-135">在“费用代码”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d2f35-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="d2f35-136">在“费用数值”字段中，输入一个数目。</span><span class="sxs-lookup"><span data-stu-id="d2f35-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="d2f35-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d2f35-137">Close the page.</span></span>
16. <span data-ttu-id="d2f35-138">单击“总计”查看汇总的发票详细信息和总计。</span><span class="sxs-lookup"><span data-stu-id="d2f35-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="d2f35-139">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-139">Click Close.</span></span>
18. <span data-ttu-id="d2f35-140">单击“过帐”过帐该发票。</span><span class="sxs-lookup"><span data-stu-id="d2f35-140">Click Post to post the invoice.</span></span> <span data-ttu-id="d2f35-141">在过帐前，您可以取消。</span><span class="sxs-lookup"><span data-stu-id="d2f35-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="d2f35-142">更改发票打印时的时间：选择“当前”（各发票更新后即打印），或选择“之后”（在更新所有发票后打印）。</span><span class="sxs-lookup"><span data-stu-id="d2f35-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="d2f35-143">如果要更改过帐前客户信用额度的检查方式，则更改“信用额度”类型。</span><span class="sxs-lookup"><span data-stu-id="d2f35-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="d2f35-144">如果您要打印发票，则选择“是”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="d2f35-145">如果您要将发票过帐，则选择“是”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="d2f35-146">您可以打印未过帐发票。</span><span class="sxs-lookup"><span data-stu-id="d2f35-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="d2f35-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="d2f35-148">复制行</span><span class="sxs-lookup"><span data-stu-id="d2f35-148">Copy lines</span></span>
<span data-ttu-id="d2f35-149">若要复制普通发票中的行，请选择一行或多行，然后单击“复制所选行”。</span><span class="sxs-lookup"><span data-stu-id="d2f35-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="d2f35-150">可以指定要创建的副本数量，也可以复制注释和附件。</span><span class="sxs-lookup"><span data-stu-id="d2f35-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="d2f35-151">可以复制分配或允许在过帐时重新创建分配。</span><span class="sxs-lookup"><span data-stu-id="d2f35-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="d2f35-152">复制行之后，可以根据需要编辑信息。</span><span class="sxs-lookup"><span data-stu-id="d2f35-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="d2f35-153">通过模板创建普通发票</span><span class="sxs-lookup"><span data-stu-id="d2f35-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="d2f35-154">您可以通过模板创建普通发票。</span><span class="sxs-lookup"><span data-stu-id="d2f35-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="d2f35-155">如果从“发票”选项卡选择“从模板新建”，则可为新普通发票选择模板名称和客户帐户。</span><span class="sxs-lookup"><span data-stu-id="d2f35-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="d2f35-156">也可以从客户选择默认值（如付款期限和付款方式），或使用随模板保存的值。</span><span class="sxs-lookup"><span data-stu-id="d2f35-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="d2f35-157">将创建新的普通发票，而您可以编辑该发票中的值。</span><span class="sxs-lookup"><span data-stu-id="d2f35-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


