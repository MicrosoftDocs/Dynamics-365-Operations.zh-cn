--- 
title: "创建日历和生成工作时间"
description: "日历描述运营资源的产能和工作时间。"
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a8dcef8d8ba6f6d41a997b5b0623cb9577ce00d3
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="0c655-103">创建日历和生成工作时间</span><span class="sxs-lookup"><span data-stu-id="0c655-103">Create a calendar and generate working times</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c655-104">日历描述运营资源的产能和工作时间。</span><span class="sxs-lookup"><span data-stu-id="0c655-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="0c655-105">该过程将帮助您定义基于工作时间模板的工作日历。</span><span class="sxs-lookup"><span data-stu-id="0c655-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="0c655-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="0c655-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="0c655-107">转到“所有工作区”>“资源周期管理”。</span><span class="sxs-lookup"><span data-stu-id="0c655-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="0c655-108">单击“日历”。</span><span class="sxs-lookup"><span data-stu-id="0c655-108">Click Calendars.</span></span>
3. <span data-ttu-id="0c655-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0c655-109">Click New.</span></span>
4. <span data-ttu-id="0c655-110">在“日历”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0c655-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="0c655-111">这是日历的 ID，用作分配日历时的参考，如分配至运营资源或资源组。</span><span class="sxs-lookup"><span data-stu-id="0c655-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="0c655-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0c655-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0c655-113">在“标准工作日工时数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0c655-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="0c655-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0c655-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="0c655-115">单击“工作时间”。</span><span class="sxs-lookup"><span data-stu-id="0c655-115">Click Working times.</span></span>
9. <span data-ttu-id="0c655-116">单击“设计工作时间”。</span><span class="sxs-lookup"><span data-stu-id="0c655-116">Click Compose working times.</span></span>
    * <span data-ttu-id="0c655-117">生成您希望能够安排工作的每日工时。</span><span class="sxs-lookup"><span data-stu-id="0c655-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="0c655-118">随着时间的推移，您可以生成其他期间的工作时间。</span><span class="sxs-lookup"><span data-stu-id="0c655-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="0c655-119">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="0c655-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="0c655-120">这是日历必须打开的第一天。</span><span class="sxs-lookup"><span data-stu-id="0c655-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="0c655-121">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="0c655-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0c655-122">这是日历打开的最后一天。</span><span class="sxs-lookup"><span data-stu-id="0c655-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="0c655-123">在“工作时间模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0c655-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="0c655-124">工作时间模板定义一周每天的工时。</span><span class="sxs-lookup"><span data-stu-id="0c655-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="0c655-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0c655-125">Click OK.</span></span>
14. <span data-ttu-id="0c655-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0c655-126">Close the page.</span></span>


