---
title: "与 Microsoft Dynamics 365 for Field Service 集成"
description: "此主题概述与 Microsoft Dynamics 365 for Field Service 集成。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: zh-cn
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="0e946-103">与 Microsoft Dynamics 365 for Field Service 集成</span><span class="sxs-lookup"><span data-stu-id="0e946-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0e946-104">Microsoft Dynamics 365 for Finance and Operations 支持在 Finance and Operations 与 Microsoft Dynamics 365 for Field Service 之间同步业务流程。</span><span class="sxs-lookup"><span data-stu-id="0e946-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="0e946-105">集成方案的配置方法是使用可扩展的数据集成器模板和 Common Data Service (CDS) 实现业务流程同步。</span><span class="sxs-lookup"><span data-stu-id="0e946-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>
<span data-ttu-id="0e946-106">可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体业务需求。</span><span class="sxs-lookup"><span data-stu-id="0e946-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="0e946-107">Field Service 集成紧接着现有客户到现金功能建立。</span><span class="sxs-lookup"><span data-stu-id="0e946-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Finance and Operations 与 Field Service 之间的业务流程同步](./media/field-service-integration.png)

<span data-ttu-id="0e946-109">Field Service 与 Finance and Operations 集成的第一阶段的重点是让 Field Service 中的工作订单和协议在 Finance and Operations 中开票。</span><span class="sxs-lookup"><span data-stu-id="0e946-109">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="0e946-110">支持的流程在 Field Service 中启动，在这里将工作订单的信息作为销售订单同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="0e946-110">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="0e946-111">在 Finance and Operations 中，将为销售订单开票以生成发票单据。</span><span class="sxs-lookup"><span data-stu-id="0e946-111">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="0e946-112">此外，还会将 Field Service 协议发票的信息同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="0e946-112">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="0e946-113">Microsoft Dynamics 365 数据集成器使用可定制项目同步数据。</span><span class="sxs-lookup"><span data-stu-id="0e946-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="0e946-114">可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体要求。</span><span class="sxs-lookup"><span data-stu-id="0e946-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="0e946-115">Field Service 与 Finance and Operations 集成的第二阶段是实现以下项的同步：</span><span class="sxs-lookup"><span data-stu-id="0e946-115">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="0e946-116">Finance and Operations 中的产品到 Field Service 中的产品（包括产品类型信息）</span><span class="sxs-lookup"><span data-stu-id="0e946-116">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="0e946-117">Field Service 中的工作订单到 Finance and Operations 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="0e946-117">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="0e946-118">Field Service 中的发票到 Finance and Operations 中的普通发票</span><span class="sxs-lookup"><span data-stu-id="0e946-118">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="0e946-119">若要查看有关如何在 Field Service 与 Finance and Operations 之间同步工作订单的示例，请观看下面的 YouTube 短片：[如何使用 Microsoft Dynamics 365 集成同步工作订单](https://www.youtube.com/watch?v=46ylO7raZAo)。</span><span class="sxs-lookup"><span data-stu-id="0e946-119">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="0e946-120">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="0e946-120">System requirements for Finance and Operations</span></span>
<span data-ttu-id="0e946-121">Field Service 集成支持以下版本：</span><span class="sxs-lookup"><span data-stu-id="0e946-121">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="0e946-122">Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）或更高版本</span><span class="sxs-lookup"><span data-stu-id="0e946-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="0e946-123">Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）已于 2018 年 4 月发布，其中包含带平台更新 15 (7.0.4841.35234) 的应用程序版本号 8.0.30.8020。</span><span class="sxs-lookup"><span data-stu-id="0e946-123">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="0e946-124">Field Service 的系统要求</span><span class="sxs-lookup"><span data-stu-id="0e946-124">System requirements for Field Service</span></span>
<span data-ttu-id="0e946-125">若要使用 Field Service 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="0e946-125">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="0e946-126">Microsoft Dynamics 365 for Field Service 9.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="0e946-126">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="0e946-127">Dynamics 365 for Field Service 版本 1612 (9.0.1.733) (DB 9.0.1.733) 联机或更高版本。</span><span class="sxs-lookup"><span data-stu-id="0e946-127">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="0e946-128">Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-128">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="0e946-129">可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="0e946-130">适用于 Dynamics 365 版本 1.0.0.0 或更高版本的 Field Service 集成解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-130">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="0e946-131">可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-131">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a><span data-ttu-id="0e946-132">与 Microsoft Dynamics 365 for Field Service 的集成，包括库存和项目信息</span><span class="sxs-lookup"><span data-stu-id="0e946-132">Integration with Microsoft Dynamics 365 for Field Service, including inventory and project information</span></span>

<span data-ttu-id="0e946-133">此第二个阶段的附加功能关注为现场技术人员提供有关 Finance and Operations 的库存信息的见解，让他们可以更新库存水平、执行物料转移。</span><span class="sxs-lookup"><span data-stu-id="0e946-133">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Finance and Operations, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="0e946-134">此外，安装或为售出货物提供服务的公司将通过项目集成受益于更好地控制以及对完整销售和服务流程的了解。</span><span class="sxs-lookup"><span data-stu-id="0e946-134">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="0e946-135">功能包括以下集成：</span><span class="sxs-lookup"><span data-stu-id="0e946-135">Functionality includes integration of:</span></span>
- <span data-ttu-id="0e946-136">仓库信息</span><span class="sxs-lookup"><span data-stu-id="0e946-136">Warehouse information</span></span>
- <span data-ttu-id="0e946-137">现有库存信息</span><span class="sxs-lookup"><span data-stu-id="0e946-137">On-hand inventory information</span></span>
- <span data-ttu-id="0e946-138">库存转移</span><span class="sxs-lookup"><span data-stu-id="0e946-138">Inventory transfers</span></span>
- <span data-ttu-id="0e946-139">库存调整</span><span class="sxs-lookup"><span data-stu-id="0e946-139">Inventory adjustments</span></span>
- <span data-ttu-id="0e946-140">与 Dynamics 365 for Field Service 工作订单连接的 Dynamics 365 for Finance and Operations 项目</span><span class="sxs-lookup"><span data-stu-id="0e946-140">Dynamics 365 for Finance and Operations projects connected with Dynamics 365 for Field Service work orders</span></span>
- <span data-ttu-id="0e946-141">包含 Dynamics 365 for Finance and Operations 项目链接的 Dynamics 365 for Field Service 工作订单将此项目编号应用到 Dynamics 365 for Finance and Operations 销售订单以允许从项目开票。</span><span class="sxs-lookup"><span data-stu-id="0e946-141">Dynamics 365 for Field Service work orders with link to Dynamics 365 for Finance and Operations projects, apply this project number to the Dynamics 365 for Finance and Operations sales order to allow invoicing from the project.</span></span> 

![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="0e946-143">Field Service 与 Finance and Operations 集成的第二阶段支持与以下模板的同步：</span><span class="sxs-lookup"><span data-stu-id="0e946-143">The second phase of the integration between Field Service and Finance and Operations enables synchronization with the following templates:</span></span>
- <span data-ttu-id="0e946-144">仓库（Fin and Ops 到 Field Service）- 仓库从 Finance and Operations 到 Field Service [高级查询]</span><span class="sxs-lookup"><span data-stu-id="0e946-144">Warehouses (Fin and Ops to Field Service) - Warehouses from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="0e946-145">产品库存（Fin and Ops 到 Field Service）- 库存水平信息从 Finance and Operations 到 Field Service [高级查询]</span><span class="sxs-lookup"><span data-stu-id="0e946-145">Product Inventory (Fin and Ops to Field Service) - Inventory level information from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="0e946-146">库存调整（Field Service 到 Fin and Ops）- 库存调整从 Field Service 到 Finance and Operations [高级查询]</span><span class="sxs-lookup"><span data-stu-id="0e946-146">Inventory Adjustment (Field Service to Fin and Ops) - Inventory adjustments from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="0e946-147">库存转移（Field Service 到 Fin and Ops）- 库存转移从 Field Service 到 Finance and Operations [高级查询]</span><span class="sxs-lookup"><span data-stu-id="0e946-147">Inventory Transfers (Field Service to Fin and Ops) - Inventory transfers from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="0e946-148">项目（Fin and Ops 到 Field Service）- 项目列表从 Finance and Operations 到 Field Service</span><span class="sxs-lookup"><span data-stu-id="0e946-148">Projects (Fin and Ops to Field Service) - Project list from Finance and Operations to Field Service</span></span> 
- <span data-ttu-id="0e946-149">项目的工作订单（Field Service 到 Fin and Ops）- Field Service 中工作订单到 Finance and Operations 中的销售订单，提供项目支持[高级查询]</span><span class="sxs-lookup"><span data-stu-id="0e946-149">Work Orders with Project (Field Service to Fin and Ops) - Work orders in Field Service to Sales orders  in Finance and Operations, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="0e946-150">包含库存单位的 Field Service 产品（Fin and Ops 到 Sales）- Finance and Operations“适售的已发布产品”到 Field Service 的“销售产品”，包括库存单位</span><span class="sxs-lookup"><span data-stu-id="0e946-150">Field Service Products with Inventory unit (Fin and Ops to Sales) - Finance and Operations 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="0e946-151">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="0e946-151">System requirements for Finance and Operations</span></span>
<span data-ttu-id="0e946-152">Field Service 集成支持以下版本：</span><span class="sxs-lookup"><span data-stu-id="0e946-152">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="0e946-153">Dynamics 365 for Finance and Operations 版本 8.1.2（2019 年 12 月）已于 2019 年 12 月发布，其中包含带平台更新 22 (7.0.5095) 的应用程序版本号 8.1.195。</span><span class="sxs-lookup"><span data-stu-id="0e946-153">Dynamics 365 for Finance and Operations version 8.1.2 (December 2019) was released in December 2019 and has an application build number 8.1.195 with Platform Update 22 (7.0.5095).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="0e946-154">Field Service 的系统要求</span><span class="sxs-lookup"><span data-stu-id="0e946-154">System requirements for Field Service</span></span>
<span data-ttu-id="0e946-155">若要使用 Field Service 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="0e946-155">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="0e946-156">Dynamics 365 9.1.x 上的 Field Service for Dynamics 365（版本 8.2.0.286）或更高版本 - 2018 年 11 月发布</span><span class="sxs-lookup"><span data-stu-id="0e946-156">Field Service for Dynamics 365 (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="0e946-157">Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-157">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="0e946-158">可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-158">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="0e946-159">适用于 Dynamics 365 版本 2.0.0.0 或更高版本的“Field Service 集成、项目和库存”解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-159">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="0e946-160">可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="0e946-160">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>

