---
title: Dynamics 365 Talent - Core HR（2018 年 9 月 17 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
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
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 20d3da65028b455ab1602e3a8b443ea7e585b1f0
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030888"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-17-2018"></a><span data-ttu-id="a1684-103">Dynamics 365 Talent - Core HR（2018 年 9 月 17 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="a1684-103">What's new or changed in Dynamics 365 Talent - Core HR (September 17, 2018)</span></span>

<span data-ttu-id="a1684-104">**内部版本 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="a1684-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="a1684-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="a1684-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="a1684-106">休假和缺勤 – 根据工作时数累积时间</span><span class="sxs-lookup"><span data-stu-id="a1684-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="a1684-107">已向休假计划添加了一种新的累积类型。</span><span class="sxs-lookup"><span data-stu-id="a1684-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="a1684-108">累积计划现在可以基于服务月数或工作时数。</span><span class="sxs-lookup"><span data-stu-id="a1684-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="a1684-109">有关详细信息，请参阅 [根据工作时数累积休假时间](leave-accrue-hours-worked.md)。</span><span class="sxs-lookup"><span data-stu-id="a1684-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18-for-finance-and-operations"></a><span data-ttu-id="a1684-110">Finance and Operations 平台更新 18</span><span class="sxs-lookup"><span data-stu-id="a1684-110">Platform update 18 for Finance and Operations</span></span>

<span data-ttu-id="a1684-111">Finance and Operations 平台更新 18 现在是 Talent 版本的一部分。</span><span class="sxs-lookup"><span data-stu-id="a1684-111">Platform update 18 for Finance and Operations is now part of the Talent release.</span></span> 

-   <span data-ttu-id="a1684-112">可通过个性化设置隐藏必填字段和其他字段。</span><span class="sxs-lookup"><span data-stu-id="a1684-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="a1684-113">这样用户就可以通过不显示缺省采用业务逻辑提供的值的字段来简化体验。</span><span class="sxs-lookup"><span data-stu-id="a1684-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="a1684-114">如果保存时隐藏的必填字段为空，也可以暂时将其显示。</span><span class="sxs-lookup"><span data-stu-id="a1684-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="a1684-115">在 Finance and Operations 平台更新 18 中，Talent Web 客户端的视觉对象现在与 Microsoft Fluent Design 风格统一。</span><span class="sxs-lookup"><span data-stu-id="a1684-115">In Platform update 18 for Finance and Operations, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="a1684-116">字段处于“读取模式”时，只需选择字段中的编辑选项即可将窗体切换为编辑。</span><span class="sxs-lookup"><span data-stu-id="a1684-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="a1684-117">只读模式下字段显示方式的更改。</span><span class="sxs-lookup"><span data-stu-id="a1684-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="a1684-118">工作区和页面中的标题加粗显示。</span><span class="sxs-lookup"><span data-stu-id="a1684-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="a1684-119">已改进了非替换查找的行为。</span><span class="sxs-lookup"><span data-stu-id="a1684-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="a1684-120">有关详细信息，请参阅[非替换查找行为的改进](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/non-replacing-lookups)。</span><span class="sxs-lookup"><span data-stu-id="a1684-120">For more information, see [Improved behavior for non-replacing lookups](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/non-replacing-lookups).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="a1684-121">缺陷修复</span><span class="sxs-lookup"><span data-stu-id="a1684-121">Bug fixes</span></span>

<span data-ttu-id="a1684-122">此版本中还包含若干缺陷修复（包括对 ACA、ADA 和 I9 的引用），并且仅在美国公司中才会启用。</span><span class="sxs-lookup"><span data-stu-id="a1684-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
