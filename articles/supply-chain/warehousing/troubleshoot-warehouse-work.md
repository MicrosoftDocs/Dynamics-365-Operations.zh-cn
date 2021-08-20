---
title: 仓库工作疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库工作时可能遇到的常见问题。
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
ms.openlocfilehash: f9dbc1e043de5c8f840b291b652ec522c9f1eb6a622e8dab88ced3fa91570e8e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775451"
---
# <a name="troubleshoot-warehouse-work"></a>仓库工作疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库工作时可能遇到的常见问题。

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>当跟踪维度组中允许空发货和空收货时，我无法移动具有序列号项的牌照。

### <a name="issue-description"></a>问题描述

如果序列号在跟踪维度组上有 *允许空发货* 和 *允许空收货* 设置，并且同一个位置有多个牌照，其中一些有序列号，另一些则没有，这种情况下您无法使用 **移动** 菜单项移动牌照。

### <a name="issue-resolution"></a>解决问题

此问题将通过 [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) 中部署的更改修复。 当允许空收货和空发货时，这些更改将使 **序列号** 字段变为可选。

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>处理移动时，我在仓库管理移动应用中收到以下错误消息：“此流程不允许库存负责人 %1。”

### <a name="issue-description"></a>问题描述

当使用仓库管理移动应用进行移动时，缺少 **负责人** 跟踪维度。 Supply Chain Management 客户端中的常规库存转移日记帐好像可以按预期工作，但只能在填充了 **所有者** 维度时过帐。

### <a name="issue-resolution"></a>解决问题

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，仓库管理流程仅支持法人所有的库存。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]