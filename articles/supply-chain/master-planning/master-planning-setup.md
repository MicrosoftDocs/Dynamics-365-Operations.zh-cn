---
title: 设置主计划
description: 此主题介绍用于设置主计划的各种重要策略和参数。
author: t-benebo
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: e30b02a6f98f638954adc7ec335babd518b92bf4
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909395"
---
# <a name="set-up-master-planning"></a>设置主计划

[!include [banner](../includes/banner.md)]

此主题介绍用于设置主计划的各种重要策略和参数。 其中包含主计划所用计划类型的概述，并说明应使用哪种策略，具体取决于您的业务需求。 还介绍可影响计划的主要参数，并说明这些参数对建议的计划订单有何影响。

## <a name="types-of-master-plans"></a>主计划的类型

主计划有两种计划类型：静态和动态。 每种类型专门针对一种特定用途。 建议您使用适用于您的场景的计划，以发挥最佳性能。

### <a name="static-plan"></a>静态计划

下次运行主计划之前，无论供应和需求如何变化，静态计划都保持不变。

静态计划用于审核和确定建议的订单。 这是是工序级计划，公司的各类人员（例如采购人员或生产规划人员）可将其用作决策基础和执行日常任务和活动。

静态计划还支持重新生成。 只要运行主计划，都将计算全新优化计划，并删除尚未审核的现有订单。

### <a name="dynamic-plan"></a>动态计划

动态计划开始时通常是静态计划的副本，但是只要主数据改变，都可能更新。 例如，如果数据改变，则创建新销售订单。

动态计划用于临时计划。 供公司监控更改的订单网络以及物料可用性，而无需中断其他人正在工作过程中使用的静态计划。 专用于可承诺量 (CTP)。 从其他订单页（如销售订单、采购订单或生产订单页）打开净需求时，动态计划即为默认计划。

动态计划使用净改变。 因此，有助于确保加快运行。

## <a name="strategies-for-using-master-plans"></a>主计划的使用策略

可在主计划中使用一个或两个计划。 所用策略取决于业务需求。

### <a name="one-plan-strategy"></a>单计划策略

对于单计划策略，静态计划和动态计划使用同一个主计划。 此策略用于制造到库存场景，此类场景中，通常不必模拟用于履行订单的计划。

单计划策略通常用于零售和配送行业，或根据服务级别协议 (SLA) 或提前期确认销售交付日期的场景。 对于此类计划，使用交货日期控件时无 CTP。

如果必须进行模拟，可对需要模拟的物料重复运行计划。 通常会确定订单模拟生成的计划订单。

### <a name="two-plan-strategy"></a>双计划策略

对于双计划策略，需要使用一个静态计划和一个不同的动态计划。 双计划策略通常用于配置到订购和制造到订购场景，在这两种场景中，必须执行销售订单模拟和计算销售订单的确切交付日期，但是计算不得影响工序。 这些模拟始终在动态计划中完成。 双计划策略在汽车和原始设备制造商 (OEM) 之类行业非常有用。

对于双计划策略，可使用交付日期控件 CTP。 如果使用 CTP，通常会在动态计划中触发运行。

### <a name="setting-up-the-plans"></a>设置计划

可在 **主计划** 页（**主计划 \> 设置 \> 计划 \> 主计划**）中创建计划。

可通过设置 **主计划参数** 页（**主计划 \> 设置 \> 主计划参数**）上的 **当前静态主计划** 和 **当前动态主计划** 字段，指定将对静态计划和动态计划使用哪些计划。 若要使用单计划策略，请在 **当前静态主计划** 和 **当前动态主计划** 字段中指定同一个计划。

## <a name="types-of-planning-methods"></a>计划方法的类型

可使用三种计算方法运行主计划：重新生成和净改变。 每种方法在运行时都会生成一个不同的计划。

请在 **主计划运行** 对话框中指定计划方法。 若要打开此对话框，请转到 **主计划 \> 主计划 \> 运行 \> 主计划**，或在 **主计划** 工作区中选择 **运行**。

### <a name="regeneration"></a>重新生成

除非确定现有计划订单，否则重新生成计划方法会删除这些订单。 将根据所有需求生成新的计划订单。 重新生成是唯一可用于静态计划的计划方法。

- 将考虑供应变化。 这些变化包括预测变化。
- 这种方法遵守 **期间** 覆盖范围代码。
- 这种方法支持产品替代功能 (PI)。

### <a name="net-change"></a>净改变

净改变计划方法生成计划订单，以涵盖上一个主计划运行以来创建或更改的需求。 运行此方法时不考虑供应改变。 系统不会考虑任何新供应，也不会删除之前创建，但不再需要的计划订单。 净改变计划方法的运行速度比重新生成方法快。 仅适用于动态计划。

- 所有需求的行动日期和将来日期都将更新。
- 这种方法不遵守 **期间** 覆盖范围代码。
- 这种方法不执行预测，即使在计划中选择了也不例外。
- 这种方法不支持产品替代功能 (PI)。

### <a name="net-change-minimized"></a>最小化的净改变

净改变最小化计划方法生成计划订单，以仅涵盖上一个主计划运行以来创建或更改的需求。 对于此方法，与净改变方法不同，只会更新新需求或更改后需求的行动日期和将来日期。 这种计划方法仅适用于动态计划。

## <a name="types-of-scheduling-methods"></a>排产方法的类型

对于各计划，必须在 **主计划** 页（**主计划 \> 设置 \> 计划 \> 主计划**）的 **常规** 快速选项卡上选择用于生产订单的排产方法。 您可以在工序级别和作业级别计划生产。

### <a name="operations-scheduling"></a>工序级排产

您可以使用工序级排产以提供生产流程的持续时间的粗略估计。 工序级排产则不将该生产工艺路线中的工序分解为作业。 有关工序级排产的详细信息，请参阅[工序级排产](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling)。

### <a name="job-scheduling"></a>作业级排产

作业级排产是更详细的排产方法，在此类排产中，每道工序拆分为单独的任务或作业。 作业级排产中包含有关产能的信息。 通常用于即刻发生或在短期内发生的车间单个作业。 有关作业级排产的详细信息，请参阅[作业级排产](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。

## <a name="time-fences-in-days"></a>按天计算的时限

对于每个计划，可选择主计划必须计算将来多长时间范围内的各种需求和其他注意事项。 此期间称为 *时限*。 要让主计划发挥最佳效果，建议调整各时限以满足您的业务需求。 对于各计划，可在 **主计划** 页（**主计划 \> 设置 \> 计划 \> 主计划**）的 **按天计算的时限** 快速选项卡上找到时限。

> [!NOTE]
> 时限指示主计划计算将来多长时间范围内的各种需求和其他注意事项。 此页中选择的时限将替换覆盖范围组中定义的时限。 这意味着如果将时限选项设置为是并定义天数，将替换覆盖范围组中定义的时限。 如果设置为“否”，则将在覆盖范围组中定义时限。 最后，如果不希望或不需要使用选项（例如，不希望使用行动消息），请将其设置为 **是**，然后将时限设置为 **0**（零）天。

### <a name="coverage"></a>覆盖范围

覆盖范围时限表示排产时限，或应包含多久的需求。 换句话说，指示您的计划范围。

可通过将 **覆盖范围** 选项设置为 **是**，覆盖主排产期间为物料定义的覆盖范围时限。 在此案例中，则输入主计划编制计算应覆盖需求的天数。 覆盖时限是基于当前日期向前推算的。 在当前日期之前发生的需求始终会得到处理。

> [!NOTE]
> 要让主计划发挥最佳效果，建议根据您的计划范围调整覆盖范围时限。

### <a name="freeze"></a>锁定

锁定时限表示满足以下条件的时限：在运行新主计划时不更改现有计划订单。 将锁定计划订单，并且不建议任何新计划订单。

可通过将 **锁定** 选项设置为 **是**，覆盖主排产期间为物料定义的锁定时限。 在此案例中，输入应锁定计划活动的天数。 请注意，在此期间不会生成新的计划订单，也无法更改现有的计划订单。

### <a name="firming"></a>确认

确认时限指示将计划订单自动转换为生产订单和采购订单的时间范围。 此过程也称为 *自动确认计划订单*。

可通过将 **确定** 选项设置为 **是**，覆盖主排产期间为物料定义的确定时限。 在此案例中，则输入一个天数，在此期间应该会自动确认计划采购订单和计划生产订单。 确认时限是基于主计划编制日期向前推算的。 仅当物料与供应商关联时，才可自动确定计划采购订单。

### <a name="forecast-plan"></a>预测计划

预测计划时限指示主计划为具有预测需求的物料创建将来多长时间范围的计划订单。

可通过将 **预测计划** 选项设置为 **是**，覆盖主排产期间为物料定义的预测计划时限。 在此案例中，则输入一个天数，在此期间基于预测计划的销售预测应包括在主计划中。

### <a name="capacity"></a>容量

产能时限指示系统在为订单排产时应考虑资源在将来多长时间范围的最大产能。 换句话说，计划将通过为物料使用生产工艺路线来为生产订单排产，并考虑生产工艺路线的资源和各资源的最大产能。

可通过将 **产能** 选项设置为 **是**，覆盖主排产期间为物料定义的产能时限。 在此案例中，输入应该为计划生产订单计划的产能天数。 主计划编制使用物料的活动生产流程并从需求日期向后计划。 如果计划生产订单的需求日期在产能时限外，则提前期由物料的交货时间确定。 产能时限是基于当前日期向前推算的。

### <a name="action-message"></a>行动消息

行动消息建议为了帮助优化供应计划，从而可对现有供应订单执行的更改。 例如，可能建议提前或推迟订单，或增加或减少订单数量。

可通过将 **行动消息** 选项设置为 **是**，覆盖主排产期间为物料定义的行动消息时限。 在此案例中，则输入主计划编制应该为需求生成行动消息的天数。 行动消息时限是基于当前日期向前推算的。

有关行动消息的详细信息，请参阅[行动消息](/dynamics365/unified-operations/supply-chain/master-planning/action-messages)。

> [!NOTE]
> 计算行动消息会导致主计划的运行时间更长。 如果不定期（每天、每周等）分析和采用行动消息，请考虑在主计划运行期间关闭计算。 若要关闭计算，请为运行的主计划将 **主计划** 页上的 **行动消息** 时限设置为 **0**（零）。 并确保为所有覆盖范围组关闭 **行动消息** 设置。

### <a name="calculated-delays"></a>计算的延迟

可指定检测和报告计划订单中将来多长时间范围内可能的延迟。 这样就可以安排可能的（延迟）交付日期。

如果不能为请求的日期履行计划订单，则根据提前期、材料和产能可用性为交易安排最早的履行日期。

### <a name="approved-requisitions-time-fence"></a>已审核的申请时限

可设置主计划，以便为申请需求创建计划订单。 将 **主计划** 页 **常规** 快速选项卡上的 **包括申请** 选项设置为 **是**。 然后，已审核申请的目标为补货时，主计划将自动创建相应计划订单以履行补货。 补货方法由设置组织中的物料的供应策略确定。 在创建和审核补货申请后，不需要其他用户操作。

通过将 **按天计算的时限** 快速选项卡上的 **已审核的申请时限** 选项设置为 **是**，可覆盖主计划编制期间为物料定义的已审核申请时限。 在此案例中，输入过去的天数，在此期间来自已审核申请的具有补货目标的需求应该被列入主计划编制中。 例如，仅在未实现时，您才可以指定前十天内创建的已审核的申请中的过期需求应予以考虑和计划。

### <a name="sequencing"></a>先后顺序

可通过先后顺序，基于与成品关联的先后顺序属性安排计划订单。 通常用于准备生产订单以打包。 例如，可根据颜色和大小按特定顺序为包装箱打包。

通过将 **先后顺序** 选项设置为 **时**，可指定应该设置将来多长时间范围内的工序或作业。 请注意，时限越长，主计划的运行时间越久。

### <a name="calculated-delays"></a>计算的延迟

延迟选项有助于确保订单具有可行的的计划日期。 **主计划** 页的 **计算的延迟** 快速选项卡上有以下选项：

- **确保计划的订单不是在主计划运行日期之前创建的** – 将此选项设置为 **是** 可帮助确保不能将订单的日期安排在过去。
- **将计算的延迟添加到需求日期**（在 **计划采购订单** 下）– 将此选项设置为 **是** 将向需求添加计算的延迟。
- **将计算的延迟添加到需求日期**（在 **计划生产订单** 下）– 将此选项设置为 **是** 将向需求添加计算的延迟。
- **将计算的延迟添加到需求日期**（在 **计划转移** 下）– 将此选项设置为 **是** 将向需求添加计算的延迟。
- **将计算的延迟添加到需求日期**（在 **计划看板** 下）– 将此选项设置为 **是** 将向需求添加计算的延迟。

如果将 **将计算的延迟添加到需求日期** 选项设置为 **是** 以向需求添加延迟，系统将考虑资源的产能，并创建可行的计划订单。 重新计算计划订单日期将增加主计划的运行时间。 因此，如果不需要使用延迟，请将选项设置为 **否**。

## <a name="positive-and-negative-days"></a>正天数和负天数

正天数和负天数影响主计划如何建议计划订单和操作。 将对物料的物料覆盖范围组设置正天数和负天数。 可在 **覆盖范围组** 页（**主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**）中定义大量覆盖范围组和设置其参数。

### <a name="positive-days"></a>正天数

正天数指示主计划考虑当前库存或收货履行将来多长时间范围内的需求。 例如，如果正天数设置为 **100**，则可使用当前库存履行接下来 100 天的需求。 如果一个订单距离当前日期 150 天，则主计划将创建计划订单以满足该需求，即使物料的现有库存可满足此订单。 对于提前期较短的快销物料，您可能不希望对将来很久以后的订单使用现有库存。 在快销物料情况下，很快会用掉当前现有库存，而将来可能会下达更多订单以及时满足将来的需求，由于物料的提前期很短，所以这是可行的。

正天数也会影响行动消息。 例如，系统可能会建议增加计划采购订单，以使其包含将来正天数范围内的需求。 如果正天数设置为 **100**，并且当前日期 30 天后对某个物料有需求，则系统会创建计划订单以满足该需求。 如果当前日期 90 天后对同一个物料有需求，系统将建议在订单中增加当前日期 30 天后的数量，以便订单中也包含 90 天后的需求。 但是，如果当前日期 150 天后对该物料有需求，系统不会建议增加订单中已计划的数量。 而是创建一个新的计划订单。

正天数通常设置为物料最长提前期与覆盖范围时段之间的数字。 建议将定期采购或生产的物料分配给正天数等于物料提前期的覆盖范围组。

### <a name="negative-days"></a>负天数

负天数指示允许物料收货延迟多久。 它们表示在您的库存为负或不足时，您愿意等待多久才订购新补货。 负天数回答以下问题：应该为物料创建新的采购订单，还是使用现有采购，即使知道物料会推迟？

例如，您的某个物料的销售订单距离当前日期 15 天。 同一个物料也有采购订单。 此采购订单的收货日期距离当前日期 20 天。 您希望为该销售订单创建一个采购订单，还是使用现有订单，即使不能及时履行销售？ 如果负天数设置为小于 **5** 以指示推迟物料最多五天，则系统会创建一个新的计划采购订单以满足该销售订单。 如果负天数设置为大于 **5**，则系统使用物料的现有订单。

负天数也会影响主计划的绩效。 如果负天数设置为较大数字，则会生成大量行动消息。

建议将负天数设置为小于物料提前期的数字。

### <a name="dynamic-negative-days"></a>动态负天数

动态负天数考虑物料的提前期和您指定的负天数。 系统将根据使用以下公式计算的负天数时段创建新的计划采购订单：

提前期 + 负天数 + 当前日期 – 需求日期

系统仅使用此时段内的计划供应订单，并且创建超出其范围的新计划订单。 动态负天数的优点是其中包含单个产品提前期，以便重复使用现有订单和避免创建将在之后某天因为提前期导致的延迟而结束的新计划订单。 

有关详细信息，请参阅[负天数和动态负天数](/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]