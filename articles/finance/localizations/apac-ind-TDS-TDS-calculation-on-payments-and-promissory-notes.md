---
title: 根据付款和本票的 TDS 计算
description: 本主题提供有关计算从源扣缴税款 (TDS) 的不同付款交易的参考信息。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ea57963e41b90bbc11efa00b85aad8bc60c2357d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023060"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a><span data-ttu-id="7cb26-103">根据付款和本票的 TDS 计算</span><span class="sxs-lookup"><span data-stu-id="7cb26-103">TDS calculation on payments and promissory notes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cb26-104">本主题提供有关计算从源扣缴税款 (TDS) 的不同付款交易的参考信息。</span><span class="sxs-lookup"><span data-stu-id="7cb26-104">This topic provides reference information about the different payment transactions that Tax Deducted at Source (TDS) is calculated on.</span></span>

| <span data-ttu-id="7cb26-105">序列号</span><span class="sxs-lookup"><span data-stu-id="7cb26-105">Serial number</span></span> | <span data-ttu-id="7cb26-106">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="7cb26-106">Transaction type</span></span> | <span data-ttu-id="7cb26-107">交易记录金额</span><span class="sxs-lookup"><span data-stu-id="7cb26-107">Transaction amount</span></span> | <span data-ttu-id="7cb26-108">页面名称和路径</span><span class="sxs-lookup"><span data-stu-id="7cb26-108">Page name and path</span></span> | <span data-ttu-id="7cb26-109">帐户类型和抵销帐户类型</span><span class="sxs-lookup"><span data-stu-id="7cb26-109">Account type and offset account type</span></span> |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| <span data-ttu-id="7cb26-110">1</span><span class="sxs-lookup"><span data-stu-id="7cb26-110">1</span></span>             | <span data-ttu-id="7cb26-111">针对发票的预先付款/付款（应付 TDS）</span><span class="sxs-lookup"><span data-stu-id="7cb26-111">Advance payment/Payment against invoice (TDS payable)</span></span> | <span data-ttu-id="7cb26-112">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7cb26-112">Debit or Credit</span></span> | <ul><li><span data-ttu-id="7cb26-113">普通日记帐（**总帐 \> 日记帐条目 \> 普通日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-113">General journal (**General ledger \> Journal entries \> General journals**)</span></span></li><li><span data-ttu-id="7cb26-114">发票日记帐（**应付帐款 \> 发票 \> 发票日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-114">Invoice journal (**Accounts payable \> Invoices \> Invoice journal**)</span></span></li><li><span data-ttu-id="7cb26-115">付款日记帐（**应付帐款 \> 付款 \> 供应商付款日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-115">Payment journal (**Accounts payable \> Payments \> Vendor payment journal**)</span></span></li></ul> | <span data-ttu-id="7cb26-116">供应商 (Dr.)，银行 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7cb26-116">Vendor (Dr.), Bank (Cr.)</span></span> |
| <span data-ttu-id="7cb26-117">2</span><span class="sxs-lookup"><span data-stu-id="7cb26-117">2</span></span>             | <span data-ttu-id="7cb26-118">针对发票的预先付款/付款（从客户进行的购买 – 应付 TDS）</span><span class="sxs-lookup"><span data-stu-id="7cb26-118">Advance payment/Payment against invoice (Purchase made from customer – TDS payable)</span></span> | <span data-ttu-id="7cb26-119">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7cb26-119">Debit or Credit</span></span> | <ul><li><span data-ttu-id="7cb26-120">普通日记帐（**总帐 \> 日记帐条目 \> 普通日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-120">General journal (**General ledger \> Journal entries \> General journals**)</span></span></li><li><span data-ttu-id="7cb26-121">发票日记帐（**应付帐款 \> 发票 \> 发票日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-121">Invoice journal (**Accounts payable \> Invoices \> Invoice journal**)</span></span></li><li><span data-ttu-id="7cb26-122">付款日记帐（**应付帐款 \> 付款 \> 供应商付款日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-122">Payment journal (**Accounts payable \> Payments \> Vendor payment journal**)</span></span></li></ul> | <span data-ttu-id="7cb26-123">客户 (Dr.)，银行 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7cb26-123">Customer (Dr.), Bank (Cr.)</span></span> |
| <span data-ttu-id="7cb26-124">3</span><span class="sxs-lookup"><span data-stu-id="7cb26-124">3</span></span>             | <span data-ttu-id="7cb26-125">本票</span><span class="sxs-lookup"><span data-stu-id="7cb26-125">Promissory notes</span></span> | <span data-ttu-id="7cb26-126">借记</span><span class="sxs-lookup"><span data-stu-id="7cb26-126">Debit</span></span> | <span data-ttu-id="7cb26-127">签发本票日记帐（**应付帐款 \> 付款 \> 本票 \> 签发本票日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-127">Draw promissory note journal (**Accounts payable \> Payments \> Promissory notes \> Draw promissory note journal**)</span></span> | <span data-ttu-id="7cb26-128">供应商 (Dr.)，分类帐 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7cb26-128">Vendor (Dr.), Ledger (Cr.)</span></span> |
| <span data-ttu-id="7cb26-129">4</span><span class="sxs-lookup"><span data-stu-id="7cb26-129">4</span></span>             | <span data-ttu-id="7cb26-130">其他收入（应收 TDS）</span><span class="sxs-lookup"><span data-stu-id="7cb26-130">Miscellaneous income (TDS receivable)</span></span> | <span data-ttu-id="7cb26-131">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7cb26-131">Debit or Credit</span></span> | <span data-ttu-id="7cb26-132">普通日记帐（**总帐 \> 日记帐条目 \> 普通日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-132">General journal (**General ledger \> Journal entries \> General journals**)</span></span> | <span data-ttu-id="7cb26-133">银行 (Dr.)，分类帐 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7cb26-133">Bank (Dr.), Ledger (Cr.)</span></span> |
| <span data-ttu-id="7cb26-134">5</span><span class="sxs-lookup"><span data-stu-id="7cb26-134">5</span></span>             | <span data-ttu-id="7cb26-135">其他支出（应付 TDS）</span><span class="sxs-lookup"><span data-stu-id="7cb26-135">Other expenses (TDS payable)</span></span> | <span data-ttu-id="7cb26-136">借方或贷方</span><span class="sxs-lookup"><span data-stu-id="7cb26-136">Debit or Credit</span></span> | <span data-ttu-id="7cb26-137">普通日记帐（**总帐 \> 日记帐条目 \> 普通日记帐**）</span><span class="sxs-lookup"><span data-stu-id="7cb26-137">General journal (**General ledger \> Journal entries \> General journals**)</span></span> | <span data-ttu-id="7cb26-138">银行 (Dr.)，分类帐 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="7cb26-138">Bank (Dr.), Ledger (Cr.)</span></span> |

<span data-ttu-id="7cb26-139">按照以下步骤根据付款和本票计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="7cb26-139">Follow these steps to calculate TDS on payments and promissory notes.</span></span>

1. <span data-ttu-id="7cb26-140">在日记帐页面上，创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="7cb26-140">On the journal pages, create journal lines.</span></span> <span data-ttu-id="7cb26-141">选择帐户类型和抵销帐户类型。</span><span class="sxs-lookup"><span data-stu-id="7cb26-141">Select the account type and offset account type.</span></span>
2. <span data-ttu-id="7cb26-142">选择 **功能 \> 结算** 以打开 **未结交易编辑** 页面。</span><span class="sxs-lookup"><span data-stu-id="7cb26-142">Select **Functions \> Settlement** to open the **Open transaction editing** page.</span></span> <span data-ttu-id="7cb26-143">然后，选择必须结算的特定发票。</span><span class="sxs-lookup"><span data-stu-id="7cb26-143">Then select a specific invoice that must be settled.</span></span> <span data-ttu-id="7cb26-144">如果已经在发票级别计算了 TDS，**金额起点** 字段显示计算 TDS 的基数金额。</span><span class="sxs-lookup"><span data-stu-id="7cb26-144">If TDS has already been calculated at the invoice level, the **Amount origin** field shows the base amount that the TDS was calculated on.</span></span> <span data-ttu-id="7cb26-145">**TDS 金额** 字段显示为交易计算的 TDS 金额。</span><span class="sxs-lookup"><span data-stu-id="7cb26-145">The **TDS amount** field shows the TDS amount that was calculated for the transaction.</span></span> <span data-ttu-id="7cb26-146">**金额** 字段显示净付款金额（即，扣除 TDS 之后的付款金额）。</span><span class="sxs-lookup"><span data-stu-id="7cb26-146">The **Amount** field shows the net payment amount (that is, the payment amount after TDS is deducted).</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cb26-147">对于已针对发票进行的付款，应用以下条件：</span><span class="sxs-lookup"><span data-stu-id="7cb26-147">For a payment that was made against an invoice, the following conditions apply:</span></span>
    >
    > - <span data-ttu-id="7cb26-148">如果付款金额和发票金额相同，当已在发票级别上计算了 TDS 时，将不会再计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="7cb26-148">If the payment amount and the invoice amount are the same, TDS isn't calculated if it has already been calculated at the invoice level.</span></span>
    > - <span data-ttu-id="7cb26-149">如果扣除 TDS 金额之后的发票金额大于付款金额，将不会计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="7cb26-149">If the invoice amount after the TDS amount is deducted is more than the payment amount, TDS isn't calculated.</span></span>
    > - <span data-ttu-id="7cb26-150">如果扣除 TDS 金额之后的发票金额小于付款金额，将根据超出发票金额的金额计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="7cb26-150">If the invoice amount after the TDS amount is deducted is less than the payment amount, TDS is calculated on the amount that exceeds the invoice amount.</span></span>

3. <span data-ttu-id="7cb26-151">在 **日记帐凭证** 页面的 **概述** 选项卡上，在 **TDS 组** 字段中，查看或更改为供应商或客户定义的默认 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="7cb26-151">On the **Journal voucher** page, on the **Overview** tab, in the **TDS groups** field, review or change the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="7cb26-152">在日记帐行上计算的 TDS 基于为 TDS 组中 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="7cb26-152">TDS that is calculated on journal lines is based on the formula that is defined for the TDS tax codes in the TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cb26-153">仅在 **供应商** 页面上为供应商将 **计算预缴税金** 选项设置为 **是** 时，才计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="7cb26-153">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the vendor on the **Vendors** page.</span></span>

4. <span data-ttu-id="7cb26-154">在 **税务信息** 选项卡的 **公司信息** 部分中，在 **名称** 字段中，您可以针对为公司设置的备用地址选择公司名称。</span><span class="sxs-lookup"><span data-stu-id="7cb26-154">On the **Tax information** tab, in the **Company information** section, in the **Name** field, you can select a company name for alternate addresses that are set up for the company.</span></span>

    <span data-ttu-id="7cb26-155">在 **预缴税金** 部分中，**评估对象的性质** 字段显示供应商或客户的评估对象类别的性质。</span><span class="sxs-lookup"><span data-stu-id="7cb26-155">In the **Withholding tax** section, the **Nature of assessee** field shows the nature of assessee category of the vendor or customer.</span></span> <span data-ttu-id="7cb26-156">**税务帐号 (TAN)** 字段显示选定公司的税务帐号 (TAN)。</span><span class="sxs-lookup"><span data-stu-id="7cb26-156">The **Tax account number (TAN)** field shows the tax account number (TAN) of the selected company.</span></span>

5. <span data-ttu-id="7cb26-157">选择 **预缴税金按钮 \> 预缴税金** 以打开 **临时预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="7cb26-157">Select **Withholding tax button \> withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="7cb26-158">此页面的上部具有以下字段：</span><span class="sxs-lookup"><span data-stu-id="7cb26-158">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="7cb26-159">**预缴税金总金额** – 已为 TDS 组的交易计算的总 TDS。</span><span class="sxs-lookup"><span data-stu-id="7cb26-159">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="7cb26-160">**值** – 已用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="7cb26-160">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="7cb26-161">总百分比基于为 TDS 税码定义和附加到 TDS 组的公式。</span><span class="sxs-lookup"><span data-stu-id="7cb26-161">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="7cb26-162">**调整后预缴税金总金额** – TDS 组中所有税码的调整后 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="7cb26-162">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="7cb26-163">**TDS** – 选中的复选框指示 TDS 组已附加到交易。</span><span class="sxs-lookup"><span data-stu-id="7cb26-163">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="7cb26-164">**概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。</span><span class="sxs-lookup"><span data-stu-id="7cb26-164">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

6. <span data-ttu-id="7cb26-165">选择 **阈值** 以打开 **阈值** 页面，您可以在该页面中查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制。</span><span class="sxs-lookup"><span data-stu-id="7cb26-165">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
7. <span data-ttu-id="7cb26-166">选择 **公式设计器** 以打开 **公式设计器** 页面，您可以在该页面中查看为特定 TDS 税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="7cb26-166">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
8. <span data-ttu-id="7cb26-167">关闭 **公式设计器** 和 **临时预缴税金交易** 页面以返回到 **日记帐凭证** 页面。</span><span class="sxs-lookup"><span data-stu-id="7cb26-167">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>
9. <span data-ttu-id="7cb26-168">验证和过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="7cb26-168">Validate and post the journal.</span></span> <span data-ttu-id="7cb26-169">已计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应付帐款。</span><span class="sxs-lookup"><span data-stu-id="7cb26-169">The TDS amount that was calculated is posted to the payable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="7cb26-170">TDS 税码的应收帐款在 **预缴税金代码** 页面上定义。</span><span class="sxs-lookup"><span data-stu-id="7cb26-170">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
10. <span data-ttu-id="7cb26-171">选择 **过帐的预缴税金** 以打开 **预缴税金交易** 页面。</span><span class="sxs-lookup"><span data-stu-id="7cb26-171">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="7cb26-172">**值** 字段显示用于计算交易的 TDS 的总百分比。</span><span class="sxs-lookup"><span data-stu-id="7cb26-172">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="7cb26-173">**概述**、**常规** 和 **金额** 选项卡上的字段显示已针对附加到交易的 TDS 组计算的 TDS 金额。</span><span class="sxs-lookup"><span data-stu-id="7cb26-173">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated for the TDS group that is attached to the transaction.</span></span>

11. <span data-ttu-id="7cb26-174">查看附加到 TDS 组的每个 TDS 税码的 TDS 计算信息。</span><span class="sxs-lookup"><span data-stu-id="7cb26-174">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>

## <a name="generate-payments"></a><span data-ttu-id="7cb26-175">生成付款</span><span class="sxs-lookup"><span data-stu-id="7cb26-175">Generate payments</span></span>

<span data-ttu-id="7cb26-176">若要生成付款，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7cb26-176">To generate payments, follow these steps.</span></span>

1. <span data-ttu-id="7cb26-177">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="7cb26-177">Follow one of these steps:</span></span>

    - <span data-ttu-id="7cb26-178">转到 **应付帐款 \> 付款 \> 供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-178">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>
    - <span data-ttu-id="7cb26-179">转到 **应收帐款 \> 付款 \> 客户付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-179">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
    - <span data-ttu-id="7cb26-180">转到 **应付帐款 \> 付款 \> 本票 \> 签发本票日记帐**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-180">Go to **Accounts payable \> Payments \> Promissory notes \> Draw promissory note journal**.</span></span>
    - <span data-ttu-id="7cb26-181">转到 **应收帐款 \> 付款 \> 汇票 \> 签发汇票日记帐**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-181">Go to **Accounts receivable \> Payments \> Bill of exchange \> Draw bill of exchange journal**.</span></span>
    - <span data-ttu-id="7cb26-182">转到 **应收帐款 \> 付款 \> 汇票 \> 重新签发汇票日记帐**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-182">Go to **Accounts receivable \> Payments \> Bill of exchange \> Redraw bill of exchange journal**.</span></span>

2. <span data-ttu-id="7cb26-183">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-183">Select **Lines**.</span></span>
3. <span data-ttu-id="7cb26-184">选择 **功能 \> 生成付款**。</span><span class="sxs-lookup"><span data-stu-id="7cb26-184">Select **Functions \> Generate payments**.</span></span>
