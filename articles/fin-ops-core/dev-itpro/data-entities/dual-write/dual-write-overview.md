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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172776"
---
# <a name="dual-write-overview"></a><span data-ttu-id="6c3c6-104">双写入概述</span><span class="sxs-lookup"><span data-stu-id="6c3c6-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="6c3c6-105">什么是双写入？</span><span class="sxs-lookup"><span data-stu-id="6c3c6-105">What is dual-write?</span></span>

<span data-ttu-id="6c3c6-106">双写入是一种自带基础结构，其提供 Microsoft Dynamics 365 中的模型驱动应用与 Finance and Operations 应用之间的近实时交互。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="6c3c6-107">当有关客户、产品、人员和操作的数据越过应用程序边界时，将为组织中的所有部门授权。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="6c3c6-108">双写入提供 Finance and Operations 应用与 Common Data Service 之间紧密耦合的双向集成。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="6c3c6-109">Finance and Operations 应用中的所有数据变化都会写入 Common Data Service，而 Common Data Service 中的所有数据变化也会导致写入 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="6c3c6-110">这个自动化的数据流提供了应用之间的集成用户体验。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![应用之间的数据关系](media/dual-write-overview.jpg)

<span data-ttu-id="6c3c6-112">双写入有两个方面：*基础结构*方面和*应用程序*方面。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="6c3c6-113">基础结构</span><span class="sxs-lookup"><span data-stu-id="6c3c6-113">Infrastructure</span></span>

<span data-ttu-id="6c3c6-114">双写入基础结构可扩展且可靠，并且具有以下关键功能：</span><span class="sxs-lookup"><span data-stu-id="6c3c6-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="6c3c6-115">应用程序之间的同步和双向数据流</span><span class="sxs-lookup"><span data-stu-id="6c3c6-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="6c3c6-116">同步和播放、暂停与继续模式，用于在联机和脱机/异步模式下共同为系统提供支持。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="6c3c6-117">在应用程序之间同步初始数据</span><span class="sxs-lookup"><span data-stu-id="6c3c6-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="6c3c6-118">适用于数据管理员的，合并的活动与错误日志视图</span><span class="sxs-lookup"><span data-stu-id="6c3c6-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="6c3c6-119">配置自定义警报和阈值与订阅通知</span><span class="sxs-lookup"><span data-stu-id="6c3c6-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="6c3c6-120">可进行筛选和转换的直观用户界面 (UI)</span><span class="sxs-lookup"><span data-stu-id="6c3c6-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="6c3c6-121">设置和查看实体依赖项和关系</span><span class="sxs-lookup"><span data-stu-id="6c3c6-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="6c3c6-122">标准和自定义实体和映射均可扩展</span><span class="sxs-lookup"><span data-stu-id="6c3c6-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="6c3c6-123">可靠的应用程序生命周期管理</span><span class="sxs-lookup"><span data-stu-id="6c3c6-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="6c3c6-124">适用于新客户的现成设置体验</span><span class="sxs-lookup"><span data-stu-id="6c3c6-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="6c3c6-125">申请</span><span class="sxs-lookup"><span data-stu-id="6c3c6-125">Application</span></span>

<span data-ttu-id="6c3c6-126">双写入在 Finance and Operations 应用中的概念与 Dynamics 365 中模型驱动应用中的概念之间建立映射。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="6c3c6-127">此项集成支持以下方案：</span><span class="sxs-lookup"><span data-stu-id="6c3c6-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="6c3c6-128">集成客户主数据</span><span class="sxs-lookup"><span data-stu-id="6c3c6-128">Integrated customer master</span></span>
+ <span data-ttu-id="6c3c6-129">访问客户会员卡和奖励分</span><span class="sxs-lookup"><span data-stu-id="6c3c6-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="6c3c6-130">统一的基础产品体验</span><span class="sxs-lookup"><span data-stu-id="6c3c6-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="6c3c6-131">感知组织层次结构</span><span class="sxs-lookup"><span data-stu-id="6c3c6-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="6c3c6-132">集成供应商主数据</span><span class="sxs-lookup"><span data-stu-id="6c3c6-132">Integrated vendor master</span></span>
+ <span data-ttu-id="6c3c6-133">访问财务和税务参考数据</span><span class="sxs-lookup"><span data-stu-id="6c3c6-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="6c3c6-134">按需价格引擎体验</span><span class="sxs-lookup"><span data-stu-id="6c3c6-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="6c3c6-135">集成的潜在客户到现金体验</span><span class="sxs-lookup"><span data-stu-id="6c3c6-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="6c3c6-136">通过现场代理吹内部资产和客户资产</span><span class="sxs-lookup"><span data-stu-id="6c3c6-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="6c3c6-137">集成的采购到付款体验</span><span class="sxs-lookup"><span data-stu-id="6c3c6-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="6c3c6-138">客户数据和单据的集成活动和通知单</span><span class="sxs-lookup"><span data-stu-id="6c3c6-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="6c3c6-139">查找现有库存量和详细信息</span><span class="sxs-lookup"><span data-stu-id="6c3c6-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="6c3c6-140">项目到现金体验</span><span class="sxs-lookup"><span data-stu-id="6c3c6-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="6c3c6-141">通过当事方概念处理多个地址和角色</span><span class="sxs-lookup"><span data-stu-id="6c3c6-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="6c3c6-142">针对用户的单个源管理</span><span class="sxs-lookup"><span data-stu-id="6c3c6-142">Single source management for users</span></span>
+ <span data-ttu-id="6c3c6-143">集成的零售和市场营销渠道</span><span class="sxs-lookup"><span data-stu-id="6c3c6-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="6c3c6-144">查看促销和折扣</span><span class="sxs-lookup"><span data-stu-id="6c3c6-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="6c3c6-145">请求服务功能</span><span class="sxs-lookup"><span data-stu-id="6c3c6-145">Request-for-service functions</span></span>
+ <span data-ttu-id="6c3c6-146">简化的服务操作</span><span class="sxs-lookup"><span data-stu-id="6c3c6-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="6c3c6-147">使用双写入的主要原因</span><span class="sxs-lookup"><span data-stu-id="6c3c6-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="6c3c6-148">双写入提供 Microsoft Dynamics 365 应用程序之间的数据集成。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="6c3c6-149">这个强大的框架链接了环境，并让不同业务应用程序可以一起工作。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="6c3c6-150">下面是为什么应该使用双写入的主要原因：</span><span class="sxs-lookup"><span data-stu-id="6c3c6-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="6c3c6-151">双写入提供 Finance and Operations 应用与 Dynamics 365 中的模型驱动应用之间紧密耦合的近实时双向集成。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="6c3c6-152">此集成使 Microsoft Dynamics 365 成为了所有业务解决方案的一站式商店。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="6c3c6-153">使用 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management，但对客户关系管理 (CRM) 使用非 Microsoft 解决方案的客户正在转向 Dynamics 365，以享受其双写入支持。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="6c3c6-154">客户、产品、操作、项目和物联网 (IoT) 的数据通过双写入自动流向 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="6c3c6-155">这种连接对于对 Microsoft Power Platform 扩展感兴趣的企业非常有用。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="6c3c6-156">双写入基础结构遵循无代码/少代码原则。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="6c3c6-157">扩展标准表到表映射和包含自定义映射所需工程工作量非常少。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="6c3c6-158">双写入同时支持在线模式和脱机模式。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="6c3c6-159">只有 Microsoft 公司同时支持在线模式和脱机模式。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="6c3c6-160">双写入对 CRM 产品的用户和架构师有何意义？</span><span class="sxs-lookup"><span data-stu-id="6c3c6-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="6c3c6-161">双写入实现了 Finance and Operations 应用与 Common Data Service 之间数据流自动化。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="6c3c6-162">在将来的版本中，Dynamics 365 中的模型驱动应用内的概念（如客户、联系人、报价单和订单）将延伸到中端市场和中高端市场客户。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="6c3c6-163">在第一个版本中，大多数自动化由双写入解决方案处理。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="6c3c6-164">在将来的版本中，这些解决方案将成为 Common Data Service 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="6c3c6-165">了解到即将推出的 Common Data Service 更改，可以长期节约工作量。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="6c3c6-166">下面是一些关键更改：</span><span class="sxs-lookup"><span data-stu-id="6c3c6-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="6c3c6-167">Common Data Service 将采用新概念，如公司和当事方。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="6c3c6-168">这些概念将影响基于 Common Data Service 创建的所有应用，如 Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service 和 Dynamics 365 Field Service。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="6c3c6-169">活动和通知单统一且已经过扩展，同时支持 C1（系统用户）和 C2（系统客户）。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="6c3c6-170">下面是 Common Data Service 中即将推出的一些更改：</span><span class="sxs-lookup"><span data-stu-id="6c3c6-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="6c3c6-171">十进制数据类型将取代金钱数据类型。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="6c3c6-172">日期有效性将在同一个位置支持过去、现在和将来的数据。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="6c3c6-173">将提供更多对货币和汇率的支持，并且将修订**汇率**应用程序编程接口 (API)。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="6c3c6-174">将支持单位转换。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="6c3c6-175">有关即将推出的更改的详细信息，请参阅 [Common Data Service 中的数据 – 阶段 1 和 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1)。</span><span class="sxs-lookup"><span data-stu-id="6c3c6-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>
