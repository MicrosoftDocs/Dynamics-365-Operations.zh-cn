---
title: 下达生产订单
description: 下达的生产订单是已授权进行生产的订单。 “已下达”一词用于描述生产订单生命周期中的状态，在其中，生产订单可用于生产车间和仓库流程的执行。
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc6d53fc87bac2e23c0d1e67954be02749042004
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423276"
---
# <a name="release-production-orders"></a><span data-ttu-id="6f6d2-104">下达生产订单</span><span class="sxs-lookup"><span data-stu-id="6f6d2-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f6d2-105">下达的生产订单是已授权进行生产的订单。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="6f6d2-106">“已下达”一词用于描述生产订单生命周期中的状态，在其中，生产订单可用于生产车间和仓库流程的执行。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="6f6d2-107">“已下达”状态的特征</span><span class="sxs-lookup"><span data-stu-id="6f6d2-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="6f6d2-108">**已下达** 状态为生产订单生命周期的一个状态。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="6f6d2-109">在状态 **下达** 中的生产订单可用于车间中的执行和仓库流程。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="6f6d2-110">**已下达** 状态具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="6f6d2-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="6f6d2-111">生产订单可以从生产订单或通过使用批处理更改为 **已下达** 状态。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="6f6d2-112">生产订单还可以从使用 **主计划** 页的 **确定时限** 字段确定的计划生产订单自动更新。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="6f6d2-113">**已下达** 状态是向车间操作员发出信号以开始在车间执行生产作业。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="6f6d2-114">生产单，例如工艺卡、工艺路线作业和作业卡提供有关生产作业的信息，并且可以分派。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="6f6d2-115">对于实际预留的物料，生成仓库工作以领取生产订单的物料。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="6f6d2-116">将作业下达到车间</span><span class="sxs-lookup"><span data-stu-id="6f6d2-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="6f6d2-117">在下达生产订单后，与该订单相关的生产作业将可见并可供登记。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="6f6d2-118">操作员可为作业登记，例如开始、停止和完成，在 **作业卡终端** 页或 **作业卡设备** 页。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="6f6d2-119">登记的时间和数量将自动从登记页转移到生产日记帐以跟踪所用的时间和数量。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="6f6d2-120">工艺卡</span><span class="sxs-lookup"><span data-stu-id="6f6d2-120">Route cards</span></span>
<span data-ttu-id="6f6d2-121">工艺卡提供来自工艺路线和工序设置以及工序级和作业级排产法的信息的概览。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="6f6d2-122">工艺路线作业</span><span class="sxs-lookup"><span data-stu-id="6f6d2-122">Route jobs</span></span>
<span data-ttu-id="6f6d2-123">工艺路线作业详细列出工序的每个作业，包括设置、处理、排队和运输时间。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="6f6d2-124">例如，喷漆之类的工序可能要求一些单独作业，例如设置时间、运行时间（用于喷漆流程）和排队时间（用于干燥）。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="6f6d2-125">作业卡</span><span class="sxs-lookup"><span data-stu-id="6f6d2-125">Job cards</span></span>
<span data-ttu-id="6f6d2-126">作业卡列出了特定工序的单独作业编号。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="6f6d2-127">每页一个作业。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-127">One job appears on each page.</span></span> <span data-ttu-id="6f6d2-128">在作业卡上包括的作业及其预估时间来自工艺路线和工序设置信息。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="6f6d2-129">从作业卡，您可以打开 **生产日记帐行**，**作业卡** 页。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="6f6d2-130">运行运营资源的人员可提供有关生产流程的反馈。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="6f6d2-131">存在一些您可以输入消耗量统计和信息（例如残次数量）的字段。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="6f6d2-132">物料消耗的仓库工作</span><span class="sxs-lookup"><span data-stu-id="6f6d2-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="6f6d2-133">原材料领料工作在下达期间生成。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="6f6d2-134">工作只为在下达订单前为生产订单实际预留的物料数量生成。</span><span class="sxs-lookup"><span data-stu-id="6f6d2-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="6f6d2-135">为原材料领料生成仓库工作需要以下设置：</span><span class="sxs-lookup"><span data-stu-id="6f6d2-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="6f6d2-136">确定在哪个仓库库位领取物料的原材料领料的库位指令</span><span class="sxs-lookup"><span data-stu-id="6f6d2-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="6f6d2-137">原材料的波次模板，在其中配置执行仓库工作的策略</span><span class="sxs-lookup"><span data-stu-id="6f6d2-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="6f6d2-138">确定物料放入位置的生产输入位置</span><span class="sxs-lookup"><span data-stu-id="6f6d2-138">A production input location that determines where materials are put</span></span>




