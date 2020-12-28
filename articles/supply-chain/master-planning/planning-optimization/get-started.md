---
title: 开始使用计划优化
description: 本主题说明如何开始使用计划优化功能。
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423444"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="9eecc-103">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="9eecc-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9eecc-104">正如[之前宣布](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios)的那样，计划优化计划替换现有的内置主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="9eecc-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="9eecc-105">如果当前使用内置的主计划引擎，则应该立即开始计划迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="9eecc-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="9eecc-106">立即开始迁移过程非常重要，因为强制执行弃用操作可能会影响您的操作。</span><span class="sxs-lookup"><span data-stu-id="9eecc-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="9eecc-107">为了避免在最后强制执行弃用时出现问题，我们强烈建议您在 2020 年 12 月 1 日之前完成迁移。</span><span class="sxs-lookup"><span data-stu-id="9eecc-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="9eecc-108">计划优化功能当前不支持 Supply Chain Management 中内置的计划引擎中提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="9eecc-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="9eecc-109">因此，重要的是要评估计划优化中当前可用的功能集是否满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="9eecc-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="9eecc-110">计划优化功能当前在 Dynamics Lifecycle Services (LCS) 中默认未启用，因此您有机会在启用该功能之前进行评估。</span><span class="sxs-lookup"><span data-stu-id="9eecc-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="9eecc-111">如果您的主计划流程不包括生产（主计划生成的计划生产订单）并且您需要版本 10.0.15 以上的内置主计划引擎，则需要在迁移到计划优化过程中请求一个例外。</span><span class="sxs-lookup"><span data-stu-id="9eecc-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="9eecc-112">从版本 10.0.16 开始，当运行内置主计划而不生成计划生产订单时，环境中将显示一条错误。</span><span class="sxs-lookup"><span data-stu-id="9eecc-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="9eecc-113">应该将计划优化用于在主计划期间不生成计划生产订单的所有新部署。</span><span class="sxs-lookup"><span data-stu-id="9eecc-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="9eecc-114">运行内置主计划引擎而不生成计划生产订单的现有环境的所有者将收到一封邮件，其中包含有关例外流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9eecc-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="9eecc-115">我们建议您与合作伙伴一起评估和计划迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="9eecc-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="9eecc-116">在打开计划优化之前，强烈建议您评估计划优化拟合分析的结果。</span><span class="sxs-lookup"><span data-stu-id="9eecc-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="9eecc-117">有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="9eecc-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="9eecc-118">可用性</span><span class="sxs-lookup"><span data-stu-id="9eecc-118">Availability</span></span>
<span data-ttu-id="9eecc-119">Planning Optimization 当前在以下 Azure 地域中可用：美国、加拿大、欧洲、英国和澳大利亚。</span><span class="sxs-lookup"><span data-stu-id="9eecc-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="9eecc-120">如果您尝试从其他地理区域安装加载项，则 LCS 将显示一条消息，指明不支持该地理区域。</span><span class="sxs-lookup"><span data-stu-id="9eecc-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="9eecc-121">请注意，Planning Optimization 不支持 Dynamics 365 Supply Chain Management 的本地部署。</span><span class="sxs-lookup"><span data-stu-id="9eecc-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="9eecc-122">许可授权</span><span class="sxs-lookup"><span data-stu-id="9eecc-122">Licensing</span></span>

<span data-ttu-id="9eecc-123">如果您可以使用当前的许可证来运行主计划，则无需购买其他许可证即可开始使用计划优化。</span><span class="sxs-lookup"><span data-stu-id="9eecc-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="9eecc-124">安装加载项</span><span class="sxs-lookup"><span data-stu-id="9eecc-124">Install the add-in</span></span>

<span data-ttu-id="9eecc-125">若要使用计划优化，请安装 Dynamics 365 Supply Chain Management 的计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="9eecc-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9eecc-126">您可以从 LCS 项目访问加载项，然后从 Supply Chain Management 用户界面 (UI) 启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="9eecc-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="9eecc-127">Planning Optimization 的要求是：支持 LCS 的第 2 层或更高层高可用性环境（不是 OneBox 环境），并且具有 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="9eecc-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="9eecc-128">如果您尝试在 OneBox 环境中安装加载项，则安装将无法完成，因此您需要取消安装。</span><span class="sxs-lookup"><span data-stu-id="9eecc-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="9eecc-129">登录到 LCS，然后打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="9eecc-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="9eecc-130">转到 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="9eecc-131">向下滚动到 **环境加载项** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="9eecc-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="9eecc-132">选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="9eecc-133">选择 **计划优化**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="9eecc-134">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="9eecc-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="9eecc-135">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-135">Select **Install**.</span></span>
1. <span data-ttu-id="9eecc-136">在 **环境加载项** 快速选项卡上，您应该看到正在安装计划优化。</span><span class="sxs-lookup"><span data-stu-id="9eecc-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="9eecc-137">几分钟后 **正在安装** 应会改为 **已安装**（您可能需要刷新页面）。</span><span class="sxs-lookup"><span data-stu-id="9eecc-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="9eecc-138">安装后，您就可以在 Dynamics 365 Supply Chain Management 中激活计划优化了。</span><span class="sxs-lookup"><span data-stu-id="9eecc-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="9eecc-139">安装计划优化加载项的主要目的是连接服务和环境。</span><span class="sxs-lookup"><span data-stu-id="9eecc-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="9eecc-140">因此，无论在环境之间移动任何代码，都必须在将使用计划优化的每个环境上分别安装该加载项。</span><span class="sxs-lookup"><span data-stu-id="9eecc-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="9eecc-141">计划优化集成</span><span class="sxs-lookup"><span data-stu-id="9eecc-141">Planning Optimization integration</span></span>

<span data-ttu-id="9eecc-142">要配置是否应将计划优化加载项用于主计划，请转到 **主计划** \> **设置** \> **计划优化参数**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="9eecc-143">连接状态</span><span class="sxs-lookup"><span data-stu-id="9eecc-143">Connection status</span></span>

<span data-ttu-id="9eecc-144">连接状态指示 Supply Chain Management 和计划优化服务之间的连接的当前状态。</span><span class="sxs-lookup"><span data-stu-id="9eecc-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="9eecc-145">下表显示可能的值。</span><span class="sxs-lookup"><span data-stu-id="9eecc-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="9eecc-146">连接状态</span><span class="sxs-lookup"><span data-stu-id="9eecc-146">Connection status</span></span> | <span data-ttu-id="9eecc-147">说明</span><span class="sxs-lookup"><span data-stu-id="9eecc-147">Description</span></span> | <span data-ttu-id="9eecc-148">是否可以使用计划优化？</span><span class="sxs-lookup"><span data-stu-id="9eecc-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="9eecc-149">已连接</span><span class="sxs-lookup"><span data-stu-id="9eecc-149">Connected</span></span> | <span data-ttu-id="9eecc-150">已在计划优化服务和 Supply Chain Management 之间建立连接。</span><span class="sxs-lookup"><span data-stu-id="9eecc-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="9eecc-151">是</span><span class="sxs-lookup"><span data-stu-id="9eecc-151">Yes</span></span> |
| <span data-ttu-id="9eecc-152">正在启用连接</span><span class="sxs-lookup"><span data-stu-id="9eecc-152">Enabling connection</span></span> | <span data-ttu-id="9eecc-153">当前正在处理打开计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="9eecc-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="9eecc-154">否</span><span class="sxs-lookup"><span data-stu-id="9eecc-154">No</span></span> |
| <span data-ttu-id="9eecc-155">已断开连接</span><span class="sxs-lookup"><span data-stu-id="9eecc-155">Disconnected</span></span> | <span data-ttu-id="9eecc-156">没有与计划优化服务的连接。</span><span class="sxs-lookup"><span data-stu-id="9eecc-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="9eecc-157">可以从 LCS 打开连接，如本主题前面所述。</span><span class="sxs-lookup"><span data-stu-id="9eecc-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="9eecc-158">否</span><span class="sxs-lookup"><span data-stu-id="9eecc-158">No</span></span> |
| <span data-ttu-id="9eecc-159">正在禁用连接</span><span class="sxs-lookup"><span data-stu-id="9eecc-159">Disabling connection</span></span> | <span data-ttu-id="9eecc-160">当前正在处理关闭计划优化服务连接的请求。</span><span class="sxs-lookup"><span data-stu-id="9eecc-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="9eecc-161">否</span><span class="sxs-lookup"><span data-stu-id="9eecc-161">No</span></span> |
| <span data-ttu-id="9eecc-162">正在获取状态</span><span class="sxs-lookup"><span data-stu-id="9eecc-162">Getting status</span></span> | <span data-ttu-id="9eecc-163">系统正在等待来自计划优化服务的状态信息。</span><span class="sxs-lookup"><span data-stu-id="9eecc-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="9eecc-164">否</span><span class="sxs-lookup"><span data-stu-id="9eecc-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="9eecc-165">“使用计划优化”选项</span><span class="sxs-lookup"><span data-stu-id="9eecc-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="9eecc-166">**使用计划优化** 选项的设置确定哪个计划引擎用于主计划：</span><span class="sxs-lookup"><span data-stu-id="9eecc-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="9eecc-167">**是** – 计划优化用于主计划。</span><span class="sxs-lookup"><span data-stu-id="9eecc-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="9eecc-168">**否** – 内置 Supply Chain Management 计划引擎用于主计划。</span><span class="sxs-lookup"><span data-stu-id="9eecc-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="9eecc-169">如果在 **使用计划优化** 选项设置为 **是** 的情况下触发了为内置 Supply Chain Management 计划引擎创建的现有计划批处理作业，这些作业将失败。</span><span class="sxs-lookup"><span data-stu-id="9eecc-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="9eecc-170">与设置集成</span><span class="sxs-lookup"><span data-stu-id="9eecc-170">Integration with the setup</span></span>

<span data-ttu-id="9eecc-171">如果打开了计划优化，则使用计划优化加载项来完成主计划。</span><span class="sxs-lookup"><span data-stu-id="9eecc-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="9eecc-172">在这种情况下，主计划结果和功能会受到影响。</span><span class="sxs-lookup"><span data-stu-id="9eecc-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9eecc-173">其他资源</span><span class="sxs-lookup"><span data-stu-id="9eecc-173">Additional resources</span></span>

[<span data-ttu-id="9eecc-174">预览条款和条件</span><span class="sxs-lookup"><span data-stu-id="9eecc-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="9eecc-175">计划优化概览</span><span class="sxs-lookup"><span data-stu-id="9eecc-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="9eecc-176">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="9eecc-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="9eecc-177">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="9eecc-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="9eecc-178">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="9eecc-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="9eecc-179">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="9eecc-179">Cancel a planning job</span></span>](cancel-planning-job.md)
