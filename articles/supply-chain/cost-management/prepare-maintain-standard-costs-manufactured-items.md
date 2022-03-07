---
title: 准备为制造物料维护标准成本
description: 本主题介绍准备维护制造物料成本的步骤。
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec68e1efc261920dc8f08ed602836b1939511dfce01008c093af7916ecd71618
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734323"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>准备为制造物料维护标准成本

[!include [banner](../includes/banner.md)]

本主题介绍准备维护制造物料成本的步骤。 制造物料的步骤与采购物料的步骤稍有不同。

分配给制造物料的策略可能会影响父级制造物料的成本计算。 若要准备维护制造物料的成本，请执行以下步骤。

1. 将某一物料模型组分配给该制造物料。 

   该物料模型组标识将使用标准成本。

2. 将某一物料组分配给制造物料。 

   该物料组包含应用于制造物料的会计科目。 具有标准成本库存模型的制造物料的会计科目包括若干生产差异、成本变化差异和库存成本重估。

3. 将库存度量单位分配给该物料。 

   该物料的成本始终按其库存度量单位表示。

4. 不用将某一成本组分配给制造物料，除非该物料将被视作采购物料。

5. 将物料清单 (BOM) 计算组分配给制造物料。 

   物料的 BOM 计算组标识应用的警告条件。 这样，BOM 计算完成后，可生成有关计算错误可能原因的警告消息。 例如，某一警告消息可以标识有效物料清单或工艺路线何时不存在。 物料清单计算组包含停止分解策略，指示何时应将制造物料视作采购物料。

6. 如果制造物料具有固定成本，请为其分配标准订单数量。 

   标准订单数量是摊销固定成本的会计批次规模。 固定成本的示例包括工艺路线工序的设置时间和 BOM 中的固定组件数量。

7. 为制造物料定义物料清单。 

   可为制造物料定义一个或多个物料清单版本。 请确认您所需的版本已标记为已审核且活动的版本，并且它们具有所需的生效日期。 该物料清单版本可以是公司范围的或特定于站点的。

8. 为制造物料定义工艺路线。 

   可为制造物料定义一个或多个工艺路线版本。 请确认您所需的版本已标记为已审核且活动的版本，并且它们具有所需的生效日期。 该工艺路线版本必须是特定于站点的。

如果要将工艺路线信息用于成本核算目的，需要执行更多的准备步骤。 例如，分配给工艺路线工序的成本类别必须正确且完整。

## <a name="related-topics"></a>相关主题

[为制造物料摊销固定成本](amortize-constant-costs-manufactured-item.md)

[设置可以生产或采购的产品](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]