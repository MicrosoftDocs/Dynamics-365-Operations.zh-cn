---
title: 产品配置模型概述
description: 本文定义与产品配置模型有关的术语和概念。 可通过产品配置模型构建可用于为单个产品配置大量产品变型的通用产品结构。
author: t-benebo
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "4031"
- intro-internal
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bee2d68a2ed2aa339ddf8232bba4541f4fe52b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871911"
---
# <a name="product-configuration-models-overview"></a>产品配置模型概述

[!include [banner](../includes/banner.md)]

本文定义与产品配置模型有关的术语和概念。 可通过产品配置模型构建可用于为单个产品配置大量产品变型的通用产品结构。

创建产品配置模型是为了表示一般产品结构。 设置产品配置模型后，您可以配置具有唯一物料清单 (BOM) 和唯一工艺路线的独特产品变型。 产品模型配置使用陈述性约束和强制性计算来处理不同产品变型之间的关系和限制。 您可以配置销售订单、销售报价单、采购订单和生产订单上的物料。 下表描述表基于约束的词语和概念。
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>组件</td>
<td>组件是产品配置模型的主要构造块。 组件显示在<strong>基于约束的产品配置模型详细信息</strong>页上的一个树状结构中。 组件可以包含以下元素：
<ul>
<li>属性</li>
<li>约束</li>
<li>计算</li>
<li>子组件</li>
<li>用户要求</li>
<li>物料清单行</li>
<li>工艺路线工序</li>
</ul></td>
</tr>
<tr class="even">
<td>属性</td>
<td>属性描述产品配置模型的所有功能。 您可以使用属性指定配置不同产品时可选择的功能。 属性用于约束和条件中。 创建属性并将其添加到产品配置模型时，将引用相关属性类型。 可为属性设置默认值。 配置产品配置模型时，配置用户界面 (UI) 中使用了默认值。 您可以将属性指定为必需、只读或隐藏。
<ul>
<li><strong>必需</strong> – 配置产品时必须为属性设置一个值。</li>
<li><strong>只读</strong> – 属性值在配置会话期间显示，但是无法更改。</li>
<li><strong>隐藏</strong> – 属性值包括在约束和条件中，但是配置会话期间不显示。</li>
</ul>
您还可以为属性指定条件。 如果满足该条件，则必须为必需属性输入一个值。 条件是必须要满足的表达式，以便将属性、物料清单行和工艺路线工序包括在产品配置模型中。 条件中引用的任何属性都是必需的。 我们建议您在<strong>属性</strong>选项卡上将属性选为必需。这样可以更轻松地标识必需属性。 属性值是重用配置的重要环节。 系统使用属性值以确定是否存在匹配用户在配置会话期间所做选择的配置。</td>
</tr>
<tr class="odd">
<td>属性类型</td>
<td>属性类型为用于产品配置模型的属性指定一组数据类型。 使用了以下属性类型：
<ul>
<li><strong>整数</strong>，具有或不具有范围</li>
<li><strong>小数</strong></li>
<li><strong>文本</strong>，具有或不具有固定列表</li>
<li><strong>布尔值</strong></li>
</ul>
如果属性类型为<strong>布尔值</strong>、具有范围的<strong>整数</strong>或具有固定列表的<strong>文本</strong>，则在设置产品配置模型时，该组值会可用。 <strong>注意：</strong>产品配置求解器仅识别下列属性类型：<strong>布尔值</strong>、具有固定列表的<strong>文本</strong>和具有范围的<strong>整数</strong>。 因此，只有这些属性类型可用于表达式约束和条件。</td>
</tr>
<tr class="even">
<td>约束</td>
<td>约束描述产品配置模型的限制。 约束用于确保配置产品时仅选择了有效值。 约束可以是表达式约束，也可以是表约束：
<ul>
<li>表达式约束仅用于与它们相关联的组件。 组件的表达式约束可以引用组件的子组件的属性。 产品配置求解器用于求解约束，并且编写约束时您必须使用求解器语法。 有关详细信息，请参阅有关表达式约束和表约束的文章链接。</li>
<li>必须定义表约束，然后才能将其应用到产品配置模型中的组件。 表约束可以是用户定义的，也可以是系统定义的。 用户定义的表约束是一种可用于描述属性类型所定义的一组属性值组合的矩阵。 例如，如果生产扬声器，则用户定义的表约束的矩阵可能包含针对扬声器表面处理和格栅的列。</li>
</ul>
<strong>示例</strong>扬声器有四种表面处理：黑色、橡木、红木和白色。 扬声器可以具有三个前格栅之一：黑色、金属或白色。 黑色表面处理对所有格栅可用，但是其他表面处理仅限于特定格栅。 下表显示在<strong>编辑表约束</strong>页上的<strong>允许的组合</strong>选项卡中显示的信息的示例。
<table>
<thead>
<tr class="header">
<th>机柜表面处理</th>
<th>前格栅</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>黑</td>
<td>黑</td>
</tr>
<tr class="even">
<td>黑</td>
<td>金属</td>
</tr>
<tr class="odd">
<td>黑</td>
<td>白色</td>
</tr>
<tr class="even">
<td>橡木</td>
<td>黑</td>
</tr>
<tr class="odd">
<td>红木</td>
<td>白色</td>
</tr>
<tr class="even">
<td>白色</td>
<td>黑</td>
</tr>
<tr class="odd">
<td>白色</td>
<td>白色</td>
</tr>
</tbody>
</table>
系统定义的表约束表示 Supply Chain Management 表中属性类型与字段之间的映射。 系统定义的表约束将属性类型与字段动态链接。 链接能让产品配置模型中的属性反映 Supply Chain Management 表中的字段的数据。</td>
</tr>
<tr class="odd">
<td>计算</td>
<td>计算表示对约束的补充。 您可以使用计算对<strong>小数</strong>和<strong>整数</strong>类型的属性执行算术运算，或执行涉及具有固定列表的<strong>文本</strong>和<strong>布尔值</strong>类型的属性的逻辑运算。 计算具有一个目标属性，可用于保留计算表达式的结果。 计算表达式是使用表达式编辑器构建的。</td>
</tr>
<tr class="even">
<td>子组件</td>
<td>子组件反映产品配置模型的树状结构。 您可以使用子组件构造产品配置模型的结构。 子组件将引用现有组件。 因此，子组件将促进在多个产品配置模型中重复使用组件。 在子组件的<strong>物料清单行详细信息</strong>页上，您可以为子组件选择不同的值。 或者，您可以选择设置产品配置模型时为其选择了值的属性。 若要将产品包括为组件或子组件，您必须在创建产品时在<strong>创建产品</strong>页上指定以下内容：
<ul>
<li>在<strong>产品类型</strong>字段中，选择<strong>物料</strong>。</li>
<li>在<strong>产品子类型</strong>字段中，选择<strong>基础产品</strong>。</li>
<li>在<strong>配置技术</strong>字段中，选择<strong>基于约束的配置</strong>。</li>
</ul>
您可以查看已发布产品是否可用作<strong>已发布产品详细信息</strong>页的<strong>常规</strong>选项卡上的组件或子组件。 如果<strong>基于约束的配置</strong>在<strong>配置技术</strong>字段中被选定，则产品可以用作组件或子组件。 您可以隐藏子组件，以便配置会话期间不会向用户显示。 与子组件关联的属性、子组件和用户要求也是隐藏的。</td>
</tr>
<tr class="odd">
<td>用户要求</td>
<td>用户要求表示用户要求与特定组件和属性之间的抽象。 您不能将用户要求映射到物料。 例如，客户要购买家庭影院系统。 销售代表可以询问客户计划将系统安装所在的房间的大小，以便确定需要多少瓦特。 在此示例中，房间大小可以是用户要求，它可以帮助确定特定组件的合适属性值。 您可以隐藏用户要求，以便配置会话期间不会向用户显示。 与用户要求关联的属性、子组件和用户要求也是隐藏的。 您可以编写条件。以便控制用户要求是否可以处于隐藏状态。 您必须使用优化建模语言 (OML) 语法编写条件。</td>
</tr>
<tr class="even">
<td>物料清单行</td>
<td>物料清单行表示产品配置模型中组件的各个物料。 在<strong>物料清单行详细信息</strong>页上，所有物料都可供选择。 可以将条件添加到物料清单行，以便根据设置产品配置模型时的用户选择，为不同产品变型选择的物料清单行可以有所不同。 条件是必须要满足的表达式，以便将属性、物料清单行和工艺路线工序包括在产品配置模型中。 在<strong>物料清单行详细信息</strong>页上，您可以选择一个不同的值。 或者，您可以映射到设置产品配置模型时为其选择了值的属性。</td>
</tr>
<tr class="odd">
<td>工艺路线工序</td>
<td>在<strong>工艺路线工序详细信息</strong>页上，您可以选择一个不同的值。 或者，您可以映射到设置产品配置模型时为其选择了值的属性。 已编写条件，如表达式约束。 条件是必须要满足的表达式，以便将属性、物料清单行和工艺路线工序包括在产品配置模型中。</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]