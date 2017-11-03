---
title: "库存日记帐"
description: "本文介绍如何使用库存日记帐过帐实际库存交易记录的不同类型。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 968bf9a243d0c0cc9f0dfec474cb207ca32f9eeb
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-journals"></a><span data-ttu-id="f3bff-103">库存日记帐</span><span class="sxs-lookup"><span data-stu-id="f3bff-103">Inventory journals</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="f3bff-104">本文介绍如何使用库存日记帐过帐实际库存交易记录的不同类型。</span><span class="sxs-lookup"><span data-stu-id="f3bff-104">This article describes how you can use inventory journals to post various types of physical inventory transactions.</span></span>

<span data-ttu-id="f3bff-105">Microsoft Dynamics 365 for Finance and Operations 中的库存日记帐用于过帐多种类型的实际库存交易记录，如发货和收货的过帐、库存变动、物料清单的创建，以及实际库存的对帐。</span><span class="sxs-lookup"><span data-stu-id="f3bff-105">The inventory journals in Microsoft Dynamics 365 for Finance and Operations are used to post physical inventory transactions of various types, such as the posting of issues and receipts, inventory movements, the creation of bills of materials (BOMs), and the reconciliation of physical inventory.</span></span> <span data-ttu-id="f3bff-106">所有这些库存日记帐以相同的方式被使用，不过，它们划分为不同类型。</span><span class="sxs-lookup"><span data-stu-id="f3bff-106">All these inventory journals are used in a similar way, but they are divided into different types.</span></span>

## <a name="types-of-inventory-journals"></a><span data-ttu-id="f3bff-107">库存日记帐的类型</span><span class="sxs-lookup"><span data-stu-id="f3bff-107">Types of inventory journals</span></span>
<span data-ttu-id="f3bff-108">提供以下库存日记帐类型：</span><span class="sxs-lookup"><span data-stu-id="f3bff-108">The following types of inventory journals are available:</span></span>

-   <span data-ttu-id="f3bff-109">移动</span><span class="sxs-lookup"><span data-stu-id="f3bff-109">Movement</span></span>
-   <span data-ttu-id="f3bff-110">库存调整</span><span class="sxs-lookup"><span data-stu-id="f3bff-110">Inventory adjustment</span></span>
-   <span data-ttu-id="f3bff-111">转移</span><span class="sxs-lookup"><span data-stu-id="f3bff-111">Transfer</span></span>
-   <span data-ttu-id="f3bff-112">物料清单</span><span class="sxs-lookup"><span data-stu-id="f3bff-112">BOM</span></span>
-   <span data-ttu-id="f3bff-113">物料到达</span><span class="sxs-lookup"><span data-stu-id="f3bff-113">Item arrival</span></span>
-   <span data-ttu-id="f3bff-114">生产输入</span><span class="sxs-lookup"><span data-stu-id="f3bff-114">Production input</span></span>
-   <span data-ttu-id="f3bff-115">正在盘点</span><span class="sxs-lookup"><span data-stu-id="f3bff-115">Counting</span></span>
-   <span data-ttu-id="f3bff-116">标签盘点</span><span class="sxs-lookup"><span data-stu-id="f3bff-116">Tag counting</span></span>

### <a name="movement"></a><span data-ttu-id="f3bff-117">移动</span><span class="sxs-lookup"><span data-stu-id="f3bff-117">Movement</span></span>

<span data-ttu-id="f3bff-118">当您使用一个库存变动日记帐时，您可以在添加库存时向物料中添加成本，不过，您必须通过在创建日记帐时指定总帐对方科目，手动将附加成本分配给特定的总帐科目。</span><span class="sxs-lookup"><span data-stu-id="f3bff-118">When you use an inventory movement journal, you can add cost to an item when you add inventory, but you must manually allocate the additional cost to a particular general ledger account by specifying a general ledger offset account when you create the journal.</span></span> <span data-ttu-id="f3bff-119">如果您想要将物料支出分配给不同部门，或者，如果要针对支出用途从库存中删除物料，则此库存日记帐类型很有用。</span><span class="sxs-lookup"><span data-stu-id="f3bff-119">This inventory journal type is useful if you want to expense an item against a different department, or if you want to remove items from inventory for expense purposes.</span></span>

### <a name="inventory-adjustment"></a><span data-ttu-id="f3bff-120">库存调整</span><span class="sxs-lookup"><span data-stu-id="f3bff-120">Inventory adjustment</span></span>

<span data-ttu-id="f3bff-121">当您使用库存调整日记帐时，您可以在添加库存时向物料中添加成本。</span><span class="sxs-lookup"><span data-stu-id="f3bff-121">When you use an inventory adjustment journal, you can add cost to an item when you add inventory.</span></span> <span data-ttu-id="f3bff-122">附加成本将基于物料组过帐模板的设置，自动过帐到特定总帐科目。</span><span class="sxs-lookup"><span data-stu-id="f3bff-122">The additional cost is automatically posted to a specific general ledger account, based on the setup of the item group posting profile.</span></span> <span data-ttu-id="f3bff-123">在物料应保留其值默认总帐对方科目时，使用此库存日记帐类型将收益和损失更新到库存数量。</span><span class="sxs-lookup"><span data-stu-id="f3bff-123">Use this inventory journal type to update gains and losses to inventory quantities when the item should keep its default general ledger offset account.</span></span> <span data-ttu-id="f3bff-124">在过帐库存调整日记帐时，将过帐库存收货或发货、更改库存值，并创建分录。</span><span class="sxs-lookup"><span data-stu-id="f3bff-124">When you post an inventory adjustment journal, an inventory receipt or issue is posted, the inventory values are changed, and ledger transactions are created.</span></span>

### <a name="transfer"></a><span data-ttu-id="f3bff-125">转移</span><span class="sxs-lookup"><span data-stu-id="f3bff-125">Transfer</span></span>

<span data-ttu-id="f3bff-126">您可以使用转移日记帐在库存位置、批次或产品变型之间转移物料而不关联任何成本影响。</span><span class="sxs-lookup"><span data-stu-id="f3bff-126">You can use transfer journals to transfer items between stocking locations, batches, or product variants without associating any cost implications.</span></span> <span data-ttu-id="f3bff-127">例如，您可以将物料在同一公司内从一个仓库转移到另一个仓库。</span><span class="sxs-lookup"><span data-stu-id="f3bff-127">For example, you can transfer items from one warehouse to another warehouse within the same company.</span></span> <span data-ttu-id="f3bff-128">在您使用转移日记帐时，必须指定“从”和“到”库存维度（例如，对于站点和仓库）。</span><span class="sxs-lookup"><span data-stu-id="f3bff-128">When you use a transfer journal, you must specify both the "from" and "to" inventory dimensions (for example, for Site and Warehouse).</span></span> <span data-ttu-id="f3bff-129">已定义库存维度的现有库存量相应更改。</span><span class="sxs-lookup"><span data-stu-id="f3bff-129">The on-hand inventory for the defined inventory dimensions is changed accordingly.</span></span> <span data-ttu-id="f3bff-130">库存转移反映物料的即时移动。</span><span class="sxs-lookup"><span data-stu-id="f3bff-130">Inventory transfers reflect the immediate movement of material.</span></span> <span data-ttu-id="f3bff-131">中转库存不被跟踪。</span><span class="sxs-lookup"><span data-stu-id="f3bff-131">In-transit inventory isn't tracked.</span></span> <span data-ttu-id="f3bff-132">如果必须跟踪中转库存，则应使用转移单。</span><span class="sxs-lookup"><span data-stu-id="f3bff-132">If in-transit inventory must be tracked, you should use a transfer order instead.</span></span> <span data-ttu-id="f3bff-133">在过帐转移日记帐时，将为每个日记帐行创建两个库存交易记录：</span><span class="sxs-lookup"><span data-stu-id="f3bff-133">When you post a transfer journal, two inventory transactions are created for each journal line:</span></span>

-   <span data-ttu-id="f3bff-134">“从”位置的库存发货</span><span class="sxs-lookup"><span data-stu-id="f3bff-134">An inventory issue at the "from" location</span></span>
-   <span data-ttu-id="f3bff-135">“到”位置的库存收货</span><span class="sxs-lookup"><span data-stu-id="f3bff-135">An inventory receipt at the "to" location</span></span>

### <a name="bom"></a><span data-ttu-id="f3bff-136">物料清单</span><span class="sxs-lookup"><span data-stu-id="f3bff-136">BOM</span></span>

<span data-ttu-id="f3bff-137">当您将物料清单报告为已完工入库时，可以创建物料清单日记帐。</span><span class="sxs-lookup"><span data-stu-id="f3bff-137">When you report a BOM as finished, you can create a BOM journal.</span></span> <span data-ttu-id="f3bff-138">通过使用物料清单日志，您可以直接过帐物料清单。</span><span class="sxs-lookup"><span data-stu-id="f3bff-138">By using a BOM journal, you can post the BOM directly.</span></span> <span data-ttu-id="f3bff-139">此过帐生成产品的的库存收货，以及关联的物料清单以及物料清单中包括的产品的库存发货。</span><span class="sxs-lookup"><span data-stu-id="f3bff-139">This posting generates an inventory receipt of the product, together with an associated BOM and an inventory issue of the products that are included in the BOM.</span></span> <span data-ttu-id="f3bff-140">此库存日记帐类型在不需要工艺路线的简单或大量生产方案中十分有用。</span><span class="sxs-lookup"><span data-stu-id="f3bff-140">This inventory journal type is useful in simple or high-volume production scenarios where routes aren't required.</span></span>

### <a name="item-arrival"></a><span data-ttu-id="f3bff-141">物料到达</span><span class="sxs-lookup"><span data-stu-id="f3bff-141">Item arrival</span></span>

<span data-ttu-id="f3bff-142">您可以使用物料到达日记帐登记物料收货（例如，从采购订单）。</span><span class="sxs-lookup"><span data-stu-id="f3bff-142">You can use the item arrival journal to register the receipt of items (for example, from purchase orders).</span></span> <span data-ttu-id="f3bff-143">可以从**“到达概览”**页上创建到达日记帐，作为到达管理的一部分，也可以手动从**“物料到达”**页创建日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="f3bff-143">An item arrival journal can be created as part of arrival management from the **Arrival overview** page, or you can manually create a journal entry from the **Item arrival** page.</span></span> <span data-ttu-id="f3bff-144">如果您启用物料到达日志名称检查领料库位，Finance and Operations 会查找接收物料的库位，如果存在空间，则会为新进物料生成库位目标。</span><span class="sxs-lookup"><span data-stu-id="f3bff-144">If you enable the item arrival journal name to check for picking locations, Finance and Operations looks for a location for received items and, if there is room, generates location destinations for the incoming items.</span></span>

### <a name="production-input"></a><span data-ttu-id="f3bff-145">生产输入</span><span class="sxs-lookup"><span data-stu-id="f3bff-145">Production input</span></span>

<span data-ttu-id="f3bff-146">生产输入日记帐的工作方式类似于物料到达日记帐，但用于生产订单。</span><span class="sxs-lookup"><span data-stu-id="f3bff-146">Production input journals work like the item arrival journals but are used for production orders.</span></span>

### <a name="counting"></a><span data-ttu-id="f3bff-147">正在盘点</span><span class="sxs-lookup"><span data-stu-id="f3bff-147">Counting</span></span>

<span data-ttu-id="f3bff-148">盘点日记帐能让您纠正为物料或物料组登记的现有库存量，然后过帐实际盘点，因此，您可以进行为对帐差异而需要的调整。</span><span class="sxs-lookup"><span data-stu-id="f3bff-148">Counting journals let you correct the current on-hand inventory that is registered for items or groups of items, and then post the actual physical count, so that you can make the adjustments that are required in order to reconcile the differences.</span></span> <span data-ttu-id="f3bff-149">您可以将盘点策略与盘点组关联，以帮助对具有多种特征的物料进行分组，因此，这些物料可以包括到盘点日记帐中。</span><span class="sxs-lookup"><span data-stu-id="f3bff-149">You can associate counting policies with counting groups to help group items that have various characteristics, so that those items can be included in a counting journal.</span></span> <span data-ttu-id="f3bff-150">例如，您可以设置盘点组以盘点具有特定频率的物料，或在存货下跌到特定级别时盘点物料。</span><span class="sxs-lookup"><span data-stu-id="f3bff-150">For example, you can set up counting groups to count items that have a specific frequency, or to count items when stock falls to a particular level.</span></span> <span data-ttu-id="f3bff-151">有关如何定义盘点组的信息，请参阅[定义库存盘点流程（任务指南）](tasks/define-inventory-counting-processes.md)。</span><span class="sxs-lookup"><span data-stu-id="f3bff-151">For information about how to define counting groups, see [Define inventory counting processes (Task guide)](tasks/define-inventory-counting-processes.md).</span></span>

### <a name="tag-counting"></a><span data-ttu-id="f3bff-152">标签盘点</span><span class="sxs-lookup"><span data-stu-id="f3bff-152">Tag counting</span></span>

<span data-ttu-id="f3bff-153">标签盘点日记帐用于将带编号的标签分配给盘点批次。</span><span class="sxs-lookup"><span data-stu-id="f3bff-153">Tag counting journals are used to assign a numbered tag to a count lot.</span></span> <span data-ttu-id="f3bff-154">标记应包含标记编号、物料编号和物料数量。</span><span class="sxs-lookup"><span data-stu-id="f3bff-154">The tag should contain a tag number, item number, and item quantity.</span></span> <span data-ttu-id="f3bff-155">为了帮助确保标记只使用一次，并且所有标记都被使用，每个物料编号应该有唯一的一组标记，其具有自己的编号规则。</span><span class="sxs-lookup"><span data-stu-id="f3bff-155">To help guarantee that a tag is used only one time, and that all tags are used, every item number should have a unique set of tags that has its own number sequence.</span></span> <span data-ttu-id="f3bff-156">可以为每个标记设置三种状态值：</span><span class="sxs-lookup"><span data-stu-id="f3bff-156">Three status values can be set for each tag:</span></span>

-   <span data-ttu-id="f3bff-157">**已使用** – 为此标签计数物料编号。</span><span class="sxs-lookup"><span data-stu-id="f3bff-157">**Used** – The item number is counted for this tag.</span></span>
-   <span data-ttu-id="f3bff-158">**已失效** – 为此标签使物料编号失效。</span><span class="sxs-lookup"><span data-stu-id="f3bff-158">**Voided** – The item number is voided for this tag.</span></span>
-   <span data-ttu-id="f3bff-159">**缺失** – 此标签缺失物料编号。</span><span class="sxs-lookup"><span data-stu-id="f3bff-159">**Missing** – The item number is missing for this tag.</span></span>

<span data-ttu-id="f3bff-160">过帐标签盘点日记帐时，基于标签盘点日记帐行创建新的盘点日记帐。</span><span class="sxs-lookup"><span data-stu-id="f3bff-160">When you post a tag counting journal, a new counting journal is created, based on the tag counting journal lines.</span></span> <span data-ttu-id="f3bff-161">有关标签盘点的详细信息，请参阅[库存标签盘点](inventory-tag-counting.md)。</span><span class="sxs-lookup"><span data-stu-id="f3bff-161">For more information about tag counting, see [Inventory tag counting](inventory-tag-counting.md).</span></span>

## <a name="working-with-journals"></a><span data-ttu-id="f3bff-162">使用日志</span><span class="sxs-lookup"><span data-stu-id="f3bff-162">Working with journals</span></span>
<span data-ttu-id="f3bff-163">一个用户一次只能访问一个日志。</span><span class="sxs-lookup"><span data-stu-id="f3bff-163">A journal can be accessed by only one user at a time.</span></span> <span data-ttu-id="f3bff-164">如果若干用户必须同时访问日记帐创建日记帐行，则该用户必须选择当前不用于避免覆盖信息。</span><span class="sxs-lookup"><span data-stu-id="f3bff-164">If several users must access journals at the same time to create journal lines, those users must select journals that aren't currently being used, to prevent information from being overwritten.</span></span> <span data-ttu-id="f3bff-165">在多个部门使用同一日记帐类型的情况下，创建多个日记帐名称（例如，每个部门一个）很有用。</span><span class="sxs-lookup"><span data-stu-id="f3bff-165">In situations where multiple departments use the same journal type, it's helpful to create multiple journal names (for example, one per department).</span></span> <span data-ttu-id="f3bff-166">它还可用于划分日记帐，以便每个过帐例程都输入到它自己的唯一库存日记帐中。</span><span class="sxs-lookup"><span data-stu-id="f3bff-166">It can also be helpful to divide journals so that each posting routine is entered in its own unique inventory journal.</span></span> <span data-ttu-id="f3bff-167">对于与库存交易记录相关联的过帐例程，为期间库存调整创建一个日志，为库存盘点创建另一个日志。</span><span class="sxs-lookup"><span data-stu-id="f3bff-167">For posting routines that are associated with inventory transactions, create one journal for periodic inventory adjustments and another for inventory counting.</span></span>

## <a name="posting-journal-lines"></a><span data-ttu-id="f3bff-168">记帐日志行</span><span class="sxs-lookup"><span data-stu-id="f3bff-168">Posting journal lines</span></span>
<span data-ttu-id="f3bff-169">您可以在任何时间过帐您创建的日记帐行，直到您锁定了来自附加交易记录的物料。</span><span class="sxs-lookup"><span data-stu-id="f3bff-169">You can post the journal lines that you create at any time until you've locked an item from additional transactions.</span></span> <span data-ttu-id="f3bff-170">在日记帐中输入的数据保留在该日记帐中，即使您关闭该日记帐而不过帐这些行。</span><span class="sxs-lookup"><span data-stu-id="f3bff-170">The data that you enter in a journal remains in that journal, even if you close the journal without posting the lines.</span></span>

