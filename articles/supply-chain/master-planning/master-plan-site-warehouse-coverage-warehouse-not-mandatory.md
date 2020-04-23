---
title: 站点和仓库覆盖范围主计划，仓库不是必需的
description: 此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。 仓库维度不是必填的。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df79b8ea9ab6e37960cfbf0ca0edcbbc21484db
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213622"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="57420-104">站点和仓库覆盖范围主计划，仓库不是必需的</span><span class="sxs-lookup"><span data-stu-id="57420-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57420-105">此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。</span><span class="sxs-lookup"><span data-stu-id="57420-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="57420-106">仓库维度不是必填的。</span><span class="sxs-lookup"><span data-stu-id="57420-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="57420-107">此主计划方案涉及以下情况：</span><span class="sxs-lookup"><span data-stu-id="57420-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="57420-108">站点维度设置为必填，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="57420-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="57420-109">不能修改此设置。</span><span class="sxs-lookup"><span data-stu-id="57420-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="57420-110">仓库维度未设置为必填的。</span><span class="sxs-lookup"><span data-stu-id="57420-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="57420-111">仓库可能已知，但是它不在主计划计算中使用。</span><span class="sxs-lookup"><span data-stu-id="57420-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="57420-112">为覆盖范围计划设置站点和仓库维度。</span><span class="sxs-lookup"><span data-stu-id="57420-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="57420-113">还可能为覆盖范围计划设置其他维度。</span><span class="sxs-lookup"><span data-stu-id="57420-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="57420-114">但是，它们不受多站点功能的影响。</span><span class="sxs-lookup"><span data-stu-id="57420-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="57420-115">下图说明如何继续主计划。</span><span class="sxs-lookup"><span data-stu-id="57420-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="57420-116">图中引用的参数及其位置如下所示：</span><span class="sxs-lookup"><span data-stu-id="57420-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="57420-117">仓库设置为“手动”。</span><span class="sxs-lookup"><span data-stu-id="57420-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="57420-118">单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。</span><span class="sxs-lookup"><span data-stu-id="57420-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="57420-119">在**主计划**快速选项卡上，查看**手动**字段。</span><span class="sxs-lookup"><span data-stu-id="57420-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="57420-120">为物料定义物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="57420-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="57420-121">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="57420-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="57420-122">选择该物料，然后在“操作窗格”上，在**计划**选项卡上单击**物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="57420-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="57420-123">为仓库定义重填关系。</span><span class="sxs-lookup"><span data-stu-id="57420-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="57420-124">单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。</span><span class="sxs-lookup"><span data-stu-id="57420-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="57420-125">在**主计划**快速选项卡上，查看**主仓库**字段组。</span><span class="sxs-lookup"><span data-stu-id="57420-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="57420-126">默认订单类型设置为“生产”、“采购订单”或“看板”。</span><span class="sxs-lookup"><span data-stu-id="57420-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="57420-127">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="57420-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="57420-128">选择该物料，然后在“操作窗格”上，在**计划**选项卡上单击**默认订单设置**。</span><span class="sxs-lookup"><span data-stu-id="57420-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="57420-129">在**默认订单设置**窗体中，查看**默认订单类型**。</span><span class="sxs-lookup"><span data-stu-id="57420-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![站点和仓库需求（仓库非必需）](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="57420-131">其他资源</span><span class="sxs-lookup"><span data-stu-id="57420-131">Additional resources</span></span>
--------

[<span data-ttu-id="57420-132">主计划和多站点功能概览</span><span class="sxs-lookup"><span data-stu-id="57420-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="57420-133">站点覆盖范围的主计划（仓库必需）</span><span class="sxs-lookup"><span data-stu-id="57420-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="57420-134">站点和仓库覆盖范围的主计划（仓库必需）</span><span class="sxs-lookup"><span data-stu-id="57420-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="57420-135">站点和仓库覆盖范围的主计划（仓库非必需）</span><span class="sxs-lookup"><span data-stu-id="57420-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="57420-136">确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="57420-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



