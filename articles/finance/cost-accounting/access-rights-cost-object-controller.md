---
title: 成本对象控制器的访问权限
description: 此主题提供关于成本对象控制员访问权限的信息。
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897616"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="fbad6-103">成本对象控制器的访问权限</span><span class="sxs-lookup"><span data-stu-id="fbad6-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbad6-104">**成本控制** 工作区是经理可以查看其成本对象的性能的一个中心点。</span><span class="sxs-lookup"><span data-stu-id="fbad6-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="fbad6-105">此工作区使经理可以使用成本核算数据，即使他们不是成本会计员。</span><span class="sxs-lookup"><span data-stu-id="fbad6-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="fbad6-106">出于安全原因，应仅允许经理查看与他们负责的具体成本对象有关的成本核算数据。</span><span class="sxs-lookup"><span data-stu-id="fbad6-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="fbad6-107">成本核算中有四个唯一角色。</span><span class="sxs-lookup"><span data-stu-id="fbad6-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="fbad6-108">角色名称</span><span class="sxs-lookup"><span data-stu-id="fbad6-108">Role name</span></span>               | <span data-ttu-id="fbad6-109">许可证</span><span class="sxs-lookup"><span data-stu-id="fbad6-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="fbad6-110">成本会计经理</span><span class="sxs-lookup"><span data-stu-id="fbad6-110">Cost accounting manager</span></span> | <span data-ttu-id="fbad6-111">活动</span><span class="sxs-lookup"><span data-stu-id="fbad6-111">Activity</span></span>     |
| <span data-ttu-id="fbad6-112">成本核算师</span><span class="sxs-lookup"><span data-stu-id="fbad6-112">Cost accountant</span></span>         | <span data-ttu-id="fbad6-113">Operations</span><span class="sxs-lookup"><span data-stu-id="fbad6-113">Operations</span></span>   |
| <span data-ttu-id="fbad6-114">成本核算师</span><span class="sxs-lookup"><span data-stu-id="fbad6-114">Cost accountant clerk</span></span>   | <span data-ttu-id="fbad6-115">Operations</span><span class="sxs-lookup"><span data-stu-id="fbad6-115">Operations</span></span>   |
| <span data-ttu-id="fbad6-116">成本对象控制器</span><span class="sxs-lookup"><span data-stu-id="fbad6-116">Cost object controller</span></span>  | <span data-ttu-id="fbad6-117">团队成员</span><span class="sxs-lookup"><span data-stu-id="fbad6-117">Team members</span></span> |

<span data-ttu-id="fbad6-118">此主题说明如何向经理分配 **成本对象控制员** 角色。</span><span class="sxs-lookup"><span data-stu-id="fbad6-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="fbad6-119">将 **成本对象控制员** 角色分配到经理后，经理可执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="fbad6-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="fbad6-120">访问 **成本控制** 工作区（在客户端中）。</span><span class="sxs-lookup"><span data-stu-id="fbad6-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="fbad6-121">钻取并获得支持钻取体验的页面的查看权限。</span><span class="sxs-lookup"><span data-stu-id="fbad6-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="fbad6-122">访问 **成本控制** 工作区（在移动应用程序中）。</span><span class="sxs-lookup"><span data-stu-id="fbad6-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="fbad6-123">**成本对象控制员** 角色不控制用户可以访问和查看其数据的成本对象。</span><span class="sxs-lookup"><span data-stu-id="fbad6-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="fbad6-124">行级别安全通过维度层次结构和访问列表层次结构提供。</span><span class="sxs-lookup"><span data-stu-id="fbad6-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="fbad6-125">授予访问权限</span><span class="sxs-lookup"><span data-stu-id="fbad6-125">Grant access rights</span></span>
<span data-ttu-id="fbad6-126">以下示例显示维度层次结构的样式。</span><span class="sxs-lookup"><span data-stu-id="fbad6-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="fbad6-127">**维度层次结构明细**</span><span class="sxs-lookup"><span data-stu-id="fbad6-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="fbad6-128">维度层次结构名称</span><span class="sxs-lookup"><span data-stu-id="fbad6-128">Dimension hierarchy name</span></span> | <span data-ttu-id="fbad6-129">维度</span><span class="sxs-lookup"><span data-stu-id="fbad6-129">Dimension</span></span>    | <span data-ttu-id="fbad6-130">维度层次结构类型名称</span><span class="sxs-lookup"><span data-stu-id="fbad6-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="fbad6-131">访问列表层次结构</span><span class="sxs-lookup"><span data-stu-id="fbad6-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="fbad6-132">组织</span><span class="sxs-lookup"><span data-stu-id="fbad6-132">Organization</span></span>             | <span data-ttu-id="fbad6-133">成本中心</span><span class="sxs-lookup"><span data-stu-id="fbad6-133">Cost centers</span></span> | <span data-ttu-id="fbad6-134">维度分类层次结构</span><span class="sxs-lookup"><span data-stu-id="fbad6-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="fbad6-135">**是**</span><span class="sxs-lookup"><span data-stu-id="fbad6-135">**Yes**</span></span>               |

<span data-ttu-id="fbad6-136">您可以使用层次结构设计器中的 **用户** 快速选项卡在各节点上插入一个或多个用户 ID。</span><span class="sxs-lookup"><span data-stu-id="fbad6-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="fbad6-137">节点</span><span class="sxs-lookup"><span data-stu-id="fbad6-137">Nodes</span></span>                 | <span data-ttu-id="fbad6-138">用户</span><span class="sxs-lookup"><span data-stu-id="fbad6-138">Users</span></span>            | <span data-ttu-id="fbad6-139">起始维度成员</span><span class="sxs-lookup"><span data-stu-id="fbad6-139">From dimension member</span></span>     |   <span data-ttu-id="fbad6-140">截止维度成员</span><span class="sxs-lookup"><span data-stu-id="fbad6-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="fbad6-141">组织</span><span class="sxs-lookup"><span data-stu-id="fbad6-141">Organization</span></span>                      | <span data-ttu-id="fbad6-142">本杰明，克莱尔</span><span class="sxs-lookup"><span data-stu-id="fbad6-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="fbad6-143">&nbsp;&nbsp;管理</span><span class="sxs-lookup"><span data-stu-id="fbad6-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="fbad6-144">四月</span><span class="sxs-lookup"><span data-stu-id="fbad6-144">April</span></span>            |                           |                         |
| <span data-ttu-id="fbad6-145">&nbsp;&nbsp;&nbsp;&nbsp;财务</span><span class="sxs-lookup"><span data-stu-id="fbad6-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="fbad6-146">艾丽西亚</span><span class="sxs-lookup"><span data-stu-id="fbad6-146">Alicia</span></span>           | <span data-ttu-id="fbad6-147">CC002</span><span class="sxs-lookup"><span data-stu-id="fbad6-147">CC002</span></span>                     | <span data-ttu-id="fbad6-148">CC003</span><span class="sxs-lookup"><span data-stu-id="fbad6-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="fbad6-149">CC007</span><span class="sxs-lookup"><span data-stu-id="fbad6-149">CC007</span></span>                     | <span data-ttu-id="fbad6-150">CC007</span><span class="sxs-lookup"><span data-stu-id="fbad6-150">CC007</span></span>                   |
| <span data-ttu-id="fbad6-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="fbad6-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="fbad6-152">尔尼</span><span class="sxs-lookup"><span data-stu-id="fbad6-152">Arnie</span></span>            | <span data-ttu-id="fbad6-153">CC001</span><span class="sxs-lookup"><span data-stu-id="fbad6-153">CC001</span></span>                     | <span data-ttu-id="fbad6-154">CC001</span><span class="sxs-lookup"><span data-stu-id="fbad6-154">CC001</span></span>                   |
| <span data-ttu-id="fbad6-155">&nbsp;&nbsp;生产</span><span class="sxs-lookup"><span data-stu-id="fbad6-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="fbad6-156">大卫</span><span class="sxs-lookup"><span data-stu-id="fbad6-156">David</span></span>            |                           |                         |
| <span data-ttu-id="fbad6-157">&nbsp;&nbsp;&nbsp;&nbsp;包装</span><span class="sxs-lookup"><span data-stu-id="fbad6-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="fbad6-158">爱伦</span><span class="sxs-lookup"><span data-stu-id="fbad6-158">Ellen</span></span>            | <span data-ttu-id="fbad6-159">CC005</span><span class="sxs-lookup"><span data-stu-id="fbad6-159">CC005</span></span>                     | <span data-ttu-id="fbad6-160">CC005</span><span class="sxs-lookup"><span data-stu-id="fbad6-160">CC005</span></span>                   |
| <span data-ttu-id="fbad6-161">&nbsp;&nbsp;&nbsp;&nbsp;程序集</span><span class="sxs-lookup"><span data-stu-id="fbad6-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="fbad6-162">克里斯</span><span class="sxs-lookup"><span data-stu-id="fbad6-162">Chris</span></span>            | <span data-ttu-id="fbad6-163">CC006</span><span class="sxs-lookup"><span data-stu-id="fbad6-163">CC006</span></span>                     | <span data-ttu-id="fbad6-164">CC006</span><span class="sxs-lookup"><span data-stu-id="fbad6-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="fbad6-165">成本会计员应分配到该层次结构的顶层，以便他们可以查看成本核算中的所有条目。</span><span class="sxs-lookup"><span data-stu-id="fbad6-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="fbad6-166">应用访问列表层次结构及其安全设置前，**成本核算参数** 页 **常规** 选项卡上的 **为成本对象维度成员启用视图访问** 选项必须设置为 **是**（**成本核算** > **设置** > **参数**）。</span><span class="sxs-lookup"><span data-stu-id="fbad6-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="fbad6-167">访问列表层次结构的设置用于控制在以下区域显示的数据：</span><span class="sxs-lookup"><span data-stu-id="fbad6-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="fbad6-168">**成本控制** 工作区（在客户端中）：</span><span class="sxs-lookup"><span data-stu-id="fbad6-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="fbad6-169">用于钻取的页面上的数据</span><span class="sxs-lookup"><span data-stu-id="fbad6-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="fbad6-170">**成本控制** 工作区（在移动应用程序中）：</span><span class="sxs-lookup"><span data-stu-id="fbad6-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="fbad6-171">卡内余额</span><span class="sxs-lookup"><span data-stu-id="fbad6-171">Balances in cards</span></span>

- <span data-ttu-id="fbad6-172">Microsoft Power BI：</span><span class="sxs-lookup"><span data-stu-id="fbad6-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="fbad6-173">Power BI 可视化项中显示的数据</span><span class="sxs-lookup"><span data-stu-id="fbad6-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="fbad6-174">在 Dynamics 365 Finance 客户端中嵌入的数据 Power BI 可视化项</span><span class="sxs-lookup"><span data-stu-id="fbad6-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="fbad6-175">在访问列表层次结构可能会影响 Power BI 中的数据前，Power BI 中的访问列表层次结构和行级别安全性必须配对。</span><span class="sxs-lookup"><span data-stu-id="fbad6-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="fbad6-176">有关详细信息，请参阅 [设置成本核算内容包的安全性](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)。</span><span class="sxs-lookup"><span data-stu-id="fbad6-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="fbad6-177">此主题说明使用 **成本控制** 工作区前必须具备的先决条件。</span><span class="sxs-lookup"><span data-stu-id="fbad6-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="fbad6-178">其他资源</span><span class="sxs-lookup"><span data-stu-id="fbad6-178">Additional resources</span></span>

- [<span data-ttu-id="fbad6-179">成本控制工作区</span><span class="sxs-lookup"><span data-stu-id="fbad6-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="fbad6-180">维度层次结构</span><span class="sxs-lookup"><span data-stu-id="fbad6-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="fbad6-181">设置成本核算内容包的安全性</span><span class="sxs-lookup"><span data-stu-id="fbad6-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
