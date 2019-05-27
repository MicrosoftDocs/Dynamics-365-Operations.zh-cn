---
title: 创建服务任务关系
description: 您可以将服务任务和服务管理或服务订单进行关联，以便介绍针对协议或订单要完成了的服务任务。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552107"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="432c5-103">创建服务任务关系</span><span class="sxs-lookup"><span data-stu-id="432c5-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="432c5-104">您可以将服务任务和服务管理或服务订单进行关联，以便介绍针对协议或订单要完成了的服务任务。</span><span class="sxs-lookup"><span data-stu-id="432c5-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="432c5-105">此信息可用于服务技术人员和客户。</span><span class="sxs-lookup"><span data-stu-id="432c5-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="432c5-106">创建与服务协议的关系</span><span class="sxs-lookup"><span data-stu-id="432c5-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="432c5-107">单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="432c5-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="432c5-108">选择某一现有服务协议，或者创建新的服务协议。</span><span class="sxs-lookup"><span data-stu-id="432c5-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="432c5-109">在“操作窗格”上，单击**服务任务**按钮。</span><span class="sxs-lookup"><span data-stu-id="432c5-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="432c5-110">在**服务任务**窗体上，按 Ctrl+N 创建新行，然后从**服务任务**列表中选择某个服务任务以将该服务任务附加到服务管理。</span><span class="sxs-lookup"><span data-stu-id="432c5-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="432c5-111">在**说明**选项卡上，在自由文本字段中输入任何内部工作记录或外部工作记录描述。</span><span class="sxs-lookup"><span data-stu-id="432c5-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="432c5-112">关闭该窗体以保存记录。</span><span class="sxs-lookup"><span data-stu-id="432c5-112">Close the form to save the record.</span></span>

<span data-ttu-id="432c5-113">重复此步骤，直到为该服务协议创建了所有必需的服务任务关系。</span><span class="sxs-lookup"><span data-stu-id="432c5-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="432c5-114">您现在可为任何附加的协议行指定这些服务任务。</span><span class="sxs-lookup"><span data-stu-id="432c5-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="432c5-115">对某一服务协议创建的服务任务关系将可用于附加到该服务协议的所有服务订单。</span><span class="sxs-lookup"><span data-stu-id="432c5-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="432c5-116">创建与服务订单的关系</span><span class="sxs-lookup"><span data-stu-id="432c5-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="432c5-117">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="432c5-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="432c5-118">选择某一现有服务订单，或者创建新的服务订单。</span><span class="sxs-lookup"><span data-stu-id="432c5-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="432c5-119">在“操作窗格”上，单击**服务任务**按钮。</span><span class="sxs-lookup"><span data-stu-id="432c5-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="432c5-120">从**服务任务**窗体，按 Ctrl+N 创建新行，然后从**服务任务**列表中选择某个服务任务以将该服务任务附加到服务管理。</span><span class="sxs-lookup"><span data-stu-id="432c5-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="432c5-121">在**说明**选项卡上，在自由文本字段中输入任何内部工作记录或外部工作记录描述。</span><span class="sxs-lookup"><span data-stu-id="432c5-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="432c5-122">关闭该窗体以保存记录。</span><span class="sxs-lookup"><span data-stu-id="432c5-122">Close the form to save the record.</span></span>

<span data-ttu-id="432c5-123">重复此步骤，直到为该服务订单创建了所有必需的服务任务关系。</span><span class="sxs-lookup"><span data-stu-id="432c5-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="432c5-124">您现在可选择在创建服务订单行时创建了其关系的服务任务。</span><span class="sxs-lookup"><span data-stu-id="432c5-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="432c5-125">在某一服务订单上创建的服务任务关系可用于特定的服务订单。</span><span class="sxs-lookup"><span data-stu-id="432c5-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="432c5-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="432c5-126">See also</span></span>

[<span data-ttu-id="432c5-127">服务任务</span><span class="sxs-lookup"><span data-stu-id="432c5-127">Service tasks</span></span>](service-tasks.md)


  


