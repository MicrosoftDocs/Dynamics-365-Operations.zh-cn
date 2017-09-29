---
title: "确定物料清单版本"
description: "在需求分解过程中，如果某一物料具有“生产”这一默认订单类型，计划引擎将基于站点查找有效的物料清单版本。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ceeb82130a3ab214ef3e9eda09294c9bcc0c7cc0
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="determine-the-bom-version"></a><span data-ttu-id="0009a-103">确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="0009a-103">Determine the BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0009a-104">在需求分解过程中，如果某一物料具有“生产”这一默认订单类型，计划引擎将基于站点查找有效的物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="0009a-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="0009a-105">此站点维度始终是已知的，并且已在需求交易记录上指明。</span><span class="sxs-lookup"><span data-stu-id="0009a-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="0009a-106">用于确定要使用的物料清单版本的如下流程：</span><span class="sxs-lookup"><span data-stu-id="0009a-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="0009a-107">如果在需求站点为物料定义了物料清单版本，将使用特定于站点的物料清单。</span><span class="sxs-lookup"><span data-stu-id="0009a-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="0009a-108">如果在需求站点为物料定义了不特定于站点的物料清单版本，将使用通用物料清单。</span><span class="sxs-lookup"><span data-stu-id="0009a-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="0009a-109">通用物料清单不指明站点，对多个站点都有效。</span><span class="sxs-lookup"><span data-stu-id="0009a-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="0009a-110">如果存在通用物料清单，则使用。</span><span class="sxs-lookup"><span data-stu-id="0009a-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="0009a-111">如果没有可供使用的通用物料清单，需求分解将到此为止。</span><span class="sxs-lookup"><span data-stu-id="0009a-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="0009a-112">有效的物料清单版本，不论是特定于站点还是通用，都必须符合要求的日期和数量条件。</span><span class="sxs-lookup"><span data-stu-id="0009a-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>






