---
title: "预算的 Excel 计划模板"
description: "此主题描述如何创建可与预算计划的 Microsoft Excel 模板。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>预算的 Excel 计划模板

此主题描述如何创建可与预算计划的 Microsoft Excel 模板。

本主题说明如何创建使用标准演示数据集和管理员用户，将使用登录与预算计划的 Excel 模板。 有关预算计划的详细信息，请参阅预算计划的概览。[] (预算计划概览 configuration.md) 您还可以按照 [101] (预算计划的基本了解模块配置和使用预算的原则 plan.md 教程)。

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>使用预算计划文档的布局，生成工作表
使用一个或多个布局，预算计划文档可以查看和编辑的。 每个布局可以具有一个关联的编辑预算计划文档模板和查看将 Excel 工作表的预算计划数据。 使用现有的布局配置，{{在此：In}}主题，预算计划文档模板生成。 **打开预算计划列出** ** (预算**&gt; ** **预算计划)。 **单击新**创建一个新的预算计划文档。 [] (![bpt1。/media/bpt11-1024x552.png)](。/media/bpt11.png) 

** **使用添加行"选项添加行。 **查看预算计划文档的布局配置单击**布局。 
[] (![bpt2。/media/bpt2-1024x274.png)](。/media/bpt2.png) 

您可以查看和调整布局配置它根据需要。 **转到模板** &gt; ** **则生成创建此布局的 Excel 文件。 在模板生成后，是**模板** &gt; **视图**打开和查看预算计划文档模板。 您可以保存该 Excel 文件。您当地的驱动器。 [] (![bpt3。/media/bpt3-1024x545.png)](。/media/bpt3.png) 

> [!NOTE] 
> 在 Excel 模板与后，预算计划文档的布局不能编辑。 若要修改布局，请删除与 Excel 模板文件和成重新生成它。 这在同步的工作表布局和需要保留字段。 

Excel 模板将包含所有从预算计划文档的布局，**元素可用于列将工作表** true。 重叠元素在 Excel 模板不允许。 例如，布局包含，如果请求 Q1，请求，Q3 Q2 请求和请求 Q4 列和季度 4 表示所有列的一个总额的总计列，则请求，每季度列"列提供使用 Excel 模板。 因为数据表中可能也就废弃和不精确，Excel 文件不能重叠时更新列在更新期间。

[] (![bpt4。/media/bpt4-1024x615.png)](。/media/bpt4.png)

> [!NOTE] 
> 使用 Excel，为了避免与查看和编辑预算计划数据的潜在问题，同一用户应将记录到工序的 Dynamics 365 和 Microsoft Dynamics Office 扩展数据连接器程序。

## <a name="add-a-header-to-budget-plan-document-template"></a>表头添加到预算计划文档模板
若要添加页眉信息，请选择在 Excel 文件的顶行并插入空白行。 **单击 Design ** **在数据连接器**添加页眉字段到的 Excel 文件。

[] (![bpt5。/media/bpt5-1024x615.png)](。/media/bpt5.png) 

** Design **在选项卡上，依次单击** ** ** **添加字段，然后选择 BudgetPlanHeader ** **为实体数据源。

[] (![bpt6。/media/bpt6-1024x615.png)](。/media/bpt6.png)

利游标到 Excel 文件的所需位置。 **字段添加标签的单击**标签添加到所选的库位。 **选择添加值**添加值字段到所选位置。 **单击"完成**设计器关闭。

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[] (![bpt7。/media/bpt7.png)](。/media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>添加一计算列到预算计划文档表模板
--------------------------------------------------------------

接下来，计算列将添加到生成的预算计划文档模板。 **请求**总 A 列，汇总 Q1 请求：请求 Q4 列和**列，根据调整**一个预定义的系数**重新计算总请求**列。

**单击 Design ** **在数据 Connector **添加列到的表。 单击** **编辑。BudgetPlanWorksheet ** **启动添加的数据源旁边的列。

[] (![bpt8。/media/bpt8-1024x301.png)](。/media/bpt8.png) 

所选字段组显示可用模板中的列。 **添加一个新列的**单击"配方"。 给定新列然后将其粘贴配方**到配方**字段。 ** **单击插入列的更新。

[] (![bpt12。/media/bpt12-1024x565.png)](。/media/bpt12.png)

> [!NOTE] 
> 若要定义配方，创建在电子表格的配方，然后复制到** **设计窗口。 工序必须表的 Dynamics 365。通常称作“AXTable1”。 例如，汇总 Q1 请求：请求 Q4 在电子表格中，AxTable1 公式=\[请求\]Q1 +AxTable1 请求\[Q2\]+AxTable1\[请求 Q3\]+AxTable1\[请求 Q4\]列。

重复上述步骤插入**调整**列。 中此列所使用公式= AxTable1\[合计\]请求\*$I$1。 这将采取的单元格中的 I1 值并乘以**的请求**请在列的值计算调整金额。

保存然后关闭该 Excel 文件。 后退工序的 Dynamics 365，和布局** **，单击**模板 &gt; 上载**上载为预算规划使用的保存的 Excel 模板。 

[] (![bpt10。/media/bpt10-1024x352.png)](。/media/bpt10.png) 

**关闭布局**滑块。 **在预算计划文档，** **查看和编辑将在 Excel 的单据单击**工作表。 注意调整的 Excel 模板用于创建此预算计划工作表，还计算更新列使用上面步骤定义的配方。 

[] (![bpt11。/media/bpt111-1024x431.png)](。/media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>用于创建计划打翻和欺骗预算模板
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>我和添加可用于附加数据源到预算计划模板？

是，您可以使用** Design **添加菜单的到同一记分卡或其他实体在 Excel 模板的其他表。 例如，您可以添加 BudgetPlanProposedProject ** **数据源同时创建和维护一建议的项目列表，在进行在 Excel 中的数据。使用预算计划。 注意，包括容积大数据源可能会影响性能的 Excel 工作簿。 

在可以使用这个** **筛选器选项**数据连接器**预期添加到筛选器附加数据源。

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>我可以隐藏在数据 Connector Design 选项的其他用户的？

"是"，请打开**数据连接器**隐藏选项从其他用户的** Design **选项。

[] (![bpt13。/media/bpt13-1024x565.png)](。/media/bpt13.png)

**扩展数据连接选项**符和兑现**启用设计**复选框。 这将隐藏从的** Design **选项** Connector **数据。

[] (![bpt14。/media/bpt14-1024x592.png)](。/media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>我可以防止用户意外数据关闭 Connector，在进行数据时？

我们建议尽可能锁定模板会阻止用户关闭它。 若要启动锁，请单击**数据 Connector **，在右上角的箭头将显示。 

[] (![bpt15。/media/bpt15-1024x285.png)](。/media/bpt15.png) 

单击其他的菜单中的箭头。 **锁定**选择。

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[] (![bpt16。/media/bpt16-1024x614.png)](。/media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>我可以使用任何其他功能，例如 Excel 单元格格式、颜色、条件格式和图表。我的预算计划模板？

大多数是标准 Excel 功能在预算计划模板将工作。 我们建议使用用户的颜色编码可以区分为只读和可编辑的各列之间。 条件格式可用于查看突出预算的有问题的区域。 使用创建表中，列的 Excel 的标准配方可以轻松地存在。

您还可以为附加分组 (创建和使用预算数据中的数据透视表和图表和可视化项。 **在数据** **在"连接**组中，请单击选项卡上，请刷新所有** **，然后单击**属性**连接。 **使用**单击选项卡。 **在刷新**，请选择**数据，请刷新当打开文件**选中此复选框。 

[] (![bpt17。/media/bpt17-1024x614.png)](。/media/bpt17.png)


