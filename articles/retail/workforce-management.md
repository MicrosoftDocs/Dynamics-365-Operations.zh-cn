---
title: "劳动力管理概览"
description: "此主题介绍如何使用劳动力管理 (WFM) 服务来利用熟悉的销售点 (POS) 客户端，现代 POS 和云 POS，使店长能够轻松管理劳动力。"
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a><span data-ttu-id="ebf64-103">劳动力管理概览</span><span class="sxs-lookup"><span data-stu-id="ebf64-103">Workforce management overview</span></span>

[!include[banner](includes/banner.md)]
    
<span data-ttu-id="ebf64-104">劳动力管理 (WFM) 服务利用熟悉的销售点 (POS) 客户端，现代 POS 和云 POS，使店长能够轻松管理劳动力。</span><span class="sxs-lookup"><span data-stu-id="ebf64-104">The Workforce management (WFM) service takes advantage of the familiar point of sale (POS) clients, Modern POS and Cloud POS, to let store managers easily manage their workforce.</span></span> <span data-ttu-id="ebf64-105">WFM 服务使用扩展框架下载 POS 中的相关包。</span><span class="sxs-lookup"><span data-stu-id="ebf64-105">The WFM service uses the extension framework to download the relevant packages in the POS.</span></span> <span data-ttu-id="ebf64-106">当关闭并重新打开 POS 时，这些包即下载完成。</span><span class="sxs-lookup"><span data-stu-id="ebf64-106">These packages are downloaded when the POS is closed and reopened.</span></span> <span data-ttu-id="ebf64-107">因此，当 Microsoft 发布 WFM 的新功能时，必须关闭并重新打开 POS 应用。</span><span class="sxs-lookup"><span data-stu-id="ebf64-107">Therefore, when Microsoft releases new features for WFM, the POS app must be closed and reopened.</span></span>

<span data-ttu-id="ebf64-108">店长可以使用该服务轻松创建和发布商店的每周工作计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-108">By using this service, store managers can easily create and publish weekly work schedule for their stores.</span></span> <span data-ttu-id="ebf64-109">商店工作人员可以迅速查看自己的计划以及同事的计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-109">Store workers can then quickly view their own schedules and the schedules of their colleagues.</span></span> <span data-ttu-id="ebf64-110">这样一来，他们可以了解谁将在分配的班次中与他们一起工作。</span><span class="sxs-lookup"><span data-stu-id="ebf64-110">In that way, they can learn who will be working with them during the assigned shifts.</span></span> <span data-ttu-id="ebf64-111">商店工作人员还可以创建缺勤、班次交换和班次提议请求。</span><span class="sxs-lookup"><span data-stu-id="ebf64-111">Store workers can also create requests for absence, shift swap, and shift offer.</span></span> <span data-ttu-id="ebf64-112">所有这些请求触发一个定义的工作流。</span><span class="sxs-lookup"><span data-stu-id="ebf64-112">All these requests trigger a defined workflow.</span></span>

<span data-ttu-id="ebf64-113">在班次中，商店工作人员可以利用 POS 客户端中内置的上下班打卡功能。</span><span class="sxs-lookup"><span data-stu-id="ebf64-113">During a shift, store workers can take advantage of the clock-in and clock-out feature that is built into the POS clients.</span></span> <span data-ttu-id="ebf64-114">之后，数据将被发送到总部 (HQ) 进行工资处理。</span><span class="sxs-lookup"><span data-stu-id="ebf64-114">The data is then sent to the headquarters (HQ) for payroll processing.</span></span> <span data-ttu-id="ebf64-115">上下班打卡功能是 POS 现有的一项功能。</span><span class="sxs-lookup"><span data-stu-id="ebf64-115">The clock-in and clock-out feature is an existing capability of the POS.</span></span> <span data-ttu-id="ebf64-116">有关设置和支持的方案的详细信息，请参阅[上班打卡和下班打卡](retail-time-attendance.md)。</span><span class="sxs-lookup"><span data-stu-id="ebf64-116">For more information about the setup and supported scenarios, see [Clock in and clock out](retail-time-attendance.md).</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="ebf64-117">支持的方案</span><span class="sxs-lookup"><span data-stu-id="ebf64-117">Supported scenarios</span></span>
<span data-ttu-id="ebf64-118">本节提供有关支持的方案的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ebf64-118">This section provides more information about the supported scenarios.</span></span>

- <span data-ttu-id="ebf64-119">**创建和发布计划** - WFM 服务使用在 HQ 中配置的 POS 权限来确定某个工作人员是否具有店长权限。</span><span class="sxs-lookup"><span data-stu-id="ebf64-119">**Create and publish schedules** – The WFM service uses the POS permissions that are configured in the HQ to determine whether a worker has store manager privileges.</span></span> <span data-ttu-id="ebf64-120">只有店长可以使用计划管理操作来创建和发布计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-120">Only store managers can create and publish schedules by using the Schedule management operation.</span></span> <span data-ttu-id="ebf64-121">他们可以将现有的工作班次从一位工作人员复制粘贴到另一位工作人员，从而快速创建计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-121">They can quickly create a schedule by copying and pasting an existing work shift from one worker to another worker.</span></span> <span data-ttu-id="ebf64-122">还可以通过将前面任何一周的计划导入到当前周的方式创建计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-122">They can also create a schedule by importing the schedule from any previous week to the current week.</span></span>

    <span data-ttu-id="ebf64-123">如果未发布计划，则计划处于草稿状态，与已发布的计划在外观上不一样。</span><span class="sxs-lookup"><span data-stu-id="ebf64-123">If a schedule isn't published, it's in a draft state and looks different than a published schedule.</span></span> <span data-ttu-id="ebf64-124">店长可以通过单击**发布**按钮发布任何一周的计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-124">Store managers can publish a schedule by clicking the **Publish** button for any week.</span></span> <span data-ttu-id="ebf64-125">发布一个星期的计划后，任何更改都会自动发布。</span><span class="sxs-lookup"><span data-stu-id="ebf64-125">After the schedule is published for a week, any changes are automatically published.</span></span> <span data-ttu-id="ebf64-126">更改示例包括添加或删除工作班次或缺勤或编辑工作班次或缺勤。</span><span class="sxs-lookup"><span data-stu-id="ebf64-126">Examples of changes include the addition or deletion of work shifts or absences, or edits to work shifts or absences.</span></span> <span data-ttu-id="ebf64-127">商店工作人员只能查看各周已经发布的计划。</span><span class="sxs-lookup"><span data-stu-id="ebf64-127">Store workers can view only schedules that have been published for various weeks.</span></span>
    
- <span data-ttu-id="ebf64-128">**创建和审核请求** - 商店工作人员可以创建三种类型的请求：</span><span class="sxs-lookup"><span data-stu-id="ebf64-128">**Create and approve requests** – Store workers can create three types of request:</span></span>

    - <span data-ttu-id="ebf64-129">请求缺勤</span><span class="sxs-lookup"><span data-stu-id="ebf64-129">Request absence</span></span>
    - <span data-ttu-id="ebf64-130">请求班次交换</span><span class="sxs-lookup"><span data-stu-id="ebf64-130">Request shift swap</span></span>
    - <span data-ttu-id="ebf64-131">请求班次提议</span><span class="sxs-lookup"><span data-stu-id="ebf64-131">Request shift offer</span></span>

    <span data-ttu-id="ebf64-132">可以使用计划请求操作创建这些请求。</span><span class="sxs-lookup"><span data-stu-id="ebf64-132">These requests can be created by using the Schedule requests operation.</span></span> <span data-ttu-id="ebf64-133">每个请求都遵循一个已定义的工作流，并且工作人员可以轻松查看其请求的当前状态。</span><span class="sxs-lookup"><span data-stu-id="ebf64-133">Each request follows a defined workflow, and workers can easily see the current status of their requests.</span></span>
    
    <span data-ttu-id="ebf64-134">缺勤请求自动发送给店长以供审核。</span><span class="sxs-lookup"><span data-stu-id="ebf64-134">Absence requests are automatically sent to the store manager for approval.</span></span> <span data-ttu-id="ebf64-135">如果存在多个店长，所有店长都可查看给定的请求，但只有一个店长可以批准或拒绝该请求。</span><span class="sxs-lookup"><span data-stu-id="ebf64-135">If there are multiple store managers, all managers can view a given request, but only one manager can approve or reject it.</span></span> <span data-ttu-id="ebf64-136">缺勤类型在零售总部中使用**零售**模块中的**休假和缺勤类型**页进行配置。</span><span class="sxs-lookup"><span data-stu-id="ebf64-136">The absence types are configured in the retail HQ by using the **Leave and absence types** page in the **Retail** module.</span></span> <span data-ttu-id="ebf64-137">在店长批准或拒绝请求之后，该请求将移至**历史记录**选项卡用于计划请求操作。</span><span class="sxs-lookup"><span data-stu-id="ebf64-137">After the store manager approves or rejects a request, it's moved to the **History** tab for the Schedule requests operation.</span></span>
    
    <span data-ttu-id="ebf64-138">班次交换或班次提议请求先发送到被请求的工作人员处。</span><span class="sxs-lookup"><span data-stu-id="ebf64-138">A shift swap or shift offer request first goes to the worker that the request was sent to.</span></span> <span data-ttu-id="ebf64-139">仅当该工作人员批准该请求后，店长才可以查看请求。</span><span class="sxs-lookup"><span data-stu-id="ebf64-139">The store manager can view the request only after this worker has approved it.</span></span> <span data-ttu-id="ebf64-140">因此，如果工作人员拒绝班次交换或班次提议请求，则经理不能查看该请求。</span><span class="sxs-lookup"><span data-stu-id="ebf64-140">Therefore, if the worker rejects the shift swap or shift offer request, the manager can't view it.</span></span> <span data-ttu-id="ebf64-141">创建请求的工作人员也可以在经理批准或拒绝该请求前取消该请求。</span><span class="sxs-lookup"><span data-stu-id="ebf64-141">The worker who created the request can also cancel it before the manager approves or denies it.</span></span>

- <span data-ttu-id="ebf64-142">**在计划视图中显示活动的商店工作人员** - 通过将某位工作人员与商店的员工通讯簿相关联等方式将该工作人员添加到商店后，该工作人员在 WFM 服务中可供调配。</span><span class="sxs-lookup"><span data-stu-id="ebf64-142">**Show the active store workers in the schedule view** – When a worker is added to a store by, for example, associating him or her with the store's employee address book, the worker becomes available for scheduling in the WFM service.</span></span> <span data-ttu-id="ebf64-143">在 HQ 中运行命名为**处理工作人员数据以进行劳动力管理**的重复批处理作业。</span><span class="sxs-lookup"><span data-stu-id="ebf64-143">A recurring batch job that is named **Process worker data for workforce management** is run in the HQ.</span></span> <span data-ttu-id="ebf64-144">该作业准备好要被发送到 Common Data Service (CDS) 的商店-工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="ebf64-144">This job prepares the store-worker associations that will be sent to the Common Data Service (CDS).</span></span>

    <span data-ttu-id="ebf64-145">从商店中删除工作人员时使用同一个流程。</span><span class="sxs-lookup"><span data-stu-id="ebf64-145">The same process is used when a worker is removed from a store.</span></span> <span data-ttu-id="ebf64-146">但是，被删除的工作人员仍然显示过去、当前和未来的周中是否有活动的工作班次或缺勤被分配到该工作人员。</span><span class="sxs-lookup"><span data-stu-id="ebf64-146">However, the worker who is removed is still shown for past, current, and future weeks if an active work shift or absence is assigned to that worker.</span></span> <span data-ttu-id="ebf64-147">因此，除非这些工作班次和缺勤被删除，否则这些周将继续显示被删除的工作人员。</span><span class="sxs-lookup"><span data-stu-id="ebf64-147">Therefore, unless these work shifts and absences are deleted, the removed worker will continue to be shown for these weeks.</span></span>

