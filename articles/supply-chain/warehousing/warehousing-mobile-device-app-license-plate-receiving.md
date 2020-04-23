---
title: 通过 Warehouse 移动应用的牌照收货
description: 此主题介绍如何设置 Warehousing 移动应用以支持使用牌照收货流程接收实际库存。
author: perlynne
manager: tfehr
ms.date: 03/31/2020
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
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261306"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="0ead6-103">通过 Warehouse 移动应用的牌照收货</span><span class="sxs-lookup"><span data-stu-id="0ead6-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="0ead6-104">此主题介绍如何设置 Warehousing 移动应用，以便支持使用牌照收货流程接收实际库存。</span><span class="sxs-lookup"><span data-stu-id="0ead6-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="0ead6-105">可使用此功能快速记录与发货通知 (ASN) 有关的入站库存的收货。</span><span class="sxs-lookup"><span data-stu-id="0ead6-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="0ead6-106">当使用仓库管理流程为转移单发货时，系统将自动创建 ASN。</span><span class="sxs-lookup"><span data-stu-id="0ead6-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="0ead6-107">对于采购订单流程，ASN 可以手动创建，也可以使用入站 ASN 数据实体流程自动导入。</span><span class="sxs-lookup"><span data-stu-id="0ead6-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="0ead6-108">ASN 数据将通过*装箱结构*链接到负荷和装运，其中的托盘（父牌照）中包含货箱（嵌套牌照）。</span><span class="sxs-lookup"><span data-stu-id="0ead6-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="0ead6-109">为了在使用具有嵌套牌照的装箱结构时减少库存交易记录数量，系统记录父牌照中的实际现有库存。</span><span class="sxs-lookup"><span data-stu-id="0ead6-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="0ead6-110">为了基于装箱结构数据触发实际现有库存从父牌照到嵌套牌照的转移，移动设备必须提供基于*打包到嵌套的牌照*工作创建流程的菜单项。</span><span class="sxs-lookup"><span data-stu-id="0ead6-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="0ead6-111">显示或跳过收货摘要页</span><span class="sxs-lookup"><span data-stu-id="0ead6-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="0ead6-112">可使用*控制是否在移动设备上显示收货摘要页*功能在牌照收货流程中利用更详细的 Warehouse 应用流程。</span><span class="sxs-lookup"><span data-stu-id="0ead6-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="0ead6-113">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="0ead6-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="0ead6-114">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="0ead6-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="0ead6-115">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="0ead6-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="0ead6-116">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="0ead6-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0ead6-117">**功能名称**：*控制是否在移动设备上显示收货摘要页*</span><span class="sxs-lookup"><span data-stu-id="0ead6-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="0ead6-118">开启此功能之后，牌照收货或牌照收货加入库处理的移动设备菜单项将提供**显示收货摘要页**设置。</span><span class="sxs-lookup"><span data-stu-id="0ead6-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="0ead6-119">此设置具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="0ead6-119">This setting has the following options:</span></span>

- <span data-ttu-id="0ead6-120">**显示详细摘要** – 牌照收货期间，工作人员将看到一个额外页面，其中显示完整的 ASN 信息。</span><span class="sxs-lookup"><span data-stu-id="0ead6-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="0ead6-121">**跳过摘要** – 工作人员将看不到完整的 ASN 信息。</span><span class="sxs-lookup"><span data-stu-id="0ead6-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="0ead6-122">仓库工作人员也将无法在接收过程中设置处置代码或添加例外。</span><span class="sxs-lookup"><span data-stu-id="0ead6-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="0ead6-123">阻止转移单已装运牌照用于目标仓库以外的其他仓库</span><span class="sxs-lookup"><span data-stu-id="0ead6-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="0ead6-124">如果 ASN 中包含已存在的牌照 ID，并且具有的实际现有数据所在仓库位置不是牌照的登记仓库位置，则不能使用牌照收货流程。</span><span class="sxs-lookup"><span data-stu-id="0ead6-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="0ead6-125">对于中转仓库不跟踪牌照（因此也不跟踪每个牌照的实际现有库存）的转移单方案，可使用*阻止转移单已装运牌照用于目标仓库以外的其他仓库*功能阻止中转中的牌照的实际现有更新。</span><span class="sxs-lookup"><span data-stu-id="0ead6-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="0ead6-126">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="0ead6-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="0ead6-127">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="0ead6-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="0ead6-128">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="0ead6-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="0ead6-129">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="0ead6-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0ead6-130">**功能名称**：*阻止转移单已装运牌照用于目标仓库以外的其他仓库*</span><span class="sxs-lookup"><span data-stu-id="0ead6-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="0ead6-131">若要在此功能可用时管理功能，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0ead6-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="0ead6-132">转到**仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="0ead6-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="0ead6-133">在**常规**选项卡的**牌照**快速选项卡上，将**中转仓库牌照政策**字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="0ead6-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="0ead6-134">**允许重复使用非跟踪牌照** – 系统的工作方式与*阻止转移单已装运牌照用于目标仓库以外的其他仓库*功能不可用时的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="0ead6-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="0ead6-135">此值是首先激活此功能时的默认设置。</span><span class="sxs-lookup"><span data-stu-id="0ead6-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="0ead6-136">**防止重复使用非跟踪牌照** – 收到转移单之前，目标仓库中仅允许与装运的牌照有关的现有更新。</span><span class="sxs-lookup"><span data-stu-id="0ead6-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="0ead6-137">更多信息</span><span class="sxs-lookup"><span data-stu-id="0ead6-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="0ead6-138">有关移动设备菜单项的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="0ead6-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
