---
title: 已删除或已弃用的平台功能
description: 本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095766"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="1dc37-103">已删除或已弃用的平台功能</span><span class="sxs-lookup"><span data-stu-id="1dc37-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dc37-104">本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。</span><span class="sxs-lookup"><span data-stu-id="1dc37-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="1dc37-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="1dc37-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="1dc37-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="1dc37-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="1dc37-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="1dc37-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="1dc37-108">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1dc37-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="1dc37-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="1dc37-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="1dc37-110">平台 update 32</span><span class="sxs-lookup"><span data-stu-id="1dc37-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="1dc37-111">“工作流请求更改”对话框中不再包含用户选择下拉列表</span><span class="sxs-lookup"><span data-stu-id="1dc37-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="1dc37-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="1dc37-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="1dc37-113">这是一个安全问题，因为可能会将更改请求发送给非预期用户。</span><span class="sxs-lookup"><span data-stu-id="1dc37-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="1dc37-114">这也是一个可用性问题，因为它会强制用户确定工作流发起者是谁和谁手动选择它们。</span><span class="sxs-lookup"><span data-stu-id="1dc37-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="1dc37-115">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="1dc37-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="1dc37-116">否</span><span class="sxs-lookup"><span data-stu-id="1dc37-116">No</span></span> |
| <span data-ttu-id="1dc37-117">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="1dc37-117">**Product areas affected**</span></span>         | <span data-ttu-id="1dc37-118">工作流</span><span class="sxs-lookup"><span data-stu-id="1dc37-118">Workflow</span></span> |
| <span data-ttu-id="1dc37-119">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="1dc37-119">**Deployment option**</span></span>              | <span data-ttu-id="1dc37-120">所有</span><span class="sxs-lookup"><span data-stu-id="1dc37-120">All</span></span> |
| <span data-ttu-id="1dc37-121">**状态**</span><span class="sxs-lookup"><span data-stu-id="1dc37-121">**Status**</span></span>                         | <span data-ttu-id="1dc37-122">已从平台更新 32 中的请求更改对话框内删除了用户选择下拉列表。</span><span class="sxs-lookup"><span data-stu-id="1dc37-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="1dc37-123">将把请求更改请求正常自动发送到发起者。</span><span class="sxs-lookup"><span data-stu-id="1dc37-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="1dc37-124">有关此功能的详细信息，请参阅[工作流审核流程中的操作](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)。</span><span class="sxs-lookup"><span data-stu-id="1dc37-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a><span data-ttu-id="1dc37-125">云托管服务呈现的分页文档中将不再支持嵌入式钻取链接</span><span class="sxs-lookup"><span data-stu-id="1dc37-125">Embedded drill-through links are no longer supported in paginated documents rendered by the cloud-hosted service</span></span> 
|   |  |
|------------|--------------------|
| <span data-ttu-id="1dc37-126">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="1dc37-126">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="1dc37-127">服务呈现的文档中嵌入的导航 URL 中可能包含敏感的业务数据。</span><span class="sxs-lookup"><span data-stu-id="1dc37-127">Navigation URLs embedded in documents rendered by the service may contain sensitive business data.</span></span> <span data-ttu-id="1dc37-128">我们将取消对文档中的嵌入式钻取链接的支持，这是我们为了进一步保护客户的数据采取的安全预防措施。</span><span class="sxs-lookup"><span data-stu-id="1dc37-128">We are removing support for embedded drill-through links in documents as a security precaution to further protect customer's data.</span></span> <span data-ttu-id="1dc37-129">此项更改还将让用户在以交互方式生成文档时可以享受性能提升。</span><span class="sxs-lookup"><span data-stu-id="1dc37-129">Users will also benefit from improved performance while interactively producing documents as a result of this change.</span></span>  |
| <span data-ttu-id="1dc37-130">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="1dc37-130">**Replaced by another feature?**</span></span>   | <span data-ttu-id="1dc37-131">无</span><span class="sxs-lookup"><span data-stu-id="1dc37-131">No</span></span> |
| <span data-ttu-id="1dc37-132">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="1dc37-132">**Product areas affected**</span></span>         | <span data-ttu-id="1dc37-133">申报</span><span class="sxs-lookup"><span data-stu-id="1dc37-133">Reporting</span></span> |
| <span data-ttu-id="1dc37-134">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="1dc37-134">**Deployment option**</span></span>              | <span data-ttu-id="1dc37-135">所有</span><span class="sxs-lookup"><span data-stu-id="1dc37-135">All</span></span> |
| <span data-ttu-id="1dc37-136">**状态**</span><span class="sxs-lookup"><span data-stu-id="1dc37-136">**Status**</span></span>                         | <span data-ttu-id="1dc37-137">正在从服务中努力移除此功能。</span><span class="sxs-lookup"><span data-stu-id="1dc37-137">This feature is actively being removed from the service.</span></span><br><br><span data-ttu-id="1dc37-138">现代客户端提供大量选项，用于生成其中包含自动生成的链接的视图，以便帮助您在应用程序中导航。</span><span class="sxs-lookup"><span data-stu-id="1dc37-138">The modern client offers numerous options for producing views that include auto-generated links to assist in navigating the application.</span></span> <span data-ttu-id="1dc37-139">将为收件人推荐通过电子邮件发送，归档和打印的外部通信使用服务呈现的分页文档。</span><span class="sxs-lookup"><span data-stu-id="1dc37-139">Paginated documents rendered by the service are recommended for external communications that are emailed, archived, and printed for recipients.</span></span> <span data-ttu-id="1dc37-140">我们改进了直接在浏览器中预览文档的体验，可以直接访问本地打印机。</span><span class="sxs-lookup"><span data-stu-id="1dc37-140">We have improved the experience for previewing documents directly in the browser, which offers direct access to local printers.</span></span> <span data-ttu-id="1dc37-141">有关详细信息，请参阅[使用嵌入式查看器预览 PDF 文档](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents)。</span><span class="sxs-lookup"><span data-stu-id="1dc37-141">For more information, see [Preview PDF documents with an embedded viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="1dc37-142">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="1dc37-142">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="1dc37-143">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="1dc37-143">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

