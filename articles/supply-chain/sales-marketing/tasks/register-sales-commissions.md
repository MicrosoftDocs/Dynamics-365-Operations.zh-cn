---
title: 登记销售佣金
description: 该过程显示如何计算和登记销售佣金。
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "355142"
---
# <a name="register-sales-commissions"></a>登记销售佣金

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程显示如何计算和登记销售佣金。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。 在开始此指南前，运行名为“设置销售佣金规则”的指南，以确保您已设置好所有必要的佣金计算设置。

记录您为佣金过程选择的客户和物料编号，并在创建本指南的销售订单时使用。


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>为销售人员符合佣金资格的销售订单开票
1. 转至“销售和营销”>“销售订单”>“所有销售订单”。
2. 单击“新建”。
3. 在“客户帐户”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 单击“确定”。
7. 在“操作窗格”上，单击“选项”。
8. 单击“更改”视图。
9. 单击“标题”视图。
10. 展开“设置”部分。
    * “销售组”字段中的值代表有一名或多名指派的销售代表的组。 组中的人员为在订单开票时以预定义的比率和分配规则接受佣金的人员。   该值复制自客户卡，但如果您想更改则可以更改。  销售组还复制到销售订单行。 您可以更改它，使其与标题和/或行之间的名称不同。  
    * “佣金组”字段的值代表您出于跟踪佣金目的为一个或多个客户创建的组。   该值复制自客户卡，但如果您想更改则可以更改。   
11. 在“操作窗格”上，单击“选项”。
12. 单击“更改”视图。
13. 单击“查看行”。
14. 在“物料编号”字段中，单击下拉按钮以打开查找。
15. 在列表中，选择为佣金设置的物料。 
16. 在“数量”字段中，输入一个数字。
    * 记录行的净额。 它代表销售收入，在此示例中它是佣金计算的基础。  
17. 单击“保存”。
18. 在操作窗格上，单击“发票”。
19. 单击“发票”。
20. 展开“参数”部分。
21. 在“数量”字段中，选择“所有”。
22. 在“过帐”字段中选择“是”。
23. 单击“确定”。
24. 单击“确定”。
    * 过帐交易记录可能需要大概一分钟。 允许完成处理，并且不关闭页面。  

## <a name="review-the-registered-sales-commissions"></a>查看登记的销售佣金
1. 在操作窗格上，单击“发票”。
2. 单击“发票”。
3. 在操作窗格上，单击“发票”。
4. 单击“佣金交易记录”。
    * 概览选项卡显示应付给与开票的销售订单相关的销售人员的佣金金额行。 我们现在查看详细信息。     
    * 如果您使用“设置销售佣金规则”指南来设置佣金销售组，将有两位销售人员接受销售佣金，并且两人平分佣金。  
    * 在此示例中，佣金的总金额计算为销售收入百分比（订单行的净额）。   
5. 关闭该页面。
6. 单击“凭证”。
    * 您可以在凭证交易记录中查看已过帐到预定义的佣金费用的佣金金额和应付佣金金额。  

