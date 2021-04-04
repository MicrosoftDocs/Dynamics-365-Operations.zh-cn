---
title: 云和边缘缩放单元的仓库订单
description: 本主题提供有关仓库订单功能的信息，它是仓库缩放单元工作负荷的一部分。
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9102f53ab1b63d08b8bba7b0ae505416ec5a83fd
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556354"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="2d31c-103">云和边缘缩放单元的仓库订单</span><span class="sxs-lookup"><span data-stu-id="2d31c-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="2d31c-104">当使用缩放单元工作负荷时，并非所有业务功能都在公开预览版中完全受支持。</span><span class="sxs-lookup"><span data-stu-id="2d31c-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="2d31c-105">如果您使用的是缩放单元，请确保仅使用本主题明确描述为受支持的那些流程。</span><span class="sxs-lookup"><span data-stu-id="2d31c-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="2d31c-106">什么是仓库订单？</span><span class="sxs-lookup"><span data-stu-id="2d31c-106">What are warehouse orders?</span></span>

<span data-ttu-id="2d31c-107">*仓库订单* 是为支持中心和缩放单元仓库部署而创建的一种订单。</span><span class="sxs-lookup"><span data-stu-id="2d31c-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="2d31c-108">当您在缩放单元上运行仓库工作负荷时，您可以使用它们来接收库存。</span><span class="sxs-lookup"><span data-stu-id="2d31c-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="2d31c-109">它们当前只能与采购订单一起使用。</span><span class="sxs-lookup"><span data-stu-id="2d31c-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="2d31c-110">仓库订单用作仓库管理处理的一部分，如在处理入站采购订单期间使用仓库应用登记实际现有库存时。</span><span class="sxs-lookup"><span data-stu-id="2d31c-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="2d31c-111">仓库订单的创建是 *发放到仓库* 流程的一部分，可用于指定缩放单位仓库的采购订单，以及为使用仓库管理流程启用的项目。</span><span class="sxs-lookup"><span data-stu-id="2d31c-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d31c-112">仓库订单仅在将[仓库管理工作负荷用于云和边缘缩放单元](cloud-edge-workload-warehousing.md)的部署中可用。</span><span class="sxs-lookup"><span data-stu-id="2d31c-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="2d31c-113">创建仓库订单</span><span class="sxs-lookup"><span data-stu-id="2d31c-113">Create a warehouse order</span></span>

<span data-ttu-id="2d31c-114">要创建仓库订单，请按照下面的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d31c-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="2d31c-115">登录到在中心运行的 Microsoft Dynamics 365 Supply Chain Management 的实例。</span><span class="sxs-lookup"><span data-stu-id="2d31c-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="2d31c-116">（在中心登录后，您必须启动 *发放到仓库* 流程。）</span><span class="sxs-lookup"><span data-stu-id="2d31c-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="2d31c-117">转到 **采购 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="2d31c-118">在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="2d31c-119">要查看相关的仓库订单行，打开相关的采购订单，在 **采购订单行** 部分选择行，然后在工具栏上选择 **仓库 \> 仓库订单行**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="2d31c-120">要查看所有行，转到 **仓库管理 \> 查询和报表 \> 仓库订单行**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="2d31c-121">您也可以通过转到 **仓库管理 > 发放到仓库 > 自动下达采购订单**，从批处理作业触发 *发放到仓库* 流程。</span><span class="sxs-lookup"><span data-stu-id="2d31c-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="2d31c-122">设置批处理作业时，您可以根据查询选择特定的采购订单行。</span><span class="sxs-lookup"><span data-stu-id="2d31c-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="2d31c-123">一个典型的方案是设置一个重复批处理作业，来发放所有预期在第二天到达的已确认采购订单行。</span><span class="sxs-lookup"><span data-stu-id="2d31c-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="2d31c-124">取消仓库订单</span><span class="sxs-lookup"><span data-stu-id="2d31c-124">Cancel a warehouse order</span></span>

<span data-ttu-id="2d31c-125">作为 *发放到仓库* 流程的一部分，采购订单库存交易将链接到仓库订单，并被中心锁定以免更新。</span><span class="sxs-lookup"><span data-stu-id="2d31c-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="2d31c-126">如果您错误地发放到仓库，或者有其他原因要撤消仓库订单行的创建，可以请求取消仓库订单行。</span><span class="sxs-lookup"><span data-stu-id="2d31c-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="2d31c-127">要取消仓库订单行，请按照下面的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d31c-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="2d31c-128">登录到在中心运行的 Supply Chain Management 实例。</span><span class="sxs-lookup"><span data-stu-id="2d31c-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="2d31c-129">转到 **仓库管理 \> 查询和报表 \> 仓库订单行**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="2d31c-130">选择相关行。</span><span class="sxs-lookup"><span data-stu-id="2d31c-130">Select the relevant line.</span></span>
1. <span data-ttu-id="2d31c-131">在操作窗格上，选择 **取消仓库订单行**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="2d31c-132">对于任何已经在等待取消或正在缩放单元上运行工作负荷的仓库中处理的行，取消行请求都将被拒绝。</span><span class="sxs-lookup"><span data-stu-id="2d31c-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="2d31c-133">监视仓库订单</span><span class="sxs-lookup"><span data-stu-id="2d31c-133">Monitor a warehouse order</span></span>

<span data-ttu-id="2d31c-134">在 **仓库订单行** 视图中，您可以通过查看 **要接收的剩余数量** 列中的值来监视入站接收的进度。</span><span class="sxs-lookup"><span data-stu-id="2d31c-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="2d31c-135">要查看与使用仓库应用完成的工作相关的详细信息，请执行以下步骤之一。</span><span class="sxs-lookup"><span data-stu-id="2d31c-135">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="2d31c-136">转到 **仓库管理 \> 查询和报表 \> 仓库订单行**，使用筛选器查找您要查找的行。</span><span class="sxs-lookup"><span data-stu-id="2d31c-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="2d31c-137">转到 **采购 \> 采购订单 \> 所有采购订单**，打开相关的采购订单。</span><span class="sxs-lookup"><span data-stu-id="2d31c-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="2d31c-138">在 **采购订单行** 部分，选择一个或多个行，然后在工具栏上选择 **仓库 \> 仓库收货条目**。</span><span class="sxs-lookup"><span data-stu-id="2d31c-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]