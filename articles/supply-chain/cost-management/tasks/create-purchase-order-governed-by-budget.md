---
title: 创建按预算管理的采购订单
description: 使用此过程可以创建为可用预算检查的采购订单。
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016179"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>创建按预算管理的采购订单

[!include [banner](../../includes/banner.md)]

使用此过程可以创建为可用预算检查的采购订单。

## <a name="review-the-budget-control-configuration"></a>检查预算控制配置

1. 转至 **预算 > 设置 > 预算控制 > 预算控制配置**。
1. 选择 **可用的预算资金** 选项卡。
1. 选择 **单据和日记帐** 选项卡。
1. 选择 **定义预算控制规则** 选项卡。
1. 选择 **定义预算组** 选项卡。
1. 关闭该页面。

## <a name="create-a-purchase-order"></a>创建采购订单

1. 转到 **采购 > 采购订单 > 所有采购订单**。
1. 选择 **新建**。
1. 在 **供应商帐户** 字段中，输入或选择一个值。
1. 展开 **常规** 快速选项卡。
1. 在 **会计日期** 字段中，设置日期。
1. 选择 **确定** 关闭对话框并打开新的采购订单。
1. 在 **采购订单行** 快速选项卡上，从工具栏中选择 **添加行** 以添加新行，然后根据需要填写行以将物料添加到订单。
1. 在 **采购订单行** 快速选项卡工具栏上，选择 **财务 \> 分配金额**。
1. 在 **会计科目** 字段中，指定一个科目。
1. 关闭该页面。

## <a name="perform-budget-checking"></a>执行预算检查

1. 继续处理您刚才向其中添加了一行的采购订单。
1. 在 **采购订单行** 快速选项卡工具栏上，选择 **财务 \> 执行预算检查**。
1. 在 **采购订单行** 快速选项卡工具栏上，选择 **财务 \> 预算检查错误或警告**。
1. **预算检查错误或警告** 对话框将打开。 查看检查结果，然后选择 **关闭** 以关闭对话框。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]