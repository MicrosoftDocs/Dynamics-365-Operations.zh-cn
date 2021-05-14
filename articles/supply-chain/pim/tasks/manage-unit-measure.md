---
title: 管理度量单位
description: 本主题介绍如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921333"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="1d210-103">管理度量单位</span><span class="sxs-lookup"><span data-stu-id="1d210-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d210-104">本主题介绍如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。</span><span class="sxs-lookup"><span data-stu-id="1d210-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="1d210-105">打开单位页面</span><span class="sxs-lookup"><span data-stu-id="1d210-105">Open the Units page</span></span>

<span data-ttu-id="1d210-106">要创建并使用系统中提供的度量单位，请转到 **组织管理 \> 设置 \> 单位 \> 单位**。</span><span class="sxs-lookup"><span data-stu-id="1d210-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="1d210-107">本主题的其余几节介绍您可以在 **单位** 页执行的操作。</span><span class="sxs-lookup"><span data-stu-id="1d210-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="1d210-108">创建标准单位和转换</span><span class="sxs-lookup"><span data-stu-id="1d210-108">Create standard units and conversions</span></span>

<span data-ttu-id="1d210-109">如果您的系统尚未包括公制和/或美国惯用系统 (USCS) 的最常用度量单位，单位设置向导可以帮助您快速开始使用基本的单位定义和转换。</span><span class="sxs-lookup"><span data-stu-id="1d210-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="1d210-110">要完成此向导，在操作窗格上选择 **单位创建向导**，然后按照屏幕上的说明操作。</span><span class="sxs-lookup"><span data-stu-id="1d210-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="1d210-111">创建或编辑度量单位</span><span class="sxs-lookup"><span data-stu-id="1d210-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="1d210-112">要创建或编辑度量单位，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1d210-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="1d210-113">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="1d210-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="1d210-114">要编辑现有单位，在列表窗格中选择它。</span><span class="sxs-lookup"><span data-stu-id="1d210-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="1d210-115">要创建新单位，在操作窗格上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1d210-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="1d210-116">在记录的标头上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="1d210-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="1d210-117">**单位** – 输入用于以系统语言引用单位的 ID 或符号。</span><span class="sxs-lookup"><span data-stu-id="1d210-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="1d210-118">此 ID 或符号通常是单位的常用缩写，如每个是 *ea*，厘米是 *cm*。</span><span class="sxs-lookup"><span data-stu-id="1d210-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="1d210-119">**描述** – 为单位输入系统语言的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="1d210-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="1d210-120">此名称通常是单位的完整名称，如 *每个* 或者 *厘米*。</span><span class="sxs-lookup"><span data-stu-id="1d210-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="1d210-121">在 **常规** 快速选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="1d210-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="1d210-122">**单位类** – 选择单位度量的属性（如长度、面积、质量或数量）。</span><span class="sxs-lookup"><span data-stu-id="1d210-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="1d210-123">**单位系统** – 选择单位所属的度量系统（*公制单位* 或 *美国惯用单位*）。</span><span class="sxs-lookup"><span data-stu-id="1d210-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="1d210-124">**基础单位** – 将此选项设置为 *是* 可以将当前单位用作其单位类的基础单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="1d210-125">在这种情况下，您只需指定单位类中基础单位和每个其他单位之间的换算系数。</span><span class="sxs-lookup"><span data-stu-id="1d210-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="1d210-126">然后，系统可以在该单位类中的所有单位之间进行转换。</span><span class="sxs-lookup"><span data-stu-id="1d210-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="1d210-127">因此，设置转换更加容易。</span><span class="sxs-lookup"><span data-stu-id="1d210-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="1d210-128">例如，如果加仑是 *体积* 单位类的基础单位，您只需设置从夸脱到加仑以及从品脱到加仑的换算系数。</span><span class="sxs-lookup"><span data-stu-id="1d210-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="1d210-129">然后，系统还可以从夸脱转换为品脱。</span><span class="sxs-lookup"><span data-stu-id="1d210-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="1d210-130">每个单位类只能有一个基础单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="1d210-131">**系统单位** – 将此选项设置为 *是* 可以将当前单位用作其单位类中所有未指定度量的假定单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="1d210-132">例如，如果用于输入数量的字段不允许指定单位（或如果用户未选择单位），系统将使用设置为 *数量* 单位类的系统单位的单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="1d210-133">每个单位类只能有一个系统单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="1d210-134">**小数精度** – 指定为当前单位指定或转换为它应该舍入的值的小数位数。</span><span class="sxs-lookup"><span data-stu-id="1d210-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="1d210-135">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1d210-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="1d210-136">定义单位转换</span><span class="sxs-lookup"><span data-stu-id="1d210-136">Define unit translations</span></span>

<span data-ttu-id="1d210-137">要为 ID 或符号以及度量单位的描述定义翻译，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1d210-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="1d210-138">创建或选择要为其创建翻译的单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="1d210-139">在操作窗格上，选择 **单位文本**。</span><span class="sxs-lookup"><span data-stu-id="1d210-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="1d210-140">**单位文本** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="1d210-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="1d210-141">您将使用此页面为所选单位的 ID 或符号定义翻译。</span><span class="sxs-lookup"><span data-stu-id="1d210-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="1d210-142">然后可以将这些翻译用于客户特定语言或供应商特定语言的外部文档。</span><span class="sxs-lookup"><span data-stu-id="1d210-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="1d210-143">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1d210-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1d210-144">在 **语言** 字段中，选择要将单位 ID 或符号翻译成的语言。</span><span class="sxs-lookup"><span data-stu-id="1d210-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="1d210-145">在 **文本** 字段中，输入所选语言的单位 ID 或符号的翻译。</span><span class="sxs-lookup"><span data-stu-id="1d210-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="1d210-146">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1d210-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1d210-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1d210-147">Close the page.</span></span>
1. <span data-ttu-id="1d210-148">在 **操作窗格** 上，选择 **翻译的单位描述**。</span><span class="sxs-lookup"><span data-stu-id="1d210-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="1d210-149">**翻译的单位描述** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="1d210-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="1d210-150">您将使用此页面为所选单位定义语言特定描述。</span><span class="sxs-lookup"><span data-stu-id="1d210-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="1d210-151">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1d210-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1d210-152">在 **语言** 字段中，选择要将单位描述翻译成的语言。</span><span class="sxs-lookup"><span data-stu-id="1d210-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="1d210-153">在 **描述** 字段中，输入所选语言的单位描述的翻译。</span><span class="sxs-lookup"><span data-stu-id="1d210-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="1d210-154">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1d210-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1d210-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1d210-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="1d210-156">定义单位换算规则</span><span class="sxs-lookup"><span data-stu-id="1d210-156">Define unit conversion rules</span></span>

<span data-ttu-id="1d210-157">要定义度量单位之间的转换规则，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1d210-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="1d210-158">创建或选择要为其定义转换规则的单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="1d210-159">在操作窗格上，选择 **单位转换**。</span><span class="sxs-lookup"><span data-stu-id="1d210-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="1d210-160">**单位转换** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="1d210-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="1d210-161">您将使用此页面定义将单位类中的所选单位与其他单位进行相互转换的规则。</span><span class="sxs-lookup"><span data-stu-id="1d210-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="1d210-162">选择以下选项卡之一，具体取决于您要设置的转换类型：</span><span class="sxs-lookup"><span data-stu-id="1d210-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="1d210-163">**标准转换** – 为所有产品设置标准转换规则。</span><span class="sxs-lookup"><span data-stu-id="1d210-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="1d210-164">**类内转换** – 为同一单位类中的单位设置产品特定转换规则。</span><span class="sxs-lookup"><span data-stu-id="1d210-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="1d210-165">**类间转换** – 为不同单位类中的单位设置产品特定转换规则。</span><span class="sxs-lookup"><span data-stu-id="1d210-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="1d210-166">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="1d210-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="1d210-167">要创建新转换，在工具栏上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1d210-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="1d210-168">要编辑现有转换，在网格中选择转换，然后在工具栏上选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="1d210-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="1d210-169">在出现的下拉对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="1d210-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="1d210-170">**产品** – 选择转换将应用的特定产品。</span><span class="sxs-lookup"><span data-stu-id="1d210-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="1d210-171">此字段仅可用于类内和类间转换。</span><span class="sxs-lookup"><span data-stu-id="1d210-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="1d210-172">**公式布局** – 将此字段设置为 *简单* 将指定具有单个系数的简单转换。</span><span class="sxs-lookup"><span data-stu-id="1d210-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="1d210-173">将其设置为 *高级* 将设置更复杂的方程式。</span><span class="sxs-lookup"><span data-stu-id="1d210-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="1d210-174">高级方程式的格式因单位类而异。</span><span class="sxs-lookup"><span data-stu-id="1d210-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="1d210-175">**源单位** – 此字段显示所选单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="1d210-176">通常，您不应更改此值。</span><span class="sxs-lookup"><span data-stu-id="1d210-176">Usually, you should not change the value.</span></span> <span data-ttu-id="1d210-177">（如果您确实更改了此值，则必须在保存后打开所选单位的 **单位转换** 页，查看新转换。）</span><span class="sxs-lookup"><span data-stu-id="1d210-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="1d210-178">**目标单位** – 选择要转换的单位。</span><span class="sxs-lookup"><span data-stu-id="1d210-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="1d210-179">**舍入** – 根据所选单位的 **小数精度** 值选择应舍入的小数（*最近*、*向上* 或 *向下*）。</span><span class="sxs-lookup"><span data-stu-id="1d210-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="1d210-180">**转换公式** – 使用下拉对话框顶部的其余字段指定两个单位之间的转换公式。</span><span class="sxs-lookup"><span data-stu-id="1d210-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="1d210-181">可用字段会有所不同，具体取决于您选择的单位类和公式布局。</span><span class="sxs-lookup"><span data-stu-id="1d210-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="1d210-182">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1d210-182">Select **OK**.</span></span>
1. <span data-ttu-id="1d210-183">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1d210-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="1d210-184">您还可以针对每个产品变型设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="1d210-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="1d210-185">有关详细信息，请参阅[按照产品变型的度量单位转换](../uom-conversion-per-product-variant.md)。</span><span class="sxs-lookup"><span data-stu-id="1d210-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
