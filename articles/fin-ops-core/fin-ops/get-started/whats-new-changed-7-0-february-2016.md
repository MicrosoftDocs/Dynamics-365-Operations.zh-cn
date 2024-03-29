---
title: Dynamics AX 7.0（2016 年 2 月）中的新增功能和更改内容
description: 本文介绍了 Microsoft Dynamics AX 7.0 中的新功能和更改的功能。 此版本包含平台和应用程序功能，于 2016 年 2 月发布。
author: sericks007
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 4cd59d5ea2ef8d280a927fd9e9fe3b9af7974d7c
ms.sourcegitcommit: 0a5885dc792fc608ae59d0ef9b36fb61790b24de
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2022
ms.locfileid: "9593979"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Dynamics AX 7.0（2016 年 2 月）中的新增功能和更改内容

[!include [banner](../includes/banner.md)]

本文介绍了 Microsoft Dynamics AX 7.0 中的新功能和更改的功能。 此版本包含平台和应用程序功能，于 2016 年 2 月发布。

## <a name="cost-management"></a>成本管理

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>可快速概览库存余额、在制品 (WIP) 库存余额，以及针对所选会计年度的库存流入量和流出量。</td>
<td>不适用</td>
<td><strong>成本管理</strong>工作区包含一个部分，在其中提供了所选会计期间的库存报表和 WIP 库存报表。 此报表基于数据集缓存，该缓存在默认情况下每 24 小时更新一次。 可以配置数据集缓存，以使用户可以手动更新它以实时报告。 <strong>成本管理</strong>工作区中的<strong>数据刷新状态卡</strong>在最后一次更新缓存时显示。</td>
<td>成本总监有兴趣知道库存或 WIP 库存报表余额是随着时间的推移增加还是减少。 通过对报表中的操作事件进行分类，成本总监可以概览库存如何流动。 如果库存或 WIP 库存是按标准成本评估的，则还可以查看登记的整体差异。</td>
</tr>
<tr>
<td>使用<strong>成本管理</strong>模块。</td>
<td>不适用</td>
<td>成本管理是作为域区域引入的。 成本相关的配置和见解分散在整个库存管理、生产控制和应付帐款中。</td>
<td>由于与成本管理关联的所有任务集中在一个模块中，因此更容易让成本总监维护系统。</td>
</tr>
<tr>
<td>与库存会计和生产会计相关的过帐类型已更新。</td>
<td><strong>InventPosting</strong>、<strong>资源</strong>、<strong>ResourceGroup</strong> 和 <strong>ProductionGroup</strong> 窗体中的标签始终不与实际使用的 <strong>LedgerPostingType</strong> 标签一致。 了解标签中使用的术语并不容易。</td>
<td>这些标签已经更新，因此<strong>InventPosting</strong>、<strong>资源</strong>、<strong>ResourceGroup</strong>和<strong>ProductionGroup</strong>页上的标签始终与实际<strong>LedgerPostingType</strong>标签匹配。 还需重命名所有标签，以便标签与操作事件匹配。 请注意，未更改实际过帐逻辑。</td>
<td>配置系统更加简单，因为新的标签与使用此过帐类型的操作事件有关。</td>
</tr>
<tr>
<td>在 Microsoft Excel 或成本计算版本中导出/导入采购价、成本或销售价。</td>
<td>您无法将价格或成本正确导入到成本计算版本，因为数据模型需要 InventDim ID。</td>
<td>引入数据实体后可以执行导入或导出功能。 此功能允许用户将价格或成本导入/导出到成本计算版本中。
<ul>
<li>导入从采购部门获得的下一年采购价的完整列表。</li>
<li>通过一个操作将成本和标准销售价从总部推送到一个或多个销售公司。</li>
</ul></td>
<td>它可以在成本总监维护系统时为其节省大量时间，尤其是当他们必须为下一会计年度维护预先确定的成本时。</td>
</tr>
<tr>
<td>可快速概览成本对象的库存余额和平均单位成本。</td>
<td>用户必须打开现有量窗体并选择反映成本对象的库存维度。 因此，用户必须知道为特定产品的财务库存标记了哪些库存维度。</td>
<td>引入了新的<strong>成本对象</strong>页。 默认情况下，此页显示与产品相关的所有成本对象。 此页显示每个成本对象的当前库存数量、值和平均单位成本。</td>
<td>它消除一些复杂性，使得更容易当一名成本总监。</td>
</tr>
<tr>
<td>在库存控制期间使用新<strong>成本条目</strong>页。</td>
<td>对登记的库存交易记录和相关的结算进行库存控制会很复杂，因为相同的交易记录可以是实际的或财务的。</td>
<td><strong>成本条目</strong>页提供一个新的方式来查看库存交易记录。
<ul>
<li>交易记录按时间顺序显示。</li>
<li>仅包括对成本有贡献的交易记录。</li>
<li>没有实际成本或财务成本的概念。</li>
<li>没有实际数量或财务数量的概念。</li>
<li>成本增量添加。</li>
</ul></td>
<td>当成本总监必须在交易记录级别执行库存控制时，它可以使他们节省大量时间。</td>
</tr>
<tr>
<td>使用新的<strong>生产 WIP 报表</strong>对话框可以查看特定产品的累计成本的汇总视图。</td>
<td>不适用</td>
<td>WIP 报表显示特定生产订单的 WIP 余额汇总，它们已按组分类到相应的成本。 图表按时间顺序显示操作过帐如何影响 WIP 余额。</td>
<td>当成本总监需要了解特定生产订单的当前 WIP 余额，或该订单已消耗的物料数量时，上述报表可以为他们节省大量时间。</td>
</tr>
<tr>
<td>使用在生产订单上引入的“查看成本比较”功能。 此功能便于比较与生产订单相关的成本。</td>
<td>用户可以仅比较估计成本和实际成本。 此操作可以在最低级别下完成。</td>
<td>成本比较功能允许成本总监比较以下数据：
<ul>
<li>有效成本和估计成本 = 计划差异</li>
<li>估计成本和实际成本 = 生产差异</li>
<li>计划差异 + 生产差异 = 合计差异</li>
</ul>
此功能单独运行，与分配给已生产物料的成本计算方法无关。 默认情况下，图表按成本组类型显示成本比较。 该图表允许用户深入到更详细的级别。</td>
<td>成本总监或生产经理可通过图表分析生产差异的来源，以及导致差异的原因。</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>开发人员

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 在云中创建可从许多设备访问的基于 Web 的解决方案。 | 不可用 | Dynamics AX 的当前版本是以新的基于 Web 的客户端和客户端框架为基础的。 | 您可以为您的最终用户提供代下一解决方案。 |
| 使用 Microsoft Visual Studio 开发解决方法。 | Microsoft MorphX 是主要开发环境，但某些开发在 Visual Studio 中进行。 | Visual Studio 是纯开发环境。 | 它保留熟悉的 Dynamics AX 2012 概念，使它们无缝满足 Visual Studio 框架和范例。 它启用与其他 .NET 语言和项目的标准互操作性。 |
| 为所有功能编译公共中间语言 (CIL)。 | X++ 编译成 p 代码。 | 全新的 X++ 编译器为所有功能生成 CIL。 CIL 与其他基于 .NET 的语言所使用的中间语言相同。 | CIL 更快，可以高效地引用托管动态链接库 (DLL) 中的类，并且可以在 .NET 实用程序的大型工具库上运行。 |
| 在 Microsoft Dynamics AX 客户端嵌入商业智能 (BI) 报表和可视化。 | 不可用 | 创建高度直观且可变的可视化。 | 它提供基于 BI 的决策见解。 |
| 与 Microsoft Office 集成。 | 不可用 | 新增功能包括 Excel Data Connector 应用程序、**工作簿设计器** 页、“导出 API”和文档管理。 | 您可以为您的最终用户创建工作效率解决方案。 |
| 自动化生成、测试和部署。 | 部分可用 | 通过使用 Developer 和 Build VM 部署开发人员拓扑结构。 自动配置“构建虚拟机”以从 Visual Studio Online (VSO) 发现、构建模块并运行测试。 支持 C\# 和 X++ 模块编译和引用。 | 它通过减少测试和验证的成本和工作，提高开发人员的工作效率。 |
| 通过覆盖和扩展进行自定义。 | 扩展不可用。 | Dynamics AX 的当前版本具有一个新的自定义模型。 | 您可以自定义由 Microsoft 或第三方 Microsoft 合作伙伴交付的模型元素的源代码和元数据。 |
| 通过使用 X++ 和一个现代 Web 框架，生成新控件和 UI 元素。 | 自定义控件依赖于外部框架，例如 Microsoft ActiveX 和 Windows Presentation Foundation (WPF)。 | 在当前版本中生成控件更容易。 X++ 框架可用于应用程序行为和业务逻辑，基于 HTML/JavaScript 的客户端允许现代化的可视化。 | 您的控件可以设计为外观和行为类似于 Dynamics AX 现成 (OOB) 控件。 |
| 通过使用新工具，评估和优化性能。 | PerfSDK、数据扩展工具包、跟踪分析器 Web 应用程序和 PerfTimer 不可用。 | PerfSDK、数据扩展工具包、跟踪分析器 Web 应用程序和 PerfTimer 是新的。 | 软件开发配套件 (SDK) 能让您在单用户以及多用户（如果适用）中测试和验证所有关键业务流程的性能。 数据扩展工具包能让您正确展开必须让主数据和交易记录数据正确展开的所有性能测试。 跟踪分析器能让您验证单用户性能测试或多用户运行。 PerfTimer 能让您查看任何查询或任何特定方法调用是否导致性能问题。 因此，您无需执行跟踪和详细分析所有内容。 |
| 通过使用 OData 公开可更新的视图。 | 不可用 | Dynamics AX 的当前版本引入公共 OData 服务终结点，它允许在多种类型的客户端上以一致的方式访问 Dynamics AX 数据。 | 通过使用 HTTP 堆栈协议，您的解决方案可以与 RESTful 服务交互，以可发现方式共享数据，并可启用广泛的集成。 |
| 利用 Business Connector 编写业务逻辑和支持集成方案。 | 可使用 Business Connector 从受管代码调用 X++ 代码。 我们建议您仅将 Business Connector 用于编写 C\# 的业务逻辑，不用于集成方案。 | 不再支持 Business Connector。 只有 X++ 已编译成托管代码才会提供编写要求。 因此，互操作更容易。 通过使用 OData，满足集成方案。 | 今后您不能使用 Business Connector。 |
| 在实际数据库字段和扩展数据类型 (EDT) 上选择标度（即小数位数）。 | 标度 16 是默认标度，不能被开发人员更改。 | EDT 和字段现在由一个标度属性，可应用于单个字段和 EDT。 默认值设置为 6，而不是 16。 | 在使用较小标度时，NCCI 表（SQL 中的内存中支持）的性能提高好几个数量级。 根据各个字段的使用需求，更改标度。 |

## <a name="financial-management"></a>财务管理

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>将科目结构导出到 Microsoft Excel。</td>
<td>不可用</td>
<td>您现在可选择科目结构并将它导出到 Excel。</td>
<td>许多客户请求能够将科目结构导出到 Excel 以便更容易筛选。</td>
</tr>
<tr>
<td>查看与单个页面上的科目结构关联的分类帐和高级规则结构。</td>
<td> 用户必须导航到多个窗体以查看使用的分类帐和科目结构。</td>
<td>FactBox 已添加到科目结构页。</td>
<td>当定义并编辑科目结构时，对重要信息的访问更容易。</td>
</tr>
<tr>
<td>查看与单个页面的会计科目表关联的分类帐。</td>
<td>用户必须导航到每个公司并打开分类帐窗体以查看分配给分类帐的会计科目表。</td>
<td>FactBox 已添加到<strong>会计科目表</strong>页。</td>
<td> 当定义并分配会计科目表时，对重要信息的访问更容易。</td>
</tr>
<tr>
<td>查看<strong>试算平衡表</strong>列表页上的单独列中的结算单调整和期末交易记录。</td>
<td>用户在单个列中查看这两种类型的交易记录。</td>
<td>一个附加参数已添加到<strong>试算平衡表</strong>列表页。</td>
<td>它允许对数据进行更简明的分析，也是某些国家/地区的管制报表所必需的。</td>
</tr>
<tr>
<td>使用新<strong>全球普通日记帐</strong>页。</td>
<td>不可用</td>
<td>新<strong>全球普通日记帐</strong>页可以输入普通日记帐。 此页面的权限添加到<strong>会计师</strong>角色。</td>
<td>使共享服务会计师无需退出该窗体或者切换公司上下文即可跨公司输入普通日记帐。</td>
</tr> 
<tr>
<td>使用新<strong>会计源管理器</strong>页。</td>
<td>通过 Dynamics AX 2012 R3 CU10 提供。</td>
<td>新<strong>会计源资源管理器</strong>页面和操作可以从<strong>试算平衡表</strong>列表页和<strong>凭证交易记录</strong>页导入到那里。</td>
<td>可查看总帐中的试算平衡表或会计条目或特别分析的最详细的源信息。</td>
</tr>
<tr>
<td>添加其他过帐层。</td>
<td>添加其他过帐层属于开发人员体验。</td>
<td>目前有十个过帐层。</td>
<td>大多数客户将添加其他过帐层。</td>
</tr>
<tr>
<td>使用相关凭证选项。</td>
<td>不可用</td>
<td>相关凭证选项仅供用户在过帐公司内部交易记录时查看对方公司的凭证。 从相关凭证中，用户可以单击详细信息并快速跳转到对方公司凭证。</td>
<td>在过帐公司内部交易记录时，用户无法看到或跟踪在对方公司过帐的凭证。</td>
</tr>
<tr>
<td>财务期间批量关闭</td>
<td>不可用</td>
<td>用户可以更新模块访问，并可以一次更改多个公司的期间状态。</td>
<td>在使用该功能之前，用户必须更改登录哪些公司，导航到分类帐日历窗体并手动更新模块访问和期间状态。</td>
</tr>
<tr>
<td>有 Oanda 支持的汇率。</td>
<td>配置要从 Oanda 导入的汇率提供商属于开发人员体验。</td>
<td>如果用户有一个 Oanda 密钥，他们可以在配置汇率提供商时输入它。</td>
<td>用户可以通过获得 Oanda 支持的定期导入的汇率来利用现成功能。</td>
</tr>
<tr>
<td>基于维度、属性、日期以及方案筛选财务报表 (Management Reporter)。</td>
<td> Management Reporter 报表的所有筛选都是通过报表的设计处理的。 例如，如果具有查看权限的用户想要查看不同日期的报表，则报表设计器必须进行修改。</td>
<td>已经添加了报表选项，因此，用户在查看报表时，可以应用不同的筛选器。 然后基于这些筛选器生成新报表。</td>
<td>财务报表的客户可以针对维度、日期、属性和方案应用不同的筛选器，而不要求更新报表设计。</td>
</tr>
<tr>
<td>在 Microsoft Dynamics AX 客户端中查看财务报表 (Management Reporter)。</td>
<td>单独的 Web 客户端用于查看 Management Reporter 报表。</td>
<td>所有财务报表均可以在 Dynamics AX 客户端访问到。 用户选择要查看的报表，报表将在客户端中显示。</td>
<td>您现在可以查看财务报表，而不必访问不同的客户端/应用程序。</td>
</tr>
<tr>
<td>从 Microsoft Dynamics AX 客户端打印财务报表 (Management Reporter)。</td>
<td>打印报表将使用浏览器的打印选项进行打印，但只打印用户可以在屏幕上看到的内容。</td>
<td>通过使用 Dynamics AX 客户端财务报表中的打印选项，用户可以选择报表的详细级别和页面设置。</td>
<td>打印的报表按用户期望而不是打印网页的方式打印。</td>
</tr><tr>
<td>通过使用“监控财务业绩”Power BI 内容分析财务数据。</td>
<td>不可用</td>
<td>在 PowerBI.com 上，选择<strong>获取数据</strong>，然后选择 <strong>Dynamics AX – 财务绩效</strong>内容包。 输入您的 Dynamics AX 终结点的 URL 以查看反映在仪表板中的数据。</td>
<td>通过三到四次单击，组织可以部署一个包含重要财务数据的 Power BI 仪表板。 内容可由组织个性化。</td>
</tr>
<tr>
<td>跟踪财务期间结帐流程。</td>
<td>不可用</td>
<td>通过使用财务期间结帐配置，可以创建结帐模板和计划。 使用<strong>财务期间结帐</strong>工作区可跨多个公司跟踪结帐计划的进度。</td>
<td>此工作区消除用于定义、计划和沟通结帐活动的手动系统。 因此，结帐天数会减少。</td>
</tr>
<tr>
<td>使用<strong>分类帐预算和预测</strong>工作区和附加的查询窗体，监控预算值与实际值，创建分类帐预测。</td>
<td>不可用</td>
<td> 该工作区可以通过 Dynamics AX 仪表板访问。 包含指向若干新查询页的链接：<strong>实际和预算汇总</strong>、<strong>预算控制统计汇总</strong>、<strong>预算登记簿条目</strong>和<strong>预算计划</strong>。</td>
<td>新的查询页便于您输入预算信息。 该工作区将所有预算维护和监控任务组合到一个地方，便于预算经理或会计经理使用。</td>
</tr>
<tr>
<td>为预算计划和预测创建布局。</td>
<td><strong>预算计划</strong>文档显示为一个行列表，其中各行具有财务维度组合的生效日期和金额。 用户必须创建和使用 Excel 模板查看数据透视表中的预算计划数据。</td>
<td>无限数量的布局可用于预算计划和预测。 您可以将所选的财务维度、用户定义的列和其他行属性（例如注释、项目和资产）组合到布局中。 用户可以通过使用任何所选的格式，在运行中切换预算计划文档的布局和编辑数据。 通过清除方案约束和使用布局定义在预算计划文档的每个阶段可以查看和编辑哪些数据，可简化预算计划的配置。</td>
<td>它能让您通过使用 Excel 和 Dynamics AX 客户端，灵活地创建和编辑预算计划。 通过使用预算计划布局设置可以生成 Excel 工作簿模板。</td>
</tr>
<tr>
<td>通过使用<strong>未结明细表</strong>报表（其中包括逾期天数）中的信息，打印<strong>供应商发票交易记录</strong>报表。</td>
<td>您必须首先打印两个不同报表：<strong>未结明细表</strong>和<strong>供应商发票交易记录</strong>。</td>
<td>有关这两个报表的信息已合并到<strong>供应商发票交易记录</strong>报表中。 <strong>未结明细表</strong>报表已弃用。</td>
<td>有了它，就不必打印两个独立但相关的报表。</td>
</tr>
<tr>
<td>直接以 PDF 格式生成管制报表。</td>
<td>您必须首先以一种格式生成一个管制报表，然后将其导出到 PDF 格式。</td>
<td>PDF 格式是管制报表的默认格式。</td>
<td>它在计算机监视器和打印的纸质副本上提供统一的显示体验。</td>
</tr>
<tr>
<td>作为批处理运行销售税结算流程。</td>
<td>不可用</td>
<td>在<strong>销售税结算期间</strong>页上，您可以指定结算流程应以批处理模式运行。</td>
<td>对于有很多涉税交易记录的期间，结算流程可能非常耗时，而作为批处理进程在后台运行该进程可能更好。</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>基础

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>随时随地访问客户端。</td>
<td>AX 2012 桌面客户端提供全套窗体，但它只能在运行 Microsoft Windows 的计算机上运行并要求安装。 终端服务器通常与桌面客户端一起使用，来启用通过广域网 (WAN) 的访问。 企业门户 Web 客户端提供更少的窗体。</td>
<td>这两个 AX 2012 客户端已经被单个的、基于标准的 Web 客户端替换了，该客户端连同企业门户客户端一起提供全套桌面客户端功能。</td>
<td>它防止开发工作在两个 UI 平台之间被拆分。 通过使用标准 Web 界面，它消除了对终端服务器的需要。</td>
</tr>
<tr>
<td>通过使用新的任务录制器，更有工作效率。</td>
<td>AX 2012 任务录制器需要直接访问应用程序对象服务器 (AOS) 计算机的权限和提高的权限，不提供编辑选项。</td>
<td>新任务录制器可以直接从 Web 客户端使用。 对任务录制器的访问不要求管理员权限。 记录的步骤可以在记录的同时实时查看，引入了新的编辑选项卡，而且除了现有业务流程建模器 (BPM) 方案，任务录制器还支持更多方案。</td>
<td>新任务录制器提供简化的体验，并在 Dynamics AX 中提供新功能。 其中某些功能立即可用，而未来会推出更多功能。</td>
</tr>
<tr>
<td>通过工作区帮助用户更好地了解其即将到来的工作。</td>
<td>角色中心提供与在企业或组织中的用户的工作职能的有关信息的概览。</td>
<td>工作区是 Dynamics AX 中的新概念，旨在作为替换角色中心的主要方式以导航到任务和特定页面。 它们提供了业务活动的一页概览，并帮助用户了解当前状态、即将到来的工作负荷，以及流程或用户的表现。 工作区比 AX 2012 角色中心更细化，用户可能可以访问多个工作区。</td>
<td>工作区旨在提高用户生产效率。 开发人员需要为产品支持的每个重大“活动”创建工作区。 AX 2012 的传统角色中心通常会被 Dynamics AX 的当前版本的多个工作区替换。</td>
</tr>
<tr>
<td>使窗体响应浏览器视区或设备大小。</td>
<td>在 AX 2012 中，窗体内容使用列严格布置，整个窗体高度/宽度很大程度上基于窗体上的控件。</td>
<td>切换到最新的 Dynamics AX 中的 Web，窗体尺寸现在基于浏览器视区大小或设备。 控件和布局参数已修改或添加以更好地响应视区大小的变化。</td>
<td>窗体内容需要更快地响应，以最佳方式利用可用的浏览器或设备的高度/宽度。 实现响应能力可能需要以窗体进行建模的方法更改。</td>
</tr>
<tr>
<td>将模式用于增强窗体的开发经验。</td>
<td>窗体模板是基于窗体样式作为 AX 2012 中窗体开发的起点提供。 窗体样式检查器（可选附加项）提供窗体如何源自其相应模板的信息。</td>
<td>在当前版本中的 Dynamics AX 中，引入了窗体模式。 窗体模式代表紧密地集成到开发体验的窗体模板和窗体样式检查器的组合。 模式已在窗体级别（如 AX 2012）定义，其他子模式现已在组和选项卡页级别提供。</td>
<td>遵守模式的窗体有许多好处，包括更加一致的用户界面、更简单的开发体验、更简单的窗体升级路径和增强的窗体布局响应性信心。</td>
</tr>
</tbody>
</table>

## <a name="help"></a>帮助

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>通过单击<strong>帮助</strong>，访问引导式程序帮助（任务指南）和概念主题。</td>
<td>AX 2012 帮助系统指向本地 Web 服务器上存储的 HTML 主题。 客户和合作伙伴可以创建自己的帮助。</td>
<td>Dynamics AX 的当前版本中的帮助系统显示在 Microsoft Dynamics Lifecycle Services (LCS) BPM 中存储的任务指南。 帮助系统还显示 Microsoft Learn 中的主题。 有关详细信息，请参阅<a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">帮助系统</a>和<a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">新任务指南（2016 年 2 月）</a>。</td>
<td>任务指南提供引导、交互式的体验，带领您完成任务或业务流程中的步骤。 您可以下载和自定义 Microsoft 提供的任务指南。 本文提供了更快、更灵活的方式来创建、交付和更新产品文档。 因此，它有助于确保您有权访问最新技术信息。</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>人力资本管理

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>在完成课程时将技能和证书传送给课程参与者。</td>
<td>这是手动流程。</td>
<td>课程完成时会提供一个新选项，以便使用新的技能和证书更新参与者的记录。</td>
<td>它提供了新的、有效的方式来更新员工记录。</td>
</tr>
<tr>
<td>快速验证雇用。</td>
<td>这是手动流程。</td>
<td>您的人力资源部门可以通过使用工作区或员工页，快速验证雇用。</td>
<td>您的人力资源部门不再需要访问多个页面来验证开始日期、经理、在职月数以及薪酬数据。</td>
</tr>
<tr>
<td>让员工查看、更新和删除系统中的信息。</td>
<td>可用，但只有有限的查看和更新功能。</td>
<td>此功能已启用，可让员工和合同工查看多种个人数据。 或者，当创建、更新或删除信息时，可以使用工作流。</td>
<td>它允许员工控制自己的信息，无论信息否与更新地址或联系人信息、申请工作、参与调查问卷或更新图像有关。 在启用工作流时，根据您的业务流程，信息可以由审核人审批或自动审批。</td>
</tr>
<tr>
<td>允许经理查看或编辑员工信息。</td>
<td>可用，但只有有限的查看和更新功能。</td>
<td>根据配置设置和安全性，经理可以查看或编辑员工信息。</td>
<td>它允许经理访问重要员工数据，因此，他们可以针对资源、绩效和员工发展作出更好的决策。</td>
</tr>
<tr>
<td>利用经理自助服务功能。</td>
<td>不可用</td>
<td>经理现在可以提交新雇佣（员工和承包商）、转岗和终止（结束雇用）请求。 经理还可以请求一个新职位、扩展职位持续时间，或请求职位更改。</td>
<td>这些方案以前只向人力资源公开。 启用这些方案在组织中为经理提供功能强大的工具。 可以启用可选工作流，以提供适当级别的审查和审核。</td>
</tr>
<tr>
<td>访问薪酬处理的结果。</td>
<td>结果仅在处理时可用。</td>
<td>在运行流程后，现在可以随时访问薪酬处理结果。</td>
<td>它可卓越地审核流程和流程的结果。 它还在员工记录更新之前提供数据的全面概览。</td>
</tr>
<tr>
<td>访问福利处理的结果。</td>
<td>结果仅在处理时可用。</td>
<td>在运行流程后，现在可以随时访问福利处理结果。</td>
<td>它提供福利登记和成本变化所更新的数据的全面概览。</td>
</tr>
<tr>
<td>查看“有效日期”时间线更改。</td>
<td>不可用</td>
<td>这一比较工具可用于员工、职位和工作。 它提供了从记录的一个版本到另一个版本的更改的全面概览。</td>
<td>在您查看随时间推移发生的员工、职位和工作记录更改时，它为您节省时间。 它能让您随着时间的推移快速比较记录的两个版本，或者所有记录。</td>
</tr>
<tr>
<td>按公司查看员工。</td>
<td>这是通过筛选执行的手动流程。</td>
<td>员工和合同工列表按您登录的公司自动筛选。</td>
<td>它提供了在登录到的公司中就职的员工的筛选视图。 对于所有员工和合同工的未筛选视图，工作人员列表仍可用。 在 Dynamics AX 的当前版本中，系统不基于在列表中选定的员工更改公司。</td>
</tr>
<tr>
<td>更新课程参与者列表。</td>
<td>不可用</td>
<td>可以从参与者列表中删除课程参与者。</td>
<td>它提供了一个简单的方式来更新错误登记的课程参与者。</td>
</tr>
<tr>
<td>按组管理薪酬事件。</td>
<td>不可用</td>
<td>此功能简化处理员工的薪酬更改。</td>
<td>它提供一个简单、简化的流程来通过薪酬工作区和相关页面更新员工记录。</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>库存管理

未添加新功能。

## <a name="localization"></a>本地化

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>配置并生成电子文档以满足不同国家/地区的法规要求。</td>
<td>电子文档是以 X++ 格式硬编码的，或者作为可扩展样式表语言转换 (XSLT) 硬编码的。 所有格式调整都需要开发工作。 对数据和格式的访问未隔离。 已调整的格式部署要求覆盖该现有格式的新的 Microsoft Dynamics AX 修补程序包。 每个格式的自定义修改都必须手动导入新 Microsoft Dynamics AX 修补程序包的源代码中。</td>
<td>电子申报 (ER) 是一个新工具，用于配置和生成针对业务用户而不是开发人员的电子文档。 ER 能让您将域特定的且独立于 Microsoft Dynamics AX 数据库的数据模型设置为文档格式的数据源。 业务用户可以基于这些域特定的数据模型来配置格式（例如，对于付款、内部统计报告或税金报表）。 用户通过使用类似于 Excel 的一种简单、直观的工具来配置格式。 ER 当前支持生成文本、XML 和 Excel 格式的电子文档。 这些文档可以同时生成并打包到到 zip 文件。 支持模型和格式数据版本控制。 格式版本可以具有有效期间。 每个数据模型或格式版本都存储在单独的配置中，并通过 LCS 分发给合作伙伴和客户。 合作伙伴和客户可以自定义 Microsoft 数据模型和格式，或者创建自己的数据模型和格式。 ER 将合作伙伴和客户配置更改保存为 Microsoft 配置的增量，以便简化到 Microsoft 配置的新版本的升级。 通过使用 LCS，合作伙伴还可以与其他合作伙伴和客户共享数据模型和格式配置，其他合作伙伴和客户可以自定义和共享它们。 增量自定义和简易升级通过整个自定义链受支持。</td>
<td>ER 简化电子文档格式的创建、维护和升级，以便符合不同国家/地区的法规要求。 ER 使创建或更改电子文档格式的流程更快、更容易。 这些更改可以由业务用户而不是开发人员完成。 ER 使合作伙伴和客户更快、更容易将格式自定义升级到由 Microsoft 或其他合作伙伴发布的新版本格式。 ER 提供一种常见方式（通过 LCS）让 Microsoft 和合作伙伴将电子文档配置分发给其他合作伙伴和客户。 ER 还使合作伙伴和客户更容易特定业务需求自定义、升级和分发电子文档格式。</td>
</tr>
<tr>
<td>(MEX) 生成墨西哥增值税 (VAT) 管制报表。</td>
<td>您必须通过使用未实现的销售增值税功能来生成<strong>销售和采购增值税</strong>报表，因此，用户可以基于状态来识别属于已实现部分和未实现部分的交易记录。</td>
<td><strong>销售和采购增值税</strong>报表已经修改，现在仅通过未实现和已实现销售税代码的定义的特定结算期间来考虑特殊增值税功能。</td>
<td>需要更改销售税代码的配置，然后用户才能正确生成这些报表。 需要特殊增值税功能，并且，用户必须配置单独的结算期间、未实现的已实现的，从而在相关部分区域识别交易记录。</td>
</tr>
<tr>
<td>(JPN) 管理日本固定资产加速折旧申报文档。</td>
<td>不可用</td>
<td>重要申报信息集中存储在一个文档中，以便更好地维护。</td>
<td>在审核和其他审查期间，文档符合性和管理简便性可帮助减少问题。</td>
</tr>
<tr>
<td>(JPN) 验证银行帐户上的 JBA 字符。</td>
<td>不可用</td>
<td>您可以验证假名字段是否仅包含 JBA 银行格式允许的字符。</td>
<td>由于无效字符，它可帮助在生成付款文档时减少对用户的干扰。</td>
</tr>
<tr>
<td>(JPN) 在会计年度结束时跟进日本固定资产尾差。</td>
<td>不可用</td>
<td>在<strong>固定资产参数</strong>页上，您可以选择在会计期间或会计年度结束时跟进。</td>
<td>它提供更大的灵活性来符合当地风俗。</td>
</tr>
<tr>
<td>(JPN) 生成日本公司纳税申报追加表 16 系列（按固定资产主要类型汇总的金额）。</td>
<td>不可用</td>
<td>在固定资产的价值模型上，您可以选择按主要类型汇总。 默认情况下，此功能用于新创建的固定资产。</td>
<td>对于具有数以千计固定资产的大型公司，汇总报表极大地减少生成报表的规模。</td>
</tr>
<tr>
<td>(JPN) 从下一会计年度开始针对日本固定资产分配特殊折旧准备金。</td>
<td>不可用</td>
<td>在具有相应的特别折旧模板的固定资产价值模型上，您可以选择从下一会计期间或下一会计年度开始分配。</td>
<td>它提供更大的灵活性来符合当地风俗。</td>
</tr>
<tr>
<td>(JPN) 生成包括修订税率的日本消费税报表。</td>
<td>消费税报表可用于 5% 的税率。</td>
<td>消费税报表包含一个用于修订税率（例如，8%）的部分。</td>
<td>布局是由政府新公布的。</td>
</tr>
<tr>
<td>(EU) 为欧盟销售清单配置舍入设置。</td>
<td>各个国家/地区的欧盟销售清单报告的舍入设置是硬编码，使用 X ++ 或可扩展样式表语言转换 (XSLT)。</td>
<td>舍入设置添加到外贸参数。 您可以为小于舍入精度的金额配置舍入精度、舍入方法、输出精度和行为。</td>
<td>这将统一并简化欧盟销售清单报告的配置。 舍入设置的调整不再需要开发工作。</td>
</tr>
<tr>
<td>(EU) 配置冲销费用适用性规则。</td>
<td>冲销费用适用规则被硬编码为国内冲销费用方案。 适用性阈值可以为每个物料组设置。 该功能仅可用于英国。</td>
<td>您可以配置每个文档类型（采购/销售订单、供应商发票、普通发票等）的冲销费用适用规则，以及组合物料、物料组和采购/销售类别的冲销费用组。 适用规则具有有效日期。 您还可以将销售税组中的单个销售税代码标记为适用于冲销费用。 销售发票报表进行调整来表示应用冲销费用的详细信息。 此功能可用于所有国家/地区。</td>
<td>此更改将统一冲销费用适用规则的配置，并支持欧洲国家/地区的国内冲销费用法规的采用。</td>
</tr>
<tr>
<td>(DE) 生成德国审计文件 - GDPdUGoBD</td>
<td>用户可以设置包含使用德国审计机构和监管机构接受的格式导出的财务数据的表的定义。</td>
<td>此功能已作为电子申报配置实现。 该功能可用于德国和奥地利。</td>
<td>这一更改为用户提供数据格式、转换的更多可能性，还提供了所有来自电子申报配置生命周期管理的优点，如轻松配置汇率、版本控制等。</td>
</tr>
<tr>
<td>(FR) 具有组合计科目的余额表。</td>
<td>具有组合计科目的余额表作为 SSRS 报表 (LedgerAccountSum_FR) 实现。</td>
<td>具有组合计科目的余额表作为 LCS 资产库本地化财务报表文件夹中提供的管理报表器报表实现。</td>
<td>这使用户能够通过在管理报表器中使用财务报表来获取自定义项的所有优点和自由。</td>
</tr>
<tr>
<td>(EU) 付款的付款通知报、出席单和控制表。</td>
<td>所有这些报表已实现，为 SSRS 报表。</td>
<td>这些报表已实现为 Open XML 模板，用于 Microsoft Excel。</td>
<td>电子支付配置包含付款文件格式设置和模板。 这使用户能够通过使用电子申报来获取报表自定义的所有优点和自由。</td>
</tr>
<tr>
<td>(EU) 为内部统计配置舍入设置。</td>
<td>各个国家/地区的内部统计报告的舍入设置是硬编码，使用 X ++ 或可扩展样式表语言转换 (XSLT)。</td>
<td>舍入设置添加到外贸参数。 您可以为小于舍入精度的金额配置舍入精度、舍入方法、输出精度和行为。</td>
<td>这将统一并简化内部统计报告的配置。 舍入设置的调整不再需要开发工作。</td>
</tr>
<tr>
<td>(EU) 设置类别层次结构中的内部统计商品代码。</td>
u<td>内部统计商品代码是一个单独的列表。 虽然存在商品代码类型的类别层次结构，这些商品代码无法在 Retail HQent 和销售类别中被视为默认设置。</td>
<td>单独的内部统计商品代码列表与商品代码类型的产品层次结构合并。</td>
<td>这将统一将商品代码分配给销售和采购单据中已发布产品和类别的方法。</td>
</tr>
<tr>
<td>(EU) 通过使用单位转换设置报告内部统计的其他单位的数量。</td>
<td>内部统计商品代码有一个文本字段，以标识其他单位，<strong>产品</strong>卡有一个字段来标识其他单位（千克）的数量。</td>
<td>用于内部统计商品代码的其他单位从“单位”列表中选择。 通过单位转换设置计算其他计价单位的数量。</td>
<td>这将统一将交易记录单位重新计算为其他单位的方法。</td>
</tr>
<tr>
<td>(EU) 将默认运输方法分配到交货方式。</td>
<td>不可用</td>
<td>将默认运输方法字段添加到交货方式。</td>
<td>这简化了内部统计报告的准备的工作。</td>
</tr>
<tr>
<td>(EU) 标记发布的产品不要在内部统计中报告。</td>
<td>不可用</td>
<td>从内部统计报告中排除物料的选项被添加到已发布产品。</td>
<td>这简化了内部统计报告的准备的工作。</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>制造

| 您能怎么做？ | Dynamics AX 2012 |
|------------------|------------------|
| 在单独的页面上针对生产订单执行物料可用性检查，该页面可从 **生产车间管理** 工作区中打开。 | 不可用 |
| 通过使用新的 **作业卡设备** 页，启动并报告生产作业的进度。 | **工作登记** 窗体主要面向大型终端屏幕，UI 通常通过鼠标单击即可访问。 |

## <a name="master-planning-and-forecasting"></a>主计划和预测

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 如果销售订单或生产订单没有做好按计划日期交货的准备，则将警告用户。 | 由主计划创建的警告叫做 *预期消息*。 *预期* 是两个当事方之间的合同，用于按照今天议定的价格（*预期价格*）采购或销售资产，但交货和付款在未来的时间点（*交货日期*）发生。 | *预期消息* 和 *将来日期* 各自重命名了 *计算的延迟* 和 *延期的日期*。 | AX 2012 中使用的术语不准确，导致不正确的翻译。 |
| 用户可以快速了解主计划运行的状态、紧急计划订单和导致延迟的计划订单。 | 该信息可用，但分散在多个窗体中。 | **主计划** 工作区提供有关上次主计划运行何时完成、是否发生任何错误、紧急计划订单是什么、以及哪个计划订单导致延迟的概览信息。 | 您可从工作区提供的概览中获益。 相关信息组合起来，可引导主计划和帮助提高生产率。 |
| 使用 Excel 更新需求预测。 | 不可用 | 当您输入需求预测、进行更新和删除需求预测时，可以利用与 Excel 的无缝集成。 | 它有助于提高效率和生产率。 |
| 根据历史交易记录数据来估计未来需求并创建需求预测。 | 在 Microsoft Dynamics AX 2012 R3 中，Microsoft SQL Server 分析服务中的预测模型用于创建需求预测。 | 利用 Microsoft Azure 机器学习云服务的功能和可扩展性来估计未来需求。 它易于使用和扩展机器学习中的预测模型以满足客户要求。 该服务执行最符合模型选择，并提供可用于计算预测的准确性 (KPI) 的关键绩效指标 (KPI)。 | 通过使用机器学习技术，生成更准确的预测。 |
| 基于主计划运行中的相关操作的可视概览，优化订单日期和数量。 | 操作图表概览可用，但会显示所有相关操作。 当应用操作时，操作将立即从视图中消失。 | 操作图表提供更好的概览。 它包含可用于仅显示已应用操作和直接相关操作的选项。 当应用操作时，操作将灰显，但仍显示。 因此，概览仍保留。 附加信息添加到操作图表，以在一页上显示数据。 | 您会生产力增强中获益，因为您只侧重于相关操作。 |

## <a name="procurement-and-sourcing"></a>采购

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 使用 **采购订单准备** 工作区可快速了解正在准备的采购订单的状态。 | 不支持 | **采购订单准备** 工作区提供订单的概览，从订单作为草稿被创建并被跟踪时起，历经工作流审核状态，直到确认。 | 您的采购部门不必再寻求多个页面的信息，而是现在从该工作区提供的概览中获益。 |
| 使用 **采购订单收货和跟进** 工作区快速了解正在等待收货的采购订单，以帮助跟进。 | 不支持 | **采购订单收货和跟进** 工作区提供等待收货或装运的已确认采购订单的概览。 该工作区包括过期收货和等待收货的列表，用以帮助供应商进行主动审核和跟进。 该工作区还列出已在仓库中发生其到达登记的采购订单，以帮助确保收货得以过帐。 尚未装运的采购订单退货也可用，以供审核。 | 您的采购部门会从科该工作区提供的概览中获益。 相关信息组合起来，可引导跟进和帮助提高生产率。 |
| 向在 Dynamics AX 客户端中承载的供应商门户发送采购订单以供确认。 允许供应商确认或拒绝。 | 不支持 | 供应商门户界面允许供应商接收采购订单以便确认或拒绝。 它还允许供应商概览帐户的所有已确认采购订单。 采购代理可以发送采购订单以请求供应商确认。 供应商必须是 Dynamics AX 中的一个登记 Microsoft Azure Active Directory (Azure AD) 用户，供应商的联系人有专用的安全角色。 | 您的采购部门从减少书面工作和手动在采购订单上跟踪响应（因为他们直接进入系统）中获益。 具有一个事实来源可减少客户和供应商之间的误解。 |

## <a name="projects"></a>项目

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 预订工作人员作为项目的资源。 | 类似于资源，除了资源之外，工作人员是直接在项目中预订的。 | 用于存储制造和生产资源的工作中心表现在可用于预订工作人员作为项目的资源。 | 在您预订项目时，您只需预订资源。 |

## <a name="retail-sales-marketing-and-customer-service"></a>零售销售、市场营销和客户服务

### <a name="retail-hq"></a>Retail HQ

Microsoft Azure 承载的 Retail HQ 能让您通过 Web 客户端集中管理和全面了解商务运营的各个方面。

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>执行促销操作。</td>
<td>用户必须访问多个窗体来管理此数据：
<ul>
<li>类别管理</li>
<li>产品管理</li>
<li>渠道产品属性</li>
<li>分类</li>
<li>目录管理</li>
<li>配套件</li>
<li>价格 &amp; 折扣</li>
</ul></td>
<td><strong>类别和产品管理</strong>工作区启用以下功能：
<ul>
<li>分类管理。</li>
<li>分类生命周期跟踪。</li>
<li>已发布产品管理。</li>
</ul>
<strong>价格和折扣管理</strong>工作区启用以下功能：
<ul>
<li>给定渠道和类别的价格和折扣管理。</li>
<li>类别价格规则管理。</li>
<li>价格和折扣优先级，用于让您向价格组和折扣分配优先级，因此，您可以控制应用它们的顺序。</li>
<li>隶属关系和类别折扣管理。</li>
</ul>
<strong>类别管理</strong>工作区启用以下功能：
<ul>
<li>有效目录的汇总。</li>
<li>单个地点中的目录生命周期跟踪。</li>
</ul></td>
<td><ul>
<li>工作区通过让工作人员集中管理与促销角色相关的任务和操作，提高工作人员的效率和生产率。</li>
<li>价格和折扣优先级功能让客户能够更多地控制如何使用价格和折扣。 此功能还启用新方案，即更高的商店价格战胜标准价格。</li>
</ul></td>
</tr>
<tr>
<td>管理零售渠道部署和操作。</td>
<td>用户必须访问多个窗体来执行以下任务：
<ul>
<li>创建和配置新渠道和相关实体。</li>
<li>管理每日商店活动。</li>
<li>在 Microsoft Dynamics AX 中处理零售交易记录，生成零售报表，并更新 Microsoft Dynamics AX 库存和财务信息。</li>
</ul>
</td>
<td><strong>渠道部署</strong>工作区能让您执行以下任务：
<ul>
<li>创建新渠道和相关实体。</li>
<li>跟踪零售商店配置的进度。</li>
<li>执行所需的步骤以完成任务，或提供信息以完成任务。</li>
<li>跟踪设备的状态，直接在商店中验证并下载 Retail Modern POS (MPOS) 程序安装。</li>
<li>访问所有相关页。</li>
</ul>
<strong>零售商店管理</strong>工作区能让您执行以下任务：
<ul>
<li>管理工作人员和工作人员的销售点 (POS) 权限。</li>
<li>跟踪给定商店或商店组的班次状态。</li>
<li>在商店中直接验证和下载 MPOS 程序安装。</li>
<li>打印报表和访问相关页。</li>
</ul>
<strong>零售商店财务</strong>工作区能让您执行以下任务：
<ul>
<li>创建、计算和过帐给定渠道的报表。</li>
<li>安排批处理作业以更新库存，并且计算和过帐报表。</li>
<li>跟踪未结报表。</li>
<li>跟踪给定商店或商店组的班次状态。</li>
<li>打印报表和快速访问所有相关页。</li>
</ul></td>
<td>工作区通过让工作人员集中管理与渠道部署、商店管理和财务相关的大多数任务和操作，提高工作人员的效率和生产率。</td>
</tr>
<tr>
<td>管理零售 IT 运营。 </td>
<td>用户必须访问多个窗体。</td>
<td><strong>零售 IT</strong> 工作区针对给定渠道在单个位置启用 Commerce Data Exchange 查询，因此，您可以执行以下任务：
<ul>
<li>下载会话。</li>
<li>上载会话。</li>
<li>跟踪失败会话，并且重新启动或运行它们。</li>
<li>查看或运行即将发生的作业。</li>
</ul></td>
<td>工作区通过让工作人员集中管理与零售 IT 运营相关的任务和操作，提高工作人员的效率和生产率。</td>
</tr>
<tr>
<td>使用数据实体导出/导入数据。</td>
<td>AX 2012 支持通过数据导入/导出框架迁移现成 Microsoft Dynamics 零售管理系统 (RMS)。</td>
<td>零售数据实体已扩展，可支持与零售有关的所有主数据和引用数据。 还有在整个 Dynamics AX 解决方案中对数据实体提供增强的支持。</td>
<td>数据实体允许客户执行元数据驱动的数据导入和导出。 OData 实体还允许客户将 Dynamics AX 与第三方程序集成。</td>
</tr>
<tr>
<td>通过使用来自 Dynamics Microsoft AX 和 POS 客户端的 BI 报表，执行智能分析。</td>
<td>超过 25 个后端办公室报表以及 5 个渠道侧报表可用。</td>
<td>超过 30 个后端办公室报表以及 10 个渠道侧报表可用。</td>
<td>这些报表允许客户有更多 BI 来预测趋势，发现见解和以持续绩效高峰运营。</td>
</tr>
<tr>
<td>通过使用“监控 Retail Channel performance”Power BI 内容来分析零售渠道销售数据。</td>
<td>不可用</td>
<td>在 PowerBI.com 上，选择<strong>获取数据</strong>，然后选择 <strong>Dynamics AX – 零售渠道绩效</strong>内容包。 输入您的 Dynamics AX 终结点的 URL 以查看反映在仪表板中的数据。</td>
<td>通过三到四次单击，组织可以部署一个包含重要财务数据的 Power BI 仪表板。 内容可由组织个性化。 此外，用户可以将 Power BI 仪表板磁贴嵌入到其在 Dynamics AX 中的个性化工作区，因此，用户随后可以快速查看分析信息。</td>
</tr>
<tr>
<td>配置用户权限。</td>
<td>不可用</td>
<td>客户可以选择 POS 操作是否可用于客户。 Retail Server 使用权限来进行应用程序编程接口 (API) 调用。</td>
<td>它能让用户配置用户级权限。</td>
</tr>
<tr>
<td>管理和验证实体配置。</td>
<td>不可用</td>
<td>配置管理器和验证器功能启用以下功能：
<ul>
<li>批量配置数据上载</li>
<li>业务实体验证</li>
</ul></td>
<td>它能让用户引导配置，以及验证配置的状态和各种配置元素的完整性。</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Retail 硬件工作站

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 使 POS 设备能连接到外围设备，例如打印机、银箱或付款设备。 | MPOS 硬件配置文件用于指定要使用的设备。 | 一个添加的硬件配置文件支持更多不同硬件，从一个工作站到下一个工作站。 在处理电子资金转帐 (EFT) 交易记录时，新的硬件工作站配置文件对每个硬件工作站都支持一个唯一的终端 ID。 EFT 支持已合并到硬件工作站，以减少 EFT 付款处理中 MPOS 的涉及。 | 它为实现提供更大的灵活性。 它还提供增强的安全性和减少的信用卡数据暴露。 |

### <a name="retail-server-and-data-management"></a>Retail Server 和数据管理

Retail Server 和数据管理允许客户和企业跨在线、商店内和呼叫中心渠道创建 omni 渠道购物体验。

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>连接到 Commerce Runtime (CRT) 数据库，其中使用 CRT 服务存储渠道的业务数据。</td>
<td>支持 OData V3。</td>
<td>支持 OData V4。</td>
<td>它帮助客户紧跟 OData 条件。 它还通过跨商店内、移动和在线渠道集成销售，创建可靠的 omni 渠道体验。</td>
</tr>
<tr>
<td>支持零售服务作为可托管服务组。</td>
<td>电子商务 API 不通过 Retail Server 受支持。</td>
<td>电子商务 API 现在通过 Retail Server 可用，用以支持联机方案。</td>
<td>它提供承载的且可扩展的电子商务服务，可以和第三方联机商店一起使用。</td>
</tr>
<tr>
<td>通过使用 Commerce Data Exchange，在 Microsoft Dynamics AX 后端办公室和渠道之间移动数据。</td>
<td>Commerce Data Exchange 是一种在 Microsoft Dynamics AX 和零售渠道（例如，在线商店或实体商店）之间传送数据的系统。 有关详细信息，请参阅<a href="/dynamicsax-2012/appuser-itpro/commerce-data-exchange">Commerce Data Exchange [AX 2012]</a>。</td>
<td>与 Microsoft Dynamics AX 2012 CU8 之间有功能对等性。 不过，请注意以下详细信息：
<ul>
<li>Commerce Data Exchange 针对云重新进行了设计。</li>
<li>异步服务使用直接数据库访问权限来访问渠道数据库。</li>
<li>Commerce Data Exchange：实时服务是作为 Microsoft Dynamics AX 自定义服务承载的。</li>
<li>MPOS 管理脱机数据库和 Retail Server 之间的同步。</li>
</ul></td>
<td>Commerce Data Exchange 针对云平台重新进行了设计。 它继续管理 Microsoft Dynamics AX 和零售渠道（例如，在线商店或实体商店）之间的数据传送。</td>
</tr>
<tr>
<td>通过使用付款 SDK，支持即插即用、半集成的跨渠道付款处理。</td>
<td>AX 2012 提供以下功能：
<ul>
<li>支持所有通道：POS、电子商务和呼叫中心。</li>
<li>支持卡存在和卡不存在。</li>
<li>接受付款的页面。</li>
<li>作为 Retail SDK 中的示例代码对 LS5300 和 MX925 提供外围支持。</li>
</ul></td>
<td>Dynamics AX 的当前版本支持所有现有 Microsoft Dynamics AX for Retail 2012 信用卡/借记卡功能和四种新的改进。</td>
<td>它允许客户处理付款的信用卡/借记卡交易记录。</td>
</tr>
<tr>
<td>通过使用 Microsoft 帐户 (Microsoft Azure Active Directory (Azure AD)) 启用设备。</td>
<td>不可用</td>
<td>提供以下功能：
<ul>
<li>针对云环境通过基于 Azure AD 的激活增强了安全性。</li>
<li>针对令牌管理增强了安全性。</li>
<li>改进了激活过程中的可靠性、故障排除和错误消息传送</li>
<li>简化了与激活有关的 IT 管理任务。</li>
<li>重新访了威胁模型并修复了安全问题。</li>
</ul></td>
<td>它提供了以下优点：
<ul>
<li>通过 Azure AD 和设备令牌/ID（使用令牌的 RS 调用，用户特定的应用程序存储）增强了安全性。</li>
<li>该停止对 MPOS（传统设备）的未授权远程使用。</li>
<li>它出于 PCI 符合性目的跟踪 MPOS 设备。</li>
<li>它使用设备令牌映射具有企业实体的物理设备。</li>
<li>它初始化顺畅 MPOS 功能的设置（编号规则和硬件配置文件），作为 MPOS 的第一个接触点。</li>
<li>它报告来自总部的设备信息。</li>
</ul></td>
</tr>
<tr>
<td>通过媒体库管理富媒体内容的编写和服务。</td>
<td>不可用</td>
<td><ul>
<li>支持图像上载，并且可以针对外部承载的和 Retail 承载的图像在媒体库中进行查看、管理和删除。</li>
<li>通过链接库中的图像和从桌面上载图像，支持从实体页（<strong>产品</strong>、<strong>目录</strong>等）上载和查看图像。</li>
<li>优化图像以达到缩略图、自定义大小和原始效果。</li>
<li>通过对批量关联使用模板和后台作业，批量链接实体。</li>
<li>Microsoft Excel 集成覆盖命名约定和预定义路径的属性组限制。</li>
<li>支持将脱机图像和安全图像用于个人可识别信息 (PII) 内容，例如 Retail 承载的员工和客户图像。</li>
</ul></td>
<td><ul>
<li>它解决围绕外部承载的图像的痛点，因此，您可以避免反复执行某些步骤，并且可以在单个位置进行管理。</li>
<li>它通过媒体库为上载的和外部承载的图像提供强大的内容管理，并且提供筛选以帮助您查找图像。</li>
<li>它能让您轻松地在外部承载的图像和实体（例如产品和类别）之间创建批量关联。</li>
<li>它为图像支持 Retail 承载的存储，为简易更新支持 Excel 集成。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>富客户体验

Retail 随时随地在任何设备上提供沉浸式移动体验。 此功能在所有通道中启用增强的购物和商店体验。

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>通过使用一个直观、触摸友好、丰富的沉浸式用户体验，来搜索、浏览、查找或扫描产品、将产品添加到购物车、接受付款，以及签出。</td>
<td>AX 2012 启用以下功能：
<ul>
<li>执行销售、退货和取消。</li>
<li>创建、修改和领取客户订单。</li>
<li>执行班次和银箱操作。</li>
<li>领取和接收订单，以及执行存货盘点。</li>
<li>查看商店内报表。</li>
</ul></td>
<td>提供与 AX 2012 MPOS 之间的功能对等性。 这包括以下功能：
<ul>
<li>跨商店/渠道进行客户查找。</li>
<li>能够创建客户订单，而无需访问实时服务。</li>
<li>改进了设备激活工作流、状态和错误消息。</li>
<li>进行了延伸性改进（例如过帐前触发和活动支持）以改进自定义。</li>
</ul></td>
<td>销售人员可以通过在商店中的任何位置使用移动设备，来处理销售交易记录和客户订单，并执行日常运营和库存管理。</td>
</tr>
<tr>
<td>通过 Cloud POS 将 POS 作为 Web 应用程序启动。</td>
<td>不可用</td>
<td>提供与 MPOS 之间的功能对等性。 这包括以下功能：
<ul>
<li>通过使用 AAD 进行设备激活</li>
<li>响应性强的布局设计</li>
<li>支持 Microsoft Edge、Internet Explorer 和 Chrome 浏览器。</li>
</ul></td>
<td>它提供了一个 Web 应用程序 POS，其具有与 MPOS 兼容的功能，并且可以在多个平台和 Web 浏览器中使用而没有配置成本。</td>
</tr>
<tr>
<td>与内容管理系统集成，以创建 omni 渠道电子商务网站。</td>
<td>支持 Microsoft SharePoint 和第三方店面。</td>
<td>提供一个电子商务平台，以支持第三方店面。 该平台包括以下功能：
<ul>
<li>一个丰富的用户 API。</li>
<li>面向任何第三方开放式 ID 提供商的身份验证集成。</li>
<li>付款集成。</li>
</ul></td>
<td>客户现在可灵活地使用其选择的内容管理系统。</td>
</tr>
<tr>
<td>通过邮件订单目录来瞄准客户，并通过快速订单条目、协助销售和使用呼叫中心的履行来简化操作。</td>
<td><ul>
<li>呼叫中心渠道</li>
<li>邮件订单目录</li>
<li>快速订单条目和协助销售</li>
<li>改进的订单履行</li>
<li>客户服务</li>
<li>集成的定价和促销/折扣</li>
</ul></td>
<td>提供与 AX 2012 呼叫中心之间的功能对等性，但价格覆盖除外。</td>
<td>呼叫中心是一种类型的零售渠道，它能让工作人员通过电话接受来自客户的订单和创建销售订单。</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>商业要素

侧重于零售和商务的配置选项可帮助简化特定于零售的配置。

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 使用商业要素仪表板。 | 提供一个区域页，其带有指向菜单项的链接。 | 商业要素仪表板提供指向常用任务的链接，包括指向工作区、Power BI Web 控件、收藏夹、最近查看页面和当前工作项的链接。 | 增强的仪表板能让工作人员提高效率并提供一个灵活的起点以适用于任何特定于零售的任务。 |
| 使用数据实体访问帐户更改。 | 帐户更改导出到文件系统上的文件夹中。 | 帐户更改可通过数据实体获得。 | 在不同系统之间移动数据时，此功能提供更大的灵活性。 此功能还可通过 OData 应用程序增强。 |
| 使用 Cloud POS 和 MPOS。 | 只支持现成的 Enterprise POS (EPOS)。 | MPOS 和 Cloud POS 替换 EPOS 客户端。 默认情况下，电子商务渠道也将添加到商业要素。 | 此功能通过可迅速部署的销售终端客户端启用更好的现成渠道支持。 |
| 实施和维护两层体系结构。 | 数据导出/导入框架能让您在 AX 2012 和第三方系统之间移动数据。 | 创建了数据实体可提高对两层体系结构的支持。 | 数据实体和 OData 应用程序提供一个抽象层，使两层方案更易于实施和维护。 |
| 简化窗体。 | 需要自定义代码，用以简化 UI。 | 窗体和菜单扩展提供标准化的 UI 简化。 | 此功能提供更方便快捷的方式来基于零售商的需要优化窗体。 |

### <a name="pos-task-recorder"></a>POS 任务录制器

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>为 Modern POS 创建和共享任务指南和文档。</td>
<td>不可用</td>
<td>MPOS 任务录制器支持以下功能：
<ul>
<li>为在 MPOS 中执行的多种任务创建任务记录。</li>
<li>生成一个文档，其中包含步骤和屏幕快照，并将该文档与业务流程模型中的节点关联。</li>
</ul></td>
<td>合作伙伴和独立软件供应商 (ISV) 可以自定义 MPOS 并提供支持文档以培训其用户。</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>可扩展性

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>跨 HQ、呼叫中心、电子商务和 POS 支持可扩展的且可轻松部署的 Retail 组件。</td>
<td>可使用 Retail SDK 扩展组件。 不支持包装和部署功能。</td>
<td>跨各种组件对可扩展性挂接进行了改进，从而更好地支持代码隔离和可用性。 下面是包括的某些功能：
<ul>
<li>工作流、活动和操作。</li>
<li>能让您轻松扩展工作流的前触发器和后触发器。</li>
<li>应用程序和操作触发器。</li>
</ul>
此外，还提供一个框架，能让您通过使用 MSBuild 来创建和包装这些组件，然后通过 Microsoft Dynamics Lifecycle Services (LCS) 无缝部署您的自定义项。</td>
<td>基于运营的垂直市场和地理位置，零售商有非常具体的要求。 通过提供易于扩展的平台，我们跨多个垂直市场提供可用性。 由于 Retail 还具有非常分散的体系结构，因此无缝部署的能力会极大提高生产率。</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>生命周期管理

Lifecycle Services (LCS) 提供一系列服务，可供客户和合作伙伴用来管理系统的生命周期，从注册到日常运营。

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>通过云部署服务来管理程序。</td>
<td>不可用</td>
<td>以下拓扑结构可以部署到云中：
<ul>
<li>Retail 一盒试用拓扑。</li>
<li>Retail 多盒高可用性拓扑结构。</li>
<li>采用 Retail SDK 的开发人员拓扑结构。</li>
</ul>
通过自助服务安装可获得改进的“低触摸”客户端组件安装：
<ul>
<li>Retail Modern POS。</li>
<li>Retail Hardware Station。</li>
<li>通过自助服务安装支持自定义包的上载和分配。</li>
</ul></td>
<td>云部署服务提供以下优点：
<ul>
<li>显著减少了部署工作量和 Retail HQ 组件的复杂性。</li>
<li>本地部署到 Microsoft Azure 公有云。</li>
<li>改进了商店内组件的自助服务安装，使配置更简便更直观</li>
</ul></td>
</tr>
<tr>
<td>监控系统的运行状况，并且诊断错误和问题。</td>
<td>此功能需要适用于 <a href="https://www.microsoft.com/en-us/download/details.aspx?id=58205">Microsoft Dynamics AX 2012 R3 CU8 Retail 的 System Center 2012 管理包</a>。</td>
<td>现在可以通过 LCS 中的<strong>运营见解</strong>仪表板来监控和诊断 Retail 组件。</td>
<td><strong>运营见解</strong>仪表板是一个基于云的监控门户，有了它便不再需要安装 System Center Operations Manager (SCOM) 基础结构。</td>
</tr>
<tr>
<td>通过使用自助服务，创建、配置、下载并安装 Retail Hardware Station 和设备。</td>
<td>通过使用安装包装器和企业门户，用户可以基于定义的拓扑结构，对特定计算机上需要的所有组件执行自动化安装和配置。</td>
<td>因为只有两个安装程序包，一个用于 MPOS 客户端，另一个用于 Retail Hardware Station 组件，因此自助服务减少了在每个级别安装这些客户端组件所需的工作量。</td>
<td>自助服务旨在最大限度地减少要求，并且更便于用户进行安装。</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>销售额

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>在您向客户承诺订单时，可快速概览交货备选方案。</td>
<td>当有产品可用性约束，而且客户在订单上请求的一个或多个产品的交货日期不能满足时，订单承诺任务就成为挑战。 若要查找可以抵消可用性和装运时间问题的备选方案，以便客户请求的日期可以满足，或为客户提供可以接受和信任的发货解决方案，则订单处理人员可能必须打开多个窗体，每个窗体都仅提供一部分必需信息。 具体而言，一个窗体显示跨站点的现有数量，另一个窗体显示内部公司设置的现有数量，第三个窗体能让用户一次一个站点/款式地计算最早可用日期，第四个窗体显示供应订单。 因此，用户不认为自己考虑了所有相关选项，而不是仅选择了一个眼前的但次优的解决方法。 用户也不觉得有效，因为在订单承诺流程期间在他们打开和关闭多个页面以及组合见解和选项时发生了许多中断。</td>
<td>基于交货日期计算的现有算法，<strong>交货备选方案</strong>页提供订单承诺的新用户体验：
<ul>
<li>它将多个窗体中的相关信息合并到一个空间。</li>
<li>它基于用户可以从中选择的最快交货（最早可用日期）条件，提供“现成的”备选交货包，例如站点/仓库/款式/运输方式组合。</li>
<li>它能让用户从模拟界面选择选项并将其转移到销售订单行。</li>
</ul></td>
<td>想要在致力于库存优化策略的同时提供高质量客户服务的公司，必须能够可靠而有竞争力地承诺订单。 毕竟，其客户自己的业务需要产品按时上市。 <strong>交货备选方案</strong>任务页通过在一个交互式位置标识和建议最佳备选订单交货日期，使得订单承诺任务更快速、简便和系统化。</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>服务管理

未添加新功能。

## <a name="transportation-management"></a>运输管理

未添加新功能。

## <a name="travel-and-expense"></a>出差和支出

未添加新功能。

## <a name="warehouse-management"></a>仓库管理

| 您能怎么做？ | Dynamics AX 2012 | Dynamics AX 7.0 | 为什么如此重要 |
|------------------|------------------|-----------------|------------------------|
| 下载、安装和配置仓库移动设备门户。 | 您可以通过一个标准设置，在 Microsoft Dynamics AX 安装过程中下载、安装和配置该门户。 它专用于自驱动的本地部署和配置。 | 您可以在仓库管理中通过菜单项下载独立安装程序。 它专用于自驱动的本地部署和配置。 | 在您设置移动设备功能时，您必须在本地安装并配置仓库移动设备门户，并在云中与 Dynamics AX 连接。 |

## <a name="additional-resources"></a>其他资源

[财务和运营新增功能或更改主页](whats-new-changed.md)

[新任务指南（2016 年 2 月）](new-task-guides-available-february-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

