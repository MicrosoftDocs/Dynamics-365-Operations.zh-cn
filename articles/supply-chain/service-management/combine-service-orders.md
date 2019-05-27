---
title: 合并服务订单
description: 可以合并服务订单。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571941"
---
# <a name="combine-service-orders"></a><span data-ttu-id="7cc79-103">合并服务订单</span><span class="sxs-lookup"><span data-stu-id="7cc79-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7cc79-104">当您在**服务协议**窗体中自动创建服务订单行时，您可以选择以下选项之一以指定您如何对它们进行分组：</span><span class="sxs-lookup"><span data-stu-id="7cc79-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="7cc79-105">**按服务协议**</span><span class="sxs-lookup"><span data-stu-id="7cc79-105">**By service agreement**</span></span>

  - <span data-ttu-id="7cc79-106">**按服务任务**</span><span class="sxs-lookup"><span data-stu-id="7cc79-106">**By service task**</span></span>

  - <span data-ttu-id="7cc79-107">**按员工**</span><span class="sxs-lookup"><span data-stu-id="7cc79-107">**By employee**</span></span>

  - <span data-ttu-id="7cc79-108">**按服务对象**</span><span class="sxs-lookup"><span data-stu-id="7cc79-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="7cc79-109">示例</span><span class="sxs-lookup"><span data-stu-id="7cc79-109">Example</span></span>

<span data-ttu-id="7cc79-110">您创建了开始日期为 2007 年 3 月 31 日的服务协议。</span><span class="sxs-lookup"><span data-stu-id="7cc79-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="7cc79-111">在**合并服务订单**字段中，指定**按服务对象**。</span><span class="sxs-lookup"><span data-stu-id="7cc79-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="7cc79-112">然后您创建了以下服务协议行：</span><span class="sxs-lookup"><span data-stu-id="7cc79-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cc79-113">协议行号</span><span class="sxs-lookup"><span data-stu-id="7cc79-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="7cc79-114">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="7cc79-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="7cc79-115">说明</span><span class="sxs-lookup"><span data-stu-id="7cc79-115">Description</span></span></p></th>
<th><p><span data-ttu-id="7cc79-116">间期</span><span class="sxs-lookup"><span data-stu-id="7cc79-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="7cc79-117">服务对象</span><span class="sxs-lookup"><span data-stu-id="7cc79-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="7cc79-118">入职日期</span><span class="sxs-lookup"><span data-stu-id="7cc79-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cc79-119">1</span><span class="sxs-lookup"><span data-stu-id="7cc79-119">1</span></span></p></td>
<td><p><span data-ttu-id="7cc79-120"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="7cc79-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="7cc79-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="7cc79-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="7cc79-122">每周</span><span class="sxs-lookup"><span data-stu-id="7cc79-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="7cc79-123">X-1</span><span class="sxs-lookup"><span data-stu-id="7cc79-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="7cc79-124">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="7cc79-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cc79-125">2</span><span class="sxs-lookup"><span data-stu-id="7cc79-125">2</span></span></p></td>
<td><p><span data-ttu-id="7cc79-126"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="7cc79-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="7cc79-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="7cc79-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="7cc79-128">每两周</span><span class="sxs-lookup"><span data-stu-id="7cc79-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="7cc79-129">X-2</span><span class="sxs-lookup"><span data-stu-id="7cc79-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="7cc79-130">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="7cc79-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cc79-131">3</span><span class="sxs-lookup"><span data-stu-id="7cc79-131">3</span></span></p></td>
<td><p><span data-ttu-id="7cc79-132"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="7cc79-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="7cc79-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="7cc79-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="7cc79-134">每周</span><span class="sxs-lookup"><span data-stu-id="7cc79-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="7cc79-135">X-2</span><span class="sxs-lookup"><span data-stu-id="7cc79-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="7cc79-136">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="7cc79-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7cc79-137">您未指定任何服务协议行的时间范围。</span><span class="sxs-lookup"><span data-stu-id="7cc79-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="7cc79-138">因此，服务订单行将不从它们所在的计算日移动。</span><span class="sxs-lookup"><span data-stu-id="7cc79-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="7cc79-139">接着，您从**创建服务订单**窗体生成了从 2007 年 4 月 1 日到 2007 年 4 月 30 日的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="7cc79-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="7cc79-140">总共创建了 10 个服务订单。</span><span class="sxs-lookup"><span data-stu-id="7cc79-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="7cc79-141">因为您选择的组合设置为**按服务对象**，创建的所有服务订单将只包含具有一个特定服务对象的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="7cc79-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="7cc79-142">从该服务协议生成并具有相同服务日期和对象的服务订单行被组合为同一个服务订单。</span><span class="sxs-lookup"><span data-stu-id="7cc79-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7cc79-143">在此示例中，在<STRONG>服务管理参数</STRONG>窗体中指定的日历没有休息日。</span><span class="sxs-lookup"><span data-stu-id="7cc79-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="7cc79-144">可以根据您在服务协议行上指定的任意时间范围将服务订单行的附加组合为服务订单。</span><span class="sxs-lookup"><span data-stu-id="7cc79-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc79-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="7cc79-145">See also</span></span>

[<span data-ttu-id="7cc79-146">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="7cc79-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


