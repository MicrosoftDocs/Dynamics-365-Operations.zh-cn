---
title: Dynamics 365 Talent 中的新增功能或更改（2019 年 10 月 29 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773869"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="6334d-103">Dynamics 365 Talent 中的新增功能或更改（2019 年 10 月 29 日）</span><span class="sxs-lookup"><span data-stu-id="6334d-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6334d-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="6334d-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="6334d-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="6334d-105">Changes in Attract</span></span>

<span data-ttu-id="6334d-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="6334d-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="6334d-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="6334d-107">Changes in Onboard</span></span>

<span data-ttu-id="6334d-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="6334d-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="6334d-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="6334d-109">Changes in Core HR</span></span>

<span data-ttu-id="6334d-110">本部分中的更改适用于内部版本号 8.1.2586。</span><span class="sxs-lookup"><span data-stu-id="6334d-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="6334d-111">某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="6334d-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="6334d-112">“删除不含角色的当事方”默认应启用 (371233)</span><span class="sxs-lookup"><span data-stu-id="6334d-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="6334d-113">在 Talent 中预配新环境时，**如果没有角色则删除当事方**默认打开。</span><span class="sxs-lookup"><span data-stu-id="6334d-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="6334d-114">当您删除工作人员时，除非启用此设置，否则不会删除与该工作人员关联的当事方。</span><span class="sxs-lookup"><span data-stu-id="6334d-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="6334d-115">当您需要导入、更改或重新导入工作人员时，此更改将限制全球通讯簿中的重复记录。</span><span class="sxs-lookup"><span data-stu-id="6334d-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="6334d-116">应允许在 Common Data Service 中删除草稿和已取消的休假请求 (376999)</span><span class="sxs-lookup"><span data-stu-id="6334d-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="6334d-117">通过此更改，您现在可以在 Common Data Service 中删除状态为**草稿**或**已取消**的休假请求。</span><span class="sxs-lookup"><span data-stu-id="6334d-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="6334d-118">单击自定义字段窗体上的“应用”后，自定义字段中的其他列表值不会反映在 Common Data Service 中 (379599)</span><span class="sxs-lookup"><span data-stu-id="6334d-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="6334d-119">当您将新列表值添加到已与 Common Data Service 同步的现有自定义字段时，在**自定义字段**窗体中应用更改后，它们现在可在 Common Data Serivce 中提供。</span><span class="sxs-lookup"><span data-stu-id="6334d-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="6334d-120">存在多个雇用时，跨法人应用入职核对清单 (371270)</span><span class="sxs-lookup"><span data-stu-id="6334d-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="6334d-121">在本周的版本中，您可以在**工作人员窗体 > 核对清单**中将核对清单应用于具有一个或多个雇用的员工。</span><span class="sxs-lookup"><span data-stu-id="6334d-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="6334d-122">福利开放登记预览功能已删除</span><span class="sxs-lookup"><span data-stu-id="6334d-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="6334d-123">连同我们在[Core HR 的战略投资推动卓越运营](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)博客文章中宣布的消息，Microsoft 已从公开预览中删除福利开放登记功能。</span><span class="sxs-lookup"><span data-stu-id="6334d-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="6334d-124">将来会发布新功能。</span><span class="sxs-lookup"><span data-stu-id="6334d-124">New functionality will be released in the future.</span></span> <span data-ttu-id="6334d-125">不支持福利开放登记功能的生产使用。</span><span class="sxs-lookup"><span data-stu-id="6334d-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6334d-126">即将到期</span><span class="sxs-lookup"><span data-stu-id="6334d-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="6334d-127">打印绩效复查</span><span class="sxs-lookup"><span data-stu-id="6334d-127">Print performance reviews</span></span>

<span data-ttu-id="6334d-128">请参阅“Dynamics 365: 2019 发布波次 2 计划”中的[打印绩效审核](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)。</span><span class="sxs-lookup"><span data-stu-id="6334d-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="6334d-129">“功能管理”工作区</span><span class="sxs-lookup"><span data-stu-id="6334d-129">Feature management workspace</span></span>

<span data-ttu-id="6334d-130">每个版本中都会增加和更新功能。</span><span class="sxs-lookup"><span data-stu-id="6334d-130">Features are added and updated in every release.</span></span> <span data-ttu-id="6334d-131">功能管理体验提供一个工作区，可在其中查看各版本已交付的功能的列表。</span><span class="sxs-lookup"><span data-stu-id="6334d-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="6334d-132">默认情况下，新功能处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="6334d-132">By default, new features are turned off.</span></span> <span data-ttu-id="6334d-133">可使用该工作区开启这些功能并查看其文档。</span><span class="sxs-lookup"><span data-stu-id="6334d-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="6334d-134">要了解有关功能管理带来的更改的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。</span><span class="sxs-lookup"><span data-stu-id="6334d-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
