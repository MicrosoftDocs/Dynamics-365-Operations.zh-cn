---
title: 创建普通发票
description: 本主题说明如何创建普通发票。
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f6ee6fda0b52b8af7c253b7d22e470345a8a421f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "332234"
---
# <a name="create-free-text-invoices"></a><span data-ttu-id="2ba17-103">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="2ba17-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ba17-104">本主题说明如何创建普通发票。</span><span class="sxs-lookup"><span data-stu-id="2ba17-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="2ba17-105">对于本流程，使用了 **USMF** 演示公司数据。</span><span class="sxs-lookup"><span data-stu-id="2ba17-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="2ba17-106">创建普通发票</span><span class="sxs-lookup"><span data-stu-id="2ba17-106">Create a free text invoice</span></span>

1. <span data-ttu-id="2ba17-107">转到**应收帐款 \> 发票 \> 所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="2ba17-108">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-108">Select **New**.</span></span>
3. <span data-ttu-id="2ba17-109">在**客户帐户**字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="2ba17-110">默认情况下，选作客户帐户的帐户用作发票帐户。</span><span class="sxs-lookup"><span data-stu-id="2ba17-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="2ba17-111">如果发票未过帐，会计状态最开始为**进行中**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="2ba17-112">发票过帐后，将分配发票编号。</span><span class="sxs-lookup"><span data-stu-id="2ba17-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="2ba17-113">如果您使用单一欧元支付区 (SEPA) 授权，当您选择客户帐户时，将自动输入直接借记授权。</span><span class="sxs-lookup"><span data-stu-id="2ba17-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="2ba17-114">在**描述**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="2ba17-115">在**主科目**字段中，指定没有维度的帐号。</span><span class="sxs-lookup"><span data-stu-id="2ba17-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="2ba17-116">本主题的后文将输入维度。</span><span class="sxs-lookup"><span data-stu-id="2ba17-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="2ba17-117">还可以为主科目输入一个或多个字符，并使用查找功能查找科目。</span><span class="sxs-lookup"><span data-stu-id="2ba17-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="2ba17-118">选择**行明细**快速选项卡，以便将维度添加到主科目。</span><span class="sxs-lookup"><span data-stu-id="2ba17-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="2ba17-119">选择**财务维度行**选项卡。</span><span class="sxs-lookup"><span data-stu-id="2ba17-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="2ba17-120">这些维度仅适用于所选行。</span><span class="sxs-lookup"><span data-stu-id="2ba17-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="2ba17-121">销售税组根据客户填充。</span><span class="sxs-lookup"><span data-stu-id="2ba17-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="2ba17-122">如果客户没有销售税组，则使用主科目的销售税组。</span><span class="sxs-lookup"><span data-stu-id="2ba17-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="2ba17-123">物料销售税组根据主科目填充。</span><span class="sxs-lookup"><span data-stu-id="2ba17-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="2ba17-124">如果主科目没有物料销售税组，则使用总帐中销售税参数中指定的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="2ba17-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="2ba17-125">可选：在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2ba17-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="2ba17-126">可选：在**单价**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2ba17-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="2ba17-127">此金额计算为数量乘以单位价格。</span><span class="sxs-lookup"><span data-stu-id="2ba17-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="2ba17-128">不过，可以通过输入一个金额覆盖该计算值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="2ba17-129">选择**销售税**查看为发票计算的销售税。</span><span class="sxs-lookup"><span data-stu-id="2ba17-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="2ba17-130">可在此页查看销售税金额，您也可以在**调整**选项卡上覆盖这些金额。</span><span class="sxs-lookup"><span data-stu-id="2ba17-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="2ba17-131">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-131">Select **OK**.</span></span>
12. <span data-ttu-id="2ba17-132">选择**费用**，以添加费用到发票中。</span><span class="sxs-lookup"><span data-stu-id="2ba17-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="2ba17-133">在**费用代码**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="2ba17-134">在**费用数值**字段中，输入一个数目。</span><span class="sxs-lookup"><span data-stu-id="2ba17-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="2ba17-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2ba17-135">Close the page.</span></span>
16. <span data-ttu-id="2ba17-136">选择**总计**查看发票详细信息和总计的汇总。</span><span class="sxs-lookup"><span data-stu-id="2ba17-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="2ba17-137">选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-137">Select **Close**.</span></span>
18. <span data-ttu-id="2ba17-138">选择**过帐**过帐发票。</span><span class="sxs-lookup"><span data-stu-id="2ba17-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="2ba17-139">可以在真正过帐前取消。</span><span class="sxs-lookup"><span data-stu-id="2ba17-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="2ba17-140">可以更改发票打印的计时。</span><span class="sxs-lookup"><span data-stu-id="2ba17-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="2ba17-141">选择**当前**以在更新各发票时打印。</span><span class="sxs-lookup"><span data-stu-id="2ba17-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="2ba17-142">选择**之后**则在更新所有发票后打印。</span><span class="sxs-lookup"><span data-stu-id="2ba17-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="2ba17-143">若要更改过帐前如何验证客户的信用额度，请更改**信用额度类型**字段中的值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="2ba17-144">若要打印发票，请将选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="2ba17-145">若要过帐发票，请将选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="2ba17-146">您可以打印未过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="2ba17-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="2ba17-147">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="2ba17-148">复制行</span><span class="sxs-lookup"><span data-stu-id="2ba17-148">Copy lines</span></span>
<span data-ttu-id="2ba17-149">若要复制普通发票中的行，请选择一行或多行，然后选择**复制所选行**。</span><span class="sxs-lookup"><span data-stu-id="2ba17-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="2ba17-150">可以指定要创建的副本数量，也可以复制注释和附件。</span><span class="sxs-lookup"><span data-stu-id="2ba17-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="2ba17-151">可以复制分配或允许在过帐时重新创建分配。</span><span class="sxs-lookup"><span data-stu-id="2ba17-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="2ba17-152">复制行之后，可以根据需要编辑信息。</span><span class="sxs-lookup"><span data-stu-id="2ba17-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="2ba17-153">通过模板创建普通发票</span><span class="sxs-lookup"><span data-stu-id="2ba17-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="2ba17-154">您可以通过模板创建普通发票。</span><span class="sxs-lookup"><span data-stu-id="2ba17-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="2ba17-155">如果从**发票**选项卡选择**从模板新建**，则可为新普通发票选择模板名称和客户帐户。</span><span class="sxs-lookup"><span data-stu-id="2ba17-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="2ba17-156">可以根据客户自动填充默认值（如付款期限和付款方式），也可以使用随模板保存的值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="2ba17-157">将创建新的普通发票，而您可以根据需要编辑值。</span><span class="sxs-lookup"><span data-stu-id="2ba17-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
