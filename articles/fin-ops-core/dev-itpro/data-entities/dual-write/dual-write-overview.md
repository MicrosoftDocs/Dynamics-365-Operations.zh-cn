---
title: 双写入概述
description: 本主题概述双写入。 双写入是一种基础结构，其提供 Microsoft Dynamics 365 模型驱动应用与 Finance and Operations 应用之间的近实时交互。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 961e6a167d4fe48c96bffcff1e54acde0ad5d805
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997416"
---
# <a name="dual-write-overview"></a><span data-ttu-id="2cdbd-104">双写入概述</span><span class="sxs-lookup"><span data-stu-id="2cdbd-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="2cdbd-105">什么是双写入？</span><span class="sxs-lookup"><span data-stu-id="2cdbd-105">What is dual-write?</span></span>

<span data-ttu-id="2cdbd-106">双写入是一种自带基础结构，其提供 Customer Engagement 应用与 Finance and Operations 应用之间的近实时交互。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="2cdbd-107">当有关客户、产品、人员和操作的数据越过应用程序边界时，将为组织中的所有部门授权。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="2cdbd-108">双写入提供 Finance and Operations 应用与 Common Data Service 之间紧密耦合的双向集成。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="2cdbd-109">Finance and Operations 应用中的所有数据变化都会写入 Common Data Service，而 Common Data Service 中的所有数据变化也会导致写入 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="2cdbd-110">这个自动化的数据流提供了应用之间的集成用户体验。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![应用之间的数据关系](media/dual-write-overview.jpg)

<span data-ttu-id="2cdbd-112">双写入有两个方面： *基础结构* 方面和 *应用程序* 方面。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="2cdbd-113">基础结构</span><span class="sxs-lookup"><span data-stu-id="2cdbd-113">Infrastructure</span></span>

<span data-ttu-id="2cdbd-114">双写入基础结构可扩展且可靠，并且具有以下关键功能：</span><span class="sxs-lookup"><span data-stu-id="2cdbd-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="2cdbd-115">应用程序之间的同步和双向数据流</span><span class="sxs-lookup"><span data-stu-id="2cdbd-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="2cdbd-116">同步和播放、暂停与继续模式，用于在联机和脱机/异步模式下共同为系统提供支持。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="2cdbd-117">在应用程序之间同步初始数据</span><span class="sxs-lookup"><span data-stu-id="2cdbd-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="2cdbd-118">适用于数据管理员的，合并的活动与错误日志视图</span><span class="sxs-lookup"><span data-stu-id="2cdbd-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="2cdbd-119">配置自定义警报和阈值与订阅通知</span><span class="sxs-lookup"><span data-stu-id="2cdbd-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="2cdbd-120">可进行筛选和转换的直观用户界面 (UI)</span><span class="sxs-lookup"><span data-stu-id="2cdbd-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="2cdbd-121">设置和查看实体依赖项和关系</span><span class="sxs-lookup"><span data-stu-id="2cdbd-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="2cdbd-122">标准和自定义实体和映射均可扩展</span><span class="sxs-lookup"><span data-stu-id="2cdbd-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="2cdbd-123">可靠的应用程序生命周期管理</span><span class="sxs-lookup"><span data-stu-id="2cdbd-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="2cdbd-124">适用于新客户的现成设置体验</span><span class="sxs-lookup"><span data-stu-id="2cdbd-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="2cdbd-125">申请</span><span class="sxs-lookup"><span data-stu-id="2cdbd-125">Application</span></span>

<span data-ttu-id="2cdbd-126">双写入在 Finance and Operations 应用中的概念与 Customer Engagement 应用中的概念之间建立映射。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="2cdbd-127">此项集成支持以下方案：</span><span class="sxs-lookup"><span data-stu-id="2cdbd-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="2cdbd-128">集成客户主数据</span><span class="sxs-lookup"><span data-stu-id="2cdbd-128">Integrated customer master</span></span>
+ <span data-ttu-id="2cdbd-129">访问客户会员卡和奖励分</span><span class="sxs-lookup"><span data-stu-id="2cdbd-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="2cdbd-130">统一的基础产品体验</span><span class="sxs-lookup"><span data-stu-id="2cdbd-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="2cdbd-131">感知组织层次结构</span><span class="sxs-lookup"><span data-stu-id="2cdbd-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="2cdbd-132">集成供应商主数据</span><span class="sxs-lookup"><span data-stu-id="2cdbd-132">Integrated vendor master</span></span>
+ <span data-ttu-id="2cdbd-133">访问财务和税务参考数据</span><span class="sxs-lookup"><span data-stu-id="2cdbd-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="2cdbd-134">按需价格引擎体验</span><span class="sxs-lookup"><span data-stu-id="2cdbd-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="2cdbd-135">集成的潜在客户到现金体验</span><span class="sxs-lookup"><span data-stu-id="2cdbd-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="2cdbd-136">通过现场代理吹内部资产和客户资产</span><span class="sxs-lookup"><span data-stu-id="2cdbd-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="2cdbd-137">集成的采购到付款体验</span><span class="sxs-lookup"><span data-stu-id="2cdbd-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="2cdbd-138">客户数据和单据的集成活动和通知单</span><span class="sxs-lookup"><span data-stu-id="2cdbd-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="2cdbd-139">查找现有库存量和详细信息</span><span class="sxs-lookup"><span data-stu-id="2cdbd-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="2cdbd-140">项目到现金体验</span><span class="sxs-lookup"><span data-stu-id="2cdbd-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="2cdbd-141">通过当事方概念处理多个地址和角色</span><span class="sxs-lookup"><span data-stu-id="2cdbd-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="2cdbd-142">针对用户的单个源管理</span><span class="sxs-lookup"><span data-stu-id="2cdbd-142">Single source management for users</span></span>
+ <span data-ttu-id="2cdbd-143">集成的零售和市场营销渠道</span><span class="sxs-lookup"><span data-stu-id="2cdbd-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="2cdbd-144">查看促销和折扣</span><span class="sxs-lookup"><span data-stu-id="2cdbd-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="2cdbd-145">请求服务功能</span><span class="sxs-lookup"><span data-stu-id="2cdbd-145">Request-for-service functions</span></span>
+ <span data-ttu-id="2cdbd-146">简化的服务操作</span><span class="sxs-lookup"><span data-stu-id="2cdbd-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="2cdbd-147">使用双写入的主要原因</span><span class="sxs-lookup"><span data-stu-id="2cdbd-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="2cdbd-148">双写入提供 Microsoft Dynamics 365 应用程序之间的数据集成。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="2cdbd-149">这个强大的框架链接了环境，并让不同业务应用程序可以一起工作。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="2cdbd-150">下面是为什么应该使用双写入的主要原因：</span><span class="sxs-lookup"><span data-stu-id="2cdbd-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="2cdbd-151">双写入提供 Finance and Operations 应用与 Dynamics 365 中的模型驱动应用之间紧密耦合的近实时双向集成。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="2cdbd-152">此集成使 Microsoft Dynamics 365 成为了所有业务解决方案的一站式商店。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="2cdbd-153">使用 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management，但对客户关系管理 (CRM) 使用非 Microsoft 解决方案的客户正在转向 Dynamics 365，以享受其双写入支持。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="2cdbd-154">客户、产品、操作、项目和物联网 (IoT) 的数据通过双写入自动流向 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="2cdbd-155">这种连接对于对 Power Platform 扩展感兴趣的企业非常有用。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="2cdbd-156">双写入基础结构遵循无代码/少代码原则。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="2cdbd-157">扩展标准表到表映射和包含自定义映射所需工程工作量非常少。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="2cdbd-158">双写入同时支持在线模式和脱机模式。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="2cdbd-159">只有 Microsoft 公司同时支持在线模式和脱机模式。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="2cdbd-160">双写入对 Customer Engagement 应用的开发人员和架构师有何意义？</span><span class="sxs-lookup"><span data-stu-id="2cdbd-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="2cdbd-161">双写入实现了 Finance and Operations 应用与 Customer Engagement 应用之间数据流自动化。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="2cdbd-162">双写入由 Common Data Service 中安装的两个 AppSource 解决方案构成。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-162">Dual-write consists of two AppSource solutions that are installed on Common Data Service.</span></span> <span data-ttu-id="2cdbd-163">这些解决方案扩展 Common Data Service 中的实体架构、插件和工作流，以使其可适应 ERP 规模。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-163">The solutions expand the entity schema, plugins, and workflows on Common Data Service so that they can scale to ERP size.</span></span> <span data-ttu-id="2cdbd-164">若要成功实施，Customer Engagement 应用的开发人员和架构师必须了解这些更改和与其对应方协作使用 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="2cdbd-165">为了创建与 Finance and Operations 应用程序之间的对等性，双写入在 Common Data Service 架构中进行一些关键更改。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Common Data Service schema.</span></span> <span data-ttu-id="2cdbd-166">如果了解此计划，可以在将来避免一些重复性的设计和开发工作。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="2cdbd-167">安装了双写入 AppSource 包之后，Common Data Service 将具有新概念，如公司和相关方。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-167">When the dual-write AppSource package is installed, Common Data Service will have new concepts such as company and party.</span></span> <span data-ttu-id="2cdbd-168">这些概念可帮助基于 Common Data Service 构建的应用程序（包括 Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service 和 Dynamics 365 Field Service）与 Finance and Operations 应用无缝交互。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-168">These concepts help applications built on Common Data Service, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="2cdbd-169">活动和通知单统一且已经过扩展，同时支持 C1（系统用户）和 C2（系统客户）。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="2cdbd-170">若要在 Finance and Operations 应用与 Common Data Service 之间传输币种时避免数据丢失，可以增加 Customer Engagement 应用中币种数据类型内的小数位数。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-170">To prevent data loss during currency transmission between Finance and Operations apps and the Common Data Service, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="2cdbd-171">此功能将现有记录自动转换为元数据层的新扩展状态。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-171">The feature autotranslates existing records to the new extended state at the metadata layer.</span></span> <span data-ttu-id="2cdbd-172">在此过程中，币种值转换为十进制数据，而不是货币数据，而货币值则支持 10 个小数位数。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="2cdbd-173">此功能是选择加入的，小数位数不需要超过 4 位的组织不需要选择加入。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="2cdbd-174">有关详细信息，请参阅[双写入货币数据类型迁移](currrency-decimal-places.md)。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="2cdbd-175">[日期有效性](../../dev-tools/date-effectivity.md)将添加到 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Common Data Service.</span></span> <span data-ttu-id="2cdbd-176">其将支持同一个实体的过去、现在和将来的数据。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="2cdbd-177">产品、报价单、订单和发票支持产品[单位转换](../../../../supply-chain/pim/tasks/manage-unit-measure.md)。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="2cdbd-178">有关即将推出的更改的详细信息，请参阅[双写入中新增或更改的功能](whats-new-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="2cdbd-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

