---
title: 审核应付帐款中的发票和关键数据
description: 本文介绍如何审核应付帐款中的账单和关键数据。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4525534f906322c7fe4c232f0f6da5b308829087
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775207"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>审核应付帐款中的账单和关键数据

[!include [banner](../../includes/banner.md)]

在您从供应商处收到针对采购订单上的货物或服务的发票时，该业务流程可能要求首先接收货物或服务，然后才能对发票进行审核以便付款。 在您开始前，请确保选择发票匹配 Configuration Key。 

在 **应付帐款参数** 页面，确保已选择 **启用发票匹配验证** 选项，已将 **过帐发票差异** 字段设置为 **要求审核**，以及已将 **行匹配政策** 字段设置为 **三向匹配**。

该程序适用于 USMF 演示公司。 应付帐款经理或会计经理将执行以下步骤。


## <a name="create-a-purchase-order"></a>创建采购订单
1. 转到 **所有采购订单**。
2. 单击 **新建**。
3. 在 **供应商帐户** 字段中，键入一个值。
4. 单击 **确定**。
5. 单击 **添加行**。
6. 在 **项目编号** 字段中，键入一个值。
7. 在“操作窗格”上，单击 **采购**。
8. 单击 **确认**。

## <a name="post-a-product-receipt"></a>将产品收据过帐
1. 在“操作窗格”上，单击 **接收**。
2. 单击 **产品收据**。
3. 在 **产品收据** 字段中，键入一个值。
4. 单击 **确定**。

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>记录供应商发票并与产品收据匹配
1. 在操作窗格上，单击 **发票 > 发票**。
2. 在 **编号** 字段中，键入一个值。
3. 单击 **默认订购数量**，以打开拖放对话框。
4. 在 **默认行数量** 字段中，选择一个选项。
5. 单击 **确定**。
6. 单击 **是**。
7. 单击 **匹配产品收据**。
8. 单击 **确定**。
9. 在操作窗格上，单击 **审核**。
10. 单击 **匹配详细信息**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
