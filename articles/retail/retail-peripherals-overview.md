---
title: "零售外设"
description: "此主题介绍与零售外设有关的概念。"
author: rubencdelgado
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c2539af8a29b580a10002bc8648505d42c7b8456
ms.contentlocale: zh-cn
ms.lasthandoff: 01/04/2019

---

# <a name="retail-peripherals"></a><span data-ttu-id="b4553-103">零售外设</span><span class="sxs-lookup"><span data-stu-id="b4553-103">Retail peripherals</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4553-104">此主题介绍与零售外设有关的概念。</span><span class="sxs-lookup"><span data-stu-id="b4553-104">This topic explains the concepts that are related to retail peripherals.</span></span> <span data-ttu-id="b4553-105">它描述可用于将外设连接到销售点 (POS) 的各种方法，以及负责管理与 POS 之间的连接的组件。</span><span class="sxs-lookup"><span data-stu-id="b4553-105">It describes the various ways that peripherals can be connected to the point of sale (POS) and the components that are responsible for managing the connection with the POS.</span></span>

## <a name="concepts"></a><span data-ttu-id="b4553-106">概念</span><span class="sxs-lookup"><span data-stu-id="b4553-106">Concepts</span></span>

### <a name="pos-registers"></a><span data-ttu-id="b4553-107">POS 收银机</span><span class="sxs-lookup"><span data-stu-id="b4553-107">POS registers</span></span>

<span data-ttu-id="b4553-108">导航：单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="b4553-108">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="b4553-109">销售点 (POS) 收银机是用来定义特定 POS 实例的特征的实体。</span><span class="sxs-lookup"><span data-stu-id="b4553-109">The point of sale (POS) register is an entity that is used to define the characteristics of a specific instance of the POS.</span></span> <span data-ttu-id="b4553-110">这些特征包括硬件配置文件或设置，它们将被零售外设用于收银机、收银机映射到的商店，以及登录该收银机的用户的视觉体验。</span><span class="sxs-lookup"><span data-stu-id="b4553-110">These characteristics include the hardware profile or setup for retail peripherals that will be used at the register, the store that the register is mapped to, and the visual experience for the user who signs in to that register.</span></span>

### <a name="devices"></a><span data-ttu-id="b4553-111">设备</span><span class="sxs-lookup"><span data-stu-id="b4553-111">Devices</span></span>

<span data-ttu-id="b4553-112">导航：单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **设备**。</span><span class="sxs-lookup"><span data-stu-id="b4553-112">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**.</span></span> <span data-ttu-id="b4553-113">设备是表示映射到 POS 收银机的设备的物理实例的实体。</span><span class="sxs-lookup"><span data-stu-id="b4553-113">A device is an entity that represents a physical instance of a device that is mapped to a POS register.</span></span> <span data-ttu-id="b4553-114">当创建一个设备时，它被映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="b4553-114">When a device is created, it's mapped to a POS register.</span></span> <span data-ttu-id="b4553-115">设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。</span><span class="sxs-lookup"><span data-stu-id="b4553-115">The device entity tracks information about when a POS register is activated, the type of client that is being used, and the application package that has been deployed to a specific device.</span></span> <span data-ttu-id="b4553-116">设备可以映射到以下应用类型：Retail Modern POS、Retail Cloud POS、Retail Modern POS – Windows Phone、Retail Modern POS – Android 和 Retail Modern POS – iOS。</span><span class="sxs-lookup"><span data-stu-id="b4553-116">Devices can be mapped to the following application types: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android, and Retail Modern POS – iOS.</span></span>

### <a name="retail-modern-pos"></a><span data-ttu-id="b4553-117">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="b4553-117">Retail Modern POS</span></span>

<span data-ttu-id="b4553-118">Modern POS 是适用于 Microsoft Windows 的 POS 程序。</span><span class="sxs-lookup"><span data-stu-id="b4553-118">Modern POS is the POS program for Microsoft Windows.</span></span> <span data-ttu-id="b4553-119">它可以部署到 Windows 10 操作系统 (OS) 上。</span><span class="sxs-lookup"><span data-stu-id="b4553-119">It can be deployed on Windows 10 operating systems (OSs).</span></span>

### <a name="cloud-pos"></a><span data-ttu-id="b4553-120">云 POS</span><span class="sxs-lookup"><span data-stu-id="b4553-120">Cloud POS</span></span>

<span data-ttu-id="b4553-121">Cloud POS 是基于浏览器且可以通过 Web 浏览器访问的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="b4553-121">Cloud POS is a browser-based version of the Modern POS program that can be accessed in a web browser.</span></span>

### <a name="modern-pos-for-ios"></a><span data-ttu-id="b4553-122">Modern POS for iOS</span><span class="sxs-lookup"><span data-stu-id="b4553-122">Modern POS for iOS</span></span>

<span data-ttu-id="b4553-123">Modern POS for iOS 是基于 iOS 且可部署到 iOS 设备上的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="b4553-123">Modern POS for iOS is an iOS-based version of the Modern POS program that can be deployed on iOS devices.</span></span>

### <a name="modern-pos-for-android"></a><span data-ttu-id="b4553-124">Modern POS for Android</span><span class="sxs-lookup"><span data-stu-id="b4553-124">Modern POS for Android</span></span>

<span data-ttu-id="b4553-125">Modern POS for Android 是基于 Android 且可部署到 Android 设备上的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="b4553-125">Modern POS for Android is an Android-based version of the Modern POS program that can be deployed on Android devices.</span></span>

### <a name="pos-peripherals"></a><span data-ttu-id="b4553-126">POS 外设</span><span class="sxs-lookup"><span data-stu-id="b4553-126">POS peripherals</span></span>

<span data-ttu-id="b4553-127">POS 外设是为满足 POS 功能而明确支持的设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-127">POS peripherals are devices that are explicitly supported for POS functions.</span></span> <span data-ttu-id="b4553-128">这些外设通常划分为特定类。</span><span class="sxs-lookup"><span data-stu-id="b4553-128">These peripherals are typically divided into specific classes.</span></span> <span data-ttu-id="b4553-129">有关这些类的详细信息，请参阅此主题的“设备分类”部分。</span><span class="sxs-lookup"><span data-stu-id="b4553-129">For more information about these classes, see the "Device classes" section of this topic.</span></span>

### <a name="hardware-station"></a><span data-ttu-id="b4553-130">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="b4553-130">Hardware station</span></span>

<span data-ttu-id="b4553-131">导航：单击**零售** &gt; **渠道** &gt; **零售商店** &gt; **所有零售商店**。</span><span class="sxs-lookup"><span data-stu-id="b4553-131">Navigation: Click **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span> <span data-ttu-id="b4553-132">选择一个商店，然后单击**硬件工作站**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b4553-132">Select a store, and then click the **Hardware stations** FastTab.</span></span> <span data-ttu-id="b4553-133">**硬件工作站**设置是一种基于渠道的设置，用于定义将部署零售外设逻辑的实例。</span><span class="sxs-lookup"><span data-stu-id="b4553-133">The **Hardware station** setting is a channel-level setting that is used to define instances where the retail peripheral logic will be deployed.</span></span> <span data-ttu-id="b4553-134">渠道级别的此设置用于确定硬件工作站的特征。</span><span class="sxs-lookup"><span data-stu-id="b4553-134">This setting at the channel level is used to determine characteristics of the hardware station.</span></span> <span data-ttu-id="b4553-135">还用于列出指定商店中可用于 Modern POS 实例的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-135">It's also used to list hardware stations that are available for a Modern POS instance in a given store.</span></span> <span data-ttu-id="b4553-136">硬件工作站内置在适用于 Windows 的 Modern POS 程序内。</span><span class="sxs-lookup"><span data-stu-id="b4553-136">The hardware station is built into the Modern POS program for Windows.</span></span> <span data-ttu-id="b4553-137">硬件工作站也可以作为单机 Microsoft Internet Information Services (IIS) 程序独立部署。</span><span class="sxs-lookup"><span data-stu-id="b4553-137">The hardware station can also be deployed independently as a stand-alone Microsoft Internet Information Services (IIS) program.</span></span> <span data-ttu-id="b4553-138">在这种情况下，可以通过网络访问。</span><span class="sxs-lookup"><span data-stu-id="b4553-138">In this case, it can be accessed via a network.</span></span>

### <a name="hardware-profile"></a><span data-ttu-id="b4553-139">硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="b4553-139">Hardware profile</span></span>

<span data-ttu-id="b4553-140">导航︰单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="b4553-140">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="b4553-141">硬件配置文件是为 POS 收银机或硬件工作站配置的设备的列表。</span><span class="sxs-lookup"><span data-stu-id="b4553-141">The hardware profile is a list of devices that are configured for a POS register or a hardware station.</span></span> <span data-ttu-id="b4553-142">硬件配置文件可以直接映射到 POS 收银机或硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-142">The hardware profile can be mapped directly to a POS register or a hardware station.</span></span>

## <a name="devices-classes"></a><span data-ttu-id="b4553-143">设备分类</span><span class="sxs-lookup"><span data-stu-id="b4553-143">Devices classes</span></span>
<span data-ttu-id="b4553-144">POS 外设通常划分为类。</span><span class="sxs-lookup"><span data-stu-id="b4553-144">POS peripherals are typically divided into classes.</span></span> <span data-ttu-id="b4553-145">此部分描述并提供 Modern POS 支持的设备的概览。</span><span class="sxs-lookup"><span data-stu-id="b4553-145">This section describes and gives an overview of the devices that Modern POS supports.</span></span>

### <a name="printer"></a><span data-ttu-id="b4553-146">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-146">Printer</span></span>

<span data-ttu-id="b4553-147">外设包括传统 POS 收据打印机和整页打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-147">Printers include traditional POS receipt printers and full-page printers.</span></span> <span data-ttu-id="b4553-148">通过适用于 Retail POS (OPOS) 和 Microsoft Windows 的对象链路与嵌入驱动程序接口为打印机提供支持。</span><span class="sxs-lookup"><span data-stu-id="b4553-148">Printer are supported through Object Linking and Embedding for Retail POS (OPOS) and Microsoft Windows driver interfaces.</span></span> <span data-ttu-id="b4553-149">最多可以同时使用两台打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-149">Up to two printers can be used at the same time.</span></span> <span data-ttu-id="b4553-150">此功能支持在收据打印机上打印付现自提的客户收据的方案，虽然包含更多信息的客户订单在整页打印机上打印。</span><span class="sxs-lookup"><span data-stu-id="b4553-150">This capability supports scenarios where cash-and-carry customer receipts are printed on receipt printers, whereas customer orders, which carry more information, are printed on a full-page printer.</span></span> <span data-ttu-id="b4553-151">收据打印机可以通过 USB 直接连接到计算机，通过以太网连接到网络，或通过 Bluetooth 连接。</span><span class="sxs-lookup"><span data-stu-id="b4553-151">Receipt printers can be connected directly to a computer via USB, connected to a network via Ethernet, or connected via Bluetooth.</span></span>

### <a name="scanner"></a><span data-ttu-id="b4553-152">扫描仪</span><span class="sxs-lookup"><span data-stu-id="b4553-152">Scanner</span></span>

<span data-ttu-id="b4553-153">最多可以同时使用两台条码扫描仪。</span><span class="sxs-lookup"><span data-stu-id="b4553-153">Up to two bar code scanners can be used at the same time.</span></span> <span data-ttu-id="b4553-154">此功能支持需要移动性更高的扫描仪来扫描体积大或重量高的物品的方案，而嵌入式固定扫描仪则用于大多数标准尺寸的物品或加快收银速度。</span><span class="sxs-lookup"><span data-stu-id="b4553-154">This capability supports scenarios where a scanner that is more mobile is required in order to scan large or heavy items, whereas a fixed embedded scanner is used for most standard-sized items, to speed up checkout times.</span></span> <span data-ttu-id="b4553-155">可以通过 OPOS、通用 Windows 平台 (UWP) 或键盘 wedge 界面为扫描仪提供支持。</span><span class="sxs-lookup"><span data-stu-id="b4553-155">Scanners can be supported through OPOS, Universal Windows Platform (UWP), or keyboard wedge interfaces.</span></span> <span data-ttu-id="b4553-156">可使用 USB 或 Bluetooth 将扫描仪连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-156">USB or Bluetooth can be used to connect a scanner to a computer.</span></span>

### <a name="msr"></a><span data-ttu-id="b4553-157">MSR</span><span class="sxs-lookup"><span data-stu-id="b4553-157">MSR</span></span>

<span data-ttu-id="b4553-158">可通过使用 OPOS 设置一台 USB 磁条阅读器 (MSR)。</span><span class="sxs-lookup"><span data-stu-id="b4553-158">One USB magnetic stripe reader (MSR) can be set up by using OPOS drivers.</span></span> <span data-ttu-id="b4553-159">如果要将单机 MSR 用于电子资金转帐 (EFT) 付款交易，则必须通过付款连接器管理 MSR。.</span><span class="sxs-lookup"><span data-stu-id="b4553-159">If you want to use a stand-alone MSR for electronic funds transfer (EFT) payment transactions, the MSR must be managed by a payment connector.</span></span> <span data-ttu-id="b4553-160">单机 MSR 可用于独立于付款连接器执行客户会员信息录入、员工签到和礼品卡录入。</span><span class="sxs-lookup"><span data-stu-id="b4553-160">Stand-alone MSRs can be used for customer loyalty entry, employee sign-in, and gift card entry, independently of the payment connector.</span></span>

### <a name="cash-drawer"></a><span data-ttu-id="b4553-161">银箱</span><span class="sxs-lookup"><span data-stu-id="b4553-161">Cash drawer</span></span>

<span data-ttu-id="b4553-162">每个硬件配置文件可以支持两个银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-162">Two cash drawers can be supported per hardware profile.</span></span> <span data-ttu-id="b4553-163">此功能允许每台收银机同时被两个班次使用。</span><span class="sxs-lookup"><span data-stu-id="b4553-163">This capability enables two active shifts per register to be available at the same time.</span></span> <span data-ttu-id="b4553-164">为了防止共享班次或一个银箱同时被多个移动 POS 设备使用，每个硬件配置文件仅允许一个银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-164">In the case of a shared shift, or a cash drawer that is used by multiple mobile POS devices at the same time, only one cash drawer is allowed per hardware profile.</span></span> <span data-ttu-id="b4553-165">银箱可以通过 USB 直接连接到计算机，连接到网络，或通过 RJ12 接口连接到收据打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-165">Cash drawers can be connected directly to a computer via USB, connected to a network, or connected to a receipt printer via an RJ12 interface.</span></span> <span data-ttu-id="b4553-166">在某些情况下，还可以通过 Bluetooth 连接银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-166">In some cases, cash drawers can also be connected via Bluetooth.</span></span>

### <a name="line-display"></a><span data-ttu-id="b4553-167">行显示内容</span><span class="sxs-lookup"><span data-stu-id="b4553-167">Line display</span></span>

<span data-ttu-id="b4553-168">行显示器用于在交易期间向客户显示产品、交易余额和其他有用信息。</span><span class="sxs-lookup"><span data-stu-id="b4553-168">Line displays are used to show products, transaction balances, and other useful information to the customer during a transaction.</span></span> <span data-ttu-id="b4553-169">可以使用 OPOS 驱动程序通过 USB 将一台行显示器连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-169">One line display can be connected to the computer via USB by using OPOS drivers.</span></span>

### <a name="signature-capture"></a><span data-ttu-id="b4553-170">签名捕获</span><span class="sxs-lookup"><span data-stu-id="b4553-170">Signature capture</span></span>

<span data-ttu-id="b4553-171">可以使用 OPOS 驱动程序通过 USB 将签名捕获设备直接连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-171">Signature capture devices can be connected directly to a computer via USB by using OPOS drivers.</span></span> <span data-ttu-id="b4553-172">在配置签名捕获时，将提示客户在设备上签名。</span><span class="sxs-lookup"><span data-stu-id="b4553-172">When signature capture is configured, the customer is prompted to sign on the device.</span></span> <span data-ttu-id="b4553-173">提供签名后，它会对收银员显示，待其接受。</span><span class="sxs-lookup"><span data-stu-id="b4553-173">After the signature is provided, it's shown to the cashier for acceptance.</span></span>

### <a name="scale"></a><span data-ttu-id="b4553-174">比例</span><span class="sxs-lookup"><span data-stu-id="b4553-174">Scale</span></span>

<span data-ttu-id="b4553-175">可以使用 OPOS 驱动程序通过 USP 将秤连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-175">Scales can be connected to the computer via USP by using OPOS drivers.</span></span> <span data-ttu-id="b4553-176">标记为“已称重”产品的产品添加到交易记录时，POS 从秤读取重量，将该产品添加到交易记录，然后使用秤提供的数量。</span><span class="sxs-lookup"><span data-stu-id="b4553-176">When a product that is marked as a "Weighed" product is added to a transaction, the POS reads the weight from the scale, adds the product to the transaction, and uses the quantity that the scale provided.</span></span>

### <a name="pin-pad"></a><span data-ttu-id="b4553-177">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="b4553-177">PIN pad</span></span>

<span data-ttu-id="b4553-178">通过 OPOS 为个人标识号 (PIN) 小键盘提供支持，但是必须通过付款连接器管理 PIN 小键盘。</span><span class="sxs-lookup"><span data-stu-id="b4553-178">Personal identification number (PIN) pads are supported through OPOS, but they must be managed via a payment connector.</span></span>

### <a name="secondary-display"></a><span data-ttu-id="b4553-179">辅助显示器</span><span class="sxs-lookup"><span data-stu-id="b4553-179">Secondary display</span></span>

<span data-ttu-id="b4553-180">如果配置了辅助显示器，将使用第二台 Windows 显示器显示基本信息。</span><span class="sxs-lookup"><span data-stu-id="b4553-180">When a secondary display is configured, the number 2 Windows display is used to show basic information.</span></span> <span data-ttu-id="b4553-181">辅助显示器用于为独立软件供应商 (ISV) 扩展提供支持，因为原始辅助显示器不可配置，显示的内容有限。</span><span class="sxs-lookup"><span data-stu-id="b4553-181">The purpose of the secondary display is to support independent software vendor (ISV) extension, because out of the box, the secondary display isn't configurable and shows limited content.</span></span>

### <a name="payment-device"></a><span data-ttu-id="b4553-182">付款设备</span><span class="sxs-lookup"><span data-stu-id="b4553-182">Payment device</span></span>

<span data-ttu-id="b4553-183">对付款设备的支持通过付款连接器实现。</span><span class="sxs-lookup"><span data-stu-id="b4553-183">Payment device support is implemented through the payment connector.</span></span> <span data-ttu-id="b4553-184">付款设备可以执行其他设备类提供的一项或多项功能。</span><span class="sxs-lookup"><span data-stu-id="b4553-184">Payment devices can perform one or many of the functions that other device classes provide.</span></span> <span data-ttu-id="b4553-185">例如，一种付款设备可以充当 MSR/卡阅读器、行显示器、签名捕获设备或 PIN 小键盘。</span><span class="sxs-lookup"><span data-stu-id="b4553-185">For example, a payment device can function as an MSR/card reader, line display, signature capture device, or PIN pad.</span></span> <span data-ttu-id="b4553-186">对付款设备的支持独立于为硬件配置文件中包含的其他设备提供的单机设备支持实现。</span><span class="sxs-lookup"><span data-stu-id="b4553-186">Support for payment devices is implemented independently of the stand-alone device support that is provided for other devices that are included in the hardware profile.</span></span>

## <a name="supported-interfaces"></a><span data-ttu-id="b4553-187">支持的接口</span><span class="sxs-lookup"><span data-stu-id="b4553-187">Supported interfaces</span></span>

### <a name="opos"></a><span data-ttu-id="b4553-188">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-188">OPOS</span></span>

<span data-ttu-id="b4553-189">为了帮助确保最大范围的设备可以与 Microsoft Dynamics 365 for Retail 配合使用，OLE for POS 行业标准成为了 Microsoft Dynamics 365 for Retail 中支持的主要零售外设平台。</span><span class="sxs-lookup"><span data-stu-id="b4553-189">To help guarantee that the largest range of devices can be used with Microsoft Dynamics 365 for Retail, the OLE for POS industry standard is the primary retail peripheral device platform that is supported in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="b4553-190">OLE for POS 标准由美国零售联合会 (NRF) 制订，建立了针对零售外设的行业标准通信协议。</span><span class="sxs-lookup"><span data-stu-id="b4553-190">The OLE for POS standard was produced by the National Retail Federation (NRF), which establishes industry-standard communication protocols for retail peripheral devices.</span></span> <span data-ttu-id="b4553-191">OPOS 是广泛采用的 OLE for POS 标准实施。</span><span class="sxs-lookup"><span data-stu-id="b4553-191">OPOS is a widely adopted implementation of the OLE for POS standard.</span></span> <span data-ttu-id="b4553-192">它开发于 20 世纪 90 年代，之后经过了多次更新。</span><span class="sxs-lookup"><span data-stu-id="b4553-192">It was developed in the mid-1990s and has been updated several times since then.</span></span> <span data-ttu-id="b4553-193">OPOS 提供设备驱动程序架构，以便将 POS 硬件与基于 Windows 的 POS 系统轻松集成。</span><span class="sxs-lookup"><span data-stu-id="b4553-193">OPOS provides a device driver architecture that enables easy integration of POS hardware with Windows–based POS systems.</span></span> <span data-ttu-id="b4553-194">OPOS 控件处理兼容硬件与 POS 软件之间的通信。</span><span class="sxs-lookup"><span data-stu-id="b4553-194">OPOS controls handle communication between compatible hardware and the POS software.</span></span> <span data-ttu-id="b4553-195">OPOS 控件包含两部分：</span><span class="sxs-lookup"><span data-stu-id="b4553-195">An OPOS control consists of two parts:</span></span>

- <span data-ttu-id="b4553-196">**控件对象** – 设备类（如行显示器）的控件对象提供软件程序的界面。</span><span class="sxs-lookup"><span data-stu-id="b4553-196">**Control object** – The control object for a device class (such as line displays) provides the interface for the software program.</span></span> <span data-ttu-id="b4553-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) 提供一组标准的 OPOS 控件对象，称为公共控件对象 (CCO)。</span><span class="sxs-lookup"><span data-stu-id="b4553-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) provides a standardized set of OPOS control objects that are known as the common control objects (CCOs).</span></span> <span data-ttu-id="b4553-198">CCO 用于测试 Microsoft Dynamics 365 for Retail 的 POS 组件。</span><span class="sxs-lookup"><span data-stu-id="b4553-198">The CCOs are used to test the POS component of Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="b4553-199">因此，如果 Microsoft Dynamics 365 for Retail 通过 OPOS 为设备类提供支持，并且制造商提供为 OPOS 构建的服务对象，此项测试有助于确保可以支持多种设备类型。</span><span class="sxs-lookup"><span data-stu-id="b4553-199">Therefore, the testing helps guarantee that, if Microsoft Dynamics 365 for Retail supports a device class through OPOS, many device types can be supported, provided that the manufacturer provides a service object that is built for OPOS.</span></span> <span data-ttu-id="b4553-200">无需明确测试每个设备类型。</span><span class="sxs-lookup"><span data-stu-id="b4553-200">You don't have to explicitly test each device type.</span></span>
- <span data-ttu-id="b4553-201">**服务对象** – 服务对象提供控件对象 (CCO) 与设备之间的通信。</span><span class="sxs-lookup"><span data-stu-id="b4553-201">**Service object** – The service object provides communication between the control object (CCO) and the device.</span></span> <span data-ttu-id="b4553-202">设备的服务对象通常由设备制造商提供。</span><span class="sxs-lookup"><span data-stu-id="b4553-202">Typically, the service object for a device is provided by the device manufacturer.</span></span> <span data-ttu-id="b4553-203">但是在某些情况下，您可能必须从制造商的网站下载服务对象。</span><span class="sxs-lookup"><span data-stu-id="b4553-203">However, in some cases, you might have to download the service object from the manufacturer's website.</span></span> <span data-ttu-id="b4553-204">例如，可能提供了更新的服务对象。</span><span class="sxs-lookup"><span data-stu-id="b4553-204">For example, a more recent service object might be available.</span></span> <span data-ttu-id="b4553-205">若要查找制造商的网站地址，请参阅您的硬件文档。</span><span class="sxs-lookup"><span data-stu-id="b4553-205">To find the address of the manufacturer's website, see your hardware documentation.</span></span>

<span data-ttu-id="b4553-206">[![控件对象和服务对象](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)</span><span class="sxs-lookup"><span data-stu-id="b4553-206">[![Control object and service object](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)</span></span>

<span data-ttu-id="b4553-207">对 OLE for POS 的 OPOS 实施的支持有助于确保当设备制造商和 POS 发布商正确实施标准时，POS 系统和支持的设备可以协同工作，即使以前未一起测试时也不例外。</span><span class="sxs-lookup"><span data-stu-id="b4553-207">Support for the OPOS implementation of OLE for POS helps guarantee that, if the device manufacturers and POS publishers implement the standard correctly, POS systems and supported devices can work together, even if they weren't previously tested together.</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-208">支持 OPOS 不保证支持采用了 OPOS 驱动设备的所有设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-208">OPOS support doesn't guarantee support for all devices that have OPOS drivers.</span></span> <span data-ttu-id="b4553-209">Microsoft Dynamics 365 for Retail 必须首先通过 OPOS 支持该设备类型（即类）。</span><span class="sxs-lookup"><span data-stu-id="b4553-209">Microsoft Dynamics 365 for Retail must first support that device type, or class, through OPOS.</span></span> <span data-ttu-id="b4553-210">此外，服务对象可能并非始终安装了最新版本的 CCO。</span><span class="sxs-lookup"><span data-stu-id="b4553-210">In addition, service objects might not always be up to date with the latest version of the CCOs.</span></span> <span data-ttu-id="b4553-211">您还应注意，服务对象的质量往往参差不齐。</span><span class="sxs-lookup"><span data-stu-id="b4553-211">You should also be aware that, in general, the quality of service objects varies.</span></span>

### <a name="windows"></a><span data-ttu-id="b4553-212">窗口</span><span class="sxs-lookup"><span data-stu-id="b4553-212">Windows</span></span>

<span data-ttu-id="b4553-213">POS 的收据打印已针对 OPOS 进行了优化。</span><span class="sxs-lookup"><span data-stu-id="b4553-213">Receipt printing at the POS is optimized for OPOS.</span></span> <span data-ttu-id="b4553-214">OPOS 往往比通过 Windows 打印快得多。</span><span class="sxs-lookup"><span data-stu-id="b4553-214">OPOS tends to be much faster than printing through Windows.</span></span> <span data-ttu-id="b4553-215">因此，最好使用 OPOS 进行打印，特别是在零售环境中，此类环境中需要打印 40 列收据，并且交易时间必须非常快。</span><span class="sxs-lookup"><span data-stu-id="b4553-215">Therefore, it's a good idea to use OPOS, especially in retail environments where 40-column receipts are printed and transaction times must be fast.</span></span> <span data-ttu-id="b4553-216">对于大多数设备，您将使用 OPOS 控件。</span><span class="sxs-lookup"><span data-stu-id="b4553-216">For most devices, you will use OPOS controls.</span></span> <span data-ttu-id="b4553-217">但是，某些 OPOS 收据打印机也支持 Windows 驱动程序。</span><span class="sxs-lookup"><span data-stu-id="b4553-217">However, some OPOS receipt printers also support Windows drivers.</span></span> <span data-ttu-id="b4553-218">通过使用 Windows 驱动程序，您可以通过一台打印机访问多台收银机的最新字体和网络。</span><span class="sxs-lookup"><span data-stu-id="b4553-218">By using a Windows driver, you can access the latest fonts and network one printer for multiple registers.</span></span> <span data-ttu-id="b4553-219">但是使用 Windows 驱动程序有一些缺点。</span><span class="sxs-lookup"><span data-stu-id="b4553-219">However, there are drawbacks to using Windows drivers.</span></span> <span data-ttu-id="b4553-220">以下是这些缺点的一些示例：</span><span class="sxs-lookup"><span data-stu-id="b4553-220">Here are some examples of these drawbacks:</span></span>

- <span data-ttu-id="b4553-221">使用 Windows 驱动程序时，图像在打印前渲染。</span><span class="sxs-lookup"><span data-stu-id="b4553-221">When Windows drivers are used, images are rendered before printing occurs.</span></span> <span data-ttu-id="b4553-222">因此，打印速度往往比使用 OPOS 控件的打印机慢。</span><span class="sxs-lookup"><span data-stu-id="b4553-222">Therefore, printing tends to be slower than it is on printers that use OPOS controls.</span></span>
- <span data-ttu-id="b4553-223">使用 Windows 驱动程序时，通过打印机连接（菊链方式）的设备可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="b4553-223">Devices that are connected through the printer ("daisy-chained") might not work correctly when Windows drivers are used.</span></span> <span data-ttu-id="b4553-224">例如，银箱可能无法打开，或者票据打印机可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="b4553-224">For example, the cash drawer might not open, or the slip printer might not word as you expect.</span></span>
- <span data-ttu-id="b4553-225">OPOS 还支持特定于零售收据打印机的更多变体集合，如裁纸或票据打印。</span><span class="sxs-lookup"><span data-stu-id="b4553-225">OPOS also supports a more extensive set of variables that are specific to retail receipt printers, such as paper cutting or slip printing.</span></span>

<span data-ttu-id="b4553-226">如果 OPOS 控件适用于您在使用的 Windows 打印机，该打印机仍然可以与 Microsoft Dynamics 365 for Retail 配合正常工作。</span><span class="sxs-lookup"><span data-stu-id="b4553-226">If OPOS controls are available for the Windows printer that you're using, the printer should still work correctly with Microsoft Dynamics 365 for Retail.</span></span>

### <a name="universal-windows-platform"></a><span data-ttu-id="b4553-227">通用 Windows 平台</span><span class="sxs-lookup"><span data-stu-id="b4553-227">Universal Windows Platform</span></span>

<span data-ttu-id="b4553-228">对于零售外设，UWP 与 Windows 对即插即用设备的支持有关。</span><span class="sxs-lookup"><span data-stu-id="b4553-228">UWP, in the case of retail peripherals, is related to Windows support for Plug and Play devices.</span></span> <span data-ttu-id="b4553-229">当即插即用设备连接到支持这种设备的 Windows 操作系统版本时，该设备不需要驱动程序即可正常使用。</span><span class="sxs-lookup"><span data-stu-id="b4553-229">When a Plug and Play device is connected to a Windows OS version that supports that type of device, no driver is required for the device to be used as intended.</span></span> <span data-ttu-id="b4553-230">例如，如果 Windows 检测到 Bluetooth 扬声器设备，该操作系统知道此设备的类类型为**扬声器**。</span><span class="sxs-lookup"><span data-stu-id="b4553-230">For example, if Windows detects a Bluetooth speaker device, the OS knows that the device has the **Speaker** class type.</span></span> <span data-ttu-id="b4553-231">因此，它将把此设备视为扬声器。</span><span class="sxs-lookup"><span data-stu-id="b4553-231">Therefore, and it treats that device as a speaker.</span></span> <span data-ttu-id="b4553-232">无需再执行任何设置。</span><span class="sxs-lookup"><span data-stu-id="b4553-232">No additional setup is required.</span></span> <span data-ttu-id="b4553-233">对于 POS 设备，可以插入大量 USB 设备，并且 Windows 将把其识别为人机接口设备 (HID)。</span><span class="sxs-lookup"><span data-stu-id="b4553-233">In the case of POS devices, many USB devices can be plugged in, and Windows will recognize them as Human Interface Devices (HIDs).</span></span> <span data-ttu-id="b4553-234">但是，可能不能确定设备提供的功能，因为设备不指定设备的类（即类型）。</span><span class="sxs-lookup"><span data-stu-id="b4553-234">However, it might not be able to determine the capabilities that the device provides, because the device doesn't specify the class, or type, of device.</span></span> <span data-ttu-id="b4553-235">在 Windows 10 中，已增加了条码扫描仪 和 MSR 的设备类。</span><span class="sxs-lookup"><span data-stu-id="b4553-235">In Windows 10, device classes for bar code scanners and MSRs have been added.</span></span> <span data-ttu-id="b4553-236">因此，如果设备向 Windows 10 声明自己是这些类之一的设备，Windows 将在相应时间注意来自该设备的事件。</span><span class="sxs-lookup"><span data-stu-id="b4553-236">Therefore, if a device declares itself to Windows 10 as a device of one of these classes, Windows will listen for events from the device at the appropriate times.</span></span> <span data-ttu-id="b4553-237">Modern POS 支持 UWP MSR 和扫描仪。</span><span class="sxs-lookup"><span data-stu-id="b4553-237">Modern POS supports UWP MSRs and scanners.</span></span> <span data-ttu-id="b4553-238">因此，准备好从这些设备之一输入，并且已连接属于这些类之一的设备时，可以使用该设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-238">Therefore, when it's ready for input from one of these devices, and a device that belongs to one of these classes is connected, the device can be used.</span></span> <span data-ttu-id="b4553-239">例如，如果在 Windows 10 计算机中插入一台 UWP 条码扫描仪，并且为 Modern POS 配置了条码签到，将在签到屏幕上激活该条码扫描仪。</span><span class="sxs-lookup"><span data-stu-id="b4553-239">For example, if a UWP bar code scanner is plugged into a Windows 10 computer, and bar code sign-in is configured for Modern POS, the bar code scanner will become active on the sign-in screen.</span></span> <span data-ttu-id="b4553-240">无需再执行任何设置。</span><span class="sxs-lookup"><span data-stu-id="b4553-240">No additional setup is required.</span></span> <span data-ttu-id="b4553-241">正在向 Windows 添加更多服务点 UWP 设备类。</span><span class="sxs-lookup"><span data-stu-id="b4553-241">Additional classes of point of service UWP devices are being added to Windows.</span></span> <span data-ttu-id="b4553-242">这些类中包括银箱和收据打印机的类。</span><span class="sxs-lookup"><span data-stu-id="b4553-242">These classes include classes for cash drawers and receipt printers.</span></span> <span data-ttu-id="b4553-243">Modern POS 中对这些新设备的支持待定。</span><span class="sxs-lookup"><span data-stu-id="b4553-243">Support for these new device classes in Modern POS is pending.</span></span>

### <a name="keyboard-wedge"></a><span data-ttu-id="b4553-244">键盘 wedge</span><span class="sxs-lookup"><span data-stu-id="b4553-244">Keyboard wedge</span></span>

<span data-ttu-id="b4553-245">键盘 wedge 设备向计算机发送数据，就像数据是从键盘键入的。</span><span class="sxs-lookup"><span data-stu-id="b4553-245">Keyboard wedge devices send data to the computer as if that data were typed on a keyboard.</span></span> <span data-ttu-id="b4553-246">因此默认情况下，POS 上的活动字段将收到扫描或刷卡的数据。</span><span class="sxs-lookup"><span data-stu-id="b4553-246">Therefore, by default, the field that is active at the POS will receive the data that is scanned or swiped.</span></span> <span data-ttu-id="b4553-247">在某些情况下，此行为可能导致将错误类型的数据扫描到错误的字段中。</span><span class="sxs-lookup"><span data-stu-id="b4553-247">In some cases, this behavior can cause the wrong type of data to be scanned into the wrong field.</span></span> <span data-ttu-id="b4553-248">例如，可能将条码扫描到本应输入信用卡数据的字段。</span><span class="sxs-lookup"><span data-stu-id="b4553-248">For example, a bar code might be scanned into a field that is intended for input of credit card data.</span></span> <span data-ttu-id="b4553-249">在大多数情况下，POS 中有逻辑可确定扫描的数据是条码还是刷卡。</span><span class="sxs-lookup"><span data-stu-id="b4553-249">In many cases, there is logic at the POS that determines whether the data that is scanned or swiped is a bar code or card swipe.</span></span> <span data-ttu-id="b4553-250">因此可以正确处理数据。</span><span class="sxs-lookup"><span data-stu-id="b4553-250">Therefore, the data is handled correctly.</span></span> <span data-ttu-id="b4553-251">但是，当设备设置为 OPOS 而不是键盘 wedge 设备时，对来自这些设备的数据的使用方式控制更严格，因为对数据的来源设备的“了解”更深。</span><span class="sxs-lookup"><span data-stu-id="b4553-251">However, when devices are set up as OPOS instead of keyboard wedge devices, there is more control over how the data from those devices can be consumed, because more is "known" about the device that the data originates from.</span></span> <span data-ttu-id="b4553-252">例如，来自条码扫描仪的数据自动识别为条码，并且相比过去使用的一般字符串搜索（如使用键盘 wedge 设备时），可以更轻松、更快地找到数据库中的关联记录。</span><span class="sxs-lookup"><span data-stu-id="b4553-252">For example, data from a bar code scanner is automatically recognized as a bar code, and the associated record in the database is found more easily and faster than if a generic string search were used, as in the case of keyboard wedge devices.</span></span>

### <a name="native-printer"></a><span data-ttu-id="b4553-253">本机打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-253">Native printer</span></span>

<span data-ttu-id="b4553-254">可以将本机（或“设备”，因为类型是在硬件配置文件中命名的）配置为提示用户选择为计算机配置的打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-254">Native (or "Device" as the type is named in the hardware profile) printers can be configured to prompt the user to select a printer that is configured for the computer.</span></span> <span data-ttu-id="b4553-255">配置了**设备**类型的打印机时，如果 Modern POS 收到了打印命令，将提示用户在列表中选择打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-255">When a printer of the **Device** type is configured, if Modern POS encounters a print command, the user is prompted to select a printer in a list.</span></span> <span data-ttu-id="b4553-256">此行为与 Windows 驱动程序的行为不同，因为硬件配置文件中的 **Windows** 打印机类型不显示打印机列表。</span><span class="sxs-lookup"><span data-stu-id="b4553-256">This behavior differs from the behavior for Windows drivers, because the **Windows** printer type in the hardware profile doesn't show a list of printers.</span></span> <span data-ttu-id="b4553-257">相反，它要求在**设备名称**字段中提供命名的打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-257">Instead, it requires that a named printer be provided in the **Device name** field.</span></span>

### <a name="windows"></a><span data-ttu-id="b4553-258">窗口</span><span class="sxs-lookup"><span data-stu-id="b4553-258">Windows</span></span>

<span data-ttu-id="b4553-259">**Windows** 设备类型仅用于打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-259">The **Windows** device type is used for printers only.</span></span> <span data-ttu-id="b4553-260">在硬件配置文件中配置了 Windows 打印机时，必须指定具体的打印机名称。</span><span class="sxs-lookup"><span data-stu-id="b4553-260">When a Windows printer is configured in the hardware profile, the specific printer name must be provided.</span></span> <span data-ttu-id="b4553-261">在 Modern POS 遇到打印事件时，如果配置了 Windows 打印机，将把该事件传递到指定的 Windows 打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-261">When Modern POS encounters print events, if a Windows printer is configured, the event will be passed to the specified Windows printer.</span></span> <span data-ttu-id="b4553-262">将不提示用户选择打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-262">The user won't be prompted to select a printer.</span></span>

### <a name="network"></a><span data-ttu-id="b4553-263">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-263">Network</span></span>

<span data-ttu-id="b4553-264">可通过 Modern POS for Windows 应用程序中内置的进程间通信 (IPC) 硬件工作站或其他 Modern POS 客户端的 IIS 硬件工作站，通过网络使用网络可寻址银箱、收据打印机和付款终端。</span><span class="sxs-lookup"><span data-stu-id="b4553-264">Network-addressable cash drawers, receipt printers, and payment terminals can be used over a network, either directly through the Interprocess Communications (IPC) hardware station that is built into the Modern POS for Windows application or through the IIS hardware station for other Modern POS clients.</span></span>

## <a name="hardware-station-deployment-options"></a><span data-ttu-id="b4553-265">硬件工作站部署选项</span><span class="sxs-lookup"><span data-stu-id="b4553-265">Hardware station deployment options</span></span>

### <a name="ipc-built-in"></a><span data-ttu-id="b4553-266">IPC（内置）</span><span class="sxs-lookup"><span data-stu-id="b4553-266">IPC (built-in)</span></span>

<span data-ttu-id="b4553-267">进程间通信 (IPC) 硬件工作站内置在 Modern POS for Windows 应用程序中。</span><span class="sxs-lookup"><span data-stu-id="b4553-267">The Interprocess Communications (IPC) hardware station is built into the Modern POS for Windows application.</span></span> <span data-ttu-id="b4553-268">若要使用 IPC 硬件工作站，请为将使用 Modern POS for Windows 应用程序的收银机分配硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-268">To use the IPC hardware station, assign a hardware profile to a register that will use the Modern POS for Windows application.</span></span> <span data-ttu-id="b4553-269">然后为将使用该收银机的商店创建一个类型为**专用**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-269">Then create a hardware station of the **Dedicated** type for the store where the register will be used.</span></span> <span data-ttu-id="b4553-270">启动 Modern POS 时，将激活 IPC 硬件工作站，而已配置的 POS 外设将准备就绪，可供使用。</span><span class="sxs-lookup"><span data-stu-id="b4553-270">When you start Modern POS, the IPC hardware station will be active, and the POS peripherals that have been configured will be ready to use.</span></span> <span data-ttu-id="b4553-271">如果因为某种原因暂时不需要本地硬件，请使用**管理硬件工作站**关闭硬件工作站功能。</span><span class="sxs-lookup"><span data-stu-id="b4553-271">If you temporarily don't require the local hardware for some reason, use the **Manage hardware stations** operation to turn off the hardware station capabilities.</span></span> <span data-ttu-id="b4553-272">Modern POS 也可以使用 IPC 硬件工作站直接与网络外设通信。</span><span class="sxs-lookup"><span data-stu-id="b4553-272">Modern POS can also use the IPC hardware station to communicate directly with network peripherals.</span></span>

### <a name="iis"></a><span data-ttu-id="b4553-273">IIS</span><span class="sxs-lookup"><span data-stu-id="b4553-273">IIS</span></span>

<span data-ttu-id="b4553-274">可以通过两种方式使用硬件工作站的 IIS 或单机版本。</span><span class="sxs-lookup"><span data-stu-id="b4553-274">You can use the IIS or stand-alone version of the hardware station in two ways.</span></span> <span data-ttu-id="b4553-275">描述符“IIS”暗示 POS 应用程序通过 Microsoft Internet Information Services 连接到硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-275">The descriptor "IIS" implies that the POS application connects to the hardware station via Microsoft Internet Information Services.</span></span> <span data-ttu-id="b4553-276">POS 应用程序通过连接设备的计算机上运行的 Web 服务连接到 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-276">The POS application connects to the IIS hardware station via web services that run on a computer where the devices are connected.</span></span> <span data-ttu-id="b4553-277">使用 IIS 时，与 IIS 硬件工作站在同一个网络中的任何 POS 收银机都可以使用与该硬件工作站相连的零售外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-277">When IIS is used, the retail peripherals that are connected to a hardware station can be used by any POS register that is on the same network as the IIS hardware station.</span></span> <span data-ttu-id="b4553-278">由于只有 Modern POS for Windows 中才包含对零售外设的内置支持，所以其他所有 Modern POS 应用程序都必须使用 IIS 硬件工作站才能与硬件配置文件中配置的 POS 外设通信。</span><span class="sxs-lookup"><span data-stu-id="b4553-278">Because only Modern POS for Windows includes built-in support for retail peripherals, all other Modern POS applications must use the IIS hardware station to communicate with POS peripherals that are configured in the hardware profile.</span></span> <span data-ttu-id="b4553-279">因此，IIS 硬件工作站的每个实例都需要运行与设备通信的 Web 服务和应用程序的计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-279">Therefore, each instance of the IIS hardware station requires a computer that runs the web service and application that communicates with the devices.</span></span> <span data-ttu-id="b4553-280">所有非 Windows Modern POS 应用程序都需要 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-280">The IIS hardware station is required for all non-Windows Modern POS applications.</span></span>

#### <a name="dedicated"></a><span data-ttu-id="b4553-281">专门</span><span class="sxs-lookup"><span data-stu-id="b4553-281">Dedicated</span></span>

<span data-ttu-id="b4553-282">Modern POS 使用**专用**类型的硬件工作站检测外设是否直接连接到正在使用该应用程序的计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-282">Modern POS uses hardware stations of the **Dedicated** type to detect that peripherals are directly connected to the computer where the app is being used.</span></span> <span data-ttu-id="b4553-283">但是，**专用**类型也可用于 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-283">However, the **Dedicated** type can also be used for IIS hardware stations.</span></span> <span data-ttu-id="b4553-284">在将 Cloud POS 用作 POS 应用程序的传统固定式 POS 方案中，**专用**硬件工作站用于运行 Cloud POS 的同一计算机上部署的 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-284">In a traditional, fixed POS scenario that uses Cloud POS as the POS application, the **Dedicated** hardware station type is used for IIS hardware stations that are deployed on the same computer that is running Cloud POS.</span></span> <span data-ttu-id="b4553-285">从零售外设的角度，专用 IIS 硬件工作站对零售外设的支持比传统的固定式 POS 方案更出色。</span><span class="sxs-lookup"><span data-stu-id="b4553-285">From a retail peripherals perspective, the dedicated IIS hardware station has better retail peripheral support for traditional, fixed POS scenarios.</span></span> <span data-ttu-id="b4553-286">专用硬件工作站支持硬件配置文件中支持的所有外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-286">Dedicated hardware stations support all peripherals that are supported in the hardware profile.</span></span>

#### <a name="shared"></a><span data-ttu-id="b4553-287">共享的</span><span class="sxs-lookup"><span data-stu-id="b4553-287">Shared</span></span>

<span data-ttu-id="b4553-288">共享硬件工作站应该可以全天供多个 POS 设备使用。</span><span class="sxs-lookup"><span data-stu-id="b4553-288">Shared hardware stations are intended to be used by multiple POS devices through the course of the day.</span></span> <span data-ttu-id="b4553-289">共享硬件工作站已经过优化，只能支持银箱、收据打印机和付款终端。</span><span class="sxs-lookup"><span data-stu-id="b4553-289">Shared hardware stations are optimized to support only cash drawers, receipt printers, and payment terminals.</span></span> <span data-ttu-id="b4553-290">不能直接连接单机条码扫描仪、行显示器，MSR、秤或其他设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-290">You can't directly connect stand-alone bar code scanners, MSRs, line displays, scales, or other devices.</span></span> <span data-ttu-id="b4553-291">否则，多个 POS 设备同时尝试声明这些外设时，将发生冲突。</span><span class="sxs-lookup"><span data-stu-id="b4553-291">Otherwise, conflicts will occur when multiple POS devices try to claim those peripherals at the same time.</span></span> <span data-ttu-id="b4553-292">下面是如何管理受支持设备的冲突：</span><span class="sxs-lookup"><span data-stu-id="b4553-292">Here is how conflicts are managed for supported devices:</span></span>

- <span data-ttu-id="b4553-293">**银箱** – 银箱通过发送到设备的事件打开。</span><span class="sxs-lookup"><span data-stu-id="b4553-293">**Cash drawer** – The cash drawer is opened via an event that is sent to the device.</span></span> <span data-ttu-id="b4553-294">仅当银箱已打开时，才会在调用银箱时发生问题。</span><span class="sxs-lookup"><span data-stu-id="b4553-294">The only issue that can occur when a cash drawer is called occurs if the cash drawer is already open.</span></span> <span data-ttu-id="b4553-295">对于共享硬件工作站，应在硬件配置文件中将银箱设置为**共享**。</span><span class="sxs-lookup"><span data-stu-id="b4553-295">In the case of shared hardware stations, the cash drawer should be set to **Shared** in the hardware profile.</span></span> <span data-ttu-id="b4553-296">发送打开命令时，此设置阻止 POS 检查银箱是否已打开。</span><span class="sxs-lookup"><span data-stu-id="b4553-296">This setting prevents the POS from checking whether the cash drawer is already open when it sends open commands.</span></span>
- <span data-ttu-id="b4553-297">**收据打印机** – 如果同时向硬件工作站发送两条收据打印命令，可能丢失其中一条命令，具体取决于设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-297">**Receipt printer** – If two receipt printing commands are sent to the hardware station at the same time, one of the commands can be lost, depending on the device.</span></span> <span data-ttu-id="b4553-298">某些设备有内存或池，可以防止此问题。</span><span class="sxs-lookup"><span data-stu-id="b4553-298">Some devices have internal memory or pooling that can prevent this issue.</span></span> <span data-ttu-id="b4553-299">如果打印命令不成功，收银员将收到错误消息，可以从 POS 重试该打印命令。</span><span class="sxs-lookup"><span data-stu-id="b4553-299">If a print command isn't successful, the cashier receives an error message and can retry the print command from the POS.</span></span>
- <span data-ttu-id="b4553-300">**付款终端** – 如果收银员尝试在已在使用的付款终端上处理交易的支付，将显示消息，通知收银员正在使用该终端，请收银员稍后重试。</span><span class="sxs-lookup"><span data-stu-id="b4553-300">**Payment terminal** – If a cashier tries to tender a transaction on a payment terminal that is already being used, a message notifies the cashier that the terminal is being used and asks the cashier to try again later.</span></span> <span data-ttu-id="b4553-301">通常，收银员可以看到终端已在使用并等待其他交易完成，再尝试处理付款。</span><span class="sxs-lookup"><span data-stu-id="b4553-301">Usually, cashiers can see that a terminal is already being used and will wait until the other transaction is completed before they try to tender again.</span></span>

<span data-ttu-id="b4553-302">为将来的版本计划了验证，以便检测是否为映射到共享硬件工作站的硬件配置文件设置了不受支持的设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-302">Validation is planned for a future release, to detect whether unsupported devices are set up for a hardware profile that is mapped to a shared hardware station.</span></span> <span data-ttu-id="b4553-303">如果检测到不受支持的设备，用户将收到消息，说明共享硬件工作站不支持这些设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-303">If any unsupported devices are detected, the user will receive a message that states that the devices aren't supported for shared hardware stations.</span></span> <span data-ttu-id="b4553-304">对于共享硬件工作站，**付款后即可选择**选项在收银机级别设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b4553-304">In the case of shared hardware stations, the **Select upon tendering** option is set to **Yes** at the register level.</span></span> <span data-ttu-id="b4553-305">然后在 POS 中为交易选择了付款时，将提示 POS 用户选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-305">The POS user is then prompted to select a hardware station when a tender is selected for a transaction at the POS.</span></span> <span data-ttu-id="b4553-306">仅在付款时选择了硬件工作站时，将把对硬件工作站的选择直接添加到移动方案的 POS 工作流。</span><span class="sxs-lookup"><span data-stu-id="b4553-306">When the hardware station is selected only at the time of tender, the hardware station selection is added directly to the POS workflow for mobile scenarios.</span></span> <span data-ttu-id="b4553-307">额外福利是，付款终端上的行显示器不用于共享方案。</span><span class="sxs-lookup"><span data-stu-id="b4553-307">As an additional benefit, the line display on the payment terminal isn't used for shared scenarios.</span></span> <span data-ttu-id="b4553-308">如果付款终端用作行显示器，交易完成前，可能阻止其他用户使用该终端。</span><span class="sxs-lookup"><span data-stu-id="b4553-308">If the payment terminal is used as a line display, other users might be blocked from using that terminal until the transaction is completed.</span></span> <span data-ttu-id="b4553-309">在移动方案中，可能在较长一段时间内向交易添加行。</span><span class="sxs-lookup"><span data-stu-id="b4553-309">In mobile scenarios, lines might be added to a transaction over a longer period.</span></span> <span data-ttu-id="b4553-310">因此，需要**付款后即可选择**选项以确保最适宜的设备可用性。</span><span class="sxs-lookup"><span data-stu-id="b4553-310">Therefore, the **Select upon tendering** option is required in order to ensure optimum device availability.</span></span>

### <a name="network-peripherals"></a><span data-ttu-id="b4553-311">网络外设</span><span class="sxs-lookup"><span data-stu-id="b4553-311">Network peripherals</span></span>

<span data-ttu-id="b4553-312">硬件配置文件中为设备指派的网络让银箱、收据打印机和付款终端可以通过网络连接来连接。</span><span class="sxs-lookup"><span data-stu-id="b4553-312">The network designation for devices in the hardware profile enables cash drawers, receipt printers, and payment terminals to be connected via a network connection.</span></span>

#### <a name="modern-pos-for-windows"></a><span data-ttu-id="b4553-313">Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="b4553-313">Modern POS for Windows</span></span>

<span data-ttu-id="b4553-314">可以为两处的网络外设指定 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="b4553-314">You can specify IP addresses for network peripherals in two places.</span></span> <span data-ttu-id="b4553-315">如果 Modern POS Windows 客户端使用一组网络外设，您应该通过使用收银机自身的“操作窗格”上的 **IP 配置**选项为这些设备设置 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="b4553-315">If the Modern POS Windows client is using a single set of network peripherals, you should set the IP addresses for those devices by using the **IP configuration** option on the Action Pane for the register itself.</span></span> <span data-ttu-id="b4553-316">对于将在 POS 收银机之间共享的网络设备，可以将为其指派的硬件配置文件直接映射到共享硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-316">In the case of network devices that will be shared among POS registers, a hardware profile that has network devices assigned to it can be mapped directly to a shared hardware station.</span></span> <span data-ttu-id="b4553-317">若要分配 IP 地址，请在**零售商店**页中选择该硬件工作站，然后使用**硬件工作站**部分中的 **IP 配置**选项指定为该硬件工作站分配的网络设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-317">To assign IP addresses, select that hardware station on the **Retail stores** page, and then use the **IP configuration** option in the **Hardware stations** section to specify the network devices that are assigned to that hardware station.</span></span> <span data-ttu-id="b4553-318">对于只有网络设备的硬件工作站，则不必部署硬件工作站本身。</span><span class="sxs-lookup"><span data-stu-id="b4553-318">For hardware stations that have only network devices, you don't have to deploy the hardware station itself.</span></span> <span data-ttu-id="b4553-319">在这种情况下，仅当要在概念上根据可网络寻址的设备在零售商店中的位置为这些设备分组时，才需要硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-319">In this case, the hardware station is required only in order to conceptually group network-addressable devices according to their location in the retail store.</span></span>

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a><span data-ttu-id="b4553-320">Cloud POS、Modern POS for iOS 和 Modern POS for Android</span><span class="sxs-lookup"><span data-stu-id="b4553-320">Cloud POS, Modern POS for iOS, and Modern POS for Android</span></span>

<span data-ttu-id="b4553-321">硬件工作站中包含驱动以物理方式相连且可网络寻址的外设的逻辑。</span><span class="sxs-lookup"><span data-stu-id="b4553-321">The logic that drives physically connected and network-addressable peripherals is contained in the hardware station.</span></span> <span data-ttu-id="b4553-322">因此，对于除 Modern POS for Windows 之外的所有 POS 客户端，必须部署并激活 IIS 硬件工作站，以便让 POS 可以与外设通信，无论这些外设是以物理方式连接到硬件工作站还是通过网络寻址。</span><span class="sxs-lookup"><span data-stu-id="b4553-322">Therefore, for all POS clients except Modern POS for Windows, an IIS hardware station must be deployed and active to enable the POS to communicate with peripherals, regardless of whether those peripherals are physically connected to a hardware station or addressed over the network.</span></span>

## <a name="setup-and-configuration"></a><span data-ttu-id="b4553-323">设置和配置</span><span class="sxs-lookup"><span data-stu-id="b4553-323">Setup and configuration</span></span>

### <a name="hardware-station-installation"></a><span data-ttu-id="b4553-324">硬件工作站安装</span><span class="sxs-lookup"><span data-stu-id="b4553-324">Hardware station installation</span></span>

<span data-ttu-id="b4553-325">有关新信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-325">For information, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>

### <a name="modern-pos-for-windows-setup-and-configuration"></a><span data-ttu-id="b4553-326">Modern POS for Windows 设置和配置</span><span class="sxs-lookup"><span data-stu-id="b4553-326">Modern POS for Windows setup and configuration</span></span>

<span data-ttu-id="b4553-327">有关新信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-327">For information, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>

### <a name="opos-device-setup-and-configuration"></a><span data-ttu-id="b4553-328">OPOS 设备设置和配置</span><span class="sxs-lookup"><span data-stu-id="b4553-328">OPOS device setup and configuration</span></span>

<span data-ttu-id="b4553-329">有关 OPOS 组件的详细信息，请参阅本文的“支持的接口”。</span><span class="sxs-lookup"><span data-stu-id="b4553-329">For more information about OPOS components, see the "Supported interfaces" section of this document.</span></span> <span data-ttu-id="b4553-330">OPOS 驱动程序通常由设备制造商提供。</span><span class="sxs-lookup"><span data-stu-id="b4553-330">Typically, OPOS drivers are provided by the device manufacturer.</span></span> <span data-ttu-id="b4553-331">安装 OPOS 设备驱动程序时，将在 Windows 注册表中的以下位置添加一个键：</span><span class="sxs-lookup"><span data-stu-id="b4553-331">When an OPOS device driver is installed, it adds a key to the Windows registry in one of the following locations:</span></span>

- <span data-ttu-id="b4553-332">**32 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-332">**32-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span></span>
- <span data-ttu-id="b4553-333">**64 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-333">**64-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span></span>

<span data-ttu-id="b4553-334">在 ServiceOPOS 注册表位置中，配置的设备根据 OPOS 设备类组织。</span><span class="sxs-lookup"><span data-stu-id="b4553-334">Within the ServiceOPOS registry location, configured devices are organized according to the OPOS device class.</span></span> <span data-ttu-id="b4553-335">将保存多个设备驱动程序。</span><span class="sxs-lookup"><span data-stu-id="b4553-335">Multiple device drivers are saved.</span></span>

## <a name="supported-scenarios-by-hardware-station-type"></a><span data-ttu-id="b4553-336">硬件工作站类型支持的方案</span><span class="sxs-lookup"><span data-stu-id="b4553-336">Supported scenarios by hardware station type</span></span>

### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a><span data-ttu-id="b4553-337">客户端支持 – IPC 硬件工作站与 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-337">Client support – IPC hardware station vs. IIS hardware station</span></span>

<span data-ttu-id="b4553-338">下表显示支持的拓扑和部署方案。</span><span class="sxs-lookup"><span data-stu-id="b4553-338">The following table shows the topologies and deployment scenarios that are supported.</span></span>

| <span data-ttu-id="b4553-339">客户</span><span class="sxs-lookup"><span data-stu-id="b4553-339">Client</span></span>      | <span data-ttu-id="b4553-340">IPC 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-340">IPC hardware station</span></span> | <span data-ttu-id="b4553-341">IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-341">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="b4553-342">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="b4553-342">Windows app</span></span> | <span data-ttu-id="b4553-343">是</span><span class="sxs-lookup"><span data-stu-id="b4553-343">Yes</span></span>                  | <span data-ttu-id="b4553-344">是</span><span class="sxs-lookup"><span data-stu-id="b4553-344">Yes</span></span>                  |
| <span data-ttu-id="b4553-345">云 POS</span><span class="sxs-lookup"><span data-stu-id="b4553-345">Cloud POS</span></span>   | <span data-ttu-id="b4553-346">无</span><span class="sxs-lookup"><span data-stu-id="b4553-346">No</span></span>                   | <span data-ttu-id="b4553-347">是</span><span class="sxs-lookup"><span data-stu-id="b4553-347">Yes</span></span>                  |
| <span data-ttu-id="b4553-348">Android</span><span class="sxs-lookup"><span data-stu-id="b4553-348">Android</span></span>     | <span data-ttu-id="b4553-349">无</span><span class="sxs-lookup"><span data-stu-id="b4553-349">No</span></span>                   | <span data-ttu-id="b4553-350">是</span><span class="sxs-lookup"><span data-stu-id="b4553-350">Yes</span></span>                  |
| <span data-ttu-id="b4553-351">iOS</span><span class="sxs-lookup"><span data-stu-id="b4553-351">iOS</span></span>         | <span data-ttu-id="b4553-352">无</span><span class="sxs-lookup"><span data-stu-id="b4553-352">No</span></span>                   | <span data-ttu-id="b4553-353">是</span><span class="sxs-lookup"><span data-stu-id="b4553-353">Yes</span></span>                  |

### <a name="network-peripherals"></a><span data-ttu-id="b4553-354">网络外设</span><span class="sxs-lookup"><span data-stu-id="b4553-354">Network peripherals</span></span>

<span data-ttu-id="b4553-355">可以直接通过 Modern POS for Windows 应用程序中内置的硬件工作站支持网络外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-355">Network peripherals can be supported directly through the hardware station that is built into the Modern POS for Windows application.</span></span> <span data-ttu-id="b4553-356">对于其他所有客户端，则必须部署 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-356">For all other clients, you must deploy an IIS hardware station.</span></span>

| <span data-ttu-id="b4553-357">客户</span><span class="sxs-lookup"><span data-stu-id="b4553-357">Client</span></span>      | <span data-ttu-id="b4553-358">IPC 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-358">IPC hardware station</span></span> | <span data-ttu-id="b4553-359">IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-359">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="b4553-360">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="b4553-360">Windows app</span></span> | <span data-ttu-id="b4553-361">是</span><span class="sxs-lookup"><span data-stu-id="b4553-361">Yes</span></span>                  | <span data-ttu-id="b4553-362">是</span><span class="sxs-lookup"><span data-stu-id="b4553-362">Yes</span></span>                  |
| <span data-ttu-id="b4553-363">云 POS</span><span class="sxs-lookup"><span data-stu-id="b4553-363">Cloud POS</span></span>   | <span data-ttu-id="b4553-364">无</span><span class="sxs-lookup"><span data-stu-id="b4553-364">No</span></span>                   | <span data-ttu-id="b4553-365">是</span><span class="sxs-lookup"><span data-stu-id="b4553-365">Yes</span></span>                  |
| <span data-ttu-id="b4553-366">Android</span><span class="sxs-lookup"><span data-stu-id="b4553-366">Android</span></span>     | <span data-ttu-id="b4553-367">无</span><span class="sxs-lookup"><span data-stu-id="b4553-367">No</span></span>                   | <span data-ttu-id="b4553-368">是</span><span class="sxs-lookup"><span data-stu-id="b4553-368">Yes</span></span>                  |
| <span data-ttu-id="b4553-369">iOS</span><span class="sxs-lookup"><span data-stu-id="b4553-369">iOS</span></span>         | <span data-ttu-id="b4553-370">无</span><span class="sxs-lookup"><span data-stu-id="b4553-370">No</span></span>                   | <span data-ttu-id="b4553-371">是</span><span class="sxs-lookup"><span data-stu-id="b4553-371">Yes</span></span>                  |

## <a name="supported-device-types-by-hardware-station-type"></a><span data-ttu-id="b4553-372">硬件工作站类型支持的设备类型</span><span class="sxs-lookup"><span data-stu-id="b4553-372">Supported device types by hardware station type</span></span>

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="b4553-373">带 IPC（内置）硬件工作站的 Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="b4553-373">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b4553-374">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="b4553-374">Supported device class</span></span></th>
<th><span data-ttu-id="b4553-375">支持的接口</span><span class="sxs-lookup"><span data-stu-id="b4553-375">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b4553-376">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-376">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-377">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-377">OPOS</span></span></li>
<li><span data-ttu-id="b4553-378">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-378">Windows driver</span></span></li>
<li><span data-ttu-id="b4553-379">设备</span><span class="sxs-lookup"><span data-stu-id="b4553-379">Device</span></span></li>
<li><span data-ttu-id="b4553-380">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-380">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-381">打印机 2</span><span class="sxs-lookup"><span data-stu-id="b4553-381">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-382">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-382">OPOS</span></span></li>
<li><span data-ttu-id="b4553-383">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-383">Windows driver</span></span></li>
<li><span data-ttu-id="b4553-384">设备</span><span class="sxs-lookup"><span data-stu-id="b4553-384">Device</span></span></li>
<li><span data-ttu-id="b4553-385">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-385">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-386">行显示内容</span><span class="sxs-lookup"><span data-stu-id="b4553-386">Line display</span></span></td>
<td><span data-ttu-id="b4553-387">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-387">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-388">双显示器</span><span class="sxs-lookup"><span data-stu-id="b4553-388">Dual display</span></span></td>
<td><span data-ttu-id="b4553-389">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-389">Windows driver</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-390">MSR</span><span class="sxs-lookup"><span data-stu-id="b4553-390">MSR</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-391">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-391">OPOS</span></span></li>
<li><span data-ttu-id="b4553-392">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="b4553-392">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="b4553-393">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="b4553-393">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-394">开票人</span><span class="sxs-lookup"><span data-stu-id="b4553-394">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-395">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-395">OPOS</span></span></li>
<li><span data-ttu-id="b4553-396">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-396">Network</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b4553-397">如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-397">Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></blockquote>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-398">开票人 2</span><span class="sxs-lookup"><span data-stu-id="b4553-398">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-399">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-399">OPOS</span></span></li>
<li><span data-ttu-id="b4553-400">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-400">Network</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b4553-401">如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-401">Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></blockquote>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-402">扫描仪</span><span class="sxs-lookup"><span data-stu-id="b4553-402">Scanner</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-403">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-403">OPOS</span></span></li>
<li><span data-ttu-id="b4553-404">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="b4553-404">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="b4553-405">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="b4553-405">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-406">扫描仪 2</span><span class="sxs-lookup"><span data-stu-id="b4553-406">Scanner 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-407">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-407">OPOS</span></span></li>
<li><span data-ttu-id="b4553-408">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="b4553-408">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="b4553-409">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="b4553-409">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-410">比例</span><span class="sxs-lookup"><span data-stu-id="b4553-410">Scale</span></span></td>
<td><span data-ttu-id="b4553-411">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-411">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-412">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="b4553-412">PIN pad</span></span></td>
<td><span data-ttu-id="b4553-413">OPOS（通过自定义付款连接器提供支持。）</span><span class="sxs-lookup"><span data-stu-id="b4553-413">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-414">签名捕获</span><span class="sxs-lookup"><span data-stu-id="b4553-414">Signature capture</span></span></td>
<td><span data-ttu-id="b4553-415">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-415">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-416">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-416">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-417">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="b4553-417">Custom device support</span></span></li>
<li><span data-ttu-id="b4553-418">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="b4553-418">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a><span data-ttu-id="b4553-419">有专用 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="b4553-419">All Modern POS clients that have a dedicated IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-420">当 IIS 硬件工作站为“专用”时，POS 客户端与硬件工作站之间存在一对一关系。</span><span class="sxs-lookup"><span data-stu-id="b4553-420">When the IIS hardware station is "dedicated," there is a one-to-one relationship between the POS client and the hardware station.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b4553-421">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="b4553-421">Supported device class</span></span></th>
<th><span data-ttu-id="b4553-422">支持的接口</span><span class="sxs-lookup"><span data-stu-id="b4553-422">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b4553-423">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-423">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-424">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-424">OPOS</span></span></li>
<li><span data-ttu-id="b4553-425">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-425">Windows driver</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b4553-426">对于网络中的 Windows 打印机，硬件工作站的用户必须有权访问该打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-426">For Windows printers on a network, the user of the hardware station must have permission to access the printer.</span></span></blockquote>
</li>
<li><span data-ttu-id="b4553-427">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-427">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-428">打印机 2</span><span class="sxs-lookup"><span data-stu-id="b4553-428">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-429">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-429">OPOS</span></span></li>
<li><span data-ttu-id="b4553-430">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-430">Windows driver</span></span></li>
<li><span data-ttu-id="b4553-431">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-431">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-432">行显示内容</span><span class="sxs-lookup"><span data-stu-id="b4553-432">Line display</span></span></td>
<td><span data-ttu-id="b4553-433">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-433">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-434">MSR</span><span class="sxs-lookup"><span data-stu-id="b4553-434">MSR</span></span></td>
<td><span data-ttu-id="b4553-435">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-435">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-436">开票人</span><span class="sxs-lookup"><span data-stu-id="b4553-436">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-437">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-437">OPOS</span></span></li>
<li><span data-ttu-id="b4553-438">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-438">Network</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b4553-439">如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-439">Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></blockquote>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-440">开票人 2</span><span class="sxs-lookup"><span data-stu-id="b4553-440">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-441">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-441">OPOS</span></span></li>
<li><span data-ttu-id="b4553-442">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-442">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-443">扫描仪</span><span class="sxs-lookup"><span data-stu-id="b4553-443">Scanner</span></span></td>
<td><span data-ttu-id="b4553-444">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-444">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-445">扫描仪 2</span><span class="sxs-lookup"><span data-stu-id="b4553-445">Scanner 2</span></span></td>
<td><span data-ttu-id="b4553-446">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-446">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-447">比例</span><span class="sxs-lookup"><span data-stu-id="b4553-447">Scale</span></span></td>
<td><span data-ttu-id="b4553-448">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-448">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-449">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="b4553-449">PIN pad</span></span></td>
<td><span data-ttu-id="b4553-450">OPOS（通过自定义付款连接器提供支持。）</span><span class="sxs-lookup"><span data-stu-id="b4553-450">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-451">签到</span><span class="sxs-lookup"><span data-stu-id="b4553-451">Sig.</span></span> <span data-ttu-id="b4553-452">捕获</span><span class="sxs-lookup"><span data-stu-id="b4553-452">capture</span></span></td>
<td><span data-ttu-id="b4553-453">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-453">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b4553-454">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-454">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-455">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="b4553-455">Custom device support</span></span></li>
<li><span data-ttu-id="b4553-456">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="b4553-456">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="b4553-457">有共享 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="b4553-457">All Modern POS clients that have a shared IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-458">当 IIS 硬件工作站为“共享”时，多台设备可同时使用该硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-458">When the IIS hardware station is "shared," multiple devices can use the hardware station at the same time.</span></span> <span data-ttu-id="b4553-459">对于此方案，应仅使用下表中列出的设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-459">For this scenario, you should use only the devices that are listed in the following table.</span></span> <span data-ttu-id="b4553-460">如果尝试共享此处未列出的设备（如条码扫描仪和 MSR），多台设备尝试声明同一外设时，将出错。</span><span class="sxs-lookup"><span data-stu-id="b4553-460">If you try to share devices that aren't listed here, such as bar code scanners and MSRs, errors will occur when multiple devices try to claim the same peripheral.</span></span> <span data-ttu-id="b4553-461">将来将明确阻止此类配置。</span><span class="sxs-lookup"><span data-stu-id="b4553-461">In the future, such a configuration will be explicitly prevented.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b4553-462">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="b4553-462">Supported device class</span></span></th>
<th><span data-ttu-id="b4553-463">支持的接口</span><span class="sxs-lookup"><span data-stu-id="b4553-463">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b4553-464">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-464">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-465">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-465">OPOS</span></span></li>
<li><span data-ttu-id="b4553-466">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-466">Windows driver</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b4553-467">对于网络中的 Windows 打印机，硬件工作站的用户必须有权访问该打印机。</span><span class="sxs-lookup"><span data-stu-id="b4553-467">For Windows printers on a network, the user of the hardware station must have permission to access the printer.</span></span></blockquote>
</li>
<li><span data-ttu-id="b4553-468">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-468">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-469">打印机 2</span><span class="sxs-lookup"><span data-stu-id="b4553-469">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-470">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-470">OPOS</span></span></li>
<li><span data-ttu-id="b4553-471">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-471">Windows driver</span></span></li>
<li><span data-ttu-id="b4553-472">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-472">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-473">开票人</span><span class="sxs-lookup"><span data-stu-id="b4553-473">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-474">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-474">OPOS</span></span></li>
<li><span data-ttu-id="b4553-475">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-475">Network</span></span>
<blockquote>[!NOTE] <span data-ttu-id="b4553-476">如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-476">Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></blockquote>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-477">开票人 2</span><span class="sxs-lookup"><span data-stu-id="b4553-477">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-478">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-478">OPOS</span></span></li>
<li><span data-ttu-id="b4553-479">网络</span><span class="sxs-lookup"><span data-stu-id="b4553-479">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b4553-480">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-480">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b4553-481">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="b4553-481">Custom device support</span></span></li>
<li><span data-ttu-id="b4553-482">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="b4553-482">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a><span data-ttu-id="b4553-483">支持的方案的配置</span><span class="sxs-lookup"><span data-stu-id="b4553-483">Configuration for supported scenarios</span></span>

<span data-ttu-id="b4553-484">有关如何创建硬件配置文件的详细信息，请参阅[定义和维护渠道客户端，包括收银机和硬件工作站](define-maintain-channel-clients-registers-hw-stations.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-484">For more information about how to create hardware profiles, see [Define and maintain channel clients, including registers and hardware stations](define-maintain-channel-clients-registers-hw-stations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-485">对于 Microsoft Dynamics 365 for Retail 版本 1611，将不再使用硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-485">For Microsoft Dynamics 365 for Retail version 1611, the hardware station profile is no longer used.</span></span> <span data-ttu-id="b4553-486">以前在硬件工作站中设置的属性现在成为了硬件工作站本身的一部分。</span><span class="sxs-lookup"><span data-stu-id="b4553-486">Attributes that you previously set up in the hardware station profile are now part of the hardware station itself.</span></span>

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="b4553-487">带 IPC（内置）硬件工作站的 Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="b4553-487">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<span data-ttu-id="b4553-488">此配置是传统固定式 POS 收银机最典型的配置。</span><span class="sxs-lookup"><span data-stu-id="b4553-488">This configuration is the most typical configuration for traditional, fixed POS registers.</span></span> <span data-ttu-id="b4553-489">对于此方案，硬件配置文件信息直接映射到收银机。</span><span class="sxs-lookup"><span data-stu-id="b4553-489">For this scenario, the hardware profile information is mapped directly to the register itself.</span></span> <span data-ttu-id="b4553-490">还必须在收银机本身中设置 EFT 终端号。</span><span class="sxs-lookup"><span data-stu-id="b4553-490">The EFT terminal number should also be set on the register itself.</span></span> <span data-ttu-id="b4553-491">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b4553-491">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="b4553-492">创建在其中配置所有所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-492">Create a hardware profile where all the required peripherals are configured.</span></span>
2. <span data-ttu-id="b4553-493">将硬件配置文件映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="b4553-493">Map the hardware profile to the POS register.</span></span>
3. <span data-ttu-id="b4553-494">为将使用该 POS 收银机的零售商店创建一个类型为**专用**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-494">Create a hardware station of the **Dedicated** type for the retail store where the POS register will be used.</span></span> <span data-ttu-id="b4553-495">描述可选。</span><span class="sxs-lookup"><span data-stu-id="b4553-495">A description is optional.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4553-496">不必在硬件工作站中设置其他任何属性。</span><span class="sxs-lookup"><span data-stu-id="b4553-496">You don't have to set any other properties on the hardware station.</span></span> <span data-ttu-id="b4553-497">其他所有所需信息（如硬件配置文件）将来自收银机本身。</span><span class="sxs-lookup"><span data-stu-id="b4553-497">All other required information, such as the hardware profile, will come from the register itself.</span></span>

4. <span data-ttu-id="b4553-498">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="b4553-498">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
5. <span data-ttu-id="b4553-499">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="b4553-499">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="b4553-500">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-500">Click **Run now** to sync changes to the POS.</span></span>
6. <span data-ttu-id="b4553-501">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="b4553-501">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="b4553-502">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-502">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="b4553-503">安装并激活 Modern POS for Windows。</span><span class="sxs-lookup"><span data-stu-id="b4553-503">Install and activate Modern POS for Windows.</span></span>
8. <span data-ttu-id="b4553-504">启动 Modern POS for Windows，然后登录到连接的外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-504">Start Modern POS for Windows, and begin to use the connected peripheral devices.</span></span>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a><span data-ttu-id="b4553-505">有专用 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="b4553-505">All Modern POS clients that have a dedicated IIS hardware station</span></span>

<span data-ttu-id="b4553-506">可将此配置用于有一个硬件工作站仅供一台 POS 收银机专用的所有 Modern POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="b4553-506">This configuration can be used for all Modern POS clients that have a hardware station that is used exclusively by one POS register.</span></span> <span data-ttu-id="b4553-507">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b4553-507">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="b4553-508">创建在其中配置所有所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-508">Create a hardware profile where all the required peripherals are configured.</span></span>
2. <span data-ttu-id="b4553-509">为将使用该 POS 收银机的零售商店创建一个类型为**专用**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-509">Create a hardware station of the **Dedicated** type for the retail store where the POS register will be used.</span></span>
3. <span data-ttu-id="b4553-510">在专用硬件工作站中，设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="b4553-510">On the dedicated hardware station, set the following properties:</span></span>

    - <span data-ttu-id="b4553-511">**主机名** – 将运行硬件工作站的主计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="b4553-511">**Host name** – The name of the host computer where the hardware station will run.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b4553-512">Cloud POS 可以解析 **localhost** 以确定运行 Cloud POS 的本地计算机。</span><span class="sxs-lookup"><span data-stu-id="b4553-512">Cloud POS can resolve **localhost** to determine the local computer where Cloud POS is running.</span></span> <span data-ttu-id="b4553-513">但是，将 Cloud POS 与硬件工作站配对所需证书必须也采用“Localhost”来充当计算机名称。</span><span class="sxs-lookup"><span data-stu-id="b4553-513">However, the certificate that is required in order to pair Cloud POS with the hardware station must also have "Localhost" as the computer name.</span></span> <span data-ttu-id="b4553-514">若要避免问题，建议您根据列出商店每个专用硬件工作站的实例。</span><span class="sxs-lookup"><span data-stu-id="b4553-514">To avoid issues, we recommend that you list an instance of each dedicated hardware station for the store, as required.</span></span> <span data-ttu-id="b4553-515">对于每个硬件工作站，主机名应该是将部署硬件工作站的具体计算机名称。</span><span class="sxs-lookup"><span data-stu-id="b4553-515">For each hardware station, the host name should be the specific computer name where the hardware station will be deployed.</span></span>

    - <span data-ttu-id="b4553-516">**端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。</span><span class="sxs-lookup"><span data-stu-id="b4553-516">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    - <span data-ttu-id="b4553-517">**硬件配置文件** – 如果硬件工作站本身中不提供硬件配置文件，将使用为收银机分配的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-517">**Hardware profile** – If the hardware profile isn't provided on the hardware station itself, the hardware profile that is assigned to the register will be used.</span></span>
    - <span data-ttu-id="b4553-518">**EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="b4553-518">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="b4553-519">此 ID 由信用卡处理方提供。</span><span class="sxs-lookup"><span data-stu-id="b4553-519">This ID is provided by the credit card processor.</span></span>
    - <span data-ttu-id="b4553-520">**包名** – 部署硬件工作站时要使用的硬件工作站包。</span><span class="sxs-lookup"><span data-stu-id="b4553-520">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4. <span data-ttu-id="b4553-521">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="b4553-521">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
5. <span data-ttu-id="b4553-522">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="b4553-522">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="b4553-523">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-523">Click **Run now** to sync changes to the POS.</span></span>
6. <span data-ttu-id="b4553-524">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="b4553-524">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="b4553-525">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-525">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="b4553-526">安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-526">Install the hardware station.</span></span> <span data-ttu-id="b4553-527">有关如何安装硬件工作站的详细信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-527">For more information about how to install the hardware station, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>
8. <span data-ttu-id="b4553-528">安装和激活 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-528">Install and activate Modern POS.</span></span> <span data-ttu-id="b4553-529">有关如何安装 Modern POS 的详细信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-529">For more information about how to install Modern POS, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>
9. <span data-ttu-id="b4553-530">登录 Modern POS，然后选择**执行非开票人操作**。</span><span class="sxs-lookup"><span data-stu-id="b4553-530">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
10. <span data-ttu-id="b4553-531">启动**管理硬件工作站**操作。</span><span class="sxs-lookup"><span data-stu-id="b4553-531">Start the **Manage hardware stations** operation.</span></span>
11. <span data-ttu-id="b4553-532">单击**管理**。</span><span class="sxs-lookup"><span data-stu-id="b4553-532">Click **Manage**.</span></span>
12. <span data-ttu-id="b4553-533">在硬件工作站管理页中，设置用于打开硬件工作站的选项。</span><span class="sxs-lookup"><span data-stu-id="b4553-533">On the hardware station management page, set the option to turn on the hardware station.</span></span>
13. <span data-ttu-id="b4553-534">选择要使用的硬件工作站，然后单击**配对**。</span><span class="sxs-lookup"><span data-stu-id="b4553-534">Select the hardware station to use, and then click **Pair**.</span></span>
14. <span data-ttu-id="b4553-535">在硬件工作站配对后，单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="b4553-535">After the hardware station is paired, click **Close**.</span></span>
15. <span data-ttu-id="b4553-536">在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。</span><span class="sxs-lookup"><span data-stu-id="b4553-536">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="b4553-537">有共享 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="b4553-537">All Modern POS clients that have a shared IIS hardware station</span></span>

<span data-ttu-id="b4553-538">此配置可用于与其他设备共享硬件工作站的所有 Modern POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="b4553-538">This configuration can be used for all Modern POS clients that share hardware stations with other devices.</span></span> <span data-ttu-id="b4553-539">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b4553-539">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="b4553-540">创建在其中配置所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-540">Create a hardware profile where the required peripherals are configured.</span></span>
2. <span data-ttu-id="b4553-541">为将使用该 POS 收银机的零售商店创建一个类型为**共享**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-541">Create a hardware station of the **Shared** type for the retail store where the POS register will be used.</span></span>
3. <span data-ttu-id="b4553-542">在共享硬件工作站中，设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="b4553-542">On the shared hardware station, set the following properties:</span></span>

    - <span data-ttu-id="b4553-543">**主机名** – 将运行硬件工作站的主计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="b4553-543">**Host name** – The name of the host computer where the hardware station will run.</span></span>
    - <span data-ttu-id="b4553-544">**描述** – 用于帮助识别硬件工作站的文本，如**退货**或**店前**。</span><span class="sxs-lookup"><span data-stu-id="b4553-544">**Description** – Text that will help identify the hardware station, such as **Returns** or **Front of store**.</span></span>
    - <span data-ttu-id="b4553-545">**端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。</span><span class="sxs-lookup"><span data-stu-id="b4553-545">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    - <span data-ttu-id="b4553-546">**硬件配置文件** – 对于共享硬件工作站，每个硬件工作站都应该有一个硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="b4553-546">**Hardware profile** – For shared hardware stations, each hardware station should have a hardware profile.</span></span> <span data-ttu-id="b4553-547">可以在硬件工作站之间共享硬件配置文件，但必须将其映射到每个硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-547">Hardware profiles can be shared among hardware stations, but they must be mapped to each hardware station.</span></span> <span data-ttu-id="b4553-548">此外，建议在多个设备共享同一个共享硬件工作站时使用共享班次。</span><span class="sxs-lookup"><span data-stu-id="b4553-548">In addition, we recommend that you use shared shifts when multiple devices use the same shared hardware station.</span></span> <span data-ttu-id="b4553-549">若要设置共享班次，单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="b4553-549">To set up a shared shift, click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="b4553-550">对于每个共享硬件配置文件，选择银箱，然后将**共享班次银箱**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b4553-550">For each shared hardware profile, select the cash drawer, and set the **Shared shift drawer** option to **Yes**.</span></span>
    - <span data-ttu-id="b4553-551">**EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="b4553-551">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="b4553-552">此 ID 由信用卡处理方提供。</span><span class="sxs-lookup"><span data-stu-id="b4553-552">This ID is provided by the credit card processor.</span></span>
    - <span data-ttu-id="b4553-553">**包名** – 部署硬件工作站时要使用的硬件工作站包。</span><span class="sxs-lookup"><span data-stu-id="b4553-553">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4. <span data-ttu-id="b4553-554">为商店中所需其他每个硬件工作站重复步骤 2 和 3。</span><span class="sxs-lookup"><span data-stu-id="b4553-554">Repeat steps 2 and 3 for each additional hardware station that is required in the store.</span></span>
5. <span data-ttu-id="b4553-555">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="b4553-555">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="b4553-556">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="b4553-556">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="b4553-557">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-557">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="b4553-558">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="b4553-558">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="b4553-559">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-559">Click **Run now** to sync changes to the POS.</span></span>
8. <span data-ttu-id="b4553-560">在步骤 2 和 3 中设置的每个主机上安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-560">Install the hardware station on each host computer that you set up in steps 2 and 3.</span></span> <span data-ttu-id="b4553-561">有关如何安装硬件工作站的详细信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-561">For more information about how to install the hardware station, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>
9. <span data-ttu-id="b4553-562">安装和激活 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-562">Install and activate Modern POS.</span></span> <span data-ttu-id="b4553-563">有关如何安装 Modern POS 的详细信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-563">For more information about how to install Modern POS, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>
10. <span data-ttu-id="b4553-564">登录 Modern POS，然后选择**执行非开票人操作**。</span><span class="sxs-lookup"><span data-stu-id="b4553-564">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
11. <span data-ttu-id="b4553-565">启动**管理硬件工作站**操作。</span><span class="sxs-lookup"><span data-stu-id="b4553-565">Start the **Manage hardware stations** operation.</span></span>
12. <span data-ttu-id="b4553-566">单击**管理**。</span><span class="sxs-lookup"><span data-stu-id="b4553-566">Click **Manage**.</span></span>
13. <span data-ttu-id="b4553-567">在硬件工作站管理页中，设置用于打开硬件工作站的选项。</span><span class="sxs-lookup"><span data-stu-id="b4553-567">On the hardware station management page, set the option to turn on the hardware station.</span></span>
14. <span data-ttu-id="b4553-568">选择要使用的硬件工作站，然后单击**配对**。</span><span class="sxs-lookup"><span data-stu-id="b4553-568">Select the hardware station to use, and then click **Pair**.</span></span>
15. <span data-ttu-id="b4553-569">为 Modern POS 将使用的每个硬件工作站重复步骤 14。</span><span class="sxs-lookup"><span data-stu-id="b4553-569">Repeat step 14 for each hardware station that Modern POS will use.</span></span>
16. <span data-ttu-id="b4553-570">为所需全部硬件工作站配对之后，单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="b4553-570">After all the required hardware stations are paired, click **Close**.</span></span>
17. <span data-ttu-id="b4553-571">在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。</span><span class="sxs-lookup"><span data-stu-id="b4553-571">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4553-572">如果设备经常使用不同硬件工作站，建议将 Modern POS 配置为收银员开始收款过程时提示其选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-572">If devices often use different hardware stations, we recommend that you configure Modern POS to prompt cashiers to select a hardware station when they begin the tender process.</span></span> <span data-ttu-id="b4553-573">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="b4553-573">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="b4553-574">选择收银机，然后将**收款后即可选择**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b4553-574">Select the register, and then set the **Select upon tender** option to **Yes**.</span></span> <span data-ttu-id="b4553-575">使用 **1090** 配送计划将更改同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="b4553-575">Use the **1090** distribution schedule to sync changes to the channel database.</span></span>

## <a name="extensibility"></a><span data-ttu-id="b4553-576">可扩展性</span><span class="sxs-lookup"><span data-stu-id="b4553-576">Extensibility</span></span>

<span data-ttu-id="b4553-577">有关硬件工作站的可扩展性方案的信息，请参阅[硬件工作站可扩展性](dev-itpro/hardware-station-extensibility.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-577">For information about extensibility scenarios for the hardware station, see [Hardware Station extensibility](dev-itpro/hardware-station-extensibility.md).</span></span>

## <a name="security"></a><span data-ttu-id="b4553-578">安全性</span><span class="sxs-lookup"><span data-stu-id="b4553-578">Security</span></span>

<span data-ttu-id="b4553-579">根据当前安全标准，以下设置应用于生产环境：</span><span class="sxs-lookup"><span data-stu-id="b4553-579">According to current security standards, the following settings should be used in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-580">硬件工作站安装程序将在安装期间通过自助服务自动执行这些注册表编辑。</span><span class="sxs-lookup"><span data-stu-id="b4553-580">The hardware station installer will automatically make these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="b4553-581">应禁用安全套接字层 (SSL)。</span><span class="sxs-lookup"><span data-stu-id="b4553-581">Secure Sockets Layer (SSL) should be disabled.</span></span>
- <span data-ttu-id="b4553-582">应启用并使用传输层安全性 (TLS) 版本 1.2（或当前最高版本）。</span><span class="sxs-lookup"><span data-stu-id="b4553-582">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4553-583">默认情况下，已禁用 SSL 和除 TLS 1.2 外的所有 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="b4553-583">By default, SSL and all versions of TLS except TLS 1.2 are disabled.</span></span>

    <span data-ttu-id="b4553-584">要编辑或启用这些值，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="b4553-584">To edit or enable these values, follow these steps:</span></span>

    1. <span data-ttu-id="b4553-585">按 Windows 徽标键+R 打开**运行**窗口。</span><span class="sxs-lookup"><span data-stu-id="b4553-585">Press the Windows logo key+R to open a **Run** window.</span></span>
    2. <span data-ttu-id="b4553-586">在**打开**字段中，键入 **Regedit**，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="b4553-586">In the **Open** field, type **Regedit**, and then click **OK**.</span></span>
    3. <span data-ttu-id="b4553-587">如果显示**用户帐户控制**消息框，请单击**是**。</span><span class="sxs-lookup"><span data-stu-id="b4553-587">If a **User Account Control** message box appears, click **Yes**.</span></span>
    4. <span data-ttu-id="b4553-588">在**注册表编辑器**窗口中，导航至 **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**。</span><span class="sxs-lookup"><span data-stu-id="b4553-588">In the **Registry Editor** window, navigate to **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**.</span></span> <span data-ttu-id="b4553-589">以自动输入了以下键，以便仅允许 TLS 1.2。</span><span class="sxs-lookup"><span data-stu-id="b4553-589">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>

        - <span data-ttu-id="b4553-590">TLS 1.2Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="b4553-590">TLS 1.2Server:Enabled=1</span></span>
        - <span data-ttu-id="b4553-591">TLS 1.2Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="b4553-591">TLS 1.2Server:DisabledByDefault=0</span></span>
        - <span data-ttu-id="b4553-592">TLS 1.2Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="b4553-592">TLS 1.2Client:Enabled=1</span></span>
        - <span data-ttu-id="b4553-593">TLS 1.2Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="b4553-593">TLS 1.2Client:DisabledByDefault=0</span></span>
        - <span data-ttu-id="b4553-594">TLS 1.1Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-594">TLS 1.1Server:Enabled=0</span></span>
        - <span data-ttu-id="b4553-595">TLS 1.1Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-595">TLS 1.1Client:Enabled=0</span></span>
        - <span data-ttu-id="b4553-596">TLS 1.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-596">TLS 1.0Server:Enabled=0</span></span>
        - <span data-ttu-id="b4553-597">TLS 1.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-597">TLS 1.0Client:Enabled=0</span></span>
        - <span data-ttu-id="b4553-598">SSL 3.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-598">SSL 3.0Server:Enabled=0</span></span>
        - <span data-ttu-id="b4553-599">SSL 3.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-599">SSL 3.0Client:Enabled=0</span></span>
        - <span data-ttu-id="b4553-600">SSL 2.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-600">SSL 2.0Server:Enabled=0</span></span>
        - <span data-ttu-id="b4553-601">SSL 2.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="b4553-601">SSL 2.0Client:Enabled=0</span></span>

- <span data-ttu-id="b4553-602">除非已知的具体原因所需，否则不应开放其他任何网络端口。</span><span class="sxs-lookup"><span data-stu-id="b4553-602">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="b4553-603">必须禁用跨源资源共享，并且必须指定允许接受的源。</span><span class="sxs-lookup"><span data-stu-id="b4553-603">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="b4553-604">应仅使用可信证书机构获取将在运行硬件工作站的计算机上使用的证书。</span><span class="sxs-lookup"><span data-stu-id="b4553-604">Only trusted certificate authorities should be used to obtain certificates that will be used on computers that run the hardware station.</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-605">请务必仔细阅读 IIS 和 Payment Card Industry (PCI) 要求的安全指南。</span><span class="sxs-lookup"><span data-stu-id="b4553-605">It's very important that you review security guidelines for IIS and the Payment Card Industry (PCI) requirements.</span></span>

## <a name="peripheral-simulator"></a><span data-ttu-id="b4553-606">外围设备模拟器</span><span class="sxs-lookup"><span data-stu-id="b4553-606">Peripheral simulator</span></span>

<span data-ttu-id="b4553-607">有关信息，请参阅 [Retail 外设模拟器](dev-itpro/retail-peripheral-simulator.md)。</span><span class="sxs-lookup"><span data-stu-id="b4553-607">For information, see [Retail peripheral simulator](dev-itpro/retail-peripheral-simulator.md).</span></span>

## <a name="microsoft-tested-peripheral-devices"></a><span data-ttu-id="b4553-608">经过 Microsoft 测试的外设</span><span class="sxs-lookup"><span data-stu-id="b4553-608">Microsoft-tested peripheral devices</span></span>

### <a name="ipc-built-in-hardware-station"></a><span data-ttu-id="b4553-609">IPC（内置）硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-609">IPC (built-in) hardware station</span></span>

<span data-ttu-id="b4553-610">已通过 Modern POS for Windows 中的内置 IPC 硬件工作站测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-610">The following peripherals were tested by using the IPC hardware station that is built into Modern POS for Windows.</span></span>

#### <a name="printer"></a><span data-ttu-id="b4553-611">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-611">Printer</span></span>

| <span data-ttu-id="b4553-612">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-612">Manufacturer</span></span> | <span data-ttu-id="b4553-613">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-613">Model</span></span>    | <span data-ttu-id="b4553-614">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-614">Interface</span></span> | <span data-ttu-id="b4553-615">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-615">Comments</span></span>                |
|--------------|----------|-----------|-------------------------|
| <span data-ttu-id="b4553-616">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-616">Epson</span></span>        | <span data-ttu-id="b4553-617">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="b4553-617">Tm-T88IV</span></span> | <span data-ttu-id="b4553-618">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-618">OPOS</span></span>      |                         |
| <span data-ttu-id="b4553-619">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-619">Epson</span></span>        | <span data-ttu-id="b4553-620">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="b4553-620">TM-T88V</span></span>  | <span data-ttu-id="b4553-621">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-621">OPOS</span></span>      |                         |
| <span data-ttu-id="b4553-622">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-622">Star</span></span>         | <span data-ttu-id="b4553-623">TSP650II</span><span class="sxs-lookup"><span data-stu-id="b4553-623">TSP650II</span></span> | <span data-ttu-id="b4553-624">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-624">OPOS</span></span>      |                         |
| <span data-ttu-id="b4553-625">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-625">Star</span></span>         | <span data-ttu-id="b4553-626">TSP650II</span><span class="sxs-lookup"><span data-stu-id="b4553-626">TSP650II</span></span> | <span data-ttu-id="b4553-627">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-627">Custom</span></span>    | <span data-ttu-id="b4553-628">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="b4553-628">Connected via network</span></span>   |
| <span data-ttu-id="b4553-629">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-629">Star</span></span>         | <span data-ttu-id="b4553-630">mPOP</span><span class="sxs-lookup"><span data-stu-id="b4553-630">mPOP</span></span>     | <span data-ttu-id="b4553-631">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-631">OPOS</span></span>      | <span data-ttu-id="b4553-632">通过 Bluetooth 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-632">Connected via Bluetooth</span></span> |
| <span data-ttu-id="b4553-633">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-633">HP</span></span>           | <span data-ttu-id="b4553-634">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="b4553-634">F7M67AA</span></span>  | <span data-ttu-id="b4553-635">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-635">OPOS</span></span>      | <span data-ttu-id="b4553-636">带电 USB</span><span class="sxs-lookup"><span data-stu-id="b4553-636">Powered USB</span></span>             |

#### <a name="bar-code-scanner"></a><span data-ttu-id="b4553-637">条码扫描仪</span><span class="sxs-lookup"><span data-stu-id="b4553-637">Bar code scanner</span></span>

| <span data-ttu-id="b4553-638">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-638">Manufacturer</span></span>  | <span data-ttu-id="b4553-639">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-639">Model</span></span>         | <span data-ttu-id="b4553-640">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-640">Interface</span></span> | <span data-ttu-id="b4553-641">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-641">Comments</span></span> |
|---------------|---------------|-----------|----------|
| <span data-ttu-id="b4553-642">Motorola</span><span class="sxs-lookup"><span data-stu-id="b4553-642">Motorola</span></span>      | <span data-ttu-id="b4553-643">DS9208</span><span class="sxs-lookup"><span data-stu-id="b4553-643">DS9208</span></span>        | <span data-ttu-id="b4553-644">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-644">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-645">Honeywell</span><span class="sxs-lookup"><span data-stu-id="b4553-645">Honeywell</span></span>     | <span data-ttu-id="b4553-646">1900</span><span class="sxs-lookup"><span data-stu-id="b4553-646">1900</span></span>          | <span data-ttu-id="b4553-647">UWP</span><span class="sxs-lookup"><span data-stu-id="b4553-647">UWP</span></span>       |          |
| <span data-ttu-id="b4553-648">符号</span><span class="sxs-lookup"><span data-stu-id="b4553-648">Symbol</span></span>        | <span data-ttu-id="b4553-649">LS2208</span><span class="sxs-lookup"><span data-stu-id="b4553-649">LS2208</span></span>        | <span data-ttu-id="b4553-650">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-650">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-651">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="b4553-651">HP Integrated</span></span> | <span data-ttu-id="b4553-652">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="b4553-652">E1L07AA</span></span>       | <span data-ttu-id="b4553-653">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-653">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-654">Datalogic</span><span class="sxs-lookup"><span data-stu-id="b4553-654">Datalogic</span></span>     | <span data-ttu-id="b4553-655">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="b4553-655">Magellan 8400</span></span> | <span data-ttu-id="b4553-656">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-656">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="b4553-657">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="b4553-657">PIN pad</span></span>

| <span data-ttu-id="b4553-658">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-658">Manufacturer</span></span> | <span data-ttu-id="b4553-659">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-659">Model</span></span>  | <span data-ttu-id="b4553-660">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-660">Interface</span></span> | <span data-ttu-id="b4553-661">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-661">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="b4553-662">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-662">VeriFone</span></span>     | <span data-ttu-id="b4553-663">1000SE</span><span class="sxs-lookup"><span data-stu-id="b4553-663">1000SE</span></span> | <span data-ttu-id="b4553-664">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-664">OPOS</span></span>      | <span data-ttu-id="b4553-665">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="b4553-665">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="b4553-666">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-666">Payment terminal</span></span>

| <span data-ttu-id="b4553-667">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-667">Manufacturer</span></span> | <span data-ttu-id="b4553-668">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-668">Model</span></span> | <span data-ttu-id="b4553-669">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-669">Interface</span></span> | <span data-ttu-id="b4553-670">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-670">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b4553-671">Equinox</span><span class="sxs-lookup"><span data-stu-id="b4553-671">Equinox</span></span>      | <span data-ttu-id="b4553-672">L5300</span><span class="sxs-lookup"><span data-stu-id="b4553-672">L5300</span></span> | <span data-ttu-id="b4553-673">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-673">Custom</span></span>    | <span data-ttu-id="b4553-674">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="b4553-674">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="b4553-675">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-675">VeriFone</span></span>     | <span data-ttu-id="b4553-676">MX925</span><span class="sxs-lookup"><span data-stu-id="b4553-676">MX925</span></span> | <span data-ttu-id="b4553-677">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-677">Custom</span></span>    | <span data-ttu-id="b4553-678">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-678">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="b4553-679">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-679">VeriFone</span></span>     | <span data-ttu-id="b4553-680">MX915</span><span class="sxs-lookup"><span data-stu-id="b4553-680">MX915</span></span> | <span data-ttu-id="b4553-681">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-681">Custom</span></span>    | <span data-ttu-id="b4553-682">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-682">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="b4553-683">银箱</span><span class="sxs-lookup"><span data-stu-id="b4553-683">Cash drawer</span></span>

| <span data-ttu-id="b4553-684">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-684">Manufacturer</span></span> | <span data-ttu-id="b4553-685">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-685">Model</span></span>     | <span data-ttu-id="b4553-686">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-686">Interface</span></span> | <span data-ttu-id="b4553-687">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-687">Comments</span></span>                |
|--------------|-----------|-----------|-------------------------|
| <span data-ttu-id="b4553-688">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-688">Star</span></span>         | <span data-ttu-id="b4553-689">mPOP</span><span class="sxs-lookup"><span data-stu-id="b4553-689">mPOP</span></span>      | <span data-ttu-id="b4553-690">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-690">OPOS</span></span>      | <span data-ttu-id="b4553-691">通过 Bluetooth 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-691">Connected via Bluetooth</span></span> |
| <span data-ttu-id="b4553-692">APG</span><span class="sxs-lookup"><span data-stu-id="b4553-692">APG</span></span>          | <span data-ttu-id="b4553-693">Atwood</span><span class="sxs-lookup"><span data-stu-id="b4553-693">Atwood</span></span>    | <span data-ttu-id="b4553-694">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-694">Custom</span></span>    | <span data-ttu-id="b4553-695">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="b4553-695">Connected via network</span></span>   |
| <span data-ttu-id="b4553-696">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-696">Star</span></span>         | <span data-ttu-id="b4553-697">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="b4553-697">SMD2-1317</span></span> | <span data-ttu-id="b4553-698">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-698">OPOS</span></span>      |                         |
| <span data-ttu-id="b4553-699">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-699">HP</span></span>           | <span data-ttu-id="b4553-700">QT457AA</span><span class="sxs-lookup"><span data-stu-id="b4553-700">QT457AA</span></span>   | <span data-ttu-id="b4553-701">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-701">OPOS</span></span>      |                         |

#### <a name="line-display"></a><span data-ttu-id="b4553-702">行显示内容</span><span class="sxs-lookup"><span data-stu-id="b4553-702">Line display</span></span>

| <span data-ttu-id="b4553-703">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-703">Manufacturer</span></span>  | <span data-ttu-id="b4553-704">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-704">Model</span></span>   | <span data-ttu-id="b4553-705">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-705">Interface</span></span> | <span data-ttu-id="b4553-706">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-706">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="b4553-707">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="b4553-707">HP integrated</span></span> | <span data-ttu-id="b4553-708">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="b4553-708">G6U79AA</span></span> | <span data-ttu-id="b4553-709">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-709">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-710">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-710">Epson</span></span>         | <span data-ttu-id="b4553-711">M58DC</span><span class="sxs-lookup"><span data-stu-id="b4553-711">M58DC</span></span>   | <span data-ttu-id="b4553-712">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-712">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="b4553-713">签名捕获</span><span class="sxs-lookup"><span data-stu-id="b4553-713">Signature capture</span></span>

| <span data-ttu-id="b4553-714">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-714">Manufacturer</span></span> | <span data-ttu-id="b4553-715">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-715">Model</span></span>  | <span data-ttu-id="b4553-716">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-716">Interface</span></span> | <span data-ttu-id="b4553-717">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-717">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="b4553-718">Scriptel</span><span class="sxs-lookup"><span data-stu-id="b4553-718">Scriptel</span></span>     | <span data-ttu-id="b4553-719">ST1550</span><span class="sxs-lookup"><span data-stu-id="b4553-719">ST1550</span></span> | <span data-ttu-id="b4553-720">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-720">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="b4553-721">比例</span><span class="sxs-lookup"><span data-stu-id="b4553-721">Scale</span></span>

| <span data-ttu-id="b4553-722">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-722">Manufacturer</span></span> | <span data-ttu-id="b4553-723">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-723">Model</span></span>         | <span data-ttu-id="b4553-724">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-724">Interface</span></span> | <span data-ttu-id="b4553-725">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-725">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="b4553-726">Datalogic</span><span class="sxs-lookup"><span data-stu-id="b4553-726">Datalogic</span></span>    | <span data-ttu-id="b4553-727">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="b4553-727">Magellan 8400</span></span> | <span data-ttu-id="b4553-728">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-728">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="b4553-729">MSR</span><span class="sxs-lookup"><span data-stu-id="b4553-729">MSR</span></span>

| <span data-ttu-id="b4553-730">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-730">Manufacturer</span></span> | <span data-ttu-id="b4553-731">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-731">Model</span></span>       | <span data-ttu-id="b4553-732">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-732">Interface</span></span> | <span data-ttu-id="b4553-733">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-733">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="b4553-734">Magtek</span><span class="sxs-lookup"><span data-stu-id="b4553-734">Magtek</span></span>       | <span data-ttu-id="b4553-735">21073075</span><span class="sxs-lookup"><span data-stu-id="b4553-735">21073075</span></span>    | <span data-ttu-id="b4553-736">UWP</span><span class="sxs-lookup"><span data-stu-id="b4553-736">UWP</span></span>       |          |
| <span data-ttu-id="b4553-737">Magtek</span><span class="sxs-lookup"><span data-stu-id="b4553-737">Magtek</span></span>       | <span data-ttu-id="b4553-738">21073062</span><span class="sxs-lookup"><span data-stu-id="b4553-738">21073062</span></span>    | <span data-ttu-id="b4553-739">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-739">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-740">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-740">HP</span></span>           | <span data-ttu-id="b4553-741">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="b4553-741">IDRA-334133</span></span> | <span data-ttu-id="b4553-742">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-742">OPOS</span></span>      |          |

### <a name="dedicated-iis-hardware-station"></a><span data-ttu-id="b4553-743">专用 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-743">Dedicated IIS hardware station</span></span>

<span data-ttu-id="b4553-744">已使用专用（而非共享）IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-744">The following peripherals were tested by using a dedicated (not shared) IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

#### <a name="printer"></a><span data-ttu-id="b4553-745">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-745">Printer</span></span>

| <span data-ttu-id="b4553-746">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-746">Manufacturer</span></span> | <span data-ttu-id="b4553-747">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-747">Model</span></span>    | <span data-ttu-id="b4553-748">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-748">Interface</span></span> | <span data-ttu-id="b4553-749">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-749">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="b4553-750">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-750">Epson</span></span>        | <span data-ttu-id="b4553-751">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="b4553-751">Tm-T88IV</span></span> | <span data-ttu-id="b4553-752">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-752">OPOS</span></span>      |                           |
| <span data-ttu-id="b4553-753">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-753">Epson</span></span>        | <span data-ttu-id="b4553-754">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="b4553-754">TM-T88V</span></span>  | <span data-ttu-id="b4553-755">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-755">OPOS</span></span>      |                           |
| <span data-ttu-id="b4553-756">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-756">Star</span></span>         | <span data-ttu-id="b4553-757">TSP650II</span><span class="sxs-lookup"><span data-stu-id="b4553-757">TSP650II</span></span> | <span data-ttu-id="b4553-758">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-758">OPOS</span></span>      |                           |
| <span data-ttu-id="b4553-759">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-759">Star</span></span>         | <span data-ttu-id="b4553-760">TSP650II</span><span class="sxs-lookup"><span data-stu-id="b4553-760">TSP650II</span></span> | <span data-ttu-id="b4553-761">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-761">Custom</span></span>    | <span data-ttu-id="b4553-762">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="b4553-762">Connected via network</span></span>     |
| <span data-ttu-id="b4553-763">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-763">Star</span></span>         | <span data-ttu-id="b4553-764">TSP100</span><span class="sxs-lookup"><span data-stu-id="b4553-764">TSP100</span></span>   | <span data-ttu-id="b4553-765">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-765">OPOS</span></span>      | <span data-ttu-id="b4553-766">需要 TSP650II 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-766">Requires TSP650II drivers</span></span> |
| <span data-ttu-id="b4553-767">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-767">HP</span></span>           | <span data-ttu-id="b4553-768">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="b4553-768">F7M67AA</span></span>  | <span data-ttu-id="b4553-769">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-769">OPOS</span></span>      | <span data-ttu-id="b4553-770">带电 USB</span><span class="sxs-lookup"><span data-stu-id="b4553-770">Powered USB</span></span>               |

#### <a name="bar-code-scanner"></a><span data-ttu-id="b4553-771">条码扫描仪</span><span class="sxs-lookup"><span data-stu-id="b4553-771">Bar code scanner</span></span>

| <span data-ttu-id="b4553-772">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-772">Manufacturer</span></span>  | <span data-ttu-id="b4553-773">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-773">Model</span></span>   | <span data-ttu-id="b4553-774">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-774">Interface</span></span> | <span data-ttu-id="b4553-775">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-775">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="b4553-776">Motorola</span><span class="sxs-lookup"><span data-stu-id="b4553-776">Motorola</span></span>      | <span data-ttu-id="b4553-777">DS9208</span><span class="sxs-lookup"><span data-stu-id="b4553-777">DS9208</span></span>  | <span data-ttu-id="b4553-778">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-778">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-779">符号</span><span class="sxs-lookup"><span data-stu-id="b4553-779">Symbol</span></span>        | <span data-ttu-id="b4553-780">LS2208</span><span class="sxs-lookup"><span data-stu-id="b4553-780">LS2208</span></span>  | <span data-ttu-id="b4553-781">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-781">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-782">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="b4553-782">HP Integrated</span></span> | <span data-ttu-id="b4553-783">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="b4553-783">E1L07AA</span></span> | <span data-ttu-id="b4553-784">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-784">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="b4553-785">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="b4553-785">PIN pad</span></span>

| <span data-ttu-id="b4553-786">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-786">Manufacturer</span></span> | <span data-ttu-id="b4553-787">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-787">Model</span></span>  | <span data-ttu-id="b4553-788">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-788">Interface</span></span> | <span data-ttu-id="b4553-789">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-789">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="b4553-790">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-790">VeriFone</span></span>     | <span data-ttu-id="b4553-791">1000SE</span><span class="sxs-lookup"><span data-stu-id="b4553-791">1000SE</span></span> | <span data-ttu-id="b4553-792">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-792">OPOS</span></span>      | <span data-ttu-id="b4553-793">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="b4553-793">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="b4553-794">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-794">Payment terminal</span></span>

| <span data-ttu-id="b4553-795">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-795">Manufacturer</span></span> | <span data-ttu-id="b4553-796">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-796">Model</span></span> | <span data-ttu-id="b4553-797">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-797">Interface</span></span> | <span data-ttu-id="b4553-798">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-798">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b4553-799">Equinox</span><span class="sxs-lookup"><span data-stu-id="b4553-799">Equinox</span></span>      | <span data-ttu-id="b4553-800">L5300</span><span class="sxs-lookup"><span data-stu-id="b4553-800">L5300</span></span> | <span data-ttu-id="b4553-801">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-801">Custom</span></span>    | <span data-ttu-id="b4553-802">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="b4553-802">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="b4553-803">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-803">VeriFone</span></span>     | <span data-ttu-id="b4553-804">MX925</span><span class="sxs-lookup"><span data-stu-id="b4553-804">MX925</span></span> | <span data-ttu-id="b4553-805">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-805">Custom</span></span>    | <span data-ttu-id="b4553-806">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-806">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="b4553-807">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-807">VeriFone</span></span>     | <span data-ttu-id="b4553-808">MX915</span><span class="sxs-lookup"><span data-stu-id="b4553-808">MX915</span></span> | <span data-ttu-id="b4553-809">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-809">Custom</span></span>    | <span data-ttu-id="b4553-810">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-810">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="b4553-811">银箱</span><span class="sxs-lookup"><span data-stu-id="b4553-811">Cash drawer</span></span>

| <span data-ttu-id="b4553-812">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-812">Manufacturer</span></span> | <span data-ttu-id="b4553-813">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-813">Model</span></span>     | <span data-ttu-id="b4553-814">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-814">Interface</span></span> | <span data-ttu-id="b4553-815">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-815">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="b4553-816">APG</span><span class="sxs-lookup"><span data-stu-id="b4553-816">APG</span></span>          | <span data-ttu-id="b4553-817">Atwood</span><span class="sxs-lookup"><span data-stu-id="b4553-817">Atwood</span></span>    | <span data-ttu-id="b4553-818">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-818">Custom</span></span>    | <span data-ttu-id="b4553-819">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="b4553-819">Connected via network</span></span> |
| <span data-ttu-id="b4553-820">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-820">Star</span></span>         | <span data-ttu-id="b4553-821">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="b4553-821">SMD2-1317</span></span> | <span data-ttu-id="b4553-822">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-822">OPOS</span></span>      |                       |
| <span data-ttu-id="b4553-823">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-823">HP</span></span>           | <span data-ttu-id="b4553-824">QT457AA</span><span class="sxs-lookup"><span data-stu-id="b4553-824">QT457AA</span></span>   | <span data-ttu-id="b4553-825">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-825">OPOS</span></span>      |                       |

#### <a name="line-display"></a><span data-ttu-id="b4553-826">行显示内容</span><span class="sxs-lookup"><span data-stu-id="b4553-826">Line display</span></span>

| <span data-ttu-id="b4553-827">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-827">Manufacturer</span></span>  | <span data-ttu-id="b4553-828">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-828">Model</span></span>   | <span data-ttu-id="b4553-829">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-829">Interface</span></span> | <span data-ttu-id="b4553-830">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-830">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="b4553-831">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="b4553-831">HP integrated</span></span> | <span data-ttu-id="b4553-832">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="b4553-832">G6U79AA</span></span> | <span data-ttu-id="b4553-833">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-833">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-834">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-834">Epson</span></span>         | <span data-ttu-id="b4553-835">M58DC</span><span class="sxs-lookup"><span data-stu-id="b4553-835">M58DC</span></span>   | <span data-ttu-id="b4553-836">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-836">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="b4553-837">签名捕获</span><span class="sxs-lookup"><span data-stu-id="b4553-837">Signature capture</span></span>

| <span data-ttu-id="b4553-838">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-838">Manufacturer</span></span> | <span data-ttu-id="b4553-839">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-839">Model</span></span>  | <span data-ttu-id="b4553-840">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-840">Interface</span></span> | <span data-ttu-id="b4553-841">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-841">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="b4553-842">Scriptel</span><span class="sxs-lookup"><span data-stu-id="b4553-842">Scriptel</span></span>     | <span data-ttu-id="b4553-843">ST1550</span><span class="sxs-lookup"><span data-stu-id="b4553-843">ST1550</span></span> | <span data-ttu-id="b4553-844">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-844">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="b4553-845">比例</span><span class="sxs-lookup"><span data-stu-id="b4553-845">Scale</span></span>

| <span data-ttu-id="b4553-846">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-846">Manufacturer</span></span> | <span data-ttu-id="b4553-847">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-847">Model</span></span>         | <span data-ttu-id="b4553-848">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-848">Interface</span></span> | <span data-ttu-id="b4553-849">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-849">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="b4553-850">Datalogic</span><span class="sxs-lookup"><span data-stu-id="b4553-850">Datalogic</span></span>    | <span data-ttu-id="b4553-851">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="b4553-851">Magellan 8400</span></span> | <span data-ttu-id="b4553-852">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-852">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="b4553-853">MSR</span><span class="sxs-lookup"><span data-stu-id="b4553-853">MSR</span></span>

| <span data-ttu-id="b4553-854">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-854">Manufacturer</span></span> | <span data-ttu-id="b4553-855">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-855">Model</span></span>       | <span data-ttu-id="b4553-856">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-856">Interface</span></span> | <span data-ttu-id="b4553-857">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-857">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="b4553-858">Magtek</span><span class="sxs-lookup"><span data-stu-id="b4553-858">Magtek</span></span>       | <span data-ttu-id="b4553-859">21073075</span><span class="sxs-lookup"><span data-stu-id="b4553-859">21073075</span></span>    | <span data-ttu-id="b4553-860">UWP</span><span class="sxs-lookup"><span data-stu-id="b4553-860">UWP</span></span>       |          |
| <span data-ttu-id="b4553-861">Magtek</span><span class="sxs-lookup"><span data-stu-id="b4553-861">Magtek</span></span>       | <span data-ttu-id="b4553-862">21073062</span><span class="sxs-lookup"><span data-stu-id="b4553-862">21073062</span></span>    | <span data-ttu-id="b4553-863">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-863">OPOS</span></span>      |          |
| <span data-ttu-id="b4553-864">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-864">HP</span></span>           | <span data-ttu-id="b4553-865">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="b4553-865">IDRA-334133</span></span> | <span data-ttu-id="b4553-866">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-866">OPOS</span></span>      |          |

### <a name="shared-iis-hardware-station"></a><span data-ttu-id="b4553-867">共享 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="b4553-867">Shared IIS hardware station</span></span>

<span data-ttu-id="b4553-868">已使用共享 IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-868">The following peripherals were tested by using a shared IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

> [!NOTE]
> <span data-ttu-id="b4553-869">仅支持打印机、付款终端和银箱。</span><span class="sxs-lookup"><span data-stu-id="b4553-869">Only a printer, payment terminal, and cash drawer are supported.</span></span>

#### <a name="printer"></a><span data-ttu-id="b4553-870">打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-870">Printer</span></span>

| <span data-ttu-id="b4553-871">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-871">Manufacturer</span></span> | <span data-ttu-id="b4553-872">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-872">Model</span></span>    | <span data-ttu-id="b4553-873">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-873">Interface</span></span> | <span data-ttu-id="b4553-874">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-874">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="b4553-875">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-875">Epson</span></span>        | <span data-ttu-id="b4553-876">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="b4553-876">Tm-T88IV</span></span> | <span data-ttu-id="b4553-877">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-877">OPOS</span></span>      |                           |
| <span data-ttu-id="b4553-878">Epson</span><span class="sxs-lookup"><span data-stu-id="b4553-878">Epson</span></span>        | <span data-ttu-id="b4553-879">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="b4553-879">TM-T88V</span></span>  | <span data-ttu-id="b4553-880">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-880">OPOS</span></span>      |                           |
| <span data-ttu-id="b4553-881">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-881">Star</span></span>         | <span data-ttu-id="b4553-882">TSP650II</span><span class="sxs-lookup"><span data-stu-id="b4553-882">TSP650II</span></span> | <span data-ttu-id="b4553-883">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-883">OPOS</span></span>      |                           |
| <span data-ttu-id="b4553-884">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-884">Star</span></span>         | <span data-ttu-id="b4553-885">TSP650II</span><span class="sxs-lookup"><span data-stu-id="b4553-885">TSP650II</span></span> | <span data-ttu-id="b4553-886">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-886">Custom</span></span>    | <span data-ttu-id="b4553-887">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="b4553-887">Connected via network</span></span>     |
| <span data-ttu-id="b4553-888">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-888">Star</span></span>         | <span data-ttu-id="b4553-889">TSP100</span><span class="sxs-lookup"><span data-stu-id="b4553-889">TSP100</span></span>   | <span data-ttu-id="b4553-890">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-890">OPOS</span></span>      | <span data-ttu-id="b4553-891">需要 TSP650II 驱动程序</span><span class="sxs-lookup"><span data-stu-id="b4553-891">Requires TSP650II drivers</span></span> |
| <span data-ttu-id="b4553-892">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-892">HP</span></span>           | <span data-ttu-id="b4553-893">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="b4553-893">F7M67AA</span></span>  | <span data-ttu-id="b4553-894">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-894">OPOS</span></span>      | <span data-ttu-id="b4553-895">带电 USB</span><span class="sxs-lookup"><span data-stu-id="b4553-895">Powered USB</span></span>               |

#### <a name="payment-terminal"></a><span data-ttu-id="b4553-896">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-896">Payment terminal</span></span>

| <span data-ttu-id="b4553-897">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-897">Manufacturer</span></span> | <span data-ttu-id="b4553-898">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-898">Model</span></span> | <span data-ttu-id="b4553-899">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-899">Interface</span></span> | <span data-ttu-id="b4553-900">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-900">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b4553-901">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-901">VeriFone</span></span>     | <span data-ttu-id="b4553-902">MX925</span><span class="sxs-lookup"><span data-stu-id="b4553-902">MX925</span></span> | <span data-ttu-id="b4553-903">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-903">Custom</span></span>    | <span data-ttu-id="b4553-904">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-904">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="b4553-905">VeriFone</span><span class="sxs-lookup"><span data-stu-id="b4553-905">VeriFone</span></span>     | <span data-ttu-id="b4553-906">MX915</span><span class="sxs-lookup"><span data-stu-id="b4553-906">MX915</span></span> | <span data-ttu-id="b4553-907">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-907">Custom</span></span>    | <span data-ttu-id="b4553-908">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="b4553-908">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="b4553-909">银箱</span><span class="sxs-lookup"><span data-stu-id="b4553-909">Cash drawer</span></span>

| <span data-ttu-id="b4553-910">制造商</span><span class="sxs-lookup"><span data-stu-id="b4553-910">Manufacturer</span></span> | <span data-ttu-id="b4553-911">型号</span><span class="sxs-lookup"><span data-stu-id="b4553-911">Model</span></span>     | <span data-ttu-id="b4553-912">接口</span><span class="sxs-lookup"><span data-stu-id="b4553-912">Interface</span></span> | <span data-ttu-id="b4553-913">评论</span><span class="sxs-lookup"><span data-stu-id="b4553-913">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="b4553-914">APG</span><span class="sxs-lookup"><span data-stu-id="b4553-914">APG</span></span>          | <span data-ttu-id="b4553-915">Atwood</span><span class="sxs-lookup"><span data-stu-id="b4553-915">Atwood</span></span>    | <span data-ttu-id="b4553-916">自定义</span><span class="sxs-lookup"><span data-stu-id="b4553-916">Custom</span></span>    | <span data-ttu-id="b4553-917">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="b4553-917">Connected via network</span></span> |
| <span data-ttu-id="b4553-918">Star</span><span class="sxs-lookup"><span data-stu-id="b4553-918">Star</span></span>         | <span data-ttu-id="b4553-919">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="b4553-919">SMD2-1317</span></span> | <span data-ttu-id="b4553-920">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-920">OPOS</span></span>      |                       |
| <span data-ttu-id="b4553-921">HP</span><span class="sxs-lookup"><span data-stu-id="b4553-921">HP</span></span>           | <span data-ttu-id="b4553-922">QT457AA</span><span class="sxs-lookup"><span data-stu-id="b4553-922">QT457AA</span></span>   | <span data-ttu-id="b4553-923">OPOS</span><span class="sxs-lookup"><span data-stu-id="b4553-923">OPOS</span></span>      |                       |

## <a name="troubleshooting"></a><span data-ttu-id="b4553-924">疑难解答</span><span class="sxs-lookup"><span data-stu-id="b4553-924">Troubleshooting</span></span>

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="b4553-925">Modern POS 可以在其列表中检测硬件工作站以进行选择，但是不能完成配对。</span><span class="sxs-lookup"><span data-stu-id="b4553-925">Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="b4553-926">**解决方案：** 验证以下潜在故障点列表：</span><span class="sxs-lookup"><span data-stu-id="b4553-926">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="b4553-927">运行 Modern POS 的计算机信任运行硬件工作站的计算机上使用的证书。</span><span class="sxs-lookup"><span data-stu-id="b4553-927">The computer that is running Modern POS trusts the certificate that is used on the computer that runs the hardware station.</span></span>

    - <span data-ttu-id="b4553-928">若要验证此设置，请转至以下 URL：`https://<Computer Name>:<Port Number>/HardwareStation/ping`。</span><span class="sxs-lookup"><span data-stu-id="b4553-928">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`.</span></span>
    - <span data-ttu-id="b4553-929">此 URL 使用 ping 验证计算机是否可访问，而浏览器则指示证书是否可信。</span><span class="sxs-lookup"><span data-stu-id="b4553-929">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="b4553-930">（例如，在 Internet Explorer 中，地址栏中显示锁图标。</span><span class="sxs-lookup"><span data-stu-id="b4553-930">(For example, in Internet Explorer, a lock icon appears in the address bar.</span></span> <span data-ttu-id="b4553-931">当您单击此图标时，Internet Explorer 验证证书当前是否可信。</span><span class="sxs-lookup"><span data-stu-id="b4553-931">When you click this icon, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="b4553-932">您可以通过查看显示的证书的详细信息，将证书安装到本地计算机上。）</span><span class="sxs-lookup"><span data-stu-id="b4553-932">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="b4553-933">在运行硬件工作站的计算机上，防火墙中将打开硬件工作站使用的端口。</span><span class="sxs-lookup"><span data-stu-id="b4553-933">On the computer that runs the hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="b4553-934">硬件工作站已通过硬件工作站安装程序结束时运行的安装商家信息工具正确安装了商家帐户信息。</span><span class="sxs-lookup"><span data-stu-id="b4553-934">The hardware station has correctly installed merchant account information through the Install merchant information tool that runs at the end of the hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="b4553-935">Modern POS 不能在其列表中检测到硬件工作站来进行选择。</span><span class="sxs-lookup"><span data-stu-id="b4553-935">Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="b4553-936">**解决方案：** 以下因素之一可能导致此问题：</span><span class="sxs-lookup"><span data-stu-id="b4553-936">**Solution:** Either of the following factors can cause this issue:</span></span>

- <span data-ttu-id="b4553-937">硬件工作站尚未在总部正确设置。</span><span class="sxs-lookup"><span data-stu-id="b4553-937">The hardware station hasn't been set up correctly in headquarters.</span></span> <span data-ttu-id="b4553-938">使用本主题前面的步骤验证是否正确输入了硬件工作站配置文件和硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="b4553-938">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="b4553-939">尚未运行作业以更新渠道配置。</span><span class="sxs-lookup"><span data-stu-id="b4553-939">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="b4553-940">在这种情况下，请运行作业 1070 以配置渠道。</span><span class="sxs-lookup"><span data-stu-id="b4553-940">In this case, run the 1070 job for channel configuration.</span></span>

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a><span data-ttu-id="b4553-941">Modern POS 不体现新的银箱设置</span><span class="sxs-lookup"><span data-stu-id="b4553-941">Modern POS doesn't reflect new cash drawer settings</span></span>

<span data-ttu-id="b4553-942">**解决方案：** 关闭当前批处理。</span><span class="sxs-lookup"><span data-stu-id="b4553-942">**Solution:** Close the current batch.</span></span> <span data-ttu-id="b4553-943">关闭当前批处理之前，不会将对银箱的更改更新到 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-943">Changes to the cash drawer aren't updated to Modern POS until the current batch is closed.</span></span>

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a><span data-ttu-id="b4553-944">Modern POS 报告零售外设有问题</span><span class="sxs-lookup"><span data-stu-id="b4553-944">Modern POS is reporting an issue with a retail peripheral</span></span>

<span data-ttu-id="b4553-945">**解决方案：** 下面是此问题的一些典型原因：</span><span class="sxs-lookup"><span data-stu-id="b4553-945">**Solution:** Here are some typical causes of this issue:</span></span>

- <span data-ttu-id="b4553-946">确保关闭了其他设备驱动程序配置实用程序。</span><span class="sxs-lookup"><span data-stu-id="b4553-946">Make sure that other device driver configuration utilities are closed.</span></span> <span data-ttu-id="b4553-947">如果打开了这些实用程序，可能会阻止 Modern POS 或硬件工作站声明设备。</span><span class="sxs-lookup"><span data-stu-id="b4553-947">If these utilities are open, they might prevent Modern POS or the hardware station from claiming the device.</span></span>
- <span data-ttu-id="b4553-948">如果将零售外设与多台 POS 设备共享，请确保其属于以下类别之一：</span><span class="sxs-lookup"><span data-stu-id="b4553-948">If the retail peripheral is shared with multiple POS devices, make sure that it belongs to one of the following categories:</span></span>

    - <span data-ttu-id="b4553-949">银箱</span><span class="sxs-lookup"><span data-stu-id="b4553-949">Cash drawer</span></span>
    - <span data-ttu-id="b4553-950">收据打印机</span><span class="sxs-lookup"><span data-stu-id="b4553-950">Receipt printer</span></span>
    - <span data-ttu-id="b4553-951">付款终端</span><span class="sxs-lookup"><span data-stu-id="b4553-951">Payment terminal</span></span>

    <span data-ttu-id="b4553-952">如果外设不属于这些类别之一，则硬件工作站的设计不支持在多台 POS 设备之间共享该外设。</span><span class="sxs-lookup"><span data-stu-id="b4553-952">If the peripheral doesn't belong to one of these categories, the hardware station isn't designed to enable the peripheral to be shared among multiple POS devices.</span></span>

- <span data-ttu-id="b4553-953">有时，设备驱动程序可能导致公共控件对象 (CCO) 停止正常工作。</span><span class="sxs-lookup"><span data-stu-id="b4553-953">Sometimes, device drivers can cause the common control objects (CCOs) to stop working correctly.</span></span> <span data-ttu-id="b4553-954">如果最近安装了设备，但是该设备无法正常工作，或您发现了其他问题，通常可以通过重新安装 CCO 来解决问题。</span><span class="sxs-lookup"><span data-stu-id="b4553-954">If a device has recently been installed, but it isn't working properly or you notice other issues, you can often resolve the issue by reinstalling the CCOs.</span></span> <span data-ttu-id="b4553-955">若要下载 CCO，请访问 <http://monroecs.com/oposccos_current.htm>。</span><span class="sxs-lookup"><span data-stu-id="b4553-955">To download the CCOs, visit <http://monroecs.com/oposccos_current.htm>.</span></span>
- <span data-ttu-id="b4553-956">如果在测试或故障排除期间频繁更改外设，可能必须重置 IIS，而不是等待高速缓存自行刷新。</span><span class="sxs-lookup"><span data-stu-id="b4553-956">If you make frequent peripheral changes during testing or troubleshooting, you might have to reset IIS instead of waiting for the cache to refresh itself.</span></span> <span data-ttu-id="b4553-957">若要重置 IIS，请执行以下步骤:</span><span class="sxs-lookup"><span data-stu-id="b4553-957">To reset IIS, follow these steps:</span></span>

    1. <span data-ttu-id="b4553-958">在**开始**菜单中键入 **CMD**。</span><span class="sxs-lookup"><span data-stu-id="b4553-958">From the **Start** menu, type **CMD**.</span></span>
    2. <span data-ttu-id="b4553-959">在搜索结果中，右键单击**命令提示符**，然后单击**以管理员身份运行**。</span><span class="sxs-lookup"><span data-stu-id="b4553-959">In the search results, right-click **Command prompt**, and then click **Run as administrator**.</span></span>
    3. <span data-ttu-id="b4553-960">在**命令提示符**窗口中，键入 **iisreset /Restart**，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="b4553-960">In the **Command prompt** window, type **iisreset /Restart** and then press Enter.</span></span>
    4. <span data-ttu-id="b4553-961">IIS 重新启动后，重新启动 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-961">After IIS has restarted, restart Modern POS.</span></span>

- <span data-ttu-id="b4553-962">频繁更改外设时，如果也频繁启动和退出 POS 客户端，则上一个 POS 会话的 dllhost 进程可能干扰当前会话。</span><span class="sxs-lookup"><span data-stu-id="b4553-962">While you're making frequent changes to peripheral devices, if you also frequently start and exit the POS client, the dllhost process from a previous POS session can interfere with the current session.</span></span> <span data-ttu-id="b4553-963">在这种情况下，关闭正在管理上一个会话的动态链接库 (DLL) 主机之前，设备可能不可用。</span><span class="sxs-lookup"><span data-stu-id="b4553-963">In this case, a device might not be usable until you close the dynamic-link library (DLL) host that is managing the previous session.</span></span> <span data-ttu-id="b4553-964">若要关闭 DLL 主机，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="b4553-964">To close the DLL host, follow these steps:</span></span>

    1. <span data-ttu-id="b4553-965">在**开始**菜单中键入**任务管理器**。</span><span class="sxs-lookup"><span data-stu-id="b4553-965">From the **Start** menu, type **Task manager**.</span></span>
    2. <span data-ttu-id="b4553-966">在搜索结果中，单击**任务管理器**。</span><span class="sxs-lookup"><span data-stu-id="b4553-966">In the search results, click **Task manager**.</span></span>
    3. <span data-ttu-id="b4553-967">在“任务管理器”中的**详细信息**选项卡上，单击带有**名称**标签的列标题，按名称以字母顺序为表排序。</span><span class="sxs-lookup"><span data-stu-id="b4553-967">In Task manager, on the **Details** tab, click the column header that is labeled **Name** to sort the table alphabetically by name.</span></span>
    4. <span data-ttu-id="b4553-968">向下滚动，直到找到 dllhost.exe。</span><span class="sxs-lookup"><span data-stu-id="b4553-968">Scroll down until you find dllhost.exe.</span></span>
    5. <span data-ttu-id="b4553-969">选择每个 DLL 主机，然后单击**结束任何**。</span><span class="sxs-lookup"><span data-stu-id="b4553-969">Select each DLL host, and then click **End task**.</span></span>
    6. <span data-ttu-id="b4553-970">关闭 DLL 主机后，重新启动 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="b4553-970">After the DLL hosts have been closed, restart Modern POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4553-971">其他资源</span><span class="sxs-lookup"><span data-stu-id="b4553-971">Additional resources</span></span>

[<span data-ttu-id="b4553-972">零售外围设备模拟器</span><span class="sxs-lookup"><span data-stu-id="b4553-972">Retail peripheral simulator</span></span>](dev-itpro/retail-peripheral-simulator.md)

