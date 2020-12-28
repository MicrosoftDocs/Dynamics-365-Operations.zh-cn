---
title: 使用 ISO20022 付款格式创建和导出供应商付款
description: 此过程显示如何在供应商付款日记帐中创建付款行，并使用 ISO2022 贷方转帐示例生成供应商付款文件。
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440853"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>使用 ISO20022 付款格式创建和导出供应商付款

[!include [banner](../../includes/banner.md)]

此主题说明如何在供应商付款日记帐中创建付款行，并使用 ISO2022 贷方转帐示例生成供应商付款文件。

这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第五个。 使用 DEMF 演示数据来完成此示例。

## <a name="example"></a>示例

1.    转到 **应付帐款 > 付款 > 付款日记帐**。
2.    单击 **新建**。
3.    在 **名称** 字段中，输入或选择一个值。
4.    单击 **行 > 付款方案 > 创建付款方案**。
5.    扩展 **要包括的记录** 部分。
6.    单击 **筛选器**。
7.    在列表中，选择 **供应商** 表和 **供应商帐户字段** 的行。
8.    在 **标准** 字段中，输入或选择一个值。 您可以为选择要付款的供应商交易应用任何条件，此示例中则是将 DE-001 用作供应商帐户。
12.    单击 **确定**。
13.    单击 **确定**。
14.    单击 **创建付款**。
15. 生成 ISO20022 付款文件。
    1.    单击 **生成付款**。
    2.    在 **付款方式** 字段中，输入或选择一个值。
    3.    在 **文件名** 字段中，键入一个值。 对于本例，由于 EUR 付款，生成的文件将为 SEPA 合规文件。 ISO20022 贷方转帐以及其他供应商付款格式也可以用于生成其他币种的付款。
    4.    在 **银行帐户** 字段中，输入或选择一个值。

