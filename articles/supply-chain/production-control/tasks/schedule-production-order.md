---
title: 计划生产订单
description: 该过程说明安排一个生产订单。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a52e2ee3bf0c5dadeda375882d16de60b31d658
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831882"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="91e9b-103">计划生产订单</span><span class="sxs-lookup"><span data-stu-id="91e9b-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91e9b-104">该过程说明安排一个生产订单。</span><span class="sxs-lookup"><span data-stu-id="91e9b-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="91e9b-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="91e9b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91e9b-106">这是生产订单循环周期七个程序中的第三个。</span><span class="sxs-lookup"><span data-stu-id="91e9b-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="91e9b-107">计划生产订单</span><span class="sxs-lookup"><span data-stu-id="91e9b-107">Schedule a production order</span></span>
1. <span data-ttu-id="91e9b-108">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="91e9b-109">选择具有“预估”状态的一个生产订单。</span><span class="sxs-lookup"><span data-stu-id="91e9b-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="91e9b-110">在“操作窗格”上，单击“计划” 。</span><span class="sxs-lookup"><span data-stu-id="91e9b-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="91e9b-111">单击“计划作业”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="91e9b-112">此页用于设置计划参数。</span><span class="sxs-lookup"><span data-stu-id="91e9b-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="91e9b-113">可以设置为特定用户或所有用户参数。</span><span class="sxs-lookup"><span data-stu-id="91e9b-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="91e9b-114">在“计划的方向”字段中，选择“从今天开始”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="91e9b-115">在“计划日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="91e9b-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="91e9b-116">选择或取消选择“有限产能”复选框。</span><span class="sxs-lookup"><span data-stu-id="91e9b-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="91e9b-117">选择或取消选择“有限物料”复选框。</span><span class="sxs-lookup"><span data-stu-id="91e9b-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="91e9b-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="91e9b-119">查看计划结果</span><span class="sxs-lookup"><span data-stu-id="91e9b-119">View the scheduling results</span></span>
1. <span data-ttu-id="91e9b-120">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="91e9b-121">单击“所有作业”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-121">Click All jobs.</span></span>
    * <span data-ttu-id="91e9b-122">此页显示的是您刚刚生成的计划作业。</span><span class="sxs-lookup"><span data-stu-id="91e9b-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="91e9b-123">展开或折叠“计划”部分。</span><span class="sxs-lookup"><span data-stu-id="91e9b-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="91e9b-124">通过“计划”快速选项卡，可以查看计划的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="91e9b-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="91e9b-125">单击“查询”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-125">Click Inquiries.</span></span>
5. <span data-ttu-id="91e9b-126">单击“产能负荷”。</span><span class="sxs-lookup"><span data-stu-id="91e9b-126">Click Capacity load.</span></span>
    * <span data-ttu-id="91e9b-127">该“产能负荷”页显示计划作业的预留产能，当前可用的预留总工时数，以及计划作业仍可用工时数。</span><span class="sxs-lookup"><span data-stu-id="91e9b-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="91e9b-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91e9b-128">Close the page.</span></span>
7. <span data-ttu-id="91e9b-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91e9b-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]