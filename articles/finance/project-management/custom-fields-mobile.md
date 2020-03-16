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
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080764"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>为 iOS 和 Android 上的 Microsoft Dynamics 365 Project Timesheet 移动应用实施自定义字段

[!include [banner](../includes/banner.md)]

本主题提供有关使用扩展实施自定义字段的常见模式。 包括以下主题：

- 自定义字段框架支持的各种数据类型
- 如何在工时表条目中显示只读或可编辑字段和如何将用户提供的值保存回数据库
- 如何在工时表标题中显示只读字段
- 如何集成其他自定义业务逻辑以在字段中输入默认值和执行更多验证

## <a name="audience"></a>受众

本主题面向要将自定义字段集成到适用于 Apple iOS 和 Google Android 的 Microsoft Dynamics 365 Project Timesheet 移动应用程序的开发人员。 假设读者熟悉 X++ 开发和项目工时单功能。

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>数据合同 – TSTimesheetCustomField X++ 类

**TSTimesheetCustomField** 类是用于提供有关工时单功能的自定义字段的 X++ 数据合同类。 将同时在 TSTimesheetDetails 数据合同和 TSTimesheetEntry 数据合同上通过自定义字段对象列表，以便在移动应用列表中显示自定义字段。

- **TSTimesheetDetails** - 工时单标题合同。
- **TSTimesheetEntry** - 工时单交易记录合同。 具有相同项目信息和 **timesheetLineRecId** 值的这些对象的组构成一行。

### <a name="fieldbasetype-types"></a>fieldBaseType (Types)

**TsTimesheetCustom** 对象的 **FieldBaseType** 属性决定应用中显示的字段类型。 支持以下 **Types** 值。

| Types 值 | 类型              | 注释 |
|-------------|-------------------|-------|
| 0           | 字符串（和枚举） | 字段显示为文本字段。 |
| 1           | 整数           | 值显示为无小数位的数字。 |
| 2           | 实数              | 值显示为有小数位的数字。<p>若要在应用中将实数值显示为货币，请使用 **fieldExtenededType** 属性。 可使用 **numberOfDecimals** 属性设置显示的小数位数。</p> |
| 3           | 日期              | 数据格式由**用户选项**中**语言和国家/地区首选项**下的**日期、时间和数字格式**设置决定。 |
| 4           | 布尔值           | |
| 15          | GUID              | |
| 16          | Int64             | |

- 如果 **TSTimesheetCustomField** 对象中不提供 **stringOptions** 属性，则向用户提供自由文本字段。

    可使用 **stringLength** 属性设置用户可输入的最大字符串长度。

- 如果在 **TSTimesheetCustomField** 对象中提供 **stringOptions** 属性，这些列表元素仅为用户可使用选项按钮（单选按钮）选择的值。

    在这种情况下，字符串字段可以充当供用户输入的枚举值。 若要将值作为枚举保存到数据库，请在保存到数据库之前，通过使用命令链手动将字符串值映射回枚举（有关示例，请参阅本主题后面的“对 TSTimesheetEntryService 使用命令链将工时单条目从应用保存回数据库”部分）。

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

可使用此属性将实数值的格式设置为货币。 仅当 **fieldBaseType** 值为 **Real** 时，这种方法才适用。

- **TSCustomFieldExtendedType:None** – 不应用格式设置。
- **TSCustomFieldExtendedType::Currency** – 将值的格式设置为货币。

    如果货币格式设置处于活动状态，可使用 **stringValue** 字段传递应用中应显示的货币代码。 该值为只读值。

    **realValue** 字段中包含应保存到数据库的金额。

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

可使用此属性指定自定义字段在应用中的显示位置。

- **TSCustomFieldSection::Header** – 字段将在应用中的**查看更多详细信息**部分显示。 这些字段始终为只读字段。
- **TSCustomFieldSection::Line** – 字段在工时单条目中所有现成行字段后显示。 这些字段可以是可编辑字段，也可以是只读字段。

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

此属性在应用提供的值被保存回数据库时标识字段。

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

此属性在应用提供的值被保存回数据库时标识字段。

### <a name="iseditable-noyes"></a>isEditable (NoYes)

如果将此属性设置为 **Yes**，则指定用户应该可以编辑工时单条目部分中的字段。 如果将此属性设置为 **No**，则将字段设置为只读字段。

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

如果将此属性设置为 **Yes**，则指定工时单条目部分中的字段为必填字段。

### <a name="label-str"></a>label (str)

此字段指定应用中字段旁边显示的标签。

### <a name="stringoptions-list-of-strings"></a>stringOptions（字符串列表）

仅当 **fieldBaseType** 设置为 **String** 时，此属性才适用。 如果设置 **stringOptions**，则由列表中的字符串指定可通过选项按钮（单选按钮）选择的字符串值。 如果不提供字符串，则允许字符串字段中的自由文本条目（有关示例，请参阅本主题后面的“对 TSTimesheetEntryService 使用命令链将工时单条目从应用保存回数据库”部分）。

### <a name="stringlength-int"></a>stringLength (int)

此属性指定字符串字段的最大长度。 仅当 **fieldBaseType** 设置为 **String** 时才适用。

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

此属性指定为实数字段显示的小数位数。 仅当 **fieldBaseType** 设置为 **Real** 时才适用。

### <a name="ordersequence-int"></a>orderSequence (int)

此属性控制当指定了多个自定义字段时自定义字段在应用中的显示顺序。 编号较小的字段先显示。

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

对于类型为 **Boolean** 的字段，此属性在服务器与应用之间传递布尔值类型的字段值。

### <a name="guidvalue-guid"></a>guidValue (guid)

对于类型为 **GUID** 的字段，此属性在服务器与应用之间传递全局唯一标识符 (GUID) 格式的字段值。

### <a name="int64value-int64"></a>int64Value (int64)

对于类型为 **Int64** 的字段，此属性在服务器与应用之间传递 Int64 类型的字段值。

### <a name="intvalue-int"></a>intValue (int)

对于类型为 **Int** 的字段，此属性在服务器与应用之间传递 Int 类型的字段值。

### <a name="realvalue-real"></a>realValue (real)

对于类型为 **Real** 的字段，此属性在服务器与应用之间传递实数类型的字段值。

### <a name="stringvalue-str"></a>stringValue (str)

对于类型为 **String** 的字段，此属性在服务器与应用之间传递字符串类型的字段值。 还用于格式设置为货币的 **Real** 类型的字段。 对于这些字段，此属性用于将币种代码传递到应用。

### <a name="datevalue-date"></a>dateValue (date)

对于类型为 **Date** 的字段，此属性在服务器与应用之间传递日期类型的字段值。

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>在工时单条目部分中显示和保存自定义字段

下面是移动应用创建工时单条目的屏幕快照。 其中显示“时间条目”部分中的现成字段和一个名称为“测试字符串”的自定义字段，并且已设置了枚举值“第二个选项”。

![测试应用中的字符串自定义字段](media/timesheet-entry.jpg)



下面是移动应用中用户选择“测试字符串”自定义字段的一个可用枚举选项的屏幕快照。  两个选项为显示为单选按钮的“第一个选项”和“第二个选项”。 当前已选择第二个选项。

![“测试字符串”自定义字段的选项按钮（单选按钮）](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>扩展 TSTimesheetLine 表，使其具有自定义字段

在典型场景中，可能会将工时单条目部分中的自定义字段的数据保存到 TSTimesheetLine 表。 但是，如果可以基于提供的 TSTimesheetTrans 记录检索数据，或者如果没有具体的记录上下文（例如，如果字段在项目参数中设置为只读），则可以使用其他表。

请注意，自定义字段不需要有任何支持数据库记录。 可以基于 X++ 逻辑动态生成这些字段。 可以在只读方案中使用这种方法（有关动态生成的自定义字段值的示例，请参阅“对 TSTimesheetDetails 类的 buildCustomFieldListForHeader 方法使用命令链填充工时单详细信息”部分）。

显示应用程序对象树的 Visual Studio 的屏幕快照。 其中显示了 TSTimesheetLine 表的一个扩展，该表中有一个 TestLineString 字段被作为自定义字段添加。

![行字符串](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>对 TSTimesheetSettings 类的 buildCustomFieldList 方法使用命令链在工时表条目部分中显示字段

此代码用于控制字段在应用中的显示设置。 例如，控制字段的类型、标签，字段是否为必填字段，以及字段在哪个部分中显示。

下面的示例显示时间条目中的一个字符串字段。 此字段有两个选项，即**第一个选项**和**第二个选项**，可通过选项按钮（单选按钮）启用这些选项。 应用中的字段与添加到 TSTimesheetLine 表的 **TestLineString** 字段关联。

请注意，使用 **TSTimesheetCustomField::newFromMetatdata()** 方法可以简化以下自定义字段属性的初始化：**fieldBaseType**、**tableName**、**fieldname**、**label**、**isEditable**、**isMandatory**、**stringLength** 和 **numberOfDecimals**。 如果愿意，也可以手动设置这些参数。

```xpp
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>对 TSTimesheetEntry 类的 buildCustomFieldListForEntry 方法使用命令链在工时表条目中输入值

**buildCustomFieldListForEntry** 方法用于在移动应用中保存的工时表行内输入值。 它采用 TSTimesheetTrans 记录充当参数。 可使用来自该记录的字段填充应用中的自定义字段值。

```xpp
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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>对 TSTimesheetEntryService 类使用命令链将来自应用的工时单条目保存回数据库

若要在典型使用时将自定义字段保存回数据库，必须扩展多个方法：

- **timesheetLineNeedsUpdating** 方法用于确定应用中的用户是否已更改了行记录，以及是否必须将行记录保存到数据库。 如果不需要考虑性能，可以简化此方法，使其始终返回 **true**。
- 可扩展 **populateTimesheetLineFromEntryDuringCreate** 和 **populateTimesheetLineFromEntryDuringUpdate** 方法，以使其在 TSTimesheetLine 数据库记录中输入来自提供的 TSTimesheetEntry 数据合同记录的值。 请注意在下面的示例中，如何通过 X++ 代码手动完成了数据库字段与条目字段之间的映射。
- 如果映射到 **TSTimesheetEntry** 对象的自定义字段必须写回到 TSTimesheetLineweek 数据库表，也可以扩展 **populateTimesheetWeekFromEntry** 方法。

> [!NOTE]
> 以下示例将用户选择的 **firstOption** 或 **secondOption** 值作为原始字符串值保存到数据库。 如果数据库字段为 **Enum** 类型的字段，则可以将这些值手动映射到枚举值，然后保存到数据库表中的枚举字段。

```xpp
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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>在工时单标题部分中显示自定义字段

下面是用户查看工时单的移动应用的屏幕快照。 右上角已选择了“更多信息”按钮，以便显示“查看更多详细信息”选项。  

![“查看更多详细信息”命令](media/show-more.png)

下面是移动应用显示工时表的“更多”部分的屏幕快照。 已向工时表标题部分添加了一个名称为“此工时单的利用率 (计算自定义字段)”的自定义字段。 为这个自定义字段设置了只读值“0.667”。

![“更多”部分](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>扩展 TSTimesheetTable 表，使其具有自定义字段

在典型场景中，标题部分中的自定义字段的数据将从 TSTimesheetHeader 表中提取。 但是，如果可以基于提供的 TSTimesheetTable 记录检索数据，或者如果没有具体的记录上下文（例如，如果字段在项目参数中设置为只读），则可以使用其他表。

请注意，自定义字段不需要有任何支持数据库记录。 可以基于 X++ 逻辑动态生成这些字段。 下面的示例显示此方法。

标题部分中的字段在应用中始终为只读字段。

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>对 TSTimesheetSettings 类的 buildCustomFieldList 方法使用命令链在标题部分中显示字段

此代码用于控制字段在应用中的显示设置。 例如，控制字段的类型、标签，字段是否为必填字段，以及字段在哪个部分中显示。

以下示例在应用的标题部分中显示一个计算值。

```xpp
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>对 TSTimesheetDetails 类的 buildCustomFieldListForHeader 方法使用命令链填写工时单详细信息

**buildCustomFieldListForHeader** 方法用于在移动应用中填写工时表标题详细信息。 它采用 TSTimesheetTable 记录充当参数。 可使用来自该记录的字段填充应用中的自定义字段值。 以下示例不从数据库读取任何值。 而是使用 X++ 逻辑生成计算值，然后在应用中显示。


```xpp
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

## <a name="other-configurabilityextensibility-opportunities"></a>其他可配置性/可扩展性机会

### <a name="adding-additional-validation-for-the-app"></a>为应用添加更多验证

数据库级别工时单功能的现有逻辑仍然可以正常工作。 若要中断保存或提交操作的完成并显示特定错误消息，可通过命令链扩展向代码添加 **throw error("message to user")**。 下面是有用的可扩展方法的三个示例：

- 如果在对工时表行执行保存操作期间对 TSTimesheetLine 表调用 **validateWrite** 返回了 **false**，将在移动应用中显示错误消息。
- 如果在应用中提交工时表期间对 TSTimesheetTable 表调用 **validateSubmit** 返回了 **false**，将向用户显示错误消息。
- 对 TSTimesheetLine 表调用 **insert** 方法期间，仍将运行用于填写字段（如**行属性**）的逻辑。

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>通过配置隐藏现成字段和将此类字段标记为只读字段

可通过项目参数将现成字段设置为在移动应用中隐藏或只读。 请设置**项目管理和会计参数**页**工时表**选项卡上**移动工时单**部分中的选项。

![项目参数](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>通过扩展更改可供选择的活动

可供项目选择的活动是通过 **TsTimesheetProjectService** 类中的 **getActivitiesForProject()** 和 **getActivityQuery()** 方法填写的。 可使用命令链将可供特定项目选择的活动的此行为更改为与您的业务场景匹配。

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>在工时单条目中输入默认项目类别

可在三个级别输入工时单条目中的默认项目类别。 可使用命令链扩展这些级别中任何一个或全部的行为以获得所需行为。 将使用以下层次结构：

1. 应用尝试放入来自项目资源的默认类别。 此默认类别是在 **TSTimesheetSettingsService** 类中的 **getCurrentUserResource** 和 **getDelegatedResourcesForCurrentUser** 方法中设置的。
2. 如果提供的默认类别不是项目资源级别，应用将尝试从项目活动提取。 此默认类别是在 **TSTimesheetProjectService** 类中的 **getActivitiesForProject** 方法中设置的。
3. 如果提供的默认类别不是项目活动级别，将从项目参数采用默认类别。 此默认类别是在 **TSTimesheetProjectService** 类中的 **getProjectDetailsbyRule** 方法中设置的。
