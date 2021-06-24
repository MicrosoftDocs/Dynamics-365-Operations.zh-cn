---
title: 外围设备
description: 此主题介绍与商业外设有关的概念。
author: rubencdelgado
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 833eb271b15dd6d32501049ce9154022a388f1d4
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189567"
---
# <a name="peripherals"></a><span data-ttu-id="30424-103">外围设备</span><span class="sxs-lookup"><span data-stu-id="30424-103">Peripherals</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="30424-104">此主题介绍与商店外设有关的概念。</span><span class="sxs-lookup"><span data-stu-id="30424-104">This topic explains the concepts that are related to store peripherals.</span></span> <span data-ttu-id="30424-105">它描述可用于将外设连接到销售点 (POS) 的各种方法，以及负责管理与 POS 之间的连接的组件。</span><span class="sxs-lookup"><span data-stu-id="30424-105">It describes the various ways that peripherals can be connected to the point of sale (POS) and the components that are responsible for managing the connection with the POS.</span></span>

## <a name="concepts"></a><span data-ttu-id="30424-106">概念</span><span class="sxs-lookup"><span data-stu-id="30424-106">Concepts</span></span>

### <a name="pos-registers"></a><span data-ttu-id="30424-107">POS 收银机</span><span class="sxs-lookup"><span data-stu-id="30424-107">POS registers</span></span>

<span data-ttu-id="30424-108">导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="30424-108">Navigation: Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="30424-109">销售点 (POS) 收银机是用来定义特定 POS 实例的特征的实体。</span><span class="sxs-lookup"><span data-stu-id="30424-109">The point of sale (POS) register is an entity that is used to define the characteristics of a specific instance of the POS.</span></span> <span data-ttu-id="30424-110">这些特征包括外设的硬件配置文件或设置，它们将被用于收银机、收银机映射到的商店，以及登录该收银机的用户的视觉体验。</span><span class="sxs-lookup"><span data-stu-id="30424-110">These characteristics include the hardware profile or setup for peripherals that will be used at the register, the store that the register is mapped to, and the visual experience for the user who signs in to that register.</span></span>

### <a name="devices"></a><span data-ttu-id="30424-111">设备</span><span class="sxs-lookup"><span data-stu-id="30424-111">Devices</span></span>

<span data-ttu-id="30424-112">导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **设备**。</span><span class="sxs-lookup"><span data-stu-id="30424-112">Navigation: Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**.</span></span> <span data-ttu-id="30424-113">设备是表示映射到 POS 收银机的设备的物理实例的实体。</span><span class="sxs-lookup"><span data-stu-id="30424-113">A device is an entity that represents a physical instance of a device that is mapped to a POS register.</span></span> <span data-ttu-id="30424-114">当创建一个设备时，它被映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="30424-114">When a device is created, it’s mapped to a POS register.</span></span> <span data-ttu-id="30424-115">设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。</span><span class="sxs-lookup"><span data-stu-id="30424-115">The device entity tracks information about when a POS register is activated, the type of client that is being used, and the application package that has been deployed to a specific device.</span></span> 

<span data-ttu-id="30424-116">设备可以映射到以下应用类型：Retail Modern POS、Retail Cloud POS、Retail Modern POS – Windows Phone、Retail Modern POS – Android 和 Retail Modern POS – iOS。</span><span class="sxs-lookup"><span data-stu-id="30424-116">Devices can be mapped to the following application types: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android, and Retail Modern POS – iOS.</span></span>

### <a name="modern-pos"></a><span data-ttu-id="30424-117">现代 POS 机</span><span class="sxs-lookup"><span data-stu-id="30424-117">Modern POS</span></span>

<span data-ttu-id="30424-118">Modern POS 是适用于 Microsoft Windows 的 POS 程序。</span><span class="sxs-lookup"><span data-stu-id="30424-118">Modern POS is the POS program for Microsoft Windows.</span></span> <span data-ttu-id="30424-119">它可以部署到 Windows 10 操作系统 (OS) 上。</span><span class="sxs-lookup"><span data-stu-id="30424-119">It can be deployed on Windows 10 operating systems (OSs).</span></span>

### <a name="cloud-pos"></a><span data-ttu-id="30424-120">云 POS</span><span class="sxs-lookup"><span data-stu-id="30424-120">Cloud POS</span></span>

<span data-ttu-id="30424-121">Cloud POS 是基于浏览器且可以通过 Web 浏览器访问的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="30424-121">Cloud POS is a browser-based version of the Modern POS program that can be accessed in a web browser.</span></span>

### <a name="modern-pos-for-ios"></a><span data-ttu-id="30424-122">Modern POS for iOS</span><span class="sxs-lookup"><span data-stu-id="30424-122">Modern POS for iOS</span></span>

<span data-ttu-id="30424-123">Modern POS for iOS 是基于 iOS 且可部署到 iOS 设备上的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="30424-123">Modern POS for iOS is an iOS-based version of the Modern POS program that can be deployed on iOS devices.</span></span>

### <a name="modern-pos-for-android"></a><span data-ttu-id="30424-124">Modern POS for Android</span><span class="sxs-lookup"><span data-stu-id="30424-124">Modern POS for Android</span></span>

<span data-ttu-id="30424-125">Modern POS for Android 是基于 Android 且可部署到 Android 设备上的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="30424-125">Modern POS for Android is an Android-based version of the Modern POS program that can be deployed on Android devices.</span></span>

### <a name="pos-peripherals"></a><span data-ttu-id="30424-126">POS 外设</span><span class="sxs-lookup"><span data-stu-id="30424-126">POS peripherals</span></span>

<span data-ttu-id="30424-127">POS 外设是为满足 POS 功能而明确支持的设备。</span><span class="sxs-lookup"><span data-stu-id="30424-127">POS peripherals are devices that are explicitly supported for POS functions.</span></span> <span data-ttu-id="30424-128">这些外设通常划分为特定类。</span><span class="sxs-lookup"><span data-stu-id="30424-128">These peripherals are typically divided into specific classes.</span></span> <span data-ttu-id="30424-129">有关这些类的详细信息，请参阅此主题的“设备分类”部分。</span><span class="sxs-lookup"><span data-stu-id="30424-129">For more information about these classes, see the “Device classes” section of this topic.</span></span>

### <a name="hardware-station"></a><span data-ttu-id="30424-130">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="30424-130">Hardware station</span></span>

<span data-ttu-id="30424-131">导航：单击 **Retail 和 Commerce** &gt; **渠道** &gt; **商店** &gt; **所有商店**。</span><span class="sxs-lookup"><span data-stu-id="30424-131">Navigation: Click **Retail and Commerce** &gt; **Channels** &gt; **Stores** &gt; **All stores**.</span></span> <span data-ttu-id="30424-132">选择一个商店，然后单击 **硬件工作站** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="30424-132">Select a store, and then click the **Hardware stations** FastTab.</span></span> <span data-ttu-id="30424-133">**硬件工作站** 设置是一种基于渠道的设置，用于定义将部署外设逻辑的实例。</span><span class="sxs-lookup"><span data-stu-id="30424-133">The **Hardware station** setting is a channel-level setting that is used to define instances where the peripheral logic will be deployed.</span></span> <span data-ttu-id="30424-134">渠道级别的此设置用于确定硬件工作站的特征。</span><span class="sxs-lookup"><span data-stu-id="30424-134">This setting at the channel level is used to determine characteristics of the hardware station.</span></span> <span data-ttu-id="30424-135">还用于列出指定商店中可用于 Modern POS 实例的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-135">It's also used to list hardware stations that are available for a Modern POS instance in a given store.</span></span> <span data-ttu-id="30424-136">硬件工作站内置在适用于 Windows 和 Android 的 Modern POS 程序内。</span><span class="sxs-lookup"><span data-stu-id="30424-136">The hardware station is built into the Modern POS programs for Windows and Android.</span></span> <span data-ttu-id="30424-137">硬件工作站也可以作为单机 Microsoft Internet Information Services (IIS) 程序独立部署。</span><span class="sxs-lookup"><span data-stu-id="30424-137">The hardware station can also be deployed independently as a stand-alone Microsoft Internet Information Services (IIS) program.</span></span> <span data-ttu-id="30424-138">在这种情况下，可以通过网络访问。</span><span class="sxs-lookup"><span data-stu-id="30424-138">In this case, it is accessed via network.</span></span>

### <a name="hardware-profile"></a><span data-ttu-id="30424-139">硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="30424-139">Hardware profile</span></span>

<span data-ttu-id="30424-140">导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="30424-140">Navigation: Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="30424-141">硬件配置文件是为 POS 收银机或硬件工作站配置的设备的列表。</span><span class="sxs-lookup"><span data-stu-id="30424-141">The hardware profile is a list of devices that are configured for a POS register or a hardware station.</span></span> <span data-ttu-id="30424-142">硬件配置文件可以直接映射到 POS 收银机或硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-142">The hardware profile can be mapped directly to a POS register or a hardware station.</span></span>

## <a name="devices-classes"></a><span data-ttu-id="30424-143">设备分类</span><span class="sxs-lookup"><span data-stu-id="30424-143">Devices classes</span></span>
<span data-ttu-id="30424-144">POS 外设通常划分为类。</span><span class="sxs-lookup"><span data-stu-id="30424-144">POS peripherals are typically divided into classes.</span></span> <span data-ttu-id="30424-145">此部分描述并提供 Modern POS 支持的设备的概览。</span><span class="sxs-lookup"><span data-stu-id="30424-145">This section describes and gives an overview of the devices that Modern POS supports.</span></span>

### <a name="printer"></a><span data-ttu-id="30424-146">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-146">Printer</span></span>

<span data-ttu-id="30424-147">外设包括传统 POS 收据打印机和整页打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-147">Printers include traditional POS receipt printers and full-page printers.</span></span> <span data-ttu-id="30424-148">通过适用于 Retail POS (OPOS) 和 Microsoft Windows 的对象链路与嵌入驱动程序接口为打印机提供支持。</span><span class="sxs-lookup"><span data-stu-id="30424-148">Printer are supported through Object Linking and Embedding for Retail POS (OPOS) and Microsoft Windows driver interfaces.</span></span> <span data-ttu-id="30424-149">最多可以同时使用两台打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-149">Up to two printers can be used at the same time.</span></span> <span data-ttu-id="30424-150">此功能支持在收据打印机上打印付现自提的客户收据的方案，虽然包含更多信息的客户订单在整页打印机上打印。</span><span class="sxs-lookup"><span data-stu-id="30424-150">This capability supports scenarios where cash-and-carry customer receipts are printed on receipt printers, whereas customer orders, which carry more information, are printed on a full-page printer.</span></span> <span data-ttu-id="30424-151">收据打印机可以通过 USB 直接连接到计算机，通过以太网连接到网络，或通过 Bluetooth 连接。</span><span class="sxs-lookup"><span data-stu-id="30424-151">Receipt printers can be connected directly to a computer via USB, connected to a network via Ethernet, or connected via Bluetooth.</span></span>

### <a name="scanner"></a><span data-ttu-id="30424-152">扫描仪</span><span class="sxs-lookup"><span data-stu-id="30424-152">Scanner</span></span>

<span data-ttu-id="30424-153">最多可以同时使用两台条码扫描仪。</span><span class="sxs-lookup"><span data-stu-id="30424-153">Up to two bar code scanners can be used at the same time.</span></span> <span data-ttu-id="30424-154">此功能支持需要移动性更高的扫描仪来扫描体积大或重量高的物品的方案，而嵌入式固定扫描仪则用于大多数标准尺寸的物品或加快收银速度。</span><span class="sxs-lookup"><span data-stu-id="30424-154">This capability supports scenarios where a scanner that is more mobile is required in order to scan large or heavy items, whereas a fixed embedded scanner is used for most standard-sized items, to speed up checkout times.</span></span> <span data-ttu-id="30424-155">可以通过 OPOS、通用 Windows 平台 (UWP) 或键盘 wedge 界面为扫描仪提供支持。</span><span class="sxs-lookup"><span data-stu-id="30424-155">Scanners can be supported through OPOS, Universal Windows Platform (UWP), or keyboard wedge interfaces.</span></span> <span data-ttu-id="30424-156">可使用 USB 或 Bluetooth 将扫描仪连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="30424-156">USB or Bluetooth can be used to connect a scanner to a computer.</span></span>

### <a name="msr"></a><span data-ttu-id="30424-157">MSR</span><span class="sxs-lookup"><span data-stu-id="30424-157">MSR</span></span>

<span data-ttu-id="30424-158">可通过使用 OPOS 设置一台 USB 磁条阅读器 (MSR)。</span><span class="sxs-lookup"><span data-stu-id="30424-158">One USB magnetic stripe reader (MSR) can be set up by using OPOS drivers.</span></span> <span data-ttu-id="30424-159">如果要将单机 MSR 用于电子资金转帐 (EFT) 付款交易，则必须通过付款连接器管理 MSR。.</span><span class="sxs-lookup"><span data-stu-id="30424-159">If you want to use a stand-alone MSR for electronic funds transfer (EFT) payment transactions, the MSR must be managed by a payment connector.</span></span> <span data-ttu-id="30424-160">单机 MSR 可用于独立于付款连接器执行客户会员信息录入、员工签到和礼品卡录入。</span><span class="sxs-lookup"><span data-stu-id="30424-160">Stand-alone MSRs can be used for customer loyalty entry, employee sign-in, and gift card entry, independently of the payment connector.</span></span>

### <a name="cash-drawer"></a><span data-ttu-id="30424-161">银箱</span><span class="sxs-lookup"><span data-stu-id="30424-161">Cash drawer</span></span>

<span data-ttu-id="30424-162">每个硬件配置文件可以支持两个银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-162">Two cash drawers can be supported per hardware profile.</span></span> <span data-ttu-id="30424-163">此功能允许每台收银机同时被两个班次使用。</span><span class="sxs-lookup"><span data-stu-id="30424-163">This capability enables two active shifts per register to be available at the same time.</span></span> <span data-ttu-id="30424-164">为了防止共享班次或一个银箱同时被多个移动 POS 设备使用，每个硬件配置文件仅允许一个银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-164">In the case of a shared shift, or a cash drawer that is used by multiple mobile POS devices at the same time, only one cash drawer is allowed per hardware profile.</span></span> <span data-ttu-id="30424-165">银箱可以通过 USB 直接连接到计算机，连接到网络，或通过 RJ12 接口连接到收据打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-165">Cash drawers can be connected directly to a computer via USB, connected to a network, or connected to a receipt printer via an RJ12 interface.</span></span> <span data-ttu-id="30424-166">在某些情况下，还可以通过 Bluetooth 连接银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-166">In some cases, cash drawers can also be connected via Bluetooth.</span></span>

### <a name="line-display"></a><span data-ttu-id="30424-167">行显示内容</span><span class="sxs-lookup"><span data-stu-id="30424-167">Line display</span></span>

<span data-ttu-id="30424-168">行显示器用于在交易期间向客户显示产品、交易余额和其他有用信息。</span><span class="sxs-lookup"><span data-stu-id="30424-168">Line displays are used to show products, transaction balances, and other useful information to the customer during a transaction.</span></span> <span data-ttu-id="30424-169">可以使用 OPOS 驱动程序通过 USB 将一台行显示器连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="30424-169">One line display can be connected to the computer via USB by using OPOS drivers.</span></span>

### <a name="signature-capture"></a><span data-ttu-id="30424-170">签名捕获</span><span class="sxs-lookup"><span data-stu-id="30424-170">Signature capture</span></span>

<span data-ttu-id="30424-171">可以使用 OPOS 驱动程序通过 USB 将签名捕获设备直接连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="30424-171">Signature capture devices can be connected directly to a computer via USB by using OPOS drivers.</span></span> <span data-ttu-id="30424-172">在配置签名捕获时，将提示客户在设备上签名。</span><span class="sxs-lookup"><span data-stu-id="30424-172">When signature capture is configured, the customer is prompted to sign on the device.</span></span> <span data-ttu-id="30424-173">提供签名后，它会对收银员显示，待其接受。</span><span class="sxs-lookup"><span data-stu-id="30424-173">After the signature is provided, it's shown to the cashier for acceptance.</span></span>

### <a name="scale"></a><span data-ttu-id="30424-174">比例</span><span class="sxs-lookup"><span data-stu-id="30424-174">Scale</span></span>

<span data-ttu-id="30424-175">可以使用 OPOS 驱动程序通过 USP 将秤连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="30424-175">Scales can be connected to the computer via USP by using OPOS drivers.</span></span> <span data-ttu-id="30424-176">标记为“已称重”产品的产品添加到交易记录时，POS 从秤读取重量，将该产品添加到交易记录，然后使用秤提供的数量。</span><span class="sxs-lookup"><span data-stu-id="30424-176">When a product that is marked as a “Weighed” product is added to a transaction, the POS reads the weight from the scale, adds the product to the transaction, and uses the quantity that the scale provided.</span></span>

### <a name="pin-pad"></a><span data-ttu-id="30424-177">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="30424-177">PIN pad</span></span>

<span data-ttu-id="30424-178">通过 OPOS 为个人标识号 (PIN) 小键盘提供支持，但是必须通过付款连接器管理 PIN 小键盘。</span><span class="sxs-lookup"><span data-stu-id="30424-178">Personal identification number (PIN) pads are supported through OPOS, but they must be managed via a payment connector.</span></span>

### <a name="secondary-display"></a><span data-ttu-id="30424-179">辅助显示器</span><span class="sxs-lookup"><span data-stu-id="30424-179">Secondary display</span></span>

<span data-ttu-id="30424-180">如果配置了辅助显示器，将使用第二台 Windows 显示器显示基本信息。</span><span class="sxs-lookup"><span data-stu-id="30424-180">When a secondary display is configured, the number 2 Windows display is used to show basic information.</span></span> <span data-ttu-id="30424-181">辅助显示器用于为独立软件供应商 (ISV) 扩展提供支持，因为原始辅助显示器不可配置，显示的内容有限。</span><span class="sxs-lookup"><span data-stu-id="30424-181">The purpose of the secondary display is to support independent software vendor (ISV) extension, because out of the box, the secondary display isn't configurable and shows limited content.</span></span>

### <a name="payment-device"></a><span data-ttu-id="30424-182">付款设备</span><span class="sxs-lookup"><span data-stu-id="30424-182">Payment device</span></span>

<span data-ttu-id="30424-183">对付款设备的支持通过付款连接器实现。</span><span class="sxs-lookup"><span data-stu-id="30424-183">Payment device support is implemented through the payment connector.</span></span> <span data-ttu-id="30424-184">付款设备可以执行其他设备类提供的一项或多项功能。</span><span class="sxs-lookup"><span data-stu-id="30424-184">Payment devices can perform one or many of the functions that other device classes provide.</span></span> <span data-ttu-id="30424-185">例如，一种付款设备可以充当 MSR/卡阅读器、行显示器、签名捕获设备或 PIN 小键盘。</span><span class="sxs-lookup"><span data-stu-id="30424-185">For example, a payment device can function as an MSR/card reader, line display, signature capture device, or PIN pad.</span></span> <span data-ttu-id="30424-186">对付款设备的支持独立于为硬件配置文件中包含的其他设备提供的单机设备支持实现。</span><span class="sxs-lookup"><span data-stu-id="30424-186">Support for payment devices is implemented independently of the stand-alone device support that is provided for other devices that are included in the hardware profile.</span></span>

## <a name="supported-interfaces"></a><span data-ttu-id="30424-187">支持的接口</span><span class="sxs-lookup"><span data-stu-id="30424-187">Supported interfaces</span></span>
### <a name="opos"></a><span data-ttu-id="30424-188">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-188">OPOS</span></span>

<span data-ttu-id="30424-189">为了帮助确保最大范围的设备可以与 Commerce 配合使用，OLE for POS 行业标准成为了支持的主要外设平台。</span><span class="sxs-lookup"><span data-stu-id="30424-189">To help guarantee that the largest range of devices can be used with Commerce, the OLE for POS industry standard is the primary peripheral device platform that is supported.</span></span> <span data-ttu-id="30424-190">OLE for POS 标准由美国零售联合会 (NRF) 制订，建立了针对外设的行业标准通信协议。</span><span class="sxs-lookup"><span data-stu-id="30424-190">The OLE for POS standard was produced by the National Retail Federation (NRF), which establishes industry-standard communication protocols for peripheral devices.</span></span> <span data-ttu-id="30424-191">OPOS 是广泛采用的 OLE for POS 标准实施。</span><span class="sxs-lookup"><span data-stu-id="30424-191">OPOS is a widely adopted implementation of the OLE for POS standard.</span></span> <span data-ttu-id="30424-192">它开发于 20 世纪 90 年代，之后经过了多次更新。</span><span class="sxs-lookup"><span data-stu-id="30424-192">It was developed in the mid-1990s and has been updated several times since then.</span></span> <span data-ttu-id="30424-193">OPOS 提供设备驱动程序架构，以便将 POS 硬件与基于 Windows 的 POS 系统轻松集成。</span><span class="sxs-lookup"><span data-stu-id="30424-193">OPOS provides a device driver architecture that enables easy integration of POS hardware with Windows–based POS systems.</span></span> <span data-ttu-id="30424-194">OPOS 控件处理兼容硬件与 POS 软件之间的通信。</span><span class="sxs-lookup"><span data-stu-id="30424-194">OPOS controls handle communication between compatible hardware and the POS software.</span></span> <span data-ttu-id="30424-195">OPOS 控件包含两部分：</span><span class="sxs-lookup"><span data-stu-id="30424-195">An OPOS control consists of two parts:</span></span>

-   <span data-ttu-id="30424-196">**控件对象** – 设备类（如行显示器）的控件对象提供软件程序的界面。</span><span class="sxs-lookup"><span data-stu-id="30424-196">**Control object** – The control object for a device class (such as line displays) provides the interface for the software program.</span></span> <span data-ttu-id="30424-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) 提供一组标准的 OPOS 控件对象，称为公共控件对象 (CCO)。</span><span class="sxs-lookup"><span data-stu-id="30424-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) provides a standardized set of OPOS control objects that are known as the common control objects (CCOs).</span></span> <span data-ttu-id="30424-198">CCO 用于测试 Commerce 的 POS 组件。</span><span class="sxs-lookup"><span data-stu-id="30424-198">The CCOs are used to test the POS component of Commerce.</span></span> <span data-ttu-id="30424-199">因此，如果 Commerce 通过 OPOS 为设备类提供支持，并且制造商提供为 OPOS 构建的服务对象，此项测试有助于确保可以支持多种设备类型。</span><span class="sxs-lookup"><span data-stu-id="30424-199">Therefore, the testing helps guarantee that, if Commerce supports a device class through OPOS, many device types can be supported, provided that the manufacturer provides a service object that is built for OPOS.</span></span> <span data-ttu-id="30424-200">无需明确测试每个设备类型。</span><span class="sxs-lookup"><span data-stu-id="30424-200">You don't have to explicitly test each device type.</span></span>
-   <span data-ttu-id="30424-201">**服务对象** – 服务对象提供控件对象 (CCO) 与设备之间的通信。</span><span class="sxs-lookup"><span data-stu-id="30424-201">**Service object** – The service object provides communication between the control object (CCO) and the device.</span></span> <span data-ttu-id="30424-202">设备的服务对象通常由设备制造商提供。</span><span class="sxs-lookup"><span data-stu-id="30424-202">Typically, the service object for a device is provided by the device manufacturer.</span></span> <span data-ttu-id="30424-203">但是在某些情况下，您可能必须从制造商的网站下载服务对象。</span><span class="sxs-lookup"><span data-stu-id="30424-203">However, in some cases, you might have to download the service object from the manufacturer’s website.</span></span> <span data-ttu-id="30424-204">例如，可能提供了更新的服务对象。</span><span class="sxs-lookup"><span data-stu-id="30424-204">For example, a more recent service object might be available.</span></span> <span data-ttu-id="30424-205">若要查找制造商的网站地址，请参阅您的硬件文档。</span><span class="sxs-lookup"><span data-stu-id="30424-205">To find the address of the manufacturer's website, see your hardware documentation.</span></span>

<span data-ttu-id="30424-206">[![控件对象和服务对象](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) 对 OLE for POS 的 OPOS 实施的支持有助于确保当设备制造商和 POS 发布商正确实施标准时，POS 系统和支持的设备可以协同工作，即使以前未一起测试也不例外。</span><span class="sxs-lookup"><span data-stu-id="30424-206">[![Control object and service object](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Support for the OPOS implementation of OLE for POS helps guarantee that, if the device manufacturers and POS publishers implement the standard correctly, POS systems and supported devices can work together, even if they weren't previously tested together.</span></span> 

> [!NOTE]
> <span data-ttu-id="30424-207">支持 OPOS 不保证支持采用了 OPOS 驱动设备的所有设备。</span><span class="sxs-lookup"><span data-stu-id="30424-207">OPOS support doesn't guarantee support for all devices that have OPOS drivers.</span></span> <span data-ttu-id="30424-208">Commerce 必须首先通过 OPOS 支持该设备类型（或类）。</span><span class="sxs-lookup"><span data-stu-id="30424-208">Commerce must first support that device type, or class, through OPOS.</span></span> <span data-ttu-id="30424-209">此外，服务对象可能并非始终安装了最新版本的 CCO。</span><span class="sxs-lookup"><span data-stu-id="30424-209">In addition, service objects might not always be up to date with the latest version of the CCOs.</span></span> <span data-ttu-id="30424-210">您还应注意，服务对象的质量往往参差不齐。</span><span class="sxs-lookup"><span data-stu-id="30424-210">You should also be aware that, in general, the quality of service objects varies.</span></span>

### <a name="windows"></a><span data-ttu-id="30424-211">窗口</span><span class="sxs-lookup"><span data-stu-id="30424-211">Windows</span></span>

<span data-ttu-id="30424-212">POS 的收据打印已针对 OPOS 进行了优化。</span><span class="sxs-lookup"><span data-stu-id="30424-212">Receipt printing at the POS is optimized for OPOS.</span></span> <span data-ttu-id="30424-213">OPOS 往往比通过 Windows 打印快得多。</span><span class="sxs-lookup"><span data-stu-id="30424-213">OPOS tends to be much faster than printing through Windows.</span></span> <span data-ttu-id="30424-214">因此，最好使用 OPOS 进行打印，特别是在需要打印 40 列收据，并且交易时间必须非常快的环境中。</span><span class="sxs-lookup"><span data-stu-id="30424-214">Therefore, it's a good idea to use OPOS, especially in environments where 40-column receipts are printed and transaction times must be fast.</span></span> <span data-ttu-id="30424-215">对于大多数设备，您将使用 OPOS 控件。</span><span class="sxs-lookup"><span data-stu-id="30424-215">For most devices, you will use OPOS controls.</span></span> <span data-ttu-id="30424-216">但是，某些 OPOS 收据打印机也支持 Windows 驱动程序。</span><span class="sxs-lookup"><span data-stu-id="30424-216">However, some OPOS receipt printers also support Windows drivers.</span></span> <span data-ttu-id="30424-217">通过使用 Windows 驱动程序，您可以通过一台打印机访问多台收银机的最新字体和网络。</span><span class="sxs-lookup"><span data-stu-id="30424-217">By using a Windows driver, you can access the latest fonts and network one printer for multiple registers.</span></span> <span data-ttu-id="30424-218">但是使用 Windows 驱动程序有一些缺点。</span><span class="sxs-lookup"><span data-stu-id="30424-218">However, there are drawbacks to using Windows drivers.</span></span> <span data-ttu-id="30424-219">以下是这些缺点的一些示例：</span><span class="sxs-lookup"><span data-stu-id="30424-219">Here are some examples of these drawbacks:</span></span>

-   <span data-ttu-id="30424-220">使用 Windows 驱动程序时，图像在打印前渲染。</span><span class="sxs-lookup"><span data-stu-id="30424-220">When Windows drivers are used, images are rendered before printing occurs.</span></span> <span data-ttu-id="30424-221">因此，打印速度往往比使用 OPOS 控件的打印机慢。</span><span class="sxs-lookup"><span data-stu-id="30424-221">Therefore, printing tends to be slower than it is on printers that use OPOS controls.</span></span>
-   <span data-ttu-id="30424-222">使用 Windows 驱动程序时，通过打印机连接（“菊链方式”）的设备可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="30424-222">Devices that are connected through the printer (“daisy-chained”) might not work correctly when Windows drivers are used.</span></span> <span data-ttu-id="30424-223">例如，银箱可能无法打开，或者票据打印机可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="30424-223">For example, the cash drawer might not open, or the slip printer might not word as you expect.</span></span>
-   <span data-ttu-id="30424-224">OPOS 还支持特定于收据打印机的更多变体集合，如裁纸或票据打印。</span><span class="sxs-lookup"><span data-stu-id="30424-224">OPOS also supports a more extensive set of variables that are specific to receipt printers, such as paper cutting or slip printing.</span></span>
-   <span data-ttu-id="30424-225">不通过 IIS 硬件工作站来支持 Windows 打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-225">Windows printers are not supported through the IIS hardware station.</span></span> 

<span data-ttu-id="30424-226">如果 OPOS 控件适用于您在使用的 Windows 打印机，该打印机仍然可以与 Commerce 配合正常工作。</span><span class="sxs-lookup"><span data-stu-id="30424-226">If OPOS controls are available for the Windows printer that you're using, the printer should still work correctly with Commerce.</span></span>

### <a name="universal-windows-platform"></a><span data-ttu-id="30424-227">通用 Windows 平台</span><span class="sxs-lookup"><span data-stu-id="30424-227">Universal Windows Platform</span></span>

<span data-ttu-id="30424-228">对于外设，UWP 与 Windows 对即插即用设备的支持有关。</span><span class="sxs-lookup"><span data-stu-id="30424-228">UWP, in the case of peripherals, is related to Windows support for Plug and Play devices.</span></span> <span data-ttu-id="30424-229">当即插即用设备连接到支持这种设备的 Windows 操作系统版本时，该设备不需要驱动程序即可正常使用。</span><span class="sxs-lookup"><span data-stu-id="30424-229">When a Plug and Play device is connected to a Windows OS version that supports that type of device, no driver is required for the device to be used as intended.</span></span> <span data-ttu-id="30424-230">例如，如果 Windows 检测到 Bluetooth 扬声器设备，该操作系统知道此设备的类类型为 **扬声器**。</span><span class="sxs-lookup"><span data-stu-id="30424-230">For example, if Windows detects a Bluetooth speaker device, the OS knows that the device has the **Speaker** class type.</span></span> <span data-ttu-id="30424-231">因此，它将把此设备视为扬声器。</span><span class="sxs-lookup"><span data-stu-id="30424-231">Therefore, and it treats that device as a speaker.</span></span> <span data-ttu-id="30424-232">无需再执行任何设置。</span><span class="sxs-lookup"><span data-stu-id="30424-232">No additional setup is required.</span></span> <span data-ttu-id="30424-233">对于 POS 设备，可以插入大量 USB 设备，并且 Windows 将把其识别为人机接口设备 (HID)。</span><span class="sxs-lookup"><span data-stu-id="30424-233">In the case of POS devices, many USB devices can be plugged in, and Windows will recognize them as Human Interface Devices (HIDs).</span></span> <span data-ttu-id="30424-234">但是，可能不能确定设备提供的功能，因为设备不指定设备的类（即类型）。</span><span class="sxs-lookup"><span data-stu-id="30424-234">However, it might not be able to determine the capabilities that the device provides, because the device doesn't specify the class, or type, of device.</span></span> <span data-ttu-id="30424-235">在 Windows 10 中，已增加了条码扫描仪 和 MSR 的设备类。</span><span class="sxs-lookup"><span data-stu-id="30424-235">In Windows 10, device classes for bar code scanners and MSRs have been added.</span></span> <span data-ttu-id="30424-236">因此，如果设备向 Windows 10 声明自己是这些类之一的设备，Windows 将在相应时间注意来自该设备的事件。</span><span class="sxs-lookup"><span data-stu-id="30424-236">Therefore, if a device declares itself to Windows 10 as a device of one of these classes, Windows will listen for events from the device at the appropriate times.</span></span> <span data-ttu-id="30424-237">Modern POS 支持 UWP MSR 和扫描仪。</span><span class="sxs-lookup"><span data-stu-id="30424-237">Modern POS supports UWP MSRs and scanners.</span></span> <span data-ttu-id="30424-238">因此，准备好从这些设备之一输入，并且已连接属于这些类之一的设备时，可以使用该设备。</span><span class="sxs-lookup"><span data-stu-id="30424-238">Therefore, when it's ready for input from one of these devices, and a device that belongs to one of these classes is connected, the device can be used.</span></span> <span data-ttu-id="30424-239">例如，如果在 Windows 10 计算机中插入一台 UWP 条码扫描仪，并且为 Modern POS 配置了条码签到，将在签到屏幕上激活该条码扫描仪。</span><span class="sxs-lookup"><span data-stu-id="30424-239">For example, if a UWP bar code scanner is plugged into a Windows 10 computer, and bar code sign-in is configured for Modern POS, the bar code scanner will become active on the sign-in screen.</span></span> <span data-ttu-id="30424-240">无需再执行任何设置。</span><span class="sxs-lookup"><span data-stu-id="30424-240">No additional setup is required.</span></span> <span data-ttu-id="30424-241">正在向 Windows 添加更多服务点 UWP 设备类。</span><span class="sxs-lookup"><span data-stu-id="30424-241">Additional classes of point of service UWP devices are being added to Windows.</span></span> <span data-ttu-id="30424-242">这些类中包括银箱和收据打印机的类。</span><span class="sxs-lookup"><span data-stu-id="30424-242">These classes include classes for cash drawers and receipt printers.</span></span> <span data-ttu-id="30424-243">Modern POS 中对这些新设备的支持待定。</span><span class="sxs-lookup"><span data-stu-id="30424-243">Support for these new device classes in Modern POS is pending.</span></span>

### <a name="keyboard-wedge"></a><span data-ttu-id="30424-244">键盘 wedge</span><span class="sxs-lookup"><span data-stu-id="30424-244">Keyboard wedge</span></span>

<span data-ttu-id="30424-245">键盘 wedge 设备向计算机发送数据，就像数据是从键盘键入的。</span><span class="sxs-lookup"><span data-stu-id="30424-245">Keyboard wedge devices send data to the computer as if that data were typed on a keyboard.</span></span> <span data-ttu-id="30424-246">因此默认情况下，POS 上的活动字段将收到扫描或刷卡的数据。</span><span class="sxs-lookup"><span data-stu-id="30424-246">Therefore, by default, the field that is active at the POS will receive the data that is scanned or swiped.</span></span> <span data-ttu-id="30424-247">在某些情况下，此行为可能导致将错误类型的数据扫描到错误的字段中。</span><span class="sxs-lookup"><span data-stu-id="30424-247">In some cases, this behavior can cause the wrong type of data to be scanned into the wrong field.</span></span> <span data-ttu-id="30424-248">例如，可能将条码扫描到本应输入信用卡数据的字段。</span><span class="sxs-lookup"><span data-stu-id="30424-248">For example, a bar code might be scanned into a field that is intended for input of credit card data.</span></span> <span data-ttu-id="30424-249">在大多数情况下，POS 中有逻辑可确定扫描的数据是条码还是刷卡。</span><span class="sxs-lookup"><span data-stu-id="30424-249">In many cases, there is logic at the POS that determines whether the data that is scanned or swiped is a bar code or card swipe.</span></span> <span data-ttu-id="30424-250">因此可以正确处理数据。</span><span class="sxs-lookup"><span data-stu-id="30424-250">Therefore, the data is handled correctly.</span></span> <span data-ttu-id="30424-251">但是，当设备设置为 OPOS 而不是键盘 wedge 设备时，对来自这些设备的数据的使用方式控制更严格，因为对数据的来源设备的“了解”更深。</span><span class="sxs-lookup"><span data-stu-id="30424-251">However, when devices are set up as OPOS instead of keyboard wedge devices, there is more control over how the data from those devices can be consumed, because more is “known” about the device that the data originates from.</span></span> <span data-ttu-id="30424-252">例如，来自条码扫描仪的数据自动识别为条码，并且相比过去使用的一般字符串搜索（如使用键盘 wedge 设备时），可以更轻松、更快地找到数据库中的关联记录。</span><span class="sxs-lookup"><span data-stu-id="30424-252">For example, data from a bar code scanner is automatically recognized as a bar code, and the associated record in the database is found more easily and faster than if a generic string search were used, as in the case of keyboard wedge devices.</span></span>

> [!NOTE]
> <span data-ttu-id="30424-253">当在 POS 中使用键盘 wedge 扫描仪时，必须对其进行编程以在最后扫描的字符之后发送回车符或 **Enter** 事件。</span><span class="sxs-lookup"><span data-stu-id="30424-253">When keyboard wedge scanners are used in the POS, they must be programmed to send a carriage return, or **Enter** event, after the last scanned character.</span></span> <span data-ttu-id="30424-254">如果未完成此配置，键盘 wedge 扫描仪将无法正常运行。</span><span class="sxs-lookup"><span data-stu-id="30424-254">If this configuration isn't done, keyboard wedge scanners won't function properly.</span></span> <span data-ttu-id="30424-255">请查阅设备制造商提供的文档，以获取有关如何追加回车符事件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="30424-255">Consult documentation provided by your device manufacturer for details on how to append the carriage return event.</span></span>  

### <a name="native-printer"></a><span data-ttu-id="30424-256">本机打印机</span><span class="sxs-lookup"><span data-stu-id="30424-256">Native printer</span></span>

<span data-ttu-id="30424-257">可以将本机（或“设备”，因为类型是在硬件配置文件中命名的）配置为提示用户选择为计算机配置的打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-257">Native (or "Device" as the type is named in the hardware profile) printers can be configured to prompt the user to select a printer that is configured for the computer.</span></span> <span data-ttu-id="30424-258">配置了 **设备** 类型的打印机时，如果 Modern POS 收到了打印命令，将提示用户在列表中选择打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-258">When a printer of the **Device** type is configured, if Modern POS encounters a print command, the user is prompted to select a printer in a list.</span></span> <span data-ttu-id="30424-259">此行为与 Windows 驱动程序的行为不同，因为硬件配置文件中的 **Windows** 打印机类型不显示打印机列表。</span><span class="sxs-lookup"><span data-stu-id="30424-259">This behavior differs from the behavior for Windows drivers, because the **Windows** printer type in the hardware profile doesn't show a list of printers.</span></span> <span data-ttu-id="30424-260">相反，它要求在 **设备名称** 字段中提供命名的打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-260">Instead, it requires that a named printer be provided in the **Device name** field.</span></span>

### <a name="network"></a><span data-ttu-id="30424-261">网络</span><span class="sxs-lookup"><span data-stu-id="30424-261">Network</span></span>

<span data-ttu-id="30424-262">可通过 Modern POS for Windows 应用程序中内置的进程间通信 (IPC) 硬件工作站或其他 Modern POS 客户端的 IIS 硬件工作站，通过网络使用网络可寻址银箱、收据打印机和付款终端。</span><span class="sxs-lookup"><span data-stu-id="30424-262">Network-addressable cash drawers, receipt printers, and payment terminals can be used over a network, either directly through the Interprocess Communications (IPC) hardware station that is built into the Modern POS for Windows application or through the IIS hardware station for other Modern POS clients.</span></span>

## <a name="hardware-station-deployment-options"></a><span data-ttu-id="30424-263">硬件工作站部署选项</span><span class="sxs-lookup"><span data-stu-id="30424-263">Hardware station deployment options</span></span>

### <a name="dedicated"></a><span data-ttu-id="30424-264">专门</span><span class="sxs-lookup"><span data-stu-id="30424-264">Dedicated</span></span>

<span data-ttu-id="30424-265">适用于 Windows 和 Android 的现代 POS 客户端包括 **专用** 或内置硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-265">Modern POS clients for Windows and Android include **Dedicated** or built-in hardware stations.</span></span> <span data-ttu-id="30424-266">这些客户端可以使用应用程序内置的业务逻辑直接与外围设备通信。</span><span class="sxs-lookup"><span data-stu-id="30424-266">Those clients can communicate directly with peripherals using business logic that is built into the applications.</span></span> <span data-ttu-id="30424-267">Android 应用程序仅支持网络设备。</span><span class="sxs-lookup"><span data-stu-id="30424-267">The Android application only supports network devices.</span></span> <span data-ttu-id="30424-268">有关 Android 外设支持的更多信息，请访问[在 Android 和 iOS 上安装 POS Hybrid 应用](./dev-itpro/hybridapp.md)文章。</span><span class="sxs-lookup"><span data-stu-id="30424-268">For more information on peripheral support for the Android, visit the [Set up POS hybrid app on Android and iOS](./dev-itpro/hybridapp.md) article.</span></span>

<span data-ttu-id="30424-269">若要使用专用硬件工作站，请为将使用 Modern POS for Windows 或 Android 应用程序的收银机分配硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="30424-269">To use the dedicated hardware station, assign a hardware profile to a register that will use the Modern POS for Windows or Android applications.</span></span> <span data-ttu-id="30424-270">然后为将使用该收银机的商店创建一个类型为 **专用** 的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-270">Then create a hardware station of the **Dedicated** type for the store where the register will be used.</span></span> <span data-ttu-id="30424-271">在非银箱模式下启动 Modern POS 并使用 **管理硬件工作站** 操作打开硬件工作站功能，默认情况下专用硬件工作站将处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="30424-271">Start the Modern POS in non-drawer mode and use the use the **Manage hardware stations** operation to turn on the hardware station capabilities, the dedicated hardware station will be active by default.</span></span> <span data-ttu-id="30424-272">接下来，注销 Modern POS，然后重新登录并打开一个班次，即可使用硬件配置文件中配置的外围设备。</span><span class="sxs-lookup"><span data-stu-id="30424-272">Next, log out of the Modern POS, then log back in and open a shift and the peripherals configured in the hardware profile will be usable.</span></span> 

### <a name="shared"></a><span data-ttu-id="30424-273">已共享</span><span class="sxs-lookup"><span data-stu-id="30424-273">Shared</span></span> 

<span data-ttu-id="30424-274">“IIS”有时也称为“IIS”硬件工作站，表示 POS 应用程序通过 Microsoft Internet 信息服务连接到硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-274">Also sometimes referred to as the "IIS" hardware station, “IIS” implying that the POS application connects to the hardware station via Microsoft Internet Information Services.</span></span> <span data-ttu-id="30424-275">POS 应用程序通过连接设备的计算机上运行的 Web 服务连接到 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-275">The POS application connects to the IIS hardware station via web services that run on a computer where the devices are connected.</span></span> <span data-ttu-id="30424-276">使用共享的硬件工作站时，与 IIS 硬件工作站在同一个网络中的任何 POS 收银机都可以使用与该硬件工作站相连的外设。</span><span class="sxs-lookup"><span data-stu-id="30424-276">When the shared hardware station is used, the peripherals that are connected to a hardware station can be used by any POS register that is on the same network as the IIS hardware station.</span></span> <span data-ttu-id="30424-277">由于只有 Modern POS for Windows 和 Android 中才包含对外设的内置支持，所以其他所有 Modern POS 应用程序都必须使用 IIS 硬件工作站才能与硬件配置文件中配置的 POS 外设通信。</span><span class="sxs-lookup"><span data-stu-id="30424-277">Because only Modern POS for Windows and Android include built-in support for peripherals, all other Modern POS applications must use the IIS hardware station to communicate with POS peripherals that are configured in the hardware profile.</span></span> <span data-ttu-id="30424-278">因此，IIS 硬件工作站的每个实例都需要运行与设备通信的 Web 服务和应用程序的计算机。</span><span class="sxs-lookup"><span data-stu-id="30424-278">Therefore, each instance of the IIS hardware station requires a computer that runs the web service and application that communicates with the devices.</span></span> 

<span data-ttu-id="30424-279">共享的硬件工作站可用于允许多个销售点客户端共享外围设备，或者可用于管理为单个销售点调配的设备组或外围设备。</span><span class="sxs-lookup"><span data-stu-id="30424-279">The shared hardware station can be used to allow multiple point of sale clients to share peripherals or can be used to manage a committed set or peripherals for a single point of sale.</span></span> 

<span data-ttu-id="30424-280">当硬件工作站用于支持多个 POS 客户端之间的外围设备共享时，应仅使用银箱、收据打印机和付款终端。</span><span class="sxs-lookup"><span data-stu-id="30424-280">When a hardware station is used to support sharing of peripherals between multiple POS clients, only cash drawers, receipt printers, and payment terminals should be used.</span></span> <span data-ttu-id="30424-281">不能直接连接单机条码扫描仪、行显示器，MSR、秤或其他设备。</span><span class="sxs-lookup"><span data-stu-id="30424-281">You can't directly connect stand-alone bar code scanners, MSRs, line displays, scales, or other devices.</span></span> <span data-ttu-id="30424-282">否则，多个 POS 设备同时尝试声明这些外设时，将发生冲突。</span><span class="sxs-lookup"><span data-stu-id="30424-282">Otherwise, conflicts will occur when multiple POS devices try to claim those peripherals at the same time.</span></span> <span data-ttu-id="30424-283">下面是如何管理受支持设备的冲突：</span><span class="sxs-lookup"><span data-stu-id="30424-283">Here is how conflicts are managed for supported devices:</span></span>

-   <span data-ttu-id="30424-284">**银箱** – 银箱通过发送到设备的事件打开。</span><span class="sxs-lookup"><span data-stu-id="30424-284">**Cash drawer** – The cash drawer is opened via an event that is sent to the device.</span></span> <span data-ttu-id="30424-285">仅当银箱已打开时，才会在调用银箱时发生问题。</span><span class="sxs-lookup"><span data-stu-id="30424-285">The only issue that can occur when a cash drawer is called occurs if the cash drawer is already open.</span></span> <span data-ttu-id="30424-286">对于共享硬件工作站，应在硬件配置文件中将银箱设置为 **共享**。</span><span class="sxs-lookup"><span data-stu-id="30424-286">In the case of shared hardware stations, the cash drawer should be set to **Shared** in the hardware profile.</span></span> <span data-ttu-id="30424-287">发送打开命令时，此设置阻止 POS 检查银箱是否已打开。</span><span class="sxs-lookup"><span data-stu-id="30424-287">This setting prevents the POS from checking whether the cash drawer is already open when it sends open commands.</span></span>
-   <span data-ttu-id="30424-288">**收据打印机** – 如果同时向硬件工作站发送两条收据打印命令，可能丢失其中一条命令，具体取决于设备。</span><span class="sxs-lookup"><span data-stu-id="30424-288">**Receipt printer** – If two receipt printing commands are sent to the hardware station at the same time, one of the commands can be lost, depending on the device.</span></span> <span data-ttu-id="30424-289">某些设备有内存或池，可以防止此问题。</span><span class="sxs-lookup"><span data-stu-id="30424-289">Some devices have internal memory or pooling that can prevent this issue.</span></span> <span data-ttu-id="30424-290">如果打印命令不成功，收银员将收到错误消息，可以从 POS 重试该打印命令。</span><span class="sxs-lookup"><span data-stu-id="30424-290">If a print command isn't successful, the cashier receives an error message and can retry the print command from the POS.</span></span>
-   <span data-ttu-id="30424-291">**付款终端** – 如果收银员尝试在已在使用的付款终端上处理交易的支付，将显示消息，通知收银员正在使用该终端，请收银员稍后重试。</span><span class="sxs-lookup"><span data-stu-id="30424-291">**Payment terminal** – If a cashier tries to tender a transaction on a payment terminal that is already being used, a message notifies the cashier that the terminal is being used and asks the cashier to try again later.</span></span> <span data-ttu-id="30424-292">通常，收银员可以看到终端已在使用并等待其他交易完成，再尝试处理付款。</span><span class="sxs-lookup"><span data-stu-id="30424-292">Usually, cashiers can see that a terminal is already being used and will wait until the other transaction is completed before they try to tender again.</span></span>

<span data-ttu-id="30424-293">为将来的版本计划了验证，以便检测是否为映射到共享硬件工作站的硬件配置文件设置了不受支持的设备。</span><span class="sxs-lookup"><span data-stu-id="30424-293">Validation is planned for a future release, to detect whether unsupported devices are set up for a hardware profile that is mapped to a shared hardware station.</span></span> <span data-ttu-id="30424-294">如果检测到不受支持的设备，用户将收到消息，说明共享硬件工作站不支持这些设备。</span><span class="sxs-lookup"><span data-stu-id="30424-294">If any unsupported devices are detected, the user will receive a message that states that the devices aren't supported for shared hardware stations.</span></span> <span data-ttu-id="30424-295">对于共享硬件工作站，**付款后即可选择** 选项在收银机级别设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="30424-295">In the case of shared hardware stations, the **Select upon tendering** option is set to **Yes** at the register level.</span></span> <span data-ttu-id="30424-296">然后在 POS 中为交易选择了付款时，将提示 POS 用户选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-296">The POS user is then prompted to select a hardware station when a tender is selected for a transaction at the POS.</span></span> <span data-ttu-id="30424-297">仅在付款时选择了硬件工作站时，将把对硬件工作站的选择直接添加到移动方案的 POS 工作流。</span><span class="sxs-lookup"><span data-stu-id="30424-297">When the hardware station is selected only at the time of tender, the hardware station selection is added directly to the POS workflow for mobile scenarios.</span></span> <span data-ttu-id="30424-298">额外福利是，付款终端上的行显示器不用于共享方案。</span><span class="sxs-lookup"><span data-stu-id="30424-298">As an additional benefit, the line display on the payment terminal isn't used for shared scenarios.</span></span> <span data-ttu-id="30424-299">如果付款终端用作行显示器，交易完成前，可能阻止其他用户使用该终端。</span><span class="sxs-lookup"><span data-stu-id="30424-299">If the payment terminal is used as a line display, other users might be blocked from using that terminal until the transaction is completed.</span></span> <span data-ttu-id="30424-300">在移动方案中，可能在较长一段时间内向交易添加行。</span><span class="sxs-lookup"><span data-stu-id="30424-300">In mobile scenarios, lines might be added to a transaction over a longer period.</span></span> <span data-ttu-id="30424-301">因此，需要 **付款后即可选择** 选项以确保最适宜的设备可用性。</span><span class="sxs-lookup"><span data-stu-id="30424-301">Therefore, the **Select upon tendering** option is required in order to ensure optimum device availability.</span></span>

### <a name="network-peripherals"></a><span data-ttu-id="30424-302">网络外设</span><span class="sxs-lookup"><span data-stu-id="30424-302">Network peripherals</span></span>

<span data-ttu-id="30424-303">硬件配置文件中为设备指派的网络让银箱、收据打印机和付款终端可以通过网络连接来连接。</span><span class="sxs-lookup"><span data-stu-id="30424-303">The network designation for devices in the hardware profile enables cash drawers, receipt printers, and payment terminals to be connected via a network connection.</span></span>

#### <a name="modern-pos-for-windows"></a><span data-ttu-id="30424-304">Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="30424-304">Modern POS for Windows</span></span>

<span data-ttu-id="30424-305">可以为两处的网络外设指定 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="30424-305">You can specify IP addresses for network peripherals in two places.</span></span> <span data-ttu-id="30424-306">如果 Modern POS Windows 客户端使用一组网络外设，您应该通过使用收银机自身的“操作窗格”上的 **IP 配置** 选项为这些设备设置 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="30424-306">If the Modern POS Windows client is using a single set of network peripherals, you should set the IP addresses for those devices by using the **IP configuration** option on the Action Pane for the register itself.</span></span> <span data-ttu-id="30424-307">对于将在 POS 收银机之间共享的网络设备，可以将为其指派的硬件配置文件直接映射到共享硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-307">In the case of network devices that will be shared among POS registers, a hardware profile that has network devices assigned to it can be mapped directly to a shared hardware station.</span></span> <span data-ttu-id="30424-308">若要分配 IP 地址，请在 **商店** 页中选择该硬件工作站，然后使用 **硬件工作站** 部分中的 **IP 配置** 选项指定为该硬件工作站分配的网络设备。</span><span class="sxs-lookup"><span data-stu-id="30424-308">To assign IP addresses, select that hardware station on the **Stores** page, and then use the **IP configuration** option in the **Hardware stations** section to specify the network devices that are assigned to that hardware station.</span></span> <span data-ttu-id="30424-309">对于只有网络设备的硬件工作站，则不必部署硬件工作站本身。</span><span class="sxs-lookup"><span data-stu-id="30424-309">For hardware stations that have only network devices, you don't have to deploy the hardware station itself.</span></span> <span data-ttu-id="30424-310">在这种情况下，仅当要在概念上根据可网络寻址的设备在商店中的位置为这些设备分组时，才需要硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-310">In this case, the hardware station is required only in order to conceptually group network-addressable devices according to their location in the store.</span></span>

#### <a name="cloud-pos-and-modern-pos-for-ios"></a><span data-ttu-id="30424-311">Cloud POS 和 Modern POS for iOS</span><span class="sxs-lookup"><span data-stu-id="30424-311">Cloud POS and Modern POS for iOS</span></span>

<span data-ttu-id="30424-312">硬件工作站中包含驱动以物理方式相连且可网络寻址的外设的逻辑。</span><span class="sxs-lookup"><span data-stu-id="30424-312">The logic that drives physically connected and network-addressable peripherals is contained in the hardware station.</span></span> <span data-ttu-id="30424-313">因此，对于除 Modern POS for Windows 和 Android 之外的所有 POS 客户端，必须部署并激活 IIS 硬件工作站，以便让 POS 可以与外设通信，无论这些外设是以物理方式连接到硬件工作站还是通过网络寻址。</span><span class="sxs-lookup"><span data-stu-id="30424-313">Therefore, for all POS clients except Modern POS for Windows and Android, an IIS hardware station must be deployed and active to enable the POS to communicate with peripherals, regardless of whether those peripherals are physically connected to a hardware station or addressed over the network.</span></span>

## <a name="setup-and-configuration"></a><span data-ttu-id="30424-314">设置和配置</span><span class="sxs-lookup"><span data-stu-id="30424-314">Setup and configuration</span></span>
### <a name="hardware-station-installation"></a><span data-ttu-id="30424-315">硬件工作站安装</span><span class="sxs-lookup"><span data-stu-id="30424-315">Hardware station installation</span></span>

<span data-ttu-id="30424-316">有关信息，请参阅[配置和安装硬件工作站](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-316">For information, see [Configure and install hardware station](retail-hardware-station-configuration-installation.md).</span></span>

### <a name="modern-pos-for-windows-setup-and-configuration"></a><span data-ttu-id="30424-317">Modern POS for Windows 设置和配置</span><span class="sxs-lookup"><span data-stu-id="30424-317">Modern POS for Windows setup and configuration</span></span>

<span data-ttu-id="30424-318">有关信息，请参阅[配置、安装和激活 Modern POS (MPOS)](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-318">For information, see [Configure, install and activate Modern POS (MPOS)](retail-modern-pos-device-activation.md).</span></span>

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a><span data-ttu-id="30424-319">Modern POS for Android 和 iOS 设置和配置</span><span class="sxs-lookup"><span data-stu-id="30424-319">Modern POS for Android and iOS setup and configuration</span></span>

<span data-ttu-id="30424-320">有关信息，请参阅[在 Android 和 iOS 中安装 POS Hybrid 应用](./dev-itpro/hybridapp.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-320">For information, see [Set up POS hybrid app on Android and iOS](./dev-itpro/hybridapp.md).</span></span>

### <a name="opos-device-setup-and-configuration"></a><span data-ttu-id="30424-321">OPOS 设备设置和配置</span><span class="sxs-lookup"><span data-stu-id="30424-321">OPOS device setup and configuration</span></span>

<span data-ttu-id="30424-322">有关 OPOS 组件的详细信息，请参阅本文的“支持的接口”。</span><span class="sxs-lookup"><span data-stu-id="30424-322">For more information about OPOS components, see the "Supported interfaces" section of this document.</span></span> <span data-ttu-id="30424-323">OPOS 驱动程序通常由设备制造商提供。</span><span class="sxs-lookup"><span data-stu-id="30424-323">Typically, OPOS drivers are provided by the device manufacturer.</span></span> <span data-ttu-id="30424-324">安装 OPOS 设备驱动程序时，将在 Windows 注册表中的以下位置添加一个键：</span><span class="sxs-lookup"><span data-stu-id="30424-324">When an OPOS device driver is installed, it adds a key to the Windows registry in one of the following locations:</span></span>

-   <span data-ttu-id="30424-325">**32 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="30424-325">**32-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span></span>
-   <span data-ttu-id="30424-326">**64 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="30424-326">**64-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span></span>

<span data-ttu-id="30424-327">在 ServiceOPOS 注册表位置中，配置的设备根据 OPOS 设备类组织。</span><span class="sxs-lookup"><span data-stu-id="30424-327">Within the ServiceOPOS registry location, configured devices are organized according to the OPOS device class.</span></span> <span data-ttu-id="30424-328">将保存多个设备驱动程序。</span><span class="sxs-lookup"><span data-stu-id="30424-328">Multiple device drivers are saved.</span></span>

## <a name="supported-scenarios-by-hardware-station-type"></a><span data-ttu-id="30424-329">硬件工作站类型支持的方案</span><span class="sxs-lookup"><span data-stu-id="30424-329">Supported scenarios by hardware station type</span></span>
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a><span data-ttu-id="30424-330">客户端支持 – IPC 硬件工作站与 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-330">Client support – IPC hardware station vs. IIS hardware station</span></span>

<span data-ttu-id="30424-331">下表显示支持的拓扑和部署方案。</span><span class="sxs-lookup"><span data-stu-id="30424-331">The following table shows the topologies and deployment scenarios that are supported.</span></span>

| <span data-ttu-id="30424-332">客户</span><span class="sxs-lookup"><span data-stu-id="30424-332">Client</span></span>      | <span data-ttu-id="30424-333">IPC 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-333">IPC hardware station</span></span> | <span data-ttu-id="30424-334">IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-334">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="30424-335">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="30424-335">Windows app</span></span> | <span data-ttu-id="30424-336">是</span><span class="sxs-lookup"><span data-stu-id="30424-336">Yes</span></span>                  | <span data-ttu-id="30424-337">是</span><span class="sxs-lookup"><span data-stu-id="30424-337">Yes</span></span>                  |
| <span data-ttu-id="30424-338">云 POS</span><span class="sxs-lookup"><span data-stu-id="30424-338">Cloud POS</span></span>   | <span data-ttu-id="30424-339">否</span><span class="sxs-lookup"><span data-stu-id="30424-339">No</span></span>                   | <span data-ttu-id="30424-340">是</span><span class="sxs-lookup"><span data-stu-id="30424-340">Yes</span></span>                  |
| <span data-ttu-id="30424-341">Android</span><span class="sxs-lookup"><span data-stu-id="30424-341">Android</span></span>     | <span data-ttu-id="30424-342">是</span><span class="sxs-lookup"><span data-stu-id="30424-342">Yes</span></span>                  | <span data-ttu-id="30424-343">是</span><span class="sxs-lookup"><span data-stu-id="30424-343">Yes</span></span>                  |
| <span data-ttu-id="30424-344">iOS</span><span class="sxs-lookup"><span data-stu-id="30424-344">iOS</span></span>         | <span data-ttu-id="30424-345">否</span><span class="sxs-lookup"><span data-stu-id="30424-345">No</span></span>                   | <span data-ttu-id="30424-346">是</span><span class="sxs-lookup"><span data-stu-id="30424-346">Yes</span></span>                  |

### <a name="network-peripherals"></a><span data-ttu-id="30424-347">网络外设</span><span class="sxs-lookup"><span data-stu-id="30424-347">Network peripherals</span></span>

<span data-ttu-id="30424-348">可以直接通过 Modern POS for Windows 和 Android 应用程序中内置的硬件工作站支持网络外设。</span><span class="sxs-lookup"><span data-stu-id="30424-348">Network peripherals can be supported directly through the hardware station that is built into the Modern POS for Windows and Android applications.</span></span> <span data-ttu-id="30424-349">对于其他所有客户端，则必须部署 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-349">For all other clients, you must deploy an IIS hardware station.</span></span>

| <span data-ttu-id="30424-350">客户</span><span class="sxs-lookup"><span data-stu-id="30424-350">Client</span></span>      | <span data-ttu-id="30424-351">IPC 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-351">IPC hardware station</span></span> | <span data-ttu-id="30424-352">IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-352">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="30424-353">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="30424-353">Windows app</span></span> | <span data-ttu-id="30424-354">是</span><span class="sxs-lookup"><span data-stu-id="30424-354">Yes</span></span>                  | <span data-ttu-id="30424-355">是</span><span class="sxs-lookup"><span data-stu-id="30424-355">Yes</span></span>                  |
| <span data-ttu-id="30424-356">云 POS</span><span class="sxs-lookup"><span data-stu-id="30424-356">Cloud POS</span></span>   | <span data-ttu-id="30424-357">否</span><span class="sxs-lookup"><span data-stu-id="30424-357">No</span></span>                   | <span data-ttu-id="30424-358">是</span><span class="sxs-lookup"><span data-stu-id="30424-358">Yes</span></span>                  |
| <span data-ttu-id="30424-359">Android</span><span class="sxs-lookup"><span data-stu-id="30424-359">Android</span></span>     | <span data-ttu-id="30424-360">是</span><span class="sxs-lookup"><span data-stu-id="30424-360">Yes</span></span>                  | <span data-ttu-id="30424-361">是</span><span class="sxs-lookup"><span data-stu-id="30424-361">Yes</span></span>                  |
| <span data-ttu-id="30424-362">iOS</span><span class="sxs-lookup"><span data-stu-id="30424-362">iOS</span></span>         | <span data-ttu-id="30424-363">否</span><span class="sxs-lookup"><span data-stu-id="30424-363">No</span></span>                   | <span data-ttu-id="30424-364">是</span><span class="sxs-lookup"><span data-stu-id="30424-364">Yes</span></span>                  |

## <a name="supported-device-types-by-hardware-station-type"></a><span data-ttu-id="30424-365">硬件工作站类型支持的设备类型</span><span class="sxs-lookup"><span data-stu-id="30424-365">Supported device types by hardware station type</span></span>
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="30424-366">带 IPC（内置）硬件工作站的 Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="30424-366">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30424-367">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="30424-367">Supported device class</span></span></th>
<th><span data-ttu-id="30424-368">支持的接口</span><span class="sxs-lookup"><span data-stu-id="30424-368">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30424-369">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-369">Printer</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-370">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-370">OPOS</span></span></li>
<li><span data-ttu-id="30424-371">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="30424-371">Windows driver</span></span></li>
<li><span data-ttu-id="30424-372">设备</span><span class="sxs-lookup"><span data-stu-id="30424-372">Device</span></span></li>
<li><span data-ttu-id="30424-373">网络</span><span class="sxs-lookup"><span data-stu-id="30424-373">Network</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-374">打印机 2</span><span class="sxs-lookup"><span data-stu-id="30424-374">Printer 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-375">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-375">OPOS</span></span></li>
<li><span data-ttu-id="30424-376">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="30424-376">Windows driver</span></span></li>
<li><span data-ttu-id="30424-377">设备</span><span class="sxs-lookup"><span data-stu-id="30424-377">Device</span></span></li>
<li><span data-ttu-id="30424-378">网络</span><span class="sxs-lookup"><span data-stu-id="30424-378">Network</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-379">行显示内容</span><span class="sxs-lookup"><span data-stu-id="30424-379">Line display</span></span></td>
<td><span data-ttu-id="30424-380">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-380">OPOS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-381">双显示器</span><span class="sxs-lookup"><span data-stu-id="30424-381">Dual display</span></span></td>
<td><span data-ttu-id="30424-382">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="30424-382">Windows driver</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-383">MSR</span><span class="sxs-lookup"><span data-stu-id="30424-383">MSR</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-384">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-384">OPOS</span></span></li>
<li><span data-ttu-id="30424-385">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="30424-385">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="30424-386">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="30424-386">Keyboard wedge (No setup is required.)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-387">开票人</span><span class="sxs-lookup"><span data-stu-id="30424-387">Drawer</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-388">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-388">OPOS</span></span></li>
<li><span data-ttu-id="30424-389">网络</span><span class="sxs-lookup"><span data-stu-id="30424-389">Network</span></span> </br><span data-ttu-id="30424-390"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-390"><strong>Note:</strong> Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-391">开票人 2</span><span class="sxs-lookup"><span data-stu-id="30424-391">Drawer 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-392">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-392">OPOS</span></span></li>
<li><span data-ttu-id="30424-393">网络</span><span class="sxs-lookup"><span data-stu-id="30424-393">Network</span></span> </br><span data-ttu-id="30424-394"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-394"><strong>Note:</strong> Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-395">扫描仪</span><span class="sxs-lookup"><span data-stu-id="30424-395">Scanner</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-396">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-396">OPOS</span></span></li>
<li><span data-ttu-id="30424-397">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="30424-397">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="30424-398">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="30424-398">Keyboard wedge (No setup is required.)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-399">扫描仪 2</span><span class="sxs-lookup"><span data-stu-id="30424-399">Scanner 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-400">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-400">OPOS</span></span></li>
<li><span data-ttu-id="30424-401">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="30424-401">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="30424-402">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="30424-402">Keyboard wedge (No setup is required.)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-403">比例</span><span class="sxs-lookup"><span data-stu-id="30424-403">Scale</span></span></td>
<td><span data-ttu-id="30424-404">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-404">OPOS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-405">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="30424-405">PIN pad</span></span></td>
<td><span data-ttu-id="30424-406">OPOS（通过自定义付款连接器提供支持。）</span><span class="sxs-lookup"><span data-stu-id="30424-406">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-407">签名捕获</span><span class="sxs-lookup"><span data-stu-id="30424-407">Signature capture</span></span></td>
<td><span data-ttu-id="30424-408">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-408">OPOS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-409">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-409">Payment terminal</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-410">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="30424-410">Custom device support</span></span></li>
<li><span data-ttu-id="30424-411">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="30424-411">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a><span data-ttu-id="30424-412">有调配的“共享”IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="30424-412">All Modern POS clients that have a committed "Shared" IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="30424-413">当 IIS 硬件工作站为“已调配”时，POS 客户端与硬件工作站之间存在一对一关系。</span><span class="sxs-lookup"><span data-stu-id="30424-413">When the IIS hardware station is “committed” there is a one-to-one relationship between the POS client and the hardware station.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30424-414">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="30424-414">Supported device class</span></span></th>
<th><span data-ttu-id="30424-415">支持的接口</span><span class="sxs-lookup"><span data-stu-id="30424-415">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30424-416">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-416">Printer</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-417">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-417">OPOS</span></span></li>
<li><span data-ttu-id="30424-418">网络</span><span class="sxs-lookup"><span data-stu-id="30424-418">Network</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-419">打印机 2</span><span class="sxs-lookup"><span data-stu-id="30424-419">Printer 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-420">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-420">OPOS</span></span></li>
<li><span data-ttu-id="30424-421">网络</span><span class="sxs-lookup"><span data-stu-id="30424-421">Network</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-422">行显示</span><span class="sxs-lookup"><span data-stu-id="30424-422">Line display</span></span></td>
<td><span data-ttu-id="30424-423">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-423">OPOS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-424">MSR</span><span class="sxs-lookup"><span data-stu-id="30424-424">MSR</span></span></td>
<td><span data-ttu-id="30424-425">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-425">OPOS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-426">开票人</span><span class="sxs-lookup"><span data-stu-id="30424-426">Drawer</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-427">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-427">OPOS</span></span></li>
<li><span data-ttu-id="30424-428">网络</span><span class="sxs-lookup"><span data-stu-id="30424-428">Network</span></span> </br><span data-ttu-id="30424-429"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-429"><strong>Note:</strong> Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-430">开票人 2</span><span class="sxs-lookup"><span data-stu-id="30424-430">Drawer 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-431">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-431">OPOS</span></span></li>
<li><span data-ttu-id="30424-432">网络</span><span class="sxs-lookup"><span data-stu-id="30424-432">Network</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-433">扫描仪</span><span class="sxs-lookup"><span data-stu-id="30424-433">Scanner</span></span></td>
<td><span data-ttu-id="30424-434">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-434">OPOS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-435">扫描仪 2</span><span class="sxs-lookup"><span data-stu-id="30424-435">Scanner 2</span></span></td>
<td><span data-ttu-id="30424-436">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-436">OPOS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-437">比例</span><span class="sxs-lookup"><span data-stu-id="30424-437">Scale</span></span></td>
<td><span data-ttu-id="30424-438">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-438">OPOS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-439">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="30424-439">PIN pad</span></span></td>
<td><span data-ttu-id="30424-440">OPOS（通过自定义付款连接器提供支持。）</span><span class="sxs-lookup"><span data-stu-id="30424-440">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-441">签到</span><span class="sxs-lookup"><span data-stu-id="30424-441">Sig.</span></span> <span data-ttu-id="30424-442">捕获</span><span class="sxs-lookup"><span data-stu-id="30424-442">capture</span></span></td>
<td><span data-ttu-id="30424-443">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-443">OPOS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-444">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-444">Payment terminal</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-445">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="30424-445">Custom device support</span></span></li>
<li><span data-ttu-id="30424-446">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="30424-446">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-shared-an-iis-hardware-station"></a><span data-ttu-id="30424-447">所有 Modern POS 客户端都共享 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-447">All Modern POS clients shared an IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="30424-448">当 IIS 硬件工作站为“共享”时，多台设备可同时使用该硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-448">When the IIS hardware station is “shared,” multiple devices can use the hardware station at the same time.</span></span> <span data-ttu-id="30424-449">对于此方案，应仅使用下表中列出的设备。</span><span class="sxs-lookup"><span data-stu-id="30424-449">For this scenario, you should use only the devices that are listed in the following table.</span></span> <span data-ttu-id="30424-450">如果尝试共享此处未列出的设备（如条码扫描仪和 MSR），多台设备尝试声明同一外设时，将出错。</span><span class="sxs-lookup"><span data-stu-id="30424-450">If you try to share devices that aren't listed here, such as bar code scanners and MSRs, errors will occur when multiple devices try to claim the same peripheral.</span></span> <span data-ttu-id="30424-451">将来将明确阻止此类配置。</span><span class="sxs-lookup"><span data-stu-id="30424-451">In the future, such a configuration will be explicitly prevented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30424-452">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="30424-452">Supported device class</span></span></th>
<th><span data-ttu-id="30424-453">支持的接口</span><span class="sxs-lookup"><span data-stu-id="30424-453">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30424-454">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-454">Printer</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-455">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-455">OPOS</span></span></li>
<li><span data-ttu-id="30424-456">网络</span><span class="sxs-lookup"><span data-stu-id="30424-456">Network</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-457">打印机 2</span><span class="sxs-lookup"><span data-stu-id="30424-457">Printer 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-458">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-458">OPOS</span></span></li>
<li><span data-ttu-id="30424-459">网络</span><span class="sxs-lookup"><span data-stu-id="30424-459">Network</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-460">开票人</span><span class="sxs-lookup"><span data-stu-id="30424-460">Drawer</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-461">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-461">OPOS</span></span></li>
<li><span data-ttu-id="30424-462">网络</span><span class="sxs-lookup"><span data-stu-id="30424-462">Network</span></span> </br><span data-ttu-id="30424-463"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-463"><strong>Note:</strong> Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30424-464">开票人 2</span><span class="sxs-lookup"><span data-stu-id="30424-464">Drawer 2</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-465">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-465">OPOS</span></span></li>
<li><span data-ttu-id="30424-466">网络</span><span class="sxs-lookup"><span data-stu-id="30424-466">Network</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30424-467">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-467">Payment terminal</span></span></td>
<td><ul>
<li><span data-ttu-id="30424-468">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="30424-468">Custom device support</span></span></li>
<li><span data-ttu-id="30424-469">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="30424-469">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a><span data-ttu-id="30424-470">支持的方案的配置</span><span class="sxs-lookup"><span data-stu-id="30424-470">Configuration for supported scenarios</span></span>
<span data-ttu-id="30424-471">有关如何创建硬件配置文件的详细信息，请参阅[定义和维护渠道客户端，包括收银机和硬件工作站](define-maintain-channel-clients-registers-hw-stations.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-471">For more information about how to create hardware profiles, see [Define and maintain channel clients, including registers and hardware stations](define-maintain-channel-clients-registers-hw-stations.md).</span></span> 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="30424-472">带 IPC（内置）硬件工作站的 Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="30424-472">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<span data-ttu-id="30424-473">此配置是传统固定式 POS 收银机最典型的配置。</span><span class="sxs-lookup"><span data-stu-id="30424-473">This configuration is the most typical configuration for traditional, fixed POS registers.</span></span> <span data-ttu-id="30424-474">对于此方案，硬件配置文件信息直接映射到收银机。</span><span class="sxs-lookup"><span data-stu-id="30424-474">For this scenario, the hardware profile information is mapped directly to the register itself.</span></span> <span data-ttu-id="30424-475">还必须在收银机本身中设置 EFT 终端号。</span><span class="sxs-lookup"><span data-stu-id="30424-475">The EFT terminal number should also be set on the register itself.</span></span> <span data-ttu-id="30424-476">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="30424-476">To set up this configuration, follow these steps.</span></span>

1.  <span data-ttu-id="30424-477">创建在其中配置所有所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="30424-477">Create a hardware profile where all the required peripherals are configured.</span></span>
2.  <span data-ttu-id="30424-478">将硬件配置文件映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="30424-478">Map the hardware profile to the POS register.</span></span>
3.  <span data-ttu-id="30424-479">为将使用该 POS 收银机的商店创建一个类型为 **专用** 的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-479">Create a hardware station of the **Dedicated** type for the store where the POS register will be used.</span></span> <span data-ttu-id="30424-480">描述可选。</span><span class="sxs-lookup"><span data-stu-id="30424-480">A description is optional.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="30424-481">不必在硬件工作站中设置其他任何属性。</span><span class="sxs-lookup"><span data-stu-id="30424-481">You don't have to set any other properties on the hardware station.</span></span> <span data-ttu-id="30424-482">其他所有所需信息（如硬件配置文件）将来自收银机本身。</span><span class="sxs-lookup"><span data-stu-id="30424-482">All other required information, such as the hardware profile, will come from the register itself.</span></span>

4.  <span data-ttu-id="30424-483">单击 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="30424-483">Click **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
5.  <span data-ttu-id="30424-484">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="30424-484">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="30424-485">单击 **立即运行** 将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="30424-485">Click **Run now** to sync changes to the POS.</span></span>
6.  <span data-ttu-id="30424-486">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="30424-486">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="30424-487">单击 **立即运行** 将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="30424-487">Click **Run now** to sync changes to the POS.</span></span>
7.  <span data-ttu-id="30424-488">安装并激活 Modern POS for Windows。</span><span class="sxs-lookup"><span data-stu-id="30424-488">Install and activate Modern POS for Windows.</span></span>
8.  <span data-ttu-id="30424-489">启动 Modern POS for Windows，然后登录到连接的外设。</span><span class="sxs-lookup"><span data-stu-id="30424-489">Start Modern POS for Windows, and begin to use the connected peripheral devices.</span></span>

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="30424-490">带 IPC（内置）硬件工作站的 Modern POS for Android</span><span class="sxs-lookup"><span data-stu-id="30424-490">Modern POS for Android with an IPC (built-in) hardware station</span></span>

<span data-ttu-id="30424-491">**10.0.8 的新功能** - Modern POS for Android 应用现在支持通过 DK 端口连接到这些打印机的 Epson 网络打印机和银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-491">**New for 10.0.8** - Epson network printers and cash drawers connected to those printers via DK port are now supported for the Modern POS fo Android app.</span></span> <span data-ttu-id="30424-492">有关详细信息，请访问[在 Android 和 iOS 上安装 POS hybrid 应用](./dev-itpro/hybridapp.md)文章。</span><span class="sxs-lookup"><span data-stu-id="30424-492">For details, visit the [Set up POS hybrid app on Android and iOS](./dev-itpro/hybridapp.md) article.</span></span>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a><span data-ttu-id="30424-493">有调配的“共享”IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="30424-493">All Modern POS clients that have a committed, shared IIS hardware station</span></span>

<span data-ttu-id="30424-494">可将此配置用于有一个硬件工作站仅供一台 POS 收银机专用的所有 Modern POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="30424-494">This configuration can be used for all Modern POS clients that have a hardware station that is used exclusively by one POS register.</span></span> <span data-ttu-id="30424-495">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="30424-495">To set up this configuration, follow these steps.</span></span>

1.  <span data-ttu-id="30424-496">创建在其中配置所有所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="30424-496">Create a hardware profile where all the required peripherals are configured.</span></span>
2.  <span data-ttu-id="30424-497">为将使用该 POS 收银机的商店创建一个类型为 **专用** 的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-497">Create a hardware station of the **Dedicated** type for the store where the POS register will be used.</span></span>
3.  <span data-ttu-id="30424-498">在专用硬件工作站中，设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="30424-498">On the dedicated hardware station, set the following properties:</span></span>
    -   <span data-ttu-id="30424-499">**主机名** – 将运行硬件工作站的主计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="30424-499">**Host name** – The name of the host computer where the hardware station will run.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="30424-500">Cloud POS 可以解析 **localhost** 以确定运行 Cloud POS 的本地计算机。</span><span class="sxs-lookup"><span data-stu-id="30424-500">Cloud POS can resolve **localhost** to determine the local computer where Cloud POS is running.</span></span> <span data-ttu-id="30424-501">但是，将 Cloud POS 与硬件工作站配对所需证书必须也采用“Localhost”来充当计算机名称。</span><span class="sxs-lookup"><span data-stu-id="30424-501">However, the certificate that is required in order to pair Cloud POS with the hardware station must also have "Localhost" as the computer name.</span></span> <span data-ttu-id="30424-502">若要避免问题，建议您根据列出商店每个专用硬件工作站的实例。</span><span class="sxs-lookup"><span data-stu-id="30424-502">To avoid issues, we recommend that you list an instance of each dedicated hardware station for the store, as required.</span></span> <span data-ttu-id="30424-503">对于每个硬件工作站，主机名应该是将部署硬件工作站的具体计算机名称。</span><span class="sxs-lookup"><span data-stu-id="30424-503">For each hardware station, the host name should be the specific computer name where the hardware station will be deployed.</span></span>
    
    -   <span data-ttu-id="30424-504">**端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。</span><span class="sxs-lookup"><span data-stu-id="30424-504">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    -   <span data-ttu-id="30424-505">**硬件配置文件** – 如果硬件工作站本身中不提供硬件配置文件，将使用为收银机分配的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="30424-505">**Hardware profile** – If the hardware profile isn't provided on the hardware station itself, the hardware profile that is assigned to the register will be used.</span></span>
    -   <span data-ttu-id="30424-506">**EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="30424-506">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="30424-507">此 ID 由信用卡处理方提供。</span><span class="sxs-lookup"><span data-stu-id="30424-507">This ID is provided by the credit card processor.</span></span>
    -   <span data-ttu-id="30424-508">**包名** – 部署硬件工作站时要使用的硬件工作站包。</span><span class="sxs-lookup"><span data-stu-id="30424-508">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4.  <span data-ttu-id="30424-509">单击 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="30424-509">Click **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
5.  <span data-ttu-id="30424-510">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="30424-510">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="30424-511">单击 **立即运行** 将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="30424-511">Click **Run now** to sync changes to the POS.</span></span>
6.  <span data-ttu-id="30424-512">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="30424-512">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="30424-513">单击 **立即运行** 将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="30424-513">Click **Run now** to sync changes to the POS.</span></span>
7.  <span data-ttu-id="30424-514">安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-514">Install the hardware station.</span></span> <span data-ttu-id="30424-515">有关如何安装硬件工作站的详细信息，请参阅[配置和安装 Retail 硬件工作站](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-515">For more information about how to install the hardware station, see [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md).</span></span>
8.  <span data-ttu-id="30424-516">安装和激活 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="30424-516">Install and activate Modern POS.</span></span> <span data-ttu-id="30424-517">有关如何安装 Modern POS 的详细信息，请参阅[配置、安装和激活 Modern POS (MPOS)](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-517">For more information about how to install Modern POS, see [Configure, install and activate Modern POS (MPOS)](retail-modern-pos-device-activation.md).</span></span>
9.  <span data-ttu-id="30424-518">登录 Modern POS，然后选择 **执行非开票人操作**。</span><span class="sxs-lookup"><span data-stu-id="30424-518">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
10. <span data-ttu-id="30424-519">启动 **管理硬件工作站** 操作。</span><span class="sxs-lookup"><span data-stu-id="30424-519">Start the **Manage hardware stations** operation.</span></span>
11. <span data-ttu-id="30424-520">单击 **管理**。</span><span class="sxs-lookup"><span data-stu-id="30424-520">Click **Manage**.</span></span>
12. <span data-ttu-id="30424-521">在硬件工作站管理页中，设置用于打开硬件工作站的选项。</span><span class="sxs-lookup"><span data-stu-id="30424-521">On the hardware station management page, set the option to turn on the hardware station.</span></span>
13. <span data-ttu-id="30424-522">选择要使用的硬件工作站，然后单击 **配对**。</span><span class="sxs-lookup"><span data-stu-id="30424-522">Select the hardware station to use, and then click **Pair**.</span></span>
14. <span data-ttu-id="30424-523">在硬件工作站配对后，单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="30424-523">After the hardware station is paired, click **Close**.</span></span>
15. <span data-ttu-id="30424-524">在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。</span><span class="sxs-lookup"><span data-stu-id="30424-524">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="30424-525">有共享 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="30424-525">All Modern POS clients that have a shared IIS hardware station</span></span>

<span data-ttu-id="30424-526">此配置可用于与其他设备共享硬件工作站的所有 Modern POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="30424-526">This configuration can be used for all Modern POS clients that share hardware stations with other devices.</span></span> <span data-ttu-id="30424-527">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="30424-527">To set up this configuration, follow these steps.</span></span>

1.  <span data-ttu-id="30424-528">创建在其中配置所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="30424-528">Create a hardware profile where the required peripherals are configured.</span></span>
2.  <span data-ttu-id="30424-529">为将使用该 POS 收银机的商店创建一个类型为 **共享** 的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-529">Create a hardware station of the **Shared** type for the store where the POS register will be used.</span></span>
3.  <span data-ttu-id="30424-530">在共享硬件工作站中，设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="30424-530">On the shared hardware station, set the following properties:</span></span>
    -   <span data-ttu-id="30424-531">**主机名** – 将运行硬件工作站的主计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="30424-531">**Host name** – The name of the host computer where the hardware station will run.</span></span>
    -   <span data-ttu-id="30424-532">**描述** – 用于帮助识别硬件工作站的文本，如 **退货** 或 **店前**。</span><span class="sxs-lookup"><span data-stu-id="30424-532">**Description** – Text that will help identify the hardware station, such as **Returns** or **Front of store**.</span></span>
    -   <span data-ttu-id="30424-533">**端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。</span><span class="sxs-lookup"><span data-stu-id="30424-533">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    -   <span data-ttu-id="30424-534">**硬件配置文件** – 对于共享硬件工作站，每个硬件工作站都应该有一个硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="30424-534">**Hardware profile** – For shared hardware stations, each hardware station should have a hardware profile.</span></span> <span data-ttu-id="30424-535">可以在硬件工作站之间共享硬件配置文件，但必须将其映射到每个硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-535">Hardware profiles can be shared among hardware stations, but they must be mapped to each hardware station.</span></span> <span data-ttu-id="30424-536">此外，建议在多个设备共享同一个共享硬件工作站时使用共享班次。</span><span class="sxs-lookup"><span data-stu-id="30424-536">In addition, we recommend that you use shared shifts when multiple devices use the same shared hardware station.</span></span> <span data-ttu-id="30424-537">若要设置共享班次，单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="30424-537">To set up a shared shift, click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="30424-538">对于每个共享硬件配置文件，选择银箱，然后将 **共享班次银箱** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="30424-538">For each shared hardware profile, select the cash drawer, and set the **Shared shift drawer** option to **Yes**.</span></span>
    -   <span data-ttu-id="30424-539">**EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="30424-539">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="30424-540">此 ID 由信用卡处理方提供。</span><span class="sxs-lookup"><span data-stu-id="30424-540">This ID is provided by the credit card processor.</span></span>
    -   <span data-ttu-id="30424-541">**包名** – 部署硬件工作站时要使用的硬件工作站包。</span><span class="sxs-lookup"><span data-stu-id="30424-541">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4.  <span data-ttu-id="30424-542">为商店中所需其他每个硬件工作站重复步骤 2 和 3。</span><span class="sxs-lookup"><span data-stu-id="30424-542">Repeat steps 2 and 3 for each additional hardware station that is required in the store.</span></span>
5.  <span data-ttu-id="30424-543">单击 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="30424-543">Click **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6.  <span data-ttu-id="30424-544">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="30424-544">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="30424-545">单击 **立即运行** 将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="30424-545">Click **Run now** to sync changes to the POS.</span></span>
7.  <span data-ttu-id="30424-546">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="30424-546">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="30424-547">单击 **立即运行** 将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="30424-547">Click **Run now** to sync changes to the POS.</span></span>
8.  <span data-ttu-id="30424-548">在步骤 2 和 3 中设置的每个主机上安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-548">Install the hardware station on each host computer that you set up in steps 2 and 3.</span></span> <span data-ttu-id="30424-549">有关如何安装硬件工作站的详细信息，请参阅[配置和安装 Retail 硬件工作站](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-549">For more information about how to install the hardware station, see [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md).</span></span>
9.  <span data-ttu-id="30424-550">安装和激活 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="30424-550">Install and activate Modern POS.</span></span> <span data-ttu-id="30424-551">有关如何安装 Modern POS 的详细信息，请参阅[配置、安装和激活 Modern POS (MPOS)](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-551">For more information about how to install Modern POS, see [Configure, install, and activate Modern POS (MPOS)](retail-modern-pos-device-activation.md).</span></span>
10. <span data-ttu-id="30424-552">登录 Modern POS，然后选择 **执行非开票人操作**。</span><span class="sxs-lookup"><span data-stu-id="30424-552">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
11. <span data-ttu-id="30424-553">启动 **管理硬件工作站** 操作。</span><span class="sxs-lookup"><span data-stu-id="30424-553">Start the **Manage hardware stations** operation.</span></span>

12. <span data-ttu-id="30424-554">单击 **管理**。</span><span class="sxs-lookup"><span data-stu-id="30424-554">Click **Manage**.</span></span>
13. <span data-ttu-id="30424-555">在硬件工作站管理页中，设置用于打开硬件工作站的选项。</span><span class="sxs-lookup"><span data-stu-id="30424-555">On the hardware station management page, set the option to turn on the hardware station.</span></span>
14. <span data-ttu-id="30424-556">选择要使用的硬件工作站，然后单击 **配对**。</span><span class="sxs-lookup"><span data-stu-id="30424-556">Select the hardware station to use, and then click **Pair**.</span></span>
15. <span data-ttu-id="30424-557">为 Modern POS 将使用的每个硬件工作站重复步骤 14。</span><span class="sxs-lookup"><span data-stu-id="30424-557">Repeat step 14 for each hardware station that Modern POS will use.</span></span>
16. <span data-ttu-id="30424-558">为所需全部硬件工作站配对之后，单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="30424-558">After all the required hardware stations are paired, click **Close**.</span></span>
17. <span data-ttu-id="30424-559">在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。</span><span class="sxs-lookup"><span data-stu-id="30424-559">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span> 

> [!NOTE]
> <span data-ttu-id="30424-560">如果设备经常使用不同硬件工作站，建议将 Modern POS 配置为收银员开始收款过程时提示其选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-560">If devices often use different hardware stations, we recommend that you configure Modern POS to prompt cashiers to select a hardware station when they begin the tender process.</span></span> <span data-ttu-id="30424-561">单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="30424-561">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="30424-562">选择收银机，然后将 **收款后即可选择** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="30424-562">Select the register, and then set the **Select upon tender** option to **Yes**.</span></span> <span data-ttu-id="30424-563">使用 **1090** 配送计划将更改同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="30424-563">Use the **1090** distribution schedule to sync changes to the channel database.</span></span>

## <a name="extensibility"></a><span data-ttu-id="30424-564">可扩展性</span><span class="sxs-lookup"><span data-stu-id="30424-564">Extensibility</span></span>
<span data-ttu-id="30424-565">有关硬件工作站的可扩展性方案的信息，请参阅[硬件工作站可扩展性](dev-itpro/hardware-station-extensibility.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-565">For information about extensibility scenarios for the hardware station, see [Hardware Station extensibility](dev-itpro/hardware-station-extensibility.md).</span></span>

## <a name="security"></a><span data-ttu-id="30424-566">安全性</span><span class="sxs-lookup"><span data-stu-id="30424-566">Security</span></span>
<span data-ttu-id="30424-567">根据当前安全标准，以下设置应用于生产环境：</span><span class="sxs-lookup"><span data-stu-id="30424-567">According to current security standards, the following settings should be used in a production environment:</span></span> 

### <a name="hardware-station-installer"></a><span data-ttu-id="30424-568">硬件工作站安装程序</span><span class="sxs-lookup"><span data-stu-id="30424-568">Hardware station installer</span></span>
<span data-ttu-id="30424-569">硬件工作站安装程序将在安装期间通过自助服务自动执行这些注册表编辑。</span><span class="sxs-lookup"><span data-stu-id="30424-569">The hardware station installer will automatically make these registry edits as part of the installation through self-service.</span></span>
 
-   <span data-ttu-id="30424-570">应禁用安全套接字层 (SSL)。</span><span class="sxs-lookup"><span data-stu-id="30424-570">Secure Sockets Layer (SSL) should be disabled.</span></span>
-   <span data-ttu-id="30424-571">应启用并使用传输层安全性 (TLS) 版本 1.2（或当前最高版本）。</span><span class="sxs-lookup"><span data-stu-id="30424-571">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span> 

### <a name="ssl-and-tls"></a><span data-ttu-id="30424-572">SSL 和 TLS</span><span class="sxs-lookup"><span data-stu-id="30424-572">SSL and TLS</span></span>
<span data-ttu-id="30424-573">默认情况下，已禁用 SSL 和除 TLS 1.2 外的所有 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="30424-573">By default, SSL and all version of TLS except TLS 1.2 are disabled.</span></span> <span data-ttu-id="30424-574">要编辑或启用这些值，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="30424-574">To edit or enable these values, follow these steps:</span></span>
    1.  <span data-ttu-id="30424-575">按 Windows 徽标键+R 打开 **运行** 窗口。</span><span class="sxs-lookup"><span data-stu-id="30424-575">Press the Windows logo key+R to open a **Run** window.</span></span>
    2.  <span data-ttu-id="30424-576">在 **打开** 字段中，键入 **Regedit**，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="30424-576">In the **Open** field, type **Regedit**, and then click **OK**.</span></span>
    3.  <span data-ttu-id="30424-577">如果显示 **用户帐户控制** 消息框，请单击 **是**。</span><span class="sxs-lookup"><span data-stu-id="30424-577">If a **User Account Control** message box appears, click **Yes**.</span></span>
    4.  <span data-ttu-id="30424-578">在 **注册表编辑器** 窗口中，导航至 **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**。</span><span class="sxs-lookup"><span data-stu-id="30424-578">In the **Registry Editor** window, navigate to **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**.</span></span> <span data-ttu-id="30424-579">以自动输入了以下键，以便仅允许 TLS 1.2。</span><span class="sxs-lookup"><span data-stu-id="30424-579">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>
        -   <span data-ttu-id="30424-580">TLS 1.2Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="30424-580">TLS 1.2Server:Enabled=1</span></span>
        -   <span data-ttu-id="30424-581">TLS 1.2Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="30424-581">TLS 1.2Server:DisabledByDefault=0</span></span>
        -   <span data-ttu-id="30424-582">TLS 1.2Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="30424-582">TLS 1.2Client:Enabled=1</span></span>
        -   <span data-ttu-id="30424-583">TLS 1.2Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="30424-583">TLS 1.2Client:DisabledByDefault=0</span></span>
        -   <span data-ttu-id="30424-584">TLS 1.1Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-584">TLS 1.1Server:Enabled=0</span></span>
        -   <span data-ttu-id="30424-585">TLS 1.1Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-585">TLS 1.1Client:Enabled=0</span></span>
        -   <span data-ttu-id="30424-586">TLS 1.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-586">TLS 1.0Server:Enabled=0</span></span>
        -   <span data-ttu-id="30424-587">TLS 1.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-587">TLS 1.0Client:Enabled=0</span></span>
        -   <span data-ttu-id="30424-588">SSL 3.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-588">SSL 3.0Server:Enabled=0</span></span>
        -   <span data-ttu-id="30424-589">SSL 3.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-589">SSL 3.0Client:Enabled=0</span></span>
        -   <span data-ttu-id="30424-590">SSL 2.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-590">SSL 2.0Server:Enabled=0</span></span>
        -   <span data-ttu-id="30424-591">SSL 2.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="30424-591">SSL 2.0Client:Enabled=0</span></span>
-   <span data-ttu-id="30424-592">除非已知的具体原因所需，否则不应开放其他任何网络端口。</span><span class="sxs-lookup"><span data-stu-id="30424-592">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
-   <span data-ttu-id="30424-593">必须禁用跨源资源共享，并且必须指定允许接受的源。</span><span class="sxs-lookup"><span data-stu-id="30424-593">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
-   <span data-ttu-id="30424-594">应仅使用可信证书机构获取将在运行硬件工作站的计算机上使用的证书。</span><span class="sxs-lookup"><span data-stu-id="30424-594">Only trusted certificate authorities should be used to obtain certificates that will be used on computers that run the hardware station.</span></span>

> [!NOTE]
> <span data-ttu-id="30424-595">请务必仔细阅读 IIS 和 Payment Card Industry (PCI) 要求的安全指南。</span><span class="sxs-lookup"><span data-stu-id="30424-595">It’s very important that you review security guidelines for IIS and the Payment Card Industry (PCI) requirements.</span></span>

## <a name="peripheral-simulator"></a><span data-ttu-id="30424-596">外围设备模拟器</span><span class="sxs-lookup"><span data-stu-id="30424-596">Peripheral simulator</span></span>
<span data-ttu-id="30424-597">有关信息，请参阅 [Commerce 的外设模拟器](dev-itpro/retail-peripheral-simulator.md)。</span><span class="sxs-lookup"><span data-stu-id="30424-597">For information, see [Peripheral simulator for Commerce](dev-itpro/retail-peripheral-simulator.md).</span></span>

## <a name="microsoft-tested-peripheral-devices"></a><span data-ttu-id="30424-598">经过 Microsoft 测试的外设</span><span class="sxs-lookup"><span data-stu-id="30424-598">Microsoft-tested peripheral devices</span></span>
### <a name="ipc-built-in-hardware-station"></a><span data-ttu-id="30424-599">IPC（内置）硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-599">IPC (built-in) hardware station</span></span>

<span data-ttu-id="30424-600">已通过 Modern POS for Windows 中的内置 IPC 硬件工作站测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="30424-600">The following peripherals were tested by using the IPC hardware station that is built into Modern POS for Windows.</span></span>

#### <a name="printer"></a><span data-ttu-id="30424-601">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-601">Printer</span></span>

| <span data-ttu-id="30424-602">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-602">Manufacturer</span></span> | <span data-ttu-id="30424-603">型号</span><span class="sxs-lookup"><span data-stu-id="30424-603">Model</span></span>    | <span data-ttu-id="30424-604">接口</span><span class="sxs-lookup"><span data-stu-id="30424-604">Interface</span></span> | <span data-ttu-id="30424-605">注释</span><span class="sxs-lookup"><span data-stu-id="30424-605">Comments</span></span>                |
|--------------|----------|-----------|-------------------------|
| <span data-ttu-id="30424-606">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-606">Epson</span></span>        | <span data-ttu-id="30424-607">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="30424-607">Tm-T88IV</span></span> | <span data-ttu-id="30424-608">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-608">OPOS</span></span>      |                         |
| <span data-ttu-id="30424-609">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-609">Epson</span></span>        | <span data-ttu-id="30424-610">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="30424-610">TM-T88V</span></span>  | <span data-ttu-id="30424-611">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-611">OPOS</span></span>      |                         |
| <span data-ttu-id="30424-612">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-612">Epson</span></span>        | <span data-ttu-id="30424-613">TM-T88</span><span class="sxs-lookup"><span data-stu-id="30424-613">TM-T88</span></span>   | <span data-ttu-id="30424-614">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-614">Custom</span></span>    | <span data-ttu-id="30424-615">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-615">Connected via network</span></span>   |
| <span data-ttu-id="30424-616">Star</span><span class="sxs-lookup"><span data-stu-id="30424-616">Star</span></span>         | <span data-ttu-id="30424-617">TSP650II</span><span class="sxs-lookup"><span data-stu-id="30424-617">TSP650II</span></span> | <span data-ttu-id="30424-618">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-618">Custom</span></span>    | <span data-ttu-id="30424-619">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-619">Connected via network</span></span>   |
| <span data-ttu-id="30424-620">Star</span><span class="sxs-lookup"><span data-stu-id="30424-620">Star</span></span>         | <span data-ttu-id="30424-621">mPOP</span><span class="sxs-lookup"><span data-stu-id="30424-621">mPOP</span></span>     | <span data-ttu-id="30424-622">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-622">OPOS</span></span>      | <span data-ttu-id="30424-623">通过 Bluetooth 连接</span><span class="sxs-lookup"><span data-stu-id="30424-623">Connected via Bluetooth</span></span> |
| <span data-ttu-id="30424-624">HP</span><span class="sxs-lookup"><span data-stu-id="30424-624">HP</span></span>           | <span data-ttu-id="30424-625">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="30424-625">F7M67AA</span></span>  | <span data-ttu-id="30424-626">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-626">OPOS</span></span>      | <span data-ttu-id="30424-627">带电 USB</span><span class="sxs-lookup"><span data-stu-id="30424-627">Powered USB</span></span>             |

> [!NOTE]
> <span data-ttu-id="30424-628">内置硬件工作站不支持 Star TSP 100 打印机。</span><span class="sxs-lookup"><span data-stu-id="30424-628">The Star TSP 100 printer isn't supported for the built-in hardware station.</span></span> <span data-ttu-id="30424-629">内置硬件工作站使用 64 位进程，此进程与现有的 Star TP 100 驱动程序不兼容。</span><span class="sxs-lookup"><span data-stu-id="30424-629">The built-in hardware station uses a 64-bit process, which isn't compatible with existing Star TP 100 drivers.</span></span> 

#### <a name="bar-code-scanner"></a><span data-ttu-id="30424-630">条码扫描仪</span><span class="sxs-lookup"><span data-stu-id="30424-630">Bar code scanner</span></span>

| <span data-ttu-id="30424-631">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-631">Manufacturer</span></span>  | <span data-ttu-id="30424-632">型号</span><span class="sxs-lookup"><span data-stu-id="30424-632">Model</span></span>         | <span data-ttu-id="30424-633">接口</span><span class="sxs-lookup"><span data-stu-id="30424-633">Interface</span></span> | <span data-ttu-id="30424-634">注释</span><span class="sxs-lookup"><span data-stu-id="30424-634">Comments</span></span> |
|---------------|---------------|-----------|----------|
| <span data-ttu-id="30424-635">Motorola</span><span class="sxs-lookup"><span data-stu-id="30424-635">Motorola</span></span>      | <span data-ttu-id="30424-636">DS9208</span><span class="sxs-lookup"><span data-stu-id="30424-636">DS9208</span></span>        | <span data-ttu-id="30424-637">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-637">OPOS</span></span>      |          |
| <span data-ttu-id="30424-638">Honeywell</span><span class="sxs-lookup"><span data-stu-id="30424-638">Honeywell</span></span>     | <span data-ttu-id="30424-639">1900</span><span class="sxs-lookup"><span data-stu-id="30424-639">1900</span></span>          | <span data-ttu-id="30424-640">UWP</span><span class="sxs-lookup"><span data-stu-id="30424-640">UWP</span></span>       |          |
| <span data-ttu-id="30424-641">符号</span><span class="sxs-lookup"><span data-stu-id="30424-641">Symbol</span></span>        | <span data-ttu-id="30424-642">LS2208</span><span class="sxs-lookup"><span data-stu-id="30424-642">LS2208</span></span>        | <span data-ttu-id="30424-643">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-643">OPOS</span></span>      |          |
| <span data-ttu-id="30424-644">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="30424-644">HP Integrated</span></span> | <span data-ttu-id="30424-645">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="30424-645">E1L07AA</span></span>       | <span data-ttu-id="30424-646">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-646">OPOS</span></span>      |          |
| <span data-ttu-id="30424-647">Datalogic</span><span class="sxs-lookup"><span data-stu-id="30424-647">Datalogic</span></span>     | <span data-ttu-id="30424-648">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="30424-648">Magellan 8400</span></span> | <span data-ttu-id="30424-649">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-649">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="30424-650">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="30424-650">PIN pad</span></span>

| <span data-ttu-id="30424-651">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-651">Manufacturer</span></span> | <span data-ttu-id="30424-652">型号</span><span class="sxs-lookup"><span data-stu-id="30424-652">Model</span></span>  | <span data-ttu-id="30424-653">接口</span><span class="sxs-lookup"><span data-stu-id="30424-653">Interface</span></span> | <span data-ttu-id="30424-654">评论</span><span class="sxs-lookup"><span data-stu-id="30424-654">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="30424-655">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-655">VeriFone</span></span>     | <span data-ttu-id="30424-656">1000SE</span><span class="sxs-lookup"><span data-stu-id="30424-656">1000SE</span></span> | <span data-ttu-id="30424-657">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-657">OPOS</span></span>      | <span data-ttu-id="30424-658">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="30424-658">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="30424-659">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-659">Payment terminal</span></span>

| <span data-ttu-id="30424-660">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-660">Manufacturer</span></span> | <span data-ttu-id="30424-661">型号</span><span class="sxs-lookup"><span data-stu-id="30424-661">Model</span></span> | <span data-ttu-id="30424-662">接口</span><span class="sxs-lookup"><span data-stu-id="30424-662">Interface</span></span> | <span data-ttu-id="30424-663">评论</span><span class="sxs-lookup"><span data-stu-id="30424-663">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="30424-664">Equinox</span><span class="sxs-lookup"><span data-stu-id="30424-664">Equinox</span></span>      | <span data-ttu-id="30424-665">L5300</span><span class="sxs-lookup"><span data-stu-id="30424-665">L5300</span></span> | <span data-ttu-id="30424-666">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-666">Custom</span></span>    | <span data-ttu-id="30424-667">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="30424-667">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="30424-668">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-668">VeriFone</span></span>     | <span data-ttu-id="30424-669">MX925</span><span class="sxs-lookup"><span data-stu-id="30424-669">MX925</span></span> | <span data-ttu-id="30424-670">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-670">Custom</span></span>    | <span data-ttu-id="30424-671">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="30424-671">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="30424-672">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-672">VeriFone</span></span>     | <span data-ttu-id="30424-673">MX915</span><span class="sxs-lookup"><span data-stu-id="30424-673">MX915</span></span> | <span data-ttu-id="30424-674">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-674">Custom</span></span>    | <span data-ttu-id="30424-675">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="30424-675">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="30424-676">银箱</span><span class="sxs-lookup"><span data-stu-id="30424-676">Cash drawer</span></span>

| <span data-ttu-id="30424-677">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-677">Manufacturer</span></span> | <span data-ttu-id="30424-678">型号</span><span class="sxs-lookup"><span data-stu-id="30424-678">Model</span></span>     | <span data-ttu-id="30424-679">接口</span><span class="sxs-lookup"><span data-stu-id="30424-679">Interface</span></span> | <span data-ttu-id="30424-680">评论</span><span class="sxs-lookup"><span data-stu-id="30424-680">Comments</span></span>                |
|--------------|-----------|-----------|-------------------------|
| <span data-ttu-id="30424-681">Star</span><span class="sxs-lookup"><span data-stu-id="30424-681">Star</span></span>         | <span data-ttu-id="30424-682">mPOP</span><span class="sxs-lookup"><span data-stu-id="30424-682">mPOP</span></span>      | <span data-ttu-id="30424-683">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-683">OPOS</span></span>      | <span data-ttu-id="30424-684">通过 Bluetooth 连接</span><span class="sxs-lookup"><span data-stu-id="30424-684">Connected via Bluetooth</span></span> |
| <span data-ttu-id="30424-685">APG</span><span class="sxs-lookup"><span data-stu-id="30424-685">APG</span></span>          | <span data-ttu-id="30424-686">Atwood</span><span class="sxs-lookup"><span data-stu-id="30424-686">Atwood</span></span>    | <span data-ttu-id="30424-687">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-687">Custom</span></span>    | <span data-ttu-id="30424-688">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-688">Connected via network</span></span>   |
| <span data-ttu-id="30424-689">Star</span><span class="sxs-lookup"><span data-stu-id="30424-689">Star</span></span>         | <span data-ttu-id="30424-690">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="30424-690">SMD2-1317</span></span> | <span data-ttu-id="30424-691">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-691">OPOS</span></span>      |                         |
| <span data-ttu-id="30424-692">HP</span><span class="sxs-lookup"><span data-stu-id="30424-692">HP</span></span>           | <span data-ttu-id="30424-693">QT457AA</span><span class="sxs-lookup"><span data-stu-id="30424-693">QT457AA</span></span>   | <span data-ttu-id="30424-694">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-694">OPOS</span></span>      |                         |
| <span data-ttu-id="30424-695">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-695">Epson</span></span>        |           | <span data-ttu-id="30424-696">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-696">Custom</span></span>    | <span data-ttu-id="30424-697">已通过 DK 端口连接到网络 Epson 打印机</span><span class="sxs-lookup"><span data-stu-id="30424-697">Connected to network Epson printer via DK port</span></span> |

#### <a name="line-display"></a><span data-ttu-id="30424-698">行显示</span><span class="sxs-lookup"><span data-stu-id="30424-698">Line display</span></span>

| <span data-ttu-id="30424-699">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-699">Manufacturer</span></span>  | <span data-ttu-id="30424-700">型号</span><span class="sxs-lookup"><span data-stu-id="30424-700">Model</span></span>   | <span data-ttu-id="30424-701">接口</span><span class="sxs-lookup"><span data-stu-id="30424-701">Interface</span></span> | <span data-ttu-id="30424-702">注释</span><span class="sxs-lookup"><span data-stu-id="30424-702">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="30424-703">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="30424-703">HP integrated</span></span> | <span data-ttu-id="30424-704">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="30424-704">G6U79AA</span></span> | <span data-ttu-id="30424-705">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-705">OPOS</span></span>      |          |
| <span data-ttu-id="30424-706">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-706">Epson</span></span>         | <span data-ttu-id="30424-707">M58DC</span><span class="sxs-lookup"><span data-stu-id="30424-707">M58DC</span></span>   | <span data-ttu-id="30424-708">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-708">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="30424-709">签名捕获</span><span class="sxs-lookup"><span data-stu-id="30424-709">Signature capture</span></span>

| <span data-ttu-id="30424-710">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-710">Manufacturer</span></span> | <span data-ttu-id="30424-711">型号</span><span class="sxs-lookup"><span data-stu-id="30424-711">Model</span></span>  | <span data-ttu-id="30424-712">接口</span><span class="sxs-lookup"><span data-stu-id="30424-712">Interface</span></span> | <span data-ttu-id="30424-713">评论</span><span class="sxs-lookup"><span data-stu-id="30424-713">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="30424-714">Scriptel</span><span class="sxs-lookup"><span data-stu-id="30424-714">Scriptel</span></span>     | <span data-ttu-id="30424-715">ST1550</span><span class="sxs-lookup"><span data-stu-id="30424-715">ST1550</span></span> | <span data-ttu-id="30424-716">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-716">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="30424-717">比例</span><span class="sxs-lookup"><span data-stu-id="30424-717">Scale</span></span>

| <span data-ttu-id="30424-718">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-718">Manufacturer</span></span> | <span data-ttu-id="30424-719">型号</span><span class="sxs-lookup"><span data-stu-id="30424-719">Model</span></span>         | <span data-ttu-id="30424-720">接口</span><span class="sxs-lookup"><span data-stu-id="30424-720">Interface</span></span> | <span data-ttu-id="30424-721">评论</span><span class="sxs-lookup"><span data-stu-id="30424-721">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="30424-722">Datalogic</span><span class="sxs-lookup"><span data-stu-id="30424-722">Datalogic</span></span>    | <span data-ttu-id="30424-723">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="30424-723">Magellan 8400</span></span> | <span data-ttu-id="30424-724">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-724">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="30424-725">MSR</span><span class="sxs-lookup"><span data-stu-id="30424-725">MSR</span></span>

| <span data-ttu-id="30424-726">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-726">Manufacturer</span></span> | <span data-ttu-id="30424-727">型号</span><span class="sxs-lookup"><span data-stu-id="30424-727">Model</span></span>       | <span data-ttu-id="30424-728">接口</span><span class="sxs-lookup"><span data-stu-id="30424-728">Interface</span></span> | <span data-ttu-id="30424-729">评论</span><span class="sxs-lookup"><span data-stu-id="30424-729">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="30424-730">Magtek</span><span class="sxs-lookup"><span data-stu-id="30424-730">Magtek</span></span>       | <span data-ttu-id="30424-731">21073075</span><span class="sxs-lookup"><span data-stu-id="30424-731">21073075</span></span>    | <span data-ttu-id="30424-732">UWP</span><span class="sxs-lookup"><span data-stu-id="30424-732">UWP</span></span>       |          |
| <span data-ttu-id="30424-733">Magtek</span><span class="sxs-lookup"><span data-stu-id="30424-733">Magtek</span></span>       | <span data-ttu-id="30424-734">21073062</span><span class="sxs-lookup"><span data-stu-id="30424-734">21073062</span></span>    | <span data-ttu-id="30424-735">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-735">OPOS</span></span>      |          |
| <span data-ttu-id="30424-736">HP</span><span class="sxs-lookup"><span data-stu-id="30424-736">HP</span></span>           | <span data-ttu-id="30424-737">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="30424-737">IDRA-334133</span></span> | <span data-ttu-id="30424-738">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-738">OPOS</span></span>      |          |

### <a name="dedicated-iis-hardware-station"></a><span data-ttu-id="30424-739">专用 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-739">Dedicated IIS hardware station</span></span>

<span data-ttu-id="30424-740">已使用专用（而非共享）IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="30424-740">The following peripherals were tested by using a dedicated (not shared) IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

#### <a name="printer"></a><span data-ttu-id="30424-741">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-741">Printer</span></span>

| <span data-ttu-id="30424-742">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-742">Manufacturer</span></span> | <span data-ttu-id="30424-743">型号</span><span class="sxs-lookup"><span data-stu-id="30424-743">Model</span></span>    | <span data-ttu-id="30424-744">接口</span><span class="sxs-lookup"><span data-stu-id="30424-744">Interface</span></span> | <span data-ttu-id="30424-745">注释</span><span class="sxs-lookup"><span data-stu-id="30424-745">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="30424-746">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-746">Epson</span></span>        | <span data-ttu-id="30424-747">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="30424-747">Tm-T88IV</span></span> | <span data-ttu-id="30424-748">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-748">OPOS</span></span>      |                           |
| <span data-ttu-id="30424-749">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-749">Epson</span></span>        | <span data-ttu-id="30424-750">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="30424-750">TM-T88V</span></span>  | <span data-ttu-id="30424-751">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-751">OPOS</span></span>      |                           |
| <span data-ttu-id="30424-752">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-752">Epson</span></span>        | <span data-ttu-id="30424-753">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="30424-753">TM-T88V</span></span>  | <span data-ttu-id="30424-754">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-754">Custom</span></span>    | <span data-ttu-id="30424-755">已通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-755">Connected via netowrk</span></span>     |
| <span data-ttu-id="30424-756">Star</span><span class="sxs-lookup"><span data-stu-id="30424-756">Star</span></span>         | <span data-ttu-id="30424-757">TSP650II</span><span class="sxs-lookup"><span data-stu-id="30424-757">TSP650II</span></span> | <span data-ttu-id="30424-758">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-758">Custom</span></span>    | <span data-ttu-id="30424-759">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-759">Connected via network</span></span>     |
| <span data-ttu-id="30424-760">HP</span><span class="sxs-lookup"><span data-stu-id="30424-760">HP</span></span>           | <span data-ttu-id="30424-761">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="30424-761">F7M67AA</span></span>  | <span data-ttu-id="30424-762">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-762">OPOS</span></span>      | <span data-ttu-id="30424-763">带电 USB</span><span class="sxs-lookup"><span data-stu-id="30424-763">Powered USB</span></span>               |

#### <a name="bar-code-scanner"></a><span data-ttu-id="30424-764">条码扫描仪</span><span class="sxs-lookup"><span data-stu-id="30424-764">Bar code scanner</span></span>

| <span data-ttu-id="30424-765">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-765">Manufacturer</span></span>  | <span data-ttu-id="30424-766">型号</span><span class="sxs-lookup"><span data-stu-id="30424-766">Model</span></span>   | <span data-ttu-id="30424-767">接口</span><span class="sxs-lookup"><span data-stu-id="30424-767">Interface</span></span> | <span data-ttu-id="30424-768">评论</span><span class="sxs-lookup"><span data-stu-id="30424-768">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="30424-769">Motorola</span><span class="sxs-lookup"><span data-stu-id="30424-769">Motorola</span></span>      | <span data-ttu-id="30424-770">DS9208</span><span class="sxs-lookup"><span data-stu-id="30424-770">DS9208</span></span>  | <span data-ttu-id="30424-771">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-771">OPOS</span></span>      |          |
| <span data-ttu-id="30424-772">符号</span><span class="sxs-lookup"><span data-stu-id="30424-772">Symbol</span></span>        | <span data-ttu-id="30424-773">LS2208</span><span class="sxs-lookup"><span data-stu-id="30424-773">LS2208</span></span>  | <span data-ttu-id="30424-774">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-774">OPOS</span></span>      |          |
| <span data-ttu-id="30424-775">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="30424-775">HP Integrated</span></span> | <span data-ttu-id="30424-776">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="30424-776">E1L07AA</span></span> | <span data-ttu-id="30424-777">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-777">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="30424-778">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="30424-778">PIN pad</span></span>

| <span data-ttu-id="30424-779">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-779">Manufacturer</span></span> | <span data-ttu-id="30424-780">型号</span><span class="sxs-lookup"><span data-stu-id="30424-780">Model</span></span>  | <span data-ttu-id="30424-781">接口</span><span class="sxs-lookup"><span data-stu-id="30424-781">Interface</span></span> | <span data-ttu-id="30424-782">评论</span><span class="sxs-lookup"><span data-stu-id="30424-782">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="30424-783">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-783">VeriFone</span></span>     | <span data-ttu-id="30424-784">1000SE</span><span class="sxs-lookup"><span data-stu-id="30424-784">1000SE</span></span> | <span data-ttu-id="30424-785">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-785">OPOS</span></span>      | <span data-ttu-id="30424-786">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="30424-786">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="30424-787">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-787">Payment terminal</span></span>

| <span data-ttu-id="30424-788">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-788">Manufacturer</span></span> | <span data-ttu-id="30424-789">型号</span><span class="sxs-lookup"><span data-stu-id="30424-789">Model</span></span> | <span data-ttu-id="30424-790">接口</span><span class="sxs-lookup"><span data-stu-id="30424-790">Interface</span></span> | <span data-ttu-id="30424-791">评论</span><span class="sxs-lookup"><span data-stu-id="30424-791">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="30424-792">Equinox</span><span class="sxs-lookup"><span data-stu-id="30424-792">Equinox</span></span>      | <span data-ttu-id="30424-793">L5300</span><span class="sxs-lookup"><span data-stu-id="30424-793">L5300</span></span> | <span data-ttu-id="30424-794">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-794">Custom</span></span>    | <span data-ttu-id="30424-795">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="30424-795">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="30424-796">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-796">VeriFone</span></span>     | <span data-ttu-id="30424-797">MX925</span><span class="sxs-lookup"><span data-stu-id="30424-797">MX925</span></span> | <span data-ttu-id="30424-798">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-798">Custom</span></span>    | <span data-ttu-id="30424-799">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="30424-799">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="30424-800">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-800">VeriFone</span></span>     | <span data-ttu-id="30424-801">MX915</span><span class="sxs-lookup"><span data-stu-id="30424-801">MX915</span></span> | <span data-ttu-id="30424-802">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-802">Custom</span></span>    | <span data-ttu-id="30424-803">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="30424-803">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="30424-804">银箱</span><span class="sxs-lookup"><span data-stu-id="30424-804">Cash drawer</span></span>

| <span data-ttu-id="30424-805">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-805">Manufacturer</span></span> | <span data-ttu-id="30424-806">型号</span><span class="sxs-lookup"><span data-stu-id="30424-806">Model</span></span>     | <span data-ttu-id="30424-807">接口</span><span class="sxs-lookup"><span data-stu-id="30424-807">Interface</span></span> | <span data-ttu-id="30424-808">评论</span><span class="sxs-lookup"><span data-stu-id="30424-808">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="30424-809">APG</span><span class="sxs-lookup"><span data-stu-id="30424-809">APG</span></span>          | <span data-ttu-id="30424-810">Atwood</span><span class="sxs-lookup"><span data-stu-id="30424-810">Atwood</span></span>    | <span data-ttu-id="30424-811">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-811">Custom</span></span>    | <span data-ttu-id="30424-812">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-812">Connected via network</span></span> |
| <span data-ttu-id="30424-813">Star</span><span class="sxs-lookup"><span data-stu-id="30424-813">Star</span></span>         | <span data-ttu-id="30424-814">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="30424-814">SMD2-1317</span></span> | <span data-ttu-id="30424-815">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-815">OPOS</span></span>      |                       |
| <span data-ttu-id="30424-816">HP</span><span class="sxs-lookup"><span data-stu-id="30424-816">HP</span></span>           | <span data-ttu-id="30424-817">QT457AA</span><span class="sxs-lookup"><span data-stu-id="30424-817">QT457AA</span></span>   | <span data-ttu-id="30424-818">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-818">OPOS</span></span>      |                       |
| <span data-ttu-id="30424-819">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-819">Epson</span></span>        |           | <span data-ttu-id="30424-820">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-820">Custom</span></span>    | <span data-ttu-id="30424-821">已通过 DK 端口连接到网络 Epson 打印机</span><span class="sxs-lookup"><span data-stu-id="30424-821">Connected to network Epson printer via DK port</span></span> |

#### <a name="line-display"></a><span data-ttu-id="30424-822">行显示</span><span class="sxs-lookup"><span data-stu-id="30424-822">Line display</span></span>

| <span data-ttu-id="30424-823">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-823">Manufacturer</span></span>  | <span data-ttu-id="30424-824">型号</span><span class="sxs-lookup"><span data-stu-id="30424-824">Model</span></span>   | <span data-ttu-id="30424-825">接口</span><span class="sxs-lookup"><span data-stu-id="30424-825">Interface</span></span> | <span data-ttu-id="30424-826">注释</span><span class="sxs-lookup"><span data-stu-id="30424-826">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="30424-827">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="30424-827">HP integrated</span></span> | <span data-ttu-id="30424-828">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="30424-828">G6U79AA</span></span> | <span data-ttu-id="30424-829">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-829">OPOS</span></span>      |          |
| <span data-ttu-id="30424-830">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-830">Epson</span></span>         | <span data-ttu-id="30424-831">M58DC</span><span class="sxs-lookup"><span data-stu-id="30424-831">M58DC</span></span>   | <span data-ttu-id="30424-832">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-832">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="30424-833">签名捕获</span><span class="sxs-lookup"><span data-stu-id="30424-833">Signature capture</span></span>

| <span data-ttu-id="30424-834">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-834">Manufacturer</span></span> | <span data-ttu-id="30424-835">型号</span><span class="sxs-lookup"><span data-stu-id="30424-835">Model</span></span>  | <span data-ttu-id="30424-836">接口</span><span class="sxs-lookup"><span data-stu-id="30424-836">Interface</span></span> | <span data-ttu-id="30424-837">评论</span><span class="sxs-lookup"><span data-stu-id="30424-837">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="30424-838">Scriptel</span><span class="sxs-lookup"><span data-stu-id="30424-838">Scriptel</span></span>     | <span data-ttu-id="30424-839">ST1550</span><span class="sxs-lookup"><span data-stu-id="30424-839">ST1550</span></span> | <span data-ttu-id="30424-840">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-840">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="30424-841">比例</span><span class="sxs-lookup"><span data-stu-id="30424-841">Scale</span></span>

| <span data-ttu-id="30424-842">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-842">Manufacturer</span></span> | <span data-ttu-id="30424-843">型号</span><span class="sxs-lookup"><span data-stu-id="30424-843">Model</span></span>         | <span data-ttu-id="30424-844">接口</span><span class="sxs-lookup"><span data-stu-id="30424-844">Interface</span></span> | <span data-ttu-id="30424-845">评论</span><span class="sxs-lookup"><span data-stu-id="30424-845">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="30424-846">Datalogic</span><span class="sxs-lookup"><span data-stu-id="30424-846">Datalogic</span></span>    | <span data-ttu-id="30424-847">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="30424-847">Magellan 8400</span></span> | <span data-ttu-id="30424-848">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-848">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="30424-849">MSR</span><span class="sxs-lookup"><span data-stu-id="30424-849">MSR</span></span>

| <span data-ttu-id="30424-850">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-850">Manufacturer</span></span> | <span data-ttu-id="30424-851">型号</span><span class="sxs-lookup"><span data-stu-id="30424-851">Model</span></span>       | <span data-ttu-id="30424-852">接口</span><span class="sxs-lookup"><span data-stu-id="30424-852">Interface</span></span> | <span data-ttu-id="30424-853">评论</span><span class="sxs-lookup"><span data-stu-id="30424-853">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="30424-854">Magtek</span><span class="sxs-lookup"><span data-stu-id="30424-854">Magtek</span></span>       | <span data-ttu-id="30424-855">21073075</span><span class="sxs-lookup"><span data-stu-id="30424-855">21073075</span></span>    | <span data-ttu-id="30424-856">UWP</span><span class="sxs-lookup"><span data-stu-id="30424-856">UWP</span></span>       |          |
| <span data-ttu-id="30424-857">Magtek</span><span class="sxs-lookup"><span data-stu-id="30424-857">Magtek</span></span>       | <span data-ttu-id="30424-858">21073062</span><span class="sxs-lookup"><span data-stu-id="30424-858">21073062</span></span>    | <span data-ttu-id="30424-859">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-859">OPOS</span></span>      |          |
| <span data-ttu-id="30424-860">HP</span><span class="sxs-lookup"><span data-stu-id="30424-860">HP</span></span>           | <span data-ttu-id="30424-861">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="30424-861">IDRA-334133</span></span> | <span data-ttu-id="30424-862">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-862">OPOS</span></span>      |          |

### <a name="shared-iis-hardware-station"></a><span data-ttu-id="30424-863">共享 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="30424-863">Shared IIS hardware station</span></span>

<span data-ttu-id="30424-864">已使用共享 IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="30424-864">The following peripherals were tested by using a shared IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span> 

> [!NOTE]
> <span data-ttu-id="30424-865">仅支持打印机、付款终端和银箱。</span><span class="sxs-lookup"><span data-stu-id="30424-865">Only a printer, payment terminal, and cash drawer are supported.</span></span>

#### <a name="printer"></a><span data-ttu-id="30424-866">打印机</span><span class="sxs-lookup"><span data-stu-id="30424-866">Printer</span></span>

| <span data-ttu-id="30424-867">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-867">Manufacturer</span></span> | <span data-ttu-id="30424-868">型号</span><span class="sxs-lookup"><span data-stu-id="30424-868">Model</span></span>    | <span data-ttu-id="30424-869">接口</span><span class="sxs-lookup"><span data-stu-id="30424-869">Interface</span></span> | <span data-ttu-id="30424-870">注释</span><span class="sxs-lookup"><span data-stu-id="30424-870">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="30424-871">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-871">Epson</span></span>        | <span data-ttu-id="30424-872">TM-T88IV</span><span class="sxs-lookup"><span data-stu-id="30424-872">TM-T88IV</span></span> | <span data-ttu-id="30424-873">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-873">OPOS</span></span>      |                           |
| <span data-ttu-id="30424-874">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-874">Epson</span></span>        | <span data-ttu-id="30424-875">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="30424-875">TM-T88V</span></span>  | <span data-ttu-id="30424-876">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-876">OPOS</span></span>      |                           |
| <span data-ttu-id="30424-877">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-877">Epson</span></span>        | <span data-ttu-id="30424-878">TM-T88</span><span class="sxs-lookup"><span data-stu-id="30424-878">TM-T88</span></span>   | <span data-ttu-id="30424-879">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-879">Custom</span></span>    | <span data-ttu-id="30424-880">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-880">Connected via network</span></span>     |
| <span data-ttu-id="30424-881">Star</span><span class="sxs-lookup"><span data-stu-id="30424-881">Star</span></span>         | <span data-ttu-id="30424-882">TSP650II</span><span class="sxs-lookup"><span data-stu-id="30424-882">TSP650II</span></span> | <span data-ttu-id="30424-883">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-883">Custom</span></span>    | <span data-ttu-id="30424-884">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-884">Connected via network</span></span>     |
| <span data-ttu-id="30424-885">HP</span><span class="sxs-lookup"><span data-stu-id="30424-885">HP</span></span>           | <span data-ttu-id="30424-886">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="30424-886">F7M67AA</span></span>  | <span data-ttu-id="30424-887">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-887">OPOS</span></span>      | <span data-ttu-id="30424-888">带电 USB</span><span class="sxs-lookup"><span data-stu-id="30424-888">Powered USB</span></span>               |

#### <a name="payment-terminal"></a><span data-ttu-id="30424-889">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-889">Payment terminal</span></span>

| <span data-ttu-id="30424-890">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-890">Manufacturer</span></span> | <span data-ttu-id="30424-891">型号</span><span class="sxs-lookup"><span data-stu-id="30424-891">Model</span></span> | <span data-ttu-id="30424-892">接口</span><span class="sxs-lookup"><span data-stu-id="30424-892">Interface</span></span> | <span data-ttu-id="30424-893">评论</span><span class="sxs-lookup"><span data-stu-id="30424-893">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="30424-894">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-894">VeriFone</span></span>     | <span data-ttu-id="30424-895">MX925</span><span class="sxs-lookup"><span data-stu-id="30424-895">MX925</span></span> | <span data-ttu-id="30424-896">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-896">Custom</span></span>    | <span data-ttu-id="30424-897">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="30424-897">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="30424-898">VeriFone</span><span class="sxs-lookup"><span data-stu-id="30424-898">VeriFone</span></span>     | <span data-ttu-id="30424-899">MX915</span><span class="sxs-lookup"><span data-stu-id="30424-899">MX915</span></span> | <span data-ttu-id="30424-900">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-900">Custom</span></span>    | <span data-ttu-id="30424-901">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="30424-901">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="30424-902">银箱</span><span class="sxs-lookup"><span data-stu-id="30424-902">Cash drawer</span></span>

| <span data-ttu-id="30424-903">制造商</span><span class="sxs-lookup"><span data-stu-id="30424-903">Manufacturer</span></span> | <span data-ttu-id="30424-904">型号</span><span class="sxs-lookup"><span data-stu-id="30424-904">Model</span></span>     | <span data-ttu-id="30424-905">接口</span><span class="sxs-lookup"><span data-stu-id="30424-905">Interface</span></span> | <span data-ttu-id="30424-906">评论</span><span class="sxs-lookup"><span data-stu-id="30424-906">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="30424-907">APG</span><span class="sxs-lookup"><span data-stu-id="30424-907">APG</span></span>          | <span data-ttu-id="30424-908">Atwood</span><span class="sxs-lookup"><span data-stu-id="30424-908">Atwood</span></span>    | <span data-ttu-id="30424-909">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-909">Custom</span></span>    | <span data-ttu-id="30424-910">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="30424-910">Connected via network</span></span> |
| <span data-ttu-id="30424-911">Star</span><span class="sxs-lookup"><span data-stu-id="30424-911">Star</span></span>         | <span data-ttu-id="30424-912">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="30424-912">SMD2-1317</span></span> | <span data-ttu-id="30424-913">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-913">OPOS</span></span>      |                       |
| <span data-ttu-id="30424-914">HP</span><span class="sxs-lookup"><span data-stu-id="30424-914">HP</span></span>           | <span data-ttu-id="30424-915">QT457AA</span><span class="sxs-lookup"><span data-stu-id="30424-915">QT457AA</span></span>   | <span data-ttu-id="30424-916">OPOS</span><span class="sxs-lookup"><span data-stu-id="30424-916">OPOS</span></span>      |                       |
| <span data-ttu-id="30424-917">Epson</span><span class="sxs-lookup"><span data-stu-id="30424-917">Epson</span></span>        |           | <span data-ttu-id="30424-918">自定义</span><span class="sxs-lookup"><span data-stu-id="30424-918">Custom</span></span>    | <span data-ttu-id="30424-919">已通过 DK 端口连接到网络 Epson 打印机</span><span class="sxs-lookup"><span data-stu-id="30424-919">Connected to network Epson printer via DK port</span></span> |


## <a name="troubleshooting"></a><span data-ttu-id="30424-920">疑难解答</span><span class="sxs-lookup"><span data-stu-id="30424-920">Troubleshooting</span></span>
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="30424-921">Modern POS 可以在其列表中检测硬件工作站以进行选择，但是不能完成配对</span><span class="sxs-lookup"><span data-stu-id="30424-921">Modern POS can detect the hardware station in its list for selection, but it can’t complete the pairing</span></span>

<span data-ttu-id="30424-922">**解决方案：** 验证以下潜在故障点列表：</span><span class="sxs-lookup"><span data-stu-id="30424-922">**Solution:** Verify the following list of potential failure points:</span></span>

-   <span data-ttu-id="30424-923">运行 Modern POS 的计算机信任运行硬件工作站的计算机上使用的证书。</span><span class="sxs-lookup"><span data-stu-id="30424-923">The computer that is running Modern POS trusts the certificate that is used on the computer that runs the hardware station.</span></span>
    -   <span data-ttu-id="30424-924">若要验证此设置，请在 Web 浏览器中转至以下 URL：https://&lt;计算机名称&gt;:&lt;端口号&gt;/HardwareStation/ping。</span><span class="sxs-lookup"><span data-stu-id="30424-924">To verify this setup, in a web browser, go to the following URL: https://&lt;Computer Name&gt;:&lt;Port Number&gt;/HardwareStation/ping.</span></span>
    -   <span data-ttu-id="30424-925">此 URL 使用 ping 验证计算机是否可访问，而浏览器则指示证书是否可信。</span><span class="sxs-lookup"><span data-stu-id="30424-925">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="30424-926">（例如，在 Internet Explorer 中，地址栏中显示锁图标。</span><span class="sxs-lookup"><span data-stu-id="30424-926">(For example, in Internet Explorer, a lock icon appears in the address bar.</span></span> <span data-ttu-id="30424-927">当您单击此图标时，Internet Explorer 验证证书当前是否可信。</span><span class="sxs-lookup"><span data-stu-id="30424-927">When you click this icon, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="30424-928">您可以通过查看显示的证书的详细信息，将证书安装到本地计算机上。）</span><span class="sxs-lookup"><span data-stu-id="30424-928">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>
-   <span data-ttu-id="30424-929">在运行硬件工作站的计算机上，防火墙中将打开硬件工作站使用的端口。</span><span class="sxs-lookup"><span data-stu-id="30424-929">On the computer that runs the hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
-   <span data-ttu-id="30424-930">硬件工作站已通过硬件工作站安装程序结束时运行的安装商家信息工具正确安装了商家帐户信息。</span><span class="sxs-lookup"><span data-stu-id="30424-930">The hardware station has correctly installed merchant account information through the Install merchant information tool that runs at the end of the hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="30424-931">Modern POS 不能在其列表中检测到硬件工作站来进行选择</span><span class="sxs-lookup"><span data-stu-id="30424-931">Modern POS can’t detect the hardware station in its list for selection</span></span>

<span data-ttu-id="30424-932">**解决方案：** 以下因素之一可能导致此问题：</span><span class="sxs-lookup"><span data-stu-id="30424-932">**Solution:** Either of the following factors can cause this issue:</span></span>

-   <span data-ttu-id="30424-933">硬件工作站尚未在总部正确设置。</span><span class="sxs-lookup"><span data-stu-id="30424-933">The hardware station hasn’t been set up correctly in headquarters.</span></span> <span data-ttu-id="30424-934">使用本主题前面的步骤验证是否正确输入了硬件工作站配置文件和硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="30424-934">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
-   <span data-ttu-id="30424-935">尚未运行作业以更新渠道配置。</span><span class="sxs-lookup"><span data-stu-id="30424-935">The jobs haven’t been run to update the channel configuration.</span></span> <span data-ttu-id="30424-936">在这种情况下，请运行作业 1070 以配置渠道。</span><span class="sxs-lookup"><span data-stu-id="30424-936">In this case, run the 1070 job for channel configuration.</span></span>

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a><span data-ttu-id="30424-937">Modern POS 不体现新的银箱设置</span><span class="sxs-lookup"><span data-stu-id="30424-937">Modern POS doesn't reflect new cash drawer settings</span></span>

<span data-ttu-id="30424-938">**解决方案：** 关闭当前批处理。</span><span class="sxs-lookup"><span data-stu-id="30424-938">**Solution:** Close the current batch.</span></span> <span data-ttu-id="30424-939">关闭当前批处理之前，不会将对银箱的更改更新到 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="30424-939">Changes to the cash drawer aren't updated to Modern POS until the current batch is closed.</span></span>

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a><span data-ttu-id="30424-940">Modern POS 报告外设有问题</span><span class="sxs-lookup"><span data-stu-id="30424-940">Modern POS is reporting an issue with a peripheral</span></span>

<span data-ttu-id="30424-941">**解决方案：** 下面是此问题的一些典型原因：</span><span class="sxs-lookup"><span data-stu-id="30424-941">**Solution:** Here are some typical causes of this issue:</span></span>

-   <span data-ttu-id="30424-942">确保关闭了其他设备驱动程序配置实用程序。</span><span class="sxs-lookup"><span data-stu-id="30424-942">Make sure that other device driver configuration utilities are closed.</span></span> <span data-ttu-id="30424-943">如果打开了这些实用程序，可能会阻止 Modern POS 或硬件工作站声明设备。</span><span class="sxs-lookup"><span data-stu-id="30424-943">If these utilities are open, they might prevent Modern POS or the hardware station from claiming the device.</span></span>
-   <span data-ttu-id="30424-944">如果将外设与多台 POS 设备共享，请确保其属于以下类别之一：</span><span class="sxs-lookup"><span data-stu-id="30424-944">If the peripheral is shared with multiple POS devices, make sure that it belongs to one of the following categories:</span></span>
    -   <span data-ttu-id="30424-945">银箱</span><span class="sxs-lookup"><span data-stu-id="30424-945">Cash drawer</span></span>
    -   <span data-ttu-id="30424-946">收据打印机</span><span class="sxs-lookup"><span data-stu-id="30424-946">Receipt printer</span></span>
    -   <span data-ttu-id="30424-947">付款终端</span><span class="sxs-lookup"><span data-stu-id="30424-947">Payment terminal</span></span>

    <span data-ttu-id="30424-948">如果外设不属于这些类别之一，则硬件工作站的设计不支持在多台 POS 设备之间共享该外设。</span><span class="sxs-lookup"><span data-stu-id="30424-948">If the peripheral doesn't belong to one of these categories, the hardware station isn't designed to enable the peripheral to be shared among multiple POS devices.</span></span>
-   <span data-ttu-id="30424-949">有时，设备驱动程序可能导致公共控件对象 (CCO) 停止正常工作。</span><span class="sxs-lookup"><span data-stu-id="30424-949">Sometimes, device drivers can cause the common control objects (CCOs) to stop working correctly.</span></span> <span data-ttu-id="30424-950">如果最近安装了设备，但是该设备无法正常工作，或您发现了其他问题，通常可以通过重新安装 CCO 来解决问题。</span><span class="sxs-lookup"><span data-stu-id="30424-950">If a device has recently been installed, but it isn't working properly or you notice other issues, you can often resolve the issue by reinstalling the CCOs.</span></span> <span data-ttu-id="30424-951">若要下载 CCO，请访问 <http://monroecs.com/oposccos_current.htm>。</span><span class="sxs-lookup"><span data-stu-id="30424-951">To download the CCOs, visit <http://monroecs.com/oposccos_current.htm>.</span></span>
-   <span data-ttu-id="30424-952">如果在测试或故障排除期间频繁更改外设，可能必须重置 IIS，而不是等待高速缓存自行刷新。</span><span class="sxs-lookup"><span data-stu-id="30424-952">If you make frequent peripheral changes during testing or troubleshooting, you might have to reset IIS instead of waiting for the cache to refresh itself.</span></span> <span data-ttu-id="30424-953">若要重置 IIS，请执行以下步骤:</span><span class="sxs-lookup"><span data-stu-id="30424-953">To reset IIS, follow these steps:</span></span>
    1.  <span data-ttu-id="30424-954">在 **开始** 菜单中键入 **CMD**。</span><span class="sxs-lookup"><span data-stu-id="30424-954">From the **Start** menu, type **CMD**.</span></span>
    2.  <span data-ttu-id="30424-955">在搜索结果中，右键单击 **命令提示符**，然后单击 **以管理员身份运行**。</span><span class="sxs-lookup"><span data-stu-id="30424-955">In the search results, right-click **Command prompt**, and then click **Run as administrator**.</span></span>
    3.  <span data-ttu-id="30424-956">在 **命令提示符** 窗口中，键入 **iisreset /Restart**，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="30424-956">In the **Command prompt** window, type **iisreset /Restart** and then press Enter.</span></span>
    4.  <span data-ttu-id="30424-957">IIS 重新启动后，重新启动 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="30424-957">After IIS has restarted, restart Modern POS.</span></span>
-   <span data-ttu-id="30424-958">频繁更改外设时，如果也频繁启动和退出 POS 客户端，则上一个 POS 会话的 dllhost 进程可能干扰当前会话。</span><span class="sxs-lookup"><span data-stu-id="30424-958">While you're making frequent changes to peripheral devices, if you also frequently start and exit the POS client, the dllhost process from a previous POS session can interfere with the current session.</span></span> <span data-ttu-id="30424-959">在这种情况下，关闭正在管理上一个会话的动态链接库 (DLL) 主机之前，设备可能不可用。</span><span class="sxs-lookup"><span data-stu-id="30424-959">In this case, a device might not be usable until you close the dynamic-link library (DLL) host that is managing the previous session.</span></span> <span data-ttu-id="30424-960">若要关闭 DLL 主机，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="30424-960">To close the DLL host, follow these steps:</span></span>
    1.  <span data-ttu-id="30424-961">在 **开始** 菜单中键入 **任务管理器**。</span><span class="sxs-lookup"><span data-stu-id="30424-961">From the **Start** menu, type **Task manager**.</span></span>
    2.  <span data-ttu-id="30424-962">在搜索结果中，单击 **任务管理器**。</span><span class="sxs-lookup"><span data-stu-id="30424-962">In the search results, click **Task manager**.</span></span>
    3.  <span data-ttu-id="30424-963">在“任务管理器”中的 **详细信息** 选项卡上，单击带有 **名称** 标签的列标题，按名称以字母顺序为表排序。</span><span class="sxs-lookup"><span data-stu-id="30424-963">In Task manager, on the **Details** tab, click the column header that is labeled **Name** to sort the table alphabetically by name.</span></span>
    4.  <span data-ttu-id="30424-964">向下滚动，直到找到 dllhost.exe。</span><span class="sxs-lookup"><span data-stu-id="30424-964">Scroll down until you find dllhost.exe.</span></span>
    5.  <span data-ttu-id="30424-965">选择每个 DLL 主机，然后单击 **结束任何**。</span><span class="sxs-lookup"><span data-stu-id="30424-965">Select each DLL host, and then click **End task**.</span></span>
    6.  <span data-ttu-id="30424-966">关闭 DLL 主机后，重新启动 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="30424-966">After the DLL hosts have been closed, restart Modern POS.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="30424-967">其他资源</span><span class="sxs-lookup"><span data-stu-id="30424-967">Additional resources</span></span>

[<span data-ttu-id="30424-968">Commerce 的外设模拟器</span><span class="sxs-lookup"><span data-stu-id="30424-968">Peripheral simulator for Commerce</span></span>](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]