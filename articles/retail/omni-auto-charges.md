<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全渠道高级自动费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此主题描述使用高级自动费用功能管理零售渠道订单的额外订单费用的功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全渠道高级自动费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此主题提供有关 Dynamics 365 for Retail 版本 10.0 中提供的高级自动费用功能的配置与部署的信息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在高级自动费用功能启用时，在任何支持的零售渠道（销售点 (POS)、呼叫中心和在线）中创建的订单均可以利用在 ERP 应用程序中为标题和行级别相关费用中定义的<bpt id="p1">[</bpt>自动费用<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept>配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在 Dynamics 365 for Retail 版本 10.0 之前的版本中，<bpt id="p1">[</bpt>自动费用<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept>配只能由在电子商务和呼叫中心渠道创建的订单访问。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在版本 10.0 及以后版本中，POS 创建的订单可以利用自动费用配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这样，额外的杂项费用可以系统化地添加到销售交易记录中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在使用版本 10.0 以前的版本时，将提示 POS 用户在创建“全部装运”或“装运所选产品”POS 交易记录期间手动输入装运费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">当应用程序的杂项费用功能用于与费用如何写入到订单的相关情况时，将不提供系统计算 - 计算依赖于用户的输入来确定费用值。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">费用只能添加为一个“装运”相关费用代码，且不能在创建后在 POS 中轻松编辑或更改。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用手动提示添加装运费用在版本 10.0 及以后版本中仍然可用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果组织不启用<bpt id="p1">**</bpt>高级自动费用<ept id="p1">**</ept>参数，手动输入费用的 POS 提示将保持相同。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用高级自动费用功能，POS 用户可以根据自动费用设置表系统化地计算所有定义的杂项费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">而且，用户将能够在标题或行级别的任何 POS 销售交易记录中添加或编辑无限制的额外费用金额（对于现金和结转或客户订单）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">启用高级自动费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">在 <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> 总部设置 <ph id="ph2">\&gt;</ph> 参数 <ph id="ph3">\&gt;</ph> 零售参数<ept id="p1">**</ept>页，转到<bpt id="p2">**</bpt>客户订单<ept id="p2">**</ept>选项卡。在<bpt id="p3">**</bpt>费用<ept id="p3">**</ept>快速选项卡上，将<bpt id="p4">**</bpt>使用高级自动费用<ept id="p4">**</ept>设置为<bpt id="p5">**</bpt>是<ept id="p5">**</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高级自动费用参数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在高级自动费用启用时，在创建全部装运或装运所选产品客户订单时，不再提示用户在 POS 终端中手动输入费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 订单费用被系统化地计算并添加到 POS 交易记录（如果找到与正在创建的订单的条件匹配的对应的自动费用表）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用户还可以通过可以添加到 POS 屏幕布局的新添加的 POS 操作手动添加或维护标题或行级别费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在高级自动费用启用时，不再使用<bpt id="p2">**</bpt>装运费用代码<ept id="p2">**</ept>和<bpt id="p3">**</bpt>退回装运费用<ept id="p3">**</ept>的现有<bpt id="p1">**</bpt>零售参数<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仅当<bpt id="p1">**</bpt>使用高级自动费用<ept id="p1">**</ept>参数设置为<bpt id="p2">**</bpt>否<ept id="p2">**</ept>时这些参数才适用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在启用此功能前，请确保您已测试并对员工进行了培训，因为这将更改装运或其他费用如何计算并添加到 POS 销售订单的业务流程。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">确保您了解此流程对从 POS 创建交易记录的影响。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于呼叫中心和电子商务订单，启用高级自动费用的影响是最小的。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在与计算额外订单费用的自动费用表相关的行为方面，呼叫中心和电子商务应用程序将继续具有以前所有的相同行为。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼叫中心渠道用户将继续能够手动编辑标题或行级别的所有系统计算出的自动费用，或者在标题或行级别手动添加额外杂项费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">其他 POS 操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">为使高级自动费用能够在您的 POS 应用程序环境中正常工作，新 POS 操作已添加。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在部署高级自动费用时，这些操作必须添加到 <bpt id="p1">[</bpt>POS 屏幕布局<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>并部署到 POS 设备。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果这些操作未添加，用户将无法在 POS 交易记录中管理或维护杂项费用，且没有办法调整或更改基于自动费用配置系统化计算的费用值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">至少，建议您将<bpt id="p1">**</bpt>管理费用<ept id="p1">**</ept>操作部署到您的 POS 布局。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">新操作如下所示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>142 - 管理费用<ept id="p1">**</ept> - 使用此操作允许 POS 用户查看和编辑通过自动费用计算手动或系统添加的 POS 交易记录的杂项费用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>141 - 添加标题费用<ept id="p1">**</ept> - 使用此操作为用户提供将标题级别杂项费用手动添加到任何 POS 销售交易记录的能力（以及选择要使用的费用代码）。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>140 - 添加行费用<ept id="p1">**</ept> - 使用此操作为用户提供将行级别杂项费用手动添加到任何 POS 销售交易记录行的能力（以及选择要使用的费用代码）。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>143 - 重新计算费用<ept id="p1">**</ept> - 使用此操作执行销售交易记录费用的完全重新计算。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先前用户覆盖的任何自动费用都将根据当前的配置重新计算。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">与 POS 操作一样，可以进行安全配置来需要经理审批才能执行操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请务必注意，即使禁用了<bpt id="p1">**</bpt>使用高级自动费用<ept id="p1">**</ept>参数，也可以将上面列出的 POS 操作添加到 POS 布局。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在此情况下，组织仍然可以享受查看手动添加的费用和使用<bpt id="p1">**</bpt>管理费用<ept id="p1">**</ept>操作编辑这些费用带来的优势。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">即使禁用了<bpt id="p3">**</bpt>使用高级自动费用<ept id="p3">**</ept>参数，用户也可以为 POS 交易记录使用<bpt id="p1">**</bpt>添加标题费用<ept id="p1">**</ept>和<bpt id="p2">**</bpt>添加行费用<ept id="p2">**</ept>操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果在禁用了<bpt id="p2">**</bpt>使用高级自动费用<ept id="p2">**</ept>时使用<bpt id="p1">**</bpt>重新计算费用<ept id="p1">**</ept>操作，该操作的功能将减少。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在此情况下，将不重新计算任何内容，并且手动添加到交易记录的所有费用都将重置为 $0.00。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用例示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在此部分，将呈现示例用例以帮助您了解零售渠道订单上下文内自动费用和杂项费用的配置和使用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这些示例说明在启用了<bpt id="p1">**</bpt>使用高级自动费用<ept id="p1">**</ept>参数时应用程序的行为。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自动费用标题费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用例场景</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商要在需要向客户装运产品的任何零售渠道中创建交易记录时自动添加运费。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商提供 2 种交货方式：陆运和空运。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果客户选择陆运，并且订单值少于 100 美元，零售商希望向客户收取 10.00 美元运费。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果订单值超过 100 美元，并且客户选择陆运，客户将不会被收取任何额外的运费。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果客户为所有订单选择空运交货方式，不论订单总值是多少，其将被收取运费 20.00 美元。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置和配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此场景需要配置两个自动费用表。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">转到<bpt id="p1">**</bpt>应收帐款 <ph id="ph1">\&gt;</ph> 费用设置 <ph id="ph2">\&gt;</ph> 自动费用<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置两个不同的标题级别自动费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一个为“陆运模式”交货配置，一个为“空运模式”交货配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于此场景，请配置它们以用于“所有客户”。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于陆运费用，在<bpt id="p1">**</bpt>自动费用<ept id="p1">**</ept>页的行部分，将 0.01 美元到 100 美元之间的订单要应用的费用定义为 10.00 美元。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">创建另一个费用行来指示超过 100.01 美元的订单没有费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自动费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于空运费用，在自动费用窗体的行部分，定义将应用于所有订单（值为 0.01 美元到 9,999,999 美元）的 20.00 美元费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将更改发送到 Retail Server/通道 DB，以便 POS 可以通过运行 <bpt id="p1">**</bpt>1040 配送计划<ept id="p1">**</ept>作业使用它们。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此场景的销售处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在上述配置步骤已完成，并且更改已应用到通道数据库后，在标题级别设置了陆运或空运方式的在 POS、呼叫中心或电子商务渠道创建的任何客户订单或销售交易记录都将使用这些费用并自动将它们应用到销售中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此时，费用将应用于在利用这些交货方式的法人内创建的所有销售交易记录，因为没有指定自动费用配置将只应用于特定销售渠道的功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于 POS 和电子商务场景，因为未在这些订单中明晰定义“标题”，仅当交易记录中的所有销售行均被设置为使用完全相同的交货方式装运时才应用标题级别费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果 POS 或电子商务创建的交易记录中存在“混合模式”履行，将仅考虑并应用行级别自动费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在呼叫中心场景中，用户控制订单标题的交货方式的设置，因此标题级别费用将为这些订单应用，即使某些销售订已配置为使用不同的交货方式。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼叫中心订单的标题级别费用将始终基于在销售订单的订单标题级别定义的交货方式。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自动费用行费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用例场景</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商想要在客户购买特定计算机型号时将额外费用添加到客户以收取设置费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此计算机需要零售商将为客户执行的额外的非可选设置操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商已通知客户将存在此设置的额外费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出于财务申报目的，零售商希望将与此费用相关的费用与产品销售价分开单独管理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当此特定计算机在任何零售渠道购买时，客户将被收取 19.99 美元的设置费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置和配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此场景需要配置一个行级别自动费用表。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">转到<bpt id="p1">**</bpt>应收帐款 <ph id="ph1">\&gt;</ph> 费用设置 <ph id="ph2">\&gt;</ph> 自动费用<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将<bpt id="p1">**</bpt>级别<ept id="p1">**</ept>下拉菜单设置为<bpt id="p2">**</bpt>行<ept id="p2">**</ept>，然后为要收取设置费用的特定产品或产品组的所有客户创建新的自动费用记录。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自动费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将费用发送到 Retail Server/通道 DB，以便 POS 可以通过运行 <bpt id="p1">**</bpt>1040 配送计划<ept id="p1">**</ept>作业使用它们。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此场景的销售处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在上述配置步骤已完成，并且更改已应用到通道数据库后，在订单中有此项目的在 POS、呼叫中心或电子商务渠道创建的任何客户订单或销售交易记录都将触发将系统地添加到订单合计的行级别费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此时，费用将应用于与法人内的行级别自动费用配置匹配的任何销售行，因为没有将行级别自动费用配置为只应用于特定销售渠道的功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手动标题费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用例场景描述</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商通过向在商店内订购产品的客户提供特殊的产品家庭交货方式，为典型流程设置了例外。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商和客户已同意客户将为此服务支付额外 25 美元的手续费。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">订单接受者需要将此额外费用添加到交易记录中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">由于此费用是总费用且与订单上的任何一个产品都无关，将使用标题费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置和配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">确保将此场景中使用的费用代码已正确配置，方法是转到<bpt id="p1">**</bpt>应收帐款 <ph id="ph1">\&gt;</ph> 费用设置 <ph id="ph2">\&gt;</ph> 费用<ept id="p1">**</ept>为此场景定义适当的费用代码。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">如果由于装运相关的折扣或促销目的，费用应被视作“装运”相关费用，应将费用代码中的<bpt id="p1">**</bpt>装运费用<ept id="p1">**</ept>设置为<bpt id="p2">**</bpt>是<ept id="p2">**</ept>。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果在处理 POS 应用程序中的退货交易期间，此费用也被允许系统地退还，应将<bpt id="p1">**</bpt>可退还<ept id="p1">**</ept>设置为<bpt id="p2">**</bpt>是<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>可退还<ept id="p1">**</ept>标志仅在<bpt id="p2">**</bpt>使用高级自动费用<ept id="p2">**</ept>参数设置为<bpt id="p3">**</bpt>是<ept id="p3">**</ept>时适用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将费用发送到 Retail Server/通道 DB，以便 POS 可以通过运行 <bpt id="p1">**</bpt>1040 配送计划<ept id="p1">**</ept>作业使用它们。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>添加标题费用<ept id="p1">**</ept>操作必须在您的 <bpt id="p2">[</bpt>POS 屏幕布局<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>中配置，以使用户可从 POS 访问的按钮可以调用此操作（操作 141）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">屏幕布局的更改也必须通过分配计划功能分配到零售渠道。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手动标题费用的销售处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要在 POS 应用程序中执行此方案，POS 用户将照常创建销售交易记录，并将产品和所有其他配置添加到销售中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在收取付款前，用户应执行<bpt id="p1">**</bpt>添加标题费用<ept id="p1">**</ept>操作，这将提示用户选择费用代码并输入费用值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在用户完成流程后，此费用将作为标题级别费用添加到销售订单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此流程可以通过使用工具栏上的<bpt id="p2">**</bpt>销售<ept id="p2">**</ept>选项卡中的现有<bpt id="p1">**</bpt>费用<ept id="p1">**</ept>功能在呼叫中心应用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在<bpt id="p1">**</bpt>维护费用<ept id="p1">**</ept>页，用户可以将新费用行添加到订单头中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手动行费用示例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用例场景</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">客户请求将其销售订单中的 2 件商品（共 5 件）包装成礼品。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">零售商提供此可选服务的费用为每件商品 2.00 美元。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">订单接受者需要将这些费用添加到需要礼品包装的特定商品。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">设置和配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">确保将此场景中使用的费用代码已正确配置，方法是转到<bpt id="p1">**</bpt>应收帐款 <ph id="ph1">\&gt;</ph> 费用设置 <ph id="ph2">\&gt;</ph> 费用<ept id="p1">**</ept>为此场景定义适当的费用代码。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果由于装运相关的折扣或促销目的，费用应被视作“装运”相关费用，应将费用代码中的<bpt id="p1">**</bpt>装运费用<ept id="p1">**</ept>设置为<bpt id="p2">**</bpt>是<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果在处理 POS 应用程序中的退货交易期间，该费用也被允许系统地退还，应将<bpt id="p1">**</bpt>可退还<ept id="p1">**</ept>设置为<bpt id="p2">**</bpt>是<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>可退还<ept id="p1">**</ept>标志仅在<bpt id="p2">**</bpt>使用高级自动费用<ept id="p2">**</ept>参数设置为<bpt id="p3">**</bpt>是<ept id="p3">**</ept>时适用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将费用发送到 Retail Server/通道 DB，以便 POS 可以通过运行 <bpt id="p1">**</bpt>1040 配送计划<ept id="p1">**</ept>作业使用它们。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>添加行费用<ept id="p1">**</ept>操作必须在您的 <bpt id="p2">[</bpt>POS 屏幕布局<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>中配置，以使用户可从 POS 访问的按钮可以调用此操作（操作 140）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">屏幕布局的更改也必须通过分配计划功能分配到零售渠道。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手动行费用的销售处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要在 POS 应用程序中执行此方案，POS 用户将照常创建销售交易记录，并将产品和所有其他配置添加到销售中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在收取付款前，用户应选择将从 POS 物料列表显示应用费用的特定行，并执行<bpt id="p1">**</bpt>添加行费用<ept id="p1">**</ept>操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">系统将提示用户选择费用代码并输入费用值。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在用户完成流程后，此费用将被链接到行并作为行级别费用添加到订单合计。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果需要，用户可以重复此流程，将其他行费用添加到交易记录中的其他物料行。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同一流程可以通过使用<bpt id="p3">**</bpt>销售订单<ept id="p3">**</ept>页上<bpt id="p2">**</bpt>销售订单行<ept id="p2">**</ept>部分的<bpt id="p1">**</bpt>财务<ept id="p1">**</ept>下拉菜单下的“维护费用”功能在呼叫中心应用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这将打开<bpt id="p1">**</bpt>维护费用<ept id="p1">**</ept>页，用户在其中可以将新行的特定费用添加到交易记录中。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">附加功能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">编辑 POS 销售交易记录中的费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理费用<ept id="p1">**</ept>操作 (142) 应该添加到 <bpt id="p2">[</bpt>POS 屏幕布局<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>，以便用户可以查看和编辑或覆盖任何系统计算或手动计算的标题或行级别费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果未添加此操作，用户将无法调整 POS 交易记录中的费用值，也不能查看费用的详细信息，如与费用关联的费用代码的类型。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在 POS 中的<bpt id="p1">**</bpt>管理费用<ept id="p1">**</ept>页，用户可以查看标题和行级别费用详细信息。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用户可以使用此页提供的<bpt id="p1">**</bpt>编辑<ept id="p1">**</ept>功能对计费到特定费用行的金额进行更改。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在费用行被手动覆盖后，它将不会被系统地重新计算，除非用户发起<bpt id="p1">**</bpt>重新计算费用<ept id="p1">**</ept>操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果已在<bpt id="p2">**</bpt>零售参数<ept id="p2">**</ept>设置页面配置了<bpt id="p1">**</bpt>费用覆盖原因代码<ept id="p1">**</ept>，当费用已在 POS 应用程序中修改时，用户将被提示提供原因代码。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果已为覆盖的费用捕获了原因代码，还将提供新报表来查看和审核这些覆盖。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此报表可以在<bpt id="p1">**</bpt>零售 <ph id="ph1">\&gt;</ph> 查询和报表 <ph id="ph2">\&gt;</ph> 费用覆盖历史记录<ept id="p1">**</ept>中找到。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">退还 POS 退货交易记录中的费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果<bpt id="p1">**</bpt>使用高级自动费用<ept id="p1">**</ept>参数设置为<bpt id="p2">**</bpt>是<ept id="p2">**</ept>，<bpt id="p3">**</bpt>退回装运费用<ept id="p3">**</ept>的现有零售参数不再适用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要指示哪些费用应在使用高级自动费用时系统地退还给客户，请确保相关费用代码已在<bpt id="p2">**</bpt>费用代码<ept id="p2">**</ept>设置页面配置为<bpt id="p1">**</bpt>可退还<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请确保设置已通过分配计划处理同步到您的零售渠道数据库。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">退还退货单交易记录中的费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">费用不会系统地退还到在 Retail 中创建的<bpt id="p1">**</bpt>退货单<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在创建<bpt id="p2">**</bpt>退货单<ept id="p2">**</ept>时，用户需要选择<bpt id="p1">**</bpt>复制费用<ept id="p1">**</ept>选项。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果没有选择<bpt id="p1">**</bpt>复制费用<ept id="p1">**</ept>，原始销售交易记录中的费用将不自动退还。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果选择<bpt id="p1">**</bpt>复制费用<ept id="p1">**</ept>，所有费用将被复制到退货单，并且用户可以手动编辑或删除他们不希望退还的任何费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼叫中心退货单流程目前不认可<bpt id="p2">**</bpt>费用代码<ept id="p2">**</ept>设置中的<bpt id="p1">**</bpt>可退还<ept id="p1">**</ept>标志。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置 POS 收据以显示费用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">以下收据元素已添加到收据行和页脚以支持高级自动费用功能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>订单行装运费用<ept id="p1">**</ept> - 此行级别元素可用于概括已应用到销售订单行的特定费用代码。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">仅在<bpt id="p2">**</bpt>费用代码<ept id="p2">**</ept>页标记为<bpt id="p1">**</bpt>装运<ept id="p1">**</ept>费用的费用代码将在此处显示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>订单行其他费用<ept id="p1">**</ept> - 此行级别元素可用于概括已应用到销售订单行的任何非装运特定费用代码。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">这些是<bpt id="p2">**</bpt>费用代码<ept id="p2">**</ept>页上的<bpt id="p1">**</bpt>装运<ept id="p1">**</ept>标志未启用的费用代码。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>订单装运费用详细信息<ept id="p1">**</ept> - 此页脚级别元素显示应用到在<bpt id="p3">**</bpt>费用代码<ept id="p3">**</ept>设置页面上标记为<bpt id="p2">**</bpt>装运<ept id="p2">**</ept>费用的订单的费用代码的描述。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>订单装运费用<ept id="p1">**</ept> - 此页脚级别元素显示装运相关费用的美元金额。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>订单其他费用详细信息<ept id="p1">**</ept> - 此页脚级别元素显示应用到未标记为装运相关费用的订单的费用代码的描述。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>订单其他费用<ept id="p1">**</ept> - 此页脚级别元素显示与装运无关的其他费用的美元金额。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">建议组织也将自由文本字段添加到收据页脚，以便定义将概括费用的区域。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">防止费用在完成 POS 订单前计算</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">某些组织可能更愿意等待用户将所有销售订单行都添加到 POS 交易记录后再计算费用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要防止在物料添加到 POS 交易记录时计算费用，在商店使用的<bpt id="p2">**</bpt>功能配置文件<ept id="p2">**</ept>中打开<bpt id="p1">**</bpt>手动费用计算<ept id="p1">**</ept>参数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">启用此参数将需要 POS 用户在完成向 POS 交易记录添加产品时使用<bpt id="p1">**</bpt>计算合计<ept id="p1">**</ept>操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>计算合计<ept id="p1">**</ept>操作然后将触发计算订单头或行的任何自动费用（如果适用）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">费用覆盖报表</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果用户手动覆盖计算费用或向交易记录添加手动费用，则可在<bpt id="p1">**</bpt>费用覆盖历史记录<ept id="p1">**</ept>报表中审计这些数据。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可以从<bpt id="p1">**</bpt>零售 <ph id="ph1">\&gt;</ph> 查询和报表 <ph id="ph2">\&gt;</ph> 费用覆盖历史记录<ept id="p1">**</ept>访问此报表。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">请务必注意，此报表需要的数据是通过“P”分发计划作业从渠道数据库导入到 HQ 的。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">因此，此作业将商店交易记录输入导入到 HQ 中之前，此报表中可能不会立即包含有关仅在 POS 中执行的覆盖的信息。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>