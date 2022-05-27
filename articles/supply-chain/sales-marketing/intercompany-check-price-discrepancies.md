---
title: 检查内部公司订单价格差异
description: 本主题介绍了如何检查内部公司订单价格差异
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3167077e653f2316f5ce54c2a07ef9c2978ecebb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678309"
---
# <a name="check-intercompany-order-price-discrepancies"></a>检查内部公司订单价格差异

[!include [banner](../../includes/banner.md)]

您可以使用此过程来检查内部公司订单的价格差异。

1. 转到 **采购 \> 定期 \> 清理 \> 检查内部公司订单价格差异**。
1. 设置批处理作业，如果您需要，然后选择 **确定** 来检查内部公司销售订单和采购订单的价格和折扣。 否则，选择 **取消** 来关闭页面，不执行检查。

    > [!TIP]
    > 如果存在任何同步问题或与价格有关的问题，这些将在要显示的参考消息中列出。 您可以打印参考信息用于参考。

1. 在参考消息中，选择相关行来打开当前法人的订单。 通过选择 **内部公司**，然后选择 **内部公司采购订单** 或 **内部公司销售订单**，在相关法人中打开订单。

    > [!NOTE]
    > 若要允许更新内部公司订单：
    >
    > 1. 转到 **应付帐款 \> 客户 \> 所有客户**。
    > 1. 在“操作”窗格上，选择 **常规** 选项卡，然后选择 **内部公司**。
    > 1. 在 **内部公司** 页面上，选择 **采购订单策略** 或 **销售订单策略**。
    > 1. 在这两个区域中选择 **允许编辑价格** 和 **允许编辑折扣**。

1. 打开您要保留价格的相关内部公司订单。
1. 对于每一订单行，更改该行的 **单价** 字段，然后将其更改回原始值。 反复更改该行的 **折扣** 字段，并且反复更改相关的 **采购费用** 或 **销售费用** 字段。 对这些值的这一反复更改将触发价格、折扣和杂项费用从该内部公司订单行到引用的内部公司订单行的同步，以便将自动对它们进行调整。

    > [!NOTE]
    > 只有在尚未对内部公司销售订单进行开票的情况下，此同步才有效。 如果该内部公司销售订单已按发票过帐，并且已创建用户发票日志，则必须通过将价格、折扣和杂项费用设置为等于内部公司客户发票日志上的对应项，来直接对内部公司采购订单行执行更改。 如果未这样做，则无法对内部公司采购订单进行按发票过帐，因为在订单合计中将存在不匹配的情况。

1. 重复该过程，直到所有内部公司采购订单和销售订单都已同步。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
