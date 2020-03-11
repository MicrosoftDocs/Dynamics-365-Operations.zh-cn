---
title: 创建任务列表和添加任务
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建任务列表和向其添加任务。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1cab31784db9f3242dce20e98762088436a5a8f8
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036824"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="bd22f-103">创建任务列表和添加任务</span><span class="sxs-lookup"><span data-stu-id="bd22f-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd22f-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建任务列表和向其添加任务。</span><span class="sxs-lookup"><span data-stu-id="bd22f-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bd22f-105">概览</span><span class="sxs-lookup"><span data-stu-id="bd22f-105">Overview</span></span>

<span data-ttu-id="bd22f-106">*任务*定义某人必须在指定日期或之前完成的一份工作或一个操作。</span><span class="sxs-lookup"><span data-stu-id="bd22f-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="bd22f-107">在 Dynamics 365 Commerce 中，任务中可以包含详细说明和有关联系人的信息。</span><span class="sxs-lookup"><span data-stu-id="bd22f-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="bd22f-108">还可以包含后勤运营、销售点 (POS) 操作或站点页的链接，以便帮助提高生产力和提供任务负责人高效完成任务所需上下文。</span><span class="sxs-lookup"><span data-stu-id="bd22f-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="bd22f-109">*任务列表*是业务流程中必须完成的任务的集合。</span><span class="sxs-lookup"><span data-stu-id="bd22f-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="bd22f-110">例如，有一个任务列表是新工作人员在入职期间必须完成的，有一个任务列表针对夜班工作的收银员，还有一个任务列表是为商店准备即将到来的假日需要完成的。</span><span class="sxs-lookup"><span data-stu-id="bd22f-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="bd22f-111">在 Commerce 中，可以将具有目标日期的每个任务列表分配给任意数量的商店或员工，并且可以将其配置为重复任务列表。</span><span class="sxs-lookup"><span data-stu-id="bd22f-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="bd22f-112">经理和工作人员都可以在 Commerce 后端创建任务列表，然后将其分配给一组商店。</span><span class="sxs-lookup"><span data-stu-id="bd22f-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="bd22f-113">创建任务列表</span><span class="sxs-lookup"><span data-stu-id="bd22f-113">Create a task list</span></span>

<span data-ttu-id="bd22f-114">若要创建任务列表，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bd22f-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="bd22f-115">转到 **Retail 和 Commerce \> 任务管理 \> 任务管理管理**。</span><span class="sxs-lookup"><span data-stu-id="bd22f-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="bd22f-116">选择**新建**，然后在**名称**、**描述**和**负责人**字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="bd22f-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="bd22f-117">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="bd22f-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="bd22f-118">向任务列表添加任务</span><span class="sxs-lookup"><span data-stu-id="bd22f-118">Add tasks to a task list</span></span>

<span data-ttu-id="bd22f-119">若要向任务列表添加任务，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bd22f-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="bd22f-120">在现有任务列表的**任务**快速选项卡上，选择**新建**添加任务。</span><span class="sxs-lookup"><span data-stu-id="bd22f-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="bd22f-121">在**创建新任务**对话框的**名称**字段中，输入任务的名称。</span><span class="sxs-lookup"><span data-stu-id="bd22f-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="bd22f-122">在**从目标日期算起的到期日期偏置**字段中，输入正整数或负整数值。</span><span class="sxs-lookup"><span data-stu-id="bd22f-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="bd22f-123">例如，如果任务应该在任务列表到期日期之前两天完成，则输入 **-2**。</span><span class="sxs-lookup"><span data-stu-id="bd22f-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="bd22f-124">在**注释**字段中，输入详细说明。</span><span class="sxs-lookup"><span data-stu-id="bd22f-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="bd22f-125">在**联系人**字段中，装入任务负责人在需要帮助时可以联系的主题专家的姓名。</span><span class="sxs-lookup"><span data-stu-id="bd22f-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="bd22f-126">在**任务链接**字段中，根据任务的性质输入链接。</span><span class="sxs-lookup"><span data-stu-id="bd22f-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="bd22f-127">虽然在创建任务列表时可以使用**分配到**字段将任务分配给某人，我们还是建议您避免在创建任务列表期间分配任务。</span><span class="sxs-lookup"><span data-stu-id="bd22f-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="bd22f-128">而是在针对单个商店实例化了列表之后分配任务。</span><span class="sxs-lookup"><span data-stu-id="bd22f-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="bd22f-129">使用任务列表帮助提高工作人员的生产力</span><span class="sxs-lookup"><span data-stu-id="bd22f-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="bd22f-130">Commerce 让您可以将任务链接到特定 POS 操作，如运行销售报表，查看面向新员工的在线培训视频，或执行后端操作。</span><span class="sxs-lookup"><span data-stu-id="bd22f-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="bd22f-131">此功能帮助任务负责人获取有关高效完成任务所需信息。</span><span class="sxs-lookup"><span data-stu-id="bd22f-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="bd22f-132">若要在创建任务时添加任务链接，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bd22f-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="bd22f-133">在现有任务列表的**任务**快速选项卡上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="bd22f-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="bd22f-134">在**编辑任务**对话框的**任务链接**字段中，选择以下选项中的一个或多个：</span><span class="sxs-lookup"><span data-stu-id="bd22f-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="bd22f-135">选择**菜单项**配置后端操作，例如“产品套件”。</span><span class="sxs-lookup"><span data-stu-id="bd22f-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="bd22f-136">选择 **POS 操作**配置 POS 操作，例如“销售报表”。</span><span class="sxs-lookup"><span data-stu-id="bd22f-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="bd22f-137">选择 **URL** 配置绝对 URL。</span><span class="sxs-lookup"><span data-stu-id="bd22f-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="bd22f-138">下图显示**编辑任务**对话框中的任务链接的选择情况。</span><span class="sxs-lookup"><span data-stu-id="bd22f-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![在“编辑任务”对话框中选择任务链接](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="bd22f-140">配置 POS 操作以使其可链接到任务</span><span class="sxs-lookup"><span data-stu-id="bd22f-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="bd22f-141">若要配置 POS 操作以使其可链接到任务，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bd22f-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="bd22f-142">转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> POS 操作**。</span><span class="sxs-lookup"><span data-stu-id="bd22f-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="bd22f-143">选择**编辑**，找到 POS 操作，然后选中其**启用任务管理**复选框。</span><span class="sxs-lookup"><span data-stu-id="bd22f-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd22f-144">其他资源</span><span class="sxs-lookup"><span data-stu-id="bd22f-144">Additional resources</span></span>

[<span data-ttu-id="bd22f-145">任务管理概述</span><span class="sxs-lookup"><span data-stu-id="bd22f-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="bd22f-146">配置任务管理</span><span class="sxs-lookup"><span data-stu-id="bd22f-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="bd22f-147">将任务列表分配给商店或员工</span><span class="sxs-lookup"><span data-stu-id="bd22f-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="bd22f-148">POS 中的任务管理</span><span class="sxs-lookup"><span data-stu-id="bd22f-148">Task management in POS</span></span>](task-mgmt-POS.md)
