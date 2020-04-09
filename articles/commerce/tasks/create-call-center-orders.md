---
title: 创建呼叫中心订单
description: 此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141422"
---
# <a name="create-call-center-orders"></a>创建呼叫中心订单

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。 此程序使用演示数据公司 USRT，旨在供销售订单职员使用。 先决条件：完成此过程的用户被设置为呼叫中心用户，并且使用至少一个源代码发布 Fabrikam 半年目录。

1. 转至“Retail 和 Commerce”>“客户”>“客户服务”。
2. 在 SearchText 字段中，输入检索条件以查找客户。
    * 对于此示例程序，键入“Karen”，然后按下选项卡。  
3. 单击“搜索”。
    * 由于演示数据中仅有一名客户的姓名是 Karen，因此它们将被自动选中。  
4. 单击“新建销售订单”。
5. 扩展或折叠“销售订单标题”部分。
6. 选择目录的源代码。
    * 如果没有活动源代码，您可以关闭源字段并跳过此步骤。  
7. 单击“添加行”。
8. 在“物料编号”字段中，输入物料搜索词。
    * 对于此示例过程，输入部分物料编号“8111”并按下选项卡。这将弹出物料检索窗口。  
9. 选择产品以添加到销售订单
10. 输入销售数量。
11. 单击“创建”。
12. 单击“完成”以获取客户付款。
13. 单击“添加”。
    * “添加”链接位于“付款”选项卡中。如果重叠，则扩展“付款”选项卡。  
14. 选择付款方式。
    * 对于此程序，选择现金付款方法。  
15. 关闭该页面。
16. 输入金额。
    * 对于此程序，输入与订单余额相等的金额，订单余额可在“销售订单摘要”页面的金额字段左侧看到。 这将允许您以全部付讫形式完成订单。  
17. 单击“确定”。
18. 单击“提交”。

