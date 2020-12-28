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
ms.openlocfilehash: 85530cf644c7b7ffe922a6fb3288f4e05c5df91c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685605"
---
# <a name="dual-write-overview"></a><span data-ttu-id="5a5db-104">双写入概述</span><span class="sxs-lookup"><span data-stu-id="5a5db-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="5a5db-105">什么是双写入？</span><span class="sxs-lookup"><span data-stu-id="5a5db-105">What is dual-write?</span></span>

<span data-ttu-id="5a5db-106">双写入是一种自带基础结构，其提供 Customer Engagement 应用与 Finance and Operations 应用之间的近实时交互。</span><span class="sxs-lookup"><span data-stu-id="5a5db-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="5a5db-107">当有关客户、产品、人员和操作的数据越过应用程序边界时，将为组织中的所有部门授权。</span><span class="sxs-lookup"><span data-stu-id="5a5db-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="5a5db-108">双写入提供 Finance and Operations 应用与 Dataverse 之间紧密耦合的双向集成。</span><span class="sxs-lookup"><span data-stu-id="5a5db-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="5a5db-109">Finance and Operations 应用中的所有数据变化都会写入 Dataverse，而 Dataverse 中的所有数据变化也会导致写入 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="5a5db-109">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="5a5db-110">这个自动化的数据流提供了应用之间的集成用户体验。</span><span class="sxs-lookup"><span data-stu-id="5a5db-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![应用之间的数据关系](media/dual-write-overview.jpg)

<span data-ttu-id="5a5db-112">双写入有两个方面：*基础结构* 方面和 *应用程序* 方面。</span><span class="sxs-lookup"><span data-stu-id="5a5db-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="5a5db-113">基础结构</span><span class="sxs-lookup"><span data-stu-id="5a5db-113">Infrastructure</span></span>

<span data-ttu-id="5a5db-114">双写入基础结构可扩展且可靠，并且具有以下关键功能：</span><span class="sxs-lookup"><span data-stu-id="5a5db-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="5a5db-115">应用程序之间的同步和双向数据流</span><span class="sxs-lookup"><span data-stu-id="5a5db-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="5a5db-116">同步和播放、暂停与继续模式，用于在联机和脱机/异步模式下共同为系统提供支持。</span><span class="sxs-lookup"><span data-stu-id="5a5db-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="5a5db-117">在应用程序之间同步初始数据</span><span class="sxs-lookup"><span data-stu-id="5a5db-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="5a5db-118">适用于数据管理员的，合并的活动与错误日志视图</span><span class="sxs-lookup"><span data-stu-id="5a5db-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="5a5db-119">配置自定义警报和阈值与订阅通知</span><span class="sxs-lookup"><span data-stu-id="5a5db-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="5a5db-120">可进行筛选和转换的直观用户界面 (UI)</span><span class="sxs-lookup"><span data-stu-id="5a5db-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="5a5db-121">设置和查看实体依赖项和关系</span><span class="sxs-lookup"><span data-stu-id="5a5db-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="5a5db-122">标准和自定义表和映射均可扩展</span><span class="sxs-lookup"><span data-stu-id="5a5db-122">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="5a5db-123">可靠的应用程序生命周期管理</span><span class="sxs-lookup"><span data-stu-id="5a5db-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="5a5db-124">适用于新客户的现成设置体验</span><span class="sxs-lookup"><span data-stu-id="5a5db-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="5a5db-125">申请</span><span class="sxs-lookup"><span data-stu-id="5a5db-125">Application</span></span>

<span data-ttu-id="5a5db-126">双写入在 Finance and Operations 应用中的概念与 Customer Engagement 应用中的概念之间建立映射。</span><span class="sxs-lookup"><span data-stu-id="5a5db-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="5a5db-127">此项集成支持以下方案：</span><span class="sxs-lookup"><span data-stu-id="5a5db-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="5a5db-128">集成客户主数据</span><span class="sxs-lookup"><span data-stu-id="5a5db-128">Integrated customer master</span></span>
+ <span data-ttu-id="5a5db-129">访问客户会员卡和奖励分</span><span class="sxs-lookup"><span data-stu-id="5a5db-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="5a5db-130">统一的基础产品体验</span><span class="sxs-lookup"><span data-stu-id="5a5db-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="5a5db-131">感知组织层次结构</span><span class="sxs-lookup"><span data-stu-id="5a5db-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="5a5db-132">集成供应商主数据</span><span class="sxs-lookup"><span data-stu-id="5a5db-132">Integrated vendor master</span></span>
+ <span data-ttu-id="5a5db-133">访问财务和税务参考数据</span><span class="sxs-lookup"><span data-stu-id="5a5db-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="5a5db-134">按需价格引擎体验</span><span class="sxs-lookup"><span data-stu-id="5a5db-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="5a5db-135">集成的潜在客户到现金体验</span><span class="sxs-lookup"><span data-stu-id="5a5db-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="5a5db-136">通过现场代理吹内部资产和客户资产</span><span class="sxs-lookup"><span data-stu-id="5a5db-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="5a5db-137">集成的采购到付款体验</span><span class="sxs-lookup"><span data-stu-id="5a5db-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="5a5db-138">客户数据和单据的集成活动和通知单</span><span class="sxs-lookup"><span data-stu-id="5a5db-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="5a5db-139">查找现有库存量和详细信息</span><span class="sxs-lookup"><span data-stu-id="5a5db-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="5a5db-140">项目到现金体验</span><span class="sxs-lookup"><span data-stu-id="5a5db-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="5a5db-141">通过当事方概念处理多个地址和角色</span><span class="sxs-lookup"><span data-stu-id="5a5db-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="5a5db-142">针对用户的单个源管理</span><span class="sxs-lookup"><span data-stu-id="5a5db-142">Single source management for users</span></span>
+ <span data-ttu-id="5a5db-143">集成的零售和市场营销渠道</span><span class="sxs-lookup"><span data-stu-id="5a5db-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="5a5db-144">查看促销和折扣</span><span class="sxs-lookup"><span data-stu-id="5a5db-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="5a5db-145">请求服务功能</span><span class="sxs-lookup"><span data-stu-id="5a5db-145">Request-for-service functions</span></span>
+ <span data-ttu-id="5a5db-146">简化的服务操作</span><span class="sxs-lookup"><span data-stu-id="5a5db-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="5a5db-147">使用双写入的主要原因</span><span class="sxs-lookup"><span data-stu-id="5a5db-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="5a5db-148">双写入提供 Microsoft Dynamics 365 应用程序之间的数据集成。</span><span class="sxs-lookup"><span data-stu-id="5a5db-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="5a5db-149">这个强大的框架链接了环境，并让不同业务应用程序可以一起工作。</span><span class="sxs-lookup"><span data-stu-id="5a5db-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="5a5db-150">下面是为什么应该使用双写入的主要原因：</span><span class="sxs-lookup"><span data-stu-id="5a5db-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="5a5db-151">双写入提供 Finance and Operations 应用与 Dynamics 365 中的模型驱动应用之间紧密耦合的近实时双向集成。</span><span class="sxs-lookup"><span data-stu-id="5a5db-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="5a5db-152">此集成使 Microsoft Dynamics 365 成为了所有业务解决方案的一站式商店。</span><span class="sxs-lookup"><span data-stu-id="5a5db-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="5a5db-153">使用 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management，但对客户关系管理 (CRM) 使用非 Microsoft 解决方案的客户正在转向 Dynamics 365，以享受其双写入支持。</span><span class="sxs-lookup"><span data-stu-id="5a5db-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="5a5db-154">客户、产品、操作、项目和物联网 (IoT) 的数据通过双写入自动流向 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="5a5db-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="5a5db-155">这种连接对于对 Power Platform 扩展感兴趣的企业非常有用。</span><span class="sxs-lookup"><span data-stu-id="5a5db-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="5a5db-156">双写入基础结构遵循无代码/少代码原则。</span><span class="sxs-lookup"><span data-stu-id="5a5db-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="5a5db-157">扩展标准表到表映射和包含自定义映射所需工程工作量非常少。</span><span class="sxs-lookup"><span data-stu-id="5a5db-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="5a5db-158">双写入同时支持在线模式和脱机模式。</span><span class="sxs-lookup"><span data-stu-id="5a5db-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="5a5db-159">只有 Microsoft 公司同时支持在线模式和脱机模式。</span><span class="sxs-lookup"><span data-stu-id="5a5db-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="5a5db-160">双写入对 Customer Engagement 应用的开发人员和架构师有何意义？</span><span class="sxs-lookup"><span data-stu-id="5a5db-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="5a5db-161">双写入实现了 Finance and Operations 应用与 Customer Engagement 应用之间数据流自动化。</span><span class="sxs-lookup"><span data-stu-id="5a5db-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="5a5db-162">双写入由 Dataverse 中安装的两个 AppSource 解决方案构成。</span><span class="sxs-lookup"><span data-stu-id="5a5db-162">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="5a5db-163">这些解决方案扩展 Dataverse 中的实体架构、插件和工作流，以使其可适应 ERP 规模。</span><span class="sxs-lookup"><span data-stu-id="5a5db-163">The solutions expand the entity schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="5a5db-164">若要成功实施，Customer Engagement 应用的开发人员和架构师必须了解这些更改和与其对应方协作使用 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="5a5db-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="5a5db-165">为了创建与 Finance and Operations 应用程序之间的对等性，双写入在 Dataverse 架构中进行一些关键更改。</span><span class="sxs-lookup"><span data-stu-id="5a5db-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="5a5db-166">如果了解此计划，可以在将来避免一些重复性的设计和开发工作。</span><span class="sxs-lookup"><span data-stu-id="5a5db-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="5a5db-167">安装了双写入 AppSource 包之后，Dataverse 将具有新概念，如公司和相关方。</span><span class="sxs-lookup"><span data-stu-id="5a5db-167">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="5a5db-168">这些概念可帮助基于 Dataverse 构建的应用程序（包括 Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service 和 Dynamics 365 Field Service）与 Finance and Operations 应用无缝交互。</span><span class="sxs-lookup"><span data-stu-id="5a5db-168">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="5a5db-169">活动和通知单统一且已经过扩展，同时支持 C1（系统用户）和 C2（系统客户）。</span><span class="sxs-lookup"><span data-stu-id="5a5db-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="5a5db-170">若要在 Finance and Operations 应用与 Dataverse 之间传输币种时避免数据丢失，可以增加 Customer Engagement 应用中币种数据类型内的小数位数。</span><span class="sxs-lookup"><span data-stu-id="5a5db-170">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="5a5db-171">此功能将现有行自动转换为元数据层的新扩展状态。</span><span class="sxs-lookup"><span data-stu-id="5a5db-171">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="5a5db-172">在此过程中，币种值转换为十进制数据，而不是货币数据，而货币值则支持 10 个小数位数。</span><span class="sxs-lookup"><span data-stu-id="5a5db-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="5a5db-173">此功能是选择加入的，小数位数不需要超过 4 位的组织不需要选择加入。</span><span class="sxs-lookup"><span data-stu-id="5a5db-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="5a5db-174">有关详细信息，请参阅[双写入货币数据类型迁移](currrency-decimal-places.md)。</span><span class="sxs-lookup"><span data-stu-id="5a5db-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="5a5db-175">[日期有效性](../../dev-tools/date-effectivity.md)将添加到 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="5a5db-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="5a5db-176">其将支持同一个实体的过去、现在和将来的数据。</span><span class="sxs-lookup"><span data-stu-id="5a5db-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="5a5db-177">产品、报价单、订单和发票支持产品[单位转换](../../../../supply-chain/pim/tasks/manage-unit-measure.md)。</span><span class="sxs-lookup"><span data-stu-id="5a5db-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="5a5db-178">有关即将推出的更改的详细信息，请参阅[双写入中新增或更改的功能](whats-new-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="5a5db-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

