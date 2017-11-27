---
title: "更新制造环境中的标准成本"
description: "本文提供有关如何在非制造环境中更新标准成本的指导。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>更新制造环境中的标准成本

[!include[banner](../includes/banner.md)]


本文提供有关如何在非制造环境中更新标准成本的指导。 

更新可以反映新物料、成本类别或间接成本计算公式。 它们还可以反映更正和成本变化。 此类型的更新影响更新标准成本必须完成的步骤，如以下情况中所示：

-   为采购的物料输入预期的标准成本变化，然后更改相应日期上的物料成本记录的状态为**活动**状态。 但是，不重新计算使用采购物料的制造物料的成本。
-   为新采购的物料输入标准成本，但不重新计算具有将这一新采购物料作为组件包含的物料清单 (BOM) 版本的制造物料的成本。
-   更正或更改采购物料的成本，或者更改分配给采购物料的成本组，并且为具有将采购物料作为组件包含的物料清单版本的所有制造物料计算成本。
-   为某一成本类别更改成本，并且为具有包含使用该成本类别的工艺路线工序的工艺路线版本的所有制造物料计算成本。
-   更改分配给工艺路线工序的成本组或分配给成本类别的成本组的成本类别。 然后为具有包含使用该成本类别的工艺路线工序的工艺路线版本的所有制造物料计算成本。
-   更改间接成本计算公式，并且为该更改影响的所有制造物料计算成本。
-   更改或添加制造物料的制造站点，并且为该站点计算物料的制造成本。
-   计算（或重新计算）某一制造物料的成本，并且为具有将该制造物料作为组件包含的物料清单版本的所有制造物料重新计算成本。
-   基于新制造物料的已定义、审核和活动的物料清单和工艺路线信息，计算此物料的成本。

每种情况都要求仔细考虑如何更新标准成本。




