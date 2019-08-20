---
title: 装运无仓库的销售订单
description: 本指南演示在将产品发运给客户时如何更新销售订单。
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62bbd65e2d80dca5a07b761e1aa76f1894b667c1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843305"
---
# <a name="ship-sales-orders-without-warehousing"></a>装运无仓库的销售订单

[!include [task guide banner](../../includes/task-guide-banner.md)]

本指南演示在将产品发运给客户时如何更新销售订单。 本指南适用于没有为仓库管理设置的履行流程（不论是基本还是高级仓库），因而不需要在装运前登记产品领料。 您可以使用演示数据公司 USMF 或您自己的数据运行该过程。 在这两种情况下，在您开始此任务前，为数量大于 1 的库存产品创建销售订单。 为了避免过帐错误，您需要检查您在订单上选择的站点和仓库中产品的现有数量包含订单数量。


## <a name="post-packing-slip-for-an-order"></a>过帐订单的装箱单
1. 转至“销售和营销”>“销售订单”>“所有销售订单”。
2. 在列表中，查找并选择您为此任务创建的订单。
3. 在列表中，单击所选行中的链接。
4. 在操作窗格，单击“领料和装箱”。
5. 单击“发布装箱单”。
6. 展开或收起“参数”部分。
7. 在“数量”字段中，选择“所有”。
    * 其他选项包括“现在交货”和“领料”。 如果订单行将部分交货，且订单行上的“现在交货”字段列有数量，您可以选择“现在交货”。 如果在您公司的订单履行流程中，领料作为单独的流程并根据领料单管理和登记，您可以选择“领料”。  
    * 确认“过帐”选项设置为“是”。  
8. 将“打印装箱单”选项设置为“是”。
    * “概览”选项卡包含在此过帐中生成的装箱单的列表。 如果您装运单个订单，通常只有一个装箱单。 但是，如果从不同站点装运订单行，过帐将自动拆分成相应的单据数。 这是强制性的，不可更改。 同样，如果订单行装运到不同的交货地址，且装运政策设置为需要拆分，过帐将会拆分成多个单据。  
9. 在“行”选项卡上，选择要装运的订单行上的行。
10. 在“更新”字段中，输入小于原始数量的数字。
11. 单击“确定”。
12. 单击“是”。
13. 关闭该页面。
14. 在“操作窗格”上，单击“选项”。
15. 单击“更改”视图。
16. 单击“标题”视图。
    * 如果订单上的所有行已全部装运，则订单状态从“未结”更改为“已交货”。  
    * 在此示例中，订单行已部分装运。 这就是订单仍处于未结状态的原因。     
    * 由于至少有一个订单行已装运，“单据状态”字段设置为“装箱单”。  
17. 在操作窗格上，单击“常规”。
18. 单击“行数量”。
19. 关闭该页面。
20. 在操作窗格中，单击“领料和装箱”。
21. 单击“装箱单”。
    * “装箱单日记帐”页含有您的订单生成的所有装箱单单据。 您可以在想要时查看并打印每个单据的详细信息。  

