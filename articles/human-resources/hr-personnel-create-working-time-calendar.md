---
title: 创建日历并生成工作时间
description: 日历描述运营资源的产能和工作时间。 本文介绍如何定义基于工作时间模板的工作日历。
author: andreabichsel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af2675468dcc1f1891d24d988c32115ae57e1d2b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465454"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="e641e-104">创建日历并生成工作时间</span><span class="sxs-lookup"><span data-stu-id="e641e-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="e641e-105">日历描述运营资源的产能和工作时间。</span><span class="sxs-lookup"><span data-stu-id="e641e-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="e641e-106">本文介绍如何定义基于工作时间模板的工作日历。</span><span class="sxs-lookup"><span data-stu-id="e641e-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="e641e-107">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="e641e-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="e641e-108">在主页上，选择 **资源生命周期管理**。</span><span class="sxs-lookup"><span data-stu-id="e641e-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="e641e-109">选择 **日历**。</span><span class="sxs-lookup"><span data-stu-id="e641e-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="e641e-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e641e-110">Select **New**.</span></span>
4. <span data-ttu-id="e641e-111">在 **日历** 字段中，为日历分类。</span><span class="sxs-lookup"><span data-stu-id="e641e-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="e641e-112">这是日历的 ID，用作分配日历时的参考，如分配至运营资源或资源组。</span><span class="sxs-lookup"><span data-stu-id="e641e-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="e641e-113">在 **名称** 字段中，为日历命名。</span><span class="sxs-lookup"><span data-stu-id="e641e-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="e641e-114">在 **标准工作日工时数** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e641e-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="e641e-115">确保选择行，然后从操作窗格选择 **工作时间**。</span><span class="sxs-lookup"><span data-stu-id="e641e-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="e641e-116">选择 **设计工作时间**。</span><span class="sxs-lookup"><span data-stu-id="e641e-116">Select **Compose working times**.</span></span> <span data-ttu-id="e641e-117">生成您希望能够安排工作的每日工时。</span><span class="sxs-lookup"><span data-stu-id="e641e-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="e641e-118">随着时间的推移，您可以生成其他期间的工作时间。</span><span class="sxs-lookup"><span data-stu-id="e641e-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="e641e-119">在 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="e641e-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="e641e-120">这是日历必须打开的第一天。</span><span class="sxs-lookup"><span data-stu-id="e641e-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="e641e-121">在 **结束日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="e641e-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="e641e-122">这是日历打开的最后一天。</span><span class="sxs-lookup"><span data-stu-id="e641e-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="e641e-123">在 **工作时间模板** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e641e-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="e641e-124">工作时间模板定义一周每天的工时。</span><span class="sxs-lookup"><span data-stu-id="e641e-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="e641e-125">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e641e-125">Select **OK**.</span></span>
13. <span data-ttu-id="e641e-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e641e-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]