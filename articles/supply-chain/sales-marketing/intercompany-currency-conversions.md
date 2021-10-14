---
title: 内部公司货币转换
description: 本主题说明内部公司交易的货币转换
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548134"
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
