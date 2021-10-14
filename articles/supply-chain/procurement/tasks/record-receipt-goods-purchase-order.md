---
title: 记录采购订单上的收货
description: 本主题介绍如何直接在采购订单中记录收货。
author: Henrikan
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ec37082ffa7816d1b07cadc595eec6e8373920a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565324"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>记录采购订单上的收货

[!include [banner](../../includes/banner.md)]

本主题介绍如何直接在采购订单中记录收货。 还可以在仓库中登记产品收货，以后再记录到采购订单中。 此任务通常由代购代理或应付账款协调员执行。 可以在 USMF 演示数据公司中使用本指南中的示例。 此示例包括简单采购订单的创建步骤，以便您将此过程用作任务指南。 如果您使用此过程和您自己的数据，则可以从 **记录收货** 子任务着手。


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>为收货准备新采购订单
1. 转到 **导航窗格 > 模块 > 采购 > 采购订单 > 所有采购订单**。
2. 选择 **新建**。
3. 在 **供应商帐户** 字段中输入 `US-101`。
4. 选择 **确定**。
5. 在 **物料编号** 字段中输入 `M0001`。
6. 在 **数量** 字段中，输入 `5`。
7. 在操作窗格上，选择 **采购**。
8. 选择 **确认**。

## <a name="record-receipt-of-goods"></a>记录收货
1. 在操作窗格上，选择 **接收**。
2. 选择 **物料收货**。 **数量** 字段用于为要接收的数量选择不同选项。 例如，如果某个数量以前在仓库中已登记，可以选择 **登记数量**。 对于此示例，请使用 **订购数量** 的值。
3. 展开 **概览** 部分。
4. 在 **物料收货** 字段中键入任何值。 此字段用于输入将用作产品收货日记帐的凭证的参考。  
5. 展开 **行** 部分。
6. 将 **数量** 设置为“4”。 您可以在此处手动指定订单中各行将收到的数量。  
7. 选择 **确定**。 此货物现已在采购订单中记录为已接收，并已创建了单据格式的产品收货日记帐以体现此信息。 可使用“产品收货”操作审查随采购订单创建的日记帐，以了解产品的收货内容和收货时间。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]