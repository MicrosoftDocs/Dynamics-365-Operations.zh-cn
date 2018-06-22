---
title: "与 Microsoft Dynamics 365 for Field Service 集成"
description: "此主题概述与 Microsoft Dynamics 365 for Field Service 集成。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: zh-cn
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="ce096-103">与 Microsoft Dynamics 365 for Field Service 集成</span><span class="sxs-lookup"><span data-stu-id="ce096-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce096-104">Microsoft Dynamics 365 for Finance and Operations 支持在 Finance and Operations 与 Microsoft Dynamics 365 for Field Service 之间同步业务流程。</span><span class="sxs-lookup"><span data-stu-id="ce096-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="ce096-105">集成方案的配置方法是使用可扩展的数据集成器模板和 Common Data Service (CDS) 实现业务流程同步。</span><span class="sxs-lookup"><span data-stu-id="ce096-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="ce096-106">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="ce096-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="ce096-107">Field Service 与 Finance and Operations 集成的第一阶段的重点是让 Field Service 中的工作订单和协议在 Finance and Operations 中开票。</span><span class="sxs-lookup"><span data-stu-id="ce096-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="ce096-108">支持的流程在 Field Service 中启动，在这里将工作订单的信息作为销售订单同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="ce096-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="ce096-109">在 Finance and Operations 中，将为销售订单开票以生成发票单据。</span><span class="sxs-lookup"><span data-stu-id="ce096-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="ce096-110">此外，还会将 Field Service 协议发票的信息同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="ce096-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="ce096-111">Microsoft Dynamics 365 数据集成器使用可定制项目同步数据。</span><span class="sxs-lookup"><span data-stu-id="ce096-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="ce096-112">可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体要求。</span><span class="sxs-lookup"><span data-stu-id="ce096-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="ce096-113">Field Service 与 Finance and Operations 集成的第二阶段是实现以下项的同步：</span><span class="sxs-lookup"><span data-stu-id="ce096-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="ce096-114">Finance and Operations 中的产品到 Field Service 中的产品（包括产品类型信息）</span><span class="sxs-lookup"><span data-stu-id="ce096-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="ce096-115">Field Service 中的工作订单到 Finance and Operations 中的销售订单</span><span class="sxs-lookup"><span data-stu-id="ce096-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="ce096-116">Field Service 中的发票到 Finance and Operations 中的普通发票</span><span class="sxs-lookup"><span data-stu-id="ce096-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="ce096-117">若要查看有关如何在 Field Service 与 Finance and Operations 之间同步工作订单的示例，请观看下面的 YouTube 短片：[在 Dynamics 365 for Field Service 与 Finance and Operations 之间同步工作订单](https://www.youtube.com/watch?v=hAB4TDVMjxU)。</span><span class="sxs-lookup"><span data-stu-id="ce096-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="ce096-118">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="ce096-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="ce096-119">Field Service 集成支持以下版本：</span><span class="sxs-lookup"><span data-stu-id="ce096-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="ce096-120">Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）或更高版本</span><span class="sxs-lookup"><span data-stu-id="ce096-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="ce096-121">Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）已于 2018 年 4 月发布，其中包含带平台更新 15 (7.0.4841.35234) 的应用程序版本号 8.0.30.8020。</span><span class="sxs-lookup"><span data-stu-id="ce096-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="ce096-122">Field Service 的系统要求</span><span class="sxs-lookup"><span data-stu-id="ce096-122">System requirements for Field Service</span></span>
<span data-ttu-id="ce096-123">若要使用 Field Service 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="ce096-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="ce096-124">Microsoft Dynamics 365 for Field Service 9.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="ce096-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="ce096-125">Dynamics 365 for Field Service 版本 1612 (9.0.1.733) (DB 9.0.1.733) 联机或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ce096-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="ce096-126">Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。</span><span class="sxs-lookup"><span data-stu-id="ce096-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="ce096-127">可从 [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="ce096-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="ce096-128">适用于 Dynamics 365 版本 1.0.0.0 或更高版本的 Field Service 集成解决方案。</span><span class="sxs-lookup"><span data-stu-id="ce096-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="ce096-129">可从 [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration) 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="ce096-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

