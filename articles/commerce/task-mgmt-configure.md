---
title: 配置任务管理
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置任务管理功能。
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
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036847"
---
# <a name="configure-task-management"></a><span data-ttu-id="9f0ae-103">配置任务管理</span><span class="sxs-lookup"><span data-stu-id="9f0ae-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f0ae-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置任务管理功能。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9f0ae-105">概览</span><span class="sxs-lookup"><span data-stu-id="9f0ae-105">Overview</span></span>

<span data-ttu-id="9f0ae-106">必须先配置任务管理，Dynamics 365 Commerce 经理和员工才能使用 Commerce 中的任务管理功能。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="9f0ae-107">配置步骤包括为经理和员工授予权限，将权限分发给销售点 (POS) 客户端，设置 POS 通知，以及配置 POS 应用程序主页中的**任务**磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="9f0ae-108">配置商店经理的权限</span><span class="sxs-lookup"><span data-stu-id="9f0ae-108">Configure permissions for store managers</span></span>

<span data-ttu-id="9f0ae-109">给定商店中的每位工作人员都可以查看为该商店分配的所有任务。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="9f0ae-110">他们还可以更新为其分配的任务的状态。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="9f0ae-111">但是，商店经理之类个人必须拥有管理权限，才能管理为商店分配的任务和创建单一目标任务。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="9f0ae-112">若要为商店经理配置任务管理权限，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="9f0ae-113">转到 **Retail 和 Commerce \> 员工 \> 权限组**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="9f0ae-114">选择特定权限组（例如，**经理**），然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="9f0ae-115">在**权限**快速选项卡上，将**允许任务管理**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="9f0ae-116">在**通知**快速选项卡上，添加**任务管理**操作，然后在**显示顺序**字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="9f0ae-117">例如，如果**订单履行**操作的**显示顺序**值已经为 **1**，则输入 **2**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="9f0ae-118">如果一位非经理人员必须在 POS 中具有任务管理权限，可以为该人授予权限。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="9f0ae-119">也可以为非经理创建新的权限组，然后将**允许任务管理**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="9f0ae-120">下图显示如何为商店经理配置任务管理权限。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![为商店经理配置任务管理权限](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="9f0ae-122">为员工配置权限</span><span class="sxs-lookup"><span data-stu-id="9f0ae-122">Configure permissions for employees</span></span>

<span data-ttu-id="9f0ae-123">员工必须有权创建任务列表，管理分配条件和配置任何任务列表的重复。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="9f0ae-124">若要配置这些权限，请为员工分配**零售任务经理**角色。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="9f0ae-125">若要为员工配置权限，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="9f0ae-126">转到 **Retail 和 Commerce \> 员工 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="9f0ae-127">选择某一员工。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-127">Select an employee.</span></span>
1. <span data-ttu-id="9f0ae-128">在**用户的角色**快速选项卡，选择**分配角色**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="9f0ae-129">在**将角色分配给用户**对话框中，选择**零售任务经理**角色，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="9f0ae-130">为 POS 客户端分配权限</span><span class="sxs-lookup"><span data-stu-id="9f0ae-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="9f0ae-131">必须先分发权限并同步到 POS 客户端，员工才能使用这些客户端。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="9f0ae-132">若要为 POS 客户端分发权限，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="9f0ae-133">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="9f0ae-134">选择 **1060**（**员工**）分发计划，然后选择**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="9f0ae-135">选择 **1070**（**渠道配置**）分发计划，然后选择**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="9f0ae-136">为任务配置 POS 通知</span><span class="sxs-lookup"><span data-stu-id="9f0ae-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="9f0ae-137">必须配置任务管理，以便 POS 应用程序中支持通知。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="9f0ae-138">若要为任务配置 POS 通知，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="9f0ae-139">转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> POS 操作**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="9f0ae-140">找到操作 **1400**（**任务管理**），然后选中其**启用通知**复选框。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="9f0ae-141">下图显示 **POS 操作**页中的**任务管理**操作。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![POS 操作页中的任务管理操作](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="9f0ae-143">有关如何配置 POS 通知的详细信息，请参阅[在销售点 (POS) 中显示订单通知](notifications-pos.md)。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="9f0ae-144">配置 POS 应用程序主页中的“任务”磁贴</span><span class="sxs-lookup"><span data-stu-id="9f0ae-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="9f0ae-145">配置 POS 应用程序主页中的**任务**磁贴之前，请参阅[销售点 (POS) 的屏幕截图](pos-screen-layouts.md)以获取有关如何配置和将新按钮添加到 POS 屏幕布局的信息。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="9f0ae-146">若要配置 POS 应用程序主页中的**任务**磁贴，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="9f0ae-147">转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> 屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="9f0ae-148">选择一个屏幕布局，选择布局大小，然后选择按钮网格。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="9f0ae-149">在**按钮网格**快速选项卡上，选择**设计器**编辑所选按钮网格。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="9f0ae-150">向主页的相应部分添加**任务**磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="9f0ae-151">下图显示 POS 主页中的**任务**磁贴的示例。</span><span class="sxs-lookup"><span data-stu-id="9f0ae-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![POS 主页上的“任务”磁贴](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="9f0ae-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="9f0ae-153">Additional resources</span></span>

[<span data-ttu-id="9f0ae-154">任务管理概述</span><span class="sxs-lookup"><span data-stu-id="9f0ae-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="9f0ae-155">创建任务列表和添加任务</span><span class="sxs-lookup"><span data-stu-id="9f0ae-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="9f0ae-156">将任务列表分配给商店或员工</span><span class="sxs-lookup"><span data-stu-id="9f0ae-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="9f0ae-157">POS 中的任务管理</span><span class="sxs-lookup"><span data-stu-id="9f0ae-157">Task management in POS</span></span>](task-mgmt-POS.md)
