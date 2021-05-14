---
title: 不符合项的操作
description: 本主题介绍如何创建和使用不符合项的操作。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956570"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="6ad70-103">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="6ad70-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ad70-104">本主题介绍如何创建和使用不符合项的操作。</span><span class="sxs-lookup"><span data-stu-id="6ad70-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="6ad70-105">您可以使用 **操作** 页定义可以对已审核的未达标执行的工作的分类。</span><span class="sxs-lookup"><span data-stu-id="6ad70-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="6ad70-106">向不符合项分配相关操作时，可以提供详细信息，如执行操作所需的关联物料、工时和费用。</span><span class="sxs-lookup"><span data-stu-id="6ad70-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="6ad70-107">系统将使用此信息计算操作的估计成本。</span><span class="sxs-lookup"><span data-stu-id="6ad70-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="6ad70-108">这些详细信息和预估成本用于参考。</span><span class="sxs-lookup"><span data-stu-id="6ad70-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="6ad70-109">针对质量的相关工序不同于可以为生产工艺路线定义的工序。</span><span class="sxs-lookup"><span data-stu-id="6ad70-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="6ad70-110">虽然您可以跟踪成本、时间和与不符合项相关的操作中使用的物料，但是您输入的数据仅作为参考信息。</span><span class="sxs-lookup"><span data-stu-id="6ad70-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="6ad70-111">它不会自动与总帐、库存子分类帐或 **考勤** 模块集成。</span><span class="sxs-lookup"><span data-stu-id="6ad70-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="6ad70-112">操作示例</span><span class="sxs-lookup"><span data-stu-id="6ad70-112">Examples of operations</span></span>

<span data-ttu-id="6ad70-113">您在一家制造公司工作。</span><span class="sxs-lookup"><span data-stu-id="6ad70-113">You work for a manufacturing company.</span></span> <span data-ttu-id="6ad70-114">为未通过质量测试的物料创建并批准了不符合项。</span><span class="sxs-lookup"><span data-stu-id="6ad70-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="6ad70-115">创建了更正，指示问题与机器上损坏的轴承有关。</span><span class="sxs-lookup"><span data-stu-id="6ad70-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="6ad70-116">更换轴承需要若干步骤，并会跟踪每个操作的责任方。</span><span class="sxs-lookup"><span data-stu-id="6ad70-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="6ad70-117">例如，可能需要执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6ad70-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="6ad70-118">停止生产线，执行清理程序。</span><span class="sxs-lookup"><span data-stu-id="6ad70-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="6ad70-119">维修人员更换轴承。</span><span class="sxs-lookup"><span data-stu-id="6ad70-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="6ad70-120">质量保证人员在重新启动机器之前对机器之进行检查。</span><span class="sxs-lookup"><span data-stu-id="6ad70-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="6ad70-121">对于此示例，可以创建以下操作来表示必须完成的工作：</span><span class="sxs-lookup"><span data-stu-id="6ad70-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="6ad70-122">停止生产线。</span><span class="sxs-lookup"><span data-stu-id="6ad70-122">Stop the production line.</span></span>
- <span data-ttu-id="6ad70-123">清理生产线。</span><span class="sxs-lookup"><span data-stu-id="6ad70-123">Clean out the production line.</span></span>
- <span data-ttu-id="6ad70-124">执行机器维修。</span><span class="sxs-lookup"><span data-stu-id="6ad70-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="6ad70-125">检查机器。</span><span class="sxs-lookup"><span data-stu-id="6ad70-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="6ad70-126">创建操作</span><span class="sxs-lookup"><span data-stu-id="6ad70-126">Create an operation</span></span>

1. <span data-ttu-id="6ad70-127">转到 **库存管理 \> 设置 \> 质量管理 \> 操作**。</span><span class="sxs-lookup"><span data-stu-id="6ad70-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="6ad70-128">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6ad70-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6ad70-129">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="6ad70-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6ad70-130">**操作** – 为操作输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="6ad70-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="6ad70-131">**描述** – 输入操作的详细描述。</span><span class="sxs-lookup"><span data-stu-id="6ad70-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="6ad70-132">**类型** – 如果操作只能用于与特定订单类型相关的不符合项，选择订单类型（*采购订单* 或 *销售订单*）。</span><span class="sxs-lookup"><span data-stu-id="6ad70-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="6ad70-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6ad70-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ad70-134">其他资源</span><span class="sxs-lookup"><span data-stu-id="6ad70-134">Additional resources</span></span>

- [<span data-ttu-id="6ad70-135">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="6ad70-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="6ad70-136">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="6ad70-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="6ad70-137">创建和处理不符合项</span><span class="sxs-lookup"><span data-stu-id="6ad70-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="6ad70-138">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="6ad70-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="6ad70-139">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="6ad70-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="6ad70-140">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="6ad70-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="6ad70-141">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="6ad70-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="6ad70-142">不符合项的问题类型</span><span class="sxs-lookup"><span data-stu-id="6ad70-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="6ad70-143">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="6ad70-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
