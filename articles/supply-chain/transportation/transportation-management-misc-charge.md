---
title: 运输管理杂项费用
description: 此主题说明运输产生的费用为何必须与费用代码关联。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423468"
---
# <a name="transportation-management-miscellaneous-charges"></a>运输管理杂项费用

[!include [banner](../includes/banner.md)]

与所有杂项费用一样，运输产生的费用必须与费用代码关联。 否则，它们将不会作为杂项费用添加回订单中。 **费用代码** 确定对于添加费用的订单和订单行费用如何计算。

转到 **运输管理 > 设置 > 评级 > 杂项费用** 定义确定特定 **费用代码** 何时应用于费用的合格条件。

每个 **费用模块** 设置（*客户* 和 *供应商*）至少应有一个将 **杂项费用类型** 设置为 *无* 的设置。 如果缺少此设置，杂项费用 *不* 会被添加到订单中。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]