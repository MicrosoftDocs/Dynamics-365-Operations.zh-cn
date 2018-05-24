---
title: "服务状态和进度字段交互"
description: "在“服务订单”窗体中，标题上的“进度”字段反映整个服务订单的状态，而“状态”报告各个服务订单行的状态。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51ef39266e8de00488954918568d00a297a9b50a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---


# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="a8817-103">服务状态和进度字段交互</span><span class="sxs-lookup"><span data-stu-id="a8817-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a8817-104">在**服务订单**窗体中，服务订单标题上的**进度**字段反映整个服务订单的状态，而**状态**报告各个服务订单行的状态。</span><span class="sxs-lookup"><span data-stu-id="a8817-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8817-105">进度</span><span class="sxs-lookup"><span data-stu-id="a8817-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="a8817-106">行 1 状态</span><span class="sxs-lookup"><span data-stu-id="a8817-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="a8817-107">行 2 状态</span><span class="sxs-lookup"><span data-stu-id="a8817-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="a8817-108">行 3 状态</span><span class="sxs-lookup"><span data-stu-id="a8817-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8817-109"><strong>进行中</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-110"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-111"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-112"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8817-113"><strong>进行中</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-114"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-115"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-116"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8817-117"><strong>进行中</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-118"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-119"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-120"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8817-121"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-122"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-123"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-124"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8817-125"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-126"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-127"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-128"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8817-129"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-130"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-131"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a8817-132"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="a8817-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8817-133">如果所有行都具有**已创建**状态，则服务订单的进度为进行中。如果有些行具有**已取消**状态或**已过帐**状态，则其进度仍为进行中。</span><span class="sxs-lookup"><span data-stu-id="a8817-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="a8817-134">如果服务订单中的所有行都标记为**已过帐**，则状态订单的进度为**已过帐**。</span><span class="sxs-lookup"><span data-stu-id="a8817-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="a8817-135">如果有些行的状态为**已过帐**，而有些行的状态为**已取消**，则进度仍为**已过帐**。</span><span class="sxs-lookup"><span data-stu-id="a8817-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  



