---
title: 成本对象控制器的访问权限
description: 此主题提供关于成本对象控制员访问权限的信息。
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fd1ed875e5c6e3f8ada3b13ea8cc05f98526691d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440787"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="eb07a-103">成本对象控制器的访问权限</span><span class="sxs-lookup"><span data-stu-id="eb07a-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb07a-104">**成本控制** 工作区是经理可以查看其成本对象的性能的一个中心点。</span><span class="sxs-lookup"><span data-stu-id="eb07a-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="eb07a-105">此工作区使经理可以使用成本核算数据，即使他们不是成本会计员。</span><span class="sxs-lookup"><span data-stu-id="eb07a-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="eb07a-106">出于安全原因，应仅允许经理查看与他们负责的具体成本对象有关的成本核算数据。</span><span class="sxs-lookup"><span data-stu-id="eb07a-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="eb07a-107">成本核算中有四个唯一角色。</span><span class="sxs-lookup"><span data-stu-id="eb07a-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="eb07a-108">角色名称</span><span class="sxs-lookup"><span data-stu-id="eb07a-108">Role name</span></span>               | <span data-ttu-id="eb07a-109">许可证</span><span class="sxs-lookup"><span data-stu-id="eb07a-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="eb07a-110">成本会计经理</span><span class="sxs-lookup"><span data-stu-id="eb07a-110">Cost accounting manager</span></span> | <span data-ttu-id="eb07a-111">活动</span><span class="sxs-lookup"><span data-stu-id="eb07a-111">Activity</span></span>     |
| <span data-ttu-id="eb07a-112">成本核算师</span><span class="sxs-lookup"><span data-stu-id="eb07a-112">Cost accountant</span></span>         | <span data-ttu-id="eb07a-113">Operations</span><span class="sxs-lookup"><span data-stu-id="eb07a-113">Operations</span></span>   |
| <span data-ttu-id="eb07a-114">成本核算师</span><span class="sxs-lookup"><span data-stu-id="eb07a-114">Cost accountant clerk</span></span>   | <span data-ttu-id="eb07a-115">Operations</span><span class="sxs-lookup"><span data-stu-id="eb07a-115">Operations</span></span>   |
| <span data-ttu-id="eb07a-116">成本对象控制器</span><span class="sxs-lookup"><span data-stu-id="eb07a-116">Cost object controller</span></span>  | <span data-ttu-id="eb07a-117">团队成员</span><span class="sxs-lookup"><span data-stu-id="eb07a-117">Team members</span></span> |

<span data-ttu-id="eb07a-118">此主题说明如何向经理分配 **成本对象控制员** 角色。</span><span class="sxs-lookup"><span data-stu-id="eb07a-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="eb07a-119">将 **成本对象控制员** 角色分配到经理后，经理可执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="eb07a-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="eb07a-120">访问 **成本控制** 工作区（在客户端中）。</span><span class="sxs-lookup"><span data-stu-id="eb07a-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="eb07a-121">钻取并获得支持钻取体验的页面的查看权限。</span><span class="sxs-lookup"><span data-stu-id="eb07a-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="eb07a-122">访问 **成本控制** 工作区（在移动应用程序中）。</span><span class="sxs-lookup"><span data-stu-id="eb07a-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="eb07a-123">**成本对象控制员** 角色不控制用户可以访问和查看其数据的成本对象。</span><span class="sxs-lookup"><span data-stu-id="eb07a-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="eb07a-124">行级别安全通过维度层次结构和访问列表层次结构提供。</span><span class="sxs-lookup"><span data-stu-id="eb07a-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="eb07a-125">授予访问权限</span><span class="sxs-lookup"><span data-stu-id="eb07a-125">Grant access rights</span></span>
<span data-ttu-id="eb07a-126">以下示例显示维度层次结构的样式。</span><span class="sxs-lookup"><span data-stu-id="eb07a-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="eb07a-127">**维度层次结构明细**</span><span class="sxs-lookup"><span data-stu-id="eb07a-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="eb07a-128">维度层次结构名称</span><span class="sxs-lookup"><span data-stu-id="eb07a-128">Dimension hierarchy name</span></span> | <span data-ttu-id="eb07a-129">维度</span><span class="sxs-lookup"><span data-stu-id="eb07a-129">Dimension</span></span>    | <span data-ttu-id="eb07a-130">维度层次结构类型名称</span><span class="sxs-lookup"><span data-stu-id="eb07a-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="eb07a-131">访问列表层次结构</span><span class="sxs-lookup"><span data-stu-id="eb07a-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="eb07a-132">组织</span><span class="sxs-lookup"><span data-stu-id="eb07a-132">Organization</span></span>             | <span data-ttu-id="eb07a-133">成本中心</span><span class="sxs-lookup"><span data-stu-id="eb07a-133">Cost centers</span></span> | <span data-ttu-id="eb07a-134">维度分类层次结构</span><span class="sxs-lookup"><span data-stu-id="eb07a-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="eb07a-135">**是**</span><span class="sxs-lookup"><span data-stu-id="eb07a-135">**Yes**</span></span>               |

<span data-ttu-id="eb07a-136">您可以使用层次结构设计器中的 **用户** 快速选项卡在各节点上插入一个或多个用户 ID。</span><span class="sxs-lookup"><span data-stu-id="eb07a-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="eb07a-137">用户</span><span class="sxs-lookup"><span data-stu-id="eb07a-137">Users</span></span>            | <span data-ttu-id="eb07a-138">维度成员范围</span><span class="sxs-lookup"><span data-stu-id="eb07a-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="eb07a-139">**节点**</span><span class="sxs-lookup"><span data-stu-id="eb07a-139">**Nodes**</span></span>                         | <span data-ttu-id="eb07a-140">**用户 ID**</span><span class="sxs-lookup"><span data-stu-id="eb07a-140">**User ID**</span></span>      | <span data-ttu-id="eb07a-141">**起始维度成员**</span><span class="sxs-lookup"><span data-stu-id="eb07a-141">**From dimension member**</span></span> | <span data-ttu-id="eb07a-142">**截止维度成员**</span><span class="sxs-lookup"><span data-stu-id="eb07a-142">**To dimension member**</span></span> |
| <span data-ttu-id="eb07a-143">组织</span><span class="sxs-lookup"><span data-stu-id="eb07a-143">Organization</span></span>                      | <span data-ttu-id="eb07a-144">本杰明，克莱尔</span><span class="sxs-lookup"><span data-stu-id="eb07a-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="eb07a-145">&nbsp;&nbsp;管理</span><span class="sxs-lookup"><span data-stu-id="eb07a-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="eb07a-146">四月</span><span class="sxs-lookup"><span data-stu-id="eb07a-146">April</span></span>            |                           |                         |
| <span data-ttu-id="eb07a-147">&nbsp;&nbsp;&nbsp;&nbsp;财务</span><span class="sxs-lookup"><span data-stu-id="eb07a-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="eb07a-148">艾丽西亚</span><span class="sxs-lookup"><span data-stu-id="eb07a-148">Alicia</span></span>           | <span data-ttu-id="eb07a-149">CC002</span><span class="sxs-lookup"><span data-stu-id="eb07a-149">CC002</span></span>                     | <span data-ttu-id="eb07a-150">CC003</span><span class="sxs-lookup"><span data-stu-id="eb07a-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="eb07a-151">CC007</span><span class="sxs-lookup"><span data-stu-id="eb07a-151">CC007</span></span>                     | <span data-ttu-id="eb07a-152">CC007</span><span class="sxs-lookup"><span data-stu-id="eb07a-152">CC007</span></span>                   |
| <span data-ttu-id="eb07a-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="eb07a-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="eb07a-154">尔尼</span><span class="sxs-lookup"><span data-stu-id="eb07a-154">Arnie</span></span>            | <span data-ttu-id="eb07a-155">CC001</span><span class="sxs-lookup"><span data-stu-id="eb07a-155">CC001</span></span>                     | <span data-ttu-id="eb07a-156">CC001</span><span class="sxs-lookup"><span data-stu-id="eb07a-156">CC001</span></span>                   |
| <span data-ttu-id="eb07a-157">&nbsp;&nbsp;生产</span><span class="sxs-lookup"><span data-stu-id="eb07a-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="eb07a-158">大卫</span><span class="sxs-lookup"><span data-stu-id="eb07a-158">David</span></span>            |                           |                         |
| <span data-ttu-id="eb07a-159">&nbsp;&nbsp;&nbsp;&nbsp;包装</span><span class="sxs-lookup"><span data-stu-id="eb07a-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="eb07a-160">爱伦</span><span class="sxs-lookup"><span data-stu-id="eb07a-160">Ellen</span></span>            | <span data-ttu-id="eb07a-161">CC005</span><span class="sxs-lookup"><span data-stu-id="eb07a-161">CC005</span></span>                     | <span data-ttu-id="eb07a-162">CC005</span><span class="sxs-lookup"><span data-stu-id="eb07a-162">CC005</span></span>                   |
| <span data-ttu-id="eb07a-163">&nbsp;&nbsp;&nbsp;&nbsp;程序集</span><span class="sxs-lookup"><span data-stu-id="eb07a-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="eb07a-164">克里斯</span><span class="sxs-lookup"><span data-stu-id="eb07a-164">Chris</span></span>            | <span data-ttu-id="eb07a-165">CC006</span><span class="sxs-lookup"><span data-stu-id="eb07a-165">CC006</span></span>                     | <span data-ttu-id="eb07a-166">CC006</span><span class="sxs-lookup"><span data-stu-id="eb07a-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="eb07a-167">成本会计员应分配到该层次结构的顶层，以便他们可以查看成本核算中的所有条目。</span><span class="sxs-lookup"><span data-stu-id="eb07a-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="eb07a-168">应用访问列表层次结构及其安全设置前，**成本核算参数** 页 **常规** 选项卡上的 **为成本对象维度成员启用视图访问** 选项必须设置为 **是**（**成本核算** > **设置** > **参数**）。</span><span class="sxs-lookup"><span data-stu-id="eb07a-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="eb07a-169">访问列表层次结构的设置用于控制在以下区域显示的数据：</span><span class="sxs-lookup"><span data-stu-id="eb07a-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="eb07a-170">**成本控制** 工作区（在客户端中）：</span><span class="sxs-lookup"><span data-stu-id="eb07a-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="eb07a-171">用于钻取的页面上的数据</span><span class="sxs-lookup"><span data-stu-id="eb07a-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="eb07a-172">**成本控制** 工作区（在移动应用程序中）：</span><span class="sxs-lookup"><span data-stu-id="eb07a-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="eb07a-173">卡内余额</span><span class="sxs-lookup"><span data-stu-id="eb07a-173">Balances in cards</span></span>

- <span data-ttu-id="eb07a-174">Microsoft Power BI：</span><span class="sxs-lookup"><span data-stu-id="eb07a-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="eb07a-175">Power BI 可视化项中显示的数据</span><span class="sxs-lookup"><span data-stu-id="eb07a-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="eb07a-176">在 Dynamics 365 Finance 客户端中嵌入的数据 Power BI 可视化项</span><span class="sxs-lookup"><span data-stu-id="eb07a-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="eb07a-177">在访问列表层次结构可能会影响 Power BI 中的数据前，Power BI 中的访问列表层次结构和行级别安全性必须配对。</span><span class="sxs-lookup"><span data-stu-id="eb07a-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="eb07a-178">有关详细信息，请参阅 [设置成本核算内容包的安全性](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)。</span><span class="sxs-lookup"><span data-stu-id="eb07a-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="eb07a-179">此主题说明使用 **成本控制** 工作区前必须具备的先决条件。</span><span class="sxs-lookup"><span data-stu-id="eb07a-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="eb07a-180">其他资源</span><span class="sxs-lookup"><span data-stu-id="eb07a-180">Additional resources</span></span>

- [<span data-ttu-id="eb07a-181">成本控制工作区</span><span class="sxs-lookup"><span data-stu-id="eb07a-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="eb07a-182">维度层次结构</span><span class="sxs-lookup"><span data-stu-id="eb07a-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="eb07a-183">设置成本核算内容包的安全性</span><span class="sxs-lookup"><span data-stu-id="eb07a-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
