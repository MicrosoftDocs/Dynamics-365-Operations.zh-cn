---
title: 已实际接收的采购订单未显示在库存结帐报表中
description: 已实际接收的采购订单未显示在“检查未结数量”库存结帐报表中。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026303"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>已实际接收的采购订单未显示在库存结帐报表中

知识库编号：4612595

## <a name="symptoms"></a>故障特征

已实际接收的采购订单未显示在 **检查未结数量** 库存结帐报表中。

## <a name="resolution"></a>解决方法

**检查未结数量** 报表显示截至所选结帐日期，无法根据财务更新的库存收货进行结算的发货交易。 您可以选择在报表中包括实际收货。 在这种情况下，如果实际收货可以覆盖无法结算的发货交易，实际收货将显示。 有关详细信息，请参阅[准备执行库存结帐](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close)。
