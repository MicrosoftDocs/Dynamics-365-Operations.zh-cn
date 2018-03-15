---
title: "服务协议"
description: "在服务协议中，您可以定义在典型服务访问中使用的资源以及如何对这些资源向客户开票。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: zh-cn
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a><span data-ttu-id="5c1bf-103">服务协议</span><span class="sxs-lookup"><span data-stu-id="5c1bf-103">Service agreements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5c1bf-104">在服务协议中，您可以定义在典型服务访问中使用的资源以及如何对这些资源向客户开票。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="5c1bf-105">所有服务协议都附加到交易记录通过其过帐和开票的项目。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="5c1bf-106">不过，您还可以通过项目直接对服务订单交易记录开票，而不必首先将该服务订单连接到某一服务协议。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="5c1bf-107">如果服务订单针对仅限一次性的服务访问，并且快速处理服务交易记录的需要优先于维护某一时段中与客户有关的详细服务协议信息的需要，则您可能决定要这样做。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="5c1bf-108">服务协议</span><span class="sxs-lookup"><span data-stu-id="5c1bf-108">Service agreement</span></span>

<span data-ttu-id="5c1bf-109">在每个服务协议中，您必须指定项目、服务协议 ID 和服务协议组。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="5c1bf-110">服务协议组可用于对服务协议进行排序和组织。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="5c1bf-111">服务协议的标题包含应用于所有附加的协议行的设置：</span><span class="sxs-lookup"><span data-stu-id="5c1bf-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="5c1bf-112">服务协议是否被暂停。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="5c1bf-113">如果服务协议被暂停，您不能根据服务协议生成服务订单。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="5c1bf-114">服务协议的持续时间。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="5c1bf-115">服务订单行如何合并到服务订单中。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="5c1bf-116">服务协议是否是模板。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="5c1bf-117">在服务协议标题中，您还设置通过输入要附加到该协议的各行的特定服务任务或服务对象可用于该服务协议的所有的服务对象和服务任务。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="5c1bf-118">从服务协议标题，您还可以将服务协议行或服务模板行复制到当前服务协议中。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="5c1bf-119">您可以暂停服务协议并停止执行各个服务协议行。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="5c1bf-120">如果选中服务协议行的**暂停**复选框，则不能：</span><span class="sxs-lookup"><span data-stu-id="5c1bf-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="5c1bf-121">从服务协议自动或手动创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="5c1bf-122">如果选中服务协议行的**已停止**复选框，则不能：</span><span class="sxs-lookup"><span data-stu-id="5c1bf-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="5c1bf-123">从服务协议行自动或手动创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="5c1bf-124">将服务协议行复制到其他服务协议或服务订单。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="5c1bf-125">如果暂停服务协议，则停止执行所有附加的行而不管这些行的状态是什么。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="5c1bf-126">服务协议行</span><span class="sxs-lookup"><span data-stu-id="5c1bf-126">Service-agreement lines</span></span>

<span data-ttu-id="5c1bf-127">每个服务协议行详细描述建议的服务工作的内容。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="5c1bf-128">这些行包含以下设置：</span><span class="sxs-lookup"><span data-stu-id="5c1bf-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="5c1bf-129">交易记录类型和交易记录类型的描述。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="5c1bf-130">执行服务工作的员工。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="5c1bf-131">必须根据服务协议对其执行服务的对象。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="5c1bf-132">执行工作以及登记关联物料、支出和费用交易记录的频率。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="5c1bf-133">服务订单行可组合到某一服务订单中的时间范围。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="5c1bf-134">用于将多组协议行一起组合到工作任务中和用于向服务技术人员和客户总结要提供什么服务任务的服务任务。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="5c1bf-135">是否停止某一行。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-135">Whether a line is stopped.</span></span> <span data-ttu-id="5c1bf-136">如果停止某一行，您不能为该单独的行创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="5c1bf-137">诸如类别和行属性之类的项目设置。</span><span class="sxs-lookup"><span data-stu-id="5c1bf-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c1bf-138">相关主题</span><span class="sxs-lookup"><span data-stu-id="5c1bf-138">Related topics</span></span>

[<span data-ttu-id="5c1bf-139">创建服务协议</span><span class="sxs-lookup"><span data-stu-id="5c1bf-139">Create service agreements</span></span>](create-service-agreements.md)
