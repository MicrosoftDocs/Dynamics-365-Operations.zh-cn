---
title: "物料清单版本的分解"
description: "本文介绍涉及物料清单 (BOM) 版本分解的主计划方案。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bce6ffd0ee284f2a5e5b5fef0bdfa92e192b2f42
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="bfb17-103">物料清单版本的分解</span><span class="sxs-lookup"><span data-stu-id="bfb17-103">Explosion of a BOM version</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bfb17-104">本文介绍涉及物料清单 (BOM) 版本分解的主计划方案。</span><span class="sxs-lookup"><span data-stu-id="bfb17-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="bfb17-105">某一物料清单版本的需求分解将创建在特定站点以及可能在特定仓库的每个物料清单行物料的需求。</span><span class="sxs-lookup"><span data-stu-id="bfb17-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="bfb17-106">在特定于站点的物料清单中，可为每一物料清单行定义特定的仓库。</span><span class="sxs-lookup"><span data-stu-id="bfb17-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="bfb17-107">此外，对于每个物料清单行，该物料的维度设置将确定该仓库是否是必需的。</span><span class="sxs-lookup"><span data-stu-id="bfb17-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="bfb17-108">然后，为每一物料清单行物料产生的这一需求将成为其他需求分解的起始点。</span><span class="sxs-lookup"><span data-stu-id="bfb17-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="bfb17-109">此主计划方案涉及以下情况：</span><span class="sxs-lookup"><span data-stu-id="bfb17-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="bfb17-110">站点维度是必填的，必须在需求交易记录上输入。</span><span class="sxs-lookup"><span data-stu-id="bfb17-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="bfb17-111">站点维度是一致的。</span><span class="sxs-lookup"><span data-stu-id="bfb17-111">The site dimension is consistent.</span></span> <span data-ttu-id="bfb17-112">因此，较低级别需求的站点与初始需求交易记录上的站点相同。</span><span class="sxs-lookup"><span data-stu-id="bfb17-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="bfb17-113">下图显示主计划编制需求分解的过程。</span><span class="sxs-lookup"><span data-stu-id="bfb17-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![使用物料清单版本的需求分解](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="bfb17-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="bfb17-115">See also</span></span>
--------

[<span data-ttu-id="bfb17-116">主计划 - 如何确定物料清单版本</span><span class="sxs-lookup"><span data-stu-id="bfb17-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="bfb17-117">主计划和多站点功能</span><span class="sxs-lookup"><span data-stu-id="bfb17-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




