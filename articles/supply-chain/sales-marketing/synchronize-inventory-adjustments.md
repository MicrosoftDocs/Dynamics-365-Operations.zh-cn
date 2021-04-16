---
title: 将库存转移和调整从 Field Service 同步到 Supply Chain Management
description: 本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存调整和转移同步到 Dynamics 365 Field Service 的模板和基础任务。
author: ChristianRytt
ms.date: 04/30/2019
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
ms.openlocfilehash: 9f3bfe950446a6e87e34c32d2593cba0af84d8e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838973"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="43a92-103">将库存转移和调整从 Field Service 同步到 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43a92-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="43a92-104">本主题讨论用于将 Dynamics 365 Supply Chain Management 中的库存调整和转移同步到 Dynamics 365 Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="43a92-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="43a92-105">[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="43a92-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="43a92-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="43a92-106">Templates and tasks</span></span>
<span data-ttu-id="43a92-107">以下模板和基础任务用于将库存调整和转移从 Field Service 同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="43a92-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="43a92-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="43a92-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="43a92-109">库调转移（Field Service 到 Supply Chain Management）</span><span class="sxs-lookup"><span data-stu-id="43a92-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="43a92-110">库调转移（Field Service 到 Supply Chain Management）</span><span class="sxs-lookup"><span data-stu-id="43a92-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="43a92-111">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="43a92-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="43a92-112">库存调整</span><span class="sxs-lookup"><span data-stu-id="43a92-112">Inventory Adjustments</span></span>
- <span data-ttu-id="43a92-113">库存转移</span><span class="sxs-lookup"><span data-stu-id="43a92-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="43a92-114">表集</span><span class="sxs-lookup"><span data-stu-id="43a92-114">Table set</span></span>
| <span data-ttu-id="43a92-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="43a92-115">Field Service</span></span>                     | <span data-ttu-id="43a92-116">供应链管理</span><span class="sxs-lookup"><span data-stu-id="43a92-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="43a92-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="43a92-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="43a92-118">Dataverse 库存调整日记帐标头和行</span><span class="sxs-lookup"><span data-stu-id="43a92-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="43a92-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="43a92-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="43a92-120">Dataverse 库存转移日记帐标头和行</span><span class="sxs-lookup"><span data-stu-id="43a92-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="43a92-121">表流</span><span class="sxs-lookup"><span data-stu-id="43a92-121">Table flow</span></span>
<span data-ttu-id="43a92-122">Field Service 中进行的库存调整和转移将在 **过帐状态** 从 **已创建** 更改为 **已过帐** 后同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="43a92-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="43a92-123">在发生此情况时，调整或转移单将锁定并变为只读。</span><span class="sxs-lookup"><span data-stu-id="43a92-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="43a92-124">这意味着调整和转移可以在 Supply Chain Management 中过帐，但是无法进行修改。</span><span class="sxs-lookup"><span data-stu-id="43a92-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="43a92-125">在 Supply Chain Management 中，您可以将批处理作业设置为自动过帐在集成期间生成的调整和转移库存日记帐。</span><span class="sxs-lookup"><span data-stu-id="43a92-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="43a92-126">请参阅以下先决条件了解有关如何启用批处理作业的详细信息。</span><span class="sxs-lookup"><span data-stu-id="43a92-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="43a92-127">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="43a92-127">Field Service CRM solution</span></span> 
<span data-ttu-id="43a92-128">**库存单位** 列已添加到 **产品** 表。</span><span class="sxs-lookup"><span data-stu-id="43a92-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="43a92-129">需要此列是因为销售和库存单位在 Supply Chain Management 中不是始终相同，对于 Supply Chain Management 中的仓库库存，需要库存单位。</span><span class="sxs-lookup"><span data-stu-id="43a92-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="43a92-130">当您在库存调整产品中同时为库存调整和库存转移设置产品时，将从产品库存产品值提取单位。</span><span class="sxs-lookup"><span data-stu-id="43a92-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="43a92-131">如果找到值，**单位** 列将在库存调整产品中被锁定。</span><span class="sxs-lookup"><span data-stu-id="43a92-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="43a92-132">**过帐状态** 列已同时添加到 **库存调整** 表和 **库存转移** 表。</span><span class="sxs-lookup"><span data-stu-id="43a92-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="43a92-133">在调整或转移被发送到 Supply Chain Management 时，此列用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="43a92-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="43a92-134">此列的默认值为“已创建 (1)”，但是它不发送到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="43a92-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="43a92-135">在将值更新为“已过帐 (2)”后，它将被发送到 Supply Chain Management，但之后您不再能够更改调整或转移或添加新行。</span><span class="sxs-lookup"><span data-stu-id="43a92-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="43a92-136">**编号规则** 列已添加到 **库存调整产品** 表。</span><span class="sxs-lookup"><span data-stu-id="43a92-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="43a92-137">此列确保集成具有唯一编号，以使集成能够创建和更新调整。</span><span class="sxs-lookup"><span data-stu-id="43a92-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="43a92-138">在创建第一个库存调整产品时，将在 **P2C AutoNumber** 表中创建新记录以保持所使用的编号系列和前缀。</span><span class="sxs-lookup"><span data-stu-id="43a92-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="43a92-139">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="43a92-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="43a92-140">供应链管理</span><span class="sxs-lookup"><span data-stu-id="43a92-140">Supply Chain Management</span></span>
<span data-ttu-id="43a92-141">集成生成的集成库存日记帐可以使用批处理作业自动过帐。</span><span class="sxs-lookup"><span data-stu-id="43a92-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="43a92-142">这从 **库存管理 > 定期任务 > Dataverse 集成 > 过帐集成库存日记帐** 启用。</span><span class="sxs-lookup"><span data-stu-id="43a92-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="43a92-143">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="43a92-143">Template mapping in Data integration</span></span>

<span data-ttu-id="43a92-144">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="43a92-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="43a92-145">库存调整（Field Service 到 Supply Chain Management）：库存调整</span><span class="sxs-lookup"><span data-stu-id="43a92-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="43a92-146">[![数据集成中的模板映射](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="43a92-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="43a92-147">库存转移（Field Service 到 Supply Chain Management）：库存转移</span><span class="sxs-lookup"><span data-stu-id="43a92-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="43a92-148">[![数据集成中的模板映射](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="43a92-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]