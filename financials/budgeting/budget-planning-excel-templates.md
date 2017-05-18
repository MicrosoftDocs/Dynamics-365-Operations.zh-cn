---
title: "预算计划的 Excel 模板"
description: "此主题描述如何创建可用于预算计划的 Microsoft Excel 模板。"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2ae8255a84f36af624e915e85bc769a8ca37fa7e
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="budget-planning-templates-for-excel"></a>预算计划的 Excel 模板

[!include[banner](../includes/banner.md)]


此主题描述如何创建可用于预算计划的 Microsoft Excel 模板。

此主题显示如何使用标准演示数据集和 Admin 用户登录创建可用于预算计划的 Excel 模板。 有关预算计划的详细信息，请参阅[预算计划概览](budget-planning-overview-configuration.md)。 也可以按照[预算计划 101](budget-plan.md) 教程了解基本模块配置和使用原则。

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>使用预算计划文档布局生成工作表
可使用一种或多种布局查看和编辑预算计划文档。 每种布局可以有一个关联预算计划文档模板，用于使用 Excel 工作表查看和编辑预算计划数据。 在此主题中，将使用现有布局配置生成预算计划文档模板。 打开**预算计划列表**（**预算编制**&gt; **预算计划**）。 单击**“新建”**创建新的预算计划文档。 [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

使用**添加**行选项添加行。 单击**布局**查看预算计划文档布局配置。 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

可以检查布局配置并根据需要调整。 转至**模板** &gt; **生成**，为该布局生成一个 Excel 文件。 生成模板之后，转至**模板** &gt; **查看**以打开并检查预算计划文档模板。 可将该 Excel 文件保存到本地驱动器。 [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> 为预算计划文档布局关联 Excel 模板之后，不能编辑该布局。 若要修改此布局，请删除关联的 Excel 模板文件并重新生成。 若要让布局中的字段和工作表中的字段保持同步，需执行此操作。 

该 Excel 模板中将包含预算计划文档模板中的所有元素，其中的**在工作表中可用**列设置为 True。 Excel 模板中不允许重叠元素。 例如，如果布局中包含 Request Q1、Request Q2、Request Q3 和 Request Q4 列，以及表示所有 4 个季度列总和的请求总计列，则只能在 Excel 模板中使用季度列或总计列。 更新期间，此 Excel 文件不能更新重叠列，因为表中的数据可能超出日期范围，因此不精确。

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> 若要避免使用 Excel 查看和编辑预算计划数据时可能出现问题，应使用相同用户登录 Dynamics 365 for Operations 和 Microsoft Dynamics Office 加载项数据连接器。

## <a name="add-a-header-to-budget-plan-document-template"></a>为预算计划文档模板添加标题
若要添加标题信息，请选择 Excel 文件中的首行，然后插入空行。 单击**数据连接器**中的**设计**向 Excel 文件添加标题字段。

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

在**设计**选项卡中，单击**添加**字段，然后选择 **BudgetPlanHeader** 作为实体数据源。

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

将光标指向 Excel 文件中的所需位置。 单击**添加标签**向所选位置添加字段标签。 选择**添加值**向所选位置添加值字段。 单击**确定**关闭该设计器。

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>向预算计划文档模板表添加计算列
--------------------------------------------------------------

接下来，将把计算列添加到生成的预算计划文档模板。 一个**请求总计**列，用于计算 Request Q1 到 Request Q4 列之和，以及一个**调整**列，用于按预定义的系数重新计算**请求总数**列。

单击**数据连接器**中的**设计**向表添加列。 单击 **BudgetPlanWorksheet** 数据源旁边的**编辑**开始添加列。

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

所选字段组将显示模板中的可用列。 单击**公式**添加新列。 为新列命名，然后将公式粘贴到**公式**字段中。 单击**更新**以插入该列。

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> 若要定义公式，请在电子表格中创建公式，然后将其复制到**设计**窗口中。 Dynamics 365 for Operations 绑定表通常命名为“AXTable1”。 例如，若要计算电子表格中的 Request Q1 到 Request Q4 列之和，则公式 = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\]。

重复此步骤以插入**调整**列。 为此列使用公式 = AxTable1\[Total request\]\*$I$1。 这将提取单元格 I1 中的值并乘以**请求总数**列中的值，以计算调整金额。

保存然后关闭该 Excel 文件。 返回 Dynamics 365 for Operations，然后在**布局**中，单击**模板 &gt; 上传**，上传要用于预算计划的所保存 Excel 模板。 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

关闭**布局**滑块。 在**预算计划**文档中，单击**工作表**，以便在 Excel 中查看和编辑文档。 请注意，此预算计划工作表是使用调整后的 Excel 模板创建的，并使用在前面的步骤中定义的公式更新计算列。 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>有关如何创建预算计划模板的提示和技巧
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>是否可以为预算计划模板添加和使用更多数据源？

可以，可以使用**设计**菜单向 Excel 模板中的同一个或其他工作表添加更多实体。 例如，可以添加 **BudgetPlanProposedProject** 数据源，以便在 Excel 中处理预算计划数据的同时，创建和维护一列建议的项目。 请注意，包含大量数据源可能影响 Excel 工作簿的性能。 

可使用**数据连接器**中的**筛选器**选项向更多数据源添加所需筛选器。

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>是否可以在数据连接器中对其他用户隐藏“设计”选项？

可以，请打开**数据连接器**选项，以便对其他用户隐藏**设计**选项。

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

展开**数据连接器选项**并清除**启用设计**复选框。 这将在**数据连接器**中隐藏**设计**选项。

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>是否可以阻止用户在处理数据时意外关闭数据连接器？

我们建议锁定模板，以防用户将其关闭。 若要开启锁定，请单击**数据连接器**；将在右上角显示一个箭头。 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

单击箭头以再显示一个菜单。 选择**锁定**。

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>是否可以在我的预算计划模板中使用其他 Excel 功能，如单元格格式、颜色、条件格式和图表？

可以，预算计划模板中支持大多数标准的 Excel 功能。 我们建议使用颜色编码，以便用户区分只读列和可编辑列。 可使用条件格式突出显示预算的问题区域。 可通过使用标准 Excel 公式在表上方轻松表示列总计。

还可以为预算数据的更多分组和可视化创建和使用透视表和图表。 在**数据**选项卡上的**连接**组中，单击**全部刷新**，然后单击**连接属性**。 单击**用法**选项卡。 在**刷新**下，选中**打开文件时刷新数据**复选框。 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)




