---
title: 创建客户的勾销日记帐
description: 此任务指南将为您展示在“收款”页、“未结客户发票”页和“客户”页如何设置勾销和勾销交易参数。
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21aaeda413e767fed1815423b0262127c6692bb6
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775291"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>创建客户的勾销日记帐

[!include [banner](../../includes/banner.md)]

此任务指南将为您展示在“收款”页、“未结客户发票”页和“客户”页如何设置勾销和勾销交易参数。 此任务使用 USMF 公司演示。


## <a name="set-up-the-write-off-parameters"></a>设置勾销参数
1. 转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**。
2. 单击 **收款** 选项卡。
3. 展开或折叠 **勾销** 部分。
    - 此 **勾销日记帐** 是普通日记帐，它将持续勾销您创建的交易记录。  
    - 您可以为每次勾销附上一个原因代码。 您可以在勾销时改写此默认值。  
    - 如果你想在勾销的原始交易记录中分离销售税，请将 **单独的销售税** 设置为“是”。  
4. 关闭该页面。
5. 转到 **信用和收款 > 设置 >客户过帐模板**。 勾销帐户将用于普通日记帐的支出帐户或预留调整。
6. 关闭该页面。

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>从帐龄余额页上勾销客户余额
1. 转到 **贷记和收款 > 收款 > 帐龄余额**。
2. 标记您要勾销客户所在的行。 例如，标记 Birch 公司所在的行。
3. 在 **操作窗格** 上，单击 **收款**。
4. 单击 **勾销**。
5. 单击 **确定**。
6. 关闭该页面。
7. 转到 **导航窗格 > 模块 > 总帐 > 日记帐条目 > 普通日记帐**。
8. 选择包含您勾销条目的日记帐批号。 创建单行以预留客户余额。 创建单行或多行以过帐勾销至勾销帐户。  
9. 关闭该页面。


## <a name="write-off-transactions-from-the-collections-page"></a>从收款页面勾销交易
1. 转到 **贷记和收款 > 收款 > 帐龄余额**。
2. 选择您要勾销交易记录的客户的名称。 例如，选择 Cave Wholesales (US-004)。
3. 标记第一个交易行。
4. 标记第二个交易行。
5. 单击 **勾销**。
6. 在 **原因注释** 字段中，键入“坏帐”。
7. 单击 **确定**。
8. 关闭该页面。
9. 关闭该页面。
10. 转到 **总帐 > 日记帐条目 > 普通日记帐**。
11. 选择包含您勾销条目的日记帐批号。 创建单行以预留客户余额。 创建单行或多行以过帐勾销至勾销帐户。  
12. 关闭该页面。


## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>从“未结客户发票”页勾销发票
1. 转至 **导航窗格 > 应收帐款 > 发票 > 未结客户发票**。
2. 标记发票行。 例如，标记 CIV-000667 所在行。
3. 在 **操作窗格** 中，单击 **发票**。
4. 单击 **勾销**。
5. 单击 **确定**。
6. 关闭该页面。

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>从“客户”页勾销客户余额
1. 转到 **应付帐款 > 客户 > 所有客户**。
2. 选择客户帐户。 例如，选择 US-001 (Contoso Retail San Diego)。
3. 在 **操作窗格** 上，单击 **收款**。
4. 单击 **勾销**。
5. 单击 **确定**。
6. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
