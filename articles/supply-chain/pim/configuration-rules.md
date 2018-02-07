---
title: "配置规则"
description: "本文提供有关配置规则的一般信息。 配置规则定义使用基于维度的配置技术的产品的物料清单 (BOM) 中物料之间的关系。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bc8e606cdc0bc5a45321c67ce9b089059f226df2
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="99871-104">配置规则</span><span class="sxs-lookup"><span data-stu-id="99871-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="99871-105">本文提供有关配置规则的一般信息。</span><span class="sxs-lookup"><span data-stu-id="99871-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="99871-106">配置规则定义使用基于维度的配置技术的产品的物料清单 (BOM) 中物料之间的关系。</span><span class="sxs-lookup"><span data-stu-id="99871-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="99871-107">在您定义基于维度的配置模型时，配置规则可用。</span><span class="sxs-lookup"><span data-stu-id="99871-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="99871-108">配置规则用于强制或禁止物料清单 (BOM) 的特定物料组合。</span><span class="sxs-lookup"><span data-stu-id="99871-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="99871-109">在物料清单创建后，并且相关物料分配给其各自配置组，一个或多个配置规则可以定义。</span><span class="sxs-lookup"><span data-stu-id="99871-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="99871-110">如果两个物料合成整体，**选择**运算符用于确保包含。</span><span class="sxs-lookup"><span data-stu-id="99871-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="99871-111">如果两个物料相互排斥，**取消选择**运算符用于确保排除。</span><span class="sxs-lookup"><span data-stu-id="99871-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="99871-112">**注意：**此信息仅适用于使用基于维度的配置技术的基础产品。</span><span class="sxs-lookup"><span data-stu-id="99871-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="99871-113">现有配置为不受配置规则后续更改的影响。</span><span class="sxs-lookup"><span data-stu-id="99871-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="99871-114">但是，在您定义新配置之前，且如果您认为规则在检查时已更改，设置规则十分重要。</span><span class="sxs-lookup"><span data-stu-id="99871-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="99871-115">**注意：**对于**选择**方法，将自动选择派生的配置组、物料编号和配置。</span><span class="sxs-lookup"><span data-stu-id="99871-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="99871-116">对于**取消选择**方法，将不能选择派生的配置组、物料编号和配置。</span><span class="sxs-lookup"><span data-stu-id="99871-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="99871-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="99871-117">See also</span></span>
--------

[<span data-ttu-id="99871-118">基于维度的产品配置</span><span class="sxs-lookup"><span data-stu-id="99871-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




