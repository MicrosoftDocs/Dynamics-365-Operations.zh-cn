---
title: Dynamics 365 Talent 中的新增功能和更改（2019 年 11 月 5 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778374"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="6249a-103">Dynamics 365 Talent 中的新增功能和更改（2019 年 11 月 5 日）</span><span class="sxs-lookup"><span data-stu-id="6249a-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6249a-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="6249a-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="6249a-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="6249a-105">Changes in Attract</span></span>

<span data-ttu-id="6249a-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="6249a-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="6249a-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="6249a-107">Changes in Onboard</span></span>

<span data-ttu-id="6249a-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="6249a-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="6249a-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="6249a-109">Changes in Core HR</span></span>

<span data-ttu-id="6249a-110">本部分中的更改适用于内部版本号 8.1.2598。</span><span class="sxs-lookup"><span data-stu-id="6249a-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="6249a-111">某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="6249a-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="6249a-112">复制 Core HR 实例</span><span class="sxs-lookup"><span data-stu-id="6249a-112">Copy a Core HR instance</span></span>

<span data-ttu-id="6249a-113">在本周的发布中，您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Talent: Core HR 数据库复制到沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="6249a-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="6249a-114">如果您有另一个沙盒环境，还可以将数据库从该环境复制到目标沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="6249a-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="6249a-115">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="6249a-115">For more information, see:</span></span>

- <span data-ttu-id="6249a-116">“Dynamics 365: 2019 发布波次 2 计划”中的[更广泛的环境管理](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management)</span><span class="sxs-lookup"><span data-stu-id="6249a-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="6249a-117">Talent 文档中的[复制 Core HR 实例](hr-copy-instance.md)</span><span class="sxs-lookup"><span data-stu-id="6249a-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="6249a-118">启用 Common Data Service 集成后，不创建 Common Data Service 集成批处理作业 (388030)</span><span class="sxs-lookup"><span data-stu-id="6249a-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="6249a-119">启用此更改后，将为 Common Data Service 集成创建批处理作业。</span><span class="sxs-lookup"><span data-stu-id="6249a-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="6249a-120">HcmPersonImageEntity 在上载时不调整人员图像的大小 (369469)</span><span class="sxs-lookup"><span data-stu-id="6249a-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="6249a-121">本周的发布更改了通过数据管理导入图像时如何调整图像大小以改善效果。</span><span class="sxs-lookup"><span data-stu-id="6249a-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="6249a-122">职位的“可用于分配日期”可以早于“启用日期”(340103)</span><span class="sxs-lookup"><span data-stu-id="6249a-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="6249a-123">进行此更改后，如果您选择早于职位**启用日期**的**可用于分配日期**，会出现警告。</span><span class="sxs-lookup"><span data-stu-id="6249a-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="6249a-124">无法在基于步骤的计划的员工自助服务中创建薪酬更改请求 (376872)</span><span class="sxs-lookup"><span data-stu-id="6249a-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="6249a-125">此发布更正了通过基于步骤的计划的员工自助服务请求薪酬更改时出现的问题。</span><span class="sxs-lookup"><span data-stu-id="6249a-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="6249a-126">如果描述超过 30 个字符，原因码将不同步到 Common Data Service，Core HR 允许 60 个 (352682)</span><span class="sxs-lookup"><span data-stu-id="6249a-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="6249a-127">进行此更改后，将在 Common Data Service 中更新具有 30 个以上字符的原因代码。</span><span class="sxs-lookup"><span data-stu-id="6249a-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="6249a-128">Common Data Service 中所做的更改也将反映在 Talent 中。</span><span class="sxs-lookup"><span data-stu-id="6249a-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="6249a-129">从 Talent 到 Finance and Operations 的地址集成 (351961)</span><span class="sxs-lookup"><span data-stu-id="6249a-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="6249a-130">此发布修复了在 Talent 中更新的地址不在 Finance and Operations 中更新的问题。</span><span class="sxs-lookup"><span data-stu-id="6249a-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="6249a-131">对地址块的更改现在将更新。</span><span class="sxs-lookup"><span data-stu-id="6249a-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6249a-132">即将到期</span><span class="sxs-lookup"><span data-stu-id="6249a-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="6249a-133">打印绩效复查</span><span class="sxs-lookup"><span data-stu-id="6249a-133">Print performance reviews</span></span>

<span data-ttu-id="6249a-134">请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。</span><span class="sxs-lookup"><span data-stu-id="6249a-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="6249a-135">“功能管理”工作区</span><span class="sxs-lookup"><span data-stu-id="6249a-135">Feature management workspace</span></span>

<span data-ttu-id="6249a-136">每个版本中都会增加和更新功能。</span><span class="sxs-lookup"><span data-stu-id="6249a-136">Features are added and updated in every release.</span></span> <span data-ttu-id="6249a-137">功能管理体验提供一个工作区，可在其中查看各版本已交付的功能的列表。</span><span class="sxs-lookup"><span data-stu-id="6249a-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="6249a-138">默认情况下，新功能处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="6249a-138">By default, new features are turned off.</span></span> <span data-ttu-id="6249a-139">可使用该工作区开启这些功能并查看其文档。</span><span class="sxs-lookup"><span data-stu-id="6249a-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="6249a-140">要了解有关功能管理带来的更改的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。</span><span class="sxs-lookup"><span data-stu-id="6249a-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
