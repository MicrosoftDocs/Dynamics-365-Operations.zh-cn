---
title: 采购订单不反映法人的语言设置
description: 采购订单上的产品名称以系统语言显示，而不是为创建采购订单的法人设置的语言
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475677"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>采购订单不反映法人的语言设置


## <a name="symptoms"></a>故障特征

采购订单上的产品名称以系统语言显示，而不是为创建采购订单的法人设置的语言。

## <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 将系统语言设置为 *EN-US*（美国英语）。
1. 确保有一个产品保留了 *EN-US* 和 *DE*（德语）语言来翻译产品名称。
1. 将法人的语言更改为 *DE*。
1. 在将 *DE* 设置为语言的法人中，创建包含该产品的采购订单。
1. 请注意，产品名称仍以美国英语（系统语言）显示。

## <a name="resolution"></a>解决方法

此为有意行为。 在采购订单上，产品始终以系统语言显示。 创建确认日记帐时将使用采购订单语言。
