---
title: 创建功能位置
description: 本主题介绍如何在资产管理中创建功能位置。
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d1f9714f57d19a13444fea9864d72c3341b15ea
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783100"
---
# <a name="create-functional-locations"></a><span data-ttu-id="b6b4f-103">创建功能位置</span><span class="sxs-lookup"><span data-stu-id="b6b4f-103">Create functional locations</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b6b4f-104">本主题介绍如何在资产管理中创建功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-104">This topic explains how to create a functional location in Asset Management.</span></span>

<span data-ttu-id="b6b4f-105">创建功能位置结构时，请注意，创建功能位置之后，不能从原始位置移动该功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-105">When you create a functional location structure, be aware once you have created a functional location, you cannot move it from the original location.</span></span> <span data-ttu-id="b6b4f-106">这意味着在资产管理中开始创建功能位置之前，应注意功能位置的结构。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-106">This means that you should carefully consider the structure of your functional locations before you start creating them in Asset Management.</span></span> <span data-ttu-id="b6b4f-107">如果对某个功能位置不满意，并且尚未使用该功能位置，可将其删除。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-107">If you regret a functional location, you can delete it, provided that it has not yet been taken into use.</span></span>

<span data-ttu-id="b6b4f-108">若要能够使用功能位置，请首先创建两个功能位置“类别”：</span><span class="sxs-lookup"><span data-stu-id="b6b4f-108">To be able to work with functional locations, you start by creating two "categories" of functional locations:</span></span>

- <span data-ttu-id="b6b4f-109">创建*一个*不包含子位置的默认功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-109">Create *one* default functional location with not sub locations.</span></span> <span data-ttu-id="b6b4f-110">此功能位置仅在新建资产时用作资产的标准位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-110">This functional location is used only as the standard location for assets when you create new assets.</span></span>  
- <span data-ttu-id="b6b4f-111">创建管理公司中的维护作业所需功能位置结构。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-111">Create the functional location structures required for managing maintenance jobs in your company.</span></span>

## <a name="create-a-default-functional-location"></a><span data-ttu-id="b6b4f-112">创建默认功能位置</span><span class="sxs-lookup"><span data-stu-id="b6b4f-112">Create a default functional location</span></span>

<span data-ttu-id="b6b4f-113">使用功能位置时，首先创建新建资产时要使用的一个默认位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-113">When you use functional locations, start by creating one default location to be used when you create new assets.</span></span> <span data-ttu-id="b6b4f-114">此功能位置是您在**资产管理** > **设置** > **资产管理参数** > **资产**链接 > **默认功能位置**字段中选择的功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-114">This functional location is the one you select in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Default functional location** field.</span></span> <span data-ttu-id="b6b4f-115">创建新资产，但尚未为这些资产设置功能位置结构时，可使用默认功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-115">The default functional location can be used when you create new assets, and you have not yet set up a functional location structure for those assets.</span></span>

1. <span data-ttu-id="b6b4f-116">选择**资产管理** > **常用** > **功能位置** > **所有功能位置**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-116">Select **Asset management** > **Common** > **Functional locations** > **All Functional locations**.</span></span>  
2. <span data-ttu-id="b6b4f-117">在**所有功能位置**中，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-117">In **All functional locations**, select **New**.</span></span>
3. <span data-ttu-id="b6b4f-118">在**功能位置**字段中插入一个 ID（如“0000”或“默认”），以指示这是特殊功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-118">Insert an ID in the **Functional location** field, for example, "0000" or "Default", to indicate that this is a special functional location.</span></span>
4. <span data-ttu-id="b6b4f-119">在**名称**字段中插入默认功能位置的名称。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-119">Insert name for the default functional location in the **Name** field.</span></span>
5. <span data-ttu-id="b6b4f-120">请*勿*在**父级**字段中选择父级 – 请将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-120">Do *not* select a parent in the **Parent** field – leave this field blank.</span></span>
6. <span data-ttu-id="b6b4f-121">在**功能位置类型**字段中，选择要用于默认功能位置的功能位置类型。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-121">In the **Functional location type** field, select the functional location type to be used for the default functional location.</span></span> <span data-ttu-id="b6b4f-122">有关如何设置功能位置类型的详细信息，请参阅[功能位置类型](../setup-for-functional-locations/functional-location-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-122">See [Functional location types](../setup-for-functional-locations/functional-location-types.md) for more information on how to set up functional location types.</span></span>
7. <span data-ttu-id="b6b4f-123">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-123">Select **OK**.</span></span> <span data-ttu-id="b6b4f-124">不应向此功能位置添加更多数据，因为在您在公司使用的功能位置中安装资产之前，该功能位置用作新资产的临时位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-124">You should not add further data to this functional location as it is only used as a temporary location for new assets until you install the assets on the functional locations used by your company.</span></span>

## <a name="create-functional-locations"></a><span data-ttu-id="b6b4f-125">创建功能位置</span><span class="sxs-lookup"><span data-stu-id="b6b4f-125">Create functional locations</span></span>

<span data-ttu-id="b6b4f-126">以下过程介绍如何创建公司中的维护管理所需功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-126">The following procedure describes how you create the functional locations required for maintenance management in your company.</span></span>

1. <span data-ttu-id="b6b4f-127">选择**资产管理** > **常用** > **功能位置** > **所有功能位置**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-127">Select **Asset management** > **Common** > **Functional locations** > **All Functional locations**.</span></span> <span data-ttu-id="b6b4f-128">可从网格视图或详细信息视图创建功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-128">You can create a functional location from grid view or details view.</span></span>
2. <span data-ttu-id="b6b4f-129">选择**新建**按钮。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-129">Select the **New** button.</span></span>
3. <span data-ttu-id="b6b4f-130">在**功能位置**字段中插入一个 ID。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-130">Insert an ID in the **Functional location** field.</span></span>
4. <span data-ttu-id="b6b4f-131">在**名称**字段中插入功能位置的名称。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-131">Insert a name for the functional location in the **Name** field.</span></span>
5. <span data-ttu-id="b6b4f-132">如果功能位置是结构中的子位置，请在**父级**字段中选择父位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-132">If the functional location is a sub location in a structure, select the parent location in the **Parent** field.</span></span>
6. <span data-ttu-id="b6b4f-133">在**功能位置类型**字段中选择一个类型。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-133">Select a type in the **Functional location type** field.</span></span>
7. <span data-ttu-id="b6b4f-134">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-134">Select **OK**.</span></span>
8. <span data-ttu-id="b6b4f-135">选择功能位置，然后单击**编辑**按钮添加更多信息。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-135">Select the functional location and click the **Edit** button to add further information.</span></span>

>[!NOTE]
><span data-ttu-id="b6b4f-136">可能必须为某个功能位置创建所有子位置，然后在开始安装资产之前更改功能位置生命周期状态，具体取决于您的功能位置生命周期状态设置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-136">Depending on your setup of functional location lifecycle states, you may have to create all sub locations for a functional location, and then change the functional location lifecycle state before you can start installing assets.</span></span> <span data-ttu-id="b6b4f-137">有关资产安装的详细信息，请参阅[在功能位置安装资产](../functional-locations/install-objects-on-functional-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-137">See [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md) for more information on asset installation.</span></span> <span data-ttu-id="b6b4f-138">请参阅[功能位置生命周期状态](../setup-for-functional-locations/functional-location-stages.md)了解有关功能位置生命周期状态设置的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-138">See [Functional location lifecycle states](../setup-for-functional-locations/functional-location-stages.md) to learn more about setup of functional location lifecycle states.</span></span>

<span data-ttu-id="b6b4f-139">在“详细信息”视图中，可以看到快速选项卡，可在其中添加和编辑有关功能位置的信息。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-139">In Details view, you will see FastTabs on which you can add and edit information about the functional location.</span></span>

## <a name="general-information"></a><span data-ttu-id="b6b4f-140">常规信息</span><span class="sxs-lookup"><span data-stu-id="b6b4f-140">General Information</span></span>

<span data-ttu-id="b6b4f-141">此部分提供功能位置结构中的父信息和子信息的概述。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-141">This section provides an overview of parent and child information in the functional location structure.</span></span> <span data-ttu-id="b6b4f-142">在**详细信息**部分中，可以查看与功能位置有关的资产属性、维护计划和资产的数量。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-142">In the **Details** section, you can see the number of asset attributes, maintenance plans, and assets related to the functional location.</span></span> <span data-ttu-id="b6b4f-143">在**库存**部分中，可以选择功能位置关联的站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-143">In the **Inventory** section, you can select the site and warehouse to which the functional location is related.</span></span> <span data-ttu-id="b6b4f-144">站点和仓库与工作订单物料预测一起使用。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-144">Site and warehouse is used in connection with work order item forecasts.</span></span> <span data-ttu-id="b6b4f-145">创建物料预测时，将自动使用资产的功能位置中的站点和仓库信息。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-145">When creating an item forecast, site and warehouse information from the functional location of the asset is automatically used.</span></span> <span data-ttu-id="b6b4f-146">在**生命周期状态**部分中，将显示有关功能位置生命周期状态的信息。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-146">In the **Lifecycle state** section, information about the functional location lifecycle state is displayed.</span></span>

## <a name="installed-assets"></a><span data-ttu-id="b6b4f-147">安装资产</span><span class="sxs-lookup"><span data-stu-id="b6b4f-147">Installed assets</span></span>

<span data-ttu-id="b6b4f-148">有关资产安装的详细信息，请参考[在功能位置安装资产](../functional-locations/install-objects-on-functional-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-148">Refer to [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md) for more information on asset installation.</span></span> <span data-ttu-id="b6b4f-149">可使用此快速选项卡上的**视图**按钮在快速选项卡上显示更多字段。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-149">You can use the **View** button on this FastTab to show more fields on the FastTab.</span></span> <span data-ttu-id="b6b4f-150">可在网格中显示**生效日期**和**子资产**字段。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-150">The **Valid from** and **Sub asset** fields can be shown in the grid.</span></span>

## <a name="asset-attribute-requirements"></a><span data-ttu-id="b6b4f-151">资产属性要求</span><span class="sxs-lookup"><span data-stu-id="b6b4f-151">Asset attribute requirements</span></span>

<span data-ttu-id="b6b4f-152">在此快速选项卡上，可添加功能位置安装的资产的具体属性属性要求。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-152">On this FastTab you can add specific attribute requirements for the assets that you install on the functional location.</span></span> <span data-ttu-id="b6b4f-153">这些要求仅供参考。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-153">These requirements are for information purposes only.</span></span> <span data-ttu-id="b6b4f-154">不会阻止安装具有其他属性要求的资产。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-154">They do not prevent you from installing assets with other attribute requirements.</span></span> <span data-ttu-id="b6b4f-155">选择**添加行**并选择属性类型。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-155">Select **Add line** and select the attribute type.</span></span> <span data-ttu-id="b6b4f-156">然后插入相关**值**，在**阈值条件**字段中选择一个阈值，然后保存记录。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-156">Then you insert the relevant **Value**, select a threshold in the **Threshold criteria** field and save the record.</span></span>

## <a name="maintenance-plans-and-maintenance-rounds"></a><span data-ttu-id="b6b4f-157">维护计划和维护阶段</span><span class="sxs-lookup"><span data-stu-id="b6b4f-157">Maintenance plans and Maintenance rounds</span></span>

<span data-ttu-id="b6b4f-158">可在此处向功能位置添加维护计划和维护阶段，包括开始日期。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-158">Here you can add maintenance plans and maintenance rounds to the functional location, including a start date.</span></span> <span data-ttu-id="b6b4f-159">可能为功能位置中安装的资产设置了其他维护计划。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-159">The assets installed on a functional location may have other maintenance plans set up.</span></span> <span data-ttu-id="b6b4f-160">所有维护计划和维护阶段都可用于为功能位置及其当前安装的资产安排资产日历条目。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-160">All maintenance plans and maintenance rounds can be used for scheduling asset calendar entries for a functional location and its currently installed assets.</span></span>

>[!NOTE]
><span data-ttu-id="b6b4f-161">如果在安排维护计划之后更新了**所有功能位置** 详细信息视图 > **维护计划**快速选项卡中维护计划内的资产类型、资产品牌和资产模型的设置，则自动删除与功能位置有关的现有维护计划条目。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-161">If you update the setup of asset types, asset brands, and asset models on maintenance plans in **All functional locations** detail view > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="b6b4f-162">若要创建新计划条目（与功能位置中已更新的维护计划设置对应），则必须为该功能位置运行新的维护计划安排。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-162">In order to create new schedule entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> 

## <a name="address"></a><span data-ttu-id="b6b4f-163">地址</span><span class="sxs-lookup"><span data-stu-id="b6b4f-163">Address</span></span>

<span data-ttu-id="b6b4f-164">在**地址**快速选项卡中插入功能位置地址。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-164">Insert the functional location address on the **Address** FastTab.</span></span> <span data-ttu-id="b6b4f-165">将继承功能位置的地址，这表示如果没有为子位置定义地址，则使用父位置的地址。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-165">Addresses on functional locations are inherited, meaning if a sub location has no address defined, the address of the parent location is used.</span></span>

## <a name="workers"></a><span data-ttu-id="b6b4f-166">工作人员</span><span class="sxs-lookup"><span data-stu-id="b6b4f-166">Workers</span></span>

<span data-ttu-id="b6b4f-167">在此快速选项卡上，可添加与功能位置有关的工人，并且可以选择功能位置充当该工人的主功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-167">On this FastTab, you can add workers affiliated with the functional location, and you can select a functional location as primary for the worker.</span></span> 

## <a name="attributes"></a><span data-ttu-id="b6b4f-168">属性</span><span class="sxs-lookup"><span data-stu-id="b6b4f-168">Attributes</span></span>

<span data-ttu-id="b6b4f-169">在此快速选项卡上，可设置功能位置属性的值。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-169">On this FastTab, you can set values for functional location attributes.</span></span> <span data-ttu-id="b6b4f-170">这些属性可用于描述与功能位置有关的属性或特征，例如，结构属性，构建类型，区域描述，或地面上或下的位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-170">These attributes can be used to describe properties or characteristics pertinent to the functional location, for example, structural properties, building type, area descriptions, or location above or under ground.</span></span>

<span data-ttu-id="b6b4f-171">选择**添加行**并选择属性类型。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-171">Select **Add line** and select the attribute type.</span></span> <span data-ttu-id="b6b4f-172">接下来，添加与属性类型有关的**值**，然后保存记录。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-172">Next, insert the **Value** related to the attribute type and save the record.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="b6b4f-173">财务维度</span><span class="sxs-lookup"><span data-stu-id="b6b4f-173">Financial dimensions</span></span>

<span data-ttu-id="b6b4f-174">可为功能位置选择财务维度。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-174">You can select financial dimensions for the functional location.</span></span> <span data-ttu-id="b6b4f-175">可设置[功能位置类型](../setup-for-functional-locations/functional-location-types.md)，以便自动更新功能位置中的财务维度。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-175">[Functional location types](../setup-for-functional-locations/functional-location-types.md) can be set up to allow for automatic update of financial dimensions from a functional location.</span></span> <span data-ttu-id="b6b4f-176">这意味着财务维度中安装的资产将自动获取功能位置的财务维度。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-176">This means that assets installed on a financial dimension automatically get the financial dimensions for the functional location.</span></span> <span data-ttu-id="b6b4f-177">如果需要不同成本中心，这非常有用，具体取决于位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-177">This is useful if you want different cost centers, depending on locations.</span></span>

<span data-ttu-id="b6b4f-178">如果在父功能位置更新与**站点**、**仓库**、**地址**和**财务维度**有关的数据，并且在更新期间进行了该选择，可相应更新相关子功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-178">When data regarding **Site**, **Warehouse**, **Address**, and **Financial dimensions** are updated on a parent functional location, the related sub functional locations can be updated accordingly if you make that selection during the update.</span></span> <span data-ttu-id="b6b4f-179">将打开一个对话框，为您提供更新选项。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-179">A dialog opens, providing you with the update options.</span></span>

## <a name="copy-a-functional-location-structure"></a><span data-ttu-id="b6b4f-180">复制功能位置结构</span><span class="sxs-lookup"><span data-stu-id="b6b4f-180">Copy a functional location structure</span></span>

<span data-ttu-id="b6b4f-181">如果公司有多个具有相似位置结构的功能位置，可使用资产管理中的复制功能快速创建一些相似的位置层次结构。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-181">If your company has several functional locations with similar location structures, you can use the copy function in Asset Management to quickly create a number of similar location hierarchies.</span></span> <span data-ttu-id="b6b4f-182">在整个结构中复制特定功能位置时，新位置或结构与复制的位置或结构同名。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-182">When you copy a specific functional location or an entire structure, the new location or structure has the same name as the one you copied.</span></span> <span data-ttu-id="b6b4f-183">完成复制过程后，可以轻松更改新功能位置的名称或其他设置，前提是为新功能位置选择的功能位置生命周期状态允许更改。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-183">After the copy procedure is done, you can easily change the name or other settings on the new functional location, provided that the functional location lifecycle state selected for the new functional location allows it.</span></span>

1. <span data-ttu-id="b6b4f-184">在**所有功能位置**中，选择要复制的功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-184">In **All functional locations**, select the functional location you want to copy.</span></span> <span data-ttu-id="b6b4f-185">例如，如果要复制整个功能位置结构（包括子位置），则选择顶级位置（即父级）。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-185">For example, you select a top location (parent) if you want to copy the entire functional location structure including sub locations.</span></span>
2. <span data-ttu-id="b6b4f-186">选择**复制功能位置结构**按钮。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-186">Select the **Copy functional location structure** button.</span></span> <span data-ttu-id="b6b4f-187">将在**复制自**字段中显示列表页中选择的位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-187">The location you selected in the list page is shown in the **Copy from** field.</span></span>
3. <span data-ttu-id="b6b4f-188">在**新功能位置**字段中插入新位置的名称。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-188">Insert the name of the new location in the **New functional location** field.</span></span>
4. <span data-ttu-id="b6b4f-189">仅当要创建的位置应该是现有功能位置结构的一部分时，才应在**粘贴位置的父级**字段中插入父 ID。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-189">In the **Parent to paste under** field, you should only insert a parent ID if the location you are creating should be part of an existing functional location structure.</span></span>
5. <span data-ttu-id="b6b4f-190">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-190">Click **OK**.</span></span> <span data-ttu-id="b6b4f-191">将在**所有功能位置**中显示新功能位置结构。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-191">The new functional location structure is shown in **All functional locations**.</span></span>

>[!NOTE]
><span data-ttu-id="b6b4f-192">复制功能位置结构时，将把新结构中的功能位置生命周期状态设置为您已经为功能位置创建的“第一个状态”。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-192">When you copy a functional location structure, functional location lifecycle states in the new structure are set to the "first state" that you have created for functional locations.</span></span> <span data-ttu-id="b6b4f-193">是否可使用**所有功能位置**中的**重命名**和**删除**按钮重命名或删除功能位置取决于功能位置的当前生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-193">Whether you can rename or delete a functional location using the **Rename** and **Delete** buttons in **All functional locations**, depends on the current lifecycle state of the functional location.</span></span>

## <a name="delete-a-functional-location"></a><span data-ttu-id="b6b4f-194">删除功能位置</span><span class="sxs-lookup"><span data-stu-id="b6b4f-194">Delete a Functional Location</span></span>

<span data-ttu-id="b6b4f-195">以下条件下可删除具有相关子位置的功能位置：尚未在尝试删除的任何功能位置安装资产，并且当前功能位置生命周期状态允许删除。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-195">A functional location with related sub locations can be deleted if no assets have been installed on any of the functional locations you are trying to delete, and if the current functional location lifecycle state allows it.</span></span>

1. <span data-ttu-id="b6b4f-196">在**所有功能位置**中，选择要删除的功能位置。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-196">In **All functional locations**, select the functional location you want to delete.</span></span>
2. <span data-ttu-id="b6b4f-197">如果需要，将功能位置更新为允许删除功能位置的功能位置生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-197">If required, update the functional location to a functional location lifecycle state that allows deletion of a functional location.</span></span>
3. <span data-ttu-id="b6b4f-198">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-198">Select **Delete**.</span></span>

>[!NOTE]
><span data-ttu-id="b6b4f-199">如果不能删除功能位置，可改为通过为此目的设置功能位置生命周期状态来处理删除。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-199">If you cannot delete a functional location, instead you can handle deletion by setting up a functional location lifecycle state for this purpose.</span></span> <span data-ttu-id="b6b4f-200">例如，可在**功能位置生命周期状态**窗体中设置“已报废”或“已删除”阶段，该阶段不应是活动阶段。</span><span class="sxs-lookup"><span data-stu-id="b6b4f-200">For example, you can set up a "Scrapped" or "Deleted" stage, which should not be an active stage, in the **Functional location lifecycle states** form.</span></span>
