---
title: 处理变动时不允许库存负责人
description: 您可能会遇到以下错误：“不允许库存负责人 %1。” 仓库管理流程仅支持法人所有的库存。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475664"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>在仓库应用中处理变动时不允许库存负责人

## <a name="symptoms"></a>故障特征

在 Warehouse Management 移动应用中处理变动时，您可能会收到以下错误消息：

> 此流程中不允许库存负责人 %1。

## <a name="cause"></a>原因

这是因为使用 Warehouse Management 移动应用进行移动时，缺少 **负责人** 跟踪维度。 Supply Chain Management 客户端中的常规库存转移日记帐好像可以按预期工作，但只能在填充了 **所有者** 维度时过帐。

## <a name="resolution"></a>解决方法

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，仓库管理流程仅支持法人所有的库存。
