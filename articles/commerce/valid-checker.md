---
title: 零售交易记录一致性检查器
description: 本主题将介绍 Dynamics 365 Commerce 中的交易记录一致性检查器功能。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3da8bdf6feb932e074680b6cb80e1b7b71f9a82b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004243"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="0d005-103">零售交易记录一致性检查器</span><span class="sxs-lookup"><span data-stu-id="0d005-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="0d005-104">本主题将介绍 Microsoft Dynamics 365 Commerce 中的交易记录一致性检查器功能。</span><span class="sxs-lookup"><span data-stu-id="0d005-104">This topic describes the transaction consistency checker functionality in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="0d005-105">一致性检查器在对账单过账流程选择交易记录之前标识和隔离不一致的交易记录。</span><span class="sxs-lookup"><span data-stu-id="0d005-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="0d005-106">在过账对账单时，过账会由于商业交易记录表中存在不一致的数据而失败。</span><span class="sxs-lookup"><span data-stu-id="0d005-106">When a statement is posted, posting can fail due to inconsistent data in the commerce transaction tables.</span></span> <span data-ttu-id="0d005-107">导致数据问题可能是由于销售点 (POS) 应用程序中不可预料的问题，或者如果从第三方 POS 系统未正确导入交易记录。</span><span class="sxs-lookup"><span data-stu-id="0d005-107">The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="0d005-108">这些不一致可能的显示方式包括：</span><span class="sxs-lookup"><span data-stu-id="0d005-108">Examples of how these inconsistencies may appear include:</span></span> 

- <span data-ttu-id="0d005-109">标题表中的交易记录总计与行中的交易记录总计不匹配。</span><span class="sxs-lookup"><span data-stu-id="0d005-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
- <span data-ttu-id="0d005-110">标题表中的行计数与交易记录表中的行数不匹配。</span><span class="sxs-lookup"><span data-stu-id="0d005-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
- <span data-ttu-id="0d005-111">标题表中的税额与行中的税额不匹配。</span><span class="sxs-lookup"><span data-stu-id="0d005-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 

<span data-ttu-id="0d005-112">当对帐单过帐流程选择不一致的交易记录时，将创建不一致的销售发票和付款日记帐，因此整个对帐单过帐流程将失败。</span><span class="sxs-lookup"><span data-stu-id="0d005-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="0d005-113">从此类状态恢复对账单涉及跨多个交易记录表的复杂数据修复。</span><span class="sxs-lookup"><span data-stu-id="0d005-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="0d005-114">交易记录一致性检查器可预防此类问题。</span><span class="sxs-lookup"><span data-stu-id="0d005-114">The transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="0d005-115">下图描述了使用交易记录一致性检查器的过账流程。</span><span class="sxs-lookup"><span data-stu-id="0d005-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="0d005-116">![使用交易记录一致性检查器的对账单过账流程](./media/validchecker.png "使用零售交易记录一致性检查器的对账单过账流程")</span><span class="sxs-lookup"><span data-stu-id="0d005-116">![Statement posting process with transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="0d005-117">**验证商店交易记录**批处理流程将检查以下方案的商业交易记录表的一致性。</span><span class="sxs-lookup"><span data-stu-id="0d005-117">The **Validate store transactions** batch process checks the consistency of the commerce transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="0d005-118">**客户帐户** - 验证交易记录表中的客户帐户是否存在于 HQ 客户主数据中。</span><span class="sxs-lookup"><span data-stu-id="0d005-118">**Customer account** – Validates that the customer account in the transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="0d005-119">**行计数** - 验证交易记录标题表中获取的行数是否与销售交易记录表中的行数匹配。</span><span class="sxs-lookup"><span data-stu-id="0d005-119">**Line count** – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>
- <span data-ttu-id="0d005-120">**含税价格** - 验证各交易行的**含税价格**参数是否一致。</span><span class="sxs-lookup"><span data-stu-id="0d005-120">**Price includes tax** – Validates that the **Price includes tax** parameter is consistent across transaction lines.</span></span>
- <span data-ttu-id="0d005-121">**付款金额** - 验证付款记录与标题上的付款金额是否匹配。</span><span class="sxs-lookup"><span data-stu-id="0d005-121">**Payment amount** - Validates that the payment records match the payment amount on header.</span></span>
- <span data-ttu-id="0d005-122">**总额** - 验证标题上的总额是否为行上的净额与纳税金额之和。</span><span class="sxs-lookup"><span data-stu-id="0d005-122">**Gross amount** – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</span></span>
- <span data-ttu-id="0d005-123">**净额** - 验证标题上的净额是行上的净额之和。</span><span class="sxs-lookup"><span data-stu-id="0d005-123">**Net amount** – Validates that the net amount on the header is the sum of the net amounts on the lines.</span></span>
- <span data-ttu-id="0d005-124">**未足额支付/超额支付** - 验证标题上的总额与付款金额之间的差别未超过最大未足额支付/超额支付配置。</span><span class="sxs-lookup"><span data-stu-id="0d005-124">**Under / Over payment** – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</span></span>
- <span data-ttu-id="0d005-125">**折扣金额** - 验证折扣表上的折扣金额与交易记录行表上的折扣金额一致，并且标题上的折扣金额是行上折扣金额之和。</span><span class="sxs-lookup"><span data-stu-id="0d005-125">**Discount amount** – Validates that the discount amount on the discount tables and the discount amount on the transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</span></span>
- <span data-ttu-id="0d005-126">**行折扣** - 验证交易记录行上的行折扣是与交易记录行对应的折扣表中所有行之和。</span><span class="sxs-lookup"><span data-stu-id="0d005-126">**Line discount** – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</span></span>
- <span data-ttu-id="0d005-127">**礼品卡物料** - Commerce 不支持礼品卡物料退货。</span><span class="sxs-lookup"><span data-stu-id="0d005-127">**Gift card item** – Commerce doesn't support the return of gift card items.</span></span> <span data-ttu-id="0d005-128">但是，礼品卡的余额可以兑现。作为退货行而不是兑现行处理的任何礼品卡物料会导致对账单过账流程失败。</span><span class="sxs-lookup"><span data-stu-id="0d005-128">However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</span></span> <span data-ttu-id="0d005-129">礼品卡物料的验证流程有助于确保交易记录表上的唯一退货礼品卡行物料是礼品卡兑现行。</span><span class="sxs-lookup"><span data-stu-id="0d005-129">The validation process for gift card items helps guarantee that the only return gift card line items on the transaction tables are gift card cash-out lines.</span></span>
- <span data-ttu-id="0d005-130">**负价格** - 验证没有负价格交易记录行。</span><span class="sxs-lookup"><span data-stu-id="0d005-130">**Negative price** – Validates that there are no negative price transaction lines.</span></span>
- <span data-ttu-id="0d005-131">**物料和变型** - 验证交易记录行上的物料和变型是否存在于物料和变型主文件中。</span><span class="sxs-lookup"><span data-stu-id="0d005-131">**Item & Variant** – Validates that items and variants on the transaction lines exist in the item and variant master file.</span></span>
- <span data-ttu-id="0d005-132">**纳税金额** - 验证纳税记录与行上的纳税金额是否匹配。</span><span class="sxs-lookup"><span data-stu-id="0d005-132">**Tax amount** - Validates that tax records match the tax amounts on the lines.</span></span>
- <span data-ttu-id="0d005-133">**序列号** - 验证该序列号是否存在于通过该序列号控制的物料的交易记录行中。</span><span class="sxs-lookup"><span data-stu-id="0d005-133">**Serial number** - Validates that the serial number is present in the transaction lines for items that are controlled by serial number.</span></span>
- <span data-ttu-id="0d005-134">**符号** - 验证数量上的符号和净额是否在所有交易记录行中相同。</span><span class="sxs-lookup"><span data-stu-id="0d005-134">**Sign** - Validates that the sign on the quantity and the net amount are the same in all the transaction lines.</span></span>
- <span data-ttu-id="0d005-135">**业务日期** - 验证交易记录的所有业务日期的财务期间是否为未结。</span><span class="sxs-lookup"><span data-stu-id="0d005-135">**Business date** - Validates that the financial periods for all the business dates for the transactions are open.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="0d005-136">设置一致性检查器</span><span class="sxs-lookup"><span data-stu-id="0d005-136">Set up the consistency checker</span></span>

<span data-ttu-id="0d005-137">通过 **Retail 和 Commerce \> Retail 和 Commerce IT \> POS 过账**配置定期运行的“验证商店交易记录”批处理。</span><span class="sxs-lookup"><span data-stu-id="0d005-137">Configure the "Validate store transactions" batch process, at **Retail and Commerce \> Retail and Commerce IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="0d005-138">批处理作业可以基于商店组织层次结构进行计划，这与设置“批量计算对账单”和“批量过账对账单”流程的方式相似。</span><span class="sxs-lookup"><span data-stu-id="0d005-138">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="0d005-139">我们建议您将此批处理流程配置为一天运行多次并对此进行计划，以便该批处理在每次执行 P 作业结束后运行。</span><span class="sxs-lookup"><span data-stu-id="0d005-139">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="0d005-140">验证流程的结果</span><span class="sxs-lookup"><span data-stu-id="0d005-140">Results of validation process</span></span>

<span data-ttu-id="0d005-141">相应交易记录中标记了批处理流程执行的验证检查的结果。</span><span class="sxs-lookup"><span data-stu-id="0d005-141">The results of the validation check by the batch process are tagged on the appropriate transaction.</span></span> <span data-ttu-id="0d005-142">交易记录中的**验证状态**字段设置为**成功**或**错误**，并且上次运行验证的日期显示在**上次验证时间**字段中。</span><span class="sxs-lookup"><span data-stu-id="0d005-142">The **Validation status** field on the transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="0d005-143">要查看更多与验证失败相关的描述性错误文本，请选择相关的商店交易记录，然后单击**验证错误**按钮。</span><span class="sxs-lookup"><span data-stu-id="0d005-143">To view more descriptive error text relating to a validation failure, select the relevant store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="0d005-144">未通过验证检查的交易和尚未验证的交易将不会导入对帐单中。</span><span class="sxs-lookup"><span data-stu-id="0d005-144">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="0d005-145">在“计算报表”流程期间，如果存在本可以包括在对帐单中，但却未包括的交易，将会通知用户。</span><span class="sxs-lookup"><span data-stu-id="0d005-145">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="0d005-146">如果发现验证错误，则修复错误的唯一方式是与 Microsoft 支持联系。</span><span class="sxs-lookup"><span data-stu-id="0d005-146">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="0d005-147">在将来的版本中，将会增加相应功能，以便用户可以通过用户界面修复失败的记录。</span><span class="sxs-lookup"><span data-stu-id="0d005-147">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="0d005-148">此外，还将提供记录和审计功能，以跟踪修改历史记录。</span><span class="sxs-lookup"><span data-stu-id="0d005-148">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="0d005-149">未来的版本中将增加支持多种方案的其他验证规则。</span><span class="sxs-lookup"><span data-stu-id="0d005-149">Additional validation rules to support more scenarios will be added in a future release.</span></span>