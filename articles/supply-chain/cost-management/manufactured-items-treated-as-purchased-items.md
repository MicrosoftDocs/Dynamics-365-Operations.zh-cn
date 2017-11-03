---
title: "设置可以生产或采购的产品"
description: "产品可以以各种方式采购：可以生产（制造）或采购（购买）。 本文介绍在您配置产品以支持多方采购时要考虑的一些典型问题。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5ed8c93c13746249605ad8742549c23bb1e0e10
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="02a90-104">设置可以生产或采购的产品</span><span class="sxs-lookup"><span data-stu-id="02a90-104">Set up products that can be produced or procured</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="02a90-105">产品可以以各种方式采购：可以生产（制造）或采购（购买）。</span><span class="sxs-lookup"><span data-stu-id="02a90-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="02a90-106">本文介绍在您配置产品以支持多方采购时要考虑的一些典型问题。</span><span class="sxs-lookup"><span data-stu-id="02a90-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="02a90-107">多来源通常用于偶尔制造的采购物料，或者，当主要是制造物料的物料发生更改以使其现在主要是采购物料时。</span><span class="sxs-lookup"><span data-stu-id="02a90-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="02a90-108">该物料首先被指定为制造物料，以便可以定义物料清单和工艺路线信息以及为物料支持生产订单。</span><span class="sxs-lookup"><span data-stu-id="02a90-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="02a90-109">生产类型应设置为**“物料清单”**（或者，对于流程生产，**“配方”**或**“联产品”**）。</span><span class="sxs-lookup"><span data-stu-id="02a90-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="02a90-110">当您使用标准成本时，可为制造物料计算物料成本记录。</span><span class="sxs-lookup"><span data-stu-id="02a90-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="02a90-111">但是，物料成本记录无法与您要用于采购目的的标准成本匹配。</span><span class="sxs-lookup"><span data-stu-id="02a90-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="02a90-112">在这种情况下，标准成本必须手动输入，并且为物料成本记录启用。</span><span class="sxs-lookup"><span data-stu-id="02a90-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="02a90-113">对于成本计算，请考虑使用特定物料清单和工艺路线以便在会计期间过程中代表产品的供应组合，随着时间的推移使差异最小化。</span><span class="sxs-lookup"><span data-stu-id="02a90-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="02a90-114">此外，一个站点的制造物料可以转移到其他站点。</span><span class="sxs-lookup"><span data-stu-id="02a90-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="02a90-115">因此，必须为物料转移的站点手动输入和启用物料的成本。</span><span class="sxs-lookup"><span data-stu-id="02a90-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="02a90-116">在您将该制造物料用作更高级别产品中的某一组件时，该组件的成本应被视作采购物料。</span><span class="sxs-lookup"><span data-stu-id="02a90-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="02a90-117">此准则适用，不论组件的成本是计算出的或手动输入的。</span><span class="sxs-lookup"><span data-stu-id="02a90-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="02a90-118">换言之，物料清单计算应将该物料的成本视作采购组件，而不是使用物料清单和工艺路线信息计算成本。</span><span class="sxs-lookup"><span data-stu-id="02a90-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> <span data-ttu-id="02a90-119">若要禁止此计算发生，请选择嵌入到分配给物料的物料清单计算组中的**“停止分解”**标志。</span><span class="sxs-lookup"><span data-stu-id="02a90-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="02a90-120">若要禁止主计划编制计算通过物料分解需求，请在物料覆盖范围中或覆盖范围组中将分解时限设置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="02a90-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="02a90-121">主计划编制计算将物料视作采购物料，并且将不为其物料清单和工艺路线信息执行进一步的计算。</span><span class="sxs-lookup"><span data-stu-id="02a90-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






