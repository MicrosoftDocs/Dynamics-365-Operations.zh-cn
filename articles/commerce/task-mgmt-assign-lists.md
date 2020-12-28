---
title: 将任务列表分配给商店或员工
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将任务列表分配给商店或员工。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410552"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="9265a-103">将任务列表分配给商店或员工</span><span class="sxs-lookup"><span data-stu-id="9265a-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9265a-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将任务列表分配给商店或员工。</span><span class="sxs-lookup"><span data-stu-id="9265a-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9265a-105">概览</span><span class="sxs-lookup"><span data-stu-id="9265a-105">Overview</span></span>

<span data-ttu-id="9265a-106">可通过 Dynamics 365 Commerce 中的任务管理将任务列表分配给多个商店或员工，或分配给商店和员工的组合。</span><span class="sxs-lookup"><span data-stu-id="9265a-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="9265a-107">例如，一位 20 家商店的地区经理可能希望将 **假日准备** 任务列表分配给所有 20 商店。</span><span class="sxs-lookup"><span data-stu-id="9265a-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="9265a-108">开始任务列表分配流程</span><span class="sxs-lookup"><span data-stu-id="9265a-108">Start the task list assignment process</span></span>

<span data-ttu-id="9265a-109">若要开始分配任务列表流程，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9265a-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="9265a-110">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。</span><span class="sxs-lookup"><span data-stu-id="9265a-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="9265a-111">选择要分配的任务列表。</span><span class="sxs-lookup"><span data-stu-id="9265a-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="9265a-112">选择 **启动流程**。</span><span class="sxs-lookup"><span data-stu-id="9265a-112">Select **Start process**.</span></span>
1. <span data-ttu-id="9265a-113">在 **启动流程** 对话框的 **常规** 选项卡上 **流程名称** 字段中，输入名称（例如，**东部商店**）。</span><span class="sxs-lookup"><span data-stu-id="9265a-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="9265a-114">在 **目标日期** 字段中，指定一个日期。</span><span class="sxs-lookup"><span data-stu-id="9265a-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="9265a-115">若要将任务列表分配给商店，请在 **商店** 选项卡上，使用 **组织层次结构** 筛选器查找和选择商店。</span><span class="sxs-lookup"><span data-stu-id="9265a-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="9265a-116">若要将任务列表分配给工作人员，请在 **工作人员** 选项卡上，找到和选择员工。</span><span class="sxs-lookup"><span data-stu-id="9265a-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="9265a-117">选择 **确定** 开始执行流程。</span><span class="sxs-lookup"><span data-stu-id="9265a-117">Select **OK** to start the process.</span></span> <span data-ttu-id="9265a-118">将把任务列表分配给所选商店或员工。</span><span class="sxs-lookup"><span data-stu-id="9265a-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="9265a-119">下图显示如何在 **启动流程** 对话框中查找和选择商店的示例。</span><span class="sxs-lookup"><span data-stu-id="9265a-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![在“启动流程”对话框中查找和选择商店](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="9265a-121">在重复执行基础上分配任务列表</span><span class="sxs-lookup"><span data-stu-id="9265a-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="9265a-122">零售商有时会有重复执行任务，如“星期四歇业核对清单”或“月初核对清单”。</span><span class="sxs-lookup"><span data-stu-id="9265a-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="9265a-123">因此，他们可能希望在重复执行基础上分配任务列表。</span><span class="sxs-lookup"><span data-stu-id="9265a-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="9265a-124">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。</span><span class="sxs-lookup"><span data-stu-id="9265a-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="9265a-125">选择要分配的任务列表。</span><span class="sxs-lookup"><span data-stu-id="9265a-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="9265a-126">选择 **启动流程**。</span><span class="sxs-lookup"><span data-stu-id="9265a-126">Select **Start process**.</span></span>
1. <span data-ttu-id="9265a-127">在 **启动流程** 对话框的 **常规** 选项卡上 **流程名称** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="9265a-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="9265a-128">将 **重复执行** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="9265a-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="9265a-129">在 **以天为单位的重复执行目标日期偏置** 字段中，输入天数。</span><span class="sxs-lookup"><span data-stu-id="9265a-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="9265a-130">例如，如果输入 **4**，则目标日期为重复执行日期加上四天。</span><span class="sxs-lookup"><span data-stu-id="9265a-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="9265a-131">在 **在后台运行** 选项卡上，选择 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="9265a-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="9265a-132">在 **定义重复执行** 对话框中，输入频率条件，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9265a-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="9265a-133">下图显示如何在 **定义重复执行** 对话框中输入频率条件的示例。</span><span class="sxs-lookup"><span data-stu-id="9265a-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![在“定义重复执行”对话框中输入频率条件](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="9265a-135">跟踪任务列表状态</span><span class="sxs-lookup"><span data-stu-id="9265a-135">Track task list status</span></span>

<span data-ttu-id="9265a-136">如果您是区域经理或商店经理，您可能需要跟踪已分配给多家商店或员工的任务列表的状态。</span><span class="sxs-lookup"><span data-stu-id="9265a-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="9265a-137">然后可以跟进未及时完成所分配任务的商店或工作人员。</span><span class="sxs-lookup"><span data-stu-id="9265a-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="9265a-138">Commerce 后端让您可以查看任务列表的状态，重新分配任务，或更改任务的状态。</span><span class="sxs-lookup"><span data-stu-id="9265a-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="9265a-139">若要跟踪所有任务的任务列表状态，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9265a-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="9265a-140">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理流程**。</span><span class="sxs-lookup"><span data-stu-id="9265a-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="9265a-141">选择 **所有任务列表** 选项卡以查看分配给各商店的所有任务列表的状态。</span><span class="sxs-lookup"><span data-stu-id="9265a-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="9265a-142">若要跟踪分配给您的所有任务的任务列表状态，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9265a-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="9265a-143">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理流程**。</span><span class="sxs-lookup"><span data-stu-id="9265a-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="9265a-144">选择 **我的任务** 或 **所有任务** 选项卡以查看或更新分配给您的任务的状态。</span><span class="sxs-lookup"><span data-stu-id="9265a-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9265a-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="9265a-145">Additional resources</span></span>

[<span data-ttu-id="9265a-146">任务管理概述</span><span class="sxs-lookup"><span data-stu-id="9265a-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="9265a-147">配置任务管理</span><span class="sxs-lookup"><span data-stu-id="9265a-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="9265a-148">创建任务列表和添加任务</span><span class="sxs-lookup"><span data-stu-id="9265a-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="9265a-149">POS 中的任务管理</span><span class="sxs-lookup"><span data-stu-id="9265a-149">Task management in POS</span></span>](task-mgmt-POS.md)
