---
title: Dynamics 365 Supply Chain Management 10.0.6（2019 年 11 月）中的新增功能或更改
description: 此主题介绍了 Dynamics 365 Supply Chain Management 10.0.6 中的新增功能或更改的功能。
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: f253355b3de4f148c11b1d9d3f43b6756e6bd38c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983667"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="e585a-103">Dynamics 365 Supply Chain Management 10.0.6（2019 年 11 月）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="e585a-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e585a-104">此主题介绍了 Microsoft Dynamics 365 Supply Chain Management 10.0.6 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="e585a-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="e585a-105">此版本的内部版本号为 10.0.234。</span><span class="sxs-lookup"><span data-stu-id="e585a-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="e585a-106">虽然公开发布日期在 11 月，新增功能在 10 月的提前版本中就已提供。</span><span class="sxs-lookup"><span data-stu-id="e585a-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="e585a-107">有关版本 10.0.6 的详细信息，请参阅[其他资源](whats-new-scm-10-0-6.md#additional-resources)。</span><span class="sxs-lookup"><span data-stu-id="e585a-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="e585a-108">产品配置模型 V2 data 数据实体</span><span class="sxs-lookup"><span data-stu-id="e585a-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="e585a-109">已发布了“产品配置模型”数据实体的第二个版本（称为“产品配置模型 V2”）。</span><span class="sxs-lookup"><span data-stu-id="e585a-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="e585a-110">还需要有默认模板“418 - 产品配置模型”，这样才能在导入/导出框架模板中使用新增的“产品配置模型 V2”数据实体。</span><span class="sxs-lookup"><span data-stu-id="e585a-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="e585a-111">不会自动更新此模板，所以您必须手动从默认位置加载该模板。</span><span class="sxs-lookup"><span data-stu-id="e585a-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="e585a-112">V2 实体将一行作为附件中的一个单独文件导出，而不是以内联方式导出，从而解决了 V1 实体的大小限制问题。</span><span class="sxs-lookup"><span data-stu-id="e585a-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="e585a-113">若要采用此更新，需要执行什么操作？</span><span class="sxs-lookup"><span data-stu-id="e585a-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="e585a-114">因为 V1 实体已弃用，所以您应该从 V1 迁移到 V2。</span><span class="sxs-lookup"><span data-stu-id="e585a-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="e585a-115">如果您在使用“418 - 产品配置模型”模板，可以单击“加载默认模板”按钮并重新加载“418 – 产品配置模型”</span><span class="sxs-lookup"><span data-stu-id="e585a-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="e585a-116">如果您需要保持与现有系统兼容，您可以暂时继续使用现有模板和（已弃用的）V1 实体，直到将您的集成移到新模板。</span><span class="sxs-lookup"><span data-stu-id="e585a-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="e585a-117">功能管理增强功能</span><span class="sxs-lookup"><span data-stu-id="e585a-117">Feature management enhancements</span></span>
<span data-ttu-id="e585a-118">功能管理现在允许默认启用所有新功能，要求执行功能确认和启用尚未启用的所有功能。</span><span class="sxs-lookup"><span data-stu-id="e585a-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="e585a-119">采购协议负责方</span><span class="sxs-lookup"><span data-stu-id="e585a-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="e585a-120">现在可以在采购协议分类窗体和生成的采购协议中定义主负责方和副负责方。</span><span class="sxs-lookup"><span data-stu-id="e585a-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="e585a-121">这使用户可以访问协议的监督者。</span><span class="sxs-lookup"><span data-stu-id="e585a-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="e585a-122">采购订单行中的 RFQ 链接</span><span class="sxs-lookup"><span data-stu-id="e585a-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="e585a-123">可以将采购订单行中的引用链接添加回其对应的来源 RFQ 行，从而轻松地为用户提供询价单支持。</span><span class="sxs-lookup"><span data-stu-id="e585a-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e585a-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="e585a-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e585a-125">缺陷修复</span><span class="sxs-lookup"><span data-stu-id="e585a-125">Bug fixes</span></span>
<span data-ttu-id="e585a-126">有关 10.0.6 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7)。</span><span class="sxs-lookup"><span data-stu-id="e585a-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="e585a-127">平台 update 30</span><span class="sxs-lookup"><span data-stu-id="e585a-127">Platform update 30</span></span>
<span data-ttu-id="e585a-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 中包含平台更新 30。</span><span class="sxs-lookup"><span data-stu-id="e585a-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="e585a-129">若要了解有关平台更新 30 的详细信息，请参阅[平台更新 30 中的新增功能或更改的功能](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md)。</span><span class="sxs-lookup"><span data-stu-id="e585a-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="e585a-130">Dynamics 365：2019 发布波次 2 计划</span><span class="sxs-lookup"><span data-stu-id="e585a-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="e585a-131">是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？</span><span class="sxs-lookup"><span data-stu-id="e585a-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="e585a-132">查看 [Dynamics 365：2019 发布波次 2 计划](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/)。</span><span class="sxs-lookup"><span data-stu-id="e585a-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="e585a-133">一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。</span><span class="sxs-lookup"><span data-stu-id="e585a-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="e585a-134">已删除和已弃用的 Supply Chain Management 功能</span><span class="sxs-lookup"><span data-stu-id="e585a-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="e585a-135">[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题介绍 Supply Chain Management 中已经或计划删除或弃用的功能。</span><span class="sxs-lookup"><span data-stu-id="e585a-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="e585a-136">*已移除* 的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="e585a-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="e585a-137">*已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="e585a-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="e585a-138">从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题中发布弃用通知。</span><span class="sxs-lookup"><span data-stu-id="e585a-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="e585a-139">对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="e585a-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="e585a-140">通常是需要对编译器进行的功能更新。</span><span class="sxs-lookup"><span data-stu-id="e585a-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
