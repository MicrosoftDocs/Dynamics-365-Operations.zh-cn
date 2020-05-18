---
title: Dynamics 365 Commerce 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Commerce 中已经删除或计划删除的功能。
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335268"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="22f96-103">Dynamics 365 Commerce 中已删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="22f96-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22f96-104">本主题介绍 Dynamics 365 Commerce 中已经删除或计划删除的功能。</span><span class="sxs-lookup"><span data-stu-id="22f96-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="22f96-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="22f96-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="22f96-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="22f96-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="22f96-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="22f96-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="22f96-108">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="22f96-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="22f96-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="22f96-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="22f96-110">Commerce 10.0.10 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="22f96-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="22f96-111">POS 操作 803 - 领料和接收</span><span class="sxs-lookup"><span data-stu-id="22f96-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="22f96-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="22f96-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="22f96-113">由于重新设计了新的操作，因此不建议执行领料和接收操作。</span><span class="sxs-lookup"><span data-stu-id="22f96-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="22f96-114">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="22f96-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="22f96-115">是。</span><span class="sxs-lookup"><span data-stu-id="22f96-115">Yes.</span></span> <span data-ttu-id="22f96-116">它被以下两个新的 POS 操作取代：入站操作 (804) 和出站操作 (805)。</span><span class="sxs-lookup"><span data-stu-id="22f96-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="22f96-117">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="22f96-117">**Product areas affected**</span></span>         | <span data-ttu-id="22f96-118">销售点 (POS) 应用程序</span><span class="sxs-lookup"><span data-stu-id="22f96-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="22f96-119">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="22f96-119">**Deployment option**</span></span>              | <span data-ttu-id="22f96-120">所有</span><span class="sxs-lookup"><span data-stu-id="22f96-120">All</span></span> |
| <span data-ttu-id="22f96-121">**状态**</span><span class="sxs-lookup"><span data-stu-id="22f96-121">**Status**</span></span>                         | <span data-ttu-id="22f96-122">已弃用：从版本 10.0.10 开始，领料和接收操作将不再接收任何新功能更新。</span><span class="sxs-lookup"><span data-stu-id="22f96-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="22f96-123">在将来的版本中，将仅对此操作进行重要的 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="22f96-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="22f96-124">鼓励所有客户迁移到新的[入站操作](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)和[出站操作](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)，它们将继续成为我们长期产品路线图的一部分。</span><span class="sxs-lookup"><span data-stu-id="22f96-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="22f96-125">Commerce 10.0.7 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="22f96-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="22f96-126">Commerce GetProductAvailabilities 和 GetAvailableInventoryNearby API</span><span class="sxs-lookup"><span data-stu-id="22f96-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="22f96-127">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="22f96-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="22f96-128">已创建优化的新 API，以取代 GetProductAvailabilities 和 GetAvailableInventoryNearby API。</span><span class="sxs-lookup"><span data-stu-id="22f96-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="22f96-129">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="22f96-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="22f96-130">是：它已被 GetEstimatedAvailabilty 和 GetEstimatedProductWarehouseAvailability API 所取代。</span><span class="sxs-lookup"><span data-stu-id="22f96-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="22f96-131">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="22f96-131">**Product areas affected**</span></span>         | <span data-ttu-id="22f96-132">电子商务应用程序 SDK</span><span class="sxs-lookup"><span data-stu-id="22f96-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="22f96-133">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="22f96-133">**Deployment option**</span></span>              | <span data-ttu-id="22f96-134">所有</span><span class="sxs-lookup"><span data-stu-id="22f96-134">All</span></span> |
| <span data-ttu-id="22f96-135">**状态**</span><span class="sxs-lookup"><span data-stu-id="22f96-135">**Status**</span></span>                         | <span data-ttu-id="22f96-136">已弃用：从版本 10.0.7 开始，将不再对 GetProductAvailabilities 和 GetAvailableInventoryNearby 进行工程投资。</span><span class="sxs-lookup"><span data-stu-id="22f96-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="22f96-137">在电子商务部署中使用这些 API 的组织应转换为新的 GetEstimatedAvailabilty 和 GetEstimatedProductWarehouseAvailability API，并启用[优化的产品可用性计算功能](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels)。</span><span class="sxs-lookup"><span data-stu-id="22f96-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="22f96-138">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="22f96-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="22f96-139">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="22f96-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
