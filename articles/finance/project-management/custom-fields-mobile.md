---
title: 为 iOS 和 Android 上的 Microsoft Dynamics 365 Project Timesheet 移动应用实施自定义字段
description: 本主题提供有关使用扩展实施自定义字段的常见模式。
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174767"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="da75e-103">为 iOS 和 Android 上的 Microsoft Dynamics 365 Project Timesheet 移动应用实施自定义字段</span><span class="sxs-lookup"><span data-stu-id="da75e-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da75e-104">本主题提供有关使用扩展实施自定义字段的常见模式。</span><span class="sxs-lookup"><span data-stu-id="da75e-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="da75e-105">包括以下主题：</span><span class="sxs-lookup"><span data-stu-id="da75e-105">The following topics are covered:</span></span>

- <span data-ttu-id="da75e-106">自定义字段框架支持的各种数据类型</span><span class="sxs-lookup"><span data-stu-id="da75e-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="da75e-107">如何在工时表条目中显示只读或可编辑字段和如何将用户提供的值保存回数据库</span><span class="sxs-lookup"><span data-stu-id="da75e-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="da75e-108">如何在工时表标题中显示只读字段</span><span class="sxs-lookup"><span data-stu-id="da75e-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="da75e-109">如何集成其他自定义业务逻辑以在字段中输入默认值和执行更多验证</span><span class="sxs-lookup"><span data-stu-id="da75e-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="da75e-110">受众</span><span class="sxs-lookup"><span data-stu-id="da75e-110">Audience</span></span>

<span data-ttu-id="da75e-111">本主题面向要将自定义字段集成到适用于 Apple iOS 和 Google Android 的 Microsoft Dynamics 365 Project Timesheet 移动应用程序的开发人员。</span><span class="sxs-lookup"><span data-stu-id="da75e-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="da75e-112">假设读者熟悉 X++ 开发和项目工时单功能。</span><span class="sxs-lookup"><span data-stu-id="da75e-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="da75e-113">数据合同 – TSTimesheetCustomField X++ 类</span><span class="sxs-lookup"><span data-stu-id="da75e-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="da75e-114">**TSTimesheetCustomField** 类是用于提供有关工时单功能的自定义字段的 X++ 数据合同类。</span><span class="sxs-lookup"><span data-stu-id="da75e-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="da75e-115">将同时在 TSTimesheetDetails 数据合同和 TSTimesheetEntry 数据合同上通过自定义字段对象列表，以便在移动应用列表中显示自定义字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="da75e-116">**TSTimesheetDetails** - 工时单标题合同。</span><span class="sxs-lookup"><span data-stu-id="da75e-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="da75e-117">**TSTimesheetEntry** - 工时单交易记录合同。</span><span class="sxs-lookup"><span data-stu-id="da75e-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="da75e-118">具有相同项目信息和 **timesheetLineRecId** 值的这些对象的组构成一行。</span><span class="sxs-lookup"><span data-stu-id="da75e-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="da75e-119">fieldBaseType (Types)</span><span class="sxs-lookup"><span data-stu-id="da75e-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="da75e-120">**TsTimesheetCustom** 对象的 **FieldBaseType** 属性决定应用中显示的字段类型。</span><span class="sxs-lookup"><span data-stu-id="da75e-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="da75e-121">支持以下 **Types** 值。</span><span class="sxs-lookup"><span data-stu-id="da75e-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="da75e-122">Types 值</span><span class="sxs-lookup"><span data-stu-id="da75e-122">Types value</span></span> | <span data-ttu-id="da75e-123">类型</span><span class="sxs-lookup"><span data-stu-id="da75e-123">Type</span></span>              | <span data-ttu-id="da75e-124">注释</span><span class="sxs-lookup"><span data-stu-id="da75e-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="da75e-125">0</span><span class="sxs-lookup"><span data-stu-id="da75e-125">0</span></span>           | <span data-ttu-id="da75e-126">字符串（和枚举）</span><span class="sxs-lookup"><span data-stu-id="da75e-126">String (and Enum)</span></span> | <span data-ttu-id="da75e-127">字段显示为文本字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="da75e-128">1</span><span class="sxs-lookup"><span data-stu-id="da75e-128">1</span></span>           | <span data-ttu-id="da75e-129">整数</span><span class="sxs-lookup"><span data-stu-id="da75e-129">Integer</span></span>           | <span data-ttu-id="da75e-130">值显示为无小数位的数字。</span><span class="sxs-lookup"><span data-stu-id="da75e-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="da75e-131">2</span><span class="sxs-lookup"><span data-stu-id="da75e-131">2</span></span>           | <span data-ttu-id="da75e-132">实数</span><span class="sxs-lookup"><span data-stu-id="da75e-132">Real</span></span>              | <span data-ttu-id="da75e-133">值显示为有小数位的数字。</span><span class="sxs-lookup"><span data-stu-id="da75e-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="da75e-134">若要在应用中将实数值显示为货币，请使用 **fieldExtenededType** 属性。</span><span class="sxs-lookup"><span data-stu-id="da75e-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="da75e-135">可使用 **numberOfDecimals** 属性设置显示的小数位数。</span><span class="sxs-lookup"><span data-stu-id="da75e-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="da75e-136">3</span><span class="sxs-lookup"><span data-stu-id="da75e-136">3</span></span>           | <span data-ttu-id="da75e-137">日期</span><span class="sxs-lookup"><span data-stu-id="da75e-137">Date</span></span>              | <span data-ttu-id="da75e-138">数据格式由**用户选项**中**语言和国家/地区首选项**下的**日期、时间和数字格式**设置决定。</span><span class="sxs-lookup"><span data-stu-id="da75e-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="da75e-139">4</span><span class="sxs-lookup"><span data-stu-id="da75e-139">4</span></span>           | <span data-ttu-id="da75e-140">布尔值</span><span class="sxs-lookup"><span data-stu-id="da75e-140">Boolean</span></span>           | |
| <span data-ttu-id="da75e-141">15</span><span class="sxs-lookup"><span data-stu-id="da75e-141">15</span></span>          | <span data-ttu-id="da75e-142">GUID</span><span class="sxs-lookup"><span data-stu-id="da75e-142">GUID</span></span>              | |
| <span data-ttu-id="da75e-143">16</span><span class="sxs-lookup"><span data-stu-id="da75e-143">16</span></span>          | <span data-ttu-id="da75e-144">Int64</span><span class="sxs-lookup"><span data-stu-id="da75e-144">Int64</span></span>             | |

- <span data-ttu-id="da75e-145">如果 **TSTimesheetCustomField** 对象中不提供 **stringOptions** 属性，则向用户提供自由文本字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="da75e-146">可使用 **stringLength** 属性设置用户可输入的最大字符串长度。</span><span class="sxs-lookup"><span data-stu-id="da75e-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="da75e-147">如果在 **TSTimesheetCustomField** 对象中提供 **stringOptions** 属性，这些列表元素仅为用户可使用选项按钮（单选按钮）选择的值。</span><span class="sxs-lookup"><span data-stu-id="da75e-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="da75e-148">在这种情况下，字符串字段可以充当供用户输入的枚举值。</span><span class="sxs-lookup"><span data-stu-id="da75e-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="da75e-149">若要将值作为枚举保存到数据库，请在保存到数据库之前，通过使用命令链手动将字符串值映射回枚举（有关示例，请参阅本主题后面的“对 TSTimesheetEntryService 使用命令链将工时单条目从应用保存回数据库”部分）。</span><span class="sxs-lookup"><span data-stu-id="da75e-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="da75e-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="da75e-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="da75e-151">可使用此属性将实数值的格式设置为货币。</span><span class="sxs-lookup"><span data-stu-id="da75e-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="da75e-152">仅当 **fieldBaseType** 值为 **Real** 时，这种方法才适用。</span><span class="sxs-lookup"><span data-stu-id="da75e-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="da75e-153">**TSCustomFieldExtendedType:None** – 不应用格式设置。</span><span class="sxs-lookup"><span data-stu-id="da75e-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="da75e-154">**TSCustomFieldExtendedType::Currency** – 将值的格式设置为货币。</span><span class="sxs-lookup"><span data-stu-id="da75e-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="da75e-155">如果货币格式设置处于活动状态，可使用 **stringValue** 字段传递应用中应显示的货币代码。</span><span class="sxs-lookup"><span data-stu-id="da75e-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="da75e-156">该值为只读值。</span><span class="sxs-lookup"><span data-stu-id="da75e-156">The value is a read-only value.</span></span>

    <span data-ttu-id="da75e-157">**realValue** 字段中包含应保存到数据库的金额。</span><span class="sxs-lookup"><span data-stu-id="da75e-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="da75e-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="da75e-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="da75e-159">可使用此属性指定自定义字段在应用中的显示位置。</span><span class="sxs-lookup"><span data-stu-id="da75e-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="da75e-160">**TSCustomFieldSection::Header** – 字段将在应用中的**查看更多详细信息**部分显示。</span><span class="sxs-lookup"><span data-stu-id="da75e-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="da75e-161">这些字段始终为只读字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-161">These fields are always read-only.</span></span>
- <span data-ttu-id="da75e-162">**TSCustomFieldSection::Line** – 字段在工时单条目中所有现成行字段后显示。</span><span class="sxs-lookup"><span data-stu-id="da75e-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="da75e-163">这些字段可以是可编辑字段，也可以是只读字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="da75e-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="da75e-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="da75e-165">此属性在应用提供的值被保存回数据库时标识字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="da75e-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="da75e-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="da75e-167">此属性在应用提供的值被保存回数据库时标识字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="da75e-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="da75e-168">isEditable (NoYes)</span></span>

<span data-ttu-id="da75e-169">如果将此属性设置为 **Yes**，则指定用户应该可以编辑工时单条目部分中的字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="da75e-170">如果将此属性设置为 **No**，则将字段设置为只读字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="da75e-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="da75e-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="da75e-172">如果将此属性设置为 **Yes**，则指定工时单条目部分中的字段为必填字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="da75e-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="da75e-173">label (str)</span></span>

<span data-ttu-id="da75e-174">此字段指定应用中字段旁边显示的标签。</span><span class="sxs-lookup"><span data-stu-id="da75e-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="da75e-175">stringOptions（字符串列表）</span><span class="sxs-lookup"><span data-stu-id="da75e-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="da75e-176">仅当 **fieldBaseType** 设置为 **String** 时，此属性才适用。</span><span class="sxs-lookup"><span data-stu-id="da75e-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="da75e-177">如果设置 **stringOptions**，则由列表中的字符串指定可通过选项按钮（单选按钮）选择的字符串值。</span><span class="sxs-lookup"><span data-stu-id="da75e-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="da75e-178">如果不提供字符串，则允许字符串字段中的自由文本条目（有关示例，请参阅本主题后面的“对 TSTimesheetEntryService 使用命令链将工时单条目从应用保存回数据库”部分）。</span><span class="sxs-lookup"><span data-stu-id="da75e-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="da75e-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="da75e-179">stringLength (int)</span></span>

<span data-ttu-id="da75e-180">此属性指定字符串字段的最大长度。</span><span class="sxs-lookup"><span data-stu-id="da75e-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="da75e-181">仅当 **fieldBaseType** 设置为 **String** 时才适用。</span><span class="sxs-lookup"><span data-stu-id="da75e-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="da75e-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="da75e-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="da75e-183">此属性指定为实数字段显示的小数位数。</span><span class="sxs-lookup"><span data-stu-id="da75e-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="da75e-184">仅当 **fieldBaseType** 设置为 **Real** 时才适用。</span><span class="sxs-lookup"><span data-stu-id="da75e-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="da75e-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="da75e-185">orderSequence (int)</span></span>

<span data-ttu-id="da75e-186">此属性控制当指定了多个自定义字段时自定义字段在应用中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="da75e-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="da75e-187">编号较小的字段先显示。</span><span class="sxs-lookup"><span data-stu-id="da75e-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="da75e-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="da75e-188">booleanValue (boolean)</span></span>

<span data-ttu-id="da75e-189">对于类型为 **Boolean** 的字段，此属性在服务器与应用之间传递布尔值类型的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="da75e-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="da75e-190">guidValue (guid)</span></span>

<span data-ttu-id="da75e-191">对于类型为 **GUID** 的字段，此属性在服务器与应用之间传递全局唯一标识符 (GUID) 格式的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="da75e-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="da75e-192">int64Value (int64)</span></span>

<span data-ttu-id="da75e-193">对于类型为 **Int64** 的字段，此属性在服务器与应用之间传递 Int64 类型的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="da75e-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="da75e-194">intValue (int)</span></span>

<span data-ttu-id="da75e-195">对于类型为 **Int** 的字段，此属性在服务器与应用之间传递 Int 类型的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="da75e-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="da75e-196">realValue (real)</span></span>

<span data-ttu-id="da75e-197">对于类型为 **Real** 的字段，此属性在服务器与应用之间传递实数类型的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="da75e-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="da75e-198">stringValue (str)</span></span>

<span data-ttu-id="da75e-199">对于类型为 **String** 的字段，此属性在服务器与应用之间传递字符串类型的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="da75e-200">还用于格式设置为货币的 **Real** 类型的字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="da75e-201">对于这些字段，此属性用于将币种代码传递到应用。</span><span class="sxs-lookup"><span data-stu-id="da75e-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="da75e-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="da75e-202">dateValue (date)</span></span>

<span data-ttu-id="da75e-203">对于类型为 **Date** 的字段，此属性在服务器与应用之间传递日期类型的字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="da75e-204">在工时单条目部分中显示和保存自定义字段</span><span class="sxs-lookup"><span data-stu-id="da75e-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="da75e-205">下面是移动应用创建工时单条目的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="da75e-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="da75e-206">其中显示“时间条目”部分中的现成字段和一个名称为“测试字符串”的自定义字段，并且已设置了枚举值“第二个选项”。</span><span class="sxs-lookup"><span data-stu-id="da75e-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![测试应用中的字符串自定义字段](media/timesheet-entry.jpg)



<span data-ttu-id="da75e-208">下面是移动应用中用户选择“测试字符串”自定义字段的一个可用枚举选项的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="da75e-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="da75e-209">两个选项为显示为单选按钮的“第一个选项”和“第二个选项”。</span><span class="sxs-lookup"><span data-stu-id="da75e-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="da75e-210">当前已选择第二个选项。</span><span class="sxs-lookup"><span data-stu-id="da75e-210">The second option is currently selected.</span></span>

![“测试字符串”自定义字段的选项按钮（单选按钮）](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="da75e-212">扩展 TSTimesheetLine 表，使其具有自定义字段</span><span class="sxs-lookup"><span data-stu-id="da75e-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="da75e-213">在典型场景中，可能会将工时单条目部分中的自定义字段的数据保存到 TSTimesheetLine 表。</span><span class="sxs-lookup"><span data-stu-id="da75e-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="da75e-214">但是，如果可以基于提供的 TSTimesheetTrans 记录检索数据，或者如果没有具体的记录上下文（例如，如果字段在项目参数中设置为只读），则可以使用其他表。</span><span class="sxs-lookup"><span data-stu-id="da75e-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="da75e-215">请注意，自定义字段不需要有任何支持数据库记录。</span><span class="sxs-lookup"><span data-stu-id="da75e-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="da75e-216">可以基于 X++ 逻辑动态生成这些字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="da75e-217">可以在只读方案中使用这种方法（有关动态生成的自定义字段值的示例，请参阅“对 TSTimesheetDetails 类的 buildCustomFieldListForHeader 方法使用命令链填充工时单详细信息”部分）。</span><span class="sxs-lookup"><span data-stu-id="da75e-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="da75e-218">显示应用程序对象树的 Visual Studio 的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="da75e-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="da75e-219">其中显示了 TSTimesheetLine 表的一个扩展，该表中有一个 TestLineString 字段被作为自定义字段添加。</span><span class="sxs-lookup"><span data-stu-id="da75e-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![行字符串](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="da75e-221">对 TSTimesheetSettings 类的 buildCustomFieldList 方法使用命令链在工时表条目部分中显示字段</span><span class="sxs-lookup"><span data-stu-id="da75e-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="da75e-222">此代码用于控制字段在应用中的显示设置。</span><span class="sxs-lookup"><span data-stu-id="da75e-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="da75e-223">例如，控制字段的类型、标签，字段是否为必填字段，以及字段在哪个部分中显示。</span><span class="sxs-lookup"><span data-stu-id="da75e-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="da75e-224">下面的示例显示时间条目中的一个字符串字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="da75e-225">此字段有两个选项，即**第一个选项**和**第二个选项**，可通过选项按钮（单选按钮）启用这些选项。</span><span class="sxs-lookup"><span data-stu-id="da75e-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="da75e-226">应用中的字段与添加到 TSTimesheetLine 表的 **TestLineString** 字段关联。</span><span class="sxs-lookup"><span data-stu-id="da75e-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="da75e-227">请注意，使用 **TSTimesheetCustomField::newFromMetatdata()** 方法可以简化以下自定义字段属性的初始化：**fieldBaseType**、**tableName**、**fieldname**、**label**、**isEditable**、**isMandatory**、**stringLength** 和 **numberOfDecimals**。</span><span class="sxs-lookup"><span data-stu-id="da75e-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="da75e-228">如果愿意，也可以手动设置这些参数。</span><span class="sxs-lookup"><span data-stu-id="da75e-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="da75e-229">对 TSTimesheetEntry 类的 buildCustomFieldListForEntry 方法使用命令链在工时表条目中输入值</span><span class="sxs-lookup"><span data-stu-id="da75e-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="da75e-230">**buildCustomFieldListForEntry** 方法用于在移动应用中保存的工时表行内输入值。</span><span class="sxs-lookup"><span data-stu-id="da75e-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="da75e-231">它采用 TSTimesheetTrans 记录充当参数。</span><span class="sxs-lookup"><span data-stu-id="da75e-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="da75e-232">可使用来自该记录的字段填充应用中的自定义字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="da75e-233">对 TSTimesheetEntryService 类使用命令链将来自应用的工时单条目保存回数据库</span><span class="sxs-lookup"><span data-stu-id="da75e-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="da75e-234">若要在典型使用时将自定义字段保存回数据库，必须扩展多个方法：</span><span class="sxs-lookup"><span data-stu-id="da75e-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="da75e-235">**timesheetLineNeedsUpdating** 方法用于确定应用中的用户是否已更改了行记录，以及是否必须将行记录保存到数据库。</span><span class="sxs-lookup"><span data-stu-id="da75e-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="da75e-236">如果不需要考虑性能，可以简化此方法，使其始终返回 **true**。</span><span class="sxs-lookup"><span data-stu-id="da75e-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="da75e-237">可扩展 **populateTimesheetLineFromEntryDuringCreate** 和 **populateTimesheetLineFromEntryDuringUpdate** 方法，以使其在 TSTimesheetLine 数据库记录中输入来自提供的 TSTimesheetEntry 数据合同记录的值。</span><span class="sxs-lookup"><span data-stu-id="da75e-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="da75e-238">请注意在下面的示例中，如何通过 X++ 代码手动完成了数据库字段与条目字段之间的映射。</span><span class="sxs-lookup"><span data-stu-id="da75e-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="da75e-239">如果映射到 **TSTimesheetEntry** 对象的自定义字段必须写回到 TSTimesheetLineweek 数据库表，也可以扩展 **populateTimesheetWeekFromEntry** 方法。</span><span class="sxs-lookup"><span data-stu-id="da75e-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="da75e-240">以下示例将用户选择的 **firstOption** 或 **secondOption** 值作为原始字符串值保存到数据库。</span><span class="sxs-lookup"><span data-stu-id="da75e-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="da75e-241">如果数据库字段为 **Enum** 类型的字段，则可以将这些值手动映射到枚举值，然后保存到数据库表中的枚举字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="da75e-242">在工时单标题部分中显示自定义字段</span><span class="sxs-lookup"><span data-stu-id="da75e-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="da75e-243">下面是用户查看工时单的移动应用的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="da75e-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="da75e-244">右上角已选择了“更多信息”按钮，以便显示“查看更多详细信息”选项。</span><span class="sxs-lookup"><span data-stu-id="da75e-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![“查看更多详细信息”命令](media/show-more.png)



<span data-ttu-id="da75e-246">下面是移动应用显示工时表的“更多”部分的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="da75e-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="da75e-247">已向工时表标题部分添加了一个名称为“此工时单的利用率 (计算自定义字段)”的自定义字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="da75e-248">为这个自定义字段设置了只读值“0.667”。</span><span class="sxs-lookup"><span data-stu-id="da75e-248">A read-only value of "0.667" is set on the custom field.</span></span>

![“更多”部分](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="da75e-250">扩展 TSTimesheetTable 表，使其具有自定义字段</span><span class="sxs-lookup"><span data-stu-id="da75e-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="da75e-251">在典型场景中，标题部分中的自定义字段的数据将从 TSTimesheetHeader 表中提取。</span><span class="sxs-lookup"><span data-stu-id="da75e-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="da75e-252">但是，如果可以基于提供的 TSTimesheetTable 记录检索数据，或者如果没有具体的记录上下文（例如，如果字段在项目参数中设置为只读），则可以使用其他表。</span><span class="sxs-lookup"><span data-stu-id="da75e-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="da75e-253">请注意，自定义字段不需要有任何支持数据库记录。</span><span class="sxs-lookup"><span data-stu-id="da75e-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="da75e-254">可以基于 X++ 逻辑动态生成这些字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="da75e-255">下面的示例显示此方法。</span><span class="sxs-lookup"><span data-stu-id="da75e-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="da75e-256">标题部分中的字段在应用中始终为只读字段。</span><span class="sxs-lookup"><span data-stu-id="da75e-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="da75e-257">对 TSTimesheetSettings 类的 buildCustomFieldList 方法使用命令链在标题部分中显示字段</span><span class="sxs-lookup"><span data-stu-id="da75e-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="da75e-258">此代码用于控制字段在应用中的显示设置。</span><span class="sxs-lookup"><span data-stu-id="da75e-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="da75e-259">例如，控制字段的类型、标签，字段是否为必填字段，以及字段在哪个部分中显示。</span><span class="sxs-lookup"><span data-stu-id="da75e-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="da75e-260">以下示例在应用的标题部分中显示一个计算值。</span><span class="sxs-lookup"><span data-stu-id="da75e-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="da75e-261">对 TSTimesheetDetails 类的 buildCustomFieldListForHeader 方法使用命令链填写工时单详细信息</span><span class="sxs-lookup"><span data-stu-id="da75e-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="da75e-262">**buildCustomFieldListForHeader** 方法用于在移动应用中填写工时表标题详细信息。</span><span class="sxs-lookup"><span data-stu-id="da75e-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="da75e-263">它采用 TSTimesheetTable 记录充当参数。</span><span class="sxs-lookup"><span data-stu-id="da75e-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="da75e-264">可使用来自该记录的字段填充应用中的自定义字段值。</span><span class="sxs-lookup"><span data-stu-id="da75e-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="da75e-265">以下示例不从数据库读取任何值。</span><span class="sxs-lookup"><span data-stu-id="da75e-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="da75e-266">而是使用 X++ 逻辑生成计算值，然后在应用中显示。</span><span class="sxs-lookup"><span data-stu-id="da75e-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="da75e-267">其他可配置性/可扩展性机会</span><span class="sxs-lookup"><span data-stu-id="da75e-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="da75e-268">为应用添加更多验证</span><span class="sxs-lookup"><span data-stu-id="da75e-268">Adding additional validation for the app</span></span>

<span data-ttu-id="da75e-269">数据库级别工时单功能的现有逻辑仍然可以正常工作。</span><span class="sxs-lookup"><span data-stu-id="da75e-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="da75e-270">若要中断保存或提交操作的完成并显示特定错误消息，可通过命令链扩展向代码添加 **throw error("message to user")**。</span><span class="sxs-lookup"><span data-stu-id="da75e-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="da75e-271">下面是有用的可扩展方法的三个示例：</span><span class="sxs-lookup"><span data-stu-id="da75e-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="da75e-272">如果在对工时表行执行保存操作期间对 TSTimesheetLine 表调用 **validateWrite** 返回了 **false**，将在移动应用中显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="da75e-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="da75e-273">如果在应用中提交工时表期间对 TSTimesheetTable 表调用 **validateSubmit** 返回了 **false**，将向用户显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="da75e-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="da75e-274">对 TSTimesheetLine 表调用 **insert** 方法期间，仍将运行用于填写字段（如**行属性**）的逻辑。</span><span class="sxs-lookup"><span data-stu-id="da75e-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="da75e-275">通过配置隐藏现成字段和将此类字段标记为只读字段</span><span class="sxs-lookup"><span data-stu-id="da75e-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="da75e-276">可通过项目参数将现成字段设置为在移动应用中隐藏或只读。</span><span class="sxs-lookup"><span data-stu-id="da75e-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="da75e-277">请设置**项目管理和会计参数**页**工时表**选项卡上**移动工时单**部分中的选项。</span><span class="sxs-lookup"><span data-stu-id="da75e-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![项目参数](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="da75e-279">通过扩展更改可供选择的活动</span><span class="sxs-lookup"><span data-stu-id="da75e-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="da75e-280">可供项目选择的活动是通过 **TsTimesheetProjectService** 类中的 **getActivitiesForProject()** 和 **getActivityQuery()** 方法填写的。</span><span class="sxs-lookup"><span data-stu-id="da75e-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="da75e-281">可使用命令链将可供特定项目选择的活动的此行为更改为与您的业务场景匹配。</span><span class="sxs-lookup"><span data-stu-id="da75e-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="da75e-282">在工时单条目中输入默认项目类别</span><span class="sxs-lookup"><span data-stu-id="da75e-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="da75e-283">可在三个级别输入工时单条目中的默认项目类别。</span><span class="sxs-lookup"><span data-stu-id="da75e-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="da75e-284">可使用命令链扩展这些级别中任何一个或全部的行为以获得所需行为。</span><span class="sxs-lookup"><span data-stu-id="da75e-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="da75e-285">将使用以下层次结构：</span><span class="sxs-lookup"><span data-stu-id="da75e-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="da75e-286">应用尝试放入来自项目资源的默认类别。</span><span class="sxs-lookup"><span data-stu-id="da75e-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="da75e-287">此默认类别是在 **TSTimesheetSettingsService** 类中的 **getCurrentUserResource** 和 **getDelegatedResourcesForCurrentUser** 方法中设置的。</span><span class="sxs-lookup"><span data-stu-id="da75e-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="da75e-288">如果提供的默认类别不是项目资源级别，应用将尝试从项目活动提取。</span><span class="sxs-lookup"><span data-stu-id="da75e-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="da75e-289">此默认类别是在 **TSTimesheetProjectService** 类中的 **getActivitiesForProject** 方法中设置的。</span><span class="sxs-lookup"><span data-stu-id="da75e-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="da75e-290">如果提供的默认类别不是项目活动级别，将从项目参数采用默认类别。</span><span class="sxs-lookup"><span data-stu-id="da75e-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="da75e-291">此默认类别是在 **TSTimesheetProjectService** 类中的 **getProjectDetailsbyRule** 方法中设置的。</span><span class="sxs-lookup"><span data-stu-id="da75e-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
