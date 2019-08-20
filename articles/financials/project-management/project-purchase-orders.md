---
title: 项目的采购订单
description: 本文介绍您可用于为项目创建采购订单的不同方法。 使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 971a4ea0abac43c160d8a6f46f385cbfc5134ffd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838863"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="d5de3-104">项目的采购订单</span><span class="sxs-lookup"><span data-stu-id="d5de3-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5de3-105">本文介绍您可用于为项目创建采购订单的不同方法。</span><span class="sxs-lookup"><span data-stu-id="d5de3-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="d5de3-106">使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。</span><span class="sxs-lookup"><span data-stu-id="d5de3-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="d5de3-107">在 Microsoft Dynamics 365 for Finance and Operations 中，您可以使用多种方法创建项目的采购订单。</span><span class="sxs-lookup"><span data-stu-id="d5de3-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="d5de3-108">使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。</span><span class="sxs-lookup"><span data-stu-id="d5de3-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="d5de3-109">创建采购订单的方法</span><span class="sxs-lookup"><span data-stu-id="d5de3-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="d5de3-110">您可以使用以下方法之一在“项目”管理与核算中创建一个采购订单。</span><span class="sxs-lookup"><span data-stu-id="d5de3-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="d5de3-111">采购订单的目的是确定采购订单的消耗时间，并随之确定对项目物料计费的时间。</span><span class="sxs-lookup"><span data-stu-id="d5de3-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5de3-112">方法</span><span class="sxs-lookup"><span data-stu-id="d5de3-112">Method</span></span></th>
<th><span data-ttu-id="d5de3-113">用途</span><span class="sxs-lookup"><span data-stu-id="d5de3-113">Purpose</span></span></th>
<th><span data-ttu-id="d5de3-114">物料的消耗</span><span class="sxs-lookup"><span data-stu-id="d5de3-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5de3-115">直接从项目创建采购订单</span><span class="sxs-lookup"><span data-stu-id="d5de3-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="d5de3-116">使用此方法以针对项目的消耗量从外部供应商采购物料。</span><span class="sxs-lookup"><span data-stu-id="d5de3-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="d5de3-117">可以通过两种方法创建采购订单：</span><span class="sxs-lookup"><span data-stu-id="d5de3-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="d5de3-118">从项目本身出发。</span><span class="sxs-lookup"><span data-stu-id="d5de3-118">From the project itself.</span></span> <span data-ttu-id="d5de3-119">在这种情况下，已经为采购订单定义项目。</span><span class="sxs-lookup"><span data-stu-id="d5de3-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="d5de3-120">通过导航到项目采购订单。</span><span class="sxs-lookup"><span data-stu-id="d5de3-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="d5de3-121">您必须选择要为其创建采购订单的供应商和项目。</span><span class="sxs-lookup"><span data-stu-id="d5de3-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="d5de3-122">更新供应商发票时消耗物料。</span><span class="sxs-lookup"><span data-stu-id="d5de3-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5de3-123">根据销售订单创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="d5de3-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="d5de3-124">如果您从项目创建销售订单，可以使用此方法采购物料。</span><span class="sxs-lookup"><span data-stu-id="d5de3-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="d5de3-125">为客户的销售订单开票后消耗物料。</span><span class="sxs-lookup"><span data-stu-id="d5de3-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5de3-126">根据物料需求创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="d5de3-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="d5de3-127">如果您从项目创建物料需求，可以使用此方法采购物料。</span><span class="sxs-lookup"><span data-stu-id="d5de3-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="d5de3-128">更新物料需求装箱单时消耗物料。</span><span class="sxs-lookup"><span data-stu-id="d5de3-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="d5de3-129">更新供应商发票或装箱单时，系统将提示您根据物料需求更新该装箱单。</span><span class="sxs-lookup"><span data-stu-id="d5de3-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="d5de3-130">有关详细信息，请参阅[根据物料需求接收采购订单上的物料](tasks/receive-items-purchase-order-item-requirement.md)。</span><span class="sxs-lookup"><span data-stu-id="d5de3-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

