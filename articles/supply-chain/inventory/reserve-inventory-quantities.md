---
title: 预留库存数量
description: 本文介绍预留库存时可用的不同选项。
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c0e283189998473469164398fa6f43c8e8825e
ms.sourcegitcommit: 3a882de1f1c27654a8e92ebc1999c75678cc9a53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2022
ms.locfileid: "9201857"
---
# <a name="reserve-inventory-quantities"></a>预留库存数量

[!include [banner](../includes/banner.md)]

本文介绍预留库存时可用的不同选项。

可以为特定的销售订单自动预留库存数量。 这意味着除非库存预留或部分库存预留已取消，否则不能从仓库中为其他订单提取预留库存。

冲销库存有许多原因：
-   先订购，先交货，这意味着客户获得可用物料的顺序与其订购顺序相同。
-   由于供应商的交货时间很长或未知而导致物料短缺。 您可能要确保某些客户或订单可获得第一批可用物料。
-   某些客户或某些类型的订单具有交货的最高优先级。
-   具有序列号或批号的物料。 您可以标记已经或将要为特定订单交货的物料。
-   为某些订单预留的特别订购的物料。
-   生产订单。 例如，您可以标记为特定订单生产或针对特定订单进行调整的物料。

创建新订单行时可以自动预留库存，也可以手动为各订单预留库存。 可以在生产流程的不同阶段预留库存。 仅可预留贮存的产品。 不能预留服务，因为没有现有库存量。 实际的现有库存量和已订购但尚未接收的库存都可以预留。 如果预留数量多于现有库存量，则将显示消息，指出您不能预留如此大的数量。 然后您无论如何都可以预留该数量，也可以更改订购数量。 可以保留该数量，也可以更改该数量。 如果预留物料的数量多于可用数量，然后在下次有可供交货的物料时补充短缺量。

## <a name="inventory-reservation-policies"></a>库存预留策略
库存预留策略在 **物料模型组** 页、**库存和仓库管理参数** 页和 **生产参数** 页设置。
### <a name="policies-on-the-item-model-groups-page"></a>物料模型组页面的策略

**库存策略** 部分包含以下预留策略。

| &nbsp;                  | &nbsp;                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **预留策略**  | **描述**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 受先进先出日期控制    | 如果您选择了 **受先进先出日期控制** 选项，则将按照先进先出原则的排序日期控制库存预留。 根据先进先出 (FIFO) 原则，基于收货物料的最早日期预留批次。                                                                                                                                                                                                                                                                       |
| 从装运日期倒推 | 只有在选择 **受先进先出日期控制** 选项后，此选项才可用。 如果您选择了 **从装运日期倒推** 复选框，则将根据后进先出 (LIFO) 原则从所需的装运日期倒推来预留库存。 如果在装运日期之前没有可用的接收，则使用先进先出预留。                                                                                                                                                                                                           |
| 物料销售预留  | 确定手动或自动预留物料。 如果自动预留，则当创建订单行时预留库存。 可以在物料编号级别为物料清单进行预留（**自动** 选项）或者为物料清单的单个元素进行预留（**分解** 选项）。 **物料销售预留** 的默认值可能继承自 **应收账款参数**。 在此页上，该值在 **常规** 选项卡上的 **销售默认值部分** 的“预留”字段中进行设置。 |
| 相同批次选择    | 相同批次预留可让您针对一批库存为销售订单行保留库存。 如果要使用此选项，还必须将 **合并要求** 选项设置为 **是**。 对跟踪维度组和存储维度组还需要额外设置。 有关详细信息，请参阅[为销售订单预留相同批次](../sales-marketing/reserve-same-batch-sales-order.md)。                                                          |
| 合并要求 | 此选项类似于 **同一批次选择** 选项，将为销售订单行预留的库存合并到一个要求中。                                                                                                                                                                                                                                                                                                                                                                                      |
| 受先过期先出日期控制    | 此选项允许您预留接近到期日期或最佳使用日期的批次。 您还需要将 **选择标准** 字段设置为选择 **到期日期** 或 **最佳使用日期**。                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>受先进先出日期控制和从装运日期倒推的示例

在此示例中，物料编号 A 存在三个不同批号的现有库存。

| 物料编号 | 批处理号 | 数量 | 日期             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5        | 2016 年 2 月 2 日 |
| A           | 1001         | 3        | 2016 年 1 月 1 日  |
| A           | 1002         | 7        | 三月 3, 2016    |

应自动预留并于 2016 年 4 月 4 日交付的销售订单将预留以下批次：
-   如果同时清除 **受先进先出日期控制** 和 **从装运日期倒推** 两个复选框，则预留批次 1000，因为它是数字最小的批次。
-   如果选中 **受先进先出日期控制** 复选框，清除 **从装运日期倒推** 复选框，则预留批次 1001，因为它是第一个收货日期的批次 (FIFO)。
-   如果同时选择 **受先进先出日期控制** 和 **从装运日期倒推** 两个复选框，则预留批次 1002，因为它是最接近销售订单装运日期的批处理收货。

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>库存和仓库管理参数策略页

**库存和仓库管理参数** 页有两个与预留有关的选项：
-   **常规** 选项卡上的 **预留已订购物料** 选项可以预留针对“应收账款”、“项目管理与核算”和“生产控制”中的物料发货而订购的物料收货。 如果您清除此选项，将只能预留已实际接收的物料。 如果某特定物料已设置为允许负库存，则此字段不相关。
-   **转移** 选项卡上的 **自动预留物料** 选项确定是否为转移单自动预留物料的默认设置。 单个转移单上的默认设置可被覆盖。

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>“生产参数”页上的库存预留策略

**生产参数** 页上的 **常规** 选项卡上的 **预留** 字段的值确定在生产流程中应预留库存的默认点。 例如，可以在编制工作计划时或者在工作开始时预留库存。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
