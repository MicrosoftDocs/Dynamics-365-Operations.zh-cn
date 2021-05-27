---
title: 客户预付款
description: 本主题说明如何设置和处理客户预付款（也称为客户保证金）。
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019412"
---
# <a name="customer-prepayments"></a><span data-ttu-id="25385-103">客户预付款</span><span class="sxs-lookup"><span data-stu-id="25385-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25385-104">当您从客户处收到付款时，将使用客户预付款，但是没有可以据其结算付款的发票。</span><span class="sxs-lookup"><span data-stu-id="25385-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="25385-105">这些付款类型也称为客户保证金。</span><span class="sxs-lookup"><span data-stu-id="25385-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="25385-106">设置和使用客户预付款的流程包括以下基本步骤。</span><span class="sxs-lookup"><span data-stu-id="25385-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="25385-107">为预付款创建客户过帐模板。</span><span class="sxs-lookup"><span data-stu-id="25385-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="25385-108">设置 **具有预付款日记帐凭证的过帐模板** 参数。</span><span class="sxs-lookup"><span data-stu-id="25385-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="25385-109">创建客户付款日记帐，然后选中每一行上的 **预付款日记帐凭证** 复选框。</span><span class="sxs-lookup"><span data-stu-id="25385-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="25385-110">过帐客户付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="25385-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="25385-111">生成发票后，使用 **结算未结交易** 页通过发票结算预付款。</span><span class="sxs-lookup"><span data-stu-id="25385-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="25385-112">为预付款创建客户过帐模板</span><span class="sxs-lookup"><span data-stu-id="25385-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="25385-113">通常，当您在货物或服务交付之前或在系统中存在发票之前接受客户的预付款或保证金时，您需要在会计科目表中将现金记录为负债而不是资产。</span><span class="sxs-lookup"><span data-stu-id="25385-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="25385-114">但是，根据您所在的国家或地区，将这些金额记录在总帐中的要求可能会有所不同。</span><span class="sxs-lookup"><span data-stu-id="25385-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="25385-115">因此，请务必咨询您的会计师，了解所有适用的本地法规。</span><span class="sxs-lookup"><span data-stu-id="25385-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="25385-116">一般而言，创建可用于预付款的过帐模板的流程与创建其他过帐模板的流程相同。</span><span class="sxs-lookup"><span data-stu-id="25385-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="25385-117">主要区别在于您在 **汇总科目** 字段中选择的主科目。</span><span class="sxs-lookup"><span data-stu-id="25385-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="25385-118">有关详细信息，请参阅[客户过帐模板](customer-posting-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="25385-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="25385-119">定义客户预付款的参数</span><span class="sxs-lookup"><span data-stu-id="25385-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="25385-120">在配置客户预付系统时，必须考虑两个主要的应收帐款参数。</span><span class="sxs-lookup"><span data-stu-id="25385-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="25385-121">请按照以下步骤配置这些参数。</span><span class="sxs-lookup"><span data-stu-id="25385-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="25385-122">转至 **应收帐款 \> 设置 \> 应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="25385-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="25385-123">可选：在 **分类帐和销售税** 选项卡上的 **付款** 快速选项卡上，将 **预付款日记帐凭证含销售税** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="25385-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="25385-124">在 **具有预付款日记帐凭证的过帐模板** 字段中，选择过帐客户预付款时要使用的客户过帐模板。</span><span class="sxs-lookup"><span data-stu-id="25385-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="25385-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="25385-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="25385-126">创建客户预付款凭证</span><span class="sxs-lookup"><span data-stu-id="25385-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="25385-127">创建客户付款日记帐时，对于每笔预付款，必须在 **客户付款日记帐** 页上将 **预付款日记帐凭证** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="25385-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="25385-128">按照以下步骤创建客户预付款。</span><span class="sxs-lookup"><span data-stu-id="25385-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="25385-129">转到 **应收帐款 \> 付款 \> 客户付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="25385-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="25385-130">选择 **新建** 创建日记帐。</span><span class="sxs-lookup"><span data-stu-id="25385-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="25385-131">在 **名称** 字段中，选择要使用的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="25385-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="25385-132">如果您在上一过程中将 **预付款日记帐凭证含销售税** 选项设置为 **是**，则必须选择选择了 **金额包括销售税** 参数的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="25385-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="25385-133">可选：在 **描述** 字段中，输入详细描述。</span><span class="sxs-lookup"><span data-stu-id="25385-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="25385-134">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="25385-134">Select **Lines**.</span></span>
6. <span data-ttu-id="25385-135">如果不存在空白行，选择 **新建** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="25385-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="25385-136">在 **日期** 字段中，输入应过帐预付款的日期。</span><span class="sxs-lookup"><span data-stu-id="25385-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="25385-137">在 **客户** 字段中，选择下一个预付款的客户。</span><span class="sxs-lookup"><span data-stu-id="25385-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="25385-138">可选：在 **描述** 字段中，输入交易的详细描述。</span><span class="sxs-lookup"><span data-stu-id="25385-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="25385-139">在 **信用** 字段中，输入预付款的金额。</span><span class="sxs-lookup"><span data-stu-id="25385-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="25385-140">在 **抵销帐户** 字段中，选择要抵销付款的帐户。</span><span class="sxs-lookup"><span data-stu-id="25385-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="25385-141">例如，选择要向其过帐付款的银行或主帐户。</span><span class="sxs-lookup"><span data-stu-id="25385-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="25385-142">在 **付款方式** 字段中，选择客户的付款方式。</span><span class="sxs-lookup"><span data-stu-id="25385-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="25385-143">在 **付款** 选项卡上，将 **预付款日记帐凭证** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="25385-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="25385-144">对必须过帐的每个其他预付款重复步骤 7 到 13。</span><span class="sxs-lookup"><span data-stu-id="25385-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="25385-145">选择 **过帐** 完成日记帐。</span><span class="sxs-lookup"><span data-stu-id="25385-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="25385-146">使用发票结算预付款</span><span class="sxs-lookup"><span data-stu-id="25385-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="25385-147">您可以使用 **客户付款** 工作区轻松找到和结算尚未完全结算的付款。</span><span class="sxs-lookup"><span data-stu-id="25385-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="25385-148">在 **主页** 仪表板上，选择 **客户付款** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="25385-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="25385-149">在 **客户交易** 部分的 **未结算付款** 选项卡上，搜索并选择要结算的付款。</span><span class="sxs-lookup"><span data-stu-id="25385-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="25385-150">选择 **结算交易**。</span><span class="sxs-lookup"><span data-stu-id="25385-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="25385-151">选中发票和将要结算的付款的 **标记** 复选框。</span><span class="sxs-lookup"><span data-stu-id="25385-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="25385-152">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="25385-152">Select **Post**.</span></span>

<span data-ttu-id="25385-153">有关如何结算未结交易的详细信息，请参阅[结算概述](/cash-bank-management/settlement-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="25385-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
