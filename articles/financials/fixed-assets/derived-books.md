---
title: "派生帐簿"
description: "本文提供衍生帐簿功能的概览。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="derived-books"></a><span data-ttu-id="f29ef-103">派生帐簿</span><span class="sxs-lookup"><span data-stu-id="f29ef-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f29ef-104">本文提供衍生帐簿功能的概览。</span><span class="sxs-lookup"><span data-stu-id="f29ef-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="f29ef-105">衍生帐簿用于简化定期计划的固定资产帐簿交易记录的过帐。</span><span class="sxs-lookup"><span data-stu-id="f29ef-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="f29ef-106">选择一个帐簿作为主帐簿。</span><span class="sxs-lookup"><span data-stu-id="f29ef-106">You choose one book as the primary book.</span></span> <span data-ttu-id="f29ef-107">这通常是用于核算折旧的帐簿。</span><span class="sxs-lookup"><span data-stu-id="f29ef-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="f29ef-108">您随后附加到作为主要帐簿以相同的间隔设置来过帐交易记录的其他帐簿。</span><span class="sxs-lookup"><span data-stu-id="f29ef-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="f29ef-109">纳税折旧帐簿通常设置为衍生帐簿。</span><span class="sxs-lookup"><span data-stu-id="f29ef-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="f29ef-110">设置为过帐到衍生帐簿的最常见交易记录是购置、购置价格调整和处置。</span><span class="sxs-lookup"><span data-stu-id="f29ef-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="f29ef-111">示例</span><span class="sxs-lookup"><span data-stu-id="f29ef-111">Example</span></span>

<span data-ttu-id="f29ef-112">帐簿 B 和帐簿 C 设置为针对购置交易记录类型的帐簿 A 的衍生帐簿。</span><span class="sxs-lookup"><span data-stu-id="f29ef-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="f29ef-113">在帐簿 A 中，为资产 123 的购置交易记录输入 1,500.00。</span><span class="sxs-lookup"><span data-stu-id="f29ef-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="f29ef-114">在过帐交易记录时，在资产 123 中为帐簿 B 生成并过帐购置交易记录，并且在资产 123 中为 1,500.00 的帐簿 C 生成并过帐购置交易记录。</span><span class="sxs-lookup"><span data-stu-id="f29ef-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="f29ef-115">在您准备该主要帐簿的交易记录以用于在固定资产日志中过帐时，还可以查看和修改衍生帐簿的交易记录。</span><span class="sxs-lookup"><span data-stu-id="f29ef-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="f29ef-116">如果您在其他日志中准备主要帐簿交易记录，则衍生价值的交易记录不显示。</span><span class="sxs-lookup"><span data-stu-id="f29ef-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="f29ef-117">然而，在您过帐主要帐簿交易记录时，它们过帐到相应的帐户和过帐层。</span><span class="sxs-lookup"><span data-stu-id="f29ef-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="f29ef-118">对于设置为按并非主要帐簿间隔的其他间隔过帐交易记录的帐簿，必须将它们作为单独的帐簿附加到固定资产，而不作为衍生帐簿附加。</span><span class="sxs-lookup"><span data-stu-id="f29ef-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="f29ef-119">有关详细信息，请参阅[使用衍生帐簿过帐](post-derived-value-models.md)。</span><span class="sxs-lookup"><span data-stu-id="f29ef-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




