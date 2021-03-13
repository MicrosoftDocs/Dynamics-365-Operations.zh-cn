---
title: 资产和工作订单
description: 本主题介绍资产管理中的资产和工作订单。
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cddb0a25286c8ce9d72aef0b835809705ad577a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020931"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="59b27-103">资产和工作订单</span><span class="sxs-lookup"><span data-stu-id="59b27-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="59b27-104">本主题介绍资产管理中的资产和工作订单。</span><span class="sxs-lookup"><span data-stu-id="59b27-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="59b27-105">资产和工作订单是资产管理的最重要部分。</span><span class="sxs-lookup"><span data-stu-id="59b27-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="59b27-106">*资产* 是需要持续维护和服务的机器或机器部件。</span><span class="sxs-lookup"><span data-stu-id="59b27-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="59b27-107">可以按分层结构创建资产，还可以将其与功能位置关联。</span><span class="sxs-lookup"><span data-stu-id="59b27-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="59b27-108">可以在资产结构的所有级别计划维护作业。</span><span class="sxs-lookup"><span data-stu-id="59b27-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="59b27-109">可以为每个资产设置各种数据，如产品信息和资产规格，以及必需的维护计划。</span><span class="sxs-lookup"><span data-stu-id="59b27-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="59b27-110">下图显示资产数据和资产与作业类型之间的隶属关系的概览。</span><span class="sxs-lookup"><span data-stu-id="59b27-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="59b27-111">红色文本用于的示例显示继承关系和依赖关系。</span><span class="sxs-lookup"><span data-stu-id="59b27-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![显示与工作类型相关的资产数据的图](media/05-overview-image.png)

<span data-ttu-id="59b27-113">每个工作订单都有工作订单类型，如预防性维护、修复性维护或检验。</span><span class="sxs-lookup"><span data-stu-id="59b27-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="59b27-114">工作订单中包含一个或多个工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="59b27-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="59b27-115">每个工作订单作业定义必须对资产执行的作业和关联的作业类型。</span><span class="sxs-lookup"><span data-stu-id="59b27-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="59b27-116">关联作业类型的示例包括 10,000 公里、50,000 公里、1 年检修和安全检验。</span><span class="sxs-lookup"><span data-stu-id="59b27-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="59b27-117">可以将一个工作订单与多个资产关联。</span><span class="sxs-lookup"><span data-stu-id="59b27-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="59b27-118">下图显示工作订单中的关键数据的概览。</span><span class="sxs-lookup"><span data-stu-id="59b27-118">The following illustration shows an overview of the key data in a work order.</span></span>

![显示工作订单中的关键数据的图](media/06-overview-image.png)

<span data-ttu-id="59b27-120">可以将一个工作订单与另一个工作订单关联，而作业类型中可以包含连续作业，用于创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="59b27-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="59b27-121">工作订单之间通常不存在依赖关系。</span><span class="sxs-lookup"><span data-stu-id="59b27-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="59b27-122">因此，可以彼此独立地更改其工作订单生命周期状态和为其排产。</span><span class="sxs-lookup"><span data-stu-id="59b27-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="59b27-123">可以通过多种方法创建与修复性、预防性或反应性维护关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="59b27-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="59b27-124">也可以手动创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="59b27-124">You can also create work orders manually.</span></span> <span data-ttu-id="59b27-125">下图显示自动或手动创建工作订单的过程概览。</span><span class="sxs-lookup"><span data-stu-id="59b27-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![显示自动或手动创建工作订单的图](media/07-overview-image.png)

<span data-ttu-id="59b27-127">如果希望为工作订单计划和运行维护作业，则必须完成多个步骤。</span><span class="sxs-lookup"><span data-stu-id="59b27-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="59b27-128">下图显示工作订单的处理的概览。</span><span class="sxs-lookup"><span data-stu-id="59b27-128">The following illustration shows an overview of the processing for a work order.</span></span>

![显示处理工作订单的概览的图](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="59b27-130">在 Dynamics 365 Supply Chain Management 和 **资产管理** 模块中工作时，通常选择 **新建** 来创建新记录，选择 **编辑** 来更新现有记录，以及选择 **保存** 来保存新数据或编辑后的数据。</span><span class="sxs-lookup"><span data-stu-id="59b27-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
