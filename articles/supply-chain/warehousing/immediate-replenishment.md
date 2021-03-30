---
title: 即时补货
description: 本主题介绍如何在位置指令无法分配库存时使用即时补货为库存补货。
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 3def95ac272a424591ed4382d5cd5841bc663654
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235380"
---
# <a name="immediate-replenishment"></a>即时补货

[!include [banner](../includes/banner.md)]

位置指令行无法分配库存时，可立即通过即时补货为库存补货。 这种补货基于位置指令设置中的一行。 如果库存现货的度量单位不是该行指定的度量单位，将立即使用该度量单位补货。

即时补货可以替代以下方法：库存分配基于位置指令中的多行，以及需求在分配结束时汇总，并使用位置指令中最后一行指定的度量单位补货。

使用即时补货的优点时可以按特定单位限制补货，并且可指示从特定位置领取数量。

## <a name="business-scenario"></a>业务方案

例如，您有一个仓库有单独的领料区域，这些区域采用“箱”和“单件”度量单位。 您希望通过尽量以箱为单位领料，然后从“单件”区域领取不足一箱的剩余数量，优化领料过程。

在这种情况下，可以使用即时补货。 在位置指令中，可为箱设置即时补货，这样只要需求数量的可领料箱数不足，就会立即使用需求补货。 通过这种方法，就优化了领料过程，所以领料中包含尽可能多的箱数。 即时补货将生成以箱为单位的补货，而需求不会传递，所以将以“单件”度量单位领取数量。 换言之，将从“单件”区域仅领取应以“单件”度量单位领取的数量（即不足一箱的数量）。 如果“箱”区域中产品短缺，则可领取总需求中尽量多箱的产品。 然后从“单件”区域领取其余数量。

## <a name="where-it-applies"></a>适用情况

如果设置了补货模板的位置指令行的分配失败，则在执行波次期间使用即时补货。

## <a name="set-up-immediate-replenishment"></a>设置即时补货

- 转至 **仓库管理** \> **设置** \> **位置指令**，然后在 **行** 选项卡的 **即时补货模板** 列表中为波形需求选择补货模板。

如果位置指令行未能分配专用度量单位，则应用补货模板。

## <a name="troubleshooting"></a>疑难解答

如果为位置指令行选择了即时补货，但是对该位置指令行使用需求补货模板时未生成补货工作，则必须调查下面的两种主要原因：

- 确保应用的需求补货模板设置为使用 **补货** 类型的正确位置模板和工作模板。
- 确保需求补货模板在其中为补货搜索现货库存的位置中现货库存充足。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]