---
title: 内部公司货币转换
description: 本文说明内部公司交易的货币转换
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851469"
---
# <a name="intercompany-currency-conversions"></a>内部公司货币转换

[!include [banner](../../includes/banner.md)]

当原始销售订单和内部公司采购订单上的货币代码不同时，将对以下字段执行货币转换（如果启用了同步）：

- **单位价格**
- **销售费用** 或 **采购费用**
- **折扣**
- **多行折扣**

然后，这些字段与内部公司销售订单行进行同步。

但是，因为内部采购订单和内部销售订单上的币种始终同步，所以以下字段不需要使用币种转换就能进行同步：

- **单位价格**
- **销售费用** 或 **采购费用**
- **折扣**
- **折扣率**
- **多行折扣**
- **多行折扣率**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
