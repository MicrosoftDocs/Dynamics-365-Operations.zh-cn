--- 
title: "下达生产订单"
description: "此程序显示了如何发放生产订单。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2ae2d84bd12d338c9bada5518c43178b22112006
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="release-a-production-order"></a><span data-ttu-id="fe5d0-103">下达生产订单</span><span class="sxs-lookup"><span data-stu-id="fe5d0-103">Release a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe5d0-104">此程序显示了如何发放生产订单。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="fe5d0-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fe5d0-106">这是解释生产订单周期七个程序中的第四个程序。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="fe5d0-107">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="fe5d0-108">在网格中，选择具有“已计划”状态的生产订单。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="fe5d0-109">在“操作窗格”中，单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="fe5d0-110">单击“发放”。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-110">Click Release.</span></span>
    * <span data-ttu-id="fe5d0-111">在此页面，您可以确认发放选择的范围的生产订单。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="fe5d0-112">如果您想要添加订单，单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="fe5d0-113">发放步骤指示何时向生产车间发放生产订单，以便车间操作员可以报告生产作业的进度。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="fe5d0-114">可以发放包含有关处理作业的相关信息的生产文件。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="fe5d0-115">对于为仓库流程设置的物料，会生成原材料领料的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="fe5d0-116">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-116">Click the General tab.</span></span>
    * <span data-ttu-id="fe5d0-117">选择应打印的生产报表。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-117">Select which production reports should be printed.</span></span> <span data-ttu-id="fe5d0-118">作业卡报表打印每个已计划作业的页面并要求生产订单按照作业水平进行计划。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="fe5d0-119">报表包含计划开始和结束时间、要生产的数量以及用于处理作业的资源的相关信息。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="fe5d0-120">工艺路线作业报表收集同一页面的相同信息，但是并不会打印每个作业的页面。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="fe5d0-121">工艺卡报表仅显示操作，而不显示作业。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="fe5d0-122">因此，此报表并不要求作业计划，而当生产订单按操作等级计划时可以使用它。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="fe5d0-123">单击“打印工艺卡”复选框。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="fe5d0-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-124">Click OK.</span></span>
7. <span data-ttu-id="fe5d0-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fe5d0-125">Close the page.</span></span>

