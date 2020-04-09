---
title: 集成的站点和仓库
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的站点和仓库数据集成。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173054"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="62116-103">集成的站点和仓库</span><span class="sxs-lookup"><span data-stu-id="62116-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="62116-104">本主题介绍 Finance and Operations 与 Common Data Service 之间的站点和仓库数据集成。</span><span class="sxs-lookup"><span data-stu-id="62116-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="62116-105">运营站点和仓库是 Supply Chain Management 应用程序中的常见概念。</span><span class="sxs-lookup"><span data-stu-id="62116-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="62116-106">用于为公司的供应链建模。</span><span class="sxs-lookup"><span data-stu-id="62116-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="62116-107">模板</span><span class="sxs-lookup"><span data-stu-id="62116-107">Templates</span></span>

<span data-ttu-id="62116-108">通过与 Common Data Service 集成，Common Data Service 中使用下表中的站点和仓库数据提供这些概念及其所有相关信息。</span><span class="sxs-lookup"><span data-stu-id="62116-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="62116-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="62116-109">Finance and Operations apps</span></span> | <span data-ttu-id="62116-110">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="62116-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="62116-111">说明</span><span class="sxs-lookup"><span data-stu-id="62116-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="62116-112">站点</span><span class="sxs-lookup"><span data-stu-id="62116-112">Sites</span></span> | <span data-ttu-id="62116-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="62116-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="62116-114">仓库</span><span class="sxs-lookup"><span data-stu-id="62116-114">Warehouses</span></span> | <span data-ttu-id="62116-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="62116-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

