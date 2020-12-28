---
title: 排除具有特定产品生命周期状态的产品
description: 此主题说明使用计划优化功能时如何基于产品的生命周期状态排除产品。
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 371d98eefa482fc3e430f2f0977ddffb9dd0d30e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645083"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="6036f-103">排除具有特定产品生命周期状态的产品</span><span class="sxs-lookup"><span data-stu-id="6036f-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6036f-104">已发布产品和已发布产品版本包括 **产品生命周期状态** 字段。</span><span class="sxs-lookup"><span data-stu-id="6036f-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="6036f-105">此字段让您可以控制主计划期间包括哪些产品以及其他一些方面。</span><span class="sxs-lookup"><span data-stu-id="6036f-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="6036f-106">您可以转到 **产品信息管理 \> 设置 \> 产品生命周期状态**，根据需要添加、删除和编辑生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="6036f-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="6036f-107">对于每个产品生命周期状态，如果在主计划期间应包括具有该状态的产品，则将 **对于计划有效** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="6036f-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="6036f-108">当此选项设置为 *否* 时，关联的产品和变型将在物料清单 (BOM) 级别从所有主计划和所有计算中排除。</span><span class="sxs-lookup"><span data-stu-id="6036f-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="6036f-109">**产品生命周期状态** 字段留为空白的已发布产品和变型，将被作为他们的产品生命周期状态的 **对于计划有效** 选项设置为 *是* 来处理。</span><span class="sxs-lookup"><span data-stu-id="6036f-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="6036f-110">换言之，它们将包括在主计划中。</span><span class="sxs-lookup"><span data-stu-id="6036f-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="6036f-111">为帮助避免不必要的供应建议，我们强烈建议您将所有过时的已发布产品和变型与产品生命周期状态关联，并将 **对于计划有效** 选项设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="6036f-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="6036f-112">当您使用不可重用的产品配置变型时，此方法特别重要，因为它可以帮助防止浪费。</span><span class="sxs-lookup"><span data-stu-id="6036f-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="6036f-113">相关资源</span><span class="sxs-lookup"><span data-stu-id="6036f-113">Related resources</span></span>

<span data-ttu-id="6036f-114">有关产品生命周期状态的详细信息，请参阅[产品生命周期状态概述](../../pim/product-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="6036f-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="6036f-115">有关包括使用产品生命周期状态将产品从主计划和物料清单级别计算中排除的步骤的详细信息，请参阅[创建产品生命周期状态以从主计划中排除产品](../../pim/tasks/exclude-products-master-planning.md)。</span><span class="sxs-lookup"><span data-stu-id="6036f-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
