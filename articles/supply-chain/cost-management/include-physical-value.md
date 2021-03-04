---
title: 包括实际成本
description: 您使用“物料模型组”页的“库存模型”选项卡上的“包括实际成本”复选框来指定在为物料计算移动平均成本价时是否考虑了实际更新的交易记录。
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6e70a40b15bf08d88958cbf3ee3e82ed63e7a48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422977"
---
# <a name="include-physical-value"></a>包括实际成本

[!include [banner](../includes/banner.md)]

您使用“物料模型组”页的“库存模型”选项卡上的“包括实际成本”复选框来指定在为物料计算移动平均成本价时是否考虑了实际更新的交易记录。

**包括实际成本** 复选框具有以下值。

| 值    | 结果                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| 已选择 | 实际更新的交易记录和财务更新的交易记录都用于计算移动平均成本价。 |
| 清除  | 只有财务更新交易记录用于计算移动平均成本价。                                     |

根据您使用的库存模型，此复选框具有略微不同的效果。

-   如果您在使用 FIFO（先进先出）、LIFO（后进先出）或 LIFO 日期库存模型时选择了 **包括实际成本** 复选框，则库存结转也将对实际更新的交易记录做出调整。
-   如果在您使用这些库存模型时没有选择 **包括实际成本** 复选框，则库存结转只对财务更新交易记录进行结算。
-   当您使用了加权平均或加权平均日期库存模型时，不管您是否选择了 **包括实际成本** 复选框，库存结转都只结算财务更新的交易记录。

**示例 1** 您选中 **包括实际成本** 复选框并收到以下采购订单：

-   数量为 2 且成本价为 USD 10.00 的采购订单已更新装箱单。
-   数量为 3 且成本价为 USD 12.00 的采购订单已更新发票。

在此示例中，移动平均成本价将是 USD 11.20 = (2x10+3x12)/(2+3)，因为物理更新的交易记录和财务更新的交易记录都用于计算该成本价。 

**示例 2** 您未选中 **包括实际成本** 复选框，物料设置的成本价是 USD 10.00。 

-   您收到已更新装箱单的数量为 20 且成本价为 USD 12.00 的采购订单。

当过账销售订单时，过账的成本金额为 USD 10.00，因为移动平均成本价将不包括实际过账的交易记录。 

> [!NOTE]
> 对于比较，如果为此物料选中 **包括实际成本** 复选框，在过帐某一销售订单时，过帐的成本金额将是 USD 12.00。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]