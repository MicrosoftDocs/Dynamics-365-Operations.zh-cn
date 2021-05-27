---
title: 为 TDS 主管机构付款设置付款费用
description: 本主题说明如何设置对从源扣缴税款 (TDS) 主管机构付款收取的付款费用。
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023073"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="ff3b9-103">为 TDS 主管机构付款设置付款费用</span><span class="sxs-lookup"><span data-stu-id="ff3b9-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff3b9-104">本主题说明如何设置对从源扣缴税款 (TDS) 主管机构付款收取的付款费用。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="ff3b9-105">转到 **应付帐款 \> 付款设置 \> 付款费用**。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="ff3b9-106">[![付款费用页面](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="ff3b9-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="ff3b9-107">选择 **新建** 以创建付款费用，并输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="ff3b9-108">在 **费用类型** 字段中，选择付款费用的类型：</span><span class="sxs-lookup"><span data-stu-id="ff3b9-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="ff3b9-109">**否**</span><span class="sxs-lookup"><span data-stu-id="ff3b9-109">**None**</span></span>
    - <span data-ttu-id="ff3b9-110">**利息** – 对向 TDS 主管机构供应商支付的延迟付款收取利息。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="ff3b9-111">**其他** – 对向 TDS 主管机构供应商支付的延迟付款收取其他费用。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="ff3b9-112">如果选择 **利息** 或 **其他**，**费用** 字段将自动设置为 **分类帐**。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="ff3b9-113">如果在 **字段类型** 中选择了 **利息** 或 **其他**，请在 **主帐户** 字段中，选择要将利息或其他费用过帐到的分类帐帐户。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="ff3b9-114">输入其他所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-114">Enter the other required details.</span></span>
6. <span data-ttu-id="ff3b9-115">在操作窗格上，选择 **付款费用设置** 以打开 **付款费用设置** 页面，您可以在该页面中设置银行、付款方式、付款说明、货币和日期间隔的各种组合的付款费用。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="ff3b9-116">[![付款费用设置页面](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="ff3b9-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="ff3b9-117">在 **概述** 选项卡上，在 **分组** 字段中，指定要为其设置付款费用的银行：</span><span class="sxs-lookup"><span data-stu-id="ff3b9-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="ff3b9-118">**表** – 费用对特定银行帐户有效。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="ff3b9-119">**组** – 费用对特定银行组有效。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="ff3b9-120">**全部** - 费用对所有银行帐户有效。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="ff3b9-121">如果在 **分组** 字段中选择了 **表** 或 **组**，请在 **银行关系** 字段中，选择要为其设置付款费用的特定银行帐户或银行组。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="ff3b9-122">在 **付款方式** 字段中，选择用于支付费用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="ff3b9-123">在 **付款说明** 字段中，选择或输入在 **付款说明** 页面上生成的付款说明代码。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="ff3b9-124">电子资金转帐付款方式应遵循“付款说明”。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="ff3b9-125">在 **付款货币** 字段中，选择用于激活费用的货币。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="ff3b9-126">只有使用选定货币的交易才能激活费用。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="ff3b9-127">如果将此字段保留为空，则所有货币都会激活费用。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="ff3b9-128">在 **百分比/金额** 字段中，选择计算方法。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="ff3b9-129">选项包括 **金额**、**百分比** 和 **间隔**。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="ff3b9-130">在 **费用金额** 字段中，将费用金额指定为付款的百分比或一笔付款的金额。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="ff3b9-131">在 **费用货币** 字段中，指定费用的货币代码。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="ff3b9-132">选择 **常规** 选项卡以查看或修改选定银行帐户的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="ff3b9-133">[![常规选项卡](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="ff3b9-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="ff3b9-134">在 **最小值** 字段中，输入激活费用的最小交易金额。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="ff3b9-135">在 **最大值** 字段中，输入激活费用的最大交易金额。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="ff3b9-136">在 **开始日期** 和 **结束日期** 字段中，定义用于计算费用的日期范围。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="ff3b9-137">在 **最小费用** 字段中，将费用金额指定为付款的百分比或一笔付款的金额。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="ff3b9-138">在 **销售税组** 字段中，选择用于计算费用金额的销售税的销售税组。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="ff3b9-139">在 **物料销售税组** 字段中，选择用于计算费用金额的物料销售税的物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="ff3b9-140">选择 **间隔** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="ff3b9-141">[![间隔选项卡](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="ff3b9-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="ff3b9-142">在 **天数** 字段中，输入付款的过帐日期（折扣日期）和本票的截止日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="ff3b9-143">在 **百分比/金额** 字段中，选择规格是百分比还是设置的金额。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="ff3b9-144">在 **费用金额** 字段中，将费用金额输入为付款的百分比或一笔付款的金额。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="ff3b9-145">关闭 **付款费用设置** 页面。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="ff3b9-146">关闭 **付款费用** 页面。</span><span class="sxs-lookup"><span data-stu-id="ff3b9-146">Close the **Payment fee** page.</span></span>
