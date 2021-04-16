---
title: 制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit
description: 本主题提供有关制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit 的信息。
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3eacc9d0cf53fa8af3ff166006cb8fab32445331
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836702"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a><span data-ttu-id="2e52f-103">制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit</span><span class="sxs-lookup"><span data-stu-id="2e52f-103">Cloud and edge scale units for manufacturing and warehouse management workloads</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2e52f-104">通过 Cloud Scale Unit 和 Edge Scale Unit，可在不同的环境中分配车间和仓库执行工作负荷。</span><span class="sxs-lookup"><span data-stu-id="2e52f-104">Cloud and edge scale units enable distribution of shop floor and warehouse execution workloads among different environments.</span></span> <span data-ttu-id="2e52f-105">此功能可以帮助提高性能，防止服务中断并最大化运行时间。</span><span class="sxs-lookup"><span data-stu-id="2e52f-105">This functionality can help improve performance, prevent service interruptions, and maximize uptime.</span></span> <span data-ttu-id="2e52f-106">它通过以下加载项提供：</span><span class="sxs-lookup"><span data-stu-id="2e52f-106">It's provided by the following add-ins:</span></span>

- <span data-ttu-id="2e52f-107">Dynamics 365 Supply Chain Management 的 Cloud Scale Unit 加载项</span><span class="sxs-lookup"><span data-stu-id="2e52f-107">Cloud Scale Unit Add-in for Dynamics 365 Supply Chain Management</span></span>
- <span data-ttu-id="2e52f-108">Dynamics 365 Supply Chain Management 的 Edge Scale Unit 加载项</span><span class="sxs-lookup"><span data-stu-id="2e52f-108">Edge Scale Unit Add-in for Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="2e52f-109">从事制造和分销业务的公司必须能够不中断且大规模地全天候运行关键业务流程。</span><span class="sxs-lookup"><span data-stu-id="2e52f-109">Companies that work with manufacturing and distribution must be able to run key business processes 24/7, without interruption and at scale.</span></span> <span data-ttu-id="2e52f-110">通过 Cloud Scale Unit 和 Edge Scale Unit，公司能够不中断地运行重要的任务关键型制造和仓库流程，即使偶尔遇到网络连接或延迟问题也是如此。</span><span class="sxs-lookup"><span data-stu-id="2e52f-110">Cloud and edge scale units enable companies to run key mission-critical manufacturing and warehouse processes without interruption, even when faced with occasional network connectivity or latency issues.</span></span>

## <a name="public-preview-information"></a><span data-ttu-id="2e52f-111">公开预览版信息</span><span class="sxs-lookup"><span data-stu-id="2e52f-111">Public preview information</span></span>

<span data-ttu-id="2e52f-112">预览版提供一个环境用作 Dynamics 365 Supply Chain Management 环境的基于云的中心，还提供一个环境用作 Cloud Scale Unit。</span><span class="sxs-lookup"><span data-stu-id="2e52f-112">The preview provides one environment that functions as a cloud-based hub of your Dynamics 365 Supply Chain Management environment and one environment that functions as a cloud scale unit.</span></span>

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a><span data-ttu-id="2e52f-113">预览版可用性</span><span class="sxs-lookup"><span data-stu-id="2e52f-113">Preview availability</span></span>

<span data-ttu-id="2e52f-114">Cloud Scale Unit 和 Edge Scale Unit 的预览版在 2020 年 10 月提供给 Supply Chain Management 的现有客户。</span><span class="sxs-lookup"><span data-stu-id="2e52f-114">The preview for cloud and edge scale units becomes available for existing customers of Supply Chain Management in October 2020.</span></span>

<span data-ttu-id="2e52f-115">若要访问在 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) 环境中部署的 10 月预览版本 10.0.15/平台更新 39，您必须成为 Supply Chain Management 的预览版提前访问计划（称为 PEAP）的一部分。</span><span class="sxs-lookup"><span data-stu-id="2e52f-115">To access the October preview release 10.0.15/Platform update 39 for deployment in your [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) environment, you must be part of the preview early access program (also known as PEAP) for Supply Chain Management.</span></span> <span data-ttu-id="2e52f-116">如果您已经是更广泛的 [Dynamics Insider Program](https://experience.dynamics.com/insider) 的成员，则可以加入 PEAP。</span><span class="sxs-lookup"><span data-stu-id="2e52f-116">You can join PEAP if you're already a member of the broader [Dynamics Insider Program](https://experience.dynamics.com/insider).</span></span> <span data-ttu-id="2e52f-117">只需选择名为“Finance & Operations：预览版提前访问计划 (PEAP)”的特定计划。</span><span class="sxs-lookup"><span data-stu-id="2e52f-117">Just select the specific program that is named "Finance & Operations: Preview early access program (PEAP)."</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e52f-118">Supply Chain Management 的缩放单元功能仅在您同意 [Finance and Operations 的 Cloud + Edge 预览版条款](https://Aka.ms/SCMCnETerms)时才可用。</span><span class="sxs-lookup"><span data-stu-id="2e52f-118">The scale unit capability for Supply Chain Management is made available only if you agree to the [Cloud + Edge Preview for Finance and Operations terms](https://Aka.ms/SCMCnETerms).</span></span>

### <a name="data-processing-for-the-preview"></a><span data-ttu-id="2e52f-119">预览版的数据处理</span><span class="sxs-lookup"><span data-stu-id="2e52f-119">Data processing for the preview</span></span>

<span data-ttu-id="2e52f-120">在公开预览版期间，某些管理服务将仅在美国托管。</span><span class="sxs-lookup"><span data-stu-id="2e52f-120">During the public preview, some management services will only be hosted in the United States.</span></span> <span data-ttu-id="2e52f-121">但是，在该功能公开发布后，这些管理服务将在 Supply Chain Management 支持的所有地区提供。</span><span class="sxs-lookup"><span data-stu-id="2e52f-121">However, when the feature becomes generally available, these management services will be available in all geographies supported by Supply Chain Management.</span></span> <span data-ttu-id="2e52f-122">这会影响缩放单元管理器使用的管理信息的传输和存储，包括：</span><span class="sxs-lookup"><span data-stu-id="2e52f-122">This affects the transfer and storage of administrative information used by the scale unit manager, including:</span></span>

- <span data-ttu-id="2e52f-123">您的租户名称和 ID</span><span class="sxs-lookup"><span data-stu-id="2e52f-123">Your tenant names and IDs</span></span>
- <span data-ttu-id="2e52f-124">您的 LCS 项目 ID</span><span class="sxs-lookup"><span data-stu-id="2e52f-124">Your LCS project IDs</span></span>
- <span data-ttu-id="2e52f-125">用于登录的管理员电子邮件</span><span class="sxs-lookup"><span data-stu-id="2e52f-125">Administrator emails used to sign in</span></span>
- <span data-ttu-id="2e52f-126">中心的环境 ID 和缩放单元</span><span class="sxs-lookup"><span data-stu-id="2e52f-126">Environment IDs for hub and scale units</span></span>
- <span data-ttu-id="2e52f-127">工作负荷配置</span><span class="sxs-lookup"><span data-stu-id="2e52f-127">Workload configurations</span></span>
- <span data-ttu-id="2e52f-128">收集的指标（例如延迟和吞吐量），显示在地图分析页面上</span><span class="sxs-lookup"><span data-stu-id="2e52f-128">Collected metrics (such as latency and throughput) which are displayed on the map analysis page</span></span>

<span data-ttu-id="2e52f-129">关闭预览环境后，将删除传输到美国数据中心和存储在其中的数据。</span><span class="sxs-lookup"><span data-stu-id="2e52f-129">Data transferred to and stored in the US data centers will be deleted when your preview environments are shut down.</span></span>

### <a name="sign-up-for-the-preview"></a><span data-ttu-id="2e52f-130">注册预览</span><span class="sxs-lookup"><span data-stu-id="2e52f-130">Sign up for the preview</span></span>

<span data-ttu-id="2e52f-131">若要注册 Supply Chain Management 的 Cloud 和 Edge 预览版，您的组织必须已经有一个实际的 Supply Chain Management 云环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-131">To sign up for the cloud and edge preview for Supply Chain Management, your organization must already have a live Supply Chain Management cloud environment.</span></span>

<span data-ttu-id="2e52f-132">缩放单元功能当前在公开预览版中。</span><span class="sxs-lookup"><span data-stu-id="2e52f-132">The scale unit capabilities are currently in public preview.</span></span> <span data-ttu-id="2e52f-133">在注册时，您必须在特定租户上使用用户帐户。</span><span class="sxs-lookup"><span data-stu-id="2e52f-133">When you sign up, you must use a user account on the specific tenant.</span></span> <span data-ttu-id="2e52f-134">对于该租户中的活动 Dynamics 365 LCS 项目，您还必须是 LCS 中的项目所有者或环境管理员。</span><span class="sxs-lookup"><span data-stu-id="2e52f-134">You must also be a project owner or an environment admin in LCS for an active Dynamics 365 LCS project in that tenant.</span></span>

<span data-ttu-id="2e52f-135">在注册预览版时，您将选择一个租户并执行注册步骤。</span><span class="sxs-lookup"><span data-stu-id="2e52f-135">When you sign up for the preview, you will select a tenant and go through the sign-up steps.</span></span> <span data-ttu-id="2e52f-136">一旦 Microsoft 可以分配预览版容量，我们将向您发送一封电子邮件，其中包含相应 LCS 项目的两个环境（中心和缩放单元）的预配详细信息和促销（促销）代码。</span><span class="sxs-lookup"><span data-stu-id="2e52f-136">As soon as Microsoft can allocate preview capacity, we will send you an email that includes the provisioning details and the promotion (promo) codes for two environments (a hub and a scale unit) for the appropriate LCS project.</span></span> <span data-ttu-id="2e52f-137">然后，您能够将两个环境部署为第 2 层沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-137">You will then be able to deploy the two environments as tier-2 sandbox environments.</span></span> <span data-ttu-id="2e52f-138">这些环境将在促销代码创建之日起的 60 天内有效。</span><span class="sxs-lookup"><span data-stu-id="2e52f-138">Those environments will be valid 60 days from the creation date of the promo codes.</span></span> <span data-ttu-id="2e52f-139">在完成下一段描述的步骤之前，您不应使用这两个环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-139">You should not use the two environments until the step that is described in the next paragraph is completed.</span></span>

<span data-ttu-id="2e52f-140">在与 Microsoft 确认已使用促销代码部署两个环境后，其中一个环境将配置为用作中心，另一个环境将配置为用作缩放单元。</span><span class="sxs-lookup"><span data-stu-id="2e52f-140">After you confirm with Microsoft that the two environments have been deployed by using the promo codes, one of the environments will be configured to work as a hub, and the other will be configured to work as a scale unit.</span></span> <span data-ttu-id="2e52f-141">然后，您可以使用[缩放单元管理器门户](https://aka.ms/SCMSUM)配置缩放单元并部署选定的仓库管理和制造工作负荷。</span><span class="sxs-lookup"><span data-stu-id="2e52f-141">You can then configure the scale units and deploy selected warehouse management and manufacturing workloads by using the [Scale Unit Manager portal](https://aka.ms/SCMSUM).</span></span>

<span data-ttu-id="2e52f-142">预览环境将在 60 天后自动删除。</span><span class="sxs-lookup"><span data-stu-id="2e52f-142">Preview environments will automatically be deleted after 60 days.</span></span> <span data-ttu-id="2e52f-143">但是，如果它们看起来没有在使用，则可能会更快删除。</span><span class="sxs-lookup"><span data-stu-id="2e52f-143">However, they might be deleted sooner if it appears that they aren't being used.</span></span> <span data-ttu-id="2e52f-144">在删除预览环境后，您可以注册并排队等待新的预览版部署。</span><span class="sxs-lookup"><span data-stu-id="2e52f-144">After your preview environments have been deleted, you can sign up and queue up for a new preview deployment.</span></span>

<span data-ttu-id="2e52f-145">若要注册预览版，请转到[缩放单元管理器门户](https://aka.ms/SCMSUM)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-145">To sign up for the preview, go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM).</span></span>

### <a name="limitations-that-apply-during-the-preview-period"></a><span data-ttu-id="2e52f-146">预览版期间适用的限制</span><span class="sxs-lookup"><span data-stu-id="2e52f-146">Limitations that apply during the preview period</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e52f-147">对于此功能的预览版计划的初始阶段，Microsoft 仅支持具有 Cloud Scale Unit 的中心，而不支持具有 Edge Scale Unit 的中心。</span><span class="sxs-lookup"><span data-stu-id="2e52f-147">For the initial phase of the preview program for this feature, Microsoft is supporting only hubs that have cloud scale units, not hubs that have edge scale units.</span></span> <span data-ttu-id="2e52f-148">Edge Scale Unit 在本地安装，并预计在计划的下一阶段可用。</span><span class="sxs-lookup"><span data-stu-id="2e52f-148">Edge scale units are installed on-premises and are expected to become available during an upcoming phase of the program.</span></span>

<span data-ttu-id="2e52f-149">由于 Cloud Scale Unit 和 Edge Scale Unit 是预览功能，因此与它们相关的服务目前仅在有限的国家和地区可用。</span><span class="sxs-lookup"><span data-stu-id="2e52f-149">Because cloud and edge scale units are a preview feature, services that are related to them are currently available in limited countries and regions.</span></span> <span data-ttu-id="2e52f-150">通过启用 Cloud Scale Unit 和 Edge Scale Unit，您确认了解与 Cloud Scale Unit 和 Edge Scale Unit 的配置和处理相关的某些数据可能存储在位于美国的数据中心中。</span><span class="sxs-lookup"><span data-stu-id="2e52f-150">By enabling cloud and edge scale units, you affirm that you understand that some data that is related to the configuration and processing of cloud and edge scale units might be stored in a data center that is located in the United States.</span></span> <span data-ttu-id="2e52f-151">通过启用 Cloud Scale Unit 和 Edge Scale Unit，您还同意 [Finance and Operations 的 Cloud + Edge 预览版条款](https://Aka.ms/SCMCnETerms)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-151">By enabling cloud and edge scale units, you also agree to the [Cloud + Edge Preview for Finance and Operations terms](https://Aka.ms/SCMCnETerms).</span></span> <span data-ttu-id="2e52f-152">若要了解有关 Cloud Scale Unit 和 Edge Scale Unit 的详细信息，请参阅[文档](https://aka.ms/scmcne)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-152">To learn more about cloud and edge scale units, see the [documentation](https://aka.ms/scmcne).</span></span>

<span data-ttu-id="2e52f-153">Microsoft 非常注重您的隐私。</span><span class="sxs-lookup"><span data-stu-id="2e52f-153">Your privacy is important to Microsoft.</span></span> <span data-ttu-id="2e52f-154">若要了解详细信息，请阅读我们的[隐私声明](https://aka.ms/privacy)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-154">To learn more, read our [Privacy Statement](https://aka.ms/privacy).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e52f-155">当在缩放单元上使用工作负荷时，公开预览版中不完全支持某些业务功能。</span><span class="sxs-lookup"><span data-stu-id="2e52f-155">Some business functionality isn't fully supported in the public preview when workloads are used on scale units.</span></span> <span data-ttu-id="2e52f-156">有关功能工作负荷的详细信息，请参阅本主题后面的部分。</span><span class="sxs-lookup"><span data-stu-id="2e52f-156">For more information about the functional workloads, see the sections later in this topic.</span></span>

## <a name="scale-units-and-dedicated-workloads"></a><span data-ttu-id="2e52f-157">缩放单元和专用工作负荷</span><span class="sxs-lookup"><span data-stu-id="2e52f-157">Scale units and dedicated workloads</span></span>

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="具有缩放单元的 Dynamics 365":::

<span data-ttu-id="2e52f-159">缩放单元通过添加专用的处理容量来扩展您的集中 Supply Chain Management 中心环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-159">Scale units extend your central Supply Chain Management hub environment by adding dedicated processing capacity.</span></span> <span data-ttu-id="2e52f-160">缩放单元可在 Cloud 中运行。</span><span class="sxs-lookup"><span data-stu-id="2e52f-160">Scale units can run in the cloud.</span></span> <span data-ttu-id="2e52f-161">或者，它们可在您的本地机构的 Edge 上运行。</span><span class="sxs-lookup"><span data-stu-id="2e52f-161">Alternatively, they can run on the edge at your local facility premises.</span></span> <span data-ttu-id="2e52f-162">缩放单元可以从中心环境临时断开连接。</span><span class="sxs-lookup"><span data-stu-id="2e52f-162">Scale units can temporarily be disconnected from the hub environment.</span></span> <span data-ttu-id="2e52f-163">在它们连接后，缩放单元将收到运行已分配工作负荷的专用处理所需的所有信息。</span><span class="sxs-lookup"><span data-stu-id="2e52f-163">When they are connected, scale units receive all the information that is required to run the dedicated processing for assigned workloads.</span></span>

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="公开预览版中的缩放单元选项":::

<span data-ttu-id="2e52f-165">对于公开预览版，您可以使用缩放单元管理器门户在 Cloud Scale Unit 上配置具有选定工作负荷的中心环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-165">For the public preview, you can configure a hub environment with selected workloads on a cloud scale unit by using the Scale Unit Manager portal.</span></span> <span data-ttu-id="2e52f-166">有权访问本地业务数据 (LBD) 本地环境的预览版参与者还可以将 LBD 环境配置为 Edge Scale Unit。</span><span class="sxs-lookup"><span data-stu-id="2e52f-166">Preview participants who have access to a Local Business Data (LBD) on-premises environment can also configure the LBD environment as an edge scale unit.</span></span>

<span data-ttu-id="2e52f-167">工作负荷是一组定义的业务功能，可以进行分解并委派给缩放单元。</span><span class="sxs-lookup"><span data-stu-id="2e52f-167">A workload is a defined set of business functionality that can be factored out and delegated to a scale unit.</span></span> <span data-ttu-id="2e52f-168">当前，预览版具有两种类型的工作负荷：</span><span class="sxs-lookup"><span data-stu-id="2e52f-168">Currently, the preview features two types of workloads:</span></span>

- <span data-ttu-id="2e52f-169">制造执行</span><span class="sxs-lookup"><span data-stu-id="2e52f-169">Manufacturing execution</span></span>
- <span data-ttu-id="2e52f-170">仓库管理</span><span class="sxs-lookup"><span data-stu-id="2e52f-170">Warehouse management</span></span>

<span data-ttu-id="2e52f-171">您可以为每个缩放单元分配其中一种工作负荷。</span><span class="sxs-lookup"><span data-stu-id="2e52f-171">You can assign one of each type of workload per scale unit.</span></span> 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="2e52f-172">缩放单元中的专用制造执行工作负荷功能</span><span class="sxs-lookup"><span data-stu-id="2e52f-172">Dedicated manufacturing execution workload capabilities in a scale unit</span></span>

<span data-ttu-id="2e52f-173">对于制造执行，Cloud Scale Unit 和 Edge Scale Unit 提供以下功能，即使 Edge 单元未连接到 Cloud：</span><span class="sxs-lookup"><span data-stu-id="2e52f-173">For manufacturing execution, cloud and edge scale units deliver the following capabilities, even when the edge units aren't connected to the cloud:</span></span>

- <span data-ttu-id="2e52f-174">机器操作员和车间主管可以访问操作生产计划。</span><span class="sxs-lookup"><span data-stu-id="2e52f-174">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="2e52f-175">机器操作员可以通过运行离散和流程制造作业来使计划保持最新状态。</span><span class="sxs-lookup"><span data-stu-id="2e52f-175">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="2e52f-176">车间主管可以调整操作计划。</span><span class="sxs-lookup"><span data-stu-id="2e52f-176">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="2e52f-177">工作人员可以访问在 Edge 中上下班打卡的考勤管理，以确保正确计算工作人员工资。</span><span class="sxs-lookup"><span data-stu-id="2e52f-177">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="2e52f-178">有关详细信息，请参阅[制造缩放单元工作负荷详细信息](cloud-edge-workload-manufacturing.md)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-178">For more information, see the [manufacturing scale unit workload details](cloud-edge-workload-manufacturing.md).</span></span>

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="2e52f-179">缩放单元中的专用仓库管理工作负荷功能</span><span class="sxs-lookup"><span data-stu-id="2e52f-179">Dedicated warehouse management workload capabilities in a scale unit</span></span>

<span data-ttu-id="2e52f-180">对于仓库管理，Cloud Scale Unit 和 Edge Scale Unit 提供以下功能，即使 Edge 单元未连接到 Cloud：</span><span class="sxs-lookup"><span data-stu-id="2e52f-180">For warehouse management, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the cloud:</span></span>

- <span data-ttu-id="2e52f-181">对销售订单和需求补货启用选定波次方法的处理。</span><span class="sxs-lookup"><span data-stu-id="2e52f-181">Processing of selected wave methods is enabled for sales orders and demand replenishment.</span></span>
- <span data-ttu-id="2e52f-182">仓库工作人员可以使用仓库管理移动应用运行销售和需求补货仓库工作。</span><span class="sxs-lookup"><span data-stu-id="2e52f-182">Warehouse workers can run sales and demand replenishment warehouse work by using the Warehouse Management mobile app.</span></span>
- <span data-ttu-id="2e52f-183">仓库工作人员可以使用仓库管理移动应用查询现有库存。</span><span class="sxs-lookup"><span data-stu-id="2e52f-183">Warehouse workers can inquire into on-hand inventory by using the Warehouse Management mobile app.</span></span>
- <span data-ttu-id="2e52f-184">仓库工作人员可以使用仓库管理移动应用创建和运行库存移动。</span><span class="sxs-lookup"><span data-stu-id="2e52f-184">Warehouse workers can create and run inventory movements by using the Warehouse Management mobile app.</span></span>
- <span data-ttu-id="2e52f-185">仓库工作人员可以使用仓库管理移动应用登记采购订单并进行储存。</span><span class="sxs-lookup"><span data-stu-id="2e52f-185">Warehouse workers can register purchase orders and do putaway by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="2e52f-186">有关详细信息，请参阅[仓库缩放单元工作负荷详细信息](cloud-edge-workload-warehousing.md)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-186">For more information, see the [warehouse scale unit workload details](cloud-edge-workload-warehousing.md).</span></span>

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a><span data-ttu-id="2e52f-187">Supply Chain Management 环境的 Onboard Scale Unit</span><span class="sxs-lookup"><span data-stu-id="2e52f-187">Onboard scale units for your Supply Chain Management environment</span></span>

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a><span data-ttu-id="2e52f-188">部署 Cloud Scale Unit 和 Edge Scale Unit 的预览版</span><span class="sxs-lookup"><span data-stu-id="2e52f-188">Deploy the preview for cloud and edge scale units</span></span>

<span data-ttu-id="2e52f-189">下图显示了 Cloud Scale Unit 的公开预览版的注册和预配流。</span><span class="sxs-lookup"><span data-stu-id="2e52f-189">The following illustration shows the sign-up and provisioning flow for the public preview for cloud scale units.</span></span>

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="预览版注册步骤":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a><span data-ttu-id="2e52f-191">选择您的 LCS 项目租户和详细的预览版流程</span><span class="sxs-lookup"><span data-stu-id="2e52f-191">Select your LCS project tenant and the detailed preview process</span></span>

<span data-ttu-id="2e52f-192">在公开预览版中，[缩放单元管理器门户](https://aka.ms/SCMSUM)显示您的帐户所属的租户列表，以及您在哪个租户中是 LCS 项目的所有者或环境管理员。</span><span class="sxs-lookup"><span data-stu-id="2e52f-192">In the public preview, the [Scale Unit Manager portal](https://aka.ms/SCMSUM) shows the list of tenants that your account is part of, and where you're an owner or environment admin for an LCS project.</span></span>

<span data-ttu-id="2e52f-193">如果您要查找的租户不在此列表中，请转到 [LCS](https://lcs.dynamics.com/v2)，并确保您是该租户的 LCS 项目的环境管理员或项目所有者。</span><span class="sxs-lookup"><span data-stu-id="2e52f-193">If the tenant that you're looking for isn't in this list, go to [LCS](https://lcs.dynamics.com/v2), and make sure that you're either an environment admin or a project owner of the LCS project for that tenant.</span></span> <span data-ttu-id="2e52f-194">请注意，仅授权选定租户中的 Azure Active Directory (Azure AD) 帐户完成注册体验。</span><span class="sxs-lookup"><span data-stu-id="2e52f-194">Note that only Azure Active Directory (Azure AD) accounts from the selected tenant are authorized to complete the sign-up experience.</span></span>

> [!NOTE]
> <span data-ttu-id="2e52f-195">将更改应用到 LCS 后，租户列表最多可能需要 30 分钟才能反映更改。</span><span class="sxs-lookup"><span data-stu-id="2e52f-195">After you apply changes to LCS, it might take up to 30 minutes for the list of tenants to reflect the changes.</span></span>

<span data-ttu-id="2e52f-196">对于每个租户，列表都会显示注册状态。</span><span class="sxs-lookup"><span data-stu-id="2e52f-196">For each tenant, the list shows the sign-up status.</span></span>

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="租户的注册选项":::

<span data-ttu-id="2e52f-198">选择 **单击此处注册** 链接注册您的 LCS 租户以参与预览版。</span><span class="sxs-lookup"><span data-stu-id="2e52f-198">Select the **Click here to sign up** link to sign up your LCS tenant to participate in the preview.</span></span> <span data-ttu-id="2e52f-199">您必须接受这些条款。</span><span class="sxs-lookup"><span data-stu-id="2e52f-199">You must accept the terms.</span></span> <span data-ttu-id="2e52f-200">您还必须提供公司电子邮件地址，Microsoft 可以通过该地址发送与预览版注册流程相关的通信。</span><span class="sxs-lookup"><span data-stu-id="2e52f-200">You must also supply a business email address where Microsoft can send communications that are related the preview sign-up process.</span></span>

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="租户的注册提交":::

<span data-ttu-id="2e52f-202">Microsoft 将审查您的请求，并通过向您在注册表单上提供的地址发送电子邮件来通知有关后续步骤的信息。</span><span class="sxs-lookup"><span data-stu-id="2e52f-202">Microsoft will review your request and inform you about the next steps by sending an email to the address that you supplied on the sign-up form.</span></span>

<span data-ttu-id="2e52f-203">在获得预览版计划的访问权限后，您将收到 LCS 项目的两个促销代码。</span><span class="sxs-lookup"><span data-stu-id="2e52f-203">After you've been granted access to the preview program, you will receive two promo codes for your LCS project.</span></span> <span data-ttu-id="2e52f-204">现在，您可以使用这些促销代码在 LCS 中部署两个环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-204">You can now use those promo codes to deploy two environments in LCS.</span></span> <span data-ttu-id="2e52f-205">这些环境必须使用 PEAP 版本 10.0.15 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="2e52f-205">The environments must use PEAP release 10.0.15 or later.</span></span> <span data-ttu-id="2e52f-206">应用完促销代码后，通知 Microsoft（按照指示），以便我们可以为预览功能启用环境。</span><span class="sxs-lookup"><span data-stu-id="2e52f-206">When you've finished applying the promo codes, notify Microsoft (as instructed), so that we can finish enabling the environments for the preview features.</span></span> <span data-ttu-id="2e52f-207">完成此配置步骤后，Microsoft 会通知您。</span><span class="sxs-lookup"><span data-stu-id="2e52f-207">Microsoft will let you know when this configuration step is completed.</span></span>

<span data-ttu-id="2e52f-208">现在，您可以开始在预览环境中配置缩放单元和工作负荷。</span><span class="sxs-lookup"><span data-stu-id="2e52f-208">You can now start to configure scale units and workloads in your preview environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e52f-209">配置 Cloud Scale Unit 时，您可以[在缩放单元管理器门户中执行所有必需步骤](#scale-unit-manager-portal)。</span><span class="sxs-lookup"><span data-stu-id="2e52f-209">When you configure cloud scale units, you can [do all the required steps in the Scale Unit Manager portal](#scale-unit-manager-portal).</span></span>
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a><span data-ttu-id="2e52f-210">使用缩放单元管理器门户管理 Cloud Scale Unit 和工作负荷</span><span class="sxs-lookup"><span data-stu-id="2e52f-210">Manage cloud scale units and workloads by using the Scale Unit Manager portal</span></span>

<span data-ttu-id="2e52f-211">转到[缩放单元管理器门户](https://aka.ms/SCMSUM)，然后使用您的租户帐户登录。</span><span class="sxs-lookup"><span data-stu-id="2e52f-211">Go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM), and sign in by using your tenant account.</span></span> <span data-ttu-id="2e52f-212">在 **配置缩放单元** 页面上，如果尚未列出中心环境，则可以添加一个。</span><span class="sxs-lookup"><span data-stu-id="2e52f-212">On the **Configure scale units** page, you can add a hub environment if it isn't already listed.</span></span> <span data-ttu-id="2e52f-213">然后，可以选择要使用缩放单元和工作负荷配置的中心。</span><span class="sxs-lookup"><span data-stu-id="2e52f-213">You can then select the hub that you want to configure with scale units and workloads.</span></span>

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="缩放单元和工作负荷管理体验":::

<span data-ttu-id="2e52f-215">若要添加一个或多个在拓扑中可用的缩放单元，请选择 **添加缩放单元**。</span><span class="sxs-lookup"><span data-stu-id="2e52f-215">To add one or more scale units that are available in your topology, select **Add scale units**.</span></span> <span data-ttu-id="2e52f-216">在预览版中，您应该看到从作为预览版计划一部分收到的一个促销代码中部署的 Cloud Scale Unit。</span><span class="sxs-lookup"><span data-stu-id="2e52f-216">In the preview, you should see the cloud scale unit that you deployed from one of the promo codes that you received as part of the preview program.</span></span>

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

<span data-ttu-id="2e52f-217">在 **已定义工作负荷** 选项卡上，使用 **创建工作负荷** 按钮将仓库管理或制造执行工作负荷添加到您的缩放单元之一。</span><span class="sxs-lookup"><span data-stu-id="2e52f-217">On the **Defined workloads** tab, use the **Create workload** button to add a warehouse management or manufacturing execution workload to one of your scale units.</span></span> <span data-ttu-id="2e52f-218">对于每个工作负荷，您必须指定工作负荷将负责的流程的上下文。</span><span class="sxs-lookup"><span data-stu-id="2e52f-218">For each workload, you must specify the context of the processes that will be owned by the workload.</span></span> <span data-ttu-id="2e52f-219">对于仓库管理工作负荷，上下文是特定站点和法人中的特定仓库。</span><span class="sxs-lookup"><span data-stu-id="2e52f-219">For warehouse management workloads, the context is a specific warehouse in a specific site and legal entity.</span></span> <span data-ttu-id="2e52f-220">对于制造执行工作负荷，上下文是法人中的特定站点。</span><span class="sxs-lookup"><span data-stu-id="2e52f-220">For manufacturing execution workloads, the context is a specific site in a legal entity.</span></span>

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="工作负荷创建":::

> [!IMPORTANT]
> <span data-ttu-id="2e52f-222">预览版中的缩放单元管理器门户不支持在分配后从缩放单元中删除工作负荷或从中心取消分配缩放单元。</span><span class="sxs-lookup"><span data-stu-id="2e52f-222">The Scale Unit Manager portal in the preview doesn't let you remove workloads from scale units or unassign a scale unit from a hub after the assignment is made.</span></span> <span data-ttu-id="2e52f-223">如果必须删除分配，请与您的预览版计划管理的联系人联系。</span><span class="sxs-lookup"><span data-stu-id="2e52f-223">If you must remove an assignment, reach out to your contact person for preview program management.</span></span>

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]