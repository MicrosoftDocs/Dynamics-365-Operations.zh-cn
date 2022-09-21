---
title: 检查配置的 ER 组件以防止运行时问题
description: 本文说明如何检查配置的电子报告 (ER) 组件，以防止可能发生的运行时问题。
author: kfend
ms.date: 09/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 1ca59d6c26dbcf065adb952409da30002d951f62
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476846"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>检查配置的 ER 组件以防止运行时问题

[!include[banner](../includes/banner.md)]

配置的每个[电子申报 (ER)](general-electronic-reporting.md) [格式](er-overview-components.md#format-components-for-outgoing-electronic-documents)和[模型映射](er-overview-components.md#model-mapping-component)组件都可以在设计时[验证](er-fillable-excel.md#validate-an-er-format)。 在此验证期间，将运行一致性检查以帮助防止可能发生的运行时问题，例如执行错误和性能降级。 对于发现的每个问题，检查都会提供问题元素的路径。 对于某些问题，可以使用自动修复。

默认情况下，在以下情况下，将自动对包含先前提到的 ER 组件的 ER 配置应用验证：

- [导入](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) ER 配置的一个新版本到您的 Microsoft Dynamics 365 Finance 实例中。
- 将可编辑 ER 配置的状态从 **草稿** 更改为 **已完成**。
- 通过应用新的基础版本[重定](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)可编辑 ER 配置。

您可以显式运行此验证。 选择以下三个选项之一，然后按照提供的步骤操作：

- 选项 1：

    1. 转到 **组织管理 \> 电子申报 \> 配置**。
    2. 在左窗格的配置树中，选择包含 ER 格式或 ER 模型映射组件的所需 ER 配置。
    3. 在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。
    4. 在操作窗格上，选择 **验证**。

- 选项 2，对于 ER 格式：

    1. 转到 **组织管理 \> 电子申报 \> 配置**。
    2. 在左窗格的配置树中，选择包含 ER 格式组件的所需 ER 配置。
    3. 在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。
    4. 在操作窗格上，选择 **设计器**。
    5. 在 **格式设计器** 页的操作窗格上，选择 **验证**。

- 选项 3，对于 ER 模型映射：

    1. 转到 **组织管理 \> 电子申报 \> 配置**。
    2. 在左窗格的配置树中，选择包含 ER 模型映射组件的所需 ER 配置。
    3. 在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。
    4. 在操作窗格上，选择 **设计器**。
    5. 在 **模型到数据源映射** 页面的操作窗格中，选择 **设计器**。
    6. 在 **模型映射设计器** 页面的操作窗格中，选择 **验证**。

若要在导入配置时跳过验证，请执行以下步骤。

1. 转到 **组织管理 \> 电子申报 \> 配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 将 **导入后验证配置** 选项设置为 **否**。

要在更改或重定版本状态时跳过验证，请按照下列步骤操作。

1. 转到 **组织管理 \> 电子申报 \> 配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 将 **配置状态更改时跳过验证并重定基本值** 选项设置为 **是**。

ER 使用以下类别为一致性检查检验分组：

- **可执行性** – 用于检测运行时可能发生的严重问题的检查。 这些问题大多数为 **错误** 级。 
- **性能** – 用于检测可能导致执行配置的 ER 组件不完整的检查。 这些问题大多数为 **警告** 级。
- **数据完整性** – 用于检测可能导致数据丢失或运行时问题的问题的检查。 这些问题大多数为 **警告** 级。

## <a name="list-of-inspections"></a>检查列表

下表提供 ER 提供的检查的概览。 有关这些检查的详细信息，请使用第一列中的链接转到本文的相关章节。 这些部分介绍了 ER 提供的组件针对的组件类型，以及如何重新配置 ER 组件以帮助防止问题。

<table>
<thead>
<tr>
<th>姓名</th>
<th>类别</th>
<th>等级</th>
<th>消息</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>类型转换</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>不能将类型为 &lt;type&gt; 的表达式转换为类型为 &lt;type&gt; 的字段。</p>
<p><b>运行时错误：</b>类型异常</p>
</td>
</tr>
<tr>
<td><a href='#i2'>类型兼容性</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>配置的表达式不能用作当前格式元素到数据源的绑定，因为此表达式返回的数据类型 &lt;type&gt; 的值超出了类型为 &lt;type&gt; 的当前格式元素支持的数据类型范围。</p>
<p><b>运行时错误：</b>类型异常</p>
</td>
</tr>
<tr>
<td><a href='#i3'>缺少配置元素</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>未找到路径 &lt;path&gt;。</p>
<p><b>运行时错误：</b>未找到配置元素 &lt;path&gt;</p>
</td>
</tr>
<tr>
<td><a href='#i4'>带 FILTER 函数的表达式的可执行性</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>FILTER 函数的列表表达式无法查询。</p>
<p><b>运行时错误：</b>不支持筛选。 验证配置以获得有关此问题的更多详细信息。</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>GROUPBY 数据源的可执行性</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>路径 &lt;path&gt; 不支持查询。</td>
</tr>
<tr>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>不能使用查询执行按函数分组。</p>
<p><b>运行时错误</b>：不能使用查询执行按函数分组。</p>
</td>
</tr>
<tr>
<td><a href='#i6'>JOIN 数据源的可执行性</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>不能在查询中联接不是筛选器的列表 &lt;path&gt;。</p>
<p><b>运行时错误：</b>函数联接的数据源应该是错误调用的筛选表达式计算字段。</p>
</td>
</tr>
<tr>
<td><a href='#i7'>FILTER 与 WHERE 函数的偏好对比</a></td>
<td>绩效</td>
<td>警告</td>
<td>从性能的角度来看，相比 WHERE，更倾向于对表达式使用 FILTER 函数。 选择“修复”以自动替换它。</td>
</tr>
<tr>
<td><a href='#i8'>ALLITEMSQUERY 相比 ALLITEMS 函数的偏好对比</a></td>
<td>绩效</td>
<td>警告</td>
<td>从性能的角度来看，相比 ALLITEMS，更倾向于对表达式使用 ALLITEMSQUERY 函数。 选择“修复”以自动替换它。</td>
</tr>
<tr>
<td><a href='#i9'>空列表用例的注意事项</a></td>
<td>可执行性</td>
<td>警告</td>
<td>
<p>列表 &lt;path&gt; 不检查空列表用例，因此会在运行时生成错误。 请为空列表用例添加检查。</p>
<p><b>运行时错误：</b>&lt;path&gt; 处列表为空</p>
<p><b><a href='#i9a'>潜在问题</a>：</b>行填充一次，而填充来源数据源中则包含多个记录</p>
</td>
</tr>
<tr>
<td><a href='#i10'>带 FILTER 函数的表达式的可执行性（高速缓存）</a></td>
<td>可执行性</td>
<td>错误​</td>
<td>
<p>FILTER 函数不能应用于所选类型的数据源。 仅当未高速缓存且无手动添加的嵌套数据源时，Table 记录类型的数据源才适用。</p>
<p><b>运行时错误：</b>不支持筛选。 验证配置以获得有关此问题的更多详细信息。</p>
</td>
</tr>
<tr>
<td><a href='#i11'>缺少绑定</a></td>
<td>可执行性</td>
<td>警告</td>
<td>
<p>路径 &lt;path&gt;在使用模型的映射时没有到任何数据源的绑定。</p>
<p><b>运行时错误：</b>未绑定路径 &lt;path&gt;</p>
</td>
</tr>
<tr>
<td><a href='#i12'>未链接模板</a></td>
<td>数据完整性</td>
<td>警告</td>
<td>文件 &lt;name&gt; 未链接到任何文件组件，因此将在更改了配置版本状态后被移除。</td>
</tr>
<tr>
<td><a href='#i13'>不同步格式</a></td>
<td>数据完整性</td>
<td>警告</td>
<td>Excel 工作表 &lt;sheet name&gt; 中无定义的名称 &lt;component name&gt;</td>
</tr>
<tr>
<td><a href='#i14'>不同步格式</a></td>
<td>数据完整性</td>
<td>警告</td>
<td>
<p>Word 模板文件中不存在 &lt;标记的 Word 内容控件&gt; 标记</p>
<p><b>运行时错误：</b>Word 模板文件中不存在 &lt;标记的 Word 内容控件&gt; 标记。</p>
</td>
</tr>
<tr>
<td><a href='#i15'>没有默认映射</a></td>
<td>数据完整性</td>
<td>错误​</td>
<td>
<p>&lt;逗号分隔的配置名称&gt; 配置中的 &lt;模型名称（根描述符）&gt; 数据模型存在多个模型映射。 将其中一个配置设置为默认配置</p>
<p><b>运行时错误：</b>&lt;逗号分隔的配置名称&gt; 配置中的 &lt;模型名称（根描述符）&gt; 数据模型存在多个模型映射。 将其中一个配置设置为默认配置。</p>
</td>
</tr>
<tr>
<td><a href='#i16'>页眉或页脚组件的设置不一致</a></td>
<td>数据完整性</td>
<td>错误​</td>
<td>
<p>页眉/页脚（&lt;组件类型：页眉或页脚&gt;）不一致</p>
<p><b>运行时：</b>如果执行了已配置的 ER 格式的草稿版本，则会在运行时使用最后配置的组件。</p>
</td>
</tr>
<tr>
<td><a href='#i17'>页面组件的设置不一致</a></td>
<td>数据完整性</td>
<td>错误​</td>
<td>有两个以上没有复制的范围组件。 请删除不必要的组件。</td>
</tr>
<tr>
<td><a href='#i18'>带 ORDERBY 函数的表达式的可执行性</a></td>
<td>可执行性</td>
<td>错误</td>
<td>
<p>ORDERBY 函数的列表表达式无法查询。</p>
<p><b>运行时错误：</b>不支持排序。 验证配置以获得有关此问题的更多详细信息。</p>
</td>
</tr>
<tr>
<td><a href='#i19'>过时的应用程序项目</a></td>
<td>数据完整性</td>
<td>警告</td>
<td>
<p>元素 &lt;路径&gt; 被标为过时元素。<br>或<br>元素 &lt;路径&gt; 被标为过时元素，并显示消息 &lt;消息文本&gt;。</p>
<p><b>运行时错误示例：</b>未找到类“&lt;路径&gt;”。</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>类型转换

ER 检查数据模型字段的数据类型是否与配置为该字段的绑定的表达式的数据类型兼容。 如果数据类型不兼容，将在 ER 模型映射设计器中会发生验证错误。 您收到的消息指出 ER 无法将 A 类型的表达式转换为 B 类型的字段。

以下步骤显示可能会如何发生此问题。

1. 开始同时配置 ER 数据模型和 ER 模型映射组件。
2. 在数据模型树中，添加一个名为 **X** 的字段，然后选择 **整数** 作为数据类型。

    ![已添加到“数据模型”页面上的数据模型树的 X 字段和整数数据类型。](./media/er-components-inspections-01.png)

3. 在模型映射设计器内的 **数据源** 窗格中，添加一个 **计算字段** 类型的数据源。
4. 将新数据源命名为 **Y**，然后对其进行配置，以使其包含表达式 `INTVALUE(100)`。
5. 将 **X** 绑定到 **Y**。
6. 在数据模型设计器中，将 **X** 字段的数据类型从 **整数** 更改为 **Int64**。
7. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。

    ![验证模型映射设计器页面上的可编辑模型映射组件。](./media/er-components-inspections-01.gif)

8. 选择 **验证** 检查 **配置** 页上所选 ER 配置的模型映射组件。

    ![检查“配置”页面上的模型映射组件。](./media/er-components-inspections-01a.png)

9. 请注意，发生了验证错误。 消息说明 **Y** 数据源的 `INTVALUE(100)` 表达式返回的 **整数** 类型的值不能存储在 **Int64** 类型的 **X** 数据模型字段中。

下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。

![“格式设计器”页面上的运行时错误。](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过更改数据模型字段的数据类型更新数据模型结构，使其与为该字段的绑定配置的表达式的数据类型相匹配。 对于前面的示例，**X** 字段的数据类型必须更改回 **整数**。

#### <a name="option-2"></a>选项 2

通过更改与数据模型字段绑定的数据源的表达式更新模型映射。 对于前面的示例，**Y** 数据源的表达式必须更改为 `INT64VALUE(100)`。

## <a name="type-compatibility"></a><a id="i2"></a>类型兼容性

ER 检查格式元素的数据类型是否与配置为该格式元素的绑定的表达式的数据类型兼容。 如果数据类型不兼容，将在 ER Operations 设计器中会发生验证错误。 收到的消息表示配置的表达式不能用作当前格式元素到数据源的绑定，因为此表达式返回的数据类型 A 的值超出了类型为 B 的当前格式元素支持的数据类型范围。

以下步骤显示可能会如何发生此问题。

1. 开始同时配置 ER 数据模型和 ER 格式组件。
2. 在数据模型树中，添加一个名为 **X** 的字段，然后选择 **整数** 作为数据类型。
3. 在格式结构树中，添加 **数值** 类型的格式元素。
4. 将新格式元素命名为 **Y**。在 **数值类型** 字段中，为数据类型选择 **整数**。
5. 将 **X** 绑定到 **Y**。
6. 在格式结构树中，将 **Y** 格式元素的数据类型从 **整数** 更改为 **Int64**。
7. 选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。

    ![在“格式设计器”页面上验证类型兼容性。](./media/er-components-inspections-02.gif)

8. 请注意，发生了验证错误。 该消息指出配置的表达式只能接受 **Int64** 值。 因此，不能在 **Y** 格式元素中输入类型为 **整数** 的 **X** 数据模型字段值。

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过更改 **数值** 格式元素的数据类型更新数据模型结构，使其与为该元素的绑定配置的表达式的数据类型相匹配。 在前面的示例中， **X** 格式元素的 **数值类型** 值必须更改回 **整数**。

#### <a name="option-2"></a>选项 2

通过将表达式从 `model.X` 更改为 `INT64VALUE(model.X)`，更新 **X** 格式元素的格式映射。

## <a name="missing-configuration-element"></a><a id="i3"></a>缺少配置元素

ER 检查绑定表达式中是否仅包含在可编辑 ER 组件中配置的数据源。 对于每个包含可编辑 ER 组件中缺少的数据源的绑定，将在 ER Operations 设计器或 ER 模型映射设计器中发生验证错误。

以下步骤显示可能会如何发生此问题。

1. 开始同时配置 ER 数据模型和 ER 模型映射组件。
2. 在数据模型树中，添加一个名为 **X** 的字段，然后选择 **整数** 作为数据类型。

    ![“数据模型”页面上包含 X 字段和整数数据类型的数据模型树。](./media/er-components-inspections-01.png)

3. 在模型映射设计器内的 **数据源** 窗格中，添加一个 **计算字段** 类型的数据源。
4. 将新数据源命名为 **Y**，然后对其进行配置，以使其包含表达式 `INTVALUE(100)`。
5. 将 **X** 绑定到 **Y**。
6. 在模型映射设计器的 **数据源** 窗格中，删除 **Y** 数据源。
7. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。

    ![检查模型映射设计器页面上的可编辑 ER 模型映射组件。](./media/er-components-inspections-03.gif)

8. 请注意，发生了验证错误。 该消息指出，**X** 数据模型字段的绑定中包含引用 **Y** 数据源的路径，但找不到此数据源。

### <a name="automatic-resolution"></a>自动解决

选择 **取消绑定** 通过删除缺少的数据源绑定自动解决此问题。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

取消绑定 **X** 数据模型字段以停止引用不存在的 **Y** 数据源。

#### <a name="option-2"></a>选项 2

在模型映射设计器的 **数据源** 窗格中，再次添加 **Y** 数据源。

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>带 FILTER 函数的表达式的可执行性

内置的 [FILTER](er-functions-list-filter.md) ER 函数用于通过下达一个 SQL 调用以访问应用程序表、视图或数据实体来获取记录列表形式的所需数据。 **记录列表** 类型的数据源用作此函数的参数，并指定调用的应用程序源。 ER 检查是否可以为 `FILTER` 函数中引用的数据源建立直接 SQL 查询。 如果无法建立直接查询，ER 模型映射设计器中会发生验证错误。 您收到的消息指出在运行时不能运行其中包含 `FILTER` 函数的 ER 表达式。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
4. 添加一个类型为 **计算字段** 的数据源。
5. 将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum="US-101")`。
6. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询 **Vendor** 数据源中的 `FILTER(Vendor, Vendor.AccountNum="US-101")` 表达式。
7. 通过向裁剪后的供应商帐号添加 **计算字段** 类型的嵌套字段，修改 **Vendor** 数据源。
8. 将这个新的嵌套字段命名为 **$AccNumber**，然后对其进行配置，以使其包含表达式 `TRIM(Vendor.AccountNum)`。
9. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询 **Vendor** 数据源中的 `FILTER(Vendor, Vendor.AccountNum="US-101")` 表达式。

    ![验证是否可以在“模型映射设计器”页面上查询具有 FILTER 函数的表达式。](./media/er-components-inspections-04.gif)

10. 请注意，发生了验证错误，因为 **Vendor** 数据源中包含一个类型为 **计算字段** 的嵌套字段，并且该嵌套字段不允许将 **FilteredVendor** 数据源的表达式转换为直接 SQL 语句。

下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。

![在“格式设计器”页面上运行可编辑格式时发生的运行时错误。](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

不是向 **Vendor** 数据源添加类型为 **计算字段** 的嵌套字段，而是将 **$AccNumber** 嵌套字段添加到 **FilteredVendor** 数据源，并进行配置，以使其包含表达式 `TRIM(FilteredVendor.AccountNum)`。 这样，`FILTER(Vendor, Vendor.AccountNum="US-101")` 表达式就可以在 SQL 级运行，之后再计算 **$ AccNumber** 嵌套字段。

#### <a name="option-2"></a>选项 2

将 **FilteredVendor** 数据源的表达式从 `FILTER(Vendor, Vendor.AccountNum="US-101")` 更改为 `WHERE(Vendor, Vendor.AccountNum="US-101")`。 建议不要更改包含大量数据的表（事务表）的表达式，因为将提取所有记录，并且将在内存中选择所需的记录。 因此，这种方法可能会导致性能低下。 有关详细信息，请参阅 [WHERE ER 函数](er-functions-list-where.md)。

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>GROUPBY 数据源的可执行性

**GROUPBY** 数据源将查询结果拆分为多组记录，通常是为了对各组执行一项或多项聚合。 可以配置每个 **GROUPBY** 数据源，以使其在数据库级或在内存中运行。 如果配置了 **GROUPBY** 数据源以使其在数据库级运行，ER 将检查是否可建立对该数据源中引用的数据源的直接 SQL 查询。 如果无法建立直接查询，ER 模型映射设计器中会发生验证错误。 您收到的消息指出，运行时不能运行配置的 **GROUPBY** 数据源。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Trans**。在 **表** 字段中，选择 **VendTrans** 指定该数据源将请求 VendTrans 表。
4. 添加一个类型为 **分组依据** 的数据源。
5. 将新数据源命名为 **GroupedTrans**，然后按照下面的方法配置：

    - 选择 **Trans** 数据源作为应分组的记录的来源。
    - 在 **执行位置** 字段中，选择 **查询** 以指定要在数据库级运行此数据源。

    ![在编辑“分组依据”参数页面上配置数据源。](./media/er-components-inspections-05a.gif)

6. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **GroupedTrans** 数据源。
7. 通过向裁剪后的供应商帐号添加 **计算字段** 类型的嵌套字段，修改 **Trans** 数据源。
8. 将新数据源命名为 **$AccNumber**，然后对其进行配置，以使其包含表达式 `TRIM(Trans.AccountNum)`。

    ![在“模型映射设计器”页面上配置数据源。](./media/er-components-inspections-05a.png)

9. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **GroupedTrans** 数据源。

    ![验证 ER 模型映射组件，并验证是否可在“模型映射设计器”页面上查询 GroupedTrans 数据源。](./media/er-components-inspections-05b.png)

10. 请注意，发生了验证错误，因为 **Trans** 数据源中包含一个类型为 **计算字段** 的嵌套字段，并且该嵌套字段不允许调用要转换为直接 SQL 语句的 **GroupedTrans** 数据源。

下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。

![在“格式设计器”页面上忽略警告时发生的运行时错误。](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

不是向 **Trans** 数据源添加类型为 **计算字段** 的嵌套字段，而是为 **GroupedTrans** 数据源的 **GroupedTrans.lines** 项添加 **$AccNumber** 嵌套字段，并进行配置，以使其包含表达式 `TRIM(GroupedTrans.lines.AccountNum)`。 这样，**GroupedTrans** 数据源就可以在 SQL 级运行，之后再计算 **$ AccNumber** 嵌套字段。

#### <a name="option-2"></a>选项 2

将 **GroupedTrans** 数据源的 **执行位置** 字段值从 **查询** 更改为 **在内存中**。 建议不要更改包含大量数据的表（事务表）的值，因为将提取所有记录，并且将在内存中执行分组和聚合。 因此，这种方法可能会导致性能低下。

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>JOIN 数据源的可执行性

[JOIN](er-join-data-sources.md) 数据源根据相关字段合并两个或更多数据库表中的记录。 可以配置每个 **JOIN** 数据源，以使其在数据库级或在内存中运行。 如果配置了 **JOIN** 数据源以使其在数据库级运行，ER 将检查是否可建立对该数据源中引用的数据源的直接 SQL 查询。 如果无法使用至少一个引用数据源建立直接 SQL 查询，ER 模型映射设计器中会发生验证错误。 您收到的消息指出，运行时不能运行配置的 **JOIN** 数据源。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
4. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
5. 将新数据源命名为 **Trans**。在 **表** 字段中，选择 **VendTrans** 指定该数据源将请求 VendTrans 表。
6. 添加一个 **计算字段** 类型的数据源作为 **Vendor** 数据源的嵌套字段。
7. 将新数据源命名为 **FilteredTrans**，然后对其进行配置，以使其包含表达式 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`。
8. 添加一个类型为 **联接** 的数据源。
9. 将新数据源命名为 **JoinedList**，然后按照下面的方法配置：

    1. 将 **Vendor** 数据源作为要联接的第一组记录添加。
    2. 将 **Vendor.FilteredTrans** 数据源作为要联接的第二组记录添加。 选择 **INNER** 作为类型。
    3. 在 **执行** 字段中，选择 **查询** 以指定要在数据库级运行此数据源。

    ![在“联接设计器”页面上配置数据源。](./media/er-components-inspections-06a.gif)

10. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **JoinedList** 数据源。
11. 将 **Vendor.FilteredTrans** 数据源的表达式从 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` 更改为 `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`。
12. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **JoinedList** 数据源。

    ![验证可编辑模型映射组件，然后在“模型映射设计器”页面上验证是否可查询 JoinedList 数据源。](./media/er-components-inspections-06b.png)

13. 请注意，发生了验证错误，因为 **Vendor.FilteredTrans** 数据源无法转换为直接 SQL 调用。 此外，直接 SQL 调用不允许调用要转换为直接 SQL 语句的 **JoinedList** 数据源。

    ![在“模型映射设计器”页面上验证 JoinedList 数据源失败导致的运行时错误。](./media/er-components-inspections-06c.png)

下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。

![在“格式设计器”页面上运行可编辑格式。](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

按照警告的建议，将 **Vendor.FilteredTrans** 数据源的表达式从 `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` 更改为 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`。

![“模型映射设计器”页面上更新后的数据源表达式。](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>选项 2

将 **JoinedList** 数据源的 **执行位置** 字段值从 **查询** 更改为 **在内存中**。 建议不要更改包含大量数据的表（事务表）的值，因为将提取所有记录，并且将在内存中发生联接。 因此，这种方法可能会导致性能低下。 将显示验证警告，以便告知您此风险。

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>FILTER 与 WHERE 函数的偏好对比

内置的 [FILTER](er-functions-list-filter.md) ER 函数用于通过下达一个 SQL 调用以访问应用程序表、视图或数据实体来获取记录列表形式的所需数据。 [WHERE](er-functions-list-where.md) 函数从给定源获取所有记录，然后在内存中选择记录。 **记录列表** 类型的数据源用作这两个函数的参数，并指定源以获取记录。 ER 检查是否可以为 **WHERE** 函数中引用的数据源建立直接 SQL 调用。 如果无法建立直接调用，ER 模型映射设计器中会发生验证警告。 您收到的消息建议您使用 **FILTER** 函数而不是 **WHERE** 函数来帮助提高效率。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Trans**。在 **表** 字段中，选择 **VendTrans** 指定该数据源将请求 VendTrans 表。
4. 添加一个 **计算字段** 类型的数据源作为 **Vendor** 数据源的嵌套字段。
5. 将新数据源命名为 **FilteredTrans**，然后对其进行配置，以使其包含表达式 `WHERE(Trans, Trans.AccountNum="US-101")`。
6. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
7. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
8. 添加一个类型为 **计算字段** 的数据源。
9. 将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `WHERE(Vendor, Vendor.AccountNum="US-101")`。
10. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。

    ![检查模型映射设计器页面上的可编辑模型映射组件。](./media/er-components-inspections-07a.png)

11. 请注意，验证警告建议对 **FilteredVendor** 和 **FilteredTrans** 数据源使用 **FILTER** 函数，而不是 **WHERE** 函数。

    ![建议在“模型映射设计器”页面上使用 FILTER 函数，而不是 WHERE 函数。](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>自动解决

选择 **修复** 以将 **WHERE** 函数替换为这种检查的 **警告** 选项卡上网格中显示的所有数据源的表达式中的 **FILTER** 函数。

或者，您可以在网格中选择单个警告的行，然后选择 **修复所选**。 在这种情况下，仅在所选警告中提到的数据源中自动更改表达式。

![选择“修复”以在“模型映射设计器”页面上将 WHERE 函数自动替换为 FILTER 函数。](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>手动解决

可以通过将 **WHERE** 函数替换为 **FILTER** 函数，手动调整验证网格中所有数据源的表达式。

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>ALLITEMSQUERY 相比 ALLITEMS 函数的偏好对比

内置的 [ALLITEMS](er-functions-list-allitems.md) 和 [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER 函数返回一个平展 **记录列表** 值，该值由表示与指定路径匹配的所有项的记录的列表构成。 ER 检查是否可以为 **ALLITEMS** 函数中引用的数据源建立直接 SQL 调用。 如果无法建立直接调用，ER 模型映射设计器中会发生验证警告。 您收到的消息建议您使用 **ALLITEMSQUERY** 函数而不是 **ALLITEMS** 函数来帮助提高效率。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
4. 添加一个类型为 **计算字段** 的数据源，以便获取多个供应商的记录。
5. 将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`。
6. 添加一个类型为 **计算字段** 的数据源，以便获取筛选后的所有供应商的交易。
7. 将新数据源命名为 **FilteredVendorTrans**，然后对其进行配置，以使其包含表达式 `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`。
8. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。

    ![检查“模型映射设计器”页面上的可编辑模型映射组件。](./media/er-components-inspections-08a.png)

9. 请注意，发生了验证警告。 此消息建议为 **FilteredVendorTrans** 数据源使用 **ALLITEMSQUERY** 函数，而不是 **ALLITEMS** 函数。

    ![建议在“模型映射设计器”页面上使用 ALLITEMSQUERY 函数，而不是 ALLITEMS 函数。](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>自动解决

选择 **修复** 以将 **ALLITEMS** 函数替换为这种检查的 **警告** 选项卡上网格中显示的所有数据源的表达式中的 **ALLITEMSQUERY** 函数。

或者，您可以在网格中选择单个警告的行，然后选择 **修复所选**。 在这种情况下，仅在所选警告中提到的数据源中自动更改表达式。

![在“模型映射设计器”页面上选择“修复所选”。](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>手动解决

可以通过将 **ALLITEMS** 函数替换为 **ALLITEMSQUERY** 函数，手动调整验证网格中提及的所有数据源的表达式。

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>空列表用例的注意事项

可以配置 ER 格式或模型映射组件以获取类型为 **记录列表** 的数据源的字段值。 ER 将检查您的设计是否考虑以下方案：调用的数据源中不包含任何记录（即为空），以防从不存在的记录获取值时发生运行时错误。

以下步骤显示可能会如何发生此问题。

1. 开始同时配置 ER 数据模型、ER 模型映射和 ER 格式组件。
2. 在数据模型树中，添加一个名称为 **Root3** 的根项。
3. 通过添加一个类型为 **记录列表** 的嵌套项，修改 **Root3** 项。
4. 将这个新的嵌套项命名为 **Vendor**。
5. 按照以下方法修改 **Vendor** 项：

    - 添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **Name**。
    - 添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **AccountNumber**。

    ![在“数据模型”页面上添加嵌套字段。](./media/er-components-inspections-09a.png)

6. 在模型映射设计器内的 **数据源** 窗格中，添加一个 **Dynamics 365 for Operations \\ 表记录** 类型的数据源。
7. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
8. 添加一个类型为 **常规 \\ 用户输入参数** 的数据源，以便在运行时对话框中搜索供应商帐户。
9. 将新数据源命名为 **RequestedAccountNum**。 在 **标签** 字段中，输入 **供应商帐号**。 在 **Operations 数据类型名称** 字段中，保留默认值 **描述**。
10. 添加一个类型为 **计算字段** 的数据源，以便筛选查询的供应商。
11. 将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`。
12. 按照以下方法将数据模型项绑定到配置的数据源：

    - 将 **FilteredVendor** 绑定到 **Vendor**。
    - 将 **FilteredVendor.AccountNum** 绑定到 **Vendor.AccountNumber**。
    - 将 **FilteredVendor.'name()'** 绑定到 **Vendor.Name**。

    ![在“模型映射设计器”页面上绑定数据模型项。](./media/er-components-inspections-09b.png)

13. 在格式结构树中，添加以下项，以便生成一个 XML 格式且包含供应商详细信息的传出文档：

    1. 添加 **Statement** 根 XML 元素。
    2. 为 **Statement** XML 元素添加嵌套的 **Party** XML 元素。
    3. 为 **Party** XML 元素添加以下嵌套的 XML 属性：

        - 姓名
        - AccountNum

14. 按照以下方法将格式元素绑定到提供的数据源：

    - 将 **Statement\\Party\\Name** 格式元素绑定到 **model.Vendor.Name** 数据源字段。
    - 将 **Statement\\Party\\AccountNum** 格式元素绑定到 **model.Vendor.AccountNumber** 数据源字段。

15. 选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。

    ![在“格式设计器”页面上验证绑定到数据源的格式元素。](./media/er-components-inspections-09c.png)

16. 请注意，发生了验证错误。 此消息表示，如果 `model.Vendor` 列表为空，在运行时可能为配置的 **Statement\\Party\\Name** 和 **Statement\\Party\\AccountNum** 格式组件引发错误。

    ![有关配置的格式组件的潜在错误的验证错误。](./media/er-components-inspections-09d.png)

下图显示了如果忽略此警告，选择 **运行** 以运行格式，然后选择不存在的供应商的帐号，将出现的运行时错误。 因为请求的供应商不存在，`model.Vendor` 列表将为空（即，其中将不包含任何记录）。

![格式映射运行期间发生的运行时错误。](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>自动解决

对于 **警告** 选项卡上网格中的所选行，可以选择 **取消绑定**。 将从格式元素中自动删除 **路径** 列中指向的绑定。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

您可以将 **Statement\\Party\\Name** 格式元素绑定到 `model.Vendor` 数据源项。 在运行时，此绑定首先调用 `model.Vendor` 数据源。 当 `model.Vendor` 返回空记录列表时，将不运行嵌套的格式元素。 因此，此格式配置不发生验证警告。

![在“格式设计器”页面上将格式元素绑定到数据源项。](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>选项 2

将 **Statement\\Party\\Name** 格式元素的绑定从 `model.Vendor.Name` 更改为 `FIRSTORNULL(model.Vendor).Name`。 更新后的绑定将有条件地把类型为 **记录列表** 的 `model.Vendor` 数据源的第一个记录转换为类型为 **记录** 的新数据源。 这个新数据源中包含同一组字段。

- 如果 `model.Vendor` 数据源中至少有一个记录，则将使用 `model.Vendor` 数据源的第一个记录的字段的值填充该记录的字段。 在这种情况下，更新后的绑定将返回供应商名称。
- 否则，将使用创建的记录的每个字段的数据类型默认值填充这些字段。 在此情况下，返回的 **字符串** 数据类型默认值为空白字符串。

因此，绑定到 `FIRSTORNULL(model.Vendor).Name` 表达式时，**Statement\\Party\\Name** 格式元素不会发生验证警告。

![更改后的绑定解决了“格式设计器”页面上的验证警告。](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>选项 3

如果要显式指定当类型为 **记录列表** 的 `model.Vendor` 数据源中不包含任何记录时在生成的文档中输入的数据（此示例中为文本 **不可用**），请将 **Statement\\Party\\Name** 格式元素的绑定从 `model.Vendor.Name` 更改为 `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`。 也可以使用表达式 `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`。

### <a name="additional-consideration"></a><a id="i9a"></a>其他注意事项

此检查还会向您警示另一个潜在问题。 默认情况下，在将 **Statement\\Party\\Name** 和 **Statement\\Party\\AccountNum** 格式元素绑定到类型为 **记录列表** 的 `model.Vendor` 数据源的相应字段时，这些绑定将运行，并采用 `model.Vendor` 数据源第一个记录的相应字段（如果该列表非空）。

因为尚未将 **Statement\\Party** 格式元素与 `model.Vendor` 数据源绑定，因此在格式执行期间将不针对 `model.Vendor` 数据源的每个记录迭代 **Statement\\Party** 元素。 相反，如果记录列表中包含多个记录，则仅使用该列表的第一个记录中的信息填充生成的文档。 因此，如果该格式用于使用有关 `model.Vendor` 数据源中的所有供应商的信息填充生成的文档，可能会出错。 若要解决此问题，请将 **Statement\\Party** 元素与 `model.Vendor` 数据源绑定。

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>带 FILTER 函数的表达式的可执行性（高速缓存）

多个内置 ER 函数（包括 [FILTER](er-functions-list-filter.md) 和 [ALLITEMSQUERY](er-functions-list-allitemsquery.md)）用于通过下达一个 SQL 调用以访问应用程序表、视图或数据实体来获取记录列表形式的所需数据。 **记录列表** 类型的数据源用作这些函数中每一个的参数，并指定调用的应用程序源。 ER 检查是否可以为这些函数之一中引用的数据源建立直接 SQL 调用。 如果因为数据源标记成了[已高速缓存](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)导致无法建立直接调用，ER 模型映射设计器中会发生验证错误。 您收到的消息指出在运行时不能运行其中包含这些函数之一的 ER 表达式。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
4. 添加一个类型为 **常规 \\ 用户输入参数** 的数据源，以便在运行时对话框中搜索供应商帐户。
5. 将新数据源命名为 **RequestedAccountNum**。 在 **标签** 字段中，输入 **供应商帐号**。 在 **Operations 数据类型名称** 字段中，保留默认值 **描述**。
6. 添加一个类型为 **计算字段** 的数据源，以便筛选查询的供应商。
7. 将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`。
8. 将配置的 **Vendor** 数据源标记为已高速缓存。

    ![在“模型映射设计器”页面上配置模型映射组件。](./media/er-components-inspections-10a.gif)

9. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。

    ![在“模型映射设计器”页面上验证应用于高速缓存供应商数据源的 FILTER 函数。](./media/er-components-inspections-10a.png)

10. 请注意，发生了验证错误。 该消息指出不能将 **FILTER** 函数应用于高速缓存的 **Vendor** 数据源。

下图显示了如果忽略此警告并选择 **运行** 以运行格式，将出现的运行时错误。

![在“格式设计器”页面上运行格式映射期间发生的运行时错误。](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

删除 **Vendor** 数据源中的 **Cache** 标志。 然后，**FilteredVendor** 数据源将变为可执行，但是每次调用 **FilteredVendor** 数据源时，都将访问 VendTable 表中引用的 **Vendor** 数据源。

#### <a name="option-2"></a>选项 2

将 **FilteredVendor** 数据源的表达式从 `FILTER(Vendor, Vendor.AccountNum="US-101")` 更改为 `WHERE(Vendor, Vendor.AccountNum="US-101")`。 在此情况下，仅在首次调用 **Vendor** 数据源时，才能访问 VendTable 表中引用的 **Vendor** 数据源。 但是，将在内存中选择记录。 因此，这种方法可能会导致性能低下。

## <a name="missing-binding"></a><a id="i11"></a>缺少绑定

当您配置 ER 格式组件时，基本 ER 数据模型将作为 ER 格式的默认数据源提供。 运行配置的 ER 格式时，将使用基本模型的[默认模型映射](er-country-dependent-model-mapping.md)使用应用程序数据填充数据模型。 如果您将格式元素绑定到未绑定到当前作为可编辑格式的默认模型映射选择的模型映射中的任何数据源的数据模型项，ER 格式设计器将显示警告。 运行时不能运行这种绑定，因为运行的格式不能使用应用程序数据填充绑定的元素。 因此，在运行时会发生错误。

以下步骤显示可能会如何发生此问题。

1. 开始同时配置 ER 数据模型、ER 模型映射和 ER 格式组件。
2. 在数据模型树中，添加一个名称为 **Root3** 的根项。
3. 通过添加一个类型为 **记录列表** 的新嵌套项，修改 **Root3** 项。
4. 将这个新的嵌套项命名为 **Vendor**。
5. 按照以下方法修改 **Vendor** 项：

    - 添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **Name**。
    - 添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **AccountNumber**。

    ![在“数据模型”页面上向供应商项添加嵌套字段。](./media/er-components-inspections-11a.png)

6. 在模型映射设计器内的 **数据源** 窗格中，添加一个 **Dynamics 365 for Operations \\ 表记录** 类型的数据源。
7. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。
8. 添加一个类型为 **常规 \\ 用户输入参数** 的数据源，以便在运行时对话框中查询供应商帐户。
9. 将新数据源命名为 **RequestedAccountNum**。 在 **标签** 字段中，输入 **供应商帐号**。 在 **Operations 数据类型名称** 字段中，保留默认值 **描述**。
10. 添加一个类型为 **计算字段** 的数据源，以便筛选查询的供应商。
11. 将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`。
12. 按照以下方法将数据模型项绑定到配置的数据源：

    - 将 **FilteredVendor** 绑定到 **Vendor**。
    - 将 **FilteredVendor.AccountNum** 绑定到 **Vendor.AccountNumber**。

    > [!NOTE]
    > **Vendor.Name** 数据模型字段保持未绑定。

    ![绑定到配置的数据源的数据模型项，以及在“模型映射设计器”页面上取消绑定的数据模型项。](./media/er-components-inspections-11b.png)

13. 在格式结构树中，添加以下项，以便生成一个 XML 格式且包含查询的供应商的详细信息的传出文档：

    1. 添加 **Statement** 根 XML 元素。
    2. 为 **Statement** XML 元素添加嵌套的 **Party** XML 元素。
    3. 为 **Party** XML 元素添加以下嵌套的 XML 属性：

        - 姓名
        - AccountNum

14. 按照以下方法将格式元素绑定到提供的数据源：

    - 将 **Statement\\Party** 格式元素绑定到 `model.Vendor` 数据源项。
    - 将 **Statement\\Party\\Name** 格式元素绑定到 **model.Vendor.Name** 数据源字段。
    - 将 **Statement\\Party\\AccountNum** 格式元素绑定到 **model.Vendor.AccountNumber** 数据源字段。

15. 选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。

    ![在“格式设计器”页面上验证 ER 格式组件。](./media/er-components-inspections-11c.png)

16. 请注意，发生了验证警告。 此消息指出 **model.Vendor.Name** 数据源字段未绑定到模型映射中配置供格式使用的任何数据源。 因此，在运行时不能填充 **Statement\\Party\\Name** 格式，并且可能会发生运行时异常。

    ![在“格式设计器”页面上验证 ER 格式元素。](./media/er-components-inspections-11d.png)

下图显示了如果忽略此警告并选择 **运行** 以运行格式，将出现的运行时错误。

![在“格式设计器”页面上运行可编辑格式。](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过为 **model.Vendor.Name** 数据源字段添加绑定来修改配置的模型映射。

#### <a name="option-2"></a>选项 2

通过删除 **Statement\\Party\\Name** 格式元素的绑定修改配置的格式。

## <a name="not-linked-template"></a><a id="i12"></a>未链接模板

在 [手动](er-fillable-excel.md#manual-entry)配置 ER 格式组件以使用模板生成传出文档时，必须手动添加 **Excel\\File** 元素，作为可编辑组件的附件添加所需模板，并在添加的 **Excel\\File** 元素中选择该附件。 这样，您指示添加的元素将在运行时填充所选模板。 在配置状态为 **草稿** 的格式组件版本时，可以向可编辑组件添加多个模板，然后在 **Excel\\文件** 元素中选择每个模板以运行 ER 格式。 这样，您可以看到在运行时如何填充不同的模板。 如果有模板未在任何 **Excel\\File** 元素中选中，ER 格式设计器将警告您，当模板的状态从 **草稿** 更改为 **已完成** 时，将从可编辑 ER 格式组件版本删除这些模板。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 格式组件。
2. 在格式结构树中，添加 **Excel\\File** 元素。
3. 为您刚才添加的 **Excel\\File** 元素添加一个 Excel 工作簿文件 **A.xlsx** 作为附件。 使用 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中配置的文档类型指定 ER 格式模板的存储。
4. 为 **Excel\\File** 元素再添加一个 Excel 工作簿文件 **B.xlsx** 作为附件。 使用用于工作簿文件A 的同一种文档类型。
5. 在 **Excel\\File** 元素中，选择工作簿文件 A。
6. 选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。

    ![在“格式设计器”页面上验证工作簿文件的可编辑格式组件。](./media/er-components-inspections-12a.gif)

7. 请注意，发生了验证警告。 该消息指出工作簿文件 B.xlsx 未链接到任何组件，并且将在更改配置版本状态后将其删除。

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

通过删除所有未链接到任何 **Excel\\File** 元素的所有模板来修改配置的格式。

## <a name="not-synced-format"></a><a id="i13"></a>不同步格式

在 [配置](er-fillable-excel.md) ER 格式组件以使用 Excel 模板生成传出文档时，可以手动添加 **Excel\\File** 元素，作为可编辑组件的附件添加所需模板，并在添加的 **Excel\\File** 元素中选择该附件。 这样，您指示添加的元素将在运行时填充所选模板。 由于添加的 Excel 模板是外部设计的，因此可编辑的 ER 格式中可能包含添加的模板中缺少的 Excel 名称。 ER 格式设计器会警告您有关引用添加的 Excel 模板中不包含的名称的 ER 格式元素的属性之间的任何不一致之处。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 格式组件。
2. 在格式结构树中，添加 **Excel\\File** 元素 **Report**。
3. 为您刚才添加的 **Excel\\File** 元素添加一个 Excel 工作簿文件 **A.xlsx** 作为附件。 使用 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中配置的文档类型指定 ER 格式模板的存储。

    > [!IMPORTANT]
    > 确保添加的 Excel 工作簿中不包含名称 **ReportTitle**。

4. 将 **Excel\\Cell** 元素 **Title** 作为 **Report** 元素的嵌套元素添加。 在 **Excel 范围** 字段中，输入 **ReportTitle**。
5. 选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。

    ![在“格式设计器”页面上验证嵌套元素和字段。](./media/er-components-inspections-13a.png)

6. 请注意，发生了验证警告。 此消息指出您正在使用的 Excel 模板的工作表 **Sheet1** 中无名称 **ReportTitle**。

    ![有关 Excel 模板的 Sheet1 中无名称 ReportTitle 的验证警告。](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过删除引用模板中缺少的 Excel 名称的所有元素来修改配置的格式。

#### <a name="option-2"></a>选项 2

通过导入 Excel 模板[更新](er-fillable-excel.md#template-import)可编辑 ER 格式。 将与导入的 Excel 模板的结构[同步](modify-electronic-reporting-format-reapply-excel-template.md)可编辑 ER 格式的结构。

### <a name="additional-consideration"></a>其他注意事项

要了解如何在[业务文档管理](er-business-document-management.md)的模板编辑器中将格式结构与 ER 模板同步，请参阅[更新业务文档模板的结构](er-bdm-update-structure.md)。

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>未与 Word 模板格式同步

在 [配置](er-fillable-excel.md) ER 格式组件以使用 Word 模板生成传出文档时，可以手动添加 **Excel\\File** 元素，作为可编辑组件的附件添加所需 Word 模板，并在添加的 **Excel\\File** 元素中选择该附件。

> [!NOTE]
> 附加 Word 文档后，ER 格式设计器将可编辑元素显示为 **Word\\File**。

这样，您指示添加的元素将在运行时填充所选模板。 由于添加的 Word 模板是外部设计的，因此可编辑的 ER 格式中可能包含添加的模板中缺少的 Word 内容控件引用。 ER 格式设计器会警告您有关引用添加的 Excel 模板中不包含的内容控件的 ER 格式元素的属性之间的任何不一致之处。

有关显示此问题可能如何发生的示例，请参见[配置可编辑格式以禁止显示摘要部分](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control)。

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过从格式元素中删除验证警告中提到的 **已移除** 公式来修改配置的格式。

#### <a name="option-2"></a>选项 2

修改使用的 Word 模板，方法是向相关 Word 内容控件[添加](er-design-configuration-word-suppress-controls.md#tag-control)必需的标记。

## <a name="no-default-mapping"></a><a id="i15"></a>没有默认映射

当[缺少绑定](#i11)检查完成后，将根据相关模型映射组件的绑定来评估检查的格式绑定。 因为你可以导入[一些](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER 模型映射配置到您的 Finance 实例，并且每个配置可能都包含适用的模型映射组件，所以必须选择一个配置作为默认配置。 否则，当您尝试运行、编辑或验证检查的 ER 格式时，将发生异常，并且您将收到以下消息：“\<configuration names separated by comma\> 配置中的 \<model name (root descriptor)\> 数据模型存在多个模型映射。 将其中一个配置设置为默认配置。”

有关显示此问题可能如何发生以及如何解决的示例，请参见[管理单个模型根的多个派生映射](er-multiple-model-mappings.md)。

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>页眉或页脚组件的设置不一致

当你 [配置](er-fillable-excel.md) ER 格式组件以使用 Excel 模板生成出站文档时，您可以添加 **Excel\\页眉** 组件以填充 Excel 工作簿中工作表顶部的页眉。 您也可以添加 **Excel\\页脚** 组件以填充工作表底部的页脚。 对于您添加的每个 **Excel\\页眉** 或者 **Excel\\页脚** 组件，您必须设置 **页眉/页脚外观** 属性，以指定要为其运行组件的页面。 因为你可以为单个 **工作表** 组件配置一些 **Excel\\页眉** 或 **Excel\\页脚** 组件，并且您可以为 Excel 工作表中的不同类型页面生成不同的页眉或页脚，因此必须为 **页眉/页脚外观** 属性的特定值配置单个 **Excel\\页眉** 或 **Excel\\页脚** 组件。 如果为 **页眉/页脚外观** 属性的特定值配置了多个 **Excel\\页眉** 或 **Excel\\页脚** 组件，则会发生验证错误，并且您会收到以下错误消息：“页眉/页脚（&lt;组件类型：页眉或页脚&gt;）不一致。”

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过删除其中一个不一致的 **Excel\\页眉** 或 **Excel\\页脚** 组件来修改配置的格式。

#### <a name="option-2"></a>选项 2

修改其中一个不一致的 **Excel\\页眉** 或 **Excel\\页脚** 组件的 **页眉/页脚外观** 属性值。

## <a name="inconsistent-setting-of-page-component"></a><a id="i17"></a>页面组件的设置不一致

当您 [配置](er-fillable-excel.md)电子报告格式组件来使用Excel 模板生成出站文档时，您可以添加 **Excel\\页面** 组件来使用电子报告公式对生成的文档进行分页。 对于您添加的每个 **Excel\\页面** 组件，您可以添加很多嵌套[范围](er-fillable-excel.md#range-component)组件，并仍然保持以下[结构](er-fillable-excel.md#page-component-structure)：

- 可以配置第一个嵌套 **范围** 组件，以将 **复制方向** 属性设置为 **不复制**。 此范围用于在生成的文档中制作页眉。
- 您可以添加很多其他嵌套 **范围** 组件，将组件的 **复制方向** 属性设置为 **垂直**。 这些范围用于填充生成的文档。
- 可以配置最后一个嵌套 **范围** 组件，以将 **复制方向** 属性设置为 **不复制**。 此范围用于在生成的文档中制作页脚并添加所需的分页符。

如果您在设计时没有在电子报告格式设计器中为电子报告格式采用此结构，将会发生验证错误，您会收到以下错误消息：“有两个以上没有复制的范围组件。 请删除不必要的组件。”

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

通过更改所有不一致的 **Excel\\范围** 组件的 **复制方向** 属性来修改配置的格式。

## <a name="executability-of-an-expression-with-orderby-function"></a><a id="i18"></a>带 ORDERBY 函数的表达式的可执行性

内置 [ORDERBY](er-functions-list-orderby.md) ER 函数用于对指定为函数参数的 **[记录列表](er-formula-supported-data-types-composite.md#record-list)** 类型的 ER 数据源的记录进行排序。

`ORDERBY` 函数的参数可以被[指定](er-functions-list-orderby.md#syntax-2)通过执行单一数据库调用作为记录列表获取排序的数据，来对应用程序表、视图或数据实体的记录进行排序。 **记录列表** 类型的数据源用作此函数的参数，并指定调用的应用程序源。

ER 检查是否可以为 `ORDERBY` 函数中引用的数据源建立直接数据库查询。 如果无法建立直接查询，ER 模型映射设计器中会发生验证错误。 您收到的消息指出在运行时不能运行其中包含 `ORDERBY` 函数的 ER 表达式。

以下步骤显示可能会如何发生此问题。

1. 开始配置 ER 模型映射组件。
2. 添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。
3. 将新数据源命名为 **Vendor**。 在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 **VendTable** 表。
4. 添加一个类型为 **计算字段** 的数据源。
5. 将新数据源命名为 **OrderedVendors**，然后对其进行配置，以使其包含表达式 `ORDERBY("Query", Vendor, Vendor.AccountNum)`。
 
    ![在“模型映射设计器”页面上配置数据源。](./media/er-components-inspections-18-1.png)

6. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询 **OrderedVendors** 数据源中的表达式。
7. 通过向裁剪后的供应商帐号添加 **计算字段** 类型的嵌套字段，修改 **Vendor** 数据源。
8. 将这个新的嵌套字段命名为 **$AccNumber**，然后对其进行配置，以使其包含表达式 `TRIM(Vendor.AccountNum)`。
9. 选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询 **Vendor** 数据源中的表达式。

    ![验证是否可以在“模型映射设计器”页面上查询 Vendor 数据源中的表达式。](./media/er-components-inspections-18-2.png)

10. 请注意，发生了验证错误，因为 **Vendor** 数据源中包含一个类型为 **计算字段** 的嵌套字段，并且该嵌套字段不允许将 **OrderedVendors** 数据源的表达式转换为直接数据库语句。 如果您忽略验证错误并选择 **运行** 运行此模型映射，则会在运行时发生同样的错误。

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

#### <a name="option-1"></a>选项 1

不是向 **Vendor** 数据源添加类型为 **计算字段** 的嵌套字段，而是将 **$AccNumber** 嵌套字段添加到 **FilteredVendors** 数据源，并配置此字段，使其包含表达式 `TRIM(FilteredVendor.AccountNum)`。 这样，`ORDERBY("Query", Vendor, Vendor.AccountNum)` 表达式就可以在数据库级别运行，**$ AccNumber** 嵌套字段可以在以后计算。

#### <a name="option-2"></a>选项 2

将 **FilteredVendors** 数据源的表达式从 `ORDERBY("Query", Vendor, Vendor.AccountNum)` 更改为 `ORDERBY("InMemory", Vendor, Vendor.AccountNum)`。 建议不要更改包含大量数据的表（事务表）的表达式，因为将提取所有记录，并且将在内存中排序所需的记录。 因此，这种方法可能会导致性能低下。

## <a name="obsolete-application-artifact"></a><a id="i19"></a>过时的应用程序项目

在设计 ER 模型映射组件或 ER 格式组件时，可以配置 ER 表达式来调用 ER 中的应用程序项目，如数据库表、类的方法等。在 Finance 版本 10.0.30 及更高版本中，您可以强制 ER 警告您引用的应用程序项目在源代码中被标记为已过时。 此警告可能很有用，因为通常过时的项目最终会从源代码中删除。 获知项目的状态可以在项目被从源代码中删除前防止您在可编辑 ER 组件中使用过时的项目，从而帮助防止在运行时从 ER 组件调用非现有应用程序项目时出错。

在 **功能管理** 工作区中启用 **验证电子报告数据源的过时元素** 功能，以开始在检查可编辑 ER 组件期间评估应用程序项目的过时属性。 目前针对以下类型的应用程序项目评估过时属性：

- 数据库表
    - 表的字段
    - 表的方法
- 应用程序类
    - 类的方法

> [!NOTE]
> 仅当数据源用于此 ER 组件的至少一个绑定时，才会在检查引用过时项目的数据源的可编辑 ER 组件期间出现警告。

> [!TIP]
> 当 [SysObsoleteAttribute](../dev-ref/xpp-attribute-classes.md#sysobsoleteattribute) 类用于通知编译器发出警告消息而不是错误时，检查警告会在设计时在 **模型映射设计器** 或 **格式设计器** 页面的 **详细信息** 快速选项卡上呈现指定的源代码。

下图显示了当 `CompanyInfo` 应用程序表的过时 `DEL_Email` 字段通过使用配置的 `company` 数据源绑定到数据模型字段时出现的验证警告。

![查看模型映射设计器页面“详细信息”快速选项卡中的验证警告。](./media/er-components-inspections-19a.png)

### <a name="automatic-resolution"></a>自动解决

没有用于自动修复此问题的选项。

### <a name="manual-resolution"></a>手动解决

通过删除与引用过时应用程序项目的数据源的所有绑定来修改配置的模型映射或格式。

## <a name="additional-resources"></a>其他资源

[ALLITEMS ER 函数](er-functions-list-allitems.md)

[ALLITEMSQUERY ER 函数](er-functions-list-allitemsquery.md)

[INT64VALUE ER 函数](er-functions-conversion-int64value.md)

[INTVALUE ER 函数](er-functions-conversion-intvalue.md)

[FILTER ER 函数](er-functions-list-filter.md)

[WHERE ER 函数](er-functions-list-where.md)

[在 ER 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据](er-join-data-sources.md)

[跟踪电子申报格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)

[业务文档管理概览](er-business-document-management.md)

[禁止在生成的报告中使用 Word 内容控件](er-design-configuration-word-suppress-controls.md)

[管理单个模型根的多个派生映射](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
