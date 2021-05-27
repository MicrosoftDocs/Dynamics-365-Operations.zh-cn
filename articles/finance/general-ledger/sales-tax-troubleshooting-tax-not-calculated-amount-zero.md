---
title: 未计算税款或税额为零
description: 本主题提供可以在税额为 0（零）或未计算税款时提供帮助的故障排除信息。
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020107"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="b1e76-103">未计算税款或税额为零</span><span class="sxs-lookup"><span data-stu-id="b1e76-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1e76-104">交易的行金额可能存在不是 0（零），但未计算税款或计算出的税额为 0 的情况。</span><span class="sxs-lookup"><span data-stu-id="b1e76-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="b1e76-105">要解决此问题，请根据需要按照以下各节中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b1e76-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="b1e76-106">验证交易是否正确选择了税代码</span><span class="sxs-lookup"><span data-stu-id="b1e76-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="b1e76-107">如果交易未选择正确的税代码，或者未选择任何税代码，将不会计算税款。</span><span class="sxs-lookup"><span data-stu-id="b1e76-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="b1e76-108">请按照以下步骤验证交易是否正确选择了税代码。</span><span class="sxs-lookup"><span data-stu-id="b1e76-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="b1e76-109">在交易行的 **行详细信息** 快速选项卡上，在 **设置** 选项卡的 **销售税** 部分，验证是否在 **物料销售税组** 和 **销售税组** 字段中选择了正确的税组。</span><span class="sxs-lookup"><span data-stu-id="b1e76-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="b1e76-110">如果未选择正确的税组，请进行选择。</span><span class="sxs-lookup"><span data-stu-id="b1e76-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="b1e76-111">[![“物料销售税组”和“销售税组”字段](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="b1e76-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="b1e76-112">转到 **税** \> **间接税** \> **销售税** \> **销售税组**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="b1e76-113">选择适当的销售税组，然后在 **设置** 快速选项卡上，记下 **销售税代码** 字段中的税代码。</span><span class="sxs-lookup"><span data-stu-id="b1e76-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="b1e76-114">[![销售税组页面](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="b1e76-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="b1e76-115">转到 **税** \> **间接税** \> **销售税** \> **物料销售税组**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="b1e76-116">选择适当的物料销售税组，然后在 **设置** 快速选项卡上，验证 **销售税代码** 字段中的税代码与销售税组的税代码是否匹配。</span><span class="sxs-lookup"><span data-stu-id="b1e76-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="b1e76-117">[![物料销售税组页面](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="b1e76-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="b1e76-118">如果税代码不匹配，更新其中一个组的销售税代码。</span><span class="sxs-lookup"><span data-stu-id="b1e76-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="b1e76-119">确认所选的税代码不免税并具有正确的税率值</span><span class="sxs-lookup"><span data-stu-id="b1e76-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="b1e76-120">如果税代码免税，或者税率是 0（零），税款计算结果将是 0。</span><span class="sxs-lookup"><span data-stu-id="b1e76-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="b1e76-121">请按照以下步骤确定所选的税代码是否免税，并验证是否对它们应用了正确的税率。</span><span class="sxs-lookup"><span data-stu-id="b1e76-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="b1e76-122">转到 **税** \> **间接税** \> **销售税** \> **销售税组**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="b1e76-123">选择适当的销售税组，然后，在 **设置** 快速选项卡上，验证 **免税** 复选框是否清除。</span><span class="sxs-lookup"><span data-stu-id="b1e76-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="b1e76-124">如果已选中，请清除。</span><span class="sxs-lookup"><span data-stu-id="b1e76-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="b1e76-125">[![“销售税组”页上的“免税”复选框](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="b1e76-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="b1e76-126">转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="b1e76-127">选择适当的销售税代码，然后验证 **值** 字段中的税率值是否不为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="b1e76-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="b1e76-128">如果为 0，更新该字段，将其设置为正确的税率。</span><span class="sxs-lookup"><span data-stu-id="b1e76-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="b1e76-129">[![销售税代码值页面上的“值”字段](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="b1e76-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="b1e76-130">确定零是否是正确的税额</span><span class="sxs-lookup"><span data-stu-id="b1e76-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="b1e76-131">在有些情况下，税额为 0（零）是正确的。</span><span class="sxs-lookup"><span data-stu-id="b1e76-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="b1e76-132">请按照以下步骤确定 0 是否是您的交易的正确税额。</span><span class="sxs-lookup"><span data-stu-id="b1e76-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="b1e76-133">转到 **总帐** \> **分类帐设置** \> **总帐参数**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="b1e76-134">在 **销售税** 选项卡上，在 **计算方法** 字段中，确认选择了 **总计**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="b1e76-135">[![“总帐参数”页上的“计算方法”字段](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="b1e76-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="b1e76-136">转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="b1e76-137">选择适当的销售税代码，选择 **计算**\>**边际基数**，确认边际基数设置为 **发票余额的净额** 或 **包括其他销售税金额的发票合计**。</span><span class="sxs-lookup"><span data-stu-id="b1e76-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="b1e76-138">有关详细信息，请参阅[包括其他销售税金额的发票合计](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts)。</span><span class="sxs-lookup"><span data-stu-id="b1e76-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="b1e76-139">如果在步骤 2 和 4 中设置了正确的值，请确定交易的总金额是否为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="b1e76-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="b1e76-140">如果总金额为 0，税额为 0 则是预期结果。</span><span class="sxs-lookup"><span data-stu-id="b1e76-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="b1e76-141">因为税款计算基于发票余额的总金额，并且该金额不是逐行计算的，所以税额 0 将在税款计算后分配给每一行。</span><span class="sxs-lookup"><span data-stu-id="b1e76-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="b1e76-142">确定是否存在自定义</span><span class="sxs-lookup"><span data-stu-id="b1e76-142">Determine whether customization exists</span></span>

<span data-ttu-id="b1e76-143">如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。</span><span class="sxs-lookup"><span data-stu-id="b1e76-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="b1e76-144">如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。</span><span class="sxs-lookup"><span data-stu-id="b1e76-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
