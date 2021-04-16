---
title: 负荷构建和装运疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理负荷构建和装运时可能遇到的常见问题。
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
ms.openlocfilehash: e9964376a794661058da78152879d2142dd7ec51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828194"
---
# <a name="troubleshoot-load-building-and-shipments"></a>负荷构建和装运疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理负荷构建和装运时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>我收到以下错误消息：“您无法为此订单行创建负荷行，因为它包含无效的库存维度...”

### <a name="issue-description"></a>问题描述

当您尝试将退货销售订单下达到仓库时，您会收到以下错误消息：

> 您无法为此订单行创建负荷行，因为它包含无效的库存维度。 您无法引用位于预留层次结构中位置维度以下的库存维度。 请从订单行中删除无效维度。

### <a name="issue-resolution"></a>解决问题

很遗憾，此产品不支持销售退货流程的负荷处理。 因此，您不能将退货销售订单下达到仓库。

在销售订单交易中，您无法引用位于预留层次结构中 **位置** 维度以下的库存维度。 解决方法是从订单行中删除无效维度。

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>我收到以下错误消息：“其中一行已在负荷中。 无法下达到仓库。”

### <a name="issue-description"></a>问题描述

如果您手动创建负荷，或者设置流程以在进行销售订单行输入之前负荷已经创建，系统将假定后续下达会手动完成，并将使用负荷中的路线和评级。

在另一个可能的场景中，您尝试对仓库执行自动下达，但是波次流程无法创建工作。 因此，仍会创建未结装运或负荷。 然后，此未结装运或负荷将阻止后续自动下达订单的尝试，直到您删除未结装运或负荷，或手动重新处理波次。

### <a name="issue-resolution"></a>解决问题

您可以从销售订单页下达，也可以从下达销售订单页自动下达，只要在下达仓库之前没有负荷。 负荷将在波次被处理后自动创建。

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>我收到以下错误消息：“无法处理交货通知更正。 交货通知仅包含需要进入仓库管理流程的物料，因为交货通知更正不支持这些物料。”

### <a name="issue-description"></a>问题描述

发布交货通知后，将无法取消，因为 **取消** 按钮不可用。 您也无法更正交货通知。 如果尝试更正，将收到此错误消息。

### <a name="issue-resolution"></a>解决问题

要更正已启用高级仓库管理 (WMS) 的物料的已过帐装箱单，必须从负荷而不是直接从订单进行过帐。

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>如何从出站负荷而不是波次创建工作？

### <a name="issue-description"></a>问题描述

这里是重现此问题的一种方法。

1. 使用销售订单或转移单创建出站负荷。
2. 将负荷发放到仓库。
3. 请注意，尚未生成任何领料工作。

### <a name="issue-resolution"></a>解决问题

如果必须在发放负荷时立即生成工作，您必须相应地配置波次模板。 在波次模板上，将以下选项设置为 *是*：

- 自动波次创建
- 在发放到仓库时处理波次
- 自动发出波次

## <a name="i-cant-re-release-a-partially-shipped-load"></a>我无法重新发放部分装运的负荷。

### <a name="issue-description"></a>问题描述

您不能将部分装运的负荷发放到仓库。 当您对仓库执行发放时，会出现“操作完成”消息，但是不会发生任何变化，也不会为剩余数量创建工作。 当您使用运输负荷功能并且有未完成的预留时，会发生此问题。

### <a name="issue-resolution"></a>解决问题

[KB 问题 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f)（“部分装运的负荷可以重新加入波次和重新处理”）在[版本 10.0.15](../get-started/whats-new-scm-10-0-15.md) 中已修复。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]