---
title: 不符合项的隔离区域
description: 本主题介绍如何创建和使用不符合项的隔离区域。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021796"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="73572-103">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="73572-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73572-104">本主题介绍如何创建和使用不符合项的隔离区域。</span><span class="sxs-lookup"><span data-stu-id="73572-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="73572-105">您将使用 **隔离区域** 页定义可以分配给不符合项的区域。</span><span class="sxs-lookup"><span data-stu-id="73572-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="73572-106">创建不符合项时，您可以在 **不符合项** 页的 **常规** 选项卡上设置 **隔离区域** 和 **隔离类型** 字段。</span><span class="sxs-lookup"><span data-stu-id="73572-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="73572-107">**隔离区域** 字段通常指示物料所在的区域或位置。</span><span class="sxs-lookup"><span data-stu-id="73572-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="73572-108">**隔离类型** 字段将物料定义为 *限制使用* 或者 *不可用*。</span><span class="sxs-lookup"><span data-stu-id="73572-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="73572-109">当您打印不符合项或不符合项的更正报告时，您可以查看物料所在的隔离区域。</span><span class="sxs-lookup"><span data-stu-id="73572-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="73572-110">您还可以为不符合项打印不符合项标记。</span><span class="sxs-lookup"><span data-stu-id="73572-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="73572-111">此报告显示分配的隔离区域和有关使用情况的信息，以提供应如何处理有缺陷物料的指导。</span><span class="sxs-lookup"><span data-stu-id="73572-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="73572-112">隔离区域可以与库存库位或运营资源对应。</span><span class="sxs-lookup"><span data-stu-id="73572-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="73572-113">隔离区域示例</span><span class="sxs-lookup"><span data-stu-id="73572-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="73572-114">示例 1</span><span class="sxs-lookup"><span data-stu-id="73572-114">Example 1</span></span>

<span data-ttu-id="73572-115">您在一家电子制造公司工作，该公司生产和分销电视、扬声器和媒体播放器。</span><span class="sxs-lookup"><span data-stu-id="73572-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="73572-116">在这种情况下，您可以配置隔离区域来表示每种类型的产品。</span><span class="sxs-lookup"><span data-stu-id="73572-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="73572-117">示例 2</span><span class="sxs-lookup"><span data-stu-id="73572-117">Example 2</span></span>

<span data-ttu-id="73572-118">三个箱子和两个架子用来存放未达标的物料。</span><span class="sxs-lookup"><span data-stu-id="73572-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="73572-119">在这种情况下，您可以配置五个隔离区域，每个箱子和每个架子各一个。</span><span class="sxs-lookup"><span data-stu-id="73572-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="73572-120">创建隔离区域</span><span class="sxs-lookup"><span data-stu-id="73572-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="73572-121">转到 **库存管理 \> 设置 \> 质量管理 \> 隔离区域**。</span><span class="sxs-lookup"><span data-stu-id="73572-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="73572-122">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="73572-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="73572-123">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="73572-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="73572-124">**隔离区域** – 为隔离区域输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="73572-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="73572-125">**描述** – 输入隔离区域的详细描述。</span><span class="sxs-lookup"><span data-stu-id="73572-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="73572-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="73572-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73572-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="73572-127">Additional resources</span></span>

- [<span data-ttu-id="73572-128">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="73572-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="73572-129">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="73572-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="73572-130">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="73572-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="73572-131">不符合项的问题类型</span><span class="sxs-lookup"><span data-stu-id="73572-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="73572-132">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="73572-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="73572-133">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="73572-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="73572-134">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="73572-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="73572-135">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="73572-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
