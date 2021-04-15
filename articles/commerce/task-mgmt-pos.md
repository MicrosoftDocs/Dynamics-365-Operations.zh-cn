---
title: POS 中的任务管理
description: 此主题介绍 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中的任务管理。
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 38ee9db94b3b222e8c0ce5d0883f47bd5d3e7d22
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796914"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="a8706-103">POS 中的任务管理</span><span class="sxs-lookup"><span data-stu-id="a8706-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8706-104">此主题介绍 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中的任务管理。</span><span class="sxs-lookup"><span data-stu-id="a8706-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="a8706-105">此 Dynamics 365 Commerce POS 应用程序具有任务管理功能，可供商店经理和工作人员管理任务和更新任务状态。</span><span class="sxs-lookup"><span data-stu-id="a8706-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="a8706-106">商店工作人员可通过选择 POS 主页中的 **任务** 磁贴或选择任务通知访问任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="a8706-107">默认情况下，商店工作人员将被带到 **我的任务** 选项卡，可在这里查看分配给他们的任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="a8706-108">但是，他们可以轻松切换到 **逾期任务**、**未结任务** 和 **任务列表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="a8706-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="a8706-109">适用于商店经理的任务操作</span><span class="sxs-lookup"><span data-stu-id="a8706-109">Task operations for store managers</span></span>

<span data-ttu-id="a8706-110">商店经理可以通过使用命令栏中的按钮，在 POS 应用程序中执行以下任务操作：</span><span class="sxs-lookup"><span data-stu-id="a8706-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="a8706-111">**分配** – 将所选任务分配给商店工作人员。</span><span class="sxs-lookup"><span data-stu-id="a8706-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="a8706-112">**任务状态** – 更改所选任务的状态。</span><span class="sxs-lookup"><span data-stu-id="a8706-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="a8706-113">**筛选** – 默认情况下，仅显示有效任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="a8706-114">但是，通过应用过滤器，经理可以查看所有任务，甚至是已完成或已取消的任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="a8706-115">**新建任务** – 在现有任务列表下创建任务，或创建单一用途任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="a8706-116">商店工作人员可以通过使用命令栏中的按钮，在 POS 应用程序中执行以下任务操作：</span><span class="sxs-lookup"><span data-stu-id="a8706-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="a8706-117">**任务状态** – 更改所选任务的状态。</span><span class="sxs-lookup"><span data-stu-id="a8706-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="a8706-118">**筛选** – 默认情况下，仅显示有效任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="a8706-119">但是，通过应用过滤器，工作人员可以查看所有任务，甚至是已完成或已取消的任务。</span><span class="sxs-lookup"><span data-stu-id="a8706-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="a8706-120">下图显示 Commerce POS 应用程序中的 **我的任务** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="a8706-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Commerce POS 应用程序中的“我的任务”选项卡](media/POS-task-management.png)

<span data-ttu-id="a8706-122">下图显示 **任务列表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="a8706-122">The following illustration shows the **Task lists** tab.</span></span>

![Commerce POS 应用程序中的“任务列表”选项卡](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="a8706-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="a8706-124">Additional resources</span></span>

[<span data-ttu-id="a8706-125">任务管理概述</span><span class="sxs-lookup"><span data-stu-id="a8706-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="a8706-126">配置任务管理</span><span class="sxs-lookup"><span data-stu-id="a8706-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="a8706-127">创建任务列表和添加任务</span><span class="sxs-lookup"><span data-stu-id="a8706-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="a8706-128">将任务列表分配给商店或员工</span><span class="sxs-lookup"><span data-stu-id="a8706-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
