---
title: 创建批处理作业
description: 批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4360cd7068658a170f5b44c2ce7c71c39c44fa8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679880"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="7270c-103">创建批处理作业</span><span class="sxs-lookup"><span data-stu-id="7270c-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7270c-104">批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。</span><span class="sxs-lookup"><span data-stu-id="7270c-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="7270c-105">通过使用创建了该作业的用户的安全凭据来运行批处理作业。</span><span class="sxs-lookup"><span data-stu-id="7270c-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="7270c-106">使用以下过程来创建批处理作业。</span><span class="sxs-lookup"><span data-stu-id="7270c-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="7270c-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="7270c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="7270c-108">创建批处理作业</span><span class="sxs-lookup"><span data-stu-id="7270c-108">Create the batch job</span></span>
1. <span data-ttu-id="7270c-109">转到 **导航窗格 > 模块 > 系统管理 > 查询 > 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="7270c-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="7270c-110">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="7270c-110">Click **New**.</span></span>
3. <span data-ttu-id="7270c-111">在 **作业描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7270c-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="7270c-112">在 **计划开始日期/时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7270c-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="7270c-113">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="7270c-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="7270c-114">创建重复执行</span><span class="sxs-lookup"><span data-stu-id="7270c-114">Create a recurrence</span></span>
1. <span data-ttu-id="7270c-115">在操作窗格上，单击 **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="7270c-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="7270c-116">单击 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="7270c-116">Click **Recurrence**.</span></span> <span data-ttu-id="7270c-117">使用这些选项输入一个重复执行的范围和模式。</span><span class="sxs-lookup"><span data-stu-id="7270c-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="7270c-118">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7270c-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="7270c-119">添加预警</span><span class="sxs-lookup"><span data-stu-id="7270c-119">Add alerts</span></span>
1. <span data-ttu-id="7270c-120">在操作窗格上，单击 **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="7270c-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="7270c-121">单击 **预警**。</span><span class="sxs-lookup"><span data-stu-id="7270c-121">Click **Alerts**.</span></span> <span data-ttu-id="7270c-122">指示批处理作业结束，出错或取消时是否希望发送预警消息。</span><span class="sxs-lookup"><span data-stu-id="7270c-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="7270c-123">然后指定是否要将预警显示为弹出消息。</span><span class="sxs-lookup"><span data-stu-id="7270c-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="7270c-124">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7270c-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="7270c-125">调整批处理作业状态</span><span class="sxs-lookup"><span data-stu-id="7270c-125">Adjust batch job status</span></span>
1. <span data-ttu-id="7270c-126">转到 **系统管理 > 查询 > 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="7270c-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="7270c-127">选择相应批处理作业。</span><span class="sxs-lookup"><span data-stu-id="7270c-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="7270c-128">在操作窗格上，单击 **批处理作业 > 功能 > 更改状态**。</span><span class="sxs-lookup"><span data-stu-id="7270c-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="7270c-129">选择相应的状态：</span><span class="sxs-lookup"><span data-stu-id="7270c-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="7270c-130">**预扣**：将批处理作业设置为 **预扣**，使其从批处理作业调度程序中扣除。</span><span class="sxs-lookup"><span data-stu-id="7270c-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="7270c-131">等同 *停止*。</span><span class="sxs-lookup"><span data-stu-id="7270c-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="7270c-132">**等待**：将批处理作业设置为 **等待**，使其等待批处理作业调度程序选取。</span><span class="sxs-lookup"><span data-stu-id="7270c-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="7270c-133">等同 *执行*。</span><span class="sxs-lookup"><span data-stu-id="7270c-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="7270c-134">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7270c-134">Click **OK**.</span></span>
