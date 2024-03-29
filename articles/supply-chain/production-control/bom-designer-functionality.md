---
title: 物料清单设计器功能
description: 本文介绍如何使用物料清单设计器页设计和使用物料清单 (BOM) 的树状结构。
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerSetup, BOMDesignerFilterDialog, BOMDesignerBOMVersion, BOMChangeLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2fda2b1d835afdcf06a50528748861fecc6792f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844198"
---
# <a name="bom-designer-functionality"></a>物料清单设计器功能

[!include [banner](../includes/banner.md)]

本文介绍如何使用物料清单设计器页设计和使用物料清单 (BOM) 的树状结构。 您可以单击“设置”选择不同的配置并指定要在树的行上显示哪些信息。

从 **已发布产品** 页打开 **物料清单设计器** 页后，后者将显示对所选物料有效且针对所选物料进行了审核的物料清单 (BOM) 的层次结构、物料的默认订单站点和实际日期。  

单击 **筛选器** 以更改视图中的初始选择。 通过将显示原则设置为 **选定/有效或选定**，您可以选择要在视图中使用的单个物料清单和工艺路线版本。 您可以选择要在物料清单设计器中显示或维护的尚未审核和无效的物料清单版本。  

**注意：** 如果您从 **物料清单** 列表页打开了物料清单设计器，该设计器不会显示工艺路线信息。 当前，物料清单或工艺路线版本的选择是物料清单和工艺路线版本的属性，适用于物料清单设计器的所有实例。  

以下各节将介绍物料清单设计器的各个选项卡上可用的功能。

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>使用物料清单设计器分析物料清单结构
物料清单设计器有两个部分：

-   物料清单结构的树视图。
-   详细信息部分中，显示所选数据的详细信息。 当您选择树视图中的节点时，详细信息部分中的 FastTabs 将基于该节点进行更新：
    -   **物料清单行详细信息** - 显示在树视图中选择的物料清单行的详细信息。
    -   **物料数据** - 显示在所选节点中使用的主要物料的详细信息。 您可以单击 **编辑已发布产品** 以维护所选物料。
    -   **物料清单** - 显示与所选节点相关的物料清单的标题。
    -   **工艺路线** - 显示与所选节点相关的工艺路线的标题。
    -   **工艺路线工序** -显示工艺路线的工序的预览。 当物料清单行分配给所选的特定工序后，该工序将标记为 **工序中需要的组件**。

## <a name="selecting-a-bom-and-route"></a>选择物料清单和工艺路线
为物料清单和工艺路线应用的筛选器将显示在物料清单设计器的标题中。 您可以使用 **筛选器** 对话框更改筛选器。 下表描述了此对话框中的字段。

<table>
<thead>
<tr class="header">
<th>字段</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>产品维度</td>
<td>如果选中的成品是基础产品，您可以定义主要选择的可用产品维度。 <strong>注意：</strong>如果您为其打开物料清单设计器的产品不是基础产品，则在<strong>筛选器</strong>对话框中无法选择产品维度。</td>
</tr>
<tr class="even">
<td>站点</td>
<td>更改为其显示物料清单树的站点。 默认站点是成品的默认库存值。</td>
</tr>
<tr class="odd">
<td>显示原则</td>
<td>选择应用于当前物料清单结构和当前工艺路线的版本显示原则：
<ul>
<li>当该原则设置为<strong>有效或选定/有效</strong>时，将找到此日期的有效物料清单或工艺路线版本。</li>
<li>当该原则设置为<strong>选定/有效或选定</strong>时，您可以通过单击<strong>物料清单</strong> &gt; <strong>物料清单版本</strong>或<strong>工艺路线</strong> &gt; <strong>工艺路线版本</strong>来选择物料清单版本或工艺路线版本。</li>
</ul></td>
</tr>
<tr class="even">
<td>版本日期</td>
<td>输入用于物料清单和工艺路线的版本日期。 该版本用于标识要在特定日期（由物料清单版本设置中的版本日期确定）使用的物料清单版本。</td>
</tr>
<tr class="odd">
<td>起始数量</td>
<td>通过选择特定起始数量来筛选版本。 如果您设置了一个值，则可以选择不同的物料清单和工艺路线版本。</td>
</tr>
<tr class="even">
<td>仅显示有效项</td>
<td>当您选中此复选框时，树结构将仅显示具有有效日期的物料清单行。 右键单击或双击物料清单行以打开<strong>编辑物料清单行</strong>页，您可以在其中查看该物料清单行的生效日期。</td>
</tr>
</tbody>
</table>

当您使用物料清单设计器审查或编辑包括一个或多个虚拟级别的物料清单时，与顶级物料关联的工艺路线通常涵盖整个物料清单层次结构。 要简化概览，您可以通过单击 **视图** &gt; **锁定工艺路线** 来锁定显示屏中的顶级工艺路线。 要解锁工艺路线，请单击 **视图** &gt; **解锁工艺路线**。

## <a name="adding-and-editing-boms-and-bom-lines"></a>添加和编辑物料清单和物料清单行
使用 **物料清单行** 或 **物料清单** 功能修改物料清单行或物料清单。 当您选择树中的某个节点时，该节点的类型将决定可用的功能。

| 职能                            | 说明                                                                                               | 节点类型和条件                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 物料清单行 &gt; 编辑                 | 打开可在其中编辑物料清单行属性的对话框。                                             | 当选择了物料清单行节点时，此功能可用。                                                                                                                                                                                                                                   |
| 物料清单行 &gt; 删除               | 从所选物料清单中删除物料清单行。                                                                  | 当选择了物料清单行节点且未锁定物料清单的编辑功能时，此功能可用。                                                                                                                                                                                             |
| 物料清单行 &gt; 在行前添加      | 打开一个对话框，您可在其中选择要包含在所选物料清单行前面的产品变型。         | 当选择了物料清单行节点时，此功能可用。                                                                                                                                                                                                                                   |
| 物料清单行 &gt; 添加到组件物料清单 | 打开一个对话框，您可在其中选择要包含在所选物料清单末尾的产品变型。       | 当所选节点具有选定的物料清单时，此字段可用。 如果此功能不可用，物料清单版本可能缺少选定的物料变型。 在这种情况下，您可以单击 **物料清单** &gt; **创建版本** 以便为所选节点创建缺少的版本。 |
| 物料清单行 &gt; 在行后添加       | 打开一个对话框，您可在其中选择要包含在所选物料清单行后面的产品变型。          | 当选择了物料清单行节点时，此功能可用。                                                                                                                                                                                                                                   |
| 物料清单 &gt; 创建版本             | 为所选节点的产品变型创建新的物料清单版本或物料清单。                             | 当选择的物料清单行节点链接到生产类型为 **物料清单** 或 **配方** 的物料时，此功能可用。                                                                                                                                                  |
| 物料清单 &gt; 计算                | 打开一个对话框，您可以在其中为所选产品变型执行成本或销售价格计算。 | 当所选节点与物料清单版本相关时，此字段可用。                                                                                                                                                                                                         |
| 物料清单 &gt; 检查                      | 验证并检查所选物料清单。                                                                      | 当所选节点与物料清单版本相关时，此字段可用。                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>配置树视图
单击 **设置** 以自定义在物料清单设计器的树视图中显示的信息。

| 字段组 | 描述                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 物料清单         | 使用该复选框可选择在树结构中显示的条件。 物料清单设计器将在两个选项卡的底部显示所选条件。 |
| 路线       | 使用该复选框可选择对工艺路线显示的条件。                                                                                    |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]