---
title: 集成的站点和仓库
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的站点和仓库数据集成。
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679312"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="417f9-103">集成的站点和仓库</span><span class="sxs-lookup"><span data-stu-id="417f9-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="417f9-104">本主题介绍 Finance and Operations 与 Dataverse 之间的站点和仓库数据集成。</span><span class="sxs-lookup"><span data-stu-id="417f9-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="417f9-105">运营站点和仓库是 Supply Chain Management 应用程序中的常见概念。</span><span class="sxs-lookup"><span data-stu-id="417f9-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="417f9-106">用于为公司的供应链建模。</span><span class="sxs-lookup"><span data-stu-id="417f9-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="417f9-107">模板</span><span class="sxs-lookup"><span data-stu-id="417f9-107">Templates</span></span>

<span data-ttu-id="417f9-108">通过与 Dataverse 集成，Dataverse 中使用下表中的站点和仓库数据表提供这些概念及其所有相关信息。</span><span class="sxs-lookup"><span data-stu-id="417f9-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="417f9-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="417f9-109">Finance and Operations apps</span></span> | <span data-ttu-id="417f9-110">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="417f9-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="417f9-111">说明</span><span class="sxs-lookup"><span data-stu-id="417f9-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="417f9-112">站点</span><span class="sxs-lookup"><span data-stu-id="417f9-112">Sites</span></span> | <span data-ttu-id="417f9-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="417f9-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="417f9-114">仓库</span><span class="sxs-lookup"><span data-stu-id="417f9-114">Warehouses</span></span> | <span data-ttu-id="417f9-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="417f9-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

