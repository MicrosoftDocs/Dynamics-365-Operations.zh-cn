---
title: 集成的站点和仓库
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的站点和仓库数据集成。
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750658"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="1549a-103">集成的站点和仓库</span><span class="sxs-lookup"><span data-stu-id="1549a-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1549a-104">本主题介绍 Finance and Operations 与 Dataverse 之间的站点和仓库数据集成。</span><span class="sxs-lookup"><span data-stu-id="1549a-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="1549a-105">运营站点和仓库是 Supply Chain Management 应用程序中的常见概念。</span><span class="sxs-lookup"><span data-stu-id="1549a-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="1549a-106">用于为公司的供应链建模。</span><span class="sxs-lookup"><span data-stu-id="1549a-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="1549a-107">模板</span><span class="sxs-lookup"><span data-stu-id="1549a-107">Templates</span></span>

<span data-ttu-id="1549a-108">通过与 Dataverse 集成，Dataverse 中使用下表中的站点和仓库数据表提供这些概念及其所有相关信息。</span><span class="sxs-lookup"><span data-stu-id="1549a-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="1549a-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="1549a-109">Finance and Operations apps</span></span> | <span data-ttu-id="1549a-110">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="1549a-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="1549a-111">说明</span><span class="sxs-lookup"><span data-stu-id="1549a-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="1549a-112">站点</span><span class="sxs-lookup"><span data-stu-id="1549a-112">Sites</span></span> | <span data-ttu-id="1549a-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="1549a-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="1549a-114">仓库</span><span class="sxs-lookup"><span data-stu-id="1549a-114">Warehouses</span></span> | <span data-ttu-id="1549a-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="1549a-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]