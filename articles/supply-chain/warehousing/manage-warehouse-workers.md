---
title: 管理仓库工作人员
description: 本文介绍如何使用 Dynamics 365 Supply Chain Management - 仓库应用程序帮助监控由您仓库的员工执行的工作。
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b143051ba39c74869d2ec56203ee4f1cda7268a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205567"
---
# <a name="manage-warehouse-workers"></a><span data-ttu-id="50db4-103">管理仓库工作人员</span><span class="sxs-lookup"><span data-stu-id="50db4-103">Manage warehouse workers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50db4-104">本文介绍如何使用 Dynamics 365 Supply Chain Management - 仓库应用程序帮助监控由您仓库的员工执行的工作。</span><span class="sxs-lookup"><span data-stu-id="50db4-104">This article describes how you can use Dynamics 365 Supply Chain Management - Warehousing app to help control and monitor the work that's carried out by employees in your warehouses.</span></span>

<span data-ttu-id="50db4-105">如果在仓库管理中使用此功能，所有仓库工作人员的操作称作*工作*。</span><span class="sxs-lookup"><span data-stu-id="50db4-105">If you're using the functionality in Warehouse management, all warehouse worker operations are referred to as *work*.</span></span> <span data-ttu-id="50db4-106">领料、移动和盘点现有库存量等工作使用移动设备记录。</span><span class="sxs-lookup"><span data-stu-id="50db4-106">Work such as picking, moving, and counting on-hand inventory is recorded by using mobile devices.</span></span> <span data-ttu-id="50db4-107">在仓库工作人员可以执行工作之前，他或她必须与人力资源的工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="50db4-107">Before a warehouse worker can perform work, he or she must be associated with a worker in Human resources.</span></span> <span data-ttu-id="50db4-108">每个**工作人员**帐户可以有多个仓库工作用户与它关联。</span><span class="sxs-lookup"><span data-stu-id="50db4-108">Each **Worker** account can have multiple warehouse work users associated with it.</span></span> <span data-ttu-id="50db4-109">这些工作用户可以在不同的仓库工作，并且可具有不同级别的各个移动设备菜单的访问权限。</span><span class="sxs-lookup"><span data-stu-id="50db4-109">Those work users can work in different warehouses and can have different levels of access to the various mobile device menus.</span></span> <span data-ttu-id="50db4-110">您可以将仓库工作用户视作所选工作人员的多重登录。</span><span class="sxs-lookup"><span data-stu-id="50db4-110">You can think of the warehouse work users as multiple logons for the selected worker.</span></span> <span data-ttu-id="50db4-111">每个工作用户具有默认仓库，并且特定工作流由可用于该工作用户的菜单项显示。</span><span class="sxs-lookup"><span data-stu-id="50db4-111">Each work user has a default warehouse, and specific workflows are exposed by the menus items that are available to that work user.</span></span> 

<span data-ttu-id="50db4-112">若要创建新的工作用户，在**工作人员**页面，在**常规**选项卡上，在**仓库**部分单击**工作人员**。</span><span class="sxs-lookup"><span data-stu-id="50db4-112">To create a new work user, on the **Workers** page, on the **General** tab, in the **Warehouses** section, click **Worker**.</span></span> <span data-ttu-id="50db4-113">您必须指定用户 ID、用户名、默认仓库和菜单名。</span><span class="sxs-lookup"><span data-stu-id="50db4-113">You must specify a user ID, a user name, a default warehouse, and a menu name.</span></span> <span data-ttu-id="50db4-114">此菜单在该用户登录到仓库移动设备门户时加载，让您定义用户有权访问的菜单项。</span><span class="sxs-lookup"><span data-stu-id="50db4-114">This menu is loaded when the user signs in to the Warehouse Mobile Device Portal, and lets you define which menu items the user has access to.</span></span> 

<span data-ttu-id="50db4-115">作为每个工作用户设置的一部分，您还可以定义特定流程的工作流。</span><span class="sxs-lookup"><span data-stu-id="50db4-115">As part of the setup for each work user, you can also define specific process workflows.</span></span> <span data-ttu-id="50db4-116">例如，可以使用**为周期盘点主管**字段指定用户是否可以在盘点操作中处理对周期盘点差异的调整，或者这些调整是否必须由另一个人首先审查。</span><span class="sxs-lookup"><span data-stu-id="50db4-116">For example, you can use the **Is a cycle count supervisor** field to specify whether the user can process adjustments to cycle counting discrepancies during a counting operation, or whether these adjustments must first be reviewed by another person.</span></span>

## <a name="defining-labor-standards"></a><span data-ttu-id="50db4-117">定义人工标准</span><span class="sxs-lookup"><span data-stu-id="50db4-117">Defining labor standards</span></span>
<span data-ttu-id="50db4-118">**人工标准**页让您可以定义系统用于计算特定类型的工作应需要的估计时间的计算方法。</span><span class="sxs-lookup"><span data-stu-id="50db4-118">The **Labor standards** page lets you define the calculation methods that the system uses to calculate the estimated time that a particular type of work should require.</span></span> <span data-ttu-id="50db4-119">此定义可以在一般级别或特定级别设置。</span><span class="sxs-lookup"><span data-stu-id="50db4-119">This definition can be set on a generic level or on a specific level.</span></span> <span data-ttu-id="50db4-120">例如，您可以定义在使用特定领料流程时，按特定单位定义的重量处理销售订单领料应需要的时间。</span><span class="sxs-lookup"><span data-stu-id="50db4-120">For example, you can define the time that should be required in order to process a sales order pick per weight for a specific unit definition when a specific picking process is used.</span></span> <span data-ttu-id="50db4-121">同时，您可以基于其他计算方法记录已领料的现有库存量的放置操作的时间。</span><span class="sxs-lookup"><span data-stu-id="50db4-121">At the same time, you can record the time, based on another calculation method, for the put operation of the on-hand inventory that is picked.</span></span> 

<span data-ttu-id="50db4-122">若要启用您定义的人工标准，则您必须为使用人工标准的每个仓库选择**允许人工标准**选项。</span><span class="sxs-lookup"><span data-stu-id="50db4-122">To enable the labor standards that you've defined, you must select the **Allow labor standards** option for each warehouse where labor standards will be used.</span></span>

## <a name="monitoring-and-controlling-warehouse-work"></a><span data-ttu-id="50db4-123">监控仓库工作</span><span class="sxs-lookup"><span data-stu-id="50db4-123">Monitoring and controlling warehouse work</span></span>
<span data-ttu-id="50db4-124">**所有工作**页让您可以监控和维护计划、进行中和已完成的所有工作。</span><span class="sxs-lookup"><span data-stu-id="50db4-124">The **All work** page lets you monitor and maintain all work that is planned, in progress, and completed.</span></span> <span data-ttu-id="50db4-125">在此页上，您可以更新不同的流程，如仓库工作用户分配和工作优先级。</span><span class="sxs-lookup"><span data-stu-id="50db4-125">From this page, you can update various processes, such as warehouse work user assignments and work priority.</span></span> <span data-ttu-id="50db4-126">您还可以深化到与工作标题和工作行相关的详细信息，以取得对预期或完成的工作流程的了解。</span><span class="sxs-lookup"><span data-stu-id="50db4-126">You can also drill down into the details that are related to the work header and work lines to gain an understanding of the expected or completed work processes.</span></span> 

<span data-ttu-id="50db4-127">如果您启用**人工标准**选项，您可以看到该工作的计算出的估计时间。</span><span class="sxs-lookup"><span data-stu-id="50db4-127">If you enable the **Labor standards** option, you can see the calculated estimated time for the work.</span></span> <span data-ttu-id="50db4-128">然后，在处理该工作时，每个工作工序的实际时间也将显示。</span><span class="sxs-lookup"><span data-stu-id="50db4-128">Then, when the work is processed, the actual time will also be shown for each work operation.</span></span> <span data-ttu-id="50db4-129">这样，您可以将估计时间计算与实际时间比较。</span><span class="sxs-lookup"><span data-stu-id="50db4-129">In this way, you can compare the estimated time calculations to the actual time.</span></span> 

<span data-ttu-id="50db4-130">此外，您可以在规则中使用估计时间来在创建工作时自动拆分工作。</span><span class="sxs-lookup"><span data-stu-id="50db4-130">Additionally, you can use the estimated time in the rules for automatically splitting work during work creation.</span></span> <span data-ttu-id="50db4-131">这样，您可以基于完成任务的预期时间进行负载平衡工作。</span><span class="sxs-lookup"><span data-stu-id="50db4-131">In this way, you can load balance work, based on the expected time to complete the tasks.</span></span> 

<span data-ttu-id="50db4-132">用于处理工作项目的时间的分析有助于推动改善仓库工作人员的效率。</span><span class="sxs-lookup"><span data-stu-id="50db4-132">Analysis of the time that is used to process work items can help drive improvements in the warehouse workers’ efficiency.</span></span> <span data-ttu-id="50db4-133">以下报表可用于帮助您完成这一分析：</span><span class="sxs-lookup"><span data-stu-id="50db4-133">The following reports are available to help with this analysis:</span></span>

-   <span data-ttu-id="50db4-134">**按用户划分的人工** – 此报表基于对照预期时间的实际时间显示工作人员的工作效率。</span><span class="sxs-lookup"><span data-stu-id="50db4-134">**Labor by user** – This report shows worker productivity, based on actual times against expected times.</span></span>
-   <span data-ttu-id="50db4-135">**按工作交易记录类型划分的人工** – 您可以使用此报表调查特定仓库流程的效率低下。</span><span class="sxs-lookup"><span data-stu-id="50db4-135">**Labor by work transaction type** – You can use this report to investigate inefficiencies in specific warehouse processes.</span></span> <span data-ttu-id="50db4-136">例如，您注意到转移单的领料在本周需要的时间比前一周更长。</span><span class="sxs-lookup"><span data-stu-id="50db4-136">For example, you notice that picks for transfer orders are taking longer this week than in previous weeks.</span></span> <span data-ttu-id="50db4-137">那么，您可以使用此信息进行进一步调查。</span><span class="sxs-lookup"><span data-stu-id="50db4-137">You can then use this information for further investigation.</span></span>




