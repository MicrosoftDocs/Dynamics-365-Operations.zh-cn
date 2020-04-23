---
title: 多级资产
description: 本主题介绍如何创建和删除多级资产。
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
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214863"
---
# <a name="multi-level-assets"></a><span data-ttu-id="92bb8-103">多级资产</span><span class="sxs-lookup"><span data-stu-id="92bb8-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="92bb8-104">本主题介绍如何创建和删除多级资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="92bb8-105">可以按分层树结构创建资产和关联的子资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="92bb8-106">这样就可以显示资产之间的关系和依赖关系。</span><span class="sxs-lookup"><span data-stu-id="92bb8-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="92bb8-107">可以将维护作业与树结构的所有级别关联。</span><span class="sxs-lookup"><span data-stu-id="92bb8-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="92bb8-108">也可以为单个级别创建统计信息，或作为所有子资产级别的总和创建。</span><span class="sxs-lookup"><span data-stu-id="92bb8-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="92bb8-109">在**所有资产**列表页（**资产管理** \> **常用** \> **资产** \> **所有资产**）上，**资产**列按分层顺序列出资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="92bb8-110">**父级**列显示关联的父级。</span><span class="sxs-lookup"><span data-stu-id="92bb8-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="92bb8-111">此外，如果已经创建了资产和子资产，则**相关信息**窗格中的**资产树**部分以树结构的形式显示资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="92bb8-112">有关如何创建资产的详细信息，请参阅[创建资产](../objects/create-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="92bb8-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="92bb8-113">若要创建子资产，请在**常规**快速选项卡上**父级**字段中选择父资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="92bb8-114">复制资产或资产结构</span><span class="sxs-lookup"><span data-stu-id="92bb8-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="92bb8-115">如果公司有多个相似资产结构，可使用资产管理中的复制功能快速创建它们。</span><span class="sxs-lookup"><span data-stu-id="92bb8-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="92bb8-116">选择**资产管理** \> **常用** \> **资产** \> **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="92bb8-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="92bb8-117">在**所有资产**列表页，选择要复制的资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="92bb8-118">例如，如果要复制整个资产结构（包括子资产），请选择父资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="92bb8-119">选择**复制资产**。</span><span class="sxs-lookup"><span data-stu-id="92bb8-119">Select **Copy asset**.</span></span> <span data-ttu-id="92bb8-120">在**复制自** 部分中，**资产**字段设置为您在列表页选择的资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="92bb8-121">在**复制到**部分的**资产**字段中，输入新资产的名称。</span><span class="sxs-lookup"><span data-stu-id="92bb8-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="92bb8-122">如果要创建的资产应该是现有资产结构的一部分，请在**父资产**部分的**资产**字段中选择一个父 ID。</span><span class="sxs-lookup"><span data-stu-id="92bb8-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="92bb8-123">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="92bb8-123">Select **OK**.</span></span> <span data-ttu-id="92bb8-124">将在**所有资产**列表页显示新资产结构。</span><span class="sxs-lookup"><span data-stu-id="92bb8-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="92bb8-125">将把与复制的资产关联的所有资产属性、维护计划和维护阶段转移到新资产或资产结构。</span><span class="sxs-lookup"><span data-stu-id="92bb8-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="92bb8-126">复制资产结构时，新结构中的子资产与复制的子资产同名。</span><span class="sxs-lookup"><span data-stu-id="92bb8-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="92bb8-127">复制过程完成后，可轻松更改资产的名称和其他设置。</span><span class="sxs-lookup"><span data-stu-id="92bb8-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="92bb8-128">在**所有资产**列表页选择资产，然后选择**编辑**按钮。</span><span class="sxs-lookup"><span data-stu-id="92bb8-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="92bb8-129">复制资产或资产结构时，将把新资产的生命周期状态重置为您为资产定义的初始生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="92bb8-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="92bb8-130">将把功能位置重置为默认功能位置。</span><span class="sxs-lookup"><span data-stu-id="92bb8-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="92bb8-131">删除资产或资产结构</span><span class="sxs-lookup"><span data-stu-id="92bb8-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="92bb8-132">如果资产有关联的子资产，则仅当没有为这些资产中的任何一个登记维护请求、工作订单作业、故障登记或条件评估时，才能删除该资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="92bb8-133">在**所有资产**列表页，选择要删除的资产。</span><span class="sxs-lookup"><span data-stu-id="92bb8-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="92bb8-134">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="92bb8-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="92bb8-135">如果不能通过此过程删除资产，另一种处理删除的方法是为此目的设置资产生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="92bb8-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="92bb8-136">例如，可在**资产生命周期状态**页设置**已报废**或**已删除**生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="92bb8-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
