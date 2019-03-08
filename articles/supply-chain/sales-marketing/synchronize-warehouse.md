---
title: 将仓库从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的仓库的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "340307"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="6338a-103">将仓库从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="6338a-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6338a-104">此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的仓库的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="6338a-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6338a-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="6338a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6338a-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="6338a-106">Templates and tasks</span></span>
<span data-ttu-id="6338a-107">以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的仓库的同步。</span><span class="sxs-lookup"><span data-stu-id="6338a-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6338a-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="6338a-108">**Template in Data integration**</span></span>
- <span data-ttu-id="6338a-109">仓库（Finance and Operations 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="6338a-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="6338a-110">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="6338a-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="6338a-111">存放地点</span><span class="sxs-lookup"><span data-stu-id="6338a-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="6338a-112">实体集</span><span class="sxs-lookup"><span data-stu-id="6338a-112">Entity set</span></span>
| <span data-ttu-id="6338a-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="6338a-113">Field Service</span></span>    | <span data-ttu-id="6338a-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6338a-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="6338a-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="6338a-115">msdyn_warehouses</span></span> | <span data-ttu-id="6338a-116">仓库</span><span class="sxs-lookup"><span data-stu-id="6338a-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="6338a-117">实体流</span><span class="sxs-lookup"><span data-stu-id="6338a-117">Entity flow</span></span>
<span data-ttu-id="6338a-118">可通过 Common Data Service (CDS) 数据集成项目将在 Finance and Operations 中创建和维护的仓库同步到 Field Service。</span><span class="sxs-lookup"><span data-stu-id="6338a-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="6338a-119">您要同步到 Field Service 的仓库将通过项目上的“高级查询和筛选”进行控制。</span><span class="sxs-lookup"><span data-stu-id="6338a-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="6338a-120">从 Finance and Operations 同步的仓库在 Field Service 中创建，**外部维护**字段设置为**是**，记录为只读。</span><span class="sxs-lookup"><span data-stu-id="6338a-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6338a-121">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="6338a-121">Field Service CRM solution</span></span>
<span data-ttu-id="6338a-122">若要为 Field Service 与 Finance and Operations 之间的同步提供支持，需要 Field Service CRM 解决方案的更多功能。</span><span class="sxs-lookup"><span data-stu-id="6338a-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="6338a-123">在此解决方案中，**外部维护**字段已添加到**仓库 (msdyn_warehouses)** 实体。</span><span class="sxs-lookup"><span data-stu-id="6338a-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="6338a-124">此字段帮助确定仓库是否是从 Finance and Operations 处理或是否只存在于 Field Service 中。</span><span class="sxs-lookup"><span data-stu-id="6338a-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="6338a-125">此字段的设置包括：</span><span class="sxs-lookup"><span data-stu-id="6338a-125">The settings for this field include:</span></span>
- <span data-ttu-id="6338a-126">**是** – 仓库来自 Finance and Operations，且不可在 Sales 中编辑。</span><span class="sxs-lookup"><span data-stu-id="6338a-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="6338a-127">**否** – 仓库在 Field Service 中直接输入并在这里维护。</span><span class="sxs-lookup"><span data-stu-id="6338a-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="6338a-128">**外部维护**字段帮助控制工作订单上库存水平、调整、转移和使用的同步。</span><span class="sxs-lookup"><span data-stu-id="6338a-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="6338a-129">只有**外部维护**设置为**是**的仓库可以用于直接同步到其他系统中的同一仓库。</span><span class="sxs-lookup"><span data-stu-id="6338a-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="6338a-130">可以在 Field Service（**外部维护** = 否）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Finance and Operations 中的单个仓库。</span><span class="sxs-lookup"><span data-stu-id="6338a-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="6338a-131">这用于您希望 Field Service 掌握详细的库存水平并向 Finance and Operations 发送更新的情况。</span><span class="sxs-lookup"><span data-stu-id="6338a-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="6338a-132">在这种情况下，Field Service 不会收到来自 Finance and Operations 的库存水平更新。</span><span class="sxs-lookup"><span data-stu-id="6338a-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="6338a-133">更多信息，请参阅[将库存调整从 Field Service 同步到 Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) 和[将 Field Service 的工作订单同步到链接到 Finance and Operations 中的项目的销售订单](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。</span><span class="sxs-lookup"><span data-stu-id="6338a-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6338a-134">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="6338a-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="6338a-135">数据集成项目</span><span class="sxs-lookup"><span data-stu-id="6338a-135">Data Integration project</span></span>
<span data-ttu-id="6338a-136">在同步仓库前，请确保更新项目上的“高级查询和筛选”以仅包括您要从 Finance and Operations 带入 Field Service 的仓库。</span><span class="sxs-lookup"><span data-stu-id="6338a-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="6338a-137">请注意，您需要 Field Service 中的仓库来将其应用到工作订单、调整和转移。</span><span class="sxs-lookup"><span data-stu-id="6338a-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="6338a-138">确保有 **msdyn_warehouses** 的**集成键**：</span><span class="sxs-lookup"><span data-stu-id="6338a-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="6338a-139">转至“数据集成”。</span><span class="sxs-lookup"><span data-stu-id="6338a-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="6338a-140">选择**连接集** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6338a-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="6338a-141">选择用于工作订单同步的连接集。</span><span class="sxs-lookup"><span data-stu-id="6338a-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="6338a-142">选择**集成键**选项卡。</span><span class="sxs-lookup"><span data-stu-id="6338a-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="6338a-143">找到 msdyn_warehouses 并确认是否添加了 **msdyn_name (name)** 键。</span><span class="sxs-lookup"><span data-stu-id="6338a-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="6338a-144">如果不显示，请通过单击页面顶部的**添加键**，然后单击**保存**添加。</span><span class="sxs-lookup"><span data-stu-id="6338a-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6338a-145">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="6338a-145">Template mapping in Data integration</span></span>

<span data-ttu-id="6338a-146">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="6338a-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="6338a-147">仓库（Finance and Operations 到 Field Service）：仓库</span><span class="sxs-lookup"><span data-stu-id="6338a-147">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="6338a-148">[![数据集成中的模板映射](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="6338a-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
