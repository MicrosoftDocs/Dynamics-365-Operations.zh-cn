---
title: "高级银行对帐概览"
description: "高级银行对帐允许您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中导入电子银行对帐单，并与银行交易记录自动对帐。  这篇文章将介绍对帐流程设置。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 95ec4ff5479ccb16c4efc5a284f3fc6a8a943108
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="18ce7-104">高级银行对帐概览</span><span class="sxs-lookup"><span data-stu-id="18ce7-104">Advanced bank reconciliation overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="18ce7-105">高级银行对帐允许您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中导入电子银行对帐单，并与银行交易记录自动对帐。</span><span class="sxs-lookup"><span data-stu-id="18ce7-105">Advanced bank reconciliation allows you to import electronic bank statements and automatically reconcile with bank transactions in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>  <span data-ttu-id="18ce7-106">这篇文章将介绍对帐流程设置。</span><span class="sxs-lookup"><span data-stu-id="18ce7-106">This article will explain the set up processes for reconciliation.</span></span>  

<span data-ttu-id="18ce7-107">在使用高级银行对帐功能之前有很多必须设置的部分。</span><span class="sxs-lookup"><span data-stu-id="18ce7-107">There are a number of pieces that must be set up before using the advanced bank reconciliation functionality.</span></span> <span data-ttu-id="18ce7-108">有关设置银行对帐单导入的详细信息，请参阅[设置银行对帐单导入流程](set-up-advanced-bank-reconciliation-import-process.md)。</span><span class="sxs-lookup"><span data-stu-id="18ce7-108">For more information about setting up bank statement import, see [Set up the bank statement import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>  <span data-ttu-id="18ce7-109">下面详细描述了对帐流程设置的要求。</span><span class="sxs-lookup"><span data-stu-id="18ce7-109">Requirements for set up of the reconciliation process are detailed below.</span></span>

## <a name="transaction-codes"></a><span data-ttu-id="18ce7-110">交易记录代码</span><span class="sxs-lookup"><span data-stu-id="18ce7-110">Transaction codes</span></span>
<span data-ttu-id="18ce7-111">可将交易记录代码用作银行对帐匹配规则的一部分。</span><span class="sxs-lookup"><span data-stu-id="18ce7-111">Transaction codes can be used as part of the bank reconciliation matching rules.</span></span>  <span data-ttu-id="18ce7-112">交易记录代码有助于仅匹配 Finance and Operations 与您的银行对帐单之间类型相同的交易记录。</span><span class="sxs-lookup"><span data-stu-id="18ce7-112">Transaction codes will help to match only the same types of transactions between Finance and Operations and your bank statement.</span></span>  <span data-ttu-id="18ce7-113">要执行此类型的匹配，必须首先从 Finance and Operations 定义用于银行交易记录的交易记录类型，然后将这些类型映射到您的银行使用的对帐单交易记录代码。</span><span class="sxs-lookup"><span data-stu-id="18ce7-113">In order to do this type of matching, you must first define transaction types used for bank transactions from Finance and Operations, then map those types to statement transaction codes used by your bank.</span></span>  <span data-ttu-id="18ce7-114">Finance and Operations 银行交易记录的交易记录类型在**银行交易记录类型**页面中定义。</span><span class="sxs-lookup"><span data-stu-id="18ce7-114">Transaction types for Finance and Operations bank transactions are defined on the **Bank transaction type** page.</span></span>  <span data-ttu-id="18ce7-115">这也是定义要用于与该交易记录类型关联的过帐的主科目。</span><span class="sxs-lookup"><span data-stu-id="18ce7-115">This is also where you define the main account to be used for postings associated with that transaction type.</span></span> 

<span data-ttu-id="18ce7-116">定义 Finance and Operations 银行交易记录代码之后，请将其映射到您的电子银行对帐单中使用的交易记录代码。</span><span class="sxs-lookup"><span data-stu-id="18ce7-116">Once your Finance and Operations bank transaction codes are defined, you then map those to the transaction codes used in your electronic bank statements.</span></span>  <span data-ttu-id="18ce7-117">此映射流程使用**交易记录代码映射**页面执行。</span><span class="sxs-lookup"><span data-stu-id="18ce7-117">This mapping process is done using the **Transaction code mapping** page.</span></span>  <span data-ttu-id="18ce7-118">将为各银行帐户分别完成交易记录代码映射。</span><span class="sxs-lookup"><span data-stu-id="18ce7-118">Transaction code mapping is completed separately for each bank account.</span></span>

## <a name="matching-rules-and-matching-rule-sets"></a><span data-ttu-id="18ce7-119">匹配规则和匹配规则集</span><span class="sxs-lookup"><span data-stu-id="18ce7-119">Matching rules and matching rule sets</span></span>
<span data-ttu-id="18ce7-120">匹配规则允许您定义 Finance and Operations 银行交易记录和银行对帐单交易记录之间的自动对帐条件。</span><span class="sxs-lookup"><span data-stu-id="18ce7-120">Matching rules allow you to define criteria for automatic reconciliation between Finance and Operations bank transactions and bank statement transactions.</span></span>  <span data-ttu-id="18ce7-121">匹配规则的设置在**对帐匹配规则**页面执行。</span><span class="sxs-lookup"><span data-stu-id="18ce7-121">Set up of matching rules is done on **Reconciliation matching rules** page.</span></span>  <span data-ttu-id="18ce7-122">有关详细信息，请参阅[设置银行对帐匹配规则](set-up-bank-reconciliation-matching-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="18ce7-122">For more information, see [Set up bank reconciliation matching rules](set-up-bank-reconciliation-matching-rules.md).</span></span> 

<span data-ttu-id="18ce7-123">匹配规则集用于定义在银行对帐流程中按顺序运行的一组匹配规则。</span><span class="sxs-lookup"><span data-stu-id="18ce7-123">Matching rule sets are used to define a group of matching rules that are run in sequence during the bank reconciliation process.</span></span>  <span data-ttu-id="18ce7-124">匹配规则集在**对帐匹配规则集**页面配置。</span><span class="sxs-lookup"><span data-stu-id="18ce7-124">Matching rule sets are configured on the **Reconciliation matching rule sets** page.</span></span>

## <a name="cash-and-bank-management-parameters"></a><span data-ttu-id="18ce7-125">现金和银行管理参数</span><span class="sxs-lookup"><span data-stu-id="18ce7-125">Cash and bank management parameters</span></span>
<span data-ttu-id="18ce7-126">在**现金和银行管理参数**页有很多特定于高级银行对帐流程的参数。</span><span class="sxs-lookup"><span data-stu-id="18ce7-126">There are a number of parameters specific to the advanced bank reconciliation process on the **Cash and bank management parameters** page.</span></span>  <span data-ttu-id="18ce7-127">**显示借方/贷方对帐单行金额**更改**银行对帐单**页上金额的视图。</span><span class="sxs-lookup"><span data-stu-id="18ce7-127">The **Show statement line amount in debit/credit** changes the view of amounts on the **Bank statement** page.</span></span>  <span data-ttu-id="18ce7-128">如果选择此选项，将在单独的借方和贷方列显示银行对帐单交易记录金额。</span><span class="sxs-lookup"><span data-stu-id="18ce7-128">If this option is selected, the bank statement transaction amounts will be shown in separate debit and credit columns.</span></span>  <span data-ttu-id="18ce7-129">如果未选中，银行对帐单交易记录金额将显示在具有适当符号的单个金额列。</span><span class="sxs-lookup"><span data-stu-id="18ce7-129">If not selected, the bank statement transaction amounts will be shown in a single amount column with the appropriate sign.</span></span> 

<span data-ttu-id="18ce7-130">在参数页上设置的验证选项覆盖匹配规则中设置的选择。</span><span class="sxs-lookup"><span data-stu-id="18ce7-130">The validation options set on the parameters page override the selections set on matching rules.</span></span>  <span data-ttu-id="18ce7-131">例如，您不能手动或自动匹配在参数页上设置的日期差异以外的单据。</span><span class="sxs-lookup"><span data-stu-id="18ce7-131">For example, you cannot manually or automatically match documents beyond the date difference set on the parameters page.</span></span>  <span data-ttu-id="18ce7-132">而且，如果选择**验证交易记录类型映射**，必须在 Finance and Operations 银行交易记录和银行对帐单交易记录之间映射交易记录类型，以手动或自动匹配交易记录。</span><span class="sxs-lookup"><span data-stu-id="18ce7-132">Also, if the option to **Validate transaction type mapping** is selected, the transaction types must be mapped between the Finance and Operations bank transaction and bank statement transaction in order for the transactions to be manually or automatically matched.</span></span> 

<span data-ttu-id="18ce7-133">您还必须配置在**现金和银行管理参数**页配置必要的编号规则。</span><span class="sxs-lookup"><span data-stu-id="18ce7-133">You also must configure the necessary number sequences on the **Cash and bank management parameters** page.</span></span>  <span data-ttu-id="18ce7-134">在**编号规则**选项卡上，为下载 **ID、报表 ID、对帐 ID 和银行对帐**引用设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="18ce7-134">On the **Number sequences** tab, set number sequence codes for the Download **ID, Statement ID, Reconcile ID, and Bank reconciliation** references.</span></span>

## <a name="bank-account-reconciliation-options"></a><span data-ttu-id="18ce7-135">银行帐户对帐选项</span><span class="sxs-lookup"><span data-stu-id="18ce7-135">Bank account reconciliation options</span></span>
<span data-ttu-id="18ce7-136">您必须首先为银行帐户启用高级银行对帐。</span><span class="sxs-lookup"><span data-stu-id="18ce7-136">You must first enable Advanced bank reconciliation for the bank account.</span></span>  <span data-ttu-id="18ce7-137">启用高级银行对帐功后，**银行帐户**页将有很多其他选项可用。</span><span class="sxs-lookup"><span data-stu-id="18ce7-137">A number of additional options are available on the **Bank account** page once the Advanced bank reconciliation functionality is enabled.</span></span> 

<span data-ttu-id="18ce7-138">**作为电子支付的确认使用银行对帐单**功能将银行对帐功能与电子付款状态集成。</span><span class="sxs-lookup"><span data-stu-id="18ce7-138">**Use bank statements as confirmation of electronic payment** functionality integrates the bank reconciliation functionality with electronic payment statuses.</span></span>  <span data-ttu-id="18ce7-139">启用后，银行单据将为设置为**已发送**的电子付款状态自动创建。</span><span class="sxs-lookup"><span data-stu-id="18ce7-139">When this is enabled, a bank document will automatically be created for the electronic payment status is set to **Sent**.</span></span>  <span data-ttu-id="18ce7-140">此外，电子付款的状态将在匹配、对帐和过帐付款后，从**已发送**更新为**已接收**。</span><span class="sxs-lookup"><span data-stu-id="18ce7-140">In addition, the status of an electronic payment will be updated from **Sent** to **Received** after the payment is matched, reconciled, and posted.</span></span> 

<span data-ttu-id="18ce7-141">**对帐单中的银行帐户名称**字段是用于电子银行对帐单的银行帐户的名称。</span><span class="sxs-lookup"><span data-stu-id="18ce7-141">The **Bank account name in statements** field is the name used for the bank account on your electronic bank statements.</span></span>  <span data-ttu-id="18ce7-142"> 当确定为银行帐户从可能包含多个银行帐户信息的对帐单导入哪些交易记录时使用此名称。</span><span class="sxs-lookup"><span data-stu-id="18ce7-142">This name is used when determining what transactions to import for a bank account from a statement that may contain information for multiple bank accounts.</span></span> 

<span data-ttu-id="18ce7-143">选项**在导入后对帐**将自动验证银行对帐单、创建新的银行对帐和工作表中，并运行默认匹配规则集。</span><span class="sxs-lookup"><span data-stu-id="18ce7-143">The option to **Reconcile after import** will automatically validate the bank statement, create a new bank reconciliation and worksheet, and run the Default matching rule set.</span></span>  <span data-ttu-id="18ce7-144">此功能自动将流程运行到必须手动匹配的阶段。</span><span class="sxs-lookup"><span data-stu-id="18ce7-144">This functionality automates the process up to the point of the transactions that must be manually matched.</span></span>  <span data-ttu-id="18ce7-145">导入时，将默认使用银行帐户上的设置。</span><span class="sxs-lookup"><span data-stu-id="18ce7-145">The setting on the bank account will default when importing.</span></span>




