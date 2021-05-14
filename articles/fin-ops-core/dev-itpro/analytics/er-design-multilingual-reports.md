---
title: 在电子报告中设计多语言报告
description: 本主题说明如何使用电子报告 (ER) 标签来设计和生成多语言报告。
author: NickSelin
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50156b8c6b3553b02d092fad9c72e90c1f70ff78
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951977"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a><span data-ttu-id="904b5-103">在电子报告中设计多语言报告</span><span class="sxs-lookup"><span data-stu-id="904b5-103">Design multilingual reports in Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="904b5-104">概览</span><span class="sxs-lookup"><span data-stu-id="904b5-104">Overview</span></span>

<span data-ttu-id="904b5-105">作为业务用户，您可以使用[电子报告 (ER)](general-electronic-reporting.md) 框架根据各个国家或地区的法律要求配置必须生成的传出文档的格式。</span><span class="sxs-lookup"><span data-stu-id="904b5-105">As a business user, you can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to configure formats for outbound documents that must be generated in accordance with the legal requirements of various countries or regions.</span></span> <span data-ttu-id="904b5-106">当这些要求需要针对不同国家或地区以不同语言生成传出文档时，您可以配置一个包含语言相关资源的 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)。</span><span class="sxs-lookup"><span data-stu-id="904b5-106">When these requirements demand that outbound documents be generated in different languages for different countries or regions, you can configure a single ER [format](general-electronic-reporting.md#FormatComponentOutbound) that contains language-dependent resources.</span></span> <span data-ttu-id="904b5-107">这样，您可以重用此格式来生成各个国家或地区的传出文档。</span><span class="sxs-lookup"><span data-stu-id="904b5-107">In that way, you can reuse the format to generate outbound documents for various countries or regions.</span></span> <span data-ttu-id="904b5-108">您可能还希望使用一个 ER 格式为相应的客户、供应商、子公司或任何其他方生成不同语言的传出文档。</span><span class="sxs-lookup"><span data-stu-id="904b5-108">You might also want to use a single ER format to generate an outbound document in different languages for corresponding customers, vendors, subsidiaries, or any other parties.</span></span>

<span data-ttu-id="904b5-109">您可以将 ER 数据模型和模型映射配置为已配置的 ER 格式的数据源，来定义指定将哪些应用程序数据放入生成的文档的数据流。</span><span class="sxs-lookup"><span data-stu-id="904b5-109">You can configure ER data models and model mappings as the data sources of configured ER formats to define the data flow that specifies what application data is put into generated documents.</span></span> <span data-ttu-id="904b5-110">作为 ER 配置[提供者](general-electronic-reporting.md#Provider)，您可以[发布](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs)配置的[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)、[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)和[格式](general-electronic-reporting.md#FormatComponentOutbound)作为 ER 解决方案的组成部分，来生成特定的传出文档。</span><span class="sxs-lookup"><span data-stu-id="904b5-110">As an ER configuration [provider](general-electronic-reporting.md#Provider), you can [publish](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) configured [data models](general-electronic-reporting.md#data-model-and-model-mapping-components), [model mappings](general-electronic-reporting.md#data-model-and-model-mapping-components), and [formats](general-electronic-reporting.md#FormatComponentOutbound) as components of an ER solution to generate specific outbound documents.</span></span> <span data-ttu-id="904b5-111">您还可以允许客户[上载](general-electronic-reporting-manage-configuration-lifecycle.md)已发布的 ER 解决方案，以便可以使用和定制该解决方案。</span><span class="sxs-lookup"><span data-stu-id="904b5-111">You can also allow customers to [upload](general-electronic-reporting-manage-configuration-lifecycle.md) the published ER solution so that it can be used and customized.</span></span> <span data-ttu-id="904b5-112">如果您希望客户讲其他语言，则可以配置 ER 组件，使其包含语言相关资源。</span><span class="sxs-lookup"><span data-stu-id="904b5-112">If you expect that customers might speak other languages, you can configure the ER components so that they contain language-dependent resources.</span></span> <span data-ttu-id="904b5-113">以此方式，可在设计时以客户的用户首选语言呈现可编辑 ER 组件的内容。</span><span class="sxs-lookup"><span data-stu-id="904b5-113">In that way, the content of an editable ER component can be presented in a customer's user-preferred language at design time.</span></span>

<span data-ttu-id="904b5-114">您可以将语言相关资源配置为 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-114">You can configure language-dependent resources as ER labels.</span></span> <span data-ttu-id="904b5-115">然后，可以使用这些标签来配置 ER 组件以用于以下目的：</span><span class="sxs-lookup"><span data-stu-id="904b5-115">You can then use those labels to configure ER components for the following purposes:</span></span>

- <span data-ttu-id="904b5-116">在设计时：</span><span class="sxs-lookup"><span data-stu-id="904b5-116">At design time:</span></span>

    - <span data-ttu-id="904b5-117">以用户首选语言呈现已配置的 ER 组件的内容。</span><span class="sxs-lookup"><span data-stu-id="904b5-117">Present the content of configured ER components in the user-preferred language.</span></span>

- <span data-ttu-id="904b5-118">在运行时：</span><span class="sxs-lookup"><span data-stu-id="904b5-118">At runtime:</span></span>

    - <span data-ttu-id="904b5-119">为传出文档生成语言相关内容。</span><span class="sxs-lookup"><span data-stu-id="904b5-119">Generate language-dependent content for outbound documents.</span></span>
    - <span data-ttu-id="904b5-120">以用户首选语言提供警告和错误消息。</span><span class="sxs-lookup"><span data-stu-id="904b5-120">Provide warning and error messages in the user-preferred language.</span></span>
    - <span data-ttu-id="904b5-121">以用户首选语言提示必填字段。</span><span class="sxs-lookup"><span data-stu-id="904b5-121">Prompt for required fields in the user-preferred language.</span></span>

<span data-ttu-id="904b5-122">可以在包含不同组件的每个 ER [配置](general-electronic-reporting.md#Configuration)中配置 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-122">ER labels can be configured in every ER [configuration](general-electronic-reporting.md#Configuration) that contains different components.</span></span> <span data-ttu-id="904b5-123">可以独立于 ER 数据模型、ER 模型映射和 ER 格式组件的已配置逻辑来维护标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-123">The labels can be maintained independently of the configured logic of ER data models, ER model mappings, and ER format components.</span></span>

<span data-ttu-id="904b5-124">每个 ER 标签由一个 ID 标识，该 ID 在保留该标签的 ER 配置范围内是唯一的。</span><span class="sxs-lookup"><span data-stu-id="904b5-124">Every ER label is identified by an ID that is unique in the scope of the ER configuration that holds that label.</span></span> <span data-ttu-id="904b5-125">每个标签可以包含 Microsoft Dynamics 365 Finance 的当前实例中支持的每种语言的标签文本。</span><span class="sxs-lookup"><span data-stu-id="904b5-125">Every label can contain label text for every language that is supported in the current instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="904b5-126">这些受支持的语言包括已部署的自定义项的语言。</span><span class="sxs-lookup"><span data-stu-id="904b5-126">These supported languages include the languages of deployed customizations.</span></span>

## <a name="entry"></a><span data-ttu-id="904b5-127">条目</span><span class="sxs-lookup"><span data-stu-id="904b5-127">Entry</span></span>

<span data-ttu-id="904b5-128">在设计 ER 数据模型、ER 模型映射或 ER 格式时，每当您选择一个可能包含可翻译上下文的字段时，就会显示 **翻译** 选项。</span><span class="sxs-lookup"><span data-stu-id="904b5-128">When you design an ER data model, an ER model mapping, or an ER format, the **Translate** option is shown whenever you select a field that might contain the translatable context.</span></span> <span data-ttu-id="904b5-129">选择此选项时，可以将所选字段链接到 **文本翻译**<a name="TextTranslationPane">窗格</a>上的 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-129">When you select this option, you can link the selected field to an ER label on the **Text translation** <a name="TextTranslationPane">pane</a>.</span></span> <span data-ttu-id="904b5-130">您可以选择现有 ER 标签，也可以添加新 ER 标签（如果尚不可用）。</span><span class="sxs-lookup"><span data-stu-id="904b5-130">You can select an existing ER label, or you can add a new ER label if it isn't available yet.</span></span> <span data-ttu-id="904b5-131">选择或添加 ER 标签时，可以为当前 Finance 实例支持的每种语言添加相关文本。</span><span class="sxs-lookup"><span data-stu-id="904b5-131">When you select or add an ER label, you can add related text for every language that is supported in the current Finance instance.</span></span>

<span data-ttu-id="904b5-132">下图显示了如何在可编辑 ER 数据模型中完成此翻译。</span><span class="sxs-lookup"><span data-stu-id="904b5-132">The following illustration shows how this translation is done in an editable ER data model.</span></span> <span data-ttu-id="904b5-133">在此示例中，可编辑 **发票模型** 的 **PurchaseOrder** 字段的 **描述** 属性被翻译为奥地利德语 (DE-AT) 和日语 (JA) 语言。</span><span class="sxs-lookup"><span data-stu-id="904b5-133">In this example, the **Description** attribute of the **PurchaseOrder** field for the editable **Invoice model** is translated into the Austrian German (DE-AT) and Japanese (JA) languages.</span></span>

![在 ER 数据模型设计器中提供 ER 标签的翻译](./media/er-multilingual-labels-refer.png)

<span data-ttu-id="904b5-135">只能翻译位于可编辑 ER 组件中的标签的标签文本。</span><span class="sxs-lookup"><span data-stu-id="904b5-135">Only label text for labels that reside in an editable ER component can be translated.</span></span> <span data-ttu-id="904b5-136">例如，如果为 ER 模型映射数据源的标签属性选择 **翻译**，然后选择位于父 ER 数据模型中的 ER 标签，则会看到标签的内容，但是无法更改。</span><span class="sxs-lookup"><span data-stu-id="904b5-136">For example, if you select **Translate** for the label attribute of an ER model mapping data source, and you then select an ER label that resides in the parent ER data model, you will see the content of the label, but you can't change it.</span></span> <span data-ttu-id="904b5-137">在这些情况下，**已翻译的文本** 字段不可用，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="904b5-137">In these cases, the **Translated text** field is unavailable, as shown in the following illustration.</span></span>

![在 ER 模型映射设计器中查看提供的 ER 标签的翻译](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> <span data-ttu-id="904b5-139">您无法使用设计器删除已在可编辑 ER 组件中输入的标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-139">You can't use the designers to delete label that has been entered in an editable ER component.</span></span>

## <a name="scope"></a><span data-ttu-id="904b5-140">作用域</span><span class="sxs-lookup"><span data-stu-id="904b5-140">Scope</span></span>

<span data-ttu-id="904b5-141">ER 标签可以在 ER 组件的几个可翻译属性中引用。</span><span class="sxs-lookup"><span data-stu-id="904b5-141">ER labels can be referred to in several translatable attributes of ER components.</span></span>

### <a name="data-model-component"></a><span data-ttu-id="904b5-142">数据模型组件</span><span class="sxs-lookup"><span data-stu-id="904b5-142">Data model component</span></span>

<span data-ttu-id="904b5-143">配置 ER 数据模型时，可以为其添加 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-143">When you configure an ER data model, you can add ER labels for it.</span></span> <span data-ttu-id="904b5-144">可以将模型项目的 **标签** 和 **描述** 属性、每个模型的字段以及每个<a id="LinkModelEnum"></a>模型枚举值链接到一个已添加到 ER 数据模型中的 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-144">**Label** and **Description** attributes of the model item, every model's field, and every <a id="LinkModelEnum"></a>model enumeration value can be linked to an ER label that is added to the ER data model.</span></span>

![在 ER 数据模型设计器中为描述属性提供翻译](./media/er-multilingual-labels-refer.png)

<span data-ttu-id="904b5-146">当以这种方式配置 ER 数据模型时，其内容将以每个用户的首选语言呈现给 ER 数据模型设计器的用户。</span><span class="sxs-lookup"><span data-stu-id="904b5-146">When an ER data model is configured in this way, its content will be presented to users of the ER data model designer in each user's preferred language.</span></span> <span data-ttu-id="904b5-147">因此，简化了模型维护。</span><span class="sxs-lookup"><span data-stu-id="904b5-147">Therefore, model maintenance is simplified.</span></span> <span data-ttu-id="904b5-148">下图说明了将 DE-AT 和 JA 设置为首选语言的用户如何使用此功能。</span><span class="sxs-lookup"><span data-stu-id="904b5-148">The following illustrations show how this functionality works for users who have DE-AT and JA set as their preferred language.</span></span>

![将 DE-AT 设置为首选语言的用户的 ER 数据模型设计器的布局](./media/er-multilingual-labels-refer-de.png)

![将 JA 设置为首选语言的用户的 ER 数据模型设计器的布局](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a><span data-ttu-id="904b5-151">模型映射组件</span><span class="sxs-lookup"><span data-stu-id="904b5-151">Model mapping component</span></span>

<span data-ttu-id="904b5-152">因为 ER 模型映射基于 ER 数据模型，所以所引用的数据模型元素的标签在模型映射设计器中以用户的首选语言显示。</span><span class="sxs-lookup"><span data-stu-id="904b5-152">Because the ER model mapping is based on an ER data model, the labels of the data model elements that are referred to are appeared in the user's preferred language in the model mapping designer.</span></span> <span data-ttu-id="904b5-153">下图显示了如何通过使用已添加到已配置数据模型中的 **描述** 属性的标签，在可编辑模型映射中解释 **PurchaseOrder** 字段的含义。</span><span class="sxs-lookup"><span data-stu-id="904b5-153">The following illustration shows how the meaning of the **PurchaseOrder** field is explained in the editable model mapping by using the label of the **Description** attribute that has been added to the configured data model.</span></span> <span data-ttu-id="904b5-154">请注意，此标签以用户的首选语言（在此示例中为 DE-AT）呈现。</span><span class="sxs-lookup"><span data-stu-id="904b5-154">Notice that this label is presented in the user's preferred language (DE-AT in this example).</span></span>

![将 DE-AT 设置为首选语言的用户的 ER 模型映射设计器的布局](./media/er-multilingual-labels-show-mapping.png)

<span data-ttu-id="904b5-156">当将 **用户输入参数** 数据源的 **标签** 属性配置为链接到 ER 标签时，与此数据源对应的参数字段将在运行时在用户对话框中以用户首选语言呈现给用户。</span><span class="sxs-lookup"><span data-stu-id="904b5-156">When the **Label** attribute of the **User input parameter** data source is configured as linked to an ER label, the parameter field that corresponds to this data source is presented in the user dialog box at runtime to users in their preferred language.</span></span>

### <a name="format-component"></a><span data-ttu-id="904b5-157">格式组件</span><span class="sxs-lookup"><span data-stu-id="904b5-157">Format component</span></span>

<span data-ttu-id="904b5-158">配置 ER 格式时，可以为其添加 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-158">When you configure an ER format, you can add ER labels for it.</span></span> <span data-ttu-id="904b5-159">可以将每个已配置数据源的 **标签** 和 **帮助文本** 属性链接到添加到 ER 格式的 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-159">The **Label** and **Help text** attributes of every configured data source can be linked to an ER label that is added to the ER format.</span></span> <span data-ttu-id="904b5-160">每个 <a id="LinkFormatEnum"></a>格式枚举值的 **标签** 和 **描述** 属性也可以链接到可从可编辑 ER 格式访问的 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-160">The **Label** and **Description** attributes of every <a id="LinkFormatEnum"></a>format enumeration value can be also linked to an ER label that is accessible from the editable ER format.</span></span>

> [!NOTE]
> <span data-ttu-id="904b5-161">您还可以将这些属性链接到父 ER 数据模型的一个 ER 标签，该标签可以重用为此 ER 数据模型配置的每种 ER 格式的模型标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-161">You can also link these attributes to an ER label of the parent ER data model that reuses the model's labels in every ER format that is configured for this ER data model.</span></span>

<span data-ttu-id="904b5-162">当以这种方式配置 ER 格式时，格式的内容将以每个用户的首选语言呈现给 ER 操作设计器的用户。</span><span class="sxs-lookup"><span data-stu-id="904b5-162">When an ER format is configured in this way, the content of the format will be presented to users of the ER Operation designer in each user's preferred language.</span></span> <span data-ttu-id="904b5-163">因此，简化了配置逻辑的格式维护和分析。</span><span class="sxs-lookup"><span data-stu-id="904b5-163">Therefore, format maintenance and analysis of the configured logic are simplified.</span></span>

<span data-ttu-id="904b5-164">因为 ER 格式基于 ER 数据模型，所以将在 ER 格式设计器中以用户首选语言呈现数据模型元素中引用的标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-164">Because an ER format is based on an ER data model, the labels that are referred to in the data model elements are presented in the ER format designer in the user-preferred language.</span></span>

<span data-ttu-id="904b5-165">当将 **用户输入参数** 数据源的 **标签** 属性配置为链接到 ER 标签时，在运行时与用户对话框中的参数相对应的字段将作为提示呈现给用户。</span><span class="sxs-lookup"><span data-stu-id="904b5-165">When the **Label** attribute of the **User input parameter** data source is linked to an ER label, the field that corresponds to the parameter in the user dialog box at runtime is presented to the user as a prompt.</span></span> <span data-ttu-id="904b5-166">下图显示了如何在设计时将 **用户输入参数** 数据源的 **标签** 属性链接到 ER 标签，以便在运行时以不同的用户首选语言向用户提示参数（为美国英语 (EN-US) 和 DE-AT 语言显示）。</span><span class="sxs-lookup"><span data-stu-id="904b5-166">The following illustrations show how you can link the **Label** attribute of the **User input parameter** data source at design time to an ER label, so that users are prompted for the parameter in different user-preferred languages (shown for English United States (EN-US) and DE-AT languages) at runtime.</span></span>

![在 ER 操作设计器中提供用户输入参数的属性的翻译](./media/er-multilingual-labels-refer-format.png)

![运行时 EN-US 用户首选语言的 ER 供应商付款处理](./media/er-multilingual-labels-show-runtime-en.png)

![运行时 DE-AT 用户首选语言的 ER 供应商付款处理](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a><span data-ttu-id="904b5-170">表达式</span><span class="sxs-lookup"><span data-stu-id="904b5-170">Expressions</span></span>

<span data-ttu-id="904b5-171">要在 ER [表达式](er-formula-language.md)中使用标签，必须使用语法 **@"GER\_LABEL:X"**，其中前缀 **@** 表示操作数引用标签，**GER\_LABEL** 表示引入了 ER 标签，**X** 是 ER 标签 ID。</span><span class="sxs-lookup"><span data-stu-id="904b5-171">To use a label in an ER [expression](er-formula-language.md), you must use the syntax **@"GER\_LABEL:X"**, where the prefix **@** indicates that the operand refers to a label, **GER\_LABEL** indicates that an ER label is involved, and **X** is the ER label ID.</span></span>

![在 ER 公式设计器中配置包含对 ER 标签的引用的 ER 表达式](./media/er-multilingual-labels-expression1.png)

<span data-ttu-id="904b5-173">要引用系统（应用程序）标签，请使用语法 **@"X"**，其中前缀 **@** 表示操作数引用标签，**X** 是系统标签 ID。</span><span class="sxs-lookup"><span data-stu-id="904b5-173">To refer to a system (application) label, use the syntax **@"X"**, where the prefix **@** indicates that the operand refers to a label, and **X** is the system label ID.</span></span>

![在 ER 公式设计器中配置包含对应用程序标签的引用的 ER 表达式](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a><span data-ttu-id="904b5-175">模型映射</span><span class="sxs-lookup"><span data-stu-id="904b5-175">Model mapping</span></span>

<span data-ttu-id="904b5-176">可以使用标签来配置 ER 模型映射的表达式。</span><span class="sxs-lookup"><span data-stu-id="904b5-176">An expression of an ER model mapping can be configured by using a label.</span></span> <span data-ttu-id="904b5-177">当运行来生成传出文档的 ER 格式调用此映射时，执行的上下文将包括语言代码。</span><span class="sxs-lookup"><span data-stu-id="904b5-177">When this mapping is called by an ER format that is run to generate an outbound document, the context of the execution includes a language code.</span></span> <span data-ttu-id="904b5-178">配置的表达式标签将使用为该上下文的语言配置的标签文本填充。</span><span class="sxs-lookup"><span data-stu-id="904b5-178">A configured expression label will be filled in with the label text that has been configured for the language of that context.</span></span>

<span data-ttu-id="904b5-179">如果引用的标签没有对调用模型映射的格式执行上下文的语言的翻译，将改用 EN-US 语言的标签文本。</span><span class="sxs-lookup"><span data-stu-id="904b5-179">If a referenced label has no translation for the language of the format execution context that calls the model mapping, the label text in the EN-US language is used instead.</span></span>

#### <a name="format"></a><span data-ttu-id="904b5-180">格式</span><span class="sxs-lookup"><span data-stu-id="904b5-180">Format</span></span>

<span data-ttu-id="904b5-181">可以使用标签来配置 ER 格式的 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="904b5-181">An ER expression of an ER format can be configured by using labels.</span></span> <span data-ttu-id="904b5-182">当运行此格式来生成传出文档时，执行的上下文将包括语言代码。</span><span class="sxs-lookup"><span data-stu-id="904b5-182">When this format is run to generate an outbound document, the context of the execution includes a language code.</span></span> <span data-ttu-id="904b5-183">配置的表达式标签将使用为该上下文的语言配置的标签文本填充。</span><span class="sxs-lookup"><span data-stu-id="904b5-183">A configured expression label will be filled in with the label text that has been configured for the language of that context.</span></span>

![在 ER 公式设计器中提供可编辑 ER 表达式的 ER 标签的翻译](./media/er-multilingual-labels-refer-in-expression.png)

![在 ER 操作设计器中引用 ER 标签的数据绑定的示例](./media/er-multilingual-labels-refer-in-binding.png)

<span data-ttu-id="904b5-186">您可以配置 ER 格式的 **文件** 组件来以用户的首选语言生成报告。</span><span class="sxs-lookup"><span data-stu-id="904b5-186">You can configure the **FILE** component of an ER format to generate the report in the user's preferred language.</span></span>

![在 ER 操作设计器中设置 FILE 组件来以用户首选语言生成报告](./media/er-multilingual-labels-language-context-user.png)

<span data-ttu-id="904b5-188">如果以这种方式配置 ER 格式，将使用 ER 标签的相应文本生成报告。</span><span class="sxs-lookup"><span data-stu-id="904b5-188">If you configure an ER format in this way, the report is generated by using the corresponding text of the ER labels.</span></span> <span data-ttu-id="904b5-189">下图显示了 EN-US 和 DE-AT 用户语言的报告示例。</span><span class="sxs-lookup"><span data-stu-id="904b5-189">The following illustrations show examples of reports for the EN-US and DE-AT user languages.</span></span>

![以 EN-US 用户首选语言生成的报告的预览](./media/er-multilingual-labels-report-preview-en.png)

![以 DE-AT 用户首选语言生成的报告的预览](./media/er-multilingual-labels-report-preview-de.png)

<span data-ttu-id="904b5-192">如果引用的标签没有对格式执行上下文的语言的翻译，将改用 EN-US 语言的标签文本。</span><span class="sxs-lookup"><span data-stu-id="904b5-192">If a referenced label has no translation for the language of the format execution context, the label text in the EN-US language is used instead.</span></span>

## <a name="language"></a><span data-ttu-id="904b5-193">语言</span><span class="sxs-lookup"><span data-stu-id="904b5-193">Language</span></span>

<span data-ttu-id="904b5-194">ER 支持多种为生成的报告指定语言的方式。</span><span class="sxs-lookup"><span data-stu-id="904b5-194">ER supports different ways to specify a language for a generated report.</span></span> <span data-ttu-id="904b5-195">在 **格式** 选项卡上的 **语言首选项** 字段中，您可以选择以下值：</span><span class="sxs-lookup"><span data-stu-id="904b5-195">In the **Language preferences** field on the **Format** tab, you can select the following values:</span></span>

- <span data-ttu-id="904b5-196">**公司首选项** – 使用公司指定的语言生成报告。</span><span class="sxs-lookup"><span data-stu-id="904b5-196">**Company preference** – Generate a report in a company-specified language.</span></span>

    ![在 ER 操作设计器中指定公司首选语言作为生成的报告的语言](./media/er-multilingual-labels-language-context-company.png)

- <span data-ttu-id="904b5-198">**用户首选项** – 使用用户首选语言生成报告。</span><span class="sxs-lookup"><span data-stu-id="904b5-198">**User preference** – Generate a report in the user's preferred language.</span></span>
- <span data-ttu-id="904b5-199">**明确定义** – 使用在设计时指定的语言生成报告。</span><span class="sxs-lookup"><span data-stu-id="904b5-199">**Explicitly defined** – Generate a report in a language that is specified at design time.</span></span>

    ![在 ER 操作设计器中指定设计时定义的语言作为生成的报告的语言](./media/er-multilingual-labels-language-context-fixed.png)

- <span data-ttu-id="904b5-201">**运行时定义** – 使用在运行时指定的语言生成报告。</span><span class="sxs-lookup"><span data-stu-id="904b5-201">**Defined at run-time** – Generate a report in a language that is specified at runtime.</span></span> <span data-ttu-id="904b5-202">如果选择此值，请在 **语言** 字段中配置返回语言的语言代码的 ER 表达式，如相应客户的语言。</span><span class="sxs-lookup"><span data-stu-id="904b5-202">If you select this value, in the **Language** field, configure an ER expression that returns the language code for the language, such as the language of the corresponding customer.</span></span>

    ![在 ER 操作设计器中指定运行时定义的语言作为生成的报告的语言](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a><span data-ttu-id="904b5-204">区域性特定格式</span><span class="sxs-lookup"><span data-stu-id="904b5-204">Culture-specific formatting</span></span>

<span data-ttu-id="904b5-205">ER 支持多种为生成的报表指定区域性的方式。</span><span class="sxs-lookup"><span data-stu-id="904b5-205">ER supports different ways to specify the culture for a generated report.</span></span> <span data-ttu-id="904b5-206">因此，正确的区域性特定格式可以用于日期、时间和数字值。</span><span class="sxs-lookup"><span data-stu-id="904b5-206">Therefore, the correct culture-specific formatting can be used for date, time, and numeric values.</span></span> <span data-ttu-id="904b5-207">设计 ER 格式时，在 **格式** 选项卡上的 **区域性首选项** 字段中，可以为 **常见\\文件**、**Excel\\文件**、**PDF\\文件** 或 **PDF\\合并器** 类型的每个格式组件选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="904b5-207">When you design an ER format, on the **Format** tab, in the **Culture preferences** field, you can select one of the following values for every format component of the **Common\\File**, **Excel\\File**, **PDF\\File**, or **PDF\\Merger** type:</span></span>

- <span data-ttu-id="904b5-208">**用户首选项** – 根据用户的首选区域性确定值的格式。</span><span class="sxs-lookup"><span data-stu-id="904b5-208">**User preference** – Format the values according to the user's preferred culture.</span></span> <span data-ttu-id="904b5-209">该区域性在 **用户选项** 页 **首选项** 选项卡上的 **日期、时间和数字格式** 字段中定义。</span><span class="sxs-lookup"><span data-stu-id="904b5-209">That culture is defined in the **Date, time, and number format** field on the **Preferences** tab of the **User options** page.</span></span>

    ![在 ER 操作设计器中将用户的首选区域性定义为所生成报表的区域性](./media/er-multilingual-labels-culture-context-user-preferred.png)

- <span data-ttu-id="904b5-211">**明确定义** – 根据设计时指定的区域性确定值的格式。</span><span class="sxs-lookup"><span data-stu-id="904b5-211">**Explicitly defined** – Format the values according to the culture that is specified at design time.</span></span>

    ![在 ER 操作设计器中将在设计时指定的区域性定义为所生成报表的区域性](./media/er-multilingual-labels-culture-context-fixed.png)

- <span data-ttu-id="904b5-213">**运行时定义** – 根据运行时指定的区域性确定值的格式。</span><span class="sxs-lookup"><span data-stu-id="904b5-213">**Defined at run-time** – Format the values according to the culture that is specified at runtime.</span></span> <span data-ttu-id="904b5-214">如果选择此值，在 **映射** 选项卡上的 **日期、时间和数字格式** 字段中，配置一个 ER 表达式，以返回该区域性的区域性代码，如相应客户的区域性。</span><span class="sxs-lookup"><span data-stu-id="904b5-214">If you select this value, on the **Mapping** tab, in the **Date, time, and number format** field, configure an ER expression that returns the culture code for the culture, such as the culture of the corresponding customer.</span></span>

    ![在 ER 操作设计器中将在运行时定义的区域性定义为所生成报表的区域性](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> <span data-ttu-id="904b5-216">您为其定义特定区域性的 ER 组件可能包含配置为填充文本值的子 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="904b5-216">An ER component that you define a specific culture for might contain child ER components that were configured to fill in a text value.</span></span> <span data-ttu-id="904b5-217">默认情况下，父组件的区域性用于确定那些组件的值的格式。</span><span class="sxs-lookup"><span data-stu-id="904b5-217">By default, the culture of the parent component is used to format the values of those components.</span></span> <span data-ttu-id="904b5-218">您可以使用以下内置 ER 函数为那些组件配置绑定，并为值格式应用替代区域性：</span><span class="sxs-lookup"><span data-stu-id="904b5-218">You can use the following built-in ER functions to configure bindings for those components and apply an alternative culture for value formatting:</span></span>
>
> - [<span data-ttu-id="904b5-219">DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="904b5-219">DATEFORMAT</span></span>](er-functions-datetime-dateformat.md#syntax-2)
> - [<span data-ttu-id="904b5-220">DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="904b5-220">DATETIMEFORMAT</span></span>](er-functions-datetime-datetimeformat.md#syntax-2)
> - [<span data-ttu-id="904b5-221">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="904b5-221">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md#syntax-2)
>
> <span data-ttu-id="904b5-222">在版本 10.0.20 及更高版本中，**常见\\文件** 和 **Excel\\文件** 类型的格式组件的区域设置用于在生成文档的 [PDF 转换](electronic-reporting-destinations.md#OutputConversionToPDF)期间确定值的格式。</span><span class="sxs-lookup"><span data-stu-id="904b5-222">In version 10.0.20 and later, the locale of format components of the **Common\\File** and **Excel\\File** types is used to format values during [PDF conversion](electronic-reporting-destinations.md#OutputConversionToPDF) of a generated document.</span></span>

## <a name="translation"></a><span data-ttu-id="904b5-223">译文</span><span class="sxs-lookup"><span data-stu-id="904b5-223">Translation</span></span>

<span data-ttu-id="904b5-224">您可以将所需的 ER 标签添加到可编辑 ER 组件中。</span><span class="sxs-lookup"><span data-stu-id="904b5-224">You can add required ER labels to an editable ER component.</span></span> <span data-ttu-id="904b5-225">添加 ER 标签后，可以通过两种方式进行翻译：手动和自动。</span><span class="sxs-lookup"><span data-stu-id="904b5-225">When an ER label is added, it can be translated in two ways: manually and automatically.</span></span>

### <a name="manual-translation"></a><span data-ttu-id="904b5-226">手动翻译</span><span class="sxs-lookup"><span data-stu-id="904b5-226">Manual translation</span></span>

<span data-ttu-id="904b5-227">在 **文本翻译**[窗格](#TextTranslationPane)上添加 ER 标签时，可以将其手动翻译为当前 Finance 实例支持的所有语言。</span><span class="sxs-lookup"><span data-stu-id="904b5-227">When you add an ER label on the **Text translation** [pane](#TextTranslationPane), you can manually translate it into all languages that are supported in the current Finance instance.</span></span> <span data-ttu-id="904b5-228">您可以在 **系统语言** 或 **用户语言** 部分的 **语言** 字段中选择首选语言，并在相应的 **已翻译的文本** 字段中输入适当的文本，然后选择 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="904b5-228">You can select the preferred language in the **Language** field in the **System language** or **User language** section, enter the appropriate text in the corresponding **Translated text** field, and then select **Translate**.</span></span> <span data-ttu-id="904b5-229">对于每种必需的语言和添加的每个标签，必须重复此流程。</span><span class="sxs-lookup"><span data-stu-id="904b5-229">This process must be repeated for every required language and every label that you add.</span></span>

### <a name="automatic-translation"></a><span data-ttu-id="904b5-230">自动翻译</span><span class="sxs-lookup"><span data-stu-id="904b5-230">Automatic translation</span></span>

<span data-ttu-id="904b5-231">ER 组件的配置是在可编辑 ER 组件所在的 ER 配置的草稿版本中完成的。</span><span class="sxs-lookup"><span data-stu-id="904b5-231">Configuration of an ER component is done in the draft version of the ER configuration that the editable ER component resides in.</span></span>

![提供对“草稿”状态下的配置版本的访问的 ER 配置页面](./media/er-multilingual-labels-configurations.png)

<span data-ttu-id="904b5-233">如本主题前面所述，您可以将所需的 ER 标签添加到可编辑 ER 组件中。</span><span class="sxs-lookup"><span data-stu-id="904b5-233">As described earlier in this topic, you can add required ER labels to an editable ER component.</span></span> <span data-ttu-id="904b5-234">这样，您可以用 EN-US 语言指定 ER 标签的文本。</span><span class="sxs-lookup"><span data-stu-id="904b5-234">In this way, you can specify the text of the ER labels in the EN-US language.</span></span> <span data-ttu-id="904b5-235">然后，您可以使用内置的 ER 函数导出 ER 组件的标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-235">You can then export the labels of the ER component by using the built-in ER function.</span></span> <span data-ttu-id="904b5-236">选择包含可编辑的 ER 组件的 ER 配置的草稿版本，然后选择 **交换 \> 导出标签**。</span><span class="sxs-lookup"><span data-stu-id="904b5-236">Select the draft version of an ER configuration that contains the editable ER component, and then select **Exchange \> Export labels**.</span></span>

![允许从选定的配置版本导出 ER 标签的 ER 配置页面](./media/er-multilingual-labels-export.png)

<span data-ttu-id="904b5-238">您可以导出所有标签，也可以导出在导出开始时指定的一种语言的标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-238">You can export either all labels or the labels for a single language that you specify at the beginning of export.</span></span> <span data-ttu-id="904b5-239">标签将导出为包含 XML 文件的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="904b5-239">Labels are exported as a zip file that contains XML files.</span></span> <span data-ttu-id="904b5-240">每个 XML 文件包含一种语言的标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-240">Every XML file contains labels for a single language.</span></span>

![包含 DE-AT 语言的 ER 标签的导出文件的示例](./media/er-multilingual-labels-in-xml.png)

<span data-ttu-id="904b5-242">此格式用于通过外部翻译服务自动翻译标签，如 [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="904b5-242">This format is used for automatic translation of labels by  external translation services such as [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md).</span></span> <span data-ttu-id="904b5-243">收到翻译的标签后，可以将它们重新导入到包含拥有这些标签的 ER 组件的 ER 配置的草稿版本中。</span><span class="sxs-lookup"><span data-stu-id="904b5-243">When you receive the translated labels, you can import them back into the draft version of an ER configuration that contains the ER components that own those labels.</span></span> <span data-ttu-id="904b5-244">选择包含可编辑的 ER 组件的 ER 配置的草稿版本，然后选择 **交换 \> 加载标签**。</span><span class="sxs-lookup"><span data-stu-id="904b5-244">Select the draft version of an ER configuration that contains the editable ER component, and select **Exchange \> Load labels**.</span></span>

![允许将 ER 标签导入到选定的配置版本的 ER 配置页面](./media/er-multilingual-labels-load.png)

<span data-ttu-id="904b5-246">翻译的标签将导入到所选的 ER 配置中。</span><span class="sxs-lookup"><span data-stu-id="904b5-246">Translated labels will be imported into the selected ER configuration.</span></span> <span data-ttu-id="904b5-247">此 ER 配置中存在的翻译的标签将被替换。</span><span class="sxs-lookup"><span data-stu-id="904b5-247">Translated labels that exist in this ER configuration are replaced.</span></span> <span data-ttu-id="904b5-248">如果 ER 配置中缺少任何翻译的标签，将追加。</span><span class="sxs-lookup"><span data-stu-id="904b5-248">If any translated label is missing in the ER configuration, it's appended.</span></span>

## <a name="lifecycle"></a><span data-ttu-id="904b5-249">生命周期</span><span class="sxs-lookup"><span data-stu-id="904b5-249">Lifecycle</span></span>

<span data-ttu-id="904b5-250">可以编辑的 ER 组件的标签以及该组件的其他内容都保存在相应版本的 ER 配置中。</span><span class="sxs-lookup"><span data-stu-id="904b5-250">Labels of an ER component that can be edited are kept, together with other content for the component, in the appropriate version of an ER configuration.</span></span>

<span data-ttu-id="904b5-251">基本 ER 组件的标签可以在您创建以引入修改的 ER 组件的派生版本中引用。</span><span class="sxs-lookup"><span data-stu-id="904b5-251">Labels of a base ER component can be referred to in a derived version of the ER component that you create to introduce your modifications.</span></span>

<span data-ttu-id="904b5-252">ER 版本控制将控制向 ER 组件中的任何属性的标签分配。</span><span class="sxs-lookup"><span data-stu-id="904b5-252">ER versioning controls label assignment to any attribute in an ER component.</span></span> <span data-ttu-id="904b5-253">对标签分配的更改将记录在已创建为所提供 ER 组件的派生版本的可编辑 ER 组件的更改列表（增量）中。</span><span class="sxs-lookup"><span data-stu-id="904b5-253">Changes to the label assignment are recorded in the list of changes (delta) of an editable ER component that has been created as a derived version of the provided ER component.</span></span> <span data-ttu-id="904b5-254">将派生版本重定为新的基本版本时，将验证这些更改。</span><span class="sxs-lookup"><span data-stu-id="904b5-254">These changes will be validated when a derived version is rebased to a new base version.</span></span>

## <a name="functions"></a><span data-ttu-id="904b5-255">功能</span><span class="sxs-lookup"><span data-stu-id="904b5-255">Functions</span></span>

<span data-ttu-id="904b5-256">内置的 [LISTOFFIELDS](er-functions-list-listoffields.md) ER 函数可以访问为某些 ER 组件项目配置的 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-256">The built-in [LISTOFFIELDS](er-functions-list-listoffields.md) ER function can access ER labels that have been configured for some items of ER components.</span></span>

<span data-ttu-id="904b5-257">如本主题前面所述，每个 [模型](#LinkModelEnum)或 [格式](#LinkFormatEnum) ER 枚举的值的 **标签** 和 **描述** 属性，可以链接到可在适当的 ER 组件中访问的 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="904b5-257">As described earlier in this topic, the **Label** and **Description** attributes of every [model](#LinkModelEnum) or [format](#LinkFormatEnum) ER enumeration's value can be linked to an ER label that is accessible in the appropriate ER component.</span></span> <span data-ttu-id="904b5-258">您可以使用 ER 枚举作为参数来配置调用 **LISTOFFIELDS** 函数的 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="904b5-258">You can configure an ER expression where you call the **LISTOFFIELDS** function by using the ER enumeration as an argument.</span></span> <span data-ttu-id="904b5-259">此表达式将返回一个列表，其中包含已定义为此函数的参数的 ER 枚举的每个值的记录。</span><span class="sxs-lookup"><span data-stu-id="904b5-259">This expression returns a list that contains a record for every value of an ER enumeration that has been defined as an argument of this function.</span></span> <span data-ttu-id="904b5-260">每个记录均包含链接到 ER 枚举值的 ER 标签的值：</span><span class="sxs-lookup"><span data-stu-id="904b5-260">Every record contains the value of an ER label that is linked to an ER enumeration value:</span></span>

- <span data-ttu-id="904b5-261">链接到 **标签** 属性的 ER 标签的值存储在返回记录的 **标签** 字段中。</span><span class="sxs-lookup"><span data-stu-id="904b5-261">The value of an ER label that is linked to the **Label** attributes is stored in the **Label** field of the returned record.</span></span>
- <span data-ttu-id="904b5-262">链接到 **描述** 属性的 ER 标签的值存储在返回记录的 **描述** 字段中。</span><span class="sxs-lookup"><span data-stu-id="904b5-262">The value of an ER label that is linked to the **Description** attributes is stored in the **Description** field of the returned record.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="904b5-263">其他资源</span><span class="sxs-lookup"><span data-stu-id="904b5-263">Additional resources</span></span>

- [<span data-ttu-id="904b5-264">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="904b5-264">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="904b5-265">电子报告功能</span><span class="sxs-lookup"><span data-stu-id="904b5-265">Electronic Reporting functions</span></span>](er-formula-language.md#functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
