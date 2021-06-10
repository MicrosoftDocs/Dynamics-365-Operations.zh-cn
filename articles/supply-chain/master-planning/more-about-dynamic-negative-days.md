---
title: 负天数和动态负天数
description: 此主题介绍有关负天数和动态负天数的信息，以及将其如何用于帮助您开展业务。
author: ChristianRytt
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37ae6ebd4347d3bbb414b7f1e4e0d54150878c02
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097226"
---
# <a name="negative-days-and-dynamic-negative-days"></a>负天数和动态负天数

[!include [banner](../includes/banner.md)]

此主题介绍有关负天数和动态负天数的信息，以及将其如何用于帮助您开展业务。 *负天数时段* 表示在您的库存为负时，您愿意等待多久才订购新补货。

本主题中包含以下信息：

- 如何创建计划订单
- 负天数时段与物料提前期之间的关联
- 如何计算动态负天数时段，以及计算时如何考虑物料提前期因素
- 如何解释与负天数有关的[有关改进物料需求计划 (MRP) 的运行时间的建议（主计划）](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx)

本主题通过三个假设场景帮助您理解此信息。 这些场景之间的差别是您获得需求的时间点：在物料提前期前、中还是后。

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>场景 1：需求是在物料提前期之前获得的

您获得需求的时间可能相对物料提前期较早，或就在提前期开始前。 下面是此场景的一个示例：

- DemoProduct 物料的采购提前期为六天。
- 在第零天（1 月 1 日），DemoProduct 物料的库存级别为 0（零）。
- 在第零天（1 月 1 日），您获得一个销售订单，其中的数量是 10 件 DemoProduct 物料。
- 在第七天（1 月 8 日），有一个现有采购订单，其中的一个数量为 10 件 DemoProduct 物料。

下图显示此场景的图形视图。

![场景 1 的图形视图](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>案例 A：负天数小于物料提前期

如果将负天数设置为小于物料提前期的数字，MRP 将查找负天数时段内的 DemoProduct 物料收货。 因为找不到任何收货，所以 MRP 会创建一个新的计划采购订单。 将立即把此计划订单推迟六天（即提前期）。 因此，将在 1 月 7 日到达。 现有采购订单将收到 **取消** 行动消息，因为创建新计划采购订单导致现有采购订单变得多余。

下图显示此案例的屏幕截图。

![场景 1 的案例 A 屏幕截图](./media/negative-days-2.png)

下图显示此案例中的结果的图形视图。

![场景 1 的案例 A 图形视图](./media/negative-days-3.png)

如果考虑 MRP 绩效和计划紧张，则此案例的效果不佳。 MRP 必须创建新计划订单，并且必须计算延迟和行动。 这些任务比较耗时。 此案例将向计划再添加两个交易。 另一方面，销售订单仅延迟六天，而不是七天。

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>案例 B：负天数大于物料提前期

若要帮助提高 MRP 绩效，可将负天数设置为大于物料提前期的数字。 因为此场景中提前期内无法获得供应，所以搜索收货可以一直进行到不能进行为止。 尽管 MRP 的运行时间较短，所以应注意订单是否有更多延迟。

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>案例 C：将物料提前期与负天数时段自动关联

若要将物料提前期与负天数时段自动关联，请使用动态负天数。 若要使用动态负天数，请转到 **主计划 \> 设置 \> 主计划参数**，然后在 **常规** 选项卡上的 **覆盖范围** 部分中，将 **使用动态负天数** 选项设置为 **是**。 然后，MRP 查找动态负天数时段内的收货。 此时段使用以下公式计算：

动态负天数时段 = 采购提前期 + 负天数时段 +（当前日期 – 需求日期）

（如果 DemoProduct 物料的默认订单类型为 **生产** 或 **转移**，则提前期为 **库存** 提前期。）

如果使用动态负天数，则 MRP 查看收货的时段现在为 6 + 2 + 0 = 8 天。 MRP 查找现有采购订单并将销售订单与其关联。 将不创建任何新的计划订单。 因此，MRP 的运行时间较短。 下图显示 DemoProduct 物料的净需求。

![场景 1 的案例 C 净需求](./media/negative-days-4.png)

下图显示此案例中的结果的图形视图。

![场景 1 的案例 C 图形视图](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>案例 D：仅使用动态负天数

如果将负天数设置为 **0**（零），并且仅使用动态负天数时段，则此动态负天数时段为 6 + 0 + 0 = 6 天。 在此案例中，结果与此场景的案例 A 的结果相同。 MRP 必须创建新计划订单，并且必须计算延迟和行动。 这些任务非常耗时，并且还可能让人精疲力尽。 您还有两个交易需要处理。 因为不能准时履行有关物料到达的需求，此案例为计划带来了不必要的复杂性。

下图显示此案例的屏幕截图。

![场景 1 的案例 D 屏幕截图](./media/negative-days-6.png)

下图显示此案例中的结果的图形视图。

![场景 1 的案例 D 图形视图](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>案例 E：同时使用大于物料提前期的负天数和动态负天数时段

如果将负天数设置为大于物料提前期的数字，并且还使用动态负天数时段，则动态负天数时段为 6 + 6 + 0 = 12 天。 这种方法可能会导致 MRP 必须在很长的时段内搜索结果。 有关案例 E 与将负天数设置为长时段的情况之间的关系的信息，请参阅本主题的[结论](#conclusion)部分。

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>场景 2：需求是在物料提前期中获得的

有时可能会在物料提前期内获得需求。 下面是此场景的一个示例：

- DemoProduct 物料的采购提前期为六天。 
- 在第零天（1 月 1 日），DemoProduct 物料的库存级别为 0（零）。
- 在第四天（1 月 5 日，这在物料提前期内），您获得了一个销售订单，其中的一个数量为 10 件 DemoProduct 物料。
- 在第七天（1 月 8 日），有一个采购订单，其中的一个数量为 10 件 DemoProduct 物料。

下图显示此场景的图形视图。

![场景 2 的图形视图](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>案例 A：负天数小于物料提前期

如果将负天数设置为小于物料提前期的数字，MRP 将查找负天数时段内的 DemoProduct 物料收货。 因为未找到任何收货，MRP 创建一个新的计划采购订单，该采购订单将当前日期用作订单日期。 将立即把此计划订单推迟六天（即提前期）。 因此，将在 1 月 7 日到达。 现有采购订单将收到 **取消** 行动消息，因为创建新计划采购订单导致现有采购订单变得多余。

下图显示此案例的屏幕截图。

![场景 2 的案例 A 屏幕截图](./media/negative-days-9.png)

下图显示此案例中的结果的图形视图。

![场景 2 的案例 A 图形视图](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>案例 B：负天数大于物料提前期

此案例类似场景 1 的案例 B。 如果将负天数设置为大于物料提前期的数字，则不会获得新的计划订单。 将把销售订单附加到现有采购订单。

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>案例 C：将物料提前期与负天数时段自动关联

此案例类似场景 1 的案例 C，因为动态负天数的效果与在该案例中一样出色。 动态负天数时段现在为 6 + 2 – 4 = 4 天。 如果使用此方法，MRP 将找到现有采购订单，并为其附加销售订单。 因为不创建新计划订单，所以 MRP 的运行时间较短。

下图显示此案例的屏幕截图。

![场景 2 的案例 C 屏幕截图](./media/negative-days-11.png)

下图显示此案例中的结果的图形视图。

![场景 2 的案例 C 图形视图](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>案例 D：仅使用动态负天数

如果将负天数设置为 **0**（零），并且仅使用动态负天数时段，则此动态负天数时段现在为 6 + 0 - 4 = 2 天。 在此案例中，结果与此场景的案例 A 的结果相同。 有关结果的图形视图，请参见此场景的案例 A。

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>案例 E：同时使用大于物料提前期的负天数和动态负天数时段

如果将负天数设置为大于物料提前期的数字，并且还使用动态负天数时段，则动态负天数时段为 6 + 6 - 4 = 8 天。 这种方法可能会导致 MRP 必须在很长的时段内搜索结果。 有关案例 E 与将负天数设置为长时段的情况之间的关系的信息，请参阅本主题的[结论](#conclusion)部分。

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>场景 3：需求是在物料提前期后获得的

需求可能是在物料提前期后获得的。 下面是此场景的一个示例：

- DemoProduct 物料的采购提前期为六天。
- 在第零天（1 月 1 日），DemoProduct 物料的库存为 0（零）。
- 在第七天（1 月 8 日，这超出了物料提前期），您获得了一个销售订单，其中的一个数量为 10 件 DemoProduct 物料。
- 在第十天（1 月 11 日），有一个采购订单，其中的一个数量为 10 件 DemoProduct 物料。

下图显示此场景的图形视图。

![场景 3 的图形视图](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>案例 A：负天数小于物料提前期

如果将负天数设置为小于物料提前期的数字，MRP 会在销售订单需求日期前两天查找。 因为找不到任何内容，所以 MRP 会在 1 月 2 日创建一个计划采购订单。 将仅为这个计划采购订单及时发货以履行销售订单需求。 现有采购订单将收到 **取消** 行动消息，因为不需要该订单。

下图显示此案例的屏幕截图。

![场景 3 的案例 A 屏幕截图](./media/negative-days-14.png)

下图显示此案例中的结果的图形视图。

![场景 3 的案例 A 图形视图](./media/negative-days-15.png)

> [!NOTE]
> 在前面的屏幕截图中，采购订单需求日期为 1 月 12 日。 因为该屏幕截图是在 2015 年截取的，当时 1 月 11 日是星期日，MRP 将需求日期移到了下一个工作日，即 1 月 12 日，星期一。 不过，采购订单的交付日期为 1 月 11 日。

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>案例 B：负天数大于物料提前期

如果将负天数设置为大于物料提前期的数字，则不会获得新的计划订单。 将把销售订单与现有采购订单关联。 因此，销售订单将延迟。 如果创建计划订单，则可为销售订单准时发货。

下图显示此案例的屏幕截图。

![场景 3 的案例 B 屏幕截图](./media/negative-days-16.png)

下图显示此案例中的结果的图形视图。

![场景 3 的案例 B 图形视图](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>案例 C：将物料提前期与负天数时段自动关联

此案例类似场景 1 的案例 C，因为动态负天数的效果与在该场景的案例 B 中一样出色，如果不更出色的话。

动态负天数时段为 6 + 2 – 7 = 1 天。 但是，在此案例中，系统仍然会考虑负天数提前期 (2)，因为 MRP 会考虑负天数提前期与动态负天数提前期之间的最大值。 因此，此案例中的结果与此场景的案例 A 的结果相同。

下图显示此案例中的结果的图形视图。

![场景 3 的案例 C 图形视图](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>案例 D：仅使用动态负天数

如果将负天数设置为 **0**（零），并且仅使用动态负天数时段，则此动态负天数时段现在为 6 + 0 - 7 = -1 天。 在此案例中，系统仍然考虑负天数提前期 (2)。 因此，此案例中的结果与此场景的案例 A 的结果相同，缺点也完全一样。 有关结果的图形视图，请参见场景 2 的案例 A。

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>案例 E：同时使用大于物料提前期的负天数和动态负天数时段

此案例与场景 1 和 2 的案例 E 相同。 优点和缺点基本分别一样。

## <a name="conclusion"></a>结论

如本主题中的三个场景所示，最好将负天数设置为大于覆盖范围组中的物料提前期的数字。 此外，最好仅使用动态负天数，并将负天数设置为在您的库存为负时，您愿意在订购新补货之前愿意等待的天数（换句话说，愿意进一步延迟需求的天数）。 此外，同一个覆盖范围组中的物料应具有类似提前期。

如果将负天数设置为 **0**（零），并且不使用动态负天数，则 MRP 设置创建新计划订单来履行需求。 在此情况下，务必使用行动消息，以确保库存不会积压。

您可能需要将负天数设置为较长时段，然后使用行动消息。 这种方法的计划结果很好，不过速度也有点慢。 还可能更难分析，因为必须分析并采用行动消息。 下面是一个示例：

- DemoProduct 物料的采购提前期为六天。
- 在第零天（1 月 1 日），DemoProduct 物料的库存为 0（零）。
- 在第零天（1 月 1 日），您获得一个销售订单，其中的数量是 10 件 DemoProduct 物料。
- 在第九天（1 月 10 日），您获得一个销售订单，其中的数量是 10 件 DemoProduct 物料。
- 在第十一天（1 月 12 日），有一个采购订单，其中的一个数量为 10 件 DemoProduct 物料。
- 负天数设置为 **20**，比物料提前期大得多。

下图显示结果的图形视图。

![示例的图形回顾](./media/negative-days-19.png)

MRP 产生以下结果。

![结果示例 1](./media/negative-days-20.png)

在上一个屏幕截图中，销售订单需求日期为 1 月 9 日，而不是 1 月 10 日。 因为该屏幕截图是在 2015 年截取的，当时 1 月 10 日是星期六，所以订单的需求日期应该是上一个工作日，即 1 月 9 日，星期五。

MRP 创建计划采购订单以履行第一个销售订单请求的需求，但是还建议您取消计划订单，因为可以将现有采购订单提前，并增加其中的数量。

结果没有问题，但是 MRP 的运行时间可能较长，因为 MRP 必须创建所有延迟和建议。 此外，规划员还可能需要更多时间来理解 MRP 结果。 最重要的是，在此情况下，规划员务必理解和使用行动消息。

如果将负天数减小到更接近物料提前期的数字，并且使用动态负天数，MRP 将产生以下结果。

![结果示例 2](./media/negative-days-21.png)

MRP 创建一个附加到第一个销售订单的计划订单。 然后，基于负天数设置将第二个销售订单与现有采购订单关联。这是正常现象。 这个计划结果也是正确的，并且 MRP 的运行时间可能较短。 在此情况下，务必了解并知道如何使用行动消息。

若要帮助确保为您的业务输入正确值，必须同时考虑功能和 MRP 运行时间。 因此，可以通过一些试错来确定最佳值。

## <a name="see-also"></a>请参阅

有关详细讨论，请参阅原始博客文章[有关（动态）负天数的详细信息](/archive/blogs/axmfg/more-about-dynamic-negative-days)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
