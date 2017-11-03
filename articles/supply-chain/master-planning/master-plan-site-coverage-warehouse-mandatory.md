---
title: "站点覆盖范围的主计划，仓库为必需"
description: "此主题介绍如何计划将站点作为覆盖范围维度的物料。 仓库是必填维度。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ca01913a0338004fabcda5136108ec3c5be8ff7
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="e66d4-104">站点覆盖范围的主计划，仓库为必需</span><span class="sxs-lookup"><span data-stu-id="e66d4-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e66d4-105">此主题介绍如何计划将站点作为覆盖范围维度的物料。</span><span class="sxs-lookup"><span data-stu-id="e66d4-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="e66d4-106">仓库是必填维度。</span><span class="sxs-lookup"><span data-stu-id="e66d4-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="e66d4-107">此主计划方案涉及以下情况：</span><span class="sxs-lookup"><span data-stu-id="e66d4-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="e66d4-108">站点维度设置为必填，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="e66d4-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="e66d4-109">不能修改此设置。</span><span class="sxs-lookup"><span data-stu-id="e66d4-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="e66d4-110">仓库维度设置为必填，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="e66d4-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="e66d4-111">为覆盖范围计划设置站点维度。</span><span class="sxs-lookup"><span data-stu-id="e66d4-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="e66d4-112">还可能为覆盖范围计划设置其他维度。</span><span class="sxs-lookup"><span data-stu-id="e66d4-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="e66d4-113">但是，它们不受多站点功能的影响。</span><span class="sxs-lookup"><span data-stu-id="e66d4-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="e66d4-114">不为覆盖范围计划设置仓库维度。</span><span class="sxs-lookup"><span data-stu-id="e66d4-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="e66d4-115">因此，按站点和还可能按其他覆盖范围计划维度聚合供应和需求。</span><span class="sxs-lookup"><span data-stu-id="e66d4-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="e66d4-116">下图说明如何继续主计划。</span><span class="sxs-lookup"><span data-stu-id="e66d4-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="e66d4-117">图中引用的参数及其位置如下所示：</span><span class="sxs-lookup"><span data-stu-id="e66d4-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="e66d4-118">为物料定义物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="e66d4-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="e66d4-119">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="e66d4-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="e66d4-120">选择物料，然后单击**计划 &gt; 物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="e66d4-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="e66d4-121">为仓库定义重填关系。</span><span class="sxs-lookup"><span data-stu-id="e66d4-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="e66d4-122">单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。</span><span class="sxs-lookup"><span data-stu-id="e66d4-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="e66d4-123">在**主计划**选项卡上，查看**主仓库**字段组。</span><span class="sxs-lookup"><span data-stu-id="e66d4-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="e66d4-124">默认订单类型设置为“生产”、“采购订单”或“看板”。</span><span class="sxs-lookup"><span data-stu-id="e66d4-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="e66d4-125">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="e66d4-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="e66d4-126">选择物料，然后依次单击**计划 &gt; 默认订单设置**。</span><span class="sxs-lookup"><span data-stu-id="e66d4-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="e66d4-127">在**“默认订单设置”**窗体中，查看**“默认订单类型”**。</span><span class="sxs-lookup"><span data-stu-id="e66d4-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![站点需求（覆盖范围仓库必需）](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="e66d4-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="e66d4-129">See also</span></span>
--------

[<span data-ttu-id="e66d4-130">主计划和多站点功能</span><span class="sxs-lookup"><span data-stu-id="e66d4-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="e66d4-131">主计划 - 站点和仓库覆盖范围，仓库是必需的</span><span class="sxs-lookup"><span data-stu-id="e66d4-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="e66d4-132">主计划 - 站点覆盖范围，仓库是必需的</span><span class="sxs-lookup"><span data-stu-id="e66d4-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="e66d4-133">主计划 - 站点和仓库覆盖范围，仓库不是必需的</span><span class="sxs-lookup"><span data-stu-id="e66d4-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="e66d4-134">主计划 - 如何确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="e66d4-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




