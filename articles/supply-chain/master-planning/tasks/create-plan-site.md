---
title: 创建站点计划
description: 生产规划人员计算特定物料生产的物料和产能需求。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d84fcd0012d4f7d87e2bc0769261fbe5f5139670
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102654"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="4f91a-103">创建站点计划</span><span class="sxs-lookup"><span data-stu-id="4f91a-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f91a-104">生产规划人员计算特定物料生产的物料和产能需求。</span><span class="sxs-lookup"><span data-stu-id="4f91a-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="4f91a-105">在采购建议创建后，他在计划的站点查找订单并确认订单，从最紧急的订单开始。</span><span class="sxs-lookup"><span data-stu-id="4f91a-105">After the sourcing suggestions are created, they find the orders at the site for which they are planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="4f91a-106">最紧急的订单是需要在当前日期确定的订单。</span><span class="sxs-lookup"><span data-stu-id="4f91a-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="4f91a-107">使用演示数据公司 USMF 执行这些任务。</span><span class="sxs-lookup"><span data-stu-id="4f91a-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="4f91a-108">创建物料的物料和产能计划</span><span class="sxs-lookup"><span data-stu-id="4f91a-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="4f91a-109">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-109">Click Master planning.</span></span>
    * <span data-ttu-id="4f91a-110">您需要导航到默认仪表板。</span><span class="sxs-lookup"><span data-stu-id="4f91a-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="4f91a-111">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-111">Click Run.</span></span>
3. <span data-ttu-id="4f91a-112">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="4f91a-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="4f91a-113">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-113">Click Filter.</span></span>
5. <span data-ttu-id="4f91a-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4f91a-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4f91a-115">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="4f91a-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="4f91a-116">例子： D0001</span><span class="sxs-lookup"><span data-stu-id="4f91a-116">Example: D0001</span></span>  
7. <span data-ttu-id="4f91a-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-117">Click OK.</span></span>
8. <span data-ttu-id="4f91a-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-118">Click OK.</span></span>
    * <span data-ttu-id="4f91a-119">这可能需要几分钟的时间。</span><span class="sxs-lookup"><span data-stu-id="4f91a-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="4f91a-120">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="4f91a-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="4f91a-121">确定物料的紧急计划订单</span><span class="sxs-lookup"><span data-stu-id="4f91a-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="4f91a-122">打开“物料编号列”筛选器。</span><span class="sxs-lookup"><span data-stu-id="4f91a-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="4f91a-123">在“物料编号”字段中安装一个筛选器，输入值“D0001”，点击筛选器操作键“开始”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="4f91a-124">打开订单日期列筛选器。</span><span class="sxs-lookup"><span data-stu-id="4f91a-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="4f91a-125">在“订单日期”字段中应用筛选器（具有当前日期值），使用“正好是”筛选器运算符。</span><span class="sxs-lookup"><span data-stu-id="4f91a-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="4f91a-126">确定物料的所有紧急订单</span><span class="sxs-lookup"><span data-stu-id="4f91a-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="4f91a-127">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="4f91a-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="4f91a-128">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-128">Click Firm.</span></span>
3. <span data-ttu-id="4f91a-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4f91a-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]