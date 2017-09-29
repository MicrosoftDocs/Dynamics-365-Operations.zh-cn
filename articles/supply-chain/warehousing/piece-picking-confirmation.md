---
title: "单件领料确认"
description: "此主题描述如何从移动设备设置和应用单件领料确认。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 62b637b81a522c353067248deea79cfbf98518e9
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="piece-picking-confirmation"></a><span data-ttu-id="7ed8d-103">单件领料确认</span><span class="sxs-lookup"><span data-stu-id="7ed8d-103">Piece picking confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7ed8d-104">单件领料允许您通过移动设备上的领料或盘点工作确认单件库存。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="7ed8d-105">对于领料，您可以确认在对要领料的工作指定的数量范围内的待处理工作的数量。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="7ed8d-106">对于盘点工作，您可以扫描您正在盘点的库存和跟踪总金额。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="7ed8d-107">启用单件领料后，将自动选择产品确认。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="7ed8d-108">对于工作类型的领料，启用最大件数。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="7ed8d-109">这允许您将最大数量设置为在工作流程中必须确认的件数。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="7ed8d-110">最大数量基于当前正在处理的工作单位。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="7ed8d-111">盘点工作类型不允许最大数量。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="7ed8d-112">您还可以使用与一个扫描的条码关联的数量和度量单位 (UOM)。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="7ed8d-113">这适用于接收进货流，包括混合牌照接收、采购订单物料、转移单和加载物料。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="7ed8d-114">它还适用于通过扫描条码可将数量添加到在条码上的 UOM 和工作单位之间转换的已确认总件数的单件领料。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="7ed8d-115">如果在盘点条码上的 UOM 时确认对序列组上的盘点允许该数量，则该数量将被添加到总计数。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="7ed8d-116">适用情况</span><span class="sxs-lookup"><span data-stu-id="7ed8d-116">Where it applies</span></span>

<span data-ttu-id="7ed8d-117">单件领料可用于所有盘点工作和任何工作类型的初始领料。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="7ed8d-118">单件领料不适用于物料受序列号控制或从牌照 (LP) 库位领取生产或看板且将物料设置为暂存的情况。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="7ed8d-119">设置单件领料</span><span class="sxs-lookup"><span data-stu-id="7ed8d-119">Set up piece picking</span></span>

1.  <span data-ttu-id="7ed8d-120">在移动设备菜单项上，打开工作确认的设置窗体：仓库管理 > **仓库管理** > **设置** > **移动设备** > **移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="7ed8d-121">从移动设备菜单项打开工作确认设置。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="7ed8d-122">当工作类型为领料或盘点时，以下选项可供选择。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-122">The following options become available for selection when the work type is pick or counting.</span></span>

| <span data-ttu-id="7ed8d-123">选项</span><span class="sxs-lookup"><span data-stu-id="7ed8d-123">Option</span></span>        | <span data-ttu-id="7ed8d-124">说明</span><span class="sxs-lookup"><span data-stu-id="7ed8d-124">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="7ed8d-125">单件领料确认</span><span class="sxs-lookup"><span data-stu-id="7ed8d-125">Piece picking confirmation</span></span>   | <span data-ttu-id="7ed8d-126">可用于领料和盘点工作类型。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-126">Available for pick and counting work types.</span></span> <span data-ttu-id="7ed8d-127">自动选择产品确认。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="7ed8d-128">允许您从移动设备确认每件库存。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> | 
| <span data-ttu-id="7ed8d-129">最大件数</span><span class="sxs-lookup"><span data-stu-id="7ed8d-129">Maximum number of pieces</span></span>     | <span data-ttu-id="7ed8d-130">如果启用单件领料确认，可用于领料工作。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="7ed8d-131">设置您必须确认的件数限制。</span><span class="sxs-lookup"><span data-stu-id="7ed8d-131">Sets a limit to the number of pieces that you must confirm.</span></span> |  

