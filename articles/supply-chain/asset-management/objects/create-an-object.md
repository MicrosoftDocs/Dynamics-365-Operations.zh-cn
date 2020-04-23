---
title: 创建资产
description: 本主题介绍如何在资产管理中创建资产。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f734def69ff50549acae1506015ce9b23a1b8a93
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209896"
---
# <a name="create-an-asset"></a><span data-ttu-id="0471f-103">创建资产</span><span class="sxs-lookup"><span data-stu-id="0471f-103">Create an asset</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0471f-104">本主题介绍如何在资产管理中创建资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-104">This topic describes how to create an asset in Asset Management.</span></span>

1. <span data-ttu-id="0471f-105">单击**资产管理** > **常用** > **资产** > **所有资产**或**有效资产**。</span><span class="sxs-lookup"><span data-stu-id="0471f-105">Click **Asset management** > **Common** > **assets** > **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="0471f-106">单击**新建**按钮。</span><span class="sxs-lookup"><span data-stu-id="0471f-106">Click the **New** button.</span></span>
3. <span data-ttu-id="0471f-107">在**创建资产**对话框中，插入与**资产**（资产 ID）和资产名称有关的数据。</span><span class="sxs-lookup"><span data-stu-id="0471f-107">In the **Create assets** dialog, insert data regarding **Asset** (the asset ID) and the asset name.</span></span> <span data-ttu-id="0471f-108">在**生效**字段中选择资产的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0471f-108">Select date and time for the asset in the **Effective** field.</span></span> <span data-ttu-id="0471f-109">从该日期开始，您可以在功能位置安装该资产，还可以在资产结构中移动和替换该资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-109">From that date, you are able to install the asset on a functional location as well as move and replace the asset in an asset structure.</span></span>
4. <span data-ttu-id="0471f-110">在**资产类型**字段中，选择资产的资产类型（必填字段）。</span><span class="sxs-lookup"><span data-stu-id="0471f-110">In the **Asset type** field, select the asset type for the asset (mandatory field).</span></span> <span data-ttu-id="0471f-111">如果需要，为资产选择**资产制造商**和**资产模型**。</span><span class="sxs-lookup"><span data-stu-id="0471f-111">If required, select **Asset manufacturer** and **Asset model** for the asset.</span></span> <span data-ttu-id="0471f-112">如果仅设置了一个产品，则将在**资产制造商**字段中自动选择该产品。</span><span class="sxs-lookup"><span data-stu-id="0471f-112">If only one product has been set up, that product is automatically selected in the **Asset manufacturer** field.</span></span> <span data-ttu-id="0471f-113">**资产制造商**和**资产模型**字段中可供选择的选项取决于[资产制造商和模型](../setup-for-objects/product-and-model.md)中的设置。</span><span class="sxs-lookup"><span data-stu-id="0471f-113">The selections available in the **Asset manufacturer** and **Asset model** fields depend on the setup in [Asset manufacturers and models](../setup-for-objects/product-and-model.md).</span></span>
5. <span data-ttu-id="0471f-114">在**父资产**组中，**资产**字段默认为空。</span><span class="sxs-lookup"><span data-stu-id="0471f-114">In the **Parent asset** group, the **Asset** field is blank as default.</span></span> <span data-ttu-id="0471f-115">如果需要，可以选择父资产，然后，将自动填写**父资产**组中的所有字段。</span><span class="sxs-lookup"><span data-stu-id="0471f-115">If required, you can select a parent asset, and then all fields in the **Parent asset** group will automatically be filled out.</span></span>
>[!NOTE]  
><span data-ttu-id="0471f-116">选择父资产时，有两个或三个选项卡可用：**我的资产**选项卡中包含与可能将您（即已登录系统的维护工人）分配给的功能位置关联的资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-116">When you select a parent asset, two or three tabs are available: The **My assets** tab contains assets related to the functional locations to which you (the maintenance worker who is logged on the system) may be allocated.</span></span> <span data-ttu-id="0471f-117">如果未在[维护工人和工作人员组](../setup-for-objects/workers-and-worker-groups.md)窗体中为维护工人设置任何功能位置，则不显示**我的资产**选项卡。</span><span class="sxs-lookup"><span data-stu-id="0471f-117">If no functional locations are set up on a maintenance worker in the [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) form, the **My assets** tab will not be visible.</span></span> <span data-ttu-id="0471f-118">**有效资产**选项卡中包含资产生命周期状态为“有效”的所有资产的列表。</span><span class="sxs-lookup"><span data-stu-id="0471f-118">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="0471f-119">**资产视图**选项卡显示功能位置及其中安装的资产的树视图。</span><span class="sxs-lookup"><span data-stu-id="0471f-119">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="0471f-120">将在**资产**组 > **功能位置**字段中为资产推荐您设置的默认功能位置。</span><span class="sxs-lookup"><span data-stu-id="0471f-120">The default functional location you have set up is suggested for the asset in the **Asset** group > **Functional location** field.</span></span> <span data-ttu-id="0471f-121">如果需要，选择其他功能位置。</span><span class="sxs-lookup"><span data-stu-id="0471f-121">Select another functional location, if required.</span></span>

>[!NOTE]
><span data-ttu-id="0471f-122">如果需要，可以在创建资产之后将其安装到其他功能位置。</span><span class="sxs-lookup"><span data-stu-id="0471f-122">After you have created an asset, you can install it on another functional location, if required.</span></span> <span data-ttu-id="0471f-123">只能在功能位置安装顶级资产（即当前无父资产的资产）。</span><span class="sxs-lookup"><span data-stu-id="0471f-123">Only top-level assets (assets without a current parent asset) can be installed on a functional location.</span></span> <span data-ttu-id="0471f-124">这表示在所选功能位置安装顶级资产和任何子资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-124">This means that you install the top level as well as any child assets on the selected functional location.</span></span> <span data-ttu-id="0471f-125">请阅读[功能位置简介](../functional-locations/introduction-to-functional-locations.md)中有关在功能位置安装资产的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0471f-125">Read more about installing assets on functional locations in [Introduction to functional locations](../functional-locations/introduction-to-functional-locations.md).</span></span>

7. <span data-ttu-id="0471f-126">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0471f-126">Click **OK**.</span></span>
8. <span data-ttu-id="0471f-127">在**所有资产**列表中选择资产，然后单击**编辑**按钮向资产添加更多信息。</span><span class="sxs-lookup"><span data-stu-id="0471f-127">Select the asset in the **All Assets** list and click the **Edit** button to add further information to the asset.</span></span>

## <a name="general-information"></a><span data-ttu-id="0471f-128">一般信息</span><span class="sxs-lookup"><span data-stu-id="0471f-128">General information</span></span>

<span data-ttu-id="0471f-129">将在**功能位置**字段中显示与资产关联的功能位置。</span><span class="sxs-lookup"><span data-stu-id="0471f-129">The functional location to which the asset is related is shown in the **Functional location** field.</span></span> <span data-ttu-id="0471f-130">如果资产是父资产，则将在**子项**字段中显示与资产关联的父项的数量。</span><span class="sxs-lookup"><span data-stu-id="0471f-130">If the asset is a parent asset, the number of children related to the asset is shown in the **Children** field.</span></span> <span data-ttu-id="0471f-131">如果资产是现有资产的子资产，则将在**父级**字段中显示父资产的 ID。</span><span class="sxs-lookup"><span data-stu-id="0471f-131">If the asset is a sub asset to an existing asset, the ID of the parent asset is shown in the **Parent** field.</span></span>

<span data-ttu-id="0471f-132">可编辑与资产有关的**资产制造商**和**资产模型**信息，用于管理备件、备用备件和作业类型默认值。</span><span class="sxs-lookup"><span data-stu-id="0471f-132">You can edit **Asset manufacturer** and **Asset model** information on the asset, which is used to manage spare parts, alternative spare parts, and job type defaults.</span></span> <span data-ttu-id="0471f-133">有关详细信息，请参阅[资产制造商和模型](../setup-for-objects/product-and-model.md)。</span><span class="sxs-lookup"><span data-stu-id="0471f-133">Refer to [Asset manufacturers and models](../setup-for-objects/product-and-model.md) for more information.</span></span> <span data-ttu-id="0471f-134">如果需要，可添加有关**模型年份**和**序列号**有关的信息。</span><span class="sxs-lookup"><span data-stu-id="0471f-134">You can also add information about **Model year** and **Serial number**, if required.</span></span>

<span data-ttu-id="0471f-135">**当前生命周期状态**用于定义资产有效还是无效。</span><span class="sxs-lookup"><span data-stu-id="0471f-135">**Current lifecycle state** is used to define if the asset is active or inactive.</span></span> <span data-ttu-id="0471f-136">创建资产时，此阶段设置设置为资产阶段组中的第一个阶段。</span><span class="sxs-lookup"><span data-stu-id="0471f-136">When creating an asset, the stage is always set to the first stage in the asset stage group.</span></span> <span data-ttu-id="0471f-137">准备好激活资产之后，单击**更新资产状态**，选择已定义为“资产有效”的生命周期状态，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="0471f-137">When you are ready to activate an asset, click **Update asset state**, and select the lifecycle state that you have defined as "asset active", and click **OK**.</span></span>

<span data-ttu-id="0471f-138">**注意：** 如果资产设置为“无效”，则不再可以为该资产创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="0471f-138">**Note:** When an asset is set to "inactive", it is no longer possible to create work orders for the asset.</span></span> <span data-ttu-id="0471f-139">此外，也不能为无效资产计划预防性维护。</span><span class="sxs-lookup"><span data-stu-id="0471f-139">Also, you cannot schedule preventive maintenance jobs for an inactive asset.</span></span>

<span data-ttu-id="0471f-140">**服务级别**和**关键性**字段与为资产创建的工作订单关联。</span><span class="sxs-lookup"><span data-stu-id="0471f-140">The **Service level** and **Criticality** fields relate to work orders created for the asset.</span></span> <span data-ttu-id="0471f-141">这些字段显示为资产的当前设置计算的**服务级别**和**关键性**数量。</span><span class="sxs-lookup"><span data-stu-id="0471f-141">The fields show the **Service level** and **Criticality** numbers calculated for the current setup for the asset.</span></span> <span data-ttu-id="0471f-142">有关设置这些值的信息，请参阅[资产服务级别](../setup-for-objects/object-priorities.md)和[资产关键性类型](../setup-for-objects/object-criticalities.md)。</span><span class="sxs-lookup"><span data-stu-id="0471f-142">Refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md) regarding setup of those values.</span></span>

## <a name="asset"></a><span data-ttu-id="0471f-143">资产</span><span class="sxs-lookup"><span data-stu-id="0471f-143">Asset</span></span>

<span data-ttu-id="0471f-144">可为资产选择**资源**。</span><span class="sxs-lookup"><span data-stu-id="0471f-144">You can select a **Resource** for the asset.</span></span> <span data-ttu-id="0471f-145">选择的资源决定为工作订单排产使用哪个日历。</span><span class="sxs-lookup"><span data-stu-id="0471f-145">The resource selection determines which calendar is used for work order scheduling.</span></span> <span data-ttu-id="0471f-146">资源选择通常用于固定资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-146">Resource selection is often used for fixed assets.</span></span> <span data-ttu-id="0471f-147">资源和资源组在**组织管理** > **资源** > **资源组**或**资源**中设置。</span><span class="sxs-lookup"><span data-stu-id="0471f-147">Resources and resource groups are set up in **Organization administration** > **Resources** > **Resource groups** or **Resources**.</span></span>

<span data-ttu-id="0471f-148">在**固定资产编号**字段中，可选择要与资产关联的固定资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-148">In the **Fixed assets number** field, you can select a fixed asset to be related to the asset.</span></span> <span data-ttu-id="0471f-149">如果资产与投资项目关联，则此项相关。</span><span class="sxs-lookup"><span data-stu-id="0471f-149">This is relevant if your asset is related to an investment project.</span></span>

- <span data-ttu-id="0471f-150">如果资产与固定资产关联，则可创建要用于与投资项目关联的工作订单的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="0471f-150">If the asset is related to a fixed asset, you can create a work order type to be used for work orders related to an investment project.</span></span> 
- <span data-ttu-id="0471f-151">有关资产的固定资产的信息与 Dynamics 365 Supply Chain Management 中的**固定资产**模块关联。</span><span class="sxs-lookup"><span data-stu-id="0471f-151">Information about fixed assets for an asset is related to the **Fixed assets** module in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0471f-152">这表示在**固定资产** > **固定资产** > **固定资产**中，可获取可能与固定资产关联的资产管理项目的概览，方法是在列表中选择资产，然后查看**相关信息**窗格 > **关联项目**部分中的内容。</span><span class="sxs-lookup"><span data-stu-id="0471f-152">This means that in **Fixed assets** > **Fixed assets** > **Fixed assets**, you can get an overview of the Asset Management projects that may be related to a fixed asset by selecting the asset in the list and viewing the contents in the **Related information** pane > **Associated projects** section.</span></span>


## <a name="details"></a><span data-ttu-id="0471f-153">明细</span><span class="sxs-lookup"><span data-stu-id="0471f-153">Details</span></span>

<span data-ttu-id="0471f-154">在**生效日期**字段中，将显示您将资产生命周期状态更新为有效状态的日期（有关设置资产生命周期状态的信息，请参阅[资产生命周期状态](../setup-for-objects/object-stages.md)）。</span><span class="sxs-lookup"><span data-stu-id="0471f-154">In the **Active from** field, the date on which you updated the asset lifecycle state to an active state (refer to [Asset lifecycle states](../setup-for-objects/object-stages.md) regarding setup of asset lifecycle states), is shown.</span></span> <span data-ttu-id="0471f-155">如果资产不再有效，并且您已将资产生命周期状态更新为无效的生命周期状态，则在**生效日期**字段中显示资产的失效日期。</span><span class="sxs-lookup"><span data-stu-id="0471f-155">If the asset is no longer active, and you have updated the asset lifecycle state to an inactive lifecycle state, the date from which the asset is inactive is shown in the **Active to** field.</span></span> <span data-ttu-id="0471f-156">如果需要，您可以手动更改这些日期。</span><span class="sxs-lookup"><span data-stu-id="0471f-156">If required, you can manually change those dates.</span></span>

<span data-ttu-id="0471f-157">如果需要，您可以在**重置日期**字段中插入预期的资产重置日期。</span><span class="sxs-lookup"><span data-stu-id="0471f-157">If required, you can insert an expected date for replacement of the asset in the **Replacement date** field.</span></span> <span data-ttu-id="0471f-158">可以在**替换值**字段中插入用于替换资产的估计值。</span><span class="sxs-lookup"><span data-stu-id="0471f-158">An estimated value for replacing the asset can be inserted in the **Replacement value** field.</span></span> <span data-ttu-id="0471f-159">示例：可使用替换信息将其与资产的维护成本进行比较，并在以后现有资产的维护成本快速增加时，决定购买新资产。</span><span class="sxs-lookup"><span data-stu-id="0471f-159">Example: You can use replacement information to compare it with the costs of maintaining an asset, and subsequently make a decision for purchasing a new asset if maintenance costs on the existing asset increase rapidly.</span></span>

## <a name="notes"></a><span data-ttu-id="0471f-160">注释</span><span class="sxs-lookup"><span data-stu-id="0471f-160">Notes</span></span>

<span data-ttu-id="0471f-161">可在**注释**快速选项卡上添加与资产有关的注释。</span><span class="sxs-lookup"><span data-stu-id="0471f-161">You can add notes related to the asset on the **Notes** FastTab.</span></span> <span data-ttu-id="0471f-162">如果要向注释添加用户信息和日期/时间戳，请在撰写注释之前，单击**添加时间戳**按钮。</span><span class="sxs-lookup"><span data-stu-id="0471f-162">Click the **Add timestamp** button before you write the note, if you want to add user information and a date/timestamp to the note.</span></span>

## <a name="attributes"></a><span data-ttu-id="0471f-163">属性</span><span class="sxs-lookup"><span data-stu-id="0471f-163">Attributes</span></span>

<span data-ttu-id="0471f-164">在此快速选项卡上，可设置资产属性的值。</span><span class="sxs-lookup"><span data-stu-id="0471f-164">On this FastTab, you can set values for asset attributes.</span></span> <span data-ttu-id="0471f-165">这些属性可用于描述与资产有关的特性或特征，例如，大小、重量或机器配置。</span><span class="sxs-lookup"><span data-stu-id="0471f-165">These attributes can be used to describe properties or characteristics pertinent to the asset, for example, size, weight, or machine configuration.</span></span>

<span data-ttu-id="0471f-166">单击**添加行**并选择属性类型。</span><span class="sxs-lookup"><span data-stu-id="0471f-166">Click **Add line** and select the attribute type.</span></span> <span data-ttu-id="0471f-167">接下来，添加与属性类型有关的**值**，然后保存记录。</span><span class="sxs-lookup"><span data-stu-id="0471f-167">Next, insert the **Value** related to the attribute type and save the record.</span></span>

>[!NOTE] 
><span data-ttu-id="0471f-168">可在**资产属性**和**资产属性概览**中获取资产属性类型及其与资产之间的关联的概览。</span><span class="sxs-lookup"><span data-stu-id="0471f-168">You can get an overview of asset attribute types and their relation to the assets in **Asset attribute** and **Asset attribute overview**.</span></span> <span data-ttu-id="0471f-169">有关详细信息，请参阅[资产属性概述](../objects/object-specification-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0471f-169">Refer to [Asset attribute overview](../objects/object-specification-overview.md) for more information.</span></span>

## <a name="vendor"></a><span data-ttu-id="0471f-170">供应商</span><span class="sxs-lookup"><span data-stu-id="0471f-170">Vendor</span></span>

<span data-ttu-id="0471f-171">在**供应商**快速选项卡上，选择资产的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="0471f-171">On the **Vendor** FastTab, select a vendor account for the asset.</span></span> <span data-ttu-id="0471f-172">此外，如果已授予了供应商保修，则可在此处插入保修信息。</span><span class="sxs-lookup"><span data-stu-id="0471f-172">Also, if a vendor warranty has been granted, you can insert warranty information here.</span></span>

## <a name="address"></a><span data-ttu-id="0471f-173">地址</span><span class="sxs-lookup"><span data-stu-id="0471f-173">Address</span></span>

<span data-ttu-id="0471f-174">在**地址**快速选项卡上，可以插入设备的地址。</span><span class="sxs-lookup"><span data-stu-id="0471f-174">On the **Address** FastTab, you can insert the address of the equipment.</span></span> <span data-ttu-id="0471f-175">如果未在资产中插入地址，但是父资产有地址，则资产使用父资产的地址。</span><span class="sxs-lookup"><span data-stu-id="0471f-175">If no address is inserted on the asset, the asset uses the address of a parent asset, if the parent asset has an address.</span></span> <span data-ttu-id="0471f-176">如果在资产层次结构中没有地址与资产或任何父项关联，则可使用安装资产的功能位置的地址。</span><span class="sxs-lookup"><span data-stu-id="0471f-176">If no address is related to the asset or any parents in the asset hierarchy, the address of the functional location on which the asset is installed may be used.</span></span> <span data-ttu-id="0471f-177">如果未将地址与该功能位置关联，则对资产使用父功能位置的地址。</span><span class="sxs-lookup"><span data-stu-id="0471f-177">If that functional location does not have an address related to it, the address of the parent functional location is used on the asset.</span></span>

## <a name="asset-management-plans"></a><span data-ttu-id="0471f-178">资产管理计划</span><span class="sxs-lookup"><span data-stu-id="0471f-178">Asset management plans</span></span>

<span data-ttu-id="0471f-179">维护计划用于为资产计划固定时间间隔的预防性维护。</span><span class="sxs-lookup"><span data-stu-id="0471f-179">Maintenance plans are used for scheduling preventive maintenance jobs at regular intervals on the asset.</span></span> <span data-ttu-id="0471f-180">可在此快速选项卡上为所选资产设置维护计划行。</span><span class="sxs-lookup"><span data-stu-id="0471f-180">On this FastTab, you can set up maintenance plan lines for the selected asset.</span></span> <span data-ttu-id="0471f-181">可以为各资产设置维护阶段，在这些阶段，需要按定期时间间隔执行相似任务。</span><span class="sxs-lookup"><span data-stu-id="0471f-181">Maintenance rounds can be set up for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="0471f-182">在**功能位置维护计划**选项卡上，可以查看与安装资产的功能位置关联的维护计划。</span><span class="sxs-lookup"><span data-stu-id="0471f-182">On the **Functional location maintenance plans** tab, you see the maintenance plans related to the functional location on which the asset is installed.</span></span>

>[!NOTE]
><span data-ttu-id="0471f-183">如果在**所有资产**中删除与资产关联的维护计划行或维护阶段，也将自动删除已根据维护计划或维护阶段创建且状态为“已创建”的所有维护计划。</span><span class="sxs-lookup"><span data-stu-id="0471f-183">If you delete a maintenance plan line or a maintenance round related to an asset in **All Asset**, you also automatically delete all maintenance schedules with status "Created" that have been created based on that maintenance plan or maintenance round.</span></span>

## <a name="functional-location-maintenance-plans"></a><span data-ttu-id="0471f-184">功能位置维护计划</span><span class="sxs-lookup"><span data-stu-id="0471f-184">Functional location maintenance plans</span></span>

<span data-ttu-id="0471f-185">在此快速选项卡上，可获取与安装资产的功能位置关联的维护计划的概览。</span><span class="sxs-lookup"><span data-stu-id="0471f-185">On this FastTab, you get an overview of the maintenance plans related to the functional location on which the asset is installed.</span></span>

## <a name="maintenance-rounds"></a><span data-ttu-id="0471f-186">维护阶段</span><span class="sxs-lookup"><span data-stu-id="0471f-186">Maintenance rounds</span></span>

<span data-ttu-id="0471f-187">在此快速选项卡上，可添加或删除与资产关联的维护阶段。</span><span class="sxs-lookup"><span data-stu-id="0471f-187">On this FastTab, you can add or remove maintenance rounds, which are related to the asset.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="0471f-188">财务维度</span><span class="sxs-lookup"><span data-stu-id="0471f-188">Financial dimensions</span></span>

<span data-ttu-id="0471f-189">可为资产选择财务维度。</span><span class="sxs-lookup"><span data-stu-id="0471f-189">You can select financial dimensions for the asset.</span></span>
