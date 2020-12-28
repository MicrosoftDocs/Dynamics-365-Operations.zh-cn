---
title: 升级和迁移到高级仓库管理疑难解答
description: 此主题介绍如何解决升级和迁移到高级仓库管理时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645809"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>升级和迁移到高级仓库管理疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决升级和迁移到高级仓库管理时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>我收到以下错误消息：“java.security.cert.certPathValidatorException：未找到认证路径的信任锚。”

### <a name="issue-description"></a>问题描述

您在仓库应用中收到此错误消息，是因为自签名证书在本地环境中的 Android 8+ 上不受信任。

### <a name="issue-resolution"></a>解决问题

请使用外部（公共）认证机构 (CA)。 仓库应用版本 1.9.0.0 中提供了针对此问题的修复。 有关此问题以及如何解决的详细信息，请参阅[解决仓库应用的连接问题](troubleshoot-warehouse-app-connection.md)。

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>批准的从基本仓库移到高级仓库的流程是什么？

### <a name="issue-description"></a>问题描述

您当前是在存货/库存管理下运行，使用的是基本存货功能，您希望转移到高级仓库以利用移动设备、波次和工作。 但是，您尝试移动时遇到了问题。 例如，您不能更改产品，让其使用存储维度（站点、仓库和位置），因为产品本身有交易。 因此，您必须了解批准的从基本仓库移到高级仓库的流程。

### <a name="issue-resolution"></a>解决问题

有关从基本仓库移到高级仓库的流程的详细信息，请参阅以下博客文章和文档：

- [为现有物料和仓库启用仓库管理流程](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [将 Microsoft Dynamics AX WMS 迁移到新的 R3 仓库和运输功能](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 物料迁移](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [将仓库管理从 Microsoft Dynamics AX 2012 升级到 Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
