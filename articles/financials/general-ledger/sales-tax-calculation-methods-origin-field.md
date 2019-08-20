---
title: “源”字段中的销售税计算方法
description: 本文说明销售税代码页上“来源”字段中的选项，以及如何基于销售税代码的所选选项计算销售税。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ec6144599e9bb74333a663a56bdbf07b1999669
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846743"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="2c4ac-103">“源”字段中的销售税计算方法</span><span class="sxs-lookup"><span data-stu-id="2c4ac-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="2c4ac-104">本文说明销售税代码页上“来源”字段中的选项，以及如何基于销售税代码的所选选项计算销售税。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="2c4ac-105">对于您在“销售税代码”页中创建的每个增值税代码，必须选择应用于“源”字段中的增值税基础金额的计算方法。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="2c4ac-106">净额百分比</span><span class="sxs-lookup"><span data-stu-id="2c4ac-106">Percentage of net amount</span></span>
<span data-ttu-id="2c4ac-107">净额百分比计算方法为“源”字段中的默认值。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="2c4ac-108">增值税被计算为采购或销售金额的百分比，不包括任何其他增值税。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="2c4ac-109">示例</span><span class="sxs-lookup"><span data-stu-id="2c4ac-109">Example</span></span>

<span data-ttu-id="2c4ac-110">税率是 25%。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-110">The tax rate is 25%.</span></span> <span data-ttu-id="2c4ac-111">发票行显示的数量为每 1.00 为 10 个物料，允许客户有 10% 的单行折扣。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="2c4ac-112">净额：(10 x 1.00) -10% = 9.00 销售税：9.00 x 25% = 2.25 总金额：9.00 + 2.25 = 11.25</span><span class="sxs-lookup"><span data-stu-id="2c4ac-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="2c4ac-113">总额百分比</span><span class="sxs-lookup"><span data-stu-id="2c4ac-113">Percentage of gross amount</span></span>
<span data-ttu-id="2c4ac-114">如果您选择总额百分比方法，销售税计算为总销售额的百分比。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="2c4ac-115">总额是行净额加该行的所有税和费用，除原始金额 = 总额百分比的一项税以外。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="2c4ac-116">示例</span><span class="sxs-lookup"><span data-stu-id="2c4ac-116">Example</span></span>

<span data-ttu-id="2c4ac-117">税务主管机构对某一物料征收了一些特殊的税种。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="2c4ac-118">在计算增值税之前，这些税种的金额添加到净额。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="2c4ac-119">假使以下销售税代码：</span><span class="sxs-lookup"><span data-stu-id="2c4ac-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="2c4ac-120">DUTY 1 = 10%，使用净额百分比计算方法</span><span class="sxs-lookup"><span data-stu-id="2c4ac-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="2c4ac-121">DUTY 2 = 20%，使用净额百分比计算方法</span><span class="sxs-lookup"><span data-stu-id="2c4ac-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="2c4ac-122">SALESTAX = 25%，使用总额百分比计算方法</span><span class="sxs-lookup"><span data-stu-id="2c4ac-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="2c4ac-123">如果净额是 10.00，然后“DUTY 1”是 1.00 (10.00 x 10%)，“DUTY 2” = 2.00 (10.00 x 20%)。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="2c4ac-124">金额如下：总额：净额 + DUTY 1 金额 + DUTY 2 金额 (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 总计 DUTIES 和 SALESTAX：1.00 + 2.00 + 3.25 = 6.25 总金额：10.00 + 6.25 = 16.25</span><span class="sxs-lookup"><span data-stu-id="2c4ac-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="2c4ac-125">**注意**</span><span class="sxs-lookup"><span data-stu-id="2c4ac-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4ac-126">仅原始金额 = 总额百分比的一个税务代码可以用于交易记录。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="2c4ac-127">如果多个此类税码为交易记录确定，错误将显示销售税不能计算。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="2c4ac-128">销售税百分比</span><span class="sxs-lookup"><span data-stu-id="2c4ac-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="2c4ac-129">当您在“原始金额”字段中选择了“销售税百分比”时，将按照“税上税”字段中选择的增值税的百分比计算增值税。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="2c4ac-130">首先计算在“税上税”字段中选择的增值税。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="2c4ac-131">然后基于第一个增值税金额计算第二个增值税。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="2c4ac-132">示例</span><span class="sxs-lookup"><span data-stu-id="2c4ac-132">Example</span></span>

<span data-ttu-id="2c4ac-133">假使以下销售税代码：</span><span class="sxs-lookup"><span data-stu-id="2c4ac-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="2c4ac-134">DUTY 1 = 10%，使用净额百分比方法</span><span class="sxs-lookup"><span data-stu-id="2c4ac-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="2c4ac-135">DUTY 2 = 20%，使用销售税百分比方法，“税上税”字段中为 Duty 1</span><span class="sxs-lookup"><span data-stu-id="2c4ac-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="2c4ac-136">SALESTAX = 25%，使用总额百分比方法</span><span class="sxs-lookup"><span data-stu-id="2c4ac-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="2c4ac-137">净额：10.00 DUTY 1：10.00 x 10% = 1.00 DUTY 2：1.00 x 20% = 0.20 总额：10.00 + 1.00 + 0.20 = 11.20 SALESTAX：11.20 x 25% = 2.80 总计 DUTIES 和 SALESTAX：1.00 + 0.20 + 2.80 = 4.00 总金额：10.00 + 4.00 = 14.00</span><span class="sxs-lookup"><span data-stu-id="2c4ac-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="2c4ac-138">**注意**</span><span class="sxs-lookup"><span data-stu-id="2c4ac-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4ac-139">多级别税上税计算是不可能的。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="2c4ac-140">税不能基于已基于其他税计算的税计算。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="2c4ac-141">多个单一级别税上税代码可以基于交易记录计算。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="2c4ac-142">单位金额</span><span class="sxs-lookup"><span data-stu-id="2c4ac-142">Amount per unit</span></span>
<span data-ttu-id="2c4ac-143">当您在“原始金额”字段中选择“单位金额”，销售税将计算为每单位固定金额乘以在凭证行输入的数量。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="2c4ac-144">在“单位”字段中必须选择单位。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="2c4ac-145">单位金额在“销售税代码值”页指定。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="2c4ac-146">示例</span><span class="sxs-lookup"><span data-stu-id="2c4ac-146">Example</span></span>

<span data-ttu-id="2c4ac-147">销售税代码的设置如下：每单位 USD 1.20 = 箱 在销售发票行上，物料销售 25 箱 销售税计算为 25 x 1.20 = 30.00</span><span class="sxs-lookup"><span data-stu-id="2c4ac-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="2c4ac-148">**注意**</span><span class="sxs-lookup"><span data-stu-id="2c4ac-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4ac-149">如果交易记录用与在销售税代码中指定的单位不同的单位输入，它将基于在“单位换算”页设置的单位换算自动换算。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="2c4ac-150">单位金额，附加选项</span><span class="sxs-lookup"><span data-stu-id="2c4ac-150">Amount per unit, additional option</span></span>

<span data-ttu-id="2c4ac-151">在“计算”选项卡上，您可以选择是否在其他税码前计算单位金额计算税，以及是否在原始金额 = 总额百分比的其他税码计算前将其添加到净额。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="2c4ac-152">示例</span><span class="sxs-lookup"><span data-stu-id="2c4ac-152">Examples</span></span>

<span data-ttu-id="2c4ac-153">我们假定基于交易记录计算 2 个税代码：</span><span class="sxs-lookup"><span data-stu-id="2c4ac-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="2c4ac-154">DUTY：原始金额 = 单位金额和销售税，该值设置为每单位 = 件为 5.00</span><span class="sxs-lookup"><span data-stu-id="2c4ac-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="2c4ac-155">SALESTAX：原始金额 = 如下例所示，该值设置为 25%</span><span class="sxs-lookup"><span data-stu-id="2c4ac-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="2c4ac-156">我们以单价 10.00 销售一件物料</span><span class="sxs-lookup"><span data-stu-id="2c4ac-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="2c4ac-157">示例 1</span><span class="sxs-lookup"><span data-stu-id="2c4ac-157">Example 1</span></span>

<span data-ttu-id="2c4ac-158">SALESTAX：原始总额 = 总额百分比方法 “在征收销售税前计算”选项不起作用，因为 SALESTAX 计算为总额百分比。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="2c4ac-159">DUTY：1 x 5.00 = 5.00 总额：10.00 + 5.00 = 15.00 SALESTAX：15.00 x 25% = 3.75 销项税总额：5.00 + 3.75 = 8.75 总金额：10.00 + 8.75 = 18.75</span><span class="sxs-lookup"><span data-stu-id="2c4ac-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="2c4ac-160">示例 2</span><span class="sxs-lookup"><span data-stu-id="2c4ac-160">Example 2</span></span>

<span data-ttu-id="2c4ac-161">SALESTAX：原始金额 = 净额百分比 未为 DUTY 计算选择“在征收销售税前计算”选项。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="2c4ac-162">净额：10.00 DUTY：1 x 5.00 = 5.00 SALESTAX：10.00 x 25% = 2.50 销项税总额：5.00 + 2.50 = 7.50 总金额：10.00 + 7.50 = 17.50</span><span class="sxs-lookup"><span data-stu-id="2c4ac-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="2c4ac-163">示例 3</span><span class="sxs-lookup"><span data-stu-id="2c4ac-163">Example 3</span></span>

<span data-ttu-id="2c4ac-164">SALESTAX：原始金额 = 净额百分比 为 DUTY 计算选择“在征收销售税前计算”选项。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="2c4ac-165">净额：10.00 DUTY：1 x 5.00 = 5.00 SALESTAX：(10.00 + 5.00) x 25% = 3.75 销项税总额：5.00 + 3.75 = 8.75 总金额：10.00 + 8.75 = 18.75</span><span class="sxs-lookup"><span data-stu-id="2c4ac-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="2c4ac-166">示例 4</span><span class="sxs-lookup"><span data-stu-id="2c4ac-166">Example 4</span></span>

<span data-ttu-id="2c4ac-167">示例 3 和示例 1 的结果相同，因为只存在一个税种。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="2c4ac-168">假设您有两个 DUTY，且只有一个包括在销售税计算的净额中：DUTY 1：5.00，使用“单位金额”方法，并选择“在征收销售税前计算”选项 DUTY 2：2.50，使用“单位金额”方法，不选择“在征收销售税前计算”选项 销售税：25%，使用“净额百分比”方法 净额：10.00 DUTY 1：1 x 5.00 = 5.00 DUTY 2：1 x 2.50 = 2.50 受销售税限制的净额：10.00 + 5.00 = 15.00 SALESTAX：15.00 x 25% = 3.75 总销售税，包括关税：5.00 + 2.50 + 3.75 = 11.25 总金额：10.00 + 11.25 = 21.25 25% SALESTAX 为净额 (10.00) + DUTY 1 (5.00) 的总和计算 = 15.00。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="2c4ac-169">在计算增值税后，DUTY 2 添加到税额中。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="2c4ac-170">已计算的净额百分比</span><span class="sxs-lookup"><span data-stu-id="2c4ac-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="2c4ac-171">已计算的净额百分比根据单据或日记帐的不同金额包括销售税参数设置处理纳税计算。</span><span class="sxs-lookup"><span data-stu-id="2c4ac-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="2c4ac-172">示例 1</span><span class="sxs-lookup"><span data-stu-id="2c4ac-172">Example 1</span></span>

<span data-ttu-id="2c4ac-173">单据/日记帐设置为“金额包括销售税 = 是” 交易记录行金额：10.00 税率：25% 销售税：交易记录行金额 x 税率 (10.00 x 25%) = 2.50 计税基数金额（原始金额）：交易记录行金额 - 销售税 (10.00 - 2.50) = 7.50</span><span class="sxs-lookup"><span data-stu-id="2c4ac-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="2c4ac-174">示例 2</span><span class="sxs-lookup"><span data-stu-id="2c4ac-174">Example 2</span></span>

<span data-ttu-id="2c4ac-175">单据/日记帐设置为“金额包括销售税 = 否” 交易记录行金额：10.00 税率：25% 销售税：(交易记录行金额 x 税率) / (100 - 税率) (10.00 x 25%) / (100% - 25%) = 3.33 计税基数金额（原始金额）：交易记录行金额 = 10.00</span><span class="sxs-lookup"><span data-stu-id="2c4ac-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="2c4ac-176">其他资源</span><span class="sxs-lookup"><span data-stu-id="2c4ac-176">Additional resources</span></span>
--------

[<span data-ttu-id="2c4ac-177">基于“边际基数”和“计算方法”字段确定销售税比率</span><span class="sxs-lookup"><span data-stu-id="2c4ac-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="2c4ac-178">全部金额和销售税代码的间隔计算选项</span><span class="sxs-lookup"><span data-stu-id="2c4ac-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



