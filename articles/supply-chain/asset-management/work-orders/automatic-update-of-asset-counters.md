---
title: 自动更新资产计数器
description: 本主题介绍如何在资产管理中自动更新资产计数器。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 005b04bd4c3476356f30ba8e97564f83307a64c7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811730"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="c0c76-103">自动更新资产计数器</span><span class="sxs-lookup"><span data-stu-id="c0c76-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0c76-104">有关手动登记资产计数器的信息，请参阅[手动更新资产计数器](../work-orders/manual-update-of-asset-counters.md)。</span><span class="sxs-lookup"><span data-stu-id="c0c76-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="c0c76-105">有关如何设置资产计数器的信息，请参阅[计数器](../setup-for-objects/counters.md)。</span><span class="sxs-lookup"><span data-stu-id="c0c76-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="c0c76-106">也可以根据生产工时或生产数量（即生产的数量）自动从生产登记更新计数器值。</span><span class="sxs-lookup"><span data-stu-id="c0c76-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="c0c76-107">此更新在**更新资产计数器**页面上完成。</span><span class="sxs-lookup"><span data-stu-id="c0c76-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="c0c76-108">可以通过设置**开始日期**参数更新一个或多个资产。</span><span class="sxs-lookup"><span data-stu-id="c0c76-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="c0c76-109">此参数指定生产登记的开始日期（生产工时或生产数量）。</span><span class="sxs-lookup"><span data-stu-id="c0c76-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="c0c76-110">换言之，它指定应该更新计数器值的日期。</span><span class="sxs-lookup"><span data-stu-id="c0c76-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="c0c76-111">自动更新中将包括与资源关联*且*具有（为了基于生产工时或生产数量进行更新而设置的）资产计数器的所有资产。</span><span class="sxs-lookup"><span data-stu-id="c0c76-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="c0c76-112">新的计数器值将创建。</span><span class="sxs-lookup"><span data-stu-id="c0c76-112">New counter values will be created.</span></span>

<span data-ttu-id="c0c76-113">对于基于生产数量的计数器，计数包括已登记的完好数量和残次数量。</span><span class="sxs-lookup"><span data-stu-id="c0c76-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="c0c76-114">如果用于生产数量登记的单位与用于计数器的单位不同，将转换数量，以便其与计数器单位一致。</span><span class="sxs-lookup"><span data-stu-id="c0c76-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="c0c76-115">正如上面的介绍，可以从生产登记更新自动计数器。</span><span class="sxs-lookup"><span data-stu-id="c0c76-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="c0c76-116">因此，必须将要自动更新其计数器的资产与资源（机器）关联。</span><span class="sxs-lookup"><span data-stu-id="c0c76-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="c0c76-117">为资源登记生产数量或生产工时之后，可更新关联的资产计数器。</span><span class="sxs-lookup"><span data-stu-id="c0c76-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="c0c76-118">选择**资产管理** > **定期** > **资产** > **更新资产计数器**。</span><span class="sxs-lookup"><span data-stu-id="c0c76-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="c0c76-119">在**开始日期**字段中，选择自动更新的开始日期。</span><span class="sxs-lookup"><span data-stu-id="c0c76-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="c0c76-120">此字段中的日期是来自**工艺路线交易记录**（**生产控制** > **查询和报表** > **生产** > **工艺路线交易记录** > **实际日期**字段）的“在制品”日期。</span><span class="sxs-lookup"><span data-stu-id="c0c76-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="c0c76-121">在**要包括的记录**快速选项卡上，您可以选择特定资产、资产类型或资源来进行自动更新。</span><span class="sxs-lookup"><span data-stu-id="c0c76-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="c0c76-122">选择**筛选器**，然后进行相关选择。</span><span class="sxs-lookup"><span data-stu-id="c0c76-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="c0c76-123">在**在后台运行**快速选项卡上，可根据需要将自动更新设置为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="c0c76-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="c0c76-124">下图显示了**更新资产计数器**对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="c0c76-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![图 1](media/12-work-orders.png)

5. <span data-ttu-id="c0c76-126">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c0c76-126">Select **OK**.</span></span> 

<span data-ttu-id="c0c76-127">自动资产计数器更新完成后，您可以在**资产计数器**页面上查看与资产相关的计数器登记。</span><span class="sxs-lookup"><span data-stu-id="c0c76-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="c0c76-128">选择**资产管理** > **通用** > **资产** > **所有资产**，选择资产，然后在操作窗格上的**资产**选项卡上，在**预防**组中，选择**计数器**。</span><span class="sxs-lookup"><span data-stu-id="c0c76-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="c0c76-129">在**资产汇总值**页面，可获取已为所有资产的所有计数器类型创建的最新登记的概览。</span><span class="sxs-lookup"><span data-stu-id="c0c76-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="c0c76-130">选择**资产管理** > **查询** > **资产** > **资产汇总值**。</span><span class="sxs-lookup"><span data-stu-id="c0c76-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="c0c76-131">此页面类似于**资产计数器**页面，但是您无法添加或编辑登记。</span><span class="sxs-lookup"><span data-stu-id="c0c76-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="c0c76-132">它仅供概览。</span><span class="sxs-lookup"><span data-stu-id="c0c76-132">It's for overview only.</span></span>

<span data-ttu-id="c0c76-133">下图显示了**资产汇总值**页面的示例。</span><span class="sxs-lookup"><span data-stu-id="c0c76-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![图 2](media/13-work-orders.png)

<span data-ttu-id="c0c76-135">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="c0c76-135">Note the following points:</span></span>

- <span data-ttu-id="c0c76-136">您仍然可以为自动更新的计数器类型手动创建计数器值登记。</span><span class="sxs-lookup"><span data-stu-id="c0c76-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="c0c76-137">有关详细信息，请参阅[手动更新资产计数器](../work-orders/manual-update-of-asset-counters.md)。</span><span class="sxs-lookup"><span data-stu-id="c0c76-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="c0c76-138">您可以设置与另一个计数器相关的计数器。</span><span class="sxs-lookup"><span data-stu-id="c0c76-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="c0c76-139">这样，当更新计数器时，相关的计数器会同时自动更新。</span><span class="sxs-lookup"><span data-stu-id="c0c76-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="c0c76-140">有关如何设置相关计数器的详细信息，请参阅[计数器](../setup-for-objects/counters.md)。</span><span class="sxs-lookup"><span data-stu-id="c0c76-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

