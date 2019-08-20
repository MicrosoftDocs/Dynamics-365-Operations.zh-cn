---
title: 维护请求
description: 本主题概述资产管理中如何管理维护请求。
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
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847428"
---
# <a name="maintenance-requests"></a><span data-ttu-id="e64dc-103">维护请求</span><span class="sxs-lookup"><span data-stu-id="e64dc-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e64dc-104">维护请求是为了在尚未创建工作订单的情况下通知经理或规划员需要执行维护或维修作业时，创建的注释或声明。</span><span class="sxs-lookup"><span data-stu-id="e64dc-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="e64dc-105">如果认为维护请求的内容有效，可以根据维护请求创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="e64dc-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="e64dc-106">可以在资产管理中为任何资产创建维护请求。</span><span class="sxs-lookup"><span data-stu-id="e64dc-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="e64dc-107">可以根据公司使用维护请求的方式创建各种类型的维护请求。</span><span class="sxs-lookup"><span data-stu-id="e64dc-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="e64dc-108">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="e64dc-108">Here are some examples:</span></span>

- <span data-ttu-id="e64dc-109">维护请求</span><span class="sxs-lookup"><span data-stu-id="e64dc-109">Maintenance requests</span></span>
- <span data-ttu-id="e64dc-110">注释</span><span class="sxs-lookup"><span data-stu-id="e64dc-110">Notes</span></span>
- <span data-ttu-id="e64dc-111">更正或增强</span><span class="sxs-lookup"><span data-stu-id="e64dc-111">Corrections or enhancements</span></span>
- <span data-ttu-id="e64dc-112">投资</span><span class="sxs-lookup"><span data-stu-id="e64dc-112">Investments</span></span>
- <span data-ttu-id="e64dc-113">仓库维修（如果要接收来自其他位置的资产，以便执行维修或维护作业，在作业完成后退还资产，则使用此类型。）</span><span class="sxs-lookup"><span data-stu-id="e64dc-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="e64dc-114">查看维护请求</span><span class="sxs-lookup"><span data-stu-id="e64dc-114">View maintenance requests</span></span>

<span data-ttu-id="e64dc-115">若要查看维护请求，请选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**、**有效维护请求**或**我的功能位置维护请求**。</span><span class="sxs-lookup"><span data-stu-id="e64dc-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="e64dc-116">每个列表页显示与维护请求有关的部分信息。</span><span class="sxs-lookup"><span data-stu-id="e64dc-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![图 1](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="e64dc-118">使用**我的功能位置维护请求**列表页查看维护请求的列表，这些维护请求中包含您作为工人关联的功能位置或在此类功能位置安装的资产。</span><span class="sxs-lookup"><span data-stu-id="e64dc-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="e64dc-119">（有关如何为维护工人设置功能位置的信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。）</span><span class="sxs-lookup"><span data-stu-id="e64dc-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="e64dc-120">尽管客户帐户信息在资产服务管理（外部维护）中可用，但却在资产管理（内部维护）中不可用。</span><span class="sxs-lookup"><span data-stu-id="e64dc-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="e64dc-121">要打开记录的详细信息视图，请在**所有维护请求**列表页的网格视图中，选择**维护请求**列中的链接。</span><span class="sxs-lookup"><span data-stu-id="e64dc-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![图 2](media/02-manage-maintenance-requests.png)

<span data-ttu-id="e64dc-123">操作窗格上的按钮排列在选项卡上。</span><span class="sxs-lookup"><span data-stu-id="e64dc-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="e64dc-124">下表简述与资产管理有关的按钮。</span><span class="sxs-lookup"><span data-stu-id="e64dc-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="e64dc-125">按钮名称</span><span class="sxs-lookup"><span data-stu-id="e64dc-125">Button name</span></span>                      | <span data-ttu-id="e64dc-126">说明</span><span class="sxs-lookup"><span data-stu-id="e64dc-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="e64dc-127">编辑​​</span><span class="sxs-lookup"><span data-stu-id="e64dc-127">Edit</span></span>                             | <span data-ttu-id="e64dc-128">编辑所选维护请求。</span><span class="sxs-lookup"><span data-stu-id="e64dc-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-129">新</span><span class="sxs-lookup"><span data-stu-id="e64dc-129">New</span></span>                              | <span data-ttu-id="e64dc-130">创建新的维护请求。</span><span class="sxs-lookup"><span data-stu-id="e64dc-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="e64dc-131">删除</span><span class="sxs-lookup"><span data-stu-id="e64dc-131">Delete</span></span>                           | <span data-ttu-id="e64dc-132">删除所选维护请求。</span><span class="sxs-lookup"><span data-stu-id="e64dc-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-133">工作订单池</span><span class="sxs-lookup"><span data-stu-id="e64dc-133">Work order pool</span></span>                  | <span data-ttu-id="e64dc-134">将所选维护请求连接到工作订单池。</span><span class="sxs-lookup"><span data-stu-id="e64dc-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="e64dc-135">工作订单</span><span class="sxs-lookup"><span data-stu-id="e64dc-135">Work order</span></span>                       | <span data-ttu-id="e64dc-136">基于所选维护请求创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="e64dc-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-137">资产故障</span><span class="sxs-lookup"><span data-stu-id="e64dc-137">Asset fault</span></span>                      | <span data-ttu-id="e64dc-138">单击**资产故障**，可在其中为所选维护请求创建故障登记。</span><span class="sxs-lookup"><span data-stu-id="e64dc-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-139">工作订单</span><span class="sxs-lookup"><span data-stu-id="e64dc-139">Work orders</span></span>                      | <span data-ttu-id="e64dc-140">显示与所选维护请求相连的所有工作订单的列表。</span><span class="sxs-lookup"><span data-stu-id="e64dc-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-141">更新维护请求状态</span><span class="sxs-lookup"><span data-stu-id="e64dc-141">Update maintenance request state</span></span> | <span data-ttu-id="e64dc-142">更新维护请求的状态。</span><span class="sxs-lookup"><span data-stu-id="e64dc-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="e64dc-143">生命周期状态日志</span><span class="sxs-lookup"><span data-stu-id="e64dc-143">Lifecycle state log</span></span>              | <span data-ttu-id="e64dc-144">查看日志，其中显示所选维护请求的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="e64dc-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-145">维护请求详细信息</span><span class="sxs-lookup"><span data-stu-id="e64dc-145">Maintenance request details</span></span>      | <span data-ttu-id="e64dc-146">打印报告，其中显示所选维护请求的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e64dc-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-147">发送出借资产</span><span class="sxs-lookup"><span data-stu-id="e64dc-147">Send loan asset</span></span>                  | <span data-ttu-id="e64dc-148">选择应该用于临时替换所选维护请求中选择的资产的出借资产。</span><span class="sxs-lookup"><span data-stu-id="e64dc-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="e64dc-149">退还出借资产</span><span class="sxs-lookup"><span data-stu-id="e64dc-149">Return loan asset</span></span>                | <span data-ttu-id="e64dc-150">将出借资产登记为已退回。</span><span class="sxs-lookup"><span data-stu-id="e64dc-150">Register the loan asset as returned.</span></span> |

