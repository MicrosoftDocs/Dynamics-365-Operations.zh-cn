---
title: 同步资源产能
description: 此主题介绍如何在日历与项目之间同步资源的产能。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760482"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="5848b-103">同步资源产能</span><span class="sxs-lookup"><span data-stu-id="5848b-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5848b-104">资源同步流程帮助确保日历和基础日历信息深入到项目资源计划。</span><span class="sxs-lookup"><span data-stu-id="5848b-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="5848b-105">如果更改日历，流程对项目资源计划进行所需的更新。</span><span class="sxs-lookup"><span data-stu-id="5848b-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="5848b-106">因为日历的资源信息提前同步，这些流程还有助于改进性能。</span><span class="sxs-lookup"><span data-stu-id="5848b-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="5848b-107">因此，资源计划信息的更新更快。</span><span class="sxs-lookup"><span data-stu-id="5848b-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="5848b-108">我们建议您批量计划流程，而不是一次计划一个。</span><span class="sxs-lookup"><span data-stu-id="5848b-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="5848b-109">否则，某些员工可能忘记上次同步信息的起迄日期。</span><span class="sxs-lookup"><span data-stu-id="5848b-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="5848b-110">如果不使用起迄日期，可能在日期同步时发生间隔。</span><span class="sxs-lookup"><span data-stu-id="5848b-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![日历同步](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="5848b-112">同步资源产能汇总</span><span class="sxs-lookup"><span data-stu-id="5848b-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="5848b-113">同步流程被设计为同步所有资源日历信息。</span><span class="sxs-lookup"><span data-stu-id="5848b-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="5848b-114">此信息包括有关对项目的资源日历产能表进行的任何更改的基本日历信息。</span><span class="sxs-lookup"><span data-stu-id="5848b-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="5848b-115">如果在项目中添加新的资源，同步可以帮助确保更新的日历信息可用。</span><span class="sxs-lookup"><span data-stu-id="5848b-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="5848b-116">此同步随时都可以进行。</span><span class="sxs-lookup"><span data-stu-id="5848b-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="5848b-117">我们建议您使用批次执行。</span><span class="sxs-lookup"><span data-stu-id="5848b-117">We recommend that you use a batch.</span></span> <span data-ttu-id="5848b-118">选项在同步产能预留中可用。</span><span class="sxs-lookup"><span data-stu-id="5848b-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="5848b-119">选择**项目管理与核算** &gt; **定期** &gt; **产能同步** &gt; **同步资源产能汇总**。</span><span class="sxs-lookup"><span data-stu-id="5848b-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="5848b-120">设置下表中的选项。</span><span class="sxs-lookup"><span data-stu-id="5848b-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="5848b-121">选项</span><span class="sxs-lookup"><span data-stu-id="5848b-121">Option</span></span>      | <span data-ttu-id="5848b-122">说明</span><span class="sxs-lookup"><span data-stu-id="5848b-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="5848b-123">期间代码</span><span class="sxs-lookup"><span data-stu-id="5848b-123">Period code</span></span> | <span data-ttu-id="5848b-124">选择性地选择总帐日期间隔代码，以设置资源产能汇总的同步流程的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="5848b-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="5848b-125">入职日期</span><span class="sxs-lookup"><span data-stu-id="5848b-125">Start date</span></span>  | <span data-ttu-id="5848b-126">输入资源产能汇总的同步流程的开始日期。</span><span class="sxs-lookup"><span data-stu-id="5848b-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="5848b-127">结束日期</span><span class="sxs-lookup"><span data-stu-id="5848b-127">End date</span></span>    | <span data-ttu-id="5848b-128">输入资源产能汇总的同步流程的结束日期。</span><span class="sxs-lookup"><span data-stu-id="5848b-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="5848b-129">[![同步流程](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="5848b-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
