---
title: "使用衍生帐簿过帐"
description: "本文介绍如何使用衍生帐簿。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: aaacf596f2ea1107a53647d779e9d2b6c37ab530
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="post-with-derived-books"></a><span data-ttu-id="64755-103">使用衍生帐簿过帐</span><span class="sxs-lookup"><span data-stu-id="64755-103">Post with derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="64755-104">本文介绍如何使用衍生帐簿。</span><span class="sxs-lookup"><span data-stu-id="64755-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="64755-105">当您为一个包含衍生帐簿的帐簿过帐交易记录时，衍生帐簿交易记录将自动从日志、采购订单或普通发票过帐。</span><span class="sxs-lookup"><span data-stu-id="64755-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="64755-106">但是，如果您在固定资产日记帐中准备主要帐簿交易记录，则可以在过帐衍生交易记录的金额前查看和修改这些金额。</span><span class="sxs-lookup"><span data-stu-id="64755-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="64755-107">某些帐户（如增值税和客户或供应商帐户）只通过主要帐簿过帐的方式更新一次。</span><span class="sxs-lookup"><span data-stu-id="64755-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="64755-108">衍生帐簿交易记录将被过帐到在“固定资产过帐模板”页中为衍生帐簿定义的帐户。</span><span class="sxs-lookup"><span data-stu-id="64755-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="64755-109">购置通常用作衍生帐簿的交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="64755-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="64755-110">如果固定资产从购置之日起就应用帐簿和衍生帐簿，就使用此类型。</span><span class="sxs-lookup"><span data-stu-id="64755-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="64755-111">也可以为交易记录类型应用其他值。</span><span class="sxs-lookup"><span data-stu-id="64755-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="64755-112">例如，如果主要帐簿和衍生帐簿在销售或处置方面具有相同的间隔，则设置衍生帐簿时可以使用所有固定资产交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="64755-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="64755-113">衍生帐簿中已过帐的折旧金额应与主要帐簿中已过帐的金额相等。</span><span class="sxs-lookup"><span data-stu-id="64755-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="64755-114">如果帐簿之间的折旧方法不同，则使用衍生流程将不应生成折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="64755-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="64755-115">示例</span><span class="sxs-lookup"><span data-stu-id="64755-115">Example</span></span> 
<span data-ttu-id="64755-116">以下信息描述如何设置具有衍生帐簿功能的购置交易记录。</span><span class="sxs-lookup"><span data-stu-id="64755-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="64755-117">在“帐簿”页面上创建帐簿。</span><span class="sxs-lookup"><span data-stu-id="64755-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="64755-118">用于核算的帐簿：VM 1，当前过帐层</span><span class="sxs-lookup"><span data-stu-id="64755-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="64755-119">用于纳税目的的帐簿：VM 2，税过帐层。</span><span class="sxs-lookup"><span data-stu-id="64755-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="64755-120">在 VM 1 上，单击“衍生帐簿”选项卡。</span><span class="sxs-lookup"><span data-stu-id="64755-120">On VM 1, click the Derived books tab.</span></span> <span data-ttu-id="64755-121">在“帐簿”字段中选择 VM 2，在“交易记录类型”字段中选择“购置”。</span><span class="sxs-lookup"><span data-stu-id="64755-121">Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="64755-122">然后，可将帐簿附加到特定的固定资产。</span><span class="sxs-lookup"><span data-stu-id="64755-122">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="64755-123">当固定资产的购置使用帐簿 VM 1 过帐时，该购置不仅在 VM 1 中过帐，而且在衍生帐簿 VM 2 中过帐。</span><span class="sxs-lookup"><span data-stu-id="64755-123">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="64755-124">两种固定资产帐簿的状态将更新为“未完成”。</span><span class="sxs-lookup"><span data-stu-id="64755-124">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="64755-125">如果不使用衍生帐簿，则必须在帐簿 VM 1 和帐簿 VM 2 中都对固定资产购置过帐。</span><span class="sxs-lookup"><span data-stu-id="64755-125">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="64755-126">有关详细信息，请参阅[衍生帐簿](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="64755-126">For more information, see [Derived books](derived-books.md)</span></span>




