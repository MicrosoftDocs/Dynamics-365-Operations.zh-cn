---
title: 在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理
description: 本主题介绍如何在 Microsoft Teams 和 Dynamics 365 Commerce 销售点 (POS) 之间同步任务管理。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020619"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="68fd6-103">在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理</span><span class="sxs-lookup"><span data-stu-id="68fd6-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68fd6-104">本主题介绍如何在 Microsoft Teams 和 Dynamics 365 Commerce 销售点 (POS) 之间同步任务管理。</span><span class="sxs-lookup"><span data-stu-id="68fd6-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="68fd6-105">Teams 集成的主要目的之一是在 POS 应用程序和 Teams 之间同步任务管理。</span><span class="sxs-lookup"><span data-stu-id="68fd6-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="68fd6-106">这样，商店员工可以使用 POS 应用程序或 Teams 来管理任务，而不必切换应用程序。</span><span class="sxs-lookup"><span data-stu-id="68fd6-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="68fd6-107">由于 Planner 用作 Teams 中任务的存储库，因此 Teams 和 Dynamics 365 Commerce 之间必须存在链接。</span><span class="sxs-lookup"><span data-stu-id="68fd6-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="68fd6-108">通过使用给定商店团队的特定计划 ID 来建立此链接。</span><span class="sxs-lookup"><span data-stu-id="68fd6-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="68fd6-109">以下过程显示了如何在 POS 和 Teams 应用程序之间设置任务管理同步。</span><span class="sxs-lookup"><span data-stu-id="68fd6-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="68fd6-110">在 Teams 中发布测试任务列表</span><span class="sxs-lookup"><span data-stu-id="68fd6-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="68fd6-111">以下过程假设您的商店团队首次使用与 Commerce 的 Microsoft Teams 任务管理集成。</span><span class="sxs-lookup"><span data-stu-id="68fd6-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="68fd6-112">若要在 Teams 中发布测试任务列表，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="68fd6-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="68fd6-113">以通信经理身份登录到 Teams。</span><span class="sxs-lookup"><span data-stu-id="68fd6-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="68fd6-114">通常，通信经理是在 Commerce 中具有 **区域经理** 角色的用户。</span><span class="sxs-lookup"><span data-stu-id="68fd6-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="68fd6-115">在左侧导航窗格中，选择 **按 Planner 划分的任务**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="68fd6-116">在 **已发布列表** 选项卡上，选择左下角的 **新建列表**，然后将新列表命名为 **测试任务列表**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="68fd6-117">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-117">Select **Create**.</span></span> <span data-ttu-id="68fd6-118">新列表将显示在 **草稿** 下。</span><span class="sxs-lookup"><span data-stu-id="68fd6-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="68fd6-119">在 **任务标题** 下，向第一个任务提供标题 **测试 Teams 集成**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="68fd6-120">然后选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="68fd6-121">在 **草稿** 列表中，选择任务列表。</span><span class="sxs-lookup"><span data-stu-id="68fd6-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="68fd6-122">然后，选择右上角的 **发布** 。</span><span class="sxs-lookup"><span data-stu-id="68fd6-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="68fd6-123">在 **选择要发布给的人** 对话框中，选择应该接收测试任务列表的团队。</span><span class="sxs-lookup"><span data-stu-id="68fd6-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="68fd6-124">选择 **下一步** 以查看您的发布计划。</span><span class="sxs-lookup"><span data-stu-id="68fd6-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="68fd6-125">如果必须进行更改，请选择 **后退**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="68fd6-126">选择 **确认继续**，然后选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="68fd6-127">发布完成后，**已发布列表** 选项卡顶部的消息指示您的任务列表是否已成功交付。</span><span class="sxs-lookup"><span data-stu-id="68fd6-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="68fd6-128">有关详细信息，请参阅[发布任务列表以创建和跟踪组织中的工作](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df)。</span><span class="sxs-lookup"><span data-stu-id="68fd6-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="68fd6-129">链接 POS 和 Teams 以进行任务管理</span><span class="sxs-lookup"><span data-stu-id="68fd6-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="68fd6-130">若要在 Commerce Headquarters 中链接 POS 和 Microsoft Teams 应用程序以进行任务管理，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="68fd6-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="68fd6-131">转到 **Retail 和 Commerce \> 任务管理 \> 与 Microsoft Teams 的任务集成**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="68fd6-132">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="68fd6-133">将 **启用任务管理集成** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="68fd6-134">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="68fd6-135">在操作窗格上，选择 **设置任务管理**。</span><span class="sxs-lookup"><span data-stu-id="68fd6-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="68fd6-136">您应该收到一条通知，指示将创建名为 **Teams 预配** 的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="68fd6-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="68fd6-137">转到 **系统管理 \> 查询 \> 批处理作业**，查找具有描述 **Teams 预配** 的最新作业。</span><span class="sxs-lookup"><span data-stu-id="68fd6-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="68fd6-138">等待此作业完成运行。</span><span class="sxs-lookup"><span data-stu-id="68fd6-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="68fd6-139">运行 **CDX 作业 1070** 以将计划 ID 和商店引用发布到 Retail Server。</span><span class="sxs-lookup"><span data-stu-id="68fd6-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68fd6-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="68fd6-140">Additional resources</span></span>

[<span data-ttu-id="68fd6-141">Dynamics 365 Commerce 和 Microsoft Teams 集成概览</span><span class="sxs-lookup"><span data-stu-id="68fd6-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="68fd6-142">启用 Dynamics 365 Commerce 和 Microsoft Teams 集成</span><span class="sxs-lookup"><span data-stu-id="68fd6-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="68fd6-143">从 Dynamics 365 Commerce 预配 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="68fd6-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="68fd6-144">在 Microsoft Teams 中管理用户角色</span><span class="sxs-lookup"><span data-stu-id="68fd6-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="68fd6-145">如果 Microsoft Teams 中有预先存在的团队，映射商店和团队</span><span class="sxs-lookup"><span data-stu-id="68fd6-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="68fd6-146">Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答</span><span class="sxs-lookup"><span data-stu-id="68fd6-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
