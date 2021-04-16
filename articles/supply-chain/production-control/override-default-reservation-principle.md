---
title: 替代生产中的默认材料预留原则
description: 本主题介绍如何为每个物料模型组设置默认的预留原则，以可以将不同的预留原则自动应用于作为生产物料清单 (BOM) 或批次订单配方一部分的每个物料。
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a1b2dd204c9a507dba387b0295f3021253e02dc4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814794"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a><span data-ttu-id="dddbf-103">替代生产中的默认材料预留原则</span><span class="sxs-lookup"><span data-stu-id="dddbf-103">Override the default reservation principle for materials in production</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="dddbf-104">*替代默认生产预留* 功能可让您为每个物料模型组设置默认的预留原则。</span><span class="sxs-lookup"><span data-stu-id="dddbf-104">The *Override default production reservation* feature lets you set a default reservation principle for each item model group.</span></span> <span data-ttu-id="dddbf-105">因此，可以将不同预留原则自动应用于属于生产物料清单 (BOM) 或批次订单配方的一部分的每个物料。</span><span class="sxs-lookup"><span data-stu-id="dddbf-105">Therefore, different reservation principles can automatically be applied for each item that is part of a production bill of materials (BOM) or batch order formula.</span></span> <span data-ttu-id="dddbf-106">您可以选择是否每个物料模型组都应替代为订单设置的默认预留原则，以及应改为为使用哪个预留原则（*手动*、*估计*、*计划*、*下达* 或 *开始*）。</span><span class="sxs-lookup"><span data-stu-id="dddbf-106">You can select whether each item model group should override the default reservation principle that is set for an order, and what reservation principle should be used instead (*manual*, *estimation*, *scheduling*, *release*, or *start*).</span></span>

<span data-ttu-id="dddbf-107">创建新生产订单或批次订单时，系统会提示您选择应该应用于该订单及其所有 BOM 行或配方行的预留原则。</span><span class="sxs-lookup"><span data-stu-id="dddbf-107">When you create a new production order or batch order, you're prompted to select the reservation principle that should be applied to that order and all its BOM lines or formula lines.</span></span> <span data-ttu-id="dddbf-108">使用 *替代默认生产预留* 功能时，部分或全部 BOM 行或配方行可以替代该预留原则，改为使用为相关物料模型组设置的预留原则。</span><span class="sxs-lookup"><span data-stu-id="dddbf-108">When the *Override default production reservation* feature is used, some or all of the BOM or formula lines can override that reservation principle and instead use the reservation principle that is set for the relevant item model group.</span></span>

<span data-ttu-id="dddbf-109">例如，如果您有需要执行领料工作的原材料或成分，为这些产品创建的 BOM 行或配方行将需要实际预留，因为实际预留是生成仓库工作的先决条件。</span><span class="sxs-lookup"><span data-stu-id="dddbf-109">For example, if you have raw materials or ingredients that require pick work, BOM or formula lines that are created for those products require a physical reservation, because physical reservation is a prerequisite for the generation of warehouse work.</span></span> <span data-ttu-id="dddbf-110">通常，如果希望预留自动执行，请选择以下预留原则之一：*估计*、*计划*、*下达* 或 *开始*。</span><span class="sxs-lookup"><span data-stu-id="dddbf-110">Typically, if you want the reservation to occur automatically, you select one of the following reservation principles: *estimation*, *scheduling*, *release*, or *start*.</span></span> <span data-ttu-id="dddbf-111">另一方面，如果您有不需要领料的材料或成分，由于它们是直接从某个位置消耗，因此通常选择 *手动* 预留原则，这不会进行任何实际预留或产生任何领料工作。</span><span class="sxs-lookup"><span data-stu-id="dddbf-111">On the other hand, if you have materials or ingredients that don't require pick work, because they are consumed directly from a location, you typically select the *manual* reservation principle, which doesn't make any physical reservations or generate any pick work.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="dddbf-112">开启功能</span><span class="sxs-lookup"><span data-stu-id="dddbf-112">Turn on the feature</span></span>

<span data-ttu-id="dddbf-113">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="dddbf-113">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="dddbf-114">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="dddbf-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="dddbf-115">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="dddbf-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="dddbf-116">**模块**：*生产控制*</span><span class="sxs-lookup"><span data-stu-id="dddbf-116">**Module:** *Production control*</span></span>
- <span data-ttu-id="dddbf-117">**功能名称**：*（预览）替代默认生产预留*</span><span class="sxs-lookup"><span data-stu-id="dddbf-117">**Feature name:** *(Preview) Override default production reservation*</span></span>

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a><span data-ttu-id="dddbf-118">将生产预留策略分配给物料模型组</span><span class="sxs-lookup"><span data-stu-id="dddbf-118">Assign a production reservation policy to an item model group</span></span>

1. <span data-ttu-id="dddbf-119">转到 **成本管理 \> 库存会计政策设置 \> 物料模型组**。</span><span class="sxs-lookup"><span data-stu-id="dddbf-119">Go to **Cost management \> Inventory accounting policies setup \> Item model groups**.</span></span>
1. <span data-ttu-id="dddbf-120">创建或选择一个物料模型组。</span><span class="sxs-lookup"><span data-stu-id="dddbf-120">Create or select an item model group.</span></span>
1. <span data-ttu-id="dddbf-121">在 **库存策略** 快速选项卡上，选中 **替代物料生产预留** 复选框。</span><span class="sxs-lookup"><span data-stu-id="dddbf-121">On the **Inventory policies** FastTab, select the **Override item production reservation** check box.</span></span>
1. <span data-ttu-id="dddbf-122">在 **预留** 字段中，为属于所选模型组的物料选择预留原则。</span><span class="sxs-lookup"><span data-stu-id="dddbf-122">In the **Reservation** field, select the reservation principle for items that belong to the selected model group.</span></span> <span data-ttu-id="dddbf-123">（这些物料包括 BOM 行或配方行上的物料。）</span><span class="sxs-lookup"><span data-stu-id="dddbf-123">(Those items include items that are on a BOM or formula line.)</span></span>

    - <span data-ttu-id="dddbf-124">**手动** – 模型组中的物料不会自动进行实际预留来用于生产。</span><span class="sxs-lookup"><span data-stu-id="dddbf-124">**Manual** – Items in the model group won't automatically be physically reserved for production.</span></span> <span data-ttu-id="dddbf-125">但是，它们仍然可以根据需要手动预留。</span><span class="sxs-lookup"><span data-stu-id="dddbf-125">However, they can still be manually reserved as required.</span></span>
    - <span data-ttu-id="dddbf-126">**估计** – 在估计生产订单期间，模型组中的物料将被实际预留。</span><span class="sxs-lookup"><span data-stu-id="dddbf-126">**Estimation** – Items in the model group will be physically reserved during estimation of the production order.</span></span>
    - <span data-ttu-id="dddbf-127">**计划** – 在计划生产订单期间，模型组中的物料将被实际预留。</span><span class="sxs-lookup"><span data-stu-id="dddbf-127">**Scheduling** – Items in the model group will be physically reserved during scheduling of the production order.</span></span>
    - <span data-ttu-id="dddbf-128">**下达** – 在生产订单下达后，模型组中的物料将被实际预留。</span><span class="sxs-lookup"><span data-stu-id="dddbf-128">**Release** – Items in the model group will be physically reserved when the production order is released.</span></span>
    - <span data-ttu-id="dddbf-129">**开始** – 模型组中的物料将在生产订单开始时进行实际预留。</span><span class="sxs-lookup"><span data-stu-id="dddbf-129">**Start** – Items in the model group will be physically reserved at the start of the production order.</span></span>

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a><span data-ttu-id="dddbf-130">示例：在散装/包装场景中使用预留原则</span><span class="sxs-lookup"><span data-stu-id="dddbf-130">Example: Using reservation principles in a bulk/pack scenario</span></span>

<span data-ttu-id="dddbf-131">在 1,000 升混合器中生产了大量润滑材料。</span><span class="sxs-lookup"><span data-stu-id="dddbf-131">A bulk lubricant material is produced in a 1,000-liter mixer.</span></span> <span data-ttu-id="dddbf-132">散装材料准备好后，被泵送到几个灌装站，在那里灌入不同大小的瓶子。</span><span class="sxs-lookup"><span data-stu-id="dddbf-132">After the bulk material is ready, it's pumped out to several filling stations, where bottles of different sizes are filled.</span></span> <span data-ttu-id="dddbf-133">灌装完成后，瓶子使用箱子进行包装。</span><span class="sxs-lookup"><span data-stu-id="dddbf-133">After filling is completed, the bottles are packed into boxes.</span></span> <span data-ttu-id="dddbf-134">这些箱子然后再经过包装放到托盘上。</span><span class="sxs-lookup"><span data-stu-id="dddbf-134">Those boxes are then packed onto pallets.</span></span>

<span data-ttu-id="dddbf-135">在此场景中，将创建批次订单来生产 1,000 升散装材料。</span><span class="sxs-lookup"><span data-stu-id="dddbf-135">In this scenario, a batch order to make 1,000 liters of bulk material is created.</span></span> <span data-ttu-id="dddbf-136">（此订单为批次订单。）此批次订单完成后，将被报告为完工入库到灌装站的材料输入位置。</span><span class="sxs-lookup"><span data-stu-id="dddbf-136">(This order is the bulk order.) When this batch order is completed, it's reported as finished to the material input location of the filling stations.</span></span> <span data-ttu-id="dddbf-137">然后创建灌装和包装每种瓶子尺寸的批次订单。</span><span class="sxs-lookup"><span data-stu-id="dddbf-137">A batch order to fill and pack each bottle size is then created.</span></span> <span data-ttu-id="dddbf-138">（这些订单是包装订单。）包装订单具有由散装材料、空瓶、标签和其他包装材料组成的配方。</span><span class="sxs-lookup"><span data-stu-id="dddbf-138">(These orders are the pack orders.) The pack orders have a formula that consists of the bulk material, an empty bottle, a label, and other packing materials.</span></span> <span data-ttu-id="dddbf-139">由于散装材料直接从混合罐流向灌装站，因此无需执行仓库工作来选择此成分，而且散装材料直接从输入位置消耗。</span><span class="sxs-lookup"><span data-stu-id="dddbf-139">Because the bulk material flows directly from the mixer tank to the filling stations, no warehouse work is required to pick this ingredient, and the bulk material is consumed directly from the input location.</span></span> <span data-ttu-id="dddbf-140">所以，预留原则设置为 *手动*。</span><span class="sxs-lookup"><span data-stu-id="dddbf-140">Therefore, the reservation principle is set to *manual*.</span></span> <span data-ttu-id="dddbf-141">其他材料通过领料工作分批进入灌装站。</span><span class="sxs-lookup"><span data-stu-id="dddbf-141">The other materials are staged to the filling station by pick work.</span></span> <span data-ttu-id="dddbf-142">因此，这些行的预留原则设置为 *下达*，以实现在下达包装订单时自动进行预留等目的。</span><span class="sxs-lookup"><span data-stu-id="dddbf-142">Therefore, the reservation principle for these lines is set to *release*, for example, so that the reservation automatically occurs when the pack order is released.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]