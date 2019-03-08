---
title: 为销售订单预留相同批次
description: 本文说明如何设置产品以对照单个库存批次预留库存。
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6089d07b0f8bc1a36703b5b1c2f24af72770d5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "309533"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="444e6-103">为销售订单预留相同批次</span><span class="sxs-lookup"><span data-stu-id="444e6-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="444e6-104">本文说明如何设置产品以对照单个库存批次预留库存。</span><span class="sxs-lookup"><span data-stu-id="444e6-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="444e6-105">相同批次预留可让您针对一批库存为销售订单行保留库存。</span><span class="sxs-lookup"><span data-stu-id="444e6-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="444e6-106">例如，订购墙纸的客户可以请求通过同一批次为整个订单供货，以避免各卷墙纸之间出现不一致的情况。</span><span class="sxs-lookup"><span data-stu-id="444e6-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="444e6-107">要将产品设置为使用相同的批次预留，以下设置必须在分配给产品的物料模型组、跟踪维度组和存储维度组中有效：</span><span class="sxs-lookup"><span data-stu-id="444e6-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="444e6-108">**物料模型组** - 物料模型组必须为库存策略选择**预留**字段组中的**相同批次选择**和**合并要求**字段。</span><span class="sxs-lookup"><span data-stu-id="444e6-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="444e6-109">**跟踪维度组** - 跟踪维度组必须为批号选择**按维度的覆盖范围计划**字段。</span><span class="sxs-lookup"><span data-stu-id="444e6-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="444e6-110">**存储维度组** - 存储维度组必须为**站点**和**仓库**选择**按维度的覆盖范围计划**字段。</span><span class="sxs-lookup"><span data-stu-id="444e6-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="444e6-111">如果在为相同批次选择设置的销售订单行上的产品预留库存，则 Microsoft Dynamics 365 for Finance and Operations 会尝试预留单个库存批次中订购的数量。</span><span class="sxs-lookup"><span data-stu-id="444e6-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="444e6-112">还应考虑任何特定的批属性要求。</span><span class="sxs-lookup"><span data-stu-id="444e6-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="444e6-113">如果无法从单个批次中填满数量，则将显示**相同批次预留冲突**页面。</span><span class="sxs-lookup"><span data-stu-id="444e6-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="444e6-114">此页面描述了这些问题以及为继续预留而采取的措施。</span><span class="sxs-lookup"><span data-stu-id="444e6-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="444e6-115">以下条件可能会阻止预留批次：</span><span class="sxs-lookup"><span data-stu-id="444e6-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="444e6-116">批处置代码将销售的**阻止预留**标记为**已阻止**。</span><span class="sxs-lookup"><span data-stu-id="444e6-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="444e6-117">根据到期日期以及任何适用的客户适售期，该批次已经到期。</span><span class="sxs-lookup"><span data-stu-id="444e6-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="444e6-118">如果物料的物料模型组受先过期先出 (FEFO) 日期控制并且已选择最佳使用日期作为选择标准，则仍可考虑预留该物料。</span><span class="sxs-lookup"><span data-stu-id="444e6-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="444e6-119">根据到期日期和最佳使用日期以及任何客户适售期，该批次的保质期剩余天数不足。</span><span class="sxs-lookup"><span data-stu-id="444e6-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>




