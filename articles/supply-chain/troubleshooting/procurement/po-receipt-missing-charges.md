---
title: 采购订单收货不包括所有费用
description: 采购订单收货不包括所有费用
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475646"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>采购订单收货不包括所有费用

## <a name="symptoms"></a>故障特征

收到采购订单时，收据中未必包含所有费用。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 在 **采购参数** 页上的 **交货** 选项卡上，确保将 **在产品收货时生成费用** 选项设置为 *是*。
1. 创建包含费用的采购订单。
1. 确认采购订单。
1. 接收采购订单。
1. 查看收货总计，并将其与预期总计进行比较。
1. 请注意，并非所有费用都包含在采购订单收货中。

## <a name="resolution"></a>解决方法

解决方法取决于设置杂项费用的方式。 有关如何设置杂项费用以满足您的要求的信息，请参阅以下博客文章：[在产品收货时过帐杂项费用](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。
