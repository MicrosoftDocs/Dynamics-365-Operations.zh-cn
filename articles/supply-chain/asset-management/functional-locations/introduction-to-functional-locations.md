---
title: 功能位置简介
description: 本主题概述资产管理中的功能位置。
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
ms.openlocfilehash: 5d7d98ec5434d9cdc93276952035b559625be2bd
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783099"
---
# <a name="introduction-to-functional-locations"></a><span data-ttu-id="85e5b-103">功能位置简介</span><span class="sxs-lookup"><span data-stu-id="85e5b-103">Introduction to functional locations</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="85e5b-104">本主题概述资产管理中的功能位置。</span><span class="sxs-lookup"><span data-stu-id="85e5b-104">This topic provides an overview of functional locations in Asset Management.</span></span> <span data-ttu-id="85e5b-105">功能位置是技术结构中的元素，如系统中的功能单元。</span><span class="sxs-lookup"><span data-stu-id="85e5b-105">Functional locations are elements of a technical structure, such as the functional units in a system.</span></span> <span data-ttu-id="85e5b-106">功能位置以层次结构的方式创建，可以在其中安装资产。</span><span class="sxs-lookup"><span data-stu-id="85e5b-106">Functional locations are created hierarchically, and you install assets on them.</span></span> <span data-ttu-id="85e5b-107">公司中的功能位置设置取决于公司的要求。</span><span class="sxs-lookup"><span data-stu-id="85e5b-107">The setup of functional locations in your company depends on the company's requirements.</span></span>

<span data-ttu-id="85e5b-108">下面是一些如何使用功能位置的示例：</span><span class="sxs-lookup"><span data-stu-id="85e5b-108">Here are some examples of how you can use functional locations:</span></span>

- <span data-ttu-id="85e5b-109">**功能** – 功能位置面向用户，用于管理具有相似行为的资产。</span><span class="sxs-lookup"><span data-stu-id="85e5b-109">**Functional** – The functional locations can be user-oriented and used to manage assets that have similar behavior.</span></span>
- <span data-ttu-id="85e5b-110">**流程相关** – 功能位置面向工作流。</span><span class="sxs-lookup"><span data-stu-id="85e5b-110">**Process-related** – The functional locations can be workflow-oriented.</span></span>
- <span data-ttu-id="85e5b-111">**空间** – 功能位置表示地理位置或地点。</span><span class="sxs-lookup"><span data-stu-id="85e5b-111">**Spatial** – The functional locations can represent geographical locations or sites.</span></span>

<span data-ttu-id="85e5b-112">每个功能位置在资产管理中独立管理。</span><span class="sxs-lookup"><span data-stu-id="85e5b-112">Each functional location is managed independently in Asset Management.</span></span> <span data-ttu-id="85e5b-113">下面是功能位置的一些有用的功能：</span><span class="sxs-lookup"><span data-stu-id="85e5b-113">Here are some of the useful features of functional locations:</span></span>

- <span data-ttu-id="85e5b-114">设置功能位置规范。</span><span class="sxs-lookup"><span data-stu-id="85e5b-114">Set up functional location specifications.</span></span>
- <span data-ttu-id="85e5b-115">设置资产规范要求。</span><span class="sxs-lookup"><span data-stu-id="85e5b-115">Set up asset specification requirements.</span></span>
- <span data-ttu-id="85e5b-116">为预防性和反应性维护设置维护顺序</span><span class="sxs-lookup"><span data-stu-id="85e5b-116">Set up maintenance sequences for preventive and reactive maintenance.</span></span>
- <span data-ttu-id="85e5b-117">管理安装的资产。</span><span class="sxs-lookup"><span data-stu-id="85e5b-117">Manage installed assets.</span></span>
- <span data-ttu-id="85e5b-118">跟踪有效请求和与所安装资产关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="85e5b-118">Track active requests and work orders that are related to installed assets.</span></span>
- <span data-ttu-id="85e5b-119">跟踪为资产登记的故障。</span><span class="sxs-lookup"><span data-stu-id="85e5b-119">Track faults that are registered on assets.</span></span>
- <span data-ttu-id="85e5b-120">跟踪与功能位置关联的资产在指定时间的维护成本。</span><span class="sxs-lookup"><span data-stu-id="85e5b-120">Track maintenance costs on the assets that are related to a functional location at any given time.</span></span>

<span data-ttu-id="85e5b-121">功能位置可用于跟踪与请求、工作订单、故障登记、条件评估、生产停止登记和资产计数器登记有关的资产。</span><span class="sxs-lookup"><span data-stu-id="85e5b-121">Functional locations provide traceability of assets in relation to requests, work orders, fault registrations, condition assessments, production stop registrations, and asset counter registrations.</span></span>

> [!NOTE]
> <span data-ttu-id="85e5b-122">即使资产在其生命周期内安装在多个功能位置，成本也可以与每个位置关联。</span><span class="sxs-lookup"><span data-stu-id="85e5b-122">Even if an asset is installed on various functional locations during its lifetime, the costs can be related to each location.</span></span> <span data-ttu-id="85e5b-123">换句话说，资产成本始终与指定时间安装资产的功能位置关联。</span><span class="sxs-lookup"><span data-stu-id="85e5b-123">In other words, asset costs are always related to the functional location that the asset was installed on at a given time.</span></span>

<span data-ttu-id="85e5b-124">功能位置**不**具备灵活性。</span><span class="sxs-lookup"><span data-stu-id="85e5b-124">Functional locations are **not** flexible.</span></span> <span data-ttu-id="85e5b-125">因此，设置功能位置层次结构之后，不能在其中移动位置。</span><span class="sxs-lookup"><span data-stu-id="85e5b-125">Therefore, after you set up a functional location hierarchy, you can't move locations around in it.</span></span> 

<span data-ttu-id="85e5b-126">创建功能位置层次结构之后，下一步是在其中安装资产。</span><span class="sxs-lookup"><span data-stu-id="85e5b-126">After you create a functional location hierarchy, the next step is to install assets on it.</span></span> <span data-ttu-id="85e5b-127">有关详细信息，请参阅[在功能位置安装资产](../functional-locations/install-objects-on-functional-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="85e5b-127">For more information, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

## <a name="all-functional-locations"></a><span data-ttu-id="85e5b-128">所有功能位置</span><span class="sxs-lookup"><span data-stu-id="85e5b-128">All functional locations</span></span>

<span data-ttu-id="85e5b-129">选择**资产管理** \> **常用** \> **功能位置** \> **所有功能位置**以打开**所有功能位置**列表页。</span><span class="sxs-lookup"><span data-stu-id="85e5b-129">Select **Asset management** \> **Common** \> **Functional locations** \> **All functional locations** to open the **All functional locations** list page.</span></span> <span data-ttu-id="85e5b-130">此页显示所有功能位置和与每个功能位置有关的信息。</span><span class="sxs-lookup"><span data-stu-id="85e5b-130">This page shows all functional locations and some of the information that is related to each.</span></span> <span data-ttu-id="85e5b-131">若要仅查看有效功能位置，请选择**有效功能位置**。</span><span class="sxs-lookup"><span data-stu-id="85e5b-131">To view only active functional locations, select **Active functional locations**.</span></span> <span data-ttu-id="85e5b-132">若要仅查看在您作为工人关联到的功能位置，请选择**我的有效功能位置**。</span><span class="sxs-lookup"><span data-stu-id="85e5b-132">To view only the functional locations that you're related to as a worker, select **My active functional locations**.</span></span> <span data-ttu-id="85e5b-133">（此项关联在**工人**页设置。</span><span class="sxs-lookup"><span data-stu-id="85e5b-133">(This relation is set up on the **Workers** page.</span></span> <span data-ttu-id="85e5b-134">有关详细信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。）</span><span class="sxs-lookup"><span data-stu-id="85e5b-134">For more information, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>

<span data-ttu-id="85e5b-135">在**所有功能位置**列表页中的**功能位置**列选择链接可查看所选记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="85e5b-135">On the **All functional locations** list page, select a link in the **Functional location** column to view the details of the selected record.</span></span> <span data-ttu-id="85e5b-136">若要编辑功能位置，请选择**编辑**按钮。</span><span class="sxs-lookup"><span data-stu-id="85e5b-136">To edit the functional location, select the **Edit** button.</span></span> <span data-ttu-id="85e5b-137">这个详细信息视图显示与位置有关的详细信息。</span><span class="sxs-lookup"><span data-stu-id="85e5b-137">The details view shows detailed information that is related to the location.</span></span> <span data-ttu-id="85e5b-138">右侧有一个**相关信息**窗格。</span><span class="sxs-lookup"><span data-stu-id="85e5b-138">It also includes a **Related information** pane on the right.</span></span> <span data-ttu-id="85e5b-139">此窗格显示功能位置层次结构。</span><span class="sxs-lookup"><span data-stu-id="85e5b-139">This pane shows the functional location hierarchy.</span></span> <span data-ttu-id="85e5b-140">可展开和折叠**相关信息**窗格。</span><span class="sxs-lookup"><span data-stu-id="85e5b-140">You can expand and collapse the **Related information** pane.</span></span>

<span data-ttu-id="85e5b-141">操作窗格上的按钮排列在选项卡上。</span><span class="sxs-lookup"><span data-stu-id="85e5b-141">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="85e5b-142">下表简述与资产管理有关的按钮。</span><span class="sxs-lookup"><span data-stu-id="85e5b-142">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="85e5b-143">按钮名称</span><span class="sxs-lookup"><span data-stu-id="85e5b-143">Button name</span></span>                         | <span data-ttu-id="85e5b-144">说明</span><span class="sxs-lookup"><span data-stu-id="85e5b-144">Description</span></span>                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85e5b-145">编辑​​</span><span class="sxs-lookup"><span data-stu-id="85e5b-145">Edit</span></span>                                | <span data-ttu-id="85e5b-146">在页面的编辑模式和查看模式之间切换。</span><span class="sxs-lookup"><span data-stu-id="85e5b-146">Switch between edit mode and view mode for the page.</span></span>                                                                                         |
| <span data-ttu-id="85e5b-147">新</span><span class="sxs-lookup"><span data-stu-id="85e5b-147">New</span></span>                                 | <span data-ttu-id="85e5b-148">创建新的功能位置。</span><span class="sxs-lookup"><span data-stu-id="85e5b-148">Create a new functional location.</span></span>                                                                                                            |
| <span data-ttu-id="85e5b-149">删除</span><span class="sxs-lookup"><span data-stu-id="85e5b-149">Delete</span></span>                              | <span data-ttu-id="85e5b-150">删除所选功能位置。</span><span class="sxs-lookup"><span data-stu-id="85e5b-150">Delete the selected functional location.</span></span>                                                                                                     |
| <span data-ttu-id="85e5b-151">重命名</span><span class="sxs-lookup"><span data-stu-id="85e5b-151">Rename</span></span>                              | <span data-ttu-id="85e5b-152">重命名所选功能位置。</span><span class="sxs-lookup"><span data-stu-id="85e5b-152">Rename the selected functional location.</span></span>                                                                                                     |
| <span data-ttu-id="85e5b-153">复制功能位置结构</span><span class="sxs-lookup"><span data-stu-id="85e5b-153">Copy functional location structure</span></span>  | <span data-ttu-id="85e5b-154">复制功能位置层次结构。</span><span class="sxs-lookup"><span data-stu-id="85e5b-154">Copy the functional location hierarchy.</span></span>                                                                                                      |
| <span data-ttu-id="85e5b-155">安装资产</span><span class="sxs-lookup"><span data-stu-id="85e5b-155">Install asset</span></span>                       | <span data-ttu-id="85e5b-156">在功能位置安装资产，包括子资产。</span><span class="sxs-lookup"><span data-stu-id="85e5b-156">Install an asset, including child assets, on the functional location.</span></span>                                                                        |
| <span data-ttu-id="85e5b-157">替换资产</span><span class="sxs-lookup"><span data-stu-id="85e5b-157">Replace asset</span></span>                       | <span data-ttu-id="85e5b-158">将资产层次结构替换为功能位置中的另一个资产层次结构。</span><span class="sxs-lookup"><span data-stu-id="85e5b-158">Replace the asset hierarchy with another asset hierarchy on the functional location.</span></span>                                                         |
| <span data-ttu-id="85e5b-159">成本控制</span><span class="sxs-lookup"><span data-stu-id="85e5b-159">Cost control</span></span>                        | <span data-ttu-id="85e5b-160">打开**功能位置成本控制**页，可在其中计算所选功能位置的成本。</span><span class="sxs-lookup"><span data-stu-id="85e5b-160">Open the **Functional location cost control** page, where you can do a cost calculation for the selected functional location.</span></span>                |
| <span data-ttu-id="85e5b-161">工时控制</span><span class="sxs-lookup"><span data-stu-id="85e5b-161">Hour control</span></span>                        | <span data-ttu-id="85e5b-162">打开**功能位置工时控制**页，可在其中计算所选功能位置的成本。</span><span class="sxs-lookup"><span data-stu-id="85e5b-162">Open the **Functional location hour control** page, where you can do a cost calculation for the selected functional location.</span></span>                |
| <span data-ttu-id="85e5b-163">资产</span><span class="sxs-lookup"><span data-stu-id="85e5b-163">Assets</span></span>                              | <span data-ttu-id="85e5b-164">打开**所有资产**页，可在其中查看与所选功能位置关联的资产的列表。</span><span class="sxs-lookup"><span data-stu-id="85e5b-164">Open the **All assets** page, where you can view a list of assets that are related to the selected functional location.</span></span>                      |
| <span data-ttu-id="85e5b-165">请求</span><span class="sxs-lookup"><span data-stu-id="85e5b-165">Requests</span></span>                            | <span data-ttu-id="85e5b-166">打开**有效请求**页，可在其中查看与所选功能位置关联的请求的列表。</span><span class="sxs-lookup"><span data-stu-id="85e5b-166">Open the **Active requests** page, where you can view a list of requests that are related to the selected functional location.</span></span>               |
| <span data-ttu-id="85e5b-167">工作订单</span><span class="sxs-lookup"><span data-stu-id="85e5b-167">Work orders</span></span>                         | <span data-ttu-id="85e5b-168">打开**有效工作订单**页，可在其中查看与所选功能位置关联的工作订单的列表。</span><span class="sxs-lookup"><span data-stu-id="85e5b-168">Open the **Active work orders** page, where you can view a list of work orders that are related to the selected functional location.</span></span>         |
| <span data-ttu-id="85e5b-169">故障</span><span class="sxs-lookup"><span data-stu-id="85e5b-169">Faults</span></span>                              | <span data-ttu-id="85e5b-170">打开**资产故障**页，可在其中查看与所选功能位置关联的资产故障登记的列表。</span><span class="sxs-lookup"><span data-stu-id="85e5b-170">Open the **Asset faults** page, where you can view a list of asset fault registrations that are related to the selected functional location.</span></span> |
| <span data-ttu-id="85e5b-171">更新功能位置状态</span><span class="sxs-lookup"><span data-stu-id="85e5b-171">Update functional location state</span></span>    | <span data-ttu-id="85e5b-172">更新所选功能位置的阶段。</span><span class="sxs-lookup"><span data-stu-id="85e5b-172">Update the stage of the selected functional location.</span></span>                                                                                        |
| <span data-ttu-id="85e5b-173">生命周期状态日志</span><span class="sxs-lookup"><span data-stu-id="85e5b-173">Lifecycle state log</span></span>                 | <span data-ttu-id="85e5b-174">查看日志，其中显示所选功能位置的阶段。</span><span class="sxs-lookup"><span data-stu-id="85e5b-174">View a log that shows the stages of the selected functional location.</span></span>                                                                        |
