---
title: "将库存级别信息从 Finance and Operations 同步到 Field Service"
description: "本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存水平信息同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: zh-cn
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c73c7-103">将库存级别信息从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="c73c7-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c73c7-104">本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存水平信息同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="c73c7-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c73c7-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="c73c7-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c73c7-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="c73c7-106">Templates and tasks</span></span>
<span data-ttu-id="c73c7-107">以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的库存现有水平的同步。</span><span class="sxs-lookup"><span data-stu-id="c73c7-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c73c7-108">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="c73c7-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="c73c7-109">产品库存（Finance and Operations 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="c73c7-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="c73c7-110">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="c73c7-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="c73c7-111">产品库存</span><span class="sxs-lookup"><span data-stu-id="c73c7-111">Product inventory</span></span>

<span data-ttu-id="c73c7-112">在发生库存水平同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="c73c7-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="c73c7-113">仓库（Finance and Operations 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="c73c7-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="c73c7-114">具有库存单位的 Field Service 产品（Finance and Operations 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="c73c7-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c73c7-115">实体集</span><span class="sxs-lookup"><span data-stu-id="c73c7-115">Entity set</span></span>

| <span data-ttu-id="c73c7-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="c73c7-116">Field Service</span></span>                      | <span data-ttu-id="c73c7-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c73c7-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="c73c7-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="c73c7-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="c73c7-119">CDS 现有库存(按仓库分类)</span><span class="sxs-lookup"><span data-stu-id="c73c7-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="c73c7-120">实体流</span><span class="sxs-lookup"><span data-stu-id="c73c7-120">Entity flow</span></span>
<span data-ttu-id="c73c7-121">将所选产品的库存水平信息从 Finance and Operations 发送到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="c73c7-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="c73c7-122">库存水平信息包括：</span><span class="sxs-lookup"><span data-stu-id="c73c7-122">The inventory level information include:</span></span> 
- <span data-ttu-id="c73c7-123">现有数量（仓库中当前实际记录的数量）</span><span class="sxs-lookup"><span data-stu-id="c73c7-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="c73c7-124">在订单数量上（订单上的总记录数量 - 即销售订单）</span><span class="sxs-lookup"><span data-stu-id="c73c7-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="c73c7-125">订购数量（总记录订购数量 - 即采购订单）</span><span class="sxs-lookup"><span data-stu-id="c73c7-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="c73c7-126">当库存水平更改时，此信息为每个仓库的每个已发放产品捕获，并基于更改跟踪同步。</span><span class="sxs-lookup"><span data-stu-id="c73c7-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="c73c7-127">在 Field Service 中，集成解决方案为增量创建库存日记帐，以获得 Field Service 中与 Finance and Operations 中的级别匹配的级别。</span><span class="sxs-lookup"><span data-stu-id="c73c7-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="c73c7-128">Finance and Operations 将充当库存水平的主水平。</span><span class="sxs-lookup"><span data-stu-id="c73c7-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="c73c7-129">因此，如果在 Field Service 中使用此功能，以及从 Finance and Operations 同步库存水平，为 Field Service 到 Finance and Operations 的工作订单、转移和调整设置集成非常重要。</span><span class="sxs-lookup"><span data-stu-id="c73c7-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="c73c7-130">从 Finance and Operations 掌握库存水平的产品和仓库可以通过“高级查询和筛选 (Power Query)”进行控制。</span><span class="sxs-lookup"><span data-stu-id="c73c7-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="c73c7-131">注意：可以在 Field Services（外部维护 = 否）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Finance and Operations 中的单个仓库。</span><span class="sxs-lookup"><span data-stu-id="c73c7-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="c73c7-132">这用于您希望 Field service 掌握详细的库存水平并向 Finance and Operations 发送更新的情况。</span><span class="sxs-lookup"><span data-stu-id="c73c7-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="c73c7-133">在这种情况下，Field service 不会收到来自 Finance and Operations 的库存水平更新。</span><span class="sxs-lookup"><span data-stu-id="c73c7-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="c73c7-134">请参阅“将库存调整从 Field Service 同步到 Finance and Operations”和“将 Field Service 的工作订单同步到链接到 Finance and Operations 中的项目的销售订单”中的更多信息。</span><span class="sxs-lookup"><span data-stu-id="c73c7-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c73c7-135">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="c73c7-135">Field Service CRM solution</span></span>
<span data-ttu-id="c73c7-136">“外部产品库存”实体是仅用于集成中的后端的新实体。</span><span class="sxs-lookup"><span data-stu-id="c73c7-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="c73c7-137">它从集成中的 Finance and Operations 接收库存水平值，然后将这些值转换为手动库存日记帐，其随后将更改仓库中的库存产品。</span><span class="sxs-lookup"><span data-stu-id="c73c7-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c73c7-138">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="c73c7-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="c73c7-139">在数据集成项目中</span><span class="sxs-lookup"><span data-stu-id="c73c7-139">In the Data Integration project</span></span>
<span data-ttu-id="c73c7-140">应用“高级查询和筛选”的筛选器控制仅所需产品和仓库将库存水平信息从 Finance and Operations 发送到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="c73c7-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c73c7-141">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="c73c7-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="c73c7-142">产品库存（Finance and Operations 到 Field Service）：产品库存</span><span class="sxs-lookup"><span data-stu-id="c73c7-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="c73c7-143">[![数据集成中的模板映射](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="c73c7-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

