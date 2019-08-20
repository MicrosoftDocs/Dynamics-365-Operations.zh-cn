---
title: 额外折旧
description: 本文提供红利折旧功能的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687ba57042ad65d3a1ff4ad92f0da774c6751eac
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840665"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="e0be2-103">额外折旧</span><span class="sxs-lookup"><span data-stu-id="e0be2-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0be2-104">本文提供红利折旧功能的概览。</span><span class="sxs-lookup"><span data-stu-id="e0be2-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="e0be2-105">对于额外折旧，您可以在资产投入使用并开始折旧的第一年中提取额外的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="e0be2-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="e0be2-106">必须在进行任何其他折旧计算前提取额外折旧。</span><span class="sxs-lookup"><span data-stu-id="e0be2-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="e0be2-107">因此，最好是在帐簿禁用“过帐到总帐”功能时使用额外折旧。</span><span class="sxs-lookup"><span data-stu-id="e0be2-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="e0be2-108">您可以使用**删除尚未过帐到总帐的交易记录**选项删除未过帐到总帐的帐簿的历史交易记录。</span><span class="sxs-lookup"><span data-stu-id="e0be2-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="e0be2-109">然后，您将来可以通过删除先前过帐的折旧交易记录在资产生命周期中容纳额外折旧。</span><span class="sxs-lookup"><span data-stu-id="e0be2-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="e0be2-110">您可以通过使用方案过程计算额外折旧，也可以创建手动额外折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="e0be2-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="e0be2-111">如果该资产帐簿存在折旧交易记录或折旧调整交易记录，则不能创建额外折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="e0be2-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="e0be2-112">当您使用方案过程计算额外折旧时，所有现有额外折旧交易记录都包括在基础计算中。</span><span class="sxs-lookup"><span data-stu-id="e0be2-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="e0be2-113">该计算还包括您为资产手动输入的任何先前的额外折旧。</span><span class="sxs-lookup"><span data-stu-id="e0be2-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="e0be2-114">如果某资产将进行多项额外折旧，将考虑优先级。</span><span class="sxs-lookup"><span data-stu-id="e0be2-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="e0be2-115">每此额外折旧减少了下此额外折旧的资产基础。</span><span class="sxs-lookup"><span data-stu-id="e0be2-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="e0be2-116">在额外折旧计算的资产基础中不考虑残值，而且折旧惯例不会应用于额外折旧。</span><span class="sxs-lookup"><span data-stu-id="e0be2-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="e0be2-117">目前在美国，某些财产符合第 179 条关于财产的规定。</span><span class="sxs-lookup"><span data-stu-id="e0be2-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="e0be2-118">通过使用第 179 条扣缴，您可以撤消某项资产的全部或部分成本，直到一个限额。</span><span class="sxs-lookup"><span data-stu-id="e0be2-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="e0be2-119">您可以通过在您投入资产的那一年减少成本来恢复成本。</span><span class="sxs-lookup"><span data-stu-id="e0be2-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="e0be2-120">示例</span><span class="sxs-lookup"><span data-stu-id="e0be2-120">Example</span></span>
<span data-ttu-id="e0be2-121">以下额外折旧与资产帐簿相关联：</span><span class="sxs-lookup"><span data-stu-id="e0be2-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="e0be2-122">**第 179 条：** 1,000.00，优先级 1</span><span class="sxs-lookup"><span data-stu-id="e0be2-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="e0be2-123">**自由区**：30%，优先级 2</span><span class="sxs-lookup"><span data-stu-id="e0be2-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="e0be2-124">资产购置成本为 5,000.00。</span><span class="sxs-lookup"><span data-stu-id="e0be2-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="e0be2-125">计算额外折旧时，根据第 179 条的折旧规定，第一笔额外折旧金额为 1,000.00 美元。</span><span class="sxs-lookup"><span data-stu-id="e0be2-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="e0be2-126">对于“自由区”折旧而言，将使用以下方法计算下一笔额外折旧金额：</span><span class="sxs-lookup"><span data-stu-id="e0be2-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="e0be2-127">购置成本 – 1,000（第 179 条的折旧规定） x 30% = 1,200</span><span class="sxs-lookup"><span data-stu-id="e0be2-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="e0be2-128">如果额外折旧金额大于剩余的购置成本，额外折旧金额将是额外折旧计算金额和剩余购置成本两者中较小的金额。</span><span class="sxs-lookup"><span data-stu-id="e0be2-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="e0be2-129">如果剩余的购置成本为 0（零）或更少，将不会生成额外折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="e0be2-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="e0be2-130">使用方案过程计算额外折旧时，将会为与资产帐簿关联的所有适用额外折旧记录创建额外折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="e0be2-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="e0be2-131">您可以创建数量不限的额外折旧记录。</span><span class="sxs-lookup"><span data-stu-id="e0be2-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="e0be2-132">将这些记录分配给资产组帐簿后，这些记录会应用于资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="e0be2-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="e0be2-133">额外折旧作为百分比或固定金额输入。</span><span class="sxs-lookup"><span data-stu-id="e0be2-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="e0be2-134">过帐折旧方案时，额外折旧交易记录将作为不同于折旧交易记录的单独的交易记录过帐到帐簿。</span><span class="sxs-lookup"><span data-stu-id="e0be2-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>



