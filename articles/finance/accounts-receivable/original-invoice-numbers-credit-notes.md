---
title: 对贷方通知单中的原始发票的引用
description: 本文说明如何在相关的贷方通知单中设置和打印原始发票编号。
author: mrolecki
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: f1f9ca3914aa02cc38ddfe9f8dd88eb7fc88fd4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281226"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>对贷方通知单中的原始账单的引用

[!include [banner](../includes/banner.md)]


在某些国家和地区，法律要求打印的贷方通知单必须包含对原始发票的引用。 本文说明如何在相关的贷方通知单中设置和打印原始发票编号。

## <a name="prerequisites"></a>先决条件

- 在 **功能管理** 工作区，打开 **销售和项目发票报表的贷记开票版式** 功能。 有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。
- 必须在“打印管理”中配置所需文档的可打印格式。

本文中所述的功能适用于以下文档：

**应收账款**

- 普通贷方通知单
- 客户贷方通知单

**项目管理与核算**

- 项目贷方通知单

## <a name="configure-accounts-receivable-parameters"></a>配置应收帐款参数

请执行以下步骤设置控制是否在相关的贷方通知单中打印对原始发票的引用的参数。

1. 转到 **应收帐款** \> **设置** \> **应收帐款参数**。
2. 在 **更新** 选项卡上，在 **发票** 快速选项卡上，将 **将贷记开票版式应用到销售和项目发票报表** 选项设置为 **是**。

![配置应收帐款参数。](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>定义对原始发票的引用

使用以下过程根据文档类型定义对原始发票的引用。

### <a name="free-text-credit-note"></a>普通贷方通知单

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 创建新的贷方通知单，或选择现有的贷方通知单。
3. 打开发票。
4. 在操作窗格上的 **发票** 选项卡上，在 **功能** 组中，选择 **贷记开票**。
5. 输入对原始发票的引用，然后选择更正原因。

![定义普通发票的引用。](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>客户贷方通知单

1. 转到 **应收帐款** \> **订单** \> **所有销售订单**。
2. 选择并打开必须更正的已开票的销售订单。
3. 在操作窗格上的 **销售** 选项卡上，在 **贷方通知单** 组中，选择 **贷方通知单**。
4. 输入更正原因。 对原始发票的引用将自动建立。

![定义销售订单的引用。](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>项目贷方通知单

1. 转到 **项目管理和会计** \> **项目发票** \> **项目发票**。
2. 选择并打开必须更正的项目发票。
3. 在操作窗格上的 **项目发票** 选项卡上，在 **功能** 组中，选择 **为贷方通知单选择**。
4. 选择 **贷记开票**。
5. 输入更正原因。 对原始发票的引用将自动建立。

![定义项目发票的引用。](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>打印贷方通知单

当您打印普通、客户和项目贷方通知单时，它们将包括对原始发票的引用和更正原因。

![打印的贷方通知单。](media/credit-note-FTI.jpg)

> [!NOTE]
> 假设将打印对原始发票的引用，请确保正确配置文档的可打印格式。

## <a name="references-to-original-invoices-in-debit-notes"></a>对借方通知单中的原始发票的引用

默认情况下，可以为贷方通知单输入对原始发票的引用。 例如，您可以在对原始发票进行负（减少）更正时输入引用。

要在对原始发票进行正（增加）更正时输入引用，您必须在 **功能管理** 工作区启用 **在借方通知单中引用原始发票** 功能。  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
