---
title: 应计概览
description: 本文介绍应计项目，并且提供有关如何设置和创建交易记录的信息。
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186754"
---
# <a name="accruals-overview"></a><span data-ttu-id="cafb3-103">应计概览</span><span class="sxs-lookup"><span data-stu-id="cafb3-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cafb3-104">本文介绍应计项目，并且提供有关如何设置和创建交易记录的信息。</span><span class="sxs-lookup"><span data-stu-id="cafb3-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="cafb3-105">应计用于在权责发生制中跟踪在取得收入的期间中识别的收入，而不是接收付款时，和跟踪支出（成本）发生时识别的支出（成本），而不是在进行付款时。</span><span class="sxs-lookup"><span data-stu-id="cafb3-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="cafb3-106">应计架构</span><span class="sxs-lookup"><span data-stu-id="cafb3-106">Accrual schemes</span></span>
<span data-ttu-id="cafb3-107">应计架构用于设置递延收入和成本，并且，同一个应计架构可以为收入和成本使用。</span><span class="sxs-lookup"><span data-stu-id="cafb3-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="cafb3-108">分类帐应计重新分摊日志行的成本或收入，以便成本和收入具结在相应的期间中。</span><span class="sxs-lookup"><span data-stu-id="cafb3-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="cafb3-109">在**应计架构**页上，您指定在应计架构应用时使用的借方科目和贷方科目。</span><span class="sxs-lookup"><span data-stu-id="cafb3-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="cafb3-110">**借方** – 您定义的将替换日记帐凭证行的借方主科目的主科目。</span><span class="sxs-lookup"><span data-stu-id="cafb3-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="cafb3-111">此科目也用于延期的冲销，基于分类帐应计交易记录。</span><span class="sxs-lookup"><span data-stu-id="cafb3-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="cafb3-112">**贷方** – 您定义的将替换日记帐凭证行的贷方主科目的主科目。</span><span class="sxs-lookup"><span data-stu-id="cafb3-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="cafb3-113">此科目也用于延期的冲销，基于分类帐应计交易记录。</span><span class="sxs-lookup"><span data-stu-id="cafb3-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="cafb3-114">在您确定使用哪些科目后，您可以指定在交易记录创建时如何创建凭证号。</span><span class="sxs-lookup"><span data-stu-id="cafb3-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="cafb3-115">您还可以指定交易记录发生的频率，交易记录创建的次数和交易记录过帐的时间。</span><span class="sxs-lookup"><span data-stu-id="cafb3-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="cafb3-116">在应计架构创建后，可以在某些日记帐中通过使用分类帐应计功能使用它。</span><span class="sxs-lookup"><span data-stu-id="cafb3-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="cafb3-117">分类帐应计</span><span class="sxs-lookup"><span data-stu-id="cafb3-117">Ledger accruals</span></span>
<span data-ttu-id="cafb3-118">当您输入日记帐时，您可以单击**功能**菜单中的**分类帐应计**。</span><span class="sxs-lookup"><span data-stu-id="cafb3-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="cafb3-119">然后，在您选择应计架构时，将看到将在期间内分布的日记帐的基准额，如应计架构所确定的。</span><span class="sxs-lookup"><span data-stu-id="cafb3-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="cafb3-120">例如，如果您在 1 月支付员工整年的保险且金额是 12,000，则您必须每个月识别该支出。</span><span class="sxs-lookup"><span data-stu-id="cafb3-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="cafb3-121">您可以选择开始日期。</span><span class="sxs-lookup"><span data-stu-id="cafb3-121">You can select the start date.</span></span> <span data-ttu-id="cafb3-122">您还可以指定应计的金额是否基于此科目或对方科目。</span><span class="sxs-lookup"><span data-stu-id="cafb3-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="cafb3-123">在您进行选择后，单击**交易记录**查看基于应计架构创建的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="cafb3-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="cafb3-124">例如，如果您在该年度的保险开支中分布 12,000，则每个月将看到 1,000。</span><span class="sxs-lookup"><span data-stu-id="cafb3-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="cafb3-125">在过帐日记帐后，可以通过使用**凭证交易记录**查询页查看交易记录。</span><span class="sxs-lookup"><span data-stu-id="cafb3-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="cafb3-126">如果应计架构不能应用（例如，当涉及销售订单发票或采购订单发票时），则您可以将预付的金额记入贷方，将支出金额记入借方。</span><span class="sxs-lookup"><span data-stu-id="cafb3-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="cafb3-127">然后您可以在应用应计架构时选择**对方**。</span><span class="sxs-lookup"><span data-stu-id="cafb3-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="cafb3-128">有关详细信息，请参阅[创建应计架构](tasks/create-accrual-schemes.md)和[创建分类帐应计交易记录](tasks/create-ledger-accrual-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="cafb3-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>
