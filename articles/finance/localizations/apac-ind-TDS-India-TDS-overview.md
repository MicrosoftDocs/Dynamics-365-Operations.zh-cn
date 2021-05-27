---
title: 印度从源扣缴税款 (TDS) 概述
description: 本主题提供有关印度从源扣缴税款 (TDS) 的详细信息。 TDS 文档涵盖了此功能的功能性。
author: kailiang
ms.date: 03/19/2021
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
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023071"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="f66e8-104">印度从源扣缴税款 (TDS) 概述</span><span class="sxs-lookup"><span data-stu-id="f66e8-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f66e8-105">本主题提供有关印度从源扣缴税款 (TDS) 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f66e8-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="f66e8-106">TDS 文档涵盖了此功能的功能性。</span><span class="sxs-lookup"><span data-stu-id="f66e8-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="f66e8-107">它还说明了如何进行 TDS 的基本设置，计算交易的 TDS，完成 TDS 结算流程，记录 TDS 证书编号以及生成 TDS 查询、TDS 对帐单和 TDS 证书。</span><span class="sxs-lookup"><span data-stu-id="f66e8-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="f66e8-108">该文档包含以下主题：</span><span class="sxs-lookup"><span data-stu-id="f66e8-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="f66e8-109">TDS 的基本设置</span><span class="sxs-lookup"><span data-stu-id="f66e8-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="f66e8-110">用于 TDS 计算的公式设计器和阈值限制功能</span><span class="sxs-lookup"><span data-stu-id="f66e8-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="f66e8-111">发票、付款、本票和内部公司交易的 TDS 计算</span><span class="sxs-lookup"><span data-stu-id="f66e8-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="f66e8-112">定期 TDS 结算流程和针对 TDS 主管机构供应商的 TDS 金额结算</span><span class="sxs-lookup"><span data-stu-id="f66e8-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="f66e8-113">记录和更新 TDS 证书编号和日期</span><span class="sxs-lookup"><span data-stu-id="f66e8-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="f66e8-114">TDS 简介</span><span class="sxs-lookup"><span data-stu-id="f66e8-114">Introduction to TDS</span></span>

<span data-ttu-id="f66e8-115">根据 1961 年的《所得税法》，所得税由服务的接收方在预付款或信用赊帐（以先发生者为准）时从源扣除。</span><span class="sxs-lookup"><span data-stu-id="f66e8-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="f66e8-116">进行付款的人必须扣除税额，仅向服务的提供方支付净余额。</span><span class="sxs-lookup"><span data-stu-id="f66e8-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="f66e8-117">TDS 适用于政府指定的服务，使用政府在某个期间指定的费率扣除税款。</span><span class="sxs-lookup"><span data-stu-id="f66e8-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="f66e8-118">扣除费率基于接收付款或提供服务的实体的状态。</span><span class="sxs-lookup"><span data-stu-id="f66e8-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="f66e8-119">状态包括 **个人**、**印度教家庭** (**HUF**)、**公司**、**事务所**、**人员协会** (**AOP**)、**个人集合体** (**BOI**) 和 **本地主管机构**。</span><span class="sxs-lookup"><span data-stu-id="f66e8-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="f66e8-120">以下各节列出了印度政府指定的 TDS 适用的服务。</span><span class="sxs-lookup"><span data-stu-id="f66e8-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="f66e8-121">**居民**</span><span class="sxs-lookup"><span data-stu-id="f66e8-121">**Residents**</span></span>

- <span data-ttu-id="f66e8-122">薪金收入（根据第 192 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="f66e8-123">证券利息收入（根据第 193 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="f66e8-124">股息收入（根据第 194 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="f66e8-125">利息收入（根据第 194A 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="f66e8-126">彩票或益智游戏收入（根据第 194B 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="f66e8-127">赛马等奖金（根据第 194BB 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="f66e8-128">承包商和分包商（根据第 194C 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="f66e8-129">保险佣金（根据第 194D 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="f66e8-130">国民储蓄计划的存款收入（根据第 194EE 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="f66e8-131">共同基金或 UTI 收入（根据第 194F 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="f66e8-132">贱价抛售或抽奖的佣金、薪酬、奖金等（根据第 194G 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="f66e8-133">佣金或经纪费付款（根据第 194H 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="f66e8-134">租金（根据第 194I 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="f66e8-135">专业服务（根据第 194J 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="f66e8-136">单位收入（根据第 194K 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="f66e8-137">购置某些不动产的补偿费（根据第 194LA 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="f66e8-138">**非居民**</span><span class="sxs-lookup"><span data-stu-id="f66e8-138">**Non-residents**</span></span>

- <span data-ttu-id="f66e8-139">支付给非居民运动员或体育协会的费用（根据第 194E 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="f66e8-140">其他款项（根据第 195 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="f66e8-141">关于非居民单位的收入（根据第 196A 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="f66e8-142">印度公司的外币债券或股票收入（根据第 196C 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="f66e8-143">境外机构投资者的证券收入（根据第 196D 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="f66e8-144">薪金和任何人均收入下的所有其他正收入（第 192 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="f66e8-145">证券利息（第 193 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="f66e8-146">除证券利息外的利息（第 194A 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="f66e8-147">支付给承包商和分包商的费用（第 194C 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="f66e8-148">彩票或填字游戏奖金（第 194B 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="f66e8-149">赛马奖金（第 194BB 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="f66e8-150">包括购买保险业务的所有付款的保险佣金（第 194D 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="f66e8-151">除应付给不是公司或外国公司的非居民的证券利息以外的任何利息（第 195 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="f66e8-152">支付给非居民运动员（包括运动员、体育协会或机构）的费用。</span><span class="sxs-lookup"><span data-stu-id="f66e8-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="f66e8-153">如果是非居民运动员，在印度的报纸、杂志等刊登任何比赛/体育的广告和文章等方面支付的费用。</span><span class="sxs-lookup"><span data-stu-id="f66e8-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="f66e8-154">包含的款项（第 194E 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="f66e8-155">支付 NSS \[国民储蓄计划\] 的存款费用（第 194EE 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="f66e8-156">支付共同基金或 UTI 的回购单位的费用（第 194F 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="f66e8-157">支付佣金或经纪费（第 194H 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="f66e8-158">支付租金（第 194I 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="f66e8-159">支付专业或技术服务的费用（第 194J 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="f66e8-160">彩票的发行者、分销商、买家、卖家的佣金，包括此类票证的薪酬或奖金（第 194G 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="f66e8-161">外币买入单位或外币买入单位转让所产生的长期资本收益的收入（第 196B 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="f66e8-162">向非居民支付债券和股票的利息或股息的任何收入（第 196C 节）</span><span class="sxs-lookup"><span data-stu-id="f66e8-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="f66e8-163">根据采购、销售、销售退货、贷方通知单、固定资产购置、预付款、提前付款、本票、就业税和内部公司交易计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="f66e8-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="f66e8-164">在当前的印度税务方案中，不根据销售交易计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="f66e8-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="f66e8-165">但是，系统包括一项规定，根据销售交易（尤其是内部公司交易）计算可退税的 TDS。</span><span class="sxs-lookup"><span data-stu-id="f66e8-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="f66e8-166">计算 TDS 时始终考虑为 TDS 组分定义的阈值和异常阈值。</span><span class="sxs-lookup"><span data-stu-id="f66e8-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="f66e8-167">必须运行定期 TDS 结算流程，并且必须将 TDS 付款结算给 TDS 主管机构供应商。</span><span class="sxs-lookup"><span data-stu-id="f66e8-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="f66e8-168">可以记录和更新从供应商或客户收到的 TDS 证书的证书编号和日期。</span><span class="sxs-lookup"><span data-stu-id="f66e8-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="f66e8-169">此外，可以在 Finance 中生成表单 26Q 和表单 27Q 季度对帐单以及 TDS 的表单 16A 证书。</span><span class="sxs-lookup"><span data-stu-id="f66e8-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="f66e8-170">设置和使用 TDS</span><span class="sxs-lookup"><span data-stu-id="f66e8-170">Setting up and working with TDS</span></span>

<span data-ttu-id="f66e8-171">下面概述了设置和使用 TDS 的流程：</span><span class="sxs-lookup"><span data-stu-id="f66e8-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="f66e8-172">**TDS 设置：**</span><span class="sxs-lookup"><span data-stu-id="f66e8-172">**TDS setup:**</span></span>

    - <span data-ttu-id="f66e8-173">参数设置：</span><span class="sxs-lookup"><span data-stu-id="f66e8-173">Parameter setup:</span></span>

        - <span data-ttu-id="f66e8-174">在总帐参数中，激活与 TDS 相关的参数。</span><span class="sxs-lookup"><span data-stu-id="f66e8-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="f66e8-175">在总帐参数中，设置预缴税金付款的编号规则。</span><span class="sxs-lookup"><span data-stu-id="f66e8-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="f66e8-176">在应付帐款和应收帐款中设置参数。</span><span class="sxs-lookup"><span data-stu-id="f66e8-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="f66e8-177">基本设置：</span><span class="sxs-lookup"><span data-stu-id="f66e8-177">Basic setup:</span></span>

        - <span data-ttu-id="f66e8-178">设置公司、客户和供应商的 TDS 登记编号。</span><span class="sxs-lookup"><span data-stu-id="f66e8-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="f66e8-179">设置 TDS 组分组。</span><span class="sxs-lookup"><span data-stu-id="f66e8-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="f66e8-180">设置 TDS 组分，向其附加 TDS 组分组，并为其定义阈值和异常阈值。</span><span class="sxs-lookup"><span data-stu-id="f66e8-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="f66e8-181">设置 TDS 主管机构。</span><span class="sxs-lookup"><span data-stu-id="f66e8-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="f66e8-182">设置 TDS 结算期间。</span><span class="sxs-lookup"><span data-stu-id="f66e8-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="f66e8-183">设置 TDS 税码，并向其附加 TDS 组分。</span><span class="sxs-lookup"><span data-stu-id="f66e8-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="f66e8-184">设置 TDS 税组，并向其附加 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="f66e8-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="f66e8-185">在公式设计器中，定义一个公式以计算 TDS 组的 TDS。</span><span class="sxs-lookup"><span data-stu-id="f66e8-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="f66e8-186">记录 TDS 减免证书编号。</span><span class="sxs-lookup"><span data-stu-id="f66e8-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="f66e8-187">分类帐帐户和公司设置：</span><span class="sxs-lookup"><span data-stu-id="f66e8-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="f66e8-188">设置 TDS 应付分类帐帐户和应收分类帐帐户。</span><span class="sxs-lookup"><span data-stu-id="f66e8-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="f66e8-189">设置公司的减税和纳税帐户编号 (TAN) 和扣税类型类别。</span><span class="sxs-lookup"><span data-stu-id="f66e8-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="f66e8-190">其他设置：</span><span class="sxs-lookup"><span data-stu-id="f66e8-190">Other setup:</span></span>

        - <span data-ttu-id="f66e8-191">设置包括 TDS 分配的付款计划。</span><span class="sxs-lookup"><span data-stu-id="f66e8-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="f66e8-192">为 TDS 主管机构设置付款的付款费用类型。</span><span class="sxs-lookup"><span data-stu-id="f66e8-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="f66e8-193">为供应商和客户设置有关 TDS 组，永久帐号 (PAN) 和 TAN 的信息。</span><span class="sxs-lookup"><span data-stu-id="f66e8-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="f66e8-194">**交易中的 TDS 计算：**</span><span class="sxs-lookup"><span data-stu-id="f66e8-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="f66e8-195">账单和付款</span><span class="sxs-lookup"><span data-stu-id="f66e8-195">Invoices and payments</span></span>
    - <span data-ttu-id="f66e8-196">本票</span><span class="sxs-lookup"><span data-stu-id="f66e8-196">Promissory notes</span></span>
    - <span data-ttu-id="f66e8-197">预先付款</span><span class="sxs-lookup"><span data-stu-id="f66e8-197">Advance payments</span></span>
    - <span data-ttu-id="f66e8-198">预付款</span><span class="sxs-lookup"><span data-stu-id="f66e8-198">Prepayments</span></span>

3. <span data-ttu-id="f66e8-199">**TDS 结算：**</span><span class="sxs-lookup"><span data-stu-id="f66e8-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="f66e8-200">定期 TDS 结算流程</span><span class="sxs-lookup"><span data-stu-id="f66e8-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="f66e8-201">向 TDS 主管机构供应商结算 TDS 付款并生成 TDS challan</span><span class="sxs-lookup"><span data-stu-id="f66e8-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="f66e8-202">**TDS 查询、对帐单和证书：**</span><span class="sxs-lookup"><span data-stu-id="f66e8-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="f66e8-203">记录和更新 TDS 证书编号和日期。</span><span class="sxs-lookup"><span data-stu-id="f66e8-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="f66e8-204">生成 TDS 查询和已过帐的 TDS 查询。</span><span class="sxs-lookup"><span data-stu-id="f66e8-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="f66e8-205">生成表单 27A、表单 26Q 和表单 27Q TDS 以及 e-TDS 季度对帐单。</span><span class="sxs-lookup"><span data-stu-id="f66e8-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="f66e8-206">生成表单 16A TDS 证书。</span><span class="sxs-lookup"><span data-stu-id="f66e8-206">Generate a Form 16A TDS certificate.</span></span>
