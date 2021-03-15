---
title: 为客户创建直接借记授权单
description: 此任务指南向您演示如何创建直接借记授权并将其使用在发票上。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f746da0bcf2b1e0cb09af6b5e2ea61938213c924
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991034"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>为客户创建直接借记授权单

[!include [banner](../../includes/banner.md)]

此任务指南向您演示如何创建直接借记授权并将其使用在发票上。


## <a name="create-a-bank-account"></a>创建银行帐户
1. 在 **导航窗格** 中，转到 **模块 > 应收帐款 > 客户 > 所有客户**。
2. 在列表中，选择一个记录。 例如，选择 US-001。
3. 在操作窗格上，单击 **客户**。
4. 单击 **银行帐户**。
5. 单击 **新建**。
6. 在 **银行帐户** 字段中，键入一个值。
7. 在 **名称** 字段中，键入一个值。
8. 在 **IBAN** 字段，键入一个值。
9. 在 **货币** 字段中，键入一个值。
10. 单击 **保存**。
11. 关闭该页面。
12. 在 **导航窗格** 中，转到 **模块 > 现金和银行管理 > 银行帐户 > 银行帐户**。
13. 在列表中，找到并选择所需记录。
14. 在列表中，单击所选行中的链接。
15. 单击 **编辑**。
16. 展开 **其他识别** 快速选项卡。
17. 在 **直接借记 ID** 字段中，键入一个值。
18. 在 **IBAN** 字段，键入一个值。
19. 关闭该页面。
20. 关闭该页面。

## <a name="define-the-electronic-payment-method"></a>定义电子付款方式
1. 在 **导航窗格** 中，转到 **模块 > 应收帐款 > 付款设置 > 付款方式**。
2. 单击 **新建**。
3. 在 **付款方式** 字段中，输入值。
4. 在 **描述** 字段中，键入一个值。
5. 在 **付款类型** 字段中，输入“电子付款”。 直接借记授权的付款方式的付款类型必须为“电子付款”。
6. 在 **需要授权** 字段选择“是”。
7. 关闭该页面。

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>向客户添加一个直接借记授权。
1. 在 **导航窗格** 中，转到 **模块 > 应收帐款 > 客户 > 所有客户**。
2. 在列表中，选择一个记录。 例如，选择 US-001。
3. 单击 **编辑**。
4. 展开 **默认付款** 快速选项卡。
5. 在 **付款方式** 字段中，输入或选择一个值。
6. 展开 **默认付款** 快速选项卡。
7. 展开 **直接借记授权** 快速选项卡。
8. 单击 **添加**。
9. 在 **银行帐户** 字段中，输入或选择一个值。
10. 在 **贷方银行帐户** 字段中，输入或选择一个值。
11. 在 **付款频率** 字段中，输入您预期为此授权付款处理的数字。
12. 单击 **确定**。
13. 单击 **打印**。
14. 点击 **授权单报告**。
15. 关闭该页面。
16. 单击 **编辑**。
17. 在 **签署日期** 字段中，输入一个日期。
18. 单击 **是**。
19. 输入授权单的签署位置。
20. 单击 **确定**。
21. 关闭该页面。

## <a name="create-a-free-text-invoice-with-mandate"></a>创建一个包含授权的普通发票
1. 在 **导航窗格** 中，转到 **模块 > 应收帐款 > 发票 > 所有普通发票**。
2. 单击 **新建**。
3. 选择您已添加了授权的客户。
4. 在 **直接借记授权 ID** 字段中，输入或选择一个值。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]