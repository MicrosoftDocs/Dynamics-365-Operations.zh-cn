---
title: 计算化整折旧金额
description: 本文讨论在“帐簿设置”页找到的“化整折旧”字段。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40fd019b1b5900fbd15866d9d3c32ed6d88147b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440810"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="33470-103">计算化整折旧金额</span><span class="sxs-lookup"><span data-stu-id="33470-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33470-104">本文讨论在“帐簿设置”页找到的“化整折旧”字段。</span><span class="sxs-lookup"><span data-stu-id="33470-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="33470-105">将为每个帐簿设置化差折扣金额。</span><span class="sxs-lookup"><span data-stu-id="33470-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="33470-106">化整折旧金额用于固定资产折旧图（显示固定资产的未来折旧和价值），也用于折旧方案。</span><span class="sxs-lookup"><span data-stu-id="33470-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="33470-107">输入此帐簿允许的最低折旧金额。</span><span class="sxs-lookup"><span data-stu-id="33470-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="33470-108">不管使用的是什么化整设置，系统都不会化整最近折旧期间的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="33470-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="33470-109">在最近折旧期间结束时，如果使用残值，则固定资产的值必须为 0（零）或残值。</span><span class="sxs-lookup"><span data-stu-id="33470-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="33470-110">示例</span><span class="sxs-lookup"><span data-stu-id="33470-110">Example</span></span>

<span data-ttu-id="33470-111">没有化整的折旧计算为 2,444.44。</span><span class="sxs-lookup"><span data-stu-id="33470-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="33470-112">如下表中所示，根据设置的化整方式，建议的金额将不同。</span><span class="sxs-lookup"><span data-stu-id="33470-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="33470-113">化整方法</span><span class="sxs-lookup"><span data-stu-id="33470-113">Rounding method</span></span> | <span data-ttu-id="33470-114">折旧金额</span><span class="sxs-lookup"><span data-stu-id="33470-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="33470-115">化整 0.1</span><span class="sxs-lookup"><span data-stu-id="33470-115">Rounding 0.1</span></span>    | <span data-ttu-id="33470-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="33470-116">2,444.40</span></span>            |
| <span data-ttu-id="33470-117">化整 1.00</span><span class="sxs-lookup"><span data-stu-id="33470-117">Rounding 1.00</span></span>   | <span data-ttu-id="33470-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="33470-118">2,444.00</span></span>            |
| <span data-ttu-id="33470-119">化整 10.00</span><span class="sxs-lookup"><span data-stu-id="33470-119">Rounding 10.00</span></span>  | <span data-ttu-id="33470-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="33470-120">2,440.00</span></span>            |
| <span data-ttu-id="33470-121">化整 100.00</span><span class="sxs-lookup"><span data-stu-id="33470-121">Rounding 100.00</span></span> | <span data-ttu-id="33470-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="33470-122">2,400.00</span></span>            |





