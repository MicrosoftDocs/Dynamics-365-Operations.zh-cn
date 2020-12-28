---
title: 固定资产折旧
description: 文主题提供固定资产折旧的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1056dadab4294072cc064670f5cfcda239e22e19
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440736"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="c7cce-103">固定资产折旧</span><span class="sxs-lookup"><span data-stu-id="c7cce-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7cce-104">文主题提供固定资产折旧的概览。</span><span class="sxs-lookup"><span data-stu-id="c7cce-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="c7cce-105">折旧是一种期间交易记录，通常会减少资产负债表中固定资产的价值，并且在损益科目中作为支出计费。</span><span class="sxs-lookup"><span data-stu-id="c7cce-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="c7cce-106">因此，主科目通常用于将折旧定期贷计到资产负债表中。</span><span class="sxs-lookup"><span data-stu-id="c7cce-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="c7cce-107">对方科目是会计科目表中的损益部分中的科目。</span><span class="sxs-lookup"><span data-stu-id="c7cce-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="c7cce-108">折旧调整</span><span class="sxs-lookup"><span data-stu-id="c7cce-108">Depreciation adjustment</span></span>
<span data-ttu-id="c7cce-109">通常，只有对已过帐折旧交易记录的更正作为“折旧调整”过帐。</span><span class="sxs-lookup"><span data-stu-id="c7cce-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="c7cce-110">因此，主科目和对方科目都同折旧科目一样进行设置。</span><span class="sxs-lookup"><span data-stu-id="c7cce-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="c7cce-111">折旧调整可以是正金额或负金额，但“主科目”（作为资产负债表科目）和“对方科目”（通常作为损益科目）的功能保持相同。</span><span class="sxs-lookup"><span data-stu-id="c7cce-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="c7cce-112">特别折旧</span><span class="sxs-lookup"><span data-stu-id="c7cce-112">Extraordinary depreciation</span></span>
<span data-ttu-id="c7cce-113">特殊折旧类似于基本折旧。</span><span class="sxs-lookup"><span data-stu-id="c7cce-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="c7cce-114">因此，主科目用于将折旧金额贷计到资产负债表中以及减少固定资产的值。</span><span class="sxs-lookup"><span data-stu-id="c7cce-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="c7cce-115">对方科目是损益科目，折旧计算为会计期间作为支出计费。</span><span class="sxs-lookup"><span data-stu-id="c7cce-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="c7cce-116">特殊折旧在工作方式上与基本折旧不同。</span><span class="sxs-lookup"><span data-stu-id="c7cce-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="c7cce-117">通过将“特殊折旧”作为单独的交易记录类型，您可以采用与基本折旧不同的方式，过帐和报告特殊折旧。</span><span class="sxs-lookup"><span data-stu-id="c7cce-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="c7cce-118">特殊折旧补偿</span><span class="sxs-lookup"><span data-stu-id="c7cce-118">Special depreciation allowance</span></span>
<span data-ttu-id="c7cce-119">您可以在资产投入使用并开始折旧的第一年使用特殊折旧补偿提取额外折旧金额。</span><span class="sxs-lookup"><span data-stu-id="c7cce-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="c7cce-120">必须在进行任何其他折旧计算前提取特殊折旧补偿。</span><span class="sxs-lookup"><span data-stu-id="c7cce-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="c7cce-121">因为特殊折旧补偿通常会在固定资产使用年限的后期才会知晓，因此最好是对不过帐到总帐的帐簿使用这种折旧类型。</span><span class="sxs-lookup"><span data-stu-id="c7cce-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="c7cce-122">您可以使用“删除尚未过帐到总帐的交易记录”定期功能删除这些帐簿的历史交易记录。</span><span class="sxs-lookup"><span data-stu-id="c7cce-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="c7cce-123">然后您可以删除固定资产帐簿的折旧历史记录，在特殊折旧补偿已知时进行过帐，再过帐当年的剩余折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="c7cce-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="c7cce-124">您可以创建任意数量的特殊折旧补偿记录。</span><span class="sxs-lookup"><span data-stu-id="c7cce-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="c7cce-125">将这些记录分配给资产组帐簿后，这些记录会应用于资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="c7cce-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="c7cce-126">特殊折旧补偿作为百分比或固定金额输入。</span><span class="sxs-lookup"><span data-stu-id="c7cce-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="c7cce-127">过帐折旧方案时，特殊折旧补偿交易记录会作为不同于折旧交易记录的交易记录过帐到帐簿。</span><span class="sxs-lookup"><span data-stu-id="c7cce-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="c7cce-128">折旧年份：日历</span><span class="sxs-lookup"><span data-stu-id="c7cce-128">Depreciation calendars</span></span>
<span data-ttu-id="c7cce-129">每个帐簿都有在折旧固定资产时使用的日历。</span><span class="sxs-lookup"><span data-stu-id="c7cce-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="c7cce-130">默认情况下，如果您未在帐簿上指示日历，帐簿将使用分类帐会计日历。</span><span class="sxs-lookup"><span data-stu-id="c7cce-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="c7cce-131">如果帐簿的关联折旧模板使用会计折旧年度，您必须为该帐簿选择会计日历。</span><span class="sxs-lookup"><span data-stu-id="c7cce-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="c7cce-132">您可以在总帐中使用 **会计日历** 页创建共享日历。</span><span class="sxs-lookup"><span data-stu-id="c7cce-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="c7cce-133">有关详细信息，请参阅[折旧法和惯例](depreciation-methods-conventions.md)。</span><span class="sxs-lookup"><span data-stu-id="c7cce-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



