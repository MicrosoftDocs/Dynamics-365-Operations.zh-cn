---
title: 收货仓库工序疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。
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
ms.openlocfilehash: 6d7fcb2ed32c57b8701bee5b90889a0a63e1f7061aa9014480ae8c543e1f229a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748659"
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

新的入站负荷处理功能 *负荷数量超收* 解决了这个问题。 要启用此功能，转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区，启用以下功能（按照它们列出的顺序）：

1. 将采购订单库存交易记录与负荷相关联
1. 负荷数量超收

有关详细信息，请参阅[针对采购订单过帐登记的产品数量](inbound-load-handling.md#post-registered-quantities)。

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>当登记入库订单时，我收到以下错误消息：“数量无效。”

### <a name="issue-description"></a>问题描述

如果在用于登记入库订单的移动设备菜单项中，**牌照分组策略** 字段设置为 *用户定义*，您将收到一条错误消息（“数量无效”），并且无法完成登记。

### <a name="issue-cause"></a>问题原因

当 *用户定义* 用作牌照分组策略时，系统将传入库存拆分为单独的牌照，如单位序列组所示。 如果批号或序列号用于跟踪将收货的物料，必须按登记的牌照指定每个批次或序列的数量。 如果为牌照指定的数量超过针对当前维度仍必须收货的数量，您将收到错误消息。

### <a name="issue-resolution"></a>解决问题

使用 **牌照分组策略** 字段设置为 *用户定义* 的移动设备菜单项登记物料时，系统可能会要求您确认或输入牌照编号、批号或序列号。

在牌照确认页面上，系统将显示为当前牌照分配的数量。 在批次或序列确认页面上，系统将显示在当前牌照上仍必须收货的数量。 它还将包含一个字段，您可以在其中输入为牌照和批号或序列号组合登记的数量。 在这种情况下，请确保为牌照登记的数量不超过仍必须收货的数量。

或者，如果在入库订单登记时生成了太多牌照，**牌照分组策略** 字段的值可以更改为 *牌照分组*，可以向物料分配新的单位序列组或者可以停用单位序列组的 **牌照分组** 选项。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
