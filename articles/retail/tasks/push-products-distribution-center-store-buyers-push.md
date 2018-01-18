--- 
title: "使用集中采购配送将产品从配送中心配送到商店"
description: "此程序会逐步演示如何创建和处理集中采购配送，以将产品从一个位置配送到一个或许多商店。"
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: fc14a4e013eadaa5b4b1df357f0c646ab68b6072
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="b65cb-103">使用集中采购配送将产品从配送中心配送到商店</span><span class="sxs-lookup"><span data-stu-id="b65cb-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b65cb-104">此程序会逐步演示如何创建和处理集中采购配送，以将产品从一个位置配送到一个或许多商店。</span><span class="sxs-lookup"><span data-stu-id="b65cb-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="b65cb-105">用户可以定义多个配置，并让系统建议如何配送产品，或手动输入物料的配送目的地，以及如何配送到每一个商店。</span><span class="sxs-lookup"><span data-stu-id="b65cb-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="b65cb-106">此程序不包括可用于集中采购配送的数据的设置，例如补货规则、组织层次结构和商店权重。</span><span class="sxs-lookup"><span data-stu-id="b65cb-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="b65cb-107">此程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="b65cb-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="b65cb-108">转至“集中采购配送”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="b65cb-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-109">Click New.</span></span>
3. <span data-ttu-id="b65cb-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b65cb-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b65cb-111">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b65cb-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="b65cb-112">在“仓库”字段中，输入或选择一个带有库存数量的产品的仓库。</span><span class="sxs-lookup"><span data-stu-id="b65cb-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="b65cb-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-113">Click Add.</span></span>
7. <span data-ttu-id="b65cb-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b65cb-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b65cb-115">在“物料编号”字段中，输入或选择一个产品。</span><span class="sxs-lookup"><span data-stu-id="b65cb-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="b65cb-116">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-116">Click Add.</span></span>
10. <span data-ttu-id="b65cb-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b65cb-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b65cb-118">在“物料编号”字段中，输入或选择一个变型产品。</span><span class="sxs-lookup"><span data-stu-id="b65cb-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="b65cb-119">在输入变型产品时，将会为每个变型产品创建行。</span><span class="sxs-lookup"><span data-stu-id="b65cb-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="b65cb-120">在列表中，标记一行。</span><span class="sxs-lookup"><span data-stu-id="b65cb-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="b65cb-121">在“已配送数量”字段中，输入您想要配送的选定产品的数量。</span><span class="sxs-lookup"><span data-stu-id="b65cb-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="b65cb-122">在“其他配送数量”字段中，输入拥有可用配送数量的产品的数量。</span><span class="sxs-lookup"><span data-stu-id="b65cb-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="b65cb-123">在“配送”字段中，输入“位置权重”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="b65cb-124">您可以选择其他类型，以使用其他配送规则。</span><span class="sxs-lookup"><span data-stu-id="b65cb-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="b65cb-125">在“补货层次结构”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="b65cb-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="b65cb-126">选择“遵守分类”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="b65cb-127">单击“计算数量”并审查已添加到“仓库”部分的行中的数量。</span><span class="sxs-lookup"><span data-stu-id="b65cb-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="b65cb-128">单击“创建订单”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-128">Click Create order.</span></span>
20. <span data-ttu-id="b65cb-129">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="b65cb-129">Click Yes.</span></span>


