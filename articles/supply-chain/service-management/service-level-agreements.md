---
title: 服务级别协议
description: 在服务级别协议中，客户同意接受基于服务公司记录问题和解决问题的最短响应时间。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cffe3a7766502dd5d888a7a99a32150967911301
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "364572"
---
# <a name="service-level-agreements"></a><span data-ttu-id="d7287-103">服务级别协议</span><span class="sxs-lookup"><span data-stu-id="d7287-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d7287-104">服务级别协议 (SLA) 是服务公司和服务客户之间的协议。</span><span class="sxs-lookup"><span data-stu-id="d7287-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="d7287-105">在 SLA 中，客户同意接受基于服务公司记录问题和解决问题的最短响应时间。</span><span class="sxs-lookup"><span data-stu-id="d7287-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="d7287-106">SLA 设置了为客户提供的服务的标准级别，并使服务公司明确何时应完成服务工作。</span><span class="sxs-lookup"><span data-stu-id="d7287-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="d7287-107">可以创建任意数目的 SLA 来为服务客户提供不同级别的服务。</span><span class="sxs-lookup"><span data-stu-id="d7287-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="d7287-108">创建服务级别协议</span><span class="sxs-lookup"><span data-stu-id="d7287-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="d7287-109">单击**服务管理** \> **设置** \> **服务协议** \> **服务级别协议**。</span><span class="sxs-lookup"><span data-stu-id="d7287-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="d7287-110">在**服务级别协议**字段中，键入服务级别协议的名称。</span><span class="sxs-lookup"><span data-stu-id="d7287-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="d7287-111">键入允许附加到服务服务级别协议的服务请求完成时间。</span><span class="sxs-lookup"><span data-stu-id="d7287-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="d7287-112">然后，如果您想要基于特定日历的服务级别协议，则选择一个日历。</span><span class="sxs-lookup"><span data-stu-id="d7287-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="d7287-113">应用服务级别协议</span><span class="sxs-lookup"><span data-stu-id="d7287-113">Apply a service level agreement</span></span>

<span data-ttu-id="d7287-114">将 SLA 直接应用到某服务协议。</span><span class="sxs-lookup"><span data-stu-id="d7287-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="d7287-115">根据 SLA 来度量您手动创建并附加到具有此 SLA 的某服务协议的服务订单。</span><span class="sxs-lookup"><span data-stu-id="d7287-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="d7287-116">您自动创建的服务订单不附加到 SLA。</span><span class="sxs-lookup"><span data-stu-id="d7287-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="d7287-117">将服务级别协议应用到服务协议</span><span class="sxs-lookup"><span data-stu-id="d7287-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="d7287-118">单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="d7287-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="d7287-119">选择您要应用 SLA 的服务协议，然后单击**操作窗格**上的**编辑**。</span><span class="sxs-lookup"><span data-stu-id="d7287-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="d7287-120">在**服务级别协议**字段中，选择要分配的 SLA。</span><span class="sxs-lookup"><span data-stu-id="d7287-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="d7287-121">将服务级别协议应用到服务协议组</span><span class="sxs-lookup"><span data-stu-id="d7287-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="d7287-122">单击**服务管理** \> **设置** \> **服务协议** \> **服务协议组**。</span><span class="sxs-lookup"><span data-stu-id="d7287-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="d7287-123">在**服务级别协议**字段中，选择要分配的 SLA。</span><span class="sxs-lookup"><span data-stu-id="d7287-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="d7287-124">根据 SLA 跟踪服务订单的时间</span><span class="sxs-lookup"><span data-stu-id="d7287-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="d7287-125">在您为 SLA 分配到的服务协议创建新的服务订单时，启动服务的交货时间间隔，且系统开始跟踪交货时间。</span><span class="sxs-lookup"><span data-stu-id="d7287-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="d7287-126">此外，可以设置以下选项：</span><span class="sxs-lookup"><span data-stu-id="d7287-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="d7287-127">可以开始和停止有关服务订单的时间记录，以登记服务订单所花费的总时间。</span><span class="sxs-lookup"><span data-stu-id="d7287-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="d7287-128">可以监控是否遵循在服务级别协议中设置的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="d7287-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="d7287-129">可以定义超过服务级别协议的时间间隔时必须设置的原因代码。</span><span class="sxs-lookup"><span data-stu-id="d7287-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7287-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7287-130">See also</span></span>

[<span data-ttu-id="d7287-131">查看对服务级别协议的遵从性</span><span class="sxs-lookup"><span data-stu-id="d7287-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


