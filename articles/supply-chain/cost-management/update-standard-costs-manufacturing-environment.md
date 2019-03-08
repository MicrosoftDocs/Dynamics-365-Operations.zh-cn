---
title: 更新制造环境中的标准成本
description: 本文提供有关如何在非制造环境中更新标准成本的指导。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fccfcec3d74bd13aa1b6511ebd37ee1454d1b47b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "332349"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="a6681-103">更新制造环境中的标准成本</span><span class="sxs-lookup"><span data-stu-id="a6681-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6681-104">本文提供有关如何在非制造环境中更新标准成本的指导。</span><span class="sxs-lookup"><span data-stu-id="a6681-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="a6681-105">更新可以反映新物料、成本类别或间接成本计算公式。</span><span class="sxs-lookup"><span data-stu-id="a6681-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="a6681-106">它们还可以反映更正和成本变化。</span><span class="sxs-lookup"><span data-stu-id="a6681-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="a6681-107">此类型的更新影响更新标准成本必须完成的步骤，如以下情况中所示：</span><span class="sxs-lookup"><span data-stu-id="a6681-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="a6681-108">为采购的物料输入预期的标准成本变化，然后更改相应日期上的物料成本记录的状态为**活动**状态。</span><span class="sxs-lookup"><span data-stu-id="a6681-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="a6681-109">但是，不重新计算使用采购物料的制造物料的成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="a6681-110">为新采购的物料输入标准成本，但不重新计算具有将这一新采购物料作为组件包含的物料清单 (BOM) 版本的制造物料的成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="a6681-111">更正或更改采购物料的成本，或者更改分配给采购物料的成本组，并且为具有将采购物料作为组件包含的物料清单版本的所有制造物料计算成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="a6681-112">为某一成本类别更改成本，并且为具有包含使用该成本类别的工艺路线工序的工艺路线版本的所有制造物料计算成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="a6681-113">更改分配给工艺路线工序的成本组或分配给成本类别的成本组的成本类别。</span><span class="sxs-lookup"><span data-stu-id="a6681-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="a6681-114">然后为具有包含使用该成本类别的工艺路线工序的工艺路线版本的所有制造物料计算成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="a6681-115">更改间接成本计算公式，并且为该更改影响的所有制造物料计算成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="a6681-116">更改或添加制造物料的制造站点，并且为该站点计算物料的制造成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="a6681-117">计算（或重新计算）某一制造物料的成本，并且为具有将该制造物料作为组件包含的物料清单版本的所有制造物料重新计算成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="a6681-118">基于新制造物料的已定义、审核和活动的物料清单和工艺路线信息，计算此物料的成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="a6681-119">每种情况都要求仔细考虑如何更新标准成本。</span><span class="sxs-lookup"><span data-stu-id="a6681-119">Each case requires careful consideration about how to update standard costs.</span></span>



