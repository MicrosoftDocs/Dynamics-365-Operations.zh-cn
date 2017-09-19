--- 
title: "创建站点计划"
description: "生产规划人员计算特定物料生产的物料和产能需求。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="4a6cd-103">创建站点计划</span><span class="sxs-lookup"><span data-stu-id="4a6cd-103">Create a plan for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a6cd-104">生产规划人员计算特定物料生产的物料和产能需求。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="4a6cd-105">在采购建议创建后，他在计划的站点查找订单并确认订单，从最紧急的订单开始。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="4a6cd-106">最紧急的订单是需要在当前日期确定的订单。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="4a6cd-107">使用演示数据公司 USMF 执行这些任务。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="4a6cd-108">创建物料的物料和产能计划</span><span class="sxs-lookup"><span data-stu-id="4a6cd-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="4a6cd-109">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-109">Click Master planning.</span></span>
    * <span data-ttu-id="4a6cd-110">您需要导航到默认仪表板。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="4a6cd-111">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-111">Click Run.</span></span>
3. <span data-ttu-id="4a6cd-112">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="4a6cd-113">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-113">Click Filter.</span></span>
5. <span data-ttu-id="4a6cd-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4a6cd-115">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="4a6cd-116">例子： D0001</span><span class="sxs-lookup"><span data-stu-id="4a6cd-116">Example: D0001</span></span>  
7. <span data-ttu-id="4a6cd-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-117">Click OK.</span></span>
8. <span data-ttu-id="4a6cd-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-118">Click OK.</span></span>
    * <span data-ttu-id="4a6cd-119">这可能需要几分钟的时间。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="4a6cd-120">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="4a6cd-121">确定物料的紧急计划订单</span><span class="sxs-lookup"><span data-stu-id="4a6cd-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="4a6cd-122">打开“物料编号列”筛选器。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="4a6cd-123">在“物料编号”字段中安装一个筛选器，输入值“D0001”，点击筛选器操作键“开始”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="4a6cd-124">打开订单日期列筛选器。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="4a6cd-125">在“订单日期”字段中应用筛选器（具有当前日期值），使用“正好是”筛选器运算符。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="4a6cd-126">确定物料的所有紧急订单</span><span class="sxs-lookup"><span data-stu-id="4a6cd-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="4a6cd-127">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="4a6cd-128">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-128">Click Firm.</span></span>
3. <span data-ttu-id="4a6cd-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4a6cd-129">Click OK.</span></span>

