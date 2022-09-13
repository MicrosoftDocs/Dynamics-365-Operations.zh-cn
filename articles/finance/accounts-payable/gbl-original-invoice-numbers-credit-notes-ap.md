---
title: 引用贷方通知单中的原始发票（供应商发票）
description: 本文介绍如何在创建贷方通知单时创建对原始发票的引用。
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: 39cf4eb7eef1a83abeb7bd44fa7b2abefee0806e
ms.sourcegitcommit: 8eb0cafe5ad20be2c4fff684e88d7d3f2249f820
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2022
ms.locfileid: "9409656"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>引用贷方通知单中的原始发票（供应商发票）

[!include [banner](../includes/banner.md)]

在某些国家和地区，法律要求打印的贷方通知单或报告程序必须包含对原始发票的引用。 本文介绍如何在创建贷方通知单时创建对原始发票的引用。

## <a name="prerequisites"></a>先决条件

在 **功能管理** 工作区中，启用 **为供应商发票启用贷方开票** 功能。 有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

本文中所述的功能适用于以下业务单据。

**应付帐款：**

- 采购订单
- 发票日记帐
- 发票登记簿

**总帐：**

- 普通日记帐

## <a name="define-a-reference-to-an-original-invoice"></a>定义对原始发票的引用

定义对原始发票的引用包括以下高级步骤：
1. 创建和过帐供应商发票。
2. 创建供应商贷方通知单。
3. 使用贷记开票功能将发票与贷方通知单相关联。
4. 过帐贷方通知单。

使用以下过程在指定的业务单据类型中定义对原始发票的引用。

### <a name="vendor-credit-note-purchase-order"></a>供应商贷方通知单（采购订单）

1. 转到 **应付帐款** > **采购订单** > **所有采购订单**。
2. 创建新的采购订单，或使用现有采购订单创建贷方通知单。
3. 在操作窗格上的 **发票** 选项卡上，在 **引入** 组中，选择 **贷记开票**。
4. 输入更正和引用原始发票的原因。

### <a name="vendor-credit-note-ledger-journals"></a>供应商贷方通知单（分类日记帐）

1. 按以下步骤之一：

    - 转到 **应付帐款** \> **发票日记帐**。
    - 转到 **应付帐款** \> **发票登记簿**。
    - 转到 **总帐** \> **日记帐条目** \> **普通日记帐**。

2. 创建新日记帐和新日记帐行。
3. 在操作窗格上，选择 **功能** \> **贷方开票**。
4. 输入更正和引用原始发票的原因。

> [!NOTE]
> 如果 **帐户类型** 字段设置为 **供应商**，则 **贷方开票** 命令在普通日记帐凭证中可见。
