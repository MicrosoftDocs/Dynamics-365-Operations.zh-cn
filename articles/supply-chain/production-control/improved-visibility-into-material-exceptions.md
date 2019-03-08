---
title: 物料异常的可见性
description: 此主题介绍如何提高用于生产订单和批次订单的原材料异常的可见性。
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: c7a5cc4f6c6f430a2ceb9125edb3916fe7b71ab8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "344746"
---
# <a name="visibility-into-material-exceptions"></a><span data-ttu-id="712e9-103">物料异常的可见性</span><span class="sxs-lookup"><span data-stu-id="712e9-103">Visibility into material exceptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="712e9-104">**生产车间管理**工作区中的三个磁贴可让您更好地了解用于生产订单和批次订单的原材料的异常情况：</span><span class="sxs-lookup"><span data-stu-id="712e9-104">In the **Production floor management** workspace, three tiles give you better visibility into exceptions for raw materials for production orders and batch orders:</span></span>

- <span data-ttu-id="712e9-105">需要关注的未发布物料行</span><span class="sxs-lookup"><span data-stu-id="712e9-105">Unreleased material lines needing attention</span></span>
- <span data-ttu-id="712e9-106">需要关注的未处理波次</span><span class="sxs-lookup"><span data-stu-id="712e9-106">Unprocessed waves needing attention</span></span>
- <span data-ttu-id="712e9-107">需要关注的开放仓库工作</span><span class="sxs-lookup"><span data-stu-id="712e9-107">Open warehouse work needing attention</span></span>

<span data-ttu-id="712e9-108">在这三个磁贴中，物料清单 (BOM) 行和配方行的原材料日期与工作区日期进行比较，也与在**配置我的工作区**菜单上为**生产单位**、**资源组**和**资源**设定的筛选器进行比较。</span><span class="sxs-lookup"><span data-stu-id="712e9-108">For all three tiles, the raw material date of the bill of materials (BOM) lines and formula lines is compared against the workspace date, and also against the filters for **Production unit**, **Resource group**, and **Resource** that are set on the **Configure my work space** menu.</span></span> <span data-ttu-id="712e9-109">默认情况下，工作区日期设定为当前日期，但您可以调整该日期。</span><span class="sxs-lookup"><span data-stu-id="712e9-109">By default, the workspace date is set to the current date, but you can adjust it.</span></span>

<span data-ttu-id="712e9-110">对于未发布的物料清单行或配方行，如果该行的原材料日期与工作区日期相同或早于工作区日期，且如果它满足工作区中的筛选器定义的条件，则需关注。</span><span class="sxs-lookup"><span data-stu-id="712e9-110">An unreleased BOM line or formula line requires attention if the raw material date of the line is the same as or earlier than the workspace date, and if it meets the criteria that are defined by the filters in the workspace.</span></span>

<span data-ttu-id="712e9-111">在下图中，蓝色栏表示对资源计划的生产作业。</span><span class="sxs-lookup"><span data-stu-id="712e9-111">In the following figure, the blue bar represents a production job that is scheduled on a resource.</span></span> <span data-ttu-id="712e9-112">该作业计划于 2017 年 5 月 1 日 (2017/05/01) 开始。</span><span class="sxs-lookup"><span data-stu-id="712e9-112">The job is scheduled to start on May 1, 2017 (2017/05/01).</span></span> <span data-ttu-id="712e9-113">此日期为原材料日期。</span><span class="sxs-lookup"><span data-stu-id="712e9-113">This date is the raw material date.</span></span> <span data-ttu-id="712e9-114">换言之，在物料清单和配方行上分配给该作业的物料必须在该日期准备就绪。</span><span class="sxs-lookup"><span data-stu-id="712e9-114">In other words, the materials that are assigned to the job on the BOM and formula lines must be ready on this date.</span></span> <span data-ttu-id="712e9-115">图中的另外一个日期，即 2017 年 5 月 6 日 (2017/05/06)，表示工作区日期。</span><span class="sxs-lookup"><span data-stu-id="712e9-115">The other date in the figure, May 6, 2017 (2017/05/06), represents the workspace date.</span></span> <span data-ttu-id="712e9-116">在此示例中，原材料日期早于工作区日期。</span><span class="sxs-lookup"><span data-stu-id="712e9-116">In this example, the raw material date is earlier than the workspace date.</span></span> <span data-ttu-id="712e9-117">因此，计划要开始使用原材料的日期已经过时，且物料清单和配方行满足需要关注的条件。</span><span class="sxs-lookup"><span data-stu-id="712e9-117">Therefore, the date when consumption of the raw material was supposed to start has passed, and the BOM and formula lines meet the criteria for requiring attention.</span></span>

![原材料日期早于工作区日期的生产作业的示例](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a><span data-ttu-id="712e9-119">需要关注的未发布物料行</span><span class="sxs-lookup"><span data-stu-id="712e9-119">Unreleased material lines needing attention</span></span>

<span data-ttu-id="712e9-120">物料清单或配方行可以通过三种方式发布到仓库：</span><span class="sxs-lookup"><span data-stu-id="712e9-120">A BOM or formula line can be released to the warehouse in three ways:</span></span>

- <span data-ttu-id="712e9-121">作为生产订单或批次订单的一部分发布</span><span class="sxs-lookup"><span data-stu-id="712e9-121">As part of a production order or batch order release</span></span>
- <span data-ttu-id="712e9-122">作为手动下达</span><span class="sxs-lookup"><span data-stu-id="712e9-122">As a manual release</span></span>
- <span data-ttu-id="712e9-123">通过批处理作业自动发布</span><span class="sxs-lookup"><span data-stu-id="712e9-123">Automatically through a batch job</span></span>

<span data-ttu-id="712e9-124">有关详细信息，请参阅[将物料清单和配方行发放到仓库](releasing-bom-and-formula-lines-to-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="712e9-124">For more information, see [Release BOM and formula lines to the warehouse](releasing-bom-and-formula-lines-to-warehouse.md).</span></span> 

<span data-ttu-id="712e9-125">如果物料清单或配方行尚未发放或已经部分发放，且满足工作区的日期和筛选器条件，则该行包括在**需要关注的未发布物料行**上显示的数字计算中。</span><span class="sxs-lookup"><span data-stu-id="712e9-125">If a BOM or formula line hasn't been released or has been only partly released, and if the date and filter criteria of the workspace are met, the line is included in the calculation of the number that appears on the **Unreleased material lines needing attention** tile.</span></span>

<span data-ttu-id="712e9-126">当您选择磁贴后，**发放到仓库**页打开。</span><span class="sxs-lookup"><span data-stu-id="712e9-126">When you select the tile, the **Release to warehouse** page is opened.</span></span> <span data-ttu-id="712e9-127">此页显示未发放的物料清单和配方行的数量，该数量由磁贴上的数字表示。</span><span class="sxs-lookup"><span data-stu-id="712e9-127">This page shows the number of unreleased BOM and formula lines that is indicated by the number on the tile.</span></span> <span data-ttu-id="712e9-128">未发放的行显示在上方网格中。</span><span class="sxs-lookup"><span data-stu-id="712e9-128">The unreleased lines appear in the upper grid.</span></span> <span data-ttu-id="712e9-129">该网格显示最初对该行估测的数量、已经发放的数量以及还必须要发放的剩余数量。</span><span class="sxs-lookup"><span data-stu-id="712e9-129">This grid shows the quantity that was originally estimated for the line, the quantity that has already been released, and the remaining quantity that must still be released.</span></span> <span data-ttu-id="712e9-130">您可以将上方网格中的行添加到下方网格中。</span><span class="sxs-lookup"><span data-stu-id="712e9-130">You can add lines from the upper grid to the lower grid.</span></span> <span data-ttu-id="712e9-131">然后从下方网格中将选定的行发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="712e9-131">From the lower grid, you can then release the selected lines to the warehouse.</span></span> <span data-ttu-id="712e9-132">您还可以从下方网格中调整要发放的数量，以便仅发放部分数量。</span><span class="sxs-lookup"><span data-stu-id="712e9-132">From the lower grid, you can also adjust the quantity to release so that only a partial quantity is released.</span></span>

## <a name="unprocessed-waves-needing-attention"></a><span data-ttu-id="712e9-133">需要关注的未处理波次</span><span class="sxs-lookup"><span data-stu-id="712e9-133">Unprocessed waves needing attention</span></span>

<span data-ttu-id="712e9-134">发放物料清单或配方行时，该行添加到新生产波次或现有开放波次中，具体取决于生产波次模板的配置。</span><span class="sxs-lookup"><span data-stu-id="712e9-134">When a BOM or formula line is released, it's added to either a new production wave or an existing open wave, depending on the configuration of the production wave template.</span></span> <span data-ttu-id="712e9-135">通过波次模板的配置，还可以设置一个波次，以便在发放物料清单或配方行时自动处理该波次。</span><span class="sxs-lookup"><span data-stu-id="712e9-135">Through the configuration of the wave template, you can also set up a wave so that it's automatically processed when a BOM or formula line is released.</span></span> <span data-ttu-id="712e9-136">处理波次时，生成用于原材料领料的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="712e9-136">When the wave is processed, warehouse work for raw material picking is generated.</span></span> <span data-ttu-id="712e9-137">如果波次模板配置为无法在发放时间处理波次，则波次仍处于未处理状态。</span><span class="sxs-lookup"><span data-stu-id="712e9-137">If the wave template is configured so that waves aren't processed at the time of release, the wave remains in an unprocessed state.</span></span> <span data-ttu-id="712e9-138">**需要关注的未处理波次**磁贴显示在未处理波次上已发放到仓库，且原材料日期早于工作区日期或与工作区日期相同的物料清单和配方行的数量。</span><span class="sxs-lookup"><span data-stu-id="712e9-138">The **Unprocessed waves needing attention** tile shows the number of BOM and formula lines that have been released to the warehouse on unprocessed waves, and that have a raw material date that is earlier than or the same as the workspace date.</span></span> <span data-ttu-id="712e9-139">应用到工作区筛选器的操作资源也必须使用该行。</span><span class="sxs-lookup"><span data-stu-id="712e9-139">The lines must also be consumed by an operation resource that applies to the filter of the workspace.</span></span>

<span data-ttu-id="712e9-140">选择磁贴后，**所有生产波次**页打开。</span><span class="sxs-lookup"><span data-stu-id="712e9-140">When the tile is selected, the **All production waves** page is opened.</span></span> <span data-ttu-id="712e9-141">此页按包含来自满足该磁贴条件的已发放物料清单和配方行的波次行的开放波次的数量进行筛选。</span><span class="sxs-lookup"><span data-stu-id="712e9-141">This page is filtered by the number of open waves that contain wave lines from released BOM and formula lines that meet the criteria for the tile.</span></span> <span data-ttu-id="712e9-142">在**所有生产波次**页上，您可以手动处理波次。</span><span class="sxs-lookup"><span data-stu-id="712e9-142">From the **All production waves** page, you can manually process the wave.</span></span>

## <a name="open-warehouse-work-needing-attention"></a><span data-ttu-id="712e9-143">需要关注的开放仓库工作</span><span class="sxs-lookup"><span data-stu-id="712e9-143">Open warehouse work needing attention</span></span>

<span data-ttu-id="712e9-144">**需要关注的开放仓库工作**磁贴显示已发放到仓库、具有未处理工作以及原材料日期早于工作区日期或与工作区日期相同的物料清单和配方行的数量。</span><span class="sxs-lookup"><span data-stu-id="712e9-144">The **Open warehouse work needing attention** tile shows the number of BOM and formula lines that have been released to the warehouse, that have unprocessed work, and that have a raw material date that is earlier than or the same as the workspace date.</span></span> <span data-ttu-id="712e9-145">应用到工作区筛选器的操作资源也必须使用该行。</span><span class="sxs-lookup"><span data-stu-id="712e9-145">The lines must also be consumed by an operation resource that applies to the filter of the workspace.</span></span>

<span data-ttu-id="712e9-146">选择磁贴后，**所有工作**页打开。</span><span class="sxs-lookup"><span data-stu-id="712e9-146">When the tile is selected, the **All work** page is opened.</span></span> <span data-ttu-id="712e9-147">此页按包含来自满足该磁贴条件的已发放物料清单和配方行的工作行的开放工作标题的数量进行筛选。</span><span class="sxs-lookup"><span data-stu-id="712e9-147">This page is filtered by the number of open work headers that contain work lines from released BOM and formula lines that meet the criteria for the tile.</span></span> <span data-ttu-id="712e9-148">在**所有工作**页上，您可以手动处理工作。</span><span class="sxs-lookup"><span data-stu-id="712e9-148">From the **All work** page, you can manually process the work.</span></span>
