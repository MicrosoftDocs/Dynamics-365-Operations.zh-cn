---
title: 通过仓库应用进行的牌照收货
description: 此主题介绍如何设置仓库应用以支持使用牌照收货流程接收实际库存。
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 60e69fd62d6d15a1fcb17644ef4710b8764ce924
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651706"
---
# <a name="license-plate-receiving-via-the-warehouse-app"></a><span data-ttu-id="b5f87-103">通过仓库应用进行的牌照收货</span><span class="sxs-lookup"><span data-stu-id="b5f87-103">License plate receiving via the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5f87-104">此主题介绍如何设置仓库应用，以便支持使用牌照收货流程接收实际库存。</span><span class="sxs-lookup"><span data-stu-id="b5f87-104">This topic explains how to set up the warehouse app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="b5f87-105">可使用此功能快速记录与发货通知 (ASN) 有关的入站库存的收货。</span><span class="sxs-lookup"><span data-stu-id="b5f87-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="b5f87-106">当使用仓库管理流程为转移单发货时，系统将自动创建 ASN。</span><span class="sxs-lookup"><span data-stu-id="b5f87-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="b5f87-107">对于采购订单流程，ASN 可以手动创建，也可以使用入站 ASN 数据实体流程自动导入。</span><span class="sxs-lookup"><span data-stu-id="b5f87-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="b5f87-108">ASN 数据将通过*装箱结构*链接到负荷和装运，其中的托盘（父牌照）中包含货箱（嵌套牌照）。</span><span class="sxs-lookup"><span data-stu-id="b5f87-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="b5f87-109">为了在使用具有嵌套牌照的装箱结构时减少库存交易记录数量，系统记录父牌照中的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="b5f87-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="b5f87-110">为了基于装箱结构数据触发实际现有库存从父牌照到嵌套牌照的转移，移动设备必须提供基于*打包到嵌套的牌照*工作创建流程的菜单项。</span><span class="sxs-lookup"><span data-stu-id="b5f87-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

## <a name="warehousing-mobile-device-app-processing"></a><span data-ttu-id="b5f87-111">仓库移动设备应用处理</span><span class="sxs-lookup"><span data-stu-id="b5f87-111">Warehousing mobile device app processing</span></span>

<span data-ttu-id="b5f87-112">当工作人员扫描传入的牌照 ID 时，系统会初始化牌照接收流程。</span><span class="sxs-lookup"><span data-stu-id="b5f87-112">When a worker scans an incoming license plate ID, the system initializes a license plate receiving process.</span></span> <span data-ttu-id="b5f87-113">根据此信息，牌照的内容（来自 ASN 的数据）在入库台货位进行实际登记。</span><span class="sxs-lookup"><span data-stu-id="b5f87-113">Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location.</span></span> <span data-ttu-id="b5f87-114">接下来的流程将取决于您的业务流程需求。</span><span class="sxs-lookup"><span data-stu-id="b5f87-114">The flows that follow will depend your business process needs.</span></span>

## <a name="work-policies"></a><span data-ttu-id="b5f87-115">工作策略</span><span class="sxs-lookup"><span data-stu-id="b5f87-115">Work policies</span></span>

<span data-ttu-id="b5f87-116">与（举例）*完工入库*移动设备菜单项流程一样，牌照接收流程基于定义的设置支持多个工作流。</span><span class="sxs-lookup"><span data-stu-id="b5f87-116">As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.</span></span>

### <a name="work-policies-with-work-creation"></a><span data-ttu-id="b5f87-117">有工作创建的工作策略</span><span class="sxs-lookup"><span data-stu-id="b5f87-117">Work policies with work creation</span></span>

<span data-ttu-id="b5f87-118">当您使用创建工作的工作策略登记传入的物料时，系统会为每次登记生成并保存储存工作记录。</span><span class="sxs-lookup"><span data-stu-id="b5f87-118">When you register incoming items using a work policy that creates work, the system generates and saves put-away work records for each registration.</span></span> <span data-ttu-id="b5f87-119">如果您使用*牌照接收和储存*工作流程，登记和储存将使用单个移动设备菜单项作为单个操作处理。</span><span class="sxs-lookup"><span data-stu-id="b5f87-119">If you use the *License plate receiving and put away* work process, then registration and put away are handled as a single operation using a single mobile device menu item.</span></span> <span data-ttu-id="b5f87-120">如果您使用*牌照接收*流程，接收和储存流程将作为两个不同的仓库操作处理，每个操作有自己的移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="b5f87-120">If you use the *License plate receiving* process, then the receiving and put-away processes are handled as two different warehouse operations, each with their own mobile device menu item.</span></span>

### <a name="work-policies-without-work-creation"></a><span data-ttu-id="b5f87-121">无工作创建的工作策略</span><span class="sxs-lookup"><span data-stu-id="b5f87-121">Work policies without work creation</span></span>

<span data-ttu-id="b5f87-122">您可以在不创建工作的情况下使用牌照接收流程。</span><span class="sxs-lookup"><span data-stu-id="b5f87-122">You can use the license plate receiving process without creating work.</span></span> <span data-ttu-id="b5f87-123">如果您定义工作订单类型为*转移收货*和/或*采购订单*的工作策略，然后您将流程用于*牌照接收（和储存）*，以下两个 Warehousing mobile app 流程将不会创建工作。</span><span class="sxs-lookup"><span data-stu-id="b5f87-123">If you define work policies that have a work order type of *Transfer receipt* and/or *Purchase orders*, and you use the process for *License plate receiving (and put away)*, the following two Warehousing mobile app processes won't create work.</span></span> <span data-ttu-id="b5f87-124">取而代之的是，他们只会在入站收货台的牌照上登记入站实际库存。</span><span class="sxs-lookup"><span data-stu-id="b5f87-124">Instead, they will just register the inbound physical inventory on the license plate at the inbound receiving dock.</span></span>

- <span data-ttu-id="b5f87-125">*牌照接收*</span><span class="sxs-lookup"><span data-stu-id="b5f87-125">*License plate receiving*</span></span>
- <span data-ttu-id="b5f87-126">*牌照接收和储存*</span><span class="sxs-lookup"><span data-stu-id="b5f87-126">*License plate receiving and put away*</span></span>

> [!NOTE]
> - <span data-ttu-id="b5f87-127">您必须在**库存货位**部分为工作策略定义至少一个位置。</span><span class="sxs-lookup"><span data-stu-id="b5f87-127">You must define at least one location for a work policy in the **Inventory locations** section.</span></span> <span data-ttu-id="b5f87-128">您不能为多个工作政策指定相同的位置。</span><span class="sxs-lookup"><span data-stu-id="b5f87-128">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="b5f87-129">仓库移动设备菜单项的**打印标签**选项不会在不创建工作的情况下打印牌照标签。</span><span class="sxs-lookup"><span data-stu-id="b5f87-129">The **Print label** option for Warehousing mobile device menu items won't print a license plate label without work creation.</span></span>

<span data-ttu-id="b5f87-130">要使此功能在您的系统上可用，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开*牌照接收增强*功能。</span><span class="sxs-lookup"><span data-stu-id="b5f87-130">To make this functionality available on your system, you must turn on the *License plate receiving enhancements* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a><span data-ttu-id="b5f87-131">在不跟踪牌照的位置接收库存</span><span class="sxs-lookup"><span data-stu-id="b5f87-131">Receive inventory on a location that doesn't track license plates</span></span>

<span data-ttu-id="b5f87-132">即使未打开**使用牌照跟踪**，也可以使用分配给货位模板的仓库货位。</span><span class="sxs-lookup"><span data-stu-id="b5f87-132">It's possible to use a warehouse location that is assigned to a location profile even when **Use license plate tracking** isn't turned on.</span></span> <span data-ttu-id="b5f87-133">因此，当您接收库存时，可以直接在某个位置登记现有库存量，而无需创建工作。</span><span class="sxs-lookup"><span data-stu-id="b5f87-133">Therefore, when you receive inventory, you can directly register the on-hand inventory on a location without work creation.</span></span>

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a><span data-ttu-id="b5f87-134">为仓库中的每个接收位置添加移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="b5f87-134">Add mobile device menu items for each receiving location in a warehouse</span></span>

<span data-ttu-id="b5f87-135">*牌照接收增强*功能使您可以通过在 Warehousing mobile app 中添加位置特定的牌照接收（和储存）菜单项，来在仓库中的任何位置接收。</span><span class="sxs-lookup"><span data-stu-id="b5f87-135">The *License plate receiving enhancements* feature lets you receive at any location in a warehouse by adding location-specific license plate receiving (and put away) menu items to the Warehousing mobile app.</span></span> <span data-ttu-id="b5f87-136">以前，系统仅支持在为每个仓库定义的默认位置接收。</span><span class="sxs-lookup"><span data-stu-id="b5f87-136">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="b5f87-137">但是，打开此功能后，牌照接收（和储存）的移动设备菜单项现在会提供**使用默认数据**选项，可让您为每个菜单项选择一个自定义的“接收”位置。</span><span class="sxs-lookup"><span data-stu-id="b5f87-137">However, when this feature is turned on, mobile device menu items for license plate receiving (and put away) now provide the **Use default data** option, which lets you select a custom "to" location for each menu item.</span></span> <span data-ttu-id="b5f87-138">（此选项已经可用于某些其他类型的菜单项。）</span><span class="sxs-lookup"><span data-stu-id="b5f87-138">(This option was already available for some other types of menu items.)</span></span>

<span data-ttu-id="b5f87-139">要使此功能在您的系统上可用，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开*牌照接收增强*功能。</span><span class="sxs-lookup"><span data-stu-id="b5f87-139">To make this functionality available on your system, you must turn on the *License plate receiving enhancements* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="b5f87-140">显示或跳过收货摘要页</span><span class="sxs-lookup"><span data-stu-id="b5f87-140">Show or skip the receiving summary page</span></span>

<span data-ttu-id="b5f87-141">可使用*控制是否在移动设备上显示收货摘要页*功能在牌照收货流程中利用更详细的 Warehouse 应用流程。</span><span class="sxs-lookup"><span data-stu-id="b5f87-141">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="b5f87-142">开启此功能之后，牌照收货或牌照收货加入库处理的移动设备菜单项将提供**显示收货摘要页**设置。</span><span class="sxs-lookup"><span data-stu-id="b5f87-142">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="b5f87-143">此设置具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="b5f87-143">This setting has the following options:</span></span>

- <span data-ttu-id="b5f87-144">**显示详细摘要** – 牌照收货期间，工作人员将看到一个额外页面，其中显示完整的 ASN 信息。</span><span class="sxs-lookup"><span data-stu-id="b5f87-144">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="b5f87-145">**跳过摘要** – 工作人员将看不到完整的 ASN 信息。</span><span class="sxs-lookup"><span data-stu-id="b5f87-145">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="b5f87-146">仓库工作人员也将无法在接收过程中设置处置代码或添加例外。</span><span class="sxs-lookup"><span data-stu-id="b5f87-146">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

<span data-ttu-id="b5f87-147">要使此功能在您的系统上可用，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开*控制是否在移动设备上显示接收摘要页*功能。</span><span class="sxs-lookup"><span data-stu-id="b5f87-147">To make this functionality available on your system, you must turn on the *Control whether to display a receiving summary page on mobile devices* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="b5f87-148">阻止转移单已装运牌照用于目标仓库以外的其他仓库</span><span class="sxs-lookup"><span data-stu-id="b5f87-148">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="b5f87-149">如果 ASN 中包含已存在的牌照 ID，并且具有的实际现有数据所在仓货位置不是牌照的登记仓货位置，则不能使用牌照接收流程。</span><span class="sxs-lookup"><span data-stu-id="b5f87-149">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration occurs.</span></span>

<span data-ttu-id="b5f87-150">对于中转仓库不跟踪牌照（因此也不跟踪每个牌照的实际现有库存）的转移单方案，可使用*阻止转移单已装运牌照用于目标仓库以外的其他仓库*功能阻止中转中的牌照的实际现有更新。</span><span class="sxs-lookup"><span data-stu-id="b5f87-150">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="b5f87-151">要使此功能在您的系统上可用，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开*阻止转移单已装运牌照用于目标仓库以外的其他仓库*。</span><span class="sxs-lookup"><span data-stu-id="b5f87-151">To make this functionality available on your system, you must turn on the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="b5f87-152">若要在此功能可用时管理功能，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b5f87-152">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="b5f87-153">转到**仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="b5f87-153">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="b5f87-154">在**常规**选项卡的**牌照**快速选项卡上，将**中转仓库牌照政策**字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="b5f87-154">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="b5f87-155">**允许重复使用非跟踪牌照** – 系统的工作方式与*阻止转移单已装运牌照用于目标仓库以外的其他仓库*功能不可用时的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="b5f87-155">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="b5f87-156">此值是首先激活此功能时的默认设置。</span><span class="sxs-lookup"><span data-stu-id="b5f87-156">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="b5f87-157">**防止重复使用非跟踪牌照** – 收到转移单之前，目标仓库中仅允许与装运的牌照有关的现有更新。</span><span class="sxs-lookup"><span data-stu-id="b5f87-157">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="b5f87-158">更多信息</span><span class="sxs-lookup"><span data-stu-id="b5f87-158">More information</span></span>

<span data-ttu-id="b5f87-159">有关移动设备菜单项的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="b5f87-159">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="b5f87-160">有关*完工入库*生产方案的详细信息，请参阅[仓库工作策略概述](warehouse-work-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="b5f87-160">For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).</span></span>

<span data-ttu-id="b5f87-161">有关入站负荷管理的详细信息，请参阅[仓库对采购订单入站负荷的处理](inbound-load-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="b5f87-161">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
