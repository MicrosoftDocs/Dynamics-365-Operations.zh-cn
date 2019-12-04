---
title: 维护计划订单
description: 本主题提供有关如何管理计划订单的信息。 介绍如何更新计划订单的状态，确定计划订单，并筛选与所选计划订单具有相同状态的计划订单。
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813768"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="827a7-104">维护计划订单</span><span class="sxs-lookup"><span data-stu-id="827a7-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="827a7-105">本主题提供有关如何管理计划订单的信息。</span><span class="sxs-lookup"><span data-stu-id="827a7-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="827a7-106">介绍如何更新计划订单的状态，确定计划订单，并筛选与所选计划订单具有相同状态的计划订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="827a7-107">您可以从**主计划**工作区、**计划订单**列表或**计划生产订单**、**计划采购订单**和**计划转移**列表中管理计划订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="827a7-108">计划订单状态</span><span class="sxs-lookup"><span data-stu-id="827a7-108">Planned order status</span></span>
<span data-ttu-id="827a7-109">您可以使用**状态**字段帮助跟踪您的进度。</span><span class="sxs-lookup"><span data-stu-id="827a7-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="827a7-110">使用了以下值：</span><span class="sxs-lookup"><span data-stu-id="827a7-110">The following values are used:</span></span>

-   <span data-ttu-id="827a7-111">当主计划生成计划订单时，该计划订单状态为**未处理**。</span><span class="sxs-lookup"><span data-stu-id="827a7-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="827a7-112">如果您决定不确认某一计划订单，则可以给予其状态**已完成**。</span><span class="sxs-lookup"><span data-stu-id="827a7-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="827a7-113">如果要确认计划订单，可将状态更改为**已审核**。</span><span class="sxs-lookup"><span data-stu-id="827a7-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="827a7-114">主计划会考虑状态为**已审核**的计划订单，所以不会在随后的主计划运行期间修改或删除这些订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="827a7-115">确认计划订单</span><span class="sxs-lookup"><span data-stu-id="827a7-115">Firming planned orders</span></span> 
<span data-ttu-id="827a7-116">确认计划订单即创建实际订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="827a7-117">这些也称为*已下达订单*或*未结订单*。</span><span class="sxs-lookup"><span data-stu-id="827a7-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="827a7-118">确认计划订单时，该订单将移至相关模块的订单部分。</span><span class="sxs-lookup"><span data-stu-id="827a7-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="827a7-119">可以从**计划订单**页选择两个确认选项：</span><span class="sxs-lookup"><span data-stu-id="827a7-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="827a7-120">**确认** – 这将确认选择的一个或多个计划订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="827a7-121">**全部确认** – 这将确认筛选器中的所有计划订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="827a7-122">如果使用**全部确认**，则不必选择计划订单，因为将确认筛选器中的所有计划订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="827a7-123">如果要确认大量计划订单，此选项非常有用。</span><span class="sxs-lookup"><span data-stu-id="827a7-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="827a7-124">可从**计划订单窗体 > 视图 > 确认历史记录**下的**确认历史记录**跟踪已确认的计划订单。</span><span class="sxs-lookup"><span data-stu-id="827a7-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="827a7-125">并行确认</span><span class="sxs-lookup"><span data-stu-id="827a7-125">Parallelize firming</span></span>
<span data-ttu-id="827a7-126">如果计划同时确认大量订单，并行化运行可改善运行时间或性能。</span><span class="sxs-lookup"><span data-stu-id="827a7-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="827a7-127">在使用**确认**或**全部确认**确认多个计划订单时，可以使用此选项。</span><span class="sxs-lookup"><span data-stu-id="827a7-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="827a7-128">提供了以下参数：</span><span class="sxs-lookup"><span data-stu-id="827a7-128">The following parameters are available:</span></span>

-   <span data-ttu-id="827a7-129">**并行确认** – 如果设置为**是**，则使用**线程数**中定义的线程数并行化确认流程。</span><span class="sxs-lookup"><span data-stu-id="827a7-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="827a7-130">**线程数** – 控制用于并行化确认流程的线程的数量。</span><span class="sxs-lookup"><span data-stu-id="827a7-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="827a7-131">仅当**并行确认**设置为**是**时，才显示此参数。</span><span class="sxs-lookup"><span data-stu-id="827a7-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="827a7-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="827a7-132">Additional resources</span></span>
--------

[<span data-ttu-id="827a7-133">主计划概览</span><span class="sxs-lookup"><span data-stu-id="827a7-133">Master plans overview</span></span>](master-plans.md)



