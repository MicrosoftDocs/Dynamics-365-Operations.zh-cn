---
title: "结束生产订单"
description: "该过程显示如何结束生产订单。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9cb20294e4abbccd0016e7188a2610796e75b26
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="end-a-production-order"></a><span data-ttu-id="84aee-103">结束生产订单</span><span class="sxs-lookup"><span data-stu-id="84aee-103">End a production order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84aee-104">该过程显示如何结束生产订单。</span><span class="sxs-lookup"><span data-stu-id="84aee-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="84aee-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="84aee-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="84aee-106">这是解释生产订单周期的七个步骤中的最后一步。</span><span class="sxs-lookup"><span data-stu-id="84aee-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="84aee-107">结束生产订单</span><span class="sxs-lookup"><span data-stu-id="84aee-107">End a production order</span></span>
1. <span data-ttu-id="84aee-108">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="84aee-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="84aee-109">选择状态“报告”为完工的生产订单。</span><span class="sxs-lookup"><span data-stu-id="84aee-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="84aee-110">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="84aee-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="84aee-111">单击“结束”。</span><span class="sxs-lookup"><span data-stu-id="84aee-111">Click End.</span></span>
    * <span data-ttu-id="84aee-112">在此页，您可以确认您是否想结束生产订单。</span><span class="sxs-lookup"><span data-stu-id="84aee-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="84aee-113">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="84aee-113">Click the General tab.</span></span>
5. <span data-ttu-id="84aee-114">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="84aee-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="84aee-115">在“报废方法”字段中，选择“分配”。</span><span class="sxs-lookup"><span data-stu-id="84aee-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="84aee-116">当您选择“分配方法”时，报废物料的成本将添加到成品中。</span><span class="sxs-lookup"><span data-stu-id="84aee-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="84aee-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="84aee-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="84aee-118">验证计算结果</span><span class="sxs-lookup"><span data-stu-id="84aee-118">Validate calculation results</span></span>
1. <span data-ttu-id="84aee-119">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="84aee-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="84aee-120">单击“查看成本比较”。</span><span class="sxs-lookup"><span data-stu-id="84aee-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="84aee-121">在结束生产订单后，可以将已实现的成本价与估计成本对比获得生产差异概览。</span><span class="sxs-lookup"><span data-stu-id="84aee-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  

