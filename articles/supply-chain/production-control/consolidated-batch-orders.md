---
title: "合并的批次订单"
description: "本文介绍合并的批次订单的概念。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="135b5-103">合并的批次订单</span><span class="sxs-lookup"><span data-stu-id="135b5-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="135b5-104">本文介绍合并的批次订单的概念。</span><span class="sxs-lookup"><span data-stu-id="135b5-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="135b5-105">生产的散装物料被视为父物料，而包装的物料被视为子物料。</span><span class="sxs-lookup"><span data-stu-id="135b5-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="135b5-106">散装物料和包装物料之间的关系以散装物料转换表示。</span><span class="sxs-lookup"><span data-stu-id="135b5-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="135b5-107">此散装物料转换在散装物料本身上定义。</span><span class="sxs-lookup"><span data-stu-id="135b5-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="135b5-108">包装的物料可包装到被视为一个单位的单个大小或多个大小的容器中。</span><span class="sxs-lookup"><span data-stu-id="135b5-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="135b5-109">通过合并散装物料的订单，您可以在单个视图中查看所有相关的批次订单，这些订单可帮助您确定任何必须完成的剩余工作。</span><span class="sxs-lookup"><span data-stu-id="135b5-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="135b5-110">合并的批次订单可以包含以下订单的任意组合：</span><span class="sxs-lookup"><span data-stu-id="135b5-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="135b5-111">单个散装物料订单和多个包装物料订单</span><span class="sxs-lookup"><span data-stu-id="135b5-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="135b5-112">多个散装物料订单和多个包装物料订单</span><span class="sxs-lookup"><span data-stu-id="135b5-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="135b5-113">多个散装物料订单和单个包装物料订单</span><span class="sxs-lookup"><span data-stu-id="135b5-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="135b5-114">仅包装物料订单</span><span class="sxs-lookup"><span data-stu-id="135b5-114">Only packed orders</span></span>





