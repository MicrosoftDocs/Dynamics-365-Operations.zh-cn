---
title: 主计划设置向导（包含视频）
description: 本文介绍如何运行主计划设置向导以设置主计划。
author: t-benebo
ms.date: 10/21/2019
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
ms.openlocfilehash: a53dfd02ac2f42fd680eb71509dbd41214160f19
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066009"
---
# <a name="master-planning-setup-wizard"></a>主计划设置向导

[!include [banner](../includes/banner.md)]

本文提供针对 **主计划设置向导** 的指南。 介绍如何计算参数建议，还提供示例来显示不同公司如何根据业务需要设置主计划。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

YouTube 上的[财务和运营播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含 [Dynamics 365 Supply Chain Management 中的主计划设置向导](https://youtu.be/c-e6n-8rZb4)视频（上面显示的）。


## <a name="specific-requirements-of-your-company"></a>您的公司的具体要求

向导的第一页询问公司的具体要求。 您对这些问题的回答不必精确，但是您应该可以提供法人的大致物料和计划订单数量。 您的回答用于配置为法人应用的参数，而不仅是应用于所选主计划的参数。 以下部分介绍计算的参数和使用的公式。

### <a name="number-of-threads"></a>线程数

- **如果制造任何物料：** 线程数 = 计划订单数 ÷ 1,000
- **如果不制造任何物料：** 线程数 = 物料数 ÷ 1,000

如果计算出的线程数超过可用线程数的 75%，则其超过每位客户的可用线程数的 75%。 （将为每个客户确定可用线程数。）

有关详细信息，请参阅[线程数](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads)。

### <a name="bundle-size"></a>捆绑大小

捆绑大小将设置为 **1**。 此值通常为最佳值，因为有助于提高主计划的性能。

有关详细信息，请参阅[帮助程序任务捆绑中的任务数](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle)。

### <a name="firming-bundle-size"></a>确认捆绑大小

- **如果制造任何物料：** 确认捆绑大小将设置为以下两个值中的较大值：**10** 和捆绑计算结果
- **如果不制造任何物料：** 确认捆绑大小将设置为以下两个值中的较大值：**50** 和捆绑计算结果

捆绑计算结果 =（计划订单数 ×（确认时限 ÷ 覆盖时限）÷ 线程数）÷ 10

### <a name="cache-size"></a>缓存大小

缓存大小将设置为 **最大值**。 此值通常为最佳值，因为有助于提高主计划的性能。

有关详细信息，请参阅[为作业捆绑中的作业分配时间](/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle)。

### <a name="manufacturing-setup"></a>制造设置

如果制造物料，则向导后面将显示 **制造设置** 页。

## <a name="scope-of-the-current-plan"></a>当前计划的范围

在向导的 **当前计划的范围** 页，您将回答与主计划中要考虑和计算的各种要求的将来时间范围有关的问题。 每个问题询问您是否要使用某项功能，以及如何配置该功能。

例如，对于预测计划功能，向导将询问“是否要在主计划中使用预测计划以便建议计划订单来满足预测的需求?”

选项如下：

- **否** – 主计划不推荐计划订单来实施预测。 在 **主计划** 的 **时限** 选项卡（**主计划 \> 设置 \> 计划 \> 主计划**）选项卡上，向导将把 **预测计划(时限)** 选项设置为 **是**，将天数设置为 **0**（零）。 此设置将覆盖在覆盖范围组中指定的时限。 因为天数设置为 **0**（零），则不使用此功能。
- **是，按照此主计划中的定义** – 字段变得可用，可在其中输入主计划将为计划订单推荐来满足预测的需求的天数。 向导将把 **预测计划(时限)** 选项设置为 **是**，将天数设置为在 **主计划** 页的 **时限** 选项卡上 **预测计划** 字段中输入的天数。 此设置将覆盖在覆盖范围组中设置的值。
- **是，按照覆盖范围中的定义** – 向导将 **预测计划(时限)** 选项设置为 **否**。 将使用在覆盖范围组中指定的时限指定为预测计划的时间长短。

此页中的其余问题及其回答采用同一个架构：

- **否** – **预测计划(时限)** 选项将设置为 **是**，天数将设置为 **0**（零）。
- **是，按照此主计划中的定义** – **预测计划(时限)** 选项将设置为 **是**。 将使用您输入的天数，并且该天数将覆盖在覆盖范围组中设置的值。
- **是，按照覆盖范围组中的定义** – **预测计划(时限)** 选项将设置为 **否**。

有关详细信息，请参阅[作业级排产](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。

## <a name="scheduling-options"></a>计划编制选项

仅当对向导第一页上的“是否制造任何计划的物料?”问题回答了 **是**，**计划编制选项** 页 才会显示。

您对此页上的第一个问题（“是否需要计划拆分为单个作业的工序?”）的回答决定 **主计划** 页的 **常规** 选项卡上的计划编制方法。

- **是** – 将使用作业级排产。
- **否** – 将使用工序级排产。

有关详细信息，请参阅[工序级排产](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling)和[作业级排产](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling)。

## <a name="updates-of-demand-and-supply"></a>需求和供应的更新

**需求和供应的更新** 页中的问题与确认、行动消息和延迟有关。

将根据您的回答和上一个部分中介绍的同一个架构更新主计划设置。

- **否** – **主计划** 页中的 **时限** 选项将设置为 **是**，天数将设置为 **0**（零）。
- **是，按照此主计划中的定义** – **时限** 选项将设置为 **是**。 将使用您输入的天数，并且该天数将覆盖在覆盖范围组中设置的值。
- **是，按照覆盖范围组中的定义** – **预时限** 选项将设置为 **否**。

对于计算的延迟，您对向导中的问题的回答将更新 **主计划** 页 **计算的延迟** 选项卡上的相应参数。

## <a name="summary-of-your-changes"></a>您的更改汇总

向导的最后一页显示根据您的响应推荐的更改。 同时显示您的设置（**当前设置**）中的值和向导推荐的值（**新配置**）。

也可以修改新配置中的参数。 参数将拆分为应用于法人的参数和仅应用于所选主计划的参数。 若要查看可通过使用此向导更改的所有设置参数，请选择页面底部的 **显示所有参数**。 然后可以更改参数。

最后，在选择 **完成** 时，将应用新配置。 如果选择 **取消**，则不应用任何更改。

## <a name="examples"></a>示例

此部分介绍两家虚构公司的设置，以便显示该设置如何根据各企业的需求而变化。

### <a name="example-1-contoso-manufacturer"></a>示例 1：Contoso Manufacturer

Contoso Manufacturer 是一家生产扬声器的制造公司。 该公司从大量供应商处购买大量用于扬声器成品的原材料和组件。 下面是它的部分供应和制造特征：

- 公司制造的最终物料采用物料清单 (BOM) 结构。
- 所有最终物料和组件通过主计划计划。 不执行手动计划。
- 将为每个最终物料的生产定义工序的工艺路线。
- 制造工厂生产最终物料。 它定义了一些铣削和钻削机器，用于处理组件。 各种组件必须由这些机器处理。
- 有多家供应商。 物料的平均提前期为一周。 同一家供应商的一组物料的提前期为七周。

在向导中，将为 Contoso Manufacturer 输入以下值：

- **覆盖范围：**

    - **问题**：“是否要指定计划区间的天数？”
    - **回答**：“是，按照覆盖范围组中的定义。”

    因为物料的提前期相差很大，所以 Contoso 不必将所有物料安排在将来的同一个期间。 将为物料创建覆盖范围组。 将把提前期相似的物料分派给同一个覆盖范围组。 每个覆盖范围组的计划区间（即覆盖时限）大致为提前期加一周的差额。 然后，主计划确保根据其提前期提前计划物料。

    因此，将为此示例创建两个覆盖范围组。 一个覆盖范围组的覆盖时限为两周，另一个的覆盖时限为八周。

    如果回答选择 **是，按照此主计划中的定义**，则输入的天数应该超过所有物料中的最大提前期。 但是，因为不必将大量物料提前这么久，所以将计算大量计划订单，但是从不使用这些订单。 因此，主计划运行时间将增加。

- **计划编制：**

    - **问题**：“是否需要计划拆分为单个作业的工序?”
    - **回答**：“是。”

    Contoso Manufacturing 必须计划和安排将对车间执行的单个作业。 因此，将使用作业级排产。

- **产能：**

    - **问题**：“是否要使用资源的产能进行排产？”
    - **回答**：“是，按照此主计划中的定义”。 输入了 **10 天**。

    将限制铣削和钻削机器的数量。 生产计划必须考虑此限制，并根据资源产能及时安排作业。 换句话说，将根据资源的限制重新计划排产的作业。 除了定义的期间，计划还将使用提前期。 （计划的生产订单可重叠。）因为物料的生产提前期为七天，所以将考虑主计划在 10 天内的资源产能。

- **先后顺序：**

    - **问题**：“是否要使用产品的顺序值为计划的订单排序？”
    - **回答**：“是，按照覆盖范围组中的定义。”

    将为每个最终物料的生产定义工艺路线。 因此，主计划将根据定义的工艺路线及时安排订单。

- **分解：**

    - **问题**：“是否要计划物料清单中所有元素的订单(针对父级和所有子级物料进行计划)?”
    - **回答**：“是，按照覆盖范围组中的定义。”

    必须计划用于生产的所有物料。 因为物料的提前期相差极大，所以主计划在使用覆盖范围组时的性能更佳。 而且，可以输入一周的差额，并且可以对与覆盖范围相同的时间进行分解。

### <a name="example-2-contoso-retailer"></a>示例 2：Contoso Retailer

Contoso Retailer 是时尚行业的一家分销公司。 该公司使用主计划，基于预测销量计算应在何时下达采购订单。 下面是该公司的部分特征：

- Contoso Retailer 使用需求预测预测销量。 将根据此预测计划采购订单。
- 商店使用补货申请。
- 从主仓库到每家商店的提前期为所有物料大约两周。

在向导中，将为 Contoso Retailer 输入以下值：

- **预测需求：**

    - **问题**：“是否要在主计划中使用预测计划以便建议计划订单来满足预测的需求?”
    - **回答**：“是，按照此主计划中的定义”。

    Contoso 中有一个需求预测，用于预测其销量。 因此，主计划必须推荐计划订单以实现预测。

- **确认：**

    - **问题**：“是否希望主计划自动将计划订单确认到订单单据(例如生产或采购订单)?”
    - **回答**：“是，按照此主计划中的定义”。 输入了 **1 天**。

    因为 Contoso Retailer 将直接从计划采购订单创建采购订单，所以如果自动确认计划采购订单，这非常有用。 因为公司每天运行主计划，所以一天的确认时限将自动确认下一天需要的所有订单。

- **已审核的申请：**

    - **问题**：“是否要包含已审核的零售商店补货申请中的需求？”
    - **回答**：“是，按照此主计划中的定义”。 输入了 **1 天**。

    Contoso 使用其商店的已审核申请创建计划采购订单来为这些商店补货。 因为每天运行主计划，所以计划中将包含前一天的申请。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
