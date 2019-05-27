---
title: 服务管理
description: 使用“服务管理”建立服务协议和服务预订、处理服务订单和客户查询以及管理和分析对客户的服务传递。
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89035687d87c674cca7fa5fd3126100c4c0ad892
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562595"
---
# <a name="service-management"></a><span data-ttu-id="ffdfe-103">服务管理</span><span class="sxs-lookup"><span data-stu-id="ffdfe-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ffdfe-104">使用**服务管理**建立服务协议和服务预订、处理服务订单和客户查询以及管理和分析对客户的服务传递。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="ffdfe-105">您可以使用服务协议定义在典型服务访问中使用的资源。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="ffdfe-106">您还可以使用服务协议查看针对那些资源向客户开发票的方式。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="ffdfe-107">服务协议还可以包括指定标准响应时间并提供记录实际时间的工具的服务级别协议。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="ffdfe-108">您可以创建服务订单以管理有关由服务技术人员计划的到客户站点的访问和未被服务技术人员计划的到客户站点的访问的信息。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="ffdfe-109">服务订单包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="ffdfe-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="ffdfe-110">服务技术人员将执行的工作的时间</span><span class="sxs-lookup"><span data-stu-id="ffdfe-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="ffdfe-111">服务或维修的类型</span><span class="sxs-lookup"><span data-stu-id="ffdfe-111">The type of service or repair</span></span>

3.  <span data-ttu-id="ffdfe-112">包括故障和诊断的详细信息的待维修的物料</span><span class="sxs-lookup"><span data-stu-id="ffdfe-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="ffdfe-113">与服务或维修相关的任何支出和费用</span><span class="sxs-lookup"><span data-stu-id="ffdfe-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="ffdfe-114">您可以接收、处理以及分派服务请求。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="ffdfe-115">在您创建了服务订单后，您可以使用服务阶段来监视进程并指定控制每一阶段所启用的操作的规则。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="ffdfe-116">在服务订单完成后，您可以在该订单上签核以确认它已完成，然后将该订单过账以开始发票流程。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="ffdfe-117">使用报告工具监视服务订单毛利和预定交易记录，打印工作描述和收据。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="ffdfe-118">业务流程</span><span class="sxs-lookup"><span data-stu-id="ffdfe-118">Business processes</span></span>

<span data-ttu-id="ffdfe-119">下图说明了**服务管理**的最高级别的业务流程，并显示了服务流程在 Microsoft Dynamics 365 for Finance and Operations 中与其他模块集成的地点。</span><span class="sxs-lookup"><span data-stu-id="ffdfe-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ffdfe-120">[![服务管理业务流程图](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="ffdfe-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="ffdfe-121">通过服务管理</span><span class="sxs-lookup"><span data-stu-id="ffdfe-121">Service management at a glance</span></span>

|<span data-ttu-id="ffdfe-122">重要任务</span><span class="sxs-lookup"><span data-stu-id="ffdfe-122">Important tasks</span></span>           | <span data-ttu-id="ffdfe-123">主要页面</span><span class="sxs-lookup"><span data-stu-id="ffdfe-123">Primary pages</span></span>                         |<span data-ttu-id="ffdfe-124">常见报告</span><span class="sxs-lookup"><span data-stu-id="ffdfe-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="ffdfe-125">履行服务协议</span><span class="sxs-lookup"><span data-stu-id="ffdfe-125">Fulfill service agreements</span></span>|<span data-ttu-id="ffdfe-126">服务协议</span><span class="sxs-lookup"><span data-stu-id="ffdfe-126">Service agreements</span></span>                     |<span data-ttu-id="ffdfe-127">服务订单毛利</span><span class="sxs-lookup"><span data-stu-id="ffdfe-127">Service order margin</span></span>         |
|<span data-ttu-id="ffdfe-128">处理客户查询</span><span class="sxs-lookup"><span data-stu-id="ffdfe-128">Handle customer inquiries</span></span> |<span data-ttu-id="ffdfe-129">服务订单</span><span class="sxs-lookup"><span data-stu-id="ffdfe-129">Service orders</span></span>                         |<span data-ttu-id="ffdfe-130">工作描述</span><span class="sxs-lookup"><span data-stu-id="ffdfe-130">Work description</span></span>             |
|                          |<span data-ttu-id="ffdfe-131">发货牌</span><span class="sxs-lookup"><span data-stu-id="ffdfe-131">Dispatch board</span></span>                         |<span data-ttu-id="ffdfe-132">交易记录 - 预订</span><span class="sxs-lookup"><span data-stu-id="ffdfe-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="ffdfe-133">预订费用交易记录</span><span class="sxs-lookup"><span data-stu-id="ffdfe-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="ffdfe-134">服务管理集成</span><span class="sxs-lookup"><span data-stu-id="ffdfe-134">Integration of Service management</span></span>

<span data-ttu-id="ffdfe-135">服务管理可以与以下模块集成：</span><span class="sxs-lookup"><span data-stu-id="ffdfe-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="ffdfe-136">销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="ffdfe-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="ffdfe-137">人力资源</span><span class="sxs-lookup"><span data-stu-id="ffdfe-137">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  

