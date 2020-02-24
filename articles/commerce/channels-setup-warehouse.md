---
title: 设置仓库
description: 本主题描述如何在 Microsoft Dynamics 365 Commerce 中设置要与新渠道一起使用的仓库。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fe785e3bfd503193a588958ae5df0d1c0fdb9e52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002304"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="4d610-103">仓库设置</span><span class="sxs-lookup"><span data-stu-id="4d610-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4d610-104">本主题描述如何在 Microsoft Dynamics 365 Commerce 中设置要与新渠道一起使用的仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d610-105">概览</span><span class="sxs-lookup"><span data-stu-id="4d610-105">Overview</span></span>

<span data-ttu-id="4d610-106">每个商业渠道都需要一个与之关联已配置仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="4d610-107">以下过程提供了为商业渠道设置仓库所需的最低配置。</span><span class="sxs-lookup"><span data-stu-id="4d610-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="4d610-108">有关仓库设置的更多信息，请参见[仓库管理概览](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)。</span><span class="sxs-lookup"><span data-stu-id="4d610-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="4d610-109">配置仓库站点</span><span class="sxs-lookup"><span data-stu-id="4d610-109">Configure a warehouse site</span></span>

<span data-ttu-id="4d610-110">在设置仓库之前，您需要配置仓库站点。</span><span class="sxs-lookup"><span data-stu-id="4d610-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="4d610-111">要配置仓库站点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="4d610-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="4d610-112">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 站点**。</span><span class="sxs-lookup"><span data-stu-id="4d610-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="4d610-113">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4d610-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d610-114">在**站点**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4d610-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="4d610-115">在**名称**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4d610-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="4d610-116">在**常规**部分中，设置适当的**时区**。</span><span class="sxs-lookup"><span data-stu-id="4d610-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="4d610-117">在**地址**部分中，输入地址。</span><span class="sxs-lookup"><span data-stu-id="4d610-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="4d610-118">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4d610-119">下图显示了一个仓库站点示例。</span><span class="sxs-lookup"><span data-stu-id="4d610-119">The following image shows an example warehouse site.</span></span>

![仓库站点示例](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="4d610-121">设置仓库</span><span class="sxs-lookup"><span data-stu-id="4d610-121">Set up a warehouse</span></span>

<span data-ttu-id="4d610-122">若要设置仓库，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4d610-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="4d610-123">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="4d610-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="4d610-124">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4d610-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d610-125">在**仓库**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4d610-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="4d610-126">如果这是到零售商店的 1:1 映射，请考虑使用商店名称或区域分销中心的名称。</span><span class="sxs-lookup"><span data-stu-id="4d610-126">If this is a 1:1 mapping to a retail store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="4d610-127">在**名称**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4d610-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="4d610-128">在**站点**下拉列表中，选择先前创建的仓库站点。</span><span class="sxs-lookup"><span data-stu-id="4d610-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="4d610-129">在**类型**字段中，选择**默认**。</span><span class="sxs-lookup"><span data-stu-id="4d610-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="4d610-130">如果要设置**检验仓库**，首先，您需要按照以下步骤创建一个额外的仓库，其中**类型**设定为**检验**。</span><span class="sxs-lookup"><span data-stu-id="4d610-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="4d610-131">如果要设置**中转仓库**，首先，您需要按照以下步骤创建一个额外的仓库，其中**类型**设定为**中转**。</span><span class="sxs-lookup"><span data-stu-id="4d610-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="4d610-132">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="4d610-133">设置库存通道</span><span class="sxs-lookup"><span data-stu-id="4d610-133">Set up inventory aisles</span></span>

<span data-ttu-id="4d610-134">要设置库存通道，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4d610-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="4d610-135">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 位置设置 \> 库存通道**。</span><span class="sxs-lookup"><span data-stu-id="4d610-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="4d610-136">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4d610-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d610-137">在**仓库**下拉列表中，选择先前创建的仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="4d610-138">在**通道**字段中，输入名称（例如“默认”）。</span><span class="sxs-lookup"><span data-stu-id="4d610-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="4d610-139">在**名称**字段中，输入名称（例如“默认通道”）。</span><span class="sxs-lookup"><span data-stu-id="4d610-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="4d610-140">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="4d610-141">设置仓库库位</span><span class="sxs-lookup"><span data-stu-id="4d610-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="4d610-142">要为标准、损坏和退货库存设置仓库库存库存，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="4d610-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="4d610-143">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="4d610-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="4d610-144">选择您之前创建的仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="4d610-145">在操作窗格上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="4d610-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="4d610-146">在操作窗格上，选择**仓库**，然后选择**库存库位**。</span><span class="sxs-lookup"><span data-stu-id="4d610-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="4d610-147">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4d610-147">On the action pane, select **New**.</span></span> <span data-ttu-id="4d610-148">**仓库**下拉列表应默认为您的新仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="4d610-149">在**通道**框中，输入您先前指定的通道的名称。</span><span class="sxs-lookup"><span data-stu-id="4d610-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="4d610-150">将**手动更新**设置至**是**</span><span class="sxs-lookup"><span data-stu-id="4d610-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="4d610-151">在**库位**框中，输入仓库的名称。</span><span class="sxs-lookup"><span data-stu-id="4d610-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="4d610-152">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="4d610-153">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4d610-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="4d610-154">**仓库**下拉列表应默认为您的新仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="4d610-155">在**通道**框中，输入您先前指定的通道的名称。</span><span class="sxs-lookup"><span data-stu-id="4d610-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="4d610-156">将**手动更新**设置至**是**</span><span class="sxs-lookup"><span data-stu-id="4d610-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="4d610-157">在**库位**框中，输入“已损坏”。</span><span class="sxs-lookup"><span data-stu-id="4d610-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="4d610-158">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="4d610-159">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4d610-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="4d610-160">**仓库**下拉列表应默认为您的新仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="4d610-161">在**通道**框中，输入您先前指定的通道的名称。</span><span class="sxs-lookup"><span data-stu-id="4d610-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="4d610-162">将**手动更新**设置至**是**</span><span class="sxs-lookup"><span data-stu-id="4d610-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="4d610-163">在**位置**框中，输入“退货”。</span><span class="sxs-lookup"><span data-stu-id="4d610-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="4d610-164">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="4d610-165">下图显示了旧金山仓库库存库位设置过程。</span><span class="sxs-lookup"><span data-stu-id="4d610-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![库存库位设置示例](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="4d610-167">完成仓库设置</span><span class="sxs-lookup"><span data-stu-id="4d610-167">Complete warehouse setup</span></span>

<span data-ttu-id="4d610-168">若要完成仓库设置，请遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="4d610-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="4d610-169">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="4d610-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="4d610-170">选择您之前创建的仓库。</span><span class="sxs-lookup"><span data-stu-id="4d610-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="4d610-171">在操作窗格上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="4d610-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="4d610-172">在**库存和仓库管理**下面：</span><span class="sxs-lookup"><span data-stu-id="4d610-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="4d610-173">将**默认收货库位**设置为上面创建的默认库位。</span><span class="sxs-lookup"><span data-stu-id="4d610-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="4d610-174">将**默认发货库位**设置为上面创建的默认库位。</span><span class="sxs-lookup"><span data-stu-id="4d610-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="4d610-175">在**地址**部分下面，输入仓库地址。</span><span class="sxs-lookup"><span data-stu-id="4d610-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="4d610-176">在**零售**部分下面：</span><span class="sxs-lookup"><span data-stu-id="4d610-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="4d610-177">在**默认退货位置**框中，输入先前创建的退货位置。</span><span class="sxs-lookup"><span data-stu-id="4d610-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="4d610-178">将**商店**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="4d610-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="4d610-179">将**重量** 设置为 **1.00**。</span><span class="sxs-lookup"><span data-stu-id="4d610-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="4d610-180">在**存储维度**框中，输入先前创建的默认位置。</span><span class="sxs-lookup"><span data-stu-id="4d610-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="4d610-181">在**仓库**部分下面，将**实际负库存**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="4d610-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="4d610-182">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="4d610-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4d610-183">下图显示了已配置仓库的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4d610-183">The following image shows details for a configured warehouse.</span></span>

![已配置仓库示例](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="4d610-185">其他资源</span><span class="sxs-lookup"><span data-stu-id="4d610-185">Additional resources</span></span>

[<span data-ttu-id="4d610-186">仓库管理概览</span><span class="sxs-lookup"><span data-stu-id="4d610-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="4d610-187">渠道概览</span><span class="sxs-lookup"><span data-stu-id="4d610-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4d610-188">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="4d610-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="4d610-189">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="4d610-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="4d610-190">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="4d610-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="4d610-191">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="4d610-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





