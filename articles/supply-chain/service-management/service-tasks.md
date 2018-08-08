---
title: "服务任务"
description: "使用服务任务可以描述要在服务订单期间完成的任务。 技术人员和客户都可以看到此信息。"
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="service-tasks"></a><span data-ttu-id="daaf8-104">服务任务</span><span class="sxs-lookup"><span data-stu-id="daaf8-104">Service tasks</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="daaf8-105">使用服务任务可以描述要在服务订单期间完成的任务。</span><span class="sxs-lookup"><span data-stu-id="daaf8-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="daaf8-106">技术人员和客户都可以看到此信息。</span><span class="sxs-lookup"><span data-stu-id="daaf8-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="daaf8-107">您在**服务任务**页面中创建服务任务；并且通过创建服务任务关系，将服务任务与特定的服务协议或服务订单相关联。</span><span class="sxs-lookup"><span data-stu-id="daaf8-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="daaf8-108">每次您创建服务任务关系时，都可以创建以下：</span><span class="sxs-lookup"><span data-stu-id="daaf8-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="daaf8-109">针对任务的内部工作记录，例如需要让技术人员知道的重要任务的详细技术请求。</span><span class="sxs-lookup"><span data-stu-id="daaf8-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="daaf8-110">可由客户看到的外部工作记录。</span><span class="sxs-lookup"><span data-stu-id="daaf8-110">External notes that the customer can see.</span></span> <span data-ttu-id="daaf8-111">这些外部工作记录针对根据客户和服务公司之间的协议要完成的任务，提供技术上较为浅显的解释。</span><span class="sxs-lookup"><span data-stu-id="daaf8-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="daaf8-112">在您设置了服务任务与服务订单或服务协议之间的服务任务关系时，在为当前服务订单或服务协议创建服务订单行或服务协议行时，可以指定此服务任务。</span><span class="sxs-lookup"><span data-stu-id="daaf8-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="daaf8-113">当您从某一服务协议生成服务订单时，可以使用分配给各服务协议行的服务任务，将服务订单行分组到服务订单中。</span><span class="sxs-lookup"><span data-stu-id="daaf8-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="daaf8-114">创建服务任务</span><span class="sxs-lookup"><span data-stu-id="daaf8-114">Create a service task</span></span>

1. <span data-ttu-id="daaf8-115">单击**服务管理** \> **设置**\> **服务任务**。</span><span class="sxs-lookup"><span data-stu-id="daaf8-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="daaf8-116">创建新行。</span><span class="sxs-lookup"><span data-stu-id="daaf8-116">Create a new line.</span></span>
3. <span data-ttu-id="daaf8-117">输入服务 ID 和描述。</span><span class="sxs-lookup"><span data-stu-id="daaf8-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="daaf8-118">示例</span><span class="sxs-lookup"><span data-stu-id="daaf8-118">Example</span></span>

<span data-ttu-id="daaf8-119">技术人员必须在客户站点对变速箱（服务对象 GB - 1234）完成两个作业。</span><span class="sxs-lookup"><span data-stu-id="daaf8-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="daaf8-120">为该客户创建了一个服务协议，并且若干交易记录与这两个作业相关联。</span><span class="sxs-lookup"><span data-stu-id="daaf8-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="daaf8-121">这两个作业的服务协议和服务协议行如下：</span><span class="sxs-lookup"><span data-stu-id="daaf8-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="daaf8-122">服务协议</span><span class="sxs-lookup"><span data-stu-id="daaf8-122">Service agreement</span></span>

| <span data-ttu-id="daaf8-123">Project</span><span class="sxs-lookup"><span data-stu-id="daaf8-123">Project</span></span> | <span data-ttu-id="daaf8-124">服务协议</span><span class="sxs-lookup"><span data-stu-id="daaf8-124">Service agreement</span></span> | <span data-ttu-id="daaf8-125">说明</span><span class="sxs-lookup"><span data-stu-id="daaf8-125">Description</span></span>                                  | <span data-ttu-id="daaf8-126">组合</span><span class="sxs-lookup"><span data-stu-id="daaf8-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="daaf8-127">9012</span><span class="sxs-lookup"><span data-stu-id="daaf8-127">9012</span></span>    | <span data-ttu-id="daaf8-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="daaf8-128">000008\_001</span></span>       | <span data-ttu-id="daaf8-129">检查和例行更换 - GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="daaf8-130">津贴</span><span class="sxs-lookup"><span data-stu-id="daaf8-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="daaf8-131">服务协议行</span><span class="sxs-lookup"><span data-stu-id="daaf8-131">Service agreement lines</span></span>

| <span data-ttu-id="daaf8-132"> 描述</span><span class="sxs-lookup"><span data-stu-id="daaf8-132">Description</span></span>             | <span data-ttu-id="daaf8-133">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="daaf8-133">Transaction type</span></span> | <span data-ttu-id="daaf8-134">服务对象</span><span class="sxs-lookup"><span data-stu-id="daaf8-134">Service object</span></span> | <span data-ttu-id="daaf8-135">服务任务</span><span class="sxs-lookup"><span data-stu-id="daaf8-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="daaf8-136">检查和清洁</span><span class="sxs-lookup"><span data-stu-id="daaf8-136">Inspection and cleaning</span></span> | <span data-ttu-id="daaf8-137">工时</span><span class="sxs-lookup"><span data-stu-id="daaf8-137">Hour</span></span>             | <span data-ttu-id="daaf8-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-138">GB-1234</span></span>        | <span data-ttu-id="daaf8-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-139">I/C - GB1234</span></span> |
| <span data-ttu-id="daaf8-140">Travel</span><span class="sxs-lookup"><span data-stu-id="daaf8-140">Travel</span></span>                  | <span data-ttu-id="daaf8-141">Expense</span><span class="sxs-lookup"><span data-stu-id="daaf8-141">Expense</span></span>          | <span data-ttu-id="daaf8-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-142">GB-1234</span></span>        | <span data-ttu-id="daaf8-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-143">I/C - GB1234</span></span> |
| <span data-ttu-id="daaf8-144">物料</span><span class="sxs-lookup"><span data-stu-id="daaf8-144">Materials</span></span>               | <span data-ttu-id="daaf8-145">项目</span><span class="sxs-lookup"><span data-stu-id="daaf8-145">Item</span></span>             | <span data-ttu-id="daaf8-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-146">GB-1234</span></span>        | <span data-ttu-id="daaf8-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-147">I/C - GB1234</span></span> |
| <span data-ttu-id="daaf8-148">例行更换</span><span class="sxs-lookup"><span data-stu-id="daaf8-148">Routine replacement</span></span>     | <span data-ttu-id="daaf8-149">工时</span><span class="sxs-lookup"><span data-stu-id="daaf8-149">Hour</span></span>             | <span data-ttu-id="daaf8-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-150">GB-1234</span></span>        | <span data-ttu-id="daaf8-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-151">RR - GB1234</span></span>  |
| <span data-ttu-id="daaf8-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="daaf8-152">GR-1</span></span>                    | <span data-ttu-id="daaf8-153">项目</span><span class="sxs-lookup"><span data-stu-id="daaf8-153">Item</span></span>             | <span data-ttu-id="daaf8-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-154">GB-1234</span></span>        | <span data-ttu-id="daaf8-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-155">RR - GB1234</span></span>  |
| <span data-ttu-id="daaf8-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="daaf8-156">GR-5</span></span>                    | <span data-ttu-id="daaf8-157">项目</span><span class="sxs-lookup"><span data-stu-id="daaf8-157">Item</span></span>             | <span data-ttu-id="daaf8-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-158">GB-1234</span></span>        | <span data-ttu-id="daaf8-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-159">RR - GB1234</span></span>  |

<span data-ttu-id="daaf8-160">这两个作业的服务协议行附加有两个服务任务。</span><span class="sxs-lookup"><span data-stu-id="daaf8-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="daaf8-161">这两个服务任务确定属于各作业的交易记录。</span><span class="sxs-lookup"><span data-stu-id="daaf8-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="daaf8-162">在第一个情况中，服务任务 I/C - GB1234 标识在对象 GB-1234 的检查和清洁中涉及的所有服务协议行。</span><span class="sxs-lookup"><span data-stu-id="daaf8-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="daaf8-163">在第二个情况中，服务任务 RR - GB1234 标识完成例行更换作业所涉及的所有服务协议行。</span><span class="sxs-lookup"><span data-stu-id="daaf8-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="daaf8-164">将服务任务与特定的协议相关联的服务任务关系如下：</span><span class="sxs-lookup"><span data-stu-id="daaf8-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="daaf8-165">服务任务</span><span class="sxs-lookup"><span data-stu-id="daaf8-165">Service tasks</span></span>

| <span data-ttu-id="daaf8-166">服务任务</span><span class="sxs-lookup"><span data-stu-id="daaf8-166">Service task</span></span> | <span data-ttu-id="daaf8-167">描述</span><span class="sxs-lookup"><span data-stu-id="daaf8-167">Description</span></span>                             | <span data-ttu-id="daaf8-168">内部工作记录</span><span class="sxs-lookup"><span data-stu-id="daaf8-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="daaf8-169">外部工作记录</span><span class="sxs-lookup"><span data-stu-id="daaf8-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="daaf8-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-170">I/C - GB1234</span></span> | <span data-ttu-id="daaf8-171">检查变速箱 GB-1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="daaf8-172">对 GB-1234 变速箱进行视觉和机械检查以及清洁。</span><span class="sxs-lookup"><span data-stu-id="daaf8-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="daaf8-173">例行检查变速箱</span><span class="sxs-lookup"><span data-stu-id="daaf8-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="daaf8-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="daaf8-174">RR - GB1234</span></span>  | <span data-ttu-id="daaf8-175">对 GB-1234 中的零件进行例行更换</span><span class="sxs-lookup"><span data-stu-id="daaf8-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="daaf8-176">对 GR-1 和 GR-5 组件进行例行维修更换（对于在 2002 年前制造的变速箱，还更换 GR-2 组件）</span><span class="sxs-lookup"><span data-stu-id="daaf8-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="daaf8-177">例行零件更换</span><span class="sxs-lookup"><span data-stu-id="daaf8-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="daaf8-178">为服务订单分组</span><span class="sxs-lookup"><span data-stu-id="daaf8-178">Group service orders</span></span>

<span data-ttu-id="daaf8-179">在您自动创建服务订单时，可以将服务任务用作分组条件。</span><span class="sxs-lookup"><span data-stu-id="daaf8-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="daaf8-180">若要按服务任务对服务订单进行分组，请将基于服务协议的服务订单应按服务任务 ID 分组的服务协议定义为其初始分组条件。</span><span class="sxs-lookup"><span data-stu-id="daaf8-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="daaf8-181">**按服务任务分组**</span><span class="sxs-lookup"><span data-stu-id="daaf8-181">**Group by service task**</span></span>

1. <span data-ttu-id="daaf8-182">单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="daaf8-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="daaf8-183">在**设置**选项卡中，选择**合并服务订单**字段中的**按服务任务**。</span><span class="sxs-lookup"><span data-stu-id="daaf8-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>



