---
title: 为退货执行发票更新
description: 此功能支持组织选择采用的业务流程，即同时由同一人对退货单和销售订单开票。
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 736496a0499e70987f80f3d4687414371606cd8c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578744"
---
# <a name="perform-invoice-updates-for-returns"></a>为退货执行发票更新 

[!include [banner](../includes/banner.md)]


退货单是一种标记为退回订单的销售订单。 因此，**所有销售订单** 列表页用于生成退货单的发票，而不是从 **退货单** 窗体中生成。 此功能支持组织选择采用的业务流程，即同时由同一人对退货单和销售订单开票。

由于退回物料的发票用于负金额，称作贷方通知单。

在您为批处理设置发票更新时，**退回订单** 类型的销售订单必须具有 **已接收** 的退货单行状态，指示该订单的装箱单已更新。

## <a name="post-an-invoice-for-a-return-order"></a>过帐退货单的发票

1.  单击 **应收帐款** \> **通用** \> **销售订单** \> **所有销售订单**。

2.  选择在 **订单类型** 字段中显示的 **退回订单** 的销售订单。

3.  在操作窗格 **发票** 选项卡的 **常规** 组中，单击 **发票**。

4.  在 **参数** 选项卡上，选中 **过帐** 复选框。

5.  查看窗体中的信息，并进行必要的更改。

6.  单击 **确定**。 – 贷方通知单已过帐。

## <a name="see-also"></a>请参阅

[退货的装箱单更新](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]