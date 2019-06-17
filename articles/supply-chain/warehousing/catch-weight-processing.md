<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="catch-weight-processing.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>catch-weight-processing.d3ca7d.6e295456838ca0195a472518b5979dfdc7819f74.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6e295456838ca0195a472518b5979dfdc7819f74</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\warehousing\catch-weight-processing.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Catch weight product processing with warehouse management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用仓库管理进行实际称重产品处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to use work templates and location directives to determine how and where work is done in the warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本主题介绍如何使用工作模板和库位指令确定在仓库中如何以及在哪里完成工作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Catch weight product processing with warehouse management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用仓库管理进行实际称重产品处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Feature exposure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">功能曝光</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To use warehouse management to process catch weight products, you must use a license configuration key to turn on the functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要使用仓库管理处理实际称重产品，必须使用许可证配置键打开功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>(Go to <bpt id="p1">**</bpt>System administration <ph id="ph1">\&gt;</ph> Setup <ph id="ph2">\&gt;</ph> License configuration<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">（转到<bpt id="p1">**</bpt>系统管理 <ph id="ph1">\&gt;</ph> 设置 <ph id="ph2">\&gt;</ph> 许可证配置<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Then, on the <bpt id="p1">**</bpt>Configuration keys<ept id="p1">**</ept> tab, expand <bpt id="p2">**</bpt>Trade <ph id="ph1">\&gt;</ph> Warehouse and Transportation management<ept id="p2">**</ept>, and select the check box for <bpt id="p3">**</bpt>Catch weight for warehouse<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">然后，在<bpt id="p1">**</bpt>配置键<ept id="p1">**</ept>选项卡上，展开<bpt id="p2">**</bpt>贸易 <ph id="ph1">\&gt;</ph> 仓库和运输管理<ept id="p2">**</ept>，然后选择<bpt id="p3">**</bpt>面向仓库的实际称重<ept id="p3">**</ept>复选框）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Both the <bpt id="p1">**</bpt>Warehouse and Transportation management<ept id="p1">**</ept> license configuration key and the <bpt id="p2">**</bpt>Process distribution <ph id="ph1">\&gt;</ph> Catch weight<ept id="p2">**</ept> license configuration keys must also be turned on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">还必须打开<bpt id="p1">**</bpt>仓库和运输管理<ept id="p1">**</ept>许可证配置键和<bpt id="p2">**</bpt>流程分配 <ph id="ph1">\&gt;</ph> 实际称重<ept id="p2">**</ept>许可证配置键。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>After the license configuration key is turned on, when you create a released product, you can select <bpt id="p1">**</bpt>Catch weight<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在许可证配置键打开后，在您创建已发放产品时，您可以选择<bpt id="p1">**</bpt>实际称重<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can also associate the released product with a storage dimension group that the <bpt id="p1">**</bpt>Use warehouse management processes<ept id="p1">**</ept> parameter is selected for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您还可以将发放的产品与为其选择了<bpt id="p1">**</bpt>使用仓库管理流程<ept id="p1">**</ept>参数的存储维度组关联。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Before you can use the product in Warehouse management, you must do some basic product-specific setup for catch weight:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您必须为实际称重进行某些基本产品的特定设置，然后才可以在“仓库管理”中使用产品：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Define the nominal weight conversion between the catch weight unit (box) and the inventory unit (kilogram <ph id="ph1">\[</ph>kg<ph id="ph2">\]</ph>) as part of a unit conversion definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在单位转换定义中定义实际称重单位（箱）和库存单位（千克）<ph id="ph1">\[</ph>kg<ph id="ph2">\]</ph> 之间的标称重量转换。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Define the minimum and maximum weight tolerances as part of the catch weight unit setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在实际称重单位设置中，定义最小和最大重量容差。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up a unit sequence group where the catch weight unit is defined as the lowest stock keeping unit (SKU).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置实际称重单位定义为最低库存单位 (SKU) 的单位序列组。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Set up a catch weight item handling policy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置实际称重物料处理策略。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Setting up and maintaining catch weight items<ept id="p1">](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有关详细信息，请参阅<bpt id="p1">[</bpt>设置和维护实际称重物料<ept id="p1">](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Transaction adjustments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">交易记录调整</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Because the weight of inventory when it comes into a warehouse can differ from the weight when the inventory is issued out of the warehouse, the catch weight product processing must adjust the inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">由于库存重量在涉及到仓库时可能不同于库存从仓库发放时的重量，所以实际称重产品处理必须调整库存。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Example 1<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>示例 1<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>During a <bpt id="p1">**</bpt>Report as finished<ept id="p1">**</ept> production process, the inbound weight of a license plate that contains eight boxes of a catch weight product is captured as 80.1 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在<bpt id="p1">**</bpt>完工入库<ept id="p1">**</ept>生产流程中，包含八箱实际称重产品的牌照的进货重量捕获为 80.1 千克。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The license plate is then stored away in the finished goods area, and during the storage period, some weight is lost into the air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">牌照之后存储在成品区域，存储期间，部分重量在空气中流失。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Later, as part of a sales order picking process, the weight of the same license plate is captured as 79.8 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">之后，在销售订单领料流程中，同一个牌照的重量捕获为 79.8 千克。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Therefore, in the system, you now have a weight difference as part of the physical dimension set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">因此，在系统中，您现在在物理维度设置中将有重量差异。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In this case, the system automatically adjusts the difference by posting a transaction for the missing 0.3 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在这种情况下，系统将通过过帐缺少的 0.3 千克的交易记录来自动调整此差异。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Example 2<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>示例 2<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In its definition, a product is set up to tolerate a minimum weight of 8 kg and a maximum weight of 12 kg for the <bpt id="p1">**</bpt>Box<ept id="p1">**</ept> catch weight unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在其定义中，产品被设置为最多允许<bpt id="p1">**</bpt>箱<ept id="p1">**</ept>实际称重单位的最小 8 千克重量、最大 12 千克重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You have two boxes of the product, and they have a registered weight of 16 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您有两箱产品，它们登记的重量为 16 千克。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If a warehouse worker picks and weighs one of the boxes, and the weight is captured as 9 kg, the remaining box will weigh 7 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果仓库工作人员领取其中一箱并称重，重量捕获为 9 千克，另一箱重量将为 7 千克。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>However, because 7 kg is below the minimum weight, the system does an automatic adjustment to increase the weight of the on-hand inventory by 1 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">但是，因为 7 千克低于最小重量，系统将执行自动调整，将现有库存重量增加 1 千克。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>To set up the accounts that these adjustments are posted to, go to <bpt id="p1">**</bpt>Cost management <ph id="ph1">\&gt;</ph> Ledger integration policies setup <ph id="ph2">\&gt;</ph> Posting<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要设置这些调整所过帐到的科目，请转到<bpt id="p1">**</bpt>成本管理 <ph id="ph1">\&gt;</ph> 分类帐集成策略设置 <ph id="ph2">\&gt;</ph> 过帐<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Then, on the <bpt id="p1">**</bpt>Inventory<ept id="p1">**</ept> tab, define the following accounts:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">然后，在<bpt id="p1">**</bpt>库存<ept id="p1">**</ept>选项卡上，定义以下科目：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Catch weight loss account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重损失科目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Catch weight profit account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重利润科目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Catch weight item handling policy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重物料处理策略</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The catch weight item handling policy defines two primary warehouse management flows for the items: when the weight of the items is captured, and how it's captured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重物料处理策略定义物料的两个主要仓库管理流程：何时捕获物料重量，以及如何捕获。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can define when the weight is captured for sales and transfer order processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您可以定义什么时候为销售和转移单处理捕获重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The weight can be captured during either of the following processes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重量可以在以下流程的任意一个流程期间捕获：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Picking<ept id="p1">**</ept> – The weight is captured during the initial pick work lines of order work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>领料<ept id="p1">**</ept> – 重量在订单工作的初始领料工作行期间捕获。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Packing<ept id="p1">**</ept> – The weight is captured during manual packing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>装箱<ept id="p1">**</ept> – 重量在人工装箱期间捕获。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>(You must send the items to a packing station.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">（必须将物料发送到装箱工作站。）</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If the actual weight is captured at the packing station during the container packing processes, warehouse workers won't be prompted to capture the weight during picking work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果实际重量在集装箱装箱流程期间在装箱工作站捕获，在领料工作期间，将不提示仓库工作人员捕获重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Instead, the average weight of the physical inventory will be used as the weight of the picked inventory that goes to the packing area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">物理库存的平均重量将被用作转到装箱区域的已领取库存的重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For internal warehouse management processes like counting and adjustment corrections it is possible to define if the weight should be captured or not.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于内部仓库管理流程，如盘点和调整更正，可以定义重量是否应捕获。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If not captured the nominal weight will be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果未捕获，将使用标称重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can also define how the weight is captured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">您还可以定义如何捕获重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In one of the two main flows, catch weight tags are tracked and used to capture the weight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在两个主要流之一，实际称重标记被跟踪并用于捕获重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the other flow, catch weight tags aren't tracked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在另一个流中，不跟踪实际称重标记。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> – The item uses catch weight tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>是<ept id="p1">**</ept> – 物料使用实际称重标记。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Each tag number represents one catch weight unit (box), and a weight and other information are associated with the tag.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">每个标记编号表示一个实际称重单位（箱），重量以及其他信息与标记关联。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>For outbound processes, the weight that is associated with the tag is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于出货流程，使用与标记关联的重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>No<ept id="p1">**</ept> – The item doesn't use catch weight tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>否<ept id="p1">**</ept> – 物料不使用实际称重标记。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The inbound and outbound weighing processes are based on the actual weight that is captured during each process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">进货和出货称重流程基于在每个流程中捕获的实际重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The process of tracking catch weight tags can be used for items that won't change weight during the storage period.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">跟踪实际称重标记的流程可以用于存储期间不会更改重量的物料。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The weight will be captured only during the inbound warehouse process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重量将仅在进货仓库流程中捕获。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>During the outbound process, the catch weight tags will just be scanned, and the weights that are associated with the tags will be used for the outbound transactional processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在出货流程中，将只扫描实际称重标记，与这些标记关联的重量将用于出货交易处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>How to capture catch weight</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果捕获实际称重</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>When catch weight tag tracking is used, a tag must always be created for every catch weigh unit that is received, and every tag must always be associated with a weight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在使用实际称重标记跟踪时，必须始终为收到的每个实际称重单位创建标记，并且每个标记必须始终与重量关联。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For example, <bpt id="p1">**</bpt>Box<ept id="p1">**</ept> is the catch weight unit, and you receive one pallet of eight boxes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例如，<bpt id="p1">**</bpt>箱<ept id="p1">**</ept>是实际称重单位，您将收到一个托盘（八箱）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In this case, eight unique catch weight tags must be created, and a weight must be associated with each tag.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在这种情况下，必须创建八个唯一的实际称重标记，并且重量必须与每个标记关联。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Depending on the inbound catch weight tag, either the weight of all eight boxes can be captured, and the average weight can then be distributed to each box, or a unique weight can be captured for each box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">根据进货实际称重标记，可以捕获全部八箱的重量，然后可以将平均重量分配到每箱，也可以为每箱捕获唯一重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>When catch weight tag tracking isn't used, the weight can be captured for each dimension set (for example, for each license plate and tracking dimension).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在不使用实际称重标记跟踪时，可以针对每个维度集捕获重量（例如，对每个牌照和跟踪维度）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Alternatively, the weight can be captured based on an aggregated level, such as five license plates (pallets).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">或者，重量可以基于聚合级别捕获，如五个牌照（托盘）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>For the methods for capturing outbound weight, you can define whether the weighing is done for each catch weight unit (that is, per box), or whether the weight is captured based on the quantity that will be picked (for example, three boxes).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于捕获出货重量的方法，您可以定义是否为每个实际称重单位（即每箱）进行称重，或是否基于将要领取的数量（例如，三箱）捕获重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Note that for the production line picking and internal movement processes, the average weight will be used if the <bpt id="p1">**</bpt>Not captured<ept id="p1">**</ept> option is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请注意，对于生产订单行领料和内部移动流程，如果使用了<bpt id="p1">**</bpt>未捕获<ept id="p1">**</ept>选项，将使用平均重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>To restrict the warehouse management picking processes from capturing weights resulting in catch weight profit/loss adjustments, the Outbound weight variance method can be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要限制仓库管理领料流程捕获会产生实际称重损/益调整的重量，可使用出货重量差异方法。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Supported scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支持的方案</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Not all workflows support catch weight product processing with warehouse management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">并非所有工作流都支持使用仓库管理进行实际称重产品处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The following restrictions currently apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当前应用以下限制。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Configuring catch weight products for warehouse management processes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">针对仓库管理流程配置实际称重产品</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For catch weight products, the storage dimension group for items can't be changed (so that warehouse management processes can be used for them).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于实际称重产品，物料的存储维度组不能更改（以便仓库管理流程可用于它们）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Only formula processing is supported for catch weight products (not bill of materials).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品（不是物料清单）仅支持配方处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Catch weight products can't be associated with a tracking dimension group by using the Owner dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不能使用所有者维度与跟踪维度组关联。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Catch weight products can't be used as services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不能作为服务使用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Catch weight products can be used as "stocked products" only as part the item model group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品只能作为物料模型组的一部分用作“贮存产品”。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Catch weight products can't be used together with the functionality for tracking "Active in sales process."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不能与此功能一起用于跟踪“在销售流程中有效”。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Catch weight products can't be used together with the functionality for capturing serial numbers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不能与此功能一起用于捕获序列号。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Therefore, products can't be transferred from a "blank" to a serial number as part of the picking/packing process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">因此，产品不能作为领料/装箱流程的一部分从“空白”转为序列号。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Catch weight products can't be used together with the functionality for registering serials before consumption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不能与此功能一起用于在消耗前登记序列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Catch weight products that are variant-enabled can't be used together with the functionality for converting variant units of measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">启用变量的实际称重产品不能与此功能一起用于转换不同的度量单位。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Catch weight products can't be marked as a retail "product kit."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不能标记为零售“产品配套件”。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Catch weight products can be used only with a unit sequence group that has catch weight handling units, and that has the catch weight unit as the lowest sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品只能与具有实际称重处理单位且将实际称重单位作为最低序列的单位序列组一起使用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>For catch weight products, the inventory unit can be converted to the catch weight unit only if the conversion produces a nominal quantity that is more than 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于实际称重产品，只有当转换生成大于 1 的标准数量时，库存单位才可以转换为实际称重单位。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The setup of bar codes for catch weight products doesn't support a variable weight setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品的条码设置不支持可变重量设置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Order processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">订单处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The creation of advance ship notice (ASN/packing structures) doesn't support weight information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">发货通知（ASN/装箱结构）的创建不支持重量信息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The order quantity must be maintained based on the catch weight unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">订单数量必须基于实际称重单位维护。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Inbound warehouse processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">进货仓库处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Receiving license plates requires that weights be assigned during registration, because weight information isn't supported as part of the advance ship notice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接收牌照需要重量在登记时分配，因为重量信息不支持作为发货通知的一部分。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When catch weight tag processes are used, the tag number must be manually assigned per catch weight unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在使用实际称重标记流程时，标记编号必须按实际称重单位手动分配。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Inventory and warehouse operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">库存和仓库操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Manual creation of quarantine orders isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持手动创建检验单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Manual movement of inventory that is related to work isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持手动移动与工作相关的库存。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Consolidation of license plates isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持合并牌照。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>License plate loading to initialize warehouse stock isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持加载来初始化仓库库存的牌照。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Batch balancing processes aren't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持批次平衡流程。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Handling of negative physical inventory isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持处理负实际库存。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Inventory marking can't be used for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">库存标记不能用于实际称重产品。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Outbound warehouse processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出货仓库处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The functionality for cluster picking isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持群集领料功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Pick and pack warehouse processing isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持领料和装箱仓库处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For catch weight products, work that is defined in a work template can be run automatically.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">对于实际称重产品，在工作模板中定义的工作可以自动运行。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The functionality for reversing work isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持冲销工作功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For catch weight products, manual packing station processing where work is created after containers are closed isn't supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于实际称重产品，不支持在集装箱关闭后创建工作的手动装箱工作站处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The functionality for pcs-by-pcs scanning isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持逐件扫描功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Production processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生产处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>For catch weight products, only batch orders for formula products are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于实际称重产品，仅支持配方产品的批次订单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Kanban functionality isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持看板功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For catch weight products, serial numbers can't be registered before consumption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于实际称重产品，序列号不能在消耗前登记。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The functionality for reversing license plates isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持冲销牌照功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For catch weight products, reporting as finished cannot be registered by serial number.</source><target logoport:matchpercent="94" state="translated" state-qualifier="x-fuzzy-match-unedited">对于实际称重产品，完工入库可通过序列号注册。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Transportation management processing</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">运输管理处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Load building workbench processing isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持装载计划工作台处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Transport request lines aren't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重产品不支持运输请求行。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Other restrictions and behaviors for catch weight product processing with warehouse management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用仓库管理的实际称重产品处理的其他限制和行为</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>During picking processes where the user isn't prompted to identify tracking dimensions, the weight assignment is done based on the average weight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在没有提示用户标识跟踪维度的领料流程中，重量分配基于平均重量进行。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>This behavior occurs when, for example, a combination of tracking dimensions is used in the same location and, after a user processes picking, only one tracking dimension value is left in the location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例如，此行为在以下情况下发生：在同一位置使用跟踪维度组合，并且在用户处理领料后，该位置只剩一个跟踪维度值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>When inventory is reserved for a catch weight product that is configured for warehouse management processes, the reservation is done based on the minimum weight that is defined, even if this quantity is the on-hand last handling quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在库存为针对仓库管理流程配置的实际称重产品预留时，预留将基于定义的最小重量进行，即使此数量是现有的最后一个处理数量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>This behavior differs from the behavior for items that aren't configured for warehouse management processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此行为与未为仓库管理流程配置的物料的行为不同。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Processes that use the weight as part of capacity calculations (wave thresholds, work maximum breaks, container maximums, location load capacities, and so on) don't use the actual weight of the inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将重量作为产能计算（波次阈值、工作最大休息时间、集装箱最大数、库位负荷产能等）的一部分使用的流程不使用库存的实际重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Instead, the processes are based on the physical handling weight that is defined for the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">流程基于为产品定义的实际处理重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In general, Retail functionality isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常，实际称重产品不支持零售功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Catch weight tags</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">实际称重标记</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Currently, the functionality for catch weight tags is supported only as part of the following scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目前，实际称重标记的功能仅作为以下方案的一部分支持：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>When processing purchase order warehouse app receiving.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当处理采购订单仓库应用接收时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>When processing load receiving via warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当通过仓库应用处理负荷接收时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>For license plate receiving that is related to a purchase order load, weight assignment is requested during the receiving process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于与采购订单负荷相关的牌照接收，重量分配在接收流程中请求。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>By contrast, for transfer order receiving, the weight from the shipment data for the transfer order is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">相对而言，对于转移单接收，将使用转移单的装运数据中的重量。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>For transfer order item and line receiving that comes from a non-warehouse management process warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于来自非仓库管理流程仓库的转移单物料和行接收。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The processing of sales return order receiving can record catch weight tags, but the processing won't be validated if the tags are the same tags that were originally shipped for a particular sales order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">销售退货单接收的处理可以记录实际称重标记，但如果标记是最初为特定销售订单行装运的相同标记，则不会验证处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>When processing a inventory status changed by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在使用仓库应用处理更改的库存状态时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>When a warehouse transfer is done by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在使用仓库应用完成仓库转移时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>When processing adjustment in and out via the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在通过仓库应用处理调入和调出时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>When picking work is processed for sales and transfer orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在为销售订单和转移单处理领料工作时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>(Note that catch weight tags can't be recorded for production component picking.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">（请注意，实际称重标记不能为生产组件领料记录。）</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>When picked quantities are reduced from load lines, regardless of whether containers are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在减少负荷行的领料数量时（不管是否使用集装箱）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>When products are packed into containers at a packing station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当产品在装箱工作站装入集装箱时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>When containers are reopened.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在重新打开集装箱时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>When formula products are reported as finished by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当配方产品使用仓库应用完工入库时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>When transport loads are processed by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在使用仓库应用处理运输负荷时。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>A catch weight tag can either be created using a warehousing app process, manually created in the form, or creating using a data entity process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可以使用仓库应用流程创建，在窗体中手动创建或使用数据实体流程创建实际称重标记。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If a catch weight tag gets associated with an inbound source document line, such as purchase order line, the tag will be registered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果实际称重标记与入货源文档行（如采购订单行）关联，将注册此标记。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>If the line is used for outbound processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果该行用于出货处理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>The tag will be updated as shipped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将把该标记更新为已装运。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>