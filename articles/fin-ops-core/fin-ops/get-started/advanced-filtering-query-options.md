---
title: 高级筛选和查询语法
description: 本主题介绍在“筛选器”窗格或网格列标题筛选器中高级筛选/排序对话框和匹配运算符的筛选和查询选项。
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdb55a9552759e5f2b670a4eeb4e5d6572ebfb77
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744091"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="28ef2-103">高级筛选和查询语法</span><span class="sxs-lookup"><span data-stu-id="28ef2-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28ef2-104">此主题介绍在“过滤器”窗格或网格列标题过滤器中使用“高级过滤器/排序”对话框或 **匹配** 运算符时的可用过滤和查询选项。</span><span class="sxs-lookup"><span data-stu-id="28ef2-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="28ef2-105">高级查询语法</span><span class="sxs-lookup"><span data-stu-id="28ef2-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="28ef2-106">语法</span><span class="sxs-lookup"><span data-stu-id="28ef2-106">Syntax</span></span></th>
<th><span data-ttu-id="28ef2-107">字符描述</span><span class="sxs-lookup"><span data-stu-id="28ef2-107">Character description</span></span></th>
<th><span data-ttu-id="28ef2-108">说明</span><span class="sxs-lookup"><span data-stu-id="28ef2-108">Description</span></span></th>
<th><span data-ttu-id="28ef2-109">示例</span><span class="sxs-lookup"><span data-stu-id="28ef2-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="28ef2-110"><em>值</em></span><span class="sxs-lookup"><span data-stu-id="28ef2-110"><em>value</em></span></span></td>
<td><span data-ttu-id="28ef2-111">等于输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-112">键入要查找的该值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="28ef2-113"><strong>Smith</strong> 查找 &quot;Smith&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-114">!<em>值</em>（感叹号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="28ef2-115">不等于输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-116">键入一个惊叹号，然后是要排除的值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="28ef2-117"><strong>!Smith</strong> 查找除 &quot;Smith&quot; 之外的所有值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-118"><em>开始值</em>..<em>结束值</em>（双句点）</span><span class="sxs-lookup"><span data-stu-id="28ef2-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="28ef2-119">用双句点分隔的两个值之间</span><span class="sxs-lookup"><span data-stu-id="28ef2-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="28ef2-120">键入开始值，然后是两个句点，最后键入结束值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="28ef2-121"><strong>1..10</strong> 查找从 1 到 10 的所有值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="28ef2-122">不过，在字符串字段中，<strong>A..C</strong> 将查找以 &quot;A&quot; 开头和以 &quot;B&quot; 开头的所有值以及恰好为 &quot;C&quot; 的值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="28ef2-123">例如，此查询不会查找 &quot;Ca&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="28ef2-124">若要查找从 &quot;A<em>&quot; 到 &quot;C</em>&quot; 的所有值，请键入 <strong>A..D</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-125">..<em>值</em>（双句点）</span><span class="sxs-lookup"><span data-stu-id="28ef2-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="28ef2-126">小于或等于输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-127">键入两个句点，然后键入值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="28ef2-128"><strong>..1000</strong> 查找小于或等于 1000 的任何数字，例如 &quot;100&quot;、&quot;999.95&quot; 和 &quot;1,000&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-129"><em>值</em>..</span><span class="sxs-lookup"><span data-stu-id="28ef2-129"><em>value</em>..</span></span> <span data-ttu-id="28ef2-130">（双句点）</span><span class="sxs-lookup"><span data-stu-id="28ef2-130">(double period)</span></span></td>
<td><span data-ttu-id="28ef2-131">大于或等于输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-132">键入值，然后键入两个句点。</span><span class="sxs-lookup"><span data-stu-id="28ef2-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="28ef2-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="28ef2-133"><strong>1000..</strong></span></span> <span data-ttu-id="28ef2-134">查找大于或等于 1000 的任何数字，例如 &quot;1,000&quot;、&quot;1,000.01&quot; 和 &quot;1,000,000&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-135">&gt;<em>值</em>（大于符号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="28ef2-136">大于输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-137">键入大于符号 (<strong>&gt;</strong>)，然后键入值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="28ef2-138"><strong>&gt;1000</strong> 查找大于 1000 的任何数字，例如 &quot;1000.01&quot;、&quot;20,000&quot; 和 &quot;1,000,000&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-139">&lt;<em>值</em>（小于符号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="28ef2-140">小于输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-141">键入小于符号 (<strong>&lt;</strong>)，然后键入值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="28ef2-142"><strong>&lt;1000</strong> 查找小于 1000 的任何数字，例如 &quot;999.99&quot;、&quot;1&quot; 和 &quot;-200&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-143"><em>值</em>\*（星号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="28ef2-144">以输入的值开头</span><span class="sxs-lookup"><span data-stu-id="28ef2-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-145">键入字符串值，然后键入星号 (<strong>\*</strong>)。</span><span class="sxs-lookup"><span data-stu-id="28ef2-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="28ef2-146"><strong>S\*</strong>查找以 &quot;S&quot; 开头的任何字符串，例如 &quot;Stockholm&quot;、&quot;Sydney&quot; 和 &quot;San Francisco&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-147">\*<em>值</em>（星号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="28ef2-148">以输入的值结尾</span><span class="sxs-lookup"><span data-stu-id="28ef2-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-149">键入星号，然后键入结尾值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="28ef2-150"><strong>\*east</strong> 查找以 &quot;east&quot; 结尾的任何字符串，例如 &quot;Northeast&quot; 和 &quot;Southeast&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-151">*<em>值</em>*（星号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="28ef2-152">包含输入的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="28ef2-153">键入星号，然后键入值，再键入另一个星号。</span><span class="sxs-lookup"><span data-stu-id="28ef2-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="28ef2-154"><strong>*th*</strong>查找包含 &quot;th&quot; 的任何字符串，例如 &quot;Northeast&quot; 和 &quot;Southeast&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-155">?</span><span class="sxs-lookup"><span data-stu-id="28ef2-155">?</span></span> <span data-ttu-id="28ef2-156">（问号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-156">(question mark)</span></span></td>
<td><span data-ttu-id="28ef2-157">具有一个或多个未知字符</span><span class="sxs-lookup"><span data-stu-id="28ef2-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="28ef2-158">在值中未知字符的位置键入一个问号。</span><span class="sxs-lookup"><span data-stu-id="28ef2-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="28ef2-159"><strong>Sm?th</strong> 查找 &quot;Smith&quot; 和 &quot;Smyth&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-160"><em>值</em>,<em>值</em>（逗号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="28ef2-161">匹配用逗号分隔的值</span><span class="sxs-lookup"><span data-stu-id="28ef2-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="28ef2-162">键入所有条件，用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="28ef2-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="28ef2-163"><strong>A, D, F, G</strong> 精确查找 &quot;A&quot;、&quot;D&quot;、&quot;F&quot; 和 &quot;G&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="28ef2-164"><strong>10, 20, 30, 100</strong> 精确查找 &quot;10、20、30、100&quot;。</span><span class="sxs-lookup"><span data-stu-id="28ef2-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-165">""（两个双引号）</span><span class="sxs-lookup"><span data-stu-id="28ef2-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="28ef2-166">匹配空值</span><span class="sxs-lookup"><span data-stu-id="28ef2-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="28ef2-167">键入两个连续的双引号以过滤该字段中的空值。</span><span class="sxs-lookup"><span data-stu-id="28ef2-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="28ef2-168">两个连续的双引号 (<strong>""</strong>) 查找当前列没有值的行。</span><span class="sxs-lookup"><span data-stu-id="28ef2-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-169">（<span class="code">Finance and Operations 查询</span>）（连字符之间的 Finance and Operations 查询）</span><span class="sxs-lookup"><span data-stu-id="28ef2-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="28ef2-170">匹配定义的查询</span><span class="sxs-lookup"><span data-stu-id="28ef2-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="28ef2-171">使用 Finance and Operations 查询语言在连字符之间键入 SQL 语句格式的查询。</span><span class="sxs-lookup"><span data-stu-id="28ef2-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="28ef2-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="28ef2-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="28ef2-173">这是根数据源中的一个字段和另一个数据源（对于 AII 客户页面）的字段的筛选条件语法示例</span><span class="sxs-lookup"><span data-stu-id="28ef2-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-174">二</span><span class="sxs-lookup"><span data-stu-id="28ef2-174">T</span></span></td>
<td><span data-ttu-id="28ef2-175">今天的日期</span><span class="sxs-lookup"><span data-stu-id="28ef2-175">Today's date</span></span></td>
<td><span data-ttu-id="28ef2-176">类型 <strong>T</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="28ef2-177"><strong>T</strong> 匹配今天的日期。</span><span class="sxs-lookup"><span data-stu-id="28ef2-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-178">(methodName(parameters))（括号之间的 <strong>SysQueryRangeUtil</strong> 方法）</span><span class="sxs-lookup"><span data-stu-id="28ef2-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="28ef2-179">匹配由 <strong>SysQueryRangeUtil</strong> 方法的参数指定的值或值范围</span><span class="sxs-lookup"><span data-stu-id="28ef2-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="28ef2-180">键入具有指定值或值的范围的参数的 <strong>SysQueryRangeUtil</strong> 方法。</span><span class="sxs-lookup"><span data-stu-id="28ef2-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="28ef2-181">单击<strong>应收帐款</strong> &gt; <strong>发票</strong> &gt; <strong>未结客户发票</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-182">按 Ctrl+Shift+F3 打开<strong>查询</strong>页。</span><span class="sxs-lookup"><span data-stu-id="28ef2-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="28ef2-183">在<strong>范围</strong>选项卡上，单击<strong>添加</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-184">在<strong>表</strong>字段中，选择<strong>未结客户交易记录</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-185">在<strong>字段</strong>字段中，选择<strong>到期日期</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-186">在<strong>条件</strong>字段中，输入 <strong>(yearRange(-2,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-187">单击<strong>OK</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="28ef2-188">更新列表页并列出与输入的条件匹配的发票。</span><span class="sxs-lookup"><span data-stu-id="28ef2-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="28ef2-189">对于此示例，在前两年到期的发票将列出。</span><span class="sxs-lookup"><span data-stu-id="28ef2-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="28ef2-190">请参阅下一部分中的表了解有关 <strong>SysQueryRangeUtil</strong> 的其他详细信息和若干示例。</span><span class="sxs-lookup"><span data-stu-id="28ef2-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="28ef2-191">使用 SysQueryRangeUtil 方法的高级日期查询</span><span class="sxs-lookup"><span data-stu-id="28ef2-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="28ef2-192">方法</span><span class="sxs-lookup"><span data-stu-id="28ef2-192">Method</span></span></th>
<th><span data-ttu-id="28ef2-193">描述</span><span class="sxs-lookup"><span data-stu-id="28ef2-193">Description</span></span></th>
<th><span data-ttu-id="28ef2-194">示例</span><span class="sxs-lookup"><span data-stu-id="28ef2-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="28ef2-195">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="28ef2-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="28ef2-196">查找与会话日期相关的日期。</span><span class="sxs-lookup"><span data-stu-id="28ef2-196">Find a date relative to the session date.</span></span> <span data-ttu-id="28ef2-197">正值表示将来日期，负值指示过去日期。</span><span class="sxs-lookup"><span data-stu-id="28ef2-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-198"><strong>明天</strong> – 输入 <strong>(Day(1))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-199"><strong>今天</strong> – 输入 <strong>(Day(0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-200"><strong>昨天</strong> – 输入 <strong>(Day(-1))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-201">DayRange (_relativeDaysFrom=0，_relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="28ef2-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="28ef2-202">查找与会话日期相关的日期范围。</span><span class="sxs-lookup"><span data-stu-id="28ef2-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="28ef2-203">正值表示将来日期，负值指示过去日期。</span><span class="sxs-lookup"><span data-stu-id="28ef2-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-204"><strong>最后 30 天</strong> – 输入 <strong>(DayRange(-30,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-205"><strong>前 30 天和后 30 天</strong> – 输入 <strong>(DayRange(-30,30))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="28ef2-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="28ef2-207">查找指定相关日期之后的所有日期。</span><span class="sxs-lookup"><span data-stu-id="28ef2-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-208"><strong>从现在起超过 30 天</strong> – 输入 <strong>(GreaterThanDate(30))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="28ef2-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="28ef2-210">查找当前时间后的所有日期/时间条目。</span><span class="sxs-lookup"><span data-stu-id="28ef2-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-211"><strong>所有将来日期/时间</strong> – 输入 <strong>(GreaterThanUtcNow())</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="28ef2-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="28ef2-213">查找指定相关日期之前的所有日期。</span><span class="sxs-lookup"><span data-stu-id="28ef2-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-214"><strong>从现在起少于七天</strong> – 输入 <strong>(LessThanDate(7))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="28ef2-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="28ef2-216">查找当前时间前的所有日期/时间条目。</span><span class="sxs-lookup"><span data-stu-id="28ef2-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-217"><strong>所有过去日期/时间</strong> – 输入 <strong>(LessThanUtcNow())</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="28ef2-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="28ef2-219">基于与当前月份相关的月查找日期范围。</span><span class="sxs-lookup"><span data-stu-id="28ef2-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-220"><strong>前两个月</strong> – 输入 <strong>(MonthRange(-2,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-221"><strong>后三个月</strong> – 输入 <strong>(MonthRange(0,3))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28ef2-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="28ef2-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="28ef2-223">基于与当前年份相关的年份查找日期范围。</span><span class="sxs-lookup"><span data-stu-id="28ef2-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28ef2-224"><strong>下一年</strong> – 输入 <strong>(YearRange(0, 1))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="28ef2-225"><strong>前一年</strong> – 输入 <strong>(YearRange(-1,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="28ef2-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]