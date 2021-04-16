---
title: 评级模板
description: 此主题介绍如何设置评级资料的数据。
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828434"
---
# <a name="rating-profiles"></a><span data-ttu-id="f7653-103">评级模板</span><span class="sxs-lookup"><span data-stu-id="f7653-103">Rating profiles</span></span>

<span data-ttu-id="f7653-104">评级资料类似于物流合同（不是法律合同）。</span><span class="sxs-lookup"><span data-stu-id="f7653-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="f7653-105">它用于确定负荷的运输关税。</span><span class="sxs-lookup"><span data-stu-id="f7653-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="f7653-106">每个评级资料对于每个装运承运人都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="f7653-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="f7653-107">在评级资料中，将装运承运人与主费率相关联。</span><span class="sxs-lookup"><span data-stu-id="f7653-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="f7653-108">主费率定义基准费率分配和基准费率。</span><span class="sxs-lookup"><span data-stu-id="f7653-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="f7653-109">基准费率确定承运人的费率。</span><span class="sxs-lookup"><span data-stu-id="f7653-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="f7653-110">您可以使用显示所有现有评级资料的通用页面设置评级资料。</span><span class="sxs-lookup"><span data-stu-id="f7653-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="f7653-111">或者，可以直接从装运承运人设置评级资料。</span><span class="sxs-lookup"><span data-stu-id="f7653-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="f7653-112">在这两种情况下，您为评级资料设置的信息是相同的。</span><span class="sxs-lookup"><span data-stu-id="f7653-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="f7653-113">在评级资料页创建或编辑评级资料</span><span class="sxs-lookup"><span data-stu-id="f7653-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="f7653-114">在 **评级资料** 页上，您可以查看所有可用的评级资料。</span><span class="sxs-lookup"><span data-stu-id="f7653-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="f7653-115">您还可以编辑现有资料和创建新资料。</span><span class="sxs-lookup"><span data-stu-id="f7653-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="f7653-116">转到 **运输管理 \> 设置 \> 评级 \> 评级资料**。</span><span class="sxs-lookup"><span data-stu-id="f7653-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="f7653-117">在操作窗格上，选择 **新建** 将新评级资料添加到网格，或选择 **编辑** 编辑现有资料。</span><span class="sxs-lookup"><span data-stu-id="f7653-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="f7653-118">在新的或现有评级资料的行中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f7653-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="f7653-119">**评级资料** – 为评级资料输入唯一标识符 (ID)。</span><span class="sxs-lookup"><span data-stu-id="f7653-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="f7653-120">**名称** – 为评级资料输入描述性名称。</span><span class="sxs-lookup"><span data-stu-id="f7653-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="f7653-121">**装运承运人** – 选择装运承运人。</span><span class="sxs-lookup"><span data-stu-id="f7653-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="f7653-122">您在设置的评级资料还将显示在所选承运人的 **装运承运人** 页上。</span><span class="sxs-lookup"><span data-stu-id="f7653-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="f7653-123">**站点** 和 **仓库** – 选择站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="f7653-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="f7653-124">**费率引擎** – 为评级资料选择费率引擎。</span><span class="sxs-lookup"><span data-stu-id="f7653-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="f7653-125">**主费率** – 为评级资料选择主费率。</span><span class="sxs-lookup"><span data-stu-id="f7653-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="f7653-126">可以使用主费率定义基准费率类型和基准费率。</span><span class="sxs-lookup"><span data-stu-id="f7653-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="f7653-127">有关详细信息，请参阅[设置主费率](set-up-rate-masters.md)。</span><span class="sxs-lookup"><span data-stu-id="f7653-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="f7653-128">**运输时间引擎** – 为评级资料选择运输时间引擎。</span><span class="sxs-lookup"><span data-stu-id="f7653-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="f7653-129">**承运人燃油指数** – 为评级资料选择承运人燃油指数。</span><span class="sxs-lookup"><span data-stu-id="f7653-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="f7653-130">**生效开始日期和时间** 和 **生效结束日期和时间** – 定义评级资料应处于有效状态的时间段。</span><span class="sxs-lookup"><span data-stu-id="f7653-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="f7653-131">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f7653-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="f7653-132">直接在装运承运人页创建评级资料</span><span class="sxs-lookup"><span data-stu-id="f7653-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="f7653-133">转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。</span><span class="sxs-lookup"><span data-stu-id="f7653-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="f7653-134">在列表中选择一个装运承运人。</span><span class="sxs-lookup"><span data-stu-id="f7653-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="f7653-135">在 **评级资料** 快速选项卡上，选择 **新建** 创建评级资料。</span><span class="sxs-lookup"><span data-stu-id="f7653-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="f7653-136">为新的评级资料设置字段。</span><span class="sxs-lookup"><span data-stu-id="f7653-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="f7653-137">这些字段对应于 **评级资料** 页上的字段，如此主题前面一节所述。</span><span class="sxs-lookup"><span data-stu-id="f7653-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="f7653-138">在 **装运承运人** 页上创建的资料也会显示在 **评级资料** 页上。</span><span class="sxs-lookup"><span data-stu-id="f7653-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]