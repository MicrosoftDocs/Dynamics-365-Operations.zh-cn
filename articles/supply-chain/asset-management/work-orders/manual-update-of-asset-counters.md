---
title: 手动更新资产计数器
description: 本主题介绍如何在资产管理中手动更新资产计数器。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6dfea7ca166948f507a1cdea20f3e4cce16080ce
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219477"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="18e23-103">手动更新资产计数器</span><span class="sxs-lookup"><span data-stu-id="18e23-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="18e23-104">计数器用于在资产上创建登记，如有关资产已运行小时数或已生产数量的登记。</span><span class="sxs-lookup"><span data-stu-id="18e23-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="18e23-105">可以将为计数器选择的计数器类型设置为继承计数器值。</span><span class="sxs-lookup"><span data-stu-id="18e23-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="18e23-106">换言之，在 **计数器** 页面的 **常规** 快速选项卡上，**继承资产计数器值** 选项设置为 **是**（**资产管理** > **设置** > **资产类型** > **计数器**）。</span><span class="sxs-lookup"><span data-stu-id="18e23-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="18e23-107">在这种情况下，当您创建该类型的新计数器行时，使用相同计数器类型的每个子资产都会自动更新。</span><span class="sxs-lookup"><span data-stu-id="18e23-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="18e23-108">在 **所有资产** 页面上，将根据资产的读数为资产创建工时或数量计数器登记。</span><span class="sxs-lookup"><span data-stu-id="18e23-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="18e23-109">选择 **资产管理** > **常用** > **资产** > **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="18e23-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="18e23-110">选择资产，然后在“操作窗格”上，在 **资产** 选项卡上的 **预防** 组中，选择 **计数器**。</span><span class="sxs-lookup"><span data-stu-id="18e23-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="18e23-111">**资产计数器** 页面显示所选资产之前进行的全部计数器登记的列表。</span><span class="sxs-lookup"><span data-stu-id="18e23-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="18e23-112">选择 **新建** 以创建登记。</span><span class="sxs-lookup"><span data-stu-id="18e23-112">Select **New** to create a registration.</span></span> <span data-ttu-id="18e23-113">将在 **资产** 字段中自动输入资产 ID。</span><span class="sxs-lookup"><span data-stu-id="18e23-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="18e23-114">在 **计数器** 字段中选择相关计数器。</span><span class="sxs-lookup"><span data-stu-id="18e23-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="18e23-115">只有与为资产选择的资产类型关联的计数器可供选择。</span><span class="sxs-lookup"><span data-stu-id="18e23-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="18e23-116">将在 **单位** 字段中自动输入关联的单位。</span><span class="sxs-lookup"><span data-stu-id="18e23-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="18e23-117">在 **已登记** 字段中，为计数器登记选择日期和时间。</span><span class="sxs-lookup"><span data-stu-id="18e23-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="18e23-118">在 **值** 字段中，输入自上次计数器登记以来的数量。</span><span class="sxs-lookup"><span data-stu-id="18e23-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="18e23-119">或者，在 **汇总值** 字段中，输入总计数量。</span><span class="sxs-lookup"><span data-stu-id="18e23-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="18e23-120">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="18e23-120">Note the following points:</span></span>

- <span data-ttu-id="18e23-121">如果以物理方式为资产安装新的计数器，则必须在 **资产计数器** 页面登记资产的更改。</span><span class="sxs-lookup"><span data-stu-id="18e23-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="18e23-122">接下来，您必须创建两个具有相同时间戳的登记行。</span><span class="sxs-lookup"><span data-stu-id="18e23-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="18e23-123">第一行必须是要替换的计数器。</span><span class="sxs-lookup"><span data-stu-id="18e23-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="18e23-124">在与新计数器相关的行上，选中 **计数器重置** 复选框。</span><span class="sxs-lookup"><span data-stu-id="18e23-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="18e23-125">**总计** 字段中的计数总数是为该计数器类型登记的所有值的计数器总计之和。</span><span class="sxs-lookup"><span data-stu-id="18e23-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="18e23-126">如果为使用其间隔类型为“从... 开始”或“到达...”的维护计划的资产选中 **计数器重置** 复选框，该计数器对新计数器行仍然有效，因为您创建的是单独的计数器行，并且是从新计数器重新开始。</span><span class="sxs-lookup"><span data-stu-id="18e23-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="18e23-127">下图显示了 **资产计数器** 页面的示例。</span><span class="sxs-lookup"><span data-stu-id="18e23-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![图 1](media/11-work-orders.png)

<span data-ttu-id="18e23-129">在 **资产计数器** 页面上（**资产管理** > **查询** > **资产** > **资产计数器**），您可以根据需要同时对多个资产进行计数器登记。</span><span class="sxs-lookup"><span data-stu-id="18e23-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="18e23-130">您可以设置范围来定义手动计数器登记的偏差。</span><span class="sxs-lookup"><span data-stu-id="18e23-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="18e23-131">如果登记超出定义的范围，您还可以指定显示的消息类型。</span><span class="sxs-lookup"><span data-stu-id="18e23-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="18e23-132">有关如何设置计数器的详细信息，请参阅[计数器](../setup-for-objects/counters.md)。</span><span class="sxs-lookup"><span data-stu-id="18e23-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]