---
title: 功能位置和资产
description: 本主题介绍资产管理中的功能位置和资产。 资产管理是 Dynamics 365 Supply Chain Management 中的一个高级模块，用于管理资产和维护作业。
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e626daa89eecf838d7cda0663d00c1c2dbecb76
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816741"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="5091c-104">功能位置和资产</span><span class="sxs-lookup"><span data-stu-id="5091c-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5091c-105">本主题介绍资产管理中的功能位置和资产。</span><span class="sxs-lookup"><span data-stu-id="5091c-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="5091c-106">资产管理是 Dynamics 365 Supply Chain Management 中的一个高级模块，用于管理资产和维护作业。</span><span class="sxs-lookup"><span data-stu-id="5091c-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="5091c-107">概览</span><span class="sxs-lookup"><span data-stu-id="5091c-107">Overview</span></span>

<span data-ttu-id="5091c-108">资产管理与其他 Finance and Operations 应用的多个模块无缝集成。</span><span class="sxs-lookup"><span data-stu-id="5091c-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="5091c-109">下图显示界面和其他模块。</span><span class="sxs-lookup"><span data-stu-id="5091c-109">The following illustration shows the interfaces with other modules.</span></span>

![显示资产管理如何与其他模块交互的图](media/01-overview-image.png)

<span data-ttu-id="5091c-111">资产管理可用于高效管理和执行与管理和服务公司中大量类型的设备有关的所有任务。</span><span class="sxs-lookup"><span data-stu-id="5091c-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="5091c-112">这些设备包括机器、生产设备和交通工具。</span><span class="sxs-lookup"><span data-stu-id="5091c-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="5091c-113">资产管理还支持多个行业的解决方案。</span><span class="sxs-lookup"><span data-stu-id="5091c-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="5091c-114">下图显示资产管理中包含的主要功能的概览。</span><span class="sxs-lookup"><span data-stu-id="5091c-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![显示资产管理中的主要功能的图](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="5091c-116">功能位置和资产</span><span class="sxs-lookup"><span data-stu-id="5091c-116">Functional locations and assets</span></span>

<span data-ttu-id="5091c-117">功能位置用于管理位置中的资产。</span><span class="sxs-lookup"><span data-stu-id="5091c-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="5091c-118">此类管理包括跟踪功能位置的资产成本。</span><span class="sxs-lookup"><span data-stu-id="5091c-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="5091c-119">功能位置采用分层结构，而位置则可以具有子位置。</span><span class="sxs-lookup"><span data-stu-id="5091c-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="5091c-120">功能位置的结构为静态结构。</span><span class="sxs-lookup"><span data-stu-id="5091c-120">The structure of functional locations is static.</span></span> <span data-ttu-id="5091c-121">换句话说，位置不能更改地点。</span><span class="sxs-lookup"><span data-stu-id="5091c-121">In other words, locations can't change place.</span></span> <span data-ttu-id="5091c-122">资产可以安装到功能位置上，也可以在以后根据需要安装到其他功能位置上。</span><span class="sxs-lookup"><span data-stu-id="5091c-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="5091c-123">资产成本始终采用资产的位置。</span><span class="sxs-lookup"><span data-stu-id="5091c-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="5091c-124">换句话说，如果将资产安装到新的功能位置，该资产将自动使用与新功能位置关联的财务维度。</span><span class="sxs-lookup"><span data-stu-id="5091c-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="5091c-125">因此，资产成本始终与当前安装资产的功能位置关联。</span><span class="sxs-lookup"><span data-stu-id="5091c-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="5091c-126">在公司对功能位置执行项目控制和报告时，对财务维度的此项自动处理有助于确保完全跟踪成本。</span><span class="sxs-lookup"><span data-stu-id="5091c-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="5091c-127">功能位置层次结构的创建方法取决于公司对维护内部设备或服务客户设备的要求。</span><span class="sxs-lookup"><span data-stu-id="5091c-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="5091c-128">下图显示基于地理位置的功能位置的示例。</span><span class="sxs-lookup"><span data-stu-id="5091c-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![显示基于地理位置的功能位置的图](media/03-overview-image.png)

<span data-ttu-id="5091c-130">下图显示基于客户的功能位置的示例。</span><span class="sxs-lookup"><span data-stu-id="5091c-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![显示基于客户的功能位置的图](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]