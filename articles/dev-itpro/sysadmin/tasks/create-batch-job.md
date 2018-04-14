--- 
title: "创建批处理作业"
description: "批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。"
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bd5cd866693a39139b77f076e8e57bbcc1e10ef8
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-batch-job"></a><span data-ttu-id="f2550-103">创建批处理作业</span><span class="sxs-lookup"><span data-stu-id="f2550-103">Create a batch job</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2550-104">批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。</span><span class="sxs-lookup"><span data-stu-id="f2550-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="f2550-105">通过使用创建了该作业的用户的安全凭据来运行批处理作业。</span><span class="sxs-lookup"><span data-stu-id="f2550-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="f2550-106">使用以下过程来创建批处理作业。</span><span class="sxs-lookup"><span data-stu-id="f2550-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="f2550-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f2550-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="f2550-108">创建批处理作业</span><span class="sxs-lookup"><span data-stu-id="f2550-108">Create the batch job</span></span>
1. <span data-ttu-id="f2550-109">转到“系统管理”>“查询”>“批处理作业”。</span><span class="sxs-lookup"><span data-stu-id="f2550-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="f2550-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f2550-110">Click New.</span></span>
3. <span data-ttu-id="f2550-111">在“作业描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f2550-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="f2550-112">在“计划开始日期/时间”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f2550-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="f2550-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f2550-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="f2550-114">创建重复执行</span><span class="sxs-lookup"><span data-stu-id="f2550-114">Create a recurrence</span></span>
1. <span data-ttu-id="f2550-115">在操作窗格上，单击“批处理作业”。</span><span class="sxs-lookup"><span data-stu-id="f2550-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="f2550-116">单击“重复执行”。</span><span class="sxs-lookup"><span data-stu-id="f2550-116">Click Recurrence.</span></span>
    * <span data-ttu-id="f2550-117">使用这些选项输入一个重复执行的范围和模式。</span><span class="sxs-lookup"><span data-stu-id="f2550-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="f2550-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2550-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="f2550-119">添加预警</span><span class="sxs-lookup"><span data-stu-id="f2550-119">Add alerts</span></span>
1. <span data-ttu-id="f2550-120">在操作窗格上，单击“批处理作业”。</span><span class="sxs-lookup"><span data-stu-id="f2550-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="f2550-121">单击“预警”。</span><span class="sxs-lookup"><span data-stu-id="f2550-121">Click Alerts.</span></span>
    * <span data-ttu-id="f2550-122">指示批处理作业结束，出错或取消时是否希望发送预警消息。</span><span class="sxs-lookup"><span data-stu-id="f2550-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="f2550-123">然后指定是否要将预警显示为弹出消息。</span><span class="sxs-lookup"><span data-stu-id="f2550-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="f2550-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2550-124">Click OK.</span></span>


