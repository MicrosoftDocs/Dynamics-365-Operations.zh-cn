---
title: 已删除或已弃用的平台功能
description: 本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087875"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="66ba5-103">已删除或已弃用的平台功能</span><span class="sxs-lookup"><span data-stu-id="66ba5-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66ba5-104">本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。</span><span class="sxs-lookup"><span data-stu-id="66ba5-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="66ba5-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="66ba5-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="66ba5-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="66ba5-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="66ba5-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="66ba5-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="66ba5-108">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="66ba5-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="66ba5-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="66ba5-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="66ba5-110">平台 update 32</span><span class="sxs-lookup"><span data-stu-id="66ba5-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="66ba5-111">“工作流请求更改”对话框中不再包含用户选择下拉列表</span><span class="sxs-lookup"><span data-stu-id="66ba5-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="66ba5-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="66ba5-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="66ba5-113">这是一个安全问题，因为可能会将更改请求发送给非预期用户。</span><span class="sxs-lookup"><span data-stu-id="66ba5-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="66ba5-114">这也是一个可用性问题，因为它会强制用户确定工作流发起者是谁和谁手动选择它们。</span><span class="sxs-lookup"><span data-stu-id="66ba5-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="66ba5-115">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="66ba5-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="66ba5-116">否</span><span class="sxs-lookup"><span data-stu-id="66ba5-116">No</span></span> |
| <span data-ttu-id="66ba5-117">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="66ba5-117">**Product areas affected**</span></span>         | <span data-ttu-id="66ba5-118">工作流</span><span class="sxs-lookup"><span data-stu-id="66ba5-118">Workflow</span></span> |
| <span data-ttu-id="66ba5-119">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="66ba5-119">**Deployment option**</span></span>              | <span data-ttu-id="66ba5-120">所有</span><span class="sxs-lookup"><span data-stu-id="66ba5-120">All</span></span> |
| <span data-ttu-id="66ba5-121">**状态**</span><span class="sxs-lookup"><span data-stu-id="66ba5-121">**Status**</span></span>                         | <span data-ttu-id="66ba5-122">已从平台更新 32 中的请求更改对话框内删除了用户选择下拉列表。</span><span class="sxs-lookup"><span data-stu-id="66ba5-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="66ba5-123">将把请求更改请求正常自动发送到发起者。</span><span class="sxs-lookup"><span data-stu-id="66ba5-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="66ba5-124">有关此功能的详细信息，请参阅[工作流审核流程中的操作](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)。</span><span class="sxs-lookup"><span data-stu-id="66ba5-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="66ba5-125">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="66ba5-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="66ba5-126">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="66ba5-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

