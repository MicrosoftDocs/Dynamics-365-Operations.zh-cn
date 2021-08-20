---
title: 装运无仓库的销售订单
description: 此主题介绍在将产品发运给客户时如何更新销售订单。
author: omulvad
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0760ff5810bb832e25d6a2d473b3cda703872a05de4936191f91664406fe18c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767308"
---
# <a name="ship-sales-orders-without-warehousing"></a>装运无仓库的销售订单

[!include [banner](../../includes/banner.md)]

此主题介绍在将产品发运给客户时如何更新销售订单。 本指南适用于没有为仓库管理设置的履行流程（不论是基本还是高级仓库），因而不需要在装运前登记产品领料。 您可以使用演示数据公司 USMF 或您自己的数据运行该过程。 在这两种情况下，在您开始此任务前，为数量大于 1 的库存产品创建销售订单。 为了避免过帐错误，您需要检查您在订单上选择的站点和仓库中产品的现有数量包含订单数量。

## <a name="post-packing-slip-for-an-order"></a>过帐订单的装箱单
1. 在导航窗格中，转到 **模块 > 销售和营销 > 销售订单 > 所有销售订单**。
2. 在列表中，查找并选择您为此任务创建的订单。
3. 在操作窗格中，选择 **领料和装箱**。
4. 选择 **将装箱单过帐**。
5. 展开或收起 **参数** 部分。
6. 在 **数量** 字段中，选择 **全部**。
    - 其他选项包括 **现在交货** 和 **领料**。 如果订单行将部分交货，且订单行上的 **现在交货** 字段列有数量，您可以选择 **现在交货**。 如果在您公司的订单履行流程中，领料作为单独的流程并根据领料单管理和登记，您可以选择 **领料**。  
    - 确认 **过帐** 选项设置为 **是**。  
7. 将 **打印装箱单** 选项设置为 **是**。 **概览** 选项卡包含在此过帐中生成的装箱单的列表。 如果您装运单个订单，通常只有一个装箱单。 但是，如果从不同站点装运订单行，过帐将自动拆分成相应的单据数。 这是强制性的，不可更改。 同样，如果订单行装运到不同的交货地址，且装运政策设置为需要拆分，过帐将会拆分成多个单据。  
8. 在 **行** 选项卡上，选择要装运的订单行上的行。
9. 在 **更新** 字段中，输入小于原始数量的数字。
10. 选择 **确定**。
11. 选择 **是**。
12. 关闭该页面。
13. 在操作窗格上，选择 **选项**。
14. 选择 **更改视图**。
15. 选择 **标题视图**。
    - 如果订单上的所有行已全部装运，则订单状态从“未结”更改为“已交货”。  
    - 在此示例中，订单行已部分装运。 这就是订单仍处于未结状态的原因。     
    - 由于至少有一个订单行已装运，**单据状态** 字段设置为“装箱单”。  
16. 在操作窗格上，选择 **常规**。
17. 选择 **行数量**。
18. 关闭该页面。
19. 在操作窗格中，选择 **领料和装箱**。
20. 选择 **装箱单**。 **装箱单日记帐** 页含有您的订单生成的所有装箱单单据。 您可以在想要时查看并打印每个单据的详细信息。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]