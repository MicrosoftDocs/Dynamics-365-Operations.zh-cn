---
title: 开始使用计划优化
description: 本主题说明如何开始使用计划优化功能。
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773907"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="fe7a7-103">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="fe7a7-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="fe7a7-104">计划优化功能当前不支持 Microsoft Dynamics 365 Supply Chain Management 内置的计划引擎中提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fe7a7-105">因此，重要的是要评估计划优化中当前可用的功能集是否满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="fe7a7-106">默认情况下，Dynamics Lifecycle Services (LCS) 中默认不启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="fe7a7-107">因此，您有机会在启用之前进行评估。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="fe7a7-108">最终，计划优化将取代现有的内置 Supply Chain Management 计划引擎。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="fe7a7-109">在打开计划优化之前，强烈建议您评估计划优化拟合分析的结果。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="fe7a7-110">有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="fe7a7-111">许可授权</span><span class="sxs-lookup"><span data-stu-id="fe7a7-111">Licensing</span></span>

<span data-ttu-id="fe7a7-112">如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="fe7a7-113">安装加载项</span><span class="sxs-lookup"><span data-stu-id="fe7a7-113">Install the add-in</span></span>

<span data-ttu-id="fe7a7-114">若要使用计划优化，请安装 Dynamics 365 Supply Chain Management 的计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fe7a7-115">您可以从 LCS 项目访问加载项，然后从 Supply Chain Management 用户界面 (UI) 启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="fe7a7-116">登录到 LCS，然后打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="fe7a7-117">转到**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="fe7a7-118">选择**维护**，或向下滚动到**环境加载项**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="fe7a7-119">选择**安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="fe7a7-120">选择**计划优化**。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="fe7a7-121">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="fe7a7-122">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="fe7a7-123">计划优化集成</span><span class="sxs-lookup"><span data-stu-id="fe7a7-123">Planning Optimization integration</span></span>

<span data-ttu-id="fe7a7-124">要配置是否应将计划优化加载项用于主计划，请转到**主计划** \> **设置** \> **计划优化集成** \> **集成参数**。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="fe7a7-125">连接状态</span><span class="sxs-lookup"><span data-stu-id="fe7a7-125">Connection status</span></span>

<span data-ttu-id="fe7a7-126">连接状态指示 Supply Chain Management 和计划优化服务之间的连接的当前状态。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="fe7a7-127">下表显示可能的值。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="fe7a7-128">连接状态</span><span class="sxs-lookup"><span data-stu-id="fe7a7-128">Connection status</span></span> | <span data-ttu-id="fe7a7-129">说明</span><span class="sxs-lookup"><span data-stu-id="fe7a7-129">Description</span></span> | <span data-ttu-id="fe7a7-130">是否可以使用计划优化？</span><span class="sxs-lookup"><span data-stu-id="fe7a7-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="fe7a7-131">已连接</span><span class="sxs-lookup"><span data-stu-id="fe7a7-131">Connected</span></span> | <span data-ttu-id="fe7a7-132">已在计划优化服务和 Supply Chain Management 之间建立连接。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="fe7a7-133">是</span><span class="sxs-lookup"><span data-stu-id="fe7a7-133">Yes</span></span> |
| <span data-ttu-id="fe7a7-134">正在启用连接</span><span class="sxs-lookup"><span data-stu-id="fe7a7-134">Enabling connection</span></span> | <span data-ttu-id="fe7a7-135">当前正在处理打开计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="fe7a7-136">否</span><span class="sxs-lookup"><span data-stu-id="fe7a7-136">No</span></span> |
| <span data-ttu-id="fe7a7-137">已断开连接</span><span class="sxs-lookup"><span data-stu-id="fe7a7-137">Disconnected</span></span> | <span data-ttu-id="fe7a7-138">没有与计划优化服务的连接。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="fe7a7-139">可以从 LCS 打开连接，如本主题前面所述。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="fe7a7-140">否</span><span class="sxs-lookup"><span data-stu-id="fe7a7-140">No</span></span> |
| <span data-ttu-id="fe7a7-141">正在禁用连接</span><span class="sxs-lookup"><span data-stu-id="fe7a7-141">Disabling connection</span></span> | <span data-ttu-id="fe7a7-142">当前正在处理关闭计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="fe7a7-143">否</span><span class="sxs-lookup"><span data-stu-id="fe7a7-143">No</span></span> |
| <span data-ttu-id="fe7a7-144">正在获取状态</span><span class="sxs-lookup"><span data-stu-id="fe7a7-144">Getting status</span></span> | <span data-ttu-id="fe7a7-145">系统正在等待来自计划优化服务的状态信息。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="fe7a7-146">否</span><span class="sxs-lookup"><span data-stu-id="fe7a7-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="fe7a7-147">“使用计划优化”选项</span><span class="sxs-lookup"><span data-stu-id="fe7a7-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="fe7a7-148">**使用计划优化**选项的设置确定哪个计划引擎用于主计划：</span><span class="sxs-lookup"><span data-stu-id="fe7a7-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="fe7a7-149">**是** – 计划优化用于主计划。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="fe7a7-150">**否** – 内置 Supply Chain Management 计划引擎用于主计划。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="fe7a7-151">如果在**使用计划优化**选项设置为**是**的情况下触发了为内置 Supply Chain Management 计划引擎创建的现有计划批处理作业，这些作业将失败。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="fe7a7-152">与设置集成</span><span class="sxs-lookup"><span data-stu-id="fe7a7-152">Integration with the setup</span></span>

<span data-ttu-id="fe7a7-153">如果打开了计划优化预览，则使用计划优化加载项来完成主计划。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="fe7a7-154">在这种情况下，主计划结果和功能会受到影响。</span><span class="sxs-lookup"><span data-stu-id="fe7a7-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="fe7a7-155">相关资源</span><span class="sxs-lookup"><span data-stu-id="fe7a7-155">Related resources</span></span>

[<span data-ttu-id="fe7a7-156">预览条款和条件</span><span class="sxs-lookup"><span data-stu-id="fe7a7-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="fe7a7-157">计划优化概述</span><span class="sxs-lookup"><span data-stu-id="fe7a7-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="fe7a7-158">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="fe7a7-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="fe7a7-159">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="fe7a7-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="fe7a7-160">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="fe7a7-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="fe7a7-161">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="fe7a7-161">Cancel a planning job</span></span>](cancel-planning-job.md)
