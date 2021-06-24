---
title: 库存库位
description: 库存库位用于与基本仓库 (WMS I) 一同确定物料的存储位置和从 WMS I 仓库领取物料的位置。
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8d5459e37b5827b6a2ff07c892c2ff25b76ecd6
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187474"
---
# <a name="inventory-locations"></a><span data-ttu-id="dea31-103">库存库位</span><span class="sxs-lookup"><span data-stu-id="dea31-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dea31-104">库存库位用于与基本仓库 (WMS I) 一同确定物料的存储位置和从 WMS I 仓库领取物料的位置。</span><span class="sxs-lookup"><span data-stu-id="dea31-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="dea31-105">此主题适用于库存管理模块中的功能。</span><span class="sxs-lookup"><span data-stu-id="dea31-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="dea31-106">它不适用于仓库管理模块中的功能。</span><span class="sxs-lookup"><span data-stu-id="dea31-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="dea31-107">术语库位表示提取物料的位置。</span><span class="sxs-lookup"><span data-stu-id="dea31-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="dea31-108">对于每个库位，还可以指定插入物料的位置。</span><span class="sxs-lookup"><span data-stu-id="dea31-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="dea31-109">在默认情况下，它们是相同的。</span><span class="sxs-lookup"><span data-stu-id="dea31-109">By default, they are the same.</span></span> <span data-ttu-id="dea31-110">通常从库位的同一侧插入和提取物料，但并非始终如此。</span><span class="sxs-lookup"><span data-stu-id="dea31-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="dea31-111">例如，保存在鲜活物品货架上的物料从一个通道插入而从另一个通道提取。</span><span class="sxs-lookup"><span data-stu-id="dea31-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="dea31-112">主要输入由库存名称给定，该库存名称通常由其坐标（仓库、通道、货架、货位和箱）确定。</span><span class="sxs-lookup"><span data-stu-id="dea31-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="dea31-113">例如，在“库存库位”页中，01-02-03-4 表示通道 1、货架 2、货位 3、储料箱 4。</span><span class="sxs-lookup"><span data-stu-id="dea31-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="dea31-114">库位属性</span><span class="sxs-lookup"><span data-stu-id="dea31-114">Location properties</span></span>

<span data-ttu-id="dea31-115">库位具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="dea31-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="dea31-116">尺寸（高度、宽度、深度和体积）</span><span class="sxs-lookup"><span data-stu-id="dea31-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="dea31-117">仓库、通道、货架、货位和箱位置</span><span class="sxs-lookup"><span data-stu-id="dea31-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="dea31-118">库位类型（堆放库位、领料库位、进货台、出货台、生产输入位置、检查库位或看板超市）</span><span class="sxs-lookup"><span data-stu-id="dea31-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="dea31-119">可以在联机系统中使用检查文本以验证操作员为特定物料选择了正确的库位。</span><span class="sxs-lookup"><span data-stu-id="dea31-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="dea31-120">此检查文本可以手动创建，也可以采用默认值。</span><span class="sxs-lookup"><span data-stu-id="dea31-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="dea31-121">排序代码</span><span class="sxs-lookup"><span data-stu-id="dea31-121">Sort codes</span></span>
<span data-ttu-id="dea31-122">使用分类代码优化领料单的处理，领料单介绍了库存中的领取物料以及领料订单所需的信息。</span><span class="sxs-lookup"><span data-stu-id="dea31-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="dea31-123">可以按通道和其他坐标指定分类代码，或者将它们手动分配给库位。</span><span class="sxs-lookup"><span data-stu-id="dea31-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="dea31-124">锁定的库位</span><span class="sxs-lookup"><span data-stu-id="dea31-124">Blocked locations</span></span>
<span data-ttu-id="dea31-125">有时，您可能想要指示库位锁定一段时间，例如在进行修理时。</span><span class="sxs-lookup"><span data-stu-id="dea31-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="dea31-126">有时，您可能希望指示只锁定输入或输出。</span><span class="sxs-lookup"><span data-stu-id="dea31-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="dea31-127">树状结构</span><span class="sxs-lookup"><span data-stu-id="dea31-127">Tree structure</span></span>

<span data-ttu-id="dea31-128">在“库存库位”页，您可以以基于库存库位坐标的树状结构，以定义的显示格式查看仓库布局。</span><span class="sxs-lookup"><span data-stu-id="dea31-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="dea31-129">通过仓库窗体维护库存库位</span><span class="sxs-lookup"><span data-stu-id="dea31-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="dea31-130">可以通过向导将库位从一个仓库复制到另一个以及创建库位。</span><span class="sxs-lookup"><span data-stu-id="dea31-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="dea31-131">在运行向导之前，应确保您在“仓库”页已定义了默认库位名称。</span><span class="sxs-lookup"><span data-stu-id="dea31-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="dea31-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="dea31-132">Additional resources</span></span>

[<span data-ttu-id="dea31-133">创建新仓库布局</span><span class="sxs-lookup"><span data-stu-id="dea31-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]