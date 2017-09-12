---
title: "针对本地环境的硬件规模调整要求"
description: "本主题列出了针对本地环境的硬件规模调整要求。"
author: kfend
manager: AnnBe
ms.date: 06/23/2017
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
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4a1cab8c126ad063a52827421d2ea1104d0c7287
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="hardware-sizing-for-on-premises-environments"></a><span data-ttu-id="b4bdc-103">针对本地环境的硬件规模调整</span><span class="sxs-lookup"><span data-stu-id="b4bdc-103">Hardware sizing for on-premises environments</span></span>
<span data-ttu-id="b4bdc-104">在你开始对本地环境执行硬件和基础结构规模调整流程前，请熟悉[系统要求](../get-started/system-requirements.md) 和[设置和部署说明](../deployment/setup-deploy-on-premises-environments.md) 以充分了解基础结构。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements](../get-started/system-requirements.md) and [Setup and deployment instructions](../deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span> 

  <span data-ttu-id="b4bdc-105">**注意：**密切关注可实现最优性能的系统设置最佳实践。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-105">**Note:** Pay close attention to the system setup best practices for optimum performance.</span></span> 

<span data-ttu-id="b4bdc-106">在查看文档后，你可以开始评估你的事务性和并发用户数量并基于平均核心吞吐量对环境调整规模的流程。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="b4bdc-107">影响规模调整的系数</span><span class="sxs-lookup"><span data-stu-id="b4bdc-107">Factors that affect sizing</span></span>
<span data-ttu-id="b4bdc-108">在下图显示的所有系数都对规模调整具有影响。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="b4bdc-109">收集的详细信息越多，你就越能更加精确地确定规模调整。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="b4bdc-110">不具有支持数据的硬件规模调整可能不准确。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="b4bdc-111">所需数据的绝对最低需求是峰值交易记录行每小时负荷。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span> 

<span data-ttu-id="b4bdc-112">[![针对本地环境的硬件规模调整](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="b4bdc-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="b4bdc-113">从左到右查看，准确估计规模调整所需的第一个和最重要的系数是交易记录模板或交易记录特征。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="b4bdc-114">始终查找每小时交易量峰值很重要。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-114">It’s important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="b4bdc-115">如果存在多个峰值期间，则需要准确地定义这些期间。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span> 

<span data-ttu-id="b4bdc-116">你了解影响基础结构的负荷后，还需了解有关这些系数的更多详细信息：</span><span class="sxs-lookup"><span data-stu-id="b4bdc-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span> 

- <span data-ttu-id="b4bdc-117">**交易记录** - 交易记录通常在一天/周中具有特定的峰值。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-117">**Transactions** - Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="b4bdc-118">这主要取决于交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="b4bdc-119">时间和支出条目通常显示每周峰值，而销售订单条目通常通过集成批量出现或在一天中缓缓出现。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span> 

- <span data-ttu-id="b4bdc-120">**并发用户的数量** - 并发用户的数量是第二重要的规模调整系数。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="b4bdc-121">基于并发用户的数量无法可靠地获取规模调整估计，因此如果这是你唯一可用的数据，则估计一个近似数字，然后当你获得更多数据时再次访问。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="b4bdc-122">准确的并发用户定义意味着：</span><span class="sxs-lookup"><span data-stu-id="b4bdc-122">An accurate concurrent user definition means that:</span></span> 
  - <span data-ttu-id="b4bdc-123">指定用户不是并发用户。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-123">Named users are not concurrent users.</span></span>
  - <span data-ttu-id="b4bdc-124">并发用户始终是指定用户的子集。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-124">Concurrent users are always a subset of named users.</span></span> 
  - <span data-ttu-id="b4bdc-125">峰值工作负荷定义规模调整的最大并发数。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-125">Peak workload defines the maximum concurrency for sizing.</span></span>
 
- <span data-ttu-id="b4bdc-126">并发用户的条件是用户满足以下所有条件：</span><span class="sxs-lookup"><span data-stu-id="b4bdc-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span> 
  - <span data-ttu-id="b4bdc-127">已登录。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-127">Logged on.</span></span> 
  - <span data-ttu-id="b4bdc-128">在盘点时的工作交易记录/查询。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-128">Working transactions/inquiries at the time of counting.</span></span> 
  - <span data-ttu-id="b4bdc-129">不是空闲会话。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-129">Not an idle session.</span></span> 
 
- <span data-ttu-id="b4bdc-130">**数据构成** - 这主要与你的系统将如何设置和配置有关。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="b4bdc-131">例如，你有多少法人、多少物料、多少 BOM 级别以及你的安全设置将有多复杂。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="b4bdc-132">这些系数中的每个系数都可能对性能有较小的影响，因此可以通过对基础结构使用明智的选项来抵消这些系数。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span> 

- <span data-ttu-id="b4bdc-133">**扩展** - 可以是简单或复杂的自定义。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="b4bdc-134">自定义的数量以及复杂性和使用的性质对所需基础结构的规模有不同的影响。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="b4bdc-135">对于复杂的自定义，建议执行性能评估以确保它们不仅通过效率测试，而且有助于了解基础结构需要。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-135">For complex customizations, it’s advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="b4bdc-136">没有根据性能和可扩展性最佳实践对扩展进行编码时，这一点甚至更加关键。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span> 

- <span data-ttu-id="b4bdc-137">**报告和分析** - 这些系数通常包括在 Finance and Operations 数据库系统中对不同数据库运行大量查询。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</span></span> <span data-ttu-id="b4bdc-138">了解和减少运行昂贵报表的频率将帮助你了解它们的影响。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span> 

- <span data-ttu-id="b4bdc-139">**第三方解决方案** - 这些解决方案，例如 ISV，同扩展一样具有相同的影响和建议。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span> 

## <a name="sizing-your-finance-and-operations-environment"></a><span data-ttu-id="b4bdc-140">对你的 Finance and Operations 环境进行规模调整</span><span class="sxs-lookup"><span data-stu-id="b4bdc-140">Sizing your Finance and Operations environment</span></span>
<span data-ttu-id="b4bdc-141">若要了解你的规模调整需求，你需要知道你需要处理的峰值交易记录量。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="b4bdc-142">大多数辅助系统，例如 Management Reporter 或 SSRS，对任务没有那么关键。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="b4bdc-143">因此，文档主要关注 AOS 和 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span> 

<span data-ttu-id="b4bdc-144">**注意：**一般来说，计算层扩大且应按 N+1 的方式设置，意味着如果你估计有三个 AOS，则添加第四个 AOS。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-144">**Note:** In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="b4bdc-145">数据库层应在 Always On 高可用性设置中进行设置。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-145">The database tier should be set up in an Always On highly-available setup.</span></span> 


## <a name="sql-server-oltp"></a><span data-ttu-id="b4bdc-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="b4bdc-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="b4bdc-147">规模调整</span><span class="sxs-lookup"><span data-stu-id="b4bdc-147">Sizing</span></span>

- <span data-ttu-id="b4bdc-148">DB 服务器上每核心每小时 3K 到 15K 交易记录行。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="b4bdc-149">主要 SQL Server 的典型 AOS 到 SQL 核心比率 3:1。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="b4bdc-150">基于所选的高可用性配置需要额外核心。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-150">Additional cores are required based on the chosen high availability configuration.</span></span> 
  - <span data-ttu-id="b4bdc-151">处理数据库负荷重的操作可能使其后退到 2:1。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-151">Processing database-heavy operations may regress this to 2:1.</span></span> 
- <span data-ttu-id="b4bdc-152">以下系数影响差异：</span><span class="sxs-lookup"><span data-stu-id="b4bdc-152">The following factors influence variations:</span></span> 
  - <span data-ttu-id="b4bdc-153">在使用中的参数设置。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-153">Parameter settings in use.</span></span> 
  - <span data-ttu-id="b4bdc-154">扩展级别。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-154">Levels of extensions.</span></span> 
  - <span data-ttu-id="b4bdc-155">附加功能的使用，如数据库日志和预警。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="b4bdc-156">极端数据库记录将进一步将每核心每小时吞吐量降低至 3K 行以下。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span> 
  - <span data-ttu-id="b4bdc-157">数据构成的复杂性 - 一个简单的会计科目表与详细的会计科目表之间的对比对吞吐量具有影响（作为示例）。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span> 
  - <span data-ttu-id="b4bdc-158">交易记录特征。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-158">Transaction characterization.</span></span>
  - <span data-ttu-id="b4bdc-159">每核心 2 GB 至 4 GB 内存。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-159">2 GB to 4 GB memory for each core.</span></span> 
  - <span data-ttu-id="b4bdc-160">DB 服务器上的辅助数据库，例如 Management Reporter 和 SSRS 数据库。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
  - <span data-ttu-id="b4bdc-161">临时 DB = DB 大小的 15%，其中文件的数量与物理处理器的数量相同。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span> 
  - <span data-ttu-id="b4bdc-162">基于总并发交易记录数量/使用量的 SAN 大小和吞吐量。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span> 

### <a name="high-availability"></a><span data-ttu-id="b4bdc-163">高可用性</span><span class="sxs-lookup"><span data-stu-id="b4bdc-163">High availability</span></span> 
<span data-ttu-id="b4bdc-164">我们建议始终在群集或镜像设置中使用 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="b4bdc-165">第二个 SQL 节点应与主节点具有相同数量的核心。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-165">The second SQL node should have the same number of cores as the primary node.</span></span> 

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="b4bdc-166">Active Directory 联合身份验证服务 (AD FS)</span><span class="sxs-lookup"><span data-stu-id="b4bdc-166">Active Directory Federation Services (AD FS)</span></span>
<span data-ttu-id="b4bdc-167">有关 AD FS 规模调整，请参阅 [AD FS 服务器产能文档](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-167">For AD FS sizing, see the [AD FS Server Capacity documentation](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="b4bdc-168">[规模调整电子表格](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) 可用于规划你的部署中的实例数量。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-168">A [sizing spreadsheet](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

<a name="aos-online-and-batch"></a><span data-ttu-id="b4bdc-169">AOS（联机和批处理）</span><span class="sxs-lookup"><span data-stu-id="b4bdc-169">AOS (Online and batch)</span></span>
----------------------

### <a name="sizing"></a><span data-ttu-id="b4bdc-170">规模调整</span><span class="sxs-lookup"><span data-stu-id="b4bdc-170">Sizing</span></span>

- <span data-ttu-id="b4bdc-171">按交易量/使用量进行规模调整</span><span class="sxs-lookup"><span data-stu-id="b4bdc-171">Sizing by transaction volume/usage</span></span>
  - <span data-ttu-id="b4bdc-172">每核心 2K 到 6K 行</span><span class="sxs-lookup"><span data-stu-id="b4bdc-172">2K to 6K lines per core</span></span>
  - <span data-ttu-id="b4bdc-173">每个实例 16 GB</span><span class="sxs-lookup"><span data-stu-id="b4bdc-173">16 GB per instance</span></span>
  - <span data-ttu-id="b4bdc-174">标准框– 4 到 24 个核心</span><span class="sxs-lookup"><span data-stu-id="b4bdc-174">Standard box – 4 to 24 cores</span></span>
  - <span data-ttu-id="b4bdc-175">每核心 10 到 15 个企业用户</span><span class="sxs-lookup"><span data-stu-id="b4bdc-175">10 to 15 Enterprise users per core</span></span>
  - <span data-ttu-id="b4bdc-176">每核心 15 到 25 个活动用户</span><span class="sxs-lookup"><span data-stu-id="b4bdc-176">15 to 25 Activity users per core</span></span>
  - <span data-ttu-id="b4bdc-177">每核心 25 到 50 个团队成员</span><span class="sxs-lookup"><span data-stu-id="b4bdc-177">25 to 50 Team members per core</span></span>
- <span data-ttu-id="b4bdc-178">批处理</span><span class="sxs-lookup"><span data-stu-id="b4bdc-178">Batch</span></span>
   - <span data-ttu-id="b4bdc-179">每核心 1 到 4 个批处理线程数。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-179">1 to 4 batch threads per core</span></span>
   - <span data-ttu-id="b4bdc-180">基于批处理窗口特征进行规模调整</span><span class="sxs-lookup"><span data-stu-id="b4bdc-180">Size based on batch window characterization</span></span>
- <span data-ttu-id="b4bdc-181">注意，AOS、数据管理和批处理在 Service Fabric 中具有相同的角色。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="b4bdc-182">你需要为合并的这三种工作负荷进行规模调整，而不像在 Microsoft Dynamics AX 2012 中一样将它们分开。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="b4bdc-183">用于 SQL Server 的相同可变性系数在此处适用。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="b4bdc-184">高可用性</span><span class="sxs-lookup"><span data-stu-id="b4bdc-184">High availability</span></span>
- <span data-ttu-id="b4bdc-185">确保可用的 AOS 比你估计的数量多 1 到 2 个。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="b4bdc-186">确保你具有至少 3 到 4 个虚拟主机可用。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="b4bdc-187">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="b4bdc-187">Management reporter</span></span>
<span data-ttu-id="b4bdc-188">在大多数情况下，除非使用广泛，否则建议的最低需求使用两个节点应可以正常工作。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="b4bdc-189">只有在使用量大的情况下，你才需要两个以上节点。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="b4bdc-190">请根据需要扩展。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="b4bdc-191">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="b4bdc-191">SQL Server Reporting Services</span></span>
<span data-ttu-id="b4bdc-192">对于一般可用性版本，只可以部署一个 SSRS 节点。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="b4bdc-193">在测试时监控你的 SSRS 节点，并根据需要增加可用于 SSRS 的核心数量。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="b4bdc-194">确保你在不同于 SSRS VM 的虚拟机上有预先配置的次节点可用。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="b4bdc-195">如果托管 SSRS 的虚拟机或虚拟主机出现问题，则这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="b4bdc-196">如果出现这种情况，将需要更换它们。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-196">If this the case, they would need to be replaced.</span></span> 

## <a name="environment-orchestrator"></a><span data-ttu-id="b4bdc-197">环境 Orchestrator</span><span class="sxs-lookup"><span data-stu-id="b4bdc-197">Environment Orchestrator</span></span>
<span data-ttu-id="b4bdc-198">Orchestrator 服务是用于管理你的部署和与 LCS 的相关通信的服务。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="b4bdc-199">此服务部署为主 Service Fabric 服务并需要至少三个 VM。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="b4bdc-200">此服务与 Service Fabric Orchestration 服务位于同一位置。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="b4bdc-201">这应该调整到群集的峰值负荷。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="b4bdc-202">有关详细信息，请参阅 [Service Fabric 群集产能规划注意事项](/azure/service-fabric/service-fabric-cluster-capacity)。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-202">For more information, see [Service Fabric cluster capacity planning considerations](/azure/service-fabric/service-fabric-cluster-capacity).</span></span>  


## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="b4bdc-203">虚拟化和过度订阅</span><span class="sxs-lookup"><span data-stu-id="b4bdc-203">Virtualization and oversubscription</span></span>
<span data-ttu-id="b4bdc-204">关键任务服务（如 AOS）应在具有专用资源（核心、内存和磁盘）的虚拟机上托管。</span><span class="sxs-lookup"><span data-stu-id="b4bdc-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>   


