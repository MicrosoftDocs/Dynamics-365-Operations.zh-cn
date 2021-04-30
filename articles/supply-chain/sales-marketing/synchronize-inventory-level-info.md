---
title: 将库存级别信息从 Supply Chain Management 同步到 Field Service
description: 本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存水平信息同步到 Dynamics 365 Field Service 的模板和基础任务。
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910267"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="2ccf4-103">将库存级别信息从 Supply Chain Management 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="2ccf4-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2ccf4-104">本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存水平信息同步到 Dynamics 365 Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="2ccf4-105">[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="2ccf4-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2ccf4-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="2ccf4-106">Templates and tasks</span></span>
<span data-ttu-id="2ccf4-107">以下模板和基础任务用于将库存现有水平从 Supply Chain Management 同步到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="2ccf4-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="2ccf4-108">**Template in Data integration**</span></span>
- <span data-ttu-id="2ccf4-109">产品库存（Supply Chain Management 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="2ccf4-110">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="2ccf4-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="2ccf4-111">产品库存</span><span class="sxs-lookup"><span data-stu-id="2ccf4-111">Product inventory</span></span>

<span data-ttu-id="2ccf4-112">在发生库存水平同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="2ccf4-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="2ccf4-113">仓库（Supply Chain Management 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="2ccf4-114">具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="2ccf4-115">实体集</span><span class="sxs-lookup"><span data-stu-id="2ccf4-115">Entity set</span></span>

| <span data-ttu-id="2ccf4-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="2ccf4-116">Field Service</span></span>                      | <span data-ttu-id="2ccf4-117">供应链管理</span><span class="sxs-lookup"><span data-stu-id="2ccf4-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="2ccf4-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="2ccf4-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="2ccf4-119">Dataverse 现有库存量（按仓库）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="2ccf4-120">实体流</span><span class="sxs-lookup"><span data-stu-id="2ccf4-120">Entity flow</span></span>
<span data-ttu-id="2ccf4-121">将所选产品的库存水平信息从 Finance and Operations 发送到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="2ccf4-122">库存水平信息包括：</span><span class="sxs-lookup"><span data-stu-id="2ccf4-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="2ccf4-123">现有数量（仓库中当前实际记录的数量）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="2ccf4-124">在订单数量上（订单上的总记录数量，如销售订单）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="2ccf4-125">订购数量（总记录订购数量，如采购订单）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="2ccf4-126">当库存水平更改时，此信息为每个仓库的每个已发放产品捕获，并基于更改跟踪同步。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="2ccf4-127">在 Field Service 中，集成解决方案为增量创建库存日记帐，以使 Field Service 中的水平与 Supply Chain Management 中的水平匹配。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="2ccf4-128">Supply Chain Management 将充当库存水平的主水平。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="2ccf4-129">因此，如果在 Field Service 中使用此功能，以及从 Supply Chain Management 同步库存水平，为 Field Service 到 Supply Chain Management 的工作订单、转移和调整设置集成非常重要。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="2ccf4-130">从 Supply Chain Management 掌握库存水平的产品和仓库可以通过“高级查询和筛选 (Power Query)”进行控制。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="2ccf4-131">可以在 Field Services（**外部维护 = 否**）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Supply Chain Management 中的单个仓库。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="2ccf4-132">这用于您希望 Field service 掌握详细的库存水平并仅向 Supply Chain Management 发送更新的情况。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="2ccf4-133">在这种情况下，Field Service 不会收到来自 Supply Chain Management 的库存水平更新。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="2ccf4-134">更多信息，请参阅[将库存调整从 Field Service 同步到 Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) 和[将 Field Service 的工作订单同步到链接到 Supply Chain Management 中的项目的销售订单](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="2ccf4-135">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="2ccf4-135">Field Service CRM solution</span></span>
<span data-ttu-id="2ccf4-136">**外部产品库存** 实体仅用于集成中的后端。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="2ccf4-137">此实体从集成中的 Supply Chain Management 接收库存水平值，然后将这些值转换为手动库存日记帐，其随后将更改仓库中的库存产品。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="2ccf4-138">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="2ccf4-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="2ccf4-139">数据集成</span><span class="sxs-lookup"><span data-stu-id="2ccf4-139">Data integration</span></span>
<span data-ttu-id="2ccf4-140">要让该项目工作，需要确保更新 msdynce_externalproductinventories 的集成密钥。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="2ccf4-141">转到 **数据集成 > 连接集**。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="2ccf4-142">选择使用的连接集。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="2ccf4-143">在 **集成密钥** 选项卡中，确保向 msdynce_externalproductinventories 添加以下密钥：</span><span class="sxs-lookup"><span data-stu-id="2ccf4-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="2ccf4-144">msdynce_productnumber（产品编号）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="2ccf4-145">msdynce_warehouseid（仓库 ID）</span><span class="sxs-lookup"><span data-stu-id="2ccf4-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="2ccf4-146">数据集成项目</span><span class="sxs-lookup"><span data-stu-id="2ccf4-146">Data integration project</span></span>
<span data-ttu-id="2ccf4-147">您可以应用“高级查询和筛选”的筛选器，以仅让某些产品和仓库将库存水平信息从 Supply Chain Management 发送到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="2ccf4-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2ccf4-148">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="2ccf4-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="2ccf4-149">产品库存（Supply Chain Management 到 Field Service）：产品库存</span><span class="sxs-lookup"><span data-stu-id="2ccf4-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="2ccf4-150">[![数据集成中的模板映射](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="2ccf4-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]