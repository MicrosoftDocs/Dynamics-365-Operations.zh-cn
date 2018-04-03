---
title: "预算编制主页"
description: "此主题概要介绍了 Microsoft Dynamics 365 for Finance and Operations 中的预算编制功能组件、预算编制工具和申报功能。"
author: twheeloc
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: efe348d9967ab7594afd22a3ebb4df76dc6607f8
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="budgeting-home-page"></a>预算编制主页

[!include[banner](../includes/banner.md)]


此主题概要介绍了 Finance and Operations 中的预算编制功能组件、预算编制工具和申报功能。 

<a name="components-of-budgeting-functionality"></a>预算功能组件
-------------------------------------

公司的资源计划周期通常包含计划、预算和预测活动。

[![预算功能组件](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

长期战略计划和年度预算计划的流程均通过预算计划文档来获得支持。 预算计划文档与 Microsoft Excel 紧密集成在一起。 用户可配置无数个货币和数量方案，也可以定义一个预算组织层次结构以支持自上而下和自下而上的预算方法。 在 Finance and Operations 中建立和审核预算之后，将预算计划转换为预算登记分录。 预算登记分录提供了用于维护预算以及通过预算代码保持金额的可追溯性的工具。 预算登记分录可让您修订原始预算、执行转移和从上一年结转预算金额。 根据建立的预算，公司可启用预算控制。 控制的级别取决于组织文化和组织的成熟度级别。 成熟度较低的组织可能将预算保留“原样”，当预算未达到预期时，它们可能更多的是被动地响应，而不是主动采取措施。 其他组织可能会启用预算控制策略以防止用户在没有预算资金时进行采购。

最后，非常成熟的组织可能会建立一种组织文化，在这种文化中，员工将获得有关组织目标的培训，并通过“考虑在线会议而不是出差”之类的策略实现这些目标。 Finance and Operations 包含让公司的管理层选择硬控制（防止超过预算的过帐）或软控制（用户将收到超过可用预算资金的警告，但用户可以自行决定如何继续）的预算控制框架。 最后，您可使用滚动预测。 滚动预测是预算与实际支出的定期比较，用于确定公司的预算执行状况。 滚动预测还用于确定趋势。 在 Finance and Operations 中，滚动预测通过在初始规划活动中制定的预算计划文档来获得支持。 滚动预测可以与针对即将到来的预算周期的规划并行执行。

-   [基本预算编制：概述和配置](basic-budgeting-overview-configuration.md)
-   [预算控制：概述和配置](budget-control-overview-configuration.md)
-   [预算计划：概述和配置](budget-planning-overview-configuration.md)
-   [职位预测](position-forecasting.md)
-   [预算计划证明文档](budget-planning-justification-docs.md)
-   [适用于预算计划的 Microsoft Excel 模板](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-finance-and-operations"></a>Finance and Operations 中的预算工具
[![预算工具](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

其他计划和预算功能跨 Finance and Operations 提供，并且与分类帐预算集成在一起。

-   **劳动力预算** - 劳动力预算包括针对职位、薪酬组等方面的详细的预算成本构成计划。
-   **固定资产预算** - 基于固定资产信息，您可以计算计划的折旧并记录其他与固定资产相关的计划交易记录。
-   **项目预算** – 在项目模块中，可以创建详细的项目预测。 项目预测将包括有关计划的工时、支出、费用和物料的详细信息。
-   **需求预测** - 基于历史交易记录数据，您可以预估未来库存需求并创建需求预测。

有关如何将计划数据从其他模板放入预算计划的信息，请参阅[预算计划与其他模块的集成](budget-planning-integration-other-modules.md)。

## <a name="user-interface-and-reporting-capabilities"></a>用户界面和报告功能
在 Finance and Operations 中，用户可以直接在 Finance and Operations 客户端中创建预算计划（通过使用可配置预算计划文档页），也可以通过 Excel 创建预算计划。 Excel 提供了几个额外功能。 例如，您可以使用外部数据作为预算计划的来源，执行自定义计算，并使用 Microsoft 数据透视表和图表。 预算计划流程中的大多数变量都可配置。 

例如，您可以定义执行预算的人员、预算的对象以及具体流程。 尽管您可以使用 Excel 进行预算计划，但 Finance and Operations 仍将作为唯一的数据来源，帮助防止预算控制问题。 周期性流程可用于将预算的初始数据纳入预算计划。 对于报告，Finance and Operations 提供了一系列标准查询页，供您查看和分析预算数据。 预算计划数据可通过 Management Reporter 访问，单独的预算计划方案可在 Management Reporter 报告中显示为列。







