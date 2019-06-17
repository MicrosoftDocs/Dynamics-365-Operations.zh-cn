<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">改进了批量跟踪物料的处理</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">此主题介绍了对零售对帐单过帐驱动程序流程中批量跟踪物料的批次处理所做的改进。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">改进了批量跟踪物料的处理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="0" state="translated">在 Microsoft Dynamics 365 for Retail 销售点 (POS) 中，无法在销售时捕获批量跟踪物料的批处理号。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">但是，对于特定配置，在总部通过客户订单或对帐单过帐来过帐销售额时，Microsoft Dynamics 系统要求批量跟踪物料具备有效的批处理号，这些编号在开票流程中使用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">如果有效的批处理号对产品可用，则来自对帐单过帐的客户订单开票流程和销售订单开票流程使用这些编号。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">否则，客户订单开票流程无法过帐，POS 用户将收到错误消息。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">对帐单过帐随后会进入错误状态。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">即使为产品启用了负库存，也会出现此错误状态。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="0" state="translated">在 Microsoft Dynamics for Retail 版本 10.0.4 和更高版本中进行的改进可帮助确保在为批量跟踪物料启用了负库存时，如果库存为 0（零）或者批处理号不可用，不会阻止这些物料通过对帐单过帐进行客户订单开票和销售订单开票。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">批处理号不可用时，新功能会使用销售行的默认批处理 ID。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="0" state="translated">要定义为客户订单使用的默认批处理 ID，请在<bpt id="p1">**</bpt>零售参数<ept id="p1">**</ept>页面的<bpt id="p2">**</bpt>客户订单<ept id="p2">**</ept>选项卡上，在<bpt id="p3">**</bpt>订单<ept id="p3">**</ept>快速选项卡中设置<bpt id="p4">**</bpt>默认批处理 ID<ept id="p4">**</ept> 字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">要定义为通过对帐单过帐进行的销售订单开票使用的默认批处理 ID，请在<bpt id="p1">**</bpt>零售参数<ept id="p1">**</ept>页面的<bpt id="p2">**</bpt>过帐<ept id="p2">**</ept>选项卡上，在<bpt id="p3">**</bpt>库存更新<ept id="p3">**</ept>快速选项卡中设置<bpt id="p4">**</bpt>默认批处理 ID<ept id="p4">**</ept> 字段。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">只有为特定商店仓库和物料启用了高级仓储时，此功能才可用。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">在以后的版本中，未使用高级仓库管理的方案也将支持此功能。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>