---
title: 计算和调整供应商发票上的销售税
description: 本主题介绍如何在 Dynamics 365 Finance 中调整供应商发票上的销售税。
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994707"
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