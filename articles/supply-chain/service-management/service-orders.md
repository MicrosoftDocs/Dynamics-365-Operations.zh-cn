---
title: 服务订单
description: 服务订单表示服务技术人员在特定日期对某一客户站点的访问。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b049b166edf2b5a318a4b1af85e7f74cfe433f2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975456"
---
# <a name="service-orders"></a><span data-ttu-id="d84c9-103">服务订单</span><span class="sxs-lookup"><span data-stu-id="d84c9-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d84c9-104">服务订单表示服务技术人员在特定日期对某一客户站点的访问。</span><span class="sxs-lookup"><span data-stu-id="d84c9-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="d84c9-105">每个服务订单都由一个或多个服务订单行构成。</span><span class="sxs-lookup"><span data-stu-id="d84c9-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="d84c9-106">服务订单行表示必须由服务技术人员执行的工时和相关物料、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="d84c9-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="d84c9-107">您可以将任务和对象服务订单行。</span><span class="sxs-lookup"><span data-stu-id="d84c9-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="d84c9-108">然后可以对服务订单行按任务或按对象。</span><span class="sxs-lookup"><span data-stu-id="d84c9-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="d84c9-109">您还可以将库存中列出的物料附加到服务订单行。</span><span class="sxs-lookup"><span data-stu-id="d84c9-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="d84c9-110">创建服务订单</span><span class="sxs-lookup"><span data-stu-id="d84c9-110">Create service orders</span></span>

<span data-ttu-id="d84c9-111">您可以创建在该协议包含基于服务协议和行的服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="d84c9-112">但是，您可以创建与某一服务协议只在期间中协议的服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="d84c9-113">例如，如果服务协议，适用于 2011 日历年中，您可以为协议创建服务订单从 2011 年 1 月 1 日和 2011 年 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="d84c9-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="d84c9-114">您可以单独，还创建服务订单，而无需将其与协议。</span><span class="sxs-lookup"><span data-stu-id="d84c9-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="d84c9-115">这些服务订单来处理不定期或一次性服务访问。</span><span class="sxs-lookup"><span data-stu-id="d84c9-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="d84c9-116">在三月，您的客户决定对两台机器以及为服务协议指定的那些机器进行服务。</span><span class="sxs-lookup"><span data-stu-id="d84c9-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="d84c9-117">对于此任务，您创建服务订单，但不将其与协议。</span><span class="sxs-lookup"><span data-stu-id="d84c9-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d84c9-118">若要创建不与服务协议关联的服务订单，必须选中<STRONG>服务管理参数</STRONG>窗体中的<STRONG>允许，但没有服务协议</STRONG>复选框。</span><span class="sxs-lookup"><span data-stu-id="d84c9-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="d84c9-119">**应用场景**</span><span class="sxs-lookup"><span data-stu-id="d84c9-119">**Scenario**</span></span>

<span data-ttu-id="d84c9-120">以下方案描述创建服务订单不与服务协议的其他情况很有用。</span><span class="sxs-lookup"><span data-stu-id="d84c9-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="d84c9-121">公司调度人员接到了一个电话，要求对电梯进行紧急服务。</span><span class="sxs-lookup"><span data-stu-id="d84c9-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="d84c9-122">不时间设置服务协议和服务的一个项目。</span><span class="sxs-lookup"><span data-stu-id="d84c9-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="d84c9-123">因此，调度人员直接在**服务订单**窗体中创建服务订单，将服务订单附加到现有项目，然后创建服务订单行。</span><span class="sxs-lookup"><span data-stu-id="d84c9-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="d84c9-124">您可为现有服务订单创建一个任务或对象关系，以便记录与该服务协议无关的工作 (B)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="d84c9-125">有关详细信息，请参阅[手动创建服务订单](create-service-orders-manually.md)和[创建服务任务关系](create-service-task-relations.md)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="d84c9-126">监控服务订单的进度</span><span class="sxs-lookup"><span data-stu-id="d84c9-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="d84c9-127">您可为服务订单设置阶段系统，以便通过公司中的不同团队和工作流程反映某一服务订单的进度。</span><span class="sxs-lookup"><span data-stu-id="d84c9-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="d84c9-128">对于每个阶段，您可以指定允许的操作。</span><span class="sxs-lookup"><span data-stu-id="d84c9-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="d84c9-129">有关原因代码的详细信息，请参阅[创建原因代码](create-reason-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="d84c9-130">**示例**</span><span class="sxs-lookup"><span data-stu-id="d84c9-130">**Example**</span></span>

<span data-ttu-id="d84c9-131">服务订单都是由该调度审核。</span><span class="sxs-lookup"><span data-stu-id="d84c9-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="d84c9-132">该调度更新服务订单的阶段并指定原因代码指示的服务订单已下达给服务技术人员。</span><span class="sxs-lookup"><span data-stu-id="d84c9-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="d84c9-133">该服务技术人员前往该客户站点并且执行该服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="d84c9-134">为服务订单指定物料需求</span><span class="sxs-lookup"><span data-stu-id="d84c9-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="d84c9-135">您可以指定的服务订单所需的库存物料。</span><span class="sxs-lookup"><span data-stu-id="d84c9-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="d84c9-136">但是，必须将该服务订单与项目。</span><span class="sxs-lookup"><span data-stu-id="d84c9-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="d84c9-137">服务订单创建物料需求通过项目进行处理。</span><span class="sxs-lookup"><span data-stu-id="d84c9-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="d84c9-138">**示例**</span><span class="sxs-lookup"><span data-stu-id="d84c9-138">**Example**</span></span>

<span data-ttu-id="d84c9-139">调度人员然后处理根据该服务协议创建的服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="d84c9-140">在第一个服务订单上，调度人员认识到服务技术人员需要现有库存中没有的一个重要备件。</span><span class="sxs-lookup"><span data-stu-id="d84c9-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="d84c9-141">因此，她直接从服务订单为该备件创建了一个物料需求。</span><span class="sxs-lookup"><span data-stu-id="d84c9-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="d84c9-142">对行进行移动和过帐</span><span class="sxs-lookup"><span data-stu-id="d84c9-142">Move and post lines</span></span>

<span data-ttu-id="d84c9-143">服务技术人员从服务访问返回，然后修改和更新服务订单行。</span><span class="sxs-lookup"><span data-stu-id="d84c9-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="d84c9-144">在服务访问期间，此技术人员执行计划在下一次服务访问的服务工作。</span><span class="sxs-lookup"><span data-stu-id="d84c9-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="d84c9-145">因此，他将这些行从后续服务访问移到当前服务访问 (E)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="d84c9-146">此技术人员然后过帐服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-146">The technician then posts the service order.</span></span> <span data-ttu-id="d84c9-147">有关详细信息，请参阅[移动服务订单行](move-service-order-lines.md)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="d84c9-148">取消服务订单</span><span class="sxs-lookup"><span data-stu-id="d84c9-148">Cancel service orders</span></span>

<span data-ttu-id="d84c9-149">为一月生成的其他服务订单之一已作废，因为该工作已取消。</span><span class="sxs-lookup"><span data-stu-id="d84c9-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="d84c9-150">因此，服务调度人员取消该服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="d84c9-151">有关详细信息，请参阅[取消服务订单](cancel-service-orders.md)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="d84c9-152">从项目过帐</span><span class="sxs-lookup"><span data-stu-id="d84c9-152">Post from projects</span></span>

<span data-ttu-id="d84c9-153">在每周结束时，调度人员想要过帐附加到特定项目的所有服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="d84c9-154">因此，该调度在**项目**窗体中查找相关项目，然后过帐已完成的服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="d84c9-155">有关详细信息，请参阅[过帐服务订单（类窗体）](https://technet.microsoft.com/library/aa574685\(v=ax.60\))。</span><span class="sxs-lookup"><span data-stu-id="d84c9-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="d84c9-156">删除服务订单</span><span class="sxs-lookup"><span data-stu-id="d84c9-156">Delete service orders</span></span>

<span data-ttu-id="d84c9-157">在下半年，您的客户认为服务访问次数过少。</span><span class="sxs-lookup"><span data-stu-id="d84c9-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="d84c9-158">您必须为服务协议的剩余时间创建新的、更频繁的服务访问系列。</span><span class="sxs-lookup"><span data-stu-id="d84c9-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="d84c9-159">因此，您必须删除现有已创建的服务订单并创建新的服务订单。</span><span class="sxs-lookup"><span data-stu-id="d84c9-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="d84c9-160">有关详细信息，请参阅[删除服务订单](delete-service-orders.md)。</span><span class="sxs-lookup"><span data-stu-id="d84c9-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d84c9-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="d84c9-161">See also</span></span>

<span data-ttu-id="d84c9-162">[服务订单（窗体）](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d84c9-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


