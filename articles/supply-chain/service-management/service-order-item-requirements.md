---
title: 服务订单物料需求
description: 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e31f58cf8782c715b97bdae0e89f684b15a76d2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215071"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="6c7f0-103">服务订单物料需求</span><span class="sxs-lookup"><span data-stu-id="6c7f0-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c7f0-104">您可以创建服务订单跟踪和管理为您的客户提供的服务。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="6c7f0-105">如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="6c7f0-106">物料需求可以从库存立即消耗，或可以启动生产订单的物料。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="6c7f0-107">通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="6c7f0-108">服务订单创建物料需求通过项目进行处理。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="6c7f0-109">若要在服务订单创建物料需求，必须将服务订单附加到项目。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="6c7f0-110">在为服务订单创建某一物料需求后，就可以从单独服务订单中的**项目**或通过**销售订单**窗体查看该物料需求。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="6c7f0-111">从服务订单查看物料需求</span><span class="sxs-lookup"><span data-stu-id="6c7f0-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="6c7f0-112">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6c7f0-113">单击**发货**，然后单击**物料需求**打开**物料需求**窗体。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="6c7f0-114">单击**项目**选项卡，然后检查**服务订单**字段以查看物料需求的服务订单。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="6c7f0-115">删除具有物料需求的服务订单</span><span class="sxs-lookup"><span data-stu-id="6c7f0-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="6c7f0-116">如果针对某一服务订单创建物料需求，则不能删除该服务订单。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="6c7f0-117">您必须首先删除物料需求，然后才能删除该服务订单。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="6c7f0-118">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6c7f0-119">单击**发货**，然后单击**物料需求**打开**物料需求**窗体。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="6c7f0-120">此窗体将列出在该服务订单上创建的物料需求。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="6c7f0-121">选择适当的物料需求行来删除，然后单击**删除**。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="6c7f0-122">–或–</span><span class="sxs-lookup"><span data-stu-id="6c7f0-122">–or–</span></span>

1.  <span data-ttu-id="6c7f0-123">单击**项目管理与核算** \> **通用** \> **项目** \> **所有项目**。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="6c7f0-124">打开具有创建了物料需求的服务订单的项目。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="6c7f0-125">在**项目**窗体中，在右边的窗格，单击**物料需求** 。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="6c7f0-126">**物料需求**窗体将打开，窗体中将列出与所选项目相关联的物料需求。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="6c7f0-127">选择适当的物料需求行来删除，然后单击**删除**。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c7f0-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c7f0-128">See also</span></span>

<span data-ttu-id="6c7f0-129">[物料需求（窗体）](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="6c7f0-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

