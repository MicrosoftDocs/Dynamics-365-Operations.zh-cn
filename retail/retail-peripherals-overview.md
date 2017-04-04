---
title: "零售外设概览"
description: "此主题介绍与零售外设的概念。 它描述不同方式负责管理与 POS 连接的负责的外围可以连接到销售点 (POS) 和组件。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>零售外设概览

此主题介绍与零售外设的概念。 它描述不同方式负责管理与 POS 连接的负责的外围可以连接到销售点 (POS) 和组件。

<a name="concepts"></a>概念
--------

### <a name="pos-registers"></a>POS 收银机

中：**单击零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** **登记。 销售终端 (POS) 登记是用于定义 POS 的特定实例特性的实体。 包括这些特性硬件配置文件或设置要在收银机使用的外设，零售商店登记映射到和外观经验的登录到该登记的用户的。

### <a name="devices"></a>设备

中：**单击零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** **设备。 设备是表示映射到 POS 收银机的设备的物理实例的实体。 设备在创建时，则映射到 POS 收银机。 设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。 设备可以映射到核销以下类型：Retail Modern POS、零售云 POS、Retail Modern POS – Windows "，Retail Modern POS –机器人和 Retail Modern POS – iOS。

### <a name="retail-modern-pos"></a>Retail Modern POS

Modern POS 是 Microsoft Windows 的 POS 程序。 它在 Windows 上可以部署 10 操作系统 (厄申)。

### <a name="cloud-pos"></a>云 POS

云 POS 是在查看器中访问 Modern POS 程序的基于浏览器的版本。

### <a name="modern-pos-for-ios"></a>iOS 的 Modern POS

iOS 的 Modern POS 是在 iOS 设备可以部署 Modern POS 的程序基于 iOS 的版本。

### <a name="modern-pos-for-android"></a>机器人的 Modern POS

机器人的 Modern POS 是在机器人设备可以部署 Modern POS 的程序基于机器人的版本。

### <a name="pos-peripherals"></a>POS 外设

POS 外设是为 POS 功能明确支持的设备。 这些外设通常划分为特定类。 有关这些类的详细信息，请参阅此主题的分类“设备”部分。

### <a name="hardware-station"></a>硬件工作站

中：**单击零售和商务** &gt; **通道** &gt; **零售店** &gt; **零售店**所有。 选择一个商店，然后单击**硬件工作站**快速选项卡。 **硬件工作站**设置是用于定义这个实例将部署零售外围逻辑的通道级别设置。 通道在级别的设置用于确定此硬件工作站的特征。 它还列出可用于 Modern POS 实例是可用于特定商店的硬件工作站。 硬件工作站生成到 Windows Modern POS 的程序。 硬件工作站可以独立还会部署为独立 Microsoft Internet Information Services (IIS) 程序。 在这种情况下，可以通过网络访问。

### <a name="hardware-profile"></a>硬件配置文件

中：**单击零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** POS 配置文件** &gt; ** **硬件配置文件。 硬件配置文件是为 POS 收银机或硬件工作站配置设备的列表。 硬件配置文件可以映射直接向 POS 收银机或硬件工作站。

## <a name="devices-classes"></a>设备分类
POS 外设通常划分为类。 此部分描述并提供 Modern POS 支持的设备的概览。

### <a name="printer"></a>打印机

打印机包括传统 POS 收据打印机和范围"页的打印机。 打印机 POS 通过 Retail (OPOS) 和 Microsoft Windows 驱动程序的对象链接和嵌入支持界面。 可以同时使用这两打印机。 此功能支持自运付现的收据打印机接收客户收据上打印的方案，而客户订单，查看附有详细信息，在一打印机打印范围的页。 收据打印机接收可以直接连接到计算机 USB 通过，连接到网络通过以太网或通过 Bluetooth 连接。

### <a name="scanner"></a>扫描仪

可以同时使用这两条码扫描仪。 此功能支持更大以要求移动的扫描或大量物料扫描仪的方案，固定的，而嵌入的扫描仪对于大多数标准尺寸的物料使用，可以加速签出时间。 扫描仪可以通过 OPOS、一般 Windows 平台 (UWP) 键盘或楔形接口支持。 USB 或 Bluetooth 可用于连接扫描仪到计算机。

### <a name="msr"></a>MSR

使用 OPOS 司机，一 USB 磁条阅读器 (MSR) 可以设置。 如果您要出于电子资金转帐 (EFT) 付款交易记录使用单独 MSR，必须由付款管理 MSR Connector。 独立 MSRs 可用于客户会员条目、员工登录和礼品卡付款条目使用，使用不受 Connector。

### <a name="cash-drawer"></a>银箱

两银箱可以按硬件配置文件支持。 此功能允许同时按收银机两个有效班次才可用。 对于共享的倒班或多个同时移动设备 POS 使用的现金，银箱，只有一银箱允许每个硬件配置文件。 银箱可以直接连接到计算机 USB 通过，连接到网络或连接到收据打印机接收通过 RJ12 界面。 银箱在某些情况下，可以通过 Bluetooth 还连接。

### <a name="line-display"></a>行显示内容

查看用于行查看产品、交易记录余额和其他有用信息。客户在交易过程。 使用 OPOS 司机，一行显示。通过 USB 连接到计算机。

### <a name="signature-capture"></a>签名捕获

使用 OPOS 司机签名，签名将捕获该设备可以直接连接到计算机。通过 USB 在签名在配置时，客户进行设备提示签名。 在提供签名后，它会显示已对接受的出纳。

### <a name="scale"></a>比例

使用 OPOS 斯科尔斯司机，可以通过 USP 连接到计算机。 在标记为“进行称重”产品时的产品添加到交易记录中，则读取 POS 刻度的重量，产品添加到交易记录，并使用刻度提供的数量。

### <a name="pin-pad"></a>PIN 小键盘

个人标识号 (PIN) 通过填充 OPOS 支持，礼品，但必须通过付款管理。Connector。

### <a name="secondary-display"></a>附属显示

如果辅助查看配置期间，则第 2 Windows 查看用于显示基本信息。 因为不足框以外，以便显示不可配置并不显示内容，以便显示有限的目的是支持独立软件供应商 (ISV) 扩展名。

### <a name="payment-device"></a>付款设备

付款设备支持通过付款 Connector 实施。 付款设备可以执行其他设备提供之一或分类的许多功能。 例如，可能付款设备功能用作 MSR/card 阅读器、行、查看签名捕获设备、PIN 小键盘。 付款设备的使用不受支持。其他设备提供在硬件配置文件支持设备无关包括实施。

## <a name="supported-interfaces"></a>支持的接口
### <a name="opos"></a>OPOS

为了帮助保障的最大范围可使用设备与 Microsoft Dynamics 365。工序，-零售业标准的 OLE for POS 是在工序 365 的 Microsoft Dynamics 中支持的主要-零售外围设备平台零售销售"。 OLE for POS 标准由国家/地区选择零售 (NRF) 执行生产，建立零售业标准外围设备的通信协议。 OPOS 是标准的 OLE for POS 一次多个阶段的实现方式。 它在 20 世纪 90 年代中期将开发的开始和配置后更新若干次。 OPOS 提供支持 POS 硬件的简便集成。Microsoft 视窗 POS 系统中一种设备驱动程序体系结构。 OPOS 兼容硬件和软件手柄控制 POS 之间的通信。 OPOS 控制包括两部分：

-   **控件对象**设备–分类的控件对象 (如行显示) 提供程序为软件界面。 向服务的门罗 (www.monroecs.com [] (http://www.monroecs.com/)) 提供标准化的 OPOS 公共控件对象组 ((CCOs) 控制的对象。 CCOs 用于测试 POS 组件零售的工序的 Microsoft Dynamics 365 -。 因此，帮助，测试保障，则工序的 Microsoft Dynamics 365 -通过支持零售 OPOS 设备分类，多种设备类型，可以支持，将制造商提供为 OPOS 生成的服务对象情况下。 没有明确必须测试设备每个类型。
-   ** **服务对象–服务提供对象控件对象 (CCO) 和设备之间的通信。 通常，设备制造商提供设备的服务对象。 但是，在某些情况下，您可能必须下载来自制造商的网站的服务对象。 例如，最近一服务对象可能可用。 若要查找制造商的网站地址，请参阅您的硬件文档。

控制![[] (服务对象和对象。/media/retail_peripherals_overview01.png)](。OLE for POS 的 OPOS 实施的/media/retail_peripherals_overview01.png) 支持的，帮助保障，如果设备制造商和 POS 发布者正确实施，标准 POS 系统和支持的设备可以，它们一起以前，即使尚未测试。 **注释：** OPOS 支持未 OPOS 司机的所有设备保障的支持。 工序的第一个必需-零售支持 Microsoft Dynamics 365 类型或设备类，通过 OPOS。 此外，服务对象可能并不始终是最新的 CCOs 的最新版本。 还应了解，服务的质量，一般来说对象更改。

### <a name="windows"></a>窗口

在 POS 打印收据的 OPOS 为优化。 OPOS 于打印倾向于通过快速 Windows。 因此，它是一个最好使用 OPOS，尤其是在 40 列打印收货的零售环境，交易记录是时间必须快的。 对于多数设备，您将使用 OPOS 控制。 但是，某些 OPOS 收据打印机接收还支持 Windows 司机。 通过使用 Windows 司机，您可以访问的最近一网络字体和打印机的多个收银机。 不过，在缺点到使用 Windows 司机。 这是这些缺点的一些示例：

-   在使用时，Windows 司机图像呈现，在打印前。 因此，超过其打印上使用 OPOS 打印机的控制倾向于慢。
-   通过的打印机设备 (“菊花链") 附加可能无法正确地工作，以便在使用时 Windows 司机。 例如，可能尚未打开银箱，或者打印机清单可能不短语，您预期。
-   OPOS 还支持特定于零售收据打印机的更多组的变量，如表或将布料清单打印。

如果是用于控制 Windows 打印机可使用打印机，您应正确地仍与零售的工序的 Microsoft Dynamics 365 -使用。

### <a name="universal-windows-platform"></a>一般 Windows 平台

UWP，如果零售外设，帮助与设备的 Windows 支持。 当一即插即用设备连接到支持这种设备的 Windows "操作系统版本司机时，不需要遵循使用设备所需的计划。 例如，则 Windows Bluetooth 检测到一扬声器设备，知道设备** "操作系统具有扬声器**类型分类。 因此和该物料将被视作扬声器为该设备。 不需要进一步的设置。 在 POS 设备，可以 USB 接通多种设备，并且，Windows 将识别。为人类相互关系 (HIDs) 设备。 但是，可能不能确定设备提供的功能，设备，因为未指定，类或类型，的设备。 在 Windows 10，条码扫描仪的设备分类和 MSRs 已添加。 因此，如果设备，声明到 Windows 10 为设备这些类之一，Windows 将细听来自设备的事件。的相应时间。 支持 UWP Modern POS 和 MSRs 扫描仪。 因此，准备，将从这些设备之一时输入的和属于这些类之一的设备连接，设备可以使用。 例如，如果 UWP，条码扫描仪插入到 Windows 10 计算机和条码登录为 Modern POS 配置，条码扫描仪将要生效在登录屏幕。 不需要进一步的设置。 问题附加的类的服务 UWP 设备添加到 Windows。 这些类包含为银箱和收据打印机接收分类。 这些新设备分类的支持。Modern POS 是未决的。

### <a name="keyboard-wedge"></a>键盘楔形

键盘楔形设备将数据发送到计算机，才能将该数据上键盘时输入了。 因此，默认情况下处于活动状态，在 POS 的字段将接收"扫描或刷的数据。 在某些情况下，此行为会导致错误的数据类型扫描到错误的字段。 例如，可能条码扫描到为信用卡数据使用输入的字段。 在大多数情况下，具有在逻辑确定的 POS 是否是条码扫描或刷卡或刷的数据。 因此，数据正确处理。 但是，当设置 OPOS 设备，为{{而不是：instead_of}}键盘楔形设备时，在对来自这些设备的数据的详细如何控制，因为可以使用，详细了解有关”"的数据来自设备。 例如，从条码扫描仪的数据都会自动将被标识为，条码，并在数据库中记录。与和快速地找到比，如果使用了一个一般串搜索，如果楔形键盘设备。

### <a name="native-printer"></a>局部的打印机

局部的 (或“设备”，当类型的"硬件配置文件将命名) 打印机可以配置提示用户选择用于计算机配置的打印机。 **在设备**时类型的配置，如果打印机，Modern POS 打印订单，用户遇到系统提示选择列表中的某一打印机。 此行为与 Windows 司机的行为，不同，因为** Windows 打印机键入**硬件配置文件。显示打印机的列表。 相反，它要求命名在**打印机设备名称**字段提供。

### <a name="windows"></a>窗口

** Windows **设备类型只需要使用的打印机。 在 Windows 打印机的"硬件配置文件时配置，必须提供特定打印机名称。 如果遇到 Modern POS 打印，事件，则 Windows 打印机配置，事件将传递到指定的 Windows 打印机。 用户将不提示选择打印机。

### <a name="network"></a>网络

网络可以解决的收据打印机、银箱和付款终端可以使用通过网络，以下内容之一通过直接生成到 Modern POS 的 Windows 应用程序或通过其他 Modern POS 客户 IIS 的硬件工作站的进程中申报 (IPC 硬件工作站)。

## <a name="hardware-station-deployment-options"></a>硬件工作站部署选项
### <a name="ipc-built-in"></a>IPC 内 (日期)

进程中申报 (IPC) 硬件工作站生成到程序的 Windows 应用 Modern POS。 IPC 若要使用硬件工作站，请将硬件配置文件分配给为 Windows 应用程序将利用 Modern POS 的登记。 然后创建硬件工作站**专用**登记为要使用的商店键入。 当您启动 Modern POS IPC，硬件工作站的有效期，然后配置的 POS 外设将立即可用。 如果因为某些原因您不需要暂时位置硬件，请使用**请管理硬件工作站**工序关闭硬件工作站功能。 IPC Modern POS 还可以使用硬件工作站直接与外围网络通信。

### <a name="iis"></a>IIS

可以用以下两种方式可以使用硬件工作站的 IIS 或独立版本。 IIS”POS“描述符暗示应用程序连接到硬件工作站通过 Microsoft Internet 信息服务。 POS 应用程序连接到 IIS 通过硬件工作站上运行的计算机设备连接的 Web 服务。 在使用时，连接到 IIS 硬件工作站的零售外设可由位于网络和 IIS 硬件工作站相同的所有 POS 收银机。 由于 Windows 的仅包括零售 Modern POS 外设的支持，内置其他 Modern POS 应用程序必须使用 IIS 硬件工作站配置文件用在硬件配置的 POS 外设通信。 因此 IIS，硬件工作站的要求每个实例运行 Web 服务和应用程序与设备连接的计算机。 IIS 硬件工作站对于某些非 Windows Modern POS 应用程序所需的。

#### <a name="dedicated"></a>专门

Modern POS 使用硬件工作站**专用**键入检测外设直接连接到应用使用的计算机。 **但是，专用**类型可以为 IIS。还可以使用硬件工作站 在 POS 使用覆盖的传统，固定的 POS 方案，POS 应用程序，专用** **硬件工作站类型。IIS 在同一计算机运行云部署 POS 硬件工作站的使用。 从一个零售外设，专用中的 IIS 硬件工作站具有传统，固定的 POS 方案的更好的零售外围网络支持。 专用的硬件工作站支持"硬件配置文件支持的所有外设。

#### <a name="shared"></a>共享的

共享的硬件工作站想按多个 POS 设备通过使用日的课程。 共享的硬件工作站支持优化收据打印机、银箱和终端只有付款。 您不能直接连接独立条码扫描仪、行显示，MSRs、缩放比例，或其他设备。 否则，当多尝试设备 POS 外设这些要求同时，将发生冲突。 这是冲突如何为支持的设备管理：

-   **银箱**银箱–通过发送到设备的事件将打开。 可能得到的唯一的，在发货银箱调用时发生，则已打开银箱。 对于共享的硬件工作站，应设置银箱**到共享**在硬件配置文件。 此设置为禁止 POS 检查银箱是否已打开，则发送打开命令时。
-   ** **收据打印机–，如果两打印收货订单同时发送到硬件工作站，某一命令可以根据设备，丢失。 设备某些可能阻止此发货中存储或合并。 如果打印订单不成功，出纳将收到错误消息，然后重试可以从" POS 打印的订单。
-   **终端**付款–如果出纳，支付-尝试在已使用的付款终端的交易记录，消息通知终端出纳使用并要求出纳后重试。 通常，出纳可以看到已使用终端和等待，在其他交易完成，在尝试再次前支付方式。

验证。一计划从将来版本中，会检测到不支持的设备是否为映射到共享的硬件的硬件工作站配置文件设置。 如果检测到任何不支持的设备，用户将收到该的消息，指出该设备不要共享该硬件工作站支持。 对于共享的硬件工作站，该**选择时支付**选项设置** **是在收银机级别。 时，或者在将支付方式选择在 POS 时，记录的交易的 POS 用户然后系统提示选择硬件工作站。 在硬件工作站在支付方式时，只有所选类添加硬件车站选择直接到移动方案的 POS 工作流。 作为一种附加利益，付款在终端的行显示没有为共享的情况而设计的。 如果付款为终端使用行显示，其他终端使用该用户可能会被锁定，直到完成交易记录。 移动在方案，行可能会添加到交易记录通过长时间。 因而，这个**选择时支付**选项要求确保最佳设备可用性。

### <a name="network-peripherals"></a>外围网络

设备的标识网络在硬件配置文件中启用收据打印机、银箱和通过网络连接将附加了付款终端。

#### <a name="modern-pos-for-windows"></a>Windows 的 Modern POS

可以为网络外设指定 IP 地址。这两个位置。 如果 Modern POS Windows 客户使用独特外设网络组，您应该设置这些设备的 IP 地址。使用操作窗格上的 IP ** **配置登记的选项。 对于在中将 POS 的共享网络设备登记，具有的硬件设备网络配置文件分配给它可以映射直接分配给共享的硬件工作站。 若要分配 IP 地址，选择"零售店** **页面的硬件工作站，在硬件工作站** **部分然后使用该** IP 配置**指定选项分配给该硬件工作站的网络设备。 对于具有只网络设备的硬件工作站，则不必部署硬件工作站。 在这种情况下，硬件工作站以根据要求的概念的零售店这个位置上只网络组可以解决的设备。

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>覆盖 POS、Modern POS 的 iOS Modern POS 和机器人的

驱动器实际连接的逻辑和解决的外围网络。"硬件工作站包含。 因此，适用于除 Modern POS 的所有客户 POS Windows 的 IIS，硬件工作站必须部署和活动支持 POS 外设与通信，而不管这些外设是否实际连接到硬件工作站通过网络或解决。

## <a name="setup-and-configuration"></a>设置和配置
### <a name="hardware-station-installation"></a>设置硬件工作站

有关信息，请参阅 Retail 硬件工作站 [] (配置和安装 Retail 硬件工作站配置 installation.md)。

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Windows 的设置和配置进行 Modern POS

有关信息，请参阅" Retail Modern POS [] (配置和安装 Retail POS activation.md 现代化设备)。

### <a name="opos-device-setup-and-configuration"></a>OPOS 设备设置和配置

OPOS 组件有关的详细信息，请参阅单据“支持的接口”部分。 通常，设备制造商提供 OPOS 司机。 当安装 OPOS 设备驱动程序后，该程序在下列位置之一的参数添加到 Windows 注册表：

-   **位 32 系统：** HKEY\_本机\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **位 64 系统：** HKEY\_本机\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

在注册表中，ServiceOPOS 位置配置的设备根据 OPOS 设备分类进行组织。 多种设备保存驱动程序。

## <a name="supported-scenarios-by-hardware-station-type"></a>按硬件工作站支持的方案的类型
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>客户–硬件工作站支持 IPC 与 IIS 硬件工作站

下表显示支持的拓扑和部署方案。

| 客户      | IPC 硬件工作站 | IIS 硬件工作站 |
|-------------|----------------------|----------------------|
| Windows 应用 | 是                  | 是                  |
| 云 POS   | 无                   | 是                  |
| 机器人     | 无                   | 是                  |
| iOS         | 无                   | 是                  |

### <a name="network-peripherals"></a>外围网络

网络外设可以直接通过建立到程序的 Windows 应用 Modern POS 的硬件工作站支持。 对于其他客户，则必须部署 IIS 硬件工作站。

| 客户      | IPC 硬件工作站 | IIS 硬件工作站 |
|-------------|----------------------|----------------------|
| Windows 应用 | 是                  | 是                  |
| 云 POS   | 无                   | 是                  |
| 机器人     | 无                   | 是                  |
| iOS         | 无                   | 是                  |

## <a name="supported-device-types-by-hardware-station-type"></a>按类型的硬件工作站支持的设备的类型
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Windows 的 Modern POS 的 IPC (日期) 内硬件工作站

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>支持的设备分类</th>
<th>支持的接口</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>打印机</td>
<td><ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>设备</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="even">
<td>打印机 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>设备</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="odd">
<td>行显示内容</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>双显示器</td>
<td>Windows 驱动程序</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>OPOS</li>
<li>UWP (不需要设置。)</li>
<li>键盘楔形 (不需要设置。)</li>
</ul></td>
</tr>
<tr class="even">
<td>开票人</td>
<td><ul>
<li>OPOS</li>
<li>如果 <strong>注意：</strong> 针对银箱，配置网络仅 <strong>使用共享的倒班</strong> 为银箱可以设置。</li>
</ul></td>
</tr>
<tr class="odd">
<td>开票人 2</td>
<td><ul>
<li>OPOS</li>
<li>如果 <strong>注意：</strong> 针对银箱，配置网络仅 <strong>使用共享的倒班</strong> 为银箱可以设置。</li>
</ul></td>
</tr>
<tr class="even">
<td>扫描仪</td>
<td><ul>
<li>OPOS</li>
<li>UWP (不需要设置。)</li>
<li>键盘楔形 (不需要设置。)</li>
</ul></td>
</tr>
<tr class="odd">
<td>扫描仪 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (不需要设置。)</li>
<li>键盘楔形 (不需要设置。)</li>
</ul></td>
</tr>
<tr class="even">
<td>比例</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN 小键盘</td>
<td>OPOS (支持通过付款 Connector 的自定义提供)。</td>
</tr>
<tr class="even">
<td>签名捕获</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>付款终端</td>
<td><ul>
<li>设备支持自定义</li>
<li>网络 (有关详细信息，请参阅付款 Connector 文档。)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>具有一个专用的 IIS 硬件工作站的所有 Modern POS 客户

**注释：**在 IIS，硬件工作站为“专用的时，具有”POS 硬件工作站和客户之间的一对一关系。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>支持的设备分类</th>
<th>支持的接口</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>打印机</td>
<td><ul>
<li>OPOS</li>
<li>Windows <strong>注意：</strong> 打印机的 Windows 司机在网络，硬件工作站的用户必须拥有访问权限打印机。</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="even">
<td>打印机 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="odd">
<td>行显示内容</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>开票人</td>
<td><ul>
<li>OPOS</li>
<li>如果 <strong>注意：</strong> 针对银箱，配置网络仅每个硬件 <strong>使用共享的倒班</strong> 配置文件。银箱可以设置。</li>
</ul></td>
</tr>
<tr class="even">
<td>开票人 2</td>
<td><ul>
<li>OPOS</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="odd">
<td>扫描仪</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>扫描仪 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>比例</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN 小键盘</td>
<td>OPOS (支持通过付款 Connector 的自定义提供)。</td>
</tr>
<tr class="odd">
<td>符号。 捕获</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>付款终端</td>
<td><ul>
<li>设备支持自定义</li>
<li>网络 (有关详细信息，请参阅付款 Connector 文档。)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>具有共享的 IIS 硬件工作站的所有 Modern POS 客户

**注释：**在 IIS，硬件工作站“共享多个期间，”设备能同时使用硬件工作站。 对于此情况，您应该使用在下表中列出的仅设备。 如果您尝试在此处列出未共享，例如条码扫描仪和 MSRs，错误的设备将发生，当多尝试设备要求相同的外设。 将来，此配置中明确会阻止。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>支持的设备分类</th>
<th>支持的接口</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>打印机</td>
<td><ul>
<li>OPOS</li>
<li>Windows <strong>注意：</strong> 打印机的 Windows 司机在网络，硬件工作站的用户必须拥有访问权限打印机。</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="even">
<td>打印机 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="odd">
<td>开票人</td>
<td><ul>
<li>OPOS</li>
<li>如果 <strong>注意：</strong> 针对银箱，配置网络仅每个硬件 <strong>使用共享的倒班</strong> 配置文件。银箱可以设置。</li>
</ul></td>
</tr>
<tr class="even">
<td>开票人 2</td>
<td><ul>
<li>OPOS</li>
<li>网络</li>
</ul></td>
</tr>
<tr class="odd">
<td>付款终端</td>
<td><ul>
<li>设备支持自定义</li>
<li>网络 (有关详细信息，请参阅付款 Connector 文档。)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>支持的方案的配置
有关如何创建硬件配置文件的详细信息，请参阅将 [定义和维护客户，包括通道登记和硬件工作站] (通道定义维护客户登记 hw stations.md)。 **注释：**版本对于工序 365 的 Microsoft Dynamics 1611，硬件工作站配置文件不能再使用。 属性您在硬件工作站配置文件为已设置现在硬件工作站的一部分。

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Windows 的 Modern POS 的 IPC (日期) 内硬件工作站

此 Configuration 是传统，固定的 POS 收银机的最一般的配置。 对于此方案，硬件配置文件信息直接到登记表。 在收银机还应设置 EFT 终端编号。 若要设置此 Configuration，请执行以下步骤。

1.  创建所需的外围配置的硬件配置文件。
2.  映射硬件配置文件。POS 收银机。
3.  创建硬件工作站**专用**为将使用 POS 收银机的零售店键入。 描述是可选的。 **注释：**您不必设置在硬件工作站的任何其他属性。 必需的信息，例如其他硬件配置文件，将来自登记。
4.  **单击零售和商务** &gt; **零售 IT ** &gt; ** **分配计划。
5.  ** **选择 1090 分配计划的新同步硬件配置文件分配给商店。 ** POS 的更改同步到的单击**立即运行。
6.  ** **选择 1040 分配计划同步新的硬件工作站到商店。 ** POS 的更改同步到的单击**立即运行。
7.  安装和启用 Windows 的 Modern POS。
8.  启动用于 Windows 的 Modern POS，然后开始用于连接的外围设备。

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>具有一个专用的 IIS 硬件工作站的所有 Modern POS 客户

此 Configuration 可以为有一个硬件工作站一个 POS 收银机使用完全 Modern POS 使用的所有客户。 若要设置此 Configuration，请执行以下步骤。

1.  创建所需的外围配置的硬件配置文件。
2.  创建硬件工作站**专用**为将使用 POS 收银机的零售店键入。
3.  在单个的硬件工作站，设置以下属性：
    -   ** **主机名–硬件工作站将运行主计算机的名称。 **注释：**云 POS 可以确定解决** localhost **云 POS 运行的本地计算机。 但是，要求以匹配与 POS 硬件工作站的云的证书还必须具有“Localhost”为计算机名称。 若要避免发货，我们建议您列出每个专用的硬件工作站的商店实例，然后根据需求。 对于每个硬件工作站，主机名应是硬件工作站将部署的特定计算机名称。
    -   ** **端口–所使用的端口。可以使用硬件工作站 Modern POS 客户进行通信。
    -   ** ** –硬件配置文件，则在硬件工作站提供，不分配给收银机的硬件配置文件中使用硬件配置文件。
    -   ** EFT POS 编号** EFT 授权–使用什么时候 EFT 的终端 ID 发送。 信用卡处理程序提供此 ID。
    -   ** **使用包装名称–硬件工作站什么时候的硬件工作站包装部署。

4.  **单击零售和商务** &gt; **零售 IT ** &gt; ** **分配计划。
5.  ** **选择 1090 分配计划的新同步硬件配置文件分配给商店。 ** POS 的更改同步到的单击**立即运行。
6.  ** **选择 1040 分配计划同步新的硬件工作站到商店。 ** POS 的更改同步到的单击**立即运行。
7.  设置硬件工作站。 有关如何安装硬件工作站的详细信息，请参阅 Retail 硬件工作站 [] (配置和安装 Retail 硬件工作站配置 installation.md)。
8.  设置并激活 Modern POS。 有关如何安装 Modern POS 的详细信息，请参阅" Retail Modern POS [] (配置和安装 Retail POS activation.md 现代化设备)。
9.  登录到并选择** Modern POS，请执行非银箱**工序。
10. 管理启动**硬件工作站**工序。
11. **管理**请单击。
12. 在硬件车站管理页面，请设置硬件工作站打开此选项。
13. 选择使用硬件工作站，然后单击**对**。
14. 在硬件工作站匹配后，单击** **结转。
15. 在硬件车站选择页，请单击新选定的硬件工作站需使它处于活动状态。

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>具有共享的 IIS 硬件工作站的所有 Modern POS 客户

此 Configuration 可以为共享与其他设备的硬件工作站的所有 Modern POS 客户使用。 若要设置此 Configuration，请执行以下步骤。

1.  创建所需的外围配置的硬件配置文件。
2.  创建硬件工作站** **共享为将使用 POS 收银机的零售店键入。
3.  在共享的硬件工作站，设置以下属性：
    -   ** **主机名–硬件工作站将运行主计算机的名称。
    -   **将帮助标识硬件工作站的描述** –短消息，如退货** ** **前面**或商店。
    -   ** **端口–所使用的端口。可以使用硬件工作站 Modern POS 客户进行通信。
    -   ** **硬件配置文件–共享的硬件工作站的，为每个硬件工作站应将硬件配置文件。 硬件配置文件可在硬件工作站中共享，但必须映射到每个硬件工作站。 此外，我们建议您使用共享的倒班，当多使用共享相同设备的硬件工作站时。 若要设置共享的倒班，请单击**零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** POS 模板** &gt; ** **硬件配置文件。 对于每个共享的硬件配置文件，请选择针对银箱，并且设置该**共享的倒班银箱**是** **选项。
    -   ** EFT POS 编号** EFT 授权–使用什么时候 EFT 的终端 ID 发送。 信用卡处理程序提供此 ID。
    -   ** **使用包装名称–硬件工作站什么时候的硬件工作站包装部署。

4.  重复中商店需的每个附加的硬件工作站的步骤 2 和 3。
5.  **单击零售和商务** &gt; **零售 IT ** &gt; ** **分配计划。
6.  ** **选择 1090 分配计划的新同步硬件配置文件分配给商店。 ** POS 的更改同步到的单击**立即运行。
7.  ** **选择 1040 分配计划同步新的硬件工作站到商店。 ** POS 的更改同步到的单击**立即运行。
8.  设置在您的设置步骤 2 和 3. 的每个主计算机的硬件工作站。 有关如何安装硬件工作站的详细信息，请参阅 Retail 硬件工作站 [] (配置和安装 Retail 硬件工作站配置 installation.md)。
9.  设置并激活 Modern POS。 有关如何安装 Modern POS 的详细信息，请参阅" Retail Modern POS [] (配置和安装 Retail POS activation.md 现代化设备)。
10. 登录到并选择** Modern POS，请执行非银箱**工序。
11. 管理启动**硬件工作站**工序。

12. **管理**请单击。
13. 在硬件车站管理页面，请设置硬件工作站打开此选项。
14. 选择使用硬件工作站，然后单击**对**。
15. 重复 Modern POS 将使用的每个硬件工作站的第 14 步。
16. 在所有所需的硬件工作站匹配后，单击** **结转。
17. 在硬件车站选择页，请单击新选定的硬件工作站需使它处于活动状态。 **注释：**设备，则通常使用不同的硬件工作站，我们建议您通过配置 Modern POS 会提示出纳选择硬件工作站，在开始流程时支付方式。 **单击零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** **登记。 选择登记，然后设置该**选择时支付方式**是** **选项。 ** **使用 1090 分配计划同步到通道数据库的更改。

## <a name="extensibility"></a>可扩展性
有关硬件工作站的扩展性方案的信息，请参阅 [] (dev 扩展性硬件工作站 itpro/硬件工作站 extensibility.md)。

## <a name="security"></a>安全性
根据当前安全标准，以下设置应在生产环境：**注释：**硬件工作站安装程序将自动进行编辑这些登记表作为安装的一部分通过自助服务。

-   应禁用安全套接字层 (SSL)。
-   传输层安全性应启用和使用 (TLS) 版本 (TLS) (或者只当前最高的版本。) **注释：**默认情况下，TLS SSL 和所有版本只有 1.2 的 TLS 禁用。 若要编辑或启用这些值，请执行以下步骤：
    1.  按 Windows 徽标 key+R 运行** **打开"窗口。
    2.  **在打开** "字段中，键入 Regedit ** **，然后单击** **好。
    3.  如果用户帐户。**控制**此时出现，则单击**是**。
    4.  **在注册表编辑器**窗口，导航** HKEY\_本机\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols **。 以下参数自动输入只允许 TLS 1.2:
        -   TLS 1.2Server: Enabled=1
        -   TLS 1.2Server: DisabledByDefault=0
        -   TLS 1.2Client: Enabled=1
        -   TLS 1.2Client: DisabledByDefault=0
        -   TLS 1.1Server: Enabled=0
        -   TLS 1.1Client: Enabled=0
        -   TLS 1.0Server: Enabled=0
        -   TLS 1.0Client: Enabled=0
        -   SSL 3.0Server: Enabled=0
        -   SSL 3.0Client: Enabled=0
        -   SSL 2.0Server: Enabled=0
        -   SSL 2.0Client: Enabled=0
-   网络应的其他端口尚未打开，除非它们。了解是必需的，指定的原因。
-   必须禁用跨来源资源共享和必须指定所接受的允许的来源。
-   仅应信任认证主管机构使用的计算机上运行。使用硬件工作站的证书。

**注释：**非常重要的您在 IIS 和支付卡行业 (PCI) 需求的安全准则。

## <a name="peripheral-simulator"></a>外围设备模拟器
有关信息，请参阅零售 [外围模拟程序] (零售外设 simulator.md)。

## <a name="microsofttested-peripheral-devices"></a>Microsofttested 外围设备
### <a name="ipc-built-in-hardware-station"></a>IPC (日期) 内硬件工作站

以下测试外围使用生成到 Windows 的 Modern POS 硬件工作站的 IPC。

#### <a name="printer"></a>打印机

| 制造商 | 型号    | 接口 | 评论                |
|--------------|----------|-----------|-------------------------|
| 爱普生        | TmT88IV | OPOS      |                         |
| 爱普生        | TM-T88V  | OPOS      |                         |
| 星级         | TSP650II | OPOS      |                         |
| 星级         | TSP650II | 自定义    | 连接通过网络   |
| 星级         | mPOP     | OPOS      | 通过 Bluetooth 连接 |
| HP           | F7M67AA  | OPOS      | 结算的 USB             |

#### <a name="bar-code-scanner"></a>条码扫描器

| 制造商  | 型号         | 接口 | 评论 |
|---------------|---------------|-----------|----------|
| 摩托罗拉      | DS9208        | OPOS      |          |
| 霍尼韦尔     | 1900          | UWP       |          |
| 符号        | LS2208        | OPOS      |          |
| 集成的 HP | E1L07AA       | OPOS      |          |
| Datalogic     | 麦哲伦 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN 小键盘

| 制造商 | 型号  | 接口 | 评论                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | 需要付款 Connector 的自定义 |

#### <a name="payment-terminal"></a>付款终端

| 制造商 | 型号 | 接口 | 评论                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| 昼夜平分利      | L5300 | 自定义    | 需要付款 Connector 的自定义                                |
| VeriFone     | MX925 | 自定义    | 需要付款 Connector 的自定义功能；连接和 USB 通过网络 |
| VeriFone     | MX915 | 自定义    | 需要付款 Connector 的自定义功能；连接和 USB 通过网络 |

#### <a name="cash-drawer"></a>银箱

| 制造商 | 型号     | 接口 | 评论                |
|--------------|-----------|-----------|-------------------------|
| 星级         | mPOP      | OPOS      | 通过 Bluetooth 连接 |
| APG          | 爱特伍    | 自定义    | 连接通过网络   |
| 星级         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>行显示内容

| 制造商  | 型号   | 接口 | 评论 |
|---------------|---------|-----------|----------|
| 集成的 HP | G6U79AA | OPOS      |          |
| 爱普生         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>签名捕获

| 制造商 | 型号  | 接口 | 评论 |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>比例

| 制造商 | 型号         | 接口 | 评论 |
|--------------|---------------|-----------|----------|
| Datalogic    | 麦哲伦 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| 制造商 | 型号       | 接口 | 评论 |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>专用的 IIS 硬件工作站

以下测试外围使用一个专用 (") 未共享的 IIS 硬件工作站和 Windows 身份的 Modern POS 一起并覆盖 POS。

#### <a name="printer"></a>打印机

| 制造商 | 型号    | 接口 | 评论                  |
|--------------|----------|-----------|---------------------------|
| 爱普生        | TmT88IV | OPOS      |                           |
| 爱普生        | TM-T88V  | OPOS      |                           |
| 星级         | TSP650II | OPOS      |                           |
| 星级         | TSP650II | 自定义    | 连接通过网络     |
| 星级         | TSP100   | OPOS      | 要求 TSP650II 司机 |
| HP           | F7M67AA  | OPOS      | 结算的 USB               |

#### <a name="bar-code-scanner"></a>条码扫描器

| 制造商  | 型号   | 接口 | 评论 |
|---------------|---------|-----------|----------|
| 摩托罗拉      | DS9208  | OPOS      |          |
| 符号        | LS2208  | OPOS      |          |
| 集成的 HP | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN 小键盘

| 制造商 | 型号  | 接口 | 评论                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | 需要付款 Connector 的自定义 |

#### <a name="payment-terminal"></a>付款终端

| 制造商 | 型号 | 接口 | 评论                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| 昼夜平分利      | L5300 | 自定义    | 需要付款 Connector 的自定义                                |
| VeriFone     | MX925 | 自定义    | 需要付款 Connector 的自定义功能；连接和 USB 通过网络 |
| VeriFone     | MX915 | 自定义    | 需要付款 Connector 的自定义功能；连接和 USB 通过网络 |

#### <a name="cash-drawer"></a>银箱

| 制造商 | 型号     | 接口 | 评论              |
|--------------|-----------|-----------|-----------------------|
| APG          | 爱特伍    | 自定义    | 连接通过网络 |
| 星级         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>行显示内容

| 制造商  | 型号   | 接口 | 评论 |
|---------------|---------|-----------|----------|
| 集成的 HP | G6U79AA | OPOS      |          |
| 爱普生         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>签名捕获

| 制造商 | 型号  | 接口 | 评论 |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>比例

| 制造商 | 型号         | 接口 | 评论 |
|--------------|---------------|-----------|----------|
| Datalogic    | 麦哲伦 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| 制造商 | 型号       | 接口 | 评论 |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>共享的 IIS 硬件工作站

以下测试外围使用共享的 IIS 硬件工作站和 Windows 身份的 Modern POS 一起并覆盖 POS。 **注释：**仅付款和终端打印机、银箱支持。

#### <a name="printer"></a>打印机

| 制造商 | 型号    | 接口 | 评论                  |
|--------------|----------|-----------|---------------------------|
| 爱普生        | TmT88IV | OPOS      |                           |
| 爱普生        | TM-T88V  | OPOS      |                           |
| 星级         | TSP650II | OPOS      |                           |
| 星级         | TSP650II | 自定义    | 连接通过网络     |
| 星级         | TSP100   | OPOS      | 要求 TSP650II 司机 |
| HP           | F7M67AA  | OPOS      | 结算的 USB               |

#### <a name="payment-terminal"></a>付款终端

| 制造商 | 型号 | 接口 | 评论                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | 自定义    | 需要付款 Connector 的自定义功能；连接和 USB 通过网络 |
| VeriFone     | MX915 | 自定义    | 需要付款 Connector 的自定义功能；连接和 USB 通过网络 |

#### <a name="cash-drawer"></a>银箱

| 制造商 | 型号     | 接口 | 评论              |
|--------------|-----------|-----------|-----------------------|
| APG          | 爱特伍    | 自定义    | 连接通过网络 |
| 星级         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>疑难解答
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS 可以检测到在其选择列表的硬件工作站的，但是，无法完成。匹配

**解决方案：**请验证潜在的故障积分以下列表：

-   是连续 Modern POS 的计算机委托计算机上运行使用硬件工作站的证书。
    -   若要验证此设置，在查看器，转到下面的 URL:https://Computer&lt;名称&gt;:&lt;端口号&gt;/HardwareStation/ping。
    -   使用 ping 验证此 URL 一计算机，可以访问，并且指示浏览器证书是否委托人。 (例如，在 Internet Explorer，锁图标将地址栏出现。 当您单击此图标时，Internet Explorer 验证证书是否正在委托人。 您可以查看通过查看证书的详细信息)。安装在本地计算机的证书
-   在运行硬件工作站的计算机上，硬件工作站将使用的端口。防火墙已打开。
-   硬件工作站通过运行在硬件工作站安装程序安装时结束的商人信息正确设置工具商人帐户信息。

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>检测 Modern POS 不能在列表其的硬件工作站的选择

**解决方案：**以下因素可能导致此发货之一：

-   硬件工作站尚未在总部设置正确。 使用下一主题{{在此：in}}验证硬件工作站配置文件和硬件工作站正确地输入。
-   作业未运行更新通道配置。 在这种情况下，请运行的作业。1070 配置通道

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS 不反映新银箱设置

**解决方案：**请关闭当前批处理。 更改为银箱没有更新到 Modern POS，关闭当前批处理。

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modern POS 报告与零售外设的发货

**解决方案：**这是此问题的一些典型的原因如下：

-   确保其他设备驱动程序关闭配置实用程序。 如果这些实用程序打开，他们可能会阻止 Modern POS 硬件工作站未申报或设备。
-   如果零售 POS 外设共享与多种设备，请注意它属于到以下类别之一：
    -   银箱
    -   收据打印机
    -   付款终端

    如果不在外围到这些类别之一，硬件工作站不启用设计在多个 POS 中将共享的外围设备。
-   在某些情况下，设备驱动程序可以归入"公共控件对象 (CCOs) 停止正确工作。 设备如果最新安装，但是，无法正常运行。请注意您或其他问题，可以通过重新安装 CCOs 通常解决该问题。 若要下载 CCOs，请访问<http://monroecs.com/oposccos_current.htm>。
-   在测试或故障排除，则期间对频繁的外围更改，您可能必须重置 IIS {{而不是：instead_of}}等待缓存以刷新。 要重置 IIS，请执行以下步骤：
    1.  **从开始**菜单上，CMD ** **类型。
    2.  在搜索结果，右键单击"命令提示符** **，然后单击** **请以管理员身份运行"。
    3.  **在命令提示符窗口** **，键入" iisreset " /Restart **然后按 Enter。
    4.  在 IIS 重新启动后，重新启动 Modern POS。
-   当您对外围设备时的常见的更改，因此，如果您需经常还将开始并退出，从客户 POS 上次 POS 会话的 dllhost 流程可以干涉当前会话。 设备在这种情况下，可能不可用，直到您结算上次会话管理的动态链接库 (DLL) 主机。 若要关闭 DLL 主机，请执行以下步骤：
    1.  **从开始**菜单，请键入**管理器**任务。
    2.  在搜索结果，单击**管理器**任务。
    3.  在任务管理器，** **详细信息，请单击选项卡中标记的列标题名称** **按字母顺序名义上表。
    4.  下移，则在您查找 dllhost.exe。
    5.  选择每 DLL 主机，然后单击** **结束任务。
    6.  主机在 DLL 关闭后，重新启动 Modern POS。


<a name="see-also"></a>请参阅
--------

[零售外围模拟程序] (零售外设 simulator.md)


