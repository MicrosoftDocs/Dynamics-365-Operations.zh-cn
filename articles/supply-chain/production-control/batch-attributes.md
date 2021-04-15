---
title: 批次属性
description: 文主题提供有关批属性的信息。 批次属性是构成库存批次的原材料和成品的特征。 本主题还说明如何分配批属性，以及如何在预留批处理时对它们进行搜索。
author: ShylaThompson
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 064b3dc7f0209b5c81580d4eb80384df74155aee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811838"
---
# <a name="batch-attributes"></a>批次属性

[!include [banner](../includes/banner.md)]

文主题提供有关批属性的信息。 批次属性是构成库存批次的原材料和成品的特征。 本主题还说明如何分配批属性，以及如何在预留批处理时对它们进行搜索。

批次属性是构成库存批次的原材料和成品的特征。 受若干因素（如环境条件、用于生产该批次的原材料的质量或成品的结果）影响，批次属性会有所不同。 不同的行业所用的批次属性的数量和类型可能相差甚远。 这是两个显示如何使用批次属性的示例：

-   在奶酪行业，牛奶（用于生产奶酪的原材料之一）可能具有脂肪含量和百分比重量之类的属性。 通过牛奶生产的奶酪可能具有类似湿度和期限之类的其他属性。
-   在钢铁行业，所生产的铁可能具有镁含量、银含量和锌含量百分比之类的属性。

为更好地管理属性的数量和类型，您可以使用批次属性组。 这样，就不必逐个添加各个属性。

## <a name="assign-batch-attributes"></a>分配批次属性
您可以将批次属性分配到库存批次中包含的各个产品或者您可以将它们分配给与特定客户关联的产品。 在您可以将批次属性分配在客户水平前，必须先将其分配在产品级别。 产品必须具有批次维度在“跟踪维度组”中设置为 **有效**。 若要将批次属性分配到单个产品，请使用“产品特定”页。 如果该属性特定于客户的产品，请使用“客户特定”页。 在您添加一个属性给产品时，还可以定义其他参数。 下面举了一些示例加以说明：

-   **整数** 或 **分数** 类型的属性的最小值和最大值范围。
-   **整数** 或 **分数** 类型属性的容差操作。 如果该属性的值超出最小值和最大值范围，行动可以是警告消息或错误消息。
-   属性的目标值。 此值是最佳值属性，并且该规则将应用于所有属性类型。

您可以访问在“产品信息管理”的 **发布产品** 页中选择的产品的页面。 在向产品分配批次属性后，可以添加特定值到 **库存批次属性** 页的属性。

## <a name="reserve-batches"></a>预留批次
在为销售订单进行批次预留以履行客户订单时，或者当您为生产订单领取和预留批次时，您可以搜索批次属性。 搜索帮助找到包含具有所需批次属性的产品的库存批次。 找到该批次或这些批次后，然后可以预留产品到起源库存交易记录行。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]