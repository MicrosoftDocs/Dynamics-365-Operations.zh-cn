---
title: 需求驱动型计划
description: 本文介绍如何为设置为分离点的物料生成计划订单。
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740294"
---
# <a name="demand-driven-planning"></a>需求驱动型计划

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

本文介绍如何为设置为分离点的物料生成计划订单。

## <a name="net-flow-and-qualified-demand"></a>净流和合格需求

在主计划期间，系统应用 *净流* 概念，将实际现有库存加上在单（尚未接收的现有供应订单）库存，然后减去所谓的 *合格需求*（合格的近期销售），从而确定有效现有数量，如以下说明中所示。 当系统确定物料属于哪个缓冲区以及订购数量应该是多少时，它会评估净流，而不是实际现有库存。

![净流计算图表的示例。](media/ddmrp-net-flow-example.png "净流计算图表的示例")

在计划运行期间触发计划订单时，订购数量将为最大水平减去净流。 为了指定订单优先级，系统会使用[基于优先级的计划](priority-based-planning.md)功能，而不是使用需求日期。 需求驱动型材料要求计划 (DDMRP) 根据订购数量占最大库存的百分比指定计划订单的优先级。 在上图中，订购数量是最大数量的 53%。 因此，补货的订单优先级将为 53。 （对于上下文，0 是最高优先级，100 是最低优先级。）

*合格需求* 为逾期需求加上今日需求再加上未来合格订单峰值。 下图显示了今天（6 月 12 日）和接下来三天的需求水平的一个示例。 DDMRP 允许您设置订单峰值阈值以标识超出正常预期的需求。 如果将阈值设置为 25 件，则图中显示的两个未来日期将适合作为订单峰值日期。 您必须使用 **物料覆盖范围** 页面单独为每个产品分配订单峰值阈值，如[设置分离点物料的缓冲区](ddmrp-buffer-profile-and-levels.md#set-up-buffers)中所述。

![合格需求计算图表的示例。](media/ddmrp-net-qualified-demand-example.png "合格需求计算图表的示例")

假设没有逾期需求，那么您现在可以将今日需求 (18) 加上两个订单峰值（29 和 26）的数量，以获得合格需求值 73。 尽管 6 月 23 日有需求，但请注意，它并未包含在净流计算中，因为 DDMRP 触发计划订单的方式与传统计划覆盖组不同。

## <a name="generating-planned-orders-with-ddmrp"></a>使用 DDMRP 生成计划订单

在计划运行期间，如果项目的净流低于再订购点，系统将创建一个新的计划订单。 当您使用 DDMRP 时，通常会每天执行一次计划运行。 因此，您实际上是每天检查一次库存水平以确定必须补充哪些物料。

下图显示了一个情况示例，即您在 6 月 20 日订购了 18 件，6 月 21 日订购了 29 件，6 月 22 日订购了 26 件，6 月 23 日订购了 20 件。 由于峰值阈值设置为 25 件，因此其中两个订单被标记为峰值。 现有 220 件此物料。

![计划示例 1。](media/ddmrp-planning-example-1.png "计划示例 1")

如果您现在运行主计划，并且发现净流低于再订购点（本例中为 219 件），则它将生成计划订单。

![计划示例 2。](media/ddmrp-planning-example-2.png "计划示例 2")

此示例会生成数量为 130 的计划采购订单，该数量等于最大水平减去净流。 基于占最大数量的百分比，为计划订单分配的优先级为 53.07。 由于在 6 月 20 日找到了这些值，因此系统创建了日期为 6 月 20 日加上物料分离提前期（此示例中为五个工作日）的计划订单。 因此，由于五个工作日是从今天开始的一周时间，因此计划订单的日期为 6 月 27 日。

> [!NOTE]
> 主计划使用 DDMRP 仅计算分离的物料。 所有其他物料均使用标准物料需求计划 (MRP) 进行计算。
