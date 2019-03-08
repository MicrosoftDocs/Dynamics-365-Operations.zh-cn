---
title: 将包含项目的工作订单从 Field Service 同步到 Finance and Operations
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Field Service 与 Microsoft Dynamics 365 for Finance and Operations 的具有项目编号的工作订单的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "329842"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="12fae-103">将包含项目的工作订单从 Field Service 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="12fae-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="12fae-104">此主题介绍用于同步 Microsoft Dynamics 365 for Field Service 与 Microsoft Dynamics 365 for Finance and Operations 的具有项目编号的工作订单的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="12fae-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="12fae-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="12fae-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="12fae-106">使用的 **Field Service 产品（Finance and Operations 到 Field Service）** 模板基于“从目标客户到现金”中的**产品（Finance and Operations 到Sales）– 直接**模板。</span><span class="sxs-lookup"><span data-stu-id="12fae-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="12fae-107">有关详细信息，请参阅[产品（Finance and Operations 到 Sales）– 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。</span><span class="sxs-lookup"><span data-stu-id="12fae-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="12fae-108">本主题仅介绍 **Field Service 产品（Finance and Operations 到 Field Service）** 与 **Field Service 产品（Finance and Operations 到Sales）– 直接**模板之间的差异。</span><span class="sxs-lookup"><span data-stu-id="12fae-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="12fae-109">主要差别在于此模板包括分配到 Field Service 中的工作订单的项目编号的映射，确保在 Finance and Operations 中创建的销售订单包含项目编号，并可以在相关项目上开票。</span><span class="sxs-lookup"><span data-stu-id="12fae-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="12fae-110">除了此模板外，请使用“高级查询和筛选”。</span><span class="sxs-lookup"><span data-stu-id="12fae-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="12fae-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="12fae-111">Templates and tasks</span></span>

<span data-ttu-id="12fae-112">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="12fae-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="12fae-113">包含项目的工作订单（Field Service 到 Finance and Operations）</span><span class="sxs-lookup"><span data-stu-id="12fae-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="12fae-114">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="12fae-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="12fae-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="12fae-115">WorkOrderHeader</span></span>
- <span data-ttu-id="12fae-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="12fae-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="12fae-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="12fae-117">WorkOrderProduct</span></span>
- <span data-ttu-id="12fae-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="12fae-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="12fae-119">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="12fae-119">Field Service CRM solution</span></span>
<span data-ttu-id="12fae-120">**外部项目**字段已添加到“工作订单”实体。</span><span class="sxs-lookup"><span data-stu-id="12fae-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="12fae-121">此字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Finance and Operations 内的一个项目。</span><span class="sxs-lookup"><span data-stu-id="12fae-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="12fae-122">**系统状态**将“打开 - 正在进行(690,970,000)”更改为更高状态后，**外部项目**字段将被锁定，您将无法添加、删除或更改值。</span><span class="sxs-lookup"><span data-stu-id="12fae-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="12fae-123">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="12fae-123">Template mapping in Data integration</span></span>

<span data-ttu-id="12fae-124">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="12fae-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="12fae-125">包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="12fae-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="12fae-126">[![数据集成中的模板映射](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="12fae-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="12fae-127">包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="12fae-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="12fae-128">[![数据集成中的模板映射](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="12fae-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="12fae-129">包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="12fae-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="12fae-130">[![数据集成中的模板映射](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="12fae-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="12fae-131">包含项目的工作订单（Field Service 到 Finance and Operations）：WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="12fae-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="12fae-132">[![数据集成中的模板映射](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="12fae-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
