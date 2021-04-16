---
title: 输入工资期初余额
description: 此主题介绍为收入代码、扣除额、福利和税款输入期初余额的步骤。
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752142"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="e3d3d-103">输入工资期初余额</span><span class="sxs-lookup"><span data-stu-id="e3d3d-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3d3d-104">此主题介绍为收入代码、扣除额、福利和税款输入期初余额的步骤。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="e3d3d-105">此信息对于从其他系统转移用于新的工资单实现方式的数据的合作伙伴十分重要。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="e3d3d-106">为了准备输入期初工资单余额，我们验证以下信息：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="e3d3d-107">在系统中输入和提供员工记录</span><span class="sxs-lookup"><span data-stu-id="e3d3d-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="e3d3d-108">将以下数据设置和分配到员工：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="e3d3d-109">付薪周期和付薪期间</span><span class="sxs-lookup"><span data-stu-id="e3d3d-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="e3d3d-110">收入代码</span><span class="sxs-lookup"><span data-stu-id="e3d3d-110">Earning codes</span></span>
    - <span data-ttu-id="e3d3d-111">税金</span><span class="sxs-lookup"><span data-stu-id="e3d3d-111">Taxes</span></span>
    - <span data-ttu-id="e3d3d-112">福利和扣除额</span><span class="sxs-lookup"><span data-stu-id="e3d3d-112">Benefits and deductions</span></span>

- <span data-ttu-id="e3d3d-113">公司应已选择可以设置工资单期初余额的日期。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="e3d3d-114">已从旧系统收集关于所有收入、福利/扣除额、福利缴纳、员工税款以及雇主税款及其年初至今金额的信息。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="e3d3d-115">当您计划输入期初余额时，考虑数据需要的详细程度。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="e3d3d-116">大多数企业输入一个合并的年初至今金额。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="e3d3d-117">但如果需要更加详细的信息，可使用季度增量输入余额。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="e3d3d-118">确定需要的详细程度决定了必须为每个工作人员手动创建多少份工资报表。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="e3d3d-119">对于单个年初至今金额，只需对每位员工手动创建一份报表。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="e3d3d-120">要执行此操作，可使用来自上一个系统的最终工资单的年初至今金额作为在新工资单系统中输入的金额。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="e3d3d-121">以下示例显示可以如何输入员工的工资单期初余额，包括收入代码、福利/扣除额和税款。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="e3d3d-122">在真实示例中，每个收入代码、福利扣缴、福利缴纳、员工税款和雇主税款都有一个行项输入的金额为年初至今金额。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="e3d3d-123">使用该代码和金额列表，按照创建已禁用核算的人工收入和工资单的步骤获取用于工资单目的的期初余额。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="e3d3d-124">禁用核算的原因是因为您不想将此期初余额工资单过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="e3d3d-125">这在旧系统中完成，并且当您在设置总帐中的期初余额时转移到新系统。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="e3d3d-126">A.</span><span class="sxs-lookup"><span data-stu-id="e3d3d-126">A.</span></span> <span data-ttu-id="e3d3d-127">如何设置要在工资单期初余额上使用的收入代码</span><span class="sxs-lookup"><span data-stu-id="e3d3d-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="e3d3d-128">当您输入工资单期初余额时，确保将您要使用的收入代码配置为启用“允许编辑收益表费率”选项。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="e3d3d-129">这可以使您手动键入来自旧系统的金额。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="e3d3d-130">B.</span><span class="sxs-lookup"><span data-stu-id="e3d3d-130">B.</span></span> <span data-ttu-id="e3d3d-131">为员工创建收益表以获得期初余额</span><span class="sxs-lookup"><span data-stu-id="e3d3d-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="e3d3d-132">此步骤为每个工作人员手动创建旧系统最后一次付薪期间的收益表，这将在新的工资单系统中创建收益表行。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="e3d3d-133">按每个收入代码以及年初至今金额和工时各输入一行。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="e3d3d-134">示例步骤如下：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="e3d3d-135">打开 **所有收益表** 页并单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="e3d3d-136">输入以下内容：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-136">Enter the following:</span></span> 

    | <span data-ttu-id="e3d3d-137">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-137">Field</span></span>      | <span data-ttu-id="e3d3d-138">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="e3d3d-139">工作线程</span><span class="sxs-lookup"><span data-stu-id="e3d3d-139">Worker</span></span>     | <span data-ttu-id="e3d3d-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="e3d3d-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="e3d3d-141">付薪周期</span><span class="sxs-lookup"><span data-stu-id="e3d3d-141">Pay cycle</span></span>  | <span data-ttu-id="e3d3d-142">sm</span><span class="sxs-lookup"><span data-stu-id="e3d3d-142">sm</span></span>                    |
    | <span data-ttu-id="e3d3d-143">付薪期间</span><span class="sxs-lookup"><span data-stu-id="e3d3d-143">Pay period</span></span> | <span data-ttu-id="e3d3d-144">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="e3d3d-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="e3d3d-145">在 **收益表行** 选项卡上输入以下数据：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="e3d3d-146">行 1：**收益表行** 选项卡</span><span class="sxs-lookup"><span data-stu-id="e3d3d-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="e3d3d-147">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-147">Field</span></span>            | <span data-ttu-id="e3d3d-148">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="e3d3d-149">收入代码</span><span class="sxs-lookup"><span data-stu-id="e3d3d-149">Earnings code</span></span>    | <span data-ttu-id="e3d3d-150">常规付薪</span><span class="sxs-lookup"><span data-stu-id="e3d3d-150">Regular pay</span></span> |
    | <span data-ttu-id="e3d3d-151">数量</span><span class="sxs-lookup"><span data-stu-id="e3d3d-151">Quantity</span></span>         | <span data-ttu-id="e3d3d-152">1.00</span><span class="sxs-lookup"><span data-stu-id="e3d3d-152">1.00</span></span>        |
    | <span data-ttu-id="e3d3d-153">费率</span><span class="sxs-lookup"><span data-stu-id="e3d3d-153">Rate</span></span>             | <span data-ttu-id="e3d3d-154">30,000</span><span class="sxs-lookup"><span data-stu-id="e3d3d-154">30,000</span></span>      |
    | <span data-ttu-id="e3d3d-155">行明细选项卡</span><span class="sxs-lookup"><span data-stu-id="e3d3d-155">Line details tab</span></span> |             |
    | <span data-ttu-id="e3d3d-156">手动</span><span class="sxs-lookup"><span data-stu-id="e3d3d-156">Manual</span></span>           | <span data-ttu-id="e3d3d-157">（已标记）</span><span class="sxs-lookup"><span data-stu-id="e3d3d-157">(marked)</span></span>    |

    <span data-ttu-id="e3d3d-158">行 2：**收益表行** 选项卡</span><span class="sxs-lookup"><span data-stu-id="e3d3d-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="e3d3d-159">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-159">Field</span></span>            | <span data-ttu-id="e3d3d-160">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="e3d3d-161">收入代码</span><span class="sxs-lookup"><span data-stu-id="e3d3d-161">Earnings code</span></span>    | <span data-ttu-id="e3d3d-162">奖金</span><span class="sxs-lookup"><span data-stu-id="e3d3d-162">Bonus</span></span>    |
    | <span data-ttu-id="e3d3d-163">数量</span><span class="sxs-lookup"><span data-stu-id="e3d3d-163">Quantity</span></span>         | <span data-ttu-id="e3d3d-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="e3d3d-164">1.0000</span></span>   |
    | <span data-ttu-id="e3d3d-165">比率</span><span class="sxs-lookup"><span data-stu-id="e3d3d-165">Rate</span></span>             | <span data-ttu-id="e3d3d-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="e3d3d-166">4250.00</span></span>  |
    | <span data-ttu-id="e3d3d-167">行明细选项卡</span><span class="sxs-lookup"><span data-stu-id="e3d3d-167">Line details tab</span></span> |          |
    | <span data-ttu-id="e3d3d-168">手动</span><span class="sxs-lookup"><span data-stu-id="e3d3d-168">Manual</span></span>           | <span data-ttu-id="e3d3d-169">（已标记）</span><span class="sxs-lookup"><span data-stu-id="e3d3d-169">(marked)</span></span> |

    <span data-ttu-id="e3d3d-170">行 3：**收益表行** 选项卡</span><span class="sxs-lookup"><span data-stu-id="e3d3d-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="e3d3d-171">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-171">Field</span></span>           | <span data-ttu-id="e3d3d-172">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="e3d3d-173">收入代码</span><span class="sxs-lookup"><span data-stu-id="e3d3d-173">Earnings code</span></span>   | <span data-ttu-id="e3d3d-174">佣金</span><span class="sxs-lookup"><span data-stu-id="e3d3d-174">Commission</span></span> |
    | <span data-ttu-id="e3d3d-175">数量</span><span class="sxs-lookup"><span data-stu-id="e3d3d-175">Quantity</span></span>        | <span data-ttu-id="e3d3d-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="e3d3d-176">1.0000</span></span>     |
    | <span data-ttu-id="e3d3d-177">比率</span><span class="sxs-lookup"><span data-stu-id="e3d3d-177">Rate</span></span>            | <span data-ttu-id="e3d3d-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="e3d3d-178">!,299.00</span></span>   |
    | <span data-ttu-id="e3d3d-179">比率</span><span class="sxs-lookup"><span data-stu-id="e3d3d-179">Rate</span></span>            | <span data-ttu-id="e3d3d-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="e3d3d-180">1,299.00</span></span>   |
    | <span data-ttu-id="e3d3d-181">行明细选项卡</span><span class="sxs-lookup"><span data-stu-id="e3d3d-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="e3d3d-182">手动</span><span class="sxs-lookup"><span data-stu-id="e3d3d-182">Manual</span></span>          | <span data-ttu-id="e3d3d-183">（已标记）</span><span class="sxs-lookup"><span data-stu-id="e3d3d-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="e3d3d-184">在 **行明细** 选项卡上为每个收益表行将 **手动** 滑块设置为 **是** 是为每个工作人员输入工资单期初余额的关键。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="e3d3d-185">在 **操作** 窗格上，单击 **发放收益表** USA-FED-ER-FICA。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="e3d3d-186">在 **操作** 窗格上单击 **工资单** 以打开 **生成工资单** 页并进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="e3d3d-187">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-187">Field</span></span>              | <span data-ttu-id="e3d3d-188">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="e3d3d-189">付款日期</span><span class="sxs-lookup"><span data-stu-id="e3d3d-189">Payment date</span></span>       | <span data-ttu-id="e3d3d-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="e3d3d-190">6/30/2017</span></span> |
    | <span data-ttu-id="e3d3d-191">付款运行类型</span><span class="sxs-lookup"><span data-stu-id="e3d3d-191">Payment run type</span></span>   | <span data-ttu-id="e3d3d-192">手动</span><span class="sxs-lookup"><span data-stu-id="e3d3d-192">Manual</span></span>    |
    | <span data-ttu-id="e3d3d-193">禁用会计</span><span class="sxs-lookup"><span data-stu-id="e3d3d-193">Disable accounting</span></span> |   <span data-ttu-id="e3d3d-194">是</span><span class="sxs-lookup"><span data-stu-id="e3d3d-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="e3d3d-195">这仅当付款运行类型为手动且用户要在付款运行上禁用核算时可用。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="e3d3d-196">单击 **确定** 并关闭 **信息日志**。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="e3d3d-197">为什么在生成工资单时需将“禁用核算”滑块设置为“是”？</span><span class="sxs-lookup"><span data-stu-id="e3d3d-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="e3d3d-198">将滑块设置为 **是** 可以防止工资单中的行被分配到总帐。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="e3d3d-199">在输入来自旧系统的帐户余额时，总帐金额可以及早更新。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="e3d3d-200">输入工资的期初余额允许你生成包括来自往年以及用于为了福利和纳税目的而标识限额的信息的报表。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="e3d3d-201">C.</span><span class="sxs-lookup"><span data-stu-id="e3d3d-201">C.</span></span> <span data-ttu-id="e3d3d-202">为员工创建工资单</span><span class="sxs-lookup"><span data-stu-id="e3d3d-202">Create pay statements for employees</span></span>

<span data-ttu-id="e3d3d-203">生成具有期初余额的工资单后，必须验证工资单是否准确反映工资单数据。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="e3d3d-204">您也必须手动更新福利和税务信息以匹配上一个工资系统中的值。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="e3d3d-205">验证上一个工资系统的金额与当前工资单上的金额匹配后，必须最终完成工资单。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="e3d3d-206">打开 **所有工资单** 页。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="e3d3d-207">突出显示上一次为 Michael Redmond 生成的工资单</span><span class="sxs-lookup"><span data-stu-id="e3d3d-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="e3d3d-208">单击 **编辑** 以打开 **工资单** 页。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="e3d3d-209">打开 **福利扣缴** 选项卡并输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="e3d3d-210">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-210">Field</span></span>             | <span data-ttu-id="e3d3d-211">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="e3d3d-212">福利</span><span class="sxs-lookup"><span data-stu-id="e3d3d-212">Benefit</span></span>           | <span data-ttu-id="e3d3d-213">扣减金额</span><span class="sxs-lookup"><span data-stu-id="e3d3d-213">Deduction amount</span></span> |
    | <span data-ttu-id="e3d3d-214">401K</span><span class="sxs-lookup"><span data-stu-id="e3d3d-214">401K</span></span>              | <span data-ttu-id="e3d3d-215">参与</span><span class="sxs-lookup"><span data-stu-id="e3d3d-215">Participate</span></span>      |
    | <span data-ttu-id="e3d3d-216">牙齿保险</span><span class="sxs-lookup"><span data-stu-id="e3d3d-216">Dental</span></span>            | <span data-ttu-id="e3d3d-217">子空间</span><span class="sxs-lookup"><span data-stu-id="e3d3d-217">SubSp</span></span>            |
    | <span data-ttu-id="e3d3d-218">被抚养人照顾支出</span><span class="sxs-lookup"><span data-stu-id="e3d3d-218">Dep care spending</span></span> | <span data-ttu-id="e3d3d-219">参与</span><span class="sxs-lookup"><span data-stu-id="e3d3d-219">Participate</span></span>      |
    | <span data-ttu-id="e3d3d-220">愿景</span><span class="sxs-lookup"><span data-stu-id="e3d3d-220">Vision</span></span>            | <span data-ttu-id="e3d3d-221">子空间</span><span class="sxs-lookup"><span data-stu-id="e3d3d-221">SupSp</span></span>            |

5. <span data-ttu-id="e3d3d-222">在 **福利缴纳** 选项卡中输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="e3d3d-223">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-223">Field</span></span>   | <span data-ttu-id="e3d3d-224">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="e3d3d-225">福利</span><span class="sxs-lookup"><span data-stu-id="e3d3d-225">Benefit</span></span> | <span data-ttu-id="e3d3d-226">缴纳金额</span><span class="sxs-lookup"><span data-stu-id="e3d3d-226">Contribution amount</span></span> |
    | <span data-ttu-id="e3d3d-227">401K</span><span class="sxs-lookup"><span data-stu-id="e3d3d-227">401K</span></span>    | <span data-ttu-id="e3d3d-228">参与</span><span class="sxs-lookup"><span data-stu-id="e3d3d-228">Participate</span></span>         |
    | <span data-ttu-id="e3d3d-229">牙齿保险</span><span class="sxs-lookup"><span data-stu-id="e3d3d-229">Dental</span></span>  | <span data-ttu-id="e3d3d-230">子空间</span><span class="sxs-lookup"><span data-stu-id="e3d3d-230">SubSp</span></span>               |
    | <span data-ttu-id="e3d3d-231">愿景</span><span class="sxs-lookup"><span data-stu-id="e3d3d-231">Vision</span></span>  | <span data-ttu-id="e3d3d-232">子空间</span><span class="sxs-lookup"><span data-stu-id="e3d3d-232">SubSp</span></span>               |

6. <span data-ttu-id="e3d3d-233">在 **税款扣缴** 选项卡中输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="e3d3d-234">字段</span><span class="sxs-lookup"><span data-stu-id="e3d3d-234">Field</span></span>           | <span data-ttu-id="e3d3d-235">值</span><span class="sxs-lookup"><span data-stu-id="e3d3d-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="e3d3d-236">税码</span><span class="sxs-lookup"><span data-stu-id="e3d3d-236">Tax code</span></span>        | <span data-ttu-id="e3d3d-237">扣减金额</span><span class="sxs-lookup"><span data-stu-id="e3d3d-237">Deduction amount</span></span> |
    | <span data-ttu-id="e3d3d-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="e3d3d-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="e3d3d-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="e3d3d-239">1600.00</span></span>          |
    | <span data-ttu-id="e3d3d-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="e3d3d-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="e3d3d-241">825.75</span><span class="sxs-lookup"><span data-stu-id="e3d3d-241">825.75</span></span>           |

7. <span data-ttu-id="e3d3d-242">在 **税款缴纳** 选项卡中输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="e3d3d-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="e3d3d-243">单击 **计算**。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="e3d3d-244">验证工作人员的工资单合计是否与旧系统年初至今金额匹配。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="e3d3d-245">您可以要暂时停止最终完成下一个步骤以对所有工资单综合进行一些总体验证。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="e3d3d-246">验证完成后，运行所有工资单并最终完成。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="e3d3d-247">如果有必要对每一年的所有以前的季度执行相同流程，则可以按季度增量执行该流程。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="e3d3d-248">这仅在客户需要在不返回旧系统中的情况下按季度查看数据时才需要。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="e3d3d-249">如果您在为员工输入期初余额时出现错误</span><span class="sxs-lookup"><span data-stu-id="e3d3d-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="e3d3d-250">可以冲销和重新输入交易记录。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="e3d3d-251">要冲销交易记录，只须在 **所有工资单** 页上完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="e3d3d-252">单击 **冲销**。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="e3d3d-253">显示以下消息时单击 **是**：“在您冲销此工资单时，将创建冲销中工资单用于抵消此工资单。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="e3d3d-254">任何一个工资单均无法编辑。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="e3d3d-255">是否希望冲销此工资单？”</span><span class="sxs-lookup"><span data-stu-id="e3d3d-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="e3d3d-256">。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-256">displays.</span></span> 

<span data-ttu-id="e3d3d-257">在你冲销工资单后，可以从你以前创建的收益表为工作人员生成新的工资单。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="e3d3d-258">在生成新的工资单前，确保更正收益表上的任何不正确的行，然后使用正确的金额生成新的工资单。</span><span class="sxs-lookup"><span data-stu-id="e3d3d-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]