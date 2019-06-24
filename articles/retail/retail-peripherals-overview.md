---
title: 零售外设
description: 此主题介绍与零售外设有关的概念。
author: rubencdelgado
manager: AnnBe
ms.date: 01/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a9fa49d0b3553ae70547aeea19d14bc6e6e08983
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577920"
---
# <a name="retail-peripherals"></a>零售外设

[!include [banner](includes/banner.md)]

此主题介绍与零售外设有关的概念。 它描述可用于将外设连接到销售点 (POS) 的各种方法，以及负责管理与 POS 之间的连接的组件。

## <a name="concepts"></a>概念

### <a name="pos-registers"></a>POS 收银机

导航：单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。 销售点 (POS) 收银机是用来定义特定 POS 实例的特征的实体。 这些特征包括硬件配置文件或设置，它们将被零售外设用于收银机、收银机映射到的商店，以及登录该收银机的用户的视觉体验。

### <a name="devices"></a>设备

导航：单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **设备**。 设备是表示映射到 POS 收银机的设备的物理实例的实体。 当创建一个设备时，它被映射到 POS 收银机。 设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。 设备可以映射到以下应用类型：Retail Modern POS、Retail Cloud POS、Retail Modern POS – Windows Phone、Retail Modern POS – Android 和 Retail Modern POS – iOS。

### <a name="retail-modern-pos"></a>Retail Modern POS

Modern POS 是适用于 Microsoft Windows 的 POS 程序。 它可以部署到 Windows 10 操作系统 (OS) 上。

### <a name="cloud-pos"></a>云 POS

Cloud POS 是基于浏览器且可以通过 Web 浏览器访问的 Modern POS 程序版本。

### <a name="modern-pos-for-ios"></a>Modern POS for iOS

Modern POS for iOS 是基于 iOS 且可部署到 iOS 设备上的 Modern POS 程序版本。

### <a name="modern-pos-for-android"></a>Modern POS for Android

Modern POS for Android 是基于 Android 且可部署到 Android 设备上的 Modern POS 程序版本。

### <a name="pos-peripherals"></a>POS 外设

POS 外设是为满足 POS 功能而明确支持的设备。 这些外设通常划分为特定类。 有关这些类的详细信息，请参阅此主题的“设备分类”部分。

### <a name="hardware-station"></a>Hardware Station

导航：单击**零售** &gt; **渠道** &gt; **零售商店** &gt; **所有零售商店**。 选择一个商店，然后单击**硬件工作站**快速选项卡。 **硬件工作站**设置是一种基于渠道的设置，用于定义将部署零售外设逻辑的实例。 渠道级别的此设置用于确定硬件工作站的特征。 还用于列出指定商店中可用于 Modern POS 实例的硬件工作站。 硬件工作站内置在适用于 Windows 的 Modern POS 程序内。 硬件工作站也可以作为单机 Microsoft Internet Information Services (IIS) 程序独立部署。 在这种情况下，可以通过网络访问。

### <a name="hardware-profile"></a>硬件配置文件

导航︰单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。 硬件配置文件是为 POS 收银机或硬件工作站配置的设备的列表。 硬件配置文件可以直接映射到 POS 收银机或硬件工作站。

## <a name="devices-classes"></a>设备分类
POS 外设通常划分为类。 此部分描述并提供 Modern POS 支持的设备的概览。

### <a name="printer"></a>打印机

外设包括传统 POS 收据打印机和整页打印机。 通过适用于 Retail POS (OPOS) 和 Microsoft Windows 的对象链路与嵌入驱动程序接口为打印机提供支持。 最多可以同时使用两台打印机。 此功能支持在收据打印机上打印付现自提的客户收据的方案，虽然包含更多信息的客户订单在整页打印机上打印。 收据打印机可以通过 USB 直接连接到计算机，通过以太网连接到网络，或通过 Bluetooth 连接。

### <a name="scanner"></a>扫描仪

最多可以同时使用两台条码扫描仪。 此功能支持需要移动性更高的扫描仪来扫描体积大或重量高的物品的方案，而嵌入式固定扫描仪则用于大多数标准尺寸的物品或加快收银速度。 可以通过 OPOS、通用 Windows 平台 (UWP) 或键盘 wedge 界面为扫描仪提供支持。 可使用 USB 或 Bluetooth 将扫描仪连接到计算机。

### <a name="msr"></a>MSR

可通过使用 OPOS 设置一台 USB 磁条阅读器 (MSR)。 如果要将单机 MSR 用于电子资金转帐 (EFT) 付款交易，则必须通过付款连接器管理 MSR。. 单机 MSR 可用于独立于付款连接器执行客户会员信息录入、员工签到和礼品卡录入。

### <a name="cash-drawer"></a>银箱

每个硬件配置文件可以支持两个银箱。 此功能允许每台收银机同时被两个班次使用。 为了防止共享班次或一个银箱同时被多个移动 POS 设备使用，每个硬件配置文件仅允许一个银箱。 银箱可以通过 USB 直接连接到计算机，连接到网络，或通过 RJ12 接口连接到收据打印机。 在某些情况下，还可以通过 Bluetooth 连接银箱。

### <a name="line-display"></a>行显示内容

行显示器用于在交易期间向客户显示产品、交易余额和其他有用信息。 可以使用 OPOS 驱动程序通过 USB 将一台行显示器连接到计算机。

### <a name="signature-capture"></a>签名捕获

可以使用 OPOS 驱动程序通过 USB 将签名捕获设备直接连接到计算机。 在配置签名捕获时，将提示客户在设备上签名。 提供签名后，它会对收银员显示，待其接受。

### <a name="scale"></a>比例

可以使用 OPOS 驱动程序通过 USP 将秤连接到计算机。 标记为“已称重”产品的产品添加到交易记录时，POS 从秤读取重量，将该产品添加到交易记录，然后使用秤提供的数量。

### <a name="pin-pad"></a>PIN 小键盘

通过 OPOS 为个人标识号 (PIN) 小键盘提供支持，但是必须通过付款连接器管理 PIN 小键盘。

### <a name="secondary-display"></a>辅助显示器

如果配置了辅助显示器，将使用第二台 Windows 显示器显示基本信息。 辅助显示器用于为独立软件供应商 (ISV) 扩展提供支持，因为原始辅助显示器不可配置，显示的内容有限。

### <a name="payment-device"></a>付款设备

对付款设备的支持通过付款连接器实现。 付款设备可以执行其他设备类提供的一项或多项功能。 例如，一种付款设备可以充当 MSR/卡阅读器、行显示器、签名捕获设备或 PIN 小键盘。 对付款设备的支持独立于为硬件配置文件中包含的其他设备提供的单机设备支持实现。

## <a name="supported-interfaces"></a>支持的接口

### <a name="opos"></a>OPOS

为了帮助确保最大范围的设备可以与 Microsoft Dynamics 365 for Retail 配合使用，OLE for POS 行业标准成为了 Microsoft Dynamics 365 for Retail 中支持的主要零售外设平台。 OLE for POS 标准由美国零售联合会 (NRF) 制订，建立了针对零售外设的行业标准通信协议。 OPOS 是广泛采用的 OLE for POS 标准实施。 它开发于 20 世纪 90 年代，之后经过了多次更新。 OPOS 提供设备驱动程序架构，以便将 POS 硬件与基于 Windows 的 POS 系统轻松集成。 OPOS 控件处理兼容硬件与 POS 软件之间的通信。 OPOS 控件包含两部分：

- **控件对象** – 设备类（如行显示器）的控件对象提供软件程序的界面。 Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) 提供一组标准的 OPOS 控件对象，称为公共控件对象 (CCO)。 CCO 用于测试 Microsoft Dynamics 365 for Retail 的 POS 组件。 因此，如果 Microsoft Dynamics 365 for Retail 通过 OPOS 为设备类提供支持，并且制造商提供为 OPOS 构建的服务对象，此项测试有助于确保可以支持多种设备类型。 无需明确测试每个设备类型。
- **服务对象** – 服务对象提供控件对象 (CCO) 与设备之间的通信。 设备的服务对象通常由设备制造商提供。 但是在某些情况下，您可能必须从制造商的网站下载服务对象。 例如，可能提供了更新的服务对象。 若要查找制造商的网站地址，请参阅您的硬件文档。

[![控件对象和服务对象](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)

对 OLE for POS 的 OPOS 实施的支持有助于确保当设备制造商和 POS 发布商正确实施标准时，POS 系统和支持的设备可以协同工作，即使以前未一起测试时也不例外。

> [!NOTE]
> 支持 OPOS 不保证支持采用了 OPOS 驱动设备的所有设备。 Microsoft Dynamics 365 for Retail 必须首先通过 OPOS 支持该设备类型（或类）。 此外，服务对象可能并非始终安装了最新版本的 CCO。 您还应注意，服务对象的质量往往参差不齐。

### <a name="windows"></a>窗口

POS 的收据打印已针对 OPOS 进行了优化。 OPOS 往往比通过 Windows 打印快得多。 因此，最好使用 OPOS 进行打印，特别是在零售环境中，此类环境中需要打印 40 列收据，并且交易时间必须非常快。 对于大多数设备，您将使用 OPOS 控件。 但是，某些 OPOS 收据打印机也支持 Windows 驱动程序。 通过使用 Windows 驱动程序，您可以通过一台打印机访问多台收银机的最新字体和网络。 但是使用 Windows 驱动程序有一些缺点。 以下是这些缺点的一些示例：

- 使用 Windows 驱动程序时，图像在打印前渲染。 因此，打印速度往往比使用 OPOS 控件的打印机慢。
- 使用 Windows 驱动程序时，通过打印机连接（菊链方式）的设备可能无法正常工作。 例如，银箱可能无法打开，或者票据打印机可能无法正常工作。
- OPOS 还支持特定于零售收据打印机的更多变体集合，如裁纸或票据打印。

如果 OPOS 控件适用于您在使用的 Windows 打印机，该打印机仍然可以与 Microsoft Dynamics 365 for Retail 配合正常工作。

### <a name="universal-windows-platform"></a>通用 Windows 平台

对于零售外设，UWP 与 Windows 对即插即用设备的支持有关。 当即插即用设备连接到支持这种设备的 Windows 操作系统版本时，该设备不需要驱动程序即可正常使用。 例如，如果 Windows 检测到 Bluetooth 扬声器设备，该操作系统知道此设备的类类型为**扬声器**。 因此，它将把此设备视为扬声器。 无需再执行任何设置。 对于 POS 设备，可以插入大量 USB 设备，并且 Windows 将把其识别为人机接口设备 (HID)。 但是，可能不能确定设备提供的功能，因为设备不指定设备的类（即类型）。 在 Windows 10 中，已增加了条码扫描仪 和 MSR 的设备类。 因此，如果设备向 Windows 10 声明自己是这些类之一的设备，Windows 将在相应时间注意来自该设备的事件。 Modern POS 支持 UWP MSR 和扫描仪。 因此，准备好从这些设备之一输入，并且已连接属于这些类之一的设备时，可以使用该设备。 例如，如果在 Windows 10 计算机中插入一台 UWP 条码扫描仪，并且为 Modern POS 配置了条码签到，将在签到屏幕上激活该条码扫描仪。 无需再执行任何设置。 正在向 Windows 添加更多服务点 UWP 设备类。 这些类中包括银箱和收据打印机的类。 Modern POS 中对这些新设备的支持待定。

### <a name="keyboard-wedge"></a>键盘 wedge

键盘 wedge 设备向计算机发送数据，就像数据是从键盘键入的。 因此默认情况下，POS 上的活动字段将收到扫描或刷卡的数据。 在某些情况下，此行为可能导致将错误类型的数据扫描到错误的字段中。 例如，可能将条码扫描到本应输入信用卡数据的字段。 在大多数情况下，POS 中有逻辑可确定扫描的数据是条码还是刷卡。 因此可以正确处理数据。 但是，当设备设置为 OPOS 而不是键盘 wedge 设备时，对来自这些设备的数据的使用方式控制更严格，因为对数据的来源设备的“了解”更深。 例如，来自条码扫描仪的数据自动识别为条码，并且相比过去使用的一般字符串搜索（如使用键盘 wedge 设备时），可以更轻松、更快地找到数据库中的关联记录。

### <a name="native-printer"></a>本机打印机

可以将本机（或“设备”，因为类型是在硬件配置文件中命名的）配置为提示用户选择为计算机配置的打印机。 配置了**设备**类型的打印机时，如果 Modern POS 收到了打印命令，将提示用户在列表中选择打印机。 此行为与 Windows 驱动程序的行为不同，因为硬件配置文件中的 **Windows** 打印机类型不显示打印机列表。 相反，它要求在**设备名称**字段中提供命名的打印机。

### <a name="windows"></a>窗口

**Windows** 设备类型仅用于打印机。 在硬件配置文件中配置了 Windows 打印机时，必须指定具体的打印机名称。 在 Modern POS 遇到打印事件时，如果配置了 Windows 打印机，将把该事件传递到指定的 Windows 打印机。 将不提示用户选择打印机。

### <a name="network"></a>网络

可通过 Modern POS for Windows 应用程序中内置的进程间通信 (IPC) 硬件工作站或其他 Modern POS 客户端的 IIS 硬件工作站，通过网络使用网络可寻址银箱、收据打印机和付款终端。

## <a name="hardware-station-deployment-options"></a>硬件工作站部署选项

### <a name="ipc-built-in"></a>IPC（内置）

进程间通信 (IPC) 硬件工作站内置在 Modern POS for Windows 应用程序中。 若要使用 IPC 硬件工作站，请为将使用 Modern POS for Windows 应用程序的收银机分配硬件配置文件。 然后为将使用该收银机的商店创建一个类型为**专用**的硬件工作站。 启动 Modern POS 时，将激活 IPC 硬件工作站，而已配置的 POS 外设将准备就绪，可供使用。 如果因为某种原因暂时不需要本地硬件，请使用**管理硬件工作站**关闭硬件工作站功能。 Modern POS 也可以使用 IPC 硬件工作站直接与网络外设通信。

### <a name="iis"></a>IIS

可以通过两种方式使用硬件工作站的 IIS 或单机版本。 描述符“IIS”暗示 POS 应用程序通过 Microsoft Internet Information Services 连接到硬件工作站。 POS 应用程序通过连接设备的计算机上运行的 Web 服务连接到 IIS 硬件工作站。 使用 IIS 时，与 IIS 硬件工作站在同一个网络中的任何 POS 收银机都可以使用与该硬件工作站相连的零售外设。 由于只有 Modern POS for Windows 中才包含对零售外设的内置支持，所以其他所有 Modern POS 应用程序都必须使用 IIS 硬件工作站才能与硬件配置文件中配置的 POS 外设通信。 因此，IIS 硬件工作站的每个实例都需要运行与设备通信的 Web 服务和应用程序的计算机。 所有非 Windows Modern POS 应用程序都需要 IIS 硬件工作站。

#### <a name="dedicated"></a>专门

Modern POS 使用**专用**类型的硬件工作站检测外设是否直接连接到正在使用该应用程序的计算机。 但是，**专用**类型也可用于 IIS 硬件工作站。 在将 Cloud POS 用作 POS 应用程序的传统固定式 POS 方案中，**专用**硬件工作站用于运行 Cloud POS 的同一计算机上部署的 IIS 硬件工作站。 从零售外设的角度，专用 IIS 硬件工作站对零售外设的支持比传统的固定式 POS 方案更出色。 专用硬件工作站支持硬件配置文件中支持的所有外设。

#### <a name="shared"></a>共享的

共享硬件工作站应该可以全天供多个 POS 设备使用。 共享硬件工作站已经过优化，只能支持银箱、收据打印机和付款终端。 不能直接连接单机条码扫描仪、行显示器，MSR、秤或其他设备。 否则，多个 POS 设备同时尝试声明这些外设时，将发生冲突。 下面是如何管理受支持设备的冲突：

- **银箱** – 银箱通过发送到设备的事件打开。 仅当银箱已打开时，才会在调用银箱时发生问题。 对于共享硬件工作站，应在硬件配置文件中将银箱设置为**共享**。 发送打开命令时，此设置阻止 POS 检查银箱是否已打开。
- **收据打印机** – 如果同时向硬件工作站发送两条收据打印命令，可能丢失其中一条命令，具体取决于设备。 某些设备有内存或池，可以防止此问题。 如果打印命令不成功，收银员将收到错误消息，可以从 POS 重试该打印命令。
- **付款终端** – 如果收银员尝试在已在使用的付款终端上处理交易的支付，将显示消息，通知收银员正在使用该终端，请收银员稍后重试。 通常，收银员可以看到终端已在使用并等待其他交易完成，再尝试处理付款。

为将来的版本计划了验证，以便检测是否为映射到共享硬件工作站的硬件配置文件设置了不受支持的设备。 如果检测到不受支持的设备，用户将收到消息，说明共享硬件工作站不支持这些设备。 对于共享硬件工作站，**付款后即可选择**选项在收银机级别设置为**是**。 然后在 POS 中为交易选择了付款时，将提示 POS 用户选择硬件工作站。 仅在付款时选择了硬件工作站时，将把对硬件工作站的选择直接添加到移动方案的 POS 工作流。 额外福利是，付款终端上的行显示器不用于共享方案。 如果付款终端用作行显示器，交易完成前，可能阻止其他用户使用该终端。 在移动方案中，可能在较长一段时间内向交易添加行。 因此，需要**付款后即可选择**选项以确保最适宜的设备可用性。

### <a name="network-peripherals"></a>网络外设

硬件配置文件中为设备指派的网络让银箱、收据打印机和付款终端可以通过网络连接来连接。

#### <a name="modern-pos-for-windows"></a>Modern POS for Windows

可以为两处的网络外设指定 IP 地址。 如果 Modern POS Windows 客户端使用一组网络外设，您应该通过使用收银机自身的“操作窗格”上的 **IP 配置**选项为这些设备设置 IP 地址。 对于将在 POS 收银机之间共享的网络设备，可以将为其指派的硬件配置文件直接映射到共享硬件工作站。 若要分配 IP 地址，请在**零售商店**页中选择该硬件工作站，然后使用**硬件工作站**部分中的 **IP 配置**选项指定为该硬件工作站分配的网络设备。 对于只有网络设备的硬件工作站，则不必部署硬件工作站本身。 在这种情况下，仅当要在概念上根据可网络寻址的设备在零售商店中的位置为这些设备分组时，才需要硬件工作站。

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Cloud POS、Modern POS for iOS 和 Modern POS for Android

硬件工作站中包含驱动以物理方式相连且可网络寻址的外设的逻辑。 因此，对于除 Modern POS for Windows 之外的所有 POS 客户端，必须部署并激活 IIS 硬件工作站，以便让 POS 可以与外设通信，无论这些外设是以物理方式连接到硬件工作站还是通过网络寻址。

## <a name="setup-and-configuration"></a>设置和配置

### <a name="hardware-station-installation"></a>硬件工作站安装

有关新信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS for Windows 设置和配置

有关信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。

### <a name="opos-device-setup-and-configuration"></a>OPOS 设备设置和配置

有关 OPOS 组件的详细信息，请参阅本文的“支持的接口”。 OPOS 驱动程序通常由设备制造商提供。 安装 OPOS 设备驱动程序时，将在 Windows 注册表中的以下位置添加一个键：

- **32 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
- **64 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

在 ServiceOPOS 注册表位置中，配置的设备根据 OPOS 设备类组织。 将保存多个设备驱动程序。

## <a name="supported-scenarios-by-hardware-station-type"></a>硬件工作站类型支持的方案

### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>客户端支持 – IPC 硬件工作站与 IIS 硬件工作站

下表显示支持的拓扑和部署方案。

| 客户      | IPC 硬件工作站 | IIS 硬件工作站 |
|-------------|----------------------|----------------------|
| Windows 应用程序 | 是                  | 是                  |
| 云 POS   | 无                   | 是                  |
| Android     | 无                   | 是                  |
| iOS         | 无                   | 是                  |

### <a name="network-peripherals"></a>网络外设

可以直接通过 Modern POS for Windows 应用程序中内置的硬件工作站支持网络外设。 对于其他所有客户端，则必须部署 IIS 硬件工作站。

| 客户      | IPC 硬件工作站 | IIS 硬件工作站 |
|-------------|----------------------|----------------------|
| Windows 应用程序 | 是                  | 是                  |
| 云 POS   | 无                   | 是                  |
| Android     | 无                   | 是                  |
| iOS         | 无                   | 是                  |

## <a name="supported-device-types-by-hardware-station-type"></a>硬件工作站类型支持的设备类型

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>带 IPC（内置）硬件工作站的 Modern POS for Windows

<table>
<thead>
<tr>
<th>支持的设备类</th>
<th>支持的接口</th>
</tr>
</thead>
<tbody>
<tr>
<td>打印机</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>设备</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>打印机 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>设备</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>行显示内容</td>
<td>OPOS</td>
</tr>
<tr>
<td>双显示器</td>
<td>Windows 驱动程序</td>
</tr>
<tr>
<td>MSR</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP（不需要设置。）</li>
<li>键盘 wedge（不需要设置。）</li>
</ul>
</td>
</tr>
<tr>
<td>开票人</td>
<td>
<ul>
<li>OPOS</li>
<li>网络
<p><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>开票人 2</td>
<td>
<ul>
<li>OPOS</li>
<li>网络
<p><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>扫描仪</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP（不需要设置。）</li>
<li>键盘 wedge（不需要设置。）</li>
</ul>
</td>
</tr>
<tr>
<td>扫描仪 2</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP（不需要设置。）</li>
<li>键盘 wedge（不需要设置。）</li>
</ul>
</td>
</tr>
<tr>
<td>比例</td>
<td>OPOS</td>
</tr>
<tr>
<td>PIN 小键盘</td>
<td>OPOS（通过自定义付款连接器提供支持。）</td>
</tr>
<tr>
<td>签名捕获</td>
<td>OPOS</td>
</tr>
<tr>
<td>付款终端</td>
<td>
<ul>
<li>自定义设备支持</li>
<li>网络（有关详细信息，请参阅付款连接器文档。）</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>有专用 IIS 硬件工作站的所有 Modern POS 客户端

> [!NOTE]
> 当 IIS 硬件工作站为“专用”时，POS 客户端与硬件工作站之间存在一对一关系。

<table>
<thead>
<tr>
<th>支持的设备类</th>
<th>支持的接口</th>
</tr>
</thead>
<tbody>
<tr>
<td>打印机</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows 驱动程序
<p><strong>注意</strong>：对于网络中的 Windows 打印机，硬件工作站的用户必须有权访问该打印机。</p>
</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>打印机 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>行显示内容</td>
<td>OPOS</td>
</tr>
<tr>
<td>MSR</td>
<td>OPOS</td>
</tr>
<tr>
<td>开票人</td>
<td>
<ul>
<li>OPOS</li>
<li>网络
<p><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>开票人 2</td>
<td>
<ul>
<li>OPOS</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>扫描仪</td>
<td>OPOS</td>
</tr>
<tr>
<td>扫描仪 2</td>
<td>OPOS</td>
</tr>
<tr>
<td>比例</td>
<td>OPOS</td>
</tr>
<tr>
<td>PIN 小键盘</td>
<td>OPOS（通过自定义付款连接器提供支持。）</td>
</tr>
<tr>
<td>签到 捕获</td>
<td>OPOS</td>
</tr>
<tr>
<td>付款终端</td>
<td>
<ul>
<li>自定义设备支持</li>
<li>网络（有关详细信息，请参阅付款连接器文档。）</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>有共享 IIS 硬件工作站的所有 Modern POS 客户端

> [!NOTE]
> 当 IIS 硬件工作站为“共享”时，多台设备可同时使用该硬件工作站。 对于此方案，应仅使用下表中列出的设备。 如果尝试共享此处未列出的设备（如条码扫描仪和 MSR），多台设备尝试声明同一外设时，将出错。 将来将明确阻止此类配置。

<table>
<thead>
<tr>
<th>支持的设备类</th>
<th>支持的接口</th>
</tr>
</thead>
<tbody>
<tr>
<td>打印机</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows 驱动程序
<p><strong>注意</strong>：对于网络中的 Windows 打印机，硬件工作站的用户必须有权访问该打印机。</p>
</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>打印机 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows 驱动程序</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>开票人</td>
<td>
<ul>
<li>OPOS</li>
<li>网络
<p><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>开票人 2</td>
<td>
<ul>
<li>OPOS</li>
<li>网络</li>
</ul>
</td>
</tr>
<tr>
<td>付款终端</td>
<td>
<ul>
<li>自定义设备支持</li>
<li>网络（有关详细信息，请参阅付款连接器文档。）</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>支持的方案的配置

有关如何创建硬件配置文件的详细信息，请参阅[定义和维护渠道客户端，包括收银机和硬件工作站](define-maintain-channel-clients-registers-hw-stations.md)。

> [!NOTE]
> 对于 Microsoft Dynamics 365 for Retail 版本 1611，将不再使用硬件工作站配置文件。 以前在硬件工作站中设置的属性现在成为了硬件工作站本身的一部分。

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>带 IPC（内置）硬件工作站的 Modern POS for Windows

此配置是传统固定式 POS 收银机最典型的配置。 对于此方案，硬件配置文件信息直接映射到收银机。 还必须在收银机本身中设置 EFT 终端号。 若要设置此配置，请执行以下步骤。

1. 创建在其中配置所有所需外设的硬件配置文件。
2. 将硬件配置文件映射到 POS 收银机。
3. 为将使用该 POS 收银机的零售商店创建一个类型为**专用**的硬件工作站。 描述可选。

    > [!NOTE]
    > 不必在硬件工作站中设置其他任何属性。 其他所有所需信息（如硬件配置文件）将来自收银机本身。

4. 单击**零售** &gt; **零售 IT** &gt; **配送计划**。
5. 选择 **1090** 配送计划，将新硬件配置文件同步到商店。 单击**立即运行**将更改同步到 POS。
6. 选择 **1040** 配送计划，将新硬件工作站同步到商店。 单击**立即运行**将更改同步到 POS。
7. 安装并激活 Modern POS for Windows。
8. 启动 Modern POS for Windows，然后登录到连接的外设。

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>有专用 IIS 硬件工作站的所有 Modern POS 客户端

可将此配置用于有一个硬件工作站仅供一台 POS 收银机专用的所有 Modern POS 客户端。 若要设置此配置，请执行以下步骤。

1. 创建在其中配置所有所需外设的硬件配置文件。
2. 为将使用该 POS 收银机的零售商店创建一个类型为**专用**的硬件工作站。
3. 在专用硬件工作站中，设置以下属性：

    - **主机名** – 将运行硬件工作站的主计算机的名称。

        > [!NOTE]
        > Cloud POS 可以解析 **localhost** 以确定运行 Cloud POS 的本地计算机。 但是，将 Cloud POS 与硬件工作站配对所需证书必须也采用“Localhost”来充当计算机名称。 若要避免问题，建议您根据列出商店每个专用硬件工作站的实例。 对于每个硬件工作站，主机名应该是将部署硬件工作站的具体计算机名称。

    - **端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。
    - **硬件配置文件** – 如果硬件工作站本身中不提供硬件配置文件，将使用为收银机分配的硬件配置文件。
    - **EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。 此 ID 由信用卡处理方提供。
    - **包名** – 部署硬件工作站时要使用的硬件工作站包。

4. 单击**零售** &gt; **零售 IT** &gt; **配送计划**。
5. 选择 **1090** 配送计划，将新硬件配置文件同步到商店。 单击**立即运行**将更改同步到 POS。
6. 选择 **1040** 配送计划，将新硬件工作站同步到商店。 单击**立即运行**将更改同步到 POS。
7. 安装硬件工作站。 有关如何安装硬件工作站的详细信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。
8. 安装和激活 Modern POS。 有关如何安装 Modern POS 的详细信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。
9. 登录 Modern POS，然后选择**执行非开票人操作**。
10. 启动**管理硬件工作站**操作。
11. 单击**管理**。
12. 在硬件工作站管理页中，设置用于打开硬件工作站的选项。
13. 选择要使用的硬件工作站，然后单击**配对**。
14. 在硬件工作站配对后，单击**关闭**。
15. 在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>有共享 IIS 硬件工作站的所有 Modern POS 客户端

此配置可用于与其他设备共享硬件工作站的所有 Modern POS 客户端。 若要设置此配置，请执行以下步骤。

1. 创建在其中配置所需外设的硬件配置文件。
2. 为将使用该 POS 收银机的零售商店创建一个类型为**共享**的硬件工作站。
3. 在共享硬件工作站中，设置以下属性：

    - **主机名** – 将运行硬件工作站的主计算机的名称。
    - **描述** – 用于帮助识别硬件工作站的文本，如**退货**或**店前**。
    - **端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。
    - **硬件配置文件** – 对于共享硬件工作站，每个硬件工作站都应该有一个硬件配置文件。 可以在硬件工作站之间共享硬件配置文件，但必须将其映射到每个硬件工作站。 此外，建议在多个设备共享同一个共享硬件工作站时使用共享班次。 若要设置共享班次，单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。 对于每个共享硬件配置文件，选择银箱，然后将**共享班次银箱**选项设置为**是**。
    - **EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。 此 ID 由信用卡处理方提供。
    - **包名** – 部署硬件工作站时要使用的硬件工作站包。

4. 为商店中所需其他每个硬件工作站重复步骤 2 和 3。
5. 单击**零售** &gt; **零售 IT** &gt; **配送计划**。
6. 选择 **1090** 配送计划，将新硬件配置文件同步到商店。 单击**立即运行**将更改同步到 POS。
7. 选择 **1040** 配送计划，将新硬件工作站同步到商店。 单击**立即运行**将更改同步到 POS。
8. 在步骤 2 和 3 中设置的每个主机上安装硬件工作站。 有关如何安装硬件工作站的详细信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。
9. 安装和激活 Modern POS。 有关如何安装 Modern POS 的详细信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。
10. 登录 Modern POS，然后选择**执行非开票人操作**。
11. 启动**管理硬件工作站**操作。
12. 单击**管理**。
13. 在硬件工作站管理页中，设置用于打开硬件工作站的选项。
14. 选择要使用的硬件工作站，然后单击**配对**。
15. 为 Modern POS 将使用的每个硬件工作站重复步骤 14。
16. 为所需全部硬件工作站配对之后，单击**关闭**。
17. 在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。

    > [!NOTE]
    > 如果设备经常使用不同硬件工作站，建议将 Modern POS 配置为收银员开始收款过程时提示其选择硬件工作站。 单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。 选择收银机，然后将**收款后即可选择**选项设置为**是**。 使用 **1090** 配送计划将更改同步到渠道数据库。

## <a name="extensibility"></a>可扩展性

有关硬件工作站的可扩展性方案的信息，请参阅[硬件工作站可扩展性](dev-itpro/hardware-station-extensibility.md)。

## <a name="security"></a>安全性

根据当前安全标准，以下设置应用于生产环境：

> [!NOTE]
> 硬件工作站安装程序将在安装期间通过自助服务自动执行这些注册表编辑。

- 应禁用安全套接字层 (SSL)。
- 应启用并使用传输层安全性 (TLS) 版本 1.2（或当前最高版本）。

    > [!NOTE]
    > 默认情况下，已禁用 SSL 和除 TLS 1.2 外的所有 TLS 版本。

    要编辑或启用这些值，请执行以下步骤：

    1. 按 Windows 徽标键+R 打开**运行**窗口。
    2. 在**打开**字段中，键入 **Regedit**，然后单击**确定**。
    3. 如果显示**用户帐户控制**消息框，请单击**是**。
    4. 在**注册表编辑器**窗口中，导航至 **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**。 以自动输入了以下键，以便仅允许 TLS 1.2。

        - TLS 1.2Server:Enabled=1
        - TLS 1.2Server:DisabledByDefault=0
        - TLS 1.2Client:Enabled=1
        - TLS 1.2Client:DisabledByDefault=0
        - TLS 1.1Server:Enabled=0
        - TLS 1.1Client:Enabled=0
        - TLS 1.0Server:Enabled=0
        - TLS 1.0Client:Enabled=0
        - SSL 3.0Server:Enabled=0
        - SSL 3.0Client:Enabled=0
        - SSL 2.0Server:Enabled=0
        - SSL 2.0Client:Enabled=0

- 除非已知的具体原因所需，否则不应开放其他任何网络端口。
- 必须禁用跨源资源共享，并且必须指定允许接受的源。
- 应仅使用可信证书机构获取将在运行硬件工作站的计算机上使用的证书。

> [!NOTE]
> 请务必仔细阅读 IIS 和 Payment Card Industry (PCI) 要求的安全指南。

## <a name="peripheral-simulator"></a>外围设备模拟器

有关信息，请参阅 [Retail 外设模拟器](dev-itpro/retail-peripheral-simulator.md)。

## <a name="microsoft-tested-peripheral-devices"></a>经过 Microsoft 测试的外设

### <a name="ipc-built-in-hardware-station"></a>IPC（内置）硬件工作站

已通过 Modern POS for Windows 中的内置 IPC 硬件工作站测试了以下外设。

#### <a name="printer"></a>打印机

| 制造商 | 型号    | 接口 | 评论                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | 自定义    | 通过网络连接   |
| Star         | mPOP     | OPOS      | 通过 Bluetooth 连接 |
| HP           | F7M67AA  | OPOS      | 带电 USB             |

#### <a name="bar-code-scanner"></a>条码扫描仪

| 制造商  | 型号         | 接口 | 评论 |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| 符号        | LS2208        | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN 小键盘

| 制造商 | 型号  | 接口 | 评论                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | 需要自定义付款连接器 |

#### <a name="payment-terminal"></a>付款终端

| 制造商 | 型号 | 接口 | 评论                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | 自定义    | 需要自定义付款连接器                                |
| VeriFone     | MX925 | 自定义    | 需要自定义付款连接器；通过网络和 USB 连接 |
| VeriFone     | MX915 | 自定义    | 需要自定义付款连接器；通过网络和 USB 连接 |

#### <a name="cash-drawer"></a>银箱

| 制造商 | 型号     | 接口 | 评论                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | 通过 Bluetooth 连接 |
| APG          | Atwood    | 自定义    | 通过网络连接   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>行显示内容

| 制造商  | 型号   | 接口 | 评论 |
|---------------|---------|-----------|----------|
| HP Integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>签名捕获

| 制造商 | 型号  | 接口 | 评论 |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>比例

| 制造商 | 型号         | 接口 | 评论 |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| 制造商 | 型号       | 接口 | 评论 |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>专用 IIS 硬件工作站

已使用专用（而非共享）IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。

#### <a name="printer"></a>打印机

| 制造商 | 型号    | 接口 | 评论                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | 自定义    | 通过网络连接     |
| HP           | F7M67AA  | OPOS      | 带电 USB               |

#### <a name="bar-code-scanner"></a>条码扫描仪

| 制造商  | 型号   | 接口 | 评论 |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| 符号        | LS2208  | OPOS      |          |
| HP Integrated | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN 小键盘

| 制造商 | 型号  | 接口 | 评论                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | 需要自定义付款连接器 |

#### <a name="payment-terminal"></a>付款终端

| 制造商 | 型号 | 接口 | 评论                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | 自定义    | 需要自定义付款连接器                                |
| VeriFone     | MX925 | 自定义    | 需要自定义付款连接器；通过网络和 USB 连接 |
| VeriFone     | MX915 | 自定义    | 需要自定义付款连接器；通过网络和 USB 连接 |

#### <a name="cash-drawer"></a>银箱

| 制造商 | 型号     | 接口 | 评论              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | 自定义    | 通过网络连接 |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>行显示内容

| 制造商  | 型号   | 接口 | 评论 |
|---------------|---------|-----------|----------|
| HP Integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>签名捕获

| 制造商 | 型号  | 接口 | 评论 |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>比例

| 制造商 | 型号         | 接口 | 评论 |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| 制造商 | 型号       | 接口 | 评论 |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>共享 IIS 硬件工作站

已使用共享 IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。

> [!NOTE]
> 仅支持打印机、付款终端和银箱。

#### <a name="printer"></a>打印机

| 制造商 | 型号    | 接口 | 评论                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | 自定义    | 通过网络连接     |
| HP           | F7M67AA  | OPOS      | 带电 USB               |

#### <a name="payment-terminal"></a>付款终端

| 制造商 | 型号 | 接口 | 评论                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | 自定义    | 需要自定义付款连接器；通过网络和 USB 连接 |
| VeriFone     | MX915 | 自定义    | 需要自定义付款连接器；通过网络和 USB 连接 |

#### <a name="cash-drawer"></a>银箱

| 制造商 | 型号     | 接口 | 评论              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | 自定义    | 通过网络连接 |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>疑难解答

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS 可以在其列表中检测硬件工作站以进行选择，但是不能完成配对。

**解决方案：** 验证以下潜在故障点列表：

- 运行 Modern POS 的计算机信任运行硬件工作站的计算机上使用的证书。

    - 若要验证此设置，请转至以下 URL：`https://<Computer Name>:<Port Number>/HardwareStation/ping`。
    - 此 URL 使用 ping 验证计算机是否可访问，而浏览器则指示证书是否可信。 （例如，在 Internet Explorer 中，地址栏中显示锁图标。 当您单击此图标时，Internet Explorer 验证证书当前是否可信。 您可以通过查看显示的证书的详细信息，将证书安装到本地计算机上。）

- 在运行硬件工作站的计算机上，防火墙中将打开硬件工作站使用的端口。
- 硬件工作站已通过硬件工作站安装程序结束时运行的安装商家信息工具正确安装了商家帐户信息。

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS 不能在其列表中检测到硬件工作站来进行选择。

**解决方案：** 以下因素之一可能导致此问题：

- 硬件工作站尚未在总部正确设置。 使用本主题前面的步骤验证是否正确输入了硬件工作站配置文件和硬件工作站。
- 尚未运行作业以更新渠道配置。 在这种情况下，请运行作业 1070 以配置渠道。

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS 不体现新的银箱设置

**解决方案：** 关闭当前批处理。 关闭当前批处理之前，不会将对银箱的更改更新到 Modern POS。

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modern POS 报告零售外设有问题

**解决方案：** 下面是此问题的一些典型原因：

- 确保关闭了其他设备驱动程序配置实用程序。 如果打开了这些实用程序，可能会阻止 Modern POS 或硬件工作站声明设备。
- 如果将零售外设与多台 POS 设备共享，请确保其属于以下类别之一：

    - 银箱
    - 收据打印机
    - 付款终端

    如果外设不属于这些类别之一，则硬件工作站的设计不支持在多台 POS 设备之间共享该外设。

- 有时，设备驱动程序可能导致公共控件对象 (CCO) 停止正常工作。 如果最近安装了设备，但是该设备无法正常工作，或您发现了其他问题，通常可以通过重新安装 CCO 来解决问题。 若要下载 CCO，请访问 <http://monroecs.com/oposccos_current.htm>。
- 如果在测试或故障排除期间频繁更改外设，可能必须重置 IIS，而不是等待高速缓存自行刷新。 若要重置 IIS，请执行以下步骤:

    1. 在**开始**菜单中键入 **CMD**。
    2. 在搜索结果中，右键单击**命令提示符**，然后单击**以管理员身份运行**。
    3. 在**命令提示符**窗口中，键入 **iisreset /Restart**，然后按 Enter。
    4. IIS 重新启动后，重新启动 Modern POS。

- 频繁更改外设时，如果也频繁启动和退出 POS 客户端，则上一个 POS 会话的 dllhost 进程可能干扰当前会话。 在这种情况下，关闭正在管理上一个会话的动态链接库 (DLL) 主机之前，设备可能不可用。 若要关闭 DLL 主机，请执行以下步骤：

    1. 在**开始**菜单中键入**任务管理器**。
    2. 在搜索结果中，单击**任务管理器**。
    3. 在“任务管理器”中的**详细信息**选项卡上，单击带有**名称**标签的列标题，按名称以字母顺序为表排序。
    4. 向下滚动，直到找到 dllhost.exe。
    5. 选择每个 DLL 主机，然后单击**结束任何**。
    6. 关闭 DLL 主机后，重新启动 Modern POS。

## <a name="additional-resources"></a>其他资源

[零售外围设备模拟器](dev-itpro/retail-peripheral-simulator.md)
