---
title: 收货仓库工序疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。
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
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645964"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>收货仓库工序疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>我收到以下错误消息：“质检订单 %1 已生成。 找不到群集配置文件，请检查您的配置。”

### <a name="issue-description"></a>问题描述

此错误消息与打开质量管理 (QMS) 的接收流程有关。 根据您环境中的配置，有关生成错误消息的交易的其他详细信息可能有助于解决此问题。

### <a name="issue-resolution"></a>解决问题

首先，请查看[群集领料](set-up-cluster-picking.md)设置，确保正确配置了群集配置文件。 除非设置了群集配置文件，否则您不能使用移动设备菜单项进行群集领料。 根据您的环境，您可能还必须查看其他相关配置。

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>混合牌照接收不使用“贷记”以外的任何处置代码。

### <a name="issue-description"></a>问题描述

当处置代码的 **操作** 字段设置为 *贷记* 或 *报废* 时，您只能使用[混合牌照接收](mixed-license-plate-receiving.md)菜单项来处理退回物料。

### <a name="issue-resolution"></a>解决问题

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，混合牌照接收仅支持将 **操作** 字段设置为 *贷记* 或 *报废* 的[处置代码](../service-management/set-up-disposition-codes.md)。

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>当我运行“更新产品收货”定期任务时，未确认的采购订单会被确认。

### <a name="issue-description"></a>问题描述

在运行 *更新产品收货* 定期任务后，系统会自动确认库存交易状态为 *已登记* 的未确认采购订单。

### <a name="issue-resolution"></a>解决问题

新的入站负荷处理功能 *负荷数量超收* 解决了这个问题。 要启用此功能，请转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，启用以下功能（按照它们列出的顺序）：

1. 将采购订单库存交易记录与负荷相关联
1. 负荷数量超收

有关详细信息，请参阅[针对采购订单过帐登记的产品数量](inbound-load-handling.md#post-registered-quantities)。
