---
title: 同步处置代码
description: 本主题介绍了内部公司商务的处置代码同步
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
ms.openlocfilehash: 27b587e576900f2b7f7fed7ee2a27a282306f0fe
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671749"
---
# <a name="synchronize-intercompany-disposition-codes"></a>同步内部公司处置代码

[!include [banner](../../includes/banner.md)]

为了支持内部公司退货，Microsoft Dynamics 365 Supply Chain Management 使您能够将外部定义的处置代码映射到相应的内部处置代码。 在设置一个内部公司业务关系链时，彼此映射的两个公司中的处置操作必须相同。 如果它们不同，则同步过程将不成功。

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>关于 3 边直接退货的处置代码

处置代码从内部公司销售订单行同步到原始销售订单行。 但是，同步仅直接影响原始销售订单行。 此影响是基于在公司 A 中设置的处置代码和杂项费用删除杂项行费用。公司 A 是创建退货单的公司。

在 3 边直接交运链中，在内部公司销售订单行上支持所有处置操作。 但是，如果产品退回给客户，您应该确认退货单中的交货地址与在原始订单中指定的客户交货地址匹配。

> [!NOTE]
> 对于采购订单，则不存在处置代码。 因此，处置代码从内部公司销售订单到原始退货单的同步必须在销售订单之间执行。

## <a name="replacing-returned-items"></a>更换退回物料

如果更换某一退回物料，并且已在公司 B 中创建了更换单，将无法选择处置代码，并且不会在公司 A 中创建附加的更换单。

## <a name="rules-for-intercompany-direct-deliveries"></a>内部公司直接交运的规则

以下一般规则适用于涉及内部公司直接交运的方案中的原始退货单。

- 如果针对原始销售订单行的基础处置操作是“贷记并报废”、“贷记”或“返还客户”，则适用“贷记”处置操作。 但是，“返还客户”操作代码会将现有行上的净额和内部公司销售订单的新同步的行上的净额设置为 0（零）。 此外，报废行始终不同步。 在将某一行添加到内部公司销售订单时，始终不为具有正数量和报废处置操作（例如，“贷记和报废”或“更换和报废”）的销售订单同步该行。
- “贷记和更换”或“报废和更换”的基础处置操作不会被否决。 它视视为“贷记和更换”或“报废和更换”的基础处置操作。 即使没有在公司 A 中创建报废行，并且没有在公司 B 中创建更换单（接收退回物料的公司），此规则也适用。 只有在执行装箱单更新时，才在公司 A 中创建更换单。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
