--- 
title: "创建呼叫中心订单"
description: "此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: b2e986df1e089ef2a394d0e9d9236d39f2726c77
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="create-call-center-orders"></a>创建呼叫中心订单

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

此程序会逐步演示如何查找客户，创建新订单，检索产品和收取客户的付款。 此程序使用演示数据公司 USRT，旨在供销售订单职员使用。 先决条件：完成此过程的用户被设置为呼叫中心用户，并且使用至少一个源代码发布 Fabrikam 半年目录。

1. 转至“零售和商业”>“客户”>“客户服务”。
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


