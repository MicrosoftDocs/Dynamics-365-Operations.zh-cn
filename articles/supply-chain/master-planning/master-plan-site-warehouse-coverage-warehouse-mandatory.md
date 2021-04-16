---
title: 站点和仓库覆盖范围主计划，仓库是必需的
description: 此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。 仓库维度是必填的。
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce4960ed6406587557ce12b72b30fa9a620d6b18
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833489"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="adbde-104">站点和仓库覆盖范围主计划，仓库是必需的</span><span class="sxs-lookup"><span data-stu-id="adbde-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adbde-105">此主题介绍如何计划将站点和仓库作为覆盖范围维度的物料。</span><span class="sxs-lookup"><span data-stu-id="adbde-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="adbde-106">仓库维度是必填的。</span><span class="sxs-lookup"><span data-stu-id="adbde-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="adbde-107">此主计划方案涉及以下情况：</span><span class="sxs-lookup"><span data-stu-id="adbde-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="adbde-108">站点维度设置为必填，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="adbde-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="adbde-109">仓库维度设置为必填，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="adbde-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="adbde-110">为覆盖范围计划设置站点和仓库维度。</span><span class="sxs-lookup"><span data-stu-id="adbde-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="adbde-111">还可能为覆盖范围计划设置其他维度。</span><span class="sxs-lookup"><span data-stu-id="adbde-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="adbde-112">但是，它们不受多站点功能的影响。</span><span class="sxs-lookup"><span data-stu-id="adbde-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="adbde-113">下图说明如何继续主计划。</span><span class="sxs-lookup"><span data-stu-id="adbde-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="adbde-114">图中引用的参数及其位置如下所示：</span><span class="sxs-lookup"><span data-stu-id="adbde-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="adbde-115">仓库设置为 **手动**。</span><span class="sxs-lookup"><span data-stu-id="adbde-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="adbde-116">单击 **库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。</span><span class="sxs-lookup"><span data-stu-id="adbde-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="adbde-117">在 **主计划** 快速选项卡上，查看 **手动** 字段。</span><span class="sxs-lookup"><span data-stu-id="adbde-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="adbde-118">为物料定义物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="adbde-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="adbde-119">单击 **产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="adbde-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="adbde-120">选择该物料，然后在“操作窗格”上，在 **计划** 选项卡上单击 **物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="adbde-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="adbde-121">为仓库定义重填关系。</span><span class="sxs-lookup"><span data-stu-id="adbde-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="adbde-122">单击 **库存管理 &gt; 设置 &gt; 库存细分 &gt; 仓库**。</span><span class="sxs-lookup"><span data-stu-id="adbde-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="adbde-123">在 **主计划** 快速选项卡上，查看 **主仓库** 字段组。</span><span class="sxs-lookup"><span data-stu-id="adbde-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="adbde-124">默认订单类型设置为“生产”、“采购订单”或“看板”。</span><span class="sxs-lookup"><span data-stu-id="adbde-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="adbde-125">单击 **产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="adbde-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="adbde-126">选择该物料，然后在“操作窗格”上，在 **计划** 选项卡上单击 **默认订单设置**。</span><span class="sxs-lookup"><span data-stu-id="adbde-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="adbde-127">在 **默认订单设置** 窗体中，查看 **默认订单类型**。</span><span class="sxs-lookup"><span data-stu-id="adbde-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![需求站点和仓库覆盖范围（仓库必需）](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="adbde-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="adbde-129">Additional resources</span></span>
--------

[<span data-ttu-id="adbde-130">主计划和多站点功能概览</span><span class="sxs-lookup"><span data-stu-id="adbde-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="adbde-131">站点覆盖范围的主计划（仓库必需）</span><span class="sxs-lookup"><span data-stu-id="adbde-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="adbde-132">站点覆盖范围的主计划（仓库非必需）</span><span class="sxs-lookup"><span data-stu-id="adbde-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="adbde-133">站点和仓库覆盖范围的主计划（仓库非必需）</span><span class="sxs-lookup"><span data-stu-id="adbde-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="adbde-134">确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="adbde-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]