---
title: 电子申报公式支持的复合数据类型
description: 本主题提供有关电子申报 (ER) 公式支持的复合数据类型的信息。
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ed9e62751b6be9fad6de3bf262d37d7977d192
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224078"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a><span data-ttu-id="20a2e-103">电子申报公式支持的复合数据类型</span><span class="sxs-lookup"><span data-stu-id="20a2e-103">Supported composite data types for Electronic reporting formulas</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20a2e-104">本主题提供有关[电子申报 (ER)](general-electronic-reporting.md) 表达式支持的复合数据类型的信息。</span><span class="sxs-lookup"><span data-stu-id="20a2e-104">This topic provides information about the composite data types that are supported in [Electronic reporting (ER)](general-electronic-reporting.md) expressions.</span></span> <span data-ttu-id="20a2e-105">复合数据类型包括[类](#class)、[容器](#container)、[记录](#record)、[记录列表](#record-list)和[对象](#object)。</span><span class="sxs-lookup"><span data-stu-id="20a2e-105">The composite data types are [class](#class), [container](#container), [record](#record), [record list](#record-list), and [object](#object).</span></span>

## <a name="class"></a><a name="class"></a><span data-ttu-id="20a2e-106">分类</span><span class="sxs-lookup"><span data-stu-id="20a2e-106">Class</span></span>

<span data-ttu-id="20a2e-107">*类* 数据类型是指公共应用程序类。</span><span class="sxs-lookup"><span data-stu-id="20a2e-107">The *class* data type refers to a public application class.</span></span> <span data-ttu-id="20a2e-108">在 ER 中，它表示为 [*记录*](#record)，其中包含引用类的每个公共方法的单独字段。</span><span class="sxs-lookup"><span data-stu-id="20a2e-108">In ER, it's represented as a [*record*](#record) that contains a separate field for every public method of the referenced class.</span></span> <span data-ttu-id="20a2e-109">当参数化方法的调用时，还必须在配置为调用该方法的 ER 表达式中指定适当类型的所需参数。</span><span class="sxs-lookup"><span data-stu-id="20a2e-109">When the call of the method is parameterized, you must also specify the required arguments of the appropriate types in an ER expression that is configured to call the method.</span></span>

<span data-ttu-id="20a2e-110">在 ER [映射](general-electronic-reporting.md#data-model-and-model-mapping-components)和 [格式](general-electronic-reporting.md#FormatComponentOutbound)组件中，您可以添加表示为数据源并返回 *类* 类型的值的 **类** 数据源。</span><span class="sxs-lookup"><span data-stu-id="20a2e-110">In ER [mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) and [format](general-electronic-reporting.md#FormatComponentOutbound) components, you can add the **Class** data source that is presented as a data source and that returns a value of the *class* type.</span></span> <span data-ttu-id="20a2e-111">此数据源公开可在运行时调用的类的公共方法。</span><span class="sxs-lookup"><span data-stu-id="20a2e-111">This data source exposes public methods of the class that can be called at runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="20a2e-112">只能从 ER 表达式调用返回值的方法。</span><span class="sxs-lookup"><span data-stu-id="20a2e-112">Only methods that return a value can be called from ER expressions.</span></span>
>
> <span data-ttu-id="20a2e-113">只能从 ER 表达式调用参数范围为 0 到 8 的方法。</span><span class="sxs-lookup"><span data-stu-id="20a2e-113">Only methods that have a range of zero to eight arguments can be called from ER expressions.</span></span>

<span data-ttu-id="20a2e-114">*类* 的默认值为 **null**。</span><span class="sxs-lookup"><span data-stu-id="20a2e-114">The default value of a *class* is **null**.</span></span>

<span data-ttu-id="20a2e-115">下图显示了如何添加 **类** 类型的 **系统信息 (xInfo)** 数据源以创建 **(xInfo)** 应用程序类的实例并调用其 **productName()** 方法，从而接收当前应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="20a2e-115">The following illustration shows how the **System information(xInfo)** data source of the **Class** type is added to make the instance of the **xInfo** application class and call its **productName()** method to receive the name of the current application.</span></span> <span data-ttu-id="20a2e-116">通过执行已为 ER 数据模型的 **软件名称 (SoftwareName)** 字段配置的 `xInfo.productName` 绑定，在运行时获取当前应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="20a2e-116">The name of the current application is fetched at runtime by execution of the `xInfo.productName` binding that was configured for the **Software name(SoftwareName)** field of the ER data model.</span></span> <span data-ttu-id="20a2e-117">此绑定调用在当前模型映射中表示为 **系统信息 (xInfo)** 数据源的 **xInfo** 应用程序类的 `productName()` 方法。</span><span class="sxs-lookup"><span data-stu-id="20a2e-117">This binding calls the `productName()` method of the **xInfo** application class that is represented in the current model mapping as the **System information(xInfo)** data source.</span></span>

<span data-ttu-id="20a2e-118">[![在 ER 模型映射设计器中配置类数据源](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)</span><span class="sxs-lookup"><span data-stu-id="20a2e-118">[![Configuring a Class data source in the ER model mapping designer](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)</span></span>

<span data-ttu-id="20a2e-119">下图显示了如何配置 ER 格式以将提供的应用程序名称放入生成的单据中。</span><span class="sxs-lookup"><span data-stu-id="20a2e-119">The following illustration shows how the ER format is configured to put the provided application name in generated documents.</span></span> <span data-ttu-id="20a2e-120">使用的数据模型的 **软件名称 (SoftwareName)** 字段已绑定到在 ER 格式的 **softwareUsed** XML 元素下嵌套的 **字符串** 组件。</span><span class="sxs-lookup"><span data-stu-id="20a2e-120">The **Software name(SoftwareName)** field of the used data model was bound to the **String** component that is nested under the **softwareUsed** XML element of the ER format.</span></span> <span data-ttu-id="20a2e-121">因此，当前应用程序的名称在运行时放置到生成的 XML 格式单据的 **softwareUsed** XML 元素中。</span><span class="sxs-lookup"><span data-stu-id="20a2e-121">So, the name of the current application is placed at runtime to the **softwareUsed** XML element of a generated document in XML format.</span></span>

<span data-ttu-id="20a2e-122">[![在 ER 格式设计器中配置电子出库单据的结构](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)</span><span class="sxs-lookup"><span data-stu-id="20a2e-122">[![Configuring the structure of an electronic outbound document in the ER format designer](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)</span></span>

## <a name="container"></a><a name="container"></a><span data-ttu-id="20a2e-123">容器</span><span class="sxs-lookup"><span data-stu-id="20a2e-123">Container</span></span>

<span data-ttu-id="20a2e-124">*容器* 数据类型保存二进制内容。</span><span class="sxs-lookup"><span data-stu-id="20a2e-124">The *container* data type holds binary content.</span></span> <span data-ttu-id="20a2e-125">*容器* 值可用于将特定信息从存储传递到生成的单据。</span><span class="sxs-lookup"><span data-stu-id="20a2e-125">A *container* value can be used to pass specific information from storage to a generated document.</span></span> <span data-ttu-id="20a2e-126">在 ER 框架中，此数据类型经常用于将媒体内容（例如公司徽标）放入生成的单据中。</span><span class="sxs-lookup"><span data-stu-id="20a2e-126">In the ER framework, this data type is frequently used to put media content such as a company logo in generated documents.</span></span>

> [!NOTE]
> <span data-ttu-id="20a2e-127">尽管每个媒体项都可以表示为 *容器* 值，但不是每个 *容器* 值都表示媒体项。</span><span class="sxs-lookup"><span data-stu-id="20a2e-127">Although every media item can be represented as a *container* value, not every *container* value represents a media item.</span></span> <span data-ttu-id="20a2e-128">因此，如果您配置 ER 格式以使其使用 *容器* 将图像放入生成的单据中，但引用的 *容器* 不返回媒体内容，可能会引发类似于以下示例的异常：“执行代码时出错：二进制（对象），使用无效参数调用的方法 constructFromContainer。”</span><span class="sxs-lookup"><span data-stu-id="20a2e-128">Therefore, if you configure an ER format so that it uses a *container* to put an image in generated documents, but the referenced *container* doesn't return media content, an exception that resembles the following example might be thrown: "Error executing code: Binary (object), method constructFromContainer called with invalid parameters."</span></span>

<span data-ttu-id="20a2e-129">*容器* 的默认值为 **null**。</span><span class="sxs-lookup"><span data-stu-id="20a2e-129">The default value of a *container* is **null**.</span></span>

<span data-ttu-id="20a2e-130">下图显示了如何将 *容器* 类型的 **位图（图像）** 字段绑定到 **销售发票** 模型映射中 **容器** 类型的数据模型 **徽标** 字段。</span><span class="sxs-lookup"><span data-stu-id="20a2e-130">The following illustration shows how the **Bitmap(Image)** field of the *Container* type is bound to the data model **Logo** field of the **Container** type in the **Sales invoice** model mapping.</span></span> <span data-ttu-id="20a2e-131">此绑定使公司徽标可用于专为 **销售发票** 根定义设计并在运行时使用此模型映射的任何 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="20a2e-131">This binding makes the company logo available to any ER format that is designed for the **SalesInvoice** root definition and that uses this model mapping at runtime.</span></span>

<span data-ttu-id="20a2e-132">[![在 ER 模型映射设计器中绑定容器类型的字段](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)</span><span class="sxs-lookup"><span data-stu-id="20a2e-132">[![Binding a field of the Container type in the ER model mapping designer](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)</span></span>

## <a name="record"></a><a name="record"></a><span data-ttu-id="20a2e-133">录制</span><span class="sxs-lookup"><span data-stu-id="20a2e-133">Record</span></span>

<span data-ttu-id="20a2e-134">*记录* 是一系列命名字段，每个字段都与[原始](er-formula-supported-data-types-primitive.md)数据类型或复合数据类型的值关联。</span><span class="sxs-lookup"><span data-stu-id="20a2e-134">A *record* is a collection of named fields, each of which is associated with a value of either a [primitive](er-formula-supported-data-types-primitive.md) data type or a composite data type.</span></span> <span data-ttu-id="20a2e-135">通常，*记录* 用于表示记录列表的单个记录。</span><span class="sxs-lookup"><span data-stu-id="20a2e-135">Usually, a *record* is used to represent a single record of a record list.</span></span> <span data-ttu-id="20a2e-136">在这种情况下，每个项目都代表单独的字段、方法和关系。</span><span class="sxs-lookup"><span data-stu-id="20a2e-136">In this case, every item represents individual fields, methods, and relations.</span></span>

<span data-ttu-id="20a2e-137">*记录* 的默认值为 **空**。</span><span class="sxs-lookup"><span data-stu-id="20a2e-137">The default value of a *record* is **empty**.</span></span>

> [!NOTE]
> <span data-ttu-id="20a2e-138">当获取空 *记录* 的字段值时，将返回适当数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="20a2e-138">When you get the value of a field of an empty *record*, the default value of the appropriate data type is returned.</span></span>

<span data-ttu-id="20a2e-139">可以使用以下函数获取 *记录*：</span><span class="sxs-lookup"><span data-stu-id="20a2e-139">A *record* can be obtained by using the following functions:</span></span>

- [<span data-ttu-id="20a2e-140">FIRST</span><span class="sxs-lookup"><span data-stu-id="20a2e-140">FIRST</span></span>](er-functions-list-first.md)
- [<span data-ttu-id="20a2e-141">FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="20a2e-141">FIRSTORNULL</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="20a2e-142">EMPTYRECORD</span><span class="sxs-lookup"><span data-stu-id="20a2e-142">EMPTYRECORD</span></span>](er-functions-record-emptyrecord.md)
- [<span data-ttu-id="20a2e-143">NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="20a2e-143">NULLCONTAINER</span></span>](er-functions-record-nullcontainer.md)

<span data-ttu-id="20a2e-144">有关转换 *记录* 值的详细信息，请参阅[列表类别中的 ER 函数列表](er-functions-category-list.md)。</span><span class="sxs-lookup"><span data-stu-id="20a2e-144">For more information about the transformation of *record* values, see [List of ER functions in the list category](er-functions-category-list.md).</span></span>

## <a name="record-list"></a><a name="record-list"></a><span data-ttu-id="20a2e-145">记录列表</span><span class="sxs-lookup"><span data-stu-id="20a2e-145">Record list</span></span>

<span data-ttu-id="20a2e-146">*记录列表* 是 *记录* 类型的项目列表。</span><span class="sxs-lookup"><span data-stu-id="20a2e-146">A *record list* is a list of items of the *record* type.</span></span> <span data-ttu-id="20a2e-147">通常，*记录列表* 用于表示已从数据库表中提取的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="20a2e-147">Usually, a *record list* is used to represent the list of records that has been fetched from a database table.</span></span>

<span data-ttu-id="20a2e-148">默认情况下，*记录列表* 的记录按顺序访问。</span><span class="sxs-lookup"><span data-stu-id="20a2e-148">By default, records of a *record list* are accessed sequentially.</span></span> <span data-ttu-id="20a2e-149">若要访问特定记录，您可以使用 [INDEX](er-functions-list-index.md) 函数并指定 *整数* 索引。</span><span class="sxs-lookup"><span data-stu-id="20a2e-149">To access a specific record, you can use the [INDEX](er-functions-list-index.md) function and specify the *integer* index.</span></span>

<span data-ttu-id="20a2e-150">*记录列表* 的默认值为 **空**。</span><span class="sxs-lookup"><span data-stu-id="20a2e-150">The default value of a *record list* is **empty**.</span></span> <span data-ttu-id="20a2e-151">您可以使用 [ISEMPTY](/er-functions-list-isempty.md) 函数评估 *记录列表* 是否为空。</span><span class="sxs-lookup"><span data-stu-id="20a2e-151">You can use the [ISEMPTY](/er-functions-list-isempty.md) function to evaluate whether a *record list* is empty.</span></span>

> [!NOTE]
> <span data-ttu-id="20a2e-152">如果 *记录列表* 为空，在每次尝试在该列表中获取 *记录* 的字段值时都将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="20a2e-152">If a *record list* is empty, any attempt to get a field value for a *record* in it causes an exception to be thrown at runtime.</span></span> <span data-ttu-id="20a2e-153">若要了解如何帮助防止此类型的运行时异常，请参阅[空列表用例的注意事项](er-components-inspections.md#i9)。</span><span class="sxs-lookup"><span data-stu-id="20a2e-153">To learn how you can help prevent runtime exceptions of this type, see [Consideration of empty list cases](er-components-inspections.md#i9).</span></span>

<span data-ttu-id="20a2e-154">可以使用以下函数启动 *记录列表*：</span><span class="sxs-lookup"><span data-stu-id="20a2e-154">A *record list* can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="20a2e-155">ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="20a2e-155">ALLITEMS</span></span>](er-functions-list-allitems.md)
- [<span data-ttu-id="20a2e-156">ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="20a2e-156">ALLITEMSQUERY</span></span>](er-functions-list-allitemsquery.md)
- [<span data-ttu-id="20a2e-157">EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="20a2e-157">EMPTYLIST</span></span>](er-functions-list-emptylist.md)
- [<span data-ttu-id="20a2e-158">LIST</span><span class="sxs-lookup"><span data-stu-id="20a2e-158">LIST</span></span>](er-functions-list-list.md)
- [<span data-ttu-id="20a2e-159">LISTDISTINCT</span><span class="sxs-lookup"><span data-stu-id="20a2e-159">LISTDISTINCT</span></span>](er-functions-list-listdistinct.md)

<span data-ttu-id="20a2e-160">有关转换 *记录列表* 值的详细信息，请参阅[列表类别中的 ER 函数列表](er-functions-category-list.md)。</span><span class="sxs-lookup"><span data-stu-id="20a2e-160">For more information about the transformation of *record list* values, see [List of ER functions in the list category](er-functions-category-list.md).</span></span> <span data-ttu-id="20a2e-161">若要了解如何引入 *记录列表* 项目，使用应用程序数据填充它们，然后使用数据生成业务单据，请参阅[设计新 ER 解决方案以打印自定义报表](er-quick-start1-new-solution.md)。</span><span class="sxs-lookup"><span data-stu-id="20a2e-161">To learn how to introduce *record list* items, fill them with application data, and then use the data to generate business documents, see [Design a new ER solution to print a custom report](er-quick-start1-new-solution.md).</span></span>

## <a name="object"></a><a name="object"></a><span data-ttu-id="20a2e-162">对象</span><span class="sxs-lookup"><span data-stu-id="20a2e-162">Object</span></span>

<span data-ttu-id="20a2e-163">*对象* 是指 *类* 的有状态实例。</span><span class="sxs-lookup"><span data-stu-id="20a2e-163">An *object* refers to a stateful instance of a *class*.</span></span> <span data-ttu-id="20a2e-164">通常，*对象* 在源代码中启动。</span><span class="sxs-lookup"><span data-stu-id="20a2e-164">Usually, an *object* is initiated in source code.</span></span> <span data-ttu-id="20a2e-165">然后，它将传递到 ER 模型映射，并提供执行上下文的详细信息。</span><span class="sxs-lookup"><span data-stu-id="20a2e-165">It's then passed to an ER model mapping and provides details of the execution context.</span></span>

<span data-ttu-id="20a2e-166">*对象* 的默认值为 **null**。</span><span class="sxs-lookup"><span data-stu-id="20a2e-166">The default value of an *object* is **null**.</span></span>

<span data-ttu-id="20a2e-167">下图显示如何添加 *对象* 类型的 **ReportDataContract** 数据源，以将生成的发票从源代码传递到 **项目发票** 模型映射。</span><span class="sxs-lookup"><span data-stu-id="20a2e-167">The following illustration shows how the **ReportDataContract** data source of the *Object* type is added to pass information about a generated invoice from source code to the **Project invoice** model mapping.</span></span> <span data-ttu-id="20a2e-168">例如，发票实例文本作为执行上下文的一部分传递。</span><span class="sxs-lookup"><span data-stu-id="20a2e-168">For example, the invoice instance text is passed as part of the execution context.</span></span> <span data-ttu-id="20a2e-169">通过执行为 ER 数据模型的 **注释** 字段配置的 `ReportDataContract.parmInvoiceInstanceText` 绑定，在运行时从源代码中获取此文本。</span><span class="sxs-lookup"><span data-stu-id="20a2e-169">This text is taken from source code at runtime by execution of the `ReportDataContract.parmInvoiceInstanceText` binding that was configured for the **Note** field of the ER data model.</span></span> <span data-ttu-id="20a2e-170">此绑定调用在当前模型映射中表示为 **ReportDataContract** 数据源的 **PSAProjInvoiceContract** 应用程序类的 `parmInvoiceInstanceText()` 方法。</span><span class="sxs-lookup"><span data-stu-id="20a2e-170">This binding calls the `parmInvoiceInstanceText()` method of the **PSAProjInvoiceContract** application class that is represented in the current model mapping as the **ReportDataContract** data source.</span></span>

<span data-ttu-id="20a2e-171">[![在 ER 模型映射设计器中配置对象数据源](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)</span><span class="sxs-lookup"><span data-stu-id="20a2e-171">[![Configuring an Object data source in the ER model mapping designer](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)</span></span>

<span data-ttu-id="20a2e-172">若要了解如何将执行上下文的详细信息从源代码传递到运行 ER 解决方案，请参阅[开发应用程序伪像以调用设计的报表](er-quick-start1-new-solution.md#DevelopCustomCode)。</span><span class="sxs-lookup"><span data-stu-id="20a2e-172">To learn how to pass details of the execution context from source code to the running ER solution, see [Develop application artefacts to call the designed report](er-quick-start1-new-solution.md#DevelopCustomCode).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20a2e-173">其他资源</span><span class="sxs-lookup"><span data-stu-id="20a2e-173">Additional resources</span></span>

- [<span data-ttu-id="20a2e-174">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="20a2e-174">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="20a2e-175">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="20a2e-175">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="20a2e-176">支持的原始数据类型</span><span class="sxs-lookup"><span data-stu-id="20a2e-176">Supported primitive data types</span></span>](er-formula-supported-data-types-primitive.md)
