---
title: 服务间隔
description: 服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10078cbd02209126e9655b823fcf844b692a4794
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562641"
---
# <a name="service-intervals"></a><span data-ttu-id="29194-103">服务间隔</span><span class="sxs-lookup"><span data-stu-id="29194-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29194-104">服务协议间隔指示在您自动创建服务订单时为服务协议行创建服务订单行所采用的频率。</span><span class="sxs-lookup"><span data-stu-id="29194-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="29194-105">在您自动创建服务订单时，将从该协议行的开始日期根据您为服务协议行指定的间隔创建服务订单行。</span><span class="sxs-lookup"><span data-stu-id="29194-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="29194-106">如果**服务协议**页面中某一服务协议行的**间隔**字段为空，则该行是一次性事件，不用于重复创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="29194-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="29194-107">示例</span><span class="sxs-lookup"><span data-stu-id="29194-107">Example</span></span>

<span data-ttu-id="29194-108">此示例阐释服务间隔将如何影响在服务订单上的服务协议行和服务订单行。</span><span class="sxs-lookup"><span data-stu-id="29194-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="29194-109">创建服务协议</span><span class="sxs-lookup"><span data-stu-id="29194-109">Create a service agreement</span></span>

<span data-ttu-id="29194-110">首先，创建一个服务协议，并将**合并服务订单**选项设置为**按服务协议**。</span><span class="sxs-lookup"><span data-stu-id="29194-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="29194-111">单击**服务协议**</span><span class="sxs-lookup"><span data-stu-id="29194-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="29194-112">在**新建**组中的**服务协议**选项卡上的**操作窗格**上，单击**服务协议**创建新的服务协议。</span><span class="sxs-lookup"><span data-stu-id="29194-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="29194-113">输入描述，在**项目 ID** 字段中选择某一项目，并在**开始日期**字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="29194-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="29194-114">在**合并服务订单** 字段中，选择**按服务协议**。</span><span class="sxs-lookup"><span data-stu-id="29194-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="29194-115">您现在创建了以下服务协议：</span><span class="sxs-lookup"><span data-stu-id="29194-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="29194-116">Project</span><span class="sxs-lookup"><span data-stu-id="29194-116">Project</span></span>      | <span data-ttu-id="29194-117">开始日期</span><span class="sxs-lookup"><span data-stu-id="29194-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29194-118">您的项目</span><span class="sxs-lookup"><span data-stu-id="29194-118">Your project</span></span> | <span data-ttu-id="29194-119">为项目指定的日期。</span><span class="sxs-lookup"><span data-stu-id="29194-119">The date you specified for the project.</span></span> <span data-ttu-id="29194-120">在此示例中，使用了当前日期。</span><span class="sxs-lookup"><span data-stu-id="29194-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="29194-121">创建服务协议行</span><span class="sxs-lookup"><span data-stu-id="29194-121">Create a service agreement line</span></span>

<span data-ttu-id="29194-122">接下来，您创建交易记录类型为**工时**的服务协议行。</span><span class="sxs-lookup"><span data-stu-id="29194-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="29194-123">为了完成示例的这一部分，您必须在**服务间隔**页面中创建服务间隔为 10 天。</span><span class="sxs-lookup"><span data-stu-id="29194-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="29194-124">选择您刚创建的服务协议。</span><span class="sxs-lookup"><span data-stu-id="29194-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="29194-125">在**行**快速选项卡上，单击**添加**按钮以在**服务协议**页面的下部窗格中创建一个新行。</span><span class="sxs-lookup"><span data-stu-id="29194-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="29194-126">在**交易记录类型**字段中选择**工时**。</span><span class="sxs-lookup"><span data-stu-id="29194-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="29194-127">在**工作人员**字段中，选择要提供服务的工作人员。</span><span class="sxs-lookup"><span data-stu-id="29194-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="29194-128">在**服务间隔**字段中，选择 10 天的服务间隔。</span><span class="sxs-lookup"><span data-stu-id="29194-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="29194-129">现在您已使用以下信息创建了一个服务协议行：</span><span class="sxs-lookup"><span data-stu-id="29194-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="29194-130">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="29194-130">Transaction type</span></span> | <span data-ttu-id="29194-131">入职日期</span><span class="sxs-lookup"><span data-stu-id="29194-131">Start date</span></span>                               | <span data-ttu-id="29194-132">服务间隔</span><span class="sxs-lookup"><span data-stu-id="29194-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="29194-133">工时</span><span class="sxs-lookup"><span data-stu-id="29194-133">Hour</span></span>             | <span data-ttu-id="29194-134">当前日期。</span><span class="sxs-lookup"><span data-stu-id="29194-134">The current date.</span></span>                        | <span data-ttu-id="29194-135">每 10 天</span><span class="sxs-lookup"><span data-stu-id="29194-135">Every 10 days</span></span>    |
| <span data-ttu-id="29194-136">工作线程</span><span class="sxs-lookup"><span data-stu-id="29194-136">Worker</span></span>           | <span data-ttu-id="29194-137">要执行服务的工作人员。</span><span class="sxs-lookup"><span data-stu-id="29194-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="29194-138">不存在为该行指定的时间范围。</span><span class="sxs-lookup"><span data-stu-id="29194-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="29194-139">创建计划的服务订单</span><span class="sxs-lookup"><span data-stu-id="29194-139">Create planned service orders</span></span>

<span data-ttu-id="29194-140">您现在可以为下个月创建计划的服务订单和服务订单行。</span><span class="sxs-lookup"><span data-stu-id="29194-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="29194-141">在**服务协议**页面**操作窗格**上的**交付**选项卡中，单击**计划服务订单**。</span><span class="sxs-lookup"><span data-stu-id="29194-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="29194-142">在**创建服务订单**页面中，在**开始日期**字段中输入当前日期，在**结束日期**字段中输入距离当前日期一个月的日期。</span><span class="sxs-lookup"><span data-stu-id="29194-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="29194-143">将**工时**滑块设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="29194-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="29194-144">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="29194-144">Click **OK**.</span></span>

<span data-ttu-id="29194-145">因为不存在针对服务订单的分组（由**合并服务订单**字段中的**按服务协议**选项定义），所以，为每个服务订单创建一个服务订单行。</span><span class="sxs-lookup"><span data-stu-id="29194-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="29194-146">服务订单已创建</span><span class="sxs-lookup"><span data-stu-id="29194-146">Service orders created</span></span>

<span data-ttu-id="29194-147">在您在**创建服务订单**对话框中指定的时间范围中，已创建三个服务订单行。</span><span class="sxs-lookup"><span data-stu-id="29194-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="29194-148">您可以在**服务协议**页面中查看服务订单行（**操作窗格** \> **交付** 选项卡 \> **查看**按钮）。</span><span class="sxs-lookup"><span data-stu-id="29194-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29194-149">相关主题</span><span class="sxs-lookup"><span data-stu-id="29194-149">Related topics</span></span>

[<span data-ttu-id="29194-150">设置服务间隔</span><span class="sxs-lookup"><span data-stu-id="29194-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

