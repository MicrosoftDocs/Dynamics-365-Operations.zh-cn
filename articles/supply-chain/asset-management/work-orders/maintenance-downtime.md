---
title: 维护停机时间
description: 本主题介绍资产管理中的维护停机时间。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918236"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="9b248-103">维护停机时间</span><span class="sxs-lookup"><span data-stu-id="9b248-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9b248-104">可以为工作订单中选择的资产创建维护停机时间登记。</span><span class="sxs-lookup"><span data-stu-id="9b248-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="9b248-105">如果要登记生产区域中一台或多台机器的维护停机时间，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="9b248-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="9b248-106">首先，创建要使用的维护停机时间原因代码，例如，分解和计划停止。</span><span class="sxs-lookup"><span data-stu-id="9b248-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="9b248-107">此操作在**维护停机时间原因代码**中执行。</span><span class="sxs-lookup"><span data-stu-id="9b248-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="9b248-108">接下来，可以在**维护停机时间**中创建维护停机时间登记，并添加相关原因代码。</span><span class="sxs-lookup"><span data-stu-id="9b248-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="9b248-109">创建维护停机原因代码</span><span class="sxs-lookup"><span data-stu-id="9b248-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="9b248-110">单击**资产管理** > **设置** > **工作订单** > **维护停机时间原因代码**。</span><span class="sxs-lookup"><span data-stu-id="9b248-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="9b248-111">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b248-111">Click **New**.</span></span>

3. <span data-ttu-id="9b248-112">在**维护停机时间原因代码**字段中插入 ID。</span><span class="sxs-lookup"><span data-stu-id="9b248-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="9b248-113">在**名称**字段中插入原因代码的名称。</span><span class="sxs-lookup"><span data-stu-id="9b248-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="9b248-114">如果资产 KPI 计算中应该包含原因代码，请选中 **KPI 包括**复选框。</span><span class="sxs-lookup"><span data-stu-id="9b248-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="9b248-115">KPI 计算中通常不应包括计划的停产，因为它们不会影响预计绩效。</span><span class="sxs-lookup"><span data-stu-id="9b248-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="9b248-116">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9b248-116">Click **Save**.</span></span>

![图 1](media/15-work-orders.png)


<span data-ttu-id="9b248-118">创建要使用的维护停机时间原因代码之后，可以为工作订单和资产创建维护停机时间登记。</span><span class="sxs-lookup"><span data-stu-id="9b248-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="9b248-119">创建维护停机时间登记</span><span class="sxs-lookup"><span data-stu-id="9b248-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="9b248-120">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="9b248-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9b248-121">选择工作订单，然后单击**维护停机时间**。</span><span class="sxs-lookup"><span data-stu-id="9b248-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="9b248-122">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="9b248-122">Click **New**.</span></span>

4. <span data-ttu-id="9b248-123">在**开始时间**和**结束时间**字段中插入维护停机时间登记的日期和时间间隔。</span><span class="sxs-lookup"><span data-stu-id="9b248-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="9b248-124">离开**结束时间**字段时，将在**持续时间**字段中自动插入以小时为单位的持续时间。</span><span class="sxs-lookup"><span data-stu-id="9b248-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="9b248-125">在**维护停机时间原因代码**字段中选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="9b248-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="9b248-126">如果要添加更多登记，请重复步骤 3-6。</span><span class="sxs-lookup"><span data-stu-id="9b248-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="9b248-127">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="9b248-127">Click **Save**.</span></span>


![图 2](media/16-work-orders.png)


<span data-ttu-id="9b248-129">用于计算维护停机时间登记的日历取决于在设置资产和参数时进行的选择。</span><span class="sxs-lookup"><span data-stu-id="9b248-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="9b248-130">如果在**资产** > **固定资产**快速选项卡 > **资源**字段中为资产选择资源，则使用为关联的资源组设置的日历，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="9b248-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![图 3](media/17-work-orders.png)


<span data-ttu-id="9b248-132">如果不为资产选择任何资源，则使用**资产管理参数**中选择的标准日历，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="9b248-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![图 4](media/18-work-orders.png)


<span data-ttu-id="9b248-134">单击**企业资产管理** > **查询** > **维护停机时间**以查看所有维护停机时间登记的概览。</span><span class="sxs-lookup"><span data-stu-id="9b248-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="9b248-135">**资产管理**模块中使用的所有日历均在**组织管理** > **设置** > **日历** > **日历**中设置。</span><span class="sxs-lookup"><span data-stu-id="9b248-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

