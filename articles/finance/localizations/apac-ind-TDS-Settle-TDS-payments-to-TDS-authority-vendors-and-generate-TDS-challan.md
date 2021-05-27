---
title: 向 TDS 主管机构供应商结算 TDS 付款并生成 TDS challan
description: 本主题说明如何向 TDS 主管机构供应商结算从源扣缴税款 (TDS) 付款。
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023065"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="1123d-103">向 TDS 主管机构供应商结算 TDS 付款并生成 TDS challan</span><span class="sxs-lookup"><span data-stu-id="1123d-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1123d-104">本主题说明如何向 TDS 主管机构供应商结算从源扣缴税款 (TDS) 付款。</span><span class="sxs-lookup"><span data-stu-id="1123d-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="1123d-105">转到 **应付帐款 \> 付款 \> 供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="1123d-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="1123d-106">[![供应商付款日记帐页](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="1123d-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="1123d-107">在 **供应商付款日记帐** 页面上，选择 **新建** 以创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="1123d-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="1123d-108">在 **帐户** 字段中，选择要向其结算 TDS 付款的 TDS 主管机构供应商。</span><span class="sxs-lookup"><span data-stu-id="1123d-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="1123d-109">选择 **结算交易** 以打开 **结算交易** 页面，您可以在该页面中查看 TDS 主管机构供应商的已结算 TDS 交易。</span><span class="sxs-lookup"><span data-stu-id="1123d-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="1123d-110">通过以下方式显示结算期间的已结算 TDS 交易：</span><span class="sxs-lookup"><span data-stu-id="1123d-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="1123d-111">评估对象类别的性质为 **公司** 的 TDS 交易显示为一个交易行。</span><span class="sxs-lookup"><span data-stu-id="1123d-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="1123d-112">评估对象类别的性质为 **HUF**、**事务所**、**个人**、**AOP**、**BOI**、**本地主管机构** 或 **其他** 的 TDS 交易显示为一个交易行。</span><span class="sxs-lookup"><span data-stu-id="1123d-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="1123d-113">**金额** 字段显示应支付给 TDS 主管机构供应商的 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="1123d-114">选择 **预缴税金交易** 以查看结算记录包括的不同 TDS 交易。</span><span class="sxs-lookup"><span data-stu-id="1123d-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="1123d-115">您可以在此页面上查看结算期间已包括在结算流程中的每个 TDS 交易的拆分。</span><span class="sxs-lookup"><span data-stu-id="1123d-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="1123d-116">在 **概述** 选项卡上，为要向 TDS 主管机构供应商结算的 TDS 交易选中 **标记** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1123d-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="1123d-117">**概述** 选项卡显示每个未结 TDS 交易的以下信息：</span><span class="sxs-lookup"><span data-stu-id="1123d-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="1123d-118">**日期** – TDS 交易日期。</span><span class="sxs-lookup"><span data-stu-id="1123d-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="1123d-119">**凭证** – 凭证编号。</span><span class="sxs-lookup"><span data-stu-id="1123d-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="1123d-120">**来源** – 用于过帐 TDS 交易的模块。</span><span class="sxs-lookup"><span data-stu-id="1123d-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="1123d-121">**供应商/客户** – 从中扣除 TDS 的供应商或客户帐号。</span><span class="sxs-lookup"><span data-stu-id="1123d-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="1123d-122">**扣减对象/当事方名称** – 从中扣除 TDS 的供应商或客户的名称。</span><span class="sxs-lookup"><span data-stu-id="1123d-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="1123d-123">**评估对象的性质** – 扣减对象所属的评估对象类别的性质。</span><span class="sxs-lookup"><span data-stu-id="1123d-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="1123d-124">**金额** – 计算 TDS 的发票金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="1123d-125">**税额** – 为交易计算的 TDS 金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1123d-126">针对不应向 TDS 主管机构供应商结算的任何 TDS 交易清除 **标记** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1123d-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="1123d-127">在 **常规** 选项卡上，**PAN** 字段显示扣减对象的永久帐号 (PAN)。</span><span class="sxs-lookup"><span data-stu-id="1123d-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="1123d-128">**日期** 字段显示 TDS 计算的日期，**值** 字段显示用于 TDS 计算的总百分比。</span><span class="sxs-lookup"><span data-stu-id="1123d-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="1123d-129">选择 **凭证** 可以查看 TDS 交易的凭证条目。</span><span class="sxs-lookup"><span data-stu-id="1123d-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="1123d-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1123d-130">Close the page.</span></span>
10. <span data-ttu-id="1123d-131">选择 **预缴税金组分** 以打开 **预缴税金组分** 页面，您可以在此页面中查看针对特定 TDS 税码的 TDS 税种组分计算的 TDS。</span><span class="sxs-lookup"><span data-stu-id="1123d-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="1123d-132">在 **概述** 选项卡上，**税种组分** 字段显示用于交易的 TDS 税种组分。</span><span class="sxs-lookup"><span data-stu-id="1123d-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="1123d-133">**金额** 字段显示为 TDS 税种组分计算的 TDS 金额（以基准货币为单位）。</span><span class="sxs-lookup"><span data-stu-id="1123d-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="1123d-134">**累计金额** 字段显示为所有已结算交易的 TDS 税种组分计算的 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="1123d-135">在 **金额** 选项卡上，**默认货币** 部分显示为 TDS 税种组分计算的 TDS 金额（以默认货币为单位）。</span><span class="sxs-lookup"><span data-stu-id="1123d-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="1123d-136">**第二货币** 部分显示使用第二货币的金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="1123d-137">关闭 **预缴税金组分** 页面。</span><span class="sxs-lookup"><span data-stu-id="1123d-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="1123d-138">在 **未结交易编辑** 页面的 **金额** 字段中，请注意将更新在结算期间要向 TDS 主管机构供应商结算的总金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="1123d-139">若要将不同 TDS 结算期间的 TDS 交易结算到 TDS 主管机构供应商，请为交易选中 **标记** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1123d-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="1123d-140">关闭 **未结交易编辑** 页面。</span><span class="sxs-lookup"><span data-stu-id="1123d-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1123d-141">如果在 **预缴税金交易** 页面上选择了几个交易进行结算，将在 **未结交易编辑** 页面的 **更正** 字段中更新选定交易的 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="1123d-142">将在 **日记帐凭证** 页面的日记帐行上更新更正金额，并将关闭 **未结交易编辑** 页面。</span><span class="sxs-lookup"><span data-stu-id="1123d-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="1123d-143">在 **日记帐凭证** 页面上，**借方** 字段显示支付给 TDS 主管机构供应商的总金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="1123d-144">输入抵销帐户详细信息。</span><span class="sxs-lookup"><span data-stu-id="1123d-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1123d-145">如果 TDS 交易具有不同的税务帐号 (TAN)，将在 **日记帐凭证** 页面上针对每个 TAN 创建日记帐行。</span><span class="sxs-lookup"><span data-stu-id="1123d-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="1123d-146">在 **付款费用** 选项卡的 **费用 ID** 字段中，选择费用类型为 **利息** 或 **其他** 的费用 ID 以收取向 TDS 主管机构供应商进行的延迟付款的付款费用。</span><span class="sxs-lookup"><span data-stu-id="1123d-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="1123d-147">在 **税务信息** 选项卡的 **公司信息** 部分中，**名称** 字段显示公司名称。</span><span class="sxs-lookup"><span data-stu-id="1123d-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="1123d-148">在 **预缴税金** 部分中，**税务帐号 (TAN)** 字段显示附加到交易行的 TAN。</span><span class="sxs-lookup"><span data-stu-id="1123d-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="1123d-149">验证和过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="1123d-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="1123d-150">选择 **预缴税金 \> Challan 信息** 以输入交易的 challan 详细信息。</span><span class="sxs-lookup"><span data-stu-id="1123d-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="1123d-151">**凭证** 字段显示交易的凭证编号。</span><span class="sxs-lookup"><span data-stu-id="1123d-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="1123d-152">如果使用帐簿条目存入 TDS 金额，选中 **按帐簿条目存入的 TDS** 复选框。</span><span class="sxs-lookup"><span data-stu-id="1123d-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="1123d-153">在 **Challan 编号** 字段中，输入用于向 TDS 主管机构供应商进行付款的 challan 编号。</span><span class="sxs-lookup"><span data-stu-id="1123d-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="1123d-154">在 **日期** 字段中，输入 challan 日期。</span><span class="sxs-lookup"><span data-stu-id="1123d-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="1123d-155">在 **银行名称** 字段中，选择应付给 TDS 主管机构供应商的 TDS 金额应存入的银行的名称。</span><span class="sxs-lookup"><span data-stu-id="1123d-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="1123d-156">该字段在 **应付帐款 \> 所有供应商 \> 设置 \> 银行帐户** 上列出为 TDS 主管机构供应商设置的所有银行帐户。</span><span class="sxs-lookup"><span data-stu-id="1123d-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="1123d-157">在 **BSR 代码** 字段中，输入银行的基本统计回归 (BSR) 代码。</span><span class="sxs-lookup"><span data-stu-id="1123d-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="1123d-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1123d-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="1123d-159">示例</span><span class="sxs-lookup"><span data-stu-id="1123d-159">Example</span></span>

<span data-ttu-id="1123d-160">使用定期 TDS 结算流程为 **租金** TDS 组分组结算期间 04/01/2009。</span><span class="sxs-lookup"><span data-stu-id="1123d-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="1123d-161">在 TDS 结算期间向 TDS 供应商主管机构帐户过帐 141,625.00 TDS 总金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="1123d-162">您可以在 TDS 主管机构供应商的 **未结交易编辑** 页面上的 **金额** 字段中查看此金额。</span><span class="sxs-lookup"><span data-stu-id="1123d-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="1123d-163">如果选择 **预缴税金交易** 以查看该期间已结算的不同 TDS 交易，将显示以下信息。</span><span class="sxs-lookup"><span data-stu-id="1123d-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="1123d-164">TDS 金额</span><span class="sxs-lookup"><span data-stu-id="1123d-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="1123d-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="1123d-165">16,995.00</span></span>  |
| <span data-ttu-id="1123d-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="1123d-166">22,660.00</span></span>  |
| <span data-ttu-id="1123d-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="1123d-167">28,325.00</span></span>  |
| <span data-ttu-id="1123d-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="1123d-168">16,995.00</span></span>  |
| <span data-ttu-id="1123d-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="1123d-169">28,325.00</span></span>  |
| <span data-ttu-id="1123d-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="1123d-170">16,995.00</span></span>  |
| <span data-ttu-id="1123d-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="1123d-171">11,330.00</span></span>  |

<span data-ttu-id="1123d-172">对于特定 TDS 金额，您可以选择 **预缴税金组分** 以查看针对特定 TDS 税码为每个 TDS 税种组分计算的 TDS。</span><span class="sxs-lookup"><span data-stu-id="1123d-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="1123d-173">对于此示例，为 TDS 金额 16,995.00 选择 **预缴税金组分**。</span><span class="sxs-lookup"><span data-stu-id="1123d-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="1123d-174">显示针对交易为每个组分计算的税额。</span><span class="sxs-lookup"><span data-stu-id="1123d-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="1123d-175">税种组分</span><span class="sxs-lookup"><span data-stu-id="1123d-175">Tax component</span></span> | <span data-ttu-id="1123d-176">时长</span><span class="sxs-lookup"><span data-stu-id="1123d-176">Amount</span></span>    | <span data-ttu-id="1123d-177">累计金额</span><span class="sxs-lookup"><span data-stu-id="1123d-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="1123d-178">TDS</span><span class="sxs-lookup"><span data-stu-id="1123d-178">TDS</span></span>           | <span data-ttu-id="1123d-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="1123d-179">1,5000.00</span></span> | <span data-ttu-id="1123d-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="1123d-180">125,000.00</span></span>         |
| <span data-ttu-id="1123d-181">附加费</span><span class="sxs-lookup"><span data-stu-id="1123d-181">Surcharge</span></span>     | <span data-ttu-id="1123d-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="1123d-182">1,500.00</span></span>  | <span data-ttu-id="1123d-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="1123d-183">12,500.00</span></span>          |
| <span data-ttu-id="1123d-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="1123d-184">PE-Cess</span></span>       | <span data-ttu-id="1123d-185">330.00</span><span class="sxs-lookup"><span data-stu-id="1123d-185">330.00</span></span>    | <span data-ttu-id="1123d-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="1123d-186">2,750.00</span></span>           |
| <span data-ttu-id="1123d-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="1123d-187">SHE Cess</span></span>      | <span data-ttu-id="1123d-188">165.00</span><span class="sxs-lookup"><span data-stu-id="1123d-188">165.00</span></span>    | <span data-ttu-id="1123d-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="1123d-189">1,375.00</span></span>           |

<span data-ttu-id="1123d-190">如果在 **预缴税金交易** 页面上仅选择了 TDS 金额 16,995.00、22,660.00 和 2,8325.00 进行结算，在 **未结交易编辑** 页面的 **更正** 字段中，结算的总金额显示为 **67,980.00**。</span><span class="sxs-lookup"><span data-stu-id="1123d-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="1123d-191">如果标记要结算的此交易，并且关闭 **未结交易编辑** 页面，将在 **日记帐凭证** 页面的 **借方** 字段中显示金额 **67,980.00**。</span><span class="sxs-lookup"><span data-stu-id="1123d-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="1123d-192">现在，您可以过帐日记帐并生成 TDS challan。</span><span class="sxs-lookup"><span data-stu-id="1123d-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="1123d-193">调整向 TDS 主管机构供应商支付的预先付款</span><span class="sxs-lookup"><span data-stu-id="1123d-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="1123d-194">若要将向 TDS 主管机构供应商支付的预先付款调整为实际付款，请转到 **应付帐款 \> 供应商 \> 所有供应商 \> 交易编辑**。</span><span class="sxs-lookup"><span data-stu-id="1123d-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="1123d-195">如果支付的实际付款超出预先付款，将为交易生成两个 challan 编号。</span><span class="sxs-lookup"><span data-stu-id="1123d-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="1123d-196">但是，TDS 查询中仅显示第一个 challan 编号。</span><span class="sxs-lookup"><span data-stu-id="1123d-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
