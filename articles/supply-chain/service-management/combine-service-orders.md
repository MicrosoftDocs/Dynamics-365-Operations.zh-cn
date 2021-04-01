---
title: 合并服务订单
description: 可以合并服务订单。
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
ms.openlocfilehash: 7bd3ac8cf3c025b082b33247fcd020aebc010bc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247710"
---
# <a name="combine-service-orders"></a><span data-ttu-id="f3f73-103">合并服务订单</span><span class="sxs-lookup"><span data-stu-id="f3f73-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f3f73-104">当您在 **服务协议** 窗体中自动创建服务订单行时，您可以选择以下选项之一以指定您如何对它们进行分组：</span><span class="sxs-lookup"><span data-stu-id="f3f73-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="f3f73-105">**按服务协议**</span><span class="sxs-lookup"><span data-stu-id="f3f73-105">**By service agreement**</span></span>

  - <span data-ttu-id="f3f73-106">**按服务任务**</span><span class="sxs-lookup"><span data-stu-id="f3f73-106">**By service task**</span></span>

  - <span data-ttu-id="f3f73-107">**按员工**</span><span class="sxs-lookup"><span data-stu-id="f3f73-107">**By employee**</span></span>

  - <span data-ttu-id="f3f73-108">**按服务对象**</span><span class="sxs-lookup"><span data-stu-id="f3f73-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="f3f73-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3f73-109">Example</span></span>

<span data-ttu-id="f3f73-110">您创建了开始日期为 2007 年 3 月 31 日的服务协议。</span><span class="sxs-lookup"><span data-stu-id="f3f73-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="f3f73-111">在 **合并服务订单** 字段中，指定 **按服务对象**。</span><span class="sxs-lookup"><span data-stu-id="f3f73-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="f3f73-112">然后您创建了以下服务协议行：</span><span class="sxs-lookup"><span data-stu-id="f3f73-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="f3f73-113">协议行号</span><span class="sxs-lookup"><span data-stu-id="f3f73-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="f3f73-114">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="f3f73-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="f3f73-115">说明</span><span class="sxs-lookup"><span data-stu-id="f3f73-115">Description</span></span></p></th>
<th><p><span data-ttu-id="f3f73-116">间期</span><span class="sxs-lookup"><span data-stu-id="f3f73-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="f3f73-117">服务对象</span><span class="sxs-lookup"><span data-stu-id="f3f73-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="f3f73-118">入职日期</span><span class="sxs-lookup"><span data-stu-id="f3f73-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3f73-119">1</span><span class="sxs-lookup"><span data-stu-id="f3f73-119">1</span></span></p></td>
<td><p><span data-ttu-id="f3f73-120"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="f3f73-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="f3f73-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="f3f73-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="f3f73-122">每周</span><span class="sxs-lookup"><span data-stu-id="f3f73-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="f3f73-123">X-1</span><span class="sxs-lookup"><span data-stu-id="f3f73-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="f3f73-124">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="f3f73-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3f73-125">2</span><span class="sxs-lookup"><span data-stu-id="f3f73-125">2</span></span></p></td>
<td><p><span data-ttu-id="f3f73-126"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="f3f73-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="f3f73-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="f3f73-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="f3f73-128">每两周</span><span class="sxs-lookup"><span data-stu-id="f3f73-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="f3f73-129">X-2</span><span class="sxs-lookup"><span data-stu-id="f3f73-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="f3f73-130">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="f3f73-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3f73-131">3</span><span class="sxs-lookup"><span data-stu-id="f3f73-131">3</span></span></p></td>
<td><p><span data-ttu-id="f3f73-132"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="f3f73-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="f3f73-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="f3f73-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="f3f73-134">每周</span><span class="sxs-lookup"><span data-stu-id="f3f73-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="f3f73-135">X-2</span><span class="sxs-lookup"><span data-stu-id="f3f73-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="f3f73-136">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="f3f73-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3f73-137">您未指定任何服务协议行的时间范围。</span><span class="sxs-lookup"><span data-stu-id="f3f73-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="f3f73-138">因此，服务订单行将不从它们所在的计算日移动。</span><span class="sxs-lookup"><span data-stu-id="f3f73-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="f3f73-139">接着，您从 **创建服务订单** 窗体生成了从 2007 年 4 月 1 日到 2007 年 4 月 30 日的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="f3f73-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="f3f73-140">总共创建了 10 个服务订单。</span><span class="sxs-lookup"><span data-stu-id="f3f73-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="f3f73-141">因为您选择的组合设置为 **按服务对象**，创建的所有服务订单将只包含具有一个特定服务对象的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="f3f73-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="f3f73-142">从该服务协议生成并具有相同服务日期和对象的服务订单行被组合为同一个服务订单。</span><span class="sxs-lookup"><span data-stu-id="f3f73-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f3f73-143">在此示例中，在<STRONG>服务管理参数</STRONG>窗体中指定的日历没有休息日。</span><span class="sxs-lookup"><span data-stu-id="f3f73-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="f3f73-144">可以根据您在服务协议行上指定的任意时间范围将服务订单行的附加组合为服务订单。</span><span class="sxs-lookup"><span data-stu-id="f3f73-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3f73-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="f3f73-145">See also</span></span>

[<span data-ttu-id="f3f73-146">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="f3f73-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]