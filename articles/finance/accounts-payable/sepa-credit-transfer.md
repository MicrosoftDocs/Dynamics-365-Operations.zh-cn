---
title: SEPA 贷方转帐概览
description: 此主题提供有关 ISO 20022 贷方转帐（包括单一欧元支付区 (SEPA) 贷方转帐和针对供应商的其他任何电子付款）的一般信息。 SEPA 贷方转帐是从一个公司或个人到另一个公司或个人的一种特定类型的付款（用欧元）。 本主题还讨论如何设置和传输贷方转帐付款文件。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bddfc706f85192f112f08e172934c7ff66faf35d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979480"
---
# <a name="sepa-credit-transfer-overview"></a><span data-ttu-id="2ef53-105">SEPA 贷方转帐概览</span><span class="sxs-lookup"><span data-stu-id="2ef53-105">SEPA credit transfer overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ef53-106">此主题提供有关 ISO 20022 贷方转帐（包括单一欧元支付区 (SEPA) 贷方转帐和针对供应商的其他任何电子付款）的一般信息。</span><span class="sxs-lookup"><span data-stu-id="2ef53-106">This article provides general information about ISO 20022 credit transfers, which include Single Euro Payments Area (SEPA) credit transfers and any other electronic payments for vendors.</span></span> <span data-ttu-id="2ef53-107">SEPA 贷方转帐是从一个公司或个人到另一个公司或个人的一种特定类型的付款（用欧元）。</span><span class="sxs-lookup"><span data-stu-id="2ef53-107">A SEPA credit transfer is a specific type of payment in euros from one company or individual to another company or individual.</span></span> <span data-ttu-id="2ef53-108">本主题还讨论如何设置和传输贷方转帐付款文件。</span><span class="sxs-lookup"><span data-stu-id="2ef53-108">The topic also explains how to set up and transmit a credit transfer payment file.</span></span>

## <a name="what-is-a-credit-transfer-message"></a><span data-ttu-id="2ef53-109">贷方转帐消息是什么？</span><span class="sxs-lookup"><span data-stu-id="2ef53-109">What is a credit transfer message?</span></span>
<span data-ttu-id="2ef53-110">贷方转帐消息是发起方（您公司）为了将资金从自己的帐户转移到贷方而发出的请求。</span><span class="sxs-lookup"><span data-stu-id="2ef53-110">The credit transfer message is a request that an initiating party (your company) sends to move funds from its own account to a creditor.</span></span> <span data-ttu-id="2ef53-111">贷方转帐消息有大量国家/地区特定和银行特定的实施。</span><span class="sxs-lookup"><span data-stu-id="2ef53-111">There are many country/region-specific and bank-specific implementations of credit transfer messages.</span></span> <span data-ttu-id="2ef53-112">其中一些在一个国家/地区内使用，一些则成为了标准。</span><span class="sxs-lookup"><span data-stu-id="2ef53-112">Some of them are used within one country/region, and some are becoming standards.</span></span> <span data-ttu-id="2ef53-113">一个享有盛誉的全球标准为 ISO 20022 及其初始消息，如“贷方转帐”。</span><span class="sxs-lookup"><span data-stu-id="2ef53-113">One well-established global standard is ISO 20022 and its initiation messages, such as Credit transfer.</span></span> <span data-ttu-id="2ef53-114">下图显示选定贷方转帐消息的关系和范围。</span><span class="sxs-lookup"><span data-stu-id="2ef53-114">The following illustration shows the relations and coverage for selected credit transfer messages.</span></span> 
<span data-ttu-id="2ef53-115">![贷方转帐](./media/credit-transfer.jpg)贷方转帐消息</span><span class="sxs-lookup"><span data-stu-id="2ef53-115">![Credit tansfer](./media/credit-transfer.jpg) Credit transfer messages</span></span> 

## <a name="what-are-iso-20022-and-sepa-payments"></a><span data-ttu-id="2ef53-116">ISO 20022 和 SEPA 付款是什么？</span><span class="sxs-lookup"><span data-stu-id="2ef53-116">What are ISO 20022 and SEPA payments?</span></span>
<span data-ttu-id="2ef53-117">单一欧元支付区 (SEPA) 由欧盟执委会设置，并指示所有电子付款均被视为国内行为，不论个人、企业或者组织和银行所在的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="2ef53-117">The Single Euro Payments Area (SEPA) is set up by the European Commission and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located.</span></span> <span data-ttu-id="2ef53-118">国内付款和跨境付款之间不存在差异。</span><span class="sxs-lookup"><span data-stu-id="2ef53-118">There is no difference between national payments and cross-border payments.</span></span> <span data-ttu-id="2ef53-119">SEPA 包含 28 个欧盟 (EU) 成员国，以及爱尔兰、列支敦斯登、挪威、瑞士、摩纳哥和圣马力诺。</span><span class="sxs-lookup"><span data-stu-id="2ef53-119">The SEPA includes the 28 member states of the European Union (EU), and also Iceland, Liechtenstein, Norway, Switzerland, Monaco, and San Marino.</span></span> <span data-ttu-id="2ef53-120">SEPA 帮助在欧洲经济区域 (EEA) 中形成付款交易记录的单一市场。</span><span class="sxs-lookup"><span data-stu-id="2ef53-120">The SEPA helps form a single market for payment transactions within the European Economic Area (EEA).</span></span> <span data-ttu-id="2ef53-121">最终，SEPA 会减少银行、企业和个人必须使用的支付形式数量。</span><span class="sxs-lookup"><span data-stu-id="2ef53-121">Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.</span></span> <span data-ttu-id="2ef53-122">欧盟执委会通过付款服务规定 (PSD) 建立 SEPA 付款的法律基础。</span><span class="sxs-lookup"><span data-stu-id="2ef53-122">The European Commission established the legal foundation for SEPA payments through the Payment Services Directive (PSD).</span></span> <span data-ttu-id="2ef53-123">欧元支付委员会 (EPC) 通过以下活动支持 SEPA:</span><span class="sxs-lookup"><span data-stu-id="2ef53-123">The European Payments Council (EPC) supports the SEPA through the following activities:</span></span>

-   <span data-ttu-id="2ef53-124">它通过使用 ISO 20022 通用财务行业消息模式 XML 格式，规定 SEPA 电子付款的标准。</span><span class="sxs-lookup"><span data-stu-id="2ef53-124">It sets the standards for SEPA electronic payments by using the ISO 20022 Universal financial industry message scheme XML format.</span></span>
-   <span data-ttu-id="2ef53-125">它确定有关处理欧元付款的规则和基准。</span><span class="sxs-lookup"><span data-stu-id="2ef53-125">It establishes rules and guidelines about the handling of euro payments.</span></span>

<span data-ttu-id="2ef53-126">EPC（包括欧洲银行）开发 SEPA 付款设备的商业和技术框架。</span><span class="sxs-lookup"><span data-stu-id="2ef53-126">The EPC, which consists of European banks, develops the commercial and technical frameworks for SEPA payment instruments.</span></span> <span data-ttu-id="2ef53-127">使用三种类型的 SEPA 付款：</span><span class="sxs-lookup"><span data-stu-id="2ef53-127">Three types of SEPA payments are used:</span></span>

-   <span data-ttu-id="2ef53-128">贷方转帐</span><span class="sxs-lookup"><span data-stu-id="2ef53-128">Credit transfers</span></span>
-   <span data-ttu-id="2ef53-129">直接借记</span><span class="sxs-lookup"><span data-stu-id="2ef53-129">Direct debits</span></span>
-   <span data-ttu-id="2ef53-130">卡</span><span class="sxs-lookup"><span data-stu-id="2ef53-130">Cards</span></span>

## <a name="what-is-a-sepa-credit-transfer"></a><span data-ttu-id="2ef53-131">SEPA 贷方转帐是什么？</span><span class="sxs-lookup"><span data-stu-id="2ef53-131">What is a SEPA credit transfer?</span></span>
<span data-ttu-id="2ef53-132">SEPA 贷方转帐是从一个公司或个人付款到另一个公司或个人。</span><span class="sxs-lookup"><span data-stu-id="2ef53-132">A SEPA credit transfer is a payment from one company or individual to another company or individual.</span></span> <span data-ttu-id="2ef53-133">付款必须按欧元，并且必须包括国际银行帐号 (IBAN) 和两个当事方的银行标识符代码 (BIC)。</span><span class="sxs-lookup"><span data-stu-id="2ef53-133">Payments must be in euros, and must include the International Bank Account Number (IBAN) and the Bank Identifier Code (BIC) for both parties.</span></span> <span data-ttu-id="2ef53-134">（BIC 也称为国际银行金融电信协会 \[SWIFT\] 代码。）此外，交易记录必须在两个当事方之间共享。</span><span class="sxs-lookup"><span data-stu-id="2ef53-134">(The BIC is also known as the Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] code.) Additionally, transaction costs must be shared between both parties.</span></span> <span data-ttu-id="2ef53-135">当事方之间的贷方转帐应使用符合 ISO 20022 付款处理标准的 XML 格式和由 EPC 指定的 XML。</span><span class="sxs-lookup"><span data-stu-id="2ef53-135">Credit transfers that occur between parties should use XML files that comply with ISO 20022 payment processing standards and the XML format, as specified by the EPC.</span></span>

## <a name="how-is-a-credit-transfer-implemented"></a><span data-ttu-id="2ef53-136">贷方转帐如何实施？</span><span class="sxs-lookup"><span data-stu-id="2ef53-136">How is a credit transfer implemented?</span></span>
<span data-ttu-id="2ef53-137">欧洲国家/地区的贷方转帐付款格式是使用 Microsoft Dynamics 365 Finance 中的电子申报 (ER) 和付款方式功能来实施的。</span><span class="sxs-lookup"><span data-stu-id="2ef53-137">The credit transfer payment format for European countries is implemented by using the Electronic reporting (ER) and Methods of payment functionality in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="2ef53-138">其他地区使用的一些贷方转帐格式仍在使用传统的付款框架。</span><span class="sxs-lookup"><span data-stu-id="2ef53-138">A few credit transfer formats that are used in other regions still use the legacy payment framework.</span></span> <span data-ttu-id="2ef53-139">在其他许多格式中，有十二种 ISO 20022 贷方转帐文件格式可用。</span><span class="sxs-lookup"><span data-stu-id="2ef53-139">Among many other formats, there are twelve ISO 20022 credit transfer file formats that are available.</span></span> <span data-ttu-id="2ef53-140">这些导出格式符合 SEPA ISO 20022 XML 标准。</span><span class="sxs-lookup"><span data-stu-id="2ef53-140">These export formats conform to the SEPA ISO 20022 XML standard.</span></span> <span data-ttu-id="2ef53-141">它们用于按照 EPC 发布的 SEPA Credit Transfer Scheme Rulebook 8.2 版中的规定，为其使用国/地区和欧元付款生成非欧元付款转帐。</span><span class="sxs-lookup"><span data-stu-id="2ef53-141">They are used to generate non-euro payment transfers for countries/regions where they are used and euro payments as specified in version 8.2 of the SEPA Credit Transfer Scheme Rulebook that the EPC releases.</span></span> <span data-ttu-id="2ef53-142">在您可以实施贷方转帐前，必须与您的银行联系，以获取加载电子银行文件所需的软件。</span><span class="sxs-lookup"><span data-stu-id="2ef53-142">Before you can implement credit transfers, you must contact your bank to obtain the software that is required in order to upload electronic banking files.</span></span> <span data-ttu-id="2ef53-143">您将使用该软件将包含付款订单的 XML 文件转移到您的银行。</span><span class="sxs-lookup"><span data-stu-id="2ef53-143">You will use that software to transfer the XML files that contain payment orders to your bank.</span></span>

## <a name="what-credit-transfer-formats-are-currently-supported"></a><span data-ttu-id="2ef53-144">目前支持哪些贷方转帐格式？</span><span class="sxs-lookup"><span data-stu-id="2ef53-144">What credit transfer formats are currently supported?</span></span>
<span data-ttu-id="2ef53-145">应始终转至 Microsoft Dynamics Lifecycle services (LCS) 中的共享资产库，并查看资产类型为 **GER 配置** 的可用文件的最新列表。</span><span class="sxs-lookup"><span data-stu-id="2ef53-145">You should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="2ef53-146">下一部分“必须执行哪些设置？”提供一个主题的链接，该主题说明如何创建 LCS 存储库以检查可用配置和导入所选配置。</span><span class="sxs-lookup"><span data-stu-id="2ef53-146">The next section, "What do I have to set up?", provides a link to the topic that explains how to create an LCS repository to review available configurations and import selected configurations.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="2ef53-147">我必须设置什么？</span><span class="sxs-lookup"><span data-stu-id="2ef53-147">What do I have to set up?</span></span>
-   <span data-ttu-id="2ef53-148">在您可以创建贷方转帐文件前，必须导入至少一个有效的贷方转帐配置到您的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="2ef53-148">Before you can create credit transfer files, at least one active credit transfer configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="2ef53-149">有关说明，请参阅[从 Lifecycle Services 下载电子申报配置](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。</span><span class="sxs-lookup"><span data-stu-id="2ef53-149">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
-   <span data-ttu-id="2ef53-150">在配置应付帐款付款方式时，请选中 **一般电子申报** 复选框，并选择相应的贷方转帐格式（如 **ISO 20022 贷方转帐 (AT)**）作为导出格式配置。</span><span class="sxs-lookup"><span data-stu-id="2ef53-150">When you configure Accounts payable methods of payment, select the **Generic electronic reporting** check box, and select the appropriate credit transfer format (for example, **ISO 20022 Credit transfer (AT)**) as an export format configuration.</span></span>
-   <span data-ttu-id="2ef53-151">还必须设置法人和银行帐户信息。</span><span class="sxs-lookup"><span data-stu-id="2ef53-151">You must also set up the legal entity and bank account information.</span></span>
-   <span data-ttu-id="2ef53-152">需要银行帐号、IBAN，有时还需要 SWIFT 代码 (BIC) 或其他 ID，才能创建有效的贷方转帐付款。</span><span class="sxs-lookup"><span data-stu-id="2ef53-152">Bank account numbers, IBANs, and sometimes SWIFT codes (BICs) or other IDs are required in order to create valid credit transfer payments.</span></span> <span data-ttu-id="2ef53-153">必须为供应商银行帐户和请求转帐的银行帐户设置这些信息。</span><span class="sxs-lookup"><span data-stu-id="2ef53-153">Therefore, you must set up them for the vendor bank account and the bank account for the organization that is requesting the transfer.</span></span>
-   <span data-ttu-id="2ef53-154">可能需要更多信息，如贷方转帐消息中涉及的各方的增值税 (VAT) 号。</span><span class="sxs-lookup"><span data-stu-id="2ef53-154">Additional information might be required, such as value-added tax (VAT) numbers for the parties that are referred to in the credit transfer message.</span></span> <span data-ttu-id="2ef53-155">如果请求此信息，则必须为供应商和法人设置。</span><span class="sxs-lookup"><span data-stu-id="2ef53-155">This information must be set up for vendors and for the legal entity when it's requested.</span></span>
-   <span data-ttu-id="2ef53-156">某些应付帐款付款方式（大多数为基于 ISO 20022 的付款方式）可能需要为 **付款格式代码集** 执行更多设置，如 **服务类型** = **SLEV**。</span><span class="sxs-lookup"><span data-stu-id="2ef53-156">Some Accounts payable methods of payment, mostly ISO 20022–based methods of payment, might require additional setup for **Payment format code sets**, such as **Service type** = **SLEV**.</span></span> <span data-ttu-id="2ef53-157">这些代码在处理付款期间用作付款交易记录额外的标记。</span><span class="sxs-lookup"><span data-stu-id="2ef53-157">Those codes are used as additional tagging for payment transactions during payment processing.</span></span> <span data-ttu-id="2ef53-158">可在两处设置付款代码的默认值（如 **类别目的**、**费用责任人**、**本地仪器** 和 **服务等级**）。</span><span class="sxs-lookup"><span data-stu-id="2ef53-158">Default values of Payment codes, like **Category purpose**, **Charge bearer**, **Local instrument** and **Service level** can be set in two places.</span></span> <span data-ttu-id="2ef53-159">第一处为 **应付帐款付款日记帐抬头**，第二处为 **应付帐款付款方式**。</span><span class="sxs-lookup"><span data-stu-id="2ef53-159">The first place is **Accounts payable payment journal header** and the second is **Accounts payable methods for payments**.</span></span> <span data-ttu-id="2ef53-160">创建付款日记帐行之后，将把在付款日记帐抬头中设置的付款代码值转移到日记帐行，如果未设置该值，则使用付款方式中的值。</span><span class="sxs-lookup"><span data-stu-id="2ef53-160">Upon payment journal lines creation, Payment code values set on payment journal header are transferred to a journal line, if not set, the values from Methods of payment are used.</span></span>

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a><span data-ttu-id="2ef53-161">哪些参数可用于生成贷方转帐付款？</span><span class="sxs-lookup"><span data-stu-id="2ef53-161">What parameters are available for generating credit transfer payments?</span></span>
<span data-ttu-id="2ef53-162">具体参数列表取决于贷方转帐格式。</span><span class="sxs-lookup"><span data-stu-id="2ef53-162">The list of specific parameters depends on the credit transfer format.</span></span> <span data-ttu-id="2ef53-163">下表显示了在供应商付款日记帐中为德国生成 ISO 20022 贷方转帐付款文件时可以使用的参数。</span><span class="sxs-lookup"><span data-stu-id="2ef53-163">The following table shows the parameters that are available when you generate a ISO 20022 credit transfer payment file for Germany in a vendor payment journal.</span></span> <span data-ttu-id="2ef53-164">通过使用 **在后台运行** 选项卡上的选项，您可以在批处理模式下运行付款生成。</span><span class="sxs-lookup"><span data-stu-id="2ef53-164">By using the options that are available on the **Run in the background** tab, you can run payment generation in batch mode.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ef53-165">字段</span><span class="sxs-lookup"><span data-stu-id="2ef53-165">Field</span></span></th>
<th><span data-ttu-id="2ef53-166">说明</span><span class="sxs-lookup"><span data-stu-id="2ef53-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ef53-167">批预定</span><span class="sxs-lookup"><span data-stu-id="2ef53-167">Batch booking</span></span></td>
<td><span data-ttu-id="2ef53-168">选中此复选框可在 XML 文件中包括批次预订标记。</span><span class="sxs-lookup"><span data-stu-id="2ef53-168">Select this check box to include the batch booking tag in the XML file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ef53-169">处理日期</span><span class="sxs-lookup"><span data-stu-id="2ef53-169">Processing date</span></span></td>
<td><span data-ttu-id="2ef53-170">输入银行应处理付款的日期。</span><span class="sxs-lookup"><span data-stu-id="2ef53-170">Enter the date when the bank should process the payments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ef53-171">格式</span><span class="sxs-lookup"><span data-stu-id="2ef53-171">Format</span></span></td>
<td><span data-ttu-id="2ef53-172">根据您的国家/地区或银行的要求，选择汇款信息的格式：</span><span class="sxs-lookup"><span data-stu-id="2ef53-172">Select the format for remittance information, depending on the requirements of your country/region or bank:</span></span>
<ul>
<li><span data-ttu-id="2ef53-173"><strong>Strd</strong> – 选择此选项可在针对一个发票结算一个付款行时使用已结构化的格式。</span><span class="sxs-lookup"><span data-stu-id="2ef53-173"><strong>Strd</strong> – Select this option to use the structured format when one payment line is settled against one invoice.</span></span> <span data-ttu-id="2ef53-174">此选项不可用于法国、德国或荷兰的特定于国家/地区的导出格式。</span><span class="sxs-lookup"><span data-stu-id="2ef53-174">This option isn&#39;t available for the country/region-specific export formats for France, Germany, or the Netherlands.</span></span></li>
<li><span data-ttu-id="2ef53-175"><strong>Ustrd</strong> – 选择此选项可在针对多个发票结算一个付款时使用未结构化的格式。</span><span class="sxs-lookup"><span data-stu-id="2ef53-175"><strong>Ustrd</strong> – Select this option to use the unstructured format when the payment is settled against multiple invoices.</span></span> <span data-ttu-id="2ef53-176">已结算发票的发票编号连接到一起，并且用作汇款信息。</span><span class="sxs-lookup"><span data-stu-id="2ef53-176">The invoice numbers for the settled invoices are concatenated and used as the remittance information.</span></span> <span data-ttu-id="2ef53-177">根据 ISO 20022 指南，非结构化汇款信息不能超过 140 个字符。</span><span class="sxs-lookup"><span data-stu-id="2ef53-177">In compliance with ISO 20022 guidelines, unstructured remittance information is limited to 140 characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ef53-178">发票数</span><span class="sxs-lookup"><span data-stu-id="2ef53-178">Number of invoices</span></span></td>
<td><span data-ttu-id="2ef53-179">输入<strong>付款通知</strong>报表从中打印的发票数量。</span><span class="sxs-lookup"><span data-stu-id="2ef53-179">Enter the number of invoices that the <strong>Payment advice</strong> report is printed from.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ef53-180">序列号</span><span class="sxs-lookup"><span data-stu-id="2ef53-180">Sequence number</span></span></td>
<td><span data-ttu-id="2ef53-181">输入序列号以标识文件。</span><span class="sxs-lookup"><span data-stu-id="2ef53-181">Enter a sequence number to identify the file.</span></span> <span data-ttu-id="2ef53-182">序列号显示在<strong>出席单</strong>报表上。</span><span class="sxs-lookup"><span data-stu-id="2ef53-182">The sequence number appears on the <strong>Attending note</strong> report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ef53-183">打印出席单</span><span class="sxs-lookup"><span data-stu-id="2ef53-183">Print attending note</span></span></td>
<td><span data-ttu-id="2ef53-184">选中此复选框可打印<strong>出席单</strong>报表。</span><span class="sxs-lookup"><span data-stu-id="2ef53-184">Select this check box to print the <strong>Attending note</strong> report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ef53-185">打印控制报表</span><span class="sxs-lookup"><span data-stu-id="2ef53-185">Print control report</span></span></td>
<td><span data-ttu-id="2ef53-186">选中此复选框可打印包含付款信息的报表。</span><span class="sxs-lookup"><span data-stu-id="2ef53-186">Select this check box to print a report that contains the payment information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ef53-187">打印随函</span><span class="sxs-lookup"><span data-stu-id="2ef53-187">Print covering letter</span></span></td>
<td><span data-ttu-id="2ef53-188">选中此复选框可打印<strong>付款通知</strong>报表。</span><span class="sxs-lookup"><span data-stu-id="2ef53-188">Select this check box to print the <strong>Payment advice</strong> report.</span></span></td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a><span data-ttu-id="2ef53-189">IBAN 和 BIC 是什么？</span><span class="sxs-lookup"><span data-stu-id="2ef53-189">What are IBANs and BICs?</span></span>
<span data-ttu-id="2ef53-190">国际银行帐号 (IBAN) 和银行标识符代码 (BIC) 用于标识在全球大量国家/地区的任何帐户。</span><span class="sxs-lookup"><span data-stu-id="2ef53-190">The International Bank Account Number (IBAN) and Bank Identifier Code (BIC) are used to identify any account in many countries/regions worldwide.</span></span> <span data-ttu-id="2ef53-191">其中包括 34 个 SEPA 国家/地区。</span><span class="sxs-lookup"><span data-stu-id="2ef53-191">These include the 34 SEPA countries/regions.</span></span> <span data-ttu-id="2ef53-192">在 **SWIFT 代码** 字段中输入 BIC，在 **IBAN** 字段中输入 IBAN。</span><span class="sxs-lookup"><span data-stu-id="2ef53-192">Enter the BIC in the **SWIFT code** field and the IBAN in the **IBAN** field.</span></span> <span data-ttu-id="2ef53-193">对于贷方的银行帐户和客户的银行帐户，这些字段位于 **银行帐户** 页上的 **银行帐户** 选项卡的 **附加标识** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="2ef53-193">For both the creditor’s bank account and the customer’s bank account, these fields are located on the **Additional identification** FastTab on the **Bank account** tab of the **Bank accounts** page.</span></span> <span data-ttu-id="2ef53-194">不再将 BIC 用于 SEPA 付款。</span><span class="sxs-lookup"><span data-stu-id="2ef53-194">The use of BIC for SEPA payments is no longer enforced.</span></span>

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a><span data-ttu-id="2ef53-195">如何将付款文件发送到银行？</span><span class="sxs-lookup"><span data-stu-id="2ef53-195">How do I transmit a payment file to the bank?</span></span>
<span data-ttu-id="2ef53-196">在您生成付款时，将生成付款文件，并且，系统会请求您从 Web 浏览器中将其保存到任何可用的位置。</span><span class="sxs-lookup"><span data-stu-id="2ef53-196">When you generate payments, the payment file is generated, and you're asked to save it from your web browser to any available location.</span></span> <span data-ttu-id="2ef53-197">下一步是将该 XML 文件发送到您的银行。</span><span class="sxs-lookup"><span data-stu-id="2ef53-197">The next step is to send the XML file to your bank.</span></span> <span data-ttu-id="2ef53-198">此流程根据银行的不同而变。</span><span class="sxs-lookup"><span data-stu-id="2ef53-198">This process varies from bank to bank.</span></span> <span data-ttu-id="2ef53-199">按照您的银行的说明将文件提交给银行以进行处理。</span><span class="sxs-lookup"><span data-stu-id="2ef53-199">Follow the instructions from your bank to submit the files to the bank for processing.</span></span>



