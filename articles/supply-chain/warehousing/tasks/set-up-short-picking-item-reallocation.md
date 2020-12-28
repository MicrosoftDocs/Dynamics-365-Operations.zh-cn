---
title: 设置领料短缺的物料重新分配
description: 此主题显示如何启用仓库工作人员，以便在为其指示的货位的库存不足时，快速找到备用货位。
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423353"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="ba367-103">设置领料短缺的物料重新分配</span><span class="sxs-lookup"><span data-stu-id="ba367-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba367-104">此过程显示如何启用仓库工作人员，以便在为其指示的货位的库存不足时，快速找到备用货位。</span><span class="sxs-lookup"><span data-stu-id="ba367-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="ba367-105">重新分配过程由 **工作异常** 控制，由仓库 **工作人员** 使用。</span><span class="sxs-lookup"><span data-stu-id="ba367-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="ba367-106">可以使用自动和/或手动重新分配流程：</span><span class="sxs-lookup"><span data-stu-id="ba367-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="ba367-107">自动重新分配 - 货位指令用于确定另一个货位是否提供这些货物。</span><span class="sxs-lookup"><span data-stu-id="ba367-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="ba367-108">如果可以，将更新工作，并将仓库用户定向到备用货位。</span><span class="sxs-lookup"><span data-stu-id="ba367-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="ba367-109">手动重新分配 - 允许仓库用户在拥有未预留货物数量的一个或多个货位中进行选择。</span><span class="sxs-lookup"><span data-stu-id="ba367-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="ba367-110">自动加手动 - 如果系统无法执行自动重新分配，并且有货位具有未预留数量，将提示用户选择货位。</span><span class="sxs-lookup"><span data-stu-id="ba367-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="ba367-111">设置工作异常</span><span class="sxs-lookup"><span data-stu-id="ba367-111">Set up work exceptions</span></span>
<span data-ttu-id="ba367-112">可以使用不同物料重新分配策略定义多个工作异常，以便让仓库工作人员可以根据处理的装运需求选择一个。</span><span class="sxs-lookup"><span data-stu-id="ba367-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="ba367-113">创建此过程时使用的是 USMF 演示数据格式。</span><span class="sxs-lookup"><span data-stu-id="ba367-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="ba367-114">在 **导航窗格** 中，转到 **仓库管理 > 设置 > 工作 > 工作异常**。</span><span class="sxs-lookup"><span data-stu-id="ba367-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="ba367-115">单击 **新建**</span><span class="sxs-lookup"><span data-stu-id="ba367-115">Click **New**</span></span> 
3. <span data-ttu-id="ba367-116">在 **工作异常代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ba367-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="ba367-117">这将是此异常的标题。</span><span class="sxs-lookup"><span data-stu-id="ba367-117">This will be the title of this exception .</span></span> <span data-ttu-id="ba367-118">例如，“手动领料短缺”。</span><span class="sxs-lookup"><span data-stu-id="ba367-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="ba367-119">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ba367-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="ba367-120">这将是此异常的使用情况简短说明。</span><span class="sxs-lookup"><span data-stu-id="ba367-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="ba367-121">例如，“领料短缺 - 物料不可用”。</span><span class="sxs-lookup"><span data-stu-id="ba367-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="ba367-122">在 **异常类型** 字段中，选择 **领料短缺**。</span><span class="sxs-lookup"><span data-stu-id="ba367-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="ba367-123">选中 **调整库存** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ba367-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="ba367-124">如果选中，领料短缺货位自动将库存调整为 0。</span><span class="sxs-lookup"><span data-stu-id="ba367-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="ba367-125">在 **默认调整类型代码** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ba367-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="ba367-126">例如，在 USMF 中，可以选择 **删除 Res Adj Out**。每个调整类型代码中包含四个特征：名称、说明、库存日记帐名称和 **删除预留**。</span><span class="sxs-lookup"><span data-stu-id="ba367-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="ba367-127">如果启用了 **删除预留**，将删除领料短缺行的预留。</span><span class="sxs-lookup"><span data-stu-id="ba367-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="ba367-128">在 **物料重新分配** 字段中，选择一个值，如“手动”。</span><span class="sxs-lookup"><span data-stu-id="ba367-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="ba367-129">如果选择“手动”或“自动和手动”，需要启用仓库工作人员才能使用手动重新分配。</span><span class="sxs-lookup"><span data-stu-id="ba367-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="ba367-130">设置工作人员以使用物料手动重新分配</span><span class="sxs-lookup"><span data-stu-id="ba367-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="ba367-131">创建此过程时使用的是 USMF 演示数据格式。</span><span class="sxs-lookup"><span data-stu-id="ba367-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="ba367-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ba367-132">Close the page.</span></span>
2. <span data-ttu-id="ba367-133">在 **导航窗格** 中，转到 **仓库管理 > 设置 > 工作人员**。</span><span class="sxs-lookup"><span data-stu-id="ba367-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="ba367-134">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="ba367-134">Click **Edit**.</span></span>
4. <span data-ttu-id="ba367-135">在列表中，选择工作人员。</span><span class="sxs-lookup"><span data-stu-id="ba367-135">In the list, select worker.</span></span> <span data-ttu-id="ba367-136">例如，Julia Funderburk。</span><span class="sxs-lookup"><span data-stu-id="ba367-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="ba367-137">展开 **用户** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="ba367-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="ba367-138">在列表中选择一个 **用户 ID**。</span><span class="sxs-lookup"><span data-stu-id="ba367-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="ba367-139">例如，24。</span><span class="sxs-lookup"><span data-stu-id="ba367-139">For example, 24.</span></span>
7. <span data-ttu-id="ba367-140">展开 **工作** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="ba367-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="ba367-141">在 **允许手动重新分配物料** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="ba367-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
