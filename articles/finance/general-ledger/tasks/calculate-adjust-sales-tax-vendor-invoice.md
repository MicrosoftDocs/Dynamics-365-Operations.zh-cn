---
title: 计算和调整供应商发票上的销售税
description: 本主题介绍如何在 Dynamics 365 Finance 中调整供应商发票上的销售税。
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd98f42b501ddabdc0cc26d2a264c533410731f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815204"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>计算和调整供应商发票上的销售税

[!include [banner](../../includes/banner.md)]

本主题介绍如何调整供应商发票上的销售税。 如果原始单据显示计算的不同税额，您可在过帐前调整这些税额。 本任务使用 DEMF 公司进行演示。

1. 在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票日记帐**。
2. 选择 **新建**。
3. 在新行的 **名称** 字段中，选择下拉菜单中的一个选项。
4. 在操作窗格中，选择 **行**。
5. 在 **帐户** 字段中，指定所需值。
6. 在 **发票** 字段中，键入一个值。
7. 在 **信用** 字段中，输入一个数字。
8. 在 **抵销帐户** 字段中，指定所需值。
9. 选择 **销售税**。
10. 在 **实际销售税总额** 字段中，输入一个数字。
11. 在 **调整** 选项卡中，可调整每个销售税代码的销售税金额。
12. 选择 **通过计算得出的金额重置实际金额**。
13. 选择 **确定**。
14. 选择 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]