---
title: 输入项目工时单
description: 通过该过程您可以利用空余的时间表窗体创建时间表。
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2fd5c1e6c38c2e4380a8c8b061b08bce2dd43c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190434"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="af3cd-103">输入项目工时单</span><span class="sxs-lookup"><span data-stu-id="af3cd-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af3cd-104">通过该过程您可以利用空余的时间表窗体创建时间表。</span><span class="sxs-lookup"><span data-stu-id="af3cd-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="af3cd-105">新时间表是以之前的时间表的信息为基础，或以**我的收藏夹**页的项目和活动分配为基础。</span><span class="sxs-lookup"><span data-stu-id="af3cd-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="af3cd-106">在默认情况下，**所有时间表**列表页显示了您在当前周期内的所有时间表。</span><span class="sxs-lookup"><span data-stu-id="af3cd-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="af3cd-107">您可以利用**我的时间表**页面中**显示**字段的下拉式列表，根据周期或项目来筛选时间列表表单，或者查看由其他工人所创建的时间表。</span><span class="sxs-lookup"><span data-stu-id="af3cd-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="af3cd-108">用于创建该过程的演示数据公司为 USSI。</span><span class="sxs-lookup"><span data-stu-id="af3cd-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="af3cd-109">在**导航窗格**中，转到**模块 > 项目管理与核算 > 工时单 > 我的工时单**。</span><span class="sxs-lookup"><span data-stu-id="af3cd-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="af3cd-110">要输入新工时单，请单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="af3cd-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="af3cd-111">“资源”下拉列表默认显示了分配给当前用户的工作人员。</span><span class="sxs-lookup"><span data-stu-id="af3cd-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="af3cd-112">如果用户被命名为委托，则此处将列出名称，使得用户可以自己输入一个时间表。</span><span class="sxs-lookup"><span data-stu-id="af3cd-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="af3cd-113">在**日期**字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="af3cd-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="af3cd-114">如果选择了该选项，则可以通过应用收藏的时间表设置创建新的时间表行。</span><span class="sxs-lookup"><span data-stu-id="af3cd-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="af3cd-115">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="af3cd-115">Click **OK**.</span></span>
5. <span data-ttu-id="af3cd-116">单击**新建行**。</span><span class="sxs-lookup"><span data-stu-id="af3cd-116">Click **New line**.</span></span>
6. <span data-ttu-id="af3cd-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="af3cd-117">In the list, mark the selected row.</span></span> <span data-ttu-id="af3cd-118">**法人**字段显示了当前默认的法人。</span><span class="sxs-lookup"><span data-stu-id="af3cd-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="af3cd-119">在**项目**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="af3cd-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="af3cd-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="af3cd-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="af3cd-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="af3cd-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="af3cd-122">在**活动编号**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="af3cd-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="af3cd-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="af3cd-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="af3cd-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="af3cd-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="af3cd-125">在**类别**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="af3cd-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="af3cd-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="af3cd-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="af3cd-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="af3cd-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="af3cd-128">输入每天工作的工时数。</span><span class="sxs-lookup"><span data-stu-id="af3cd-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="af3cd-129">以小数格式输入工时。</span><span class="sxs-lookup"><span data-stu-id="af3cd-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="af3cd-130">例如，如果您工作了两小时十五分钟，输入2.25。</span><span class="sxs-lookup"><span data-stu-id="af3cd-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="af3cd-131">**行明细**中是以下可用选项：</span><span class="sxs-lookup"><span data-stu-id="af3cd-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="af3cd-132">在**常规**和**财务维度**选项卡中添加有关税款和财务维度的信息。</span><span class="sxs-lookup"><span data-stu-id="af3cd-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="af3cd-133">在**注释**选项卡中添加有关工时单行的注释。</span><span class="sxs-lookup"><span data-stu-id="af3cd-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="af3cd-134">在**操作窗格**中，单击**工作流**打开下列对话框。</span><span class="sxs-lookup"><span data-stu-id="af3cd-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="af3cd-135">单击**提交**。</span><span class="sxs-lookup"><span data-stu-id="af3cd-135">Click **Submit**.</span></span>
22. <span data-ttu-id="af3cd-136">单击**提交**。</span><span class="sxs-lookup"><span data-stu-id="af3cd-136">Click **Submit**.</span></span>

