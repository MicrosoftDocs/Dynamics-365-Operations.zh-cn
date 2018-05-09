---
title: "输入工资期初余额"
description: "此主题介绍为收入代码、扣除额、福利和税款输入期初余额的步骤。 此信息对于要从其他系统迁移或转移用于新的工资单实现方式的数据的合作伙伴十分重要。"
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 49d2de890f99a25b72a41cb879b16220a77c1f24
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="f6f42-104">输入工资期初余额</span><span class="sxs-lookup"><span data-stu-id="f6f42-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6f42-105">此主题介绍为收入代码、扣除额、福利和税款输入期初余额的步骤。</span><span class="sxs-lookup"><span data-stu-id="f6f42-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="f6f42-106">此信息对于从其他系统转移用于新的工资单实现方式的数据的合作伙伴十分重要。</span><span class="sxs-lookup"><span data-stu-id="f6f42-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="f6f42-107">为了准备输入期初工资单余额，我们验证以下信息：</span><span class="sxs-lookup"><span data-stu-id="f6f42-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="f6f42-108">在系统中输入和提供员工记录</span><span class="sxs-lookup"><span data-stu-id="f6f42-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="f6f42-109">将以下数据设置和分配到员工：</span><span class="sxs-lookup"><span data-stu-id="f6f42-109">The following data is set up and assigned to employees:</span></span>
> 
> > * <span data-ttu-id="f6f42-110">付薪周期和付薪期间</span><span class="sxs-lookup"><span data-stu-id="f6f42-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="f6f42-111">收入代码</span><span class="sxs-lookup"><span data-stu-id="f6f42-111">Earning codes</span></span>
> > * <span data-ttu-id="f6f42-112">税金</span><span class="sxs-lookup"><span data-stu-id="f6f42-112">Taxes</span></span>
> > * <span data-ttu-id="f6f42-113">福利和扣除额</span><span class="sxs-lookup"><span data-stu-id="f6f42-113">Benefits and deductions</span></span>
> 
> * <span data-ttu-id="f6f42-114">公司应已选择可以设置工资单期初余额的日期。</span><span class="sxs-lookup"><span data-stu-id="f6f42-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
> 
> * <span data-ttu-id="f6f42-115">已从旧系统收集关于所有收入、福利/扣除额、福利缴纳、员工税款以及雇主税款及其年初至今金额的信息。</span><span class="sxs-lookup"><span data-stu-id="f6f42-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="f6f42-116">当您计划输入期初余额时，考虑数据需要的详细程度。</span><span class="sxs-lookup"><span data-stu-id="f6f42-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="f6f42-117">大多数企业输入一个合并的年初至今金额。</span><span class="sxs-lookup"><span data-stu-id="f6f42-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="f6f42-118">但如果需要更加详细的信息，可使用季度增量输入余额。</span><span class="sxs-lookup"><span data-stu-id="f6f42-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="f6f42-119">确定需要的详细程度决定了必须为每个工作人员手动创建多少份工资报表。</span><span class="sxs-lookup"><span data-stu-id="f6f42-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="f6f42-120">对于单个年初至今金额，只需对每位员工手动创建一份报表。</span><span class="sxs-lookup"><span data-stu-id="f6f42-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="f6f42-121">要执行此操作，可使用来自上一个系统的最终工资单的年初至今金额作为在新工资单系统中输入的金额。</span><span class="sxs-lookup"><span data-stu-id="f6f42-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="f6f42-122">以下示例显示可以如何输入员工的工资单期初余额，包括收入代码、福利/扣除额和税款。</span><span class="sxs-lookup"><span data-stu-id="f6f42-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="f6f42-123">在真实示例中，每个收入代码、福利扣缴、福利缴纳、员工税款和雇主税款都有一个行项输入的金额为年初至今金额。</span><span class="sxs-lookup"><span data-stu-id="f6f42-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="f6f42-124">使用该代码和金额列表，按照创建已禁用核算的人工收入和工资单的步骤获取用于工资单目的的期初余额。</span><span class="sxs-lookup"><span data-stu-id="f6f42-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="f6f42-125">禁用核算的原因是因为您不想将此期初余额工资单过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="f6f42-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="f6f42-126">这在旧系统中完成，并且当您在设置总帐中的期初余额时转移到新系统。</span><span class="sxs-lookup"><span data-stu-id="f6f42-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="f6f42-127">A.</span><span class="sxs-lookup"><span data-stu-id="f6f42-127">A.</span></span> <span data-ttu-id="f6f42-128">如何设置要在工资单期初余额上使用的收入代码</span><span class="sxs-lookup"><span data-stu-id="f6f42-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="f6f42-129">当您输入工资单期初余额时，确保将您要使用的收入代码配置为启用“允许编辑收益表费率”选项。</span><span class="sxs-lookup"><span data-stu-id="f6f42-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="f6f42-130">这可以使您手动键入来自旧系统的金额。</span><span class="sxs-lookup"><span data-stu-id="f6f42-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="f6f42-131">B.</span><span class="sxs-lookup"><span data-stu-id="f6f42-131">B.</span></span> <span data-ttu-id="f6f42-132">为员工创建收益表以获得期初余额</span><span class="sxs-lookup"><span data-stu-id="f6f42-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="f6f42-133">此步骤为每个工作人员手动创建旧系统最后一次付薪期间的收益表，这将在新的工资单系统中创建收益表行。</span><span class="sxs-lookup"><span data-stu-id="f6f42-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="f6f42-134">按每个收入代码以及年初至今金额和工时各输入一行。</span><span class="sxs-lookup"><span data-stu-id="f6f42-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="f6f42-135">示例步骤如下：</span><span class="sxs-lookup"><span data-stu-id="f6f42-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="f6f42-136">打开**所有收益表**页并单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="f6f42-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="f6f42-137">输入以下内容：</span><span class="sxs-lookup"><span data-stu-id="f6f42-137">Enter the following:</span></span> 

| <span data-ttu-id="f6f42-138">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-138">Field</span></span>      | <span data-ttu-id="f6f42-139">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="f6f42-140">工作线程</span><span class="sxs-lookup"><span data-stu-id="f6f42-140">Worker</span></span>     | <span data-ttu-id="f6f42-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="f6f42-141">Michael Redmond</span></span>       |
| <span data-ttu-id="f6f42-142">付薪周期</span><span class="sxs-lookup"><span data-stu-id="f6f42-142">Pay cycle</span></span>  | <span data-ttu-id="f6f42-143">sm</span><span class="sxs-lookup"><span data-stu-id="f6f42-143">sm</span></span>                    |
| <span data-ttu-id="f6f42-144">付薪期间</span><span class="sxs-lookup"><span data-stu-id="f6f42-144">Pay period</span></span> | <span data-ttu-id="f6f42-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="f6f42-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="f6f42-146">在**收益表行**选项卡上输入以下数据：</span><span class="sxs-lookup"><span data-stu-id="f6f42-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="f6f42-147">行 1：**收益表行**选项卡</span><span class="sxs-lookup"><span data-stu-id="f6f42-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="f6f42-148">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-148">Field</span></span>            | <span data-ttu-id="f6f42-149">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="f6f42-150">收入代码</span><span class="sxs-lookup"><span data-stu-id="f6f42-150">Earnings code</span></span>    | <span data-ttu-id="f6f42-151">常规付薪</span><span class="sxs-lookup"><span data-stu-id="f6f42-151">Regular pay</span></span> |
| <span data-ttu-id="f6f42-152">数量</span><span class="sxs-lookup"><span data-stu-id="f6f42-152">Quantity</span></span>         | <span data-ttu-id="f6f42-153">1.00</span><span class="sxs-lookup"><span data-stu-id="f6f42-153">1.00</span></span>        |
| <span data-ttu-id="f6f42-154">工资</span><span class="sxs-lookup"><span data-stu-id="f6f42-154">Rage</span></span>             | <span data-ttu-id="f6f42-155">30,000</span><span class="sxs-lookup"><span data-stu-id="f6f42-155">30,000</span></span>      |
| <span data-ttu-id="f6f42-156">行明细选项卡</span><span class="sxs-lookup"><span data-stu-id="f6f42-156">Line details tab</span></span> |             |
| <span data-ttu-id="f6f42-157">手动</span><span class="sxs-lookup"><span data-stu-id="f6f42-157">Manual</span></span>           | <span data-ttu-id="f6f42-158">（已标记）</span><span class="sxs-lookup"><span data-stu-id="f6f42-158">(marked)</span></span>    |

<span data-ttu-id="f6f42-159">行 2：**收益表行**选项卡</span><span class="sxs-lookup"><span data-stu-id="f6f42-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="f6f42-160">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-160">Field</span></span>            | <span data-ttu-id="f6f42-161">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="f6f42-162">收入代码</span><span class="sxs-lookup"><span data-stu-id="f6f42-162">Earnings code</span></span>    | <span data-ttu-id="f6f42-163">奖金</span><span class="sxs-lookup"><span data-stu-id="f6f42-163">Bonus</span></span>    |
| <span data-ttu-id="f6f42-164">数量</span><span class="sxs-lookup"><span data-stu-id="f6f42-164">Quantity</span></span>         | <span data-ttu-id="f6f42-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="f6f42-165">1.0000</span></span>   |
| <span data-ttu-id="f6f42-166">比率</span><span class="sxs-lookup"><span data-stu-id="f6f42-166">Rate</span></span>             | <span data-ttu-id="f6f42-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="f6f42-167">4250.00</span></span>  |
| <span data-ttu-id="f6f42-168">行明细选项卡</span><span class="sxs-lookup"><span data-stu-id="f6f42-168">Line details tab</span></span> |          |
| <span data-ttu-id="f6f42-169">手动</span><span class="sxs-lookup"><span data-stu-id="f6f42-169">Manual</span></span>           | <span data-ttu-id="f6f42-170">（已标记）</span><span class="sxs-lookup"><span data-stu-id="f6f42-170">(marked)</span></span> |

<span data-ttu-id="f6f42-171">行 3：**收益表行**选项卡</span><span class="sxs-lookup"><span data-stu-id="f6f42-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="f6f42-172">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-172">Field</span></span>           | <span data-ttu-id="f6f42-173">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="f6f42-174">收入代码</span><span class="sxs-lookup"><span data-stu-id="f6f42-174">Earnings code</span></span>   | <span data-ttu-id="f6f42-175">佣金</span><span class="sxs-lookup"><span data-stu-id="f6f42-175">Commission</span></span> |
| <span data-ttu-id="f6f42-176">数量</span><span class="sxs-lookup"><span data-stu-id="f6f42-176">Quantity</span></span>        | <span data-ttu-id="f6f42-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="f6f42-177">1.0000</span></span>     |
| <span data-ttu-id="f6f42-178">比率</span><span class="sxs-lookup"><span data-stu-id="f6f42-178">Rate</span></span>            | <span data-ttu-id="f6f42-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="f6f42-179">!,299.00</span></span>   |
| <span data-ttu-id="f6f42-180">比率</span><span class="sxs-lookup"><span data-stu-id="f6f42-180">Rate</span></span>            | <span data-ttu-id="f6f42-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="f6f42-181">1,299.00</span></span>   |
| <span data-ttu-id="f6f42-182">行明细选项卡</span><span class="sxs-lookup"><span data-stu-id="f6f42-182">Line detail tab</span></span> |            |
| <span data-ttu-id="f6f42-183">手动</span><span class="sxs-lookup"><span data-stu-id="f6f42-183">Manual</span></span>          | <span data-ttu-id="f6f42-184">（已标记）</span><span class="sxs-lookup"><span data-stu-id="f6f42-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="f6f42-185">在**行明细**选项卡上为每个收益表行将**手动**滑块设置为**是**是为每个工作人员输入工资单期初余额的关键。</span><span class="sxs-lookup"><span data-stu-id="f6f42-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="f6f42-186">在**操作**窗格上，单击**发放收益表** USA-FED-ER-FICA。</span><span class="sxs-lookup"><span data-stu-id="f6f42-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="f6f42-187">在**操作**窗格上单击**工资单**以打开**生成工资单**页并进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="f6f42-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="f6f42-188">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-188">Field</span></span>              | <span data-ttu-id="f6f42-189">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="f6f42-190">付款日期</span><span class="sxs-lookup"><span data-stu-id="f6f42-190">Payment date</span></span>       | <span data-ttu-id="f6f42-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="f6f42-191">6/30/2017</span></span> |
| <span data-ttu-id="f6f42-192">付款运行类型</span><span class="sxs-lookup"><span data-stu-id="f6f42-192">Payment run type</span></span>   | <span data-ttu-id="f6f42-193">手动</span><span class="sxs-lookup"><span data-stu-id="f6f42-193">Manual</span></span>    |
| <span data-ttu-id="f6f42-194">禁用会计</span><span class="sxs-lookup"><span data-stu-id="f6f42-194">Disable accounting</span></span> |   <span data-ttu-id="f6f42-195">是</span><span class="sxs-lookup"><span data-stu-id="f6f42-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="f6f42-196">这仅当付款运行类型为手动且用户要在付款运行上禁用核算时可用。</span><span class="sxs-lookup"><span data-stu-id="f6f42-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="f6f42-197">单击**确定**并关闭**信息日志**。</span><span class="sxs-lookup"><span data-stu-id="f6f42-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="f6f42-198">为什么在生成工资单时需将“禁用核算”滑块设置为“是”？</span><span class="sxs-lookup"><span data-stu-id="f6f42-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="f6f42-199">将滑块设置为**是**可以防止工资单中的行被分配到总帐。</span><span class="sxs-lookup"><span data-stu-id="f6f42-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="f6f42-200">在输入来自旧系统的帐户余额时，总帐金额可以及早更新。</span><span class="sxs-lookup"><span data-stu-id="f6f42-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="f6f42-201">输入工资的期初余额允许你生成包括来自往年以及用于为了福利和纳税目的而标识限额的信息的报表。</span><span class="sxs-lookup"><span data-stu-id="f6f42-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="f6f42-202">C.</span><span class="sxs-lookup"><span data-stu-id="f6f42-202">C.</span></span> <span data-ttu-id="f6f42-203">为员工创建工资单</span><span class="sxs-lookup"><span data-stu-id="f6f42-203">Create pay statements for employees</span></span>
<span data-ttu-id="f6f42-204">生成具有期初余额的工资单后，必须验证工资单是否准确反映工资单数据。</span><span class="sxs-lookup"><span data-stu-id="f6f42-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="f6f42-205">您也必须手动更新福利和税务信息以匹配上一个工资系统中的值。</span><span class="sxs-lookup"><span data-stu-id="f6f42-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="f6f42-206">验证上一个工资系统的金额与当前工资单上的金额匹配后，必须最终完成工资单。</span><span class="sxs-lookup"><span data-stu-id="f6f42-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="f6f42-207">打开**所有工资单**页。</span><span class="sxs-lookup"><span data-stu-id="f6f42-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="f6f42-208">突出显示上一次为 Michael Redmond 生成的工资单</span><span class="sxs-lookup"><span data-stu-id="f6f42-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="f6f42-209">单击**编辑**以打开**工资单**页。</span><span class="sxs-lookup"><span data-stu-id="f6f42-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="f6f42-210">打开**福利扣缴**选项卡并输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="f6f42-210">Open the **Benefit deductions** tab and enter the following:</span></span>

|       <span data-ttu-id="f6f42-211">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-211">Field</span></span>       |      <span data-ttu-id="f6f42-212">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-212">Value</span></span>       |
|-------------------|------------------|
|      <span data-ttu-id="f6f42-213">福利</span><span class="sxs-lookup"><span data-stu-id="f6f42-213">Benefit</span></span>      | <span data-ttu-id="f6f42-214">扣减金额</span><span class="sxs-lookup"><span data-stu-id="f6f42-214">Deduction amount</span></span> |
|       <span data-ttu-id="f6f42-215">401K</span><span class="sxs-lookup"><span data-stu-id="f6f42-215">401K</span></span>        |   <span data-ttu-id="f6f42-216">参与</span><span class="sxs-lookup"><span data-stu-id="f6f42-216">Participate</span></span>    |
|      <span data-ttu-id="f6f42-217">牙齿保险</span><span class="sxs-lookup"><span data-stu-id="f6f42-217">Dental</span></span>       |      <span data-ttu-id="f6f42-218">子空间</span><span class="sxs-lookup"><span data-stu-id="f6f42-218">SubSp</span></span>       |
| <span data-ttu-id="f6f42-219">被抚养人照顾支出</span><span class="sxs-lookup"><span data-stu-id="f6f42-219">Dep care spending</span></span> |   <span data-ttu-id="f6f42-220">参与</span><span class="sxs-lookup"><span data-stu-id="f6f42-220">Participate</span></span>    |
|      <span data-ttu-id="f6f42-221">愿景</span><span class="sxs-lookup"><span data-stu-id="f6f42-221">Vision</span></span>       |      <span data-ttu-id="f6f42-222">子空间</span><span class="sxs-lookup"><span data-stu-id="f6f42-222">SupSp</span></span>       |

5. <span data-ttu-id="f6f42-223">在**福利缴纳**选项卡中输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="f6f42-223">In the **Benefit contributions** tab and enter the following:</span></span>

|  <span data-ttu-id="f6f42-224">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-224">Field</span></span>  |        <span data-ttu-id="f6f42-225">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-225">Value</span></span>        |
|---------|---------------------|
| <span data-ttu-id="f6f42-226">福利</span><span class="sxs-lookup"><span data-stu-id="f6f42-226">Benefit</span></span> | <span data-ttu-id="f6f42-227">缴纳金额</span><span class="sxs-lookup"><span data-stu-id="f6f42-227">Contribution amount</span></span> |
|  <span data-ttu-id="f6f42-228">401K</span><span class="sxs-lookup"><span data-stu-id="f6f42-228">401K</span></span>   |     <span data-ttu-id="f6f42-229">参与</span><span class="sxs-lookup"><span data-stu-id="f6f42-229">Participate</span></span>     |
| <span data-ttu-id="f6f42-230">牙齿保险</span><span class="sxs-lookup"><span data-stu-id="f6f42-230">Dental</span></span>  |        <span data-ttu-id="f6f42-231">子空间</span><span class="sxs-lookup"><span data-stu-id="f6f42-231">SubSp</span></span>        |
| <span data-ttu-id="f6f42-232">愿景</span><span class="sxs-lookup"><span data-stu-id="f6f42-232">Vision</span></span>  |        <span data-ttu-id="f6f42-233">子空间</span><span class="sxs-lookup"><span data-stu-id="f6f42-233">SubSp</span></span>        |

6. <span data-ttu-id="f6f42-234">在**税款扣缴**选项卡中输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="f6f42-234">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="f6f42-235">字段</span><span class="sxs-lookup"><span data-stu-id="f6f42-235">Field</span></span>           | <span data-ttu-id="f6f42-236">值</span><span class="sxs-lookup"><span data-stu-id="f6f42-236">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="f6f42-237">税码</span><span class="sxs-lookup"><span data-stu-id="f6f42-237">Tax code</span></span>        | <span data-ttu-id="f6f42-238">扣减金额</span><span class="sxs-lookup"><span data-stu-id="f6f42-238">Deduction amount</span></span> |
| <span data-ttu-id="f6f42-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="f6f42-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="f6f42-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="f6f42-240">1600.00</span></span>          |
| <span data-ttu-id="f6f42-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="f6f42-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="f6f42-242">825.75</span><span class="sxs-lookup"><span data-stu-id="f6f42-242">825.75</span></span>           |

7. <span data-ttu-id="f6f42-243">在**税款缴纳**选项卡中输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="f6f42-243">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="f6f42-244">单击**计算**。</span><span class="sxs-lookup"><span data-stu-id="f6f42-244">Click **Calculate**.</span></span>
   > [!IMPORTANT] 
   > <span data-ttu-id="f6f42-245">验证工作人员的工资单合计是否与旧系统年初至今金额匹配。</span><span class="sxs-lookup"><span data-stu-id="f6f42-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="f6f42-246">您可以要暂时停止最终完成下一个步骤以对所有工资单综合进行一些总体验证。</span><span class="sxs-lookup"><span data-stu-id="f6f42-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="f6f42-247">验证完成后，运行所有工资单并最终完成。</span><span class="sxs-lookup"><span data-stu-id="f6f42-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="f6f42-248">如果有必要对每一年的所有以前的季度执行相同流程，则可以按季度增量执行该流程。</span><span class="sxs-lookup"><span data-stu-id="f6f42-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="f6f42-249">这仅在客户需要在不返回旧系统中的情况下按季度查看数据时才需要。</span><span class="sxs-lookup"><span data-stu-id="f6f42-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="f6f42-250">如果您在为员工输入期初余额时出现错误</span><span class="sxs-lookup"><span data-stu-id="f6f42-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="f6f42-251">可以冲销和重新输入交易记录。</span><span class="sxs-lookup"><span data-stu-id="f6f42-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="f6f42-252">要冲销交易记录，只须在**所有工资单**页上完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f6f42-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="f6f42-253">单击**冲销**。</span><span class="sxs-lookup"><span data-stu-id="f6f42-253">Click **Reverse**.</span></span>

2. <span data-ttu-id="f6f42-254">显示以下消息时单击**是**：“在您冲销此工资单时，将创建冲销中工资单用于抵消此工资单。</span><span class="sxs-lookup"><span data-stu-id="f6f42-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="f6f42-255">任何一个工资单均无法编辑。</span><span class="sxs-lookup"><span data-stu-id="f6f42-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="f6f42-256">是否希望冲销此工资单？”</span><span class="sxs-lookup"><span data-stu-id="f6f42-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="f6f42-257">。</span><span class="sxs-lookup"><span data-stu-id="f6f42-257">displays.</span></span> 

<span data-ttu-id="f6f42-258">在你冲销工资单后，可以从你以前创建的收益表为工作人员生成新的工资单。</span><span class="sxs-lookup"><span data-stu-id="f6f42-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="f6f42-259">在生成新的工资单前，确保更正收益表上的任何不正确的行，然后使用正确的金额生成新的工资单。</span><span class="sxs-lookup"><span data-stu-id="f6f42-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

