---
title: 设置托运
description: 本主题介绍如何配置入站托运库存工序。
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 51f7d6b0402ebbed417554978fc8d927f6b9c606
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207201"
---
# <a name="set-up-consignment"></a><span data-ttu-id="e16bc-103">设置托运</span><span class="sxs-lookup"><span data-stu-id="e16bc-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e16bc-104">本主题介绍如何配置入站托运库存工序。</span><span class="sxs-lookup"><span data-stu-id="e16bc-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="e16bc-105">托运库存是由供应商所拥有，但存储在您的站点的库存。</span><span class="sxs-lookup"><span data-stu-id="e16bc-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="e16bc-106">在您准备好消耗或使用库存时，您接过库存的所有权。</span><span class="sxs-lookup"><span data-stu-id="e16bc-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="e16bc-107">此主题介绍启用托运流程所需的设置。</span><span class="sxs-lookup"><span data-stu-id="e16bc-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="e16bc-108">有关托运流程的详细信息，请参阅[设置托运](consignment.md)。</span><span class="sxs-lookup"><span data-stu-id="e16bc-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="e16bc-109">库存所有者</span><span class="sxs-lookup"><span data-stu-id="e16bc-109">Inventory owners</span></span>
<span data-ttu-id="e16bc-110">要记录实际入站托运库存，您需要定义供应商所有者。</span><span class="sxs-lookup"><span data-stu-id="e16bc-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="e16bc-111">此操作在**库存所有者**页完成。</span><span class="sxs-lookup"><span data-stu-id="e16bc-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="e16bc-112">当您选择一个**供应商帐户**后，将为**名称**和**所有者**字段生成默认值。</span><span class="sxs-lookup"><span data-stu-id="e16bc-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="e16bc-113">**所有者**字段中的值将对供应商可见，因此如果您的供应商帐户名称不易被外部人员识别，则您可能要更改该名称。</span><span class="sxs-lookup"><span data-stu-id="e16bc-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="e16bc-114">可以编辑**所有者**字段，但仅在您保存**库存所有者**记录时。</span><span class="sxs-lookup"><span data-stu-id="e16bc-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="e16bc-115">**名称**字段使用供应商帐户关联的当事方的名称进行填充，并且无法更改。</span><span class="sxs-lookup"><span data-stu-id="e16bc-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="e16bc-116">[![库存所有者](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="e16bc-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="e16bc-117">跟踪维度组</span><span class="sxs-lookup"><span data-stu-id="e16bc-117">Tracking dimension group</span></span>
<span data-ttu-id="e16bc-118">要在托运流程中使用的物料必须与**所有者**维度设置为**活动**的**跟踪维度组**相关联。</span><span class="sxs-lookup"><span data-stu-id="e16bc-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="e16bc-119">所有者维度始终选择了**实际库存**和**财务库存**选项。</span><span class="sxs-lookup"><span data-stu-id="e16bc-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="e16bc-120">从不选择**按维度的覆盖范围计划**。</span><span class="sxs-lookup"><span data-stu-id="e16bc-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="e16bc-121">[![跟踪维度组](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="e16bc-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="e16bc-122">库存所有权更改日记帐</span><span class="sxs-lookup"><span data-stu-id="e16bc-122">Inventory ownership change journal</span></span>
<span data-ttu-id="e16bc-123">**库存所有权更改**日记帐用于记录托运库存所有权从供应商转移到消耗它的法人。</span><span class="sxs-lookup"><span data-stu-id="e16bc-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="e16bc-124">同任何库存日记帐一样，它必须使用库存日记帐名称进行标识。</span><span class="sxs-lookup"><span data-stu-id="e16bc-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="e16bc-125">这些名称在**库存日记帐名称**页上创建，且**日记帐类型**必须设置为**所有权更改**。</span><span class="sxs-lookup"><span data-stu-id="e16bc-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="e16bc-126">[![库存所有权更改日记帐](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="e16bc-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="e16bc-127">托运流程中的供应商协作</span><span class="sxs-lookup"><span data-stu-id="e16bc-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="e16bc-128">如果您的供应商使用供应商协作界面，他们可以使用该界面监控您的站点的库存的消耗量。</span><span class="sxs-lookup"><span data-stu-id="e16bc-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="e16bc-129">有关设置供应商使用供应商协作的详细信息，请参阅[供应商门户用户安全性](../procurement/configure-security-vendor-portal-users.md)。</span><span class="sxs-lookup"><span data-stu-id="e16bc-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>
