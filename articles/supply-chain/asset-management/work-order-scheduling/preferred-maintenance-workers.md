---
title: 设置首选维护工人
description: 本主题说明如何在资产管理中设置首选维护工人。
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887403"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="304be-103">首选维护工人</span><span class="sxs-lookup"><span data-stu-id="304be-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="304be-104">可在工作订单安排期间创建有关分配哪些维护工人来完成工作订单的首选项。</span><span class="sxs-lookup"><span data-stu-id="304be-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="304be-105">此功能为可选功能，但是可帮助您根据工人技能和能力选择最有资格完成作业的维护工人。</span><span class="sxs-lookup"><span data-stu-id="304be-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="304be-106">因此，在工作订单安排期间，将使用**首选维护工人**中的设置来确定是否应将特定维护工人或工人组安排给某个工作订单。</span><span class="sxs-lookup"><span data-stu-id="304be-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="304be-107">将仅安排在安排时可用的维护工人。</span><span class="sxs-lookup"><span data-stu-id="304be-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="304be-108">如果安排期间某项首选维护工人设置与工作订单匹配，但是将该维护工人分配给了其他作业，将把工作订单安排给另一位可用维护工人。</span><span class="sxs-lookup"><span data-stu-id="304be-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="304be-109">设置首选维护工人之前，必须首先设置应该可供选择的维护工人和工人组。</span><span class="sxs-lookup"><span data-stu-id="304be-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="304be-110">有关如何设置维护工人和工人组的描述，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="304be-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="304be-111">设置首选工人</span><span class="sxs-lookup"><span data-stu-id="304be-111">Set up preferred workers</span></span>

<span data-ttu-id="304be-112">可以将首选维护工人或工人组关联到</span><span class="sxs-lookup"><span data-stu-id="304be-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="304be-113">贸易</span><span class="sxs-lookup"><span data-stu-id="304be-113">trade</span></span>  
- <span data-ttu-id="304be-114">维护作业类型变型</span><span class="sxs-lookup"><span data-stu-id="304be-114">maintenance job type variant</span></span>  
- <span data-ttu-id="304be-115">维护作业类型</span><span class="sxs-lookup"><span data-stu-id="304be-115">maintenance job type</span></span>  
- <span data-ttu-id="304be-116">维护作业类型类别</span><span class="sxs-lookup"><span data-stu-id="304be-116">maintenance job type category</span></span>  
- <span data-ttu-id="304be-117">asset / 资产</span><span class="sxs-lookup"><span data-stu-id="304be-117">asset</span></span>  
- <span data-ttu-id="304be-118">资产类型</span><span class="sxs-lookup"><span data-stu-id="304be-118">asset type</span></span>  

<span data-ttu-id="304be-119">或这些选项的组合。</span><span class="sxs-lookup"><span data-stu-id="304be-119">or a combination of those selections.</span></span> <span data-ttu-id="304be-120">为同一条记录选择的越多，设置越具体。</span><span class="sxs-lookup"><span data-stu-id="304be-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="304be-121">单击**资产管理** > **设置** > **工人** > **首选维护工人**。</span><span class="sxs-lookup"><span data-stu-id="304be-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="304be-122">单击**新建**创建一条新记录。</span><span class="sxs-lookup"><span data-stu-id="304be-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="304be-123">首先创建在上面的项目符号列表中显示的字段内未进行任何选择的“默认”维护工人或工人组设置。</span><span class="sxs-lookup"><span data-stu-id="304be-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="304be-124">这意味着仅在**首选维护工人组**字段或**首选维护工人**字段中进行选择。</span><span class="sxs-lookup"><span data-stu-id="304be-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="304be-125">下图中的示例显示，第一个记录中选择了“请求”来充当首选维护工人组。</span><span class="sxs-lookup"><span data-stu-id="304be-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="304be-126">如果在安排工作订单期间没有其他更具体的组合与工作订单的内容匹配，将在安排工作订单期间使用默认设置。</span><span class="sxs-lookup"><span data-stu-id="304be-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="304be-127">重复步骤 2 以创建新的记录。</span><span class="sxs-lookup"><span data-stu-id="304be-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="304be-128">进行所需选择，具体取决于首选工人或工人组的详细程度。</span><span class="sxs-lookup"><span data-stu-id="304be-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="304be-129">*示例：* 下图中的第六个记录内，选择了维护工人 Shawn Richardson 来充当首选工人。</span><span class="sxs-lookup"><span data-stu-id="304be-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="304be-130">安排包含资产“CH-BP1-03-02”和维护作业类型“设施评估”的工作订单时，如果他当时有空，将自动选择他。</span><span class="sxs-lookup"><span data-stu-id="304be-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="304be-131">通常当在安排工作订单期间选择了首选维护工人时，资产将在所有**首选维护工人**记录中查找可能的匹配项，始终首先查找最具体的组合。</span><span class="sxs-lookup"><span data-stu-id="304be-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="304be-132">如果未找到匹配项，将使用在**首选维护工人组**字段或**首选维护工人**字段中进行了选择的“默认”记录。</span><span class="sxs-lookup"><span data-stu-id="304be-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![图 1](media/02-work-order-scheduling.png)

<span data-ttu-id="304be-134">也可以设置在创建维护请求或工作订单时可选择的负责维护工人。</span><span class="sxs-lookup"><span data-stu-id="304be-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="304be-135">如果需要，可在**所有工作订单**和**所有维护请求**中编辑所选内容。</span><span class="sxs-lookup"><span data-stu-id="304be-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="304be-136">有关详细信息，请参阅[负责的维护工人](../setup-for-maintenance-requests/responsible-workers.md)。</span><span class="sxs-lookup"><span data-stu-id="304be-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="304be-137">安排工作订单期间，可以计算分数来确定哪些工人应完成与工作订单关联的作业（这些分数在**资产管理参数** > **工作订单计划编制**链接中设置）。</span><span class="sxs-lookup"><span data-stu-id="304be-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="304be-138">如果在安排工作订单期间两位或更多首选维护工人或负责的维护工人得到的分数相同，则随机选择一位工人。</span><span class="sxs-lookup"><span data-stu-id="304be-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="304be-139">否则，始终选择为其分配的分数最高的工人来完成工作订单。</span><span class="sxs-lookup"><span data-stu-id="304be-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

