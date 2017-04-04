---
title: "预算编制主页"
description: "此主题提供预算功能的组件，预算的工具和报告功能概览。Microsoft Dynamics 365 中的工序。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: f7b4efc06b8e64c05da026850b41cb5b68c33ec3
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-home-page"></a>预算编制主页

此主题提供预算功能的组件，预算的工具和报告功能概览。Microsoft Dynamics 365 中的工序。

<a name="components-of-budgeting-functionality"></a>预算功能组件
-------------------------------------

公司的资源计划周期通常包含计划、预算和预测活动。
![[] (预算功能的组件。/media/budgeting 功能 Components.jpg)](。/media/budgeting 功能) components.jpg 战略计划编制和年度预算计划的过程通过预算计划文档支持。 预算计划文档以 Microsoft Excel 紧密集成。 用户可配置无数个货币和数量方案，也可以定义预算组织层次结构以支持自上而下和自下而上的预算方法。 在 Microsoft Dynamics 365 for Operations 中建立和审核预算后，预算计划将转换为预算登记分录。 预算登记分录提供了维护预算和通过预算代码保持金额的可追溯性的工具。 预算登记分录可让您修订原始预算、执行转移和从上一年结转预算金额。 根据建立的预算，公司可启用预算控制。 控制的级别取决于组织文化和组织成熟度级别。 成熟度较低的组织可能将预算保留“原样”，当预算未达到期望时，它们可能更倾向于被动地响应，而不会主动采取措施。 其他组织可能启用预算控制策略以防止用户在没有预算资金时进行采购。 最后，脂肪成熟组织可能受教育建立员工目标有关组织的有组织区域性策略，并通过遵循这些目标 (例如{{而不考虑“联机会话是：instead_of}}出差”。 工序的 Dynamics 365 包括通过公司的法规困难选择禁止过帐控制 (将转到在预算) 或为"柔性"的控制的预算控制框架 (从中它们将超出预算资金的有效用户警告，但可以为他们自己确定如何执行)。 此外，您可以使用滚动预测。 滚动预测是预算常规的比较。实际和使用定义公司经营的准确预算。 滚动预测还用于确定趋势。 在 Microsoft Dynamics 365 for Operations 中，滚动预测通过作为初始规划活动的预算计划文档获得支持。 滚动预测可以与针对即将到来的预算周期的规划并行执行。

-   [基本预算编制：概述和配置](basic-budgeting-overview-configuration.md)
-   [预算控制：概述和配置](budget-control-overview-configuration.md)
-   [预算计划：概述和配置](budget-planning-overview-configuration.md)
-   [职位预测](position-forecasting.md)
-   预算计划文档理由 [] (预算计划对齐方式 docs.md)
-   [预算计划的 Microsoft Excel 模板] (将预算计划 templates.md Excel)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Dynamics 365 for Operations 中的预算工具
[] (![预算的工具。/media/budgeting-tools.jpg)](。/media/budgeting-tools.jpg) 

其他计划和预算功能跨 Dynamics 365 for Operations 提供，并且与分类帐预算集成。

-   **劳动力预算** - 劳动力预算包括针对职位、薪酬组等方面的详细的预算成本构成计划。
-   **固定资产预算** - 基于固定资产信息，您可以计算计划的折旧并记录其他与固定资产相关的计划交易记录。
-   **项目预算** – 在项目模块中，可以创建详细的项目预测。 项目预测将包括有关计划的工时、支出、费用和物料的详细信息。
-   **基于历史交易记录数据** –的需求预测，您可以估计将来的需求和要求库存创建预测。

有关如何将计划数据从其他模板放入预算计划的信息，请参阅[预算计划与其他模块的集成](budget-planning-integration-other-modules.md)。

## <a name="user-interface-and-reporting-capabilities"></a>用户界面和报告功能
在 Dynamics 365 for Operations 中，用户可以直接在 Dynamics 365 for Operations 客户端中创建预算计划（通过使用可配置预算计划文档页），也可以通过 Excel 创建预算计划。 Excel 提供了几个额外功能。 例如，您可以使用外部数据作为预算计划的来源，执行自定义计算，并使用 Microsoft 数据透视表和图表。 预算计划流程中的大多数变量都可配置。 例如，您可以定义执行预算的人员、预算的对象以及具体流程。 尽管您可以使用 Excel 进行预算计划，但 Dynamics 365 for Operations 被保留为唯一的事实来源，帮助防止预算控制问题。 周期性流程可用于将预算的初始数据纳入预算计划。 对于报告，Dynamics 365 for Operations 提供了一系列标准查询页，供您查看和分析预算数据。 预算计划数据可通过 Management Reporter 访问，单独的预算计划方案可在 Management Reporter 报告中显示为列。





