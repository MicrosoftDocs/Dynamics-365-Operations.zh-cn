---
title: 升级和迁移到高级仓库管理疑难解答
description: 此主题介绍如何解决升级和迁移到高级仓库管理时可能遇到的常见问题。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907879"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="811c8-103">升级和迁移到高级仓库管理疑难解答</span><span class="sxs-lookup"><span data-stu-id="811c8-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="811c8-104">此主题介绍如何解决升级和迁移到高级仓库管理时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="811c8-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="811c8-105">我收到以下错误消息：“java.security.cert.certPathValidatorException：未找到认证路径的信任锚。”</span><span class="sxs-lookup"><span data-stu-id="811c8-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="811c8-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="811c8-106">Issue description</span></span>

<span data-ttu-id="811c8-107">您会在仓库管理移动应用中收到此错误消息，因为自签名证书在本地环境中的 Android 8+ 上不受信任。</span><span class="sxs-lookup"><span data-stu-id="811c8-107">You receive this error message in the Warehouse Management mobile app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="811c8-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="811c8-108">Issue resolution</span></span>

<span data-ttu-id="811c8-109">请使用外部（公共）认证机构 (CA)。</span><span class="sxs-lookup"><span data-stu-id="811c8-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="811c8-110">仓库应用版本 1.9.0.0 中提供了针对此问题的修复。</span><span class="sxs-lookup"><span data-stu-id="811c8-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="811c8-111">有关此问题以及如何解决的详细信息，请参阅[仓库管理移动应用连接问题故障排除](troubleshoot-warehouse-app-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="811c8-111">For more information about this issue and how to fix it, see [Troubleshoot Warehouse Management mobile app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="811c8-112">批准的从基本仓库移到高级仓库的流程是什么？</span><span class="sxs-lookup"><span data-stu-id="811c8-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="811c8-113">问题描述</span><span class="sxs-lookup"><span data-stu-id="811c8-113">Issue description</span></span>

<span data-ttu-id="811c8-114">您当前是在存货/库存管理下运行，使用的是基本存货功能，您希望转移到高级仓库以利用移动设备、波次和工作。</span><span class="sxs-lookup"><span data-stu-id="811c8-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="811c8-115">但是，您尝试移动时遇到了问题。</span><span class="sxs-lookup"><span data-stu-id="811c8-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="811c8-116">例如，您不能更改产品，让其使用存储维度（站点、仓库和位置），因为产品本身有交易。</span><span class="sxs-lookup"><span data-stu-id="811c8-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="811c8-117">因此，您必须了解批准的从基本仓库移到高级仓库的流程。</span><span class="sxs-lookup"><span data-stu-id="811c8-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="811c8-118">解决问题</span><span class="sxs-lookup"><span data-stu-id="811c8-118">Issue resolution</span></span>

<span data-ttu-id="811c8-119">有关从基本仓库移到高级仓库的流程的详细信息，请参阅以下博客文章和文档：</span><span class="sxs-lookup"><span data-stu-id="811c8-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="811c8-120">为现有物料和仓库启用仓库管理流程</span><span class="sxs-lookup"><span data-stu-id="811c8-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="811c8-121">将 Microsoft Dynamics AX WMS 迁移到新的 R3 仓库和运输功能</span><span class="sxs-lookup"><span data-stu-id="811c8-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="811c8-122">WMSI/WMS2 物料迁移</span><span class="sxs-lookup"><span data-stu-id="811c8-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="811c8-123">将仓库管理从 Microsoft Dynamics AX 2012 升级到 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="811c8-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]