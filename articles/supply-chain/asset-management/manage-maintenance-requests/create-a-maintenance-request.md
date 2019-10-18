---
title: 创建维护请求
description: 本主题说明如何在资产管理中创建维护请求。
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e97d96a5485f17d0abc7c2fc2f8c4fdf4bbd4bb4
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024629"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="26678-103">创建维护请求</span><span class="sxs-lookup"><span data-stu-id="26678-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="26678-104">如果维护工人或生产工人发现需要维修设备，但是不能立即开展维修作业，可以使用维护请求。</span><span class="sxs-lookup"><span data-stu-id="26678-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="26678-105">**示例：** 一位维护工人正在进行维修，这时她发现必须维修同一位置的另一个资产。</span><span class="sxs-lookup"><span data-stu-id="26678-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="26678-106">但是，这位工人没有时间，或没有维修作业所需备件。</span><span class="sxs-lookup"><span data-stu-id="26678-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="26678-107">因此，她为该资产创建了维护请求，并输入了简短的问题说明。</span><span class="sxs-lookup"><span data-stu-id="26678-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="26678-108">Active maintenance requests section of the Related information pane on the right side of the **所有资产**或**有效资产**页面（**资产管理** \> **常用** \> **资产** \> **所有资产**或**有效资产**）右侧**相关信息**窗格的**有效维护请求**部分中显示与所选资产关联的有效维护请求。</span><span class="sxs-lookup"><span data-stu-id="26678-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="26678-109">选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**或**有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="26678-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="26678-110">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="26678-110">Select **New**.</span></span>
3. <span data-ttu-id="26678-111">在**创建请求**对话框的**维护请求类型**字段中，选择维护请求的类型。</span><span class="sxs-lookup"><span data-stu-id="26678-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="26678-112">将推荐默认类型。</span><span class="sxs-lookup"><span data-stu-id="26678-112">A default type is suggested.</span></span>
4. <span data-ttu-id="26678-113">在**描述**字段中，输入用于简要描述维护请求的名称或标题。</span><span class="sxs-lookup"><span data-stu-id="26678-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="26678-114">在**功能位置**和**资产**字段中，根据需要设置功能位置或资产，或功能位置和资产的组合。</span><span class="sxs-lookup"><span data-stu-id="26678-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="26678-115">创建维护请求时可以不选择资产，以后可以向该维护请求添加资产。</span><span class="sxs-lookup"><span data-stu-id="26678-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="26678-116">如果已登录的维护工人与该资产的关联资源有关，将自动设置**资产**字段。</span><span class="sxs-lookup"><span data-stu-id="26678-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="26678-117">如果已经为所选资产关联了维护请求，将在**创建请求**对话框顶部显示消息栏，告知您现有维护请求的 ID。</span><span class="sxs-lookup"><span data-stu-id="26678-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="26678-118">消息栏该告知您该资产是否涵盖在某个保修协议内。</span><span class="sxs-lookup"><span data-stu-id="26678-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="26678-119">在**服务级别**字段中，选择服务级别，用于指示请求的紧急程度。</span><span class="sxs-lookup"><span data-stu-id="26678-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="26678-120">如果在步骤 5 中选择了资产，可使用**故障特征**、**故障区域**和**故障类型**字段创建故障登记。</span><span class="sxs-lookup"><span data-stu-id="26678-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="26678-121">如果维护请求导致了维护停机时间，请输入停机时间的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="26678-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="26678-122">将把**启动人**字段自动设置为您的名称。</span><span class="sxs-lookup"><span data-stu-id="26678-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="26678-123">将把**实际开始时间**字段自动设置为当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="26678-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="26678-124">但是，您可以根据需要更改此值。</span><span class="sxs-lookup"><span data-stu-id="26678-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="26678-125">在**注释**字段中，输入所需的其他任何注释。</span><span class="sxs-lookup"><span data-stu-id="26678-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="26678-126">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="26678-126">Select **OK**.</span></span>

![图 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="26678-128">维护请求的后续处理</span><span class="sxs-lookup"><span data-stu-id="26678-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="26678-129">创建维护请求之后，将其转化为工作订单之前，应该更新有关该维护请求的各种信息。</span><span class="sxs-lookup"><span data-stu-id="26678-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="26678-130">通常由规划员或其他管理员工完成此任务。</span><span class="sxs-lookup"><span data-stu-id="26678-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="26678-131">在**所有维护请求**或**有效维护请求**页，选择要处理的请求，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="26678-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="26678-132">在详细信息视图中，可以更新各种信息。</span><span class="sxs-lookup"><span data-stu-id="26678-132">In the details view, you can update various information.</span></span> <span data-ttu-id="26678-133">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="26678-133">Here are some examples:</span></span>

- <span data-ttu-id="26678-134">选择并验证资产。</span><span class="sxs-lookup"><span data-stu-id="26678-134">Select and verify the asset.</span></span> <span data-ttu-id="26678-135">如果必须在以后选择其他资产，可以将**已验证资产**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="26678-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="26678-136">选择负责的维护工人组和/或负责的维护工人。</span><span class="sxs-lookup"><span data-stu-id="26678-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="26678-137">有关所需设置的详细信息，请参阅[负责的维护工人](../setup-for-maintenance-requests/responsible-workers.md)。</span><span class="sxs-lookup"><span data-stu-id="26678-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="26678-138">选择维护作业类型，并且如果此信息相关，则选择关联的维护作业变体和作业交易。</span><span class="sxs-lookup"><span data-stu-id="26678-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="26678-139">在**纬度**和**经度**字段中输入地理坐标。</span><span class="sxs-lookup"><span data-stu-id="26678-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="26678-140">将把向维护请求添加的所有坐标自动传输给关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="26678-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![图 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="26678-142">如果在创建维护请求时选择资产，则可向该资产添加一个故障。</span><span class="sxs-lookup"><span data-stu-id="26678-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="26678-143">创建维护请求之后，可以根据需要添加更多故障。</span><span class="sxs-lookup"><span data-stu-id="26678-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="26678-144">若要添加故障，请选择**所有维护请求**页中的**资产故障**。</span><span class="sxs-lookup"><span data-stu-id="26678-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
