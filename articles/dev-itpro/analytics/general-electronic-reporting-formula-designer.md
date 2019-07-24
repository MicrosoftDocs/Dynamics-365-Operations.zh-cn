---
title: 电子申报中 (ER) 的配方设计器
description: 本主题说明如何在电子申报 (ER) 中使用配方设计器。
author: NickSelin
manager: AnnBe
ms.date: 05/14/2014
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f8461f851f6f54def8a04d0f2548961b9a1ca4d
ms.sourcegitcommit: ce84a1faeda6013ef6a90038d811a72f375b604e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "1625864"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>电子申报中 (ER) 的配方设计器

[!include [banner](../includes/banner.md)]

本主题说明如何在电子申报 (ER) 中使用配方设计器。 在您在 ER 中为特定电子文档设计格式时，您可以使用公式转换数据，以便使其满足该文档的履行和格式的要求。 这些公式类似 Microsoft Excel 中的公式。 公式中支持各种函数类型：文本、日期和时间、数学、逻辑、信息、数据类型转换和其他（企业域特定函数）。

## <a name="formula-designer-overview"></a>配方设计器概述

ER 支持公式设计器。 因此，在设计时，您可以配置在运行时可用于执行以下任务的表达式：

- 将从 Microsoft Dynamics 365 for Finance and Operations 数据库接收的数据以及应输入的数据转换为设计作为 ER 格式的数据源的 ER 数据模型。 （例如，这些转换可以包括筛选、分组和数据转换类型。）
- 设置必须发送到生成电子单据的数据的格式，以便满足特定 ER 格式的布局和条件。 （例如，可以根据请求的语言、文化或编码完成格式化）。
- 控制电子单据的创建过程。 （例如，表达式可根据处理数据启用或禁用该格式的特定元素的输出。 还可以中断单据创建过程，或向用户显示消息。）

执行以下任何操作时，可打开**公式设计器**页面：

- 数据源物料绑定到数据模型组件。
- 数据源物料绑定到格式组件。
- 完成作为数据源的一部分的计算字段的维护。
- 定义用户输入参数的可见性条件。
- 设计格式转换。
- 定义启用格式组件的条件。
- 定义格式的 FILE 组件的文件名。
- 定义流程控制验证的条件。
- 定义流程控制验证的消息文本。

## <a name="designing-er-formulas"></a>设计 ER 配方

### <a name="data-binding"></a>数据绑定

ER 公式设计器可以用于定义转换接收自数据源的数据的表达式，以便数据在运行时可以在数据用户中输入数据：

- 从 Finance and Operations 数据源和运行时参数转换为 ER 数据模型
- 从 ER 数据模型转换为 ER 格式
- 从 Finance and Operations 数据源和运行时参数转换为 ER 格式

下图显示了此类表达式的设计。 在此示例中，表达式将 Finance and Operations 内部统计表的 **Intrastat.AmountMST** 字段的值舍入到两位小数，然后返回舍入值。

[![数据绑定](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

下图显示了如何使用此类表达式。 在此示例中，设计的表达式的结果输入在**纳税申报模型**数据模型的 **Transaction.InvoicedAmount** 组件中。

[![使用的数据绑定](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

运行时，设计的公式 **ROUND (Intrastat.AmountMST, 2)** 将内部统计表中各记录的 **AmountMST** 字段的值舍入为两位小数。 然后在**纳税申报**数据模型的 **Transaction.InvoicedAmount** 组件中输入舍入后的值。

### <a name="data-formatting"></a>数据格式设置

ER 配方设计器可以用于定义确定接收自数据源的数据的格式的表达式，以便数据可以作为生成电子文档的一部分发送。 可能必须将格式设置作为应对某种格式重复使用的典型规则来应用。 在这种情况下，可将该格式设置在格式配置中引入一次，作为具有格式设置表达式的指定转换。 此指定的转换然后可链接到许多格式组件，这些组件是必须根据创建的格式表达式设置其输出的格式。

下图显示了此类转换的设计。 在此示例中，**TrimmedString** 转换通过去除前导空格和尾随空格截断**字符串**数据类型的传入数据。 然后返回截断后的字符串值。

[![转换](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

下图显示了如何使用此类转换。 在此示例中，若干格式组件在运行时将文本作为输出发送到生成电子单据。 所有这些组件名义上引用 **TrimmedString** 转换。

[![正在使用的转换](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

上图中 **partyName** 组件之类格式组件引用 **TrimmedString** 转换时，该转换将把文本作为输出发送到生成电子单据。 此文本中不包含前导空格和尾随空格。

如果您具有必须单独应用的格式，可以将此格式作为特定格式组件绑定的单个表达式引入。 下图显示了此类表达式。 在此示例中，**partyType** 格式组件通过将数据源中 **Model.Company.RegistrationType** 字段的传入数据转换为大写文本的表达式绑定到数据源。 然后，该表达式将该文本作为输出发送到电子单据。

[![将格式应用于单个组件](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>流程控制

ER 格式设计器可用于定义控制生成电子单据的流程的表达式。 您可以执行以下任务：

- 定义确定必须停止文档创建流程的条件。
- 指定表达式，这些表达式将创建有关已停止流程的用户的消息或引发有关继续报表生成流程的执行日志消息。
- 指定生成电子单据的文件名并控制其创建的条件。

流程控制的每个规则设计为单个验证。 下图显示了此类验证。 此示例中是对配置的说明：

- 在 **INSTAT** 节点在生成 XML 文件期间创建时，将对验证进行评估。
- 如果事务列表为空，验证将停止执行流程并返回 **FALSE**。
- 验证返回使用用户首选语言的包括 Finance and Operations 标签 SYS70894 文本的错误消息。

[![验证](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER 配方设计器还可用于生成文件名来生成电子单据和控制文件创建流程。 下图显示了此类流程控制的设计。 此示例中是对配置的说明：

- **model.Intrastat** 数据源的记录列表拆分为多个批次。 每个批次最多包含 1,000 条记录。
- 输出创建以 XML 格式为创建的每个批次包含一个文件的压缩文件。
- 表达式通过连接文件名和文件名扩展返回生成电子文档的文件名。 对于第二个批次和所有后续的批次，文件名作为后缀包含批次 ID。
- 表达式为包含至少一条记录的批次启用（通过返回 **TRUE**）文件创建流程。

[![文件控制](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>基本语法

ER 表达式可以包含任意或所有以下元素：

- 常量
- 运算符
- 参考
- 路径
- 功能

#### <a name="constants"></a>常量

您可以在设计表达式时使用文本和数值常量（即未计算的值）。 例如，表达式 **VALUE ("100") + 20** 使用数值常量 **20** 和字符串常量 **100**，返回数值 **120**。 ER 公式设计器支持转义序列。 因此，可以指定应以不同方式处理的表达式字符串。 例如，表达式 **"Leo Tolstoy ""War and Peace"" Volume 1"** 返回文本字符串 **Leo Tolstoy "War and Peace" Volume 1**。

#### <a name="operators"></a>运算符

下表显示您可以用于执行基本算术运算的算术运算符，例如加、减、乘和除。

| 操作员 | 含义               | 示例 |
|----------|-----------------------|---------|
| +        | 增加额              | 1+2     |
| -        | 减法，负 | 5-2，-1 |
| \*       | 乘        | 7\*8    |
| /        | 分部              | 9/3     |

下表显示支持的比较运算符。 您可以使用这些运算符比较两个值。

| 操作员 | 含义                  | 示例    |
|----------|--------------------------|------------|
| =        | 相等                    | X=Y        |
| &gt;     | 大于             | X&gt;Y     |
| &lt;     | 小于                | X&lt;Y     |
| &gt;=    | 大于等于 | X&gt;=Y    |
| &lt;=    | 小于等于    | X&lt;=Y    |
| &lt;&gt; | 不等于             | X&lt;&gt;Y |

也可以将星号 (&) 用作文本连接运算符。 这样就可以将一个或多个文本字符串联接或连接为一段文本。

| 操作员 | 含义     | 示例                                             |
|----------|-------------|-----------------------------------------------------|
| &        | 连接 | "没有东西打印" & ":&nbsp;" & "未找到记录" |

##### <a name="operator-precedence"></a>运算符优先级

复合表达式部分评估的顺序很重要。 例如，表达式 **1 + 4 / 2** 的结果根据先执行加运算还是除运算有所不同。 您可以使用括号明确定义表达式如何进行评估。 例如，要指示应首先执行加运算，您可以将之前的表达式更改为 **(1 + 4) / 2**。 如果不在表达式中明确指定运算顺序，顺序将基于分配给支持的运算符的默认优先级。 下表显示分配给每个运算符的优先级。 有较高优先级的运算符（例如，7）在具有较低优先级的运算符之前进行评估（例如，1）。

| 优先级 | 运算符      | 语法                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | 分组       | ( … )                                                                   |
| 6          | 成员访问  | … 。 …                                                                   |
| 5          | 函数调用  | … ( … )                                                                 |
| 4          | 乘 | … \* …<br>… / …                                                         |
| 3          | 加法的       | … + …<br>… - …                                                          |
| 2          | 比较     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | 分隔     | … , …                                                                   |

如果表达式中包含多个具有相同优先级的连续运算符，将从左到右执行这些运算。 例如，表达式 **1 + 6 / 2 \* 3 &gt; 5** 返回 **true**。 我们建议您使用括号明确指示评估表达式中所需的运算顺序，以使表达式更便于读取和维护。

#### <a name="references"></a>参考

在表达式设计期间当前 ER 组件的所有数据源均可用作指定引用。 （当前 ER 组件可以是模型或格式。）例如，当前的 ER 数据模型包含 **ReportingDate** 数据源，并且该数据源返回 **DATETIME** 数据类型的值。 若要获取在生成文档中正确格式化的值，您可以按照如下方法在表达式中引用数据源：**DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**。

不代表字母的引用数据源的名称中的所有字符必须前加单引号 (')。 如果引用数据源的名称包含至少一个不代表字母的符号，名称必须以单引号括起。 （例如，这些非字母符号可以是标点符号或其他书面符号。）下面是一些示例：

- **今日日期和时间**数据源必须在 ER 表达式中引用，如下所示：**今日日期和时间**。
- **Customers** 数据源的 **name()** 方法必须在 ER 表达式中引用，如下所示：**Customers.'name()'**。

如果 Finance and Operations 数据源的方法有参数，则使用下面的语法调用这些方法：

- 如果 **System** 数据源的 **isLanguageRTL** 方法具有 **String** 数据类型的 **EN-US** 参数，则该方法必须在 ER 表达式中引用为 **System.'isLanguageRTL'("EN-US")**。
- 当方法名称仅包含一个字母数字符号时，引号不是必需的。 但是，如果名称中包含括号，则它们是表方法所必需的。

当 **System** 数据源被添加到引用**全局** Finance and Operations 应用程序类的 ER 映射时，表达式返回布尔值 **FALSE**。 修改后的表达式 **System.' isLanguageRTL'("AR")** 返回布尔值 **TRUE**。

可限制值传递到此类型方法的参数的方式：

- 只有常量可传递到此类型的方法。 常量的值定义为设计时间。
- 此类型的参数仅支持原始（基本）数据类型。 （原始数据类型为整数、实数、布尔值、字符串等。）

#### <a name="paths"></a>路径

在表达式引用结构化的数据源时，可以使用路径定义选择该数据源的特定基本元素。 点字符 (.) 用于分离结构化数据源的各个元素。 例如，当前的 ER 数据模型包含 **InvoiceTransactions** 数据源，并且该数据源返回记录列表。 **InvoiceTransactions** 记录结构包含 **AmountDebit** 和 **AmountCredit** 字段，并且这两个字段都将返回数值。 因此，您可以设计以下表达式来计算发票金额：**InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**。

#### <a name="functions"></a>功能

下一节介绍可用于 ER 表达式的函数。 根据调用函数参数的列表，可将表达式上下文（当前 ER 数据模型或 ER 格式）的所有数据源用作调用函数的参数，以便与调用函数的参数列表保持一致。 也可以将常量用作调用函数的参数。 例如，当前的 ER 数据模型包含 **InvoiceTransactions** 数据源，并且该数据源返回记录列表。 **InvoiceTransactions** 记录结构包含 **AmountDebit** 和 **AmountCredit** 字段，并且这两个字段都将返回数值。 因此，若要计算发票金额，可以设计使用内置的 ER 舍入函数的以下表达式：**ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**。

## <a name="supported-functions"></a>支持的函数

以下各表介绍可用于设计 ER 数据模型和 ER 报表的数据处理函数。 函数列表不是固定的。 开发人员可扩展它。 若要查看您可以使用的函数的列表，请打开 ER 公式设计器中的函数窗格。

### <a name="date-and-time-functions"></a>日期和时间函数

| 职能 | 描述 | 示例 |
|----------|-------------|---------|
| ADDDAYS（日期时间，天） | 添加指定的天数到指定的日期/时间值。 | **ADDDAYS (NOW(), 7)** 返回未来七天的日期和时间。 |
| DATETODATETIME（日期） | 转换指定日期值为一个日期/时间值。 | **DATETODATETIME (CompInfo. 'getCurrentDate()')** 返回当前的 Finance and Operations 会话日期 2015 年 12 月 24 日为 **12/24/2015 12:00:00 AM**。 在此示例中，**CompInfo** 为 **Finance and Operations/Table** 类型且引用 CompanyInfo 表的 ER 数据源。 |
| NOW () | 返回当前的 Finance and Operations 应用程序服务器日期和时间作为日期/时间值。 | |
| TODAY () | 返回当前的 Finance and Operations 应用程序服务器日期作为日期值。 | |
| NULLDATE () | 返回**空**日期值。 | |
| NULLDATETIME () | 返回**空**日期/时间值。 | |
| DATETIMEFORMAT（日期时间，格式） | 转换指定的日期/时间值为指定格式的字符串。 （有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)。） | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** 根据指定的自定义格式返回当前的 Finance and Operations 应用程序服务器日期 2015 年 12 月 24 日为 **"24-12-2015"**。 |
| DATETIMEFORMAT（日期时间，格式，区域性） | 转换指定的日期/时间值为指定格式和[区域性](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)的字符串。 （有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)。） | **DATETIMEFORMAT (NOW(), "d", "de")** 根据所选的德国区域性返回当前的 Finance and Operations 应用程序服务器日期 2015 年 12 月 24 日为 **"24.12.2015"**。 |
| SESSIONTODAY () | 返回当前的 Finance and Operations 会话日期作为日期值。 | |
| SESSIONNOW () | 返回当前的 Finance and Operations 会话日期和时间作为日期/时间值。 | |
| DATEFORMAT（日期，格式） | 以指定格式返回指定日期的字符串表示形式。 | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** 根据指定的自定义格式返回当前的 Finance and Operations 会话日期 2015 年 12 月 24 日为 **"24-12-2015"**。 |
| DATEFORMAT（日期，格式，区域性） | 转换指定的日期值为指定格式和[区域性](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)的字符串。 （有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)。） | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** 根据所选的德国区域性返回当前的 Finance and Operations 会话日期 2015 年 12 月 24 日为 **"24.12.2015"**。 |
| DAYOFYEAR（日期） | 返回 1 月 1 日与指定日期之间的天数的整数表现形式。 | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** 返回 **61**。 **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** 返回 **1**。 |
| DAYS (date 1, date 2) | 返回指定的第一个日期与第二个日期之间的天数。 第一个日期比第二个日期晚时返回正值，第一个日期等于第二个日期时返回 **0**，第一个日期比第二个日期早时返回负值。 | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** 返回 **-1**。 |

### <a name="data-conversion-functions"></a>数据转换函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| DATETODATETIME（日期） | 转换指定日期值为一个日期/时间值。 | **DATETODATETIME (CompInfo. 'getCurrentDate()')** 返回当前的 Finance and Operations 会话日期 2015 年 12 月 24 日为 **12/24/2015 12:00:00 AM**。 在此示例中，**CompInfo** 为 **Finance and Operations/Table** 类型且引用 CompanyInfo 表的 ER 数据源。 |
| DATEVALUE（字符串，格式） | 以指定格式返回指定字符串的日期表示形式。 | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** 根据指定的自定义格式和默认应用程序的 **EN-US** 区域性返回日期 2016 年 12 月 21 日。 |
| DATEVALUE（字符串，格式，区域性） | 以指定格式和区域性返回指定字符串的日期表示形式。 | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** 根据指定的自定义格式和区域性返回日期 2016 年 1 月 16 日。 但是，**DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** 将引发异常，以通知用户指定字符串无法识别为有效日期。 |
| DATETIMEVALUE（字符串，格式） | 以指定格式返回指定字符串的日期/时间表示形式。 | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** 根据指定的自定义格式和默认应用程序的 **EN-US** 区域性返回 2016 年 12 月 21 日早上 2 点 55 分。 |
| DATETIMEVALUE（字符串，格式，区域性） | 以指定格式和区域性返回指定字符串的日期/时间表示形式。 | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** 根据指定的自定义格式和区域性返回 2016 年 12 月 21 日早上 2 点 55 分。 但是，**DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** 将引发异常，以通知用户指定字符串无法识别为有效日期。 |

### <a name="list-functions"></a>列表函数

<table>
<thead>
<tr>
<th>职能</th>
<th>说明</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr>
<td>拆分（输入，长度）</td>
<td>拆分指定的输入字符串为子字符串，每个子字符串具有指定的长度。 返回结果为新的列表。</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> 返回包含具有 <strong>STRING</strong> 字段的两个记录的新列表。 第一个记录中的字段包含文本 <strong>&quot;abc&quot;</strong>，第二个记录中的字段包含文本 <strong>&quot;d&quot;</strong>。</td>
</tr>
<tr>
<td>SPLIT（输入、分隔符）</td>
<td>根据指定的分隔符拆分指定的输入字符串为子字符串。</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> 返回包含具有 <strong>STRING</strong> 字段的三个记录的新列表。 第一个记录中的字段包含文本 <strong>&quot;X&quot;</strong>，第二个记录中的字段包含文本 &quot;&nbsp;&quot;，第三个记录中的字段包含文本 <strong>&quot;y&quot;</strong>。 如果分隔符是空的，将返回一个新列表，其中包括具有包含输入文本的 <strong>STRING</strong> 字段的一个记录。 如果输入为空，新的空列表将返回。
如果输入或分隔符未指定（空），将引发应用程序异常。</td>
</tr>
<tr>
<td>拆分列表（列表，数字）</td>
<td>将指定的列表拆分为多个批次，每个批次包含指定的记录数。 返回结果为包含以下元素的批次的新列表：
<ul>
<li>作为常规列表的批次（<strong>值</strong>组件）</li>
<li>当前批处理号（<strong>BatchNumber</strong> 组件）</li>
</ul>
</td>
<td>下图中，将创建一个<strong>行</strong>数据源以充当三条记录组成的记录列表。 此列表分为多个批次，每个批次中最多包含两条记录。
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>下图显示设计的格式布局。 在此格式布局中，创建了与<strong>行</strong>数据源的绑定，以便生成 XML 格式的输出。 此输出为各批次及其中的记录提供单个节点。</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>下图显示运行设计的格式的结果。</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (record 1 [, record 2, …])</td>
<td>返回从指定的参数创建的新列表。</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> 返回空记录，在其中字段列表包含 <strong>MainData</strong> 和 <strong>OtherData</strong> 记录列表的所有字段。</td>
</tr>
<tr>
<td>LISTJOIN (list 1, list 2, …)</td>
<td>返回从指定的参数列表的连接列表。</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> 返回六个记录的列表，在其中 <strong>STRING</strong> 数据类型的一个字段包含一个字母。</td>
</tr>
<tr>
<td>ISEMPTY（列表）</td>
<td>如果指定的列表不包含任何元素，返回 <strong>TRUE</strong>。 否则，返回 <strong>FALSE</strong>。</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST（列表）</td>
<td>通过使用指定的列表返回空列表为列表结构的来源。</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> 返回具有与 <strong>SPLIT</strong> 函数返回的列表相同结构的新空列表。</td>
</tr>
<tr>
<td>FIRST（列表）</td>
<td>如果该记录不为空，返回指定列表的第一个记录。 否则，将引发异常。</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL（列表）</td>
<td>如果该记录不为空，返回指定列表的第一个记录。 否则，将返回<strong>空</strong>记录。</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM（列表）</td>
<td>返回仅包含指定列表的第一项的列表。</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS（路径）</td>
<td>此函数作为内存内选择运行。 它返回表示匹配指定路径的所有项的新的平展表。 路径必须定义为记录列表数据类型的数据源元素的有效数据源路径。 路径字符串和日期等数据元素应在 ER 表达式生成器中设计时引发错误。</td>
<td>如果您输入 <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> 为数据源 (DS)，<strong>COUNT( ALLITEMS (DS.Value))</strong> 返回 <strong>3</strong>。</td>
</tr>
<tr>
<td>ALLITEMSQUERY（路径）</td>
<td>此函数返回一个联接的 SQL 查询。 它返回表示匹配指定路径的所有项的新的平展表。 指定的路径必须定义为记录列表数据类型的数据源元素的有效数据源路径，并且必须至少包含一个关系。 路径字符串和日期等数据元素应在 ER 表达式生成器中设计时引发错误。</td>
<td>在模型映射中定义以下数据源：
<ul>
<li><strong>CustInv</strong>（<strong>表记录</strong>类型），引用的是 CustInvoiceTable 表</li> 
<li><strong>FilteredInv</strong>（<strong>计算字段</strong>类型），其中包含表达式 <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong>（<strong>计算字段</strong>类型），其中包含表达式 <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>运行模型映射以调用 <strong>JourLines</strong> 数据源时，将运行以下 SQL 语句：</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY（列表 [，表达式 1，表达式 2，...]）</td>
<td>根据指定变量排序后返回指定的列表。 可将这些变量定义为表达式。</td>
<td>如果<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源，<strong>ORDERBY (Vendors, Vendors.'name()')</strong> 返回升序排列的按名称排序的供应商列表。</td>
</tr>
<tr>
<td>REVERSE（列表）</td>
<td>以反转排序顺序返回指定的列表。</td>
<td>如果<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源，<strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> 返回降序排列的按名称排序的供应商列表。</td>
</tr>
<tr>
<td>WHERE（列表，条件）</td>
<td>根据指定条件筛选后返回指定的列表。 将对内存中的列表应用指定条件。 因此，<strong>WHERE</strong> 函数与 <strong>FILTER</strong> 函数不同。</td>
<td>如果<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源，<strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> 返回仅包含属于供应商组 40 的供应商的列表。</td>
</tr>
<tr>
<td>ENUMERATE（列表）</td>
<td>返回包括指定列表的枚举记录并显示以下元素的新列表：
<ul>
<li>作为常规列表的指定列表记录（<strong>值</strong>组件）</li>
<li>当前记录索引（<strong>编号</strong>组件）</li>
</ul>
</td>
<td>在下图中中，<strong>枚举</strong>数据源创建为引用 VendTable 表的<strong>供应商</strong>数据源的供应商记录的枚举列表。
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>下图显示格式。 在此格式布局中，创建了数据绑定，以便生成 XML 格式的输出。 此输出将单个供应商表示为枚举的节点。</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>下图显示运行设计的格式的结果。</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT（列表）</td>
<td>如果列表不为空，返回指定列表中的记录数。 否则，返回 <strong>0</strong>（零）。</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> 返回 <strong>2</strong>，因为 <strong>SPLIT</strong> 函数创建包含两个记录的列表。</td>
</tr>
<tr>
<td>LISTOFFIELDS（路径）</td>
<td>返回从以下其中一种类型的参数创建的记录列表：
<ul>
<li>模型枚举</li>
<li>格式枚举</li>
<li>集装箱</li>
</ul>
<p>创建的列表由具有以下字段的记录组成：</p>
<ul>
<li>姓名</li>
<li>标签</li>
<li>说明</li>
</ul>
运行时，<strong>标签</strong>和<strong>说明</strong>字段将返回基于格式的语言设置的值。
</td>
<td>在下图中，数据模型中引入了枚举。
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>下图显示以下详细信息：</p>
<ul>
<li>模型枚举作为数据源插入了报表中。</li>
<li>ER 表达式将模型枚举用作 <strong>LISTOFFIELDS</strong> 函数的参数。</li>
<li>使用创建的 ER 表达式将记录列表类型的数据源插入了报表中。</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>以下示例显示绑定到使用 <strong>LISTOFFIELDS</strong> 函数创建的记录列表类型数据源的 ER 格式元素。</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>下图显示运行设计的格式的结果。</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] 根据父 FILE 和 FOLDER 格式元素的语言设置，在 ER 格式的输出中输入了经过翻译的标签和说明文本。</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (path, language)</td>
<td>返回从变量（如模型枚举、格式枚举或容器）创建的记录列表。 创建的列表由具有以下字段的记录组成：
<ul>
<li>姓名</li>
<li>标签</li>
<li>说明</li>
<li>已翻译</li>
</ul>
运行时，<strong>标签</strong>和<strong>说明</strong>字段将返回基于格式的语言设置和指定语言的值。 <strong>已翻译</strong>字段指示<strong>标签</strong>字段已翻译为指定语言。
</td>
<td>例如，使用<strong>计算字段</strong>数据源类型为 <strong>enumType</strong> 数据模型枚举配置 <strong>enumType_de</strong> 和 <strong>enumType_deCH</strong> 数据源。
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>在此情况下，可使用以下表达式获取瑞士德语（如果此翻译可用）的枚举值标签。 如果瑞士德语翻译不可用，标签将为德语。</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN（列表、字段名称，分隔符）</td>
<td>返回由指定列表中的指定字段的连接值组成的字符串。 这些值通过指定分隔符分隔。</td>
<td>如果输入 <strong>SPLIT(&quot;abc&quot; , 1)</strong> 作为数据源 (DS)，则 <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> 返回 <strong>&quot;a-b-c&quot;</strong>。</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT（列表、限值，源限制）</td>
<td>将指定列表拆分为子列表组成的新列表，并返回记录列表内容的结果。 <strong>限值</strong>参数定义拆分原始列表的限值。 <strong>限制源</strong>参数定义增加总和的步骤。 如果限值源超过定义的限值时，限值不适用于原始列表的单个项目。</td>
<td>下图显示一个格式。 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>下图显示用于该格式的数据源。</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>下图显示运行该格式的结果。 在此情况下，输出为商品项目的简单列表。</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>在以下图中，调整了同一个格式，以显示单个批次必须包括总重量不应超过限值 9 的商品的批次中的商品物料的列表。</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>下图显示运行调整后的格式的结果。</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] 此限值不适用于原始列表的最后一个物料，因为其限值源（重量）的值 (11) 超出定义的限值 (9)。 在报表生成过程中（如有必要）使用相应格式元素的 <strong>WHERE</strong> 函数或 <strong>Enabled</strong> 表达式忽略（跳过）子列表。</blockquote>
</td>
</tr>
<tr>
<td>FILTER（列表，条件）</td>
<td>已修改查询以针对指定条件进行筛选后，返回指定列表。 此函数与 <strong>WHERE</strong> 函数，因为指定条件适用于数据库级别的<strong>表格记录</strong>类型的任何 ER 数据源。 可使用表格和关系定义列表和条件。</td>
<td>如果<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源，<strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> 返回仅包含属于供应商组 40 的供应商的列表。 如果<strong>供应商</strong>配置为引用 VendTable 表的 ER 数据源，并且配置为 ER 数据源的 <strong>parmVendorBankGroup</strong> 返回<strong>字符串</strong>数据类型的值，则 <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> 返回仅包含属于特定空白组的供应商帐户的列表。</td>
</tr>
<tr>
<td>INDEX (list, index)</td>
<td>此函数用于返回列表中的特定数字索引选择的记录。 如果索引超出了列表中的记录范围，则引发异常。</td>
<td>如果为<strong>计算字段</strong>类型输入的数据源为 <strong>DS</strong>，而该数据源中包含表达式 <strong>SPLIT ("A|B|C", “|”), 2</strong>，则表达式 <strong>DS.Value</strong> 将返回文本值“B”。 表达式 <strong>INDEX (SPLIT ("A|B|C", “|”), 2).Value</strong> 也返回文本值“B”。</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>逻辑函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| CASE（表达式，选项 1，结果 1 \[，选项 2，结果 2\] ... \[, 默认结果\]） | 根据指定的备选选项评估指定的表达式值。 返回与表达式的值相等的选项的结果。 否则，返回可选默认结果（如果指定了默认结果）。 （默认结果是前面不加选项的最后一个参数。） | 当当前的 Finance and Operations 会话日期是在 10 月和 12 月之间时，**CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** 返回字符串 **"WINTER"**。 否则，它返回一个空字符串。 |
| IF（条件，值 1，值 2） | 在满足指定条件时，返回第一个指定值。 否则，返回第二个指定值。 如果值 1 和值 2 是记录或记录列表，结果将只包含两个列表都存在的字段。 | **IF (1=2, "condition is met", "condition is not met")** 返回字符串 **"condition is not met"**。 |
| NOT（条件） | 返回指定条件的冲销逻辑值。 | **NOT (TRUE)** 返回 **FALSE**。 |
| AND (condition 1\[, condition 2, …\]) | 如果指定的*所有*条件均为 True，返回 **TRUE**。 否则，返回 **FALSE**。 | **AND (1=1, "a"="a")** 返回 **TRUE**。 **AND (1=2, "a"="a")** 返回 **FALSE**。 |
| OR (condition 1\[, condition 2, …\]) | 如果指定的*所有*条件均为 False，返回 **FALSE**。 如果指定的*任何*条件均为 True，返回 **TRUE**。 | **OR (1=2, "a"="a")** 返回 **TRUE**。 |
| VALUEIN（输入、列表、列表项表达式） | 确定指定的输入是否匹配指定列表中任何项目的值。 如果指定的输入与运行至少一个记录的指定表达式的结果匹配，则返回 **TRUE**。 否则，返回 **FALSE**。 **输入**参数表示数据源元素的路径。 将匹配此元素的值。 **列表**参数将记录列表类型的数据源元素的路径表示为包含表达式的记录的列表。 此元素的值将与指定输入比较。 **列表项表达式**参数表示指向或包含应用于匹配的指定列表的一个字段的表达式。 | 有关示例，请参阅随后的[示例：VALUEIN（输入、列表、列表项表达式）](#examples-valuein-input-list-list-item-expression)部分。 |

#### <a name="examples-valuein-input-list-list-item-expression"></a>示例：VALUEIN（输入、列表、列表项表达式）
一般来说，**VALUEIN** 函数转换为一组 **OR** 条件：

(input = list.item1.value) OR (input = list.item2.value) OR …

##### <a name="example-1"></a>示例 1
您在模型映射中定义以下数据源：**列表**（**计算字段**类型）。 此数据源包含表达式 **SPLIT ("a,b,c", ",")**。

在调用配置为 **VALUEIN ("B", List, List.Value)** 表达式的数据源时，它将返回 **TRUE**。 在这种情况下，**VALUEIN** 函数转换为以下一组条件：

**(("B" = "a") or ("B" = "b") or ("B" = "c"))**, where **("B" = "b")** is equal to **TRUE**

在调用配置为 **VALUEIN ("B", List, LEFT(List.Value, 0))** 表达式的数据源时，它将返回 **FALSE**。 在这种情况下，**VALUEIN** 函数转换为以下条件：

**("B" = "")**, which isn't equal to **TRUE**

请注意，此条件的文本中的字符数的上限为 32,768 个字符。 因此，您不应该在运行时创建可能超出此限制的数据源。 如果超出限制，应用程序将停止运行，并将引发异常。 例如，如果数据源被配置为 **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)**，并且 **List1** 和 **List2** 列表包含大量记录，将发生此情况。

在某些情况下，**VALUEIN** 函数通过使用 **EXISTS JOIN** 运算符转换为数据库语句。 此行为会在使用 **FILTER** 函数并且当满足以下条件时发生：

- **ASK FOR QUERY** 选项将对引用记录列表的 **VALUEIN** 函数的数据源关闭。 （附加条件不会在运行时应用于此数据源。）
- 不会为引用记录列表的 **VALUEIN** 函数的数据源配置嵌套表达式。
- **VALUEIN** 函数的列表项引用指定数据源的字段（不是表达式或方法）。

请考虑使用此选项而不是 **WHERE** 函数，如本示例前面所述。

##### <a name="example-2"></a>示例 2

在模型映射中定义以下数据源：

- **In**（**表记录**类型），引用的是 Intrastat 表
- **Port**（**表记录**类型），引用的是 IntrastatPort 表

在调用配置为 **FILTER (In, VALUEIN(In.Port, Port, Port.PortId)** 表达式的数据源时，以下 SQL 语句将生成以返回筛选的内部统计表记录：

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

对于 **dataAreaId** 字段，最后的 SQL 语句使用 **IN** 运算符生成。

##### <a name="example-3"></a>示例 3

在模型映射中定义以下数据源：

- **Le**（**计算字段**类型），包含表达式 **SPLIT ("DEMF,GBSI,USMF", ",")**
- **In**（**表记录**类型），引用内部统计表，其**跨公司**选项打开

在调用配置为 **FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)** 表达式的数据源时，最后的 SQL 语句包含以下条件：

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>数学函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| ABS（数字） | 返回指定数字的绝对值。 （即，返回不带符号的数字。） | **ABS (-1)** 返回 **1**。 |
| POWER（数字，功率） | 返回将指定的正数增加到指定的功率的结果。 | **POWER (10, 2)** 返回 **100**。 |
| NUMBERVALUE（字符串，小数分隔符，数字分组分隔符） | 将指定的字符串转换为数字。 将在十进制数字的整数和小数部分之间使用小数点分隔符。 指定的数字分组分隔符用作千分位分隔符。 | **NUMBERVALUE("1 234,56", ",", " ")** 返回值 **1234.56**。 |
| VALUE（字符串） | 将指定的字符串转换为数字。 逗号和点字符 (.) 被视为小数分隔符，前导连字符 (-) 用作负号。 如果指定字符串中包含其他非数值字符，将引发异常。 | **VALUE ("1 234,56")** 引发异常。 |
| ROUND（数字，小数位） | 返回已舍入到指定小数位数的指定数字：<ul><li>如果**小数**参数的值大于 0（零），则指定的数值舍入到这个多位小数位数。</li><li>如果**小数**参数的值为 **0**（零），则指定的数值舍入到最近的整数。</li><li>如果**小数**参数的值小于 0（零），则指定的数值舍入到小数点左边。</li></ul> | **ROUND (1200.767, 2)** 舍入到两位小数，返回 **1200.77**。 **ROUND (1200.767, -3)** 舍入到最接近的 1,000 的倍数，返回 **1000**。 |
| ROUNDDOWN（数字，小数位） | 返回已向下舍入到指定小数位数的指定数字。<blockquote>[!NOTE] 此函数类似 **ROUND**，但始终向下（朝零）舍入到指定的数字。</blockquote> | **ROUNDDOWN (1200.767, 2)** 向下舍入到两位小数，返回 **1200.76**。 **ROUNDDOWN (1700.767, -3)** 向下舍入到最接近的 1,000 的倍数，返回 **1000**。 |
| ROUNDUP（数字，小数位） | 返回已向上舍入到指定小数位数的指定数字。<blockquote>[!NOTE] 此函数类似 **ROUND**，但始终向上（不朝零）舍入到指定的数字。</blockquote> | **ROUNDUP (1200.763, 2)** 向上舍入到两位小数，返回 **1200.77**。 **ROUNDUP (1200.767, -3)** 向上舍入到最接近的 1,000 的倍数，返回 **2000**。 |

### <a name="data-conversion-functions"></a>数据转换函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| VALUE（字符串） | 将指定的字符串转换为数字。 逗号和点字符 (.) 被视为小数分隔符，前导连字符 (-) 用作负号。 如果指定字符串中包含其他非数值字符，将引发异常。 | **VALUE ("1 234,56")** 引发异常。 |
| NUMBERVALUE（字符串，小数分隔符，数字分组分隔符） | 将指定的字符串转换为数字。 将在十进制数字的整数和小数部分之间使用小数点分隔符。 指定的数字分组分隔符用作千分位分隔符。 | **NUMBERVALUE("1 234,56", ",", " ")** 返回 **1234.56**。 |
| INTVALUE（字符串） | 返回指定字符串的整数表示形式。 将截断所有小数部分。 | **INTVALUE ("100.77")** 返回 **100**。 |
| INTVALUE（编号） | 返回指定数字的整数表示形式。 将截断所有小数部分。 | **INTVALUE (-100.77)** 返回 **-100**。 |
| INT64VALUE（字符串） | 返回指定字符串的 int64 表示形式。 将截断所有小数部分。 | **INT64VALUE ("22565422744")** 返回 **22565422744**。 |
| INT64VALUE（数字） | 返回指定数字的 int64 表示形式。 将截断所有小数部分。 | **INT64VALUE (22565422744.00)** 返回 **22565422744**。 |

### <a name="record-functions"></a>记录函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| NULLCONTAINER（列表） | 返回与指定的记录列表或记录具有相同结构的**空**记录。<blockquote>[!NOTE] 此函数已废弃。 使用 **EMPTYRECORD**。</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** 返回具有与 **SPLIT** 函数返回的列表相同结构的新空记录。 |
| EMPTYRECORD（记录） | 返回与指定的记录列表或记录具有相同结构的**空**记录。<blockquote>[!NOTE] **null** 记录为其中的所有字符串都有空值的记录。 空值对于数字来说为 **0**（零），对于字符串来说为空字符串，依此类推。</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** 返回具有与 **SPLIT** 函数返回的列表相同结构的新空记录。 |

### <a name="text-functions"></a>文本函数

<table>
<thead>
<tr>
<th>职能</th>
<th>说明</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER（字符串）</td>
<td>返回已转换为大写字母的指定字符串。</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> 返回 <strong>&quot;SAMPLE&quot;</strong>。</td>
</tr>
<tr>
<td>LOWER（字符串）</td>
<td>返回已转换为小写字母的指定字符串。</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> 返回 <strong>&quot;sample&quot;</strong>。</td>
</tr>
<tr>
<td>LEFT（字符串，字符数）</td>
<td>从指定字符串的开头返回指定数目的字符。</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> 返回 <strong>&quot;Sam&quot;</strong>。</td>
</tr>
<tr>
<td>RIGHT（字符串，字符数）</td>
<td>从指定字符串的结尾返回指定数目的字符。</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> 返回 <strong>&quot;ple&quot;</strong>。</td>
</tr>
<tr>
<td>MID（字符串，起始位置，字符数）</td>
<td>从指定位置开始返回指定字符串的指定数目的字符。</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> 返回 <strong>&quot;amp&quot;</strong>。</td>
</tr>
<tr>
<td>LEN（字符串）</td>
<td>返回指定字符串中的字符数。</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> 返回 <strong>6</strong>。</td>
</tr>
<tr>
<td>CHAR（数字）</td>
<td>返回指定的 Unicode 数值引用的字符的字符串。</td>
<td><strong>CHAR (255)</strong> 返回 <strong>&quot;ÿ&quot;</strong>。
<blockquote>[!NOTE] 此函数返回的字符串取决于在父 FILE 格式元素中选择的编码。 有关支持的编码的列表，请参阅<a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">编码类</a>。</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE（字符串 1 [，2，…]）</td>
<td>返回已联接为一个字符串的所有指定文本字符串。</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong>返回 <strong>&quot;abcdef&quot;</strong>。
<blockquote>[!NOTE] 表达式 <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> 也返回 <strong>&quot;abcdef&quot;</strong>。</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE（字符串，模式，替换）</td>
<td>返回指定串字符，其中所有在指定模式字符串中出现的字符已由指定替换字符相应位置的字符替换。</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> 将模式 <strong>&quot;cd&quot;</strong> 替换为字符串 <strong>&quot;GH&quot;</strong>，并返回 <strong>&quot;abGHef&quot;</strong>。</td>
</tr>
<tr>
<td>REPLACE（字符串，模式，替换，正则表达式标志）</td>
<td>在指定的<strong>正则表达式标记</strong>参数为 <strong>True</strong> 时，返回指定字符串，并且其已通过应用指定为此函数的<strong>模式</strong>参数的正则表达式来修改。 此表达式用于查找必须替换的字符。 指定的<strong>替换</strong>参数的字符用于替换找到的字符。 在指定的<strong>正则表达式标记</strong>参数为 <strong>False</strong> 时，此函数类似 <strong>TRANSLATE</strong>。</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> 应用删除所有非数字符号的正则表达式，并返回 <strong>&quot;19234564971&quot;</strong>。 <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> 将模式 <strong>&quot;cd&quot;</strong> 替换为字符串 <strong>&quot;GH&quot;</strong>，并返回 <strong>&quot;abGHef&quot;</strong>。</td>
</tr>
<tr>
<td>TEXT（输入）</td>
<td>返回指定的输入，并且其已转换为根据当前 Finance and Operations 实例的服务器区域设置设置格式的文本字符串。 对于 <strong>real</strong> 类型的值，字符串转换被限制为两位小数。</td>
<td>如果将 Finance and Operations 实例的服务器区域定义为 <strong>EN-US</strong>，<strong>TEXT (NOW ())</strong> 返回当前 Finance and Operations 会话日期 2015 年 12 月 17 日为文本字符串 <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>。 <strong>TEXT (1/3)</strong> 返回 <strong>&quot;0.33&quot;</strong>。</td>
</tr>
<tr>
<td>FORMAT (string 1, string 2[, string 3, …])</td>
<td>返回指定字符串，并且其已通过代替任何出现的带有第 <em>n</em> 个参数的 <strong>%N</strong> 设置格式。 这些参数是字符串。 如果参数不是为参量提供，则参量在字符串中返回为 <strong>&quot;%N&quot;</strong>。 对于 <strong>real</strong> 类型的值，字符串转换被限制为两位小数。</td>
<td>在下图中，数据源 <strong>PaymentModel</strong> 通过<strong>客户</strong>组件返回客户记录列表，通过 <strong>ProcessingDate</strong> 字段返回处理日期值。
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>在指定用于为所选客户生成电子文件的 ER 格式中，<strong>PaymentModel</strong> 被选择为数据源并控制流程。 当所选客户在处理报表的日期停止时，将引发异常以通知用户。 为此类处理控制设计的配方可以使用以下资源：</p>
<ul>
<li>Finance and Operations 标签 SYS70894，具有以下文本：
<ul>
<li><strong>对于 EN-US 语言：</strong>&quot;Nothing to print&quot;</li>
<li><strong>对于 DE 语言：</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Finance and Operations 标签 SYS18389，具有以下文本：
<ul>
<li><strong>对于 EN-US 语言：</strong>&quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>对于 DE 语言：</strong>&quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>这是一个可设计的公式：</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>如果报表于 2015 年 12 月 17 日为 <strong>Litware 零售</strong>客户处理，在 <strong>EN-US</strong> 区域性和 <strong>EN-US</strong> 语言中，此公式返回以下文本，其可能向用户呈现为异常消息：</p>
<p>&quot;没有要打印的内容。 客户 Litware 零售已于 2015 年 12 月 17 日停止。&quot;</p>
<p>如果 2015 年 12 月 17 日为 <strong>Litware 零售</strong>客户处理同一个报表，在 <strong>DE</strong> 区域性和 <strong>DE</strong> 语言中，此公式返回以下文本（使用不同的日期格式）：</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt。&quot;</p>
<blockquote>[!NOTE] 以下语法在标签的 ER 公式中应用：
<ul>
<li><strong>对于 Finance and Operations 资源的标签：</strong><strong>@&quot;X&quot;</strong>，其中 <strong>X</strong> 是应用程序对象树 (AOT) 中的标签 ID</li>
<li><strong>对于位于 ER 配置中的标签：</strong><strong>@&quot;GER_LABEL:X&quot;</strong>，其中 <strong>X</strong> 是 ER 配置中的标签 ID</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT（数字，格式）</td>
<td>以指定格式返回指定数值的字符串表示形式。 （有关支持的格式的信息，请参阅<a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">标准</a>和<a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">自定义</a>。）此函数在其中运行的环境确定设置数字格式的区域性。</td>
<td>对于 EN-US 区域性，<strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> 返回 <strong>&quot;45.00 %&quot;</strong>。 <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> 返回 <strong>&quot;10&quot;</strong>。</td>
</tr>
<tr>
<td>NUMBERFORMAT (number, format, culture)</td>
<td>以指定格式和给定区域性返回指定数字的字符串表示形式。 （有关支持格式的信息，请参阅<a href="https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings">标准</a>和<a href="https://docs.microsoft.com/en-us/dotnet/standard/base-types/custom-numeric-format-strings">自定义</a>。）</td>
<td><strong>NUMBERFORMAT (10/3, “F2”, "de")</strong> 返回 <strong>3,33</strong>，而 <strong>NUMBERFORMAT (10/3, “F2”, "en-us")</strong> 则返回 <strong>3.33</strong>。</td>
</tr>
<tr>
<td>NUMERALSTOTEXT（数字，语言，币种，打印币种名称标志，小数点）</td>
<td>返回已以指定语言拼出（转换为文本字符串）的指定数字。 语言代码可选。 定义为空字符串时，将使用运行上下文的语言代码。 （运行上下文的语言代码是为生成文件夹或文件定义的。）币种代码也可选。 定义为空字符串时，采用公司币种。
<blockquote>[!NOTE] 仅为以下语言代码分析<strong>打印币种名称标记</strong>和<strong>小数点</strong>参数：<strong>CS</strong>、<strong>ET</strong>、<strong>HU</strong>、<strong>LT</strong>、<strong>LV</strong>、<strong>PL</strong> 和 <strong>RU</strong>。 此外，仅为国家或地区的上下文支持币种名称偏差的 Finance and Operations 公司分析<strong>打印币种名称标记</strong>参数。</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> 返回 <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>。 <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> 返回 <strong>&quot;Sto dwadzieścia&quot;</strong>。 <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> 返回 <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>。</td>
</tr>
<tr>
<td>PADLEFT（字符串，长度，填充字符）</td>
<td>返回指定长度的字符串，其中指定字符串的开头是使用指定字符填充的。</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> 返回文本字符串 <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>。</td>
</tr>
<tr>
<td>TRIM（字符串）</td>
<td>返回已截断前导空格和尾随空格且已除去单词之间的多个空格的指定文本字符串。</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> 返回 <strong>&quot;Sample text&quot;</strong>。</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME（枚举数据源路径，枚举值标签文本）</td>
<td>根据枚举标签的指定文本返回指定枚举数据源的值。</td>
<td>在下图中，数据模型中引入了 <strong>ReportDirection</strong> 枚举。 请注意，为枚举值定义标签。
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>下图显示以下详细信息：</p>
<ul>
<li><strong>ReportDirection</strong> 模型枚举作为数据源 <strong>$Direction</strong> 插入了报表中。</li>
<li>ER 表达式 <strong>$IsArrivals</strong> 设计为将该模型枚举用作此函数的参数。 此表达式的值为 <strong>TRUE</strong>。</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE（输入）</td>
<td>将<strong>字符串</strong>数据类型的指定输入转换为 <strong>GUID</strong> 数据类型的数据项。<blockquote>[!NOTE] 若要执行反向转换（即，将指定的 <strong>GUID</strong> 数据类型的输入转换为<strong>字符串</strong>数据类型的数据项），您可以使用 <strong>TEXT()</strong> 函数。</blockquote></td>
<td>在模型映射中定义以下数据源：
<ul>
<li><strong>myID</strong>（<strong>计算字段</strong>类型），其中包含表达式 <strong>GUIDVALUE(&quot;AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Users</strong>（<strong>表记录</strong>类型），引用的是 UserInfo 表</li>
</ul>
如果定义了这些数据源，就可以使用 <strong>FILTER (Users, Users.objectId = myID)</strong> 之类表达式按 <strong>GUID</strong> 数据类型的 <strong>objectId</strong> 字段筛选 UserInfo 表。
</td>
</tr>
<tr>
<td>JSONVALUE（ID、路径）</td>
<td>分析按指定路径访问且格式为 JavaScript Object Notation (JSON) 的数据，以便提取基于指定 ID 的标量值。</td>
<td>数据源 <strong>$JsonField</strong> 中包含 JSON 格式的以下数据：<strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>。 对于此数据源，</strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> 返回<strong>字符串</strong>数据类型的值 <strong>7.3.1234.1</strong>。</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>数据转换函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| TEXT（输入） | 返回指定的输入，并且其已转换为根据当前 Finance and Operations 实例的服务器区域设置设置格式的文本字符串。 对于 **real** 类型的值，字符串转换被限制为两位小数。 | 如果将 Finance and Operations 实例的服务器区域定义为 **EN-US**，**TEXT (NOW ())** 返回当前 Finance and Operations 会话日期 2015 年 12 月 17 日为文本字符串 **"12/17/2015 07:59:23 AM"**。 **TEXT (1/3)** 返回 **"0.33"**。 |
| QRCODE（字符串） | 为指定字符串返回 base64 二进制格式的快速响应码 (QR 代码) 图像。 | **QRCODE ("Sample text")** 返回 **U2FtcGxlIHRleHQ=**。 |

### <a name="data-collection-functions"></a>数据收集功能

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| FORMATELEMENTNAME () | 返回当前格式的元素的名称。 在当前文件的**收集输出详细信息**标记关闭时返回空字符串。 | 有关如何使用此函数的详细信息，请参阅**盘点和合计格式输出的 ER 使用数据**任务指南，这是**购置/开发 IT 服务/解决方案组件**业务流程的一部分。 |
| SUMIFS (key string for summing, criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | 在此格式运行且满足指定条件（范围和值配对）时，返回为 XML 节点（其名称定义为键）收集的值的总和。 在当前文件的**收集输出详细信息**标记关闭时返回 **0**（零）值。 | |
| SUMIF（要合计的键字符串，条件范围字符串，条件值字符串） | 在此格式运行且满足指定条件（范围和值）时，返回为 XML 节点（其名称定义为键）收集的值的总和。 在当前文件的**收集输出详细信息**标记关闭时返回 **0**（零）值。 | |
| COUNTIFS (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | 在此格式运行且满足指定条件（范围和值配对）时，返回收集的 XML 节点的数量。 在当前文件的**收集输出详细信息**标记关闭时返回 **0**（零）值。 | |
| COUNTIF（范围条件字符串，条件值字符串） | 在此格式运行且满足指定条件（范围和值）时，返回收集的 XML 节点的数量。 在当前文件的标记**收集输出详细信息**关闭时返回 **0**（零）值。 | |
| COLLECTEDLIST (criteria range1 string, criteria value1 string \[, criteria range2 string, criteria value2 string, …\]) | 在此格式运行且满足指定条件（范围和值）时，返回为 XML 节点收集的值的列表。 在当前文件的**收集输出详细信息**标记关闭时返回空列表。 | |

### <a name="other-business-domainspecific-functions"></a>其他（业务域特定的）函数

| 职能 | 说明 | 示例 |
|----------|-------------|---------|
| CONVERTCURRENCY（金额，源币种，目标币种，日期，格式） | 通过使用指定日期的指定 Finance and Operations 公司的设置，将指定的货币金额从指定源币种转换为指定目标币种。 | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** 基于 DEMF 公司的设置返回当前会话日期一欧元的等额美元。 |
| ROUNDAMOUNT（数字，小数位，舍入规则） | 根据指定的舍入规则将指定金额舍入为指定小数位数。<blockquote>[!NOTE] 舍入规则必须指定为 Finance and Operations **RoundOffType** 枚举的值。</blockquote> | 如果 **model.RoundOff** 参数设置为 **Downward**，**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** 返回值 **1000.78**。 如果 **model.RoundOff** 参数设置为 **Normal** 或 **Rounding-up**，**ROUNDAMOUNT (1000.787, 2, model.RoundOff)** 返回值 **1000.79**。 |
| CURCredRef（位数） | 基于指定发票编号的数字返回贷方引用。 | **CURCredRef ("VEND-200002")** 返回 **"2200002"**。 |
| MOD\_97（位数） | 基于指定发票编号的数字返回贷方引用为 MOD97 表达式。 | **MOD\_97 ("VEND-200002")** 返回 **"20000285"**。 |
| ISOCredRef（位数） | 基于指定发票编号的数字和字母符号返回国际标准化组织 (ISO) 贷方引用。<blockquote>[!NOTE] 若要从不是 ISO 兼容的字母表中清除符号，输入参数必须在传递给此函数前转换。</blockquote> | **ISOCredRef ("VEND-200002")** 返回 **"RF23VEND-200002"**。 |
| CN\_GBT\_AdditionalDimensionID （字符串，数字） | 获取指定的额外财务维度 ID。 在 **string** 参数中，维度在此字符串中显示为以逗号分隔的 ID。 **number** 参数定义字符串中所请求维度的序列代码。 | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** 返回 **"CC"**。 |
| GetCurrentCompany () | 返回用户目前已登录到的法人（公司）的代码的文本表示形式。 | **GETCURRENTCOMPANY ()** 为在 Finance and Operations 中已登录 的 **Contoso Entertainment System USA** 公司的用户返回 **USMF**。 |
| CH\_BANK\_MOD\_10（位数） | 基于指定发票编号的数字返回贷方引用为 MOD10 表达式。 | **CH\_BANK\_MOD\_10 ("VEND-200002")** 返回 **3**。 |
| FA\_SUM（固定资产代码，值模型代码，开始日期，结束日期） | 返回指定期间的固定资产金额的准备的数据容器。 | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** 返回具有值模型 **Current** 的固定资产 **"COMP-000001"** 从 **Date1** 到 **Date2** 期间的已准备的数据容器。 |
| FA\_BALANCE（固定资产代码，值模型代码，报告年度，报告日期） | 返回固定资产余额的准备的数据容器。 报告年度必须在 Finance and Operations 中指定为 **AssetYear** 枚举的值。 | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** 返回具有值模型 **Current** 的固定资产 **"COMP-000001"** 的余额在当前 Finance and Operations 会话日期的准备的数据容器。 |
| TABLENAME2ID（字符串） | 为指定表名返回表 ID 的整数表示形式。 | **TABLENAME2ID ("Intrastat")** 返回 **1510**。 |
| ISVALIDCHARACTERISO7064（字符串） | 当指定字符串表示有效的国际银行帐号 (IBAN) 时，返回布尔值 **TRUE**。 否则，返回布尔值 **FALSE**。 | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** 返回 **TRUE**。 **ISVALIDCHARACTERISO7064 ("AT61")** 返回 **FALSE**。 |
| NUMSEQVALUE（编号规则代码、作用域、作用域 ID） | 基于指定的编号规则代码、作用域和作用域 ID 返回新生成的编号规则值。 作用域必须指定为 **ERExpressionNumberSequenceScopeType**枚举（**共享**、**法人**或**公司**）的值。 对于**共享**作用域，指定一个空字符串作为作用域 ID。 对于**公司**和**法人**作用域，指定公司代码作为作用域 ID。 对于**公司**和**法人**作用域，如果您指定空字符串作为作用域 ID，则将使用当前的公司代码。 | 在模型映射中定义以下数据源：<ul><li>**enumScope**（**Dynamics 365 for Operations 枚举**类型），引用 **ERExpressionNumberSequenceScopeType** 枚举</li><li>**NumSeq**（**计算字段**类型），包含表达式 **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")**</li></ul>在调用 **NumSeq** 数据源时，将返回为提供 ER 格式在其中运行的上下文的公司配置的 **Gene\_1** 编号规则的新生成值。 |
| NUMSEQVALUE（编号规则代码） | 基于指定的编号规则、**公司**作用域，以及提供 ER 格式在其中运行的上下文的公司的代码（作为作用域 ID）返回新生成的编号规则值。 | 您在模型映射中定义以下数据源：**NumSeq**（**计算字段**类型）。 此数据源包含表达式 **NUMSEQVALUE ("Gene\_1")**。 在调用 **NumSeq** 数据源时，将返回为提供 ER 格式在其中运行的上下文的公司配置的 **Gene\_1** 编号规则的新生成值。 |
| NUMSEQVALUE（编号规则记录 ID） | 基于指定的编号规则记录 ID 返回新生成的编号规则值。 | 在模型映射中定义以下数据源：<ul><li>**LedgerParms**（**表**类型），引用的是 LedgerParameters 表</li><li>**NumSeq**（**计算字段**类型），包含表达式 **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)**</li></ul>在调用 **NumSeq** 数据源时，将返回在提供 ER 格式在其中运行的上下文的公司的总帐参数中配置的编号规则的新生成值。 此编号规则唯一标识日记帐，并充当将交易记录链接在一起的批号。 |

### <a name="functions-list-extension"></a>函数的列表扩展

ER 允许您扩展 ER 表达式中使用的函数列表的功能。 需要执行一些工程工作。 有关详细信息，请参阅[扩展电子申报查询功能的列表](general-electronic-reporting-formulas-list-extension.md)。

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [扩展电子申报 (ER) 功能的列表](general-electronic-reporting-formulas-list-extension.md)
