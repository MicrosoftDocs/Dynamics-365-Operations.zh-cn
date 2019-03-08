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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "308406"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="42d26-103">计算化整折旧金额</span><span class="sxs-lookup"><span data-stu-id="42d26-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42d26-104">本文讨论在“帐簿设置”页找到的“化整折旧”字段。</span><span class="sxs-lookup"><span data-stu-id="42d26-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="42d26-105">将为每个帐簿设置化差折扣金额。</span><span class="sxs-lookup"><span data-stu-id="42d26-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="42d26-106">化整折旧金额用于固定资产折旧图（显示固定资产的未来折旧和价值），也用于折旧方案。</span><span class="sxs-lookup"><span data-stu-id="42d26-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="42d26-107">输入此帐簿允许的最低折旧金额。</span><span class="sxs-lookup"><span data-stu-id="42d26-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="42d26-108">不管使用的是什么化整设置，系统都不会化整最近折旧期间的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="42d26-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="42d26-109">在最近折旧期间结束时，如果使用残值，则固定资产的值必须为 0（零）或残值。</span><span class="sxs-lookup"><span data-stu-id="42d26-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="42d26-110">示例</span><span class="sxs-lookup"><span data-stu-id="42d26-110">Example</span></span>

<span data-ttu-id="42d26-111">没有化整的折旧计算为 2,444.44。</span><span class="sxs-lookup"><span data-stu-id="42d26-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="42d26-112">如下表中所示，根据设置的化整方式，建议的金额将不同。</span><span class="sxs-lookup"><span data-stu-id="42d26-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="42d26-113">舍入方法</span><span class="sxs-lookup"><span data-stu-id="42d26-113">Rounding method</span></span> | <span data-ttu-id="42d26-114">折旧金额</span><span class="sxs-lookup"><span data-stu-id="42d26-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="42d26-115">化整 0.1</span><span class="sxs-lookup"><span data-stu-id="42d26-115">Rounding 0.1</span></span>    | <span data-ttu-id="42d26-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="42d26-116">2,444.40</span></span>            |
| <span data-ttu-id="42d26-117">化整 1.00</span><span class="sxs-lookup"><span data-stu-id="42d26-117">Rounding 1.00</span></span>   | <span data-ttu-id="42d26-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="42d26-118">2,444.00</span></span>            |
| <span data-ttu-id="42d26-119">化整 10.00</span><span class="sxs-lookup"><span data-stu-id="42d26-119">Rounding 10.00</span></span>  | <span data-ttu-id="42d26-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="42d26-120">2,440.00</span></span>            |
| <span data-ttu-id="42d26-121">化整 100.00</span><span class="sxs-lookup"><span data-stu-id="42d26-121">Rounding 100.00</span></span> | <span data-ttu-id="42d26-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="42d26-122">2,400.00</span></span>            |





