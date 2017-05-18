---
title: "电子申报中的配方设计器"
description: "本主题说明如何在电子申报 (ER) 中使用配方设计器。 在您在 ER 中为特定电子文档设计格式时，您可以使用与 Microsoft Excel 类似的数据换算公式满足该文档的履行和格式的要求。 支持的各种函数类型 - 文本、日期和时间、数学逻辑、信息、数据类型转换和其他（企业域特定函数）。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 335a0d7ca466028e8b157cb4e04df7d0f4880e73
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>电子申报中的配方设计器

[!include[banner](../includes/banner.md)]


本主题说明如何在电子申报 (ER) 中使用配方设计器。 在您在 ER 中为特定电子文档设计格式时，您可以使用与 Microsoft Excel 类似的数据换算公式满足该文档的履行和格式的要求。 支持的各种函数类型 - 文本、日期和时间、数学逻辑、信息、数据类型转换和其他（企业域特定函数）。

<a name="formula-designer-overview"></a>配方设计器概述
-------------------------

电子申报 (ER) 支持配方设计器。 因此，在设计时间，您可以配置可用于运行时间以下任务的表达式：

-   将从 Microsoft Dynamics 365 for Operations 数据库接收的数据以及应填充的数据转换为设计作为 ER 格式的数据源的 ER 数据模型（筛选、分组、数据类型转换等）。
-   根据特定 ER 格式的布局和条件（根据请求的语言或文化、编码等）设置必须发送到生成的电子文档的数据的格式。
-   控制电子文档生成的过程（启用/禁用特定格式元素的输出，具体取决于处理数据、中断文档创建、丢弃最终用户的消息等）。

当您执行以下任何一项操作时，便可以打开配方设计器页：

-   数据源物料绑定到数据模型组件。
-   数据源物料绑定到格式组件。
-   完成作为数据源的一部分的计算字段的维护。
-   定义用户输入参数的可见性条件。
-   设计格式转换。
-   定义启用格式组件的条件。
-   定义格式的 FILE 组件的文件名。
-   定义流程控制验证的条件。
-   定义流程控制验证的消息文本。

## <a name="designing-er-formulas"></a>设计 ER 配方
### <a name="data-binding"></a>数据绑定

ER 配方设计器可以用于定义转换接收自数据源的数据的表达式，以便数据在运行时可以在数据用户中填充：

-   从 Dynamics 365 for Operations 数据源和运行时参数转换为 ER 数据模型。
-   从 ER 数据模型转换为 ER 格式。
-   从 Dynamics 365 for Operations 数据源和运行时参数转换为 ER 格式。

下图显示了此类表达式的设计。 在此示例中，表达式返回 Dynamics 365 for Operations **内部统计**表的 **Intrastat.AmountMST** 字段的值（在该值舍入到两位小数后）。 [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) 下图显示如何使用此类表达式。 在此示例中，设计的表达式的结果填充在**纳税申报模型**数据模型的 **Transaction.InvoicedAmount** 组件中。 [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) 在运行时，设计的配方，**ROUND (Intrastat.AmountMST, 2)** 会将**内部统计**表的每个记录的 **AmountMST** 字段的值舍入到两位小数，并将舍入值填充到**纳税申报**数据模型的 **Transaction.InvoicedAmount** 组件。

### <a name="data-formatting"></a>数据格式设置

ER 配方设计器可以用于定义确定接收自数据源的数据的格式的表达式，以便数据可以作为生成电子文档的一部分发送。 如果您具有必须应用为应为格式重复使用的典型规则，则可在设计格式配置中将它作为使用格式设置表达式的指定转换引入一次。 此指定的转换然后可链接到许多格式组件，这些组件是必须根据创建的表达式设置其输出的格式。 下图显示了此类转换的设计。 在此示例中，**TrimmedString** 转换获取**字符串**数据类型的传入数据，并在返回字符串值时截断前导和尾随空格。 [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) 下图显示了如何使用此类转换。 在此示例中，在运行时作为输出发送到生成电子文档的若干格式组件按名称引用 **TrimmedString** 转换。 [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) 在格式组件引用 **TrimmedString** 转换时（例如，上图中的 **partyName** 组件），它将文本作为输出发送至生成的文档。 文本不包括前导和尾随空格。 如果您具有必须单独应用的格式，可以将此格式作为特定格式组件绑定的单个表达式引入。 下图显示了此类表达式。 在此示例中，**partyType** 格式组件通过将数据源中 **Model.Company.RegistrationType** 字段的传入数据转换为大写文本并将该文本作为输出发送到电子文档的表达式绑定到数据源。 [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>流程控制

ER 配方设计器可用于定义控制生成文档的流程的表达式。 您可以:

-   定义确定必须停止文档创建流程的条件。
-   指定表达式，这些表达式将创建有关已停止流程的最终用户的消息或引发有关继续报表生成流程的执行日志消息。
-   指定生成文档的文件名并控制其创建的条件。

流程控制的每个规则设计为单个验证。 下图显示了此类验证。 此示例中是对配置的说明：

-   在 **INSTAT** 节点在生成 XML 文件时创建时，将对验证进行评估。
-   如果事务列表为空，验证将停止执行流程并返回 **FALSE**。
-   验证返回使用用户首选语言的包括标签 SYS70894 文本的错误消息。

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg)  ER 配方设计器还可用于指定文件名来生成电子文档和控制文件创建流程。 下图显示了此类流程控制的设计。 此示例中是对配置的说明：

-   来自 **model.Intrastat** 数据源的记录列表划分为多个批次，每个批次包含最多 1000 条记录。
-   输出创建以 XML 格式为创建的每个批次包含一个文件的压缩文件。
-   表达式通过连接文件名和文件扩展名返回生成电子文档的文件名。 对于第二个批次和所有后续的批次，文件名作为后缀包含批次 ID。
-   表达式为包含至少一条记录的批次启用（通过返回 **TRUE**）文件创建流程。

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>基本语法

ER 表达式可以包含任意或所有以下元素：

-   常量
-   运算符
-   引用
-   路径
-   功能

#### <a name="constants"></a>常量

您可以在设计表达式时使用文本和数值常量（未计算的值）。 例如，表达式 **VALUE ("100") + 20** 使用数值常量 20 和字符串常量“100”，返回数值 **120**。 ER 配方设计器支持转义序列，这意味着您可以指定应通过其他方式处理的表达式字符串。 例如，表达式 **"Leo Tolstoy ""War and Peace"" Volume 1"** 返回文本字符串 **Leo Tolstoy "War and Peace" Volume 1**。

#### <a name="operators"></a>运算符

下表显示您可以用于执行基本算术运算的算术运算符，例如加、减、除和乘。

| 操作员 | 含义              | 示例 |
|----------|----------------------|---------|
| +        | 增加额             | 1+2     |
| -        | 减法，负 | 5-2 -1  |
| \*       | 乘       | 7\*8    |
| /        | 分部             | 9/3     |

下表显示支持的且您可以用于比较两个值的比较运算符。

| 操作员 | 含义                  | 示例    |
|----------|--------------------------|------------|
| =        | 相等                    | X=Y        |
| &gt;     | 大于             | X&gt;Y     |
| &lt;     | 小于                | X&lt;Y     |
| &gt;=    | 大于等于 | X&gt;=Y    |
| &lt;=    | 小于等于    | X&lt;=Y    |
| &lt;&gt; | 不等于             | X&lt;&gt;Y |

此外，您可以使用和符号 (&) 作为文本连接运算符连接或连结一个或多个文本字符串到单个文本。

| 操作员 | 含义     | 示例                                        |
|----------|-------------|------------------------------------------------|
| &        | 连接 | “没有东西打印”和“：”和“未找到记录” |

#### <a name="operator-precedence"></a>运算符优先级

复合表达式部分评估的顺序很重要。 例如，先执行加运算还是除运算会影响表达式 **1 + 4 / 2** 的结果。 您可以使用括号明确定义表达式如何进行评估。 例如，要指示应首先执行加运算，您可以将之前的表达式修改为 **(1 + 4) / 2**。 如果在表达式中必须执行的运算的顺序未明确定义，顺序将基于分配给支持的运算符的默认优先级。 下表显示运算符和分配给每个运算符的优先级。 有较高优先级的运算符（例如，7）在具有较低优先级的运算符之前进行评估（例如，1）。

| 优先级 | 运算符      | 语法                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | 分组       | ( … )                                                    |
| 6          | 成员访问  | … 。 …                                                    |
| 5          | 函数调用  | … ( … )                                                  |
| 4          | 乘 | … \* … … / …                                             |
| 3          | 加法的       | … + … … - …                                              |
| 2          | 比较     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | 分隔     | … , …                                                    |

具有相同优先级的同一行上的运算符。 如果表达式包含多个运算符，表达式从左到右进行评估。 例如，表达式 **1 + 6 / 2 \* 3 &gt; 5** 返回 **true**。 我们建议您使用括号明确指示评估表达式的预期顺序，以使表达式更便于读取和维护。

#### <a name="references"></a>引用

在表达式设计期间当前 ER 组件（模型或格式）的所有数据源均可用作指定引用。 例如，当前的 ER 数据模型包含数据源 **ReportingDate** 数据源，该数据源返回 **DATETIME** 数据类型的值。 若要获取在生成文档中正确格式化的值，您可以按照如下方法在表达式中引用数据源：<**DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")** 不代表字母的引用数据源的名称中的所有字符必须前加单引号 (')。 如果引用数据源的名称包含至少一个不代表字母的符号（例如，标点符号或任何其他文字符号），名称必须以单引号括起。 下面举了一些示例加以说明：

-   **今日日期和时间**数据源必须在 ER 表达式中引用，如下所示：**“今日日期和时间”**
-   **Customers** 数据源的 **name()** 方法必须在 ER 表达式中引用，如下所示：**Customers.'name()'**

#### <a name="path"></a>路径

在表达式引用结构化的数据源时，可以使用路径定义选择该数据源的特定基本元素。 点字符 (.) 用于分离结构化数据源的各个元素。 例如，当前的 ER 数据模型包含 **InvoiceTransactions** 数据源，该数据源返回记录列表。 **InvoiceTransactions** 记录结构包含 **AmountDebit** 和 **AmountCredit** 字段，这两个字段将返回数值。 因此，您可以设计以下表达式来计算发票金额：**InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>功能

下一节介绍可用于 ER 表达式的函数。 根据调用函数参数的列表，可将表达式上下文（当前 ER 数据模型或 ER 格式）以及常量的所有数据源用作调用函数的参数。 例如，当前的 ER 数据模型包含 **InvoiceTransactions** 数据源，该数据源返回记录列表。 **InvoiceTransactions** 记录结构包含 **AmountDebit** 和 **AmountCredit** 字段，这两个字段将返回数值。 因此，若要计算发票金额，可以设计使用内置的 ER 舍入函数的以下表达式：**ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>支持的函数
以下各表介绍可用于设计 ER 数据模型和 ER 报表的数据处理函数。 此函数列表不是固定的，可由开发人员进行扩充。 若要查看您可以使用的功能的列表，请访问 ER 配方设计器中的功能窗格。

### <a name="date-and-time-functions"></a>日期和时间函数

| 职能                                   | 描述                                                                                                                                                                                                                                                                                                                                                      | 示例                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS（日期时间，天）                   | 添加指定的天数到指定的日期时间值。                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** 返回未来七天的日期和时间。                                                                                                                                                                                                                            |
| DATETODATETIME（日期）                      | 转换指定日期值为一个日期时间值。                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate()')** 返回当前的 Dynamics 365 for Operations 会话日期 12/24/2015 为 **12/24/2015 12:00:00 AM**。 在此示例中，**CompInfo** 为引用 CompanyInfo 表的 **Dynamics 365 for Operations/Table** 类型的 ER 数据源。 |
| NOW ()                                     | 返回当前的 Dynamics 365 for Operations 应用程序服务器日期和时间作为日期时间值。                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | 返回当前的 Dynamics 365 for Operations 应用程序服务器日期作为日期值。                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | 返回**空**日期值。                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | 返回**空**日期时间值。                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT（日期时间，格式）          | 转换指定的日期时间值为指定格式的字符串。 （有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)。）                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** 根据指定的自定义格式返回当前的 Dynamics 365 for Operations 应用程序服务器日期 12/24/2015 为 **"24-12-2015"**。                                                                                                          |
| DATETIMEFORMAT（日期时间，格式，区域性） | 转换指定的日期时间值为指定格式和[区域性](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)的字符串。 （有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)。） | **DATETIMEFORMAT (NOW(), "d", "de")** 根据所选的德国区域性返回当前的 Dynamics 365 for Operations 应用程序服务器日期 12/24/2015 为 **"24.12.2015"**。                                                                                                             |
| SESSIONTODAY ()                            | 返回当前的 Dynamics 365 for Operations 会话日期作为日期值。                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | 返回当前的 Dynamics 365 for Operations 会话日期和时间作为日期时间值。                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT（日期，格式）                  | 使用指定格式返回日期的字符串表示形式。                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** 根据指定的自定义格式返回当前的 Dynamics 365 for Operations 会话日期 12/24/2015 为 “**24-12-2015**”。                                                                                                                      |
| DATEFORMAT（日期，格式，区域性）         | 转换指定的日期值为指定格式和[区域性](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)的字符串。 （有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)。）     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** 根据所选的德国区域性返回当前的 Dynamics 365 for Operations 会话时间 12/24/2015 为 **“24.12.2015”**。                                                                                                                       |

### <a name="list-functions"></a>列表函数

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>职能</th>
<th>说明</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>拆分（输入，长度）</td>
<td>拆分指定的输入字符串为子字符串，每个子字符串具有指定的长度。 返回结果为新的列表。</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> 返回包含具有 <strong>STRING</strong> 字段的两个记录的新列表。 第一个记录中的字段包含文本 <strong>&quot;abc&quot;</strong>，第二个记录中的字段包含文本 <strong>&quot;d&quot;</strong>。</td>
</tr>
<tr class="even">
<td>拆分列表（列表，数字）</td>
<td>将指定的列表拆分为多个批次，每个批次包含指定的记录数。 返回结果为包含以下元素的批次的新列表：
<ul>
<li>作为常规列表的批次（<strong>值</strong>组件）</li>
<li>当前批处理号（<strong>BatchNumber</strong> 组件）</li>
</ul></td>
<td>在以下示例中，<strong>行</strong>数据源作为三个记录的记录列表创建，并划分为多个批次，每个批次最多包含两个记录。 <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> 它显示了设计的格式布局，在其中创建与<strong>行</strong>数据源的绑定来生成以此格式呈现每个批次和记录的单个节点的 XML 格式的输出。 <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> 以下是运行设计的格式的结果。 <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST（记录 1 [，记录 2，...]）</td>
<td>返回从指定的参数创建的新列表。</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> 返回空记录，在其中字段列表包含 <strong>MainData</strong> 和 <strong>OtherData</strong> 记录列表的所有字段。</td>
</tr>
<tr class="even">
<td>LISTJOIN（列表 1，列表 2，...）</td>
<td>返回从指定的参数列表的连接列表。</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> 返回六个记录的列表，在其中 <strong>STRING</strong> 数据类型的一个字段包含一个字母。</td>
</tr>
<tr class="odd">
<td>ISEMPTY（列表）</td>
<td>如果指定的列表不包含任何元素，返回 <strong>TRUE</strong>。 否则，返回 <strong>FALSE</strong>。</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST（列表）</td>
<td>通过使用指定的列表返回空列表为列表结构的来源。</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> 返回具有与 <strong>SPLIT</strong> 函数返回的列表相同结构的新空列表。</td>
</tr>
<tr class="odd">
<td>FIRST（列表）</td>
<td>如果该记录不为空，返回指定列表的第一个记录。 否则，将引发异常。</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL（列表）</td>
<td>如果该记录不为空，返回指定列表的第一个记录。 否则，将返回<strong>空</strong>记录。</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM（列表）</td>
<td>返回仅包含指定列表的第一项的列表。</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS（路径）</td>
<td>返回表示匹配指定路径的所有项的新的平展表。 路径必须定义为到记录列表数据类型的数据源元素的有效的数据源路径。 字符串、日期路径等数据元素应在 ER 表达式生成器中设计时引发错误。</td>
<td>如果您输入 <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> 为数据源 (DS)，<strong>COUNT( ALLITEMS (DS.Value))</strong> 返回 <strong>3</strong>。</td>
</tr>
<tr class="odd">
<td>ORDERBY（列表 [，表达式 1，表达式 2，...]）</td>
<td>返回指定的列表，其根据指定可以定义为表达式的指定参数排序。</td>
<td>在<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源时，<strong>ORDERBY (Vendors, Vendors.'name()')</strong> 返回升序排列的按名称排序的供应商列表。</td>
</tr>
<tr class="even">
<td>REVERSE（列表）</td>
<td>以反转排序顺序返回指定的列表。</td>
<td>在<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源时，<strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> 返回降序排列的按名称排序的供应商列表。</td>
</tr>
<tr class="odd">
<td>WHERE（列表，条件）</td>
<td>返回指定的列表，其根据指定的条件进行筛选。 不同于<strong>筛选器</strong>功能，指定条件应用于内存中的列表。</td>
<td>在<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源时，<strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> 返回属于供应商组 40 的供应商列表。</td>
</tr>
<tr class="even">
<td>ENUMERATE（列表）</td>
<td>返回包括指定列表的枚举记录并显示以下元素的新列表：
<ul>
<li>作为常规列表的指定列表记录（<strong>值</strong>组件）</li>
<li>当前记录索引（<strong>编号</strong>组件）</li>
</ul></td>
<td>在以下示例中，<strong>枚举</strong>数据源创建为引用 <strong>VendTable</strong> 表的<strong>供应商</strong>数据源的供应商记录的枚举列表。 <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>这里是格式，其中创建数据绑定来作为枚举节点生成呈现单个供应商的 XML 格式的输出。 <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> 这是运行设计的格式的结果。 <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT（列表）</td>
<td>如果列表不为空，返回指定列表中的记录数。 否则，返回 <strong>0</strong>（零）。</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> 返回 <strong>2</strong>，因为 <strong>SPLIT</strong> 函数创建包含两个记录的列表。</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS（路径）</td>
<td>返回从以下其中一种类型的参数创建的记录列表：
<ul>
<li>模型枚举</li>
<li>格式枚举</li>
<li>集装箱</li>
</ul>
创建的列表将包括具有以下字段的记录：
<ul>
<li>姓名</li>
<li>标签</li>
<li>说明</li>
</ul>
“标签”和“说明”字段将基于格式的语言设置在运行时值返回。</td>
<td>以下示例显示在数据模型中引入的枚举。 <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a> 将显示以下示例：
<ul>
<li>作为数据源插入报表的模型枚举。</li>
<li>设计为使用模型枚举作为此功能参数的 ER 表达式。</li>
<li>使用创建的 ER 表达式插入报表中的记录列表类型的数据源。</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>  以下示例显示了绑定到使用 LISTOFFIELDS 功能创建的记录列表类型的数据源的 ER 格式元素。<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>这是设计的格式执行的结果。<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>注意：:</strong>翻译的标签和说明文本根据为父 FILE 和 FOLDER 格式元素配置的语言设置填充到 ER 格式输出。</td>
</tr>
<tr class="odd">
<td>STRINGJOIN（列表、字段名称，分隔符）</td>
<td>从使用选定的分隔符分隔的列表中返回字段的串联值字符串。</td>
<td>如果输入 SPLIT(“abc” , 1) 作为数据源 DS，表达式 STRINGJOIN (DS, DS.Value, “:”) 返回 “a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT（列表、限值，源限制）</td>
<td>将特定列表拆分为由子列表组成的新列表，并将结果返回到记录列表目录中。 限值参数指定拆分原始列表的限值。 限制源参数指定增加总和的步骤。 当限值源超过定义的限值时，限值不适用于给定列表的单个项目。</td>
<td>以下示例显示了使用数据源的示例格式。 <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>这是显示商品项目简单列表的结果格式执行。<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>以下示例显示了单个批次必须包括总重不超过限值 9 的商品时，用来显示商品项目列表的调整后的相同格式。<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>这是调整后的格式执行的结果。 <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>注意：</strong>此限值不适用于原始列表的最后一个项目，因为其限值源（重量）的值 (11) 超过定义的限值 (9)。 在报表生成过程中（如有必要）使用相应格式元素的函数 <strong>WHERE</strong> 或 <strong>Enabled</strong> 表达式忽略（跳过）子列表。</td>
</tr>
<tr class="odd">
<td>FILTER（列表，条件）</td>
<td>返回通过修改查询为指定条件进行筛选的特定列表。 不同于 <strong>WHERE</strong> 函数，指定条件适用于表格记录类型的任何 ER 数据源的数据库级别。</td>
<td>当<strong>供应商</strong>配置为引用 <strong>VendTable</strong> 表的 ER 数据源时，FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) 返回仅属于供应商组“40”的供应商列表。</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>逻辑函数

| 职能                                                                                | 说明                                                                                                                                                                                                                                                                     | 示例                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (expression, option 1, result 1 \[, option 2, result 2\] ... \[, default result\]) | 根据指定的备选选项评估指定的表达式值。 返回与表达式的值相等的选项的结果。 否则，将返回可以选择输入的默认结果（前面不加选项的最后一个参数）。 | 当前 Dynamics 365 for Operations 会话日期为 10 月至 12 月之间时，**CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** 返回字符串 **"WINTER"**。 否则，它返回一个空字符串。 |
| IF（条件，值 1，值 2）                                                        | 在满足指定条件时，返回指定值 1。 否则，返回值 2。 如果值 1 和值 2 是记录或记录列表，结果将只包含两个列表都存在的字段。                                                                     | **IF (1=2, "condition is met", "condition is not met")** 返回字符串 **"condition is not met"**。                                                                                                                                                      |
| NOT（条件）                                                                         | 返回指定条件的冲销逻辑值。                                                                                                                                                                                                                   | **NOT (TRUE)** 返回 **FALSE**。                                                                                                                                                                                                                            |
| AND (condition 1\[, condition 2, ...\])                                                 | 如果指定的*所有*条件均为 True，返回 **TRUE**。 否则，返回 **FALSE**。                                                                                                                                                                                            | **AND (1=1, "a"="a")** 返回 **TRUE**。 **AND (1=2, "a"="a")** 返回 **FALSE**。                                                                                                                                                                           |
| OR (condition 1\[, condition 2, ...\])                                                  | 如果指定的*所有*条件均为 False，返回 **FALSE**。 如果指定的*任何*条件均为 True，返回 **TRUE**。                                                                                                                                                                 | **OR (1=2, "a"="a")** 返回 **TRUE**。                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>数学函数

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>职能</th>
<th>描述</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS（数字）</td>
<td>返回指定数值的绝对值（不带符号的数值）。</td>
<td><strong>ABS (-1)</strong> 返回 <strong>1</strong>。</td>
</tr>
<tr class="even">
<td>POWER（数字，功率）</td>
<td>返回将指定的正数增加到指定的功率的结果。</td>
<td><strong>POWER (10, 2)</strong> 返回 <strong>100</strong>。</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE（字符串，小数分隔符，数字分组分隔符）</td>
<td>将指定的字符串转换为数字。 指定的符号用于分隔十进制数的的整数和小数部分，并且也使用指定的千位分隔符。</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> 返回值 <strong>1234.56</strong>。</td>
</tr>
<tr class="even">
<td>VALUE（字符串）</td>
<td>将指定的字符串转换为数字。 逗号和点字符 (.) 被视为小数分隔符，前导连字符 (-) 用作负号。 如果其他非数值字符在指定字符串中出现，将引发异常。</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> 引发异常。</td>
</tr>
<tr class="odd">
<td>ROUND（数字，小数位）</td>
<td>返回指定的数值，其舍入到指定的小数位数：
<ul>
<li>如果指定的小数值大于 0（零），则指定的数值舍入到指定的小数位数。</li>
<li>如果指定的小数值为 0（零），则指定的数值舍入到最近的整数。</li>
<li>如果指定的小数值小于 0（零），则指定的数值舍入到小数点左边。</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> 舍入到两位小数，返回 <strong>1200.77</strong>。 <strong>ROUND (1200.767, -3)</strong> 舍入到最接近的 1,000 的倍数，返回 <strong>1000</strong>。</td>
</tr>
<tr class="even">
<td>ROUNDDOWN（数字，小数位）</td>
<td>返回指定的数值，其向下舍入（向零舍入）到指定的小数位数。 <strong>注意：</strong>此函数类似 <strong>ROUND</strong>，但始终向下舍入到指定的数字。</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> 向下舍入到两位小数，返回 <strong>1200.76</strong>。 <strong>ROUNDDOWN (1700.767, -3)</strong> 向下舍入到最接近的 1,000 的倍数，返回 <strong>1000</strong>。</td>
</tr>
<tr class="odd">
<td>ROUNDUP（数字，小数位）</td>
<td>返回指定的数值，其向上舍入（离零舍入）到指定的小数位数。 <strong>注意：</strong>此函数类似 <strong>ROUND</strong>，但始终向上舍入到指定的数字。</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> 向上舍入到两位小数，返回 <strong>1200.77</strong>。 <strong>ROUNDUP (1200.767, -3)</strong> 向上舍入到最接近的 1,000 的倍数，返回 <strong>2000</strong>。</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>记录函数

| 职能             | 描述                                                                                                                                                                                                                                     | 示例                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER（列表） | 返回与指定的记录列表或记录具有相同结构的**空**记录。 **注意：**此函数已废弃。 使用 **EMPTYRECORD**。                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** 返回具有与 **SPLIT** 函数返回的列表相同结构的新空记录。 |
| EMPTYRECORD（记录） | 返回与指定的记录列表或记录具有相同结构的**空**记录。 **注意：****空**记录是所有字段为空值的记录（**0** \[zero\] 表示数字，空字符串表示字符串等）。 | **EMPTYRECORD (SPLIT ("abc", 1))** 返回具有与 **SPLIT** 函数返回的列表相同结构的新空记录。   |

### <a name="text-functions"></a>文本函数

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>职能</th>
<th>描述</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER（字符串）</td>
<td>返回指定字符串，其转换为大写字母。</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> 返回 <strong>&quot;SAMPLE&quot;</strong>。</td>
</tr>
<tr class="even">
<td>LOWER（字符串）</td>
<td>返回指定字符串，其转换为小写字母。</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> 返回 <strong>&quot;sample&quot;</strong>。</td>
</tr>
<tr class="odd">
<td>LEFT（字符串，字符数）</td>
<td>从指定字符串的开头返回指定数目的字符。</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> 返回 <strong>&quot;Sam&quot;</strong>。</td>
</tr>
<tr class="even">
<td>RIGHT（字符串，字符数）</td>
<td>从指定字符串的结尾返回指定数目的字符。</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> 返回 <strong>&quot;ple&quot;</strong>。</td>
</tr>
<tr class="odd">
<td>MID（字符串，起始位置，字符数）</td>
<td>从指定位置开始返回指定字符串的指定数目的字符。</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> 返回 <strong>&quot;amp&quot;</strong>。</td>
</tr>
<tr class="even">
<td>LEN（字符串）</td>
<td>返回指定字符串中的字符数。</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> 返回 <strong>6</strong>。</td>
</tr>
<tr class="odd">
<td>CHAR（数字）</td>
<td>返回指定的 Unicode 数值引用的字符的字符串。</td>
<td><strong>CHAR (255)</strong> 返回 <strong>&quot;ÿ&quot;</strong>。 <strong>注意：</strong> 返回的字符串取决于在父 FILE 格式元素中选择的编码。 受支持的编码列表可以在<a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">编码类</a>主题中找到。</td>
</tr>
<tr class="even">
<td>CONCATENATE（字符串 1 [，2，…]）</td>
<td>返回所有指定的文本字符串，其连接到一个字符串。</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong>返回 <strong>&quot;abcdef&quot;</strong>。 <strong>注意：</strong>表达式 <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> 也返回 <strong>&quot;abcdef&quot;</strong>。</td>
</tr>
<tr class="odd">
<td>TRANSLATE（字符串，模式，替换）</td>
<td>返回指定串字符，在其中所有在指定模式字符串中出现的字符由指定替换字符相应位置的字符替换。</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> 将模式 <strong>&quot;cd&quot;</strong> 替换为字符串 <strong>&quot;GH&quot;</strong>，并返回 <strong>&quot;abGHef&quot;</strong>。</td>
</tr>
<tr class="even">
<td>REPLACE（字符串，模式，替换，正则表达式标志）</td>
<td>在指定的正则表达式标志为 <strong>True</strong> 时，返回指定字符串，其通过应用指定为此函数的模式参数的正则表达式来修改。 此表达式用于查找必须替换的字符。 指定的替换参数的字符用于替换找到的字符。 在指定的正则表达式标志为 <strong>False</strong> 时，此函数类似 <strong>TRANSLATE</strong>。</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> 应用删除所有非数字符号的正则表达式，并返回 <strong>&quot;19234564971&quot;</strong>。 <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> 将模式 <strong>&quot;cd&quot;</strong> 替换为字符串 <strong>&quot;GH&quot;</strong>，并返回 <strong>&quot;abGHef&quot;</strong>。</td>
</tr>
<tr class="odd">
<td>TEXT（输入）</td>
<td>返回指定的输入，其转换为根据当前 Dynamics 365 for Operations 实例的服务器区域设置设置格式的文本字符串。 对于 <strong>real</strong> 类型的值，字符串转换被限制为两位小数。</td>
<td>如果 Dynamics 365 for Operations 实例服务器区域设置被定义为 <strong>EN-US</strong>，则 <strong>TEXT (NOW ())</strong> 返回当前 Dynamics 365 for Operations 会话日期 12/17/2015 为文本字符串 <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>。 <strong>TEXT (1/3)</strong> 返回 <strong>&quot;0.33&quot;</strong>。</td>
</tr>
<tr class="even">
<td>FORMAT（字符串 1，字符串 2 [，字符串 3，...]）</td>
<td>返回指定字符串，其通过代替任何出现的带有 <em>n</em> 参数的 <strong>%N</strong> 设置格式。 这些参数是字符串。 如果参数不是为参量提供，则参量在字符串中返回为 <strong>&quot;%N&quot;</strong>。 对于 <strong>real</strong> 类型的值，字符串转换被限制为两位小数。</td>
<td>在此示例中，数据源 <strong>PaymentModel</strong> 通过<strong>客户</strong>组件返回客户记录列表，通过 <strong>ProcessingDate</strong> 字段返回处理日期值。 <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> 在指定用于为所选客户生成电子文件的 ER 格式中，<strong>PaymentModel</strong> 被选择为数据源并控制流程。 当所选客户在处理报表的日期停止时，将引发最终用户异常。 为此类处理控制设计的配方可以使用以下资源：
<ul>
<li>Dynamics 365 for Operations 标签 SYS70894，具有以下文本：
<ul>
<li><strong>对于 EN-US 语言：</strong>&quot;Nothing to print&quot;</li>
<li><strong>对于 DE 语言：</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations 标签 SYS18389，具有以下文本：
<ul>
<li><strong>对于 EN-US 语言：</strong>&quot;Customer %1 is stopped for %2&quot;。</li>
<li><strong>对于 DE 语言：</strong>&quot;Debitor '%1' wird für %2 gesperrt&quot;。</li>
</ul></li>
</ul>
这是一个可设计的公式：FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;。 &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) 如果报表于 2015 年 12 月 17 日为 <strong>Litware 零售客户</strong>处理，在 <strong>EN-US</strong> 区域性和 <strong>EN-US</strong> 语言中，此公式返回以下文本，其可能呈现为最终用户的异常消息：&quot;Nothing to print。 客户 Litware 零售已于 2015 年 12 月 17 日停止。&quot; 如果 2015 年 12 月 17 日为 <strong>Litware 零售客户</strong>处理同一个报表，在 <strong>DE</strong> 区域性和 <strong>DE</strong> 语言中，此公式返回以下文本（使用不同的日期格式）：&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt。&quot; <strong>注意：</strong>以下语法在标签的 ER 公式中应用：
<ul>
<li><strong>对于 Dynamics 365 for Operations 资源的标签：</strong> <strong>@&quot;X&quot;</strong>，其中 X 是应用程序对象树 (AOT) 中的标签 ID</li>
<li><strong>对于位于 ER 配置中的标签：</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>，其中 X 是 ER 配置中的标签 ID</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT（数字，格式）</td>
<td>以指定格式返回指定数值的字符串表示形式。 （有关支持的格式的信息，请参阅<a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">标准</a>和<a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">自定义</a>。）此函数在其中运行的环境确定设置数字格式的区域性。</td>
<td>对于 EN-US 区域性，<strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> 返回 <strong>&quot;45.00 %&quot;</strong>。 <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> 返回 <strong>&quot;10&quot;</strong>。</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT（数字，语言，币种，打印币种名称标志，小数点）</td>
<td>返回拼写（转换）成指定语言的文本字符串的数字。 语言代码可选：定义为空字符串时，将使用运行上下文语言代码（为生成文件夹或文件定义）。 币种代码可选。 定义为空字符串时，采用公司币种。 注意，仅分析以下语言代码的<strong>打印币种名称</strong>参数和<strong>小数点</strong>参数：<strong>CS</strong>、<strong>ET</strong>、<strong>HU</strong>、<strong>LT</strong>、<strong>LV</strong>、<strong>PL</strong>、<strong>RU</strong>。 请注意，仅对国家/地区上下文支持币种偏差的 Dynamics 365 for Operations 公司分析<strong>打印币种名称</strong>参数。</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) 返回“One Thousand Two Hundred Thirty Four and 56”，NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) 返回“Sto dwadzieścia”，NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) 返回“Сто двадцать евро 21 евроцент”</td>
</tr>
<tr class="odd">
<td>PADLEFT（字符串，长度，填充字符）</td>
<td>返回指定长度的字符串，其中当前字符串的开头是使用指定字符填充的。</td>
<td>PADLEFT (“1234”, 10, “ “) 返回字符串 “      1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>数据收集功能

职能

说明

示例

FORMATELEMENTNAME ()

返回当前格式的元素的名称。 在当前文件的标记**收集输出详细信息**关闭时返回空字符串。

请参阅**盘点和合计格式输出的 ER 使用数据**（**购置/开发 IT 服务/解决方案组件**业务流程的一部分）任务指南了解有关这些功能使用的更多信息。

SUMIFS (key string for summing, criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\])

返回 XML 节点（具有定义为键的名称）值的总和，该总和在此格式执行期间收集且满足输入的条件（范围和值配对）。 在当前文件的标记**收集输出详细信息**关闭时返回零值。

SUMIF（要合计的键字符串，条件范围字符串，条件值字符串）

返回 XML 节点（具有定义为键的名称）值的总和，该总和在此格式执行期间收集且满足输入的条件（范围和值）。 关闭标记当前文件的**收集输出详细信息**时，返回零值。

COUNTIFS (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\])

返回 XML 节点的数量，该数量在此格式执行期间收集且满足输入的条件（范围和值配对）。 关闭标记当前文件的**收集输出详细信息**时，返回零值。

COUNTIF（范围条件字符串，条件值字符串）

返回 XML 节点的数量，该数量在此格式执行期间收集且满足输入的条件（范围和值）。 关闭标记当前文件的**收集输出详细信息**时，返回零值。

COLLECTEDLIST (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\])

返回 XML 节点值的列表，该列表在此格式执行期间收集且满足输入的条件（范围和值）。 在当前文件的标记**收集输出详细信息**关闭时返回空列表。

### <a name="other-business-domainspecific-functions"></a>其他（业务域特定的）函数

| 职能                                                                         | 说明                                                                                                                                                                                                                                                        | 示例                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY（金额，源币种，目标币种，日期，格式）        | 通过使用指定日期的指定 Dynamics 365 for Operations 公司的设置，将指定的货币金额从源币种转换为目标币种。                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** 基于 DEMF 公司的设置返回当前会话日期一欧元的等额美元。                                                                                                                                  |
| ROUNDAMOUNT（数字，小数位，舍入规则）                                       | 根据指定的舍入规则和指定小数位数舍入指定金额。 **注意：**舍入规则必须指定为 Dynamics 365 for Operations **RoundOffType** 枚举的值。                          | 如果 **model.RoundOff** 参数设置为 ****Downward****，**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** 返回值 **1000.78**。 如果 **model.RoundOff** 参数设置为 **Normal** 或 **Rounding-up**，**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** 返回值 **1000.79**。 |
| CURCredRef（位数）                                                              | 基于指定发票编号的数字返回贷方引用。                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** 返回 **"2200002"**。                                                                                                                                                                                                                                                         |
| MOD\_97（位数）                                                                 | 基于指定发票编号的数字返回贷方引用为 MOD97 表达式。                                                                                                                                                            | **MOD\_97 ("VEND-200002")** 返回 **"20000285"**。                                                                                                                                                                                                                                                           |
| ISOCredRef（位数）                                                              | 基于指定发票编号的数字和字母符号返回 ISO 贷方引用。 **注意：**若要从不是 ISO 兼容的字母表中清除符号，输入参数必须在传递给此函数前转换。 | **ISOCredRef ("VEND-200002")** 返回 **"RF23VEND-200002"**。                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID （字符串，数字）                                  | 获取额外财务维度 ID。 维度在此字符串中显示为以逗号分隔的 ID。 数字定义所请求的维度在此字符串中的序列代码。                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) 返回“CC”                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | 返回当前登录的公司的代码。                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10（位数）                                                       | 基于指定发票编号的数字返回贷方引用为 MOD10 表达式。                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") 返回 3                                                                                                                                                                                                                                                                   |
| FA\_SUM（固定资产代码，值模型代码，开始日期，结束日期）               | 返回固定资产金额在一段期间的已准备的数据容器。                                                                                                                                                                                         | FA\_SUM ("COMP-000001", “Current”, Date1, Date2) 返回具有值模型 “Current” 的固定资产 "COMP-000001" 从日期 1 到日期 2 期间的已准备的数据容器。                                                                                                                        |
| FA\_BALANCE（固定资产代码，值模型代码，报告年度，报告日期） | 返回固定资产余额的准备的数据容器。 报告年度必须指定为 Dynamics 365 for Operations 枚举 **AssetYear** 的值。                                                                                           | FA\_SUM ("COMP-000001", “Current”, AxEnumAssetYear.ThisYear, SESSIONTODAY ()) 返回具有值模型 “Current” 的固定资产 "COMP-000001" 的余额在当前 365 for Operations 会话日期的准备的数据容器。                                                                |

### <a name="functions-list-extension"></a>函数的列表扩展

ER 允许您扩展 ER 表达式中使用的函数列表的功能。 需要执行一些工程工作。 有关详细信息，请参阅[扩展电子申报查询功能的列表](general-electronic-reporting-formulas-list-extension.md)。

<a name="see-also"></a>请参阅
--------

[电子申报概览](general-electronic-reporting.md)

[扩展电子申报 (ER) 功能的列表](general-electronic-reporting-formulas-list-extension.md)




