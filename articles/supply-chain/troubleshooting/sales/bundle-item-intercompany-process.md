---
title: 内部公司流程不支持捆绑物料
description: 不可购买捆绑物料。 销售订单只能购买捆绑物料的组成部分，不能购买捆绑物料本身。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475690"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>内部公司流程不支持捆绑物料

## <a name="symptoms"></a>故障特征

捆绑物料不能用于采购订单，因为如果检查捆绑物料的销售订单行，您会注意到数量为 *0*（零），状态为 *已取消*。

## <a name="resolution"></a>解决方法

此为有意行为。 销售订单仅购买捆绑物料的组件。 不购买捆绑物料本身。 如果必须购买捆绑，请考虑是否必须将其标记为捆绑物料，因为此功能是为收入确认场景设计的。 有关捆绑物料的详细信息，请参阅[捆绑销售](/dynamics365/finance/accounts-receivable/revenue-recognition-setup)。
