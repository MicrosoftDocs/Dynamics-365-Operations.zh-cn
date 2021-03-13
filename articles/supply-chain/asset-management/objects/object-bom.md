---
title: 资产 BOM
description: 本主题介绍资产管理中的物料清单 (BOM)。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baaf516eb386c3cf63d72bf31800b8731121fe26
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019505"
---
# <a name="asset-boms"></a><span data-ttu-id="d4533-103">资产 BOM</span><span class="sxs-lookup"><span data-stu-id="d4533-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d4533-104">本主题介绍资产管理中的物料清单 (BOM)。</span><span class="sxs-lookup"><span data-stu-id="d4533-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="d4533-105">**资产 BOM** 也显示资产整个生命周期内为其使用的所有物料（备件和其他物料）的列表。</span><span class="sxs-lookup"><span data-stu-id="d4533-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="d4533-106">创建新资产时，应考虑在设置过程中设置资产 BOM。</span><span class="sxs-lookup"><span data-stu-id="d4533-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="d4533-107">这样就可以跟踪资产从创建日期开始的物料历史记录。</span><span class="sxs-lookup"><span data-stu-id="d4533-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="d4533-108">完成维护作业，并且已在工作订单中登记了物料消耗之后，可以跟踪对资产使用的备件和其他物料的消耗。</span><span class="sxs-lookup"><span data-stu-id="d4533-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="d4533-109">可通过此功能保留所有资产的完整物料消耗记录。</span><span class="sxs-lookup"><span data-stu-id="d4533-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="d4533-110">例如，可使用此记录监视是否经常更换特定备件，或跟踪当前对资产使用的备件或其他物料。</span><span class="sxs-lookup"><span data-stu-id="d4533-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="d4533-111">在工作订单中，物料消耗可能同时包含备件和其他物料，如润滑油、螺栓和垫圈。</span><span class="sxs-lookup"><span data-stu-id="d4533-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="d4533-112">可根据资产管理中的设置自动更新资产 BOM。</span><span class="sxs-lookup"><span data-stu-id="d4533-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="d4533-113">如果已创建了工作订单生命周期状态来处理已完工或已完成的工作订单，并且如果 **工作订单生命周期状态** 页上该工作订单生命周期状态的 **更新资产 BOM** 选项设置为 **是**，则当该工作订单更新为该生命周期状态时，将在 **资产 BOM** 页上自动更新对该工作订单使用的所有物料。</span><span class="sxs-lookup"><span data-stu-id="d4533-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="d4533-114">也可以通过在 **资产 BOM** 页上创建新物料行，手动更新资产 BOM。</span><span class="sxs-lookup"><span data-stu-id="d4533-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="d4533-115">在工作订单中登记了物料消耗之后，可在 **资产 BOM** 页上跟踪资产的备件历史记录。</span><span class="sxs-lookup"><span data-stu-id="d4533-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="d4533-116">若要使用此功能，必须在 **备件物料组** 页上选择应该用于登记备件的物料组。</span><span class="sxs-lookup"><span data-stu-id="d4533-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="d4533-117">若要使用资产 BOM 功能，必须首先设置所需备件物料组。</span><span class="sxs-lookup"><span data-stu-id="d4533-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="d4533-118">然后，如果要在工作订单完成时自动更新资产 BOM，可设置工作订单生命周期状态来处理该更新。</span><span class="sxs-lookup"><span data-stu-id="d4533-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="d4533-119">设置备件物料组</span><span class="sxs-lookup"><span data-stu-id="d4533-119">Set up spare parts item groups</span></span>

<span data-ttu-id="d4533-120">备件历史记录的设置基于在 **库存和仓库管理** 模块中创建的物料组。</span><span class="sxs-lookup"><span data-stu-id="d4533-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="d4533-121">在资产管理中，设置物料组，以便跟踪所选物料组中的物料的备件历史记录。</span><span class="sxs-lookup"><span data-stu-id="d4533-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="d4533-122">选择 **资产管理** \> **设置** \> **资产** \> **备件物料组**。</span><span class="sxs-lookup"><span data-stu-id="d4533-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="d4533-123">选择 **新建** 以设置物料组。</span><span class="sxs-lookup"><span data-stu-id="d4533-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="d4533-124">在 **物料组** 字段中，选择组。</span><span class="sxs-lookup"><span data-stu-id="d4533-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="d4533-125">将在 **名称** 字段中自动输入组的名称。</span><span class="sxs-lookup"><span data-stu-id="d4533-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="d4533-126">查看和更新资产 BOM</span><span class="sxs-lookup"><span data-stu-id="d4533-126">View and update asset BOMs</span></span>

<span data-ttu-id="d4533-127">过程工作订单中的消耗后，可在 **资产 BOM** 页中查看登记的物料消耗。</span><span class="sxs-lookup"><span data-stu-id="d4533-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="d4533-128">选择 **资产管理** \> **常用** \> **资产** \> **有效资产**。</span><span class="sxs-lookup"><span data-stu-id="d4533-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="d4533-129">在列表中选择资产，然后选择 **资产 BOM**。</span><span class="sxs-lookup"><span data-stu-id="d4533-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4533-130">若要查看所有资产的所有物料消耗登记，请选择 **资产管理** \> **查询** \> **资产** \> **资产 BOM**。</span><span class="sxs-lookup"><span data-stu-id="d4533-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="d4533-131">选择 **更新资产 BOM**。</span><span class="sxs-lookup"><span data-stu-id="d4533-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="d4533-132">可通过选择 **选择**，根据需要向更新添加资产、资产类型和资源。</span><span class="sxs-lookup"><span data-stu-id="d4533-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="d4533-133">选择 **确定** 开始更新。</span><span class="sxs-lookup"><span data-stu-id="d4533-133">Select **OK** to start the update.</span></span> <span data-ttu-id="d4533-134">也可以将更新功能设置为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="d4533-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="d4533-135">如果要查看与物料有关的更多信息，可添加库存维度。</span><span class="sxs-lookup"><span data-stu-id="d4533-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="d4533-136">选择 **库存** \> **维护显示**，然后选中要查看的维度的复选框。</span><span class="sxs-lookup"><span data-stu-id="d4533-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="d4533-137">若要将所有资产的此设置保留在 **资产 BOM** 页上，请将 **保存设置** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d4533-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="d4533-138">若要获取有关资产管理中何处对所选行使用物料，与资产之间的关联，作业类型默认值，备件和工作订单的概览，请选择 **物料使用位置**。</span><span class="sxs-lookup"><span data-stu-id="d4533-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="d4533-139">如果要仅查看有效物料行，请选择 **查看** \> **当前**。</span><span class="sxs-lookup"><span data-stu-id="d4533-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="d4533-140">若要查看所有物料行（包括到期日期比当前日期早的行），请选择 **查看** \> **所有**。</span><span class="sxs-lookup"><span data-stu-id="d4533-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="d4533-141">完成工作订单后，如果与相关资产关联的某些物料或备件已到期或已替换为其他物料或备件，建议您相应更新资产 BOM。</span><span class="sxs-lookup"><span data-stu-id="d4533-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="d4533-142">在资产 BOM 中创建新物料行</span><span class="sxs-lookup"><span data-stu-id="d4533-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="d4533-143">可为资产手动创建物料行。</span><span class="sxs-lookup"><span data-stu-id="d4533-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="d4533-144">在 **资产 BOM** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d4533-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="d4533-145">在 **资产** 字段中，选择要为物料行添加的资产。</span><span class="sxs-lookup"><span data-stu-id="d4533-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="d4533-146">在 **行号** 字段中，输入行的序号。</span><span class="sxs-lookup"><span data-stu-id="d4533-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="d4533-147">在 **有效** 字段中，输入物料的开始日期。</span><span class="sxs-lookup"><span data-stu-id="d4533-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="d4533-148">如果物料将到期，请在 **到期** 字段中输入结束日期。</span><span class="sxs-lookup"><span data-stu-id="d4533-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="d4533-149">在 **物料编号** 字段中，选择物料。</span><span class="sxs-lookup"><span data-stu-id="d4533-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="d4533-150">将在 **产品名** 字段中自动输入名称。</span><span class="sxs-lookup"><span data-stu-id="d4533-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="d4533-151">在 **数量** 字段中，输入所用数量。</span><span class="sxs-lookup"><span data-stu-id="d4533-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="d4533-152">将自动更新 **单位** 字段。</span><span class="sxs-lookup"><span data-stu-id="d4533-152">The **Unit** field is automatically updated.</span></span>
