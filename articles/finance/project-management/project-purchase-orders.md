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
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174550"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="d0f67-104">项目的采购订单</span><span class="sxs-lookup"><span data-stu-id="d0f67-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0f67-105">本文介绍您可用于为项目创建采购订单的不同方法。</span><span class="sxs-lookup"><span data-stu-id="d0f67-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="d0f67-106">使用的方法取决于当消耗采购物料和将采购物料费用计入项目时，采购订单的用途。</span><span class="sxs-lookup"><span data-stu-id="d0f67-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="d0f67-107">创建采购订单的方法</span><span class="sxs-lookup"><span data-stu-id="d0f67-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="d0f67-108">您可以使用以下方法之一在“项目”管理与核算中创建一个采购订单。</span><span class="sxs-lookup"><span data-stu-id="d0f67-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="d0f67-109">采购订单的目的是确定采购订单的消耗时间，并随之确定对项目物料计费的时间。</span><span class="sxs-lookup"><span data-stu-id="d0f67-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0f67-110">方法</span><span class="sxs-lookup"><span data-stu-id="d0f67-110">Method</span></span></th>
<th><span data-ttu-id="d0f67-111">用途</span><span class="sxs-lookup"><span data-stu-id="d0f67-111">Purpose</span></span></th>
<th><span data-ttu-id="d0f67-112">物料的消耗</span><span class="sxs-lookup"><span data-stu-id="d0f67-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0f67-113">直接从项目创建采购订单</span><span class="sxs-lookup"><span data-stu-id="d0f67-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="d0f67-114">使用此方法以针对项目的消耗量从外部供应商采购物料。</span><span class="sxs-lookup"><span data-stu-id="d0f67-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="d0f67-115">可以通过两种方法创建采购订单：</span><span class="sxs-lookup"><span data-stu-id="d0f67-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="d0f67-116">从项目本身出发。</span><span class="sxs-lookup"><span data-stu-id="d0f67-116">From the project itself.</span></span> <span data-ttu-id="d0f67-117">在这种情况下，已经为采购订单定义项目。</span><span class="sxs-lookup"><span data-stu-id="d0f67-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="d0f67-118">通过导航到项目采购订单。</span><span class="sxs-lookup"><span data-stu-id="d0f67-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="d0f67-119">您必须选择要为其创建采购订单的供应商和项目。</span><span class="sxs-lookup"><span data-stu-id="d0f67-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="d0f67-120">更新供应商发票时消耗物料。</span><span class="sxs-lookup"><span data-stu-id="d0f67-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0f67-121">根据销售订单创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="d0f67-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="d0f67-122">如果您从项目创建销售订单，可以使用此方法采购物料。</span><span class="sxs-lookup"><span data-stu-id="d0f67-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="d0f67-123">为客户的销售订单开票后消耗物料。</span><span class="sxs-lookup"><span data-stu-id="d0f67-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0f67-124">根据物料需求创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="d0f67-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="d0f67-125">如果您从项目创建物料需求，可以使用此方法采购物料。</span><span class="sxs-lookup"><span data-stu-id="d0f67-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="d0f67-126">更新物料需求装箱单时消耗物料。</span><span class="sxs-lookup"><span data-stu-id="d0f67-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="d0f67-127">更新供应商发票或装箱单时，系统将提示您根据物料需求更新该装箱单。</span><span class="sxs-lookup"><span data-stu-id="d0f67-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="d0f67-128">有关详细信息，请参阅[根据物料需求接收采购订单上的物料](tasks/receive-items-purchase-order-item-requirement.md)。</span><span class="sxs-lookup"><span data-stu-id="d0f67-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

