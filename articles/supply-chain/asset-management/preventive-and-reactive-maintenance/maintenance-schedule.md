---
title: 维护安排
description: 本主题介绍资产管理中的维护安排。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89938a4c5fd9a520c6582215a438670f73085228
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252934"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="356d7-103">维护安排</span><span class="sxs-lookup"><span data-stu-id="356d7-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="356d7-104">维护安排中包含预计要执行的所有预防性维护计划、维护请求和维护阶段的列表。可能已将某些安排行转换成了工作订单。</span><span class="sxs-lookup"><span data-stu-id="356d7-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="356d7-105">这四个维护安排视图稍有不同，具体取决于要查看哪些维护安排行。</span><span class="sxs-lookup"><span data-stu-id="356d7-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="356d7-106">菜单项</span><span class="sxs-lookup"><span data-stu-id="356d7-106">Menu item</span></span>                  | <span data-ttu-id="356d7-107">内容的描述</span><span class="sxs-lookup"><span data-stu-id="356d7-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="356d7-108">所有维护安排</span><span class="sxs-lookup"><span data-stu-id="356d7-108">All maintenance schedule</span></span>       | <span data-ttu-id="356d7-109">将显示所有维护安排行。</span><span class="sxs-lookup"><span data-stu-id="356d7-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="356d7-110">我的资产计划</span><span class="sxs-lookup"><span data-stu-id="356d7-110">My asset schedule</span></span>        | <span data-ttu-id="356d7-111">此列表中显示其中包含在您作为工人关联的功能位置(在[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)中设置)安装的资产的所有维护安排行。</span><span class="sxs-lookup"><span data-stu-id="356d7-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="356d7-112">打开维护安排行</span><span class="sxs-lookup"><span data-stu-id="356d7-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="356d7-113">此列表中显示状态为“已创建”（表示尚未转换为工作订单或尚未被放弃）的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="356d7-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="356d7-114">打开维护安排池</span><span class="sxs-lookup"><span data-stu-id="356d7-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="356d7-115">此列表中显示与工作订单池关联的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="356d7-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="356d7-116">如果一个维护安排行包含在多个工作订单池中(请参阅 [工作订单池](../work-orders/work-order-pools.md))，将为 **打开维护安排池** 中的每个池显示一条记录。</span><span class="sxs-lookup"><span data-stu-id="356d7-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="356d7-117">这是为了优化工作订单池中的筛选选项。</span><span class="sxs-lookup"><span data-stu-id="356d7-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="356d7-118">若要打开一个维护安排：</span><span class="sxs-lookup"><span data-stu-id="356d7-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="356d7-119">单击 **资产管理** > **常用** > **维护安排** > **所有维护安排** 或 **打开维护安排行** 或 **打开维护安排池**。</span><span class="sxs-lookup"><span data-stu-id="356d7-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="356d7-120">若要更新维护安排，请单击 **维护计划** 或 **维护阶段**。</span><span class="sxs-lookup"><span data-stu-id="356d7-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="356d7-121">可编辑维护安排行，方法是选择维护安排行，然后单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="356d7-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="356d7-122">例如，可以轻松更新作业的服务级别或负责工人。</span><span class="sxs-lookup"><span data-stu-id="356d7-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="356d7-123">只能编辑尚未与工作订单关联的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="356d7-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="356d7-124">可删除维护安排行，方法是在列表页中选择该维护安排行，然后单击 **删除**。</span><span class="sxs-lookup"><span data-stu-id="356d7-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="356d7-125">可放弃维护安排行，方法是在列表页中选择该维护安排行，然后单击 **放弃**。</span><span class="sxs-lookup"><span data-stu-id="356d7-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="356d7-126">此功能非常有用，例如，当一个资产有 2,000 公里的维护计划和 10,000 公里的维护计划时。</span><span class="sxs-lookup"><span data-stu-id="356d7-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="356d7-127">然后，您可能希望放弃基于 2,000 公里维护计划创建，并且与 10,000 公里、 20,000 公里、30,000 公里，以此类推的维护计划一致的行。</span><span class="sxs-lookup"><span data-stu-id="356d7-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="356d7-128">如果放弃与某个维护计划关联的维护安排行，安排维护计划时，始终不会再次显示该行。</span><span class="sxs-lookup"><span data-stu-id="356d7-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="356d7-129">如果希望选择的所有维护安排行包含在同一个工作订单池中，可以在 **所有维护安排** 中选择一些维护安排行，然后单击 **工作订单池**。</span><span class="sxs-lookup"><span data-stu-id="356d7-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="356d7-130">如果要对多个维护安排行进行相同调整，可以在 **所有维护安排** 或 **打开维护安排行** 或 **打开维护安排池** 中选择一些维护安排行，然后单击 **调整安排**。</span><span class="sxs-lookup"><span data-stu-id="356d7-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="356d7-131">可更改与所选维护安排行关联的预计开始日期和结束日期，服务级别，以及负责维护工人组或负责维护工人。</span><span class="sxs-lookup"><span data-stu-id="356d7-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="356d7-132">将维护安排行与工作订单关联之后，将在 **工作订单** 字段中显示工作订单 ID。</span><span class="sxs-lookup"><span data-stu-id="356d7-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="356d7-133">可在 **所有资产** 详细信息视图 > **资产维护计划** 快速选项卡上为资产选择维护计划。</span><span class="sxs-lookup"><span data-stu-id="356d7-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="356d7-134">以后，如果在 **所有资产** 中删除与资产关联的维护计划行，也将自动删除已根据维护计划创建且状态为“已创建”的所有维护计划行。</span><span class="sxs-lookup"><span data-stu-id="356d7-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="356d7-135">另请参阅[创建资产](../objects/create-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="356d7-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="356d7-136">下图显示 **所有维护安排** 列表页。</span><span class="sxs-lookup"><span data-stu-id="356d7-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![图 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]