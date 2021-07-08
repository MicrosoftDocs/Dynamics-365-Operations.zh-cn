---
title: 制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit
description: 本主题提供有关制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit 的信息。
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 24c322712edf1277eabfdd708f528d89bcf43640
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261738"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a><span data-ttu-id="ab448-103">用于制造和仓库管理工作负载的云和边缘缩放单元</span><span class="sxs-lookup"><span data-stu-id="ab448-103">Cloud and edge scale units for manufacturing and warehouse management workloads</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="ab448-104">根据管理服务使用的条款向您提供 Microsoft Dynamics 365 Supply Chain Management 的缩放单元功能。</span><span class="sxs-lookup"><span data-stu-id="ab448-104">The scale unit capability for Microsoft Dynamics 365 Supply Chain Management is made available to you under the terms that govern the use of the service.</span></span> <span data-ttu-id="ab448-105">有关详细信息，请参阅 [Microsoft Dynamics 法律信息](https://go.microsoft.com/fwlink/?LinkID=290927)。</span><span class="sxs-lookup"><span data-stu-id="ab448-105">For more information, see [Microsoft Dynamics Legal Information](https://go.microsoft.com/fwlink/?LinkID=290927).</span></span>
>
> <span data-ttu-id="ab448-106">当启用 Cloud Scale Unit 和 Edge Scale Unit 时，系统将要求您确认了解与 Cloud Scale Unit 和 Edge Scale Unit 的配置和处理相关的某些数据可能存储在位于美国的数据中心中。</span><span class="sxs-lookup"><span data-stu-id="ab448-106">When you enable cloud and edge scale units, you will be asked to affirm that you understand that some data that is related to the configuration and processing of cloud and edge scale units might be stored in a data center that is located in the United States.</span></span> <span data-ttu-id="ab448-107">若要了解有关 Cloud Scale Unit 和 Edge Scale Unit 的数据处理的详细信息，请参阅本主题后面的[缩放单元管理期间的数据处理](#data-processing-management)部分。</span><span class="sxs-lookup"><span data-stu-id="ab448-107">To learn more about data processing for cloud and edge scale units, see the [Data processing during management of scale units](#data-processing-management) section later in this topic.</span></span>

## <a name="core-value-proposition-for-scale-units"></a><span data-ttu-id="ab448-108">缩放单元的核心价值主张</span><span class="sxs-lookup"><span data-stu-id="ab448-108">Core value proposition for scale units</span></span>

<span data-ttu-id="ab448-109">从事制造和分销业务的公司必须能够不中断且大规模地全天候运行关键业务流程。</span><span class="sxs-lookup"><span data-stu-id="ab448-109">Companies that work with manufacturing and distribution must be able to run key business processes 24/7, without interruption and at scale.</span></span> <span data-ttu-id="ab448-110">通过 Cloud Scale Unit 和 Edge Scale Unit，公司能够不中断地运行重要的任务关键型制造和仓库流程，即使偶尔遇到网络连接或延迟问题也是如此。</span><span class="sxs-lookup"><span data-stu-id="ab448-110">Cloud and edge scale units enable companies to run key mission-critical manufacturing and warehouse processes without interruption, even when faced with occasional network connectivity or latency issues.</span></span>

<span data-ttu-id="ab448-111">通过 Cloud Scale Unit 和 Edge Scale Unit，可在不同的环境中分配车间和仓库执行工作负荷。</span><span class="sxs-lookup"><span data-stu-id="ab448-111">Cloud and edge scale units enable distribution of shop floor and warehouse execution workloads among different environments.</span></span> <span data-ttu-id="ab448-112">此功能可以帮助提高性能，防止服务中断并最大化运行时间。</span><span class="sxs-lookup"><span data-stu-id="ab448-112">This functionality can help improve performance, prevent service interruptions, and maximize uptime.</span></span> <span data-ttu-id="ab448-113">通过 Supply Chain Management 订阅的以下加载项提供缩放单元：</span><span class="sxs-lookup"><span data-stu-id="ab448-113">Scale units are provided through the following add-ins for your Supply Chain Management subscription:</span></span>

- <span data-ttu-id="ab448-114">Dynamics 365 Supply Chain Management 的 Cloud Scale Unit 加载项（*2021 年 4 月推出*）</span><span class="sxs-lookup"><span data-stu-id="ab448-114">Cloud Scale Unit Add-in for Dynamics 365 Supply Chain Management (*available April 2021*)</span></span>
- <span data-ttu-id="ab448-115">Dynamics 365 Supply Chain Management 的 Edge Scale Unit 加载项（*即将推出*）</span><span class="sxs-lookup"><span data-stu-id="ab448-115">Edge Scale Unit Add-in for Dynamics 365 Supply Chain Management (*available soon*)</span></span>

<span data-ttu-id="ab448-116">将通过增量增强不断发布工作负荷功能。</span><span class="sxs-lookup"><span data-stu-id="ab448-116">Workload capabilities are being released on a continuous basis through incremental enhancements.</span></span>

## <a name="scale-units-and-dedicated-workloads"></a><span data-ttu-id="ab448-117">缩放单元和专用工作负荷</span><span class="sxs-lookup"><span data-stu-id="ab448-117">Scale units and dedicated workloads</span></span>

<span data-ttu-id="ab448-118">缩放单元通过添加专用的处理容量来扩展您的集中 Supply Chain Management 中心环境。</span><span class="sxs-lookup"><span data-stu-id="ab448-118">Scale units extend your central Supply Chain Management hub environment by adding dedicated processing capacity.</span></span> <span data-ttu-id="ab448-119">缩放单元可在 Cloud 中运行。</span><span class="sxs-lookup"><span data-stu-id="ab448-119">Scale units can run in the cloud.</span></span> <span data-ttu-id="ab448-120">或者，它们可在您的本地机构的 Edge 上本地运行。</span><span class="sxs-lookup"><span data-stu-id="ab448-120">Alternatively, they can run on the edge, on-premises at your local facility.</span></span>

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="具有缩放单元的 Dynamics 365":::

<span data-ttu-id="ab448-122">缩放单元为已分配的工作负荷提供弹性、可靠性和规模。</span><span class="sxs-lookup"><span data-stu-id="ab448-122">Scale units provide resilience, reliability, and scale for the assigned workloads.</span></span> <span data-ttu-id="ab448-123">Edge Scale Unit 可以临时从云中心环境中断开连接，工作人员可以继续在 Edge 上的已分配工作负荷中工作。</span><span class="sxs-lookup"><span data-stu-id="ab448-123">Edge scale units can be temporarily disconnected from the cloud hub environment, and workers continue to work in the assigned workloads on the edge.</span></span>

<span data-ttu-id="ab448-124">*工作负荷* 是一组定义的业务功能，可以进行分解并委派给缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-124">A *workload* is a defined set of business functionality that can be factored out and delegated to a scale unit.</span></span> <span data-ttu-id="ab448-125">尽管已发布仓库管理的工作负荷，但制造执行的工作负荷仍处于预览状态。</span><span class="sxs-lookup"><span data-stu-id="ab448-125">Although the workload for warehouse management has been released, the workload for manufacturing execution is still in preview.</span></span>

<span data-ttu-id="ab448-126">您可以使用[缩放单元管理器门户](https://sum.dynamics.com)为选定工作负荷配置中心环境和 Cloud Scale Unit。</span><span class="sxs-lookup"><span data-stu-id="ab448-126">You can configure your hub environment and cloud scale units for selected workloads by using the [Scale Unit Manager portal](https://sum.dynamics.com).</span></span> <span data-ttu-id="ab448-127">您还可以针对每个缩放单元分配多个工作负荷。</span><span class="sxs-lookup"><span data-stu-id="ab448-127">You can also assign multiple workloads per scale unit.</span></span> <span data-ttu-id="ab448-128">有关当前版本中 Cloud Scale Unit 的先决条件和限制的信息，请参阅本主题后面的 [Cloud Scale Unit 的先决条件和限制](#cloud-scale-unit-prerequisites)部分。</span><span class="sxs-lookup"><span data-stu-id="ab448-128">For information about the prerequisites and limitations for cloud scale units in the current release, see the [Prerequisites and limitations for cloud scale units](#cloud-scale-unit-prerequisites) section later in this topic.</span></span>

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="ab448-129">缩放单元中的专用仓库管理工作负荷功能</span><span class="sxs-lookup"><span data-stu-id="ab448-129">Dedicated warehouse management workload capabilities in a scale unit</span></span>

<span data-ttu-id="ab448-130">仓库管理工作负荷是缩放单元的第一个分发的工作负荷，并且已正式发布。</span><span class="sxs-lookup"><span data-stu-id="ab448-130">The warehouse management workload is the first distributed workload for scale units that has been released for general availability.</span></span>

<span data-ttu-id="ab448-131">对于仓库管理，缩放单元提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="ab448-131">For warehouse management, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="ab448-132">系统可以处理销售订单和需求补货的选定波次方法。</span><span class="sxs-lookup"><span data-stu-id="ab448-132">The system can process selected wave methods for sales orders and demand replenishment.</span></span>
- <span data-ttu-id="ab448-133">仓库工作人员可以使用仓库管理移动应用运行销售和需求补货仓库工作。</span><span class="sxs-lookup"><span data-stu-id="ab448-133">Warehouse workers can run sales and demand replenishment warehouse work by using the Warehouse Management mobile app.</span></span>
- <span data-ttu-id="ab448-134">仓库工作人员可以使用仓库管理移动应用查询现有库存。</span><span class="sxs-lookup"><span data-stu-id="ab448-134">Warehouse workers can inquire into on-hand inventory by using the Warehouse Management mobile app.</span></span>
- <span data-ttu-id="ab448-135">仓库工作人员可以使用仓库管理移动应用创建和运行库存移动。</span><span class="sxs-lookup"><span data-stu-id="ab448-135">Warehouse workers can create and run inventory movements by using the Warehouse Management mobile app.</span></span>
- <span data-ttu-id="ab448-136">仓库工作人员可以使用仓库管理移动应用登记采购订单并进行储存。</span><span class="sxs-lookup"><span data-stu-id="ab448-136">Warehouse workers can register purchase orders and do putaway by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ab448-137">有关详细信息，请参阅 [Cloud Scale Unit 和 Edge Scale Unit 的仓库管理工作负荷](cloud-edge-workload-warehousing.md)。</span><span class="sxs-lookup"><span data-stu-id="ab448-137">For more information, see [Warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="ab448-138">缩放单元中的专用制造执行工作负荷功能</span><span class="sxs-lookup"><span data-stu-id="ab448-138">Dedicated manufacturing execution workload capabilities in a scale unit</span></span>

<span data-ttu-id="ab448-139">制造工作负荷的第一个版本当前处于预览状态，将提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="ab448-139">The first release of the manufacturing workload is currently in preview and delivers the following capabilities:</span></span>

- <span data-ttu-id="ab448-140">机器操作员和车间主管可以访问操作生产计划。</span><span class="sxs-lookup"><span data-stu-id="ab448-140">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="ab448-141">机器操作员可以通过运行离散和流程制造作业来使计划保持最新状态。</span><span class="sxs-lookup"><span data-stu-id="ab448-141">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="ab448-142">车间主管可以调整操作计划。</span><span class="sxs-lookup"><span data-stu-id="ab448-142">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="ab448-143">工作人员可以访问在 Edge 中上下班打卡的考勤管理，以确保正确计算工作人员工资。</span><span class="sxs-lookup"><span data-stu-id="ab448-143">Workers can access time and attendance for clock-in and clock-out on the edge to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="ab448-144">有关详细信息，请参阅 [Cloud Scale Unit 和 Edge Scale Unit 的制造执行工作负荷](cloud-edge-workload-manufacturing.md)。</span><span class="sxs-lookup"><span data-stu-id="ab448-144">For more information, see [Manufacturing execution workloads for cloud and edge scale units](cloud-edge-workload-manufacturing.md).</span></span>

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a><span data-ttu-id="ab448-145">为 Supply Chain Management 启用分布式混合拓扑之前的注意事项</span><span class="sxs-lookup"><span data-stu-id="ab448-145">Considerations before you enable the distributed, hybrid topology for Supply Chain Management</span></span>

<span data-ttu-id="ab448-146">通过启用分布式混合拓扑，您可以转换 Supply Chain Management 云环境，使其充当一个中心。</span><span class="sxs-lookup"><span data-stu-id="ab448-146">By enabling the distributed, hybrid topology, you transition your Supply Chain Management cloud environment so that it functions as a hub.</span></span> <span data-ttu-id="ab448-147">您还可以在 Cloud 中或在 Edge 上关联配置为缩放单元的其他环境。</span><span class="sxs-lookup"><span data-stu-id="ab448-147">You can also associate additional environments that are configured as scale units in the cloud or on the edge.</span></span>

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a><span data-ttu-id="ab448-148">Cloud Scale Unit 的先决条件和限制</span><span class="sxs-lookup"><span data-stu-id="ab448-148">Prerequisites and limitations for cloud scale units</span></span>

<span data-ttu-id="ab448-149">在缩放单元的当前版本中，某些功能尚不可用，但随着时间的推移可能会添加到增量版本中。</span><span class="sxs-lookup"><span data-stu-id="ab448-149">In the current release for scale units, some capabilities aren't yet available but might be added in incremental releases over time.</span></span>

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a><span data-ttu-id="ab448-150">您必须是 Supply Chain Management 的许可客户</span><span class="sxs-lookup"><span data-stu-id="ab448-150">You must be a licensed customer of Supply Chain Management</span></span>

<span data-ttu-id="ab448-151">若要加入到分布式拓扑，您必须具有 Supply Chain Management 的许可证。</span><span class="sxs-lookup"><span data-stu-id="ab448-151">To onboard to the distributed topology, you must have a license for Supply Chain Management.</span></span> <span data-ttu-id="ab448-152">您的现有云环境将成为混合拓扑中的中心。</span><span class="sxs-lookup"><span data-stu-id="ab448-152">Your existing cloud environment will become the hub in your hybrid topology.</span></span> <span data-ttu-id="ab448-153">您可以将沙盒环境和生产环境声明为中心环境，并且可以根据所获取的加载项添加缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-153">You can declare both sandbox environments and production environments as hub environments, and you can add scale units according to the add-ins that you acquire.</span></span>

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a><span data-ttu-id="ab448-154">您的现有项目必须通过 LCS 的全球商业版本进行管理</span><span class="sxs-lookup"><span data-stu-id="ab448-154">Your existing project must be administered via the global commercial version of LCS</span></span>

<span data-ttu-id="ab448-155">您的现有 Microsoft Dynamics Lifecyle Services (LCS) 项目必须满足以下版本要求：</span><span class="sxs-lookup"><span data-stu-id="ab448-155">Your existing Microsoft Dynamics Lifecyle Services (LCS) project must meet the following version requirements:</span></span>

- <span data-ttu-id="ab448-156">该项目必须通过 [lcs.dynamics.com](https://lcs.dynamics.com) 上 LCS 的全球商业版本进行管理。</span><span class="sxs-lookup"><span data-stu-id="ab448-156">The project must be administered via the global commercial version of LCS at [lcs.dynamics.com](https://lcs.dynamics.com).</span></span>
- <span data-ttu-id="ab448-157">LCS 的本地版本（例如 [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) 和 [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)）不受支持。</span><span class="sxs-lookup"><span data-stu-id="ab448-157">Local versions of LCS (such as [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) and [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) aren't supported.</span></span>
- <span data-ttu-id="ab448-158">LCS 的 Governmental Cloud 版本不受支持。</span><span class="sxs-lookup"><span data-stu-id="ab448-158">Governmental Cloud versions of LCS aren't supported.</span></span>
- <span data-ttu-id="ab448-159">LCS 的 Mooncake 版本不受支持。</span><span class="sxs-lookup"><span data-stu-id="ab448-159">The Mooncake version of LCS isn't supported.</span></span>

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a><span data-ttu-id="ab448-160">您的当前生产环境必须是 LCS 中的自助服务类型</span><span class="sxs-lookup"><span data-stu-id="ab448-160">Your current production environment must be of the Self-Service type in LCS</span></span>

<span data-ttu-id="ab448-161">您的当前生产环境必须标记有 LCS 中的 **自助服务** 类型。</span><span class="sxs-lookup"><span data-stu-id="ab448-161">Your current production environment must be tagged with the **Self-Service** type in LCS.</span></span> <span data-ttu-id="ab448-162">此类型指示已转换您的 LCS 项目的租户，因此它支持 Azure Service Fabric 托管模型。</span><span class="sxs-lookup"><span data-stu-id="ab448-162">This type indicates that the tenant of your LCS project has already been converted so that it supports the Azure Service Fabric hosting model.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab448-163">作为服务架构 (IaaS) 运行的环境类型不受支持。</span><span class="sxs-lookup"><span data-stu-id="ab448-163">Environment types that run as infrastructure as a service (IaaS) aren't supported.</span></span> <span data-ttu-id="ab448-164">这些环境通常标记有 LCS 中的 **Microsoft 托管** 类型。</span><span class="sxs-lookup"><span data-stu-id="ab448-164">These environments are typically tagged with the **Microsoft Managed** type in LCS.</span></span> <span data-ttu-id="ab448-165">如果您拥有此类型的环境，请与您的 Microsoft 联系人合作以了解迁移到 **自助服务** 类型的时间线。</span><span class="sxs-lookup"><span data-stu-id="ab448-165">If you have environments of this type, work with your Microsoft contact to understand your migration timeline to the **Self-Service** type.</span></span>

<span data-ttu-id="ab448-166">Microsoft 正在将 Supply Chain Management 的所有云环境从 IaaS 模型转换到在 Service Fabric 中托管的拓扑。</span><span class="sxs-lookup"><span data-stu-id="ab448-166">Microsoft is in the process of transitioning all cloud environments of Supply Chain Management from an IaaS model to a topology that is hosted in Service Fabric.</span></span> <span data-ttu-id="ab448-167">此迁移可以提供更好的可扩展性，并且有助于简化服务管理。</span><span class="sxs-lookup"><span data-stu-id="ab448-167">This move brings better scalability and helps make service management easier.</span></span> <span data-ttu-id="ab448-168">因此，可以更快实现部署和维护操作。</span><span class="sxs-lookup"><span data-stu-id="ab448-168">Therefore, deployment and maintenance operations are faster.</span></span> <span data-ttu-id="ab448-169">同样，服务组件将迁移到微服务的概念，服务托管模型将从虚拟机 (VM) 模型[转换](https://docs.microsoft.com/virtualization/windowscontainers/about/containers-vs-vm)到轻型容器化体系结构。</span><span class="sxs-lookup"><span data-stu-id="ab448-169">Likewise, service components are being migrated to the concept of microservices, and the service hosting model will [transition](https://docs.microsoft.com/virtualization/windowscontainers/about/containers-vs-vm) from a virtual machine (VM) model to a lightweight containerized architecture.</span></span>

<span data-ttu-id="ab448-170">最终，相同的基于 Service Fabric 的容器化服务基础架构将同时为服务的 Cloud 和 Edge 实例提供支持，而不管实例是 Cloud 中的中心，还是 Cloud 中或 Edge 上的缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-170">Ultimately, the same Service Fabric–based containerized service infrastructure will power both cloud and edge instances of the service, regardless of whether an instance is a hub in the cloud, or a scale unit in the cloud or on the edge.</span></span>

<span data-ttu-id="ab448-171">您必须先将项目租户转换到 Service Fabric 托管的模型，然后才能加入到支持缩放单元的混合拓扑。</span><span class="sxs-lookup"><span data-stu-id="ab448-171">Before you can onboard to the hybrid topology that supports scale units, your project tenant must be transitioned to the Service Fabric–hosted model.</span></span> <span data-ttu-id="ab448-172">此外，必须转换将充当中心的任何环境。</span><span class="sxs-lookup"><span data-stu-id="ab448-172">Additionally, any environment that will act as a hub must be converted.</span></span>

> [!TIP]
> <span data-ttu-id="ab448-173">若要查询您的 LCS 项目租户的状态，请在 [LCS](https://lcs.dynamics.com/) 中查找环境的类型，或者与您的合作伙伴或 Microsoft 联系人联系。</span><span class="sxs-lookup"><span data-stu-id="ab448-173">To inquire about the status of your LCS project tenant, look up the type of your environment in [LCS](https://lcs.dynamics.com/), or reach out to your partner or Microsoft contact.</span></span>

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a><span data-ttu-id="ab448-174">不支持将本地业务数据（本地）环境用作缩放单元的中心</span><span class="sxs-lookup"><span data-stu-id="ab448-174">Local business data (on-premises) environments aren't supported as hubs for scale units</span></span>

<span data-ttu-id="ab448-175">本地环境不能用作缩放单元的中心。</span><span class="sxs-lookup"><span data-stu-id="ab448-175">On-premises environments can't function as hubs for scale units.</span></span> <span data-ttu-id="ab448-176">中心环境必须始终由云托管。</span><span class="sxs-lookup"><span data-stu-id="ab448-176">Hub environments must always be cloud hosted.</span></span>

#### <a name="scale-unit-management-capabilities-are-limited"></a><span data-ttu-id="ab448-177">缩放单元管理功能受限制</span><span class="sxs-lookup"><span data-stu-id="ab448-177">Scale unit management capabilities are limited</span></span>

<span data-ttu-id="ab448-178">可以帮助移动工作负荷的管理功能受限制。</span><span class="sxs-lookup"><span data-stu-id="ab448-178">Management capabilities that can help with the movement of workloads are limited.</span></span> <span data-ttu-id="ab448-179">某些管理操作在自助服务方式中不受支持，您必须通过合作伙伴或 Microsoft 联系人请求支持。</span><span class="sxs-lookup"><span data-stu-id="ab448-179">Some management operations aren't supported in a self-service manner, and you might have to request support through your partner or Microsoft contact.</span></span> <span data-ttu-id="ab448-180">示例包括缩放单元之间的某些工作负荷移动和灾难情况下的临时特别移动。</span><span class="sxs-lookup"><span data-stu-id="ab448-180">Examples include some workload movements between scale units and temporary ad-hoc movements in disaster scenarios.</span></span>

#### <a name="metrics-and-measurements-arent-yet-available"></a><span data-ttu-id="ab448-181">指标和度量尚不可用</span><span class="sxs-lookup"><span data-stu-id="ab448-181">Metrics and measurements aren't yet available</span></span>

<span data-ttu-id="ab448-182">可帮助您为缩放单元选择最佳应用程序的指标和度量尚不可用。</span><span class="sxs-lookup"><span data-stu-id="ab448-182">Metrics and measures that might help you select the best application for your scale units aren't yet available.</span></span> <span data-ttu-id="ab448-183">与您的 Microsoft 联系人或实施合作伙伴合作，选择最有利的应用程序。</span><span class="sxs-lookup"><span data-stu-id="ab448-183">Work with your Microsoft contact or implementation partner to select the most beneficial application.</span></span>

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a><span data-ttu-id="ab448-184">缩放单元管理期间的数据处理</span><span class="sxs-lookup"><span data-stu-id="ab448-184">Data processing during management of scale units</span></span>

<span data-ttu-id="ab448-185">当您使 Dynamics 365 环境针对 Cloud Scale Unit 和 Edge Scale Unit 支持分布式混合拓扑时，某些管理服务将仅在美国托管，就像 LCS 一样。</span><span class="sxs-lookup"><span data-stu-id="ab448-185">When you enable your Dynamics 365 environment to support the distributed, hybrid topology for cloud and edge scale units, some management services will be hosted only in the United States, as for LCS.</span></span> <span data-ttu-id="ab448-186">此行为会影响[缩放单元管理器门户](https://sum.dynamics.com)使用的某些管理和配置信息的传输和存储。</span><span class="sxs-lookup"><span data-stu-id="ab448-186">This behavior affects the transfer and storage of some administrative and configuration information that is used by the [Scale Unit Manager portal](https://sum.dynamics.com).</span></span> <span data-ttu-id="ab448-187">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="ab448-187">Here are some examples:</span></span>

- <span data-ttu-id="ab448-188">您的租户名称和 ID</span><span class="sxs-lookup"><span data-stu-id="ab448-188">Your tenant names and IDs</span></span>
- <span data-ttu-id="ab448-189">您的 LCS 项目 ID</span><span class="sxs-lookup"><span data-stu-id="ab448-189">Your LCS project IDs</span></span>
- <span data-ttu-id="ab448-190">用于登录的管理员和项目所有者电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="ab448-190">Administrator and project owner email addresses that are used for sign-in</span></span>
- <span data-ttu-id="ab448-191">中心的环境 ID 和缩放单元</span><span class="sxs-lookup"><span data-stu-id="ab448-191">Environment IDs for the hub and scale units</span></span>
- <span data-ttu-id="ab448-192">工作负荷配置，包括法人和设施的名称和实际地址，以便您的拓扑可以显示在地理地图上</span><span class="sxs-lookup"><span data-stu-id="ab448-192">Workload configurations, including the names and physical addresses of legal entities and facilities, so that your topology can be shown on a geographic map</span></span>
- <span data-ttu-id="ab448-193">收集的指标（例如延迟和吞吐量），将显示在地图分析页面上，以帮助您选择最有用的缩放单元</span><span class="sxs-lookup"><span data-stu-id="ab448-193">Collected metrics (such as latency and throughput) that will be shown on the map analysis page to help you select the most beneficial use of your scale units</span></span>

<span data-ttu-id="ab448-194">根据 Microsoft 数据保留策略，将删除传输到美国数据中心并存储在其中的数据。</span><span class="sxs-lookup"><span data-stu-id="ab448-194">Data that is transferred to and stored in the US data centers will be deleted according to Microsoft data retention policies.</span></span> <span data-ttu-id="ab448-195">Microsoft 非常注重您的隐私。</span><span class="sxs-lookup"><span data-stu-id="ab448-195">Your privacy is important to Microsoft.</span></span> <span data-ttu-id="ab448-196">若要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。</span><span class="sxs-lookup"><span data-stu-id="ab448-196">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

## <a name="onboarding-in-two-stages"></a><span data-ttu-id="ab448-197">加入分为两个阶段</span><span class="sxs-lookup"><span data-stu-id="ab448-197">Onboarding in two stages</span></span>

<span data-ttu-id="ab448-198">加入到分布式混合拓扑的流程具有两个阶段。</span><span class="sxs-lookup"><span data-stu-id="ab448-198">The process of onboarding to the distributed, hybrid topology has two stages.</span></span> <span data-ttu-id="ab448-199">在第一个阶段中，您必须验证自定义以确保它们可在具有缩放单元的分布式拓扑中工作。</span><span class="sxs-lookup"><span data-stu-id="ab448-199">During the first stage, you must validate customizations to ensure that they work in the distributed topology that has scale units.</span></span> <span data-ttu-id="ab448-200">沙盒和生产环境仅在第二阶段中移动。</span><span class="sxs-lookup"><span data-stu-id="ab448-200">Sandbox and production environments are moved only during the second stage.</span></span>

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a><span data-ttu-id="ab448-201">阶段 1：在单盒开发环境中评估自定义</span><span class="sxs-lookup"><span data-stu-id="ab448-201">Stage 1: Evaluate customizations in one-box development environments</span></span>

<span data-ttu-id="ab448-202">在开始加入沙盒或生产环境之前，建议您在开发设置中探索缩放单元，例如单盒环境（也称为第 1 层环境），以便您可以验证流程、自定义和解决方案。</span><span class="sxs-lookup"><span data-stu-id="ab448-202">Before you start to onboard your sandbox or production environments, we recommend that you explore scale units in a development setup, such as a one-box environment (also known as a tier-1 environment), so that you can validate processes, customizations, and solutions.</span></span> <span data-ttu-id="ab448-203">在此阶段中，数据和自定义将应用到单盒环境。</span><span class="sxs-lookup"><span data-stu-id="ab448-203">During this stage, data and customizations will be applied to the one-box environments.</span></span> <span data-ttu-id="ab448-204">一个环境用作中心，另一个环境用作缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-204">One environment takes the role of the hub, and the other takes the role of a scale unit.</span></span> <span data-ttu-id="ab448-205">此设置提供识别和修复问题的最佳方法。</span><span class="sxs-lookup"><span data-stu-id="ab448-205">This setup provides the best way to identify and fix issues.</span></span> <span data-ttu-id="ab448-206">最新的提前访问 (PEAP) 版本也可以用于完成此阶段。</span><span class="sxs-lookup"><span data-stu-id="ab448-206">The latest early access (PEAP) build can also be used to complete this stage.</span></span>

<span data-ttu-id="ab448-207">对于阶段 1，应使用[单盒开发环境的缩放单元部署工具](https://github.com/microsoft/SCMScaleUnitDevTools)。</span><span class="sxs-lookup"><span data-stu-id="ab448-207">For stage 1, you should use the [scale unit deployment tools for one-box development environments](https://github.com/microsoft/SCMScaleUnitDevTools).</span></span> <span data-ttu-id="ab448-208">这些工具使您可以在一个或两个单独的单盒环境中配置中心和缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-208">These tools let you configure hub and scale units in one or two separate one-box environments.</span></span> <span data-ttu-id="ab448-209">这些工具作为二进制版本提供，并在 GitHub 上以源代码的形式提供。</span><span class="sxs-lookup"><span data-stu-id="ab448-209">The tools are provided as a binary release and in source code on GitHub.</span></span> <span data-ttu-id="ab448-210">研究项目 wiki，其中包括描述如何使用工具的[分步使用指南](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide)。</span><span class="sxs-lookup"><span data-stu-id="ab448-210">Study the project wiki, which includes a [Step by step usage guide](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) that describes how the tools are used.</span></span>

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a><span data-ttu-id="ab448-211">阶段 2：获取加载项，并在沙盒和生产环境中进行部署</span><span class="sxs-lookup"><span data-stu-id="ab448-211">Stage 2: Acquire add-ins, and deploy in your sandbox and production environments</span></span>

<span data-ttu-id="ab448-212">若要将沙盒或生产环境之一加入到新拓扑，您必须获取一个或多个 Cloud Scale Unit（以及将来的 Edge Scale Unit）的加载项。</span><span class="sxs-lookup"><span data-stu-id="ab448-212">To onboard one of your sandbox or production environments to the new topology, you must acquire add-ins for one or more cloud scale units (and, in the future, for edge scale units).</span></span> <span data-ttu-id="ab448-213">加载项将在 [LCS](https://lcs.dynamics.com/) 中授予相应的项目和环境插槽，以便可以部署缩放单元环境。</span><span class="sxs-lookup"><span data-stu-id="ab448-213">The add-ins will grant corresponding project and environment slots in [LCS](https://lcs.dynamics.com/) so that the scale unit environments can be deployed.</span></span>

> [!NOTE]
> <span data-ttu-id="ab448-214">缩放单元加载项不与有限数量的用户耦合，但可以根据管理员分配的角色供现有订阅中的任何用户使用。</span><span class="sxs-lookup"><span data-stu-id="ab448-214">The scale unit add-ins aren't coupled to a limited number of users but can be used by any user in the existing subscription, based on the roles that the administrator assigns.</span></span>

<span data-ttu-id="ab448-215">在多个库存单位 (SKU) 和定价选项中提供缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-215">Scale units are offered in multiple stock keeping units (SKUs) and pricing options.</span></span> <span data-ttu-id="ab448-216">因此，您可以选择最能满足您计划的每月交易量和性能要求的选项。</span><span class="sxs-lookup"><span data-stu-id="ab448-216">Therefore, you can choose the option that best meets your planned monthly transaction volume and performance requirements.</span></span>

<span data-ttu-id="ab448-217">入门级 SKU 称为 *基本*，性能更高的 SKU 称为 *标准*。</span><span class="sxs-lookup"><span data-stu-id="ab448-217">The entry-level SKU is known as *Basic*, and the more performant SKU is known as *Standard*.</span></span> <span data-ttu-id="ab448-218">每个 SKU 都预先加载有特定数量的每月交易。</span><span class="sxs-lookup"><span data-stu-id="ab448-218">Each SKU is pre-loaded with a specific number of monthly transactions.</span></span> <span data-ttu-id="ab448-219">但是，您可以通过为每个 SKU 添加超额加载项来增加每月交易预算。</span><span class="sxs-lookup"><span data-stu-id="ab448-219">However, you can increase the monthly transaction budget by adding overage add-ins for each SKU.</span></span>

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Cloud Scale Unit 的加载项":::

> [!TIP]
> <span data-ttu-id="ab448-221">若要确定最能满足您的需求的规模，请与您的合作伙伴和 Microsoft 合作，以了解所需的每月交易规模。</span><span class="sxs-lookup"><span data-stu-id="ab448-221">To identify the sizing that best meets your needs, work with your partner and Microsoft to understand the monthly transaction size that you require.</span></span>

<span data-ttu-id="ab448-222">购买每个缩放单元加载项后，您不仅可以获取每月交易量，还有权使用 LCS 中特定数量的环境插槽。</span><span class="sxs-lookup"><span data-stu-id="ab448-222">The purchase of each scale unit add-in not only gives you a monthly volume of transactions but also entitles you to a specific number of environment slots in LCS.</span></span> <span data-ttu-id="ab448-223">对于每个 Cloud Scale Unit 加载项，您都有权使用一个新生产槽和一个新沙盒槽。</span><span class="sxs-lookup"><span data-stu-id="ab448-223">For each Cloud Scale Unit Add-in, you're entitled to one new production slot and one new sandbox slot.</span></span> <span data-ttu-id="ab448-224">在加入流程期间，将添加具有这些插槽的新 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="ab448-224">During the onboarding process, a new LCS project will be added that has these slots.</span></span> <span data-ttu-id="ab448-225">插槽的使用权受到限制，因此必须将插槽用作具有云中心的缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-225">The usage rights for the slots are bound so that the slots must be used as scale units that have a cloud hub.</span></span>

<span data-ttu-id="ab448-226">超额加载项不能赋予您使用新环境的权限。</span><span class="sxs-lookup"><span data-stu-id="ab448-226">Overage add-ins don't entitle you to new environment slots.</span></span>

<span data-ttu-id="ab448-227">如果要获取更多沙盒环境，您可以购买额外的常规沙盒槽。</span><span class="sxs-lookup"><span data-stu-id="ab448-227">If you want to acquire more sandbox environments, you can purchase additional regular sandbox slots.</span></span> <span data-ttu-id="ab448-228">然后，Microsoft 可以帮助您启用这些插槽作为混合拓扑的沙盒缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-228">Microsoft can then help you enable those slots as sandbox scale units for the hybrid topology.</span></span>

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a><span data-ttu-id="ab448-229">加入到 Supply Chain Management 的分布式混合拓扑</span><span class="sxs-lookup"><span data-stu-id="ab448-229">Onboard to the distributed, hybrid topology for Supply Chain Management</span></span>

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a><span data-ttu-id="ab448-230">选择您的 LCS 项目租户和详细的加入流程</span><span class="sxs-lookup"><span data-stu-id="ab448-230">Select your LCS project tenant and the detailed onboarding process</span></span>

<span data-ttu-id="ab448-231">完成计划如何加入到 Supply Chain Management 的分布式混合拓扑后，您将使用[缩放单元管理器门户](https://aka.ms/SCMSUM)开始加入流程。</span><span class="sxs-lookup"><span data-stu-id="ab448-231">After you've finished planning how you will onboard to the distributed, hybrid topology for Supply Chain Management, you will use the [Scale Unit Manager portal](https://aka.ms/SCMSUM) to begin the onboarding process.</span></span> <span data-ttu-id="ab448-232">在门户中，选择 **Dynamics 365 租户** 选项卡。此选项卡显示您的帐户所属的租户列表，以及您在哪个租户中是 LCS 项目的所有者或环境管理员。</span><span class="sxs-lookup"><span data-stu-id="ab448-232">In the portal, select the **Dynamics 365 Tenants** tab. This tab shows the list of tenants that your account is part of, and where you're an owner or environment admin for an LCS project.</span></span>

<span data-ttu-id="ab448-233">如果您要查找的租户不在列表中，请转到 [LCS](https://lcs.dynamics.com/v2)，并确保您是该租户的 LCS 项目的环境管理员或项目所有者。</span><span class="sxs-lookup"><span data-stu-id="ab448-233">If the tenant that you're looking for isn't in the list, go to [LCS](https://lcs.dynamics.com/v2), and make sure that you're either an environment admin or a project owner of the LCS project for that tenant.</span></span> <span data-ttu-id="ab448-234">仅授权选定租户中的 Azure Active Directory (Azure AD) 帐户完成注册体验。</span><span class="sxs-lookup"><span data-stu-id="ab448-234">Only Azure Active Directory (Azure AD) accounts from the selected tenant are authorized to complete the sign-up experience.</span></span>

> [!NOTE]
> <span data-ttu-id="ab448-235">将更改应用到 LCS 后，租户列表最多可能需要 30 分钟才能反映更改。</span><span class="sxs-lookup"><span data-stu-id="ab448-235">After you apply changes to LCS, the list of tenants might take up to 30 minutes to reflect the changes.</span></span>

<span data-ttu-id="ab448-236">对于每个租户，列表都会显示加入状态。</span><span class="sxs-lookup"><span data-stu-id="ab448-236">For each tenant, the list shows the onboarding status.</span></span>

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Dynamics 365 租户选项卡上的租户列表":::

<span data-ttu-id="ab448-238">选择 **单击此处开始** 以请求加入 LCS 租户。</span><span class="sxs-lookup"><span data-stu-id="ab448-238">Select **Click here to get started** to request onboarding for the LCS tenant.</span></span> <span data-ttu-id="ab448-239">您必须接受这些条款。</span><span class="sxs-lookup"><span data-stu-id="ab448-239">You must accept the terms.</span></span> <span data-ttu-id="ab448-240">您还必须提供公司电子邮件地址，Microsoft 可以通过该地址发送与加入流程相关的通信。</span><span class="sxs-lookup"><span data-stu-id="ab448-240">You must also supply a business email address where Microsoft can send communications that are related the onboarding process.</span></span>

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="租户的注册提交":::

<span data-ttu-id="ab448-242">Microsoft 将审查您的请求，并通过向您在注册窗体中提供的地址发送电子邮件来通知有关后续步骤的信息。</span><span class="sxs-lookup"><span data-stu-id="ab448-242">Microsoft will review your request and inform you about the next steps by sending an email to the address that you supplied in the sign-up form.</span></span> <span data-ttu-id="ab448-243">Microsoft 将与您紧密合作，为您的业务场景在混合拓扑中启用缩放单元。</span><span class="sxs-lookup"><span data-stu-id="ab448-243">Microsoft will be working closely with you to enable scale units in the hybrid topology for your business scenario.</span></span>

<span data-ttu-id="ab448-244">完成加入后，您可以使用端口配置缩放单元和工作负荷。</span><span class="sxs-lookup"><span data-stu-id="ab448-244">After the onboarding is completed, you can use the port to configure scale units and workloads.</span></span>

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a><span data-ttu-id="ab448-245">使用缩放单元管理器门户管理 Cloud Scale Unit 和工作负荷</span><span class="sxs-lookup"><span data-stu-id="ab448-245">Manage cloud scale units and workloads by using the Scale Unit Manager portal</span></span>

<span data-ttu-id="ab448-246">转到[缩放单元管理器门户](https://aka.ms/SCMSUM)，然后使用您的租户帐户登录。</span><span class="sxs-lookup"><span data-stu-id="ab448-246">Go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM), and sign in by using your tenant account.</span></span> <span data-ttu-id="ab448-247">在 **配置缩放单元** 页面上，如果尚未列出中心环境，则可以添加一个。</span><span class="sxs-lookup"><span data-stu-id="ab448-247">On the **Configure scale units** page, you can add a hub environment if it isn't already listed.</span></span> <span data-ttu-id="ab448-248">然后，可以选择要使用缩放单元和工作负荷配置的中心。</span><span class="sxs-lookup"><span data-stu-id="ab448-248">You can then select the hub that you want to configure with scale units and workloads.</span></span>

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="缩放单元和工作负荷管理体验":::

<span data-ttu-id="ab448-250">若要添加一个或多个在订阅中可用的缩放单元，请选择 **添加缩放单元**。</span><span class="sxs-lookup"><span data-stu-id="ab448-250">To add one or more scale units that are available in your subscriptions, select **Add scale units**.</span></span>

<span data-ttu-id="ab448-251">在 **已定义工作负荷** 选项卡上，使用 **创建工作负荷** 按钮将仓库管理工作负荷添加到您的缩放单元之一。</span><span class="sxs-lookup"><span data-stu-id="ab448-251">On the **Defined workloads** tab, use the **Create workload** button to add a warehouse management workload to one of your scale units.</span></span> <span data-ttu-id="ab448-252">对于每个工作负荷，您必须指定工作负荷将负责的流程的上下文。</span><span class="sxs-lookup"><span data-stu-id="ab448-252">For each workload, you must specify the context of the processes that will be owned by the workload.</span></span> <span data-ttu-id="ab448-253">对于仓库管理工作负荷，上下文是特定站点和法人中的特定仓库。</span><span class="sxs-lookup"><span data-stu-id="ab448-253">For warehouse management workloads, the context is a specific warehouse in a specific site and legal entity.</span></span>

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="工作负荷创建":::

> [!TIP]
> <span data-ttu-id="ab448-255">随着时间的推移，将向缩放单元管理器体验添加增量增强，以帮助简化生命周期管理操作。</span><span class="sxs-lookup"><span data-stu-id="ab448-255">Over time, incremental enhancements will be added to the Scale Unit Manager experience to help make lifecycle management operations easier.</span></span> <span data-ttu-id="ab448-256">当前版本的特定功能记录在加入手册中，该手册适用于正在加入到 Supply Chain Management 的分布式混合拓扑。</span><span class="sxs-lookup"><span data-stu-id="ab448-256">The specific capabilities for the current release are documented in an onboarding handbook that is available to customers who are in the process of onboarding to the distributed, hybrid topology for Supply Chain Management.</span></span> <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
