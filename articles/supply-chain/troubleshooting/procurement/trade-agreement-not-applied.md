---
title: 贸易协议条件不应用于导入的订单行
description: 贸易协议价格和折扣不应用于通过数据管理导入的销售或采购订单行
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
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475716"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>贸易协议条件不应用于导入的订单行

## <a name="symptoms"></a>故障特征

适用于销售或采购订单行的贸易协议不应用于通过数据管理导入的行。 但是，相同的贸易协议应用于手动创建的销售或采购订单行。

## <a name="cause"></a>原因

如果通过数据管理导入的采购订单行已经包含价格信息，将不会重新评估这些行的贸易协议。 例如，如果 **单行折扣率** 或为某行设置了价格和折扣值，则不会查找该行的贸易协议。

## <a name="workaround"></a>解决方法

此行为是预期的，对于销售订单和采购订单是相似的。

解决方法是，导入采购订单行而不设置任何价格信息。 然后将应用贸易协议，并将基于定义的贸易协议更新采购订单行。
