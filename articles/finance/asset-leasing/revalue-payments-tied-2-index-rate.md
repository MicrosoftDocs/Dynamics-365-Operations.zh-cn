---
title: 重估与指数利率链接的租赁付款
description: 本主题描述了由于指数利率的变化而导致可变租赁付款发生变化时，对租赁使用权 (ROU) 负债进行的调整。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 83684afbd5e11b890a59bc1469ddefffd1777c4e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440945"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>重估与指数利率链接的租赁付款

[!include [banner](../includes/banner.md)]

本主题描述了由于指数利率的变化而导致可变租赁付款发生变化时，对租赁使用权 (ROU) 负债进行的调整。 租赁负债和使用权资产将进行调整，以计入新的付款金额。 根据会计准则编纂专题 842 (ASC 842)（这是美国公认会计准则 (US GAAP) 中的准则），除非现金流发生了更多变化，否则在由于指数利率改变导致付款增加或减少时，只有可变付款会改变。 这些其他变化可能包括与利率有关的租赁条款的变化。 有关详细信息，请参阅 ASC 842-10-55-225 和国际财务报告准则 16 (IFRS 16) 第 42(b) 段。

## <a name="adjust-lease-payments"></a>调整租赁付款

按照以下步骤重估与指数利率链接的租赁付款。

1. 要运行租赁指数重估流程，请转到 **资产租赁 \> 定期 \> 指数利率重估**。

    将显示 **指数利率重估** 页，其中显示所有先前已运行的租赁指数重估流程。 此页面上的信息包括从编号规则设置生成的流程 ID、法人、已调整的租赁帐簿数量、IFRS 16 租赁的总负债调整，以及针对 ASC 842 租赁调整的可变付款总额。

2. 要运行重估，请在操作窗格上选择 **租赁指数重估**。

    将显示 **指数重估参数** 对话框。 可在此处筛选并选择在选择要重估的租赁时应使用哪些租赁、租赁组或其他条件。 此外，还可以在 **后台运行** 选项卡上设置指数重估流程，以使其批量运行。

4. 选择用于选择后台处理中应包括的租赁的筛选器，然后选择 **确定**。

    将显示 **指数利率重估预览** 对话框，其中显示将重估的租赁。 还显示资产和负债调整或可变付款调整。
    
5. 要防止重估租赁，请选择 **应该** 重估的租赁。 如果不选择任何租赁，将重估所有租赁。 完成后，选择 **确定** 重估租赁付款。
6. 要查看为特定指数重估流程创建的交易，请选择流程 ID，然后选择 **交易**。

    将显示一个对话框，其中显示处理期间创建的交易的详细信息。

> [!NOTE]
> 只能重估重估日期在系统日期当天或之前的租赁。 系统将自动忽略重估日期晚于系统日期的所有租赁。

## <a name="asc-842-leases--index-revaluation"></a>ASC 842 租赁 – 指数重估

要查看租赁重估过程对 ASC 842 租赁的影响，请打开租赁的付款计划。 该页面仅显示由于指数重估而在重估日期更改之日或之后更改的可变付款。 摊销和折旧计划保持不变。 当您创建具有可变付款的发票时，可变付款会借记到可变付款过帐科目。 此外，根据租赁帐簿的设置，可变付款金额还会添加到直接过帐到供应商或过帐到 Notes 应付帐款的贷方条目中。

租赁详细信息页面上的付款计划行会自动使用新行更新，该行指示新的指数利率。 此外，还会有一列显示该行是手动创建的，还是通过指数重估流程创建的。

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16 租赁 – 指数重估

要查看租赁重估过程对 IFRS 16 租赁的影响，请打开调整后租赁的租赁详细信息。 **租赁期** 和 **资产使用年限** 字段已更新，以反映从开始日期或修改日期到重估日期的过程。 此外，付款计划行已更新，以反映租赁中的新付款、新指数利率和行的创建方式。

您可以查看从重估日期开始新生成的付款计划，并显示更新后的付款总额。 还创建了新的租赁负债摊销计划和资产折旧计划，以反映调整后的付款计划。

日记帐条目已将调整日记帐条目自动过帐到与指数重估相关的租赁付款变更的科目。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]