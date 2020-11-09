---
title: 拆分固定资产
description: 此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000285"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="d3eba-103">拆分固定资产</span><span class="sxs-lookup"><span data-stu-id="d3eba-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3eba-104">此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="d3eba-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="d3eba-105">它使用会计角色和 USMF 演示数据。</span><span class="sxs-lookup"><span data-stu-id="d3eba-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="d3eba-106">创建新的固定资产</span><span class="sxs-lookup"><span data-stu-id="d3eba-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="d3eba-107">在导航窗格中，转到 **模块 \> 固定资产 \> 固定资产 \> 固定资产** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="d3eba-108">选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-108">Select **New**.</span></span>
3. <span data-ttu-id="d3eba-109">在 **固定资产组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3eba-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="d3eba-110">请注意，固定资产编号将在稍后的拆分流程使用。</span><span class="sxs-lookup"><span data-stu-id="d3eba-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="d3eba-111">在 **名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3eba-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="d3eba-112">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="d3eba-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="d3eba-113">拆分固定资产</span><span class="sxs-lookup"><span data-stu-id="d3eba-113">Split a fixed asset</span></span>

<span data-ttu-id="d3eba-114">在拆分完全折旧资产之前，应手动将资产帐簿状态从 **已结算** 更改为 **未结** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="d3eba-115">此步骤是必需的，因为如果您必须过帐资产的交易（例如处置销售），帐簿状态必须为 **未结** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="d3eba-116">更改资产帐簿状态后，请按照以下步骤拆分资产。</span><span class="sxs-lookup"><span data-stu-id="d3eba-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="d3eba-117">在列表中，查找并选择要拆分的固定资产的链接。</span><span class="sxs-lookup"><span data-stu-id="d3eba-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="d3eba-118">选择 **帐簿** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-118">Select **Books**.</span></span> <span data-ttu-id="d3eba-119">选择拆分到新资产的帐簿</span><span class="sxs-lookup"><span data-stu-id="d3eba-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="d3eba-120">选择 **功能** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-120">Select **Functions**.</span></span>
4. <span data-ttu-id="d3eba-121">选择 **拆分固定资产** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="d3eba-122">在 **目标固定资产** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3eba-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="d3eba-123">在 **目标帐簿** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d3eba-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d3eba-124">在 **交易记录日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="d3eba-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="d3eba-125">在 **百分比** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d3eba-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="d3eba-126">在 **日记帐名称** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3eba-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="d3eba-127">选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="d3eba-128">过帐日记帐交易记录</span><span class="sxs-lookup"><span data-stu-id="d3eba-128">Post the journal transaction</span></span>

1. <span data-ttu-id="d3eba-129">在导航窗格中，转到 **模块 \> 固定资产 \> 日记帐条目 \> 固定资产日记帐** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="d3eba-130">在列表中，选择在拆分流程创建的日记帐。</span><span class="sxs-lookup"><span data-stu-id="d3eba-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="d3eba-131">选择 **行** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-131">Select **Lines**.</span></span>

    - <span data-ttu-id="d3eba-132">验证已创建的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="d3eba-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="d3eba-133">创建原始资产的购置调整交易记录，以通过拆分流程指定的百分比减少价值。</span><span class="sxs-lookup"><span data-stu-id="d3eba-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="d3eba-134">为新资产创建相同金额的购置交易记录。</span><span class="sxs-lookup"><span data-stu-id="d3eba-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="d3eba-135">选择 **过帐** 。</span><span class="sxs-lookup"><span data-stu-id="d3eba-135">Select **Post**.</span></span>
