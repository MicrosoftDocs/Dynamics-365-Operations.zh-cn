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
ms.openlocfilehash: 9aba1dabe3b2304c1f0dfd449982af1d4bc15d6b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742625"
---
# <a name="retail-peripherals"></a><span data-ttu-id="1a669-103">零售外设</span><span class="sxs-lookup"><span data-stu-id="1a669-103">Retail peripherals</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a669-104">此主题介绍与零售外设有关的概念。</span><span class="sxs-lookup"><span data-stu-id="1a669-104">This topic explains the concepts that are related to retail peripherals.</span></span> <span data-ttu-id="1a669-105">它描述可用于将外设连接到销售点 (POS) 的各种方法，以及负责管理与 POS 之间的连接的组件。</span><span class="sxs-lookup"><span data-stu-id="1a669-105">It describes the various ways that peripherals can be connected to the point of sale (POS) and the components that are responsible for managing the connection with the POS.</span></span>

## <a name="concepts"></a><span data-ttu-id="1a669-106">概念</span><span class="sxs-lookup"><span data-stu-id="1a669-106">Concepts</span></span>

### <a name="pos-registers"></a><span data-ttu-id="1a669-107">POS 收银机</span><span class="sxs-lookup"><span data-stu-id="1a669-107">POS registers</span></span>

<span data-ttu-id="1a669-108">导航：单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="1a669-108">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="1a669-109">销售点 (POS) 收银机是用来定义特定 POS 实例的特征的实体。</span><span class="sxs-lookup"><span data-stu-id="1a669-109">The point of sale (POS) register is an entity that is used to define the characteristics of a specific instance of the POS.</span></span> <span data-ttu-id="1a669-110">这些特征包括硬件配置文件或设置，它们将被零售外设用于收银机、收银机映射到的商店，以及登录该收银机的用户的视觉体验。</span><span class="sxs-lookup"><span data-stu-id="1a669-110">These characteristics include the hardware profile or setup for retail peripherals that will be used at the register, the store that the register is mapped to, and the visual experience for the user who signs in to that register.</span></span>

### <a name="devices"></a><span data-ttu-id="1a669-111">设备</span><span class="sxs-lookup"><span data-stu-id="1a669-111">Devices</span></span>

<span data-ttu-id="1a669-112">导航：单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **设备**。</span><span class="sxs-lookup"><span data-stu-id="1a669-112">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**.</span></span> <span data-ttu-id="1a669-113">设备是表示映射到 POS 收银机的设备的物理实例的实体。</span><span class="sxs-lookup"><span data-stu-id="1a669-113">A device is an entity that represents a physical instance of a device that is mapped to a POS register.</span></span> <span data-ttu-id="1a669-114">当创建一个设备时，它被映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="1a669-114">When a device is created, it's mapped to a POS register.</span></span> <span data-ttu-id="1a669-115">设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。</span><span class="sxs-lookup"><span data-stu-id="1a669-115">The device entity tracks information about when a POS register is activated, the type of client that is being used, and the application package that has been deployed to a specific device.</span></span> <span data-ttu-id="1a669-116">设备可以映射到以下应用类型：Retail Modern POS、Retail Cloud POS、Retail Modern POS – Windows Phone、Retail Modern POS – Android 和 Retail Modern POS – iOS。</span><span class="sxs-lookup"><span data-stu-id="1a669-116">Devices can be mapped to the following application types: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android, and Retail Modern POS – iOS.</span></span>

### <a name="retail-modern-pos"></a><span data-ttu-id="1a669-117">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="1a669-117">Retail Modern POS</span></span>

<span data-ttu-id="1a669-118">Modern POS 是适用于 Microsoft Windows 的 POS 程序。</span><span class="sxs-lookup"><span data-stu-id="1a669-118">Modern POS is the POS program for Microsoft Windows.</span></span> <span data-ttu-id="1a669-119">它可以部署到 Windows 10 操作系统 (OS) 上。</span><span class="sxs-lookup"><span data-stu-id="1a669-119">It can be deployed on Windows 10 operating systems (OSs).</span></span>

### <a name="cloud-pos"></a><span data-ttu-id="1a669-120">云 POS</span><span class="sxs-lookup"><span data-stu-id="1a669-120">Cloud POS</span></span>

<span data-ttu-id="1a669-121">Cloud POS 是基于浏览器且可以通过 Web 浏览器访问的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="1a669-121">Cloud POS is a browser-based version of the Modern POS program that can be accessed in a web browser.</span></span>

### <a name="modern-pos-for-ios"></a><span data-ttu-id="1a669-122">Modern POS for iOS</span><span class="sxs-lookup"><span data-stu-id="1a669-122">Modern POS for iOS</span></span>

<span data-ttu-id="1a669-123">Modern POS for iOS 是基于 iOS 且可部署到 iOS 设备上的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="1a669-123">Modern POS for iOS is an iOS-based version of the Modern POS program that can be deployed on iOS devices.</span></span>

### <a name="modern-pos-for-android"></a><span data-ttu-id="1a669-124">Modern POS for Android</span><span class="sxs-lookup"><span data-stu-id="1a669-124">Modern POS for Android</span></span>

<span data-ttu-id="1a669-125">Modern POS for Android 是基于 Android 且可部署到 Android 设备上的 Modern POS 程序版本。</span><span class="sxs-lookup"><span data-stu-id="1a669-125">Modern POS for Android is an Android-based version of the Modern POS program that can be deployed on Android devices.</span></span>

### <a name="pos-peripherals"></a><span data-ttu-id="1a669-126">POS 外设</span><span class="sxs-lookup"><span data-stu-id="1a669-126">POS peripherals</span></span>

<span data-ttu-id="1a669-127">POS 外设是为满足 POS 功能而明确支持的设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-127">POS peripherals are devices that are explicitly supported for POS functions.</span></span> <span data-ttu-id="1a669-128">这些外设通常划分为特定类。</span><span class="sxs-lookup"><span data-stu-id="1a669-128">These peripherals are typically divided into specific classes.</span></span> <span data-ttu-id="1a669-129">有关这些类的详细信息，请参阅此主题的“设备分类”部分。</span><span class="sxs-lookup"><span data-stu-id="1a669-129">For more information about these classes, see the "Device classes" section of this topic.</span></span>

### <a name="hardware-station"></a><span data-ttu-id="1a669-130">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="1a669-130">Hardware station</span></span>

<span data-ttu-id="1a669-131">导航：单击**零售** &gt; **渠道** &gt; **零售商店** &gt; **所有零售商店**。</span><span class="sxs-lookup"><span data-stu-id="1a669-131">Navigation: Click **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span> <span data-ttu-id="1a669-132">选择一个商店，然后单击**硬件工作站**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="1a669-132">Select a store, and then click the **Hardware stations** FastTab.</span></span> <span data-ttu-id="1a669-133">**硬件工作站**设置是一种基于渠道的设置，用于定义将部署零售外设逻辑的实例。</span><span class="sxs-lookup"><span data-stu-id="1a669-133">The **Hardware station** setting is a channel-level setting that is used to define instances where the retail peripheral logic will be deployed.</span></span> <span data-ttu-id="1a669-134">渠道级别的此设置用于确定硬件工作站的特征。</span><span class="sxs-lookup"><span data-stu-id="1a669-134">This setting at the channel level is used to determine characteristics of the hardware station.</span></span> <span data-ttu-id="1a669-135">还用于列出指定商店中可用于 Modern POS 实例的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-135">It's also used to list hardware stations that are available for a Modern POS instance in a given store.</span></span> <span data-ttu-id="1a669-136">硬件工作站内置在适用于 Windows 的 Modern POS 程序内。</span><span class="sxs-lookup"><span data-stu-id="1a669-136">The hardware station is built into the Modern POS program for Windows.</span></span> <span data-ttu-id="1a669-137">硬件工作站也可以作为单机 Microsoft Internet Information Services (IIS) 程序独立部署。</span><span class="sxs-lookup"><span data-stu-id="1a669-137">The hardware station can also be deployed independently as a stand-alone Microsoft Internet Information Services (IIS) program.</span></span> <span data-ttu-id="1a669-138">在这种情况下，可以通过网络访问。</span><span class="sxs-lookup"><span data-stu-id="1a669-138">In this case, it can be accessed via a network.</span></span>

### <a name="hardware-profile"></a><span data-ttu-id="1a669-139">硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="1a669-139">Hardware profile</span></span>

<span data-ttu-id="1a669-140">导航︰单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="1a669-140">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="1a669-141">硬件配置文件是为 POS 收银机或硬件工作站配置的设备的列表。</span><span class="sxs-lookup"><span data-stu-id="1a669-141">The hardware profile is a list of devices that are configured for a POS register or a hardware station.</span></span> <span data-ttu-id="1a669-142">硬件配置文件可以直接映射到 POS 收银机或硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-142">The hardware profile can be mapped directly to a POS register or a hardware station.</span></span>

## <a name="devices-classes"></a><span data-ttu-id="1a669-143">设备分类</span><span class="sxs-lookup"><span data-stu-id="1a669-143">Devices classes</span></span>
<span data-ttu-id="1a669-144">POS 外设通常划分为类。</span><span class="sxs-lookup"><span data-stu-id="1a669-144">POS peripherals are typically divided into classes.</span></span> <span data-ttu-id="1a669-145">此部分描述并提供 Modern POS 支持的设备的概览。</span><span class="sxs-lookup"><span data-stu-id="1a669-145">This section describes and gives an overview of the devices that Modern POS supports.</span></span>

### <a name="printer"></a><span data-ttu-id="1a669-146">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-146">Printer</span></span>

<span data-ttu-id="1a669-147">外设包括传统 POS 收据打印机和整页打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-147">Printers include traditional POS receipt printers and full-page printers.</span></span> <span data-ttu-id="1a669-148">通过适用于 Retail POS (OPOS) 和 Microsoft Windows 的对象链路与嵌入驱动程序接口为打印机提供支持。</span><span class="sxs-lookup"><span data-stu-id="1a669-148">Printer are supported through Object Linking and Embedding for Retail POS (OPOS) and Microsoft Windows driver interfaces.</span></span> <span data-ttu-id="1a669-149">最多可以同时使用两台打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-149">Up to two printers can be used at the same time.</span></span> <span data-ttu-id="1a669-150">此功能支持在收据打印机上打印付现自提的客户收据的方案，虽然包含更多信息的客户订单在整页打印机上打印。</span><span class="sxs-lookup"><span data-stu-id="1a669-150">This capability supports scenarios where cash-and-carry customer receipts are printed on receipt printers, whereas customer orders, which carry more information, are printed on a full-page printer.</span></span> <span data-ttu-id="1a669-151">收据打印机可以通过 USB 直接连接到计算机，通过以太网连接到网络，或通过 Bluetooth 连接。</span><span class="sxs-lookup"><span data-stu-id="1a669-151">Receipt printers can be connected directly to a computer via USB, connected to a network via Ethernet, or connected via Bluetooth.</span></span>

### <a name="scanner"></a><span data-ttu-id="1a669-152">扫描仪</span><span class="sxs-lookup"><span data-stu-id="1a669-152">Scanner</span></span>

<span data-ttu-id="1a669-153">最多可以同时使用两台条码扫描仪。</span><span class="sxs-lookup"><span data-stu-id="1a669-153">Up to two bar code scanners can be used at the same time.</span></span> <span data-ttu-id="1a669-154">此功能支持需要移动性更高的扫描仪来扫描体积大或重量高的物品的方案，而嵌入式固定扫描仪则用于大多数标准尺寸的物品或加快收银速度。</span><span class="sxs-lookup"><span data-stu-id="1a669-154">This capability supports scenarios where a scanner that is more mobile is required in order to scan large or heavy items, whereas a fixed embedded scanner is used for most standard-sized items, to speed up checkout times.</span></span> <span data-ttu-id="1a669-155">可以通过 OPOS、通用 Windows 平台 (UWP) 或键盘 wedge 界面为扫描仪提供支持。</span><span class="sxs-lookup"><span data-stu-id="1a669-155">Scanners can be supported through OPOS, Universal Windows Platform (UWP), or keyboard wedge interfaces.</span></span> <span data-ttu-id="1a669-156">可使用 USB 或 Bluetooth 将扫描仪连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-156">USB or Bluetooth can be used to connect a scanner to a computer.</span></span>

### <a name="msr"></a><span data-ttu-id="1a669-157">MSR</span><span class="sxs-lookup"><span data-stu-id="1a669-157">MSR</span></span>

<span data-ttu-id="1a669-158">可通过使用 OPOS 设置一台 USB 磁条阅读器 (MSR)。</span><span class="sxs-lookup"><span data-stu-id="1a669-158">One USB magnetic stripe reader (MSR) can be set up by using OPOS drivers.</span></span> <span data-ttu-id="1a669-159">如果要将单机 MSR 用于电子资金转帐 (EFT) 付款交易，则必须通过付款连接器管理 MSR。.</span><span class="sxs-lookup"><span data-stu-id="1a669-159">If you want to use a stand-alone MSR for electronic funds transfer (EFT) payment transactions, the MSR must be managed by a payment connector.</span></span> <span data-ttu-id="1a669-160">单机 MSR 可用于独立于付款连接器执行客户会员信息录入、员工签到和礼品卡录入。</span><span class="sxs-lookup"><span data-stu-id="1a669-160">Stand-alone MSRs can be used for customer loyalty entry, employee sign-in, and gift card entry, independently of the payment connector.</span></span>

### <a name="cash-drawer"></a><span data-ttu-id="1a669-161">银箱</span><span class="sxs-lookup"><span data-stu-id="1a669-161">Cash drawer</span></span>

<span data-ttu-id="1a669-162">每个硬件配置文件可以支持两个银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-162">Two cash drawers can be supported per hardware profile.</span></span> <span data-ttu-id="1a669-163">此功能允许每台收银机同时被两个班次使用。</span><span class="sxs-lookup"><span data-stu-id="1a669-163">This capability enables two active shifts per register to be available at the same time.</span></span> <span data-ttu-id="1a669-164">为了防止共享班次或一个银箱同时被多个移动 POS 设备使用，每个硬件配置文件仅允许一个银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-164">In the case of a shared shift, or a cash drawer that is used by multiple mobile POS devices at the same time, only one cash drawer is allowed per hardware profile.</span></span> <span data-ttu-id="1a669-165">银箱可以通过 USB 直接连接到计算机，连接到网络，或通过 RJ12 接口连接到收据打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-165">Cash drawers can be connected directly to a computer via USB, connected to a network, or connected to a receipt printer via an RJ12 interface.</span></span> <span data-ttu-id="1a669-166">在某些情况下，还可以通过 Bluetooth 连接银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-166">In some cases, cash drawers can also be connected via Bluetooth.</span></span>

### <a name="line-display"></a><span data-ttu-id="1a669-167">行显示内容</span><span class="sxs-lookup"><span data-stu-id="1a669-167">Line display</span></span>

<span data-ttu-id="1a669-168">行显示器用于在交易期间向客户显示产品、交易余额和其他有用信息。</span><span class="sxs-lookup"><span data-stu-id="1a669-168">Line displays are used to show products, transaction balances, and other useful information to the customer during a transaction.</span></span> <span data-ttu-id="1a669-169">可以使用 OPOS 驱动程序通过 USB 将一台行显示器连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-169">One line display can be connected to the computer via USB by using OPOS drivers.</span></span>

### <a name="signature-capture"></a><span data-ttu-id="1a669-170">签名捕获</span><span class="sxs-lookup"><span data-stu-id="1a669-170">Signature capture</span></span>

<span data-ttu-id="1a669-171">可以使用 OPOS 驱动程序通过 USB 将签名捕获设备直接连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-171">Signature capture devices can be connected directly to a computer via USB by using OPOS drivers.</span></span> <span data-ttu-id="1a669-172">在配置签名捕获时，将提示客户在设备上签名。</span><span class="sxs-lookup"><span data-stu-id="1a669-172">When signature capture is configured, the customer is prompted to sign on the device.</span></span> <span data-ttu-id="1a669-173">提供签名后，它会对收银员显示，待其接受。</span><span class="sxs-lookup"><span data-stu-id="1a669-173">After the signature is provided, it's shown to the cashier for acceptance.</span></span>

### <a name="scale"></a><span data-ttu-id="1a669-174">比例</span><span class="sxs-lookup"><span data-stu-id="1a669-174">Scale</span></span>

<span data-ttu-id="1a669-175">可以使用 OPOS 驱动程序通过 USP 将秤连接到计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-175">Scales can be connected to the computer via USP by using OPOS drivers.</span></span> <span data-ttu-id="1a669-176">标记为“已称重”产品的产品添加到交易记录时，POS 从秤读取重量，将该产品添加到交易记录，然后使用秤提供的数量。</span><span class="sxs-lookup"><span data-stu-id="1a669-176">When a product that is marked as a "Weighed" product is added to a transaction, the POS reads the weight from the scale, adds the product to the transaction, and uses the quantity that the scale provided.</span></span>

### <a name="pin-pad"></a><span data-ttu-id="1a669-177">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="1a669-177">PIN pad</span></span>

<span data-ttu-id="1a669-178">通过 OPOS 为个人标识号 (PIN) 小键盘提供支持，但是必须通过付款连接器管理 PIN 小键盘。</span><span class="sxs-lookup"><span data-stu-id="1a669-178">Personal identification number (PIN) pads are supported through OPOS, but they must be managed via a payment connector.</span></span>

### <a name="secondary-display"></a><span data-ttu-id="1a669-179">辅助显示器</span><span class="sxs-lookup"><span data-stu-id="1a669-179">Secondary display</span></span>

<span data-ttu-id="1a669-180">如果配置了辅助显示器，将使用第二台 Windows 显示器显示基本信息。</span><span class="sxs-lookup"><span data-stu-id="1a669-180">When a secondary display is configured, the number 2 Windows display is used to show basic information.</span></span> <span data-ttu-id="1a669-181">辅助显示器用于为独立软件供应商 (ISV) 扩展提供支持，因为原始辅助显示器不可配置，显示的内容有限。</span><span class="sxs-lookup"><span data-stu-id="1a669-181">The purpose of the secondary display is to support independent software vendor (ISV) extension, because out of the box, the secondary display isn't configurable and shows limited content.</span></span>

### <a name="payment-device"></a><span data-ttu-id="1a669-182">付款设备</span><span class="sxs-lookup"><span data-stu-id="1a669-182">Payment device</span></span>

<span data-ttu-id="1a669-183">对付款设备的支持通过付款连接器实现。</span><span class="sxs-lookup"><span data-stu-id="1a669-183">Payment device support is implemented through the payment connector.</span></span> <span data-ttu-id="1a669-184">付款设备可以执行其他设备类提供的一项或多项功能。</span><span class="sxs-lookup"><span data-stu-id="1a669-184">Payment devices can perform one or many of the functions that other device classes provide.</span></span> <span data-ttu-id="1a669-185">例如，一种付款设备可以充当 MSR/卡阅读器、行显示器、签名捕获设备或 PIN 小键盘。</span><span class="sxs-lookup"><span data-stu-id="1a669-185">For example, a payment device can function as an MSR/card reader, line display, signature capture device, or PIN pad.</span></span> <span data-ttu-id="1a669-186">对付款设备的支持独立于为硬件配置文件中包含的其他设备提供的单机设备支持实现。</span><span class="sxs-lookup"><span data-stu-id="1a669-186">Support for payment devices is implemented independently of the stand-alone device support that is provided for other devices that are included in the hardware profile.</span></span>

## <a name="supported-interfaces"></a><span data-ttu-id="1a669-187">支持的接口</span><span class="sxs-lookup"><span data-stu-id="1a669-187">Supported interfaces</span></span>

### <a name="opos"></a><span data-ttu-id="1a669-188">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-188">OPOS</span></span>

<span data-ttu-id="1a669-189">为了帮助确保最大范围的设备可以与 Microsoft Dynamics 365 for Retail 配合使用，OLE for POS 行业标准成为了 Microsoft Dynamics 365 for Retail 中支持的主要零售外设平台。</span><span class="sxs-lookup"><span data-stu-id="1a669-189">To help guarantee that the largest range of devices can be used with Microsoft Dynamics 365 for Retail, the OLE for POS industry standard is the primary retail peripheral device platform that is supported in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1a669-190">OLE for POS 标准由美国零售联合会 (NRF) 制订，建立了针对零售外设的行业标准通信协议。</span><span class="sxs-lookup"><span data-stu-id="1a669-190">The OLE for POS standard was produced by the National Retail Federation (NRF), which establishes industry-standard communication protocols for retail peripheral devices.</span></span> <span data-ttu-id="1a669-191">OPOS 是广泛采用的 OLE for POS 标准实施。</span><span class="sxs-lookup"><span data-stu-id="1a669-191">OPOS is a widely adopted implementation of the OLE for POS standard.</span></span> <span data-ttu-id="1a669-192">它开发于 20 世纪 90 年代，之后经过了多次更新。</span><span class="sxs-lookup"><span data-stu-id="1a669-192">It was developed in the mid-1990s and has been updated several times since then.</span></span> <span data-ttu-id="1a669-193">OPOS 提供设备驱动程序架构，以便将 POS 硬件与基于 Windows 的 POS 系统轻松集成。</span><span class="sxs-lookup"><span data-stu-id="1a669-193">OPOS provides a device driver architecture that enables easy integration of POS hardware with Windows–based POS systems.</span></span> <span data-ttu-id="1a669-194">OPOS 控件处理兼容硬件与 POS 软件之间的通信。</span><span class="sxs-lookup"><span data-stu-id="1a669-194">OPOS controls handle communication between compatible hardware and the POS software.</span></span> <span data-ttu-id="1a669-195">OPOS 控件包含两部分：</span><span class="sxs-lookup"><span data-stu-id="1a669-195">An OPOS control consists of two parts:</span></span>

- <span data-ttu-id="1a669-196">**控件对象** – 设备类（如行显示器）的控件对象提供软件程序的界面。</span><span class="sxs-lookup"><span data-stu-id="1a669-196">**Control object** – The control object for a device class (such as line displays) provides the interface for the software program.</span></span> <span data-ttu-id="1a669-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) 提供一组标准的 OPOS 控件对象，称为公共控件对象 (CCO)。</span><span class="sxs-lookup"><span data-stu-id="1a669-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) provides a standardized set of OPOS control objects that are known as the common control objects (CCOs).</span></span> <span data-ttu-id="1a669-198">CCO 用于测试 Microsoft Dynamics 365 for Retail 的 POS 组件。</span><span class="sxs-lookup"><span data-stu-id="1a669-198">The CCOs are used to test the POS component of Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1a669-199">因此，如果 Microsoft Dynamics 365 for Retail 通过 OPOS 为设备类提供支持，并且制造商提供为 OPOS 构建的服务对象，此项测试有助于确保可以支持多种设备类型。</span><span class="sxs-lookup"><span data-stu-id="1a669-199">Therefore, the testing helps guarantee that, if Microsoft Dynamics 365 for Retail supports a device class through OPOS, many device types can be supported, provided that the manufacturer provides a service object that is built for OPOS.</span></span> <span data-ttu-id="1a669-200">无需明确测试每个设备类型。</span><span class="sxs-lookup"><span data-stu-id="1a669-200">You don't have to explicitly test each device type.</span></span>
- <span data-ttu-id="1a669-201">**服务对象** – 服务对象提供控件对象 (CCO) 与设备之间的通信。</span><span class="sxs-lookup"><span data-stu-id="1a669-201">**Service object** – The service object provides communication between the control object (CCO) and the device.</span></span> <span data-ttu-id="1a669-202">设备的服务对象通常由设备制造商提供。</span><span class="sxs-lookup"><span data-stu-id="1a669-202">Typically, the service object for a device is provided by the device manufacturer.</span></span> <span data-ttu-id="1a669-203">但是在某些情况下，您可能必须从制造商的网站下载服务对象。</span><span class="sxs-lookup"><span data-stu-id="1a669-203">However, in some cases, you might have to download the service object from the manufacturer's website.</span></span> <span data-ttu-id="1a669-204">例如，可能提供了更新的服务对象。</span><span class="sxs-lookup"><span data-stu-id="1a669-204">For example, a more recent service object might be available.</span></span> <span data-ttu-id="1a669-205">若要查找制造商的网站地址，请参阅您的硬件文档。</span><span class="sxs-lookup"><span data-stu-id="1a669-205">To find the address of the manufacturer's website, see your hardware documentation.</span></span>

<span data-ttu-id="1a669-206">[![控件对象和服务对象](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)</span><span class="sxs-lookup"><span data-stu-id="1a669-206">[![Control object and service object](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)</span></span>

<span data-ttu-id="1a669-207">对 OLE for POS 的 OPOS 实施的支持有助于确保当设备制造商和 POS 发布商正确实施标准时，POS 系统和支持的设备可以协同工作，即使以前未一起测试时也不例外。</span><span class="sxs-lookup"><span data-stu-id="1a669-207">Support for the OPOS implementation of OLE for POS helps guarantee that, if the device manufacturers and POS publishers implement the standard correctly, POS systems and supported devices can work together, even if they weren't previously tested together.</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-208">支持 OPOS 不保证支持采用了 OPOS 驱动设备的所有设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-208">OPOS support doesn't guarantee support for all devices that have OPOS drivers.</span></span> <span data-ttu-id="1a669-209">Microsoft Dynamics 365 for Retail 必须首先通过 OPOS 支持该设备类型（或类）。</span><span class="sxs-lookup"><span data-stu-id="1a669-209">Microsoft Dynamics 365 for Retail must first support that device type, or class, through OPOS.</span></span> <span data-ttu-id="1a669-210">此外，服务对象可能并非始终安装了最新版本的 CCO。</span><span class="sxs-lookup"><span data-stu-id="1a669-210">In addition, service objects might not always be up to date with the latest version of the CCOs.</span></span> <span data-ttu-id="1a669-211">您还应注意，服务对象的质量往往参差不齐。</span><span class="sxs-lookup"><span data-stu-id="1a669-211">You should also be aware that, in general, the quality of service objects varies.</span></span>

### <a name="windows"></a><span data-ttu-id="1a669-212">窗口</span><span class="sxs-lookup"><span data-stu-id="1a669-212">Windows</span></span>

<span data-ttu-id="1a669-213">POS 的收据打印已针对 OPOS 进行了优化。</span><span class="sxs-lookup"><span data-stu-id="1a669-213">Receipt printing at the POS is optimized for OPOS.</span></span> <span data-ttu-id="1a669-214">OPOS 往往比通过 Windows 打印快得多。</span><span class="sxs-lookup"><span data-stu-id="1a669-214">OPOS tends to be much faster than printing through Windows.</span></span> <span data-ttu-id="1a669-215">因此，最好使用 OPOS 进行打印，特别是在零售环境中，此类环境中需要打印 40 列收据，并且交易时间必须非常快。</span><span class="sxs-lookup"><span data-stu-id="1a669-215">Therefore, it's a good idea to use OPOS, especially in retail environments where 40-column receipts are printed and transaction times must be fast.</span></span> <span data-ttu-id="1a669-216">对于大多数设备，您将使用 OPOS 控件。</span><span class="sxs-lookup"><span data-stu-id="1a669-216">For most devices, you will use OPOS controls.</span></span> <span data-ttu-id="1a669-217">但是，某些 OPOS 收据打印机也支持 Windows 驱动程序。</span><span class="sxs-lookup"><span data-stu-id="1a669-217">However, some OPOS receipt printers also support Windows drivers.</span></span> <span data-ttu-id="1a669-218">通过使用 Windows 驱动程序，您可以通过一台打印机访问多台收银机的最新字体和网络。</span><span class="sxs-lookup"><span data-stu-id="1a669-218">By using a Windows driver, you can access the latest fonts and network one printer for multiple registers.</span></span> <span data-ttu-id="1a669-219">但是使用 Windows 驱动程序有一些缺点。</span><span class="sxs-lookup"><span data-stu-id="1a669-219">However, there are drawbacks to using Windows drivers.</span></span> <span data-ttu-id="1a669-220">以下是这些缺点的一些示例：</span><span class="sxs-lookup"><span data-stu-id="1a669-220">Here are some examples of these drawbacks:</span></span>

- <span data-ttu-id="1a669-221">使用 Windows 驱动程序时，图像在打印前渲染。</span><span class="sxs-lookup"><span data-stu-id="1a669-221">When Windows drivers are used, images are rendered before printing occurs.</span></span> <span data-ttu-id="1a669-222">因此，打印速度往往比使用 OPOS 控件的打印机慢。</span><span class="sxs-lookup"><span data-stu-id="1a669-222">Therefore, printing tends to be slower than it is on printers that use OPOS controls.</span></span>
- <span data-ttu-id="1a669-223">使用 Windows 驱动程序时，通过打印机连接（菊链方式）的设备可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="1a669-223">Devices that are connected through the printer ("daisy-chained") might not work correctly when Windows drivers are used.</span></span> <span data-ttu-id="1a669-224">例如，银箱可能无法打开，或者票据打印机可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="1a669-224">For example, the cash drawer might not open, or the slip printer might not word as you expect.</span></span>
- <span data-ttu-id="1a669-225">OPOS 还支持特定于零售收据打印机的更多变体集合，如裁纸或票据打印。</span><span class="sxs-lookup"><span data-stu-id="1a669-225">OPOS also supports a more extensive set of variables that are specific to retail receipt printers, such as paper cutting or slip printing.</span></span>

<span data-ttu-id="1a669-226">如果 OPOS 控件适用于您在使用的 Windows 打印机，该打印机仍然可以与 Microsoft Dynamics 365 for Retail 配合正常工作。</span><span class="sxs-lookup"><span data-stu-id="1a669-226">If OPOS controls are available for the Windows printer that you're using, the printer should still work correctly with Microsoft Dynamics 365 for Retail.</span></span>

### <a name="universal-windows-platform"></a><span data-ttu-id="1a669-227">通用 Windows 平台</span><span class="sxs-lookup"><span data-stu-id="1a669-227">Universal Windows Platform</span></span>

<span data-ttu-id="1a669-228">对于零售外设，UWP 与 Windows 对即插即用设备的支持有关。</span><span class="sxs-lookup"><span data-stu-id="1a669-228">UWP, in the case of retail peripherals, is related to Windows support for Plug and Play devices.</span></span> <span data-ttu-id="1a669-229">当即插即用设备连接到支持这种设备的 Windows 操作系统版本时，该设备不需要驱动程序即可正常使用。</span><span class="sxs-lookup"><span data-stu-id="1a669-229">When a Plug and Play device is connected to a Windows OS version that supports that type of device, no driver is required for the device to be used as intended.</span></span> <span data-ttu-id="1a669-230">例如，如果 Windows 检测到 Bluetooth 扬声器设备，该操作系统知道此设备的类类型为**扬声器**。</span><span class="sxs-lookup"><span data-stu-id="1a669-230">For example, if Windows detects a Bluetooth speaker device, the OS knows that the device has the **Speaker** class type.</span></span> <span data-ttu-id="1a669-231">因此，它将把此设备视为扬声器。</span><span class="sxs-lookup"><span data-stu-id="1a669-231">Therefore, and it treats that device as a speaker.</span></span> <span data-ttu-id="1a669-232">无需再执行任何设置。</span><span class="sxs-lookup"><span data-stu-id="1a669-232">No additional setup is required.</span></span> <span data-ttu-id="1a669-233">对于 POS 设备，可以插入大量 USB 设备，并且 Windows 将把其识别为人机接口设备 (HID)。</span><span class="sxs-lookup"><span data-stu-id="1a669-233">In the case of POS devices, many USB devices can be plugged in, and Windows will recognize them as Human Interface Devices (HIDs).</span></span> <span data-ttu-id="1a669-234">但是，可能不能确定设备提供的功能，因为设备不指定设备的类（即类型）。</span><span class="sxs-lookup"><span data-stu-id="1a669-234">However, it might not be able to determine the capabilities that the device provides, because the device doesn't specify the class, or type, of device.</span></span> <span data-ttu-id="1a669-235">在 Windows 10 中，已增加了条码扫描仪 和 MSR 的设备类。</span><span class="sxs-lookup"><span data-stu-id="1a669-235">In Windows 10, device classes for bar code scanners and MSRs have been added.</span></span> <span data-ttu-id="1a669-236">因此，如果设备向 Windows 10 声明自己是这些类之一的设备，Windows 将在相应时间注意来自该设备的事件。</span><span class="sxs-lookup"><span data-stu-id="1a669-236">Therefore, if a device declares itself to Windows 10 as a device of one of these classes, Windows will listen for events from the device at the appropriate times.</span></span> <span data-ttu-id="1a669-237">Modern POS 支持 UWP MSR 和扫描仪。</span><span class="sxs-lookup"><span data-stu-id="1a669-237">Modern POS supports UWP MSRs and scanners.</span></span> <span data-ttu-id="1a669-238">因此，准备好从这些设备之一输入，并且已连接属于这些类之一的设备时，可以使用该设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-238">Therefore, when it's ready for input from one of these devices, and a device that belongs to one of these classes is connected, the device can be used.</span></span> <span data-ttu-id="1a669-239">例如，如果在 Windows 10 计算机中插入一台 UWP 条码扫描仪，并且为 Modern POS 配置了条码签到，将在签到屏幕上激活该条码扫描仪。</span><span class="sxs-lookup"><span data-stu-id="1a669-239">For example, if a UWP bar code scanner is plugged into a Windows 10 computer, and bar code sign-in is configured for Modern POS, the bar code scanner will become active on the sign-in screen.</span></span> <span data-ttu-id="1a669-240">无需再执行任何设置。</span><span class="sxs-lookup"><span data-stu-id="1a669-240">No additional setup is required.</span></span> <span data-ttu-id="1a669-241">正在向 Windows 添加更多服务点 UWP 设备类。</span><span class="sxs-lookup"><span data-stu-id="1a669-241">Additional classes of point of service UWP devices are being added to Windows.</span></span> <span data-ttu-id="1a669-242">这些类中包括银箱和收据打印机的类。</span><span class="sxs-lookup"><span data-stu-id="1a669-242">These classes include classes for cash drawers and receipt printers.</span></span> <span data-ttu-id="1a669-243">Modern POS 中对这些新设备的支持待定。</span><span class="sxs-lookup"><span data-stu-id="1a669-243">Support for these new device classes in Modern POS is pending.</span></span>

### <a name="keyboard-wedge"></a><span data-ttu-id="1a669-244">键盘 wedge</span><span class="sxs-lookup"><span data-stu-id="1a669-244">Keyboard wedge</span></span>

<span data-ttu-id="1a669-245">键盘 wedge 设备向计算机发送数据，就像数据是从键盘键入的。</span><span class="sxs-lookup"><span data-stu-id="1a669-245">Keyboard wedge devices send data to the computer as if that data were typed on a keyboard.</span></span> <span data-ttu-id="1a669-246">因此默认情况下，POS 上的活动字段将收到扫描或刷卡的数据。</span><span class="sxs-lookup"><span data-stu-id="1a669-246">Therefore, by default, the field that is active at the POS will receive the data that is scanned or swiped.</span></span> <span data-ttu-id="1a669-247">在某些情况下，此行为可能导致将错误类型的数据扫描到错误的字段中。</span><span class="sxs-lookup"><span data-stu-id="1a669-247">In some cases, this behavior can cause the wrong type of data to be scanned into the wrong field.</span></span> <span data-ttu-id="1a669-248">例如，可能将条码扫描到本应输入信用卡数据的字段。</span><span class="sxs-lookup"><span data-stu-id="1a669-248">For example, a bar code might be scanned into a field that is intended for input of credit card data.</span></span> <span data-ttu-id="1a669-249">在大多数情况下，POS 中有逻辑可确定扫描的数据是条码还是刷卡。</span><span class="sxs-lookup"><span data-stu-id="1a669-249">In many cases, there is logic at the POS that determines whether the data that is scanned or swiped is a bar code or card swipe.</span></span> <span data-ttu-id="1a669-250">因此可以正确处理数据。</span><span class="sxs-lookup"><span data-stu-id="1a669-250">Therefore, the data is handled correctly.</span></span> <span data-ttu-id="1a669-251">但是，当设备设置为 OPOS 而不是键盘 wedge 设备时，对来自这些设备的数据的使用方式控制更严格，因为对数据的来源设备的“了解”更深。</span><span class="sxs-lookup"><span data-stu-id="1a669-251">However, when devices are set up as OPOS instead of keyboard wedge devices, there is more control over how the data from those devices can be consumed, because more is "known" about the device that the data originates from.</span></span> <span data-ttu-id="1a669-252">例如，来自条码扫描仪的数据自动识别为条码，并且相比过去使用的一般字符串搜索（如使用键盘 wedge 设备时），可以更轻松、更快地找到数据库中的关联记录。</span><span class="sxs-lookup"><span data-stu-id="1a669-252">For example, data from a bar code scanner is automatically recognized as a bar code, and the associated record in the database is found more easily and faster than if a generic string search were used, as in the case of keyboard wedge devices.</span></span>

### <a name="native-printer"></a><span data-ttu-id="1a669-253">本机打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-253">Native printer</span></span>

<span data-ttu-id="1a669-254">可以将本机（或“设备”，因为类型是在硬件配置文件中命名的）配置为提示用户选择为计算机配置的打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-254">Native (or "Device" as the type is named in the hardware profile) printers can be configured to prompt the user to select a printer that is configured for the computer.</span></span> <span data-ttu-id="1a669-255">配置了**设备**类型的打印机时，如果 Modern POS 收到了打印命令，将提示用户在列表中选择打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-255">When a printer of the **Device** type is configured, if Modern POS encounters a print command, the user is prompted to select a printer in a list.</span></span> <span data-ttu-id="1a669-256">此行为与 Windows 驱动程序的行为不同，因为硬件配置文件中的 **Windows** 打印机类型不显示打印机列表。</span><span class="sxs-lookup"><span data-stu-id="1a669-256">This behavior differs from the behavior for Windows drivers, because the **Windows** printer type in the hardware profile doesn't show a list of printers.</span></span> <span data-ttu-id="1a669-257">相反，它要求在**设备名称**字段中提供命名的打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-257">Instead, it requires that a named printer be provided in the **Device name** field.</span></span>

### <a name="windows"></a><span data-ttu-id="1a669-258">窗口</span><span class="sxs-lookup"><span data-stu-id="1a669-258">Windows</span></span>

<span data-ttu-id="1a669-259">**Windows** 设备类型仅用于打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-259">The **Windows** device type is used for printers only.</span></span> <span data-ttu-id="1a669-260">在硬件配置文件中配置了 Windows 打印机时，必须指定具体的打印机名称。</span><span class="sxs-lookup"><span data-stu-id="1a669-260">When a Windows printer is configured in the hardware profile, the specific printer name must be provided.</span></span> <span data-ttu-id="1a669-261">在 Modern POS 遇到打印事件时，如果配置了 Windows 打印机，将把该事件传递到指定的 Windows 打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-261">When Modern POS encounters print events, if a Windows printer is configured, the event will be passed to the specified Windows printer.</span></span> <span data-ttu-id="1a669-262">将不提示用户选择打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-262">The user won't be prompted to select a printer.</span></span>

### <a name="network"></a><span data-ttu-id="1a669-263">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-263">Network</span></span>

<span data-ttu-id="1a669-264">可通过 Modern POS for Windows 和 Modern POS for Android 应用程序中内置的进程间通信 (IPC) 硬件工作站或其他 Modern POS 客户端的 IIS 硬件工作站，通过网络使用网络可寻址银箱、收据打印机和付款终端。</span><span class="sxs-lookup"><span data-stu-id="1a669-264">Network-addressable cash drawers, receipt printers, and payment terminals can be used over a network, either directly through the Interprocess Communications (IPC) hardware station that is built into the Modern POS for Windows and Modern POS for Android applications or through the IIS hardware station for other Modern POS clients.</span></span>

## <a name="hardware-station-deployment-options"></a><span data-ttu-id="1a669-265">硬件工作站部署选项</span><span class="sxs-lookup"><span data-stu-id="1a669-265">Hardware station deployment options</span></span>

### <a name="ipc-built-in"></a><span data-ttu-id="1a669-266">IPC（内置）</span><span class="sxs-lookup"><span data-stu-id="1a669-266">IPC (built-in)</span></span>

<span data-ttu-id="1a669-267">进程间通信 (IPC) 硬件工作站内置在 Modern POS for Windows 和 Modern POS for Android 应用程序中。</span><span class="sxs-lookup"><span data-stu-id="1a669-267">The Interprocess Communications (IPC) hardware station is built into the Modern POS for Windows and Modern POS for Android application.</span></span> <span data-ttu-id="1a669-268">若要使用 IPC 硬件工作站，请为将使用 Modern POS for Windows 应用程序的收银机分配硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-268">To use the IPC hardware station, assign a hardware profile to a register that will use the Modern POS for Windows application.</span></span> <span data-ttu-id="1a669-269">然后为将使用该收银机的商店创建一个类型为**专用**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-269">Then create a hardware station of the **Dedicated** type for the store where the register will be used.</span></span> <span data-ttu-id="1a669-270">启动 Modern POS 时，将激活 IPC 硬件工作站，而已配置的 POS 外设将准备就绪，可供使用。</span><span class="sxs-lookup"><span data-stu-id="1a669-270">When you start Modern POS, the IPC hardware station will be active, and the POS peripherals that have been configured will be ready to use.</span></span> <span data-ttu-id="1a669-271">如果因为某种原因暂时不需要本地硬件，请使用**管理硬件工作站**关闭硬件工作站功能。</span><span class="sxs-lookup"><span data-stu-id="1a669-271">If you temporarily don't require the local hardware for some reason, use the **Manage hardware stations** operation to turn off the hardware station capabilities.</span></span> <span data-ttu-id="1a669-272">Modern POS 也可以使用 IPC 硬件工作站直接与网络外设通信。</span><span class="sxs-lookup"><span data-stu-id="1a669-272">Modern POS can also use the IPC hardware station to communicate directly with network peripherals.</span></span>

### <a name="iis"></a><span data-ttu-id="1a669-273">IIS</span><span class="sxs-lookup"><span data-stu-id="1a669-273">IIS</span></span>

<span data-ttu-id="1a669-274">可以通过两种方式使用硬件工作站的 IIS 或单机版本。</span><span class="sxs-lookup"><span data-stu-id="1a669-274">You can use the IIS or stand-alone version of the hardware station in two ways.</span></span> <span data-ttu-id="1a669-275">描述符“IIS”暗示 POS 应用程序通过 Microsoft Internet Information Services 连接到硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-275">The descriptor "IIS" implies that the POS application connects to the hardware station via Microsoft Internet Information Services.</span></span> <span data-ttu-id="1a669-276">POS 应用程序通过连接设备的计算机上运行的 Web 服务连接到 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-276">The POS application connects to the IIS hardware station via web services that run on a computer where the devices are connected.</span></span> <span data-ttu-id="1a669-277">使用 IIS 时，与 IIS 硬件工作站在同一个网络中的任何 POS 收银机都可以使用与该硬件工作站相连的零售外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-277">When IIS is used, the retail peripherals that are connected to a hardware station can be used by any POS register that is on the same network as the IIS hardware station.</span></span> <span data-ttu-id="1a669-278">由于只有 Modern POS for Windows 中才包含对零售外设的内置支持，所以其他所有 Modern POS 应用程序都必须使用 IIS 硬件工作站才能与硬件配置文件中配置的 POS 外设通信。</span><span class="sxs-lookup"><span data-stu-id="1a669-278">Because only Modern POS for Windows includes built-in support for retail peripherals, all other Modern POS applications must use the IIS hardware station to communicate with POS peripherals that are configured in the hardware profile.</span></span> <span data-ttu-id="1a669-279">因此，IIS 硬件工作站的每个实例都需要运行与设备通信的 Web 服务和应用程序的计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-279">Therefore, each instance of the IIS hardware station requires a computer that runs the web service and application that communicates with the devices.</span></span> <span data-ttu-id="1a669-280">所有非 Windows Modern POS 应用程序都需要 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-280">The IIS hardware station is required for all non-Windows Modern POS applications.</span></span>

#### <a name="dedicated"></a><span data-ttu-id="1a669-281">专门</span><span class="sxs-lookup"><span data-stu-id="1a669-281">Dedicated</span></span>

<span data-ttu-id="1a669-282">Modern POS 使用**专用**类型的硬件工作站检测外设是否直接连接到正在使用该应用程序的计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-282">Modern POS uses hardware stations of the **Dedicated** type to detect that peripherals are directly connected to the computer where the app is being used.</span></span> <span data-ttu-id="1a669-283">但是，**专用**类型也可用于 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-283">However, the **Dedicated** type can also be used for IIS hardware stations.</span></span> <span data-ttu-id="1a669-284">在将 Cloud POS 用作 POS 应用程序的传统固定式 POS 方案中，**专用**硬件工作站用于运行 Cloud POS 的同一计算机上部署的 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-284">In a traditional, fixed POS scenario that uses Cloud POS as the POS application, the **Dedicated** hardware station type is used for IIS hardware stations that are deployed on the same computer that is running Cloud POS.</span></span> <span data-ttu-id="1a669-285">从零售外设的角度，专用 IIS 硬件工作站对零售外设的支持比传统的固定式 POS 方案更出色。</span><span class="sxs-lookup"><span data-stu-id="1a669-285">From a retail peripherals perspective, the dedicated IIS hardware station has better retail peripheral support for traditional, fixed POS scenarios.</span></span> <span data-ttu-id="1a669-286">专用硬件工作站支持硬件配置文件中支持的所有外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-286">Dedicated hardware stations support all peripherals that are supported in the hardware profile.</span></span>

#### <a name="shared"></a><span data-ttu-id="1a669-287">共享的</span><span class="sxs-lookup"><span data-stu-id="1a669-287">Shared</span></span>

<span data-ttu-id="1a669-288">共享硬件工作站应该可以全天供多个 POS 设备使用。</span><span class="sxs-lookup"><span data-stu-id="1a669-288">Shared hardware stations are intended to be used by multiple POS devices through the course of the day.</span></span> <span data-ttu-id="1a669-289">共享硬件工作站已经过优化，只能支持银箱、收据打印机和付款终端。</span><span class="sxs-lookup"><span data-stu-id="1a669-289">Shared hardware stations are optimized to support only cash drawers, receipt printers, and payment terminals.</span></span> <span data-ttu-id="1a669-290">不能直接连接单机条码扫描仪、行显示器，MSR、秤或其他设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-290">You can't directly connect stand-alone bar code scanners, MSRs, line displays, scales, or other devices.</span></span> <span data-ttu-id="1a669-291">否则，多个 POS 设备同时尝试声明这些外设时，将发生冲突。</span><span class="sxs-lookup"><span data-stu-id="1a669-291">Otherwise, conflicts will occur when multiple POS devices try to claim those peripherals at the same time.</span></span> <span data-ttu-id="1a669-292">下面是如何管理受支持设备的冲突：</span><span class="sxs-lookup"><span data-stu-id="1a669-292">Here is how conflicts are managed for supported devices:</span></span>

- <span data-ttu-id="1a669-293">**银箱** – 银箱通过发送到设备的事件打开。</span><span class="sxs-lookup"><span data-stu-id="1a669-293">**Cash drawer** – The cash drawer is opened via an event that is sent to the device.</span></span> <span data-ttu-id="1a669-294">仅当银箱已打开时，才会在调用银箱时发生问题。</span><span class="sxs-lookup"><span data-stu-id="1a669-294">The only issue that can occur when a cash drawer is called occurs if the cash drawer is already open.</span></span> <span data-ttu-id="1a669-295">对于共享硬件工作站，应在硬件配置文件中将银箱设置为**共享**。</span><span class="sxs-lookup"><span data-stu-id="1a669-295">In the case of shared hardware stations, the cash drawer should be set to **Shared** in the hardware profile.</span></span> <span data-ttu-id="1a669-296">发送打开命令时，此设置阻止 POS 检查银箱是否已打开。</span><span class="sxs-lookup"><span data-stu-id="1a669-296">This setting prevents the POS from checking whether the cash drawer is already open when it sends open commands.</span></span>
- <span data-ttu-id="1a669-297">**收据打印机** – 如果同时向硬件工作站发送两条收据打印命令，可能丢失其中一条命令，具体取决于设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-297">**Receipt printer** – If two receipt printing commands are sent to the hardware station at the same time, one of the commands can be lost, depending on the device.</span></span> <span data-ttu-id="1a669-298">某些设备有内存或池，可以防止此问题。</span><span class="sxs-lookup"><span data-stu-id="1a669-298">Some devices have internal memory or pooling that can prevent this issue.</span></span> <span data-ttu-id="1a669-299">如果打印命令不成功，收银员将收到错误消息，可以从 POS 重试该打印命令。</span><span class="sxs-lookup"><span data-stu-id="1a669-299">If a print command isn't successful, the cashier receives an error message and can retry the print command from the POS.</span></span>
- <span data-ttu-id="1a669-300">**付款终端** – 如果收银员尝试在已在使用的付款终端上处理交易的支付，将显示消息，通知收银员正在使用该终端，请收银员稍后重试。</span><span class="sxs-lookup"><span data-stu-id="1a669-300">**Payment terminal** – If a cashier tries to tender a transaction on a payment terminal that is already being used, a message notifies the cashier that the terminal is being used and asks the cashier to try again later.</span></span> <span data-ttu-id="1a669-301">通常，收银员可以看到终端已在使用并等待其他交易完成，再尝试处理付款。</span><span class="sxs-lookup"><span data-stu-id="1a669-301">Usually, cashiers can see that a terminal is already being used and will wait until the other transaction is completed before they try to tender again.</span></span>

<span data-ttu-id="1a669-302">为将来的版本计划了验证，以便检测是否为映射到共享硬件工作站的硬件配置文件设置了不受支持的设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-302">Validation is planned for a future release, to detect whether unsupported devices are set up for a hardware profile that is mapped to a shared hardware station.</span></span> <span data-ttu-id="1a669-303">如果检测到不受支持的设备，用户将收到消息，说明共享硬件工作站不支持这些设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-303">If any unsupported devices are detected, the user will receive a message that states that the devices aren't supported for shared hardware stations.</span></span> <span data-ttu-id="1a669-304">对于共享硬件工作站，**付款后即可选择**选项在收银机级别设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="1a669-304">In the case of shared hardware stations, the **Select upon tendering** option is set to **Yes** at the register level.</span></span> <span data-ttu-id="1a669-305">然后在 POS 中为交易选择了付款时，将提示 POS 用户选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-305">The POS user is then prompted to select a hardware station when a tender is selected for a transaction at the POS.</span></span> <span data-ttu-id="1a669-306">仅在付款时选择了硬件工作站时，将把对硬件工作站的选择直接添加到移动方案的 POS 工作流。</span><span class="sxs-lookup"><span data-stu-id="1a669-306">When the hardware station is selected only at the time of tender, the hardware station selection is added directly to the POS workflow for mobile scenarios.</span></span> <span data-ttu-id="1a669-307">额外福利是，付款终端上的行显示器不用于共享方案。</span><span class="sxs-lookup"><span data-stu-id="1a669-307">As an additional benefit, the line display on the payment terminal isn't used for shared scenarios.</span></span> <span data-ttu-id="1a669-308">如果付款终端用作行显示器，交易完成前，可能阻止其他用户使用该终端。</span><span class="sxs-lookup"><span data-stu-id="1a669-308">If the payment terminal is used as a line display, other users might be blocked from using that terminal until the transaction is completed.</span></span> <span data-ttu-id="1a669-309">在移动方案中，可能在较长一段时间内向交易添加行。</span><span class="sxs-lookup"><span data-stu-id="1a669-309">In mobile scenarios, lines might be added to a transaction over a longer period.</span></span> <span data-ttu-id="1a669-310">因此，需要**付款后即可选择**选项以确保最适宜的设备可用性。</span><span class="sxs-lookup"><span data-stu-id="1a669-310">Therefore, the **Select upon tendering** option is required in order to ensure optimum device availability.</span></span>

### <a name="network-peripherals"></a><span data-ttu-id="1a669-311">网络外设</span><span class="sxs-lookup"><span data-stu-id="1a669-311">Network peripherals</span></span>

<span data-ttu-id="1a669-312">硬件配置文件中为设备指派的网络让银箱、收据打印机和付款终端可以通过网络连接来连接。</span><span class="sxs-lookup"><span data-stu-id="1a669-312">The network designation for devices in the hardware profile enables cash drawers, receipt printers, and payment terminals to be connected via a network connection.</span></span>

#### <a name="modern-pos-for-windows"></a><span data-ttu-id="1a669-313">Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="1a669-313">Modern POS for Windows</span></span>

<span data-ttu-id="1a669-314">可以为两处的网络外设指定 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1a669-314">You can specify IP addresses for network peripherals in two places.</span></span> <span data-ttu-id="1a669-315">如果 Modern POS Windows 客户端使用一组网络外设，您应该通过使用收银机自身的“操作窗格”上的 **IP 配置**选项为这些设备设置 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1a669-315">If the Modern POS Windows client is using a single set of network peripherals, you should set the IP addresses for those devices by using the **IP configuration** option on the Action Pane for the register itself.</span></span> <span data-ttu-id="1a669-316">对于将在 POS 收银机之间共享的网络设备，可以将为其指派的硬件配置文件直接映射到共享硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-316">In the case of network devices that will be shared among POS registers, a hardware profile that has network devices assigned to it can be mapped directly to a shared hardware station.</span></span> <span data-ttu-id="1a669-317">若要分配 IP 地址，请在**零售商店**页中选择该硬件工作站，然后使用**硬件工作站**部分中的 **IP 配置**选项指定为该硬件工作站分配的网络设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-317">To assign IP addresses, select that hardware station on the **Retail stores** page, and then use the **IP configuration** option in the **Hardware stations** section to specify the network devices that are assigned to that hardware station.</span></span> <span data-ttu-id="1a669-318">对于只有网络设备的硬件工作站，则不必部署硬件工作站本身。</span><span class="sxs-lookup"><span data-stu-id="1a669-318">For hardware stations that have only network devices, you don't have to deploy the hardware station itself.</span></span> <span data-ttu-id="1a669-319">在这种情况下，仅当要在概念上根据可网络寻址的设备在零售商店中的位置为这些设备分组时，才需要硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-319">In this case, the hardware station is required only in order to conceptually group network-addressable devices according to their location in the retail store.</span></span>

#### <a name="modern-pos-for-android"></a><span data-ttu-id="1a669-320">Modern POS for Android</span><span class="sxs-lookup"><span data-stu-id="1a669-320">Modern POS for Android</span></span>

<span data-ttu-id="1a669-321">从 Dynamics 365 for Retail 版本 8.1.3 开始，Modern POS for Android 应用程序中包含内置 IPC 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-321">As of Dynamics 365 for Retail version 8.1.3, the Modern POS for Android application includes a built-in IPC hardware station.</span></span> <span data-ttu-id="1a669-322">此硬件工作站支持与网络打印机和付款连接器通信。</span><span class="sxs-lookup"><span data-stu-id="1a669-322">This hardware station supports communicating with network printers and payment connectors.</span></span> <span data-ttu-id="1a669-323">有关详细信息，请访问 [适用于 Android docs 的 Hybrid 应用文章](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/hybridapp#dedicated-hardware-station-support-for-the-hybrid-android-app)。</span><span class="sxs-lookup"><span data-stu-id="1a669-323">For more information, visit the [Hybrid app for Android docs article](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/hybridapp#dedicated-hardware-station-support-for-the-hybrid-android-app).</span></span> 

#### <a name="cloud-pos-and-modern-pos-for-ios"></a><span data-ttu-id="1a669-324">Cloud POS 和 Modern POS for iOS</span><span class="sxs-lookup"><span data-stu-id="1a669-324">Cloud POS and Modern POS for iOS</span></span>

<span data-ttu-id="1a669-325">硬件工作站中包含驱动以物理方式相连且可网络寻址的外设的逻辑。</span><span class="sxs-lookup"><span data-stu-id="1a669-325">The logic that drives physically connected and network-addressable peripherals is contained in the hardware station.</span></span> <span data-ttu-id="1a669-326">因此，对于除 Modern POS for Windows 之外的所有 POS 客户端，必须部署并激活 IIS 硬件工作站，以便让 POS 可以与外设通信，无论这些外设是以物理方式连接到硬件工作站还是通过网络寻址。</span><span class="sxs-lookup"><span data-stu-id="1a669-326">Therefore, for all POS clients except Modern POS for Windows, an IIS hardware station must be deployed and active to enable the POS to communicate with peripherals, regardless of whether those peripherals are physically connected to a hardware station or addressed over the network.</span></span>

## <a name="setup-and-configuration"></a><span data-ttu-id="1a669-327">设置和配置</span><span class="sxs-lookup"><span data-stu-id="1a669-327">Setup and configuration</span></span>

### <a name="hardware-station-installation"></a><span data-ttu-id="1a669-328">硬件工作站安装</span><span class="sxs-lookup"><span data-stu-id="1a669-328">Hardware station installation</span></span>

<span data-ttu-id="1a669-329">有关新信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-329">For information, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>

### <a name="modern-pos-for-windows-setup-and-configuration"></a><span data-ttu-id="1a669-330">Modern POS for Windows 设置和配置</span><span class="sxs-lookup"><span data-stu-id="1a669-330">Modern POS for Windows setup and configuration</span></span>

<span data-ttu-id="1a669-331">有关信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-331">For information, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>

### <a name="opos-device-setup-and-configuration"></a><span data-ttu-id="1a669-332">OPOS 设备设置和配置</span><span class="sxs-lookup"><span data-stu-id="1a669-332">OPOS device setup and configuration</span></span>

<span data-ttu-id="1a669-333">有关 OPOS 组件的详细信息，请参阅本文的“支持的接口”。</span><span class="sxs-lookup"><span data-stu-id="1a669-333">For more information about OPOS components, see the "Supported interfaces" section of this document.</span></span> <span data-ttu-id="1a669-334">OPOS 驱动程序通常由设备制造商提供。</span><span class="sxs-lookup"><span data-stu-id="1a669-334">Typically, OPOS drivers are provided by the device manufacturer.</span></span> <span data-ttu-id="1a669-335">安装 OPOS 设备驱动程序时，将在 Windows 注册表中的以下位置添加一个键：</span><span class="sxs-lookup"><span data-stu-id="1a669-335">When an OPOS device driver is installed, it adds a key to the Windows registry in one of the following locations:</span></span>

- <span data-ttu-id="1a669-336">**32 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-336">**32-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span></span>
- <span data-ttu-id="1a669-337">**64 位系统：** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-337">**64-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span></span>

<span data-ttu-id="1a669-338">在 ServiceOPOS 注册表位置中，配置的设备根据 OPOS 设备类组织。</span><span class="sxs-lookup"><span data-stu-id="1a669-338">Within the ServiceOPOS registry location, configured devices are organized according to the OPOS device class.</span></span> <span data-ttu-id="1a669-339">将保存多个设备驱动程序。</span><span class="sxs-lookup"><span data-stu-id="1a669-339">Multiple device drivers are saved.</span></span>

## <a name="supported-scenarios-by-hardware-station-type"></a><span data-ttu-id="1a669-340">硬件工作站类型支持的方案</span><span class="sxs-lookup"><span data-stu-id="1a669-340">Supported scenarios by hardware station type</span></span>

### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a><span data-ttu-id="1a669-341">客户端支持 – IPC 硬件工作站与 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-341">Client support – IPC hardware station vs. IIS hardware station</span></span>

<span data-ttu-id="1a669-342">下表显示支持的拓扑和部署方案。</span><span class="sxs-lookup"><span data-stu-id="1a669-342">The following table shows the topologies and deployment scenarios that are supported.</span></span>

| <span data-ttu-id="1a669-343">客户</span><span class="sxs-lookup"><span data-stu-id="1a669-343">Client</span></span>      | <span data-ttu-id="1a669-344">IPC 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-344">IPC hardware station</span></span> | <span data-ttu-id="1a669-345">IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-345">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="1a669-346">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="1a669-346">Windows app</span></span> | <span data-ttu-id="1a669-347">是</span><span class="sxs-lookup"><span data-stu-id="1a669-347">Yes</span></span>                  | <span data-ttu-id="1a669-348">是</span><span class="sxs-lookup"><span data-stu-id="1a669-348">Yes</span></span>                  |
| <span data-ttu-id="1a669-349">云 POS</span><span class="sxs-lookup"><span data-stu-id="1a669-349">Cloud POS</span></span>   | <span data-ttu-id="1a669-350">否</span><span class="sxs-lookup"><span data-stu-id="1a669-350">No</span></span>                   | <span data-ttu-id="1a669-351">是</span><span class="sxs-lookup"><span data-stu-id="1a669-351">Yes</span></span>                  |
| <span data-ttu-id="1a669-352">Android</span><span class="sxs-lookup"><span data-stu-id="1a669-352">Android</span></span>     | <span data-ttu-id="1a669-353">是</span><span class="sxs-lookup"><span data-stu-id="1a669-353">Yes</span></span>                  | <span data-ttu-id="1a669-354">是</span><span class="sxs-lookup"><span data-stu-id="1a669-354">Yes</span></span>                  |
| <span data-ttu-id="1a669-355">iOS</span><span class="sxs-lookup"><span data-stu-id="1a669-355">iOS</span></span>         | <span data-ttu-id="1a669-356">否</span><span class="sxs-lookup"><span data-stu-id="1a669-356">No</span></span>                   | <span data-ttu-id="1a669-357">是</span><span class="sxs-lookup"><span data-stu-id="1a669-357">Yes</span></span>                  |

### <a name="network-peripherals"></a><span data-ttu-id="1a669-358">网络外设</span><span class="sxs-lookup"><span data-stu-id="1a669-358">Network peripherals</span></span>

<span data-ttu-id="1a669-359">可以直接通过 Modern POS for Windows 应用程序中内置的硬件工作站支持网络外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-359">Network peripherals can be supported directly through the hardware station that is built into the Modern POS for Windows application.</span></span> <span data-ttu-id="1a669-360">对于其他所有客户端，则必须部署 IIS 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-360">For all other clients, you must deploy an IIS hardware station.</span></span>

| <span data-ttu-id="1a669-361">客户</span><span class="sxs-lookup"><span data-stu-id="1a669-361">Client</span></span>      | <span data-ttu-id="1a669-362">IPC 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-362">IPC hardware station</span></span> | <span data-ttu-id="1a669-363">IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-363">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="1a669-364">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="1a669-364">Windows app</span></span> | <span data-ttu-id="1a669-365">是</span><span class="sxs-lookup"><span data-stu-id="1a669-365">Yes</span></span>                  | <span data-ttu-id="1a669-366">是</span><span class="sxs-lookup"><span data-stu-id="1a669-366">Yes</span></span>                  |
| <span data-ttu-id="1a669-367">云 POS</span><span class="sxs-lookup"><span data-stu-id="1a669-367">Cloud POS</span></span>   | <span data-ttu-id="1a669-368">否</span><span class="sxs-lookup"><span data-stu-id="1a669-368">No</span></span>                   | <span data-ttu-id="1a669-369">是</span><span class="sxs-lookup"><span data-stu-id="1a669-369">Yes</span></span>                  |
| <span data-ttu-id="1a669-370">Android</span><span class="sxs-lookup"><span data-stu-id="1a669-370">Android</span></span>     | <span data-ttu-id="1a669-371">是</span><span class="sxs-lookup"><span data-stu-id="1a669-371">Yes</span></span>                  | <span data-ttu-id="1a669-372">是</span><span class="sxs-lookup"><span data-stu-id="1a669-372">Yes</span></span>                  |
| <span data-ttu-id="1a669-373">iOS</span><span class="sxs-lookup"><span data-stu-id="1a669-373">iOS</span></span>         | <span data-ttu-id="1a669-374">否</span><span class="sxs-lookup"><span data-stu-id="1a669-374">No</span></span>                   | <span data-ttu-id="1a669-375">是</span><span class="sxs-lookup"><span data-stu-id="1a669-375">Yes</span></span>                  |

## <a name="supported-device-types-by-hardware-station-type"></a><span data-ttu-id="1a669-376">硬件工作站类型支持的设备类型</span><span class="sxs-lookup"><span data-stu-id="1a669-376">Supported device types by hardware station type</span></span>

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="1a669-377">带 IPC（内置）硬件工作站的 Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="1a669-377">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1a669-378">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="1a669-378">Supported device class</span></span></th>
<th><span data-ttu-id="1a669-379">支持的接口</span><span class="sxs-lookup"><span data-stu-id="1a669-379">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1a669-380">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-380">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-381">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-381">OPOS</span></span></li>
<li><span data-ttu-id="1a669-382">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-382">Windows driver</span></span></li>
<li><span data-ttu-id="1a669-383">设备</span><span class="sxs-lookup"><span data-stu-id="1a669-383">Device</span></span></li>
<li><span data-ttu-id="1a669-384">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-384">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-385">打印机 2</span><span class="sxs-lookup"><span data-stu-id="1a669-385">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-386">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-386">OPOS</span></span></li>
<li><span data-ttu-id="1a669-387">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-387">Windows driver</span></span></li>
<li><span data-ttu-id="1a669-388">设备</span><span class="sxs-lookup"><span data-stu-id="1a669-388">Device</span></span></li>
<li><span data-ttu-id="1a669-389">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-389">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-390">行显示内容</span><span class="sxs-lookup"><span data-stu-id="1a669-390">Line display</span></span></td>
<td><span data-ttu-id="1a669-391">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-391">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-392">双显示器</span><span class="sxs-lookup"><span data-stu-id="1a669-392">Dual display</span></span></td>
<td><span data-ttu-id="1a669-393">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-393">Windows driver</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-394">MSR</span><span class="sxs-lookup"><span data-stu-id="1a669-394">MSR</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-395">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-395">OPOS</span></span></li>
<li><span data-ttu-id="1a669-396">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="1a669-396">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="1a669-397">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="1a669-397">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-398">开票人</span><span class="sxs-lookup"><span data-stu-id="1a669-398">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-399">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-399">OPOS</span></span></li>
<li><span data-ttu-id="1a669-400">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-400">Network</span></span>
<p><span data-ttu-id="1a669-401"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-401"><strong>Note:</strong> Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-402">开票人 2</span><span class="sxs-lookup"><span data-stu-id="1a669-402">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-403">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-403">OPOS</span></span></li>
<li><span data-ttu-id="1a669-404">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-404">Network</span></span>
<p><span data-ttu-id="1a669-405"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-405"><strong>Note:</strong> Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-406">扫描仪</span><span class="sxs-lookup"><span data-stu-id="1a669-406">Scanner</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-407">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-407">OPOS</span></span></li>
<li><span data-ttu-id="1a669-408">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="1a669-408">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="1a669-409">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="1a669-409">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-410">扫描仪 2</span><span class="sxs-lookup"><span data-stu-id="1a669-410">Scanner 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-411">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-411">OPOS</span></span></li>
<li><span data-ttu-id="1a669-412">UWP（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="1a669-412">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="1a669-413">键盘 wedge（不需要设置。）</span><span class="sxs-lookup"><span data-stu-id="1a669-413">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-414">比例</span><span class="sxs-lookup"><span data-stu-id="1a669-414">Scale</span></span></td>
<td><span data-ttu-id="1a669-415">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-415">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-416">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="1a669-416">PIN pad</span></span></td>
<td><span data-ttu-id="1a669-417">OPOS（通过自定义付款连接器提供支持。）</span><span class="sxs-lookup"><span data-stu-id="1a669-417">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-418">签名捕获</span><span class="sxs-lookup"><span data-stu-id="1a669-418">Signature capture</span></span></td>
<td><span data-ttu-id="1a669-419">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-419">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-420">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-420">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-421">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="1a669-421">Custom device support</span></span></li>
<li><span data-ttu-id="1a669-422">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="1a669-422">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a><span data-ttu-id="1a669-423">有专用 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="1a669-423">All Modern POS clients that have a dedicated IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-424">当 IIS 硬件工作站为“专用”时，POS 客户端与硬件工作站之间存在一对一关系。</span><span class="sxs-lookup"><span data-stu-id="1a669-424">When the IIS hardware station is "dedicated," there is a one-to-one relationship between the POS client and the hardware station.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1a669-425">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="1a669-425">Supported device class</span></span></th>
<th><span data-ttu-id="1a669-426">支持的接口</span><span class="sxs-lookup"><span data-stu-id="1a669-426">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1a669-427">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-427">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-428">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-428">OPOS</span></span></li>
<li><span data-ttu-id="1a669-429">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-429">Windows driver</span></span>
<p><span data-ttu-id="1a669-430"><strong>注意</strong>：对于网络中的 Windows 打印机，硬件工作站的用户必须有权访问该打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-430"><strong>Note:</strong> For Windows printers on a network, the user of the hardware station must have permission to access the printer.</span></span></p>
</li>
<li><span data-ttu-id="1a669-431">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-431">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-432">打印机 2</span><span class="sxs-lookup"><span data-stu-id="1a669-432">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-433">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-433">OPOS</span></span></li>
<li><span data-ttu-id="1a669-434">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-434">Windows driver</span></span></li>
<li><span data-ttu-id="1a669-435">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-435">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-436">行显示内容</span><span class="sxs-lookup"><span data-stu-id="1a669-436">Line display</span></span></td>
<td><span data-ttu-id="1a669-437">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-437">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-438">MSR</span><span class="sxs-lookup"><span data-stu-id="1a669-438">MSR</span></span></td>
<td><span data-ttu-id="1a669-439">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-439">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-440">开票人</span><span class="sxs-lookup"><span data-stu-id="1a669-440">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-441">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-441">OPOS</span></span></li>
<li><span data-ttu-id="1a669-442">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-442">Network</span></span>
<p><span data-ttu-id="1a669-443"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-443"><strong>Note:</strong> Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-444">开票人 2</span><span class="sxs-lookup"><span data-stu-id="1a669-444">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-445">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-445">OPOS</span></span></li>
<li><span data-ttu-id="1a669-446">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-446">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-447">扫描仪</span><span class="sxs-lookup"><span data-stu-id="1a669-447">Scanner</span></span></td>
<td><span data-ttu-id="1a669-448">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-448">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-449">扫描仪 2</span><span class="sxs-lookup"><span data-stu-id="1a669-449">Scanner 2</span></span></td>
<td><span data-ttu-id="1a669-450">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-450">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-451">比例</span><span class="sxs-lookup"><span data-stu-id="1a669-451">Scale</span></span></td>
<td><span data-ttu-id="1a669-452">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-452">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-453">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="1a669-453">PIN pad</span></span></td>
<td><span data-ttu-id="1a669-454">OPOS（通过自定义付款连接器提供支持。）</span><span class="sxs-lookup"><span data-stu-id="1a669-454">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-455">签到</span><span class="sxs-lookup"><span data-stu-id="1a669-455">Sig.</span></span> <span data-ttu-id="1a669-456">捕获</span><span class="sxs-lookup"><span data-stu-id="1a669-456">capture</span></span></td>
<td><span data-ttu-id="1a669-457">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-457">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1a669-458">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-458">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-459">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="1a669-459">Custom device support</span></span></li>
<li><span data-ttu-id="1a669-460">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="1a669-460">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="1a669-461">有共享 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="1a669-461">All Modern POS clients that have a shared IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-462">当 IIS 硬件工作站为“共享”时，多台设备可同时使用该硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-462">When the IIS hardware station is "shared," multiple devices can use the hardware station at the same time.</span></span> <span data-ttu-id="1a669-463">对于此方案，应仅使用下表中列出的设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-463">For this scenario, you should use only the devices that are listed in the following table.</span></span> <span data-ttu-id="1a669-464">如果尝试共享此处未列出的设备（如条码扫描仪和 MSR），多台设备尝试声明同一外设时，将出错。</span><span class="sxs-lookup"><span data-stu-id="1a669-464">If you try to share devices that aren't listed here, such as bar code scanners and MSRs, errors will occur when multiple devices try to claim the same peripheral.</span></span> <span data-ttu-id="1a669-465">将来将明确阻止此类配置。</span><span class="sxs-lookup"><span data-stu-id="1a669-465">In the future, such a configuration will be explicitly prevented.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1a669-466">支持的设备类</span><span class="sxs-lookup"><span data-stu-id="1a669-466">Supported device class</span></span></th>
<th><span data-ttu-id="1a669-467">支持的接口</span><span class="sxs-lookup"><span data-stu-id="1a669-467">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1a669-468">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-468">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-469">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-469">OPOS</span></span></li>
<li><span data-ttu-id="1a669-470">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-470">Windows driver</span></span>
<p><span data-ttu-id="1a669-471"><strong>注意</strong>：对于网络中的 Windows 打印机，硬件工作站的用户必须有权访问该打印机。</span><span class="sxs-lookup"><span data-stu-id="1a669-471"><strong>Note:</strong> For Windows printers on a network, the user of the hardware station must have permission to access the printer.</span></span></p>
</li>
<li><span data-ttu-id="1a669-472">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-472">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-473">打印机 2</span><span class="sxs-lookup"><span data-stu-id="1a669-473">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-474">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-474">OPOS</span></span></li>
<li><span data-ttu-id="1a669-475">Windows 驱动程序</span><span class="sxs-lookup"><span data-stu-id="1a669-475">Windows driver</span></span></li>
<li><span data-ttu-id="1a669-476">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-476">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-477">开票人</span><span class="sxs-lookup"><span data-stu-id="1a669-477">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-478">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-478">OPOS</span></span></li>
<li><span data-ttu-id="1a669-479">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-479">Network</span></span>
<p><span data-ttu-id="1a669-480"><strong>注意</strong>：如果为银箱设置<strong>使用共享班次</strong>，则每个硬件配置文件只能设置一个银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-480"><strong>Note:</strong> Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-481">开票人 2</span><span class="sxs-lookup"><span data-stu-id="1a669-481">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-482">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-482">OPOS</span></span></li>
<li><span data-ttu-id="1a669-483">网络</span><span class="sxs-lookup"><span data-stu-id="1a669-483">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1a669-484">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-484">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1a669-485">自定义设备支持</span><span class="sxs-lookup"><span data-stu-id="1a669-485">Custom device support</span></span></li>
<li><span data-ttu-id="1a669-486">网络（有关详细信息，请参阅付款连接器文档。）</span><span class="sxs-lookup"><span data-stu-id="1a669-486">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a><span data-ttu-id="1a669-487">支持的方案的配置</span><span class="sxs-lookup"><span data-stu-id="1a669-487">Configuration for supported scenarios</span></span>

<span data-ttu-id="1a669-488">有关如何创建硬件配置文件的详细信息，请参阅[定义和维护渠道客户端，包括收银机和硬件工作站](define-maintain-channel-clients-registers-hw-stations.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-488">For more information about how to create hardware profiles, see [Define and maintain channel clients, including registers and hardware stations](define-maintain-channel-clients-registers-hw-stations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-489">对于 Microsoft Dynamics 365 for Retail 版本 1611，将不再使用硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-489">For Microsoft Dynamics 365 for Retail version 1611, the hardware station profile is no longer used.</span></span> <span data-ttu-id="1a669-490">以前在硬件工作站中设置的属性现在成为了硬件工作站本身的一部分。</span><span class="sxs-lookup"><span data-stu-id="1a669-490">Attributes that you previously set up in the hardware station profile are now part of the hardware station itself.</span></span>

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="1a669-491">带 IPC（内置）硬件工作站的 Modern POS for Windows</span><span class="sxs-lookup"><span data-stu-id="1a669-491">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<span data-ttu-id="1a669-492">此配置是传统固定式 POS 收银机最典型的配置。</span><span class="sxs-lookup"><span data-stu-id="1a669-492">This configuration is the most typical configuration for traditional, fixed POS registers.</span></span> <span data-ttu-id="1a669-493">对于此方案，硬件配置文件信息直接映射到收银机。</span><span class="sxs-lookup"><span data-stu-id="1a669-493">For this scenario, the hardware profile information is mapped directly to the register itself.</span></span> <span data-ttu-id="1a669-494">还必须在收银机本身中设置 EFT 终端号。</span><span class="sxs-lookup"><span data-stu-id="1a669-494">The EFT terminal number should also be set on the register itself.</span></span> <span data-ttu-id="1a669-495">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1a669-495">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="1a669-496">创建在其中配置所有所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-496">Create a hardware profile where all the required peripherals are configured.</span></span>
2. <span data-ttu-id="1a669-497">将硬件配置文件映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="1a669-497">Map the hardware profile to the POS register.</span></span>
3. <span data-ttu-id="1a669-498">为将使用该 POS 收银机的零售商店创建一个类型为**专用**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-498">Create a hardware station of the **Dedicated** type for the retail store where the POS register will be used.</span></span> <span data-ttu-id="1a669-499">描述可选。</span><span class="sxs-lookup"><span data-stu-id="1a669-499">A description is optional.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a669-500">不必在硬件工作站中设置其他任何属性。</span><span class="sxs-lookup"><span data-stu-id="1a669-500">You don't have to set any other properties on the hardware station.</span></span> <span data-ttu-id="1a669-501">其他所有所需信息（如硬件配置文件）将来自收银机本身。</span><span class="sxs-lookup"><span data-stu-id="1a669-501">All other required information, such as the hardware profile, will come from the register itself.</span></span>

4. <span data-ttu-id="1a669-502">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="1a669-502">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
5. <span data-ttu-id="1a669-503">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="1a669-503">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="1a669-504">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-504">Click **Run now** to sync changes to the POS.</span></span>
6. <span data-ttu-id="1a669-505">选择 **1070** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="1a669-505">Select the **1070** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="1a669-506">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-506">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="1a669-507">安装并激活 Modern POS for Windows。</span><span class="sxs-lookup"><span data-stu-id="1a669-507">Install and activate Modern POS for Windows.</span></span>
8. <span data-ttu-id="1a669-508">启动 Modern POS for Windows，然后登录到连接的外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-508">Start Modern POS for Windows, and begin to use the connected peripheral devices.</span></span>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a><span data-ttu-id="1a669-509">有专用 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="1a669-509">All Modern POS clients that have a dedicated IIS hardware station</span></span>

<span data-ttu-id="1a669-510">可将此配置用于有一个硬件工作站仅供一台 POS 收银机专用的所有 Modern POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="1a669-510">This configuration can be used for all Modern POS clients that have a hardware station that is used exclusively by one POS register.</span></span> <span data-ttu-id="1a669-511">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1a669-511">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="1a669-512">创建在其中配置所有所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-512">Create a hardware profile where all the required peripherals are configured.</span></span>
2. <span data-ttu-id="1a669-513">为将使用该 POS 收银机的零售商店创建一个类型为**专用**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-513">Create a hardware station of the **Dedicated** type for the retail store where the POS register will be used.</span></span>
3. <span data-ttu-id="1a669-514">在专用硬件工作站中，设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="1a669-514">On the dedicated hardware station, set the following properties:</span></span>

    - <span data-ttu-id="1a669-515">**主机名** – 将运行硬件工作站的主计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="1a669-515">**Host name** – The name of the host computer where the hardware station will run.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1a669-516">Cloud POS 可以解析 **localhost** 以确定运行 Cloud POS 的本地计算机。</span><span class="sxs-lookup"><span data-stu-id="1a669-516">Cloud POS can resolve **localhost** to determine the local computer where Cloud POS is running.</span></span> <span data-ttu-id="1a669-517">但是，将 Cloud POS 与硬件工作站配对所需证书必须也采用“Localhost”来充当计算机名称。</span><span class="sxs-lookup"><span data-stu-id="1a669-517">However, the certificate that is required in order to pair Cloud POS with the hardware station must also have "Localhost" as the computer name.</span></span> <span data-ttu-id="1a669-518">若要避免问题，建议您根据列出商店每个专用硬件工作站的实例。</span><span class="sxs-lookup"><span data-stu-id="1a669-518">To avoid issues, we recommend that you list an instance of each dedicated hardware station for the store, as required.</span></span> <span data-ttu-id="1a669-519">对于每个硬件工作站，主机名应该是将部署硬件工作站的具体计算机名称。</span><span class="sxs-lookup"><span data-stu-id="1a669-519">For each hardware station, the host name should be the specific computer name where the hardware station will be deployed.</span></span>

    - <span data-ttu-id="1a669-520">**端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。</span><span class="sxs-lookup"><span data-stu-id="1a669-520">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    - <span data-ttu-id="1a669-521">**硬件配置文件** – 如果硬件工作站本身中不提供硬件配置文件，将使用为收银机分配的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-521">**Hardware profile** – If the hardware profile isn't provided on the hardware station itself, the hardware profile that is assigned to the register will be used.</span></span>
    - <span data-ttu-id="1a669-522">**EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="1a669-522">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="1a669-523">此 ID 由信用卡处理方提供。</span><span class="sxs-lookup"><span data-stu-id="1a669-523">This ID is provided by the credit card processor.</span></span>
    - <span data-ttu-id="1a669-524">**包名** – 部署硬件工作站时要使用的硬件工作站包。</span><span class="sxs-lookup"><span data-stu-id="1a669-524">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4. <span data-ttu-id="1a669-525">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="1a669-525">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
5. <span data-ttu-id="1a669-526">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="1a669-526">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="1a669-527">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-527">Click **Run now** to sync changes to the POS.</span></span>
6. <span data-ttu-id="1a669-528">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="1a669-528">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="1a669-529">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-529">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="1a669-530">安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-530">Install the hardware station.</span></span> <span data-ttu-id="1a669-531">有关如何安装硬件工作站的详细信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-531">For more information about how to install the hardware station, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>
8. <span data-ttu-id="1a669-532">安装和激活 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-532">Install and activate Modern POS.</span></span> <span data-ttu-id="1a669-533">有关如何安装 Modern POS 的详细信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-533">For more information about how to install Modern POS, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>
9. <span data-ttu-id="1a669-534">登录 Modern POS，然后选择**执行非开票人操作**。</span><span class="sxs-lookup"><span data-stu-id="1a669-534">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
10. <span data-ttu-id="1a669-535">启动**管理硬件工作站**操作。</span><span class="sxs-lookup"><span data-stu-id="1a669-535">Start the **Manage hardware stations** operation.</span></span>
11. <span data-ttu-id="1a669-536">单击**管理**。</span><span class="sxs-lookup"><span data-stu-id="1a669-536">Click **Manage**.</span></span>
12. <span data-ttu-id="1a669-537">在硬件工作站管理页中，设置用于打开硬件工作站的选项。</span><span class="sxs-lookup"><span data-stu-id="1a669-537">On the hardware station management page, set the option to turn on the hardware station.</span></span>
13. <span data-ttu-id="1a669-538">选择要使用的硬件工作站，然后单击**配对**。</span><span class="sxs-lookup"><span data-stu-id="1a669-538">Select the hardware station to use, and then click **Pair**.</span></span>
14. <span data-ttu-id="1a669-539">在硬件工作站配对后，单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="1a669-539">After the hardware station is paired, click **Close**.</span></span>
15. <span data-ttu-id="1a669-540">在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。</span><span class="sxs-lookup"><span data-stu-id="1a669-540">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="1a669-541">有共享 IIS 硬件工作站的所有 Modern POS 客户端</span><span class="sxs-lookup"><span data-stu-id="1a669-541">All Modern POS clients that have a shared IIS hardware station</span></span>

<span data-ttu-id="1a669-542">此配置可用于与其他设备共享硬件工作站的所有 Modern POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="1a669-542">This configuration can be used for all Modern POS clients that share hardware stations with other devices.</span></span> <span data-ttu-id="1a669-543">若要设置此配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1a669-543">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="1a669-544">创建在其中配置所需外设的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-544">Create a hardware profile where the required peripherals are configured.</span></span>
2. <span data-ttu-id="1a669-545">为将使用该 POS 收银机的零售商店创建一个类型为**共享**的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-545">Create a hardware station of the **Shared** type for the retail store where the POS register will be used.</span></span>
3. <span data-ttu-id="1a669-546">在共享硬件工作站中，设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="1a669-546">On the shared hardware station, set the following properties:</span></span>

    - <span data-ttu-id="1a669-547">**主机名** – 将运行硬件工作站的主计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="1a669-547">**Host name** – The name of the host computer where the hardware station will run.</span></span>
    - <span data-ttu-id="1a669-548">**描述** – 用于帮助识别硬件工作站的文本，如**退货**或**店前**。</span><span class="sxs-lookup"><span data-stu-id="1a669-548">**Description** – Text that will help identify the hardware station, such as **Returns** or **Front of store**.</span></span>
    - <span data-ttu-id="1a669-549">**端口** – 硬件工作站用于与 Modern POS 客户端通信的端口。</span><span class="sxs-lookup"><span data-stu-id="1a669-549">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    - <span data-ttu-id="1a669-550">**硬件配置文件** – 对于共享硬件工作站，每个硬件工作站都应该有一个硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="1a669-550">**Hardware profile** – For shared hardware stations, each hardware station should have a hardware profile.</span></span> <span data-ttu-id="1a669-551">可以在硬件工作站之间共享硬件配置文件，但必须将其映射到每个硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-551">Hardware profiles can be shared among hardware stations, but they must be mapped to each hardware station.</span></span> <span data-ttu-id="1a669-552">此外，建议在多个设备共享同一个共享硬件工作站时使用共享班次。</span><span class="sxs-lookup"><span data-stu-id="1a669-552">In addition, we recommend that you use shared shifts when multiple devices use the same shared hardware station.</span></span> <span data-ttu-id="1a669-553">若要设置共享班次，单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="1a669-553">To set up a shared shift, click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="1a669-554">对于每个共享硬件配置文件，选择银箱，然后将**共享班次银箱**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="1a669-554">For each shared hardware profile, select the cash drawer, and set the **Shared shift drawer** option to **Yes**.</span></span>
    - <span data-ttu-id="1a669-555">**EFT POS 号** – 发送 EFT 授权时使用的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="1a669-555">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="1a669-556">此 ID 由信用卡处理方提供。</span><span class="sxs-lookup"><span data-stu-id="1a669-556">This ID is provided by the credit card processor.</span></span>
    - <span data-ttu-id="1a669-557">**包名** – 部署硬件工作站时要使用的硬件工作站包。</span><span class="sxs-lookup"><span data-stu-id="1a669-557">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4. <span data-ttu-id="1a669-558">为商店中所需其他每个硬件工作站重复步骤 2 和 3。</span><span class="sxs-lookup"><span data-stu-id="1a669-558">Repeat steps 2 and 3 for each additional hardware station that is required in the store.</span></span>
5. <span data-ttu-id="1a669-559">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="1a669-559">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="1a669-560">选择 **1090** 配送计划，将新硬件配置文件同步到商店。</span><span class="sxs-lookup"><span data-stu-id="1a669-560">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="1a669-561">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-561">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="1a669-562">选择 **1040** 配送计划，将新硬件工作站同步到商店。</span><span class="sxs-lookup"><span data-stu-id="1a669-562">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="1a669-563">单击**立即运行**将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-563">Click **Run now** to sync changes to the POS.</span></span>
8. <span data-ttu-id="1a669-564">在步骤 2 和 3 中设置的每个主机上安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-564">Install the hardware station on each host computer that you set up in steps 2 and 3.</span></span> <span data-ttu-id="1a669-565">有关如何安装硬件工作站的详细信息，请参阅 [Retail 硬件工作站配置和安装](retail-hardware-station-configuration-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-565">For more information about how to install the hardware station, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>
9. <span data-ttu-id="1a669-566">安装和激活 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-566">Install and activate Modern POS.</span></span> <span data-ttu-id="1a669-567">有关如何安装 Modern POS 的详细信息，请参阅 [Retail Modern POS 配置和安装](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-567">For more information about how to install Modern POS, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>
10. <span data-ttu-id="1a669-568">登录 Modern POS，然后选择**执行非开票人操作**。</span><span class="sxs-lookup"><span data-stu-id="1a669-568">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
11. <span data-ttu-id="1a669-569">启动**管理硬件工作站**操作。</span><span class="sxs-lookup"><span data-stu-id="1a669-569">Start the **Manage hardware stations** operation.</span></span>
12. <span data-ttu-id="1a669-570">单击**管理**。</span><span class="sxs-lookup"><span data-stu-id="1a669-570">Click **Manage**.</span></span>
13. <span data-ttu-id="1a669-571">在硬件工作站管理页中，设置用于打开硬件工作站的选项。</span><span class="sxs-lookup"><span data-stu-id="1a669-571">On the hardware station management page, set the option to turn on the hardware station.</span></span>
14. <span data-ttu-id="1a669-572">选择要使用的硬件工作站，然后单击**配对**。</span><span class="sxs-lookup"><span data-stu-id="1a669-572">Select the hardware station to use, and then click **Pair**.</span></span>
15. <span data-ttu-id="1a669-573">为 Modern POS 将使用的每个硬件工作站重复步骤 14。</span><span class="sxs-lookup"><span data-stu-id="1a669-573">Repeat step 14 for each hardware station that Modern POS will use.</span></span>
16. <span data-ttu-id="1a669-574">为所需全部硬件工作站配对之后，单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="1a669-574">After all the required hardware stations are paired, click **Close**.</span></span>
17. <span data-ttu-id="1a669-575">在硬件工作站选择页中，单击最近选择的硬件工作站将其激活。</span><span class="sxs-lookup"><span data-stu-id="1a669-575">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a669-576">如果设备经常使用不同硬件工作站，建议将 Modern POS 配置为收银员开始收款过程时提示其选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-576">If devices often use different hardware stations, we recommend that you configure Modern POS to prompt cashiers to select a hardware station when they begin the tender process.</span></span> <span data-ttu-id="1a669-577">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="1a669-577">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="1a669-578">选择收银机，然后将**收款后即可选择**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="1a669-578">Select the register, and then set the **Select upon tender** option to **Yes**.</span></span> <span data-ttu-id="1a669-579">使用 **1090** 配送计划将更改同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="1a669-579">Use the **1090** distribution schedule to sync changes to the channel database.</span></span>

## <a name="extensibility"></a><span data-ttu-id="1a669-580">可扩展性</span><span class="sxs-lookup"><span data-stu-id="1a669-580">Extensibility</span></span>

<span data-ttu-id="1a669-581">有关硬件工作站的可扩展性方案的信息，请参阅[硬件工作站可扩展性](dev-itpro/hardware-station-extensibility.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-581">For information about extensibility scenarios for the hardware station, see [Hardware Station extensibility](dev-itpro/hardware-station-extensibility.md).</span></span>

## <a name="security"></a><span data-ttu-id="1a669-582">安全性</span><span class="sxs-lookup"><span data-stu-id="1a669-582">Security</span></span>

<span data-ttu-id="1a669-583">根据当前安全标准，以下设置应用于生产环境：</span><span class="sxs-lookup"><span data-stu-id="1a669-583">According to current security standards, the following settings should be used in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-584">硬件工作站安装程序将在安装期间通过自助服务自动执行这些注册表编辑。</span><span class="sxs-lookup"><span data-stu-id="1a669-584">The hardware station installer will automatically make these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="1a669-585">应禁用安全套接字层 (SSL)。</span><span class="sxs-lookup"><span data-stu-id="1a669-585">Secure Sockets Layer (SSL) should be disabled.</span></span>
- <span data-ttu-id="1a669-586">应启用并使用传输层安全性 (TLS) 版本 1.2（或当前最高版本）。</span><span class="sxs-lookup"><span data-stu-id="1a669-586">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a669-587">默认情况下，已禁用 SSL 和除 TLS 1.2 外的所有 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="1a669-587">By default, SSL and all versions of TLS except TLS 1.2 are disabled.</span></span>

    <span data-ttu-id="1a669-588">要编辑或启用这些值，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="1a669-588">To edit or enable these values, follow these steps:</span></span>

    1. <span data-ttu-id="1a669-589">按 Windows 徽标键+R 打开**运行**窗口。</span><span class="sxs-lookup"><span data-stu-id="1a669-589">Press the Windows logo key+R to open a **Run** window.</span></span>
    2. <span data-ttu-id="1a669-590">在**打开**字段中，键入 **Regedit**，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="1a669-590">In the **Open** field, type **Regedit**, and then click **OK**.</span></span>
    3. <span data-ttu-id="1a669-591">如果显示**用户帐户控制**消息框，请单击**是**。</span><span class="sxs-lookup"><span data-stu-id="1a669-591">If a **User Account Control** message box appears, click **Yes**.</span></span>
    4. <span data-ttu-id="1a669-592">在**注册表编辑器**窗口中，导航至 **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**。</span><span class="sxs-lookup"><span data-stu-id="1a669-592">In the **Registry Editor** window, navigate to **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**.</span></span> <span data-ttu-id="1a669-593">以自动输入了以下键，以便仅允许 TLS 1.2。</span><span class="sxs-lookup"><span data-stu-id="1a669-593">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>

        - <span data-ttu-id="1a669-594">TLS 1.2Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="1a669-594">TLS 1.2Server:Enabled=1</span></span>
        - <span data-ttu-id="1a669-595">TLS 1.2Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="1a669-595">TLS 1.2Server:DisabledByDefault=0</span></span>
        - <span data-ttu-id="1a669-596">TLS 1.2Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="1a669-596">TLS 1.2Client:Enabled=1</span></span>
        - <span data-ttu-id="1a669-597">TLS 1.2Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="1a669-597">TLS 1.2Client:DisabledByDefault=0</span></span>
        - <span data-ttu-id="1a669-598">TLS 1.1Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-598">TLS 1.1Server:Enabled=0</span></span>
        - <span data-ttu-id="1a669-599">TLS 1.1Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-599">TLS 1.1Client:Enabled=0</span></span>
        - <span data-ttu-id="1a669-600">TLS 1.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-600">TLS 1.0Server:Enabled=0</span></span>
        - <span data-ttu-id="1a669-601">TLS 1.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-601">TLS 1.0Client:Enabled=0</span></span>
        - <span data-ttu-id="1a669-602">SSL 3.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-602">SSL 3.0Server:Enabled=0</span></span>
        - <span data-ttu-id="1a669-603">SSL 3.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-603">SSL 3.0Client:Enabled=0</span></span>
        - <span data-ttu-id="1a669-604">SSL 2.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-604">SSL 2.0Server:Enabled=0</span></span>
        - <span data-ttu-id="1a669-605">SSL 2.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="1a669-605">SSL 2.0Client:Enabled=0</span></span>

- <span data-ttu-id="1a669-606">除非已知的具体原因所需，否则不应开放其他任何网络端口。</span><span class="sxs-lookup"><span data-stu-id="1a669-606">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="1a669-607">必须禁用跨源资源共享，并且必须指定允许接受的源。</span><span class="sxs-lookup"><span data-stu-id="1a669-607">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="1a669-608">应仅使用可信证书机构获取将在运行硬件工作站的计算机上使用的证书。</span><span class="sxs-lookup"><span data-stu-id="1a669-608">Only trusted certificate authorities should be used to obtain certificates that will be used on computers that run the hardware station.</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-609">请务必仔细阅读 IIS 和 Payment Card Industry (PCI) 要求的安全指南。</span><span class="sxs-lookup"><span data-stu-id="1a669-609">It's very important that you review security guidelines for IIS and the Payment Card Industry (PCI) requirements.</span></span>

## <a name="peripheral-simulator"></a><span data-ttu-id="1a669-610">外围设备模拟器</span><span class="sxs-lookup"><span data-stu-id="1a669-610">Peripheral simulator</span></span>

<span data-ttu-id="1a669-611">有关信息，请参阅 [Retail 外设模拟器](dev-itpro/retail-peripheral-simulator.md)。</span><span class="sxs-lookup"><span data-stu-id="1a669-611">For information, see [Retail peripheral simulator](dev-itpro/retail-peripheral-simulator.md).</span></span>

## <a name="microsoft-tested-peripheral-devices"></a><span data-ttu-id="1a669-612">经过 Microsoft 测试的外设</span><span class="sxs-lookup"><span data-stu-id="1a669-612">Microsoft-tested peripheral devices</span></span>

### <a name="ipc-built-in-hardware-station"></a><span data-ttu-id="1a669-613">IPC（内置）硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-613">IPC (built-in) hardware station</span></span>

<span data-ttu-id="1a669-614">已通过 Modern POS for Windows 中的内置 IPC 硬件工作站测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-614">The following peripherals were tested by using the IPC hardware station that is built into Modern POS for Windows.</span></span>

#### <a name="printer"></a><span data-ttu-id="1a669-615">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-615">Printer</span></span>

| <span data-ttu-id="1a669-616">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-616">Manufacturer</span></span> | <span data-ttu-id="1a669-617">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-617">Model</span></span>      | <span data-ttu-id="1a669-618">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-618">Interface</span></span> | <span data-ttu-id="1a669-619">注释</span><span class="sxs-lookup"><span data-stu-id="1a669-619">Comments</span></span>                |
|--------------|------------|-----------|-------------------------|
| <span data-ttu-id="1a669-620">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-620">Epson</span></span>        | <span data-ttu-id="1a669-621">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="1a669-621">Tm-T88IV</span></span>   | <span data-ttu-id="1a669-622">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-622">OPOS</span></span>      |                         |
| <span data-ttu-id="1a669-623">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-623">Epson</span></span>        | <span data-ttu-id="1a669-624">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="1a669-624">TM-T88V</span></span>    | <span data-ttu-id="1a669-625">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-625">OPOS</span></span>      |                         |
| <span data-ttu-id="1a669-626">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-626">Epson</span></span>        | <span data-ttu-id="1a669-627">ePOS-Print</span><span class="sxs-lookup"><span data-stu-id="1a669-627">ePOS-Print</span></span> | <span data-ttu-id="1a669-628">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-628">Custom</span></span>    | <span data-ttu-id="1a669-629">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-629">Connected via network</span></span>   |
| <span data-ttu-id="1a669-630">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-630">Star</span></span>         | <span data-ttu-id="1a669-631">TSP650II</span><span class="sxs-lookup"><span data-stu-id="1a669-631">TSP650II</span></span>   | <span data-ttu-id="1a669-632">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-632">OPOS</span></span>      |                         |
| <span data-ttu-id="1a669-633">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-633">Star</span></span>         | <span data-ttu-id="1a669-634">TSP650II</span><span class="sxs-lookup"><span data-stu-id="1a669-634">TSP650II</span></span>   | <span data-ttu-id="1a669-635">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-635">Custom</span></span>    | <span data-ttu-id="1a669-636">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-636">Connected via network</span></span>   |
| <span data-ttu-id="1a669-637">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-637">Star</span></span>         | <span data-ttu-id="1a669-638">mPOP</span><span class="sxs-lookup"><span data-stu-id="1a669-638">mPOP</span></span>       | <span data-ttu-id="1a669-639">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-639">OPOS</span></span>      | <span data-ttu-id="1a669-640">通过 Bluetooth 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-640">Connected via Bluetooth</span></span> |
| <span data-ttu-id="1a669-641">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-641">HP</span></span>           | <span data-ttu-id="1a669-642">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="1a669-642">F7M67AA</span></span>    | <span data-ttu-id="1a669-643">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-643">OPOS</span></span>      | <span data-ttu-id="1a669-644">带电 USB</span><span class="sxs-lookup"><span data-stu-id="1a669-644">Powered USB</span></span>             |

#### <a name="bar-code-scanner"></a><span data-ttu-id="1a669-645">条码扫描仪</span><span class="sxs-lookup"><span data-stu-id="1a669-645">Bar code scanner</span></span>

| <span data-ttu-id="1a669-646">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-646">Manufacturer</span></span>  | <span data-ttu-id="1a669-647">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-647">Model</span></span>         | <span data-ttu-id="1a669-648">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-648">Interface</span></span> | <span data-ttu-id="1a669-649">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-649">Comments</span></span> |
|---------------|---------------|-----------|----------|
| <span data-ttu-id="1a669-650">Motorola</span><span class="sxs-lookup"><span data-stu-id="1a669-650">Motorola</span></span>      | <span data-ttu-id="1a669-651">DS9208</span><span class="sxs-lookup"><span data-stu-id="1a669-651">DS9208</span></span>        | <span data-ttu-id="1a669-652">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-652">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-653">Honeywell</span><span class="sxs-lookup"><span data-stu-id="1a669-653">Honeywell</span></span>     | <span data-ttu-id="1a669-654">1900</span><span class="sxs-lookup"><span data-stu-id="1a669-654">1900</span></span>          | <span data-ttu-id="1a669-655">UWP</span><span class="sxs-lookup"><span data-stu-id="1a669-655">UWP</span></span>       |          |
| <span data-ttu-id="1a669-656">符号</span><span class="sxs-lookup"><span data-stu-id="1a669-656">Symbol</span></span>        | <span data-ttu-id="1a669-657">LS2208</span><span class="sxs-lookup"><span data-stu-id="1a669-657">LS2208</span></span>        | <span data-ttu-id="1a669-658">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-658">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-659">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="1a669-659">HP Integrated</span></span> | <span data-ttu-id="1a669-660">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="1a669-660">E1L07AA</span></span>       | <span data-ttu-id="1a669-661">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-661">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-662">Datalogic</span><span class="sxs-lookup"><span data-stu-id="1a669-662">Datalogic</span></span>     | <span data-ttu-id="1a669-663">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="1a669-663">Magellan 8400</span></span> | <span data-ttu-id="1a669-664">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-664">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="1a669-665">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="1a669-665">PIN pad</span></span>

| <span data-ttu-id="1a669-666">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-666">Manufacturer</span></span> | <span data-ttu-id="1a669-667">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-667">Model</span></span>  | <span data-ttu-id="1a669-668">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-668">Interface</span></span> | <span data-ttu-id="1a669-669">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-669">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="1a669-670">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-670">VeriFone</span></span>     | <span data-ttu-id="1a669-671">1000SE</span><span class="sxs-lookup"><span data-stu-id="1a669-671">1000SE</span></span> | <span data-ttu-id="1a669-672">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-672">OPOS</span></span>      | <span data-ttu-id="1a669-673">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="1a669-673">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="1a669-674">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-674">Payment terminal</span></span>

| <span data-ttu-id="1a669-675">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-675">Manufacturer</span></span> | <span data-ttu-id="1a669-676">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-676">Model</span></span>        | <span data-ttu-id="1a669-677">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-677">Interface</span></span> | <span data-ttu-id="1a669-678">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-678">Comments</span></span>                                                                       |
|--------------|--------------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1a669-679">Equinox</span><span class="sxs-lookup"><span data-stu-id="1a669-679">Equinox</span></span>      | <span data-ttu-id="1a669-680">L5300</span><span class="sxs-lookup"><span data-stu-id="1a669-680">L5300</span></span>        | <span data-ttu-id="1a669-681">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-681">Custom</span></span>    | <span data-ttu-id="1a669-682">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="1a669-682">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="1a669-683">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-683">VeriFone</span></span>     | <span data-ttu-id="1a669-684">MX925</span><span class="sxs-lookup"><span data-stu-id="1a669-684">MX925</span></span>        | <span data-ttu-id="1a669-685">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-685">Custom</span></span>    | <span data-ttu-id="1a669-686">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-686">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="1a669-687">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-687">VeriFone</span></span>     | <span data-ttu-id="1a669-688">MX915</span><span class="sxs-lookup"><span data-stu-id="1a669-688">MX915</span></span>        | <span data-ttu-id="1a669-689">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-689">Custom</span></span>    | <span data-ttu-id="1a669-690">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-690">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="1a669-691">Verifone</span><span class="sxs-lookup"><span data-stu-id="1a669-691">Verifone</span></span>     | <span data-ttu-id="1a669-692">查看注释</span><span class="sxs-lookup"><span data-stu-id="1a669-692">See comments</span></span> | <span data-ttu-id="1a669-693">Adyen</span><span class="sxs-lookup"><span data-stu-id="1a669-693">Adyen</span></span>     | <span data-ttu-id="1a669-694">Adyen 连接器支持[此处](https://www.adyen.com/pos-payments/terminals)列出的所有设备</span><span class="sxs-lookup"><span data-stu-id="1a669-694">The Adyen connector supports all devices listed [here](https://www.adyen.com/pos-payments/terminals)</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="1a669-695">银箱</span><span class="sxs-lookup"><span data-stu-id="1a669-695">Cash drawer</span></span>

| <span data-ttu-id="1a669-696">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-696">Manufacturer</span></span> | <span data-ttu-id="1a669-697">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-697">Model</span></span>     | <span data-ttu-id="1a669-698">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-698">Interface</span></span> | <span data-ttu-id="1a669-699">注释</span><span class="sxs-lookup"><span data-stu-id="1a669-699">Comments</span></span>                |
|--------------|-----------|-----------|-------------------------|
| <span data-ttu-id="1a669-700">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-700">Star</span></span>         | <span data-ttu-id="1a669-701">mPOP</span><span class="sxs-lookup"><span data-stu-id="1a669-701">mPOP</span></span>      | <span data-ttu-id="1a669-702">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-702">OPOS</span></span>      | <span data-ttu-id="1a669-703">通过 Bluetooth 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-703">Connected via Bluetooth</span></span> |
| <span data-ttu-id="1a669-704">APG</span><span class="sxs-lookup"><span data-stu-id="1a669-704">APG</span></span>          | <span data-ttu-id="1a669-705">Atwood</span><span class="sxs-lookup"><span data-stu-id="1a669-705">Atwood</span></span>    | <span data-ttu-id="1a669-706">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-706">Custom</span></span>    | <span data-ttu-id="1a669-707">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-707">Connected via network</span></span>   |
| <span data-ttu-id="1a669-708">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-708">Star</span></span>         | <span data-ttu-id="1a669-709">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="1a669-709">SMD2-1317</span></span> | <span data-ttu-id="1a669-710">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-710">OPOS</span></span>      |                         |
| <span data-ttu-id="1a669-711">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-711">HP</span></span>           | <span data-ttu-id="1a669-712">QT457AA</span><span class="sxs-lookup"><span data-stu-id="1a669-712">QT457AA</span></span>   | <span data-ttu-id="1a669-713">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-713">OPOS</span></span>      |                         |

#### <a name="line-display"></a><span data-ttu-id="1a669-714">行显示内容</span><span class="sxs-lookup"><span data-stu-id="1a669-714">Line display</span></span>

| <span data-ttu-id="1a669-715">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-715">Manufacturer</span></span>  | <span data-ttu-id="1a669-716">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-716">Model</span></span>   | <span data-ttu-id="1a669-717">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-717">Interface</span></span> | <span data-ttu-id="1a669-718">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-718">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="1a669-719">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="1a669-719">HP integrated</span></span> | <span data-ttu-id="1a669-720">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="1a669-720">G6U79AA</span></span> | <span data-ttu-id="1a669-721">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-721">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-722">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-722">Epson</span></span>         | <span data-ttu-id="1a669-723">M58DC</span><span class="sxs-lookup"><span data-stu-id="1a669-723">M58DC</span></span>   | <span data-ttu-id="1a669-724">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-724">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="1a669-725">签名捕获</span><span class="sxs-lookup"><span data-stu-id="1a669-725">Signature capture</span></span>

| <span data-ttu-id="1a669-726">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-726">Manufacturer</span></span> | <span data-ttu-id="1a669-727">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-727">Model</span></span>  | <span data-ttu-id="1a669-728">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-728">Interface</span></span> | <span data-ttu-id="1a669-729">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-729">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="1a669-730">Scriptel</span><span class="sxs-lookup"><span data-stu-id="1a669-730">Scriptel</span></span>     | <span data-ttu-id="1a669-731">ST1550</span><span class="sxs-lookup"><span data-stu-id="1a669-731">ST1550</span></span> | <span data-ttu-id="1a669-732">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-732">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="1a669-733">比例</span><span class="sxs-lookup"><span data-stu-id="1a669-733">Scale</span></span>

| <span data-ttu-id="1a669-734">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-734">Manufacturer</span></span> | <span data-ttu-id="1a669-735">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-735">Model</span></span>         | <span data-ttu-id="1a669-736">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-736">Interface</span></span> | <span data-ttu-id="1a669-737">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-737">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="1a669-738">Datalogic</span><span class="sxs-lookup"><span data-stu-id="1a669-738">Datalogic</span></span>    | <span data-ttu-id="1a669-739">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="1a669-739">Magellan 8400</span></span> | <span data-ttu-id="1a669-740">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-740">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="1a669-741">MSR</span><span class="sxs-lookup"><span data-stu-id="1a669-741">MSR</span></span>

| <span data-ttu-id="1a669-742">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-742">Manufacturer</span></span> | <span data-ttu-id="1a669-743">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-743">Model</span></span>       | <span data-ttu-id="1a669-744">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-744">Interface</span></span> | <span data-ttu-id="1a669-745">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-745">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="1a669-746">Magtek</span><span class="sxs-lookup"><span data-stu-id="1a669-746">Magtek</span></span>       | <span data-ttu-id="1a669-747">21073075</span><span class="sxs-lookup"><span data-stu-id="1a669-747">21073075</span></span>    | <span data-ttu-id="1a669-748">UWP</span><span class="sxs-lookup"><span data-stu-id="1a669-748">UWP</span></span>       |          |
| <span data-ttu-id="1a669-749">Magtek</span><span class="sxs-lookup"><span data-stu-id="1a669-749">Magtek</span></span>       | <span data-ttu-id="1a669-750">21073062</span><span class="sxs-lookup"><span data-stu-id="1a669-750">21073062</span></span>    | <span data-ttu-id="1a669-751">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-751">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-752">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-752">HP</span></span>           | <span data-ttu-id="1a669-753">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="1a669-753">IDRA-334133</span></span> | <span data-ttu-id="1a669-754">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-754">OPOS</span></span>      |          |

### <a name="dedicated-iis-hardware-station"></a><span data-ttu-id="1a669-755">专用 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-755">Dedicated IIS hardware station</span></span>

<span data-ttu-id="1a669-756">已使用专用（而非共享）IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-756">The following peripherals were tested by using a dedicated (not shared) IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

#### <a name="printer"></a><span data-ttu-id="1a669-757">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-757">Printer</span></span>

| <span data-ttu-id="1a669-758">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-758">Manufacturer</span></span> | <span data-ttu-id="1a669-759">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-759">Model</span></span>    | <span data-ttu-id="1a669-760">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-760">Interface</span></span> | <span data-ttu-id="1a669-761">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-761">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="1a669-762">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-762">Epson</span></span>        | <span data-ttu-id="1a669-763">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="1a669-763">Tm-T88IV</span></span> | <span data-ttu-id="1a669-764">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-764">OPOS</span></span>      |                           |
| <span data-ttu-id="1a669-765">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-765">Epson</span></span>        | <span data-ttu-id="1a669-766">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="1a669-766">TM-T88V</span></span>  | <span data-ttu-id="1a669-767">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-767">OPOS</span></span>      |                           |
| <span data-ttu-id="1a669-768">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-768">Star</span></span>         | <span data-ttu-id="1a669-769">TSP650II</span><span class="sxs-lookup"><span data-stu-id="1a669-769">TSP650II</span></span> | <span data-ttu-id="1a669-770">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-770">OPOS</span></span>      |                           |
| <span data-ttu-id="1a669-771">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-771">Star</span></span>         | <span data-ttu-id="1a669-772">TSP650II</span><span class="sxs-lookup"><span data-stu-id="1a669-772">TSP650II</span></span> | <span data-ttu-id="1a669-773">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-773">Custom</span></span>    | <span data-ttu-id="1a669-774">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-774">Connected via network</span></span>     |
| <span data-ttu-id="1a669-775">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-775">HP</span></span>           | <span data-ttu-id="1a669-776">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="1a669-776">F7M67AA</span></span>  | <span data-ttu-id="1a669-777">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-777">OPOS</span></span>      | <span data-ttu-id="1a669-778">带电 USB</span><span class="sxs-lookup"><span data-stu-id="1a669-778">Powered USB</span></span>               |

#### <a name="bar-code-scanner"></a><span data-ttu-id="1a669-779">条码扫描仪</span><span class="sxs-lookup"><span data-stu-id="1a669-779">Bar code scanner</span></span>

| <span data-ttu-id="1a669-780">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-780">Manufacturer</span></span>  | <span data-ttu-id="1a669-781">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-781">Model</span></span>   | <span data-ttu-id="1a669-782">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-782">Interface</span></span> | <span data-ttu-id="1a669-783">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-783">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="1a669-784">Motorola</span><span class="sxs-lookup"><span data-stu-id="1a669-784">Motorola</span></span>      | <span data-ttu-id="1a669-785">DS9208</span><span class="sxs-lookup"><span data-stu-id="1a669-785">DS9208</span></span>  | <span data-ttu-id="1a669-786">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-786">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-787">符号</span><span class="sxs-lookup"><span data-stu-id="1a669-787">Symbol</span></span>        | <span data-ttu-id="1a669-788">LS2208</span><span class="sxs-lookup"><span data-stu-id="1a669-788">LS2208</span></span>  | <span data-ttu-id="1a669-789">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-789">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-790">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="1a669-790">HP Integrated</span></span> | <span data-ttu-id="1a669-791">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="1a669-791">E1L07AA</span></span> | <span data-ttu-id="1a669-792">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-792">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="1a669-793">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="1a669-793">PIN pad</span></span>

| <span data-ttu-id="1a669-794">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-794">Manufacturer</span></span> | <span data-ttu-id="1a669-795">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-795">Model</span></span>  | <span data-ttu-id="1a669-796">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-796">Interface</span></span> | <span data-ttu-id="1a669-797">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-797">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="1a669-798">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-798">VeriFone</span></span>     | <span data-ttu-id="1a669-799">1000SE</span><span class="sxs-lookup"><span data-stu-id="1a669-799">1000SE</span></span> | <span data-ttu-id="1a669-800">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-800">OPOS</span></span>      | <span data-ttu-id="1a669-801">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="1a669-801">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="1a669-802">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-802">Payment terminal</span></span>

| <span data-ttu-id="1a669-803">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-803">Manufacturer</span></span> | <span data-ttu-id="1a669-804">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-804">Model</span></span> | <span data-ttu-id="1a669-805">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-805">Interface</span></span> | <span data-ttu-id="1a669-806">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-806">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1a669-807">Equinox</span><span class="sxs-lookup"><span data-stu-id="1a669-807">Equinox</span></span>      | <span data-ttu-id="1a669-808">L5300</span><span class="sxs-lookup"><span data-stu-id="1a669-808">L5300</span></span> | <span data-ttu-id="1a669-809">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-809">Custom</span></span>    | <span data-ttu-id="1a669-810">需要自定义付款连接器</span><span class="sxs-lookup"><span data-stu-id="1a669-810">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="1a669-811">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-811">VeriFone</span></span>     | <span data-ttu-id="1a669-812">MX925</span><span class="sxs-lookup"><span data-stu-id="1a669-812">MX925</span></span> | <span data-ttu-id="1a669-813">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-813">Custom</span></span>    | <span data-ttu-id="1a669-814">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-814">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="1a669-815">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-815">VeriFone</span></span>     | <span data-ttu-id="1a669-816">MX915</span><span class="sxs-lookup"><span data-stu-id="1a669-816">MX915</span></span> | <span data-ttu-id="1a669-817">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-817">Custom</span></span>    | <span data-ttu-id="1a669-818">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-818">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="1a669-819">银箱</span><span class="sxs-lookup"><span data-stu-id="1a669-819">Cash drawer</span></span>

| <span data-ttu-id="1a669-820">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-820">Manufacturer</span></span> | <span data-ttu-id="1a669-821">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-821">Model</span></span>     | <span data-ttu-id="1a669-822">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-822">Interface</span></span> | <span data-ttu-id="1a669-823">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-823">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="1a669-824">APG</span><span class="sxs-lookup"><span data-stu-id="1a669-824">APG</span></span>          | <span data-ttu-id="1a669-825">Atwood</span><span class="sxs-lookup"><span data-stu-id="1a669-825">Atwood</span></span>    | <span data-ttu-id="1a669-826">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-826">Custom</span></span>    | <span data-ttu-id="1a669-827">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-827">Connected via network</span></span> |
| <span data-ttu-id="1a669-828">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-828">Star</span></span>         | <span data-ttu-id="1a669-829">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="1a669-829">SMD2-1317</span></span> | <span data-ttu-id="1a669-830">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-830">OPOS</span></span>      |                       |
| <span data-ttu-id="1a669-831">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-831">HP</span></span>           | <span data-ttu-id="1a669-832">QT457AA</span><span class="sxs-lookup"><span data-stu-id="1a669-832">QT457AA</span></span>   | <span data-ttu-id="1a669-833">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-833">OPOS</span></span>      |                       |

#### <a name="line-display"></a><span data-ttu-id="1a669-834">行显示内容</span><span class="sxs-lookup"><span data-stu-id="1a669-834">Line display</span></span>

| <span data-ttu-id="1a669-835">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-835">Manufacturer</span></span>  | <span data-ttu-id="1a669-836">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-836">Model</span></span>   | <span data-ttu-id="1a669-837">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-837">Interface</span></span> | <span data-ttu-id="1a669-838">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-838">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="1a669-839">HP Integrated</span><span class="sxs-lookup"><span data-stu-id="1a669-839">HP integrated</span></span> | <span data-ttu-id="1a669-840">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="1a669-840">G6U79AA</span></span> | <span data-ttu-id="1a669-841">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-841">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-842">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-842">Epson</span></span>         | <span data-ttu-id="1a669-843">M58DC</span><span class="sxs-lookup"><span data-stu-id="1a669-843">M58DC</span></span>   | <span data-ttu-id="1a669-844">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-844">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="1a669-845">签名捕获</span><span class="sxs-lookup"><span data-stu-id="1a669-845">Signature capture</span></span>

| <span data-ttu-id="1a669-846">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-846">Manufacturer</span></span> | <span data-ttu-id="1a669-847">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-847">Model</span></span>  | <span data-ttu-id="1a669-848">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-848">Interface</span></span> | <span data-ttu-id="1a669-849">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-849">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="1a669-850">Scriptel</span><span class="sxs-lookup"><span data-stu-id="1a669-850">Scriptel</span></span>     | <span data-ttu-id="1a669-851">ST1550</span><span class="sxs-lookup"><span data-stu-id="1a669-851">ST1550</span></span> | <span data-ttu-id="1a669-852">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-852">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="1a669-853">比例</span><span class="sxs-lookup"><span data-stu-id="1a669-853">Scale</span></span>

| <span data-ttu-id="1a669-854">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-854">Manufacturer</span></span> | <span data-ttu-id="1a669-855">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-855">Model</span></span>         | <span data-ttu-id="1a669-856">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-856">Interface</span></span> | <span data-ttu-id="1a669-857">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-857">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="1a669-858">Datalogic</span><span class="sxs-lookup"><span data-stu-id="1a669-858">Datalogic</span></span>    | <span data-ttu-id="1a669-859">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="1a669-859">Magellan 8400</span></span> | <span data-ttu-id="1a669-860">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-860">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="1a669-861">MSR</span><span class="sxs-lookup"><span data-stu-id="1a669-861">MSR</span></span>

| <span data-ttu-id="1a669-862">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-862">Manufacturer</span></span> | <span data-ttu-id="1a669-863">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-863">Model</span></span>       | <span data-ttu-id="1a669-864">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-864">Interface</span></span> | <span data-ttu-id="1a669-865">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-865">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="1a669-866">Magtek</span><span class="sxs-lookup"><span data-stu-id="1a669-866">Magtek</span></span>       | <span data-ttu-id="1a669-867">21073075</span><span class="sxs-lookup"><span data-stu-id="1a669-867">21073075</span></span>    | <span data-ttu-id="1a669-868">UWP</span><span class="sxs-lookup"><span data-stu-id="1a669-868">UWP</span></span>       |          |
| <span data-ttu-id="1a669-869">Magtek</span><span class="sxs-lookup"><span data-stu-id="1a669-869">Magtek</span></span>       | <span data-ttu-id="1a669-870">21073062</span><span class="sxs-lookup"><span data-stu-id="1a669-870">21073062</span></span>    | <span data-ttu-id="1a669-871">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-871">OPOS</span></span>      |          |
| <span data-ttu-id="1a669-872">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-872">HP</span></span>           | <span data-ttu-id="1a669-873">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="1a669-873">IDRA-334133</span></span> | <span data-ttu-id="1a669-874">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-874">OPOS</span></span>      |          |

### <a name="shared-iis-hardware-station"></a><span data-ttu-id="1a669-875">共享 IIS 硬件工作站</span><span class="sxs-lookup"><span data-stu-id="1a669-875">Shared IIS hardware station</span></span>

<span data-ttu-id="1a669-876">已使用共享 IIS 硬件工作站和 Modern POS for Windows 及 Cloud POS 测试了以下外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-876">The following peripherals were tested by using a shared IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

> [!NOTE]
> <span data-ttu-id="1a669-877">仅支持打印机、付款终端和银箱。</span><span class="sxs-lookup"><span data-stu-id="1a669-877">Only a printer, payment terminal, and cash drawer are supported.</span></span>

#### <a name="printer"></a><span data-ttu-id="1a669-878">打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-878">Printer</span></span>

| <span data-ttu-id="1a669-879">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-879">Manufacturer</span></span> | <span data-ttu-id="1a669-880">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-880">Model</span></span>    | <span data-ttu-id="1a669-881">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-881">Interface</span></span> | <span data-ttu-id="1a669-882">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-882">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="1a669-883">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-883">Epson</span></span>        | <span data-ttu-id="1a669-884">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="1a669-884">Tm-T88IV</span></span> | <span data-ttu-id="1a669-885">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-885">OPOS</span></span>      |                           |
| <span data-ttu-id="1a669-886">Epson</span><span class="sxs-lookup"><span data-stu-id="1a669-886">Epson</span></span>        | <span data-ttu-id="1a669-887">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="1a669-887">TM-T88V</span></span>  | <span data-ttu-id="1a669-888">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-888">OPOS</span></span>      |                           |
| <span data-ttu-id="1a669-889">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-889">Star</span></span>         | <span data-ttu-id="1a669-890">TSP650II</span><span class="sxs-lookup"><span data-stu-id="1a669-890">TSP650II</span></span> | <span data-ttu-id="1a669-891">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-891">OPOS</span></span>      |                           |
| <span data-ttu-id="1a669-892">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-892">Star</span></span>         | <span data-ttu-id="1a669-893">TSP650II</span><span class="sxs-lookup"><span data-stu-id="1a669-893">TSP650II</span></span> | <span data-ttu-id="1a669-894">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-894">Custom</span></span>    | <span data-ttu-id="1a669-895">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-895">Connected via network</span></span>     |
| <span data-ttu-id="1a669-896">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-896">HP</span></span>           | <span data-ttu-id="1a669-897">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="1a669-897">F7M67AA</span></span>  | <span data-ttu-id="1a669-898">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-898">OPOS</span></span>      | <span data-ttu-id="1a669-899">带电 USB</span><span class="sxs-lookup"><span data-stu-id="1a669-899">Powered USB</span></span>               |

#### <a name="payment-terminal"></a><span data-ttu-id="1a669-900">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-900">Payment terminal</span></span>

| <span data-ttu-id="1a669-901">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-901">Manufacturer</span></span> | <span data-ttu-id="1a669-902">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-902">Model</span></span> | <span data-ttu-id="1a669-903">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-903">Interface</span></span> | <span data-ttu-id="1a669-904">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-904">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1a669-905">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-905">VeriFone</span></span>     | <span data-ttu-id="1a669-906">MX925</span><span class="sxs-lookup"><span data-stu-id="1a669-906">MX925</span></span> | <span data-ttu-id="1a669-907">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-907">Custom</span></span>    | <span data-ttu-id="1a669-908">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-908">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="1a669-909">VeriFone</span><span class="sxs-lookup"><span data-stu-id="1a669-909">VeriFone</span></span>     | <span data-ttu-id="1a669-910">MX915</span><span class="sxs-lookup"><span data-stu-id="1a669-910">MX915</span></span> | <span data-ttu-id="1a669-911">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-911">Custom</span></span>    | <span data-ttu-id="1a669-912">需要自定义付款连接器；通过网络和 USB 连接</span><span class="sxs-lookup"><span data-stu-id="1a669-912">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="1a669-913">银箱</span><span class="sxs-lookup"><span data-stu-id="1a669-913">Cash drawer</span></span>

| <span data-ttu-id="1a669-914">制造商</span><span class="sxs-lookup"><span data-stu-id="1a669-914">Manufacturer</span></span> | <span data-ttu-id="1a669-915">型号</span><span class="sxs-lookup"><span data-stu-id="1a669-915">Model</span></span>     | <span data-ttu-id="1a669-916">接口</span><span class="sxs-lookup"><span data-stu-id="1a669-916">Interface</span></span> | <span data-ttu-id="1a669-917">评论</span><span class="sxs-lookup"><span data-stu-id="1a669-917">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="1a669-918">APG</span><span class="sxs-lookup"><span data-stu-id="1a669-918">APG</span></span>          | <span data-ttu-id="1a669-919">Atwood</span><span class="sxs-lookup"><span data-stu-id="1a669-919">Atwood</span></span>    | <span data-ttu-id="1a669-920">自定义</span><span class="sxs-lookup"><span data-stu-id="1a669-920">Custom</span></span>    | <span data-ttu-id="1a669-921">通过网络连接</span><span class="sxs-lookup"><span data-stu-id="1a669-921">Connected via network</span></span> |
| <span data-ttu-id="1a669-922">Star</span><span class="sxs-lookup"><span data-stu-id="1a669-922">Star</span></span>         | <span data-ttu-id="1a669-923">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="1a669-923">SMD2-1317</span></span> | <span data-ttu-id="1a669-924">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-924">OPOS</span></span>      |                       |
| <span data-ttu-id="1a669-925">HP</span><span class="sxs-lookup"><span data-stu-id="1a669-925">HP</span></span>           | <span data-ttu-id="1a669-926">QT457AA</span><span class="sxs-lookup"><span data-stu-id="1a669-926">QT457AA</span></span>   | <span data-ttu-id="1a669-927">OPOS</span><span class="sxs-lookup"><span data-stu-id="1a669-927">OPOS</span></span>      |                       |

## <a name="troubleshooting"></a><span data-ttu-id="1a669-928">疑难解答</span><span class="sxs-lookup"><span data-stu-id="1a669-928">Troubleshooting</span></span>

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="1a669-929">Modern POS 可以在其列表中检测硬件工作站以进行选择，但是不能完成配对。</span><span class="sxs-lookup"><span data-stu-id="1a669-929">Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="1a669-930">**解决方案：** 验证以下潜在故障点列表：</span><span class="sxs-lookup"><span data-stu-id="1a669-930">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="1a669-931">运行 Modern POS 的计算机信任运行硬件工作站的计算机上使用的证书。</span><span class="sxs-lookup"><span data-stu-id="1a669-931">The computer that is running Modern POS trusts the certificate that is used on the computer that runs the hardware station.</span></span>

    - <span data-ttu-id="1a669-932">若要验证此设置，请转至以下 URL：`https://<Computer Name>:<Port Number>/HardwareStation/ping`。</span><span class="sxs-lookup"><span data-stu-id="1a669-932">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`.</span></span>
    - <span data-ttu-id="1a669-933">此 URL 使用 ping 验证计算机是否可访问，而浏览器则指示证书是否可信。</span><span class="sxs-lookup"><span data-stu-id="1a669-933">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="1a669-934">（例如，在 Internet Explorer 中，地址栏中显示锁图标。</span><span class="sxs-lookup"><span data-stu-id="1a669-934">(For example, in Internet Explorer, a lock icon appears in the address bar.</span></span> <span data-ttu-id="1a669-935">当您单击此图标时，Internet Explorer 验证证书当前是否可信。</span><span class="sxs-lookup"><span data-stu-id="1a669-935">When you click this icon, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="1a669-936">您可以通过查看显示的证书的详细信息，将证书安装到本地计算机上。）</span><span class="sxs-lookup"><span data-stu-id="1a669-936">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="1a669-937">在运行硬件工作站的计算机上，防火墙中将打开硬件工作站使用的端口。</span><span class="sxs-lookup"><span data-stu-id="1a669-937">On the computer that runs the hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="1a669-938">硬件工作站已通过硬件工作站安装程序结束时运行的安装商家信息工具正确安装了商家帐户信息。</span><span class="sxs-lookup"><span data-stu-id="1a669-938">The hardware station has correctly installed merchant account information through the Install merchant information tool that runs at the end of the hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="1a669-939">Modern POS 不能在其列表中检测到硬件工作站来进行选择。</span><span class="sxs-lookup"><span data-stu-id="1a669-939">Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="1a669-940">**解决方案：** 以下因素之一可能导致此问题：</span><span class="sxs-lookup"><span data-stu-id="1a669-940">**Solution:** Either of the following factors can cause this issue:</span></span>

- <span data-ttu-id="1a669-941">硬件工作站尚未在总部正确设置。</span><span class="sxs-lookup"><span data-stu-id="1a669-941">The hardware station hasn't been set up correctly in headquarters.</span></span> <span data-ttu-id="1a669-942">使用本主题前面的步骤验证是否正确输入了硬件工作站配置文件和硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="1a669-942">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="1a669-943">尚未运行作业以更新渠道配置。</span><span class="sxs-lookup"><span data-stu-id="1a669-943">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="1a669-944">在这种情况下，请运行作业 1070 以配置渠道。</span><span class="sxs-lookup"><span data-stu-id="1a669-944">In this case, run the 1070 job for channel configuration.</span></span>

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a><span data-ttu-id="1a669-945">Modern POS 不体现新的银箱设置</span><span class="sxs-lookup"><span data-stu-id="1a669-945">Modern POS doesn't reflect new cash drawer settings</span></span>

<span data-ttu-id="1a669-946">**解决方案：** 关闭当前批处理。</span><span class="sxs-lookup"><span data-stu-id="1a669-946">**Solution:** Close the current batch.</span></span> <span data-ttu-id="1a669-947">关闭当前批处理之前，不会将对银箱的更改更新到 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-947">Changes to the cash drawer aren't updated to Modern POS until the current batch is closed.</span></span>

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a><span data-ttu-id="1a669-948">Modern POS 报告零售外设有问题</span><span class="sxs-lookup"><span data-stu-id="1a669-948">Modern POS is reporting an issue with a retail peripheral</span></span>

<span data-ttu-id="1a669-949">**解决方案：** 下面是此问题的一些典型原因：</span><span class="sxs-lookup"><span data-stu-id="1a669-949">**Solution:** Here are some typical causes of this issue:</span></span>

- <span data-ttu-id="1a669-950">确保关闭了其他设备驱动程序配置实用程序。</span><span class="sxs-lookup"><span data-stu-id="1a669-950">Make sure that other device driver configuration utilities are closed.</span></span> <span data-ttu-id="1a669-951">如果打开了这些实用程序，可能会阻止 Modern POS 或硬件工作站声明设备。</span><span class="sxs-lookup"><span data-stu-id="1a669-951">If these utilities are open, they might prevent Modern POS or the hardware station from claiming the device.</span></span>
- <span data-ttu-id="1a669-952">如果将零售外设与多台 POS 设备共享，请确保其属于以下类别之一：</span><span class="sxs-lookup"><span data-stu-id="1a669-952">If the retail peripheral is shared with multiple POS devices, make sure that it belongs to one of the following categories:</span></span>

    - <span data-ttu-id="1a669-953">银箱</span><span class="sxs-lookup"><span data-stu-id="1a669-953">Cash drawer</span></span>
    - <span data-ttu-id="1a669-954">收据打印机</span><span class="sxs-lookup"><span data-stu-id="1a669-954">Receipt printer</span></span>
    - <span data-ttu-id="1a669-955">付款终端</span><span class="sxs-lookup"><span data-stu-id="1a669-955">Payment terminal</span></span>

    <span data-ttu-id="1a669-956">如果外设不属于这些类别之一，则硬件工作站的设计不支持在多台 POS 设备之间共享该外设。</span><span class="sxs-lookup"><span data-stu-id="1a669-956">If the peripheral doesn't belong to one of these categories, the hardware station isn't designed to enable the peripheral to be shared among multiple POS devices.</span></span>

- <span data-ttu-id="1a669-957">有时，设备驱动程序可能导致公共控件对象 (CCO) 停止正常工作。</span><span class="sxs-lookup"><span data-stu-id="1a669-957">Sometimes, device drivers can cause the common control objects (CCOs) to stop working correctly.</span></span> <span data-ttu-id="1a669-958">如果最近安装了设备，但是该设备无法正常工作，或您发现了其他问题，通常可以通过重新安装 CCO 来解决问题。</span><span class="sxs-lookup"><span data-stu-id="1a669-958">If a device has recently been installed, but it isn't working properly or you notice other issues, you can often resolve the issue by reinstalling the CCOs.</span></span> <span data-ttu-id="1a669-959">若要下载 CCO，请访问 <http://monroecs.com/oposccos_current.htm>。</span><span class="sxs-lookup"><span data-stu-id="1a669-959">To download the CCOs, visit <http://monroecs.com/oposccos_current.htm>.</span></span>
- <span data-ttu-id="1a669-960">如果在测试或故障排除期间频繁更改外设，可能必须重置 IIS，而不是等待高速缓存自行刷新。</span><span class="sxs-lookup"><span data-stu-id="1a669-960">If you make frequent peripheral changes during testing or troubleshooting, you might have to reset IIS instead of waiting for the cache to refresh itself.</span></span> <span data-ttu-id="1a669-961">若要重置 IIS，请执行以下步骤:</span><span class="sxs-lookup"><span data-stu-id="1a669-961">To reset IIS, follow these steps:</span></span>

    1. <span data-ttu-id="1a669-962">在**开始**菜单中键入 **CMD**。</span><span class="sxs-lookup"><span data-stu-id="1a669-962">From the **Start** menu, type **CMD**.</span></span>
    2. <span data-ttu-id="1a669-963">在搜索结果中，右键单击**命令提示符**，然后单击**以管理员身份运行**。</span><span class="sxs-lookup"><span data-stu-id="1a669-963">In the search results, right-click **Command prompt**, and then click **Run as administrator**.</span></span>
    3. <span data-ttu-id="1a669-964">在**命令提示符**窗口中，键入 **iisreset /Restart**，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="1a669-964">In the **Command prompt** window, type **iisreset /Restart** and then press Enter.</span></span>
    4. <span data-ttu-id="1a669-965">IIS 重新启动后，重新启动 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-965">After IIS has restarted, restart Modern POS.</span></span>

- <span data-ttu-id="1a669-966">频繁更改外设时，如果也频繁启动和退出 POS 客户端，则上一个 POS 会话的 dllhost 进程可能干扰当前会话。</span><span class="sxs-lookup"><span data-stu-id="1a669-966">While you're making frequent changes to peripheral devices, if you also frequently start and exit the POS client, the dllhost process from a previous POS session can interfere with the current session.</span></span> <span data-ttu-id="1a669-967">在这种情况下，关闭正在管理上一个会话的动态链接库 (DLL) 主机之前，设备可能不可用。</span><span class="sxs-lookup"><span data-stu-id="1a669-967">In this case, a device might not be usable until you close the dynamic-link library (DLL) host that is managing the previous session.</span></span> <span data-ttu-id="1a669-968">若要关闭 DLL 主机，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="1a669-968">To close the DLL host, follow these steps:</span></span>

    1. <span data-ttu-id="1a669-969">在**开始**菜单中键入**任务管理器**。</span><span class="sxs-lookup"><span data-stu-id="1a669-969">From the **Start** menu, type **Task manager**.</span></span>
    2. <span data-ttu-id="1a669-970">在搜索结果中，单击**任务管理器**。</span><span class="sxs-lookup"><span data-stu-id="1a669-970">In the search results, click **Task manager**.</span></span>
    3. <span data-ttu-id="1a669-971">在“任务管理器”中的**详细信息**选项卡上，单击带有**名称**标签的列标题，按名称以字母顺序为表排序。</span><span class="sxs-lookup"><span data-stu-id="1a669-971">In Task manager, on the **Details** tab, click the column header that is labeled **Name** to sort the table alphabetically by name.</span></span>
    4. <span data-ttu-id="1a669-972">向下滚动，直到找到 dllhost.exe。</span><span class="sxs-lookup"><span data-stu-id="1a669-972">Scroll down until you find dllhost.exe.</span></span>
    5. <span data-ttu-id="1a669-973">选择每个 DLL 主机，然后单击**结束任何**。</span><span class="sxs-lookup"><span data-stu-id="1a669-973">Select each DLL host, and then click **End task**.</span></span>
    6. <span data-ttu-id="1a669-974">关闭 DLL 主机后，重新启动 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="1a669-974">After the DLL hosts have been closed, restart Modern POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a669-975">其他资源</span><span class="sxs-lookup"><span data-stu-id="1a669-975">Additional resources</span></span>

[<span data-ttu-id="1a669-976">零售外围设备模拟器</span><span class="sxs-lookup"><span data-stu-id="1a669-976">Retail peripheral simulator</span></span>](dev-itpro/retail-peripheral-simulator.md)
