---
title: 设置首选维护工人
description: 本主题说明如何在资产管理中设置首选维护工人。
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888921"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="7a337-103">设置首选维护工人</span><span class="sxs-lookup"><span data-stu-id="7a337-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7a337-104">在工作订单计划期间，您可以优先选择要分配哪个维护工人或工作人员组来完成工作订单。</span><span class="sxs-lookup"><span data-stu-id="7a337-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="7a337-105">此功能为可选功能，但是可帮助您根据工人技能和能力选择最有资格完成作业的维护工人。</span><span class="sxs-lookup"><span data-stu-id="7a337-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="7a337-106">将仅安排在安排时可用的维护工人。</span><span class="sxs-lookup"><span data-stu-id="7a337-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="7a337-107">如果安排期间某项首选维护工人设置与工作订单匹配，但是将该维护工人分配给了其他作业，将把工作订单安排给另一位可用维护工人。</span><span class="sxs-lookup"><span data-stu-id="7a337-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="7a337-108">在设置首选维护工人之前，必须首先设置维护工人和工作人员组。</span><span class="sxs-lookup"><span data-stu-id="7a337-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="7a337-109">有关如何设置维护工人和工作人员组的描述，请参阅[维护工人和工作人员组](../setup-for-objects/workers-and-worker-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="7a337-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="7a337-110">设置首选工人</span><span class="sxs-lookup"><span data-stu-id="7a337-110">Set up preferred workers</span></span>

<span data-ttu-id="7a337-111">可以将首选维护工人或工作人员组关联到以下一项或多项：</span><span class="sxs-lookup"><span data-stu-id="7a337-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="7a337-112">贸易</span><span class="sxs-lookup"><span data-stu-id="7a337-112">trade</span></span>  
- <span data-ttu-id="7a337-113">维护作业类型变型</span><span class="sxs-lookup"><span data-stu-id="7a337-113">maintenance job type variant</span></span>  
- <span data-ttu-id="7a337-114">维护作业类型</span><span class="sxs-lookup"><span data-stu-id="7a337-114">maintenance job type</span></span>  
- <span data-ttu-id="7a337-115">维护作业类型类别</span><span class="sxs-lookup"><span data-stu-id="7a337-115">maintenance job type category</span></span>  
- <span data-ttu-id="7a337-116">asset / 资产</span><span class="sxs-lookup"><span data-stu-id="7a337-116">asset</span></span>  
- <span data-ttu-id="7a337-117">资产类型</span><span class="sxs-lookup"><span data-stu-id="7a337-117">asset type</span></span>  

<span data-ttu-id="7a337-118">为同一条记录选择的越多，设置越具体。</span><span class="sxs-lookup"><span data-stu-id="7a337-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="7a337-119">单击**资产管理** > **设置** > **工人** > **首选维护工人**。</span><span class="sxs-lookup"><span data-stu-id="7a337-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="7a337-120">单击**新建**创建一条新记录。</span><span class="sxs-lookup"><span data-stu-id="7a337-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="7a337-121">首先创建一个“默认”维护工人或工作人员组。</span><span class="sxs-lookup"><span data-stu-id="7a337-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="7a337-122">这意味着仅在**首选维护工人组**字段或**首选维护工人**字段中进行选择。</span><span class="sxs-lookup"><span data-stu-id="7a337-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="7a337-123">下面屏幕截图中的示例显示，第一个记录中选择了“请求”来充当**首选维护工人组**。</span><span class="sxs-lookup"><span data-stu-id="7a337-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="7a337-124">如果在安排工作订单期间没有其他更具体的组合与工作订单的内容匹配，将使用默认设置。</span><span class="sxs-lookup"><span data-stu-id="7a337-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="7a337-125">重复步骤 2 以创建新的记录。</span><span class="sxs-lookup"><span data-stu-id="7a337-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="7a337-126">进行所需选择，具体取决于首选工人或工人组的详细程度。</span><span class="sxs-lookup"><span data-stu-id="7a337-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="7a337-127">*示例：* 下面屏幕截图中的第六个记录内，选择了维护工人 Shawn Richardson 来充当首选工人。</span><span class="sxs-lookup"><span data-stu-id="7a337-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="7a337-128">安排包含资产“CH-BP1-03-02”和维护作业类型“设施评估”的工作订单时，如果他当时有空，将自动选择他。</span><span class="sxs-lookup"><span data-stu-id="7a337-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="7a337-129">通常当在安排工作订单期间选择了首选维护工人时，资产将在所有**首选维护工人**记录中查找可能的匹配项，始终首先查找最具体的组合。</span><span class="sxs-lookup"><span data-stu-id="7a337-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="7a337-130">如果未找到匹配项，将使用在**首选维护工人组**字段或**首选维护工人**字段中进行了选择的“默认”记录。</span><span class="sxs-lookup"><span data-stu-id="7a337-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![图 1](media/02-work-order-scheduling.png)

<span data-ttu-id="7a337-132">也可以设置在创建维护请求或工作订单时可选择的*负责*维护工人。</span><span class="sxs-lookup"><span data-stu-id="7a337-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="7a337-133">如果需要，可在**所有工作订单**和**所有维护请求**中编辑所选内容。</span><span class="sxs-lookup"><span data-stu-id="7a337-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="7a337-134">有关详细信息，请参阅[负责维护工人](../setup-for-maintenance-requests/responsible-workers.md)。</span><span class="sxs-lookup"><span data-stu-id="7a337-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="7a337-135">安排工作订单期间，可以计算分数来确定哪些工人应完成与工作订单关联的作业（这些分数在**资产管理参数** > **工作订单计划编制**链接中设置）。</span><span class="sxs-lookup"><span data-stu-id="7a337-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="7a337-136">如果在安排工作订单期间两位或更多首选维护工人或负责的维护工人得到的分数相同，则随机选择一位工人。</span><span class="sxs-lookup"><span data-stu-id="7a337-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="7a337-137">否则，始终选择为其分配的分数最高的工人来完成工作订单。</span><span class="sxs-lookup"><span data-stu-id="7a337-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

