---
title: 服务状态和进度字段交互
description: 在“服务订单”窗体中，标题上的“进度”字段反映整个服务订单的状态，而“状态”报告各个服务订单行的状态。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66871d07bdfd949e29a704f53b3e5698d996c2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254207"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="92ec2-103">服务状态和进度字段交互</span><span class="sxs-lookup"><span data-stu-id="92ec2-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="92ec2-104">在 **服务订单** 窗体中，服务订单标题上的 **进度** 字段反映整个服务订单的状态，而 **状态** 报告各个服务订单行的状态。</span><span class="sxs-lookup"><span data-stu-id="92ec2-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92ec2-105">进度</span><span class="sxs-lookup"><span data-stu-id="92ec2-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="92ec2-106">行 1 状态</span><span class="sxs-lookup"><span data-stu-id="92ec2-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="92ec2-107">行 2 状态</span><span class="sxs-lookup"><span data-stu-id="92ec2-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="92ec2-108">行 3 状态</span><span class="sxs-lookup"><span data-stu-id="92ec2-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92ec2-109"><strong>进行中</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-110"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-111"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-112"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92ec2-113"><strong>进行中</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-114"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-115"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-116"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92ec2-117"><strong>进行中</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-118"><strong>已创建</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-119"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-120"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92ec2-121"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-122"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-123"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-124"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92ec2-125"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-126"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-127"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-128"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92ec2-129"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-130"><strong>已过帐</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-131"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92ec2-132"><strong>已取消</strong></span><span class="sxs-lookup"><span data-stu-id="92ec2-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92ec2-133">如果所有行都具有 **已创建** 状态，则服务订单的进度为进行中。如果有些行具有 **已取消** 状态或 **已过帐** 状态，则其进度仍为进行中。</span><span class="sxs-lookup"><span data-stu-id="92ec2-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="92ec2-134">如果服务订单中的所有行都标记为 **已过帐**，则状态订单的进度为 **已过帐**。</span><span class="sxs-lookup"><span data-stu-id="92ec2-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="92ec2-135">如果有些行的状态为 **已过帐**，而有些行的状态为 **已取消**，则进度仍为 **已过帐**。</span><span class="sxs-lookup"><span data-stu-id="92ec2-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]