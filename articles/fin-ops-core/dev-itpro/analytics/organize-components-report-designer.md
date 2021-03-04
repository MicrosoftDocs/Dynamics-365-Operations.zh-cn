---
title: 整理报表设计器中的报表组件
description: 在您设计构建基块并生成报表后，组织这些对象以便用户更容易地找到它们，这种方法非常有用。 本文介绍了如何组织现有报表、构建基块和报表设计器中的对象。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 58525da35eb9e9376cb5793ad6c6fa45b9de42e6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685803"
---
# <a name="organize-report-components-in-report-designer"></a>整理报表设计器中的报表组件

[!include [banner](../includes/banner.md)]

在您设计构建基块并生成报表后，组织这些对象以便用户更容易地找到它们，这种方法非常有用。 本文介绍了如何组织现有报表、构建基块和报表设计器中的对象。

您可以在报表设计器中重命名文件夹、报表、构建基块和其他对象以帮助整理您的文件。 根据重命名的对象的类型，您可能必须更新与该对象的关联。

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>在报表设计器中重命名文件夹或构建基块
在报表设计器中，你可以重命名文件夹、报表定义、行定义、列定义和报告树定义。

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>在报表设计器中重命名文件夹或构建基块

1. 在报表设计器中，使用导航窗格找到要重命名的文件夹或对象。
2. 右键单击该文件夹或对象，然后单击 **重命名**。 导航窗格中的 **名称** 字段将变为可用。
3. 键入新名称，然后按 Enter。
4. 如果构建基块是行定义、列定义或报告结构树定义，则必须更新与其关联的其他构建基块。 右键单击在步骤 3 中重命名的构建基块，选择 **关联**，然后选择列表中的某个项目以更新它。
5. 重复步骤 4，直到所有关联项目都已更新。

## <a name="create-and-manage-report-groups"></a>创建和管理报表组
您可以对报表定义进行分组以同时生成多个报表。 要创建、修改、删除和生成报表组，您必须具有设计人员或管理员角色。 具有生成人员角色的用户可生成报表组，还可修改为报告组设置的用户报表定义。

### <a name="create-a-report-group"></a>创建报表组

1. 在报表设计器中，单击导航窗格中的 **报表组**。
2. 在 **文件** 菜单上，单击 **新建** &gt; **报表组定义** 在查看器窗口中打开一个新报告组。 或者，单击工具栏上的 **报表组** 按钮 ![报表组](media/report-group.gif "报表组")。
3. 单击 **报表组** 选项卡。要覆盖用于生成此报表的各个报表定义的相关信息，请选中 **覆盖各个报表定义中的公司、详细信息和日期设置** 复选框。 公司名称、详细级别、临时设置和日期信息将自动输入，但您仍可以进行更新。
4. 如果要生成显示申报币种的多个报表，请选中 **包含所有申报币种** 复选框。 然后您可以通过在查看报表时单击 Web 查看器上的 **币种** 按钮来访问多个视图。
5. 在 **组中的报表** 字段中，单击 **添加** 以选择要包含在报表组中的报表。 要在 **添加** 对话框中选择多个报表，请在按住 Ctrl 键的同时选择报表。 完成选择报告后，单击 **确定**。
6. 单击 **文件** &gt; **保存** 以保存新报表组。

### <a name="modify-a-report-group"></a>修改报表组

1. 在报表设计器中，单击导航窗格中的 **报表组**。
2. 双击要修改的报表组。
3. 在 **报表组** 选项卡上，进行所需的更改。
4. 在 **文件** 菜单中，单击 **保存** 保存修改过的报表组，或者单击工具栏中的 **保存** 按钮 ![保存](media/save.gif "保存")。

> [注意] 如果您已计划了报表以便它们以设置的间隔生成，则可以覆盖这些设置并立即生成报表。

### <a name="generate-a-report-group-report"></a>生成报表组报表

1. 在报表设计器中，单击导航窗格中的 **报表组**。
2. 打开要生成的报表组。
3. 单击 **生成报表** 按钮 ![生成报表](media/generate-report.gif "生成报表")以生成报表。

### <a name="delete-a-report-group"></a>删除报表组

1. 在报表设计器中，单击导航窗格中的 **报表组**。
2. 右键单击要删除的报表组，然后选择 **删除**。
3. 当出现一条确认消息时，请单击 **是**。

## <a name="report-group-tab-controls"></a>“报表组”选项卡控件
下表描述 **报表组** 选项卡的控件。

<table>
<thead>
<tr>
<th>控件</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr>
<td>覆盖各个报表定义中的公司、详细信息和日期设置</td>
<td>选中此复选框可覆盖此报表组中的报表的各个报表定义（仅用于生成这些报表）。</td>
</tr>
<tr>
<td>公司名称</td>
<td>选择要用于报表的公司。</td>
</tr>
<tr>
<td>详细程度</td>
<td>指定报表中包含的详细信息级别。
<ul>
<li><strong>财务</strong>− 高级别的摘要报表。 您无法深化到科目和维度（通过报告结构树添加的帐户和维度除外）。</li>
<li><strong>财务 &amp; 科目</strong> - 包含高度概括性汇总和科目详细信息的报表。</li>
<li><strong>财务、科目 &amp; 交易记录</strong> - 包含高度概括性汇总和交易记录详细信息的报表。</li>
</ul></td>
</tr>
<tr>
<td>临时信息</td>
<td>指定报表中包含的活动的类型。
<ul>
<li><strong>仅限过帐活动</strong> − 仅包括财务数据中已过帐的交易记录和余额。</li>
<li><strong>已过帐和未过帐的活动</strong> − 包括财务数据中输入的和已过帐的所有交易记录和余额。</li>
<li><strong>仅限未过帐活动</strong> − 仅包括财务数据中已输入但尚未过帐的交易记录。</li>
</ul></td>
</tr>
<tr>
<td>包括所有申报币种</td>
<td>在 Microsoft Dynamics ERP 系统中配置的所有其他申报币种均在此处列出。 选择此复选框以生成使用指定的币种的其他报表。 若要在 Web 查看器中查看这些报表，请单击<strong>币种</strong>，然后选择一种货币。</td>
</tr>
<tr>
<td>不与报表定义一起保存的日期信息</td>
<td><ul>
<li>基准期间</li>
<li>基准年</li>
<li>覆盖的期间</li>
</ul>
只有默认基准期间设置与报表定义一起保存。</td>
</tr>
<tr>
<td>与报表定义一起保存的日期信息</td>
<td><ul>
<li>报表日期</li>
<li>默认基准期间</li>
</ul></td>
</tr>
<tr>
<td>组中的报表</td>
<td>添加、删除和重新排序报表组中的报表。
<ul>
<li>若要将报表定义添加到报表组，请双击该报表组以将其打开，然后单击<strong>添加</strong>。 选择要包含在报表组中的报表，然后单击<strong>确定</strong>。</li>
<li>若要从报表组删除报表，选中该报表，然后单击<strong>删除</strong>。</li>
<li>要修改生成报表的顺序，请在列表中选择一个报表，然后单击<strong>上移</strong>或<strong>下移</strong>。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>其他资源

[财务报告](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]