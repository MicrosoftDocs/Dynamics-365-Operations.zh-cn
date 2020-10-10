---
title: 开始使用计划优化
description: 本主题说明如何开始使用计划优化功能。
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887256"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="df0e8-103">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="df0e8-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df0e8-104">计划优化功能当前不支持 Microsoft Dynamics 365 Supply Chain Management 内置的计划引擎中提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="df0e8-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="df0e8-105">因此，重要的是要评估计划优化中当前可用的功能集是否满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="df0e8-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="df0e8-106">默认情况下，Dynamics Lifecycle Services (LCS) 中默认不启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="df0e8-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="df0e8-107">因此，您有机会在启用之前进行评估。</span><span class="sxs-lookup"><span data-stu-id="df0e8-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="df0e8-108">最终，计划优化将取代现有的内置 Supply Chain Management 计划引擎。</span><span class="sxs-lookup"><span data-stu-id="df0e8-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="df0e8-109">在打开计划优化之前，强烈建议您评估计划优化拟合分析的结果。</span><span class="sxs-lookup"><span data-stu-id="df0e8-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="df0e8-110">有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="df0e8-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="df0e8-111">可用性</span><span class="sxs-lookup"><span data-stu-id="df0e8-111">Availability</span></span>
<span data-ttu-id="df0e8-112">Planning Optimization 当前在以下 Azure 地域中可用：美国、加拿大、欧洲、英国和澳大利亚。</span><span class="sxs-lookup"><span data-stu-id="df0e8-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="df0e8-113">如果您尝试从其他地理区域安装加载项，则 LCS 将显示一条消息，指明不支持该地理区域。</span><span class="sxs-lookup"><span data-stu-id="df0e8-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="df0e8-114">请注意，Planning Optimization 不支持 Dynamics 365 Supply Chain Management 的本地部署。</span><span class="sxs-lookup"><span data-stu-id="df0e8-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="df0e8-115">许可授权</span><span class="sxs-lookup"><span data-stu-id="df0e8-115">Licensing</span></span>

<span data-ttu-id="df0e8-116">如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。</span><span class="sxs-lookup"><span data-stu-id="df0e8-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="df0e8-117">安装加载项</span><span class="sxs-lookup"><span data-stu-id="df0e8-117">Install the add-in</span></span>

<span data-ttu-id="df0e8-118">若要使用计划优化，请安装 Dynamics 365 Supply Chain Management 的计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="df0e8-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="df0e8-119">您可以从 LCS 项目访问加载项，然后从 Supply Chain Management 用户界面 (UI) 启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="df0e8-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="df0e8-120">Planning Optimization 的要求是：支持 LCS 的第 2 层或更高层高可用性环境（不是 OneBox 环境），并且具有 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="df0e8-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="df0e8-121">如果您尝试在 OneBox 环境中安装加载项，则安装将无法完成，因此您需要取消安装。</span><span class="sxs-lookup"><span data-stu-id="df0e8-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="df0e8-122">登录到 LCS，然后打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="df0e8-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="df0e8-123">转到**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="df0e8-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="df0e8-124">向下滚动到**环境加载项**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="df0e8-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="df0e8-125">选择**安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="df0e8-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="df0e8-126">选择**计划优化**。</span><span class="sxs-lookup"><span data-stu-id="df0e8-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="df0e8-127">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="df0e8-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="df0e8-128">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="df0e8-128">Select **Install**.</span></span>
1. <span data-ttu-id="df0e8-129">在**环境加载项**快速选项卡上，您应该看到正在安装计划优化。</span><span class="sxs-lookup"><span data-stu-id="df0e8-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="df0e8-130">几分钟后**正在安装**应会改为**已安装**（您可能需要刷新页面）。</span><span class="sxs-lookup"><span data-stu-id="df0e8-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="df0e8-131">安装后，您就可以在 Dynamics 365 Supply Chain Management 中激活计划优化了。</span><span class="sxs-lookup"><span data-stu-id="df0e8-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="df0e8-132">计划优化集成</span><span class="sxs-lookup"><span data-stu-id="df0e8-132">Planning Optimization integration</span></span>

<span data-ttu-id="df0e8-133">要配置是否应将计划优化加载项用于主计划，请转到**主计划** \> **设置** \> **计划优化参数**。</span><span class="sxs-lookup"><span data-stu-id="df0e8-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="df0e8-134">连接状态</span><span class="sxs-lookup"><span data-stu-id="df0e8-134">Connection status</span></span>

<span data-ttu-id="df0e8-135">连接状态指示 Supply Chain Management 和计划优化服务之间的连接的当前状态。</span><span class="sxs-lookup"><span data-stu-id="df0e8-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="df0e8-136">下表显示可能的值。</span><span class="sxs-lookup"><span data-stu-id="df0e8-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="df0e8-137">连接状态</span><span class="sxs-lookup"><span data-stu-id="df0e8-137">Connection status</span></span> | <span data-ttu-id="df0e8-138">说明</span><span class="sxs-lookup"><span data-stu-id="df0e8-138">Description</span></span> | <span data-ttu-id="df0e8-139">是否可以使用计划优化？</span><span class="sxs-lookup"><span data-stu-id="df0e8-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="df0e8-140">已连接</span><span class="sxs-lookup"><span data-stu-id="df0e8-140">Connected</span></span> | <span data-ttu-id="df0e8-141">已在计划优化服务和 Supply Chain Management 之间建立连接。</span><span class="sxs-lookup"><span data-stu-id="df0e8-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="df0e8-142">是</span><span class="sxs-lookup"><span data-stu-id="df0e8-142">Yes</span></span> |
| <span data-ttu-id="df0e8-143">正在启用连接</span><span class="sxs-lookup"><span data-stu-id="df0e8-143">Enabling connection</span></span> | <span data-ttu-id="df0e8-144">当前正在处理打开计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="df0e8-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="df0e8-145">否</span><span class="sxs-lookup"><span data-stu-id="df0e8-145">No</span></span> |
| <span data-ttu-id="df0e8-146">已断开连接</span><span class="sxs-lookup"><span data-stu-id="df0e8-146">Disconnected</span></span> | <span data-ttu-id="df0e8-147">没有与计划优化服务的连接。</span><span class="sxs-lookup"><span data-stu-id="df0e8-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="df0e8-148">可以从 LCS 打开连接，如本主题前面所述。</span><span class="sxs-lookup"><span data-stu-id="df0e8-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="df0e8-149">否</span><span class="sxs-lookup"><span data-stu-id="df0e8-149">No</span></span> |
| <span data-ttu-id="df0e8-150">正在禁用连接</span><span class="sxs-lookup"><span data-stu-id="df0e8-150">Disabling connection</span></span> | <span data-ttu-id="df0e8-151">当前正在处理关闭计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="df0e8-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="df0e8-152">否</span><span class="sxs-lookup"><span data-stu-id="df0e8-152">No</span></span> |
| <span data-ttu-id="df0e8-153">正在获取状态</span><span class="sxs-lookup"><span data-stu-id="df0e8-153">Getting status</span></span> | <span data-ttu-id="df0e8-154">系统正在等待来自计划优化服务的状态信息。</span><span class="sxs-lookup"><span data-stu-id="df0e8-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="df0e8-155">否</span><span class="sxs-lookup"><span data-stu-id="df0e8-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="df0e8-156">“使用计划优化”选项</span><span class="sxs-lookup"><span data-stu-id="df0e8-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="df0e8-157">**使用计划优化**选项的设置确定哪个计划引擎用于主计划：</span><span class="sxs-lookup"><span data-stu-id="df0e8-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="df0e8-158">**是** – 计划优化用于主计划。</span><span class="sxs-lookup"><span data-stu-id="df0e8-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="df0e8-159">**否** – 内置 Supply Chain Management 计划引擎用于主计划。</span><span class="sxs-lookup"><span data-stu-id="df0e8-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="df0e8-160">如果在**使用计划优化**选项设置为**是**的情况下触发了为内置 Supply Chain Management 计划引擎创建的现有计划批处理作业，这些作业将失败。</span><span class="sxs-lookup"><span data-stu-id="df0e8-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="df0e8-161">与设置集成</span><span class="sxs-lookup"><span data-stu-id="df0e8-161">Integration with the setup</span></span>

<span data-ttu-id="df0e8-162">如果打开了计划优化预览，则使用计划优化加载项来完成主计划。</span><span class="sxs-lookup"><span data-stu-id="df0e8-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="df0e8-163">在这种情况下，主计划结果和功能会受到影响。</span><span class="sxs-lookup"><span data-stu-id="df0e8-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df0e8-164">其他资源</span><span class="sxs-lookup"><span data-stu-id="df0e8-164">Additional resources</span></span>

[<span data-ttu-id="df0e8-165">预览条款和条件</span><span class="sxs-lookup"><span data-stu-id="df0e8-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="df0e8-166">计划优化概览</span><span class="sxs-lookup"><span data-stu-id="df0e8-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="df0e8-167">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="df0e8-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="df0e8-168">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="df0e8-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="df0e8-169">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="df0e8-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="df0e8-170">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="df0e8-170">Cancel a planning job</span></span>](cancel-planning-job.md)
