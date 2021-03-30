---
title: 登记销售佣金
description: 此主题介绍如何计算和登记销售佣金。
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82c8dc2f284923b5583bf983413a015b9ece8252
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205921"
---
# <a name="register-sales-commissions"></a>登记销售佣金

[!include [banner](../../includes/banner.md)]

此主题介绍如何计算和登记销售佣金。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。 在开始此指南前，运行名为“设置销售佣金规则”的指南，以确保您已设置好所有必要的佣金计算设置。

记录您为佣金过程选择的客户和物料编号，并在创建本指南的销售订单时使用。


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>为销售人员符合佣金资格的销售订单开票
1. 在导航窗格中，转到 **模块 > 销售和营销 > 销售订单 > 所有销售订单**。
2. 选择 **新建**。
3. 在 **客户帐户** 字段中，从下拉菜单选择所需记录。
4. 选择 **确定**。
5. 在操作窗格上，选择 **选项**。
6. 选择 **更改视图**。
7. 选择 **标题视图**。
8. 展开 **设置** 部分。

    - **销售组** 字段中的值代表有一名或多名指派的销售代表的组。 组中的人员为在订单开票时以预定义的比率和分配规则接受佣金的人员。   
    - 该值复制自客户卡，但如果您想更改则可以更改。  
    - 销售组还复制到销售订单行。 您可以更改它，使其与标题和/或行之间的名称不同。  
    - **佣金组** 字段的值代表您出于跟踪佣金目的为一个或多个客户创建的组。   
    - 该值复制自客户卡，但如果您想更改则可以更改。   

9. 在操作窗格上，选择 **选项**。
10. 选择 **更改视图**。
11. 选择 **行视图**。
12. 在 **物料编号** 字段的下拉菜单中，选择已为其设置了佣金的物料。 
13. 在 **数量** 字段中，输入一个数字。 记录行的净额。 它代表销售收入，在此示例中它是佣金计算的基础。  
14. 选择 **保存**。
15. 在操作窗格上，选择 **发票**。
16. 选择 **发票**。
17. 展开 **参数** 部分。
18. 在 **数量** 字段中，选择 **全部**。
19. 在 **过帐** 字段中选择 **是**。
20. 选择 **确定**，然后在下一个窗格中选择 **确定**。 过帐交易记录可能需要大概一分钟。 允许完成处理，并且不关闭页面。  

## <a name="review-the-registered-sales-commissions"></a>查看登记的销售佣金
1. 在操作窗格上，选择 **发票**，然后再次选择 **发票**。
2. 在操作窗格上，选择 **发票**，然后选择 **佣金交易记录**。

    - **概览** 选项卡显示应付给与开票的销售订单相关的销售人员的佣金金额行。 我们现在查看详细信息。  
    - 如果您使用“设置销售佣金规则”指南来设置 **佣金销售** 组，将有两位销售人员接受销售佣金，并且两人平分佣金。  
    - 在此示例中，佣金的总金额计算为销售收入百分比（订单行的净额）。  
3. 关闭该页面。
4. 选择 **凭证**。 您可以在凭证交易记录中查看已过帐到预定义的佣金费用的佣金金额和应付佣金金额。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]