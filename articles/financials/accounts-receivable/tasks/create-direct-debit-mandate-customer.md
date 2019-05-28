---
title: 为客户创建直接借记授权单
description: 此任务指南向您演示如何创建直接借记授权并将其使用在发票上。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572527"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>为客户创建直接借记授权单

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南向您演示如何创建直接借记授权并将其使用在发票上。


## <a name="create-a-bank-account"></a>创建银行帐户
1. 转到“应付账款”>“客户”>“所有客户”。
2. 例如，选择 US-001。
3. 在“操作窗格”上，单击“客户”。
4. 单击“银行帐户”。
5. 单击“新建”。
6. 在“银行帐户”字段中，键入一个值。
7. 在“名称”字段中，键入一个值。
8. 在“IBAN”字段，键入一个值。
9. 在“货币”字段中，键入一个值。
10. 单击“保存”。
11. 关闭该页面。
12. 转至“现金和银行管理”>“银行帐户”>“银行帐户”。
13. 在列表中，找到并选择所需记录。
14. 在列表中，单击所选行中的链接。
15. 单击“编辑”。
16. 展开”其他识别“部分。
17. 在“直接借记 ID”字段中，键入一个值。
18. 在“IBAN”字段，键入一个值。
19. 关闭该页面。
20. 关闭该页面。

## <a name="define-the-electronic-payment-method"></a>定义电子付款方式
1. 转到“应收账款”>“付款设置”>“付款方式”。
2. 单击“新建”。
3. 在“付款方式”字段中，输入值。
4. 在“描述”字段中，键入一个值。
5. 直接借记授权的付款方式的付款类型必须为“电子付款”。
6. 在“需要授权”字段选择“是”。
7. 关闭该页面。

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>向客户添加一个直接借记授权。
1. 转到“应付账款”>“客户”>“所有客户”。
2. 例如，选择 US-001。
3. 单击“编辑”。
4. 展开“默认付款”部分。
5. 在“付款方式”字段中，输入或选择一个值。
6. 展开“默认付款”部分。
7. 展开“直接借记授权”部分。
8. 单击“添加”。
9. 在“银行帐户”字段中，输入或选择一个值。
10. 在“贷方银行帐户”字段中，输入或选择一个值。
11. 输入您预期为此授权付款处理的数字。
12. 单击“确定”。
13. 单击“打印”。
14. 点击“授权单报告”。
15. 关闭该页面。
16. 单击“编辑”。
17. 在“签署日期”字段中，输入一个日期。
18. 单击“是”。
19. 输入授权单的签署位置。
20. 单击“确定”。
21. 关闭该页面。

## <a name="create-a-free-text-invoice-with-mandate"></a>创建一个包含授权的普通发票
1. 转到“应收账款”>“发票”>“所有普通发票”。
2. 单击“新建”。
3. 选择您已添加了授权的客户。
4. 在“直接借记授权 ID”字段中，输入或选择一个值。

