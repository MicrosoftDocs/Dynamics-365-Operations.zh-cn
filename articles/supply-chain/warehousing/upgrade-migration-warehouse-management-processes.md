---
title: "将产品和仓库管理从 AX 2012 迁移到 Finance and Operations"
description: "此主题提供产品和仓库管理迁移选项的概览。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 92d0b4dd9611de4d717f30dc8736c673835bea29
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a><span data-ttu-id="538a2-103">将产品和仓库管理从 AX 2012 迁移到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="538a2-103">Migrate products and warehouse management from AX 2012 to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="538a2-104">本主题提供关于 Microsoft Dynamics 365 for Finance and Operations 中的产品和仓库管理迁移选项的概览。</span><span class="sxs-lookup"><span data-stu-id="538a2-104">This topic provides an overview of the product and warehouse management migration options within Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="introduction"></a><span data-ttu-id="538a2-105">介绍</span><span class="sxs-lookup"><span data-stu-id="538a2-105">Introduction</span></span>
------------

<span data-ttu-id="538a2-106">在升级到 Finance and Operations 期间，如果产品所关联的存储维度组的设置与 Finance and Operations 中对存储维度组设置的要求不匹配，则该产品被锁定。</span><span class="sxs-lookup"><span data-stu-id="538a2-106">During an upgrade to Finance and Operations, products are blocked if they are associated with a storage dimension group that has settings that don't match the requirements for storage dimension group settings in Finance and Operations.</span></span> <span data-ttu-id="538a2-107">但是，在升级后，您可以使用**更改物料的存储维度组**流程中的一组迁移选项取消锁定在升级期间被锁定的产品。</span><span class="sxs-lookup"><span data-stu-id="538a2-107">However, after the upgrade, you can use a set of migration options in the **Change storage dimension group for items** process to unblock products that were blocked during upgrade.</span></span> <span data-ttu-id="538a2-108">之后可以处理这些产品的交易记录。</span><span class="sxs-lookup"><span data-stu-id="538a2-108">You can then process transactions for those products.</span></span> <span data-ttu-id="538a2-109">您的一些物料可能已经与其站点、仓库和库位库存维度处于活动状态且被物理跟踪的存储维度组关联。</span><span class="sxs-lookup"><span data-stu-id="538a2-109">Some of your items might already be associated with storage dimension groups where the Site, Warehouse, and Location inventory dimensions are active and physically tracked.</span></span> <span data-ttu-id="538a2-110">在这种情况下，您可以使用**更改物料的存储维度组**流程允许这些物料在仓库管理流程中使用。</span><span class="sxs-lookup"><span data-stu-id="538a2-110">In this case, you can use the **Change storage dimension group for items** process to enable those items to be used in warehouse management processes.</span></span> <span data-ttu-id="538a2-111">如果您要为现有物料使用仓库管理功能，此功能十分有用。</span><span class="sxs-lookup"><span data-stu-id="538a2-111">This feature is useful if you want to use the warehouse management functionality for existing items.</span></span>

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a><span data-ttu-id="538a2-112">使用 AX 2012 R3 WMSII 时，升级到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="538a2-112">Upgrading to Finance and Operations, when AX 2012 R3 WMSII is used</span></span>
<span data-ttu-id="538a2-113">Finance and Operations 不再支持来自 Microsoft Dynamics AX 2012 的旧 **WMSII** 模块。</span><span class="sxs-lookup"><span data-stu-id="538a2-113">Finance and Operations, no longer supports the legacy **WMSII** module from Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="538a2-114">相反，您可以使用新的**仓库管理**模块。</span><span class="sxs-lookup"><span data-stu-id="538a2-114">Instead, you can use the new **Warehouse management** module.</span></span> <span data-ttu-id="538a2-115">在以前的版本中，可能为财务库存选择库位和托盘 ID 库存维度。</span><span class="sxs-lookup"><span data-stu-id="538a2-115">In previous versions, the Location and Pallet ID inventory dimensions could be selected for financial inventory.</span></span> <span data-ttu-id="538a2-116">但是，作为升级流程的一部分，不可以再为财务库存启用托盘 ID 库存维度。</span><span class="sxs-lookup"><span data-stu-id="538a2-116">However, as part of the upgrade process, the Pallet ID inventory dimension can no longer be enabled for financial inventory.</span></span> <span data-ttu-id="538a2-117">所有与使用托盘 ID 库存维度的存储维度组关联的产品将被锁定且不会被处理。</span><span class="sxs-lookup"><span data-stu-id="538a2-117">All products that are associated with a storage dimension group that uses the Pallet ID inventory dimension will be blocked and won't be processed.</span></span>

### <a name="enabling-items-in-finance-and-operations"></a><span data-ttu-id="538a2-118">在 Finance and Operations 中启用物料</span><span class="sxs-lookup"><span data-stu-id="538a2-118">Enabling items in Finance and Operations</span></span>

<span data-ttu-id="538a2-119">在 Finance and Operations 中，作为仓库管理流程一部分使用的物料必须与选择了**使用仓库管理流程**参数的存储维度组相关联。</span><span class="sxs-lookup"><span data-stu-id="538a2-119">In Finance and Operations, items that will be used as part of warehouse management processes must be associated with a storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span> <span data-ttu-id="538a2-120">选择此设置后，站点、仓库、库存状态、库位和牌照库存维度变为活动状态。</span><span class="sxs-lookup"><span data-stu-id="538a2-120">When this setting is selected, the Site, Warehouse, Inventory status, Location, and License plate inventory dimensions become active.</span></span> <span data-ttu-id="538a2-121">您可以仅为已经与库位库存维度处于活动状态的存储维度组关联的物料更改此类型的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-121">You can change to this type of storage dimension group only for items that are already associated with storage dimension groups where the Location inventory dimension is active.</span></span>

### <a name="items-that-are-blocked-for-inventory-updates"></a><span data-ttu-id="538a2-122">已针对库存更新锁定的物料</span><span class="sxs-lookup"><span data-stu-id="538a2-122">Items that are blocked for inventory updates</span></span>

<span data-ttu-id="538a2-123">要查看在升级期间已锁定且无法处理的已发布产品的列表，请单击**库存管理** &gt; **设置** &gt; **库存** &gt; **针对库存更新锁定的物料**。</span><span class="sxs-lookup"><span data-stu-id="538a2-123">To view the list of released products that were blocked during upgrade and can't be processed, click **Inventory management** &gt; **Setup** &gt; **Inventory** &gt; **Items blocked for inventory updates**.</span></span>

### <a name="reapplying-blocked-products"></a><span data-ttu-id="538a2-124">重新应用锁定的产品</span><span class="sxs-lookup"><span data-stu-id="538a2-124">Reapplying blocked products</span></span>

<span data-ttu-id="538a2-125">要取消锁定在升级期间已锁定的产品，必须为该产品选择新的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-125">To unblock products that were blocked during upgrade, you must select a new storage dimension group for the products.</span></span> <span data-ttu-id="538a2-126">请注意，即使存在未结的库存交易记录，您也可以更改存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-126">Note that you can change the storage dimension group even if open inventory transactions exist.</span></span> <span data-ttu-id="538a2-127">要使用在升级期间已锁定的物料，您有两个选项：</span><span class="sxs-lookup"><span data-stu-id="538a2-127">To use items that were blocked during upgrade, you have two options:</span></span>

-   <span data-ttu-id="538a2-128">将物料的存储维度组更改为仅使用站点、仓库和库位库存维度的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-128">Change the storage dimension group for the item to a storage dimension group that uses only the Site, Warehouse, and Location inventory dimensions.</span></span> <span data-ttu-id="538a2-129">进行此更改后，不再使用托盘 ID 库存维度。</span><span class="sxs-lookup"><span data-stu-id="538a2-129">As a result of this change, the Pallet ID inventory dimension is no longer used.</span></span>
-   <span data-ttu-id="538a2-130">将物料的存储维度组更改为使用仓库管理流程的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-130">Change the storage dimension group for the item to a storage dimension group that uses the warehouse management processes.</span></span> <span data-ttu-id="538a2-131">进行此更改后，现在开始使用牌照库存维度。</span><span class="sxs-lookup"><span data-stu-id="538a2-131">As a result of this change, the License plate inventory dimension is now used.</span></span>

### <a name="migration-processes"></a><span data-ttu-id="538a2-132">迁移流程</span><span class="sxs-lookup"><span data-stu-id="538a2-132">Migration processes</span></span>

<span data-ttu-id="538a2-133">在 Finance and Operations 中，物料跟踪是仓库管理流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="538a2-133">In Finance and Operations, item tracking is part of the warehouse management processes.</span></span> <span data-ttu-id="538a2-134">对于这些流程，所有仓库及其库位必须与库位模板相关联。</span><span class="sxs-lookup"><span data-stu-id="538a2-134">For these processes, all warehouses and their locations must be associated with a location profile.</span></span> <span data-ttu-id="538a2-135">从概念上讲，如果您要使用仓库管理流程，必须处理两个流程：</span><span class="sxs-lookup"><span data-stu-id="538a2-135">Conceptually, if you want to use warehouse management processes, two processes must be handled:</span></span>

-   <span data-ttu-id="538a2-136">必须启用现有仓库以使用仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="538a2-136">Existing warehouses must be enabled to use warehouse management processes.</span></span>
-   <span data-ttu-id="538a2-137">现有的已发布的产品必须与使用仓库管理流程的新的存储维度组相关联。</span><span class="sxs-lookup"><span data-stu-id="538a2-137">Existing released products must be associated with a new storage dimension group that uses warehouse management processes.</span></span>

<span data-ttu-id="538a2-138">如果源存储维度组使用托盘 ID 库存维度，使用托盘 ID 库位维度的现有库存的库位必须与选择了**使用牌照跟踪**参数的库位模板相关联。</span><span class="sxs-lookup"><span data-stu-id="538a2-138">If the source storage dimension groups use the Pallet ID inventory dimension, the locations of existing on-hand inventory that used the Pallet ID inventory dimension must be associated with a location profile where the **Use license plate tracking** parameter is selected.</span></span> <span data-ttu-id="538a2-139">如果不应启用现有仓库以使用仓库管理流程，您可以将现有库存的存储维度组更改为仅处理站点、仓库和库位库存维度的组。</span><span class="sxs-lookup"><span data-stu-id="538a2-139">If the existing warehouses should not be enabled to use warehouse management processes, you can change the storage dimension groups of the existing on-hand inventory to groups that handle only the Site, Warehouse, and Location inventory dimensions.</span></span>

### <a name="using-the-warehouse-management-processes"></a><span data-ttu-id="538a2-140">使用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="538a2-140">Using the warehouse management processes</span></span>

<span data-ttu-id="538a2-141">在您可以使用**仓库管理**模块中的已发布产品前，产品必须使用选择了**使用仓库管理流程**参数的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-141">Before you can use released products in the **Warehouse management** module, the products must use a storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span>

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a><span data-ttu-id="538a2-142">启用仓库以使用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="538a2-142">Enable warehouses to use warehouse management processes</span></span>

1.  <span data-ttu-id="538a2-143">创建至少一个新的库位模板。</span><span class="sxs-lookup"><span data-stu-id="538a2-143">Create at least one new location profile.</span></span>
2.  <span data-ttu-id="538a2-144">单击**仓库管理** &gt; **设置** &gt;**启用仓库管理流程** &gt;**启用仓库设置**。</span><span class="sxs-lookup"><span data-stu-id="538a2-144">Click **Warehouse management** &gt; **Setup** &gt; **Enable warehouse management processes** &gt; **Enable warehouse setup**.</span></span>
3.  <span data-ttu-id="538a2-145">在**启用仓库设置**页，添加应启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="538a2-145">On the **Enable warehouse setup** page, add the warehouses that should be enabled.</span></span> <span data-ttu-id="538a2-146">您可以直接在页面上或使用 Microsoft Office 集成完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="538a2-146">You can complete this step either directly on the page or by using the Microsoft Office integration.</span></span>
4.  <span data-ttu-id="538a2-147">将库位模板分配到所有库位。</span><span class="sxs-lookup"><span data-stu-id="538a2-147">Assign a location profile to all the locations.</span></span> <span data-ttu-id="538a2-148">您可以直接从页面使用 Microsoft Office 集成轻松地完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="538a2-148">You can easily complete this step by using the Microsoft Office integration directly from the page.</span></span> <span data-ttu-id="538a2-149">您可以在 [数据管理](../../dev-itpro/data-entities/data-entities.md) 中导出和导入数据或使用数据实体处理。</span><span class="sxs-lookup"><span data-stu-id="538a2-149">You can either export and import the data, or use the data entity processing in [Data management](../../dev-itpro/data-entities/data-entities.md).</span></span>
5.  <span data-ttu-id="538a2-150">验证更改。</span><span class="sxs-lookup"><span data-stu-id="538a2-150">Validate the changes.</span></span> <span data-ttu-id="538a2-151">作为验证过程的一部分，发生不同的数据完整性验证。</span><span class="sxs-lookup"><span data-stu-id="538a2-151">As part of the validation process, various validations of data integrity occur.</span></span> <span data-ttu-id="538a2-152">作为更大的升级流程的一部分，可能必须在源实现上调整发生的发货。</span><span class="sxs-lookup"><span data-stu-id="538a2-152">As part of a larger upgrade process, issues that occur might have to be adjusted on the source implementation.</span></span> <span data-ttu-id="538a2-153">在这种情况下，需要附加数据升级。</span><span class="sxs-lookup"><span data-stu-id="538a2-153">In this case, an additional data upgrade will be required.</span></span>
6.  <span data-ttu-id="538a2-154">处理更改。</span><span class="sxs-lookup"><span data-stu-id="538a2-154">Process the changes.</span></span>

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a><span data-ttu-id="538a2-155">更改物料的存储维度组，以便其使用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="538a2-155">Change the storage dimension group for items, so that it uses warehouse management processes</span></span>

1.  <span data-ttu-id="538a2-156">创建新的**库存状态**值，并将它分配为**仓库管理参数**设置中的**默认库存状态 ID**值。</span><span class="sxs-lookup"><span data-stu-id="538a2-156">Create a new **Inventory status** value, and assign it as the **Default inventory status ID** value in the **Warehouse management parameters** settings.</span></span>
2.  <span data-ttu-id="538a2-157">创建选择了**使用仓库管理流程**参数的新的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="538a2-157">Create a new storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span>
3.  <span data-ttu-id="538a2-158">在**预留层次结构**页，根据物料的存储和跟踪维度组定义新的预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="538a2-158">On the **Reservation hierarchy** page, define a new reservation hierarchy according to the item’s storage and tracking dimension groups.</span></span>
4.  <span data-ttu-id="538a2-159">创建一个或多个单位序列组且序列组至少包括与用于物料的库存单位相同的单位。</span><span class="sxs-lookup"><span data-stu-id="538a2-159">Create one or more unit sequence groups that include at least the same units that are used for the items' inventory units.</span></span>
5.  <span data-ttu-id="538a2-160">单击**仓库管理** &gt; **设置** &gt;**启用仓库管理流程** &gt;**更改物料的存储维度组**。</span><span class="sxs-lookup"><span data-stu-id="538a2-160">Click **Warehouse management** &gt; **Setup** &gt; **Enable warehouse management processes** &gt; **Change storage dimension group for items**.</span></span>
6.  <span data-ttu-id="538a2-161">在**更改物料的存储维度组**页，添加物料编号、存储维度组和单位序列组。</span><span class="sxs-lookup"><span data-stu-id="538a2-161">On the **Change storage dimension group for items** page, add the item numbers, storage dimension groups, and unit sequence groups.</span></span> <span data-ttu-id="538a2-162">您可以直接在页面上、使用 Microsoft Office 集成或使用 [数据管理](../../dev-itpro/data-entities/data-entities.md) 中的数据实体流程完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="538a2-162">You can complete this step directly on the page, by using the Microsoft Office integration, or by using the data entity process in [Data management](../../dev-itpro/data-entities/data-entities.md).</span></span>
7.  <span data-ttu-id="538a2-163">验证更改。</span><span class="sxs-lookup"><span data-stu-id="538a2-163">Validate the changes.</span></span> <span data-ttu-id="538a2-164">作为验证过程的一部分，发生不同的数据完整性验证。</span><span class="sxs-lookup"><span data-stu-id="538a2-164">As part of the validation process, various validations of data integrity occur.</span></span> <span data-ttu-id="538a2-165">作为更大的升级流程的一部分，可能必须在源实现上调整发生的发货。</span><span class="sxs-lookup"><span data-stu-id="538a2-165">As part of a larger upgrade process, issues that occur might have to be adjusted on the source implementation.</span></span> <span data-ttu-id="538a2-166">在这种情况下，需要附加数据升级。</span><span class="sxs-lookup"><span data-stu-id="538a2-166">In this case, additional data upgrade will be required.</span></span>
8.  <span data-ttu-id="538a2-167">处理更改。</span><span class="sxs-lookup"><span data-stu-id="538a2-167">Process the changes.</span></span> <span data-ttu-id="538a2-168">更新所有库存维度可能需要一段时间。</span><span class="sxs-lookup"><span data-stu-id="538a2-168">An update of all the inventory dimensions can take a while.</span></span> <span data-ttu-id="538a2-169">您可以使用批处理作业任务监控进度。</span><span class="sxs-lookup"><span data-stu-id="538a2-169">You can monitor the progress by using the batch jobs tasks.</span></span>



