<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="configure-account-structures.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>configure-account-structures.6e0715.5fbd4b34d09b4ba8e1d34234c8e32268bba18778.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5fbd4b34d09b4ba8e1d34234c8e32268bba18778</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\general-ledger\configure-account-structures.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure account structures</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置科目结构</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about account structures and financial dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此主题提供有关科目结构和财务维度的信息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure account structures</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置科目结构</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Account structures use the main account and financial dimensions to create a set of rules that determine the order and values used when entering the account number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">科目结构使用主科目和财务维度创建一组规则，用于在输入科目编号时确定所用顺序和值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You can set up as many account structures as you need for your business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可根据企业的需要设置任意数量的科目结构。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The account structures are assigned to a company’s ledger setup, so they can be shared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将把科目结构分配给公司的日记帐设置，以便共享。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When creating an account structure, the maximum number of segments is 11.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">创建科目结构时，最大科目段数为 11。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you need more segments than this, thoroughly evaluate your setup and requirements, as it will impact the user experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果需要的科目段超过此数量，请彻底评估您的设置和需求，因为这会影响用户体验。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Consider if a segment could be derived in a reporting scenario using a hierarchy instead of during data entry, or by using a user-defined field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">考虑科目段在申报方案中是否使用层次结构派生，而不是在数据录入期间或通过使用用户定义的字段派生。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For example, if you want to report on location, but you can figure location by department or cost center, you would not need location as a financial dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例如，如果要按位置申报，但是您可以通过部门或成本中心识别位置，则不需要将位置设置为财务维度。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If after evaluation you do determine more than 11 segments are needed, you can add additional segments using advanced rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果在评估后的确认定需要的科目段数超过 11 个，则可使用高级规则添加更多科目段。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Account structures require the main account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">科目结构需要主科目。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The main account does not need to be the first segment in the structure, but it does identify what account structure is being used during the account number entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主科目不需要是结构中的第一个科目段，但的确可用于在录入科目编号时确定使用的是哪个科目结构。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Because of this, a main account value can only exist in one structure assigned to the ledger so that they do not overlap.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">因此，只有分配给日记帐的一个结构中可以有主科目值，以免重合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>After the account structure is identified, the allowed values list is filtered to guide the user through picking only valid dimension values, decreasing the possibility of an incorrect journal entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">识别了科目结构之后，将筛选允许值列表以引导用户仅选择有效的维度值，从而日记帐录入错误的可能性。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you plan to budget against a financial dimension, it will need to be part of an account structure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果计划针对财务维度编制预算，则该财务维度需要是科目结构的一部分。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Budgeting does not currently utilize advanced rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">编制预算现在不使用高级规则。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To illustrate a best practice for setting up an account structure, let's assume that a company wants to track their balance sheet accounts (100000..399999) at the account and business unit financial dimension level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">为了说明有关设置科目结构的最佳实践，假设一家公司希望在科目和业务单位财务维度级别跟踪自己的资产负债表科目 (100000..399999)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For revenue and expense accounts (400000..999999), they track financial dimensions Business Unit, Department, and Cost center.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于收入科目和支出科目 (400000..999999)，该公司跟踪财务维度“业务单位”、“部门”和“成本中心”。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If they make a sale, they also like to track Customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果他们开展销售，也希望跟踪客户。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Using this scenario, it would be recommended to have two account structures assigned to the company’s ledger - one for Balance sheet accounts, and one for Profit and Loss accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果使用此方案，建议为该公司的日记帐指定两个科目结构 - 一个用于资产负债表科目，一个用于损益科目。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To optimize the user experience and validation, Customer should be an advanced rule that is only used when a sales account is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要优化用户体验和验证，“客户”应该是仅当使用了销售科目时财神爷的高级规则。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Balance sheet account structure<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>资产负债表科目结构<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Main account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主科目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Business unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">业务单位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>100000..399999</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">100000..399999</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>*;” “</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">*;” “</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Profit and loss account structure<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>损益科目结构<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Main account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主科目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Business unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">业务单位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Department</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">部门</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Cost center</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">成本中心</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>400000..999999</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">400000..999999</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>*;” “</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">*;” “</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>*;” “</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">*;” “</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>*;” “</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">*;” “</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>*;” “</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">*;” “</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Advanced rule for adding a Customer<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>用于添加客户的高级规则<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Criteria: Where Main account is between 400000 and 499999, then add customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件：主科目介于 400000 与 499999 之间时，添加客户。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It cannot be left blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">不能将其保留为空。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">客户</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In this simplified example, all values and blank are allowed so * and “ “ are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在这个简化的示例中，允许所有值和空白，所以使用了 * 和 “ “。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Segments and allowed values</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">段落和允许的值</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The <bpt id="p1">**</bpt>Segments<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Allowed values details<ept id="p2">**</ept> section provides a grid like experience for entering the rules that will be followed on validation during posting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>科目段<ept id="p1">**</ept>和<bpt id="p2">**</bpt>允许的值详细信息<ept id="p2">**</ept>部分提供了网格式体验，用于输入过帐期间验证时要遵循的规则。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You can type directly in the cells in the grid, import it from Excel, or use the <bpt id="p1">**</bpt>Allowed value details<ept id="p1">**</ept> section to guide you through it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可直接在网格中的单元格内键入，从 Excel 导入，或使用<bpt id="p1">**</bpt>允许的值详细信息<ept id="p1">**</ept>部分引导您完成。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The <bpt id="p1">**</bpt>Allowed value details<ept id="p1">**</ept> section guides you through creating criteria using <bpt id="p2">**</bpt>Operators<ept id="p2">**</ept> such as begins with, is between, includes, and many others.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>允许的值详细信息<ept id="p1">**</ept>部分可引导您使用开头为、介于、包含等各种<bpt id="p2">**</bpt>运算符<ept id="p2">**</ept>创建条件。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Allow values<ept id="p1">](./media/account.png)](./media/account.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>允许值<ept id="p1">](./media/account.png)](./media/account.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Allowed values will default onto a journal or accounting distribution entry page when there are no other possible values to select according to the account structure setup.</source><target logoport:matchpercent="0" state="translated">在根据科目结构设置没有其他潜在值可供选择时，将把允许的值设置为日记帐或会计分配录入页中的默认值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Here's an example of the <bpt id="p1">**</bpt>Profit and loss account structure<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">下面是<bpt id="p1">**</bpt>损益科目结构<ept id="p1">**</ept>的示例。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Main account</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">主科目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Business unit</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">业务单位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Department</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">部门</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Cost center</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">成本中心</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>400000..999999</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">400000..999999</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>002</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">002</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>022</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">022</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>014</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">014</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>When entering a journal and selecting an account in the profit and loss range, selecting business unit '002' will cause values 022 and 014 to be the default on the account control.</source><target logoport:matchpercent="0" state="translated">输入日记帐和在损益范围内选择科目时，选择业务单位“002”将导致把值 022 和 014 设置为科目控件上的默认值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>This behavior will also occur with the accounting distribution page.</source><target logoport:matchpercent="0" state="translated">还将在会计分配页中发生以下行为。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>More than 7 criteria needed</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">需要 7 个以上的条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>If you have more than 7 criteria that are needed, you can continue adding them on the next line.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">如果需要的条件超过 7 个，则可在下一行中继续添加条件。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>You will notice when working in the <bpt id="p1">**</bpt>Allowed value details<ept id="p1">**</ept> section that the <bpt id="p2">**</bpt>+Add new<ept id="p2">**</ept> criteria is nt longer active after the seventh criteria is entered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您将发现在<bpt id="p1">**</bpt>允许的值详细信息<ept id="p1">**</ept>部分中工作时，输入了第七个条件之后，<bpt id="p2">**</bpt>+新添<ept id="p2">**</ept>添加将不再处于活动状态。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>This is due to many factors such as:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">原因很多，例如：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Column width</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列宽</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>How the data is stored</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数据的存储方式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Performance of the <bpt id="p1">**</bpt>Allowed value details<ept id="p1">**</ept> control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>允许的值详细信息<ept id="p1">**</ept>控件的性能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Usability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可用性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To continue to add additional criteria, click <bpt id="p1">**</bpt>Duplicate in the Segment<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Allowed values section<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要继续添加更多添加，请单击<bpt id="p1">**</bpt>在科目段中复制<ept id="p1">**</ept>和<bpt id="p2">**</bpt>允许的值部分<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This will copy the criteria to a new line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这样就会把条件复制到新行中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>You can then type over or modify the <bpt id="p1">**</bpt>Allowed value details<ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">然后可以再次键入或修改<bpt id="p1">**</bpt>允许的值详细信息<ept id="p1">**</ept>部分。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Best practices</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">最佳实践</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>When setting up your account structures there are some best practices you can follow.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">设置科目结构时，可以遵循一些最佳实践。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>However, this is only guidance so a holistic discussion about your business, growth plan, and maintenance plan should be considered as part of that discussion.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">但是，这只是指导，所以在通盘讨论中应考虑业务、成长计划和维持计划。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Make main account first or as close to the front of the account structure as possible, so users get the best guided experience they can during account entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">让主科目成为科目结构的第一项或尽量靠近科目结构前面，这样用户就可以在录入科目时获得最佳的引导式体验。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Reuse account structures as much as possible to reduce maintenance across your legal entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">尽量重复使用科目结构，以减少法人中的维护。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>For variations across legal entities, consider using advanced rules so that account structures can be reused.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于法人中的变型，请考虑使用高级规则，以便重复使用科目结构。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>When defining allowed values, use ranges and wildcards as much as possible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定义允许的值时，请尽量使用范围和通配符。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This not only allows you to grow and change without maintenance, but the system also performs more ideally with this configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这样在此配置下不仅可以在不进行维护的情况下增长和变化，而且系统还可以更理想地运行。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Do not just put an asterisk for every segment in the account structure and then solely rely on the advanced rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请不要只是为科目结构中的每个科目段放一个星号，然后单纯地依赖高级规则。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This can be difficult to manage and often leads to user error during maintenance that can make the system unable to post.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这样可能很难管理，往往会在维护期间导致用户错误，从而让系统无法过帐。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Account structure activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">科目结构启用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>When you are satifisfied with your new setup or a change to an account structure, you must activate it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果对科目结构的新设置或更改感到满意，必须将其激活。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>If an account structure is assigned to a ledger, this activation can be a long running process, as all unposted transactions in the system must be synced to the new structure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果为日记帐分配了科目结构，此项激活可能需要运行很长一段时间，因为必须将系统中的所有未过帐交易记录同步到新结构中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Posted transactions are not impacted with account structure changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">科目结构的变化不影响已过帐交易记录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>For more information, see <bpt id="p1">[</bpt>Plan your chart of accounts<ept id="p1">](plan-chart-of-accounts.md)</ept>, <bpt id="p2">[</bpt>Financial dimensions<ept id="p2">](financial-dimensions.md)</ept> and <bpt id="p3">[</bpt>Enter account and dimension combinations (segmented entry control)<ept id="p3">](enter-account-dimension-combinations-segmented-entry-control.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关详细信息，请参阅<bpt id="p1">[</bpt>计划您的会计科目表<ept id="p1">](plan-chart-of-accounts.md)</ept>、<bpt id="p2">[</bpt>财务维度<ept id="p2">](financial-dimensions.md)</ept>和<bpt id="p3">[</bpt>输入科目和维度组合（分段式录入控件）<ept id="p3">](enter-account-dimension-combinations-segmented-entry-control.md)</ept>。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>