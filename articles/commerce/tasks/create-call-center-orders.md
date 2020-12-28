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
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594228"
---
# <a name="create-call-center-orders"></a>创建呼叫中心订单

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。 此程序使用演示数据公司 USRT，旨在供销售订单职员使用。 先决条件：完成此过程的用户被设置为呼叫中心用户，并且使用至少一个源代码发布 Fabrikam 半年目录。

1. 转到 **Retail 和 Commerce \> 客户 \> 客户服务**。
2. 对于 **SearchText**，输入搜索条件以查找客户。
    * 对于此示例过程，输入“Karen”，然后选择 **选项卡**。  
3. 选择搜索。
    * 由于演示数据中仅有一名客户的姓名是“Karen”，因此将自动选中。  
4. 选择 **新建销售订单**。
5. 展开或折叠 **销售订单** 标题部分。
6. 选择目录的源代码。
    * 如果没有活动源代码，您可以跳过此步骤。  
7. 选择 **添加行**。
8. 对于 **物料编号**，输入物料搜索词。
    * 对于此示例过程，输入部分物料编号“8111”并按下选项卡。此操作将显示物料搜索窗口。  
9. 选择要添加到销售订单的产品。
10. 输入销售数量。
11. 选择 **创建**。
12. 选择 **完成** 以捕获客户付款。
13. 选择 **添加**。
    * “添加”链接位于“付款”选项卡中。如果重叠，则扩展“付款”选项卡。  
14. 选择付款方式。
    * 对于此程序，选择现金付款方法。  
15. 关闭该页面。
16. 输入金额。
    * 对于此过程，输入与订单余额相等的金额，可在“销售订单摘要”页面的金额字段左侧看到订单余额。 此操作将允许您以全额付清形式完成订单。  
17. 选择 **确定**。
18. 选择 **提交**。

## <a name="additional-resources"></a>其他资源

[按交货方式自定义事务电子邮件](../customize-email-delivery-mode.md)

[在 POS 上更改交货方式](../pos-change-delivery-mode.md)

