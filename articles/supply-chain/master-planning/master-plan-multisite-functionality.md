---
title: 主计划和多站点功能概览
description: 主计划考虑站点和仓库库存维度的设置。
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b26ff5c2f580c30113b82302bbad744bbf285ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213714"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="a0a31-103">主计划和多站点功能概览</span><span class="sxs-lookup"><span data-stu-id="a0a31-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0a31-104">主计划考虑站点和仓库库存维度的设置。</span><span class="sxs-lookup"><span data-stu-id="a0a31-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="a0a31-105">站点维度是必需的，您还可以将仓库维度设置为必需。</span><span class="sxs-lookup"><span data-stu-id="a0a31-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="a0a31-106">维度是必填时，必须为所有库存交易记录输入维度值。</span><span class="sxs-lookup"><span data-stu-id="a0a31-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="a0a31-107">因此，在编制主计划期间，初始需求的站点和仓库是已知的。</span><span class="sxs-lookup"><span data-stu-id="a0a31-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="a0a31-108">站点维度还必须是一致的，以便在分解更低级别的需求期间站点值保持不变。</span><span class="sxs-lookup"><span data-stu-id="a0a31-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="a0a31-109">仓库未设置为必填时，不能从初始需求知道仓库。</span><span class="sxs-lookup"><span data-stu-id="a0a31-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="a0a31-110">计划引擎必须根据为该物料定义的设置、各个仓库以及订单行的详细信息确定要使用哪个仓库。</span><span class="sxs-lookup"><span data-stu-id="a0a31-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="a0a31-111">以下主题说明在定义不同设置时计划引擎如何确定要使用的仓库。</span><span class="sxs-lookup"><span data-stu-id="a0a31-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="a0a31-112">站点和仓库覆盖范围的主计划（仓库必需）</span><span class="sxs-lookup"><span data-stu-id="a0a31-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="a0a31-113">站点覆盖范围的主计划（仓库必需）</span><span class="sxs-lookup"><span data-stu-id="a0a31-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="a0a31-114">站点和仓库覆盖范围的主计划（仓库非必需）</span><span class="sxs-lookup"><span data-stu-id="a0a31-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="a0a31-115">站点覆盖范围的主计划（仓库非必需）</span><span class="sxs-lookup"><span data-stu-id="a0a31-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="a0a31-116">确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="a0a31-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



