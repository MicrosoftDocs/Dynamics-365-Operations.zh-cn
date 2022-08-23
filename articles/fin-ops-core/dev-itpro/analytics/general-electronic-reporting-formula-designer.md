---
title: 电子申报中 (ER) 的配方设计器
description: 本文提供有关如何在电子报告 (ER) 中使用公式设计器的信息。
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 3620fa886fd4b609a0f1f08b2338ab725065efe7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287919"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>电子申报中 (ER) 的配方设计器

[!include [banner](../includes/banner.md)]

本文说明如何在电子报告 (ER) 中使用公式设计器。 在您在 ER 中为特定电子文档设计格式时，您可以使用公式转换数据，以便使其满足该文档的履行和格式的要求。 这些公式类似 Microsoft Excel 中的公式。 公式中支持各种函数类型：文本、日期和时间、数学、逻辑、信息、数据类型转换函数，以及其他的企业域特定函数。

## <a name="formula-designer-overview"></a>配方设计器概览

ER 支持公式设计器。 因此，在设计时，您可以配置在运行时可用于执行以下任务的表达式：

- 将从应用程序数据库接收的数据以及应输入的数据转换为设计作为 ER 格式的数据源的 ER 数据模型。 （例如，这些转换可以包括筛选、分组和数据转换类型。）
- 设置必须发送到生成电子单据的数据的格式，以便满足特定 ER 格式的布局和条件。 （例如，可以根据请求的语言、文化或编码完成格式化）。
- 控制电子单据的创建过程。 （例如，表达式可根据处理数据启用或禁用该格式的特定元素的输出。 还可以中断单据创建过程，或向用户显示消息。）

执行以下任何操作时，可打开 **公式设计器** 页面：

- 数据源物料绑定到数据模型组件。
- 数据源物料绑定到格式组件。
- 完成作为数据源的一部分的计算字段的维护。
- 定义用户输入参数的可见性和可编辑性条件。
- 定义用户输入参数的默认值。
- 设计格式转换。
- 定义启用格式组件的条件。
- 定义格式的 FILE 组件的文件名。
- 定义流程控制验证的条件。
- 定义流程控制验证的消息文本。

## <a name="data-binding"></a><a name="Binding"></a>数据绑定

ER 公式设计器可以用于定义转换接收自数据源的数据的表达式，以便数据在运行时可以按以下方式在数据用户中输入数据：

- 从应用程序数据源和运行时参数转换为 ER 数据模型
- 从 ER 数据模型转换为 ER 格式
- 从应用程序数据源和运行时参数转换为 ER 格式

下图显示了此类表达式的设计。 在此示例中，表达式将内部统计表中的 **Intrastat.AmountMST** 字段的值舍入到两位小数，然后返回舍入值。

[![数据绑定表达式。](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

下图显示了如何使用此类表达式。 在此示例中，设计的表达式的结果输入在 **纳税申报模型** 数据模型的 **Transaction.InvoicedAmount** 组件中。

[![要使用的数据绑定表达式。](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

运行时，设计的公式 `ROUND (Intrastat.AmountMST, 2)` 将内部统计表中各记录的 **AmountMST** 字段的值舍入为两位小数。 然后在 **纳税申报** 数据模型的 **Transaction.InvoicedAmount** 组件中输入化整后的值。

## <a name="data-formatting"></a><a name="Transformation"></a>数据格式设置

ER 配方设计器可以用于定义确定接收自数据源的数据的格式的表达式，以便数据可以作为生成电子文档的一部分发送。 可能必须将格式设置作为应对某种格式重复使用的典型规则来应用。 在这种情况下，可将该格式设置在格式配置中引入一次，作为具有格式设置表达式的指定转换。 此指定的转换然后可链接到许多格式组件，这些组件是必须根据创建的格式表达式设置其输出的格式。

下图显示了此类转换的设计。 在此示例中，**TrimmedString** 转换通过去除前导空格和尾随空格截断 *字符串* 数据类型的传入数据。 然后返回截断后的字符串值。

[![转换。](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

下图显示了如何使用此类转换。 在此示例中，若干格式组件在运行时将文本作为输出发送到生成电子单据。 所有这些组件名义上引用 **TrimmedString** 转换。

[![要使用的转换。](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

上图中 **partyName** 组件之类格式组件引用 **TrimmedString** 转换时，该转换将把文本作为输出发送到生成电子单据。 此文本中不包含前导空格和尾随空格。

如果您具有必须单独应用的格式，可以将此格式作为特定格式组件绑定的单个表达式引入。 下图显示了此类表达式。 在此示例中，**partyType** 格式组件通过将数据源中 **Model.Company.RegistrationType** 字段的传入数据转换为大写文本的表达式绑定到数据源。 然后，该表达式将该文本作为输出发送到电子单据。

[![将格式应用于单个组件。](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>流程控制

ER 格式设计器可用于定义控制生成电子单据的流程的表达式。 您可以执行以下任务：

- 定义确定必须停止文档创建流程的条件。
- 指定表达式，这些表达式将创建有关已停止流程的用户的消息或引发有关继续报表生成流程的执行日志消息。
- 指定生成电子单据的文件名并控制其创建的条件。

流程控制的每个规则设计为单个验证。 下图显示了此类验证。 此示例中是对配置的说明：

- 在 **INSTAT** 节点在生成 XML 文件期间创建时，将对验证进行评估。
- 如果事务列表为空，验证将停止执行流程并返回 **FALSE**。
- 验证返回使用用户首选语言的包括标签 SYS70894 文本的错误消息。

[![验证。](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER 配方设计器还可用于生成文件名来生成电子单据和控制文件创建流程。 下图显示了此类流程控制的设计。 此示例中是对配置的说明：

- **model.Intrastat** 数据源的记录列表拆分为多个批次。 每个批次最多包含 1,000 条记录。
- 输出创建以 XML 格式为创建的每个批次包含一个文件的压缩文件。
- 表达式通过连接文件名和文件名扩展返回生成电子文档的文件名。 对于第二个批次和所有后续的批次，文件名作为后缀包含批次 ID。
- 表达式为包含至少一条记录的批次启用（通过返回 **TRUE**）文件创建流程。

[![流程流控制。](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>单据内容控制

可使用 ER 配方设计器配置表达式，用于控制运行时将哪些数据放到生成的电子单据中。 这些表达式可根据处理数据和配置的逻辑启用或禁用该格式的特定元素的输出。 可以在 **工序设计器** 页 **映射** 选项卡上的 **启用** 字段中为单个格式元素输入这些表达式。 您可以作为返回 *布尔* 值的逻辑条件输入表达式：

- 如果条件返回 **True**，当前格式元素将运行。
- 如果条件返回 **False**，当前格式元素将跳过。

下图显示了此类型的表达式。 （例如，Microsoft 提供的 **ISO20022 贷方转帐 (NO)** 格式配置的版本 11.12.11）。配置的 **XMLHeader** 格式组件用于描述采用 ISO 20022 XML 消息标准的贷方转帐消息的结构。 配置的 **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** 格式组件是为了向生成的消息添加 **Ustrd** XML 元素，并放置未结构化格式的汇款信息来充当以下 XML 元素的文本：

- **PaymentNotes** 组件用于生成付款附注的文本。
- **DelimitedSequence** 组件生成以逗号分隔的发票编号，用于结算当前贷方转帐。

[![PaymentNotes 和 DelimitedSequence 组件。](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes** 和 **DelimitedSequence** 组件使用问号标记。 问号表示组件的使用是有条件的。 在这种情况下，组件的使用基于以下条件：
>
> - 为 **PaymentNotes** 组件定义的 `@.PaymentsNotes <> ""` 表达式使（通过返回 **TRUE**） **Ustrd** XML 元素能够填充付款附注文本（如果该文本在当前贷方转帐中不是空白）。
>
>    [![PaymentNotes 组件的表达式。](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - 为 **DelimitedSequence** 组件定义的 `@.PaymentsNotes = ""` 表达式使（通过返回 **TRUE**）**Ustrd** XML 元素可以填充为用于结算当前贷方转帐的发票编号的逗号分隔列表（如果该贷方转帐的付款批注文本是空白的）。
>
>    [![DelimitedSequence 组件的表达式。](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> 根据此设置，为每笔借方付款生成的消息（**Ustrd** XML 元素）中将包含付款附注的文本，或当该文本为空时，则包含用于结算此付款的以逗号分隔的发票编号列表。

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>验证配置的公式

在 **公式设计器** 页面，选择 **测试** 验证配置的公式如何工作。

[![选择“测试”以验证公式。](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

当需要公式参数的值时，可以从 **公式设计器** 页打开 **测试表达式** 对话框。 在大多数情况下，这些参数必须手动定义，因为配置的绑定不是在设计时运行。 **公式设计器** 页面的 **测试结果** 选项卡将显示执行已配置公式的结果。

下面的示例显示如何测试为外贸域配置的公式，以确保内部统计商品代码仅包含数字。

测试此公式时，可以使用 **测试表达式** 对话框来指定用于测试的内部统计商品代码的值。

[![指定用于测试的内部统计商品代码。](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

指定内部统计商品代码并选择 **确定** 后，**公式设计器** 页面 **测试结果** 选项卡将显示执行已配置公式的结果。 然后，您可以评估结果是否可接受。 如果结果不可接受，您可以更新公式并再次进行测试。

[![测试结果。](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

有些公式无法在设计时测试。 例如，公式可能会返回无法显示在 **测试结果** 选项卡上的数据类型的结果。在这种情况下，您会收到一条错误消息，指示该公式无法测试。

[![错误消息。](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [电子申报公式语言](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
