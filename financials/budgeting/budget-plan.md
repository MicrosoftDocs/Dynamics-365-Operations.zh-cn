---
title: "预算计划"
description: "实验室此目标为工序在预算更新规划范围的功能提供了一引导的查看 Microsoft Dynamics 365。 此实验室的目的是说明预算计划模块的快速配置示例，并显示如何使用此配置完成预算计划。  实验室此专门要关注- -创建预算计划配置用户和安全性的以下业务过程或任务组织层次结构-定义预算计划方案预算计划布局、列和 Excel 模板-创建和激活预算计划流程-创建预算计划文档通过在请求来自总帐的分配调整-实际使用预算计划文档数据-编辑预算计划文档在 Excel 的数据"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>预算计划

实验室此目标为工序在预算更新规划范围的功能提供了一引导的查看 Microsoft Dynamics 365。 此实验室的目的是说明预算计划模块的快速配置示例，并显示如何使用此配置完成预算计划。  实验室此专门要关注- -创建预算计划配置用户和安全性的以下业务过程或任务组织层次结构-定义预算计划方案预算计划布局、列和 Excel 模板-创建和激活预算计划流程-创建预算计划文档通过在请求来自总帐的分配调整-实际使用预算计划文档数据-编辑预算计划文档在 Excel 的数据 

<a name="prerequisites"></a>先决条件 
------------------

对于当前指南，则需要工序环境的访问 Dynamics 365 的 Contoso 演示数据和设置为实例中的管理员。 不使用在专用浏览器模式为此实验室-从在查看器的其他会计科目 (如果需要) 注销并登录。工序管理员凭据的 Dynamics 365。 在签名到工序时的 Dynamics 365，则必须** **请检查“保存我登录”复选框。 这将创建 Excel 应用程序当前需要的永久 Cookie。 并非 IE 之外，则登录到工序的 Dynamics 365 使用浏览器，则提示将在 Excel 应用中登录。 在您单击 Excel 应用程序中的“登录”时，IE 弹出窗口将打开，在您登录时您**必须**选中“我保持登录状态”复选框。 如果单击 Excel 应用程序中的“登录”似乎未发生什么，那么您应该清除 IE Cookie 缓存。

## <a name="scenario-overview"></a>**Scenario overview**
Julia 担任德国 Contoso Entertainment Systems (DEMF) 的财务经理。 由于 FY2016 即将来临，她需要为下一个年度设定公司的预算。 预算编制看似如下：

1.  Julia 使用前一年的实际金额作为起点创建预算。
2.  基于前一年的实际情况，她创建下一个年度 12 个月的估计
3.  Julia 与首席财务官一起审核预算。 一旦完成，她将对预算进行必要的调整，然后完成预算编制。

预算计划方案的配置架构查找的公式如下所示：

![屏幕截图 1](./media/screenshot1-300x152.png)

使用以下茱莉亚 Excel 模板编制预算：

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>练习 1：配置
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**任务：1**创建组织层次结构
由于所有预算流程在财务部门进行，因此 Julia 需要创建非常简单的组织层次结构 – 仅包括财务部门。 1.1. 导航到组织层次结构 (组织管理 &gt; 组织 &gt; 组织层次结构) 然后单击"新建按钮

![屏幕截图 3](./media/screenshot3.png) 

1.2. 键入名称。这个组织层次结构然后单击该按钮以分配目的

[] (![Screenshot4。/media/screen 射击 4.png)](。/media/screen 射击 4.png) 

1.3. 选择预算的计划目的、单击按钮添加和创建新分配的组织层次结构： 

[] (![Screenshot5。/media/screen 射击 5.png)](。/media/screen 射击 5.png)

1.4. 对安全组织用途重复上述步骤。 完成后关闭窗体。

[] (![Screenshot6。/media/screen 射击 6.png)](。/media/screen 射击 6.png)

1.5. 在“组织层次结构”窗体中单击按钮“查看”。 单击层次结构设计器中的“编辑”，并通过单击按钮“插入”创建层次结构。

[] (![Screenshot7。/media/screen 射击 7.png)](。/media/screen 射击 7.png) 

1.6. 为预算编制层次结构选择财务部门。 

[] (![Screenshot8。/media/screen 射击 8.png)](。/media/screen 射击 8.png)

1.7. 在完成后，单击按钮“发布”和“关闭”。 选择 1/1/2015 用作层次结构发布的生效日期。

[] (![Screenshot9。/media/screen 射击 9.png)](。/media/screen 射击 9.png)

## <a name="task-2-configure-user-security"></a>任务 2：配置用户安全性
预算计划使用特殊安全策略配置对预算计划数据的访问。 Julia 需要授予她自己对财务预算计划的访问权限。 2.1. 到 DEMF 法人环境的切换：[] (![Screenshot10。/media/screen 射击 10.png)](。/media/screen 射击 10.png /media/screen)。 导航到预算 &gt; 设置 &gt; 预算计划 &gt; 让预算计划配置。 在"参数选项卡上，安全设置基于组织的安全模型![[] (Screenshot11 值。/media/screen 射击 11.png)](。/media/screen 射击 11.png /media/screen)。 导航到系统 &gt; 管理用户。 给予用户 Admin (Julia Funderburk) 预算经理角色。 [] (![Screenshot12。/media/screen 射击 12.png)](。/media/screen 射击 12.png /media/screen)。 领取单击"分配用户角色和组织![[] (Screenshot13。/media/screen 射击 13.png)](。/media/screen 射击 13.png /media/screen)。 选择“授予访问特定组织的权限”。 在第一步中选择创建的组织层次结构。 领料财务和节点单击具有子重要按钮的***的授予！*** * –来确定您在 DEMF 法人上下文，在执行此任务为组织，安全。法定的 entity*时![[] (Screenshot14 应用。/media/screen 射击 14.png)](。/media/screen 射击 14.png)

## <a name="task-3-create-scenarios"></a>任务 3：创建方案
3.1. 导航到 BudgetingSetup&gt;&gt; 预算计划 &gt; 让预算计划配置。 在“方案”页，请注意我们在此实验室将进一步使用的方案：上一年实际和预算。 *注意：如果您需要，可以为此练习创建新的方案并使用这些方案。* [] (![Screenshot15。/media/screen 射击 15.png)](。/media/screen 射击 15.png) *Note:因为茱莉亚不能为预算编制使用官方核准流程，我们将跳过{{在此：in}}实验室工作流和阶段设置工作流、阶段，并且将自动使用现有设置–审核工作流。用于此工作流 configuration.*附录参阅

## <a name="task-4-create-budget-plan-columns"></a>任务4：创建预算计划列
预算计划列可以是基于货币或基于数量的列，可用于预算计划文档格式。 在我们的示例中，我们需要创建上一年实际列以及在一个预算年度中表示每个月的 12 个列。 列可以通过单击“添加”按钮并填充值来创建，也可以使用数据实体协助。 在此实验室，我们将使用数据实体填充值。 4.1. 在 BudgetingSetup&gt;&gt; 预算计划 &gt; 让预算计划配置开口管柱页。 单击窗体上领取和列的右上角中 Office "按钮 (未筛选视图![[] () Screenshot16。/media/screen 射击 16.png)](。/media/screen 射击 16.png /media/screen)。 系统将打开用于填充值的 Excel 工作簿。 如果系统提示，单击"启用编辑和信任此应用![[] (Screenshot18。/media/screen 射击 18.png)](。/media/screen 射击 18.png [] ()![Screenshot17。/media/screen 射击 17.png)](。/media/screen 射击 17.png /media/screen)。 我们将需要多列的值。 上单击正确的侧窗格中的网格设计将列添加到列：[] (![Screenshot19。/media/screen 射击 19.png)](。/media/screen 射击 19.png /media/screen)。 单击以看到"可用"列的 PlanColumns 旁边的一点铅笔按钮网格添加到![[] (Screenshot20。/media/screen 射击 20.png)](。/media/screen 射击 20.png /media/screen)。 在添加它们的每个字段可用的双击到选择的字段和 Screenshot21 单击"更新![[] (。/media/screen 射击 21.png)](。/media/screen 射击 21.png /media/screen)。 在 Excel 表中添加需要创建的所有列。 在 Excel 中使用 AutoFill 功能快速添加行。 确定添加行，表的一部分 (在垂直使用滚动时，应该就能看到在网格)![Screenshot22 的 [] (上面的列标题。/media/screen 射击 22.png)](。/media/screen 射击 22.png /media/screen)。 后退工序的 Dynamics 365 页并刷新。 已过帐值将显示在工序的 Dynamics 365。 [] (![Screenshot23。/media/screen 射击 23.png)](。/media/screen 射击 23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>任务 5：创建预算计划文档格式和模板
格式定义当用户打开预算计划文档时，预算计划文档行网格将呈现的外观。 它还可以切换预算计划文档的格式，可以在不同的角度查看相同数据。 现在，因为她将列定义为用于我们的预算计划文档，Julia 需要创建预算计划文档格式，其将看起来类似于她用于创建预算数据的 Excel 表（参见此实验室的“方案概览”部分）5.1. 在 BudgetingSetup&gt;&gt; 预算计划 &gt; 布局预算计划配置打开页面。 创建月度预算条目的新格式：

-   选择 MA+BU 维度集将主科目和业务单位包括在格式中。
-   列出在“元素”部分的上一步中创建的所有预算计划列。 允许除上一年度以外的所有实际可以编辑。
-   单击“描述”按钮选择哪些财务维度应在网格中显示描述。

[] (![Screenshot24。/media/screen 射击 24.png)](。/media/screen 基于射击了我们可以创建作为一个可用于选择的方法将使用 Excel 模板的编辑预算数据的预算计划布局定义) 的 24.png。 因为 Excel 模板必须与预算计划格式定义匹配，您在生成 Excel 模板后将无法编辑预算计划格式，因此应在所有格式组件定义后执行此任务。 5.2. 对于在 5.1 创建的布局。 步骤，单击按钮模板 &gt; 生成。 确认警告消息。 若要查看模板，请单击"视图模板 &gt;。 *Note:确保选择“保存”并且选择应存储它以编辑模板的位置。如果该用户选择“打开”对话框中，完成，不保存更改的文件。不会保留，在该文件是 closed.* [] (![Screenshot25。/media/screen 射击 25.png)](。/media/screen 射击 25.png /media/screen)。 &lt; 选项步骤&gt; Excel 模板进行修改它会查找对用户更加友好–将总，配方标题字段中，格式、保存更改的文件并且上载到预算计划布局通过单击![版式 &gt; 上载 [] (Screenshot26。/media/screen 射击 26.png)](。/media/screen 射击 26.png)

## <a name="task-6-create-a-budget-planning-process"></a>任务 6：创建预算计划流程
Julia 需要创建和激活合并上述所有设置的新预算计划流程以开始输入预算计划。 预算计划流程定义哪些预算组织、工作流、格式和模板用于创建预算计划。 6.1. 导航到预算 &gt; 设置 &gt; 预算计划 &gt; 和预算计划流程创建一个新记录。

-   预算计划流程 – DEMF 预算编制 FY2016
-   预算周期 – FY2016
-   分类帐 – DEMF
-   默认科目结构 – 制造损益
-   组织层次结构 – 选择在实验室开始时创建的层次结构
-   预算计划工作流 – 为财务部门分配自动 – 审核工作流
-   在预算计划阶段规则和模板中，为每个工作流预算计划阶段选择是否允许“添加行”和“修改行”，以及哪些格式应在默认情况下使用

*注意：您可以创建其他文档格式，并且通过单击“备选格式”按钮指定它们可用于预算计划工作流阶段。* [] (![Screenshot27。/media/screen 射击 27.png)](。/media/screen 射击 27.png /media/screen)。 选择激活的操作 &gt; 启用此预算计划工作流![[] (Screenshot28。/media/screen 射击 28.png)](。/media/screen 射击 28.png)

<a name="exercise-2-process-simulation"></a>练习 2：流程模似
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>任务 7：从总帐生成预算计划的初始数据
7.1. 导航到生成定期 &gt; 的预算 &gt; 来自总帐预算计划。 填写定期流程参数，然后单击“生成”按钮。 [] (![Screenshot29。/media/screen 射击 29.png)](。/media/screen 射击 29.png /media/screen)。 导航到预算的 &gt; 预算计划查找"流程创建的预算计划。 [] (![Screenshot30。/media/screen 射击 30.png)](。/media/screen 射击 30.png /media/screen)。 通过单击文档编号超链接打开文档详细信息。 预算计划将显示在" {{在此：during}}实验室创建定义的版式![[] (Screenshot31 期间。/media/screen 射击 31.png)](。/media/screen 射击 31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>任务 8：基于上一年度实际创建当前年度预算
分配方法可用于在预算计划中轻松地将预算计划的信息从一个方案复制到另一个/在各个期间内分布它们/分配到维度。 我们将使用分配来从上一年度实际创建当前年度预算。 8.1. 领取在预算计划文档网格的所有行，并单击按钮分配预算![[] (Screenshot32。/media/screen 射击 32.png)](。/media/screen 射击 32.png /media/screen)。 选择的期间参数分配方法、源帐户和目标、方案和单击"分配 

[] (![Screenshot33。/media/screen 射击 33.png)](。/media/screen 射击 33.png)

使用增值曲线期间参数，以前年度实际金额在期间上复制到当前年度预算并将它们分摊。 

[] (![Screenshot34。/media/screen 射击 34.png)](。/media/screen 射击 34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>任务 9：使用 Excel 调整预算计划文档并完成文档
9.1. 单击按钮工作表到 Excel 打开单据的内容

[] (![Screenshot35。/media/screen 射击 35.png)](。/media/screen 射击 35.png)

9.2. 在 Excel 工作簿打开时，调整预算计划文档中的数字，然后单击“发布”按钮。

[] (![Screenshot36。/media/screen 射击 36.png)](。/media/screen 射击 36.png)

9.3. 到预算计划文档的退货。工序的 Dynamics 365。 单击工作 &gt; 流提交自动审核文档

[] (![Screenshot37。/media/screen 射击 37.png)](。/media/screen 射击 37.png) 

一旦完成工作流，预算计划文档阶段更改到审核。 [] (![Screenshot38。/media/screen 射击 38.png)](。/media/screen 射击 38.png)

<a name="appendix"></a>附录
========

### <a name="auto-approve-workflow-configuration"></a>自动审核工作流配置

A. 使用 &gt; 模板 &gt; 预算计划 &gt; 工作流，预算的预算设置预算计划的工作流创建新工作流：

[] (![Screenshot39。/media/screen 射击 39.png)](。/media/screen 射击 39.png)

此工作流将只包含一任务–预算计划过渡阶段 

[] (![Screenshot40。/media/screen 射击 40.png)](。/media/screen 射击 40.png) 

保存然后激活工作流。 

B。 导航到预算 &gt; 设置 &gt; 预算计划 &gt; 让预算计划配置。 阶段在选项卡–最初创建和提交 2 的阶段 

[] (![Screenshot41。/media/screen 射击 41.png)](。/media/screen 射击 41.png)

C。 导航到预算 &gt; 设置 &gt; 预算计划 &gt; 让预算计划配置。 在工作流阶段选项卡关联工作流–自动审核在与阶段姓名首字母缩写 A 创建和提交的步骤 

[] (![Screenshot42。/media/screen 射击 42.png)](。/media/screen 射击 42.png)  


