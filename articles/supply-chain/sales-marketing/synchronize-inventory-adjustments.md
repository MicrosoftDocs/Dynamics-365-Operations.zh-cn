---
title: "将库存转移和调整从 Field Service 同步到 Finance and Operations"
description: "本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存调整和转移同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。"
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: zh-cn
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="08da5-103">将库存调整从 Field Service 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08da5-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="08da5-104">本主题讨论用于将 Microsoft Dynamics 365 for Finance and Operations 中的库存调整和转移同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="08da5-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="08da5-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="08da5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="08da5-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="08da5-106">Templates and tasks</span></span>
<span data-ttu-id="08da5-107">以下模板和基础任务用于运行 Microsoft Dynamics 365 for Field Service 到 Microsoft Dynamics 365 for Finance and Operations 的库存调整和转移的同步。</span><span class="sxs-lookup"><span data-stu-id="08da5-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="08da5-108">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="08da5-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="08da5-109">库存调整（Field Service 到 Finance and Operations）</span><span class="sxs-lookup"><span data-stu-id="08da5-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="08da5-110">库存转移（Field Service 到 Finance and Operations）</span><span class="sxs-lookup"><span data-stu-id="08da5-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="08da5-111">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="08da5-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="08da5-112">库存调整</span><span class="sxs-lookup"><span data-stu-id="08da5-112">Inventory Adjustments</span></span>
- <span data-ttu-id="08da5-113">库存转移</span><span class="sxs-lookup"><span data-stu-id="08da5-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="08da5-114">实体集</span><span class="sxs-lookup"><span data-stu-id="08da5-114">Entity set</span></span>
| <span data-ttu-id="08da5-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="08da5-115">Field Service</span></span>                     | <span data-ttu-id="08da5-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08da5-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="08da5-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="08da5-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="08da5-118">CDS 库存调整日记帐标头和行</span><span class="sxs-lookup"><span data-stu-id="08da5-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="08da5-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="08da5-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="08da5-120">CDS 库存转移日记帐标头和行</span><span class="sxs-lookup"><span data-stu-id="08da5-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="08da5-121">实体流</span><span class="sxs-lookup"><span data-stu-id="08da5-121">Entity flow</span></span>
<span data-ttu-id="08da5-122">Field Service 中进行的库存调整和转移将在**过帐状态**从“已创建”更改为“已过帐”后同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="08da5-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="08da5-123">在发生此情况时，调整或转移单将被锁定并变为只读，因为调整和转移可能在 Finance and Operations 中过帐，因此无法修改。</span><span class="sxs-lookup"><span data-stu-id="08da5-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="08da5-124">在 Finance and Operations 中，您可以将批处理作业设置为自动过帐通过集成生成的调整和转移库存日记帐。</span><span class="sxs-lookup"><span data-stu-id="08da5-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="08da5-125">请参阅以下先决条件了解有关如何启用批处理作业的详细信息。</span><span class="sxs-lookup"><span data-stu-id="08da5-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="08da5-126">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="08da5-126">Field Service CRM solution</span></span> 
<span data-ttu-id="08da5-127">“库存单位”字段已添加到“产品”实体。</span><span class="sxs-lookup"><span data-stu-id="08da5-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="08da5-128">需要此字段是因为销售和库存单位在 Operations 中不是始终相同，对于工序中的仓库库存，我们需要库存单位。</span><span class="sxs-lookup"><span data-stu-id="08da5-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="08da5-129">当您在库存调整产品中同时为库存调整和库存转移设置产品时，将从产品库存产品值提取单位。</span><span class="sxs-lookup"><span data-stu-id="08da5-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="08da5-130">如果找到值，单位字段将在库存调整产品中被锁定</span><span class="sxs-lookup"><span data-stu-id="08da5-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="08da5-131">“过帐状态”字段已同时添加到库存调整实体和库存转移实体。</span><span class="sxs-lookup"><span data-stu-id="08da5-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="08da5-132">在调整或转移被发送到 Operations 时，此字段用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="08da5-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="08da5-133">字段默认为“已创建 (1)”，及之后不会发送到 Operations。</span><span class="sxs-lookup"><span data-stu-id="08da5-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="08da5-134">在更改为“已过帐 (2)”后，它将被发送到 Operations，但之后您不再能够在“调整”或“转移”中更改任何内容或向其添加任何新行。</span><span class="sxs-lookup"><span data-stu-id="08da5-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="08da5-135">“编号规则”字段已添加到“库存调整产品”实体。</span><span class="sxs-lookup"><span data-stu-id="08da5-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="08da5-136">此字段帮助集成具有唯一编号，以便集成了解何时执行创建和更新。</span><span class="sxs-lookup"><span data-stu-id="08da5-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="08da5-137">在创建第一个库存调整产品时，将在“P2C 自动编号”实体中创建新记录以保持所使用的编号系列和前缀。</span><span class="sxs-lookup"><span data-stu-id="08da5-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="08da5-138">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="08da5-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="08da5-139">在 Finance and Operations 中</span><span class="sxs-lookup"><span data-stu-id="08da5-139">In Finance and Operations</span></span>
<span data-ttu-id="08da5-140">集成生成的集成库存日记帐可以通过批处理作业自动过帐。</span><span class="sxs-lookup"><span data-stu-id="08da5-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="08da5-141">这从以下位置启用：库存管理 > 定期任务 > CDS 集成 > 过帐集成库存日记帐</span><span class="sxs-lookup"><span data-stu-id="08da5-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="08da5-142">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="08da5-142">Template mapping in Data integration</span></span>

<span data-ttu-id="08da5-143">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="08da5-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="08da5-144">库存调整（Field Service 到 Finance and Operations）：库存调整</span><span class="sxs-lookup"><span data-stu-id="08da5-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="08da5-145">[![数据集成中的模板映射](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="08da5-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="08da5-146">库存转移（Field Service 到 Finance and Operations）：库存转移</span><span class="sxs-lookup"><span data-stu-id="08da5-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="08da5-147">[![数据集成中的模板映射](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="08da5-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

