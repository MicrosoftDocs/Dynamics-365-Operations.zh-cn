---
title: "库存标签盘点"
description: "本文提供有关您用于将仓库的实际内容与现有库存量进行比较的标签盘点的信息。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 9e129fda638cfd8cff0e40079747f7ca70fa7531
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2017

---

# <a name="inventory-tag-counting"></a><span data-ttu-id="7c780-103">库存标签盘点</span><span class="sxs-lookup"><span data-stu-id="7c780-103">Inventory tag counting</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="7c780-104">本文提供有关您用于将仓库的实际内容与现有库存量进行比较的标签盘点的信息。</span><span class="sxs-lookup"><span data-stu-id="7c780-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="7c780-105">通过在**标签盘点**页上创建行，您将在每个库存物料上放置一个标签编号（如从 1 到 500 的数字）。</span><span class="sxs-lookup"><span data-stu-id="7c780-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="7c780-106">在盘点期间，您应在相应标签上输入物料编号和数量。</span><span class="sxs-lookup"><span data-stu-id="7c780-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="7c780-107">此标签随后可用作标签盘点日记帐中的输入的基础。</span><span class="sxs-lookup"><span data-stu-id="7c780-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="7c780-108">过帐标签盘点日记帐后，将在**“盘点”**页上创建一个新的盘点日记帐。</span><span class="sxs-lookup"><span data-stu-id="7c780-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="7c780-109">新日记帐基于您创建的标签盘点日记帐行。</span><span class="sxs-lookup"><span data-stu-id="7c780-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="7c780-110">要按特定库存维度对物料进行标签盘点，请在创建标签盘点日记帐时在**“显示维度”**页上选择维度。</span><span class="sxs-lookup"><span data-stu-id="7c780-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="7c780-111">例如，要盘点特定仓库中的物料，请选中**“仓库”**复选框。</span><span class="sxs-lookup"><span data-stu-id="7c780-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="7c780-112">如果选择了**“库存和仓库管理参数”**页上的**“盘点期间锁定物料”**滑块，则在盘点期间无法实际更新物料。</span><span class="sxs-lookup"><span data-stu-id="7c780-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="7c780-113">但是，标签盘点日记帐中的物料在盘点期间不会锁定。</span><span class="sxs-lookup"><span data-stu-id="7c780-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="7c780-114">在将标签盘点行过帐并转移到盘点日记帐之前不会创建库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="7c780-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="7c780-115">如果随机输入了标签并且您希望标识缺失的标签，请单击**“标签”**列标题以按标签为行排序。</span><span class="sxs-lookup"><span data-stu-id="7c780-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="see-also"></a><span data-ttu-id="7c780-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="7c780-116">See also</span></span>
--------

[<span data-ttu-id="7c780-117">周期盘点</span><span class="sxs-lookup"><span data-stu-id="7c780-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)

