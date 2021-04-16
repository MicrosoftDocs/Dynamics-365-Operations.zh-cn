---
title: 部分预留的转移单批发布
description: 此主题描述如何从移动设备设置和应用部分预留的转移单批发布。
author: pjacobse
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7802fe379941b915450b7c60c1187187038c95f2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837505"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="db76d-103">部分预留的转移单批发布</span><span class="sxs-lookup"><span data-stu-id="db76d-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db76d-104">通过部分预留的转移单批发布功能可以使用批处理作业将转移单部分发布到仓库。</span><span class="sxs-lookup"><span data-stu-id="db76d-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="db76d-105">由于您可以选择发布部分数量，因此您无需等到全部订单数量在仓库中可用后再发布订单。</span><span class="sxs-lookup"><span data-stu-id="db76d-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="db76d-106">将订单发布到仓库是一项高级仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="db76d-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="db76d-107">此流程包括仓库工作人员使用移动设备可以执行的活动，如领料、包装和装运。</span><span class="sxs-lookup"><span data-stu-id="db76d-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="db76d-108">适用情况</span><span class="sxs-lookup"><span data-stu-id="db76d-108">Where it applies</span></span>

<span data-ttu-id="db76d-109">通过此功能可以使用批处理作业将转移单发布到仓库。</span><span class="sxs-lookup"><span data-stu-id="db76d-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="db76d-110">当仓库中没有足够的库存，但您仍然想要将一个仓库的物料转移到另一个仓库时，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="db76d-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="db76d-111">如何设置</span><span class="sxs-lookup"><span data-stu-id="db76d-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="db76d-112">指定转移单和销售订单的履行条件</span><span class="sxs-lookup"><span data-stu-id="db76d-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="db76d-113">可以在批处理中将订单部分发布到仓库前，必须满足履行条件。</span><span class="sxs-lookup"><span data-stu-id="db76d-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="db76d-114">这些履行条件由履行策略确定。</span><span class="sxs-lookup"><span data-stu-id="db76d-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="db76d-115">转移单和销售订单的履行策略在公司级别指定。</span><span class="sxs-lookup"><span data-stu-id="db76d-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="db76d-116">根据履行策略的设置，批发布订单将被接受或拒绝。</span><span class="sxs-lookup"><span data-stu-id="db76d-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="db76d-117">然后对订单进行相应的处理。</span><span class="sxs-lookup"><span data-stu-id="db76d-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="db76d-118">若要为转移单和销售订单创建履行策略，请单击 **仓库管理** \> **设置** \> **发放到仓库** \> **履行策略**，然后通过输入名称和描述创建履行策略。</span><span class="sxs-lookup"><span data-stu-id="db76d-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="db76d-119">若要指定履行费率、值类型和违反履行策略时要显示的消息，请单击 **仓库管理** \> **设置** \> **发放到仓库** \> **履行策略**，然后设置 **履行费率**、**值类型** 和 **履行违反消息** 字段。</span><span class="sxs-lookup"><span data-stu-id="db76d-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="db76d-120">设置转移单和销售订单的履行策略</span><span class="sxs-lookup"><span data-stu-id="db76d-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="db76d-121">若要设置转移单的履行策略，请单击 **库存管理** \> **设置** \>**库存和仓库管理参数** \> **转移单** \> **仓库管理**，然后选择转移单履行策略。</span><span class="sxs-lookup"><span data-stu-id="db76d-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="db76d-122">若要设置销售订单的履行策略，请单击 **应收账款** \> **设置**\> **应收账款参数** \> **仓库管理**，然后选择销售订单履行策略。</span><span class="sxs-lookup"><span data-stu-id="db76d-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="db76d-123">允许批发布并指定应批发布的数量。</span><span class="sxs-lookup"><span data-stu-id="db76d-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="db76d-124">批处理作业用于在批处理中将订单发布到仓库。</span><span class="sxs-lookup"><span data-stu-id="db76d-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="db76d-125">用于区分应在批处理作业中运行的订单的参数在批处理作业本身上进行设置。</span><span class="sxs-lookup"><span data-stu-id="db76d-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="db76d-126">**数量** 参数指定是否应批发布全部数量或实际预留的数量。</span><span class="sxs-lookup"><span data-stu-id="db76d-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="db76d-127">**允许发布已部分发放的订单** 参数确定批处理中的订单在提前部分发放时是否应接受或拒绝。</span><span class="sxs-lookup"><span data-stu-id="db76d-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="db76d-128">若要设置转移单的 **数量** 和 **允许发布已部分发放的订单** 参数，请单击 **仓库管理** \> **发放到仓库** \> **自动发放转移单**。</span><span class="sxs-lookup"><span data-stu-id="db76d-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="db76d-129">若要设置销售订单的 **数量** 和 **允许发布已部分发放的订单** 参数，请单击 **仓库管理** \> **发放到仓库** \> **自动发放销售订单**。</span><span class="sxs-lookup"><span data-stu-id="db76d-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]