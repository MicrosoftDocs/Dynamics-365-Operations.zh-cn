---
title: 升级或迁移到 WMS 时发生认证路径错误
description: 如果在升级或迁移到 WMS 时应用显示“找不到认证路径的信任锚”错误，本页面提供有关如何解决此问题的信息。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475662"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>更新和迁移到 WMS 时找不到认证路径的信任锚

## <a name="symptoms"></a>故障特征

升级和迁移到高级仓库管理 (WMS) 时，Warehouse Management 应用可能会显示以下错误消息：

> “java.security.cert.certPathValidatorException：找到不认证路径的信任锚。

## <a name="cause"></a>原因

这是因为本地部署环境中的 Android 8+ 不信任自签名证书。

## <a name="resolution"></a>解决方法

请使用外部（公共）认证机构 (CA)。 Warehouse Management 应用版本 1.9.0.0 中提供了针对此问题的修复。 有关此问题及其解决方法的详细信息，请参阅[设置应用连接时找不到认证路径的信任锚](certification-path-app-connection-error.md)。
