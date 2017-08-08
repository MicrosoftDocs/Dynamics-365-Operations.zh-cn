---
title: "高级筛选和查询语法"
description: "本文介绍当您在“高级筛选/排序”对话框中使用“matches”运算符时可用的筛选和查询选项。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 616366009ce7bf7135704e980becc331617cf5af
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="advanced-filtering-and-query-syntax"></a>高级筛选和查询语法

[!include[banner](../includes/banner.md)]


本文介绍当您在“高级筛选/排序”对话框中使用“matches”运算符时可用的筛选和查询选项。

<a name="advanced-query-syntax"></a>高级查询语法
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>语法</th>
<th>字符描述</th>
<th>说明</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>值</em></td>
<td>等于输入的值</td>
<td>键入要查找的该值。</td>
<td><strong>Smith</strong> 查找 &quot;Smith&quot;。</td>
</tr>
<tr class="even">
<td>!<em>值</em>（感叹号）</td>
<td>不等于输入的值</td>
<td>键入一个惊叹号，然后是要排除的值。</td>
<td><strong>!Smith</strong> 查找除 &quot;Smith&quot; 之外的所有值。</td>
</tr>
<tr class="odd">
<td><em>开始值</em>..<em>结束值</em>（双句点）</td>
<td>用双句点分隔的两个值之间</td>
<td>键入开始值，然后是两个句点，最后键入结束值。</td>
<td><strong>1..10</strong> 查找从 1 到 10 的所有值。 不过，在字符串字段中，<strong>A..C</strong> 将查找以 &quot;A&quot; 开头和以 &quot;B&quot; 开头的所有值以及恰好为 &quot;C&quot; 的值。 例如，此查询不会查找 &quot;Ca&quot;。 若要查找从 &quot;A*&quot; 到 &quot;C*&quot; 的所有值，请键入 <strong>A..D</strong>。</td>
</tr>
<tr class="even">
<td>..<em>值</em>（双句点）</td>
<td>小于或等于输入的值</td>
<td>键入两个句点，然后键入值。</td>
<td><strong>..1000</strong> 查找小于或等于 1000 的任何数字，例如 &quot;100&quot;、&quot;999.95&quot; 和 &quot;1,000&quot;。</td>
</tr>
<tr class="odd">
<td><em>值</em>.. （双句点）</td>
<td>大于或等于输入的值</td>
<td>键入值，然后键入两个句点。</td>
<td><strong>1000..</strong> 查找大于或等于 1000 的任何数字，例如 &quot;1,000&quot;、&quot;1,000.01&quot; 和 &quot;1,000,000&quot;。</td>
</tr>
<tr class="even">
<td>&gt;<em>值</em>（大于符号）</td>
<td>大于输入的值</td>
<td>键入大于符号 (<strong>&gt;</strong>)，然后键入值。</td>
<td><strong>&gt;1000</strong> 查找大于 1000 的任何数字，例如 &quot;1000.01&quot;、&quot;20,000&quot; 和 &quot;1,000,000&quot;。</td>
</tr>
<tr class="odd">
<td>&lt;<em>值</em>（小于符号）</td>
<td>小于输入的值</td>
<td>键入小于符号 (<strong>&lt;</strong>)，然后键入值。</td>
<td><strong>&lt;1000</strong> 查找小于 1000 的任何数字，例如 &quot;999.99&quot;、&quot;1&quot; 和 &quot;-200&quot;。</td>
</tr>
<tr class="even">
<td><em>值</em>*（星号）</td>
<td>以输入的值开头</td>
<td>键入字符串值，然后键入星号 (<strong>*</strong>)。</td>
<td><strong>S*</strong>查找以 &quot;S&quot; 开头的任何字符串，例如 &quot;Stockholm&quot;、&quot;Sydney&quot; 和 &quot;San Francisco&quot;。</td>
</tr>
<tr class="odd">
<td>*<em>值</em>（星号）</td>
<td>以输入的值结尾</td>
<td>键入星号，然后键入结尾值。</td>
<td><strong>*east</strong> 查找以 &quot;east&quot; 结尾的任何字符串，例如 &quot;Northeast&quot; 和 &quot;Southeast&quot;。</td>
</tr>
<tr class="even">
<td>*<em>值</em>*（星号）</td>
<td>包含输入的值</td>
<td>键入星号，然后键入值，再键入另一个星号。</td>
<td><strong>*th*</strong>查找包含 &quot;th&quot; 的任何字符串，例如 &quot;Northeast&quot; 和 &quot;Southeast&quot;。</td>
</tr>
<tr class="odd">
<td>? （问号）</td>
<td>具有一个或多个未知字符</td>
<td>在值中未知字符的位置键入一个问号。</td>
<td><strong>Sm?th</strong> 查找 &quot;Smith&quot; 和 &quot;Smyth&quot;。</td>
</tr>
<tr class="even">
<td><em>值</em>,<em>值</em>（逗号）</td>
<td>匹配用逗号分隔的值</td>
<td>键入所有条件，用逗号分隔。</td>
<td><strong>A, D, F, G</strong> 精确查找 &quot;A&quot;、&quot;D&quot;、&quot;F&quot; 和 &quot;G&quot;。 <strong>10, 20, 30, 100</strong> 精确查找 &quot;10、20、30、100&quot;。</td>
</tr>
<tr class="odd">
<td>（<span class="code">SQL 语句</span>）（括号间的 SQL 语句）</td>
<td>匹配定义的查询</td>
<td>在括号间键入查询，作为 SQL 语句。</td>
<td><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>二</td>
<td>今天的日期</td>
<td>类型 <strong>T</strong>。</td>
<td><strong>T</strong> 匹配今天的日期。</td>
</tr>
<tr class="odd">
<td>(methodName(parameters))（括号之间的 <strong>SysQueryRangeUtil</strong> 方法）</td>
<td>匹配由 <strong>SysQueryRangeUtil</strong> 方法的参数指定的值或值范围</td>
<td>键入具有指定值或值的范围的参数的 <strong>SysQueryRangeUtil</strong> 方法。</td>
<td><ol>
<li>单击<strong>应收帐款</strong> &gt; <strong>发票</strong> &gt; <strong>未结客户发票</strong>。</li>
<li>按 Ctrl+Shift+F3 打开<strong>查询</strong>页。</li>
<li>在<strong>范围</strong>选项卡上，单击<strong>添加</strong>。</li>
<li>在<strong>表</strong>字段中，选择<strong>未结客户交易记录</strong>。</li>
<li>在<strong>字段</strong>字段中，选择<strong>到期日期</strong>。</li>
<li>在<strong>条件</strong>字段中，输入 <strong>(yearRange(-2,0))</strong>。</li>
<li>单击“<strong>OK</strong>”。 更新列表页并列出与输入的条件匹配的发票。 对于此示例，在前两年到期的发票将列出。</li>
</ol>
请参阅下一部分中的表了解有关 <strong>SysQueryRangeUtil</strong> 的其他详细信息和若干示例。</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>使用 SysQueryRangeUtil 方法的高级日期查询
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>方法</th>
<th>描述</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Day (_relativeDays=0)</td>
<td>查找与会话日期相关的日期。 正值表示将来日期，负值指示过去日期。</td>
<td><ul>
<li><strong>明天</strong> – 输入 <strong>(Day(1))</strong>。</li>
<li><strong>今天</strong> – 输入 <strong>(Day(0))</strong>。</li>
<li><strong>昨天</strong> – 输入 <strong>(Day(-1))</strong>。</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0，_relativeDaysTo=0)</td>
<td>查找与会话日期相关的日期范围。 正值表示将来日期，负值指示过去日期。</td>
<td><ul>
<li><strong>最后 30 天</strong> – 输入 <strong>(DayRange(-30,0))</strong>。</li>
<li><strong>前 30 天和后 30 天</strong> – 输入 <strong>(DayRange(-30,30))</strong>。</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>查找指定相关日期之后的所有日期。</td>
<td><ul>
<li><strong>从现在起超过 30 天</strong> – 输入 <strong>(GreaterThanDate(30))</strong>。</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>查找当前时间后的所有日期/时间条目。</td>
<td><ul>
<li><strong>所有将来日期/时间</strong> – 输入 <strong>(GreaterThanUtcNow())</strong>。</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>查找指定相关日期之前的所有日期。</td>
<td><ul>
<li><strong>从现在起少于七天</strong> – 输入 <strong>(LessThanDate(7))</strong>。</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>查找当前时间前的所有日期/时间条目。</td>
<td><ul>
<li><strong>所有过去日期/时间</strong> – 输入 <strong>(LessThanUtcNow())</strong>。</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>基于与当前月份相关的月查找日期范围。</td>
<td><ul>
<li><strong>前两个月</strong> – 输入 <strong>(MonthRange(-2,0))</strong>。</li>
<li><strong>后三个月</strong> – 输入 <strong>(MonthRange(0,3))</strong>。</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>基于与当前年份相关的年份查找日期范围。</td>
<td><ul>
<li><strong>下一年</strong> – 输入 <strong>(YearRange(0, 1))</strong>。</li>
<li><strong>前一年</strong> – 输入 <strong>(YearRange(-1,0))</strong>。</li>
</ul></td>
</tr>
</tbody>
</table>






