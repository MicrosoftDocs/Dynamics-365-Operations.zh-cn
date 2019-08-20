---
title: 将库存转移和调整从 Field Service 同步到 Finance and Operations
description: 本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存调整和转移同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835710"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="27064-103">将库存调整从 Field Service 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27064-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27064-104">本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存调整和转移同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="27064-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="27064-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="27064-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="27064-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="27064-106">Templates and tasks</span></span>
<span data-ttu-id="27064-107">以下模板和基础任务用于同步 Microsoft Dynamics 365 for Field Service 到 Microsoft Dynamics 365 for Finance and Operations 的库存调整和转移。</span><span class="sxs-lookup"><span data-stu-id="27064-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="27064-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="27064-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="27064-109">库存调整（Field Service 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="27064-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="27064-110">库存转移（Field Service 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="27064-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="27064-111">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="27064-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="27064-112">库存调整</span><span class="sxs-lookup"><span data-stu-id="27064-112">Inventory Adjustments</span></span>
- <span data-ttu-id="27064-113">库存转移</span><span class="sxs-lookup"><span data-stu-id="27064-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="27064-114">实体集</span><span class="sxs-lookup"><span data-stu-id="27064-114">Entity set</span></span>
| <span data-ttu-id="27064-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="27064-115">Field Service</span></span>                     | <span data-ttu-id="27064-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27064-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="27064-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="27064-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="27064-118">CDS 库存调整日记帐标头和行</span><span class="sxs-lookup"><span data-stu-id="27064-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="27064-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="27064-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="27064-120">CDS 库存转移日记帐标头和行</span><span class="sxs-lookup"><span data-stu-id="27064-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="27064-121">实体流</span><span class="sxs-lookup"><span data-stu-id="27064-121">Entity flow</span></span>
<span data-ttu-id="27064-122">Field Service 中进行的库存调整和转移将在**过帐状态**从**已创建**更改为**已过帐**后同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="27064-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="27064-123">在发生此情况时，调整或转移单将锁定并变为只读。</span><span class="sxs-lookup"><span data-stu-id="27064-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="27064-124">这意味着调整和转移可以在 Finance and Operations 中过帐，但是无法进行修改。</span><span class="sxs-lookup"><span data-stu-id="27064-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="27064-125">在 Finance and Operations 中，您可以将批处理作业设置为自动过帐在集成期间生成的调整和转移库存日记帐。</span><span class="sxs-lookup"><span data-stu-id="27064-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="27064-126">请参阅以下先决条件了解有关如何启用批处理作业的详细信息。</span><span class="sxs-lookup"><span data-stu-id="27064-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="27064-127">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="27064-127">Field Service CRM solution</span></span> 
<span data-ttu-id="27064-128">**库存单位**字段已添加到**产品**实体。</span><span class="sxs-lookup"><span data-stu-id="27064-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="27064-129">需要此字段是因为销售和库存单位在 Finance and Operations 中不是始终相同，对于 Finance and Operations 中的仓库库存，需要库存单位。</span><span class="sxs-lookup"><span data-stu-id="27064-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="27064-130">当您在库存调整产品中同时为库存调整和库存转移设置产品时，将从产品库存产品值提取单位。</span><span class="sxs-lookup"><span data-stu-id="27064-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="27064-131">如果找到值，**单位**字段将在库存调整产品中被锁定</span><span class="sxs-lookup"><span data-stu-id="27064-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="27064-132">**过帐状态**字段已同时添加到**库存调整**实体和**库存转移**实体。</span><span class="sxs-lookup"><span data-stu-id="27064-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="27064-133">在调整或转移被发送到 Finance and Operations 时，此字段用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="27064-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="27064-134">此字段的默认值为“已创建 (1)”，但是它不发送到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="27064-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="27064-135">在将值更新为“已过帐 (2)”后，它将被发送到 Finance and Operations，但之后您不再能够更改调整或转移或添加新行。</span><span class="sxs-lookup"><span data-stu-id="27064-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="27064-136">**编号规则**字段已添加到**库存调整产品**实体。</span><span class="sxs-lookup"><span data-stu-id="27064-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="27064-137">此字段确保集成具有唯一编号，以使集成能够创建和更新调整。</span><span class="sxs-lookup"><span data-stu-id="27064-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="27064-138">在创建第一个库存调整产品时，将在**P2C 自动编号**实体中创建新记录以保持所使用的编号系列和前缀。</span><span class="sxs-lookup"><span data-stu-id="27064-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="27064-139">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="27064-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="27064-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27064-140">Finance and Operations</span></span>
<span data-ttu-id="27064-141">集成生成的集成库存日记帐可以使用批处理作业自动过帐。</span><span class="sxs-lookup"><span data-stu-id="27064-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="27064-142">这从**库存管理 > 定期任务 > CDS 集成 > 过帐集成库存日记帐**启用</span><span class="sxs-lookup"><span data-stu-id="27064-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="27064-143">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="27064-143">Template mapping in Data integration</span></span>

<span data-ttu-id="27064-144">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="27064-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="27064-145">库存调整（Field Service 到 Fin and Ops）：库存调整</span><span class="sxs-lookup"><span data-stu-id="27064-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="27064-146">[![数据集成中的模板映射](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="27064-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="27064-147">库存转移（Field Service 到 Fin and Ops）：库存转移</span><span class="sxs-lookup"><span data-stu-id="27064-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="27064-148">[![数据集成中的模板映射](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="27064-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
