---
title: 记录供应商发票和匹配接收的数量
description: 在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be1e818e8a97684248c9c0b9d43c39e631f855f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979255"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>记录供应商发票和匹配接收的数量

[!include [banner](../../includes/banner.md)]

在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。 在您开始前，请确保选择发票匹配 Configuration Key。 

在应付帐款参数页面，确保已选择“启用发票匹配验证”选项，已设置“过帐发票差异”字段为“请求批准”，以及已设置“行匹配政策”字段为三向匹配。

该程序适用于 USMF 演示公司。 应付帐款经理或会计经理将执行以下步骤。


## <a name="create-a-purchase-order"></a>创建采购订单
1. 转到“所有采购订单”。
2. 单击“新建”。
3. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
4. 在“供应商帐户”字段中，输入一个供应商帐户。
5. 单击“确定”。
6. 单击“添加行”。
7. 在“项目编号”字段中，输入一个值。
8. 在操作窗格上，单击“采购”。
9. 单击“确认”。

## <a name="post-a-product-receipt"></a>将产品收据过帐
1. 在操作窗格上，单击“接收”。
2. 单击“产品收据”。
3. 在列表中，标记所选的行。
4. 在“产品收据”字段中，输入一个值。
5. 单击“确定”。

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>记录供应商发票并与产品收据匹配
1. 在操作窗格上，单击“发票”。
2. 单击“发票”。
3. 在“编号”字段中，输入一个值。
4. 单击“默认订购数量”，以打开拖放对话框。
5. 在“默认行数量”字段中，选择一个选项。
6. 单击“确定”。
7. 单击“是”。
8. 单击“匹配产品收据”。
9. 单击“确定”。
10. 在操作窗格上，单击“审核”。
11. 单击“匹配详细信息”。

