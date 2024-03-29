---
title: 基于报价单和询价的计划
description: 本文介绍如何设置主计划以在生成计划订单时考虑报价单和询价 (RFQ)。
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690072"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>基于报价单和询价的计划

[!include [banner](../../includes/banner.md)]

报价单和询价 (RFQ) 代表着可能到来的订单，甚至是可能在未来得到的订单。 因此，在主计划期间考虑这些信息是有意义的，进而可以根据现有的询价以及每个报价单将成为实际订单的可能性来计划额外的产品供应。 本文介绍如何设置主计划以在生成计划订单时考虑报价单和询价。

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>设置主计划以考虑销售报价单和/或询价

使用以下过程将主计划设置为考虑销售报价单和/或询价。

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**。
1. 在列表窗格中选择一个现有计划，或在操作窗格上选择 **新建** 创建新计划。
1. 在 **常规** 快速选项卡上，设置以下字段：

    - **包括销售报价单** – 将此选项设置为 *是* 将在当前计划运行时考虑销售报价单。 将其设置为 *否* 将忽略。
    - **概率 %** – 设置将报价单包含在主计划中所需达到的最低置信度级别。 主计划计算将包括从具有此概率百分比或更高概率的机会创建的所有报价单。 要包括所有报价单，包括没有被分配概率或没有关联机会的报价单，将此字段设置为 *0*（零）。 有关报价单概率的更多信息，请参阅下一节。
    - **包括询价** – 将此选项设置为 *是* 将在当前计划运行时考虑询价。 将其设置为 *否* 将忽略。 如果您选择考虑询价，系统将为它们创建计划采购订单，但在解决询价之前不会指定供应商。 为询价创建的计划采购订单可能会影响其他计划订单的数量。

1. 继续以通常的方式设置您的主计划。

## <a name="assign-and-view-probabilities-for-quotations"></a>分配和查看报价单的概率

如上一节所述，主计划会仅考虑达到或超过为计划定义的概率阈值（如果已定义阈值）的报价单。 但是，概率不直接在每个报价单上设置。 而是继承自用于生成报价单的机会。 因此，直接在 **所有报价单** 页面创建的报价单不会被分配概率或关联机会，主计划也不会考虑它们（除非 **概率 %** 字段设置为 *0* \[零\]）。 要为其分配概率，报价单必须从机会生成。

### <a name="create-a-quotation-from-an-opportunity"></a>从机会创建报价单

使用以下过程为机会分配概率，然后从该机会创建报价单。

1. 转到 **销售和市场营销 \> 关系 \> 机会 \> 所有机会**。
1. 选择现有机会，或在操作窗格上选择 **新建** 创建新机会。
1. 填写机会页面以您需要的方式识别机会。 确保将 **概率** 字段设置为适当的值。 只有设置为查找此值或更高值的概率的主计划会考虑由此机会生成的报价单。
1. 在操作窗格上，选择 **保存**。
1. 在操作窗格的 **机会** 选项卡上，在 **新建** 组中，根据要创建的报价单类型，选择 **销售报价单** 或 **项目报价单**。
1. 在 **创建报价单** 对话框中，根据需要设置字段，然后选择 **确定**。
1. 将创建并打开一个新报价单。 在 **行** 快速选项卡，使用工具栏根据需要添加销售行或项目行来定义报价单的内容。
1. 在操作窗格上，选择 **保存**。 然后关闭报价单。

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>查看分配给报价单的概率

查看分配给报价单的概率的唯一方法是打开用于创建该报价单的机会，如以下过程所述。

1. 转到 **销售和市场营销 \> 销售报价单 \> 所有报价单**。
1. 如果 **机会 ID** 列未显示（在默认安装中隐藏），按照以下步骤让其临时显示。 （或者，要使 **机会 ID** 列保持可用，创建一个包含它的[已保存视图](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json)。）

    1. 在网格中选择并按住（或右键单击），然后选择 **插入列**。
    1. 在 **插入列** 对话框中，找到 **字段** 字段设置为 *机会* 的行，选中该行的 **选择** 复选框。
    1. 选择 **更新** 将选定的列添加到 **所有报价单** 页面。

1. 在网格中，找到相关报价单的行。 然后，在 **机会 ID** 列中，选择该行的值。

    > [!NOTE]
    > 如果要查找项目报价单，可能必须选择 **报价单类型** 列标题并清除其筛选器。 在默认安装中，此筛选器设置为仅显示销售报价单。

1. 相关机会将打开。 您现在可以根据需要查看和编辑 **概率** 值了。
