---
title: 创建工作订单
description: 本主题介绍如何在资产管理中创建工作订单。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206119"
---
# <a name="creating-work-orders"></a><span data-ttu-id="f1e7f-103">创建工作订单</span><span class="sxs-lookup"><span data-stu-id="f1e7f-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f1e7f-104">已安排了预防性维护作业之后，接下来需要为这些作业创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="f1e7f-105">这在其中一个维护安排内完成。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="f1e7f-106">维护安排中的已安排作业可以采用不同类型：</span><span class="sxs-lookup"><span data-stu-id="f1e7f-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="f1e7f-107">引用类型</span><span class="sxs-lookup"><span data-stu-id="f1e7f-107">Reference type</span></span> | <span data-ttu-id="f1e7f-108">说明</span><span class="sxs-lookup"><span data-stu-id="f1e7f-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e7f-109">维护计划</span><span class="sxs-lookup"><span data-stu-id="f1e7f-109">Maintenance plans</span></span>     | <span data-ttu-id="f1e7f-110">基于维护安排类型“时间”或“计数器”的预防性维护作业。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="f1e7f-111">维护阶段</span><span class="sxs-lookup"><span data-stu-id="f1e7f-111">Maintenance rounds</span></span>    | <span data-ttu-id="f1e7f-112">其中包含多个需要相似维护类型的资产的预防性维护作业。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="f1e7f-113">维护请求</span><span class="sxs-lookup"><span data-stu-id="f1e7f-113">Maintenance request</span></span>   | <span data-ttu-id="f1e7f-114">手动创建的资产维护或维修请求，可转化为工作订单。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="f1e7f-115">单击**资产管理** > **常用** > **所有维护安排**或**打开维护安排行**或**打开维护安排池**。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="f1e7f-116">选择要为其创建工作订单的已安排维护作业，然后单击**工作订单**。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="f1e7f-117">在**创建工作订单**对话框中，将在**维护预测工时数**字段中显示所选行的预测工时总数。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="f1e7f-118">在**参数**部分中，选择应创建多少个工作订单。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="f1e7f-119">可为每个维护安排行创建一个工作订单，或根据在**每个以下对象一个工作订单**部分中进行的选择创建一些工作订单。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="f1e7f-120">选择将在创建的所有工作订单中使用的**工作订单类型**。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="f1e7f-121">下图显示了**创建工作订单**对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![图 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="f1e7f-123">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-123">Click **OK**.</span></span> <span data-ttu-id="f1e7f-124">将创建一个或多个工作订单。</span><span class="sxs-lookup"><span data-stu-id="f1e7f-124">One or more work orders are created.</span></span>

