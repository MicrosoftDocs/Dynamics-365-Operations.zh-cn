---
title: 将库存级别信息从 Finance and Operations 同步到 Field Service
description: 本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存水平信息同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535690"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e031a-103">将库存级别信息从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="e031a-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e031a-104">本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存水平信息同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="e031a-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e031a-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e031a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e031a-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="e031a-106">Templates and tasks</span></span>
<span data-ttu-id="e031a-107">以下模板和基础任务用于同步 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的库存现有水平。</span><span class="sxs-lookup"><span data-stu-id="e031a-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e031a-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="e031a-108">**Template in Data integration**</span></span>
- <span data-ttu-id="e031a-109">产品库存（Fin and Ops 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="e031a-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="e031a-110">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="e031a-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="e031a-111">产品库存</span><span class="sxs-lookup"><span data-stu-id="e031a-111">Product inventory</span></span>

<span data-ttu-id="e031a-112">在发生库存水平同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="e031a-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e031a-113">仓库（Fin and Ops 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="e031a-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="e031a-114">具有库存单位的 Field Service 产品（Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="e031a-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e031a-115">实体集</span><span class="sxs-lookup"><span data-stu-id="e031a-115">Entity set</span></span>

| <span data-ttu-id="e031a-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e031a-116">Field Service</span></span>                      | <span data-ttu-id="e031a-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e031a-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e031a-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e031a-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e031a-119">CDS 现有库存(按仓库分类)</span><span class="sxs-lookup"><span data-stu-id="e031a-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e031a-120">实体流</span><span class="sxs-lookup"><span data-stu-id="e031a-120">Entity flow</span></span>
<span data-ttu-id="e031a-121">将所选产品的库存水平信息从 Finance and Operations 发送到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="e031a-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="e031a-122">库存水平信息包括：</span><span class="sxs-lookup"><span data-stu-id="e031a-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="e031a-123">现有数量（仓库中当前实际记录的数量）</span><span class="sxs-lookup"><span data-stu-id="e031a-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="e031a-124">在订单数量上（订单上的总记录数量，如销售订单）</span><span class="sxs-lookup"><span data-stu-id="e031a-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="e031a-125">订购数量（总记录订购数量，如采购订单）</span><span class="sxs-lookup"><span data-stu-id="e031a-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="e031a-126">当库存水平更改时，此信息为每个仓库的每个已发放产品捕获，并基于更改跟踪同步。</span><span class="sxs-lookup"><span data-stu-id="e031a-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e031a-127">在 Field Service 中，集成解决方案为增量创建库存日记帐，以使 Field Service 中的水平与 Finance and Operations 中的水平匹配。</span><span class="sxs-lookup"><span data-stu-id="e031a-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="e031a-128">Finance and Operations 将充当库存水平的主水平。</span><span class="sxs-lookup"><span data-stu-id="e031a-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="e031a-129">因此，如果在 Field Service 中使用此功能，以及从 Finance and Operations 同步库存水平，为 Field Service 到 Finance and Operations 的工作订单、转移和调整设置集成非常重要。</span><span class="sxs-lookup"><span data-stu-id="e031a-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="e031a-130">从 Finance and Operations 掌握库存水平的产品和仓库可以通过“高级查询和筛选 (Power Query)”进行控制。</span><span class="sxs-lookup"><span data-stu-id="e031a-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="e031a-131">可以在 Field Services（**外部维护 = 否**）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Finance and Operations 中的单个仓库。</span><span class="sxs-lookup"><span data-stu-id="e031a-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e031a-132">这用于您希望 Field service 掌握详细的库存水平并仅向 Finance and Operations 发送更新的情况。</span><span class="sxs-lookup"><span data-stu-id="e031a-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="e031a-133">在这种情况下，Field Service 不会收到来自 Finance and Operations 的库存水平更新。</span><span class="sxs-lookup"><span data-stu-id="e031a-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="e031a-134">更多信息，请参阅[将库存调整从 Field Service 同步到 Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) 和[将 Field Service 的工作订单同步到链接到 Finance and Operations 中的项目的销售订单](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。</span><span class="sxs-lookup"><span data-stu-id="e031a-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e031a-135">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="e031a-135">Field Service CRM solution</span></span>
<span data-ttu-id="e031a-136">**外部产品库存**实体仅用于集成中的后端。</span><span class="sxs-lookup"><span data-stu-id="e031a-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="e031a-137">此实体从集成中的 Finance and Operations 接收库存水平值，然后将这些值转换为手动库存日记帐，其随后将更改仓库中的库存产品。</span><span class="sxs-lookup"><span data-stu-id="e031a-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e031a-138">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="e031a-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="e031a-139">数据集成</span><span class="sxs-lookup"><span data-stu-id="e031a-139">Data integration</span></span>
<span data-ttu-id="e031a-140">要让该项目工作，需要确保更新 msdynce_externalproductinventories 的集成密钥。</span><span class="sxs-lookup"><span data-stu-id="e031a-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="e031a-141">转到**数据集成 > 连接集**。</span><span class="sxs-lookup"><span data-stu-id="e031a-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="e031a-142">选择使用的连接集。</span><span class="sxs-lookup"><span data-stu-id="e031a-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="e031a-143">在**集成密钥**选项卡中，确保向 msdynce_externalproductinventories 添加以下密钥：</span><span class="sxs-lookup"><span data-stu-id="e031a-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="e031a-144">msdynce_productnumber（产品编号）</span><span class="sxs-lookup"><span data-stu-id="e031a-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="e031a-145">msdynce_warehouseid（仓库 ID）</span><span class="sxs-lookup"><span data-stu-id="e031a-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="e031a-146">数据集成项目</span><span class="sxs-lookup"><span data-stu-id="e031a-146">Data integration project</span></span>
<span data-ttu-id="e031a-147">您可以应用“高级查询和筛选”的筛选器，以仅让某些产品和仓库将库存水平信息从 Finance and Operations 发送到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="e031a-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e031a-148">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="e031a-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="e031a-149">产品库存（Fin and Ops 到 Field Service）：产品库存</span><span class="sxs-lookup"><span data-stu-id="e031a-149">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="e031a-150">[![数据集成中的模板映射](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e031a-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
