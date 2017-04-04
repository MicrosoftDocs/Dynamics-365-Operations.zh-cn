---
title: "建模一精瘦的组织"
description: "文本提供有关建模精益组织的重要概念的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 536b20d5c4c2030800df25d0d227deaac386aee5
ms.lasthandoff: 03/29/2017


---

# <a name="modeling-a-lean-organization"></a>建模一精瘦的组织

文本提供有关建模精益组织的重要概念的信息。 

通常，lean manufacturing 通常不只是不相关的看板规则或材料供应策略的集合。 材料和产品在整个工作单元中的流动以及特定生产或供应方案的位置可描述为流程或传输活动的一个序列或小型网络。 此序列或网络称为生产流。

## <a name="production-flows-in-lean-manufacturing"></a>lean manufacturing 中的生产流
在基于生产订单的生产方案中，可将材料发给特定的生产订单。 在基于物料清单 (BOM) 和工艺路线一系列工序期间，制造产品，并最终在提供的位置接收产品。 生产订单的吞吐量时间从数分钟到数周不等。 所有相关成本、材料和人工都在生产订单上累计。 为了缩短交货提前期和减少批量生产导致的工作中心之间的过量库存，lean manufacturing 在制造和仓库补货中引入了看板补货和看板超市。 通常，这些功能会中断部分独立的看板周期的生产。 针对半成品的看板补货不再由成品的订单触发。 为了为在 Microsoft Dynamics AX 中建议的各种看板方案重新建立生产和成本上下文，我们引入了基于活动的生产流程以作为 lean manufacturing 的支柱。 所有看板规则都引用了此预定义结构。 基于活动的模型支持比支持的 Dynamics AX 之前的 Lean manufacturing 版本更广泛的方案设置。 不过，由于所有方案使用相同的基于活动的用户界面，此模型不会为车间工作人员增加复杂性。

## <a name="semifinished-products-nonbom-levels"></a>临时 nonBOM (层级)
Lean Manufacturing for Dynamics AX 将库产品和半成品整合到单个框架中，从而为所有案例提供统一的用户体验。 由于此体系结构，附加的物料清单层将不再需要引入以启用用于半成品的看板。 此体系结构还有助于使库存交易记录缩减为最小数量。

## <a name="products-and-material-in-work-in-progress"></a>正在处理中的产品和材料
如果每个领料流程或看板登记都生成了消耗的物料的交易记录，那么将批次大小减小至 lean manufacturing 中的单件流的理想状态可能导致库存交易记录显著增加。 生产流体系结构允许将材料随贮存或运输物料处理单元大小中的领料看板一起转移到生产流。 发放的物料的值将加到与生产流相关的在制品 (WIP) 帐户中。 此行为类似于发放到生产订单的物料的行为。 同一原则适用于产品和半成品。 除非这些产品是在生产流中创建、转移或消耗的，否则库存交易记录是可选的。 当产品过帐到库存后，生产流的 WIP 帐户将减去相关的标准成本，从而变小。

## <a name="value-streams-and-value-stream-mapping"></a>价值流和价值流映射
Lean Manufacturing for Dynamics AX 的体系结构的灵感来源于 Womack 和 Jones 提出的 5 大精益原则：客户价值、价值流、流动、拉动和尽善尽美。 在现实制造世界中，实施 lean manufacturing 解决方案的一个久经考验的方法是价值流映射 (VSM)。 此方法由 Rother 和 Shook 在其 Lean Manufacturing 研究所出版物《学会观察》中引入。 在 Dynamics AX 中，未来状态价值流可建模为生产流版本。 价值流的所有流程都将建模为流度活动。 如果必须登记转移状态或者需要到库存领料或合并装运的集成，那么移动或转移可建模为转移活动。 价值流本身将建模为 Dynamics AX 中的运营单位。 因此，价值流可以用作财务维度。

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>基于生产流的精益制造的成本计算
生产流的成本的定期合并可纠正相关 WIP 帐户和为生产流提供的产品确定的差异。

## <a name="continuous-improvement"></a>持续改进
为了更好地支持持续改进，应在时效性版本中实施生产流。 因此，现有生产流版本，以及所有相关看板规则，可复制到生产流的未来版本。 此外，在为生产验证和启用未来状态的生产流前可以建模未来状态的生产流。 为帮助确保物料在转换日期当天和以后无缝地流动，来自旧生产流版本的现有看板将自动关联到新版本。

## <a name="simplicity"></a>简易性
对于 Lean manufacturing 的实施 Dynamics AX 中，我们在选择启用唯一可扩展的体系结构中将建模的简单和复杂生产方案的生产流程和活动方法。 在活动的概念的找找显示需要它的这些用户的新简单：物流和车间工作人员。 通过针对基于活动的作业（而不是库存交易记录）进行报告，适用于所有精益制造变型的统一用户界面将业务复杂性从用户界面转移到其所属的地方：作为精益制造的支柱的生产流。


