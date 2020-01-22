---
title: 高级筛选和查询语法
description: 本文介绍在“过滤器”窗格或网格列标题过滤器中使用“高级过滤器/排序”对话框或匹配运算符时的可用过滤和查询选项。
author: jasongre
manager: AnnBe
ms.date: 01/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5a96921436311440ba60c3fa31135457cf9f291
ms.sourcegitcommit: 8585de8acf579bcc033671ef270fa9d92230121b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/02/2020
ms.locfileid: "2931280"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="562cb-103">高级筛选和查询语法</span><span class="sxs-lookup"><span data-stu-id="562cb-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="562cb-104">本文介绍在“过滤器”窗格或网格列标题过滤器中使用“高级过滤器/排序”对话框或**匹配**运算符时的可用过滤和查询选项。</span><span class="sxs-lookup"><span data-stu-id="562cb-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="562cb-105">高级查询语法</span><span class="sxs-lookup"><span data-stu-id="562cb-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562cb-106">语法</span><span class="sxs-lookup"><span data-stu-id="562cb-106">Syntax</span></span></th>
<th><span data-ttu-id="562cb-107">字符描述</span><span class="sxs-lookup"><span data-stu-id="562cb-107">Character description</span></span></th>
<th><span data-ttu-id="562cb-108">说明</span><span class="sxs-lookup"><span data-stu-id="562cb-108">Description</span></span></th>
<th><span data-ttu-id="562cb-109">示例</span><span class="sxs-lookup"><span data-stu-id="562cb-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562cb-110"><em>值</em></span><span class="sxs-lookup"><span data-stu-id="562cb-110"><em>value</em></span></span></td>
<td><span data-ttu-id="562cb-111">等于输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-112">键入要查找的该值。</span><span class="sxs-lookup"><span data-stu-id="562cb-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="562cb-113"><strong>Smith</strong> 查找 &quot;Smith&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-114">!<em>值</em>（感叹号）</span><span class="sxs-lookup"><span data-stu-id="562cb-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="562cb-115">不等于输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-116">键入一个惊叹号，然后是要排除的值。</span><span class="sxs-lookup"><span data-stu-id="562cb-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="562cb-117"><strong>!Smith</strong> 查找除 &quot;Smith&quot; 之外的所有值。</span><span class="sxs-lookup"><span data-stu-id="562cb-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-118"><em>开始值</em>..<em>结束值</em>（双句点）</span><span class="sxs-lookup"><span data-stu-id="562cb-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="562cb-119">用双句点分隔的两个值之间</span><span class="sxs-lookup"><span data-stu-id="562cb-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="562cb-120">键入开始值，然后是两个句点，最后键入结束值。</span><span class="sxs-lookup"><span data-stu-id="562cb-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="562cb-121"><strong>1..10</strong> 查找从 1 到 10 的所有值。</span><span class="sxs-lookup"><span data-stu-id="562cb-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="562cb-122">不过，在字符串字段中，<strong>A..C</strong> 将查找以 &quot;A&quot; 开头和以 &quot;B&quot; 开头的所有值以及恰好为 &quot;C&quot; 的值。</span><span class="sxs-lookup"><span data-stu-id="562cb-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="562cb-123">例如，此查询不会查找 &quot;Ca&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="562cb-124">若要查找从 &quot;A<em>&quot; 到 &quot;C</em>&quot; 的所有值，请键入 <strong>A..D</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-125">..<em>值</em>（双句点）</span><span class="sxs-lookup"><span data-stu-id="562cb-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="562cb-126">小于或等于输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-127">键入两个句点，然后键入值。</span><span class="sxs-lookup"><span data-stu-id="562cb-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="562cb-128"><strong>..1000</strong> 查找小于或等于 1000 的任何数字，例如 &quot;100&quot;、&quot;999.95&quot; 和 &quot;1,000&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-129"><em>值</em>..</span><span class="sxs-lookup"><span data-stu-id="562cb-129"><em>value</em>..</span></span> <span data-ttu-id="562cb-130">（双句点）</span><span class="sxs-lookup"><span data-stu-id="562cb-130">(double period)</span></span></td>
<td><span data-ttu-id="562cb-131">大于或等于输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-132">键入值，然后键入两个句点。</span><span class="sxs-lookup"><span data-stu-id="562cb-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="562cb-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="562cb-133"><strong>1000..</strong></span></span> <span data-ttu-id="562cb-134">查找大于或等于 1000 的任何数字，例如 &quot;1,000&quot;、&quot;1,000.01&quot; 和 &quot;1,000,000&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-135">&gt;<em>值</em>（大于符号）</span><span class="sxs-lookup"><span data-stu-id="562cb-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="562cb-136">大于输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-137">键入大于符号 (<strong>&gt;</strong>)，然后键入值。</span><span class="sxs-lookup"><span data-stu-id="562cb-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="562cb-138"><strong>&gt;1000</strong> 查找大于 1000 的任何数字，例如 &quot;1000.01&quot;、&quot;20,000&quot; 和 &quot;1,000,000&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-139">&lt;<em>值</em>（小于符号）</span><span class="sxs-lookup"><span data-stu-id="562cb-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="562cb-140">小于输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-141">键入小于符号 (<strong>&lt;</strong>)，然后键入值。</span><span class="sxs-lookup"><span data-stu-id="562cb-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="562cb-142"><strong>&lt;1000</strong> 查找小于 1000 的任何数字，例如 &quot;999.99&quot;、&quot;1&quot; 和 &quot;-200&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-143"><em>值</em>\*（星号）</span><span class="sxs-lookup"><span data-stu-id="562cb-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="562cb-144">以输入的值开头</span><span class="sxs-lookup"><span data-stu-id="562cb-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-145">键入字符串值，然后键入星号 (<strong>\*</strong>)。</span><span class="sxs-lookup"><span data-stu-id="562cb-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="562cb-146"><strong>S\*</strong>查找以 &quot;S&quot; 开头的任何字符串，例如 &quot;Stockholm&quot;、&quot;Sydney&quot; 和 &quot;San Francisco&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-147">\*<em>值</em>（星号）</span><span class="sxs-lookup"><span data-stu-id="562cb-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="562cb-148">以输入的值结尾</span><span class="sxs-lookup"><span data-stu-id="562cb-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-149">键入星号，然后键入结尾值。</span><span class="sxs-lookup"><span data-stu-id="562cb-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="562cb-150"><strong>\*east</strong> 查找以 &quot;east&quot; 结尾的任何字符串，例如 &quot;Northeast&quot; 和 &quot;Southeast&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-151">*<em>值</em>*（星号）</span><span class="sxs-lookup"><span data-stu-id="562cb-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="562cb-152">包含输入的值</span><span class="sxs-lookup"><span data-stu-id="562cb-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="562cb-153">键入星号，然后键入值，再键入另一个星号。</span><span class="sxs-lookup"><span data-stu-id="562cb-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="562cb-154"><strong>*th*</strong>查找包含 &quot;th&quot; 的任何字符串，例如 &quot;Northeast&quot; 和 &quot;Southeast&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-155">?</span><span class="sxs-lookup"><span data-stu-id="562cb-155">?</span></span> <span data-ttu-id="562cb-156">（问号）</span><span class="sxs-lookup"><span data-stu-id="562cb-156">(question mark)</span></span></td>
<td><span data-ttu-id="562cb-157">具有一个或多个未知字符</span><span class="sxs-lookup"><span data-stu-id="562cb-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="562cb-158">在值中未知字符的位置键入一个问号。</span><span class="sxs-lookup"><span data-stu-id="562cb-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="562cb-159"><strong>Sm?th</strong> 查找 &quot;Smith&quot; 和 &quot;Smyth&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-160"><em>值</em>,<em>值</em>（逗号）</span><span class="sxs-lookup"><span data-stu-id="562cb-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="562cb-161">匹配用逗号分隔的值</span><span class="sxs-lookup"><span data-stu-id="562cb-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="562cb-162">键入所有条件，用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="562cb-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="562cb-163"><strong>A, D, F, G</strong> 精确查找 &quot;A&quot;、&quot;D&quot;、&quot;F&quot; 和 &quot;G&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="562cb-164"><strong>10, 20, 30, 100</strong> 精确查找 &quot;10、20、30、100&quot;。</span><span class="sxs-lookup"><span data-stu-id="562cb-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-165">""（两个双引号）</span><span class="sxs-lookup"><span data-stu-id="562cb-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="562cb-166">匹配空值</span><span class="sxs-lookup"><span data-stu-id="562cb-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="562cb-167">键入两个连续的双引号以过滤该字段中的空值。</span><span class="sxs-lookup"><span data-stu-id="562cb-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="562cb-168">两个连续的双引号 (<strong>""</strong>) 查找当前列没有值的行。</span><span class="sxs-lookup"><span data-stu-id="562cb-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-169">（<span class="code">SQL 语句</span>）（括号间的 SQL 语句）</span><span class="sxs-lookup"><span data-stu-id="562cb-169">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="562cb-170">匹配定义的查询</span><span class="sxs-lookup"><span data-stu-id="562cb-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="562cb-171">在括号间键入查询，作为 SQL 语句。</span><span class="sxs-lookup"><span data-stu-id="562cb-171">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="562cb-172"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="562cb-172"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-173">二</span><span class="sxs-lookup"><span data-stu-id="562cb-173">T</span></span></td>
<td><span data-ttu-id="562cb-174">今天的日期</span><span class="sxs-lookup"><span data-stu-id="562cb-174">Today's date</span></span></td>
<td><span data-ttu-id="562cb-175">类型 <strong>T</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-175">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="562cb-176"><strong>T</strong> 匹配今天的日期。</span><span class="sxs-lookup"><span data-stu-id="562cb-176"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562cb-177">(methodName(parameters))（括号之间的 <strong>SysQueryRangeUtil</strong> 方法）</span><span class="sxs-lookup"><span data-stu-id="562cb-177">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="562cb-178">匹配由 <strong>SysQueryRangeUtil</strong> 方法的参数指定的值或值范围</span><span class="sxs-lookup"><span data-stu-id="562cb-178">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="562cb-179">键入具有指定值或值的范围的参数的 <strong>SysQueryRangeUtil</strong> 方法。</span><span class="sxs-lookup"><span data-stu-id="562cb-179">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="562cb-180">单击<strong>应收账款</strong> &gt; <strong>发票</strong> &gt; <strong>未结客户发票</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-180">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="562cb-181">按 Ctrl+Shift+F3 打开<strong>查询</strong>页。</span><span class="sxs-lookup"><span data-stu-id="562cb-181">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="562cb-182">在<strong>范围</strong>选项卡上，单击<strong>添加</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-182">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="562cb-183">在<strong>表</strong>字段中，选择<strong>未结客户交易记录</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-183">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="562cb-184">在<strong>字段</strong>字段中，选择<strong>到期日期</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-184">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="562cb-185">在<strong>条件</strong>字段中，输入 <strong>(yearRange(-2,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-185">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="562cb-186">单击<strong>OK</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-186">Click <strong>OK</strong>.</span></span> <span data-ttu-id="562cb-187">更新列表页并列出与输入的条件匹配的发票。</span><span class="sxs-lookup"><span data-stu-id="562cb-187">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="562cb-188">对于此示例，在前两年到期的发票将列出。</span><span class="sxs-lookup"><span data-stu-id="562cb-188">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="562cb-189">请参阅下一部分中的表了解有关 <strong>SysQueryRangeUtil</strong> 的其他详细信息和若干示例。</span><span class="sxs-lookup"><span data-stu-id="562cb-189">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="562cb-190">使用 SysQueryRangeUtil 方法的高级日期查询</span><span class="sxs-lookup"><span data-stu-id="562cb-190">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562cb-191">方法</span><span class="sxs-lookup"><span data-stu-id="562cb-191">Method</span></span></th>
<th><span data-ttu-id="562cb-192">描述</span><span class="sxs-lookup"><span data-stu-id="562cb-192">Description</span></span></th>
<th><span data-ttu-id="562cb-193">示例</span><span class="sxs-lookup"><span data-stu-id="562cb-193">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562cb-194">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="562cb-194">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="562cb-195">查找与会话日期相关的日期。</span><span class="sxs-lookup"><span data-stu-id="562cb-195">Find a date relative to the session date.</span></span> <span data-ttu-id="562cb-196">正值表示将来日期，负值指示过去日期。</span><span class="sxs-lookup"><span data-stu-id="562cb-196">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-197"><strong>明天</strong> – 输入 <strong>(Day(1))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-197"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="562cb-198"><strong>今天</strong> – 输入 <strong>(Day(0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-198"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="562cb-199"><strong>昨天</strong> – 输入 <strong>(Day(-1))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-199"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-200">DayRange (_relativeDaysFrom=0，_relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="562cb-200">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="562cb-201">查找与会话日期相关的日期范围。</span><span class="sxs-lookup"><span data-stu-id="562cb-201">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="562cb-202">正值表示将来日期，负值指示过去日期。</span><span class="sxs-lookup"><span data-stu-id="562cb-202">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-203"><strong>最后 30 天</strong> – 输入 <strong>(DayRange(-30,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-203"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="562cb-204"><strong>前 30 天和后 30 天</strong> – 输入 <strong>(DayRange(-30,30))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-204"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-205">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="562cb-205">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="562cb-206">查找指定相关日期之后的所有日期。</span><span class="sxs-lookup"><span data-stu-id="562cb-206">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-207"><strong>从现在起超过 30 天</strong> – 输入 <strong>(GreaterThanDate(30))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-207"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-208">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="562cb-208">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="562cb-209">查找当前时间后的所有日期/时间条目。</span><span class="sxs-lookup"><span data-stu-id="562cb-209">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-210"><strong>所有将来日期/时间</strong> – 输入 <strong>(GreaterThanUtcNow())</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-210"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-211">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="562cb-211">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="562cb-212">查找指定相关日期之前的所有日期。</span><span class="sxs-lookup"><span data-stu-id="562cb-212">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-213"><strong>从现在起少于七天</strong> – 输入 <strong>(LessThanDate(7))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-213"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-214">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="562cb-214">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="562cb-215">查找当前时间前的所有日期/时间条目。</span><span class="sxs-lookup"><span data-stu-id="562cb-215">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-216"><strong>所有过去日期/时间</strong> – 输入 <strong>(LessThanUtcNow())</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-216"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-217">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="562cb-217">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="562cb-218">基于与当前月份相关的月查找日期范围。</span><span class="sxs-lookup"><span data-stu-id="562cb-218">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-219"><strong>前两个月</strong> – 输入 <strong>(MonthRange(-2,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-219"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="562cb-220"><strong>后三个月</strong> – 输入 <strong>(MonthRange(0,3))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-220"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562cb-221">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="562cb-221">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="562cb-222">基于与当前年份相关的年份查找日期范围。</span><span class="sxs-lookup"><span data-stu-id="562cb-222">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="562cb-223"><strong>下一年</strong> – 输入 <strong>(YearRange(0, 1))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-223"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="562cb-224"><strong>前一年</strong> – 输入 <strong>(YearRange(-1,0))</strong>。</span><span class="sxs-lookup"><span data-stu-id="562cb-224"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
