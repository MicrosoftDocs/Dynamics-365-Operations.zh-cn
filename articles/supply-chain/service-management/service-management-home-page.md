---
title: 服务管理概览
description: 使用“服务管理”建立服务协议和服务预订、处理服务订单和客户查询以及管理和分析对客户的服务传递。
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70c0a6c82e0227319c4e95ad7b60a97c7b03401a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010489"
---
# <a name="service-management-overview"></a><span data-ttu-id="8b2e0-103">服务管理概览</span><span class="sxs-lookup"><span data-stu-id="8b2e0-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8b2e0-104">使用 **服务管理** 建立服务协议和服务预订、处理服务订单和客户查询以及管理和分析对客户的服务传递。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="8b2e0-105">您可以使用服务协议定义在典型服务访问中使用的资源。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="8b2e0-106">您还可以使用服务协议查看针对那些资源向客户开发票的方式。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="8b2e0-107">服务协议还可以包括指定标准响应时间并提供记录实际时间的工具的服务级别协议。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="8b2e0-108">您可以创建服务订单以管理有关由服务技术人员计划的到客户站点的访问和未被服务技术人员计划的到客户站点的访问的信息。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="8b2e0-109">服务订单包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="8b2e0-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="8b2e0-110">服务技术人员将执行的工作的时间</span><span class="sxs-lookup"><span data-stu-id="8b2e0-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="8b2e0-111">服务或维修的类型</span><span class="sxs-lookup"><span data-stu-id="8b2e0-111">The type of service or repair</span></span>

3.  <span data-ttu-id="8b2e0-112">包括故障和诊断的详细信息的待维修的物料</span><span class="sxs-lookup"><span data-stu-id="8b2e0-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="8b2e0-113">与服务或维修相关的任何支出和费用</span><span class="sxs-lookup"><span data-stu-id="8b2e0-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="8b2e0-114">您可以接收、处理以及分派服务请求。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="8b2e0-115">在您创建了服务订单后，您可以使用服务阶段来监视进程并指定控制每一阶段所启用的操作的规则。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="8b2e0-116">在服务订单完成后，您可以在该订单上签核以确认它已完成，然后将该订单过账以开始发票流程。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="8b2e0-117">使用报告工具监视服务订单毛利和预定交易记录，打印工作描述和收据。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="8b2e0-118">业务流程</span><span class="sxs-lookup"><span data-stu-id="8b2e0-118">Business processes</span></span>

<span data-ttu-id="8b2e0-119">下图说明了 **服务管理** 的最高级别的业务流程，并显示了服务流程与其他模块集成的地点。</span><span class="sxs-lookup"><span data-stu-id="8b2e0-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules.</span></span>

<span data-ttu-id="8b2e0-120">[![服务管理业务流程图](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="8b2e0-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="8b2e0-121">通过服务管理</span><span class="sxs-lookup"><span data-stu-id="8b2e0-121">Service management at a glance</span></span>

|<span data-ttu-id="8b2e0-122">重要任务</span><span class="sxs-lookup"><span data-stu-id="8b2e0-122">Important tasks</span></span>           | <span data-ttu-id="8b2e0-123">主要页面</span><span class="sxs-lookup"><span data-stu-id="8b2e0-123">Primary pages</span></span>                         |<span data-ttu-id="8b2e0-124">常见报告</span><span class="sxs-lookup"><span data-stu-id="8b2e0-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="8b2e0-125">履行服务协议</span><span class="sxs-lookup"><span data-stu-id="8b2e0-125">Fulfill service agreements</span></span>|<span data-ttu-id="8b2e0-126">服务协议</span><span class="sxs-lookup"><span data-stu-id="8b2e0-126">Service agreements</span></span>                     |<span data-ttu-id="8b2e0-127">服务订单毛利</span><span class="sxs-lookup"><span data-stu-id="8b2e0-127">Service order margin</span></span>         |
|<span data-ttu-id="8b2e0-128">处理客户查询</span><span class="sxs-lookup"><span data-stu-id="8b2e0-128">Handle customer inquiries</span></span> |<span data-ttu-id="8b2e0-129">服务订单</span><span class="sxs-lookup"><span data-stu-id="8b2e0-129">Service orders</span></span>                         |<span data-ttu-id="8b2e0-130">工作描述</span><span class="sxs-lookup"><span data-stu-id="8b2e0-130">Work description</span></span>             |
|                          |<span data-ttu-id="8b2e0-131">发货牌</span><span class="sxs-lookup"><span data-stu-id="8b2e0-131">Dispatch board</span></span>                         |<span data-ttu-id="8b2e0-132">交易记录 - 预订</span><span class="sxs-lookup"><span data-stu-id="8b2e0-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="8b2e0-133">预订费用交易记录</span><span class="sxs-lookup"><span data-stu-id="8b2e0-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="8b2e0-134">服务管理集成</span><span class="sxs-lookup"><span data-stu-id="8b2e0-134">Integration of Service management</span></span>

<span data-ttu-id="8b2e0-135">服务管理可以与以下模块集成：</span><span class="sxs-lookup"><span data-stu-id="8b2e0-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="8b2e0-136">销售和市场营销概览</span><span class="sxs-lookup"><span data-stu-id="8b2e0-136">Sales and marketing overview</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="8b2e0-137">人力资源</span><span class="sxs-lookup"><span data-stu-id="8b2e0-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

