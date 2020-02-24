---
title: 设置呼叫中心的连续性计划
description: 本文介绍如何为呼叫中心设置连续性计划。
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 738841407b63ef604da092b7c8f4d0f2064d3886
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021758"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="f4671-103">设置呼叫中心的连续性计划</span><span class="sxs-lookup"><span data-stu-id="f4671-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4671-104">本文介绍如何为呼叫中心设置连续性计划。</span><span class="sxs-lookup"><span data-stu-id="f4671-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="f4671-105">在连续性计划中，也被称作重复执行订单计划，客户根据预定义的计划收货常规产品装运。</span><span class="sxs-lookup"><span data-stu-id="f4671-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="f4671-106">每个装运可以包含不同的产品，如在每月一书俱乐部或相同产品可以重复发送的情况下。</span><span class="sxs-lookup"><span data-stu-id="f4671-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="f4671-107">若要设置连续性计划，必须完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="f4671-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="f4671-108">在**呼叫中心参数**页设置连续性参数。</span><span class="sxs-lookup"><span data-stu-id="f4671-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="f4671-109">创建指定详细信息的连续性计划，如付款计划、装运的时间和是否提前记帐。</span><span class="sxs-lookup"><span data-stu-id="f4671-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="f4671-110">还必须添加连续性计划中所包含的产品列表。</span><span class="sxs-lookup"><span data-stu-id="f4671-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="f4671-111">每个产品接收一个从 1 开始的连续分配的事件 ID 编号。</span><span class="sxs-lookup"><span data-stu-id="f4671-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="f4671-112">事件 ID 决定产品发送的顺序。</span><span class="sxs-lookup"><span data-stu-id="f4671-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="f4671-113">如果客户在每个装运接收不同产品，产品从当前事件开始基于其事件 ID 按连续顺序发送。</span><span class="sxs-lookup"><span data-stu-id="f4671-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="f4671-114">如果客户在每个装运接收相同产品，列表仅包含一个有事件 ID 的产品。</span><span class="sxs-lookup"><span data-stu-id="f4671-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="f4671-115">且相同事件重复发生。</span><span class="sxs-lookup"><span data-stu-id="f4671-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="f4671-116">可以指定每个事件重复的次数。</span><span class="sxs-lookup"><span data-stu-id="f4671-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="f4671-117">创建父产品来表示在任务 2 中创建的连续性计划。</span><span class="sxs-lookup"><span data-stu-id="f4671-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="f4671-118">如果添加此产品到销售订单，则**连续性**页打开。</span><span class="sxs-lookup"><span data-stu-id="f4671-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="f4671-119">然后可以使用此页创建实际的连续性订单。</span><span class="sxs-lookup"><span data-stu-id="f4671-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="f4671-120">父产品不指定该客户在每个装运中接收的单独产品。</span><span class="sxs-lookup"><span data-stu-id="f4671-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="f4671-121">在您按照上述说明设置了继续订货之后，您可以为客户创建一个连续性订单。</span><span class="sxs-lookup"><span data-stu-id="f4671-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="f4671-122">您也需不得不执行以下这些额外的维护任务。</span><span class="sxs-lookup"><span data-stu-id="f4671-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="f4671-123">**更新当前连续性事件期间** – 设置告知系统当前事件期间是什么的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="f4671-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="f4671-124">**创建连续性子订单** – 创建父连续性订单的子订单。</span><span class="sxs-lookup"><span data-stu-id="f4671-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="f4671-125">**处理连续性付款** – 处理与连续性销售订单关联的帐单和通知。</span><span class="sxs-lookup"><span data-stu-id="f4671-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="f4671-126">**扩展连续性行**（如果要求）– 扩展连续性事件可重复的次数。</span><span class="sxs-lookup"><span data-stu-id="f4671-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="f4671-127">重复装运可能超过在呼叫中心参数的**连续性重复阈值**字段中设置的限制。</span><span class="sxs-lookup"><span data-stu-id="f4671-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="f4671-128">**执行连续性更新**（如果要求）– 同步连续性计划和连续性父销售订单之间的更改。</span><span class="sxs-lookup"><span data-stu-id="f4671-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="f4671-129">**关闭连续性父行和父订单** – 关闭连续性订单。</span><span class="sxs-lookup"><span data-stu-id="f4671-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>
