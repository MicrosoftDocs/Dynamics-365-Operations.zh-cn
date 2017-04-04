---
title: "产品配置模型中的表达式约束和表约束"
description: "本主题介绍的是表达式约束和表约束的使用。 约束控制的对象是您在配置销售订单、销售报价单、采购订单或生产订单的产品时您可以选择的属性值。 您可以根据自己喜欢的构建约束方式来选择使用表达式约束或表约束。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1fe8a0d90a3f707fa7b0fea0310c819ce5040a42
ms.lasthandoff: 03/30/2017


---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>产品配置模型中的表达式约束和表约束

本主题介绍的是表达式约束和表约束的使用。 约束控制的对象是您在配置销售订单、销售报价单、采购订单或生产订单的产品时您可以选择的属性值。 您可以根据自己喜欢的构建约束方式来选择使用表达式约束或表约束。 

约束用于控制您在配置销售订单、销售报价单、采购订单或生产订单的产品时可以选择的属性值。 您可以根据自己喜欢的构建约束方式来选择使用表达式约束或表约束。

## <a name="what-are-expression-constraints"></a>什么是表达式约束？
表达式约束的特性是使用算术和布尔运算符和函数的表达式。 表达式约束是为产品配置模型中的特定组件而写的。 它不能为其他组件重用或共享。 但是，组件的表达式约束可以引用组件的子组件的特性。

## <a name="what-are-table-constraints"></a>什么是表约束？
约束表列出了在配置产品时允许属性值的组合。 表约束定义可以被广泛使用。 当您为产品配置模型中的组件创建一个表约束时，您要选择一个表约束定义。 若要创建合理的组合，您要给组件添加特定类型的属性。 每个属性类型具有一个特定值。

### <a name="example-of-a-table-constraint"></a>表约束示例

此示例显示如何如何将扬声器的配置限制到特定的机柜表面处理和格栅。 第一个表显示通常可用于配置的机柜表面处理和格栅。 **值。内阁完成** **和前格栅**属性类型定义。

| 属性类型 | 值                      |
|----------------|-----------------------------|
| 机柜表面处理 | 黑色、橡木、红木、白色 |
| 前格栅    | 黑色、金属、白色         |

下一个表显示由“颜色和表面处理”****表约束定义的组合。 通过使用此表约束，您可以配置具有橡木表面处理和黑色格栅的扬声器、具有红木表面处理和白色格栅的扬声器，等等。

| 完成         | 格栅                       |
|----------------|-----------------------------|
| 橡木            | 黑色                       |
| 红木       | 白色                       |
| 白色          | 黑色                       |
| 白色          | 白色                       |
| 黑色          | 黑色                       |
| 黑          | 金属                       | 

您可以创建系统定义的表约束和用户定义的表约束 有关详细信息，请参阅[系统定义的和用户定义的表约束](system-defined-user-defined-table-constraints.md)。

## <a name="what-syntax-should-be-used-to-write-constraints"></a>什么语法应将写入约束？
编写约束时，必须使用优化建模语言 (OML) 语法。 系统使用 Microsoft 难题解人基础约束解难题人解决约束。

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>我应该使用表约束还是表达式约束？
您可以使用表达式约束或表约束，具体取决于您喜欢生成约束的方式。 您建立的表约束为一个矩阵表，而表达式约束则是单个报表。 在您配置产品时，可以随意使用约束条件。 以下示例显示两种方法有何不同。  

当您使用以下设置约束配置产品时，这些组合是允许的：

-   颜色为黑色、大小为 30 或 50 的产品
-   颜色为红色、大小为 20 的产品

### <a name="table-constraint-setup"></a>表约束设置

| 颜色 | 大小 |
|-------|------|
| 黑 | 30   |
| 黑 | 50   |
| 红色   | 20   |

### <a name="expression-constraint-setup"></a>表达式约束设置

(颜色 == “黑色” & (尺寸 == “30” | 尺寸 == “50”)) | (颜色 ==“红色” & 大小 = “20” ）

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>当我编写表达式约束时，我应该使用运算符还是中缀表示法？
您既可以使用运算符又可以使用中缀表示法来编写表达式约束。 对于**“Min”**、**“Max”**和**“Abs”**运算符，您不能使用中缀表示法。 这些运算符作为标准运算符包括在大多数编程语言中。

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>在编写表达式约束时，我可以使用哪些运算符和中缀表示法？
下表列出的是您在产品配置模型中为组件编写表达式约束时，可以使用的运算符和中缀表示法。 第一个表中的示例显示如何使用中缀表示法或运算符编写表达式。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>操作员</th>
<th>描述</th>
<th>语法</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>提示</td>
<td>如果第一个条件为 false，则为 true；第二个条件为 true 或两者都为 true。</td>
<td>提示[a, b]，中缀：a -: b</td>
<td><ul>
<li><strong>运算符：</strong> [暗示 x! = 0，y &gt;] = 0</li>
<li><strong>中缀批注：</strong> ! x- 0 =:y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>并</td>
<td>只有所有条件为 true，则为 true。 如果条件数为 0 （零），则产生 <strong>True</strong>。</td>
<td>和 args []，缀中：b &amp; z… &amp;</td>
<td><ul>
<li><strong>运算符：</strong> [x 和==，y &lt;2] = 2</li>
<li><strong>中缀批注：</strong> == y &lt;x 2 &amp; = 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>或</td>
<td>如有条件为 true，则为 true。 如果条件数为 0 (零)，则产生 <strong>False</strong>。</td>
<td>或 args []，缀中：。_=_窗体_=__=_…z</td>
<td><ul>
<li><strong>运算符：</strong> 或 [2 x ==，y &lt;] = 2</li>
<li><strong>中缀批注：</strong> == x 2_=_y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>加</td>
<td>这将合计其条件。 如果条件数为 0 （零），则产生 <strong>0</strong>。</td>
<td>正 args []，缀中：" + + + z 窗体…</td>
<td><ul>
<li><strong>运算符：</strong>Plus[x, y, 2] == z</li>
<li><strong>中缀表示法：</strong>x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>减</td>
<td>这就否定了此参数。 它必须只有一个条件。</td>
<td>减[expr]，中缀：-expr</td>
<td><ul>
<li><strong>运算符：</strong>Minus[x] == y</li>
<li><strong>中缀表示法：</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>绝对值</td>
<td>取其条件的绝对值。 它必须只有一个条件。</td>
<td>绝对值[expr]</td>
<td><strong>运算符：</strong>Abs[x]</td>
</tr>
<tr class="odd">
<td>时间</td>
<td>取其条件的产物。 如果条件数为 0 （零），则产生 <strong>1</strong>。</td>
<td>时间 args []，缀中：* "窗体* z *…</td>
<td><ul>
<li><strong>运算符：</strong>Times[x, y, 2] == z</li>
<li><strong>中缀表示法：</strong>x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>能力</td>
<td>取指数。 它从右到左求幂。 (换言之，它是权限关联的。) 因此，<strong>高级 []，其余，窗体。</strong> 一定等效 <strong>高级" [，高层级 []，其余] 窗体</strong>的。 只有指数为正常数时才可以使用 <strong>Power</strong>。</td>
<td>高级 args []，缀中：^ b ^… ^ z</td>
<td><ul>
<li><strong>运算符：</strong>Power[x, 2] == y</li>
<li><strong>中缀表示法：</strong>x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>最大值</td>
<td>生成最大条件。 如果条件数为 0 (零)，则生成结果为<strong>“无穷大”</strong>。</td>
<td>最大值[args]</td>
<td><strong>运算符：</strong>Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>最小值</td>
<td>生成最小条件。 如果条件数为 0 (零)，则生成结果为<strong>“无穷大”</strong>。</td>
<td>最小值[args]</td>
<td><strong>运算符：</strong>Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>不</td>
<td>生成其条件的相反逻辑。 它必须只有一个条件。</td>
<td>非[expr]，中缀：!expr</td>
<td><ul>
<li><strong>运算符：</strong> 未 x [] &amp; 不 [y == 3]</li>
<li><strong>中缀表示法：</strong>!x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

下表示例显示的是如何编写中缀表示法。

| 中缀表示法    | 说明                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| x + y + z         | 增加额                                                                                      |
| x \* y \* z       | 乘                                                                                |
| x - y             | 二进制减法的转换方式与第二个数为负的二进制加法相同。 |
| x ^ y ^ z         | 具有右关联的求幂                                                   |
| ! x                | 布尔值“非”。                                                                                   |
| x -:y            | 布尔值影响                                                                           |
|  x | y | z         | 布尔值“或”                                                                                    |
| & y x 和 z         | 布尔值“与”                                                                                   |
| x == y == z       | 等式                                                                                      |
| ! x! y == z       | 明确的                                                                                      |
| x &lt; y &lt; z   | 小于                                                                                     |
| x &gt; y &gt; z   | 大于                                                                                  |
| x &lt;= y &lt;= z | 小于等于                                                                         |
| x &gt;= y &gt;= z | 大于等于                                                                      |
| (x)               | 括号覆盖默认优先级顺序。                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>为什么我的表达式约束验证为错误？
您不能使用预留的关键字作为产品配置模型中的属性、组件或子组件的求解器名称。 这是不能预留使用的关键字的列表：

-   上限
-   分项指标
-   相等
-   场地
-   如果
-   小于
-   大于
-   提示
-   日志
-   最大
-   最小值
-   减
-   加
-   功率
-   时间
-   时隙
-   型号
-   决策
-   目标


<a name="see-also"></a>请参阅
--------

[创建表达式约束 (任务指南)](http://ax.help.dynamics.com/en/wiki/create-an-expression-constraint/)

[请一个计算添加到配置产品模型 (任务指南)](http://ax.help.dynamics.com/en/wiki/add-a-calculation-to-a-product-configuration-model/)


