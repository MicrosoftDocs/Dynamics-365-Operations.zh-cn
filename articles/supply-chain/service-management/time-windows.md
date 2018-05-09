---
title: "时间范围"
description: "您可以使用时间范围优化服务订单行的计划。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
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
ms.openlocfilehash: a537c2491f2540e48b6ccdccaee11b4fa8b208d9
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="time-windows"></a><span data-ttu-id="06901-103">时间范围</span><span class="sxs-lookup"><span data-stu-id="06901-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06901-104">您可以使用时间范围优化服务订单行的计划。</span><span class="sxs-lookup"><span data-stu-id="06901-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="06901-105">您可以设置系统，以便自动创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="06901-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="06901-106">基于时间范围指定的条件，您可以将尽可能多的服务订单行连接到尽可能少的服务订单。</span><span class="sxs-lookup"><span data-stu-id="06901-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="06901-107">时间范围指定某一服务订单行从其计算日期中可以移动多远。</span><span class="sxs-lookup"><span data-stu-id="06901-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="06901-108">在计划发生服务订单行时，计算日期为日期。</span><span class="sxs-lookup"><span data-stu-id="06901-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="06901-109">该日期基于其间隔设置和您在**创建服务订单**页面中定义的服务期间。</span><span class="sxs-lookup"><span data-stu-id="06901-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="06901-110">您使用以下表中的值定义时间范围：</span><span class="sxs-lookup"><span data-stu-id="06901-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="06901-111">方法</span><span class="sxs-lookup"><span data-stu-id="06901-111">Method</span></span> | <span data-ttu-id="06901-112">说明</span><span class="sxs-lookup"><span data-stu-id="06901-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06901-113">周</span><span class="sxs-lookup"><span data-stu-id="06901-113">Week</span></span>   | <span data-ttu-id="06901-114">服务订单行可以移到与初始计算日期处于同一周内的任何开放日期的日期。</span><span class="sxs-lookup"><span data-stu-id="06901-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="06901-115">月</span><span class="sxs-lookup"><span data-stu-id="06901-115">Month</span></span>  | <span data-ttu-id="06901-116">服务订单行可以移到与初始计算日期处于同一月内的任何开放日期的日期。</span><span class="sxs-lookup"><span data-stu-id="06901-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="06901-117">例如，一个服务订单行的计算日期为 2017 年 2 月 15 日。</span><span class="sxs-lookup"><span data-stu-id="06901-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="06901-118">可将该服务订单行安排到 2017 年 2 月 1 日到 2 月 28 日之间的任何一个工作日。</span><span class="sxs-lookup"><span data-stu-id="06901-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="06901-119">手动</span><span class="sxs-lookup"><span data-stu-id="06901-119">Manual</span></span> | <span data-ttu-id="06901-120">您定义服务订单行可移动的最初计算日期之前或之后的最大天数。</span><span class="sxs-lookup"><span data-stu-id="06901-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="06901-121">如果没有为某一服务协议行指定时间范围，则从该服务协议派生的服务订单行必须就在最初计划的那一日期执行。</span><span class="sxs-lookup"><span data-stu-id="06901-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06901-122">相关主题</span><span class="sxs-lookup"><span data-stu-id="06901-122">Related topics</span></span>

[<span data-ttu-id="06901-123">创建时间范围</span><span class="sxs-lookup"><span data-stu-id="06901-123">Create time windows</span></span>](create-time-windows.md)


