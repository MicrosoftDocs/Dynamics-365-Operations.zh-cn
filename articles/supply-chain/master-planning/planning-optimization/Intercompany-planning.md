---
title: 内部公司计划
description: 本主题介绍内部公司计划，并说明如何在 Microsoft Dynamics 365 Supply Chain Management 中使用计划优化配置内部公司计划。
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd498489e18eaba81720757faa14c0bf7b7d67f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263390"
---
# <a name="intercompany-planning"></a><span data-ttu-id="5d8dc-103">内部公司计划</span><span class="sxs-lookup"><span data-stu-id="5d8dc-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d8dc-104">对于某些组织，物流工序取决于组织中的其他法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="5d8dc-105">由于每个法人都有单独的会计科目表，因此使用内部公司销售和采购来处理这些工序。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="5d8dc-106">本主题介绍内部公司计划，并说明如何在 Microsoft Dynamics 365 Supply Chain Management 中使用计划优化配置内部公司计划。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="5d8dc-107">本主题使用以下重要的内部公司术语：</span><span class="sxs-lookup"><span data-stu-id="5d8dc-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="5d8dc-108">**上游** – 公司或供应链中的相对参考。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="5d8dc-109">它指示以原材料供应商的方向变动。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="5d8dc-110">**下游** – 公司或供应链中的相对参考。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="5d8dc-111">它指示以客户的方向变动。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="5d8dc-112">**计划内部公司需求** – 公司的产品的计划需求，基于下游公司的产品的计划需求。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="5d8dc-113">在主计划中，一家公司的计划可以包括与另一家公司计划的计划订单相关的计划内部公司需求。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="5d8dc-114">此功能非常有用，因为它可以全面了解公司之间的计划订单。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="5d8dc-115">它还可以确保创建所有必需的计划供应订单，但无需为内部公司需求确定计划订单。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="5d8dc-116">如果从包含计划下游需求的主计划中运行主计划，来自相关内部公司供应商的计划采购订单将作为需求包括在计划中。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="5d8dc-117">所需的设置</span><span class="sxs-lookup"><span data-stu-id="5d8dc-117">Required setup</span></span>

<span data-ttu-id="5d8dc-118">若要使用内部公司计划，必须按照以下方式准备系统：</span><span class="sxs-lookup"><span data-stu-id="5d8dc-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="5d8dc-119">必须在所有相关公司中发布相关产品。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="5d8dc-120">有关详细信息，请参阅 Microsoft Learn 上的[在 Dynamics 365 Supply Chain Management 中配置和使用内部公司交易](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/)。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="5d8dc-121">下游需求必须通过与上游公司具有内部公司关系以及具有客户的相关默认库存维度（站点和仓库）的供应商购买来满足。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="5d8dc-122">有关详细信息，请参阅 Microsoft Learn 上的[在 Dynamics 365 Supply Chain Management 中配置和使用内部公司交易](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/)。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="5d8dc-123">上游公司的主计划必须包括计划的下游需求，并且相关公司和主计划必须在下游计划中指定。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="5d8dc-124">包括计划的下游需求</span><span class="sxs-lookup"><span data-stu-id="5d8dc-124">Include planned downstream demand</span></span>

<span data-ttu-id="5d8dc-125">按照以下步骤配置主计划以使其包括计划的下游需求。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="5d8dc-126">转到 **主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="5d8dc-127">选择或创建主计划。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="5d8dc-128">在 **内部公司计划** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="5d8dc-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="5d8dc-129">**包括计划的下游需求** – 将此选项设置为 *是* 以为主计划启用内部公司计划。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="5d8dc-130">**下游计划** – 如果将 **包括计划的下游需求** 选项设置为 *是*，使用工具栏和网格从其他公司添加所需的主规划。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="5d8dc-131">使用多级限定标准跨公司限定</span><span class="sxs-lookup"><span data-stu-id="5d8dc-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="5d8dc-132">在多级限定标准中，您可以查看跨公司限定标准，以查看供应所涵盖的初始需求来源。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="5d8dc-133">若要查看多级限定标准信息，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="5d8dc-134">转到 **主计划 \> 主计划 \> 计划订单**。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="5d8dc-135">选择或打开计划订单。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="5d8dc-136">在操作窗格的 **视图** 选项卡上，在 **要求** 组中，选择 **多级限定标准**。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="5d8dc-137">涉及两家公司的内部公司示例</span><span class="sxs-lookup"><span data-stu-id="5d8dc-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="5d8dc-138">对于此示例，在 USMF 公司中创建计划生产订单以覆盖 DEMF 公司中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="5d8dc-139">在 USMF 中，直接需求是计划内部公司需求。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="5d8dc-140">若要使此需求显示在 USMF 中，请先在 DEMF 中运行主规划，然后再在 USMF 中运行。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="5d8dc-141">下图显示此示例如何显示在计划生产订单的 **多级限定标准** 页面上。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![涉及两家公司的内部公司示例](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="5d8dc-143">涉及三家公司的内部公司示例</span><span class="sxs-lookup"><span data-stu-id="5d8dc-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="5d8dc-144">对于此示例，在 USMF 公司中创建计划采购订单以覆盖 FRRT 公司中的销售订单。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="5d8dc-145">在 DEMF 和 USMF 公司中，直接需求是计划内部公司需求。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="5d8dc-146">若要使此需求显示在 USMF 中，请先在 FRRT 中运行主规划，然后再在 DEMF 中运行，最后在 USMF 中运行。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="5d8dc-147">下图显示此示例如何显示在计划生产订单的 **多级限定标准** 页面上。</span><span class="sxs-lookup"><span data-stu-id="5d8dc-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![涉及三家公司的内部公司示例](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]