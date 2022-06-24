---
title: 添加付款金额类型
description: 本文介绍如何在资产租赁中设置付款金额类型。
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03fc903e6cfe78ef2fed7e3a0744a8f809f6892d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891600"
---
# <a name="add-payment-amount-types"></a>添加付款金额类型

[!include [banner](../includes/banner.md)]

本文介绍如何在资产租赁中设置付款金额类型。 这样，您可以详细列出租赁付款金额，而不是在付款计划行上添加一次性付款总额。

要添加付款金额类型，请执行以下步骤。

1. 转到 **资产租赁 \> 设置 \> 付款金额类型**。
2. 选择 **新建**。
3. 输入新的付款类型和说明。

> [!NOTE]
> 对于 IFRS 16 指数重估，您必须创建一个付款金额类型并将其标记为 **用于 IFRS16 指数重估**。 对 IFRS 16 帐簿运行指数重估流程时，将使用此付款金额类型，并且它将考虑由于指数重估流程而发生的更改。
>
> 当租赁中的 **付款分解** 选项设置为 **是** 时，如果运行 IFRS 16 指数重估，但没有 IFRS 16 付款类型，则将不会完成该流程。

只能将一条记录标记为 **用于 IFRS16 指数重估**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
