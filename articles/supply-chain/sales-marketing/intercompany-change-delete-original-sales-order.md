---
title: 更改或删除原始内部公司销售订单
description: 本主题介绍了如何更改和删除原始销售订单功能
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
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548122"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>更改或删除原始内部公司销售订单

[!include [banner](../../includes/banner.md)]

更改销售订单时，您的更改会自动与相关内部公司采购订单和内部公司销售订单同步。

> [!NOTE]
> 外部供应商的采购订单不受您做出的任何更改的影响；与外部供应商的采购订单行相关的原始销售订单行也不受影响。

以下表汇总了您可以做出的更改和预期结果。

| 操作​ | 结果 |
|---|---|
| 删除原始销售订单。 | 相关的内部公司采购订单和内部公司销售订单也随之删除。 如果订单的状态为 **领料单** 或处在更靠后的流程中，则您不能删除销售订单。 |
| 删除原始销售订单行。 | 相关的内部公司采购订单行和内部公司销售订单行也随之删除。 如果订单的状态为 **领料单** 或处在更靠后的流程中，则您不能删除销售订单行。 |
| 将新销售订单行添加到原始销售订单。 | 将在内部公司采购订单和内部公司销售订单中添加新销售订单行。 |
| 更改原始销售订单行中的数量。 | 数量将内部公司采购订单行和内部公司销售订单行进行同步。 将在所有订单中重新计算净金额。 |
| 对原始销售订单禁用直接交运。 | 如果内部公司销售订单行已达到 **领料单**、**输出订单** 或 **领料单日记帐** 的最低状态，则无法更改原始销售订单上的 **直接交货** 字段。 将内部公司采购订单上的交货地址更改为标准交货地址（标准采购订单交货地址）。 此外，将内部公司采购订单行更改为该行的标准交货地址。 这些更改都会与内部公司销售订单和订单行同步。 将原始销售订单的所有行上的交货类型更改为 **无**，并将该字段与内部公司采购订单行进行同步。 外部供应商的采购订单不受影响；与外部供应商的采购订单行相关的原始销售订单行也不受影响。 内部公司采购订单和订单行中的交货日期，以及内部公司销售订单和订单行中请求的接收日期/装运日期都将更新。 |
| 对原始销售订单启用直接交运。 | 如果内部公司销售订单行已达到 **领料单**、**输出订单** 或 **领料单日记帐** 的最低状态，则无法更改原始销售订单上的 **直接交货** 字段。 内部公司采购订单中的交货地址更改为原始销售订单中的交货地址，并与内部公司销售订单保持同步。 将原始销售订单的所有行上的交货类型更改为 **直接交货**，并将该字段与内部公司采购订单行进行同步。 每个原始销售订单行中的交货地址将与内部公司采购订单行和内部公司销售订单行保持同步。 内部公司采购订单和订单行中的交货日期，以及内部公司销售订单和订单行中请求的接收日期/装运日期都将更新。 |
| 将单据添加到原始销售订单头和订单行。 | 单据将复制到内部公司采购订单和内部公司销售订单。 |
| 更改或删除单据。 | 如果更改或删除单据，将会相应地更改或删除内部公司采购订单和内部公司销售订单上的相应单据。 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]