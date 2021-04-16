---
title: 拆分固定资产
description: 此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa21d5698275ff691ca83d29abd297a796b652d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823900"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="aa6a1-103">拆分固定资产</span><span class="sxs-lookup"><span data-stu-id="aa6a1-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa6a1-104">此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="aa6a1-105">它使用会计角色和 USMF 演示数据。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="aa6a1-106">创建新的固定资产</span><span class="sxs-lookup"><span data-stu-id="aa6a1-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="aa6a1-107">在导航窗格中，转到 **模块 \> 固定资产 \> 固定资产 \> 固定资产**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="aa6a1-108">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-108">Select **New**.</span></span>
3. <span data-ttu-id="aa6a1-109">在 **固定资产组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="aa6a1-110">请注意，固定资产编号将在稍后的拆分流程使用。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="aa6a1-111">在 **名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="aa6a1-112">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="aa6a1-113">拆分固定资产</span><span class="sxs-lookup"><span data-stu-id="aa6a1-113">Split a fixed asset</span></span>

<span data-ttu-id="aa6a1-114">在拆分完全折旧资产之前，应手动将资产帐簿状态从 **已结算** 更改为 **未结**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="aa6a1-115">此步骤是必需的，因为如果您必须过帐资产的交易（例如处置销售），帐簿状态必须为 **未结**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="aa6a1-116">还必须开启 **总帐参数** 页面 **常规** 选项卡上的 **一个凭证可以允许多个交易记录** 参数。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="aa6a1-117">资产帐簿状态更改并允许一张凭单中有多项交易记录后，请完成以下步骤拆分资产。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="aa6a1-118">在列表中，查找并选择要拆分的固定资产的链接。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="aa6a1-119">选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-119">Select **Books**.</span></span> <span data-ttu-id="aa6a1-120">选择拆分到新资产的帐簿</span><span class="sxs-lookup"><span data-stu-id="aa6a1-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="aa6a1-121">选择 **功能**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-121">Select **Functions**.</span></span>
4. <span data-ttu-id="aa6a1-122">选择 **拆分固定资产**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="aa6a1-123">在 **目标固定资产** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="aa6a1-124">在 **目标帐簿** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aa6a1-125">在 **交易记录日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="aa6a1-126">在 **百分比** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="aa6a1-127">在 **日记帐名称** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="aa6a1-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="aa6a1-129">过帐日记帐交易记录</span><span class="sxs-lookup"><span data-stu-id="aa6a1-129">Post the journal transaction</span></span>

1. <span data-ttu-id="aa6a1-130">在导航窗格中，转到 **模块 \> 固定资产 \> 日记帐条目 \> 固定资产日记帐**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="aa6a1-131">在列表中，选择在拆分流程创建的日记帐。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="aa6a1-132">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-132">Select **Lines**.</span></span>

    - <span data-ttu-id="aa6a1-133">验证已创建的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="aa6a1-134">创建原始资产的购置调整交易记录，以通过拆分流程指定的百分比减少价值。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="aa6a1-135">为新资产创建相同金额的购置交易记录。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="aa6a1-136">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="aa6a1-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]