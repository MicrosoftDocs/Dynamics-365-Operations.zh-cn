---
title: 与 Microsoft Dynamics 365 Field Service 的集成概述
description: 本主题提供与 Microsoft Dynamics 365 Field Service 集成的概述。
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 18eef310470cafd9d59bb1c848bbaeb8bf5b9fa1
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528891"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="f7184-103">与 Microsoft Dynamics 365 Field Service 的集成概述</span><span class="sxs-lookup"><span data-stu-id="f7184-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7184-104">Supply Chain Management 实现 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 之间的业务流程同步。</span><span class="sxs-lookup"><span data-stu-id="f7184-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="f7184-105">集成方案的配置方法是使用可扩展的数据集成器模板和 Common Data Service 实现业务流程同步。</span><span class="sxs-lookup"><span data-stu-id="f7184-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="f7184-106">可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体业务需求。</span><span class="sxs-lookup"><span data-stu-id="f7184-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="f7184-107">Field Service 集成紧接着现有客户到现金功能建立。</span><span class="sxs-lookup"><span data-stu-id="f7184-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/field-service-integration.png)

<span data-ttu-id="f7184-109">Field Service 与 Supply Chain Management 集成的第一阶段的重点是让 Field Service 中的工作订单和协议在 Supply Chain Management 中开票。</span><span class="sxs-lookup"><span data-stu-id="f7184-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="f7184-110">支持的流程在 Field Service 中启动，在这里将工作订单的信息作为销售订单同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="f7184-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="f7184-111">在 Supply Chain Management 中，将为销售订单开票以生成发票单据。</span><span class="sxs-lookup"><span data-stu-id="f7184-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="f7184-112">此外，还会将 Field Service 协议发票的信息同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="f7184-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="f7184-113">Microsoft Dynamics 365 数据集成器使用可定制项目同步数据。</span><span class="sxs-lookup"><span data-stu-id="f7184-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="f7184-114">可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体要求。</span><span class="sxs-lookup"><span data-stu-id="f7184-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="f7184-115">Field Service 与 Supply Chain Management 集成的第二阶段是实现以下项的同步：</span><span class="sxs-lookup"><span data-stu-id="f7184-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="f7184-116">将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品</span><span class="sxs-lookup"><span data-stu-id="f7184-116">Synchronize products in Supply Chain Management to products in Field Service</span></span>](field-service-product.md)
- [<span data-ttu-id="f7184-117">将 Field Service 中的工作订单同步到 Supply Chain Management 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="f7184-117">Synchronize work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="f7184-118">将 Field Service 中的协议发票同步为 Supply Chain Management 中的普通发票</span><span class="sxs-lookup"><span data-stu-id="f7184-118">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="f7184-119">若要查看有关如何在 Field Service 与 Supply Chain Management 之间同步工作订单的示例，请观看下面的 YouTube 短片：[如何使用 Microsoft Dynamics 365 集成同步工作订单](https://www.youtube.com/watch?v=46ylO7raZAo)。</span><span class="sxs-lookup"><span data-stu-id="f7184-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="f7184-120">与 Field Service 的集成，包括库存和项目信息</span><span class="sxs-lookup"><span data-stu-id="f7184-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="f7184-121">此第二个阶段的附加功能关注为现场技术人员提供有关 Supply Chain Management 的库存信息的见解，让他们可以更新库存水平、执行物料转移。</span><span class="sxs-lookup"><span data-stu-id="f7184-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="f7184-122">此外，安装或为售出货物提供服务的公司将通过项目集成受益于更好地控制以及对完整销售和服务流程的了解。</span><span class="sxs-lookup"><span data-stu-id="f7184-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="f7184-123">功能包括以下集成：</span><span class="sxs-lookup"><span data-stu-id="f7184-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="f7184-124">仓库信息</span><span class="sxs-lookup"><span data-stu-id="f7184-124">Warehouse information</span></span>
- <span data-ttu-id="f7184-125">现有库存信息</span><span class="sxs-lookup"><span data-stu-id="f7184-125">On-hand inventory information</span></span>
- <span data-ttu-id="f7184-126">库存转移</span><span class="sxs-lookup"><span data-stu-id="f7184-126">Inventory transfers</span></span>
- <span data-ttu-id="f7184-127">库存调整</span><span class="sxs-lookup"><span data-stu-id="f7184-127">Inventory adjustments</span></span>
- <span data-ttu-id="f7184-128">与 Dynamics 365 Field Service 工作订单连接的 Supply Chain Management 项目</span><span class="sxs-lookup"><span data-stu-id="f7184-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="f7184-129">包含 Supply Chain Management 项目链接的 Dynamics 365 Field Service 工作订单将此项目编号应用于销售订单以允许从项目开票。</span><span class="sxs-lookup"><span data-stu-id="f7184-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="f7184-131">Field Service 与 Supply Chain Management 集成的第二阶段支持与以下模板的同步：</span><span class="sxs-lookup"><span data-stu-id="f7184-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="f7184-132">仓库（Supply Chain Management 到 Field Service）- 仓库从 Supply Chain Management 到 Field Service [高级查询]</span><span class="sxs-lookup"><span data-stu-id="f7184-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="f7184-133">产品库存（Supply Chain Management 到 Field Service）- 库存级别信息从 Supply Chain Management 到 Field Service [高级查询]</span><span class="sxs-lookup"><span data-stu-id="f7184-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="f7184-134">库存调整（Field Service 到 Supply Chain Management）- 库存调整从 Field Service 到 Supply Chain Management [高级查询]</span><span class="sxs-lookup"><span data-stu-id="f7184-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="f7184-135">库存转移（Field Service 到 Supply Chain Management）- 库存转移从 Field Service 到 Supply Chain Management [高级查询]</span><span class="sxs-lookup"><span data-stu-id="f7184-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="f7184-136">项目（Supply Chain Management 到 Field Service）- 项目列表从 Supply Chain Management 到 Field Service</span><span class="sxs-lookup"><span data-stu-id="f7184-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="f7184-137">项目的工作订单（Field Service 到 Supply Chain Management）- Field Service 中工作订单到 Supply Chain Management 中的销售订单，提供项目支持[高级查询]</span><span class="sxs-lookup"><span data-stu-id="f7184-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="f7184-138">包含库存单位的 Field Service 产品（Supply Chain Management 到 Sales）- Supply Chain Management“适售的已发布产品”到 Field Service 的“销售产品”，包括库存单位</span><span class="sxs-lookup"><span data-stu-id="f7184-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="f7184-139">系统要求</span><span class="sxs-lookup"><span data-stu-id="f7184-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="f7184-140">Supply Chain Management 的系统要求</span><span class="sxs-lookup"><span data-stu-id="f7184-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="f7184-141">Field Service 集成支持以下版本：</span><span class="sxs-lookup"><span data-stu-id="f7184-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="f7184-142">Dynamics 365 for Finance and Operations 版本 8.1.2（2018 年 12 月）通过平台更新 22 (7.0.5095) 在 2018 年 12 月发布，具有应用程序内部版本号 8.1.195。</span><span class="sxs-lookup"><span data-stu-id="f7184-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="f7184-143">Field Service 的系统要求</span><span class="sxs-lookup"><span data-stu-id="f7184-143">System requirements for Field Service</span></span>
<span data-ttu-id="f7184-144">若要使用 Field Service 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="f7184-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="f7184-145">Dynamics 365 9.1.x 上的 Field Service（版本 8.2.0.286）或更高版本 - 2018 年 11 月发布</span><span class="sxs-lookup"><span data-stu-id="f7184-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="f7184-146">Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。</span><span class="sxs-lookup"><span data-stu-id="f7184-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="f7184-147">可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="f7184-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="f7184-148">适用于 Dynamics 365 版本 2.0.0.0 或更高版本的“Field Service 集成、项目和库存”解决方案。</span><span class="sxs-lookup"><span data-stu-id="f7184-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="f7184-149">可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="f7184-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
