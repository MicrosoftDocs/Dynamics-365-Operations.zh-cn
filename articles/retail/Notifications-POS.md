<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="Notifications-POS.md" target-language="zh-CN">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>Notifications-POS.74d2b9.6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\Notifications-POS.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Show order notifications in the point of sale (POS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在销售点 (POS) 中显示订单通知</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to enable order notifications in the point of sale and the notification framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此主题介绍如何在销售点和通知框架中启用订单通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Show order notifications in the point of sale (POS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在销售点 (POS) 中显示订单通知</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In the modern retail environment, store associates are assigned various tasks, such as helping customers, entering transactions, doing stock counts, and receiving orders in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在现代零售环境中，商店店员被分配了各种任务，例如帮助客户、输入交易记录、执行存货盘点以及在商店接收订单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The point of sale (POS) client provides a single application where associates can perform all these tasks and many others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">销售点 (POS) 客户端提供一个应用程序，可供店员执行所有这些任务和其他大量任务。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Because various tasks must be performed during the day, associates might have to be notified when something requires their attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">由于各种任务必须在当天执行，所以可能必须在需要店员注意时通知店员。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The notification framework in the POS helps by letting retailers configure role-based notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 中的通知框架可以提供帮助，方法是让零售商配置基于角色的通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In Microsoft Dynamics 365 for Retail with application update 5, these notifications can be configured only for POS operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在具有应用程序更新 5 的 Microsoft Dynamics 365 for Retail 中，这些通知仅可针对 POS 操作进行配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Currently, the system can show notifications only for order fulfillment operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">现在，系统只能显示有关订单履行操作的通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, because the framework is designed to be extensible, developers will eventually be able to write a notification handler for any operation and show the notifications for that operation in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">但是，由于该框架设计为可扩展，所以开发人员最终将可以编写有关任何操作的通知处理程序，并在 POS 中显示相应操作的通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Enable notifications for order fulfillment operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">启用用于订单履行操作的通知</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To enable notifications for order fulfillment operations, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要启用有关订单履行操作的通知，请执行以下步骤。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Operations<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">转至<bpt id="p1">**</bpt>零售<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>渠道设置<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS 设置<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>操作<ept id="p5">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Search for the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> operation, and select the <bpt id="p2">**</bpt>Enable notifications<ept id="p2">**</ept> check box for it to specify that the notification framework should listen to the handler for this operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">搜索<bpt id="p1">**</bpt>订单履行<ept id="p1">**</ept>操作，然后为其选中<bpt id="p2">**</bpt>启用通知<ept id="p2">**</ept>复选框，以便指定通知框架应针对此操作侦听处理程序。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If the handler is implemented, notifications for this operation will then be shown in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果实施该处理程序，将在 POS 中显示有关此操作的通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Employees<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph>, under Retail tab, open the POS permissions associated with the worker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">转到<bpt id="p1">**</bpt>零售<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>员工<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>工作人员<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph>，在“零售”选项卡下，打开与该工作人员关联的 POS 权限。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Expand the <bpt id="p1">**</bpt>Notifications<ept id="p1">**</ept> FastTab, add the <bpt id="p2">**</bpt>Order fulfillment<ept id="p2">**</ept> operation, and set the <bpt id="p3">**</bpt>Display order<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>1<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展开<bpt id="p1">**</bpt>通知<ept id="p1">**</ept>快速选项卡，添加<bpt id="p2">**</bpt>订单履行<ept id="p2">**</ept>操作，然后将<bpt id="p3">**</bpt>显示顺序<ept id="p3">**</ept>字段设置为 <bpt id="p4">**</bpt>1<ept id="p4">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If more than one notification is configured, this field is used to arrange the notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">如果配置了多个通知，将把此字段用于排列通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Notifications that have a lower <bpt id="p1">**</bpt>Display order<ept id="p1">**</ept> value appear above notifications that have a higher value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>显示顺序<ept id="p1">**</ept>值较低的通知在该值较高的通知上方显示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Notifications that have a <bpt id="p1">**</bpt>Display order<ept id="p1">**</ept> value of <bpt id="p2">**</bpt>1<ept id="p2">**</ept> are at the top.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>显示顺序<ept id="p1">**</ept>值为 <bpt id="p2">**</bpt>1<ept id="p2">**</ept> 的通知在最上面显示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Notifications are shown only for operations that are added on the <bpt id="p1">**</bpt>Notifications<ept id="p1">**</ept> FastTab, and you can add operations there only if the <bpt id="p2">**</bpt>Enable notifications<ept id="p2">**</ept> check box for those operations has been selected on the <bpt id="p3">**</bpt>POS operations<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将仅显示有关<bpt id="p1">**</bpt>通知<ept id="p1">**</ept>快速选项卡上添加的操作的通知，而只有 <bpt id="p3">**</bpt>POS 操作<ept id="p3">**</ept>页上已选中了<bpt id="p2">**</bpt>启用通知<ept id="p2">**</ept>选项卡，才能在这里添加操作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Additionally, notifications for an operation are shown to workers only if the operation is added to the POS permissions for those workers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此外，仅当将操作添加到了工作人员的 POS 权限，才对这些工作人员显示有关该操作的通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Notifications can be overridden at the user level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可以在用户级别覆盖通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Open the worker's record, select <bpt id="p1">**</bpt>POS permissions<ept id="p1">**</ept>, and then edit the user's notification subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">打开工作人员的记录，选择 <bpt id="p1">**</bpt>POS 权限<ept id="p1">**</ept>，然后编辑该用户的通知订阅。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profiles<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Functionality profiles<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">转至<bpt id="p1">**</bpt>零售<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>渠道设置<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS 设置<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS 配置文件<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>功能配置文件<ept id="p5">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the <bpt id="p1">**</bpt>Notification interval<ept id="p1">**</ept> field, specify how often notifications should be pulled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在<bpt id="p1">**</bpt>通知时间间隔<ept id="p1">**</ept>字段中，指定提取通知的频率。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For some notifications, the POS must make real-time calls to the back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">对于某些通知，POS 必须实时调用后端办公应用程序。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>These calls consume the compute capacity of your back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">这些调用将消耗后端办公应用程序的计算能力。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Therefore, when you set the notification interval, you should consider both your business requirements and the impact of real-time calls to the back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">因此，设置通知时间间隔时，应同时考虑业务需求和实时调用对后端办公应用程序的影响。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero) turns off notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">值为 <bpt id="p1">**</bpt>0<ept id="p1">**</ept>（零）将关闭通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">转到<bpt id="p1">**</bpt>零售<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>零售 IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>配送计划<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Select the <bpt id="p1">**</bpt>1060<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Staff<ept id="p2">**</ept>) schedule to synchronize notification subscription settings, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">选择 <bpt id="p1">**</bpt>1060<ept id="p1">**</ept>（<bpt id="p2">**</bpt>员工<ept id="p2">**</ept>）计划以同步通知订阅设置，然后选择<bpt id="p3">**</bpt>立即运行<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Next, select the <bpt id="p1">**</bpt>1070<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Channel configuration<ept id="p2">**</ept>) schedule to synchronize the permission interval, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接下来，选择 <bpt id="p1">**</bpt>1070<ept id="p1">**</ept>（<bpt id="p2">**</bpt>渠道配置<ept id="p2">**</ept>）计划以同步权限时间间隔，然后选择<bpt id="p3">**</bpt>立即运行<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>View notifications in the POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在 POS 中查看通知</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>After you complete the preceding steps, the workers will be able to view the notifications in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完成上述步骤之后，工作人员就可以在 POS 中查看通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>To view notifications, press the notification icon in the top right corner of the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要查看通知，按 POS 右上角的通知图标。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>A notification center appears and shows notifications for the order fulfillment operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通知中心将显示，其中显示有关订单履行操作的通知。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The notification center should show the following groups in the order fulfillment operation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通知中心应该在订单履行操作中显示以下组：</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Store pickup<ept id="p1">**</ept> – This group shows the count of orders that have a delivery mode of <bpt id="p2">**</bpt>Pickup<ept id="p2">**</ept>, and that are scheduled for pickup from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>商店提货<ept id="p1">**</ept> - 此组显示交货方式为<bpt id="p2">**</bpt>提货<ept id="p2">**</ept>并且已经计划从当前商店提货的订单计数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>You can press the number on the group to open the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可按组上的编号打开<bpt id="p1">**</bpt>订单履行<ept id="p1">**</ept>页。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In this case, the page will be filtered so that it shows only the active orders that are set up for pickup from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在此情况下，将过滤页面，以便仅显示为从当前商店提货而设置的有效订单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>Ship from store<ept id="p1">**</ept> – This group shows the count of orders that have the delivery mode of <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept>, and that are scheduled for shipment from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>从商店装运<ept id="p1">**</ept> - 此组显示交货方式为<bpt id="p2">**</bpt>装运<ept id="p2">**</ept>并且已经计划从当前商店装运的订单计数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>You can press the number on the group to open the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可按组上的编号打开<bpt id="p1">**</bpt>订单履行<ept id="p1">**</ept>页。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In this case, the page will be filtered so that it shows only the active orders that are set up for shipment from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在此情况下，将过滤页面，以便仅显示为从当前商店装运而设置的有效订单。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>When new orders are assigned to the store for fulfillment, the notification icon changes to indicate that there are new notifications, and the count for the appropriate groups is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将新订单分配给商店履行时，通知图标将更改，以指示有新通知，并将更新相应组的计数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Even though the groups are refreshed at regular intervals however, POS users can manually refresh the groups at any time by selecting the <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> button next to the group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">尽管组按照定期时间间隔刷新，但是 POS 用户随时可以通过选择组旁边的<bpt id="p1">**</bpt>刷新<ept id="p1">**</ept>按钮手动刷新组。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Lastly, if a group has a new item, that the current worker hasn't viewed, then the group shows a burst symbol to indicate new content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最后，如果组有当前工作人员尚未查看的新项，该组将显示一个爆炸符号以指示新内容。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Enable live content on POS buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在 POS 按钮上启用实时内容</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>POS buttons can now show a count to help workers easily determine which tasks require their immediate attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 按钮现在可以显示计数以帮助工作人员轻松确定哪些任务需要他们立即注意。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>To show this number on a POS button, you must complete the notification setup that is described earlier in this topic (that is, you must enable notifications for an operation, set up a notification interval, and update the POS permission group for the worker).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要在 POS 按钮上显示此编号，必须完成此主题前文介绍的通知设置（即，必须启用有关操作的通知，设置通知时间间隔和更新工作人员的 POS 权限组）。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Additionally, you must open the button grid designer, view the button's properties, and select the <bpt id="p1">**</bpt>Enable live content<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">此外，还必须打开按钮网格设计器，查看按钮的属性，以及选中<bpt id="p1">**</bpt>启用实时内容<ept id="p1">**</ept>复选框。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In the <bpt id="p1">**</bpt>Content alignment<ept id="p1">**</ept> field, you can select whether the count appears in the upper-right corner of the button (<bpt id="p2">**</bpt>Top right<ept id="p2">**</ept>) or in the center (<bpt id="p3">**</bpt>Center<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在<bpt id="p1">**</bpt>内容对齐<ept id="p1">**</ept>字段中，可选择计数在按钮右上角（<bpt id="p2">**</bpt>靠上右对齐<ept id="p2">**</ept>）还是中央（<bpt id="p3">**</bpt>居中<ept id="p3">**</ept>）显示。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The live content can be enabled for operations only if the <bpt id="p1">**</bpt>Enable notifications<ept id="p1">**</ept> check box has been selected for them on the <bpt id="p2">**</bpt>POS operations<ept id="p2">**</ept> page, as described earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仅当按照此主题中前文的说明在 <bpt id="p2">**</bpt>POS 操作<ept id="p2">**</ept>页上为操作选中了<bpt id="p1">**</bpt>启用通知<ept id="p1">**</ept>复选框，才能为操作启用实时内容。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The following illustration shows the live content settings in the button grid designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下图显示按钮网格设计器中的实时内容设置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">![</bpt>Live content settings in the button grid designer<ept id="p1">]</ept><bpt id="p2">(./media/ButtonGridDesigner.png "</bpt>Live content settings in the button grid designer<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>按钮网格设计器中的实时内容设置<ept id="p1">]</ept><bpt id="p2">(./media/ButtonGridDesigner.png "</bpt>按钮网格设计器中的实时内容设置<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To show the notification count on a button, you need to ensure that the correct screen layout is being updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要在按钮上显示通知数量，需要确保更新正确的屏幕布局。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>To determine the screen layout that is being used by the POS, select the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> icon in upper-right corner and note the <bpt id="p2">**</bpt>Screen layout ID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Layout resolution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">若要确定 POS 使用的屏幕布局，请选择右上角的<bpt id="p1">**</bpt>设置<ept id="p1">**</ept>图标，然后记下<bpt id="p2">**</bpt>屏幕布局 ID<ept id="p2">**</ept> 和<bpt id="p3">**</bpt>布局分辨率<ept id="p3">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Now using Edge browser, go to the <bpt id="p1">**</bpt>Screen layout<ept id="p1">**</ept> page in Dynamics 365 for Finance and Operations, find the <bpt id="p2">**</bpt>Screen layout ID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Layout resolution<ept id="p3">**</ept> identified above and select the <bpt id="p4">**</bpt>Enable live content<ept id="p4">**</ept> check box.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">现在使用 Edge 浏览器转到 Dynamics 365 for Finance and Operations 中的<bpt id="p1">**</bpt>屏幕布局<ept id="p1">**</ept>页面，找到上面确定的<bpt id="p2">**</bpt>屏幕布局 ID<ept id="p2">**</ept> 和<bpt id="p3">**</bpt>布局分辨率<ept id="p3">**</ept>，然后选中<bpt id="p4">**</bpt>启用动态内容<ept id="p4">**</ept>复选框。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> Distribution schedule<ept id="p1">**</ept> and run the 1090 (Registers) job to synchronize layout changes.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">转到 <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> 配送计划<ept id="p1">**</ept>，然后运行 1090（收银机）作业以同步布局更改。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">![</bpt>Find the screen layout used by POS<ept id="p1">]</ept><bpt id="p2">(./media/Choose_screen_layout.png "</bpt>Find the screen layout <ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>查找 POS 使用的屏幕布局<ept id="p1">]</ept><bpt id="p2">(./media/Choose_screen_layout.png "</bpt>查找屏幕布局<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The following illustration shows the effect of selecting <bpt id="p1">**</bpt>Top right<ept id="p1">**</ept> versus <bpt id="p2">**</bpt>Center<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>Content alignment<ept id="p3">**</ept> field for buttons of various sizes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下图显示在<bpt id="p3">**</bpt>内容对齐<ept id="p3">**</ept>字段中选择<bpt id="p1">**</bpt>靠上右对齐<ept id="p1">**</ept>与<bpt id="p2">**</bpt>居中<ept id="p2">**</ept>对各种尺寸的按钮的影响。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">![</bpt>Live content on POS buttons<ept id="p1">]</ept><bpt id="p2">(./media/ButtonsWithLiveContent.png "</bpt>Live content on POS buttons<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>POS 按钮上的实时内容<ept id="p1">]</ept><bpt id="p2">(./media/ButtonsWithLiveContent.png "</bpt>POS 按钮上的实时内容<ept id="p2">")</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>