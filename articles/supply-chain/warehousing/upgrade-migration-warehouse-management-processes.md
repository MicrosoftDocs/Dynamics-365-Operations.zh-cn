---
title: "将仓库管理从Microsoft Dynamics AX 2012 升级到 Finance and Operations"
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
ms.sourcegitcommit: 6c6c7c3f63b7a49820811a7ec80248b09b6e3acf
ms.openlocfilehash: 9651188102d96e68df939e941051a50a76339f03
ms.contentlocale: zh-cn
ms.lasthandoff: 06/19/2018

---

# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a><span data-ttu-id="a3bdf-103">将仓库管理从Microsoft Dynamics AX 2012 升级到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3bdf-103">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Finance and Operations</span></span>


[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3bdf-104">此主题概述运行 WMSII 模块从 Microsoft Dynamics AX 2012 R3 升级到 Microsoft Dynamics 365 for Finance and Operations 的过程。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-104">This topic provides an overview of the process of upgrading from Microsoft Dynamics AX 2012 R3, running the WMSII module, to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a3bdf-105">Finance and Operations 不再支持来自 Microsoft Dynamics AX 2012 的旧 **WMSII** 模块。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-105">Finance and Operations, no longer supports the legacy **WMSII** module from Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="a3bdf-106">相反，您可以使用**仓库管理**模块。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-106">Instead, you can use the **Warehouse management** module.</span></span> <span data-ttu-id="a3bdf-107">在 WMSII 模块中，可为财务库存选择“库位”和“托盘 ID”库存维度，但是在 Finance and Operations 中，不能将“托盘 ID”库存维度用于财务库存。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-107">In the WMSII module, the Location and Pallet ID inventory dimensions could be selected for financial inventory, however, the Pallet ID inventory dimension cannot be used for financial inventory in Finance and Operations.</span></span>

<span data-ttu-id="a3bdf-108">升级期间，将标识与使用“托盘 ID”库存维度的存储维度组关联的所有产品，并标记为已锁定，不可为升级处理。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-108">During an upgrade, all products that are associated with a storage dimension group that uses the Pallet ID inventory dimension are identified, marked as blocked, and not processed for upgrade.</span></span>

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a><span data-ttu-id="a3bdf-109">使用 AX 2012 R3 WMSII 时，升级到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3bdf-109">Upgrading to Finance and Operations, when AX 2012 R3 WMSII is used</span></span>
<span data-ttu-id="a3bdf-110">在升级后，您可以使用**更改物料的存储维度组**窗体中的一组选项取消锁定在升级期间被锁定的产品，然后处理这些产品的交易记录。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-110">After the upgrade, you can use a set of options in the **Change storage dimension group for items** form to unblock products that were blocked during upgrade, and then process transactions for those products.</span></span>

### <a name="enabling-items-in-finance-and-operations"></a><span data-ttu-id="a3bdf-111">在 Finance and Operations 中启用物料</span><span class="sxs-lookup"><span data-stu-id="a3bdf-111">Enabling items in Finance and Operations</span></span>
<span data-ttu-id="a3bdf-112">需要执行此更改，因为在 Finance and Operations 中，物料跟踪是仓库管理流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-112">This change is required because in Finance and Operations, item tracking is part of the warehouse management processes.</span></span> <span data-ttu-id="a3bdf-113">对于这些流程，所有仓库及其库位必须与库位模板相关联。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-113">For these processes, all warehouses and their locations must be associated with a location profile.</span></span> <span data-ttu-id="a3bdf-114">如果您要使用仓库管理流程，则必须配置以下设置：</span><span class="sxs-lookup"><span data-stu-id="a3bdf-114">If you want to use warehouse management processes, the following must be configured:</span></span>
-   <span data-ttu-id="a3bdf-115">必须启用现有仓库以使用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="a3bdf-115">Existing warehouses must be enabled to use warehouse management processes</span></span> 
-   <span data-ttu-id="a3bdf-116">现有的已发布的产品必须与使用仓库管理流程的存储维度组相关联</span><span class="sxs-lookup"><span data-stu-id="a3bdf-116">Existing released products must be associated with a storage dimension group that uses warehouse management processes</span></span> 

<span data-ttu-id="a3bdf-117">如果源存储维度组使用托盘 ID 库存维度，使用托盘 ID 库位维度的现有库存的库位必须与选择了**使用牌照跟踪**参数的库位模板相关联。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-117">If the source storage dimension groups use the Pallet ID inventory dimension, the locations of existing on-hand inventory that used the Pallet ID inventory dimension must be associated with a location profile in which the **Use license plate tracking** parameter is selected.</span></span> <span data-ttu-id="a3bdf-118">如果不应启用现有仓库以使用仓库管理流程，您可以将现有库存的存储维度组更改为仅处理站点、仓库和库位库存维度的组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-118">If the existing warehouses should not be enabled to use warehouse management processes, you can change the storage dimension groups of the existing on-hand inventory to groups that handle only the Site, Warehouse, and Location inventory dimensions.</span></span> 

> [!NOTE] 
>  <span data-ttu-id="a3bdf-119">即使存在未结的库存交易记录，您也可以更改物料的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-119">You can change the storage dimension group for items even if open inventory transactions exist.</span></span>

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a><span data-ttu-id="a3bdf-120">找到因为托盘 ID 而锁定的产品</span><span class="sxs-lookup"><span data-stu-id="a3bdf-120">Find products that were blocked because of Pallet ID</span></span>
<span data-ttu-id="a3bdf-121">要查看在升级期间已锁定且无法处理的已发布产品的列表，请单击**库存管理** &gt; **设置** &gt; **库存** &gt; **针对库存更新锁定的物料**。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-121">To view the list of released products that were blocked during upgrade and can't be processed, click **Inventory management** &gt; **Setup** &gt; **Inventory** &gt; **Items blocked for inventory updates**.</span></span>

## <a name="change-storage-dimension-group-for-blocked-products"></a><span data-ttu-id="a3bdf-122">更改已锁定产品的存储维度组</span><span class="sxs-lookup"><span data-stu-id="a3bdf-122">Change storage dimension group for blocked products</span></span> 
 
<span data-ttu-id="a3bdf-123">若要作为仓库管理流程一部分使用，物料必须与“库位”库存维度处于活动状态且选择了**使用仓库管理流程**参数的存储维度组相关联。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-123">To be used as part of a warehouse management process, an item must be associated with a storage dimension group in which the Location inventory dimension is active, and the **Use warehouse management processes** parameter is selected.</span></span> <span data-ttu-id="a3bdf-124">选择此设置后，站点、仓库、库存状态、库位和牌照库存维度变为活动状态。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-124">When this setting is selected, the Site, Warehouse, Inventory status, Location, and License plate inventory dimensions become active.</span></span>

<span data-ttu-id="a3bdf-125">要取消锁定在升级期间已锁定的产品，必须为该产品选择新的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-125">To unblock products that were blocked during upgrade, you must select a new storage dimension group for the products.</span></span> <span data-ttu-id="a3bdf-126">请注意，即使存在未结的库存交易记录，您也可以更改存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-126">Note that you can change the storage dimension group even if open inventory transactions exist.</span></span> <span data-ttu-id="a3bdf-127">要使用在升级期间已锁定的物料，您有两个选项：</span><span class="sxs-lookup"><span data-stu-id="a3bdf-127">To use items that were blocked during upgrade, you have two options:</span></span>

-   <span data-ttu-id="a3bdf-128">将物料的存储维度组更改为仅使用站点、仓库和库位库存维度的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-128">Change the storage dimension group for the item to a storage dimension group that uses only the Site, Warehouse, and Location inventory dimensions.</span></span> <span data-ttu-id="a3bdf-129">进行此更改后，不再使用托盘 ID 库存维度。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-129">As a result of this change, the Pallet ID inventory dimension is no longer used.</span></span>
-   <span data-ttu-id="a3bdf-130">将物料的存储维度组更改为使用仓库管理流程的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-130">Change the storage dimension group for the item to a storage dimension group that uses the warehouse management processes.</span></span> <span data-ttu-id="a3bdf-131">进行此更改后，现在开始使用牌照库存维度。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-131">As a result of this change, the License plate inventory dimension is now used.</span></span>

## <a name="configure-warehouse-management-processes"></a><span data-ttu-id="a3bdf-132">配置仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="a3bdf-132">Configure warehouse management processes</span></span>
<span data-ttu-id="a3bdf-133">在您可以使用**仓库管理**模块中的已发布产品前，产品必须使用选择了**使用仓库管理流程**参数的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-133">Before you can use released products in the **Warehouse management** module, the products must use a storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span>

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a><span data-ttu-id="a3bdf-134">启用仓库以使用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="a3bdf-134">Enable warehouses to use warehouse management processes</span></span>

1.  <span data-ttu-id="a3bdf-135">创建至少一个新的库位模板。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-135">Create at least one new location profile.</span></span>
2.  <span data-ttu-id="a3bdf-136">单击**仓库管理** &gt; **设置** &gt;**启用仓库管理流程** &gt;**启用仓库设置**。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-136">Click **Warehouse management** &gt; **Setup** &gt; **Enable warehouse management processes** &gt; **Enable warehouse setup**.</span></span>
3.  <span data-ttu-id="a3bdf-137">在**启用仓库设置**页，添加应启用的仓库。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-137">On the **Enable warehouse setup** page, add the warehouses that should be enabled.</span></span> <span data-ttu-id="a3bdf-138">您可以直接在页面上或使用 Microsoft Office 集成完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-138">You can complete this step either directly on the page or by using the Microsoft Office integration.</span></span>
4.  <span data-ttu-id="a3bdf-139">将库位模板分配到所有库位。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-139">Assign a location profile to all the locations.</span></span> <span data-ttu-id="a3bdf-140">您可以直接从页面使用 Microsoft Office 集成轻松地完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-140">You can easily complete this step by using the Microsoft Office integration directly from the page.</span></span> <span data-ttu-id="a3bdf-141">您可以在 [数据管理](../../dev-itpro/data-entities/data-entities.md) 中导出和导入数据或使用数据实体处理。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-141">You can either export and import the data, or use the data entity processing in [Data management](../../dev-itpro/data-entities/data-entities.md).</span></span>
5.  <span data-ttu-id="a3bdf-142">验证更改。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-142">Validate the changes.</span></span> <span data-ttu-id="a3bdf-143">作为验证过程的一部分，发生不同的数据完整性验证。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-143">As part of the validation process, various validations of data integrity occur.</span></span> <span data-ttu-id="a3bdf-144">作为更大的升级流程的一部分，可能必须在源实现上调整发生的发货。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-144">As part of a larger upgrade process, issues that occur might have to be adjusted on the source implementation.</span></span> <span data-ttu-id="a3bdf-145">在这种情况下，需要附加数据升级。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-145">In this case, an additional data upgrade will be required.</span></span>
6.  <span data-ttu-id="a3bdf-146">处理更改。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-146">Process the changes.</span></span>

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a><span data-ttu-id="a3bdf-147">更改物料的存储维度组，以便其使用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="a3bdf-147">Change the storage dimension group for items, so that it uses warehouse management processes</span></span>

1.  <span data-ttu-id="a3bdf-148">创建新的**库存状态**值，并将它分配为**仓库管理参数**设置中的**默认库存状态 ID**值。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-148">Create a new **Inventory status** value, and assign it as the **Default inventory status ID** value in the **Warehouse management parameters** settings.</span></span>
2.  <span data-ttu-id="a3bdf-149">创建选择了**使用仓库管理流程**参数的新的存储维度组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-149">Create a new storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span>
3.  <span data-ttu-id="a3bdf-150">在**预留层次结构**页，根据物料的存储和跟踪维度组定义新的预留层次结构。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-150">On the **Reservation hierarchy** page, define a new reservation hierarchy according to the item’s storage and tracking dimension groups.</span></span>
4.  <span data-ttu-id="a3bdf-151">创建一个或多个单位序列组且序列组至少包括与用于物料的库存单位相同的单位。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-151">Create one or more unit sequence groups that include at least the same units that are used for the items' inventory units.</span></span>
5.  <span data-ttu-id="a3bdf-152">单击**仓库管理** &gt; **设置** &gt;**启用仓库管理流程** &gt;**更改物料的存储维度组**。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-152">Click **Warehouse management** &gt; **Setup** &gt; **Enable warehouse management processes** &gt; **Change storage dimension group for items**.</span></span>
6.  <span data-ttu-id="a3bdf-153">在**更改物料的存储维度组**页，添加物料编号、存储维度组和单位序列组。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-153">On the **Change storage dimension group for items** page, add the item numbers, storage dimension groups, and unit sequence groups.</span></span> <span data-ttu-id="a3bdf-154">您可以直接在页面上、使用 Microsoft Office 集成或使用 [数据管理](../../dev-itpro/data-entities/data-entities.md) 中的数据实体流程完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-154">You can complete this step directly on the page, by using the Microsoft Office integration, or by using the data entity process in [Data management](../../dev-itpro/data-entities/data-entities.md).</span></span>
7.  <span data-ttu-id="a3bdf-155">验证更改。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-155">Validate the changes.</span></span> <span data-ttu-id="a3bdf-156">作为验证过程的一部分，发生不同的数据完整性验证。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-156">As part of the validation process, various validations of data integrity occur.</span></span> <span data-ttu-id="a3bdf-157">作为更大的升级流程的一部分，可能必须在源实现上调整发生的发货。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-157">As part of a larger upgrade process, issues that occur might have to be adjusted on the source implementation.</span></span> <span data-ttu-id="a3bdf-158">在这种情况下，需要附加数据升级。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-158">In this case, additional data upgrade will be required.</span></span>
8.  <span data-ttu-id="a3bdf-159">处理更改。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-159">Process the changes.</span></span> <span data-ttu-id="a3bdf-160">更新所有库存维度可能需要一段时间。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-160">An update of all the inventory dimensions can take a while.</span></span> <span data-ttu-id="a3bdf-161">您可以使用批处理作业任务监控进度。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-161">You can monitor the progress by using the batch jobs tasks.</span></span>

