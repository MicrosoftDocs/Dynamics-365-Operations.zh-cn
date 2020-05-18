---
title: Dynamics 365 Supply Chain Management 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Supply Chain Management 中已经删除或计划删除的功能。
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331240"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="614bf-103">Dynamics 365 Supply Chain Management 中已删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="614bf-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="614bf-104">随着记录 Dynamics 365 Supply Chain Management 的已删除或已弃用功能，将更新此主题。</span><span class="sxs-lookup"><span data-stu-id="614bf-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="614bf-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="614bf-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="614bf-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="614bf-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="614bf-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="614bf-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="614bf-108">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="614bf-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="614bf-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="614bf-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="614bf-110">Supply Chain Management 10.0.11 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="614bf-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="614bf-111">将内置的 Supply Chain Management 主计划引擎用于分发方案</span><span class="sxs-lookup"><span data-stu-id="614bf-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="614bf-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="614bf-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="614bf-113">为了在主计划运行期间提高性能并最大限度减小 SQL 数据库负荷，Planning Optimization 已取代了内置的 Supply Chain Management 主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="614bf-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="614bf-114">通过 Planning Optimization，即使在办公时间也可以执行快速计划运行。</span><span class="sxs-lookup"><span data-stu-id="614bf-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="614bf-115">这使计划人员可以立即对需求或计划参数的变化做出反应。</span><span class="sxs-lookup"><span data-stu-id="614bf-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="614bf-116">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="614bf-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="614bf-117">是的，Planning Optimization 将取代现有的内置 Supply Chain Management 主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="614bf-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="614bf-118">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="614bf-118">**Product areas affected**</span></span>         | <span data-ttu-id="614bf-119">Supply Chain Management - 主计划</span><span class="sxs-lookup"><span data-stu-id="614bf-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="614bf-120">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="614bf-120">**Deployment option**</span></span>              | <span data-ttu-id="614bf-121">仅限云。</span><span class="sxs-lookup"><span data-stu-id="614bf-121">Cloud only.</span></span> <span data-ttu-id="614bf-122">本地部署不支持 Planning Optimization。</span><span class="sxs-lookup"><span data-stu-id="614bf-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="614bf-123">**状态**</span><span class="sxs-lookup"><span data-stu-id="614bf-123">**Status**</span></span>                         | <span data-ttu-id="614bf-124">已弃用。</span><span class="sxs-lookup"><span data-stu-id="614bf-124">Deprecated.</span></span> <span data-ttu-id="614bf-125">自 2021 年 4 月起，内置的 Dynamics 365 Supply Chain Management 主计划引擎将不再支持分发方案。</span><span class="sxs-lookup"><span data-stu-id="614bf-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="614bf-126">对于分发方案，客户必须将 Planning Optimization 用于主计划计算。</span><span class="sxs-lookup"><span data-stu-id="614bf-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="614bf-127">有关详细信息，请参阅 [Planning Optimization 文档](https://go.microsoft.com/fwlink/?linkid=2105830)。</span><span class="sxs-lookup"><span data-stu-id="614bf-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="614bf-128">在 2021 年 4 月之后，在本地部署 Dynamics 365 Supply Chain Management 的客户可以继续将 Supply Chain Management 主计划引擎用于分发方案。</span><span class="sxs-lookup"><span data-stu-id="614bf-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="614bf-129">但是，将不再提供其他功能增强。</span><span class="sxs-lookup"><span data-stu-id="614bf-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="614bf-130">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="614bf-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="614bf-131">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="614bf-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
