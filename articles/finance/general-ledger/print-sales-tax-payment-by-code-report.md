---
title: 按代码报告打印销售税付款
description: 本文介绍按记帐币种或销售税代码币种打印销售税支付（按代码）报表所需设置和操作。
author: AdamTrukawka
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.search.form: ''
ms.openlocfilehash: ea11826d21b66e6283abf24b3f7b0945e6eb9192
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272359"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>打印销售税支付（按代码）报表 

[!include [banner](../includes/banner.md)]

若要打开 **销售税支付（按代码）报表** 报表，请转到 **税务** \> **查询和报表** \> **销售税报表** \> **销售税支付（按代码）**。 默认情况下，将使用法人的记帐币种为 **销售税报告代码** 页中设置的所有报告代码生成报表金额。

也可以生成此报表，以使其使用销售税代码的币种为分配给 **销售税代码** 页中的销售税代码的所有报告代码的销售税支付金额。

## <a name="turn-on-the-feature"></a>开启功能

在 **功能管理** 工作区中，开启以下功能：**以销售税代码货币生成销售税按代码支付报表**。

## <a name="run-the-report"></a>运行报表

1. 转到 **计税** \> **查询和报表** \> **销售税报表** \> **销售税支付（按代码）**。
2. 在 **报表币种** 字段中，选择以下值之一：

    - **记帐币种** – 使用记帐币种打印报表金额。
    - **销售税代码币种** – 使用销售税代码的币种打印报表金额。

    ![“销售税支付（按代码）”对话框。](media/Sales-tax-payment-by-code.png)

下图显示生成的报表的示例。 如果报告代码分配给的销售税代码的 **销售税币种** 字段设置为 **EUR**，则此报表显示报告代码 **101** 的币种为 **EUR**。

![销售税支付（按代码）报表的示例。](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
