---
title: 仓库工作疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库工作时可能遇到的常见问题。
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
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645785"
---
# <a name="troubleshoot-warehouse-work"></a>仓库工作疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库工作时可能遇到的常见问题。

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>当跟踪维度组中允许空发货和空收货时，我无法移动具有序列号项的牌照。

### <a name="issue-description"></a>问题描述

如果序列号在跟踪维度组上有 *允许空发货* 和 *允许空收货* 设置，并且同一个位置有多个牌照，其中一些有序列号，另一些则没有，这种情况下您无法使用 **移动** 菜单项移动牌照。

### <a name="issue-resolution"></a>解决问题

此问题将通过 [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) 中部署的更改修复。 当允许空收货和空发货时，这些更改将使 **序列号** 字段变为可选。

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>处理移动时，我在仓库应用中收到以下错误消息：“此流程不允许库存所有者 %1。”

### <a name="issue-description"></a>问题描述

当使用仓库应用进行移动时，缺少 **所有者** 跟踪维度。 Supply Chain Management 客户端中的常规库存转移日记帐好像可以按预期工作，但只能在填充了 **所有者** 维度时过帐。

### <a name="issue-resolution"></a>解决问题

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，仓库管理流程仅支持法人所有的库存。
