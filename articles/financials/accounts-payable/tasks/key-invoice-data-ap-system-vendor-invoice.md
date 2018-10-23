--- 
title: "使用供应商发票的 AP 系统中的重要发票数据"
description: "本任务指南将帮助您根据采购订单创建供应商发票，并查看采购订单、收据和发票的匹配结果（三向匹配）。"
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a>使用供应商发票的 AP 系统中的重要发票数据

[!include [task guide banner](../../includes/task-guide-banner.md)]

本任务指南将帮助您根据采购订单创建供应商发票，并查看采购订单、收据和发票的匹配结果（三向匹配）。


## <a name="create-a-purchase-order"></a>创建采购订单
1. 转到“应付账款”>“采购订单”>“所有采购订单”。
2. 单击“新建”。
3. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
4. 查找并选择一个供应商。 例如，滚动到 US-104。
5. 选择供应商 US-104。
6. 单击“确定”。
7. 在“物料编号”字段中，单击下拉按钮以打开查找。
8. 选择一个库存物料。 例如，选择物料编号 1000。
9. 展开或折叠“行详细信息”部分。
10. 单击“设置”选项卡。
    * 您可以覆盖匹配政策，改为使用不匹配、双向匹配或三向匹配。  
11. 展开或折叠“行详细信息”部分。
12. 在操作窗格上，单击“采购”。
13. 单击“确认”。

## <a name="receive-the-products"></a>接收产品
1. 在操作窗格上，单击“接收”。
2. 单击“产品收据”。
3. 在“产品收据”字段中，输入产品收据编号。 例如，输入 PR123。
4. 单击“确定”过帐产品收据。
5. 关闭该页面。

## <a name="create-a-vendor-invoice"></a>创建供应商发票
1. 转到“应付账款”>“采购订单”>“已接收但未开票采购订单”。
2. 选择您创建的采购订单。
3. 在“操作窗格”中，单击“发票”。
4. 单击“发票”。
5. 在“编号”字段中，输入发票编号。
6. 在“发票描述”字段中，键入一个值。
7. 在“发票日期”字段中，输入日期。
8. 在“单价”字段中，输入 1200。
9. 单击“添加行”。
10. 在“物料编号”字段中，单击下拉按钮以打开查找。
11. 在列表中，找到安装费用项目编号。 例如：S0001
12. 选择安装费用项目编号。
    * 请注意，自您作出更改后，尚未执行匹配。  
13. 单击“更新匹配状态”。
14. 在操作窗格上，单击“审核”。
15. 单击“匹配详细信息”。
    * 列有服务的新行并不需要匹配，因此状态仍为“不执行”。  
16. 为您接收的库存物料选择产品收据。
    * 已就产品收据匹配行，但数量或价格不匹配，所以匹配失败。  
17. 在“单位价格”字段中，输入一个数字。
    * 由于单位价格匹配，因而状态更新为“已通过”。 如果您的政策允许有差异，或匹配只是一个警告，您仍然可以过帐发票。  
18. 关闭该页面。
19. 单击“过帐”。
20. 关闭窗体。
    * 请注意，采购订单不再列为“已接收但未开票”。  


