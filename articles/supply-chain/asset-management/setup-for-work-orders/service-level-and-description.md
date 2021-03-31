---
title: 服务级别和描述
description: 本主题介绍资产管理中的服务级别和描述。
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65a3a0b6c2c052c41be469591c1281c1cce2b7d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226777"
---
# <a name="service-level-and-description"></a><span data-ttu-id="9c5ed-103">服务级别和描述</span><span class="sxs-lookup"><span data-stu-id="9c5ed-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9c5ed-104">创建工作订单时，可能希望为其定义服务级别和向其添加一般描述。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="9c5ed-105">可以在 **工作订单服务级别** 页上创建工作订单服务级别，在 **工作订单描述** 页上创建描述。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="9c5ed-106">创建服务级别</span><span class="sxs-lookup"><span data-stu-id="9c5ed-106">Create a service level</span></span>

1. <span data-ttu-id="9c5ed-107">选择 **资产管理** \> **设置** \> **工作订单** \> **服务级别**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="9c5ed-108">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-108">Select **New**.</span></span>
3. <span data-ttu-id="9c5ed-109">在 **服务级别** 字段中，键入服务级别（例如，一个数字）。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="9c5ed-110">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="9c5ed-111">在 **工作订单** 快速选项卡上，可定义预计开始和结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="9c5ed-112">此快速选项卡上的字段定义工作订单应该的开始和结束期间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="9c5ed-113">用于手动创建的工作订单和基于维护请求创建的工作订单。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="9c5ed-114">在 **开始日期** 字段中，输入天数以定义工作订单的应该开始期间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="9c5ed-115">此天数从工作订单的创建日期开始计算。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="9c5ed-116">例如，如果工作订单应该在创建时开始，请输入 **0**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="9c5ed-117">如果工作订单应该在创建后一周内开始，请输入 **7**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="9c5ed-118">除了开始日期，若要为工作订单再设置开始时间，请将 **设置开始时间** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="9c5ed-119">然后在 **开始时间** 字段中输入开始时间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="9c5ed-120">如果将此选项设置为 **否**，将使用当前时间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="9c5ed-121">在 **结束日期** 字段中，输入天数以定义工作订单的应该结束期间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="9c5ed-122">此天数从工作订单的开始日期开始计算。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="9c5ed-123">例如，如果工作订单应该在其开始日期后一周内结束，请输入 **7**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="9c5ed-124">除了结束日期，若要为工作订单再设置结束时间，请将 **设置结束时间** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="9c5ed-125">然后在 **结束时间** 字段中输入结束时间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="9c5ed-126">如果将此选项设置为 **否**，将使用当前时间。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="9c5ed-127">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-127">Select **Save**.</span></span>

![工作订单服务级别页面](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="9c5ed-129">创建描述</span><span class="sxs-lookup"><span data-stu-id="9c5ed-129">Create a description</span></span>

1. <span data-ttu-id="9c5ed-130">选择 **资产管理** \> **设置** \> **工作订单** \> **描述**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="9c5ed-131">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-131">Select **New**.</span></span>
3. <span data-ttu-id="9c5ed-132">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="9c5ed-133">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-133">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]