---
title: 领料和打包疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中领料和打包时可能遇到的常见问题。
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
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645469"
---
# <a name="troubleshoot-picking-and-packing"></a>领料和打包疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中领料和打包时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>我收到以下错误消息：“如果设置了维度序列号，维度位置不能保留为空。”

### <a name="issue-description"></a>问题描述

如果您使用启用了高级仓库管理 (WMS) 的仓库为序列物料创建转移单，然后在工作完成后尝试确认装运，这时会收到此错误消息。

### <a name="issue-resolution"></a>解决问题

**默认收货位置** 字段在“来源”仓库的中转仓库中是空白的。 要解决此问题，请在中转仓库中指定默认收货位置。 请确保此位置是由牌照控制的。

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>我收到以下错误消息：“无效牌照。”

### <a name="issue-description"></a>问题描述

当您扫描牌照 ID 时，会在仓库应用中收到此错误消息。

### <a name="issue-resolution"></a>解决问题

请确保牌照表中存在该牌照 ID，并且牌照上的物料和数量均可用（换言之，它们没有被锁定）。

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>我收到以下错误消息：“字段 'Load weight'(=-%1) 只能包含正数。 已取消更新。”

### <a name="issue-description"></a>问题描述

当您处理从打包位置到暂存位置，或从暂存位置到停靠位置的工作时，如果有未结工作，将会收到此错误消息。

### <a name="issue-resolution"></a>解决问题

要解决此问题，请转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查**，运行 **仓库负荷重量一致性检查** 流程。

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>我收到以下错误消息：“数量对于单位 %1 无效。”

### <a name="issue-description"></a>问题描述

当您尝试跨多个批次执行 *拆分领料* 时，会收到此错误消息。

### <a name="issue-resolution"></a>解决问题

仓库工作人员必须在仓库应用中使用 *领料短缺* 流程。 如果您尝试从同一位置为多个批次领料，还可以在仓库应用中使用 **完全** 选项。

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>我无法将库存移动到牌照控制的位置。

### <a name="issue-description"></a>问题描述

您不能减少负荷上的已领料数量。

### <a name="issue-resolution"></a>解决问题

在早期版本中，您不能减少负荷上的已领料数量。 但是，现在您可以取消牌照控制的位置的领料。 您必须在 **减少领料数量** 页上为负荷行指定 **位置** 值和 **牌照** 值。

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>我可以按仓库打印交货通知或打包内容吗？

### <a name="issue-description"></a>问题描述

您要在 **工作审计模板行更新** 页上按仓库或站点打印交货通知或打包内容。

### <a name="issue-resolution"></a>解决问题

使用“打印管理”设置打印文档时，请通过“打印管理”限制范围（站点/仓库），而不要在 **工作审计模板行更新** 页上选择 **编辑打印设置**。

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>装箱单从销售订单过帐后，我无法取消。

### <a name="issue-description"></a>问题描述

为 WMS 启用了领料和装运流程后，无法取消从销售订单过帐的装箱单。

### <a name="issue-resolution"></a>解决问题

要更正已启用 WMS 的物料的已过帐装箱单，必须从负荷而不是从订单进行过帐。 Microsoft 已评估此问题，确定了这是一项功能限制。 通常，通过仓库管理流程领料和装运的销售订单可以从负荷或装运以及销售订单文档本身更新装箱单。 但是，如果从销售订单文档对销售订单进行装箱单更新，装箱单冲销仍然无法从负荷或销售订单进行。 因此，我们建议您从负荷使用装箱单过帐。 在这种情况下，将启用必须从负荷进行的冲销。

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>我收到以下错误消息：“找不到足够的工作来建立群集。”

### <a name="issue-description"></a>问题描述

当您使用 *系统导向的群集领料* 流程时，如果您配置了一个群集配置文件，例如可以在配置文件中为 10 个位置领料，那么当有足够的工作可以为 10 个位置领料时，该流程将按计划运行。 但是，如果只有八个位置要领料，您会收到此错误消息，因为一个群集的工作不足。

### <a name="issue-resolution"></a>解决问题

要解决此问题，请编辑群集配置文件，将 **激活位置** 选项设置为 *否*。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]