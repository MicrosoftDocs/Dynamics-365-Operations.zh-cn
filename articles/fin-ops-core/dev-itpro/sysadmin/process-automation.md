---
title: 流程自动化
description: 本主题详细介绍如何通过流程自动化简单计划批处理服务器将运行的流程。
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920821"
---
# <a name="process-automation"></a><span data-ttu-id="24950-103">流程自动化</span><span class="sxs-lookup"><span data-stu-id="24950-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="24950-104">可通过流程自动化简单计划批处理服务器将运行的流程。</span><span class="sxs-lookup"><span data-stu-id="24950-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="24950-105">最终用户可通过更新后的计划工作日历视图查看和处理计划的工作和已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="24950-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="24950-106">系统管理</span><span class="sxs-lookup"><span data-stu-id="24950-106">Administration</span></span>

<span data-ttu-id="24950-107">系统管理模块中 **设置** 菜单下提供所有流程自动化的集中管理页面。</span><span class="sxs-lookup"><span data-stu-id="24950-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="24950-108">此页将列出系统中设置的所有自动化流程（系列）。</span><span class="sxs-lookup"><span data-stu-id="24950-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="24950-109">还将允许您直接从此页面添加新的流程自动化。</span><span class="sxs-lookup"><span data-stu-id="24950-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="24950-110">设置系列后，可以从此列表管理每个系列。</span><span class="sxs-lookup"><span data-stu-id="24950-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="24950-111">可以选择编辑整个系列，将其删除，查看列表视图中的所有发生次数，或在要暂停计划的工作一段时间时禁用系列。</span><span class="sxs-lookup"><span data-stu-id="24950-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="24950-112">禁用此功能后，将不会显示在功能管理中禁用的任何流程。</span><span class="sxs-lookup"><span data-stu-id="24950-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="24950-113">此外，流程自动化计划引擎不会为禁用的功能计划任何事件或后台流程。</span><span class="sxs-lookup"><span data-stu-id="24950-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="24950-114">重新启用此功能将导致过去计划的任何事件或后台流程立即运行。</span><span class="sxs-lookup"><span data-stu-id="24950-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="24950-115">流程自动化计划引擎依赖于系统批处理作业 **流程自动化轮询系统作业** 运行。</span><span class="sxs-lookup"><span data-stu-id="24950-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="24950-116">任何时候都不应该更改或篡改此作业。</span><span class="sxs-lookup"><span data-stu-id="24950-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="24950-117">日历视图</span><span class="sxs-lookup"><span data-stu-id="24950-117">Calendar view</span></span>

<span data-ttu-id="24950-118">流程自动化的一个主要优势是，可以在简单的日历视图中查看计划的工作。</span><span class="sxs-lookup"><span data-stu-id="24950-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="24950-119">可通过此视图一次查看一周的工作。</span><span class="sxs-lookup"><span data-stu-id="24950-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="24950-120">您将在 **流程自动化** 页面右侧看到此视图。</span><span class="sxs-lookup"><span data-stu-id="24950-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="24950-121">将使用为所选系列计划的工作填充此视图。</span><span class="sxs-lookup"><span data-stu-id="24950-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="24950-122">[![流程自动化日历](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="24950-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="24950-123">发生次数更改</span><span class="sxs-lookup"><span data-stu-id="24950-123">Occurrence changes</span></span>

<span data-ttu-id="24950-124">可以修改每个发生次数，不会影响其来源系列定义的其他发生次数。</span><span class="sxs-lookup"><span data-stu-id="24950-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="24950-125">可以从日历编辑计划的工作的发生次数，方法是选择 **查看/编辑** 按钮，然后选择 **发生次数**。</span><span class="sxs-lookup"><span data-stu-id="24950-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="24950-126">通过此页面，您可以访问系列设置向导中最初显示的所有设置，并且可以为所选发生次数进行一次性更改。</span><span class="sxs-lookup"><span data-stu-id="24950-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="24950-127">也可以通过在日历视图中选择 **禁用** 按钮关闭计划的工作的发生次数。</span><span class="sxs-lookup"><span data-stu-id="24950-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="24950-128">开发人员文档</span><span class="sxs-lookup"><span data-stu-id="24950-128">Developer documentation</span></span>

<span data-ttu-id="24950-129">流程自动化框架允许开发人员扩展流程自动化框架。</span><span class="sxs-lookup"><span data-stu-id="24950-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="24950-130">[流程自动化框架](../process-automation/process-automation-framework.md)文档介绍如何创建通过流程自动化向导计划的批处理服务器需要运行的自定义流程，以及如何在日历视图中自动显示。</span><span class="sxs-lookup"><span data-stu-id="24950-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
