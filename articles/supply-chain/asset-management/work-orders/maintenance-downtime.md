---
title: 工作订单的维护停机时间
description: 此主题介绍如何为工作订单中选择的资产创建维护停机时间登记。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 263a044a0a378e95ea271ac1c6f468f9e3287f26
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802717"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="88ee2-103">工作订单的维护停机时间</span><span class="sxs-lookup"><span data-stu-id="88ee2-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="88ee2-104">可以为工作订单中选择的资产创建维护停机时间登记。</span><span class="sxs-lookup"><span data-stu-id="88ee2-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="88ee2-105">如果要登记生产区域中一台或多台机器的维护停机时间，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="88ee2-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="88ee2-106">首先，创建要使用的维护停机时间原因代码，如**分解**和**计划停止**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="88ee2-107">此步骤在**维护停机时间原因代码**页面执行。</span><span class="sxs-lookup"><span data-stu-id="88ee2-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="88ee2-108">然后，可以在**维护停机时间**页面创建维护停机时间登记，并添加相关的维护停机时间原因代码。</span><span class="sxs-lookup"><span data-stu-id="88ee2-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="88ee2-109">创建维护停机原因代码</span><span class="sxs-lookup"><span data-stu-id="88ee2-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="88ee2-110">选择**资产管理** > **设置** > **工作订单** > **维护停机时间原因代码**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="88ee2-111">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-111">Select **New**.</span></span>

3. <span data-ttu-id="88ee2-112">在**维护停机时间原因代码**字段中，输入维护停机时间原因代码的 ID。</span><span class="sxs-lookup"><span data-stu-id="88ee2-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="88ee2-113">在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="88ee2-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="88ee2-114">如果原因代码应包含在资产的关键绩效指标 (KPI) 的计算中，请选中 **KPI 包括**复选框。</span><span class="sxs-lookup"><span data-stu-id="88ee2-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="88ee2-115">通常，KPI 计算中不应包括计划的停产，因为它们不会影响预计绩效。</span><span class="sxs-lookup"><span data-stu-id="88ee2-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="88ee2-116">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-116">Select **Save**.</span></span>

<span data-ttu-id="88ee2-117">下图显示**维护停机时间原因代码**页面的示例。</span><span class="sxs-lookup"><span data-stu-id="88ee2-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![图 1](media/15-work-orders.png)

<span data-ttu-id="88ee2-119">创建要使用的维护停机时间原因代码之后，可以为工作订单和资产创建维护停机时间登记。</span><span class="sxs-lookup"><span data-stu-id="88ee2-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="88ee2-120">创建维护停机时间登记</span><span class="sxs-lookup"><span data-stu-id="88ee2-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="88ee2-121">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="88ee2-122">选择工作订单，然后在**工作订单**选项卡上，在**资产**组中，选择**维护停机时间**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="88ee2-123">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-123">Select **New**.</span></span>

4. <span data-ttu-id="88ee2-124">在**开始时间**和**结束时间**字段中，定义维护停机时间登记的日期和时间间隔。</span><span class="sxs-lookup"><span data-stu-id="88ee2-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="88ee2-125">离开**结束时间**字段时，将在**持续时间**字段中自动插入以小时为单位的持续时间。</span><span class="sxs-lookup"><span data-stu-id="88ee2-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="88ee2-126">在**维护停机时间原因代码**字段中，选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="88ee2-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="88ee2-127">重复执行第 3 步到第 5 步，以添加更多登记。</span><span class="sxs-lookup"><span data-stu-id="88ee2-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="88ee2-128">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-128">Select **Save**.</span></span>

<span data-ttu-id="88ee2-129">下图显示了维护停机时间登记的示例。</span><span class="sxs-lookup"><span data-stu-id="88ee2-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![图 2](media/16-work-orders.png)

<span data-ttu-id="88ee2-131">用于计算维护停机时间登记的日历取决于在设置资产和参数时进行的选择。</span><span class="sxs-lookup"><span data-stu-id="88ee2-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="88ee2-132">如果在**所有资产**页面的**固定资产**快速选项卡上的**资源**字段中为资产选择资源，则使用为关联的资源组设置的日历，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="88ee2-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![图 3](media/17-work-orders.png)

<span data-ttu-id="88ee2-134">如果不为资产选择任何资源，则使用在**资产管理参数**页面选择的标准日历，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="88ee2-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![图 4](media/18-work-orders.png)

<span data-ttu-id="88ee2-136">要查看所有维护停机时间登记的概览，单击**资产管理** > **查询** > **维护停机时间**。</span><span class="sxs-lookup"><span data-stu-id="88ee2-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="88ee2-137">**资产管理**模块中使用的所有日历均在**组织管理** > **设置** > **日历** > **日历**中设置。</span><span class="sxs-lookup"><span data-stu-id="88ee2-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

