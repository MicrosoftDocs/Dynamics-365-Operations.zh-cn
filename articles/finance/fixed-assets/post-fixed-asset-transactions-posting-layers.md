---
title: 将固定资产交易记录过帐到过帐层
description: 本文提供固定资产交易记录的过帐层功能的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770704"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="53197-103">将固定资产交易记录过帐到过帐层</span><span class="sxs-lookup"><span data-stu-id="53197-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53197-104">本文提供固定资产交易记录的过帐层功能的概览。</span><span class="sxs-lookup"><span data-stu-id="53197-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="53197-105">通常，出于不同的目的会采用不同的方法对固定资产进行折旧。</span><span class="sxs-lookup"><span data-stu-id="53197-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="53197-106">出于纳税目的，将根据当前的纳税规则计算折旧，以实现尽可能高的税前折旧；但出于报告目的，将根据会计法和标准计算折旧。</span><span class="sxs-lookup"><span data-stu-id="53197-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="53197-107">各种折旧都分别在过帐层进行计算和记录。</span><span class="sxs-lookup"><span data-stu-id="53197-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="53197-108">附加到固定资产的每个帐簿都是针对具有整体折旧目标的特定过帐层设置的。</span><span class="sxs-lookup"><span data-stu-id="53197-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="53197-109">有十个过帐层：当前、工序、纳税和七个自定义层。</span><span class="sxs-lookup"><span data-stu-id="53197-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="53197-110">您还可以通过将“过帐到总帐”字段设置为“否”，为帐簿禁用过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="53197-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="53197-111">“过帐层”字段将自动设置为“无”。</span><span class="sxs-lookup"><span data-stu-id="53197-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="53197-112">不过帐到总帐的帐簿通常用于报税用途。</span><span class="sxs-lookup"><span data-stu-id="53197-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="53197-113">这样您的灵活性更高，可以删除资产帐簿的历史交易信息，因为这些信息尚未提交给总帐。</span><span class="sxs-lookup"><span data-stu-id="53197-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="53197-114">固定资产日记帐通过“日记帐名称”页面上的总帐 >日记帐设置 >日记帐名称进行定义。</span><span class="sxs-lookup"><span data-stu-id="53197-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="53197-115">可以将折旧过帐到其中的每个日志都只能由其日志名称为一个过帐层定义。</span><span class="sxs-lookup"><span data-stu-id="53197-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="53197-116">日记帐中的过帐层无法更改。</span><span class="sxs-lookup"><span data-stu-id="53197-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="53197-117">此限制有助于保障每个过帐层的交易记录都单独存放。</span><span class="sxs-lookup"><span data-stu-id="53197-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="53197-118">因此，必须为每个过帐层至少创建一个日志名称。</span><span class="sxs-lookup"><span data-stu-id="53197-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="53197-119">如果您在使用不过帐到总帐的帐簿，则还必须创建过帐层设置为“无”的日记帐。</span><span class="sxs-lookup"><span data-stu-id="53197-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="53197-120">您可以在“固定资产过帐模板”页指定固定资产交易记录的会计科目。</span><span class="sxs-lookup"><span data-stu-id="53197-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="53197-121">对于每个过帐模板，都必须选择相关的交易记录类型和帐簿，然后指定会计科目。</span><span class="sxs-lookup"><span data-stu-id="53197-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="53197-122">设置要过帐到总帐的每个帐簿的过帐模板记录。</span><span class="sxs-lookup"><span data-stu-id="53197-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="53197-123">使用衍生帐簿，可以将交易记录同时过帐到不同的过帐层。</span><span class="sxs-lookup"><span data-stu-id="53197-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="53197-124">可以在过帐层对应于帐簿过帐层的日记帐中创建主帐簿的交易记录。</span><span class="sxs-lookup"><span data-stu-id="53197-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="53197-125">在过帐期间，衍生帐簿交易记录将过帐到相应的过帐层。</span><span class="sxs-lookup"><span data-stu-id="53197-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="53197-126">有关详细信息，请参阅[衍生帐簿](derived-books.md)和[使用衍生帐簿过帐](post-derived-value-models.md)。</span><span class="sxs-lookup"><span data-stu-id="53197-126">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



