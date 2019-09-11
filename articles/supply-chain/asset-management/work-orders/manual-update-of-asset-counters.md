---
title: 手动更新资产计数器
description: 本主题介绍如何在资产管理中手动更新资产计数器。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875527"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="c0c49-103">手动更新资产计数器</span><span class="sxs-lookup"><span data-stu-id="c0c49-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c0c49-104">计数器用于创建与资产有关的登记，例如，运行小时数或生产数量数。</span><span class="sxs-lookup"><span data-stu-id="c0c49-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="c0c49-105">如果为计数器选择的计数器类型设置为继承计数器值（**资产管理** > **设置** > **资产类型** > **计数器** > **常规**快速选项卡 > **继承资产计数器值**切换按钮设置为“是”），则当您新建该类型的计数器行时，将自动更新使用同一个计数器类型的所有子资产。</span><span class="sxs-lookup"><span data-stu-id="c0c49-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="c0c49-106">在**所有资产**中，将根据资产的读数为资产创建工时或数量计数器登记。</span><span class="sxs-lookup"><span data-stu-id="c0c49-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="c0c49-107">单击**资产管理** > **常用** > **资产** > **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="c0c49-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="c0c49-108">在列表中选择资产，然后单击**计数器**。</span><span class="sxs-lookup"><span data-stu-id="c0c49-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="c0c49-109">在**资产计数器**窗体中，可以查看所选资产的之前全部计数器登记的列表。</span><span class="sxs-lookup"><span data-stu-id="c0c49-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="c0c49-110">单击**新建**以创建新的登记。</span><span class="sxs-lookup"><span data-stu-id="c0c49-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="c0c49-111">将自动插入资产 ID。</span><span class="sxs-lookup"><span data-stu-id="c0c49-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="c0c49-112">在**计数器**字段中选择相关计数器。</span><span class="sxs-lookup"><span data-stu-id="c0c49-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="c0c49-113">只有与为资产选择的资产类型关联的计数器才可用。</span><span class="sxs-lookup"><span data-stu-id="c0c49-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="c0c49-114">将在**单位**字段中自动插入关联的单位。</span><span class="sxs-lookup"><span data-stu-id="c0c49-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="c0c49-115">为计数器登记选择日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c0c49-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="c0c49-116">在**值**字段中，插入上一个计数器登记后的数字，或者在**汇总值**字段中插入计数总数。</span><span class="sxs-lookup"><span data-stu-id="c0c49-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="c0c49-117">如果以物理方式为资产安装新的计数器，则需要在**资产计数器**中登记资产的更改。</span><span class="sxs-lookup"><span data-stu-id="c0c49-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="c0c49-118">接下来，必须创建两个具有相同时间戳的登记行，然后在与新计数器有关的行中，选中**计数器重置**复选框。</span><span class="sxs-lookup"><span data-stu-id="c0c49-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="c0c49-119">创建这两个登记行时，第一行必须针对要替换的计数器。</span><span class="sxs-lookup"><span data-stu-id="c0c49-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="c0c49-120">**总计**字段中的计数总数是为该计数器类型登记的所有值的计数器总计之和。</span><span class="sxs-lookup"><span data-stu-id="c0c49-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="c0c49-121">如果为使用其间隔类型为“从... 开始”或“到达...”的维护计划的资产选中**计数器重置**复选框，该计数器对新计数器行仍然有效，因为您创建的是单独的计数器行，并且是从新计数器重新开始。</span><span class="sxs-lookup"><span data-stu-id="c0c49-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![图 1](media/11-work-orders.png)


<span data-ttu-id="c0c49-123">如果要为多个资产创建计数器登记，可以在**资产管理** > **查询** > **资产** > **资产计数器**中进行。</span><span class="sxs-lookup"><span data-stu-id="c0c49-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="c0c49-124">可以设置范围来定义手动计数器登记中的偏差，以及登记超出定义的范围时应该显示的消息类型。</span><span class="sxs-lookup"><span data-stu-id="c0c49-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="c0c49-125">有关设置计数器的信息，请参阅[计数器](../setup-for-objects/counters.md)主题。</span><span class="sxs-lookup"><span data-stu-id="c0c49-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
