---
title: 配置查找数据源以使用 ER 应用程序特定的参数
description: 本主题说明如何配置电子报告 (ER) 格式的查找数据源以使用 ER 应用程序特定的参数。
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 131d14f1f1aa329bd71b1f8a4015192736bd8e44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022567"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a><span data-ttu-id="f18b9-103">配置查找数据源以使用 ER 应用程序特定的参数</span><span class="sxs-lookup"><span data-stu-id="f18b9-103">Configure Lookup data sources to use ER application-specific parameters</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f18b9-104">[电子报告 (ER)](general-electronic-reporting.md) 应用程序特定的参数功能使您可以以 ER 格式配置数据筛选，使其基于一组抽象规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-104">The [Electronic reporting (ER)](general-electronic-reporting.md) application-specific parameters feature lets you configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="f18b9-105">可以将这组规则配置为使用以 ER 格式提供的 **查找** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="f18b9-105">This set of rules can be configured to use the data source of the **Lookup** type that is available in an ER format.</span></span> <span data-ttu-id="f18b9-106">然后，您可以使用基于相应 ER 格式的 **查找** 数据源的设置以及当前法人数据自动生成的用户界面 (UI)，指定 ER 组件设计器之外的实际规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-106">You can then specify real rules beyond the ER components designers by using the user interface (UI) that is automatically generated based on the settings of the **Lookup** data source of the corresponding ER format and the current legal entity data.</span></span> <span data-ttu-id="f18b9-107">最终，当执行此 ER 格式时，将通过 ER 格式的 **查找** 数据源访问指定的规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-107">Eventually, the specified rules will be accessed by the ER format's **Lookup** data source when this ER format is executed.</span></span>

> [!NOTE]
> <span data-ttu-id="f18b9-108">使用可编辑 ER 格式的已配置数据源指定哪些应用程序数据用于配置实际规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-108">Use the configured data sources of the editable ER format to specify what application data is used to configure real rules.</span></span>

<span data-ttu-id="f18b9-109">使用 [ER Operations 设计器](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base)将 **查找** 数据源引入到 ER 格式中。</span><span class="sxs-lookup"><span data-stu-id="f18b9-109">Use the [ER Operations designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) to bring a data source of the **Lookup** type in to your ER format.</span></span> <span data-ttu-id="f18b9-110">必须配置数据源以描述抽象规则的外观，包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="f18b9-110">The data source must be configured to describe how your abstract rules look, including the following:</span></span>

   - <span data-ttu-id="f18b9-111">某些数据类型的参数集，提供其值以指定单个规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-111">The parameter set of certain data type whose value is provided to specify a single rule.</span></span>
   - <span data-ttu-id="f18b9-112">当将此规则视为最适合的规则时，单个规则返回的某些数据类型的值类型。</span><span class="sxs-lookup"><span data-stu-id="f18b9-112">The value type of certain data type that is returned by a single rule when this rule is considered the most appropriate among others.</span></span>

<span data-ttu-id="f18b9-113">您可以配置以下类型的 **查找** 数据源，具体取决于任何已配置规则返回的值类型：</span><span class="sxs-lookup"><span data-stu-id="f18b9-113">You can configure the following types of **Lookup** data sources depending on the type of value that is returned by any configured rule:</span></span>

   - <span data-ttu-id="f18b9-114">在必须返回模型枚举值时，使用 **数据模型\查找** 类型。</span><span class="sxs-lookup"><span data-stu-id="f18b9-114">Use the **Data model\Lookup** type when a model enumeration value must be returned.</span></span>
   - <span data-ttu-id="f18b9-115">在必须返回应用程序枚举值或应用程序 [扩展数据类型](../extensibility/extensible-edts.md)值时，使用 **Dynamics 365 Operations\查找** 类型。</span><span class="sxs-lookup"><span data-stu-id="f18b9-115">Use the **Dynamics 365 Operations\Lookup** type when an application enumeration value or an application [extended data type](../extensibility/extensible-edts.md) value must be returned.</span></span>
   - <span data-ttu-id="f18b9-116">在必须返回格式枚举值时，使用 **格式枚举\查找** 类型。</span><span class="sxs-lookup"><span data-stu-id="f18b9-116">Use the **Format enumeration\Lookup** type when a format enumeration value must be returned.</span></span>

<span data-ttu-id="f18b9-117">下图显示了如何以示例 ER 格式配置格式枚举。</span><span class="sxs-lookup"><span data-stu-id="f18b9-117">The following illustration shows how a format enumeration can be configured in the sample ER format.</span></span>

   ![显示格式枚举作为已配置查找数据源的基础](./media/er-lookup-data-sources-img1.gif)

<span data-ttu-id="f18b9-119">下图显示了配置为在生成报告的不同部分中报告不同类型税务的格式组件。</span><span class="sxs-lookup"><span data-stu-id="f18b9-119">The following illustration shows the format components that were configured to report different type of taxes in a different section of a generated report.</span></span>

   ![显示格式部分以分别报告不同类型的税务](./media/er-lookup-data-sources-img2.png)

<span data-ttu-id="f18b9-121">下图显示了 ER Operations 设计器如何允许添加 **格式枚举\查找** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="f18b9-121">The following illustration shows how the ER Operations designer allows the addition of a data source of the **Format enumeration\Lookup** type.</span></span>  <span data-ttu-id="f18b9-122">添加的数据源配置为返回 `List of taxation levels` 格式枚举的值。</span><span class="sxs-lookup"><span data-stu-id="f18b9-122">The added data source is configured as returning a value of the `List of taxation levels` format enumeration.</span></span>

   ![添加格式枚举\查找类型的 ER 数据源](./media/er-lookup-data-sources-img3.gif)

<span data-ttu-id="f18b9-124">下图显示了如何将添加的数据源配置为使用 **模型** 数据源的 **Model.Data.Tax** 记录列表的 **代码** 字段作为必须为每个配置规则指定的参数。</span><span class="sxs-lookup"><span data-stu-id="f18b9-124">The following illustration shows how the added data source is configured to use the **Code** field of the **Model.Data.Tax** record list of the **Model** data source as a parameter that must be specified for every configured rule.</span></span>

![配置格式枚举\查找类型的已添加数据源的参数](./media/er-lookup-data-sources-img4.gif)

<span data-ttu-id="f18b9-126">添加的 `Model.Data.Tax` 数据源配置为通过访问 **TaxTable** 应用程序表的记录为每个配置规则指定税码。</span><span class="sxs-lookup"><span data-stu-id="f18b9-126">The added `Model.Data.Tax` data source is configured to specify a tax code for every configured rule by accessing records of the **TaxTable** application table.</span></span>

   ![查看格式枚举\查找类型的单个公司查找数据源](./media/er-lookup-data-sources-img5.gif)

<span data-ttu-id="f18b9-128">您可以使用与已配置数据源的结构自动对齐的 UI 为选择的 ER 格式设置查找规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-128">You can set up the lookup rules for the selected ER format by using the UI that is automatically aligned with the structure of the configured data source.</span></span> <span data-ttu-id="f18b9-129">当前，此 UI 要求对于每个规则，都指定返回的值作为 `List of taxation levels` 格式枚举值，以及指定税码作为参数。</span><span class="sxs-lookup"><span data-stu-id="f18b9-129">Currently, this UI requires that for each rule, you specify the returned value as the `List of taxation levels` format enumeration value as well as the tax code as a parameter.</span></span>

   ![设置已配置数据源的规则](./media/er-lookup-data-sources-img6.gif)

<span data-ttu-id="f18b9-131">下图显示了如何配置 **计算字段** 类型的 `Model.Data.Summary.LevelByLookup` 数据源以调用提供所需参数的已配置 **查找** 数据源。</span><span class="sxs-lookup"><span data-stu-id="f18b9-131">The following illustration shows how the `Model.Data.Summary.LevelByLookup` data source of the **Calculated field** type can be configured to call the configured **Lookup** data source providing the required parameters.</span></span> <span data-ttu-id="f18b9-132">若要在运行时处理此调用，ER 按定义的顺序浏览已配置规则的列表，以找到满足所提供条件的第一个规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-132">To process this call at runtime, ER goes through the list of configured rules in the defined sequence to locate the first rule that satisfies the provided conditions.</span></span> <span data-ttu-id="f18b9-133">在此示例中，该规则包含与提供的税码匹配的税码。</span><span class="sxs-lookup"><span data-stu-id="f18b9-133">In this example, it's the rule that contains the tax code that matches the provided one.</span></span> <span data-ttu-id="f18b9-134">因此，找到最适合的规则，此数据源返回为找到的规则配置的枚举值。</span><span class="sxs-lookup"><span data-stu-id="f18b9-134">As the result, the most appropriate rule is found and the enumeration value that is configured for the found rule is returned by this data source.</span></span>

> [!NOTE]
> <span data-ttu-id="f18b9-135">如果找不到适用的规则，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="f18b9-135">An exception is thrown when no applicable rule is found.</span></span> <span data-ttu-id="f18b9-136">若要防止这些异常，请在规则列表的末尾配置其他规则，以处理提供非配置值或未提供值的情况。</span><span class="sxs-lookup"><span data-stu-id="f18b9-136">To prevent these exceptions, configure additional rules at the end of the rules list to handle cases when a non-configured value or no value is provided.</span></span> <span data-ttu-id="f18b9-137">相应地使用 **\*非空白\***和 **\*空白\***选项。</span><span class="sxs-lookup"><span data-stu-id="f18b9-137">Use the **\*Not blank**\* and **\*Blank**\* options accordingly.</span></span>  
>
> ![添加数据源以调用已配置的查找数据源](./media/er-lookup-data-sources-img7.png)

<span data-ttu-id="f18b9-139">当您针对可编辑的查找数据源将 **跨公司** 选项设置为 **是** 时，将新的所需 **公司** 参数添加到此数据源的参数集。</span><span class="sxs-lookup"><span data-stu-id="f18b9-139">When you set the **Cross-company** option to **Yes** for the editable lookup data source, you add a new required **Company** parameter to the set of parameters of this data source.</span></span> <span data-ttu-id="f18b9-140">当调用查找数据源时，必须在运行时指定 **公司** 参数的值。</span><span class="sxs-lookup"><span data-stu-id="f18b9-140">The value of the **Company** parameter must be specified at runtime when the lookup data source is called.</span></span> <span data-ttu-id="f18b9-141">当在运行时指定公司代码时，为此公司配置的规则用于查找最适合的规则，并返回相应的值。</span><span class="sxs-lookup"><span data-stu-id="f18b9-141">When the company code is specified at runtime, the rules configured for this company are used to find the most appropriate rule, and the corresponding value is returned.</span></span> <span data-ttu-id="f18b9-142">下图显示了如何执行此操作以及如何更改可编辑数据源的参数集。</span><span class="sxs-lookup"><span data-stu-id="f18b9-142">The following illustration shows how you can do this and how the set of parameters of the editable data source is changed.</span></span>

   ![查看格式枚举\查找类型的跨公司查找数据源](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> <span data-ttu-id="f18b9-144">分别选择每个公司以为可编辑 ER 格式的此查找数据源配置规则集。</span><span class="sxs-lookup"><span data-stu-id="f18b9-144">Select every company seperately to configure the set of rules for this lookup data source of the editable ER format.</span></span> <span data-ttu-id="f18b9-145">当使用未完成其查找设置的公司代码调用跨公司查找时，将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="f18b9-145">An exception is thrown at runtime when the cross-company lookup is called with the code of the company for which the lookup setting was not completed.</span></span>
>
> <span data-ttu-id="f18b9-146">确保向使用跨公司 **查找** 数据源运行 ER 格式的用户授予权限，以访问此数据源范围内的每个公司的数据。</span><span class="sxs-lookup"><span data-stu-id="f18b9-146">Make sure that you grant permissions for a user who runs the ER format with the cross-company **Lookup** data source to access the data of every company that is in scope of this data source.</span></span> <span data-ttu-id="f18b9-147">否则，将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="f18b9-147">Otherwise, an exception is thrown at runtime.</span></span>

<span data-ttu-id="f18b9-148">从版本 10.0.19 开始，将提供 **查找** 数据源的扩展功能。</span><span class="sxs-lookup"><span data-stu-id="f18b9-148">Starting in version 10.0.19, the extended capabilities of the **Lookup** data sources are available.</span></span> <span data-ttu-id="f18b9-149">当针对可编辑查找数据源将 **扩展** 选项设置为 **是** 时，已配置查找数据源将转换为提供其他功能以分析配置规则集的结构数据源。</span><span class="sxs-lookup"><span data-stu-id="f18b9-149">When you set the **Extended** option to **Yes** for the editable lookup data source, the configured lookup data source is transformed to the structured data source that offers the additional capabilities to analyze the configured set of rules.</span></span> <span data-ttu-id="f18b9-150">下图显示了此转换。</span><span class="sxs-lookup"><span data-stu-id="f18b9-150">The following illustration shows this transformation.</span></span>

   ![查看格式枚举\查找类型的结构查找数据源](./media/er-lookup-data-sources-img9.gif)

- <span data-ttu-id="f18b9-152">**查找** 子项设计为一个函数，用于基于提供的参数集从可配置规则集中查找最适合的规则。</span><span class="sxs-lookup"><span data-stu-id="f18b9-152">The **Lookup** sub-item is designed as a function to find the most appropriate rule from the set of configurable rules based on the provided set of parameters.</span></span>
- <span data-ttu-id="f18b9-153">**IsLookupResultSet** 子项设计为一个函数，用于接受基本枚举数据源的提供值，并在规则集包含至少一个将提供的枚举值配置为返回值的规则时，返回 *布尔* 值 **True**。</span><span class="sxs-lookup"><span data-stu-id="f18b9-153">The **IsLookupResultSet** sub-item is designed as a function to accept the provided value of the base enumeration data source and return the *Boolean* value of **True** when the set of rules contain at least one rule for which the provided enumeration value was configured as a returned value.</span></span> <span data-ttu-id="f18b9-154">当没有规则配置为返回提供的枚举值时，此函数返回 *布尔* 值 **False**。</span><span class="sxs-lookup"><span data-stu-id="f18b9-154">This function returns the *Boolean* value of **False** when there are no rules configured to return the provided enumeration value.</span></span>
- <span data-ttu-id="f18b9-155">**设置** 子项设计为一个函数，用于返回已配置规则集作为记录列表的记录。</span><span class="sxs-lookup"><span data-stu-id="f18b9-155">The **Setting** sub-item is designed as a function that returns the set of configured rules as records of a record list.</span></span> <span data-ttu-id="f18b9-156">已配置规则的返回值和参数集在每个返回的记录中显示为相关数据类型的字段：</span><span class="sxs-lookup"><span data-stu-id="f18b9-156">The returned values and the set of parameters of the configured rules are presented in every returned record as fields of the relevant data types:</span></span>

    - <span data-ttu-id="f18b9-157">返回值显示为 **查找结果** 字段。</span><span class="sxs-lookup"><span data-stu-id="f18b9-157">The returned value is presented as the **Lookup result** field.</span></span>
    - <span data-ttu-id="f18b9-158">配置的参数显示为具有参数名称的字段（在此示例中为 **代码** 字段）。</span><span class="sxs-lookup"><span data-stu-id="f18b9-158">The configured parameters are presented as fields having names of parameters (**Code** field in this example).</span></span>

<span data-ttu-id="f18b9-159">有关如何配置 **查找** 数据源的详细信息，请参阅[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)。</span><span class="sxs-lookup"><span data-stu-id="f18b9-159">For more information about to how configure the **Lookup** data source, see [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md).</span></span> <span data-ttu-id="f18b9-160">若要了解如何设置查找规则，请参阅[为每个法人设置 ER 格式的参数](er-app-specific-parameters-set-up.md)。</span><span class="sxs-lookup"><span data-stu-id="f18b9-160">To learn how to set the Lookup rules, see [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f18b9-161">其他资源</span><span class="sxs-lookup"><span data-stu-id="f18b9-161">Additional resources</span></span>

[<span data-ttu-id="f18b9-162">配置电子报告格式以使用每个法人指定的参数</span><span class="sxs-lookup"><span data-stu-id="f18b9-162">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)

[<span data-ttu-id="f18b9-163">为每个法人设置电子报告格式的参数</span><span class="sxs-lookup"><span data-stu-id="f18b9-163">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
