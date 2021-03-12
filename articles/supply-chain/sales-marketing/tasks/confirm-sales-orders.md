---
title: 确认销售订单
description: 该过程说明了如何确认销售订单。
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c09ef2f78353a75ecb2dfffef6965cb1ac0873
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991807"
---
# <a name="confirm-sales-orders"></a>确认销售订单

[!include [banner](../../includes/banner.md)]

该过程说明了如何确认销售订单。 将会向您显示如何确认单个订单，以及如何一次确认多个订单。 这些任务通常由销售订单处理员完成。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。 在您开始前，确保同一客户的若干未结销售订单可用。 如果您正在使用 USMF，您可以使用客户 US-027。


## <a name="confirm-a-single-sales-order"></a>确认单一销售订单
1. 转到 **导航窗格 > 模块 > 销售和营销 > 销售订单 > 所有销售订单**。
2. 在列表中，查找并选择您想要确认的订单。
3. 单击销售订单编号上的链接，以打开选中的订单。
4. 在 **操作窗格** 上，单击 **销售**。
5. 单击 **确认销售订单**。
6. 展开 **参数** 部分。 确保将 **过帐** 选项设置为“是”。  
7. 将 **打印确认选项** 设置为“是”。 **检查信用额度** 字段规定了用于计算客户的剩余信用额度的方法。 该选项默认从“应收账款参数”页复制而来。 如果在确认特定销售订单时，您想要跳过信用额度检查，可以将 **检查信用额度** 设置为“无”。 但是，您应该清楚，即使此字段被设置为“无”，如果客户主数据中的 **强制信用额度** 选项被选中，信用额度检查仍将会执行。 
8. 单击 **确定**。
9. 单击 **是**。
10. 关闭该页面。
11. 在 **操作窗格** 上，单击 **选项**。
12. 单击 **更改视图**。
13. 单击 **标题视图**。 在确认订单时，**文档状态** 设置为“确认”。 
14. 在 **操作窗格** 上，单击 **销售**。
15. 单击 **销售订单确认**。
16. 关闭该页面。

## <a name="confirm-multiple-sales-orders-at-once"></a>一次确认多个销售订单
1. 转到 **销售和营销 > 销售订单 > 订单确认 > 确认销售订单**。
2. 单击 **选择**。
3. 在 **范围** 选项卡的列表中，查找并选择引用 **客户帐户** 字段的记录。
4. 在 **标准** 字段中，单击下拉按钮以打开查找。
5. 在列表中，查找并选择拥有您想要批量确认的多个订单的客户帐户。 如果正在使用 USMF，您可以选择帐户 US-027。  
6. 单击 **确定**。
    - **概述** 选项卡会显示与查询条件匹配的订单列表。 这些将包括在确认中。  
    - **参数** 部分的 **汇总更新** 字段规定了将多个订单汇总到一个确认文件所需的参数。 该选项默认从 **应收账款参数** 页中 **汇总更新设置的默认值** 复制而来。  
7. 在 **汇总更新** 字段中，选择“订单”。 创建汇总更新所需的最少参数是 **发票帐户** 和 **币种**。 这意味着不允许汇总更新拥有不同的发票帐户和不同的币种。 附加参数可以在“汇总更新参数”页内设置，并且 **汇总更新参数** 页可以从 **应收账款参数** 页访问。 
8. 在 **销售订单** 字段中，单击下拉按钮以打开查找。
9. 在列表中，选择您想将其纳入汇总订单的销售订单。
10. 单击 **排列**。
11. 单击 **确定**。
12. 单击 **确定**。

