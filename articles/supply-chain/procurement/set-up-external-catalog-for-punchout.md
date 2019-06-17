<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-external-catalog-for-punchout.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-external-catalog-for-punchout.474d96.39baa331120d765543c3cf662ce53d2bcfe404ab.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>39baa331120d765543c3cf662ce53d2bcfe404ab</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\procurement\set-up-external-catalog-for-punchout.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up an external catalog for PunchOut eProcurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">为电子采购发包设置外部目录</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the use of an  external catalog or punchout catalog to collect quote information from a vendor and add it to a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此主题描述使用外部目录或发包目录从供应商收集报价信息并将其添加到申请。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up an external catalog for PunchOut eProcurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">为电子采购发包设置外部目录</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>By using the external catalog, you can ensure that the product and price information that you subsequently process in Dynamics 365 for Finance and Operations July 2017 is accurate and up to date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通过使用外部目录，您可以确保您在 Dynamics 365 for Finance and Operations 2017 年 7 月版中后续处理的产品和价格信息准确和最新。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The requisition can then be approved and converted to a purchase order and an order can be placed at the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">之后可以批准申请和转换为采购订单，并且可以向供应商下单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the external catalog is set up and an employee is preparing a requisition, there will be an option to redirect to an external site, the external catalog, and return the shopping basket that was created at the external site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置好外部目录并且员工准备申请时，将有一个选项重定向到外部站点，即外部目录，并返回在外部站点创建的购物篮。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This communication is based on the cXML protocol and it has to be set up between the systems of the buying and the selling organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此通信基于 cXML 协议且必须在购买和销售组织的系统间建立。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To set up the communication, your vendor has to provide pieces of information for you to use in the configuraiton of the external catalog such as Identity, domain of the buyers company, for example, "DUNS" and "DUNS number", credentials, and the URL to reach the vendors catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要建立通信，您的供应商必须为您提供在外部目录配置中使用的信息，例如身份、采购员公司的域（如“DUNS”和“DUNS 编号”）、凭据以及要到达供应商目录的 URL。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Setting up an external catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置外部目录</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The external catalog should enable an employee who enters a purchase requisition to be redirected to an external site to select products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部目录应支持输入采购申请的员工被重定向到外部站点以选择产品。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The products that the employee selects from the external catalog are returned to Dynamics 365 for Finance and Operations with up-to-date price information and from here, they can be added to the purchase requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">员工从外部目录选择的产品连同最新价格信息被返回到 Dynamics 365 for Finance and Operations，并且可以添加到采购申请。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The intention is not to enable employees to place an order on the external site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">其目的是不允许员工在外部站点下单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>When setting up the external catalog, you need to make sure that the purpose of the site that can be accessed by the external catalog is to collect quote information and not to place a real order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置外部目录时，您需确保外部目录可访问的站点的目的是收集报价信息，不是实际下单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To set up an external vendor catalog, complete the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要设置外部供应商目录，请完成以下任务：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Set up a procurement category hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置一个采购类别层次结构。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Set up policies for procurement category hierarchies<ept id="p1">](tasks/set-up-policies-procurement-category-hierarchies.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关详细信息，请参阅 <bpt id="p1">[</bpt>设置采购类别层次结构的策略<ept id="p1">](tasks/set-up-policies-procurement-category-hierarchies.md)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Register the vendor in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在 Finance and Operations 中登记供应商。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Before you can set up configurations to access an external vendor’s catalog, you must set up the vendor and the vendor contact in Microsoft Dynamics 365.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在您可以设置访问外部供应商目录的配置时，您必须先在 Microsoft Dynamics 365 中设置供应商和供应商联系人。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The external catalog’s vendor must also be added to the selected procurement category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部目录供应商也必须添加到所选采购类别。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For more information about registering vendors in Microsoft Dynamics 365, see <bpt id="p1">[</bpt>Manage vendor collaboration users<ept id="p1">](manage-vendor-collaboration-users.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关在 Microsoft Dynamics 365 中登记供应商的详细信息，请参阅<bpt id="p1">[</bpt>管理供应商协作用户<ept id="p1">](manage-vendor-collaboration-users.md)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For information about how to assign vendors to a procurement category, see <bpt id="p1">[</bpt>Approve vendors for specific procurement categories<ept id="p1">](tasks/approve-vendors-specific-procurement-categories.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关如何分配供应商到采购类别的信息，请参阅 <bpt id="p1">[</bpt>核准特定采购类别的供应商<ept id="p1">](tasks/approve-vendors-specific-procurement-categories.md)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Make sure that the units of measure and the currency that the vendor uses are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">确保设置供应商使用的度量单位和币种。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For information about how to create a unit of measure, see <bpt id="p1">[</bpt>Manage units of measure<ept id="p1">](../pim/tasks/manage-unit-measure.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关如何创建度量单位的信息，请参阅<bpt id="p1">[</bpt>管理度量单位<ept id="p1">](../pim/tasks/manage-unit-measure.md)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Configure the external vendor catalog by using the requirements for your vendor’s external catalog site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用对您的供应商的外部目录站点的要求配置外部供应商目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more details about this task, see <bpt id="p1">[</bpt>Configure the external vendor catalog<ept id="p1">](#configure-the-external-vendor-catalog)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关此任务的更多详细信息，请参阅<bpt id="p1">[</bpt>配置外部供应商目录<ept id="p1">](#configure-the-external-vendor-catalog)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Test the vendor’s external catalog configurations to verify that the settings are valid and that you can access the vendor’s external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">测试供应商外部目录配置以验证设置是有效的而且您可以访问供应商外部目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Use the <bpt id="p1">**</bpt>Validate settings<ept id="p1">**</ept> action to validate the request setup message that you’ve defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用<bpt id="p1">**</bpt>验证设置<ept id="p1">**</ept>操作验证您定义的请求设置消息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This message should cause the vendors external catalog site to be opened in a browser window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此消息可以导致供应商外部目录站点在浏览器窗口中打开。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>During validation, you can’t order items and services from the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在验证期间，无法从供应商订购物料和服务。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>To order items and services, you must access the vendor’s catalog from a purchase requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要订购物料和服务，则必须从采购申请访问供应商的目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Activate the external catalog by using the <bpt id="p1">**</bpt>Activate catalog<ept id="p1">**</ept> button on the <bpt id="p2">**</bpt>External catalogs<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通过使用<bpt id="p1">**</bpt>外部目录<ept id="p1">**</ept>页上的<bpt id="p2">**</bpt>激活目录<ept id="p2">**</ept>按钮激活外部目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The external catalog must be activated before employees can use it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部目录必须在员工可以使用之前激活。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You can inactivate the external catalog at any time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您可以在任何时间停用外部目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Configure the external vendor catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置外部供应商目录</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This section gives more details about task 4 in the preceding section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本节提供关于上一节中的任务 4 的更多详细信息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Enter a name and description for the vendor’s external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">输入供应商外部目录的名称和描述。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The name that you enter will appear on the cart that represents the external catalog that is shown to employees who creates a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您输入的名称将出现在代表外部目录的购物车中，显示给创建申请的员工。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Employees can click on the cart to open the catalog on the vendor’s external catalog site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">员工可以单击购物车以打开供应商外部目录站点上的目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Add an image by using the<bpt id="p1"> **</bpt>External catalog image<ept id="p1">**</ept> action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通过使用<bpt id="p1"> **</bpt>外部目录图像<ept id="p1">**</ept>操作添加图像。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The image will appear on the cart that represents the external catalog that is shown to employees who create a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此图像将出现在代表外部目录的购物车中，显示给创建申请的员工。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Note that the image’s width and height must be equal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请注意，图像的宽度和高度必须相等。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Otherwise the image won’t be displayed correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">否则图像不会正确显示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Select whether the vendor’s external catalog website should appear in the same browser window as the one where the employee has created the requisition, or if it should open in a new window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">选择供应商的外部目录网站是否应显示在员工创建申请时的相同浏览器窗口中，或者是否应在新窗口中打开。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Select the vendor for the catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">选择目录的供应商。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In the <bpt id="p1">**</bpt>Legal entities<ept id="p1">**</ept> list, there is a row for each legal entity where the vendor is set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在<bpt id="p1">**</bpt>法人<ept id="p1">**</ept>列表中，每个法人都有一行用于设置供应商。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To allow users to request products directly from the vendor’s catalog in some legal entities but not others, you can use the <bpt id="p1">**</bpt>Prevent access<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Allow access<ept id="p2">**</ept> button for each legal entity where you want the catalog to be or not to be available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要允许用户直接从某人法人（而不从其他法人）的供应商目录中申请产品，您可以对您希望提供或不提供目录的各个法人使用<bpt id="p1">**</bpt>禁止访问<ept id="p1">**</ept>或<bpt id="p2">**</bpt>允许访问<ept id="p2">**</ept>按钮。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the <bpt id="p1">**</bpt>Default expiration (Days)<ept id="p1">**</ept> field, enter the number of days that a quotation received from the external catalog is valid and can be used to purchase from the external vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在<bpt id="p1">**</bpt>默认到期（天数）<ept id="p1">**</ept>字段中，输入从外部目录收到的报价单有效，且可以用来从外部供应商进行采购的天数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>When a quotation is created and retrieved from the vendor’s external catalog site, the quotation is valid as of the current system date and remains valid for the number of days that you enter in this field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">从供应商外部目录站点创建和检索报价单时，报价单截至当前系统日期有效，且在您在此字段输入的天数内一直有效。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Click the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> button to start mapping the procurement categories to the external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">单击<bpt id="p1">**</bpt>添加<ept id="p1">**</ept>按钮以开始将采购目录映射到外部目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source> Then, in the Category name list, select a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">然后，在目录名称列表中，选择一个类别。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The list of categories is a superset of procurement categories that the vendor has been mapped to in all the legal entities that are set up for the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">类别列表是为供应商设置的所有法人中的供应商已经映射到的采购类别的超集。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Procurement policies are used to allow or restrict access to categories for the buying legal entity or receiving operating unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">采购策略用于允许或限制对采购法人或接收运营单位的类别的访问权限。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source> Punchout to an external catalog requires that access be allowed to at least one of the procurement categories that is mapped to the catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">发包到外部目录要求允许访问至少一个映射到目录的采购类别。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Set up the cXML setup request message that will be sent to the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置将发送到供应商的 cXML 设置请求消息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The automatically generated message format is the minimal template that is required in order to start a session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自动生成的消息格式是为了启动会话所需的最小模板。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Fill in values for the tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">填写标记的值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>At any time, you can reload the system-generated message template by clicking <bpt id="p1">**</bpt>Restore message format<ept id="p1">**</ept>.<ph id="ph1"> </ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在任何时候，您都可以通过单击<bpt id="p1">**</bpt>还原消息格式<ept id="p1">**</ept>重载系统生成的消息模板。<ph id="ph1"> </ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Note that if you restore the message format, the current message will be replaced by the automatically generated message format, which has empty tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请注意，如果还原消息格式，当前消息将自动替换成自动生成的具有空标记的消息格式。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>cXML setup message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">cXML 设置消息</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Below you can find a description of the tags that are included in the template:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您可以在下方找到模板中包含的标记的描述：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">字段</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">说明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>&lt; Header &gt;&lt; From &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; From &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The domain of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">采购员公司的域。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>&lt; Header &gt;&lt; From &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; From &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The identity of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">采购员公司的标识。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>&lt; Header &gt;&lt; To &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; To &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The domain of the vendor’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">供应商公司的域。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>&lt; Header &gt;&lt; To &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; To &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The identity of the vendor’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">供应商公司的标识。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The domain of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">采购员公司的域。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; Identity &gt;&lt; /Identity&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; Identity &gt;&lt; /Identity&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The identity of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">采购员公司的标识。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; SharedSecret &gt;&lt; /SharedSecret &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; SharedSecret &gt;&lt; /SharedSecret &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The shared secret for the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">采购员公司的共享密钥。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>&lt; Request deploymentMode=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; 请求 deploymentMode=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The test or production deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">测试或生产部署。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>&lt; Request &gt;&lt; PunchOutSetupRequest &gt;&lt; SupplierSetup &gt;&lt; URL &gt;&lt; /URL&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Request &gt;&lt; PunchOutSetupRequest &gt;&lt; SupplierSetup &gt;&lt; URL &gt;&lt; /URL&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The URL of the vendor’s punchout endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">供应商发包终结点的 URL。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Extrinsic elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外在元素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>An extrinsic element is additional information, such as a user name that is based on a user that punches out. The extrinsic element is set when the punchout occurs and it can be sent in the request setup message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外在元素的附加信息，例如基于发包的用户的用户名称。外在元素在发生发包且可以在请求设置消息中发送时进行设置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Your vendor could have a requirement for receiving an extrinsic element in the setup request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您的供应商可能提出在设置请求中收到外在元素的要求。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In that case, you should add the extrinsic element to the list of extrinsic elements in the <bpt id="p1">**</bpt>Message format<ept id="p1">**</ept> section of the <bpt id="p2">**</bpt>External catalog<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在这种情况下，您应将外在元素添加到<bpt id="p1">**</bpt>外部目录<ept id="p1">**</ept>页的<bpt id="p2">**</bpt>消息格式<ept id="p2">**</ept>部分中的外在元素列表。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Specify a name for the extrinsic element that the vendor can recognize and map it to a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定供应商可以识别并将其映射到值的外在元素的名称。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The options for values are: User name, User email, or Random value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">值的选项为：用户名、用户电子邮件或随机值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For more information about the cXML protocol, see the <bpt id="p1">[</bpt>cXML.org website<ept id="p1">](http://cxml.org/)</ept>.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">有关 cXML 协议的详细信息，请访问 <bpt id="p1">[</bpt>cXML.org 网站<ept id="p1">](http://cxml.org/)</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Post back message</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">回发消息</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The post back message is the message that is received from the vendor when the user checks out from the external site and returns to Finance and Operations.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">回发消息是当用户从外部站点签出并返回到 Finance and Operations 时从供应商收到的消息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Post back messages can’t be configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">回发消息不能进行配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>The messages are based on the cXML protocol definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此消息基于 cXML 协议定义。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source> Here is the information that can be part of the post back message that is received on a requisition line:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下信息可以是在申请行中收到的回发信息的一部分：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Message received from vendor</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">从供应商接收的消息</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Copied to requisition line in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">复制到 Finance and Operations 中的申请行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>&lt; ItemIn quantity=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemIn quantity=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Quantity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数量</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>&lt; ItemIn&gt;&lt; ItemID &gt;&lt; SupplierPartID &gt;&lt; /SupplierPartID &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemIn&gt;&lt; ItemID &gt;&lt; SupplierPartID &gt;&lt; /SupplierPartID &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>External item ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部物料 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>&lt; ItemDetail&gt;&lt; UnitPrice &gt;&lt; Money currency=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail&gt;&lt; UnitPrice &gt;&lt; Money currency=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">币种</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>&lt; ItemDetail &gt;&lt; UnitPrice &gt;&lt; Money &gt;&lt; /Money &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; UnitPrice &gt;&lt; Money &gt;&lt; /Money &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Unit price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">单价</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>&lt; ItemDetail &gt;&lt; Description ShortName=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Description ShortName=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Product name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">产品名称</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>&lt; ItemDetail &gt;&lt; Description &gt;&lt; /Description &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Description &gt;&lt; /Description &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Included in item description; Product name if ShortName is not specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">包含在物料描述中；产品名称，如果未指定 ShortName。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>&lt; ItemDetail &gt;&lt; UnitOfMeasure &gt;&lt; /UnitOfMeasure &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; UnitOfMeasure &gt;&lt; /UnitOfMeasure &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">单位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>&lt; ItemDetail &gt;&lt; Classification &gt;&lt; /Classification &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Classification &gt;&lt; /Classification &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Included in item description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">包含在物料描述中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>&lt; ItemDetail &gt;&lt; Classification domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Classification domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Included in item description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">包含在物料描述中</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Delete an external catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">删除外部目录</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Delete an external catalog with the Delete action on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">删除页面上具有删除操作的外部目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If a product from the external vendor catalog has been requested, the external vendor catalog cannot be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果从外部供应商的目录请求产品，不能删除外部供应商目录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Instead, the status of the external vendor catalog is set to inactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">相反，外部供应商目录的状态被设置为无效。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>If you want to remove access to the external vendor’s catalog site, but not delete it, change the external catalog status to Inactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果您要取消对外部供应商的目录站点的访问，但是不删除它，请将外部目录的状态更改为无效。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>