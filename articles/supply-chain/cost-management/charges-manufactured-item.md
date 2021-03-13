---
title: 显示制造物料的费用
description: 制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2e181e6c933a4c360320e4539f8434c20d409358
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008258"
---
# <a name="display-charges-for-a-manufactured-item"></a>显示制造物料的费用

[!include [banner](../includes/banner.md)]

制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。

物料的费用的计算出的金额能和物料的单位成本一起显示。 然而，该费用有时候作为单独的字段显示，并且它们不包括在该物料的单位成本。 当费用作为单独的字段出现时，一个字段显示费用的总金额，另一个字段显示用于摊销该金额的成本计算批次规模。 例如，“物料价格”页显示作为两个单独的字段的费用。 然而，“完成”页显示物料的单位总成本，并且摊销的成本包括在单位成本中。

出于标准成本目的，某一制造物料的费用始终包括在该物料的单位成本中。 而出于计划成本目的，可以选择是否包括杂项费用。 成本计算版本内的策略强制包括在制造物料的成本中的费用。 在您启用某一物料的成本记录时，为该物料的基本成本信息更新费用，显示在“物料价格”页上。 该费用作为两个单独的字段显示，并且它们不包括在该物料的单位成本。 每次启用都将更新该物料的基本成本信息，即使该启用反映不同的站点。 因此，您应该查看作为参考信息的基本成本信息。





