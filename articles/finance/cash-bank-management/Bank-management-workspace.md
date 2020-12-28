---
title: 银行管理工作区
description: 此主题提供了有关银行管理工作区的信息。 此工作区显示与公司银行帐户关联的信息，并包括一个汇总视图和一个分析页。 汇总视图显示汇总磁贴、银行帐户信息、余额图表和关联信息。 分析页使用 Microsoft Power BI 的功能显示与银行帐户余额相关的视觉对象。
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4b7d2da346880278f684a796f2d649e7da52b647
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "4440938"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="9dd93-106">银行管理工作区</span><span class="sxs-lookup"><span data-stu-id="9dd93-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dd93-107">**银行管理** 工作区显示与公司银行帐户关联的信息。</span><span class="sxs-lookup"><span data-stu-id="9dd93-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="9dd93-108">该工作区包括一个 **汇总** 视图和一个 **分析** 页。</span><span class="sxs-lookup"><span data-stu-id="9dd93-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="9dd93-109">**汇总** 视图显示汇总磁贴、银行帐户信息、余额图表和关联信息。</span><span class="sxs-lookup"><span data-stu-id="9dd93-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="9dd93-110">**分析** 页使用 Microsoft Power BI 的功能显示与银行帐户余额相关的视觉对象。</span><span class="sxs-lookup"><span data-stu-id="9dd93-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="9dd93-111">汇总视图</span><span class="sxs-lookup"><span data-stu-id="9dd93-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="9dd93-112">汇总</span><span class="sxs-lookup"><span data-stu-id="9dd93-112">Summary</span></span>

<span data-ttu-id="9dd93-113">在 **汇总** 部分中的磁贴提供您的银行帐户概览并提供最常用页面的快速访问。</span><span class="sxs-lookup"><span data-stu-id="9dd93-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="9dd93-114">银行对帐信息特定于高级银行对帐功能。</span><span class="sxs-lookup"><span data-stu-id="9dd93-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="9dd93-115">包含的信息仅适用于 **银行帐户** 页上的 **高级银行对帐** 选项设置为 **是** 的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="9dd93-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="9dd93-116">从 **汇总** 部分可以导入跨所有法人的银行帐户的电子银行文件。</span><span class="sxs-lookup"><span data-stu-id="9dd93-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="9dd93-117">银行帐户</span><span class="sxs-lookup"><span data-stu-id="9dd93-117">Bank accounts</span></span>

<span data-ttu-id="9dd93-118">法人中的每个银行帐户用 **银行帐户** 部分的一张卡表示。</span><span class="sxs-lookup"><span data-stu-id="9dd93-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="9dd93-119">显示当前余额，并且您可以钻取到构成该汇总余额金额的交易记录。</span><span class="sxs-lookup"><span data-stu-id="9dd93-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="9dd93-120">**过渡交易记录** 金额也可以让您钻取到构成该汇总金额的交易记录。</span><span class="sxs-lookup"><span data-stu-id="9dd93-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="9dd93-121">过渡交易记录是指已经使用过渡功能过帐但尚未清除的任何待定交易记录。</span><span class="sxs-lookup"><span data-stu-id="9dd93-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="9dd93-122">**待定余额** 金额是指当前余额减去过渡或待定交易记录。</span><span class="sxs-lookup"><span data-stu-id="9dd93-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="9dd93-123">卡上还显示上次对帐的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="9dd93-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="9dd93-124">仅当对银行帐户启用高级银行对帐时才显示此信息。</span><span class="sxs-lookup"><span data-stu-id="9dd93-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="9dd93-125">所有者权益</span><span class="sxs-lookup"><span data-stu-id="9dd93-125">Balance</span></span>

<span data-ttu-id="9dd93-126">**余额** 图表显示在 **银行帐户** 部分选择的银行帐户的历史余额信息或法人中的所有银行帐户的历史余额信息汇总。</span><span class="sxs-lookup"><span data-stu-id="9dd93-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="9dd93-127">此信息适用于不同期间：本周、本月、本年度、过去五年以及所有期间（银行帐户的完整历史记录）。</span><span class="sxs-lookup"><span data-stu-id="9dd93-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="9dd93-128">如果您正在查看单个银行帐户的 **余额** 图表，则以银行帐户币种显示历史余额。</span><span class="sxs-lookup"><span data-stu-id="9dd93-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="9dd93-129">如果您正在查看法人中的所有银行帐户的图表，则以记帐币种显示历史余额。</span><span class="sxs-lookup"><span data-stu-id="9dd93-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="9dd93-130">图表顶部显示上次更新数据的时间信息。</span><span class="sxs-lookup"><span data-stu-id="9dd93-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="9dd93-131">您可以按需要更新数据。</span><span class="sxs-lookup"><span data-stu-id="9dd93-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="9dd93-132">相关信息</span><span class="sxs-lookup"><span data-stu-id="9dd93-132">Related information</span></span>

<span data-ttu-id="9dd93-133">从 **相关信息** 部分可打开 **普通日记帐** 页面以完成银行转帐。</span><span class="sxs-lookup"><span data-stu-id="9dd93-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="9dd93-134">您还可以快速打开 **银行交易记录** 和 **过渡交易** 页。</span><span class="sxs-lookup"><span data-stu-id="9dd93-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="9dd93-135">分析视图</span><span class="sxs-lookup"><span data-stu-id="9dd93-135">Analytics view</span></span>

<span data-ttu-id="9dd93-136">**分析** 页提供有关当前公司中的银行帐户的重要指标。</span><span class="sxs-lookup"><span data-stu-id="9dd93-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="9dd93-137">页面上提供以下可视化项：</span><span class="sxs-lookup"><span data-stu-id="9dd93-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="9dd93-138">系统币种的银行总余额</span><span class="sxs-lookup"><span data-stu-id="9dd93-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="9dd93-139">按法人分类的余额</span><span class="sxs-lookup"><span data-stu-id="9dd93-139">Balance by legal entity</span></span>
-   <span data-ttu-id="9dd93-140">银行帐户币种的今日实际余额与预测余额比较</span><span class="sxs-lookup"><span data-stu-id="9dd93-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="9dd93-141">按银行帐户分类的余额</span><span class="sxs-lookup"><span data-stu-id="9dd93-141">Balance by bank account</span></span>
-   <span data-ttu-id="9dd93-142">原币余额</span><span class="sxs-lookup"><span data-stu-id="9dd93-142">Balance by currency</span></span>

<span data-ttu-id="9dd93-143">您可以从 **现金概览–所有公司** 工作区查看跨所有公司的银行分析。</span><span class="sxs-lookup"><span data-stu-id="9dd93-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="9dd93-144">有关详细信息，请参阅[现金概览 Power BI 内容](Cash-Overview-Power-BI-content.md)。</span><span class="sxs-lookup"><span data-stu-id="9dd93-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>
