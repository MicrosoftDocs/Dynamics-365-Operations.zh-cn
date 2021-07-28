---
title: 打印销售税支付（按代码）报表
description: 此主题介绍按记帐币种或销售税代码币种打印销售税支付（按代码）报表所需设置和操作。
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dad1cad6dcda1c7768f9be8bd7bd4426be7fbcbb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358849"
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