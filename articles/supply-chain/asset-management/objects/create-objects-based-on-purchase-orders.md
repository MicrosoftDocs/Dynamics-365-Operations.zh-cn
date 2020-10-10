---
title: 基于采购订单创建资产
description: 本主题说明如何在资产管理中创建资产物料的列表，这些资产物料可充当为维护作业创建资产的基础。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889017"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="86aea-103">基于采购订单创建资产</span><span class="sxs-lookup"><span data-stu-id="86aea-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="86aea-104">本主题说明如何在资产管理中创建资产物料的列表，这些资产物料可充当为维护作业创建资产的基础。</span><span class="sxs-lookup"><span data-stu-id="86aea-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="86aea-105">可根据资产物料查看已经为这些物料创建的采购订单行的列表。</span><span class="sxs-lookup"><span data-stu-id="86aea-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="86aea-106">此功能的作用是在资产管理中基于采购订单轻松创建资产。</span><span class="sxs-lookup"><span data-stu-id="86aea-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="86aea-107">首先，在**资产物料**中设置要用于通过采购订单创建资产的物料。</span><span class="sxs-lookup"><span data-stu-id="86aea-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="86aea-108">创建采购订单行之后，在**暂挂资产**中创建资产。</span><span class="sxs-lookup"><span data-stu-id="86aea-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="86aea-109">可以决定应该在采购订单的哪个阶段创建资产。</span><span class="sxs-lookup"><span data-stu-id="86aea-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="86aea-110">选择资产物料</span><span class="sxs-lookup"><span data-stu-id="86aea-110">Select asset items</span></span>

1. <span data-ttu-id="86aea-111">单击**资产管理** > **设置** > **资产** > **物料**。</span><span class="sxs-lookup"><span data-stu-id="86aea-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="86aea-112">单击**新建**创建新资产物料。</span><span class="sxs-lookup"><span data-stu-id="86aea-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="86aea-113">在**物料编号**字段中选择物料。</span><span class="sxs-lookup"><span data-stu-id="86aea-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="86aea-114">离开该字段时，将在**产品名**字段中自动插入物料名称。</span><span class="sxs-lookup"><span data-stu-id="86aea-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="86aea-115">在**常规**快速选项卡上，选择物料的资产类型。</span><span class="sxs-lookup"><span data-stu-id="86aea-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="86aea-116">选择物料的资产制造商和模型。</span><span class="sxs-lookup"><span data-stu-id="86aea-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="86aea-117">保存该物料。</span><span class="sxs-lookup"><span data-stu-id="86aea-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="86aea-118">通过暂挂资产创建资产</span><span class="sxs-lookup"><span data-stu-id="86aea-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="86aea-119">单击**资产管理** > **常用** > **资产** > **暂挂资产**。</span><span class="sxs-lookup"><span data-stu-id="86aea-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="86aea-120">将看到基于**资产物料**中所选物料更新后的采购订单列表。</span><span class="sxs-lookup"><span data-stu-id="86aea-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="86aea-121">可筛选采购订单状态，以便选择应该在哪个生命周期状态创建资产。</span><span class="sxs-lookup"><span data-stu-id="86aea-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="86aea-122">例如，您可能希望仅当在采购订单中过帐了产品收据时才创建资产。</span><span class="sxs-lookup"><span data-stu-id="86aea-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="86aea-123">在采购订单行中选择**参考编号**链接，以便查看有关物料的详细信息。</span><span class="sxs-lookup"><span data-stu-id="86aea-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="86aea-124">如果要编辑**库存维度**快速选项卡上显示哪些维度，请单击**显示维度**按钮，然后进行选择。</span><span class="sxs-lookup"><span data-stu-id="86aea-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="86aea-125">如果要基于采购订单行创建资产，请选中列表页上**标记**列中该行的复选框，然后单击**创建资产**。</span><span class="sxs-lookup"><span data-stu-id="86aea-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="86aea-126">将显示消息，告知您资产 ID。</span><span class="sxs-lookup"><span data-stu-id="86aea-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="86aea-127">在**所有资产**列表中选择资产，然后单击**编辑**向资产添加更多信息。</span><span class="sxs-lookup"><span data-stu-id="86aea-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="86aea-128">如果因为不希望创建资产而要删除行，请选中**暂挂资产**中**标记**列内该行的复选框，然后单击**放弃暂挂资产**。</span><span class="sxs-lookup"><span data-stu-id="86aea-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="86aea-129">将显示消息，告知您资产 ID。</span><span class="sxs-lookup"><span data-stu-id="86aea-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="86aea-130">您将不删除采购订单或销售订单，而是仅删除本该用于在**资产管理**中创建资产的记录。</span><span class="sxs-lookup"><span data-stu-id="86aea-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="86aea-131">将把所有产品维度（尺寸、颜色、配置等）自动转给资产属性。</span><span class="sxs-lookup"><span data-stu-id="86aea-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="86aea-132">创建资产时，将直接为资产创建跟踪维度（序列号）。</span><span class="sxs-lookup"><span data-stu-id="86aea-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="86aea-133">查找暂挂资产</span><span class="sxs-lookup"><span data-stu-id="86aea-133">Find pending assets</span></span>

<span data-ttu-id="86aea-134">可运行**暂挂资产盘点**以检查是否有暂挂资产。</span><span class="sxs-lookup"><span data-stu-id="86aea-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="86aea-135">例如，可使用此功能在每次准备好将暂挂资产创建为资产时接收通知。</span><span class="sxs-lookup"><span data-stu-id="86aea-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="86aea-136">单击**资产管理** > **定期** > **资产** > **暂挂资产盘点**。</span><span class="sxs-lookup"><span data-stu-id="86aea-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="86aea-137">单击**确定**运行作业并更新**暂挂资产**中的列表。</span><span class="sxs-lookup"><span data-stu-id="86aea-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="86aea-138">可以将此作业设置为批处理作业，例如，每天一次。</span><span class="sxs-lookup"><span data-stu-id="86aea-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="86aea-139">**注意：** 如果在创建资产*之后*根据适合物料更改了采购订单中的数据，将不会在资产上体现这些更改。</span><span class="sxs-lookup"><span data-stu-id="86aea-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
