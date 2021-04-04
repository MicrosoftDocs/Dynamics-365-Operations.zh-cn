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
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3d249809f15b50c59620d69a901a427dc3ecb2f0
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477576"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="1fec0-103">将任务列表分配给商店或员工</span><span class="sxs-lookup"><span data-stu-id="1fec0-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1fec0-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将任务列表分配给商店或员工。</span><span class="sxs-lookup"><span data-stu-id="1fec0-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1fec0-105">可通过 Dynamics 365 Commerce 中的任务管理将任务列表分配给多个商店或员工，或分配给商店和员工的组合。</span><span class="sxs-lookup"><span data-stu-id="1fec0-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="1fec0-106">例如，一位 20 家商店的地区经理可能希望将 **假日准备** 任务列表分配给所有 20 商店。</span><span class="sxs-lookup"><span data-stu-id="1fec0-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="1fec0-107">开始任务列表分配流程</span><span class="sxs-lookup"><span data-stu-id="1fec0-107">Start the task list assignment process</span></span>

<span data-ttu-id="1fec0-108">若要开始分配任务列表流程，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1fec0-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="1fec0-109">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="1fec0-110">选择要分配的任务列表。</span><span class="sxs-lookup"><span data-stu-id="1fec0-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="1fec0-111">选择 **启动流程**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-111">Select **Start process**.</span></span>
1. <span data-ttu-id="1fec0-112">在 **启动流程** 对话框的 **常规** 选项卡上 **流程名称** 字段中，输入名称（例如，**东部商店**）。</span><span class="sxs-lookup"><span data-stu-id="1fec0-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="1fec0-113">在 **目标日期** 字段中，指定一个日期。</span><span class="sxs-lookup"><span data-stu-id="1fec0-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="1fec0-114">若要将任务列表分配给商店，请在 **商店** 选项卡上，使用 **组织层次结构** 筛选器查找和选择商店。</span><span class="sxs-lookup"><span data-stu-id="1fec0-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="1fec0-115">若要将任务列表分配给工作人员，请在 **工作人员** 选项卡上，找到和选择员工。</span><span class="sxs-lookup"><span data-stu-id="1fec0-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="1fec0-116">选择 **确定** 开始执行流程。</span><span class="sxs-lookup"><span data-stu-id="1fec0-116">Select **OK** to start the process.</span></span> <span data-ttu-id="1fec0-117">将把任务列表分配给所选商店或员工。</span><span class="sxs-lookup"><span data-stu-id="1fec0-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="1fec0-118">下图显示如何在 **启动流程** 对话框中查找和选择商店的示例。</span><span class="sxs-lookup"><span data-stu-id="1fec0-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![在“启动流程”对话框中查找和选择商店](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="1fec0-120">在重复执行基础上分配任务列表</span><span class="sxs-lookup"><span data-stu-id="1fec0-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="1fec0-121">零售商有时会有重复执行任务，如“星期四歇业核对清单”或“月初核对清单”。</span><span class="sxs-lookup"><span data-stu-id="1fec0-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="1fec0-122">因此，他们可能希望在重复执行基础上分配任务列表。</span><span class="sxs-lookup"><span data-stu-id="1fec0-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="1fec0-123">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="1fec0-124">选择要分配的任务列表。</span><span class="sxs-lookup"><span data-stu-id="1fec0-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="1fec0-125">选择 **启动流程**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-125">Select **Start process**.</span></span>
1. <span data-ttu-id="1fec0-126">在 **启动流程** 对话框的 **常规** 选项卡上 **流程名称** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="1fec0-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="1fec0-127">将 **重复执行** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="1fec0-128">在 **以天为单位的重复执行目标日期偏置** 字段中，输入天数。</span><span class="sxs-lookup"><span data-stu-id="1fec0-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="1fec0-129">例如，如果输入 **4**，则目标日期为重复执行日期加上四天。</span><span class="sxs-lookup"><span data-stu-id="1fec0-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="1fec0-130">在 **在后台运行** 选项卡上，选择 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="1fec0-131">在 **定义重复执行** 对话框中，输入频率条件，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="1fec0-132">下图显示如何在 **定义重复执行** 对话框中输入频率条件的示例。</span><span class="sxs-lookup"><span data-stu-id="1fec0-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![在“定义重复执行”对话框中输入频率条件](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="1fec0-134">跟踪任务列表状态</span><span class="sxs-lookup"><span data-stu-id="1fec0-134">Track task list status</span></span>

<span data-ttu-id="1fec0-135">如果您是区域经理或商店经理，您可能需要跟踪已分配给多家商店或员工的任务列表的状态。</span><span class="sxs-lookup"><span data-stu-id="1fec0-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="1fec0-136">然后可以跟进未及时完成所分配任务的商店或工作人员。</span><span class="sxs-lookup"><span data-stu-id="1fec0-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="1fec0-137">Commerce 后端让您可以查看任务列表的状态，重新分配任务，或更改任务的状态。</span><span class="sxs-lookup"><span data-stu-id="1fec0-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="1fec0-138">若要跟踪所有任务的任务列表状态，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1fec0-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="1fec0-139">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理流程**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="1fec0-140">选择 **所有任务列表** 选项卡以查看分配给各商店的所有任务列表的状态。</span><span class="sxs-lookup"><span data-stu-id="1fec0-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="1fec0-141">若要跟踪分配给您的所有任务的任务列表状态，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1fec0-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="1fec0-142">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理流程**。</span><span class="sxs-lookup"><span data-stu-id="1fec0-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="1fec0-143">选择 **我的任务** 或 **所有任务** 选项卡以查看或更新分配给您的任务的状态。</span><span class="sxs-lookup"><span data-stu-id="1fec0-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fec0-144">其他资源</span><span class="sxs-lookup"><span data-stu-id="1fec0-144">Additional resources</span></span>

[<span data-ttu-id="1fec0-145">任务管理概述</span><span class="sxs-lookup"><span data-stu-id="1fec0-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="1fec0-146">配置任务管理</span><span class="sxs-lookup"><span data-stu-id="1fec0-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="1fec0-147">创建任务列表和添加任务</span><span class="sxs-lookup"><span data-stu-id="1fec0-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="1fec0-148">POS 中的任务管理</span><span class="sxs-lookup"><span data-stu-id="1fec0-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
