---
title: 运输管理杂项费用
description: 此主题说明运输产生的费用为何必须与费用代码关联。
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 776c73b1a29666e393bed7c40059a578fe86cb0d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576176"
---
# <a name="transportation-management-miscellaneous-charges"></a>运输管理杂项费用

[!include [banner](../includes/banner.md)]

与所有杂项费用一样，运输产生的费用必须与费用代码关联。 否则，它们将不会作为杂项费用添加回订单中。 **费用代码** 确定对于添加费用的订单和订单行费用如何计算。

转到 **运输管理 > 设置 > 评级 > 杂项费用** 定义确定特定 **费用代码** 何时应用于费用的合格条件。

每个 **费用模块** 设置（*客户* 和 *供应商*）至少应有一个将 **杂项费用类型** 设置为 *无* 的设置。 如果缺少此设置，杂项费用 *不* 会被添加到订单中。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]