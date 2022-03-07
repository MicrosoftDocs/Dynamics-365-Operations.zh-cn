---
title: 退货的装箱单更新
description: 在退回物料可以入库前，它们所属于的订单的装箱单必须更新。
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f586537aa2d4cb47b0e55e76e401ea6852e1d60
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580376"
---
# <a name="packing-slip-updates-for-returns"></a>退货的装箱单更新  

[!include [banner](../includes/banner.md)]


在退回物料可以入库前，它们所属于的订单的装箱单必须更新。 就像发票更新流程是对财务交易记录进行的更新一样，装箱单更新流程是对库存记录的物理更新；这意味着它对库存进行更改。 在退货时，分配给处置操作的步骤在装箱单更新期间执行。

装箱单更新可通过物料到达日志或退货单进行处理。

作为过账装箱单的流程，可以选择将来自客户装运文档的装箱单参考编号与订单行相关联。 此关联可选和仅供参考。 它并不创建任何交易记录更新。

如果不是所有的预期退货物料都已到达，则应只包括在装箱单更新中接收的数量。 保留订单上的剩余物料，直至其余的退货装运已到达。

如果某一物料在经过检验后发送回装运和接收部门，例如，在检验人员不知道在库存中何处存储物料时，必须更新相应的装箱单，正确登记和操作指定为检验结果的处置代码。

在更新来自销售协议的退回物料的装箱单时，自动更新该物料的销售协议承诺反映数量或金额的变化。 

## <a name="see-also"></a>请参阅

[为退货执行发票更新](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]