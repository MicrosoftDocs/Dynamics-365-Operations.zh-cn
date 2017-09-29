---
title: "本地部署的系统要求"
description: "此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 本地部署的系统要求。"
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 721c5851cd399398a8dcec5ae110b97a4f17ae0a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a><span data-ttu-id="8ed56-103">本地部署的系统要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-103">System requirements for on-premises deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8ed56-104">此主题列出了当前版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 本地部署的系统要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for on-premises deployments.</span></span> <span data-ttu-id="8ed56-105">在你安装 Finance and Operations 前，适合执行此步骤时验证你正在使用的系统是否满足或超出最低网络、硬件和软件要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="network-requirements"></a><span data-ttu-id="8ed56-106">网络要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-106">Network requirements</span></span>
<span data-ttu-id="8ed56-107">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（本地部署）支持使用 Internet 协议版本 4 (IPv4) 或 Internet 协议版本 6 (IPv6) 的网络。</span><span class="sxs-lookup"><span data-stu-id="8ed56-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) can work on networks that use Internet Protocol Version 4 (IPv4) or Internet Protocol Version 6 (IPv6).</span></span> <span data-ttu-id="8ed56-108">在计划系统时考虑网络环境并遵照以下指南。</span><span class="sxs-lookup"><span data-stu-id="8ed56-108">Consider the network environment when you plan your system, and use the following guidelines.</span></span>

### <a name="network-response-time"></a><span data-ttu-id="8ed56-109">网络响应时间</span><span class="sxs-lookup"><span data-stu-id="8ed56-109">Network response time</span></span>
<span data-ttu-id="8ed56-110">下表列出了本地系统中 Web 浏览器与应用程序对象服务器 (AOS) 之间连接以及 AOS 与数据库之间连接的最低网络要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-110">The following table lists the minimum network requirements for the connection between the web browser and Application Object Server (AOS), and for the connection between AOS and the database in an on-premises system.</span></span>

| <span data-ttu-id="8ed56-111">值</span><span class="sxs-lookup"><span data-stu-id="8ed56-111">Value</span></span>     | <span data-ttu-id="8ed56-112">从 Web 浏览器到 AOS</span><span class="sxs-lookup"><span data-stu-id="8ed56-112">Web browser to AOS</span></span>                      | <span data-ttu-id="8ed56-113">从 AOS 到数据库</span><span class="sxs-lookup"><span data-stu-id="8ed56-113">AOS to database</span></span> |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed56-114">带宽</span><span class="sxs-lookup"><span data-stu-id="8ed56-114">Bandwidth</span></span> | <span data-ttu-id="8ed56-115">每用户每秒 50 千字节 (KBps)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-115">50 kilobytes per second (KBps) per user</span></span> | <span data-ttu-id="8ed56-116">每秒 100 兆字节 (Mbps)</span><span class="sxs-lookup"><span data-stu-id="8ed56-116">100 megabytes per second (MBps)</span></span> |
| <span data-ttu-id="8ed56-117">延迟</span><span class="sxs-lookup"><span data-stu-id="8ed56-117">Latency</span></span>   | <span data-ttu-id="8ed56-118">低于 250–300 毫秒 (ms)</span><span class="sxs-lookup"><span data-stu-id="8ed56-118">Less than 250–300 milliseconds (ms)</span></span>     | <span data-ttu-id="8ed56-119">低于 1 ms（仅限局域网 (LAN)）。</span><span class="sxs-lookup"><span data-stu-id="8ed56-119">Less than 1 ms (local area network [LAN] only).</span></span> <span data-ttu-id="8ed56-120">AOS 和数据库必须在同一个地点。</span><span class="sxs-lookup"><span data-stu-id="8ed56-120">AOS and the database must be co-located.</span></span> |

- <span data-ttu-id="8ed56-121">Finance and Operations（本地）适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。</span><span class="sxs-lookup"><span data-stu-id="8ed56-121">Finance and Operations (on-premises) is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="8ed56-122">该延迟是从浏览器客户端到托管 Finance and Operations 的数据中心的延迟。</span><span class="sxs-lookup"><span data-stu-id="8ed56-122">This latency is the latency from a browser client to the datacenter that hosts Finance and Operations.</span></span>
- <span data-ttu-id="8ed56-123">Finance and Operations（本地）的带宽要求取决于你的方案。</span><span class="sxs-lookup"><span data-stu-id="8ed56-123">Bandwidth requirements for Finance and Operations (on-premises) depend on your scenario.</span></span> <span data-ttu-id="8ed56-124">典型方案要求浏览器与 Finance and Operations 服务器之间的带宽超过每秒 50 千字节 KBps。</span><span class="sxs-lookup"><span data-stu-id="8ed56-124">Typical scenarios require a bandwidth of more than 50 KBps between the browser and the Finance and Operations server.</span></span> <span data-ttu-id="8ed56-125">但是，对于需要高负载要求的方案（如涉及工作区或大量自定义的方案），建议提供更高带宽。</span><span class="sxs-lookup"><span data-stu-id="8ed56-125">However, we recommend higher bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span> <span data-ttu-id="8ed56-126">具体带宽量取决于使用。</span><span class="sxs-lookup"><span data-stu-id="8ed56-126">The specific amount of bandwidth depends on use.</span></span>

<span data-ttu-id="8ed56-127">不支持将 AOS 和 Microsoft SQL Server 数据库安装在不同的数据中心的部署。</span><span class="sxs-lookup"><span data-stu-id="8ed56-127">Deployments where AOS and the Microsoft SQL Server database are in different datacenters aren't supported.</span></span> <span data-ttu-id="8ed56-128">AOS 和 SQL Server 数据库必须在同一个地点。</span><span class="sxs-lookup"><span data-stu-id="8ed56-128">AOS and the SQL Server database must be co-located.</span></span> 

<span data-ttu-id="8ed56-129">一般来说，Finance and Operations 经过优化以缩短浏览器到服务器的往返。</span><span class="sxs-lookup"><span data-stu-id="8ed56-129">In general, Finance and Operations is optimized to reduce browser-to-server round trips.</span></span> <span data-ttu-id="8ed56-130">从浏览器客户端到数据中心的往返次数要么为零，要么是每次用户交互往返一次，并且整个负载经过压缩。</span><span class="sxs-lookup"><span data-stu-id="8ed56-130">The number of round trips from a browser client to the datacenter is either zero or one for each user interaction, and the payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="8ed56-131">请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-131">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="8ed56-132">给定位置的并行使用很难计算。</span><span class="sxs-lookup"><span data-stu-id="8ed56-132">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="8ed56-133">我们建议使用真实模拟 Finance and Operations 的非生产环境作为针对你的特定案例的性能的最佳衡量。</span><span class="sxs-lookup"><span data-stu-id="8ed56-133">We recommend that you use a real-life simulation against a non-production environment of Finance and Operations as the best gauge of performance for your specific case.</span></span> 

### <a name="lan-environments"></a><span data-ttu-id="8ed56-134">LAN 环境</span><span class="sxs-lookup"><span data-stu-id="8ed56-134">LAN environments</span></span>
<span data-ttu-id="8ed56-135">在 LAN 环境中，不需要通过 Microsoft Windows Server 中的 Microsoft 远程桌面即可连接到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="8ed56-135">In LAN environments, Microsoft Remote Desktop in Microsoft Windows Server isn't required in order to connect to Finance and Operations.</span></span> <span data-ttu-id="8ed56-136">但是，构成服务器部署的虚拟机 (VM) 上的服务操作可能需要远程桌面。</span><span class="sxs-lookup"><span data-stu-id="8ed56-136">However, Remote Desktop might be required for servicing operations on the virtual machines (VMs) that make up the server deployments.</span></span>

### <a name="wan-environments"></a><span data-ttu-id="8ed56-137">WAN 环境</span><span class="sxs-lookup"><span data-stu-id="8ed56-137">WAN environments</span></span>
<span data-ttu-id="8ed56-138">在广域网 (WAN) 环境中，不需要通过 Windows Server 中的远程桌面即可连接到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="8ed56-138">In wide area network (WAN) environments, Remote Desktop in Windows Server isn't required in order to connect to Finance and Operations.</span></span>

### <a name="internet-connectivity-requirements"></a><span data-ttu-id="8ed56-139">Internet 连接要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-139">Internet connectivity requirements</span></span>
<span data-ttu-id="8ed56-140">Finance and Operations（本地）不要求来自用户工作站的 Internet 连接。</span><span class="sxs-lookup"><span data-stu-id="8ed56-140">Finance and Operations (on-premises) doesn't require internet connectivity from user workstations.</span></span> <span data-ttu-id="8ed56-141">但是，如果没有 Internet 连接，一些功能将不可用。</span><span class="sxs-lookup"><span data-stu-id="8ed56-141">However, some features won't be available if there is no internet connectivity.</span></span>

|                    |   |
|--------------------|---|
| <span data-ttu-id="8ed56-142">**浏览器客户端**</span><span class="sxs-lookup"><span data-stu-id="8ed56-142">**Browser client**</span></span> | <span data-ttu-id="8ed56-143">没有 Internet 连接的内部网方案是本地部署选项的一个设计点。</span><span class="sxs-lookup"><span data-stu-id="8ed56-143">An intranet scenario without internet connectivity is a design point for the on-premises deployment option.</span></span> <span data-ttu-id="8ed56-144">要求云服务的某些功能将不可用，例如 Microsoft Dynamics Lifecycle Services (LCS) 中的帮助和任务指南库。</span><span class="sxs-lookup"><span data-stu-id="8ed56-144">Some features that require cloud services won't be available, such as Help and Task guide libraries in Microsoft Dynamics Lifecycle Services (LCS).</span></span> |
| <span data-ttu-id="8ed56-145">**服务器**</span><span class="sxs-lookup"><span data-stu-id="8ed56-145">**Server**</span></span>         | <span data-ttu-id="8ed56-146">AOS 或 Microsoft Azure Service Fabric 层级必须能够与 LCS 通信。</span><span class="sxs-lookup"><span data-stu-id="8ed56-146">The AOS or Microsoft Azure Service Fabric tier must be able to communicate with LCS.</span></span> <span data-ttu-id="8ed56-147">本地的基于浏览器的客户端不需要访问 Internet。</span><span class="sxs-lookup"><span data-stu-id="8ed56-147">The on-premises browser-based client doesn't require internet access.</span></span> |
| <span data-ttu-id="8ed56-148">**遥测**</span><span class="sxs-lookup"><span data-stu-id="8ed56-148">**Telemetry**</span></span>      | <span data-ttu-id="8ed56-149">如果存在长时间的连接中断，遥测数据可能会丢失。</span><span class="sxs-lookup"><span data-stu-id="8ed56-149">Telemetry data might be lost if there are long interruptions in connectivity.</span></span> <span data-ttu-id="8ed56-150">与 LCS 的连接中断不影响本地应用程序功能。</span><span class="sxs-lookup"><span data-stu-id="8ed56-150">Interruptions in connectivity to LCS don't affect the on-premises application functionality.</span></span> |
| <span data-ttu-id="8ed56-151">**LCS**</span><span class="sxs-lookup"><span data-stu-id="8ed56-151">**LCS**</span></span>            | <span data-ttu-id="8ed56-152">部署、代码部署和服务操作要求连接到 LCS。</span><span class="sxs-lookup"><span data-stu-id="8ed56-152">Connectivity to LCS is required for deployment, code deployment, and servicing operations.</span></span> |

## <a name="telemetry-data-transfer-to-the-cloud"></a><span data-ttu-id="8ed56-153">将遥测数据转移到云</span><span class="sxs-lookup"><span data-stu-id="8ed56-153">Telemetry data transfer to the cloud</span></span>
<span data-ttu-id="8ed56-154">大多数遥测数据存储在本地并且可以通过 Microsoft Windows 中的事件查看器访问。</span><span class="sxs-lookup"><span data-stu-id="8ed56-154">Most telemetry data is stored locally and can be accessed by using Event Viewer in Microsoft Windows.</span></span> <span data-ttu-id="8ed56-155">遥测事件中的一个小子集被转移到云中的 Microsoft 遥测管道进行诊断。</span><span class="sxs-lookup"><span data-stu-id="8ed56-155">A small subset of telemetry events is transferred to the Microsoft telemetry pipeline in the cloud for diagnostics.</span></span> <span data-ttu-id="8ed56-156">客户数据和用户的可识别数据不是发送到 Microsoft 的遥测数据的一部分。</span><span class="sxs-lookup"><span data-stu-id="8ed56-156">Customer data and user-identifiable data aren't part of the telemetry data that is sent to Microsoft.</span></span> <span data-ttu-id="8ed56-157">VM 名称被发送到 Microsoft 以帮助执行环境管理和来自 LCS 门户的诊断。</span><span class="sxs-lookup"><span data-stu-id="8ed56-157">VM names are sent to Microsoft to help with environment management and diagnostics from the LCS portal.</span></span>

## <a name="domain-requirements"></a><span data-ttu-id="8ed56-158">域需求</span><span class="sxs-lookup"><span data-stu-id="8ed56-158">Domain requirements</span></span>
<span data-ttu-id="8ed56-159">在安装 Finance and Operations（本地）时考虑以下域要求：</span><span class="sxs-lookup"><span data-stu-id="8ed56-159">Consider the following domain requirements when you install Finance and Operations (on-premises):</span></span>

- <span data-ttu-id="8ed56-160">托管 Finance and Operations（本地）组件的 VM 必须属于 Active Directory 域。</span><span class="sxs-lookup"><span data-stu-id="8ed56-160">VMs that host Finance and Operations (on-premises) components must belong to an Active Directory domain.</span></span> <span data-ttu-id="8ed56-161">Active Directory 域服务 (AD DS) 必须在本机模式中配置。</span><span class="sxs-lookup"><span data-stu-id="8ed56-161">Active Directory Domain Services (AD DS) must be configured in native mode.</span></span>
- <span data-ttu-id="8ed56-162">运行 Finance and Operations（本地）组件的 VM 必须可以彼此访问。</span><span class="sxs-lookup"><span data-stu-id="8ed56-162">VMs that run Finance and Operations (on-premises) components must have access to each other.</span></span> <span data-ttu-id="8ed56-163">此访问在 AD DS 中配置。</span><span class="sxs-lookup"><span data-stu-id="8ed56-163">This access is configured in AD DS.</span></span> 
- <span data-ttu-id="8ed56-164">域控制器必须是 Microsoft Windows Server 2012 R2 或更高版本，域功能级别必须是 2012 R2 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="8ed56-164">The domain controller must be Microsoft Windows Server 2012 R2 or later, and the domain functional level must be 2012 R2 or more.</span></span>

## <a name="hardware-requirements"></a><span data-ttu-id="8ed56-165">硬件要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-165">Hardware requirements</span></span>
<span data-ttu-id="8ed56-166">本节介绍运行 Finance and Operations（本地）所需的硬件。</span><span class="sxs-lookup"><span data-stu-id="8ed56-166">This section describes the hardware that is required in order to run Finance and Operations (on-premises).</span></span>

<span data-ttu-id="8ed56-167">基于系统配置、数据构成以及你决定要使用的应用程序和功能，实际硬件要求将不同。</span><span class="sxs-lookup"><span data-stu-id="8ed56-167">The actual hardware requirements vary, based on the system configuration, the data composition, and the applications and features that you decide to use.</span></span> <span data-ttu-id="8ed56-168">以下是可能影响 Finance and Operations（本地）适当硬件选择的一些因素：</span><span class="sxs-lookup"><span data-stu-id="8ed56-168">Here are some of the factors that can affect the choice of appropriate hardware for Finance and Operations (on-premises):</span></span>

- <span data-ttu-id="8ed56-169">每小时的交易数量</span><span class="sxs-lookup"><span data-stu-id="8ed56-169">The number of transactions per hour</span></span>
- <span data-ttu-id="8ed56-170">并发用户的数量</span><span class="sxs-lookup"><span data-stu-id="8ed56-170">The number of concurrent users</span></span>

## <a name="minimum-infrastructure-requirements"></a><span data-ttu-id="8ed56-171">最低基础结构需求</span><span class="sxs-lookup"><span data-stu-id="8ed56-171">Minimum infrastructure requirements</span></span>
<span data-ttu-id="8ed56-172">Finance and Operations（本地）使用 Service Fabric 托管 AOS、批处理、数据管理、Management Reporter 和环境 Orchestrator 服务。</span><span class="sxs-lookup"><span data-stu-id="8ed56-172">Finance and Operations (on-premises) uses Service Fabric to host the AOS, Batch, Data management, Management reporter, and Environment orchestrator services.</span></span> <span data-ttu-id="8ed56-173">Microsoft SQL Server Reporting Services (SSRS) 不在 Service Fabric 群集中托管。</span><span class="sxs-lookup"><span data-stu-id="8ed56-173">Microsoft SQL Server Reporting Services (SSRS) aren't hosted in the Service Fabric cluster.</span></span>

<span data-ttu-id="8ed56-174">必须为 SQL Server 设置至少具有两个用于生产的节点的高可用性 HADRON。</span><span class="sxs-lookup"><span data-stu-id="8ed56-174">SQL Server must have a high-availability HADRON setup that has at least two nodes for production use.</span></span>

<span data-ttu-id="8ed56-175">下图显示了为 Service Fabric 群集建议的最低节点数量。</span><span class="sxs-lookup"><span data-stu-id="8ed56-175">The following illustration shows the minimum number of nodes that is recommended for your Service Fabric cluster.</span></span>

<span data-ttu-id="8ed56-176">[![为 Service Fabric 群集建议的节点数量](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png)</span><span class="sxs-lookup"><span data-stu-id="8ed56-176">[![Recommended number of nodes for the Service Fabric cluster](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png)</span></span> 

## <a name="processor-and-ram-requirements"></a><span data-ttu-id="8ed56-177">处理器和 RAM 要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-177">Processor and RAM requirements</span></span>
<span data-ttu-id="8ed56-178">下表列出了运行此部署选项所需的每个角色所需的处理器的数量和随机存取内存 (RAM) 量。</span><span class="sxs-lookup"><span data-stu-id="8ed56-178">The following tables list the number of processors and the amount of random-access memory (RAM) that are required for each role that is required in order to run this deployment option.</span></span> <span data-ttu-id="8ed56-179">有关详细信息，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)中的 Service Fabric 独立群集建议最低要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-179">For more information, see the recommended minimum requirements for a Service Fabric standalone cluster in [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

> [!NOTE]
> <span data-ttu-id="8ed56-180">如果在同一台计算机上安装了其他 Microsoft 软件，系统还必须符合该软件的硬件要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-180">If other Microsoft software is installed on the same computer, the system must also comply with the hardware requirements for that software.</span></span> <span data-ttu-id="8ed56-181">如果其他服务器应用程序与 AOS 安装在同一台计算机上，我们建议你将这些服务器应用程序限制为 1 千兆字节 (GB) RAM。</span><span class="sxs-lookup"><span data-stu-id="8ed56-181">If other server applications are installed on the same computer as AOS, we recommend that you limit those server applications 1 gigabyte (GB) of RAM.</span></span>

<span data-ttu-id="8ed56-182">**按角色和拓扑类型的规模调整**</span><span class="sxs-lookup"><span data-stu-id="8ed56-182">**Sizing by role and topology type**</span></span>

| <span data-ttu-id="8ed56-183">拓扑</span><span class="sxs-lookup"><span data-stu-id="8ed56-183">Topology</span></span>   | <span data-ttu-id="8ed56-184">节点（节点类型）</span><span class="sxs-lookup"><span data-stu-id="8ed56-184">Role (node type)</span></span>              | <span data-ttu-id="8ed56-185">建议的处理器核数量</span><span class="sxs-lookup"><span data-stu-id="8ed56-185">Recommended processor cores</span></span> | <span data-ttu-id="8ed56-186">建议的内存 (GB)</span><span class="sxs-lookup"><span data-stu-id="8ed56-186">Recommended memory (GB)</span></span> |
|------------|-------------------------------|-----------------------------|-------------------------|
| <span data-ttu-id="8ed56-187">生产</span><span class="sxs-lookup"><span data-stu-id="8ed56-187">Production</span></span> | <span data-ttu-id="8ed56-188">AOS、数据管理、批处理</span><span class="sxs-lookup"><span data-stu-id="8ed56-188">AOS, Data management, Batch</span></span>   | <span data-ttu-id="8ed56-189">8</span><span class="sxs-lookup"><span data-stu-id="8ed56-189">8</span></span>                           | <span data-ttu-id="8ed56-190">24</span><span class="sxs-lookup"><span data-stu-id="8ed56-190">24</span></span>                      |
|            | <span data-ttu-id="8ed56-191">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="8ed56-191">Management Reporter</span></span>           | <span data-ttu-id="8ed56-192">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-192">4</span></span>                           | <span data-ttu-id="8ed56-193">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-193">16</span></span>                      |
|            | <span data-ttu-id="8ed56-194">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8ed56-194">SQL Server Reporting Services</span></span> | <span data-ttu-id="8ed56-195">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-195">4</span></span>                           | <span data-ttu-id="8ed56-196">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-196">16</span></span>                      |
|            | <span data-ttu-id="8ed56-197">Orchestrator</span><span class="sxs-lookup"><span data-stu-id="8ed56-197">Orchestrator</span></span>                  | <span data-ttu-id="8ed56-198">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-198">4</span></span>                           | <span data-ttu-id="8ed56-199">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-199">16</span></span>                      |
| <span data-ttu-id="8ed56-200">沙盒</span><span class="sxs-lookup"><span data-stu-id="8ed56-200">Sandbox</span></span>    | <span data-ttu-id="8ed56-201">AOS、数据管理、批处理</span><span class="sxs-lookup"><span data-stu-id="8ed56-201">AOS, Data management, Batch</span></span>   | <span data-ttu-id="8ed56-202">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-202">4</span></span>                           | <span data-ttu-id="8ed56-203">24</span><span class="sxs-lookup"><span data-stu-id="8ed56-203">24</span></span>                      |
|            | <span data-ttu-id="8ed56-204">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="8ed56-204">Management Reporter</span></span>           | <span data-ttu-id="8ed56-205">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-205">4</span></span>                           | <span data-ttu-id="8ed56-206">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-206">16</span></span>                      |
|            | <span data-ttu-id="8ed56-207">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8ed56-207">SQL Server Reporting Services</span></span> | <span data-ttu-id="8ed56-208">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-208">4</span></span>                           | <span data-ttu-id="8ed56-209">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-209">16</span></span>                      |
|            | <span data-ttu-id="8ed56-210">Orchestrator</span><span class="sxs-lookup"><span data-stu-id="8ed56-210">Orchestrator</span></span>                  | <span data-ttu-id="8ed56-211">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-211">4</span></span>                           | <span data-ttu-id="8ed56-212">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-212">16</span></span>                      |

<span data-ttu-id="8ed56-213">**生产和沙盒部署的最低规模调整估计\***</span><span class="sxs-lookup"><span data-stu-id="8ed56-213">**Minimum sizing estimates for production and sandbox deployments\***</span></span>

| <span data-ttu-id="8ed56-214">拓扑</span><span class="sxs-lookup"><span data-stu-id="8ed56-214">Topology</span></span>                                        | <span data-ttu-id="8ed56-215">角色</span><span class="sxs-lookup"><span data-stu-id="8ed56-215">Role</span></span>                          | <span data-ttu-id="8ed56-216">实例数</span><span class="sxs-lookup"><span data-stu-id="8ed56-216">Number of instances</span></span> |
|-------------------------------------------------|-------------------------------|---------------------|
| <span data-ttu-id="8ed56-217">生产</span><span class="sxs-lookup"><span data-stu-id="8ed56-217">Production</span></span>                                      | <span data-ttu-id="8ed56-218">AOS（数据管理、批处理）</span><span class="sxs-lookup"><span data-stu-id="8ed56-218">AOS (Data management, Batch)</span></span>  | <span data-ttu-id="8ed56-219">3</span><span class="sxs-lookup"><span data-stu-id="8ed56-219">3</span></span>                   |
|                                                 | <span data-ttu-id="8ed56-220">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="8ed56-220">Management Reporter</span></span>           | <span data-ttu-id="8ed56-221">2</span><span class="sxs-lookup"><span data-stu-id="8ed56-221">2</span></span>                   |
|                                                 | <span data-ttu-id="8ed56-222">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8ed56-222">SQL Server Reporting Services</span></span> | <span data-ttu-id="8ed56-223">1</span><span class="sxs-lookup"><span data-stu-id="8ed56-223">1</span></span>                   |
|                                                 | <span data-ttu-id="8ed56-224">Orchestrator\*\*</span><span class="sxs-lookup"><span data-stu-id="8ed56-224">Orchestrator\*\*</span></span>              | <span data-ttu-id="8ed56-225">3</span><span class="sxs-lookup"><span data-stu-id="8ed56-225">3</span></span>                   |
| <span data-ttu-id="8ed56-226">沙盒</span><span class="sxs-lookup"><span data-stu-id="8ed56-226">Sandbox</span></span>                                         | <span data-ttu-id="8ed56-227">AOS、数据管理、批处理</span><span class="sxs-lookup"><span data-stu-id="8ed56-227">AOS, Data management, Batch</span></span>   | <span data-ttu-id="8ed56-228">2</span><span class="sxs-lookup"><span data-stu-id="8ed56-228">2</span></span>                   |
|                                                 | <span data-ttu-id="8ed56-229">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="8ed56-229">Management Reporter</span></span>           | <span data-ttu-id="8ed56-230">1</span><span class="sxs-lookup"><span data-stu-id="8ed56-230">1</span></span>                   |
|                                                 | <span data-ttu-id="8ed56-231">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8ed56-231">SQL Server Reporting Services</span></span> | <span data-ttu-id="8ed56-232">1</span><span class="sxs-lookup"><span data-stu-id="8ed56-232">1</span></span>                   |
|                                                 | <span data-ttu-id="8ed56-233">Orchestrator</span><span class="sxs-lookup"><span data-stu-id="8ed56-233">Orchestrator</span></span>                  | <span data-ttu-id="8ed56-234">3</span><span class="sxs-lookup"><span data-stu-id="8ed56-234">3</span></span>                   |
| <span data-ttu-id="8ed56-235">*生产和沙盒拓扑摘要*</span><span class="sxs-lookup"><span data-stu-id="8ed56-235">*Summary for production and sandbox topologies*</span></span> |                               | <span data-ttu-id="8ed56-236">*16*</span><span class="sxs-lookup"><span data-stu-id="8ed56-236">*16*</span></span>                |

<span data-ttu-id="8ed56-237">\* 此表中的数字正在由预览客户验证，可能根据这些客户的反馈进行调整。</span><span class="sxs-lookup"><span data-stu-id="8ed56-237">\* The numbers in this table are being validated by our preview customers and might be adjusted based on the feedback from those customers.</span></span>

<span data-ttu-id="8ed56-238">\*\*Orchestrator 被指定为主节点类型，也用于运行 Service Fabric 服务。</span><span class="sxs-lookup"><span data-stu-id="8ed56-238">\*\* Orchestrator is designated as the primary node type and will also be used to run the Service Fabric services.</span></span>

<span data-ttu-id="8ed56-239">**后端 SQL Server 和 AD DS 的初始估计**</span><span class="sxs-lookup"><span data-stu-id="8ed56-239">**Initial estimates for the back-end SQL Server and AD DS**</span></span>

<table>
<thead>
<tr>
<th></th>
<th><span data-ttu-id="8ed56-240">角色</span><span class="sxs-lookup"><span data-stu-id="8ed56-240">Role</span></span></th>
<th><span data-ttu-id="8ed56-241">VM/实例</span><span class="sxs-lookup"><span data-stu-id="8ed56-241">VMs/instances</span></span></th>
<th><span data-ttu-id="8ed56-242">内核</span><span class="sxs-lookup"><span data-stu-id="8ed56-242">Cores</span></span></th>
<th><span data-ttu-id="8ed56-243">内核总数</span><span class="sxs-lookup"><span data-stu-id="8ed56-243">Total cores</span></span></th>
<th><span data-ttu-id="8ed56-244">每个实例的内存 (GB)</span><span class="sxs-lookup"><span data-stu-id="8ed56-244">Memory per instance (GB)</span></span></th>
<th><span data-ttu-id="8ed56-245">内存总量 (GB)</span><span class="sxs-lookup"><span data-stu-id="8ed56-245">Total memory (GB)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><span data-ttu-id="8ed56-246"><strong>共享基础结构</strong></span><span class="sxs-lookup"><span data-stu-id="8ed56-246"><strong>Shared infrastructure</strong></span></span></td>
<td><span data-ttu-id="8ed56-247">SQL Server*</span><span class="sxs-lookup"><span data-stu-id="8ed56-247">SQL Server*</span></span></td>
<td><span data-ttu-id="8ed56-248">2</span><span class="sxs-lookup"><span data-stu-id="8ed56-248">2</span></span></td>
<td><span data-ttu-id="8ed56-249">8</span><span class="sxs-lookup"><span data-stu-id="8ed56-249">8</span></span></td>
<td><span data-ttu-id="8ed56-250">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-250">16</span></span></td>
<td><span data-ttu-id="8ed56-251">32</span><span class="sxs-lookup"><span data-stu-id="8ed56-251">32</span></span></td>
<td><span data-ttu-id="8ed56-252">64</span><span class="sxs-lookup"><span data-stu-id="8ed56-252">64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ed56-253">文件服务器/存储是网络/高可用性存储</span><span class="sxs-lookup"><span data-stu-id="8ed56-253">File server/Storage area network/Highly available storage</span></span></td>
<td colspan="5"><p><span data-ttu-id="8ed56-254">后端存储必须基于运行时存储区域网络 (SAN) 中的固态硬盘 (SSD)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-254">The back-end storage must be based on solid-state drives (SSDs) on a runtime storage area network (SAN).</span></span></p>
<p><span data-ttu-id="8ed56-255">大小和每秒输入/输出操作 (IOPS) 吞吐量基于工作负载的大小。</span><span class="sxs-lookup"><span data-stu-id="8ed56-255">Size and input/output operations per second (IOPS) throughput is based on the size of the workload.</span></span></p></td>
</tr>
<tr>
<td><span data-ttu-id="8ed56-256">Active Directory</span><span class="sxs-lookup"><span data-stu-id="8ed56-256">Active Directory</span></span></td>
<td><span data-ttu-id="8ed56-257">3</span><span class="sxs-lookup"><span data-stu-id="8ed56-257">3</span></span></td>
<td><span data-ttu-id="8ed56-258">4</span><span class="sxs-lookup"><span data-stu-id="8ed56-258">4</span></span></td>
<td><span data-ttu-id="8ed56-259">12</span><span class="sxs-lookup"><span data-stu-id="8ed56-259">12</span></span></td>
<td><span data-ttu-id="8ed56-260">16</span><span class="sxs-lookup"><span data-stu-id="8ed56-260">16</span></span></td>
<td><span data-ttu-id="8ed56-261">48</span><span class="sxs-lookup"><span data-stu-id="8ed56-261">48</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ed56-262"><em>共享基础结构摘要</em></span><span class="sxs-lookup"><span data-stu-id="8ed56-262"><em>Summary for shared infrastructure</em></span></span></td>
<td></td>
<td><span data-ttu-id="8ed56-263"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="8ed56-263"><em>5</em></span></span></td>
<td></td>
<td><span data-ttu-id="8ed56-264"><em>28</em></span><span class="sxs-lookup"><span data-stu-id="8ed56-264"><em>28</em></span></span></td>
<td></td>
<td><span data-ttu-id="8ed56-265"><em>112</em></span><span class="sxs-lookup"><span data-stu-id="8ed56-265"><em>112</em></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ed56-266">\*SQL Server 大小高度依赖于工作负荷。</span><span class="sxs-lookup"><span data-stu-id="8ed56-266">\* SQL Server sizes are highly dependent on workloads.</span></span> <span data-ttu-id="8ed56-267">有关详细信息，请参阅[针对本地环境的硬件规模调整](hardware-sizing-on-premises-environments.md)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-267">For more information, see [Hardware sizing for on-premises environments](hardware-sizing-on-premises-environments.md).</span></span>

## <a name="storage"></a><span data-ttu-id="8ed56-268">存储</span><span class="sxs-lookup"><span data-stu-id="8ed56-268">Storage</span></span>

- <span data-ttu-id="8ed56-269">**AOS** - Finance and Operations（本地）使用服务器消息块 (SMB) 3.0 共享以存储非结构化数据。</span><span class="sxs-lookup"><span data-stu-id="8ed56-269">**AOS** – Finance and Operations (on-premises) uses a Server Message Block (SMB) 3.0 share to store unstructured data.</span></span> <span data-ttu-id="8ed56-270">有关详细信息，请参阅 [Windows Server 2016 中的 Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-270">For more information, see [Storage Spaces Direct in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).</span></span>
- <span data-ttu-id="8ed56-271">**SQL** - 支持以下选项：</span><span class="sxs-lookup"><span data-stu-id="8ed56-271">**SQL** – The following options are viable:</span></span>

    - <span data-ttu-id="8ed56-272">高可用 SSD 设置</span><span class="sxs-lookup"><span data-stu-id="8ed56-272">A highly available SSD setup</span></span>
    - <span data-ttu-id="8ed56-273">专门针对在线交易处理 (OLTP) 吞吐量进行过优化的 SAN</span><span class="sxs-lookup"><span data-stu-id="8ed56-273">A SAN that is optimized for online transaction processing (OLTP) throughputs</span></span>
    - <span data-ttu-id="8ed56-274">高性能直接连接的存储 (DAS)</span><span class="sxs-lookup"><span data-stu-id="8ed56-274">High-performance direct-attached storage (DAS)</span></span> 

- <span data-ttu-id="8ed56-275">**SQL Server 和数据管理 IOPS** - 用于数据管理和 SQL Server 的存储每秒钟至少应具有 2,000 次 IOPS。</span><span class="sxs-lookup"><span data-stu-id="8ed56-275">**SQL Server and data management IOPS** – The storage for both data management and SQL Server should have at least 2,000 IOPS.</span></span> <span data-ttu-id="8ed56-276">生产 IOPS 取决于许多因素。</span><span class="sxs-lookup"><span data-stu-id="8ed56-276">Production IOPS depends on many factors.</span></span> <span data-ttu-id="8ed56-277">有关详细信息，请参阅[针对本地环境的硬件规模调整](hardware-sizing-on-premises-environments.md)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-277">For more information, see [Hardware sizing for on-premises environments](hardware-sizing-on-premises-environments.md).</span></span>
- <span data-ttu-id="8ed56-278">**VM IOPS** - 每个 VM 应具有至少 100 次的写入 IOPS。</span><span class="sxs-lookup"><span data-stu-id="8ed56-278">**VM IOPS** – Each VM should have at least 100 write IOPS.</span></span>

## <a name="virtual-host-requirements"></a><span data-ttu-id="8ed56-279">虚拟主机要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-279">Virtual host requirements</span></span>
<span data-ttu-id="8ed56-280">当你设置 Finance and Operations（本地）环境的虚拟主机时，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) 和[描述 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description)中的指南。</span><span class="sxs-lookup"><span data-stu-id="8ed56-280">When you set up the virtual hosts for a Finance and Operations (on-premises) environment, see the guidelines in [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) and [Describing a service fabric cluster](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description).</span></span> <span data-ttu-id="8ed56-281">每个虚拟主机都应具有足够的核心用于正在进行规模调整的基础结构。</span><span class="sxs-lookup"><span data-stu-id="8ed56-281">Each virtual host should have enough cores for the infrastructure that is being sized.</span></span> <span data-ttu-id="8ed56-282">当 SQL Server 位于物理硬件但其他所有内容均虚拟化时，可以进行多种高级配置。</span><span class="sxs-lookup"><span data-stu-id="8ed56-282">Multiple advanced configurations are possible, where SQL Server resides on physical hardware but everything else is virtualized.</span></span> <span data-ttu-id="8ed56-283">如果 SQL Server 虚拟化，磁盘子系统应为快速 SAN 或等效物。</span><span class="sxs-lookup"><span data-stu-id="8ed56-283">If SQL Server is virtualized, the disk subsystem should be a fast SAN or the equivalent.</span></span> <span data-ttu-id="8ed56-284">在任何情况下，确保虚拟主机的基本设置可用性高且冗余。</span><span class="sxs-lookup"><span data-stu-id="8ed56-284">In all cases, make sure that the basic setup of the virtual host is highly available and redundant.</span></span> <span data-ttu-id="8ed56-285">在任何情况下，在使用虚拟化时，不应拍摄 VM 快照。</span><span class="sxs-lookup"><span data-stu-id="8ed56-285">In all cases, when virtualization is used, no VM snapshots should be taken.</span></span>

## <a name="software-requirements-for-all-server-computers"></a><span data-ttu-id="8ed56-286">针对所有服务器计算机的软件要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-286">Software requirements for all server computers</span></span>
<span data-ttu-id="8ed56-287">在安装任何 Finance and Operations（本地）组件前，计算机上必须存在以下软件：</span><span class="sxs-lookup"><span data-stu-id="8ed56-287">The following software must be present on a computer before any Finance and Operations (on-premises) components can be installed:</span></span>

- <span data-ttu-id="8ed56-288">Microsoft .NET Framework 版本 4.5.1 或更高版本</span><span class="sxs-lookup"><span data-stu-id="8ed56-288">The Microsoft .NET Framework version 4.5.1 or later</span></span>
- <span data-ttu-id="8ed56-289">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8ed56-289">Service Fabric</span></span>

<span data-ttu-id="8ed56-290">有关详细信息，请参阅[计划和准备你的 Service Fabric 群集](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-290">For more information, see [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="supported-server-operating-systems"></a><span data-ttu-id="8ed56-291">支持的服务器操作系统</span><span class="sxs-lookup"><span data-stu-id="8ed56-291">Supported server operating systems</span></span>
<span data-ttu-id="8ed56-292">下表列出了支持 Finance and Operations 组件的服务器操作系统。</span><span class="sxs-lookup"><span data-stu-id="8ed56-292">The following table lists the server operating systems that are supported for Finance and Operations components.</span></span>

| <span data-ttu-id="8ed56-293">操作系统</span><span class="sxs-lookup"><span data-stu-id="8ed56-293">Operating system</span></span>                                     | <span data-ttu-id="8ed56-294">注释</span><span class="sxs-lookup"><span data-stu-id="8ed56-294">Notes</span></span> |
|------------------------------------------------------|-------|
| <span data-ttu-id="8ed56-295">Microsoft Windows Server 2016 数据中心或标准</span><span class="sxs-lookup"><span data-stu-id="8ed56-295">Microsoft Windows Server 2016 Datacenter or Standard</span></span> | <span data-ttu-id="8ed56-296">以下是针对托管 AOS 的数据库和 Service Fabric 群集的要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-296">These requirements are for the database and the Service Fabric cluster that hosts AOS.</span></span> |

## <a name="software-requirements-for-database-servers"></a><span data-ttu-id="8ed56-297">针对数据库服务器的软件要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-297">Software requirements for database servers</span></span>

- <span data-ttu-id="8ed56-298">仅 SQL Server 2016 的 64 位版本受支持。</span><span class="sxs-lookup"><span data-stu-id="8ed56-298">Only 64-bit versions of SQL Server 2016 are supported.</span></span>
- <span data-ttu-id="8ed56-299">在生产环境中，我们建议你针对你使用的 SQL Server 版本安装最新累积更新 (CU)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-299">In a production environment, we recommend that you install the latest cumulative update (CU) for the version of SQL Server that you’re using.</span></span>
- <span data-ttu-id="8ed56-300">Finance and Operations（本地）支持区分大小写、区分重音、区分假名、不区分全半角的 Unicode 排序规则。</span><span class="sxs-lookup"><span data-stu-id="8ed56-300">Finance and Operations (on-premises) supports Unicode collations that are case-insensitive, accent-sensitive, kana-sensitive, and width-insensitive.</span></span> <span data-ttu-id="8ed56-301">排序规则必须与运行 AOS 实例的计算机的 Windows 区域设置相匹配。</span><span class="sxs-lookup"><span data-stu-id="8ed56-301">The collation must match the Windows locale of the computers that are running AOS instances.</span></span> <span data-ttu-id="8ed56-302">如果你正在设置新的安装，建议你选择 Windows 排序规则而不是 SQL Server 排序规则。</span><span class="sxs-lookup"><span data-stu-id="8ed56-302">If you’re setting up a new installation, we recommend that you select a Windows collation instead of a SQL Server collation.</span></span> <span data-ttu-id="8ed56-303">有关如何选择 SQL Server 数据库排序规则的详细信息，请参阅 [SQL Server 文档](/sql/sql-server/sql-server-technical-documentation)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-303">For more information about how to select a collation for a SQL Server database, see the [SQL Server documentation](/sql/sql-server/sql-server-technical-documentation).</span></span>

<span data-ttu-id="8ed56-304">下表列出了支持 Finance and Operations 数据库的 SQL Server 版本。</span><span class="sxs-lookup"><span data-stu-id="8ed56-304">The following table lists the SQL Server versions that are supported for the Finance and Operations databases.</span></span> <span data-ttu-id="8ed56-305">有关详细信息，请参阅 [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) 的最低硬件要求。</span><span class="sxs-lookup"><span data-stu-id="8ed56-305">For more information, see the minimum hardware requirements for [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).</span></span>

| <span data-ttu-id="8ed56-306">需求</span><span class="sxs-lookup"><span data-stu-id="8ed56-306">Requirement</span></span>                                                      | <span data-ttu-id="8ed56-307">注释</span><span class="sxs-lookup"><span data-stu-id="8ed56-307">Notes</span></span> |
|------------------------------------------------------------------|-------|
| <span data-ttu-id="8ed56-308">Microsoft SQL Server 2016 Standard 版本 或 Enterprise 版本</span><span class="sxs-lookup"><span data-stu-id="8ed56-308">Microsoft SQL Server 2016 Standard Edition or Enterprise Edition</span></span> | <span data-ttu-id="8ed56-309">有关 SQL Server 2016 的硬件要求，请参阅[安装 SQL Server 2016 的硬件和软件要求](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-309">For the hardware requirements for SQL Server 2016, see [Hardware and Software Requirements for Installing SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server).</span></span> |

## <a name="software-requirements-for-client-computers"></a><span data-ttu-id="8ed56-310">针对客户端计算机的软件要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-310">Software requirements for client computers</span></span>
<span data-ttu-id="8ed56-311">Finance and Operations Web 应用程序可以使用兼容 HTML 5.0 的 Web 浏览器在任何设备上运行。</span><span class="sxs-lookup"><span data-stu-id="8ed56-311">The Finance and Operations web application can run on any device that has an HTML 5.0–compliant web browser.</span></span> <span data-ttu-id="8ed56-312">下面是 Microsoft 已确认的一些特定设备/浏览器组合：</span><span class="sxs-lookup"><span data-stu-id="8ed56-312">Here are some of the specific device/browser combinations that Microsoft has confirmed:</span></span>

- <span data-ttu-id="8ed56-313">Windows 10 上的 Microsoft Edge（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="8ed56-313">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="8ed56-314">Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="8ed56-314">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="8ed56-315">Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="8ed56-315">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
- <span data-ttu-id="8ed56-316">Mac OS X 10.10 (Yosemite)、10.11 (Capitan)、10.12 (Sierra) 或 Apple iPad 上的 Apple Safari（最新公开提供的版本）</span><span class="sxs-lookup"><span data-stu-id="8ed56-316">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

## <a name="software-requirements-for-active-directory-federation-services"></a><span data-ttu-id="8ed56-317">Active Directory 联合身份验证服务的软件要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-317">Software requirements for Active Directory Federation Services</span></span> 
<span data-ttu-id="8ed56-318">需要 Windows Server 2016 上的 Active Directory 联合身份验证服务 (AD FS)</span><span class="sxs-lookup"><span data-stu-id="8ed56-318">Active Directory Federation Services (AD FS) on Windows Server 2016 is required.</span></span>

<span data-ttu-id="8ed56-319">域控制器必须是 Windows Server 2012 R2 或更高版本，域功能级别必须是 2012 R2 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="8ed56-319">The domain controller must be Windows Server 2012 R2 or later, and the domain functional level must be 2012 R2 or more.</span></span> <span data-ttu-id="8ed56-320">有关域功能级别的详细信息，请参阅以下页面：</span><span class="sxs-lookup"><span data-stu-id="8ed56-320">For more information about domain functional levels, see the following pages:</span></span>

- <span data-ttu-id="8ed56-321">[什么是 Active Directory 功能级别](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed56-321">[What Are Active Directory Functional Levels](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)</span></span>
- <span data-ttu-id="8ed56-322">[了解 Active Directory 域服务功能级别](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed56-322">[Understanding Active Directory Domain Services Functional Levels](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="8ed56-323">支持的 Microsoft Office 应用程序</span><span class="sxs-lookup"><span data-stu-id="8ed56-323">Supported Microsoft Office applications</span></span>
<span data-ttu-id="8ed56-324">以下 Microsoft Office 应用程序在 Finance and Operations 的云和本地部署中受支持：</span><span class="sxs-lookup"><span data-stu-id="8ed56-324">The following Microsoft Office applications are supported in the cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="8ed56-325">若要运行 Microsoft Excel 和 Microsoft Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。</span><span class="sxs-lookup"><span data-stu-id="8ed56-325">To run the Microsoft Excel and Microsoft Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="8ed56-326">有关版本要求的详细信息，请参阅 [Office 集成疑难解答](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting)。</span><span class="sxs-lookup"><span data-stu-id="8ed56-326">For more information about version requirements, see [Office integration troubleshooting](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span></span>
-   <span data-ttu-id="8ed56-327">若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="8ed56-327">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>
 
## <a name="hardware-and-software-requirements-for-retail-components"></a><span data-ttu-id="8ed56-328">针对 Retail 组件的硬件和软件要求</span><span class="sxs-lookup"><span data-stu-id="8ed56-328">Hardware and software requirements for Retail components</span></span>
<span data-ttu-id="8ed56-329">Finance and Operations（本地）目前不包括 Retail 组件。</span><span class="sxs-lookup"><span data-stu-id="8ed56-329">Currently, Finance and Operations (on-premises) doesn't include the Retail components.</span></span>

