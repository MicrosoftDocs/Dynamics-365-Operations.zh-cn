---
title: 自动更新资产计数器
description: 本主题介绍如何在资产管理中自动更新资产计数器。
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
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875532"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="12997-103">自动更新资产计数器</span><span class="sxs-lookup"><span data-stu-id="12997-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="12997-104">上一部分中介绍了手动登记资产计数器。</span><span class="sxs-lookup"><span data-stu-id="12997-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="12997-105">[计数器](../setup-for-objects/counters.md)中介绍了设置资产计数器。</span><span class="sxs-lookup"><span data-stu-id="12997-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="12997-106">也可以根据生产工时或生产数量自动从生产登记更新计数器值。</span><span class="sxs-lookup"><span data-stu-id="12997-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="12997-107">这在**更新资产计数器**中执行。</span><span class="sxs-lookup"><span data-stu-id="12997-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="12997-108">可以通过插入**开始日期**参数更新一个或多个资产。</span><span class="sxs-lookup"><span data-stu-id="12997-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="12997-109">此参数指定生产登记（工时数或生产数量）的开始日期，即应开始更新计数器值的日期。</span><span class="sxs-lookup"><span data-stu-id="12997-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="12997-110">自动更新中将包括与资源关联*且*具有（为了基于生产的数量或生产工时进行更新而设置的）资产计数器的所有资产，并且将创建新的计数器值。</span><span class="sxs-lookup"><span data-stu-id="12997-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="12997-111">计数中将包括基于登记的生产数量、良品数量和错误数量的相关计数器。</span><span class="sxs-lookup"><span data-stu-id="12997-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="12997-112">如果用于生产数量登记的单位不是计数器使用的单位，将转换数量，以便与计数器单位一致。</span><span class="sxs-lookup"><span data-stu-id="12997-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="12997-113">正如上面的介绍，可以从生产登记更新自动计数器。</span><span class="sxs-lookup"><span data-stu-id="12997-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="12997-114">因此，必须将要自动更新其计数器的资产与资源（机器）关联。</span><span class="sxs-lookup"><span data-stu-id="12997-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="12997-115">下面的说明提供有关设置和处理生产订单（在**生产控制**模块中）的概览，而此类设置和处理则是在**资产管理**模块中自动更新资产的计数器的基础。</span><span class="sxs-lookup"><span data-stu-id="12997-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="12997-116">为资源登记生产数量或生产工时之后，可更新关联的资产计数器。</span><span class="sxs-lookup"><span data-stu-id="12997-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="12997-117">单击**资产管理** > **定期** > **资产** > **更新资产计数器**。</span><span class="sxs-lookup"><span data-stu-id="12997-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="12997-118">在**开始日期**字段中选择自动更新的开始日期。</span><span class="sxs-lookup"><span data-stu-id="12997-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="12997-119">此字段中的日期是来自**工艺路线交易记录**（**生产控制** > **查询和报表** > **生产** > **工艺路线交易记录** > **实际日期**字段）的“在制品”日期。</span><span class="sxs-lookup"><span data-stu-id="12997-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="12997-120">如果要选择特定资产、资产类型或资源以进行自动更新，请单击**要包括的记录**快速选项卡上的**筛选**，然后进行相关选择。</span><span class="sxs-lookup"><span data-stu-id="12997-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="12997-121">如果需要，可以在**在后台运行**快速选项卡上将自动更新设置为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="12997-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![图 1](media/12-work-orders.png)

5. <span data-ttu-id="12997-123">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="12997-123">Click **OK**.</span></span> <span data-ttu-id="12997-124">完成了资产计数器自动更新之后，可以在**资产计数器**（**资产管理** > **常用** > **资产** > **所有资产** > 选择资产 > **计数器**按钮）中查看与资产关联的计数器登记。</span><span class="sxs-lookup"><span data-stu-id="12997-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="12997-125">在**资产计数器总计**中，可获取为所有资产的所有计数器类型创建的最新登记的概览。</span><span class="sxs-lookup"><span data-stu-id="12997-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="12997-126">单击**资产管理** > **查询** > **资产** > **资产汇总值**。</span><span class="sxs-lookup"><span data-stu-id="12997-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="12997-127">该值类似**资产计数器**，但是您不能在**资产汇总值**中添加或编辑登记。</span><span class="sxs-lookup"><span data-stu-id="12997-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="12997-128">它仅供概览。</span><span class="sxs-lookup"><span data-stu-id="12997-128">It is for overview only.</span></span>

![图 2](media/13-work-orders.png)


- <span data-ttu-id="12997-130">您仍然可以为自动更新的计数器类型手动创建计数器值登记。</span><span class="sxs-lookup"><span data-stu-id="12997-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="12997-131">有关详细信息，请参阅“手动更新资产计数器”。</span><span class="sxs-lookup"><span data-stu-id="12997-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="12997-132">可设置与其他计数器关联的计数器，这意味着更新计数器时，同时将自动更新关联的计数器。</span><span class="sxs-lookup"><span data-stu-id="12997-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="12997-133">有关设置关联的计数器，请参阅[计数器](../setup-for-objects/counters.md)。</span><span class="sxs-lookup"><span data-stu-id="12997-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
