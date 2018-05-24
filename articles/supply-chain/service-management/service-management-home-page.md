---
title: "服务管理"
description: "使用“服务管理”建立服务协议和服务预订、处理服务订单和客户查询以及管理和分析对客户的服务传递。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: zh-cn
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="f8b67-103">服务管理</span><span class="sxs-lookup"><span data-stu-id="f8b67-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f8b67-104">使用**服务管理**建立服务协议和服务预订、处理服务订单和客户查询以及管理和分析对客户的服务传递。</span><span class="sxs-lookup"><span data-stu-id="f8b67-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="f8b67-105">您可以使用服务协议定义在典型服务访问中使用的资源。</span><span class="sxs-lookup"><span data-stu-id="f8b67-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="f8b67-106">您还可以使用服务协议查看针对那些资源向客户开发票的方式。</span><span class="sxs-lookup"><span data-stu-id="f8b67-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="f8b67-107">服务协议还可以包括指定标准响应时间并提供记录实际时间的工具的服务级别协议。</span><span class="sxs-lookup"><span data-stu-id="f8b67-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="f8b67-108">您可以创建服务订单以管理有关由服务技术人员计划的到客户站点的访问和未被服务技术人员计划的到客户站点的访问的信息。</span><span class="sxs-lookup"><span data-stu-id="f8b67-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="f8b67-109">服务订单包括以下信息：</span><span class="sxs-lookup"><span data-stu-id="f8b67-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="f8b67-110">服务技术人员将执行的工作的时间</span><span class="sxs-lookup"><span data-stu-id="f8b67-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="f8b67-111">服务或维修的类型</span><span class="sxs-lookup"><span data-stu-id="f8b67-111">The type of service or repair</span></span>

3.  <span data-ttu-id="f8b67-112">包括故障和诊断的详细信息的待维修的物料</span><span class="sxs-lookup"><span data-stu-id="f8b67-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="f8b67-113">与服务或维修相关的任何支出和费用</span><span class="sxs-lookup"><span data-stu-id="f8b67-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="f8b67-114">客户可以使用“企业门户”通过 Internet 提交服务请求。</span><span class="sxs-lookup"><span data-stu-id="f8b67-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="f8b67-115">您可以接收、处理以及分派这些请求。</span><span class="sxs-lookup"><span data-stu-id="f8b67-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="f8b67-116">在您创建了服务订单后，您可以使用服务阶段来监视进程并指定控制每一阶段所启用的操作的规则。</span><span class="sxs-lookup"><span data-stu-id="f8b67-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="f8b67-117">在服务订单完成后，您可以在该订单上签核以确认它已完成，然后将该订单过账以开始发票流程。</span><span class="sxs-lookup"><span data-stu-id="f8b67-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="f8b67-118">使用报告工具监视服务订单毛利和预定交易记录，打印工作描述和收据。</span><span class="sxs-lookup"><span data-stu-id="f8b67-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="f8b67-119">业务流程</span><span class="sxs-lookup"><span data-stu-id="f8b67-119">Business processes</span></span>

<span data-ttu-id="f8b67-120">下图显示**服务管理**的高级业务流程，并显示在哪些情况下服务流程与 Microsoft Dynamics 365 for Finance and Operations 中的其他模块集成。</span><span class="sxs-lookup"><span data-stu-id="f8b67-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f8b67-121">[![服务管理业务流程图](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="f8b67-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="f8b67-122">通过服务管理</span><span class="sxs-lookup"><span data-stu-id="f8b67-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8b67-123">重要任务</span><span class="sxs-lookup"><span data-stu-id="f8b67-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="f8b67-124">主要窗体</span><span class="sxs-lookup"><span data-stu-id="f8b67-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="f8b67-125">常见报告</span><span class="sxs-lookup"><span data-stu-id="f8b67-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8b67-126">履行服务协议</span><span class="sxs-lookup"><span data-stu-id="f8b67-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="f8b67-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">服务协议（窗体）</a></span><span class="sxs-lookup"><span data-stu-id="f8b67-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="f8b67-128"><strong>服务订单毛利</strong></span><span class="sxs-lookup"><span data-stu-id="f8b67-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8b67-129">处理客户查询</span><span class="sxs-lookup"><span data-stu-id="f8b67-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="f8b67-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">服务订单（窗体）</a></span><span class="sxs-lookup"><span data-stu-id="f8b67-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="f8b67-131"><strong>工作描述</strong></span><span class="sxs-lookup"><span data-stu-id="f8b67-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f8b67-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">发货牌（窗体）</a></span><span class="sxs-lookup"><span data-stu-id="f8b67-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="f8b67-133"><strong>交易记录 - 预订</strong></span><span class="sxs-lookup"><span data-stu-id="f8b67-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f8b67-134"><strong>预订费用交易记录</strong></span><span class="sxs-lookup"><span data-stu-id="f8b67-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="f8b67-135">服务管理集成</span><span class="sxs-lookup"><span data-stu-id="f8b67-135">Integration of Service management</span></span>

<span data-ttu-id="f8b67-136">“服务管理”可以与 Microsoft Dynamics 365 for Finance and Operations 中的以下模块集成：</span><span class="sxs-lookup"><span data-stu-id="f8b67-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="f8b67-137">销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="f8b67-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="f8b67-138">人力资源</span><span class="sxs-lookup"><span data-stu-id="f8b67-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


