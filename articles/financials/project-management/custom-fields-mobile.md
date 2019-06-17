<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="0" state="translated">为 iOS 和 Android 上的 Microsoft Dynamics 365 Project Timesheet 移动应用实施自定义字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="0" state="translated">本主题提供有关使用扩展实施自定义字段的常见模式。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">为 iOS 和 Android 上的 Microsoft Dynamics 365 Project Timesheet 移动应用实施自定义字段</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">本主题提供有关使用扩展实施自定义字段的常见模式。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">包括以下主题：</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="0" state="translated">自定义字段框架支持的各种数据类型</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="0" state="translated">如何在工时表条目中显示只读或可编辑字段和如何将用户提供的值保存回数据库</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="0" state="translated">如何在工时表标题中显示只读字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="0" state="translated">如何集成其他自定义业务逻辑以在字段中输入默认值和执行更多验证</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">受众</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="0" state="translated">本主题面向要将自定义字段集成到适用于 Apple iOS 和 Google Android 的 Microsoft Dynamics 365 Project Timesheet 移动应用程序的开发人员。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="0" state="translated">假设读者熟悉 X++ 开发和项目工时单功能。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="0" state="translated">数据合同 – TSTimesheetCustomField X++ 类</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> 类是用于提供有关工时单功能的自定义字段的 X++ 数据合同类。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="0" state="translated">将同时在 TSTimesheetDetails 数据合同和 TSTimesheetEntry 数据合同上通过自定义字段对象列表，以便在移动应用列表中显示自定义字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - 工时单标题合同。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - 工时单交易记录合同。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="0" state="translated">具有相同项目信息和 <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> 值的这些对象的组构成一行。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="0" state="translated">fieldBaseType (Types)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="0" state="translated"><bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> 对象的 <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> 属性决定应用中显示的字段类型。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">支持以下 <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> 值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="0" state="translated">Types 值</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">类型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">注释</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">字符串（和枚举）</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">字段显示为文本字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">整数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="0" state="translated">值显示为无小数位的数字。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">实数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">值显示为有小数位的数字。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="0" state="translated">若要在应用中将实数值显示为货币，请使用 <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> 属性。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="0" state="translated">可使用 <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> 属性设置显示的小数位数。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">日期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="0" state="translated">数据格式由<bpt id="p3">**</bpt>用户选项<ept id="p3">**</ept>中<bpt id="p2">**</bpt>语言和国家/地区首选项<ept id="p2">**</ept>下的<bpt id="p1">**</bpt>日期、时间和数字格式<ept id="p1">**</ept>设置决定。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">布尔值</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="0" state="translated">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="0" state="translated">如果 <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> 对象中不提供 <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> 属性，则向用户提供自由文本字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="0" state="translated">可使用 <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> 属性设置用户可输入的最大字符串长度。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="0" state="translated">如果在 <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> 对象中提供 <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> 属性，这些列表元素仅为用户可使用选项按钮（单选按钮）选择的值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">在这种情况下，字符串字段可以充当供用户输入的枚举值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="0" state="translated">若要将值作为枚举保存到数据库，请在保存到数据库之前，通过使用命令链手动将字符串值映射回枚举（有关示例，请参阅本主题后面的“对 TSTimesheetEntryService 使用命令链将工时单条目从应用保存回数据库”部分）。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="0" state="translated">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="0" state="translated">可使用此属性将实数值的格式设置为货币。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">仅当 <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> 值为 <bpt id="p2">**</bpt>Real<ept id="p2">**</ept> 时，这种方法才适用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – 不应用格式设置。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – 将值的格式设置为货币。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="0" state="translated">如果货币格式设置处于活动状态，可使用 <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> 字段传递应用中应显示的货币代码。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="0" state="translated">该值为只读值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> 字段中包含应保存到数据库的金额。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="0" state="translated">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="0" state="translated">可使用此属性指定自定义字段在应用中的显示位置。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – 字段将在应用中的<bpt id="p2">**</bpt>查看更多详细信息<ept id="p2">**</ept>部分显示。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="0" state="translated">这些字段始终为只读字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – 字段在工时单条目中所有现成行字段后显示。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="0" state="translated">这些字段可以是可编辑字段，也可以是只读字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="0" state="translated">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="0" state="translated">此属性在应用提供的值被保存回数据库时标识字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="0" state="translated">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">此属性在应用提供的值被保存回数据库时标识字段。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="0" state="translated">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="0" state="translated">如果将此属性设置为 <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>，则指定用户应该可以编辑工时单条目部分中的字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="0" state="translated">如果将此属性设置为 <bpt id="p1">**</bpt>No<ept id="p1">**</ept>，则将字段设置为只读字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="0" state="translated">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">如果将此属性设置为 <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>，则指定工时单条目部分中的字段为必填字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="0" state="translated">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="0" state="translated">此字段指定应用中字段旁边显示的标签。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="0" state="translated">stringOptions（字符串列表）</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">仅当 <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> 设置为 <bpt id="p2">**</bpt>String<ept id="p2">**</ept> 时，此属性才适用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="0" state="translated">如果设置 <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept>，则由列表中的字符串指定可通过选项按钮（单选按钮）选择的字符串值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="0" state="translated">如果不提供字符串，则允许字符串字段中的自由文本条目（有关示例，请参阅本主题后面的“对 TSTimesheetEntryService 使用命令链将工时单条目从应用保存回数据库”部分）。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="0" state="translated">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="0" state="translated">此属性指定字符串字段的最大长度。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">仅当 <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> 设置为 <bpt id="p2">**</bpt>String<ept id="p2">**</ept> 时才适用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="0" state="translated">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="0" state="translated">此属性指定为实数字段显示的小数位数。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">仅当 <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> 设置为 <bpt id="p2">**</bpt>Real<ept id="p2">**</ept> 时才适用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="0" state="translated">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="0" state="translated">此属性控制当指定了多个自定义字段时自定义字段在应用中的显示顺序。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="0" state="translated">编号较小的字段先显示。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="0" state="translated">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="0" state="translated">对于类型为 <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递布尔值类型的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="0" state="translated">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">对于类型为 <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递全局唯一标识符 (GUID) 格式的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="0" state="translated">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">对于类型为 <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递 Int64 类型的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="0" state="translated">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">对于类型为 <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递 Int 类型的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="0" state="translated">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">对于类型为 <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递实数类型的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="0" state="translated">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">对于类型为 <bpt id="p1">**</bpt>String<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递字符串类型的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="0" state="translated">还用于格式设置为货币的 <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> 类型的字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="0" state="translated">对于这些字段，此属性用于将币种代码传递到应用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="0" state="translated">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">对于类型为 <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> 的字段，此属性在服务器与应用之间传递日期类型的字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="0" state="translated">在工时单条目部分中显示和保存自定义字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="0" state="translated">下面是移动应用创建工时单条目的屏幕快照。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="0" state="translated">其中显示“时间条目”部分中的现成字段和一个名称为“测试字符串”的自定义字段，并且已设置了枚举值“第二个选项”。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="0" state="translated">测试应用中的字符串自定义字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="0" state="translated">下面是移动应用中用户选择“测试字符串”自定义字段的一个可用枚举选项的屏幕快照。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="0" state="translated">两个选项为显示为单选按钮的“第一个选项”和“第二个选项”。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="0" state="translated">当前已选择第二个选项。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="0" state="translated">“测试字符串”自定义字段的选项按钮（单选按钮）</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="0" state="translated">扩展 TSTimesheetLine 表，使其具有自定义字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="0" state="translated">在典型场景中，可能会将工时单条目部分中的自定义字段的数据保存到 TSTimesheetLine 表。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="0" state="translated">但是，如果可以基于提供的 TSTimesheetTrans 记录检索数据，或者如果没有具体的记录上下文（例如，如果字段在项目参数中设置为只读），则可以使用其他表。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="0" state="translated">请注意，自定义字段不需要有任何支持数据库记录。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="0" state="translated">可以基于 X++ 逻辑动态生成这些字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="0" state="translated">可以在只读方案中使用这种方法（有关动态生成的自定义字段值的示例，请参阅“对 TSTimesheetDetails 类的 buildCustomFieldListForHeader 方法使用命令链填充工时单详细信息”部分）。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="0" state="translated">显示应用程序对象树的 Visual Studio 的屏幕快照。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="0" state="translated">其中显示了 TSTimesheetLine 表的一个扩展，该表中有一个 TestLineString 字段被作为自定义字段添加。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="0" state="translated">行字符串</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="0" state="translated">对 TSTimesheetSettings 类的 buildCustomFieldList 方法使用命令链在工时表条目部分中显示字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="0" state="translated">此代码用于控制字段在应用中的显示设置。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="0" state="translated">例如，控制字段的类型、标签，字段是否为必填字段，以及字段在哪个部分中显示。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="0" state="translated">下面的示例显示时间条目中的一个字符串字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="0" state="translated">此字段有两个选项，即<bpt id="p1">**</bpt>第一个选项<ept id="p1">**</ept>和<bpt id="p2">**</bpt>第二个选项<ept id="p2">**</ept>，可通过选项按钮（单选按钮）启用这些选项。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="0" state="translated">应用中的字段与添加到 TSTimesheetLine 表的 <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> 字段关联。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="0" state="translated">请注意，使用 <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> 方法可以简化以下自定义字段属性的初始化：<bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>、<bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>、<bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>、<bpt id="p5">**</bpt>label<ept id="p5">**</ept>、<bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>、<bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>、<bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> 和 <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="0" state="translated">如果愿意，也可以手动设置这些参数。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">对 TSTimesheetEntry 类的 buildCustomFieldListForEntry 方法使用命令链在工时表条目中输入值</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> 方法用于在移动应用中保存的工时表行内输入值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="0" state="translated">它采用 TSTimesheetTrans 记录充当参数。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="0" state="translated">可使用来自该记录的字段填充应用中的自定义字段值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="0" state="translated">对 TSTimesheetEntryService 类使用命令链将来自应用的工时单条目保存回数据库</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="0" state="translated">若要在典型使用时将自定义字段保存回数据库，必须扩展多个方法：</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> 方法用于确定应用中的用户是否已更改了行记录，以及是否必须将行记录保存到数据库。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">如果不需要考虑性能，可以简化此方法，使其始终返回 <bpt id="p1">**</bpt>true<ept id="p1">**</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="0" state="translated">可扩展 <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> 和 <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> 方法，以使其在 TSTimesheetLine 数据库记录中输入来自提供的 TSTimesheetEntry 数据合同记录的值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="0" state="translated">请注意在下面的示例中，如何通过 X++ 代码手动完成了数据库字段与条目字段之间的映射。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="0" state="translated">如果映射到 <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> 对象的自定义字段必须写回到 TSTimesheetLineweek 数据库表，也可以扩展 <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> 方法。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="0" state="translated">以下示例将用户选择的 <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> 或 <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> 值作为原始字符串值保存到数据库。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="0" state="translated">如果数据库字段为 <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> 类型的字段，则可以将这些值手动映射到枚举值，然后保存到数据库表中的枚举字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">在工时单标题部分中显示自定义字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">下面是用户查看工时单的移动应用的屏幕快照。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="0" state="translated">右上角已选择了“更多信息”按钮，以便显示“查看更多详细信息”选项。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">“查看更多详细信息”命令</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="0" state="translated">下面是移动应用显示工时表的“更多”部分的屏幕快照。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="0" state="translated">已向工时表标题部分添加了一个名称为“此工时单的利用率 (计算自定义字段)”的自定义字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="0" state="translated">为这个自定义字段设置了只读值“0.667”。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">“更多”部分</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">扩展 TSTimesheetTable 表，使其具有自定义字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">在典型场景中，标题部分中的自定义字段的数据将从 TSTimesheetHeader 表中提取。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">但是，如果可以基于提供的 TSTimesheetTable 记录检索数据，或者如果没有具体的记录上下文（例如，如果字段在项目参数中设置为只读），则可以使用其他表。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">请注意，自定义字段不需要有任何支持数据库记录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">可以基于 X++ 逻辑动态生成这些字段。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">下面的示例显示此方法。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">标题部分中的字段在应用中始终为只读字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">对 TSTimesheetSettings 类的 buildCustomFieldList 方法使用命令链在标题部分中显示字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">此代码用于控制字段在应用中的显示设置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">例如，控制字段的类型、标签，字段是否为必填字段，以及字段在哪个部分中显示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="0" state="translated">以下示例在应用的标题部分中显示一个计算值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">对 TSTimesheetDetails 类的 buildCustomFieldListForHeader 方法使用命令链填写工时单详细信息</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> 方法用于在移动应用中填写工时表标题详细信息。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">它采用 TSTimesheetTable 记录充当参数。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">可使用来自该记录的字段填充应用中的自定义字段值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="0" state="translated">以下示例不从数据库读取任何值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="0" state="translated">而是使用 X++ 逻辑生成计算值，然后在应用中显示。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="0" state="translated">其他可配置性/可扩展性机会</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="0" state="translated">为应用添加更多验证</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="0" state="translated">数据库级别工时单功能的现有逻辑仍然可以正常工作。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="0" state="translated">若要中断保存或提交操作的完成并显示特定错误消息，可通过命令链扩展向代码添加 <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="0" state="translated">下面是有用的可扩展方法的三个示例：</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="0" state="translated">如果在对工时表行执行保存操作期间对 TSTimesheetLine 表调用 <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> 返回了 <bpt id="p2">**</bpt>false<ept id="p2">**</ept>，将在移动应用中显示错误消息。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">如果在应用中提交工时表期间对 TSTimesheetTable 表调用 <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> 返回了 <bpt id="p2">**</bpt>false<ept id="p2">**</ept>，将向用户显示错误消息。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="0" state="translated">对 TSTimesheetLine 表调用 <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> 方法期间，仍将运行用于填写字段（如<bpt id="p1">**</bpt>行属性<ept id="p1">**</ept>）的逻辑。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="0" state="translated">通过配置隐藏现成字段和将此类字段标记为只读字段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="0" state="translated">可通过项目参数将现成字段设置为在移动应用中隐藏或只读。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="0" state="translated">请设置<bpt id="p3">**</bpt>项目管理和会计参数<ept id="p3">**</ept>页<bpt id="p2">**</bpt>工时表<ept id="p2">**</ept>选项卡上<bpt id="p1">**</bpt>移动工时单<ept id="p1">**</ept>部分中的选项。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">项目参数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="0" state="translated">通过扩展更改可供选择的活动</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">可供项目选择的活动是通过 <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> 类中的 <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> 和 <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> 方法填写的。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="0" state="translated">可使用命令链将可供特定项目选择的活动的此行为更改为与您的业务场景匹配。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="0" state="translated">在工时单条目中输入默认项目类别</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="0" state="translated">可在三个级别输入工时单条目中的默认项目类别。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="0" state="translated">可使用命令链扩展这些级别中任何一个或全部的行为以获得所需行为。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="0" state="translated">将使用以下层次结构：</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="0" state="translated">应用尝试放入来自项目资源的默认类别。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">此默认类别是在 <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> 类中的 <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> 和 <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> 方法中设置的。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="0" state="translated">如果提供的默认类别不是项目资源级别，应用将尝试从项目活动提取。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="0" state="translated">此默认类别是在 <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> 类中的 <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> 方法中设置的。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">如果提供的默认类别不是项目活动级别，将从项目参数采用默认类别。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">此默认类别是在 <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> 类中的 <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> 方法中设置的。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>