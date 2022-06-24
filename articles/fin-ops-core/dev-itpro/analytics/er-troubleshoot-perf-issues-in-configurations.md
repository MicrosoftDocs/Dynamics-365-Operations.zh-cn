---
title: 解决 ER 配置中的性能问题
description: 本文说明如何查找和修复电子报告 (ER) 配置中的性能问题。
author: NickSelin
ms.date: 05/12/2022
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
ms.openlocfilehash: 28ff68309bad7a6c1b6009ba03ef4b20aceb5194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847331"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>解决 ER 配置中的性能问题

本文说明如何查找和解决[电子报告](general-electronic-reporting.md) (ER) [配置](general-electronic-reporting.md#Configuration)中的性能问题。

通常，性能调查包括几个步骤。

1. [收集](#collecting-data)数据。
2. 分析收集的数据。
3. 根据分析结果，使用 ER 配置[进行更改](#making-changes)，或决定收集更多数据。

## <a name="troubleshooting"></a>疑难解答

### <a name="analyze-execution-time"></a>分析执行时间

执行时间可能取决于不可预测的因素，例如在同一环境中运行的其他任务以及首次调用时使用数据的缓存。 因此，您应该多次重复执行和度量。

有时，性能问题不是由用于申报的 ER 格式配置引起的。 相反，它们是由用于打开该 ER 格式配置的 X++ 代码引起的。

1. 在[操作中心](#infolog-time)或[事件日志](#event-log-time)中，查看报表的执行时间。
2. 将报表的执行时间与场景中的总执行时间进行比较。
3. 如果报表的执行时间远远小于总执行时间，则考虑报表处理的数据量：

    - 如果报表处理少量数据，则问题可能涉及配置的加载时间。
    - 如果报表处理大量数据，则问题可能涉及预处理 X++。 使用[跟踪分析程序](#analyze-trace-parser-trace)分析此案例。

    对于其他案例，请参阅后续部分。

4. 运行涉及不同数据量的多个测试，以确定执行时间如何取决于数据量。

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>分析跟踪分析程序跟踪

准备一个小例子，或者在报表生成的随机部分中收集几个跟踪。

然后，在[跟踪分析程序](#trace-parser)中，进行标准的自下而上分析，并回答以下问题：

- 在时间消耗方面，排名靠前的方法是什么？
- 这些方法使用了总时间的哪一部分？

回答相同的查询问题。

如果您看到方法以“ER”为前缀，请转到下一部分。

如果您看到方法或查询源自应用程序套件，请考虑通用优化（例如，创建索引）。

分析调用次数。 如果数量明显高于预期，请考虑缓存配置的相应节点。

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>分析数据库调用

准备一个包含少量数据的示例，以便您可以收集 [ER 跟踪](#electronic-reporting-traces)。

然后在 ER 模型映射设计器中打开跟踪，并查看页面底部。 回答以下问题：

- 是否有任何查询重复？ 如果有，请考虑以下修复之一：

    - [使用缓存](#use-caching)，如果您认为在一个父记录中有多个调用。
    - [使用缓存的参数化计算字段](#cached-parameterized)，如果您认为在不同的记录中有对同一记录的调用。
    - [使用 **JOIN** 数据源](#use-join-datasource)，如果您必须从数据库中读取大量不同的记录。

- 查询数和提取的记录数是否与数据总量相对应？ 例如，如果单据具有 10 行，统计数据显示报表提取 10 行还是 1,000 行？ 如果您有大量提取的记录，请考虑以下修复之一：

    - [使用 **FILTER** 函数而不是 **WHERE** 函数](#filter)在 Microsoft SQL Server 端处理数据。
    - 使用缓存避免提取相同的数据。
    - [使用收集的数据函数](#collected-data)避免提取相同的数据进行汇总。

### <a name="analyze-perfview-traces"></a>分析 PerfView 跟踪

[PerfView](#perfview) 是面向经验丰富的开发人员的工具。 有关以下步骤的更多详细信息，请参阅[时钟时间调查基本知识](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics)。

1. 使用线程时间收集跟踪。
2. 仅包括使用 **runUnattended** 的堆栈，以仅筛选具有配置执行的线程。 （将 **runUnattended** 添加到 **IncPats** 输入框。）
3. 折叠所有 CPU、网络和阻止时间。
4. 加载 [PerfView 的 ER 预设](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml)。
5. 选择 **ER** \> **其他预设**。
6. 查看名称：

    - 您可能会看到消耗时间最多的平台代码。
    - 您可以两次点击（或双击）并浏览到 **被调用者**。

        如果找到前缀为“ERExpression”的类，并且如果这些函数与公式相关，您可以根据类名称猜测函数名称，并且可以查看 ER 存储库以查看属性。

### <a name="fixes"></a>修复

- 如果您看到查询消耗了大部分 CPU 时间，请尝试减少查询次数：

    - 对于重复查询，[查看 ER 跟踪](#analyze-database-calls)。
    - 查看提取了多少记录，并评估理论上应该提取多少数据。

- 如果您看到使用的函数消耗了大部分 CPU 时间，请尝试查找配置中消耗了大部分资源的位置。
- 如果您看到数据收集函数消耗了大部分 CPU 时间，请考虑在模型映射端将其替换为 *SQL 分组依据*。

### <a name="collecting-data"></a><a name="collecting-data"></a>收集数据

根据您的环境，可通过多种方法收集可用数据：

- 获取总运行时间：

    - 通过操作中心
    - 通过事件日志

- 分析执行：

    - 通过使用 ER 工具
    - 通过使用跟踪分析程序
    - 通过使用 PerfView

#### <a name="collecting-data-in-a-production-environment"></a>在生产环境中收集数据

有时，问题只能在生产环境中重现。 可以通过以下方式收集数据：

- 通过使用[跟踪分析程序](../perf-test/trace-trace-tutorial.md)跟踪
- 通过使用 [ER 执行](trace-execution-er-troubleshoot-perf.md)跟踪
- 通过使用总执行时间

#### <a name="collecting-data-in-a-development-environment"></a>在开发环境中收集数据

除了可以在生产环境中使用的工具外，还有几种可以在开发环境中使用的工具：

- 事件日志 (Microsoft-Dynamics-ElectronicReporting)。 此日志可以为您提供总执行时间。
- 常见的 .NET 工具，例如 PerfView。

此外，开发环境为您提供了更大的试验灵活性。 例如，您可以关闭部分报表以查看执行时间如何受到影响。

### <a name="tools"></a><a name="tools"></a>工具

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>操作中心中的执行时间

ER 可以在操作中心中显示配置的执行时间。 此选项仅适用于特定用户和特定公司，并且仅适用于交互式会话。 若要使此功能可用，请按照下列步骤操作。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **用户参数** 对话框中，将 **显示文件生成时间** 选项设置为 **是**。

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>事件日志中的执行时间

1. 打开 Windows 事件查看器。
2. 在 **应用程序和服务日志** 下，打开 **Microsoft-Dynamics-ElectronicReporting/Operational**。
3. 查找其中 **EventID=2** 的 **FormatMapingRun** 事件，因为这些事件包含有关经过时间的信息。

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>跟踪分析程序跟踪 

因为 ER 在 X++ 中实现，因此您可以使用常见的 X++ 工具分析性能。 有关详细信息，请参阅[使用跟踪分析程序进行跟踪](../perf-test/trace-trace-tutorial.md)。

此方法有一些限制。 因为部分 ER 在 C# 中实现，因此并非所有详细信息都可用。 但是，您可以查看数据使用情况详细信息。 此外，长时间的报表运行可能会超出跟踪存储限制。

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER 跟踪

ER 可以收集自己的跟踪，并且它具有这些跟踪的可视化和分析工具。 有关详细信息，请参阅[跟踪 ER 格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)。

#### <a name="perfview"></a><a name="perfview"></a>PerfView

因为 X++ 和 ER 都在 .NET 平台顶部实现，因此您可以使用常见的 .NET 工具。 例如，您可以使用免费的 [PerfView](https://github.com/Microsoft/perfview) 工具。

您还可以从命令行收集数据。 例如，以下 Windows PowerShell 脚本收集执行时间，直到任何格式的执行在计算机上停止为止。

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

此方法有一些限制。 您必须对计算机具有管理访问权限。 此外，您必须是一名经验丰富的开发人员，因为这是一个陡峭的学习曲线。

### <a name="making-changes"></a><a name="making-changes"></a>进行更改

#### <a name="use-caching"></a><a name="use-caching"></a>使用缓存

虽然缓存减少了再次提取数据所需的时间量，但它会消耗内存。 在提取的数据量不是很大的情况下使用缓存。 有关显示如何使用缓存的详细信息和示例，请参阅[根据来自执行跟踪的信息改善模型映射](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)。

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a>减少提取的数据量

您可以通过限制运行时获取的应用程序表记录中的字段数来减少要缓存的内存消耗。 在这种情况下，您将只获取您在 ER 模型映射中需要的应用程序表的那些字段值。 将不会提取该表中的其他字段。 因此，缓存提取的记录所需的内存量将减少。 有关详细信息，请参阅[通过减少运行时获取的表字段的数量来提高 ER 解决方案的性能](er-reduce-fetched-fields-number.md)。

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>使用缓存的参数化计算字段

有时，必须反复查找值。 示例包括帐户名称和帐号。 为了帮助节省时间，您可以创建一个在顶层具有参数的计算字段，然后将该字段添加到缓存中。

我们建议您仅在缓存的数据大小较小时使用此方法。 有关详细信息，请参阅[通过添加参数化的计算字段数据源提高 ER 解决方案的性能](er-calculated-field-ds-performance.md)。

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>使用 JOIN 数据源

**JOIN** 数据源允许通过一个查询提取多个连接记录。 不必使用单独的查询来提取每个连接记录。 例如，如果您有 1,000 行，并且按关系提取每行的项目数据，您将有 1,001 个查询 (= 1,000 + 1)。 如果使用 **JOIN** 数据源，您将仅使用一个查询来提取相同的数据。 有关详细信息，请参阅[在 ER 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据](er-join-data-sources.md)。

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>使用 FILTER 函数而不是 WHERE 函数

**[FILTER](er-functions-list-filter.md)** 函数在 SQL Server 上运行条件，而 **WHERE** 函数从列表中提取所有数据（一次一条记录）并针对每条记录应用条件。 例如，您要从 1,000 条记录中选择一条记录。 如果使用 **WHERE**，将提取全部 1,000 条记录。 但是，如果使用 **FILTER**，将只提取一条记录。 **FILTER** 也可以在数据库端使用索引。

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>使用收集的数据函数或累积的数据数据源

如果您的配置具有之前按报表汇总了提取数据的 *分组依据* 组件，该组件将再次提取所有数据。 通过使用收集的数据函数，您可以使 ER 在第一次提取期间积累数据。 有关详细信息，请参阅 [ER 配置格式以进行计数和合计](tasks/er-format-counting-summing-2.md)。

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>在 X++ 中重写部分配置

ER 支持调用表和类的方法，包括扩展。 考虑在 X++ 中重写部分模型映射以帮助提高性能。

ER 可以使用来自以下来源的数据：

- 类（**对象** 和 **类** 数据源）
- 表（**表** 和 **表记录** 数据源）

[ER 应用程序编程接口 (API)](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) 还提供一种从调用代码发送预计算的数据的方法。 应用程序套件包含此方法的许多示例。
