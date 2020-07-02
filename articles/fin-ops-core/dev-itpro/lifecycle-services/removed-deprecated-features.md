---
title: Lifecycle Services (LCS) 中已移除或弃用的功能
description: 本主题介绍已经从 Microsoft Dynamics Lifecycle Services (LCS) 移除或计划移除的功能。
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e571cc26f55e0bd7a1eef301e193921e0b3f8e31
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454687"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="00be6-103">Lifecycle Services (LCS) 中已移除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="00be6-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="00be6-104">本主题介绍已从 Microsoft Dynamics Lifecycle Services (LCS) 移除或弃用的功能。</span><span class="sxs-lookup"><span data-stu-id="00be6-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="00be6-105">*已移除*的功能在服务中不再可用。</span><span class="sxs-lookup"><span data-stu-id="00be6-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="00be6-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="00be6-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="00be6-107">提供此列表是为了让您可以在制定自己的计划时考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="00be6-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="00be6-108">2019 年 10 月公告</span><span class="sxs-lookup"><span data-stu-id="00be6-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="00be6-109">业务流程建模器中的流程图图表</span><span class="sxs-lookup"><span data-stu-id="00be6-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="00be6-110"><strong>弃用/移除的原因</strong></span><span class="sxs-lookup"><span data-stu-id="00be6-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="00be6-111">我们正在弃用业务流程建模器 (BPM) 中的流程图图表组件，因为旧版设计导致使用率较低。</span><span class="sxs-lookup"><span data-stu-id="00be6-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00be6-112"><strong>被另一个功能取代？</strong></span><span class="sxs-lookup"><span data-stu-id="00be6-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="00be6-113">否</span><span class="sxs-lookup"><span data-stu-id="00be6-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00be6-114"><strong>影响的区域</strong></span><span class="sxs-lookup"><span data-stu-id="00be6-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="00be6-115">业务流程建模器</span><span class="sxs-lookup"><span data-stu-id="00be6-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00be6-116"><strong>状态</strong></span><span class="sxs-lookup"><span data-stu-id="00be6-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="00be6-117">已弃用：BPM 中的流程图图表组件预计将于 2020 年移除。</span><span class="sxs-lookup"><span data-stu-id="00be6-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="00be6-118">以下功能将不可用：</span><span class="sxs-lookup"><span data-stu-id="00be6-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="00be6-119">所有流程图均为只读，不可编辑。</span><span class="sxs-lookup"><span data-stu-id="00be6-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="00be6-120">与流程图活动关联的形状属性也将不可用。</span><span class="sxs-lookup"><span data-stu-id="00be6-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="00be6-121">这些流程图既包括自动生成的默认流程图，也包括基于这些默认流程图修改的自定义流程图。</span><span class="sxs-lookup"><span data-stu-id="00be6-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="00be6-122">流程步骤为只读，不可编辑。</span><span class="sxs-lookup"><span data-stu-id="00be6-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="00be6-123">旧版适应/差距分析功能将不再可用。</span><span class="sxs-lookup"><span data-stu-id="00be6-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="00be6-124">因此，不会再自动创建差距列表或提供导出。</span><span class="sxs-lookup"><span data-stu-id="00be6-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="00be6-125"><strong>注意：</strong>此功能先前已被弃用，已由 Microsoft Azure DevOps 集成取代。</span><span class="sxs-lookup"><span data-stu-id="00be6-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="00be6-126">将不再提供流程图的版本历史记录。</span><span class="sxs-lookup"><span data-stu-id="00be6-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
