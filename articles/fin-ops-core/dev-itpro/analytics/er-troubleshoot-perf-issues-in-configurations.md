---
title: 解决 ER 配置中的性能问题
description: 本主题说明如何查找和修复电子申报 (ER) 配置中的性能问题。
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216857"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="7e171-103">解决 ER 配置中的性能问题</span><span class="sxs-lookup"><span data-stu-id="7e171-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="7e171-104">本主题说明如何查找和解决[电子申报](general-electronic-reporting.md) (ER) [配置](general-electronic-reporting.md#Configuration)中的性能问题。</span><span class="sxs-lookup"><span data-stu-id="7e171-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="7e171-105">通常，性能调查包括几个步骤。</span><span class="sxs-lookup"><span data-stu-id="7e171-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="7e171-106">[收集](#collecting-data)数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="7e171-107">分析收集的数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="7e171-108">根据分析结果，使用 ER 配置[进行更改](#making-changes)，或决定收集更多数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="7e171-109">疑难解答</span><span class="sxs-lookup"><span data-stu-id="7e171-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="7e171-110">分析执行时间</span><span class="sxs-lookup"><span data-stu-id="7e171-110">Analyze execution time</span></span>

<span data-ttu-id="7e171-111">执行时间可能取决于不可预测的因素，例如在同一环境中运行的其他任务以及首次调用时使用数据的缓存。</span><span class="sxs-lookup"><span data-stu-id="7e171-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="7e171-112">因此，您应该多次重复执行和度量。</span><span class="sxs-lookup"><span data-stu-id="7e171-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="7e171-113">有时，性能问题不是由用于申报的 ER 格式配置引起的。</span><span class="sxs-lookup"><span data-stu-id="7e171-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="7e171-114">相反，它们是由用于打开该 ER 格式配置的 X++ 代码引起的。</span><span class="sxs-lookup"><span data-stu-id="7e171-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="7e171-115">在[操作中心](#infolog-time)或[事件日志](#event-log-time)中，查看报表的执行时间。</span><span class="sxs-lookup"><span data-stu-id="7e171-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="7e171-116">将报表的执行时间与场景中的总执行时间进行比较。</span><span class="sxs-lookup"><span data-stu-id="7e171-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="7e171-117">如果报表的执行时间远远小于总执行时间，则考虑报表处理的数据量：</span><span class="sxs-lookup"><span data-stu-id="7e171-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="7e171-118">如果报表处理少量数据，则问题可能涉及配置的加载时间。</span><span class="sxs-lookup"><span data-stu-id="7e171-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="7e171-119">如果报表处理大量数据，则问题可能涉及预处理 X++。</span><span class="sxs-lookup"><span data-stu-id="7e171-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="7e171-120">使用[跟踪分析程序](#analyze-trace-parser-trace)分析此案例。</span><span class="sxs-lookup"><span data-stu-id="7e171-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="7e171-121">对于其他案例，请参阅后续部分。</span><span class="sxs-lookup"><span data-stu-id="7e171-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="7e171-122">运行涉及不同数据量的多个测试，以确定执行时间如何取决于数据量。</span><span class="sxs-lookup"><span data-stu-id="7e171-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="7e171-123">分析跟踪分析程序跟踪</span><span class="sxs-lookup"><span data-stu-id="7e171-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="7e171-124">准备一个小例子，或者在报表生成的随机部分中收集几个跟踪。</span><span class="sxs-lookup"><span data-stu-id="7e171-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="7e171-125">然后，在[跟踪分析程序](#trace-parser)中，进行标准的自下而上分析，并回答以下问题：</span><span class="sxs-lookup"><span data-stu-id="7e171-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="7e171-126">在时间消耗方面，排名靠前的方法是什么？</span><span class="sxs-lookup"><span data-stu-id="7e171-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="7e171-127">这些方法使用了总时间的哪一部分？</span><span class="sxs-lookup"><span data-stu-id="7e171-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="7e171-128">回答相同的查询问题。</span><span class="sxs-lookup"><span data-stu-id="7e171-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="7e171-129">如果您看到方法以“ER”为前缀，请转到下一部分。</span><span class="sxs-lookup"><span data-stu-id="7e171-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="7e171-130">如果您看到方法或查询源自应用程序套件，请考虑通用优化（例如，创建索引）。</span><span class="sxs-lookup"><span data-stu-id="7e171-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="7e171-131">分析调用次数。</span><span class="sxs-lookup"><span data-stu-id="7e171-131">Analyze the number of calls.</span></span> <span data-ttu-id="7e171-132">如果数量明显高于预期，请考虑缓存配置的相应节点。</span><span class="sxs-lookup"><span data-stu-id="7e171-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="7e171-133">分析数据库调用</span><span class="sxs-lookup"><span data-stu-id="7e171-133">Analyze database calls</span></span>

<span data-ttu-id="7e171-134">准备一个包含少量数据的示例，以便您可以收集 [ER 跟踪](#electronic-reporting-traces)。</span><span class="sxs-lookup"><span data-stu-id="7e171-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="7e171-135">然后在 ER 模型映射设计器中打开跟踪，并查看页面底部。</span><span class="sxs-lookup"><span data-stu-id="7e171-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="7e171-136">回答以下问题：</span><span class="sxs-lookup"><span data-stu-id="7e171-136">Answer the following questions:</span></span>

- <span data-ttu-id="7e171-137">是否有任何查询重复？</span><span class="sxs-lookup"><span data-stu-id="7e171-137">Is there any query duplication?</span></span> <span data-ttu-id="7e171-138">如果有，请考虑以下修复之一：</span><span class="sxs-lookup"><span data-stu-id="7e171-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="7e171-139">[使用缓存](#use-caching)，如果您认为在一个父记录中有多个调用。</span><span class="sxs-lookup"><span data-stu-id="7e171-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="7e171-140">[使用缓存的参数化计算字段](#cached-parameterized)，如果您认为在不同的记录中有对同一记录的调用。</span><span class="sxs-lookup"><span data-stu-id="7e171-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="7e171-141">[使用 **JOIN** 数据源](#use-join-datasource)，如果您必须从数据库中读取大量不同的记录。</span><span class="sxs-lookup"><span data-stu-id="7e171-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="7e171-142">查询数和提取的记录数是否与数据总量相对应？</span><span class="sxs-lookup"><span data-stu-id="7e171-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="7e171-143">例如，如果单据具有 10 行，统计数据显示报表提取 10 行还是 1,000 行？</span><span class="sxs-lookup"><span data-stu-id="7e171-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="7e171-144">如果您有大量提取的记录，请考虑以下修复之一：</span><span class="sxs-lookup"><span data-stu-id="7e171-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="7e171-145">[使用 **FILTER** 函数而不是 **WHERE** 函数](#filter)在 SQL Server 端处理数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="7e171-146">使用缓存避免提取相同的数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="7e171-147">[使用收集的数据函数](#collected-data)避免提取相同的数据进行汇总。</span><span class="sxs-lookup"><span data-stu-id="7e171-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="7e171-148">分析 PerfView 跟踪</span><span class="sxs-lookup"><span data-stu-id="7e171-148">Analyze PerfView traces</span></span>

<span data-ttu-id="7e171-149">[PerfView](#perfview) 是面向经验丰富的开发人员的工具。</span><span class="sxs-lookup"><span data-stu-id="7e171-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="7e171-150">有关以下步骤的更多详细信息，请参阅[时钟时间调查基本知识](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics)。</span><span class="sxs-lookup"><span data-stu-id="7e171-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="7e171-151">使用线程时间收集跟踪。</span><span class="sxs-lookup"><span data-stu-id="7e171-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="7e171-152">仅包括使用 **runUnattended** 的堆栈，以仅筛选具有配置执行的线程。</span><span class="sxs-lookup"><span data-stu-id="7e171-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="7e171-153">（将 **runUnattended** 添加到 **IncPats** 输入框。）</span><span class="sxs-lookup"><span data-stu-id="7e171-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="7e171-154">折叠所有 CPU、网络和阻止时间。</span><span class="sxs-lookup"><span data-stu-id="7e171-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="7e171-155">加载 [PerfView 的 ER 预设](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml)。</span><span class="sxs-lookup"><span data-stu-id="7e171-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="7e171-156">选择 **ER** \> **其他预设**。</span><span class="sxs-lookup"><span data-stu-id="7e171-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="7e171-157">查看名称：</span><span class="sxs-lookup"><span data-stu-id="7e171-157">Look at the names:</span></span>

    - <span data-ttu-id="7e171-158">您可能会看到消耗时间最多的平台代码。</span><span class="sxs-lookup"><span data-stu-id="7e171-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="7e171-159">您可以两次点击（或双击）并浏览到 **被调用者**。</span><span class="sxs-lookup"><span data-stu-id="7e171-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="7e171-160">如果找到前缀为“ERExpression”的类，并且如果这些函数与公式相关，您可以根据类名称猜测函数名称，并且可以查看 ER 存储库以查看属性。</span><span class="sxs-lookup"><span data-stu-id="7e171-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="7e171-161">修复</span><span class="sxs-lookup"><span data-stu-id="7e171-161">Fixes</span></span>

- <span data-ttu-id="7e171-162">如果您看到查询消耗了大部分 CPU 时间，请尝试减少查询次数：</span><span class="sxs-lookup"><span data-stu-id="7e171-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="7e171-163">对于重复查询，[查看 ER 跟踪](#analyze-database-calls)。</span><span class="sxs-lookup"><span data-stu-id="7e171-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="7e171-164">查看提取了多少记录，并评估理论上应该提取多少数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="7e171-165">如果您看到使用的函数消耗了大部分 CPU 时间，请尝试查找配置中消耗了大部分资源的位置。</span><span class="sxs-lookup"><span data-stu-id="7e171-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="7e171-166">如果您看到数据收集函数消耗了大部分 CPU 时间，请考虑在模型映射端将其替换为 *SQL 分组依据*。</span><span class="sxs-lookup"><span data-stu-id="7e171-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="7e171-167">收集数据</span><span class="sxs-lookup"><span data-stu-id="7e171-167">Collecting data</span></span>

<span data-ttu-id="7e171-168">根据您的环境，可通过多种方法收集可用数据：</span><span class="sxs-lookup"><span data-stu-id="7e171-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="7e171-169">获取总运行时间：</span><span class="sxs-lookup"><span data-stu-id="7e171-169">Get the total running time:</span></span>

    - <span data-ttu-id="7e171-170">通过操作中心</span><span class="sxs-lookup"><span data-stu-id="7e171-170">From the Action center</span></span>
    - <span data-ttu-id="7e171-171">通过事件日志</span><span class="sxs-lookup"><span data-stu-id="7e171-171">From the event log</span></span>

- <span data-ttu-id="7e171-172">分析执行：</span><span class="sxs-lookup"><span data-stu-id="7e171-172">Profile the execution:</span></span>

    - <span data-ttu-id="7e171-173">通过使用 ER 工具</span><span class="sxs-lookup"><span data-stu-id="7e171-173">By using ER tools</span></span>
    - <span data-ttu-id="7e171-174">通过使用跟踪分析程序</span><span class="sxs-lookup"><span data-stu-id="7e171-174">By using Trace parser</span></span>
    - <span data-ttu-id="7e171-175">通过使用 PerfView</span><span class="sxs-lookup"><span data-stu-id="7e171-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="7e171-176">在生产环境中收集数据</span><span class="sxs-lookup"><span data-stu-id="7e171-176">Collecting data in a production environment</span></span>

<span data-ttu-id="7e171-177">有时，问题只能在生产环境中重现。</span><span class="sxs-lookup"><span data-stu-id="7e171-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="7e171-178">可以通过以下方式收集数据：</span><span class="sxs-lookup"><span data-stu-id="7e171-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="7e171-179">通过使用[跟踪分析程序](../perf-test/trace-trace-tutorial.md)跟踪</span><span class="sxs-lookup"><span data-stu-id="7e171-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="7e171-180">通过使用 [ER 执行](trace-execution-er-troubleshoot-perf.md)跟踪</span><span class="sxs-lookup"><span data-stu-id="7e171-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="7e171-181">通过使用总执行时间</span><span class="sxs-lookup"><span data-stu-id="7e171-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="7e171-182">在开发环境中收集数据</span><span class="sxs-lookup"><span data-stu-id="7e171-182">Collecting data in a development environment</span></span>

<span data-ttu-id="7e171-183">除了可以在生产环境中使用的工具外，还有几种可以在开发环境中使用的工具：</span><span class="sxs-lookup"><span data-stu-id="7e171-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="7e171-184">事件日志 (Microsoft-Dynamics-ElectronicReporting)。</span><span class="sxs-lookup"><span data-stu-id="7e171-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="7e171-185">此日志可以为您提供总执行时间。</span><span class="sxs-lookup"><span data-stu-id="7e171-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="7e171-186">常见的 .NET 工具，例如 PerfView。</span><span class="sxs-lookup"><span data-stu-id="7e171-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="7e171-187">此外，开发环境为您提供了更大的试验灵活性。</span><span class="sxs-lookup"><span data-stu-id="7e171-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="7e171-188">例如，您可以关闭部分报表以查看执行时间如何受到影响。</span><span class="sxs-lookup"><span data-stu-id="7e171-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="7e171-189">工具</span><span class="sxs-lookup"><span data-stu-id="7e171-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="7e171-190">操作中心中的执行时间</span><span class="sxs-lookup"><span data-stu-id="7e171-190">Execution time in the Action center</span></span>

<span data-ttu-id="7e171-191">ER 可以在操作中心中显示配置的执行时间。</span><span class="sxs-lookup"><span data-stu-id="7e171-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="7e171-192">此选项仅适用于特定用户和特定公司，并且仅适用于交互式会话。</span><span class="sxs-lookup"><span data-stu-id="7e171-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="7e171-193">若要使此功能可用，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7e171-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="7e171-194">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="7e171-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7e171-195">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="7e171-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="7e171-196">在 **用户参数** 对话框中，将 **显示文件生成时间** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="7e171-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="7e171-197">事件日志中的执行时间</span><span class="sxs-lookup"><span data-stu-id="7e171-197">Execution time in the event log</span></span>

1. <span data-ttu-id="7e171-198">打开 Windows 事件查看器。</span><span class="sxs-lookup"><span data-stu-id="7e171-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="7e171-199">在 **应用程序和服务日志** 下，打开 **Microsoft-Dynamics-ElectronicReporting/Operational**。</span><span class="sxs-lookup"><span data-stu-id="7e171-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="7e171-200">查找其中 **EventID=2** 的 **FormatMapingRun** 事件，因为这些事件包含有关经过时间的信息。</span><span class="sxs-lookup"><span data-stu-id="7e171-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="7e171-201">跟踪分析程序跟踪</span><span class="sxs-lookup"><span data-stu-id="7e171-201">Trace parser traces</span></span> 

<span data-ttu-id="7e171-202">因为 ER 在 X++ 中实现，因此您可以使用常见的 X++ 工具分析性能。</span><span class="sxs-lookup"><span data-stu-id="7e171-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="7e171-203">有关详细信息，请参阅[使用跟踪分析程序进行跟踪](../perf-test/trace-trace-tutorial.md)。</span><span class="sxs-lookup"><span data-stu-id="7e171-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="7e171-204">此方法有一些限制。</span><span class="sxs-lookup"><span data-stu-id="7e171-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="7e171-205">因为部分 ER 在 C# 中实现，因此并非所有详细信息都可用。</span><span class="sxs-lookup"><span data-stu-id="7e171-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="7e171-206">但是，您可以查看数据使用情况详细信息。</span><span class="sxs-lookup"><span data-stu-id="7e171-206">However, you can view the data usage details.</span></span> <span data-ttu-id="7e171-207">此外，长时间的报表运行可能会超出跟踪存储限制。</span><span class="sxs-lookup"><span data-stu-id="7e171-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="7e171-208">ER 跟踪</span><span class="sxs-lookup"><span data-stu-id="7e171-208">ER traces</span></span>

<span data-ttu-id="7e171-209">ER 可以收集自己的跟踪，并且它具有这些跟踪的可视化和分析工具。</span><span class="sxs-lookup"><span data-stu-id="7e171-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="7e171-210">有关详细信息，请参阅[跟踪 ER 格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="7e171-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="7e171-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="7e171-211">PerfView</span></span>

<span data-ttu-id="7e171-212">因为 X++ 和 ER 都在 .NET 平台顶部实现，因此您可以使用常见的 .NET 工具。</span><span class="sxs-lookup"><span data-stu-id="7e171-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="7e171-213">例如，您可以使用免费的 [PerfView](https://github.com/Microsoft/perfview) 工具。</span><span class="sxs-lookup"><span data-stu-id="7e171-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="7e171-214">您还可以从命令行收集数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-214">You can also collect data from the command line.</span></span> <span data-ttu-id="7e171-215">例如，以下 Windows PowerShell 脚本收集执行时间，直到任何格式的执行在计算机上停止为止。</span><span class="sxs-lookup"><span data-stu-id="7e171-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="7e171-216">此方法有一些限制。</span><span class="sxs-lookup"><span data-stu-id="7e171-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="7e171-217">您必须对计算机具有管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="7e171-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="7e171-218">此外，您必须是一名经验丰富的开发人员，因为这是一个陡峭的学习曲线。</span><span class="sxs-lookup"><span data-stu-id="7e171-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="7e171-219">进行更改</span><span class="sxs-lookup"><span data-stu-id="7e171-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="7e171-220">使用缓存</span><span class="sxs-lookup"><span data-stu-id="7e171-220">Use caching</span></span>

<span data-ttu-id="7e171-221">虽然缓存减少了再次提取数据所需的时间量，但它会消耗内存。</span><span class="sxs-lookup"><span data-stu-id="7e171-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="7e171-222">在提取的数据量不是很大的情况下使用缓存。</span><span class="sxs-lookup"><span data-stu-id="7e171-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="7e171-223">有关显示如何使用缓存的详细信息和示例，请参阅[根据来自执行跟踪的信息改善模型映射](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)。</span><span class="sxs-lookup"><span data-stu-id="7e171-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="7e171-224">使用缓存的参数化计算字段</span><span class="sxs-lookup"><span data-stu-id="7e171-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="7e171-225">有时，必须反复查找值。</span><span class="sxs-lookup"><span data-stu-id="7e171-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="7e171-226">示例包括帐户名称和帐号。</span><span class="sxs-lookup"><span data-stu-id="7e171-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="7e171-227">为了帮助节省时间，您可以创建一个在顶层具有参数的计算字段，然后将该字段添加到缓存中。</span><span class="sxs-lookup"><span data-stu-id="7e171-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="7e171-228">我们建议您仅在缓存的数据大小较小时使用此方法。</span><span class="sxs-lookup"><span data-stu-id="7e171-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="7e171-229">有关详细信息，请参阅[通过添加参数化的计算字段数据源提高 ER 解决方案的性能](er-calculated-field-ds-performance.md)。</span><span class="sxs-lookup"><span data-stu-id="7e171-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="7e171-230">使用 JOIN 数据源</span><span class="sxs-lookup"><span data-stu-id="7e171-230">Use a JOIN data source</span></span>

<span data-ttu-id="7e171-231">**JOIN** 数据源允许通过一个查询提取多个连接记录。</span><span class="sxs-lookup"><span data-stu-id="7e171-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="7e171-232">不必使用单独的查询来提取每个连接记录。</span><span class="sxs-lookup"><span data-stu-id="7e171-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="7e171-233">例如，如果您有 1,000 行，并且按关系提取每行的项目数据，您将有 1,001 个查询 (= 1,000 + 1)。</span><span class="sxs-lookup"><span data-stu-id="7e171-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="7e171-234">如果使用 **JOIN** 数据源，您将仅使用一个查询来提取相同的数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="7e171-235">有关详细信息，请参阅[在 ER 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据](er-join-data-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="7e171-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="7e171-236">使用 FILTER 函数而不是 WHERE 函数</span><span class="sxs-lookup"><span data-stu-id="7e171-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="7e171-237">**[FILTER](er-functions-list-filter.md)** 函数在 SQL Server 上运行条件，而 **WHERE** 函数从列表中提取所有数据（一次一条记录）并针对每条记录应用条件。</span><span class="sxs-lookup"><span data-stu-id="7e171-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="7e171-238">例如，您要从 1,000 条记录中选择一条记录。</span><span class="sxs-lookup"><span data-stu-id="7e171-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="7e171-239">如果使用 **WHERE**，将提取全部 1,000 条记录。</span><span class="sxs-lookup"><span data-stu-id="7e171-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="7e171-240">但是，如果使用 **FILTER**，将只提取一条记录。</span><span class="sxs-lookup"><span data-stu-id="7e171-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="7e171-241">**FILTER** 也可以在数据库端使用索引。</span><span class="sxs-lookup"><span data-stu-id="7e171-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="7e171-242">使用收集的数据函数或累积的数据数据源</span><span class="sxs-lookup"><span data-stu-id="7e171-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="7e171-243">如果您的配置具有之前按报表汇总了提取数据的 *分组依据* 组件，该组件将再次提取所有数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="7e171-244">通过使用收集的数据函数，您可以使 ER 在第一次提取期间积累数据。</span><span class="sxs-lookup"><span data-stu-id="7e171-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="7e171-245">有关详细信息，请参阅 [ER 配置格式以进行计数和合计](tasks/er-format-counting-summing-2.md)。</span><span class="sxs-lookup"><span data-stu-id="7e171-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="7e171-246">在 X++ 中重写部分配置</span><span class="sxs-lookup"><span data-stu-id="7e171-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="7e171-247">ER 支持调用表和类的方法，包括扩展。</span><span class="sxs-lookup"><span data-stu-id="7e171-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="7e171-248">考虑在 X++ 中重写部分模型映射以帮助提高性能。</span><span class="sxs-lookup"><span data-stu-id="7e171-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="7e171-249">ER 可以使用来自以下来源的数据：</span><span class="sxs-lookup"><span data-stu-id="7e171-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="7e171-250">类（**对象** 和 **类** 数据源）</span><span class="sxs-lookup"><span data-stu-id="7e171-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="7e171-251">表（**表** 和 **表记录** 数据源）</span><span class="sxs-lookup"><span data-stu-id="7e171-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="7e171-252">[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) 还提供一种从调用代码发送预计算的数据的方法。</span><span class="sxs-lookup"><span data-stu-id="7e171-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="7e171-253">应用程序套件包含此方法的许多示例。</span><span class="sxs-lookup"><span data-stu-id="7e171-253">The application suite contains numerous examples of this approach.</span></span>
