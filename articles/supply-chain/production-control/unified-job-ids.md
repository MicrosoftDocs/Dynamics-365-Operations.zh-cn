---
title: 统一作业 ID 编号规则
description: 此功能提供一个统一的编号规则，可为生产控制、制造执行和考勤管理模块生成作业 ID。
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824933"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="67137-103">统一作业 ID 编号规则</span><span class="sxs-lookup"><span data-stu-id="67137-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67137-104">此功能提供一个统一的编号规则，可为生产控制、制造执行和考勤管理模块生成作业 ID。</span><span class="sxs-lookup"><span data-stu-id="67137-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="67137-105">之前，您能够为每个模块选择不同的编号规则，如果其中两个或多个规则使用相同的格式，可能会导致作业 ID 冲突。</span><span class="sxs-lookup"><span data-stu-id="67137-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="67137-106">此类冲突可能导致数据损坏。</span><span class="sxs-lookup"><span data-stu-id="67137-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="67137-107">为您的系统启用此功能</span><span class="sxs-lookup"><span data-stu-id="67137-107">Turn on this feature for your system</span></span>

<span data-ttu-id="67137-108">如果您的系统尚未包含本主题中所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *统一作业 ID 编号规则* 功能。</span><span class="sxs-lookup"><span data-stu-id="67137-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="67137-109">设置统一作业 ID 编号规则</span><span class="sxs-lookup"><span data-stu-id="67137-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="67137-110">启用此功能后，将弃用生产控制、制造执行和考勤管理模块的参数页面上的现有 **作业标识** 编号规则设置，并将添加新的 **统一作业 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="67137-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="67137-111">**统一作业 ID** 值由全部三个模块共享，从而确保所有模块引用相同的编号规则。</span><span class="sxs-lookup"><span data-stu-id="67137-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="67137-112">因此，作业 ID 在全部三个模块中都是唯一的，并且永远不会发生冲突。</span><span class="sxs-lookup"><span data-stu-id="67137-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="67137-113">若要设置统一作业 ID 编号规则：</span><span class="sxs-lookup"><span data-stu-id="67137-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="67137-114">如上一部分所述打开功能。</span><span class="sxs-lookup"><span data-stu-id="67137-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="67137-115">确定要用于统一作业 ID 的编号规则，或创建新的编号规则。</span><span class="sxs-lookup"><span data-stu-id="67137-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="67137-116">有关详细信息，请参阅[编号规则概述](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="67137-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="67137-117">转到 **生产控制参数**、**制造执行参数** 或 **考勤管理参数** 页面。</span><span class="sxs-lookup"><span data-stu-id="67137-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="67137-118">选择哪个页面都没有关系，因为在其中任何页面上进行此设置时，所有其他页面都将自动更新。</span><span class="sxs-lookup"><span data-stu-id="67137-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="67137-119">在选定的参数页面上打开 **编号规则** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="67137-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="67137-120">将之前标识的 **编号规则代码** 分配到网格的 **统一作业 ID**。</span><span class="sxs-lookup"><span data-stu-id="67137-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
