---
title: "预算计划"
description: "此实验室的目的是提供预算计划领域中 Microsoft Dynamics 365 for Operations 功能更新的指导性视图。 此实验室的目的是说明预算计划模块的快速配置示例，并显示如何使用此配置完成预算计划。  此实验室专门介绍以下业务流程或任务：- 为预算计划创建组织层次结构和配置用户安全 - 定义预算计划方案、预算计划列、布局和 Excel 模板 - 创建和启用预算计划流程 - 通过从总帐拉出实际值创建预算计划文档 - 使用分配调整预算计划文档数据 - 在 Excel 中编辑预算计划文档数据"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: dbe2b386de9e88af354015705e1444987a3f7e82
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="budget-planning"></a>预算计划

[!include[banner](../includes/banner.md)]


此实验室的目的是提供预算计划领域中 Microsoft Dynamics 365 for Operations 功能更新的指导性视图。 此实验室的目的是说明预算计划模块的快速配置示例，并显示如何使用此配置完成预算计划。  此实验室专门介绍以下业务流程或任务：- 为预算计划创建组织层次结构和配置用户安全 - 定义预算计划方案、预算计划列、布局和 Excel 模板 - 创建和启用预算计划流程 - 通过从总帐拉出实际值创建预算计划文档 - 使用分配调整预算计划文档数据 - 在 Excel 中编辑预算计划文档数据 

<a name="prerequisites"></a>先决条件 
------------------

对于本教程，您需要访问含 Contoso 演示数据的 Dynamics 365 for Operations 环境，并需要在该实例上被配置为管理员。 请勿为此实验室使用“专用”浏览器模式 - 如果需要，从浏览器中的任何其他帐户退出并使用 Dynamics 365 for Operations 管理员凭据登录。 在登录到 Dynamics 365 for Operations 时，**必须**选中“我保持登录状态”复选框。 这将创建 Excel 应用程序当前需要的永久 Cookie。 如果您使用 IE 之外的浏览器登录到 Dynamics 365 for Operations，那么系统将提示您在 Excel 应用程序内登录。 在您单击 Excel 应用程序中的“登录”时，IE 弹出窗口将打开，在您登录时您**必须**选中“我保持登录状态”复选框。 如果单击 Excel 应用程序中的“登录”似乎未发生什么，那么您应该清除 IE Cookie 缓存。

## <a name="scenario-overview"></a>**方案概览**
Julia 担任德国 Contoso Entertainment Systems (DEMF) 的财务经理。 由于 FY2016 即将来临，她需要为下一个年度设定公司的预算。 预算编制看似如下：

1.  Julia 使用前一年的实际金额作为起点创建预算。
2.  基于前一年的实际情况，她创建下一个年度 12 个月的估计
3.  Julia 与首席财务官一起审核预算。 一旦完成，她将对预算进行必要的调整，然后完成预算编制。

方案的预算计划配置架构如下：

![预算计划配置架构](./media/screenshot1-300x152.png)

Julia 使用以下 Excel 模板编制预算：

[![Excel 模板](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>练习 1：配置
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**任务 1：创建组织的层次结构**
由于所有预算流程在财务部门进行，因此 Julia 需要创建非常简单的组织层次结构 – 仅包括财务部门。 1.1. 导航到组织层次结构（“组织管理”&gt;>“组织”&gt;“组织层次结构”），然后单击新的按钮

![组织层次结构](./media/screenshot3.png) 

1.2. 键入组织层次结构的名称，然后单击按钮“分配用途”

[![名称](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. 选择预算计划用途，单击按钮“添加并分配新创建的组织层次结构”： 

[![分配用途](./media/screenshot5.png)](./media/screenshot5.png)

1.4. 对安全组织用途重复上述步骤。 完成后关闭窗体。

[![安全组织](./media/screenshot6.png)](./media/screenshot6.png)

1.5. 在“组织层次结构”窗体中单击按钮“查看”。 单击层次结构设计器中的“编辑”，并通过单击按钮“插入”创建层次结构。

[![插入](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. 为预算编制层次结构选择财务部门。 

[![财务](./media/screenshot8.png)](./media/screenshot8.png)

1.7. 在完成后，单击按钮“发布”和“关闭”。 选择 1/1/2015 用作层次结构发布的生效日期。

[![有效日期](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>任务 2：配置用户安全性
预算计划使用特殊安全策略配置对预算计划数据的访问。 Julia 需要授予她自己对财务预算计划的访问权限。 

2.1. 切换到 DEMF 法人环境： 

[![DEMF](./media/screenshot10.png)](./media/screenshot10.png) 

2.2。 导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。 在“参数”选项卡上，设置“安全模型值”为“基于安全组织” 

[![参数](./media/screenshot11.png)](./media/screenshot11.png) 

2.3。 导致至“系统管理”&gt;“用户”&gt;“用户”。 给予用户 Admin (Julia Funderburk) 预算经理角色。 

[![预算管理器](./media/screenshot12.png)](./media/screenshot12.png) 

2.4。 领料用户角色单击“分配组织”屏幕截图 

[![分配组织](./media/screenshot13.png)](./media/screenshot13.png)

2.5。 选择“授予访问特定组织的权限”。 在第一步中选择创建的组织层次结构。 选择财务节点然后单击“授予组织及其子组织的访问权限”按钮 

***重要信息！*** *确保在执行此任务时您位于 DEMF 法人环境中，因为组织安全按法人应用* 

[![授予访问权](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>任务 3：创建方案
3.1. 导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。 在“方案”页，请注意我们在此实验室将进一步使用的方案：上一年实际和预算。 

*注意：如果您需要，可以为此练习创建新的方案并使用这些方案。* 

[![新方案](./media/screenshot15.png)](./media/screenshot15.png) 

*注意：因为 Julia 未为预算编制使用正式审核流程，我们在此实验室将跳过工作流、阶段和工作流阶段设置，并且将使用现有的自动 – 审核工作流设置。请参阅此工作流配置的附录。*

## <a name="task-4-create-budget-plan-columns"></a>任务4：创建预算计划列
预算计划列可以是基于货币或基于数量的列，可用于预算计划文档格式。 在我们的示例中，我们需要创建上一年实际列以及在一个预算年度中表示每个月的 12 个列。 列可以通过单击“添加”按钮并填充值来创建，也可以使用数据实体协助。 在此实验室，我们将使用数据实体填充值。 

4.1. 在“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算计划配置”中打开“列”页。 单击窗体右上角的 Office 按钮并且选择“列”（未筛选） 

[![未筛选列](./media/screenshot16.png)](./media/screenshot16.png) 

4.2。 系统将打开用于填充值的 Excel 工作簿。 如果系统提示，单击“启用编辑”和“信任此应用程序” 

[![启用编辑](./media/screenshot18.png)](./media/screenshot18.png) 

[![信任此应用程序](./media/screenshot17.png)](./media/screenshot17.png)

4.3。 我们需要更多列来容纳这些值。 在右侧窗格中单击“设计”添加列到网格： 

[![设计](./media/screenshot19.png)](./media/screenshot19.png) 

4.4。 单击 PlanColumns 旁边的小铅笔按钮查看可添加到网格的列 

[![编辑](./media/screenshot20.png)](./media/screenshot20.png) 

4.5。 双击每个可用字段并将其添加到所选字段并单击“更新” 

![更新](./media/screenshot21.png)](./media/screenshot21.png) 

4.6。 在 Excel 表中添加需要创建的所有列。 在 Excel 中使用 AutoFill 功能快速添加行。 确保行添加为表的一部分（在使用垂直滚动时，您应能够看到网格顶部的列标题） 

[![Autofill](./media/screenshot22.png)](./media/screenshot22.png) 

4.7。 返回 Dynamics 365 for Operations 并刷新页面。 将在 Dynamics 365 for Operations 中显示发布的值。 

[![刷新](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>任务 5：创建预算计划文档格式和模板
格式定义当用户打开预算计划文档时，预算计划文档行网格将呈现的外观。 它还可以切换预算计划文档的格式，可以在不同的角度查看相同数据。 现在，因为她将列定义为用于我们的预算计划文档，Julia 需要创建预算计划文档格式，其将看起来类似于她用于创建预算数据的 Excel 表（参见此实验室的“方案概览”部分） 

5.1。 在“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算计划配置”中打开“格式”页。 创建月度预算条目的新格式：

-   选择 MA+BU 维度集将主科目和业务单位包括在格式中。
-   列出在“元素”部分的上一步中创建的所有预算计划列。 允许除上一年度以外的所有实际可以编辑。
-   单击“描述”按钮选择哪些财务维度应在网格中显示描述。

[![描述](./media/screenshot24.png)](./media/screenshot24.png) 

基于预算计划格式定义，我们可以创建一个用作编辑预算数据备选方法的 Excel 模板。 因为 Excel 模板必须与预算计划格式定义匹配，您在生成 Excel 模板后将无法编辑预算计划格式，因此应在所有格式组件定义后执行此任务。 

5.2. 对于步骤 5.1. 中创建的布局， 单击按钮“模板”&gt;“生成”。 确认警告消息。 若要查看模板，单击“模板”&gt;“查看”。 

*注意：确保选择“另存为”并且选择应存储以便编辑该模板的位置。如果用户在对话框中选择打开“打开”而不保存，已完成的文档更改在文件关闭时不会保留。* 
[![模板视图](./media/screenshot25.png)](./media/screenshot25.png) 

5.3。 &lt;可选步骤&gt; 修改 Excel 模板使它看似对用户更易用 – 添加汇总公式、标题字段、格式等。保存更改并上载该文件到预算计划格式，方法是通过单击“布局”&gt;“上载”[ ![上载](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>任务 6：创建预算计划流程
Julia 需要创建和激活合并上述所有设置的新预算计划流程以开始输入预算计划。 预算计划流程定义哪些预算组织、工作流、格式和模板用于创建预算计划。 

6.1. 导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算计划流程”并创建新记录。

-   预算计划流程 – DEMF 预算编制 FY2016
-   预算周期 – FY2016
-   分类帐 – DEMF
-   默认科目结构 – 制造损益
-   组织层次结构 – 选择在实验室开始时创建的层次结构
-   预算计划工作流 – 为财务部门分配自动 – 审核工作流
-   在预算计划阶段规则和模板中，为每个工作流预算计划阶段选择是否允许“添加行”和“修改行”，以及哪些格式应在默认情况下使用

*注意：您可以创建其他文档格式，并且通过单击“备选格式”按钮指定它们可用于预算计划工作流阶段。* 

[![备用布局](./media/screenshot27.png)](./media/screenshot27.png) 

6.2。 选择“操作”&gt;“激活”激活此预算计划工作流 

[![启用](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>练习 2：流程模似
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>任务 7：从总帐生成预算计划的初始数据
7.1. 导航到“预算编制”&gt;“定期”&gt;“从总帐生成预算计划”。 填写定期流程参数，然后单击“生成”按钮。 

[![生成](./media/screenshot29.png)](./media/screenshot29.png) 

7.2。 导航到“预算编制”&gt;“预算计划”查找“生成”流程创建的预算计划。 

[![预算计划](./media/screenshot30.png)](./media/screenshot30.png) 

7.3。 通过单击文档编号超链接打开文档详细信息。 预算计划将显示为在此实验室期间创建的格式中定义的格式 

[![预算计划显示](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>任务 8：基于上一年度实际创建当前年度预算
分配方法可用于在预算计划中轻松地将预算计划的信息从一个方案复制到另一个/在各个期间内分布它们/分配到维度。 我们将使用分配来从上一年度实际创建当前年度预算。 

8.1. 在预算计划文档网格中选择所有行，然后单击按钮分配预算 

[![所有行](./media/screenshot32.png)](./media/screenshot32.png) 

8.2。 选择分配方法、期间参数、源和目标方案并单击“分配” 

[![分配](./media/screenshot33.png)](./media/screenshot33.png)

将把上一年的实际金额复制到当年年度预算，并使用销售曲线期间参数在期间内分配它们。 

[![销售曲线](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>任务 9：使用 Excel 调整预算计划文档并完成文档
9.1. 单击按钮“工作表”在 Excel 中打开文档内容

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. 在 Excel 工作簿打开时，调整预算计划文档中的数字，然后单击“发布”按钮。

[![发布](./media/screenshot36.png)](./media/screenshot36.png)

9.3. 返回到 Dynamics 365 for Operations 中的预算计划文档。 单击“工作流”&gt;“提交”自动审核文档

[![自动审核](./media/screenshot37.png)](./media/screenshot37.png) 

一旦完成工作流，预算计划文档阶段更改为“已审核”。 [![已审核](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>附录
========

### <a name="auto-approve-workflow-configuration"></a>自动审核工作流配置

A. “预算编制”&gt;“设置”&gt;“预算计划”&gt;“预算”工作流 使用模板预算计划工作流创建新工作流：

[![创建新工作流](./media/screenshot39.png)](./media/screenshot39.png)

此工作流只包含一任务 – 阶段转换预算计划 

[![阶段转换预算计划](./media/screenshot40.png)](./media/screenshot40.png) 

保存并激活工作流。 

B. 导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。 在“阶段”选项卡上创建 2 个阶段 – 初始和已提交 

[![初始和已提交](./media/screenshot41.png)](./media/screenshot41.png)

C. 导航到“预算编制”&gt;“设置”&gt;“预算计划”&gt;>“预算计划配置”。 在“工作流阶段”选项卡中，将在步骤 A 中创建的工作流自动 – 审核与阶段“初始”和“已提交”关联 

[![预算和预算计划](./media/screenshot42.png)](./media/screenshot42.png)  




