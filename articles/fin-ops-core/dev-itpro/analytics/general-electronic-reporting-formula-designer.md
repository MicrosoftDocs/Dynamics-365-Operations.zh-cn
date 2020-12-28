---
title: 电子申报中 (ER) 的配方设计器
description: 本主题提供有关如何在电子申报 (ER) 中使用公式设计器的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d96fe041fd0ffb292909c1e724068efebe0184b9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682641"
---
# <a name="formula-designer-in-electronic-reporting-er"></a><span data-ttu-id="61e23-103">电子申报中 (ER) 的配方设计器</span><span class="sxs-lookup"><span data-stu-id="61e23-103">Formula designer in Electronic reporting (ER)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61e23-104">本主题说明如何在电子申报 (ER) 中使用配方设计器。</span><span class="sxs-lookup"><span data-stu-id="61e23-104">This topic explains how to use the formula designer in Electronic reporting (ER).</span></span> <span data-ttu-id="61e23-105">在您在 ER 中为特定电子文档设计格式时，您可以使用公式转换数据，以便使其满足该文档的履行和格式的要求。</span><span class="sxs-lookup"><span data-stu-id="61e23-105">When you design a format for a specific electronic document in ER, you can use formulas to transform data so that it meets the requirements for the document's fulfillment and formatting.</span></span> <span data-ttu-id="61e23-106">这些公式类似 Microsoft Excel 中的公式。</span><span class="sxs-lookup"><span data-stu-id="61e23-106">These formulas resemble formulas in Microsoft Excel.</span></span> <span data-ttu-id="61e23-107">公式中支持各种函数类型：文本、日期和时间、数学、逻辑、信息、数据类型转换函数，以及其他的企业域特定函数。</span><span class="sxs-lookup"><span data-stu-id="61e23-107">Various types of functions are supported in the formulas: text, date and time, mathematical, logical, information, and data type conversion functions, and also other, business domain–specific functions.</span></span>

## <a name="formula-designer-overview"></a><span data-ttu-id="61e23-108">配方设计器概览</span><span class="sxs-lookup"><span data-stu-id="61e23-108">Formula designer overview</span></span>

<span data-ttu-id="61e23-109">ER 支持公式设计器。</span><span class="sxs-lookup"><span data-stu-id="61e23-109">ER supports the formula designer.</span></span> <span data-ttu-id="61e23-110">因此，在设计时，您可以配置在运行时可用于执行以下任务的表达式：</span><span class="sxs-lookup"><span data-stu-id="61e23-110">Therefore, at design time, you can configure expressions that can be used for the following tasks at runtime:</span></span>

- <span data-ttu-id="61e23-111">将从应用程序数据库接收的数据以及应输入的数据转换为设计作为 ER 格式的数据源的 ER 数据模型。</span><span class="sxs-lookup"><span data-stu-id="61e23-111">Transform data that is received from an application database and that should be entered in an ER data model that is designed to be a data source for ER formats.</span></span> <span data-ttu-id="61e23-112">（例如，这些转换可以包括筛选、分组和数据转换类型。）</span><span class="sxs-lookup"><span data-stu-id="61e23-112">(For example, these transformations might include filtering, grouping, and data type conversion.)</span></span>
- <span data-ttu-id="61e23-113">设置必须发送到生成电子单据的数据的格式，以便满足特定 ER 格式的布局和条件。</span><span class="sxs-lookup"><span data-stu-id="61e23-113">Format data that must be sent to a generating electronic document in accordance with the layout and conditions of a specific ER format.</span></span> <span data-ttu-id="61e23-114">（例如，可以根据请求的语言、文化或编码完成格式化）。</span><span class="sxs-lookup"><span data-stu-id="61e23-114">(For example, the formatting might be done in accordance with the requested language or culture, or the encoding).</span></span>
- <span data-ttu-id="61e23-115">控制电子单据的创建过程。</span><span class="sxs-lookup"><span data-stu-id="61e23-115">Control the process of creating electronic documents.</span></span> <span data-ttu-id="61e23-116">（例如，表达式可根据处理数据启用或禁用该格式的特定元素的输出。</span><span class="sxs-lookup"><span data-stu-id="61e23-116">(For example, the expressions can enable or disable the output of specific elements of the format, depending on processing data.</span></span> <span data-ttu-id="61e23-117">还可以中断单据创建过程，或向用户显示消息。）</span><span class="sxs-lookup"><span data-stu-id="61e23-117">They can also interrupt the document creation process or throw messages to users.)</span></span>

<span data-ttu-id="61e23-118">执行以下任何操作时，可打开 **公式设计器** 页面：</span><span class="sxs-lookup"><span data-stu-id="61e23-118">You can open the **Formula designer** page when you perform any of the following actions:</span></span>

- <span data-ttu-id="61e23-119">数据源物料绑定到数据模型组件。</span><span class="sxs-lookup"><span data-stu-id="61e23-119">Bind data source items to data model components.</span></span>
- <span data-ttu-id="61e23-120">数据源物料绑定到格式组件。</span><span class="sxs-lookup"><span data-stu-id="61e23-120">Bind data source items to format components.</span></span>
- <span data-ttu-id="61e23-121">完成作为数据源的一部分的计算字段的维护。</span><span class="sxs-lookup"><span data-stu-id="61e23-121">Complete maintenance of calculated fields that are part of data sources.</span></span>
- <span data-ttu-id="61e23-122">定义用户输入参数的可见性条件。</span><span class="sxs-lookup"><span data-stu-id="61e23-122">Define the visibility conditions for user input parameters.</span></span>
- <span data-ttu-id="61e23-123">设计格式转换。</span><span class="sxs-lookup"><span data-stu-id="61e23-123">Design a format's transformations.</span></span>
- <span data-ttu-id="61e23-124">定义启用格式组件的条件。</span><span class="sxs-lookup"><span data-stu-id="61e23-124">Define the enabling conditions for the format's components.</span></span>
- <span data-ttu-id="61e23-125">定义格式的 FILE 组件的文件名。</span><span class="sxs-lookup"><span data-stu-id="61e23-125">Define the file names for the format's FILE components.</span></span>
- <span data-ttu-id="61e23-126">定义流程控制验证的条件。</span><span class="sxs-lookup"><span data-stu-id="61e23-126">Define the conditions for process control validations.</span></span>
- <span data-ttu-id="61e23-127">定义流程控制验证的消息文本。</span><span class="sxs-lookup"><span data-stu-id="61e23-127">Define the message text for process control validations.</span></span>

## <a name="data-binding"></a><a name="Binding"></a><span data-ttu-id="61e23-128">数据绑定</span><span class="sxs-lookup"><span data-stu-id="61e23-128">Data binding</span></span>

<span data-ttu-id="61e23-129">ER 公式设计器可以用于定义转换接收自数据源的数据的表达式，以便数据在运行时可以按以下方式在数据用户中输入数据：</span><span class="sxs-lookup"><span data-stu-id="61e23-129">The ER formula designer can be used to define an expression that transforms data that is received from data sources, so that the data can be entered in the data consumer in the following ways at runtime:</span></span>

- <span data-ttu-id="61e23-130">从应用程序数据源和运行时参数转换为 ER 数据模型</span><span class="sxs-lookup"><span data-stu-id="61e23-130">From application data sources and runtime parameters to an ER data model</span></span>
- <span data-ttu-id="61e23-131">从 ER 数据模型转换为 ER 格式</span><span class="sxs-lookup"><span data-stu-id="61e23-131">From an ER data model to an ER format</span></span>
- <span data-ttu-id="61e23-132">从应用程序数据源和运行时参数转换为 ER 格式</span><span class="sxs-lookup"><span data-stu-id="61e23-132">From application data sources and runtime parameters to an ER format</span></span>

<span data-ttu-id="61e23-133">下图显示了此类表达式的设计。</span><span class="sxs-lookup"><span data-stu-id="61e23-133">The following illustration shows the design of an expression of this type.</span></span> <span data-ttu-id="61e23-134">在此示例中，表达式将内部统计表中的 **Intrastat.AmountMST** 字段的值舍入到两位小数，然后返回舍入值。</span><span class="sxs-lookup"><span data-stu-id="61e23-134">In this example, the expression rounds the value of the **Intrastat.AmountMST** field in the Intrastat table to two decimal places and then returns the rounded value.</span></span>

<span data-ttu-id="61e23-135">[![数据绑定表达式](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-135">[![Data binding expression](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)</span></span>

<span data-ttu-id="61e23-136">下图显示了如何使用此类表达式。</span><span class="sxs-lookup"><span data-stu-id="61e23-136">The following illustration shows how an expression of this type can be used.</span></span> <span data-ttu-id="61e23-137">在此示例中，设计的表达式的结果输入在 **纳税申报模型** 数据模型的 **Transaction.InvoicedAmount** 组件中。</span><span class="sxs-lookup"><span data-stu-id="61e23-137">In this example, the result of the designed expression is entered in the **Transaction.InvoicedAmount** component of the **Tax reporting model** data model.</span></span>

<span data-ttu-id="61e23-138">[![使用的数据绑定表达式](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-138">[![Data binding expression being used](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)</span></span>

<span data-ttu-id="61e23-139">运行时，设计的公式 `ROUND (Intrastat.AmountMST, 2)` 将内部统计表中各记录的 **AmountMST** 字段的值舍入为两位小数。</span><span class="sxs-lookup"><span data-stu-id="61e23-139">At runtime, the designed formula, `ROUND (Intrastat.AmountMST, 2)`, rounds the value of the **AmountMST** field for each record in the Intrastat table to two decimal places.</span></span> <span data-ttu-id="61e23-140">然后在 **纳税申报** 数据模型的 **Transaction.InvoicedAmount** 组件中输入化整后的值。</span><span class="sxs-lookup"><span data-stu-id="61e23-140">It then enters the rounded value in the **Transaction.InvoicedAmount** component of the **Tax reporting** data model.</span></span>

## <a name="data-formatting"></a><a name="Transformation"></a><span data-ttu-id="61e23-141">数据格式设置</span><span class="sxs-lookup"><span data-stu-id="61e23-141">Data formatting</span></span>

<span data-ttu-id="61e23-142">ER 配方设计器可以用于定义确定接收自数据源的数据的格式的表达式，以便数据可以作为生成电子文档的一部分发送。</span><span class="sxs-lookup"><span data-stu-id="61e23-142">The ER formula designer can be used to define an expression that formats data that is received from data sources, so that the data can be sent as part of the generating electronic document.</span></span> <span data-ttu-id="61e23-143">可能必须将格式设置作为应对某种格式重复使用的典型规则来应用。</span><span class="sxs-lookup"><span data-stu-id="61e23-143">You might have formatting that must be applied as a typical rule that should be reused for a format.</span></span> <span data-ttu-id="61e23-144">在这种情况下，可将该格式设置在格式配置中引入一次，作为具有格式设置表达式的指定转换。</span><span class="sxs-lookup"><span data-stu-id="61e23-144">In this case, you can introduce that formatting one time in the format configuration, as a named transformation that has a formatting expression.</span></span> <span data-ttu-id="61e23-145">此指定的转换然后可链接到许多格式组件，这些组件是必须根据创建的格式表达式设置其输出的格式。</span><span class="sxs-lookup"><span data-stu-id="61e23-145">This named transformation can then be linked to many format components where the output must be formatted according to the formatting expression that you created.</span></span>

<span data-ttu-id="61e23-146">下图显示了此类转换的设计。</span><span class="sxs-lookup"><span data-stu-id="61e23-146">The following illustration shows the design of a transformation of this type.</span></span> <span data-ttu-id="61e23-147">在此示例中，**TrimmedString** 转换通过去除前导空格和尾随空格截断 *字符串* 数据类型的传入数据。</span><span class="sxs-lookup"><span data-stu-id="61e23-147">In this example, the **TrimmedString** transformation truncates incoming data of the *String* data type by removing leading and trailing spaces.</span></span> <span data-ttu-id="61e23-148">然后返回截断后的字符串值。</span><span class="sxs-lookup"><span data-stu-id="61e23-148">It then returns the truncated string value.</span></span>

<span data-ttu-id="61e23-149">[![转换](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-149">[![Transformation](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)</span></span>

<span data-ttu-id="61e23-150">下图显示了如何使用此类转换。</span><span class="sxs-lookup"><span data-stu-id="61e23-150">The following illustration shows how a transformation of this type can be used.</span></span> <span data-ttu-id="61e23-151">在此示例中，若干格式组件在运行时将文本作为输出发送到生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="61e23-151">In this example, several format components send text as output to the generating electronic document at runtime.</span></span> <span data-ttu-id="61e23-152">所有这些组件名义上引用 **TrimmedString** 转换。</span><span class="sxs-lookup"><span data-stu-id="61e23-152">All these format components refer to the **TrimmedString** transformation by name.</span></span>

<span data-ttu-id="61e23-153">[![正在使用的转换](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-153">[![Transformation being used](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)</span></span>

<span data-ttu-id="61e23-154">上图中 **partyName** 组件之类格式组件引用 **TrimmedString** 转换时，该转换将把文本作为输出发送到生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="61e23-154">When format components, such as the **partyName** component in the preceding illustration, refer to the **TrimmedString** transformation, the transformation sends text as output to the generating electronic document.</span></span> <span data-ttu-id="61e23-155">此文本中不包含前导空格和尾随空格。</span><span class="sxs-lookup"><span data-stu-id="61e23-155">This text doesn't include leading and trailing spaces.</span></span>

<span data-ttu-id="61e23-156">如果您具有必须单独应用的格式，可以将此格式作为特定格式组件绑定的单个表达式引入。</span><span class="sxs-lookup"><span data-stu-id="61e23-156">If you have formatting that must be applied individually, you can introduce that formatting as an individual expression of a binding of a specific format component.</span></span> <span data-ttu-id="61e23-157">下图显示了此类表达式。</span><span class="sxs-lookup"><span data-stu-id="61e23-157">The following illustration shows an expression of this type.</span></span> <span data-ttu-id="61e23-158">在此示例中，**partyType** 格式组件通过将数据源中 **Model.Company.RegistrationType** 字段的传入数据转换为大写文本的表达式绑定到数据源。</span><span class="sxs-lookup"><span data-stu-id="61e23-158">In this example, the **partyType** format component is bound to the data source via an expression that converts incoming data from the **Model.Company.RegistrationType** field in the data source to uppercase text.</span></span> <span data-ttu-id="61e23-159">然后，该表达式将该文本作为输出发送到电子单据。</span><span class="sxs-lookup"><span data-stu-id="61e23-159">The expression then sends that text as output to the electronic document.</span></span>

<span data-ttu-id="61e23-160">[![将格式应用于单个组件](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-160">[![Applying formatting to an individual component](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)</span></span>

## <a name="process-flow-control"></a><a name="Validation"></a><span data-ttu-id="61e23-161">流程控制</span><span class="sxs-lookup"><span data-stu-id="61e23-161">Process flow control</span></span>

<span data-ttu-id="61e23-162">ER 格式设计器可用于定义控制生成电子单据的流程的表达式。</span><span class="sxs-lookup"><span data-stu-id="61e23-162">The ER formula designer can be used to define expressions that control the process flow of generating electronic documents.</span></span> <span data-ttu-id="61e23-163">您可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="61e23-163">You can perform the following tasks:</span></span>

- <span data-ttu-id="61e23-164">定义确定必须停止文档创建流程的条件。</span><span class="sxs-lookup"><span data-stu-id="61e23-164">Define conditions that determine when a document creation process must be stopped.</span></span>
- <span data-ttu-id="61e23-165">指定表达式，这些表达式将创建有关已停止流程的用户的消息或引发有关继续报表生成流程的执行日志消息。</span><span class="sxs-lookup"><span data-stu-id="61e23-165">Specify expressions that either create messages for the user about stopped processes or throw execution log messages about the continuing process of report generation.</span></span>
- <span data-ttu-id="61e23-166">指定生成电子单据的文件名并控制其创建的条件。</span><span class="sxs-lookup"><span data-stu-id="61e23-166">Specify the file names of generating electronic documents, and control the conditions of their creation.</span></span>

<span data-ttu-id="61e23-167">流程控制的每个规则设计为单个验证。</span><span class="sxs-lookup"><span data-stu-id="61e23-167">Each rule of the process flow control is designed as an individual validation.</span></span> <span data-ttu-id="61e23-168">下图显示了此类验证。</span><span class="sxs-lookup"><span data-stu-id="61e23-168">The following illustration shows a validation of this type.</span></span> <span data-ttu-id="61e23-169">此示例中是对配置的说明：</span><span class="sxs-lookup"><span data-stu-id="61e23-169">Here is an explanation of the configuration in this example:</span></span>

- <span data-ttu-id="61e23-170">在 **INSTAT** 节点在生成 XML 文件期间创建时，将对验证进行评估。</span><span class="sxs-lookup"><span data-stu-id="61e23-170">The validation is evaluated when the **INSTAT** node is created during generation of the XML file.</span></span>
- <span data-ttu-id="61e23-171">如果事务列表为空，验证将停止执行流程并返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="61e23-171">If the list of transactions is empty, the validation stops the execution process and returns **FALSE**.</span></span>
- <span data-ttu-id="61e23-172">验证返回使用用户首选语言的包括标签 SYS70894 文本的错误消息。</span><span class="sxs-lookup"><span data-stu-id="61e23-172">The validation returns an error message that includes the text of label SYS70894 in the user's preferred language.</span></span>

<span data-ttu-id="61e23-173">[![验证](./media/picture-validation.jpg)](./media/picture-validation.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-173">[![Validation](./media/picture-validation.jpg)](./media/picture-validation.jpg)</span></span>

<span data-ttu-id="61e23-174">ER 配方设计器还可用于生成文件名来生成电子单据和控制文件创建流程。</span><span class="sxs-lookup"><span data-stu-id="61e23-174">The ER formula designer can also be used to generate a file name for a generating electronic document and to control the file creation process.</span></span> <span data-ttu-id="61e23-175">下图显示了此类流程控制的设计。</span><span class="sxs-lookup"><span data-stu-id="61e23-175">The following illustration shows the design of a process flow control of this type.</span></span> <span data-ttu-id="61e23-176">此示例中是对配置的说明：</span><span class="sxs-lookup"><span data-stu-id="61e23-176">Here is an explanation of the configuration in this example:</span></span>

- <span data-ttu-id="61e23-177">**model.Intrastat** 数据源的记录列表拆分为多个批次。</span><span class="sxs-lookup"><span data-stu-id="61e23-177">The list of records from the **model.Intrastat** data source is divided into batches.</span></span> <span data-ttu-id="61e23-178">每个批次最多包含 1,000 条记录。</span><span class="sxs-lookup"><span data-stu-id="61e23-178">Each batch contains up to 1,000 records.</span></span>
- <span data-ttu-id="61e23-179">输出创建以 XML 格式为创建的每个批次包含一个文件的压缩文件。</span><span class="sxs-lookup"><span data-stu-id="61e23-179">The output creates a zip file that contains one file in XML format for every batch that was created.</span></span>
- <span data-ttu-id="61e23-180">表达式通过连接文件名和文件名扩展返回生成电子文档的文件名。</span><span class="sxs-lookup"><span data-stu-id="61e23-180">An expression returns a file name for generating electronic documents by concatenating the file name and the file name extension.</span></span> <span data-ttu-id="61e23-181">对于第二个批次和所有后续的批次，文件名作为后缀包含批次 ID。</span><span class="sxs-lookup"><span data-stu-id="61e23-181">For the second batch and all subsequent batches, the file name contains the batch ID as a suffix.</span></span>
- <span data-ttu-id="61e23-182">表达式为包含至少一条记录的批次启用（通过返回 **TRUE**）文件创建流程。</span><span class="sxs-lookup"><span data-stu-id="61e23-182">An expression enables (by returning **TRUE**) the file creation process for batches that contain at least one record.</span></span>

<span data-ttu-id="61e23-183">[![流程控制](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)</span><span class="sxs-lookup"><span data-stu-id="61e23-183">[![Process flow control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)</span></span>

## <a name="document-content-control"></a><a name="Enabled"></a><span data-ttu-id="61e23-184">单据内容控制</span><span class="sxs-lookup"><span data-stu-id="61e23-184">Document content control</span></span>

<span data-ttu-id="61e23-185">可使用 ER 配方设计器配置表达式，用于控制运行时将哪些数据放到生成的电子单据中。</span><span class="sxs-lookup"><span data-stu-id="61e23-185">The ER formula designer can be used to configure expressions that control what data will be put into generated electronic documents at runtime.</span></span> <span data-ttu-id="61e23-186">这些表达式可根据处理数据和配置的逻辑启用或禁用该格式的特定元素的输出。</span><span class="sxs-lookup"><span data-stu-id="61e23-186">The expressions can enable or disable the output of specific elements of the format, depending on processing data and configured logic.</span></span> <span data-ttu-id="61e23-187">可以在 **工序设计器** 页 **映射** 选项卡上的 **启用** 字段中为单个格式元素输入这些表达式。</span><span class="sxs-lookup"><span data-stu-id="61e23-187">These expressions can be entered for a single format element in the **Enabled** field on the **Mapping** tab of the **Operations designer** page.</span></span> <span data-ttu-id="61e23-188">您可以作为返回 *布尔* 值的逻辑条件输入表达式：</span><span class="sxs-lookup"><span data-stu-id="61e23-188">You can enter the expressions as a logic condition that returns a *Boolean* value:</span></span>

- <span data-ttu-id="61e23-189">如果条件返回 **True**，当前格式元素将运行。</span><span class="sxs-lookup"><span data-stu-id="61e23-189">If the condition returns **True**, the current format element is run.</span></span>
- <span data-ttu-id="61e23-190">如果条件返回 **False**，当前格式元素将跳过。</span><span class="sxs-lookup"><span data-stu-id="61e23-190">If the condition returns **False**, the current format element is skipped.</span></span>

<span data-ttu-id="61e23-191">下图显示了此类型的表达式。</span><span class="sxs-lookup"><span data-stu-id="61e23-191">The following illustration shows expressions of this type.</span></span> <span data-ttu-id="61e23-192">（例如，Microsoft 提供的 **ISO20022 贷方转帐 (NO)** 格式配置的版本 11.12.11）。配置的 **XMLHeader** 格式组件用于描述采用 ISO 20022 XML 消息标准的贷方转帐消息的结构。</span><span class="sxs-lookup"><span data-stu-id="61e23-192">(Version 11.12.11 of the **ISO20022 Credit transfer (NO)** format configuration that is provided by Microsoft is used as an example.) The **XMLHeader** format component is configured to describe the structure of the credit transfer message according to the ISO 20022 XML message standards.</span></span> <span data-ttu-id="61e23-193">配置的 **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** 格式组件是为了向生成的消息添加 **Ustrd** XML 元素，并放置未结构化格式的汇款信息来充当以下 XML 元素的文本：</span><span class="sxs-lookup"><span data-stu-id="61e23-193">The **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** format component is configured to add the **Ustrd** XML element to the generated message and to put the remittance information in an unstructured format as text of the following XML elements:</span></span>

- <span data-ttu-id="61e23-194">**PaymentNotes** 组件用于生成付款附注的文本。</span><span class="sxs-lookup"><span data-stu-id="61e23-194">The **PaymentNotes** component is used to generate the text of payment notes.</span></span>
- <span data-ttu-id="61e23-195">**DelimitedSequence** 组件生成以逗号分隔的发票编号，用于结算当前贷方转帐。</span><span class="sxs-lookup"><span data-stu-id="61e23-195">The **DelimitedSequence** component generates comma-separated invoice numbers that are used to settle the current credit transfer.</span></span>

<span data-ttu-id="61e23-196">[![PaymentNotes 和 DelimitedSequence 组件](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-196">[![PaymentNotes and DelimitedSequence components](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)</span></span>

> [!NOTE]
> <span data-ttu-id="61e23-197">**PaymentNotes** 和 **DelimitedSequence** 组件使用问号标记。</span><span class="sxs-lookup"><span data-stu-id="61e23-197">The **PaymentNotes** and **DelimitedSequence** components are labeled by using a question mark.</span></span> <span data-ttu-id="61e23-198">问号表示组件的使用是有条件的。</span><span class="sxs-lookup"><span data-stu-id="61e23-198">A question mark indicates that the use of a component is conditional.</span></span> <span data-ttu-id="61e23-199">在这种情况下，组件的使用基于以下条件：</span><span class="sxs-lookup"><span data-stu-id="61e23-199">In this case, use of the components is based on the following criteria:</span></span>
>
> - <span data-ttu-id="61e23-200">为 **PaymentNotes** 组件定义的 `@.PaymentsNotes <> ""` 表达式使（通过返回 **TRUE**） **Ustrd** XML 元素能够填充付款附注文本（如果该文本在当前贷方转帐中不是空白）。</span><span class="sxs-lookup"><span data-stu-id="61e23-200">The `@.PaymentsNotes <> ""` expression that is defined for the **PaymentNotes** component enables (by returning **TRUE**) the **Ustrd** XML element to be filled with the text of payment notes, if that text isn't blank for the current credit transfer.</span></span>
>
>    <span data-ttu-id="61e23-201">[![PaymentNotes 组件的表达式](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-201">[![Expression for the PaymentNotes component](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)</span></span>
>
> - <span data-ttu-id="61e23-202">为 **DelimitedSequence** 组件定义的 `@.PaymentsNotes = ""` 表达式使（通过返回 **TRUE**）**Ustrd** XML 元素可以填充为用于结算当前贷方转帐的发票编号的逗号分隔列表（如果该贷方转帐的付款批注文本是空白的）。</span><span class="sxs-lookup"><span data-stu-id="61e23-202">The `@.PaymentsNotes = ""` expression that is defined for the **DelimitedSequence** component enables (by returning **TRUE**) the **Ustrd** XML element to be filled with a comma-separated list of the invoice numbers that are used to settle the current credit transfer, if the text of payment notes for that credit transfer is blank.</span></span>
>
>    <span data-ttu-id="61e23-203">[![DelimitedSequence 组件的表达式](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-203">[![Expression for the DelimitedSequence component](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)</span></span>
> 
> <span data-ttu-id="61e23-204">根据此设置，为每笔借方付款生成的消息（**Ustrd** XML 元素）中将包含付款附注的文本，或当该文本为空时，则包含用于结算此付款的以逗号分隔的发票编号列表。</span><span class="sxs-lookup"><span data-stu-id="61e23-204">Based on this setup, the message that is generated for each debtor payment, the **Ustrd** XML element, will contain either the text of payment notes or, when that text is blank, a comma-separated list of the invoice numbers that are used to settle the payment.</span></span>

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a><span data-ttu-id="61e23-205">验证配置的公式</span><span class="sxs-lookup"><span data-stu-id="61e23-205">Validation of configured formulas</span></span>

<span data-ttu-id="61e23-206">在 **公式设计器** 页面，选择 **测试** 验证配置的公式如何工作。</span><span class="sxs-lookup"><span data-stu-id="61e23-206">On the **Formula designer** page, select **Test** to validate how the configured formula works.</span></span>

<span data-ttu-id="61e23-207">[![选择“测试”验证公式](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-207">[![Selecting Test to validate a forumula](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)</span></span>

<span data-ttu-id="61e23-208">当需要公式参数的值时，可以从 **公式设计器** 页打开 **测试表达式** 对话框。</span><span class="sxs-lookup"><span data-stu-id="61e23-208">When the values of formula arguments are required, you can open the **Test expression** dialog box from the **Formula designer** page.</span></span> <span data-ttu-id="61e23-209">在大多数情况下，这些参数必须手动定义，因为配置的绑定不是在设计时运行。</span><span class="sxs-lookup"><span data-stu-id="61e23-209">In most cases, these arguments must be manually defined, because the configured bindings aren't run at design time.</span></span> <span data-ttu-id="61e23-210">**公式设计器** 页面的 **测试结果** 选项卡将显示执行已配置公式的结果。</span><span class="sxs-lookup"><span data-stu-id="61e23-210">The **Test result** tab on the **Formula designer** page shows the result from execution of the configured formula.</span></span>

<span data-ttu-id="61e23-211">下面的示例显示如何测试为外贸域配置的公式，以确保内部统计商品代码仅包含数字。</span><span class="sxs-lookup"><span data-stu-id="61e23-211">The following example shows how you can test the formula that is configured for the foreign trade domain to make sure that the Intrastat commodity code contains only digits.</span></span>

<span data-ttu-id="61e23-212">测试此公式时，可以使用 **测试表达式** 对话框来指定用于测试的内部统计商品代码的值。</span><span class="sxs-lookup"><span data-stu-id="61e23-212">When you test this formula, you can use the **Test expression** dialog box to specify the value of the Intrastat commodity code for testing.</span></span>

<span data-ttu-id="61e23-213">[![指定用于测试的内部统计商品代码](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-213">[![Specifying the Intrastat commodity code for testing](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)</span></span>

<span data-ttu-id="61e23-214">指定内部统计商品代码并选择 **确定** 后，**公式设计器** 页面 **测试结果** 选项卡将显示执行已配置公式的结果。</span><span class="sxs-lookup"><span data-stu-id="61e23-214">After you specify the Intrastat commodity code and select **OK**, the **Test result** tab on the **Formula designer** page shows the result of execution of the configured formula.</span></span> <span data-ttu-id="61e23-215">然后，您可以评估结果是否可接受。</span><span class="sxs-lookup"><span data-stu-id="61e23-215">You can then evaluate whether the result is acceptable.</span></span> <span data-ttu-id="61e23-216">如果结果不可接受，您可以更新公式并再次进行测试。</span><span class="sxs-lookup"><span data-stu-id="61e23-216">If the result isn't acceptable, you can update the formula and test it again.</span></span>

<span data-ttu-id="61e23-217">[![测试结果](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-217">[![Test result](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)</span></span>

<span data-ttu-id="61e23-218">有些公式无法在设计时测试。</span><span class="sxs-lookup"><span data-stu-id="61e23-218">Some formulas can't be tested at design time.</span></span> <span data-ttu-id="61e23-219">例如，公式可能会返回无法显示在 **测试结果** 选项卡上的数据类型的结果。在这种情况下，您会收到一条错误消息，指示该公式无法测试。</span><span class="sxs-lookup"><span data-stu-id="61e23-219">For example, a formula might return a result of a data type that can't be shown on the **Test result** tab. In this case, you receive an error message that states that the formula can't be tested.</span></span>

<span data-ttu-id="61e23-220">[![错误消息](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)</span><span class="sxs-lookup"><span data-stu-id="61e23-220">[![Error message](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61e23-221">其他资源</span><span class="sxs-lookup"><span data-stu-id="61e23-221">Additional resources</span></span>

- [<span data-ttu-id="61e23-222">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="61e23-222">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="61e23-223">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="61e23-223">Electronic reporting formula language</span></span>](er-formula-language.md)
