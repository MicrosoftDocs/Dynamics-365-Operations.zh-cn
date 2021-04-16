---
title: SEPA 直接借记概览
description: 单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。 国内和跨境付款之间不存在差异。 SEPA 包含 28 个欧盟 (EU) 成员国，以及冰岛、列支敦斯登、挪威、瑞士、摩纳哥和圣马力诺。 SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。 最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf3872a47a92509af5857c0c1aec0d4da4095d19
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835260"
---
# <a name="sepa-direct-debit-overview"></a><span data-ttu-id="297a4-107">SEPA 直接借记概览</span><span class="sxs-lookup"><span data-stu-id="297a4-107">SEPA direct debit overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="297a4-108">单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="297a4-108">The Single Euro Payments Area (SEPA) is set up by the European Commission, and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located.</span></span> <span data-ttu-id="297a4-109">国内和跨境付款之间不存在差异。</span><span class="sxs-lookup"><span data-stu-id="297a4-109">There is no difference between national and cross-border payments.</span></span> <span data-ttu-id="297a4-110">SEPA 包含 28 个欧盟 (EU) 成员国，以及冰岛、列支敦斯登、挪威、瑞士、摩纳哥和圣马力诺。</span><span class="sxs-lookup"><span data-stu-id="297a4-110">The SEPA includes the 28 European Union (EU) member states, as well as Iceland, Liechtenstein, Norway, Switzerland, Monaco and San Marino.</span></span> <span data-ttu-id="297a4-111">SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。</span><span class="sxs-lookup"><span data-stu-id="297a4-111">The SEPA helps form a single market for payment transactions within the European Economic Area (EEA).</span></span> <span data-ttu-id="297a4-112">最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。</span><span class="sxs-lookup"><span data-stu-id="297a4-112">Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.</span></span>   

<a name="what-is-the-goal-of-sepa-direct-debits"></a><span data-ttu-id="297a4-113">SEPA 直接借记的目标是什么？</span><span class="sxs-lookup"><span data-stu-id="297a4-113">What is the goal of SEPA direct debits?</span></span>
---------------------------------------

<span data-ttu-id="297a4-114">在向债权人授予客户已签署授权的情况下，SEPA 直接借记允许债权人从客户的银行帐户中筹集资金。</span><span class="sxs-lookup"><span data-stu-id="297a4-114">A SEPA direct debit allows a creditor to collect funds from a customer’s bank account, provided that a signed mandate has been granted by the customer to the creditor.</span></span> <span data-ttu-id="297a4-115">客户签署授权允许债权人收取付款并指示客户的银行支付该收款。</span><span class="sxs-lookup"><span data-stu-id="297a4-115">The customer signs a mandate that authorizes the creditor to collect a payment and instructs the customer’s bank to pay the collection.</span></span> 

<span data-ttu-id="297a4-116">SEPA 直接借记第一次创建了一种可以用于 32 个 SEPA 国家/地区中国内和跨境欧元直接借记的付款工具。</span><span class="sxs-lookup"><span data-stu-id="297a4-116">SEPA Direct Debits create, for the first time, a payment instrument that can be used for both national and cross-border euro direct debits throughout the 32 SEPA countries/regions.</span></span> 

<span data-ttu-id="297a4-117">可采用两种方案：SEPA 核心直接借记方案和 SEPA 企业到企业 (B2B) 直接借记方案。</span><span class="sxs-lookup"><span data-stu-id="297a4-117">There are two schemes available: the SEPA Core Direct Debit Scheme and the SEPA Business to Business (B2B) Direct Debit Scheme.</span></span> <span data-ttu-id="297a4-118">两种方案使用相同的文件格式。</span><span class="sxs-lookup"><span data-stu-id="297a4-118">Both schemes use the same file format.</span></span>

## <a name="what-is-the-core-direct-debit-scheme"></a><span data-ttu-id="297a4-119">什么是核心直接借记方案？</span><span class="sxs-lookup"><span data-stu-id="297a4-119">What is the Core Direct Debit scheme?</span></span>
<span data-ttu-id="297a4-120">SEPA 核心直接借记方案是基本方案。</span><span class="sxs-lookup"><span data-stu-id="297a4-120">The SEPA Core Direct Debit Scheme is the basic scheme.</span></span> <span data-ttu-id="297a4-121">它具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="297a4-121">It has the following attributes:</span></span>
-   <span data-ttu-id="297a4-122">资金以欧元转帐（即便是银行帐户可能以其他币种存有资金）。</span><span class="sxs-lookup"><span data-stu-id="297a4-122">The transfer of funds is in euros (even though the bank accounts may hold funds in other currencies).</span></span>
-   <span data-ttu-id="297a4-123">客户和债权人必须各自持有位于 SEPA 中信用机构的帐户。</span><span class="sxs-lookup"><span data-stu-id="297a4-123">The customer and creditor must each hold an account with a credit institution that is located within the SEPA.</span></span>
-   <span data-ttu-id="297a4-124">客户必须授予该债权人一份已签署的授权。</span><span class="sxs-lookup"><span data-stu-id="297a4-124">The customer must grant a signed mandate to the creditor.</span></span>
-   <span data-ttu-id="297a4-125">在最后启动收款的 36 个月之后授权到期。</span><span class="sxs-lookup"><span data-stu-id="297a4-125">Mandates expire 36 months after the last initiated collection.</span></span>
-   <span data-ttu-id="297a4-126">只要授权有效或在最后收款之后的至少 14 个月里，债权人必须保存授权。</span><span class="sxs-lookup"><span data-stu-id="297a4-126">The creditor must store mandates for as long as the mandate is valid and for at least 14 months after the last collection.</span></span>
-   <span data-ttu-id="297a4-127">该方案可以用于单个（一次性）收款或重复直接借记收款。</span><span class="sxs-lookup"><span data-stu-id="297a4-127">The scheme may be used for single (one-time) or recurring direct debit collections.</span></span>
-   <span data-ttu-id="297a4-128">客户在其帐户借记后长达八周内具有接收退款“不受质询”的权利。</span><span class="sxs-lookup"><span data-stu-id="297a4-128">Customers have a “no questions asked” right to receive a refund for up to eight weeks after the debit of their account.</span></span>

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a><span data-ttu-id="297a4-129">什么是 SEPA 企业到企业 (B2B) 直接借记方案？</span><span class="sxs-lookup"><span data-stu-id="297a4-129">What is the SEPA Business to Business (B2B) Direct Debit scheme?</span></span>
<span data-ttu-id="297a4-130">SEPA B2B 直接借记方案应用于企业到企业的交易记录以及在 SEPA 核心直接借记方案上设置。</span><span class="sxs-lookup"><span data-stu-id="297a4-130">The SEPA B2B Direct Debit Scheme applies to business-to-business transactions and builds on the SEPA Core Direct Debit Scheme.</span></span> <span data-ttu-id="297a4-131">主要差异在于：</span><span class="sxs-lookup"><span data-stu-id="297a4-131">The main differences are:</span></span>
-   <span data-ttu-id="297a4-132">在客户为私人个体（消费者）时，不允许 SEPA B2B 直接借记方案。</span><span class="sxs-lookup"><span data-stu-id="297a4-132">The SEPA B2B Direct Debit Scheme is not allowed when the customer is a private individual (consumer).</span></span>
-   <span data-ttu-id="297a4-133">该客户没有资格获取已授权交易记录的退款。</span><span class="sxs-lookup"><span data-stu-id="297a4-133">The customer is not entitled to obtain a refund of an authorized transaction.</span></span>
-   <span data-ttu-id="297a4-134">客户银行必须根据授权信息对收款进行验证，以确保该收款为授权的。</span><span class="sxs-lookup"><span data-stu-id="297a4-134">Customer banks must make sure that that the collection is authorized, by verifying the collection against mandate information.</span></span> <span data-ttu-id="297a4-135">客户银行和客户必须同意针对每个直接借记执行验证。</span><span class="sxs-lookup"><span data-stu-id="297a4-135">Customer banks and customers are required to agree on the verification that will be performed for each direct debit.</span></span>
-   <span data-ttu-id="297a4-136">该方案提供较短的时间线用于呈现直接借记及缩短返还周期。</span><span class="sxs-lookup"><span data-stu-id="297a4-136">The scheme offers a shorter timeline for presenting direct debits and reduces the return period.</span></span>

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a><span data-ttu-id="297a4-137">我能将 COR1 方案用于直接借记授权单吗？</span><span class="sxs-lookup"><span data-stu-id="297a4-137">Can I use the COR1 scheme for direct debit mandates?</span></span>
<span data-ttu-id="297a4-138">是。</span><span class="sxs-lookup"><span data-stu-id="297a4-138">Yes.</span></span> <span data-ttu-id="297a4-139">您可以在奥地利、比利时、德国、法国、意大利、西班牙和荷兰对 SEPA 直接借记授权单使用 COR1 方案。</span><span class="sxs-lookup"><span data-stu-id="297a4-139">You can use the COR1 scheme for SEPA direct debit mandates in Austria, Belgium, Germany, France, Italy, Spain, and the Netherlands.</span></span> <span data-ttu-id="297a4-140">该方案提供针对直接借记收款为债权人提供短时提前通知。</span><span class="sxs-lookup"><span data-stu-id="297a4-140">The scheme provides a shorter pre-notification period for the direct debit collection for the creditor.</span></span>

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a><span data-ttu-id="297a4-141">什么是国际银行帐号 (IBAN) 和银行标识符代码 (BIC)?</span><span class="sxs-lookup"><span data-stu-id="297a4-141">What are International Bank Account Numbers (IBAN) and Bank Identifier Codes (BIC)?</span></span>
<span data-ttu-id="297a4-142">国际银行帐号 (IBAN) 和银行标识符代码 (BIC) 用于标识在 32 个 SEPA 国家/地区的任何帐户。</span><span class="sxs-lookup"><span data-stu-id="297a4-142">The International Bank Account Number (IBAN) and Bank Identifier Code (BIC) are used to identify any account in the 32 SEPA countries/regions.</span></span> <span data-ttu-id="297a4-143">在“SWIFT 代码”字段中输入 BIC，在“IBAN”字段中输入 IBAN。</span><span class="sxs-lookup"><span data-stu-id="297a4-143">Enter the BIC in the SWIFT code field and the IBAN in the IBAN field.</span></span> <span data-ttu-id="297a4-144">这两个字段位于“银行帐户”页中的“银行帐户”选项卡上的“附加标识”快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="297a4-144">Both fields are located on the Additional identification FastTab on the Bank account tab in the Bank accounts page.</span></span> <span data-ttu-id="297a4-145">这对于债权人的银行帐户和客户的银行帐户皆适用。</span><span class="sxs-lookup"><span data-stu-id="297a4-145">This is true for both the creditor’s bank account and the customer’s bank account.</span></span>

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a><span data-ttu-id="297a4-146">我在何处输入债权人标识符（直接借记 ID）?</span><span class="sxs-lookup"><span data-stu-id="297a4-146">Where do I enter creditor identifiers (Direct debit IDs)?</span></span>
<span data-ttu-id="297a4-147">在 SEPA 中，每个债权人由唯一的标识符确定债权人。</span><span class="sxs-lookup"><span data-stu-id="297a4-147">In the SEPA, each creditor is identified by a unique creditor identifier.</span></span> <span data-ttu-id="297a4-148">此标识符允许客户和客户银行筛选每个直接借记，然后根据客户说明处理或拒绝该直接借记。</span><span class="sxs-lookup"><span data-stu-id="297a4-148">This identifier lets the customer and the customer bank filter each direct debit, and then process or reject the direct debit according to customer instructions.</span></span> <span data-ttu-id="297a4-149">债权人必须通过其银行申请此标识符。</span><span class="sxs-lookup"><span data-stu-id="297a4-149">Creditors must request this identifier through their bank.</span></span> <span data-ttu-id="297a4-150">在“直接借记 ID”中针对法人的银行帐户输入此标识符。</span><span class="sxs-lookup"><span data-stu-id="297a4-150">Enter this identifier in the Direct debit ID field for the bank account for the legal entity.</span></span>

## <a name="what-are-mandates"></a><span data-ttu-id="297a4-151">什么是授权？</span><span class="sxs-lookup"><span data-stu-id="297a4-151">What are mandates?</span></span>
<span data-ttu-id="297a4-152">客户签署授权允许债权人收取付款并指示客户的银行支付该收款。</span><span class="sxs-lookup"><span data-stu-id="297a4-152">The customer signs a mandate that authorizes the creditor to collect a payment and instructs the customer’s bank to pay the collection.</span></span> <span data-ttu-id="297a4-153">客户可以以纸质或电子形式签发授权。</span><span class="sxs-lookup"><span data-stu-id="297a4-153">The customer can issue the mandate in paper form or electronically.</span></span> <span data-ttu-id="297a4-154">默认情况下，在最后启动直接借记的 36 个月之后该授权到期。</span><span class="sxs-lookup"><span data-stu-id="297a4-154">By default, the mandate expires 36 months after the direct debit is last initiated.</span></span>

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a><span data-ttu-id="297a4-155">我在何处指定 SEPA 直接借记文件格式 (ISO 20022)?</span><span class="sxs-lookup"><span data-stu-id="297a4-155">Where do I specify the SEPA Direct Debit file format (ISO 20022)?</span></span>
<span data-ttu-id="297a4-156">SEPA 数据格式基于 ISO 20022 消息标准。</span><span class="sxs-lookup"><span data-stu-id="297a4-156">The SEPA data formats are based on the ISO 20022 message standards.</span></span> <span data-ttu-id="297a4-157">当您配置应收帐款的付款方式时，您将选中“一般电子申报”复选框并选择 SEPA 直接借记格式作为导出格式配置。</span><span class="sxs-lookup"><span data-stu-id="297a4-157">You will check the Generic electronic reporting checkbox and select the SEPA Direct debit format as an export format configuration when you configure accounts receivable methods of payment.</span></span> <span data-ttu-id="297a4-158">当您在客户付款日记帐中生成一个付款文件时，您使用该付款方式。</span><span class="sxs-lookup"><span data-stu-id="297a4-158">You use that method of payment when you generate a payment file in a customer payment journal.</span></span>

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a><span data-ttu-id="297a4-159">我可以生成哪种格式的 SEPA 直接借记付款文件？</span><span class="sxs-lookup"><span data-stu-id="297a4-159">In what file formats can I generate SEPA direct debit payment files?</span></span>
<span data-ttu-id="297a4-160">可以按照以下格式为 SEPA 直接借记生成电子付款文件：</span><span class="sxs-lookup"><span data-stu-id="297a4-160">You can generate electronic payment files for SEPA direct debits in the following formats:</span></span>
-   <span data-ttu-id="297a4-161">针对比利时、德国、西班牙、法国、意大利和荷兰按 ISO 20022 PAIN.008.001.02 XML 文件格式生成 SEPA 直接借记付款文件。</span><span class="sxs-lookup"><span data-stu-id="297a4-161">SEPA direct debit payment files in the PAIN.008.001.02 XML file format for Belgium, Germany, Spain, France, Italy, and the Netherlands.</span></span>
-   <span data-ttu-id="297a4-162">针对奥地利按 PAIN.008.001.02 XML 文件格式生成 SEPA 直接借记付款文件，针对德国按照 PAIN.008.003.02 XML 文件格式生成 SEPA 直接借记付款文件。</span><span class="sxs-lookup"><span data-stu-id="297a4-162">SEPA direct debit payment files in the PAIN.008.001.02 XML file format for Austria, and in the PAIN.008.003.02 XML file format for Germany.</span></span>

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a><span data-ttu-id="297a4-163">如何使用 SEPA 直接借记退款和还款？</span><span class="sxs-lookup"><span data-stu-id="297a4-163">How do refunds and returns work with SEPA direct debits?</span></span>
<span data-ttu-id="297a4-164">在两个 SEPA 直接借记方案中，客户具有某些退款权限。</span><span class="sxs-lookup"><span data-stu-id="297a4-164">Under both SEPA Direct Debit schemes, customers have certain rights to refunds.</span></span> <span data-ttu-id="297a4-165">在到期日期后的八周内，允许客户撤消任何已授权的交易记录，而不必说明原因。</span><span class="sxs-lookup"><span data-stu-id="297a4-165">The customer is allowed to recall any authorized transactions during an eight-week period after the due date, without having to give a reason.</span></span> <span data-ttu-id="297a4-166">在未授权的交易记录情况下，该时间延长至到期日期的 13 个月之后。</span><span class="sxs-lookup"><span data-stu-id="297a4-166">In the case of unauthorized transactions, the period is extended to 13 months after the due date.</span></span> <span data-ttu-id="297a4-167">通过使用“客户交易记录”页中的“取消付款”按钮手动完成撤消任何已执行的付款。</span><span class="sxs-lookup"><span data-stu-id="297a4-167">Reversals of any payments that have been made are accomplished manually by using the Cancel payment button in the Customer transactions page.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]