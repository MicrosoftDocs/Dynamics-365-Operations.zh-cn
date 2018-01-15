---
title: "使用中心合并计划装载量"
description: "本文介绍当您从其他仓库将货物交付给同一客户，或将多个供应商的货物接收到同一个仓库时，在枢纽合并装运的功能。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 577204b49355a470769237eb46ad74e7f319a55e
ms.openlocfilehash: 3920bf73c51e8310c8b44bd42a4b185f6dc8ed3e
ms.contentlocale: zh-cn
ms.lasthandoff: 01/15/2018

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="a705b-103">使用中心合并计划装载量</span><span class="sxs-lookup"><span data-stu-id="a705b-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a705b-104">本文介绍当您从其他仓库将货物交付给同一客户，或将多个供应商的货物接收到同一个仓库时，在枢纽合并装运的功能。</span><span class="sxs-lookup"><span data-stu-id="a705b-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="a705b-105">当您从其他仓库将货物交付给同一客户，或货物从多个供应商交货到同一个仓库时，它对于合并枢纽的装运非常有用。</span><span class="sxs-lookup"><span data-stu-id="a705b-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="a705b-106">构建负荷</span><span class="sxs-lookup"><span data-stu-id="a705b-106">Building loads</span></span>
<span data-ttu-id="a705b-107">您必须先启用**运输管理参数**页的**在途计划**选项，才能够使用枢纽合并。</span><span class="sxs-lookup"><span data-stu-id="a705b-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="a705b-108">您还必须创建将发生合并的枢纽。</span><span class="sxs-lookup"><span data-stu-id="a705b-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="a705b-109">下图显示枢纽合并的示例。</span><span class="sxs-lookup"><span data-stu-id="a705b-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="a705b-110">在这种情况下，不同仓库的销售订单前往同一个客户。</span><span class="sxs-lookup"><span data-stu-id="a705b-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="a705b-111">基本负荷基于销售订单以通常的方式创建，通过使用**装载计划工作台**页。</span><span class="sxs-lookup"><span data-stu-id="a705b-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="a705b-112">若要在将负荷交付给客户前合并枢纽的两个负荷，在**装载计划工作台**页，在**运输**字段中，选择**枢纽合并**。</span><span class="sxs-lookup"><span data-stu-id="a705b-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="a705b-113">在选择每个负荷的正确枢纽时，负荷将枢纽作为“邮寄”目的地。</span><span class="sxs-lookup"><span data-stu-id="a705b-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="a705b-114">您还将在**装载计划工作台**页的**供应和需求**部分有两个“运输请求行”。</span><span class="sxs-lookup"><span data-stu-id="a705b-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="a705b-115">然后可以为新的负荷添加这两个行。</span><span class="sxs-lookup"><span data-stu-id="a705b-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="a705b-116">此新的负荷将具有两个销售订单行，并且还将枢纽作为“取件”地址，以及将客户 A 作为“邮寄”目的地。</span><span class="sxs-lookup"><span data-stu-id="a705b-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="a705b-117">然后三个负荷准备好进行评价和路由，像任何其他负荷一样。</span><span class="sxs-lookup"><span data-stu-id="a705b-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="a705b-118">您可以选择系统为每个负荷建议的任何装运承运人。</span><span class="sxs-lookup"><span data-stu-id="a705b-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="a705b-119">[![集中整合](./media/hubconsol.jpg)](./media/hubconsol.jpg) 您还可以使用相同的方法来合并多个转移单的负荷。</span><span class="sxs-lookup"><span data-stu-id="a705b-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="a705b-120">在这种情况下，上图中的客户 A 是一仓库。</span><span class="sxs-lookup"><span data-stu-id="a705b-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="a705b-121">或者，您可以合并多个采购订单的负荷，其中将不同供应商的负荷交付到同一仓库。</span><span class="sxs-lookup"><span data-stu-id="a705b-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="a705b-122">可以有多个合并枢纽，并可以在多个枢纽合并更多来自不同仓库的负荷。</span><span class="sxs-lookup"><span data-stu-id="a705b-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="a705b-123">构建基本负荷并使用枢纽合并选项后，您使用合并的运输请求行构建新的负荷。</span><span class="sxs-lookup"><span data-stu-id="a705b-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="a705b-124">然后评价并路由负荷。</span><span class="sxs-lookup"><span data-stu-id="a705b-124">You then rate and route your loads.</span></span>




