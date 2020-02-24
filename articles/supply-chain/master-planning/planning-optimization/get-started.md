---
title: 开始使用计划优化
description: 本主题说明如何开始使用计划优化功能。
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971456"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="a7075-103">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="a7075-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="a7075-104">计划优化功能当前不支持 Microsoft Dynamics 365 Supply Chain Management 内置的计划引擎中提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="a7075-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a7075-105">因此，重要的是要评估计划优化中当前可用的功能集是否满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="a7075-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="a7075-106">默认情况下，Dynamics Lifecycle Services (LCS) 中默认不启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="a7075-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="a7075-107">因此，您有机会在启用之前进行评估。</span><span class="sxs-lookup"><span data-stu-id="a7075-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="a7075-108">最终，计划优化将取代现有的内置 Supply Chain Management 计划引擎。</span><span class="sxs-lookup"><span data-stu-id="a7075-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="a7075-109">在打开计划优化之前，强烈建议您评估计划优化拟合分析的结果。</span><span class="sxs-lookup"><span data-stu-id="a7075-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="a7075-110">有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="a7075-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="a7075-111">许可授权</span><span class="sxs-lookup"><span data-stu-id="a7075-111">Licensing</span></span>

<span data-ttu-id="a7075-112">如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。</span><span class="sxs-lookup"><span data-stu-id="a7075-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="a7075-113">安装加载项</span><span class="sxs-lookup"><span data-stu-id="a7075-113">Install the add-in</span></span>

<span data-ttu-id="a7075-114">若要使用计划优化，请安装 Dynamics 365 Supply Chain Management 的计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="a7075-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a7075-115">您可以从 LCS 项目访问加载项，然后从 Supply Chain Management 用户界面 (UI) 启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="a7075-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="a7075-116">登录到 LCS，然后打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="a7075-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="a7075-117">转到**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="a7075-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="a7075-118">向下滚动到**环境加载项**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a7075-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="a7075-119">选择**安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="a7075-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="a7075-120">选择**计划优化**。</span><span class="sxs-lookup"><span data-stu-id="a7075-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="a7075-121">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="a7075-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="a7075-122">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="a7075-122">Select **Install**.</span></span>
1. <span data-ttu-id="a7075-123">在**环境加载项**快速选项卡上，您应该看到正在安装计划优化。</span><span class="sxs-lookup"><span data-stu-id="a7075-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="a7075-124">几分钟后**正在安装**应会改为**已安装**（您可能需要刷新页面）。</span><span class="sxs-lookup"><span data-stu-id="a7075-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="a7075-125">安装后，您就可以在 Dynamics 365 Supply Chain Management 中激活计划优化了。</span><span class="sxs-lookup"><span data-stu-id="a7075-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="a7075-126">计划优化集成</span><span class="sxs-lookup"><span data-stu-id="a7075-126">Planning Optimization integration</span></span>

<span data-ttu-id="a7075-127">要配置是否应将计划优化加载项用于主计划，请转到**主计划** \> **设置** \> **计划优化参数**。</span><span class="sxs-lookup"><span data-stu-id="a7075-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="a7075-128">连接状态</span><span class="sxs-lookup"><span data-stu-id="a7075-128">Connection status</span></span>

<span data-ttu-id="a7075-129">连接状态指示 Supply Chain Management 和计划优化服务之间的连接的当前状态。</span><span class="sxs-lookup"><span data-stu-id="a7075-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="a7075-130">下表显示可能的值。</span><span class="sxs-lookup"><span data-stu-id="a7075-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="a7075-131">连接状态</span><span class="sxs-lookup"><span data-stu-id="a7075-131">Connection status</span></span> | <span data-ttu-id="a7075-132">说明</span><span class="sxs-lookup"><span data-stu-id="a7075-132">Description</span></span> | <span data-ttu-id="a7075-133">是否可以使用计划优化？</span><span class="sxs-lookup"><span data-stu-id="a7075-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="a7075-134">已连接</span><span class="sxs-lookup"><span data-stu-id="a7075-134">Connected</span></span> | <span data-ttu-id="a7075-135">已在计划优化服务和 Supply Chain Management 之间建立连接。</span><span class="sxs-lookup"><span data-stu-id="a7075-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="a7075-136">是</span><span class="sxs-lookup"><span data-stu-id="a7075-136">Yes</span></span> |
| <span data-ttu-id="a7075-137">正在启用连接</span><span class="sxs-lookup"><span data-stu-id="a7075-137">Enabling connection</span></span> | <span data-ttu-id="a7075-138">当前正在处理打开计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="a7075-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="a7075-139">否</span><span class="sxs-lookup"><span data-stu-id="a7075-139">No</span></span> |
| <span data-ttu-id="a7075-140">已断开连接</span><span class="sxs-lookup"><span data-stu-id="a7075-140">Disconnected</span></span> | <span data-ttu-id="a7075-141">没有与计划优化服务的连接。</span><span class="sxs-lookup"><span data-stu-id="a7075-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="a7075-142">可以从 LCS 打开连接，如本主题前面所述。</span><span class="sxs-lookup"><span data-stu-id="a7075-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="a7075-143">否</span><span class="sxs-lookup"><span data-stu-id="a7075-143">No</span></span> |
| <span data-ttu-id="a7075-144">正在禁用连接</span><span class="sxs-lookup"><span data-stu-id="a7075-144">Disabling connection</span></span> | <span data-ttu-id="a7075-145">当前正在处理关闭计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="a7075-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="a7075-146">否</span><span class="sxs-lookup"><span data-stu-id="a7075-146">No</span></span> |
| <span data-ttu-id="a7075-147">正在获取状态</span><span class="sxs-lookup"><span data-stu-id="a7075-147">Getting status</span></span> | <span data-ttu-id="a7075-148">系统正在等待来自计划优化服务的状态信息。</span><span class="sxs-lookup"><span data-stu-id="a7075-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="a7075-149">否</span><span class="sxs-lookup"><span data-stu-id="a7075-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="a7075-150">“使用计划优化”选项</span><span class="sxs-lookup"><span data-stu-id="a7075-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="a7075-151">**使用计划优化**选项的设置确定哪个计划引擎用于主计划：</span><span class="sxs-lookup"><span data-stu-id="a7075-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="a7075-152">**是** – 计划优化用于主计划。</span><span class="sxs-lookup"><span data-stu-id="a7075-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="a7075-153">**否** – 内置 Supply Chain Management 计划引擎用于主计划。</span><span class="sxs-lookup"><span data-stu-id="a7075-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="a7075-154">如果在**使用计划优化**选项设置为**是**的情况下触发了为内置 Supply Chain Management 计划引擎创建的现有计划批处理作业，这些作业将失败。</span><span class="sxs-lookup"><span data-stu-id="a7075-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="a7075-155">与设置集成</span><span class="sxs-lookup"><span data-stu-id="a7075-155">Integration with the setup</span></span>

<span data-ttu-id="a7075-156">如果打开了计划优化预览，则使用计划优化加载项来完成主计划。</span><span class="sxs-lookup"><span data-stu-id="a7075-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="a7075-157">在这种情况下，主计划结果和功能会受到影响。</span><span class="sxs-lookup"><span data-stu-id="a7075-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="a7075-158">相关资源</span><span class="sxs-lookup"><span data-stu-id="a7075-158">Related resources</span></span>

[<span data-ttu-id="a7075-159">预览条款和条件</span><span class="sxs-lookup"><span data-stu-id="a7075-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="a7075-160">计划优化概述</span><span class="sxs-lookup"><span data-stu-id="a7075-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="a7075-161">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="a7075-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="a7075-162">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="a7075-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="a7075-163">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="a7075-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="a7075-164">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="a7075-164">Cancel a planning job</span></span>](cancel-planning-job.md)
