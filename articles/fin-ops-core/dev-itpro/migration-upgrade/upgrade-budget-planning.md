---
title: 升级预算计划
description: 本文说明必须重新配置的功能，描述完成升级后应考虑的新功能。
author: panolte
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: panolte
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7d8d59def24fd138b4cf1d36e286b786e13b096e
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124019"
---
# <a name="upgrade-budget-planning"></a>升级预算计划

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012 和 Dynamics 365 Finance 的预算计划之间存在显著差异。 某些功能尚未升级，因此需要重新配置。 本文说明必须重新配置的功能，描述完成升级后应考虑的新功能。  

Finance 的预算计划有很多 Dynamics AX 2012 未提供的增强功能。 本文说明升级客户必须进行的更改。 还指出了升级过程中应考虑的新功能。 由于更改范围原因，任何现有预算计划将无法打开，直到进行了本文列出的更改。 但是，报表应继续工作，无需其他更改。

## <a name="overview-of-changes"></a>更改概览
财务和运营的预算进行了许多重大更改。 这些更改用于让预算计划配置更加轻松且更有可能重用，进而减少年复一年的维护和设置。 AX 2012 的以下区域不再出现在 Finance 中：

-   预算计划模板（预算计划配置）
-   预算计划文件夹（预算计划配置）
-   方案约束（预算计划配置）
-   用于预算计划阶段规则和模板的模板（预算计划流程）
-   工作表模板的矩阵字段
-   预算计划 Microsoft Excel 模板向导

一些新概念不能从以前的功能直接升级。 因此，您必须完成某些重新配置以处理这些新概念。 以下各部分介绍已替换上述列表中各项的概念。

### <a name="columns"></a>列

列是替换 Excel 模板的组成部分以及矩阵字段的新概念。 列可以表示期间、月份、季度、年份或所有时间。 时间引用是动态的。 它指向与预算流程相关的期间或年份。 例如，**上一年 1 月** 列引用 -1 年的会计期间 1。 列特定于一个预算计划方案，如实际或预算请求。

### <a name="layouts"></a>布局

布局是替换 Excel 模板的新概念。 布局包含定义应显示哪个预算或实际数据和期间的列。 布局还在客户和 Excel 加载项之间共享。 因此，当您在财务和运营客户端输入或查看数据时的用户体验要好于 AX 2012 的用户体验。 若要在 Finance 客户端输入数据，您将不再被限制只查看和输入事务视图中的一个方案。 而比较视图让您可以同时查看和输入多个期间和帐户的金额。 还可以定义布局，以便您可以输入和查看币种、注释和其他可选数据。 布局还允许您定义应显示的分类帐维度和维度描述。 布局还包含了方案约束来定义模板中哪些列可以编辑，以及哪些列应在 Excel 中提供。 在您定义了一个布局后，将为其生成模板。 反之，此模板创建相应的 Excel 模板。 然后，您可以编辑 Excel 模板以包含更多公式和格式，然后将它们再次上载。 布局随后被分配到 **预算计划流程** 页的每个阶段规则。 因此，布局替换模板，并以相同方式分配和使用。

### <a name="budget-planning-processes"></a>预算计划过程

预算计划流程在 AX 2012 中大致相同。 最重要的更改是模板替换为布局。 如果之前有任何流程在 AX 2012 完成，流程状态将更新为进行中，以便可以进行更改。 必须分配布局，以便每个阶段规则确定在客户端中打开计划时显示哪些方案和时间期间。 布局还确定哪些 Excel 模板在 Dynamic 365 Finance 外部打开，以便您可以查看预算。 **默认科目结构** 是预算计划流程的新的必填字段。 对于每个预算计划流程，应指定应该用于预算的主科目结构。

### <a name="attachments"></a>附件

在 AX 2012 中，理由文档保存到附件文件夹。 以前的理由文档将不升级。 理由文档现在存储于数据库中。 如果此信息应保存在升级的版本中，您可以通过使用操作窗格中的 **理由** 按钮，作为附件为每个计划上载最终理由文档。 在 AX 2012 中，每个预算计划的 Excel 工作表基于模板创建。 在 Finance 中，所有计划打开布局的副本。 但是，不保存对 Excel 文件的更改。 每个计划分别使用的所有公式或支持信息必须通过文档、理由文档或某些其他补充流程添加。

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>从 AX 2012 配置升级后的环境
为了帮助您确定如何配置升级的系统，以下示例使用来自 AX 2012 演示数据的升级的预算流程。 列的默认配置数据已创建，为升级流程提供帮助。 如果不能满足您的配置要求，您可以更新或删除此默认数据。 **注意：** 系统中存在不进行设置的新的必填字段。 如果您在某个页面上被卡住，如 **预算计划配置** 页，并且不能导航，您可以关闭您的浏览器，然后重新打开不同的页面，按正确顺序输入详细信息。 存在没有设置的必填字段。 因此，在完成所有配置并设置所有必填字段前可能出现问题。 本文说明如何根据需要设置这些字段。 以下是这些必填字段的一部分：

-   **预算计划流程** 页：**默认科目结构** 字段
-   **预算计划流程** 页：**预算计划阶段规则和布局** 快速选项卡上的 **布局** 字段在

### <a name="define-columns-and-layouts"></a>定义列和布局

1. 在 **预算计划配置** 页上，单击 **列** 选项卡。作为升级的一部分，新列根据您的预算计划行自动创建。 列现在使用动态日期，其时间和年份从在预算计划流程中定义的会计年度算起。 **注意：** 由于升级期间的性能原因，假定所有预算周期表示日历年度，不是会计年度。 如果您使用会计年度，您必须进行编辑以将列正确映射到其会计年度。 例如，以下元素存在于 AX 2012 中：
   -   预算计划方案：实际、基准、预算请求、已审核的预算
   -   2017 年所有方案的预算计划行和 2017 年和 2016 年的实际值

   以下列将在财务和运营中创建：

   | 列名    | 预算计划方案 | 列时段 | 年偏移 |
   |----------------|----------------------|--------------------|-------------|
   | 一月方案 1 | 实际值              | 1                  | 0           |
   | 一月方案 2 | 基线             | 1                  | 0           |
   | 一月方案 3 | 预算请求       | 1                  | 0           |
   | 一月方案 4 | 已审核的预算      | 1                  | 0           |
   | 一月方案 5 | 实际值              | 1                  | -1          |
   | 二月方案 1 | 实际值              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   在此示例中，名为 **一月方案 1** 的列为被发现一月存在交易记录的最近预算计划交易记录数据创建。 类似列为包含数据的每个方案创建。 在该年度的所有期间均存在列之后，列为以前年度创建。
2. 更改列名称和描述以及所有其他详细信息，在客户端手动更改，或通过指向预算计划列数据实体的 Excel 加载项进行批量更新。 之前为矩阵字段设置的所有筛选器现在在列中设置。
3. 创建新的预算计划布局。 指向多个列的布局定义显示在 Excel 和客户端中的视图。 布局首先需要您指定分类帐维度集来确定哪些财务维度可以输入。 在指定维度集后，单击 **描述** 选择要包含在布局中的维度描述。
4. 在 **布局元素** 快速选项卡，单击 **添加** 为每行添加元数据，如币种、注释或确定收入和费用行的预算类。 接下来，为时间期间添加列，以及应用于此预算周期和阶段的方案。 您可以在客户端或通过指向预算计划布局元素数据实体的 Excel 加载项进行手动更改。
5. 对于每个布局元素，选择该列是否可编辑，以及列是否应显示在此布局的 Excel 工作簿中。 **注意：** 对于我们的历史计划，您可能需要考虑显示该流程所有预算计划方案的 12 个月度列的布局。

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>更新预算计划流程以为每个预算阶段使用适当的布局

1.  在 **预算计划流程** 页，选择要配置的流程。
2.  在操作窗格中单击 **编辑**。
3.  为此预算计划流程指定默认科目结构。 **默认科目结构** 是必须设置的新必填字段。
4.  在 **预算计划阶段规则和布局** 快速选项卡上，在 **布局** 字段中，选择以前配置且适合此阶段的布局。
5.  继续选择为各个预算计划阶段选择相同或不同的布局，然后保存您的更改。

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>要在预算流程考虑的其他功能
### <a name="budget-planning-workspace"></a>预算计划工作区

此工作区同时为预算所有者和各个预算参与者设计。 它具有指向需要您注意的所有预算文档的链接。 还有预算流程的报表和关键绩效指标 (KPI)。 预算管理员可以在 **预算编制参数** 页为所有用户定义当前的预算计划流程。 在 **工作区设置** 选项卡，**预算计划** 快速选项卡包含您可以在其中选择预算计划流程的字段。

### <a name="alternate-layouts"></a>备用布局

备选布局是让您可以在不同布局中查看计划的新功能。 可以作为选项提供一个或多个布局。 您随后可以在月度布局或季度布局中查看预算计划。 您在 **预算计划流程** 页的 **预算计划阶段规则和布局** 快速选项卡上定义备用布局。

### <a name="budget-milestones"></a>预算里程碑

作为预算流程的一部分，了解关键日期和截止时间非常重要。 您现在可以配置日期以使它们具有描述。 预算用户打开预算进行编辑或查看分配给他们的任何内容时将看到这些描述。

### <a name="copy-from-budget-plan-allocation"></a>从预算计划分配复制

新分配方法允许您从父计划分配到子计划，而不必通过层次结构中的中间级别。 此方对于以前只是为预算分配和审核创建财务维度的客户尤其有用。

### <a name="generating-budget-plans-from-new-budget-sources"></a>从新预算来源生成预算计划

以下选项添加为定期流程。 这些选项让您可以使用其他模块的现有数据作为起始点生成预算计划：

-   从需求预测生成预算计划
-   从供应预测生成预算计划
-   从项目生成预算计划
-   从预算登记簿生成预算计划

### <a name="more-complete-tracking-of-amounts"></a>更完整的金额跟踪

在 AX 2012 中，预算计划有为每个值都存储的单个计划金额。 在 Finance 中，已扩展了数据模型。 现在每个值有记帐币种、交易币种和申报币种。 在升级期间，将自动为现有数据填充这些新列。

### <a name="do-not-convert-currency-in-aggregation"></a>不要转换合并中的币种

通常，在子计划聚合到父级别时，金额将从交易币种自动转换为组织的记帐币种。 在您将 **不要转换聚合中的币种** 选项设置为 **否** 时，聚合金额仍保留为原始币种。 因此，此选项允许对受汇率波动影响的部分进行更精确的调整。

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>从预算计划回顾到对预算作出贡献的其他模块

预算计划可从需求或供应预测、项目和其他区域生成。 按维度集划分的预算计划查询包括让您运行查询以确定预算计划的来源数据的若干选项。

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>覆盖或追加到分配计划的计划。

如果存在多个必须分配的金额来源，可以指定应该附加的金额。 在这种情况下，金额不会覆盖任何现有金额。 而是追加到现有金额。

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>预算计划配置的默认财务维度集

**预算计划配置** 页可现在包括可以在其中指定默认财务维度集的字段。 虽然此字段为可选字段，但对于某些查询可能是必填项。 如果您希望按维度集分组或筛选报告分组，此字段也可能是必填项。

### <a name="data-entities"></a>数据实体

若干数据实体已添加以支持预算计划的快速实施。 实体还允许您通过 Excel 进行许多更改。 因此，无需通过客户端一次只创建一个物料。 这是新数据实体的列表：

-   实体名称
-   预算参数
-   预算计划参数
-   预算计划方案
-   预算计划阶段
-   预算计划工作流阶段
-   预算计划分配表
-   预算计划阶段分配
-   预算计划优先级
-   预算计划列
-   预算计划布局元素






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
