---
title: 自动创建服务订单
description: 您可以生成基于服务协议的有效期间的服务协议的服务订单。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824622"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="a8722-103">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="a8722-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a8722-104">您可以生成基于服务协议的有效期间的服务协议的服务订单。</span><span class="sxs-lookup"><span data-stu-id="a8722-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="a8722-105">您基于某一服务协议生成的所有服务订单都附加到此服务协议上。</span><span class="sxs-lookup"><span data-stu-id="a8722-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="a8722-106">服务订单自动根据以下设置生成：</span><span class="sxs-lookup"><span data-stu-id="a8722-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="a8722-107">在服务协议行中设置的服务协议间隔。</span><span class="sxs-lookup"><span data-stu-id="a8722-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="a8722-108">服务协议间隔指示创建服务订单行的频率。</span><span class="sxs-lookup"><span data-stu-id="a8722-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="a8722-109">有关服务间隔的详细信息，请参阅[服务间隔](service-intervals.md)。</span><span class="sxs-lookup"><span data-stu-id="a8722-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="a8722-110">您在 **创建服务订单** 窗体的 **开始日期** 字段和 **结束日期** 字段中为定义服务期间而指定的期间。</span><span class="sxs-lookup"><span data-stu-id="a8722-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="a8722-111">有关如何创建服务订单的详细信息，请参阅[自动创建服务订单](create-service-orders-automatically.md)。</span><span class="sxs-lookup"><span data-stu-id="a8722-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="a8722-112">服务协议标头上的 **合并服务订单** 选项。</span><span class="sxs-lookup"><span data-stu-id="a8722-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="a8722-113">此选项定义是否基于服务协议生成服务订单行，并根据员工、服务任务、服务对象或服务协议合并服务订单。</span><span class="sxs-lookup"><span data-stu-id="a8722-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="a8722-114">有关详细信息，请参阅[合并服务订单](combine-service-orders.md)。</span><span class="sxs-lookup"><span data-stu-id="a8722-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="a8722-115">服务协议行上的 **时间范围** 选项。</span><span class="sxs-lookup"><span data-stu-id="a8722-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="a8722-116">时间范围定义某一服务订单行相对于其计算日期可以移动多远。</span><span class="sxs-lookup"><span data-stu-id="a8722-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="a8722-117">有关时间范围的详细信息，请参阅[时间范围](time-windows.md)。</span><span class="sxs-lookup"><span data-stu-id="a8722-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="a8722-118">如果为某一服务订单指定的日期在您在<STRONG>服务管理参数</STRONG>窗体中选择的日历上未打开，则您将收到一个消息，指示存在日历冲突。</span><span class="sxs-lookup"><span data-stu-id="a8722-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="a8722-119">您可以放心地忽略这一消息；即使该日期在日历上已关闭，仍会创建该服务订单。</span><span class="sxs-lookup"><span data-stu-id="a8722-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="a8722-120">示例 1</span><span class="sxs-lookup"><span data-stu-id="a8722-120">Example 1</span></span>

<span data-ttu-id="a8722-121">此服务协议从 2012 年 1 月 1 日持续到 2012 年 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="a8722-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="a8722-122">如果您在 **创建服务订单** 窗体中指定的服务器为 2012 年 11 月 1 日到 2013 年 2 月 1 日，则从 2012 年 11 月 1 日到 2012 年 12 月 31 日创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="a8722-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="a8722-123">示例 2</span><span class="sxs-lookup"><span data-stu-id="a8722-123">Example 2</span></span>

<span data-ttu-id="a8722-124">此服务协议从 2012 年 1 月 1 日持续到 2012 年 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="a8722-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="a8722-125">将把两个服务协议行附加到此服务协议。</span><span class="sxs-lookup"><span data-stu-id="a8722-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="a8722-126">第一个服务协议行的开始日期为 2012 年 1 月 2 日，结束日期为 2012 年 3 月 1 日。</span><span class="sxs-lookup"><span data-stu-id="a8722-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="a8722-127">第二个服务协议行的开始日期为 2012 年 4 月 2 日，结束日期为 2012 年 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="a8722-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="a8722-128">您将在 **创建服务订单** 窗体中指定一个从 2012 年 10 月 1 日到 2012 年 12 月 31 日的期间。</span><span class="sxs-lookup"><span data-stu-id="a8722-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="a8722-129">因此，只为第二个服务协议行生成服务订单，因为第一个协议行的开始日期和结束日期在您为该服务订单指定的期间之前。</span><span class="sxs-lookup"><span data-stu-id="a8722-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]