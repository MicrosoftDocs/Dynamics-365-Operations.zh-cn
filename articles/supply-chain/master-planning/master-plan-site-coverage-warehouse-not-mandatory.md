---
title: "站点覆盖范围的主计划，仓库非必需"
description: "此主题介绍如何计划为覆盖范围设置站点维度的物料。"
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 79582e92daeaf0afb032448d36be12edd0926089
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="62553-103">站点覆盖范围的主计划，仓库非必需</span><span class="sxs-lookup"><span data-stu-id="62553-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="62553-104">此主题介绍如何计划为覆盖范围设置站点维度的物料。</span><span class="sxs-lookup"><span data-stu-id="62553-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="62553-105">此主计划方案涉及以下情况：</span><span class="sxs-lookup"><span data-stu-id="62553-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="62553-106">站点维度设置为必填，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="62553-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="62553-107">仓库维度未设置为必填的。</span><span class="sxs-lookup"><span data-stu-id="62553-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="62553-108">仓库可能已知，但是它不在主计划计算中使用。</span><span class="sxs-lookup"><span data-stu-id="62553-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="62553-109">为覆盖范围计划设置站点维度。</span><span class="sxs-lookup"><span data-stu-id="62553-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="62553-110">不为覆盖范围计划设置仓库维度。</span><span class="sxs-lookup"><span data-stu-id="62553-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="62553-111">因此，按站点和还可能按其他覆盖范围计划维度聚合供应和需求。</span><span class="sxs-lookup"><span data-stu-id="62553-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="62553-112">下图说明如何继续主计划。</span><span class="sxs-lookup"><span data-stu-id="62553-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="62553-113">图中引用的参数及其位置如下所示：</span><span class="sxs-lookup"><span data-stu-id="62553-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="62553-114">为物料定义物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="62553-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="62553-115">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="62553-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="62553-116">选择物料，然后单击**计划 &gt; 物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="62553-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="62553-117">为仓库定义重填关系。</span><span class="sxs-lookup"><span data-stu-id="62553-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="62553-118">单击**库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。</span><span class="sxs-lookup"><span data-stu-id="62553-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="62553-119">在**主计划**选项卡上，查看**主仓库**字段组。</span><span class="sxs-lookup"><span data-stu-id="62553-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="62553-120">默认订单类型设置为“生产”、“采购订单”或“看板”。</span><span class="sxs-lookup"><span data-stu-id="62553-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="62553-121">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="62553-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="62553-122">选择物料，然后依次单击**计划 &gt; 默认订单设置**。</span><span class="sxs-lookup"><span data-stu-id="62553-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="62553-123">在**“默认订单设置”**窗体中，查看**“默认订单类型”**字段。</span><span class="sxs-lookup"><span data-stu-id="62553-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![站点需求（覆盖范围仓库非必需）](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a><span data-ttu-id="62553-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="62553-125">See also</span></span>
--------

[<span data-ttu-id="62553-126">主计划和多站点功能</span><span class="sxs-lookup"><span data-stu-id="62553-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="62553-127">主计划 - 站点覆盖范围，仓库是必需的</span><span class="sxs-lookup"><span data-stu-id="62553-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="62553-128">主计划 - 站点和仓库覆盖范围，仓库不是必需的</span><span class="sxs-lookup"><span data-stu-id="62553-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="62553-129">主计划 - 站点和仓库覆盖范围，仓库是必需的</span><span class="sxs-lookup"><span data-stu-id="62553-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="62553-130">主计划 - 如何确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="62553-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



