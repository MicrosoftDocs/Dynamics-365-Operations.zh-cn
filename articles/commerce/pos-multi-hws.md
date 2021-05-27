---
title: 打印机和银箱的专用的付款终端和提示
description: 本主题提供有关使用专用付款终端以及提示用户选择银箱和收据打印机的功能的信息。
author: rubendel
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a3c7eb9580f9155dd33f6351f37eb1edd269a3d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018625"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a><span data-ttu-id="22506-103">打印机和银箱的专用的付款终端和提示</span><span class="sxs-lookup"><span data-stu-id="22506-103">Dedicated payment terminals and prompts for a printer and cash drawer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22506-104">本主题提供有关使用专用付款终端以及提示用户选择银箱和收据打印机的功能的信息。</span><span class="sxs-lookup"><span data-stu-id="22506-104">This topic provides information about the capability to have a dedicated payment terminal and prompt the user to select a cash drawer and a receipt printer.</span></span>

## <a name="overview"></a><span data-ttu-id="22506-105">概览</span><span class="sxs-lookup"><span data-stu-id="22506-105">Overview</span></span>

<span data-ttu-id="22506-106">现代零售商正在寻找简化店内结帐体验的方法。</span><span class="sxs-lookup"><span data-stu-id="22506-106">Modern retailers are searching for ways to streamline the in-store checkout experience.</span></span> <span data-ttu-id="22506-107">通过电子付款进行无纸化结帐的最新趋势不仅有助于使购买体验更加顺畅，还可以减少为每个商店员工提供全套外围设备的需求。</span><span class="sxs-lookup"><span data-stu-id="22506-107">Recent trends toward paperless checkout through electronic payments not only help to make the purchasing experience smoother but also reduce the need to have a full complement of peripheral devices available for every store associate.</span></span>

<span data-ttu-id="22506-108">Microsoft Dynamics 365 Commerce 通过实现以下方案来支持这些趋势：销售点 (POS) 设备始终会有分配给它的专用付款终端，但没有自己的收据打印机或银箱。</span><span class="sxs-lookup"><span data-stu-id="22506-108">Microsoft Dynamics 365 Commerce supports these trends by enabling a scenario where a point of sale (POS) device has a dedicated payment terminal assigned to it all the time, but it doesn't have its own receipt printer or cash drawer.</span></span> <span data-ttu-id="22506-109">当员工必须打印收据或接收现金付款时，系统会提示他们选择已配置这些设备的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="22506-109">When associates must print a receipt or take a cash payment, they are prompted to select a hardware station where those devices are configured.</span></span>

## <a name="key-terms"></a><span data-ttu-id="22506-110">重要术语</span><span class="sxs-lookup"><span data-stu-id="22506-110">Key terms</span></span>

| <span data-ttu-id="22506-111">条款</span><span class="sxs-lookup"><span data-stu-id="22506-111">Term</span></span> | <span data-ttu-id="22506-112">说明</span><span class="sxs-lookup"><span data-stu-id="22506-112">Description</span></span> |
|---|---|
| <span data-ttu-id="22506-113">登记簿</span><span class="sxs-lookup"><span data-stu-id="22506-113">Register</span></span> | <span data-ttu-id="22506-114">用于配置 POS 收银机实例的实体。</span><span class="sxs-lookup"><span data-stu-id="22506-114">The entity that is used to configure an instance of a POS register.</span></span> |
| <span data-ttu-id="22506-115">设备</span><span class="sxs-lookup"><span data-stu-id="22506-115">Device</span></span> | <span data-ttu-id="22506-116">POS 收银机和分配给它的 Modern POS 应用程序的物理实例的表示形式。</span><span class="sxs-lookup"><span data-stu-id="22506-116">A representation of the physical instance of a POS register and the Modern POS application that is assigned to it.</span></span> |
| <span data-ttu-id="22506-117">专用硬件工作站</span><span class="sxs-lookup"><span data-stu-id="22506-117">Dedicated hardware station</span></span> | <span data-ttu-id="22506-118">内置在适用于 Windows 的 Modern POS 和适用于 Android 的 Modern POS 应用程序中的硬件工作站业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="22506-118">The hardware station business logic that is built into the Modern POS for Windows and Modern POS for Android applications.</span></span> |
| <span data-ttu-id="22506-119">银箱弹出 (d/k) 端口</span><span class="sxs-lookup"><span data-stu-id="22506-119">Drawer kick (d/k) port</span></span> | <span data-ttu-id="22506-120">将银箱连接到收据打印机的传统方法。</span><span class="sxs-lookup"><span data-stu-id="22506-120">A traditional method for connecting a cash drawer to a receipt printer.</span></span> |
| <span data-ttu-id="22506-121">网络外设</span><span class="sxs-lookup"><span data-stu-id="22506-121">Network peripherals</span></span> | <span data-ttu-id="22506-122">对网络支持的付款终端、收据打印机和银箱的内置支持。</span><span class="sxs-lookup"><span data-stu-id="22506-122">Built-in support for network-enabled payment terminals, receipt printers, and cash drawers.</span></span> |

## <a name="supported-pos-clients-and-devices"></a><span data-ttu-id="22506-123">支持的 POS 客户端和设备</span><span class="sxs-lookup"><span data-stu-id="22506-123">Supported POS clients and devices</span></span>

<span data-ttu-id="22506-124">本主题中介绍的功能由适用于 Windows 的 Modern POS 和适用于 Android的 Modern POS 的 POS 客户端支持。</span><span class="sxs-lookup"><span data-stu-id="22506-124">The functionality that is described in this topic is supported by the Modern POS for Windows and Modern POS for Android POS clients.</span></span>

<span data-ttu-id="22506-125">此功能支持网络支持的付款终端和收据打印机。</span><span class="sxs-lookup"><span data-stu-id="22506-125">This functionality supports network-enabled payment terminals and receipt printers.</span></span> <span data-ttu-id="22506-126">您可以通过 d/k 端口将银箱连接到网络支持的收据打印机，以此来提供银箱支持。</span><span class="sxs-lookup"><span data-stu-id="22506-126">You can provide cash drawer support by connecting the cash drawer to the network-enabled receipt printer via the d/k port.</span></span>

<span data-ttu-id="22506-127">此功能的现成支持由[适用于 Adyen 的 Dynamics 365 Payment Connector](./dev-itpro/adyen-connector.md?tabs=8-1-3) 提供。</span><span class="sxs-lookup"><span data-stu-id="22506-127">Out-of-box support for this functionality is provided by the [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).</span></span> <span data-ttu-id="22506-128">但是，可以通过 Commerce 付款软件开发套件 (SDK) 支持其他付款连接器。</span><span class="sxs-lookup"><span data-stu-id="22506-128">However, other payment connectors might be supported via the Commerce software development kit (SDK) for payments.</span></span> <span data-ttu-id="22506-129">支持的收据打印机包括 Star Micronics 和 Epson 的网络支持的收据打印机。</span><span class="sxs-lookup"><span data-stu-id="22506-129">Supported receipt printers include network-enabled receipt printers from Star Micronics and Epson.</span></span>

<span data-ttu-id="22506-130">要设置 Star Micronics 收据打印机，请使用 Star Micronics 打印机实用程序配置设备，以可以通过网络上使用它。</span><span class="sxs-lookup"><span data-stu-id="22506-130">To set up Star Micronics receipt printers, use the Star Micronics Printer Utility to configure the device so that it can be used over the network.</span></span> <span data-ttu-id="22506-131">此实用程序还会提供设备的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="22506-131">This utility will also provide the IP address of the device.</span></span>

<span data-ttu-id="22506-132">要设置 Epson 收据打印机，请使用 Epson ePOS-Print 实用程序将设备设置为使用网络协议。</span><span class="sxs-lookup"><span data-stu-id="22506-132">To set up Epson receipt printers, use the Epson ePOS-Print utility to set up the device to use network protocols.</span></span>

<span data-ttu-id="22506-133">有关如何设置网络外围设备的详细信息，请参阅[网络外围设备支持概述](./dev-itpro/network-peripherals.md)。</span><span class="sxs-lookup"><span data-stu-id="22506-133">For more information about how to set up network peripherals, see [Network peripheral support overview](./dev-itpro/network-peripherals.md).</span></span>

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a><span data-ttu-id="22506-134">为打印机和银箱设置专用付款终端和提示</span><span class="sxs-lookup"><span data-stu-id="22506-134">Set up a dedicated payment terminal and a prompt for a printer and cash drawer</span></span>

### <a name="set-up-hardware-profiles"></a><span data-ttu-id="22506-135">设置硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="22506-135">Set up hardware profiles</span></span>

<span data-ttu-id="22506-136">您必须有两种类型的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="22506-136">You must have two types of hardware profile.</span></span> <span data-ttu-id="22506-137">第一种分配给收银机。</span><span class="sxs-lookup"><span data-stu-id="22506-137">The first is assigned to the register.</span></span> <span data-ttu-id="22506-138">第二种分配给商店级别的硬件工作站，用于对网络收据打印机和银箱进行逻辑分组。</span><span class="sxs-lookup"><span data-stu-id="22506-138">The second is assigned to a hardware station at the store level, and is used to logically group network receipt printers and cash drawers.</span></span>

#### <a name="set-up-a-hardware-profile-for-the-register"></a><span data-ttu-id="22506-139">设置收银机的硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="22506-139">Set up a hardware profile for the register</span></span>

<span data-ttu-id="22506-140">要设置分配给收银机的硬件配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="22506-140">To set up the hardware profile that is assigned to the register, follow these steps.</span></span>

1. <span data-ttu-id="22506-141">在 Dynamics 365 Commerce 中，搜索 **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="22506-141">In Dynamics 365 Commerce, search for **Hardware profile**.</span></span>
2. <span data-ttu-id="22506-142">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="22506-142">Select **New**.</span></span>
3. <span data-ttu-id="22506-143">分配硬件配置文件编号，然后输入描述。</span><span class="sxs-lookup"><span data-stu-id="22506-143">Assign a hardware profile number, and then enter a description.</span></span> <span data-ttu-id="22506-144">此硬件配置文件将分配给收银机本身。</span><span class="sxs-lookup"><span data-stu-id="22506-144">This hardware profile will be assigned to the register itself.</span></span> <span data-ttu-id="22506-145">因此，诸如 **专用与后备** 这样的描述就可以。</span><span class="sxs-lookup"><span data-stu-id="22506-145">Therefore, a description such as **Dedicated with fallback** will suffice.</span></span>
4. <span data-ttu-id="22506-146">在不同设备类型的快速选项卡上，设置以下设备类型。</span><span class="sxs-lookup"><span data-stu-id="22506-146">On the FastTabs for different device types, set up the following device types.</span></span>

    | <span data-ttu-id="22506-147">设备</span><span class="sxs-lookup"><span data-stu-id="22506-147">Device</span></span> | <span data-ttu-id="22506-148">类型</span><span class="sxs-lookup"><span data-stu-id="22506-148">Type</span></span> | <span data-ttu-id="22506-149">设备名称</span><span class="sxs-lookup"><span data-stu-id="22506-149">Device name</span></span> | <span data-ttu-id="22506-150">其他详细信息</span><span class="sxs-lookup"><span data-stu-id="22506-150">Additional details</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="22506-151">打印机</span><span class="sxs-lookup"><span data-stu-id="22506-151">Printer</span></span> | <span data-ttu-id="22506-152">网络</span><span class="sxs-lookup"><span data-stu-id="22506-152">Network</span></span> | <span data-ttu-id="22506-153">*任何*</span><span class="sxs-lookup"><span data-stu-id="22506-153">*Any*</span></span> | <span data-ttu-id="22506-154">设备名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="22506-154">The device name is case-sensitive.</span></span> <span data-ttu-id="22506-155">**收据模板 ID** 应该与映射到网络打印机的 **收据模板 ID** 相同，网络打印机在渠道级别分配给硬件工作站的硬件配置文件中设置。</span><span class="sxs-lookup"><span data-stu-id="22506-155">The **Receipt profile ID** should be the same as the **Receipt profile ID** that is mapped to the network printer that is set up in the hardware profile that is assigned to the hardware station at the channel level.</span></span> |
    | <span data-ttu-id="22506-156">银箱</span><span class="sxs-lookup"><span data-stu-id="22506-156">Cash drawer</span></span> | <span data-ttu-id="22506-157">网络</span><span class="sxs-lookup"><span data-stu-id="22506-157">Network</span></span> | <span data-ttu-id="22506-158">*任何*</span><span class="sxs-lookup"><span data-stu-id="22506-158">*Any*</span></span> | <span data-ttu-id="22506-159">设备名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="22506-159">The device name is case-sensitive.</span></span> <span data-ttu-id="22506-160">将 **使用共享班次** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="22506-160">Set the **Use shared shift** option to **Yes**.</span></span> |
    | <span data-ttu-id="22506-161">EFT 服务</span><span class="sxs-lookup"><span data-stu-id="22506-161">EFT service</span></span> | <span data-ttu-id="22506-162">Adyen</span><span class="sxs-lookup"><span data-stu-id="22506-162">Adyen</span></span> | <span data-ttu-id="22506-163">不适用</span><span class="sxs-lookup"><span data-stu-id="22506-163">Not applicable</span></span> | <span data-ttu-id="22506-164">有关如何设置现成的 Adyen 连接器的信息，请参阅[适用于 Adyen 的 Dynamics 365 Payment Connector](./dev-itpro/adyen-connector.md?tabs=8-1-3)。</span><span class="sxs-lookup"><span data-stu-id="22506-164">For information about how to set up the out-of-box Adyen connector, see [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).</span></span> <span data-ttu-id="22506-165">可以通过 [Commerce 付款软件开发套件 (SDK)](./dev-itpro/end-to-end-payment-extension.md) 支持其他付款连接器。</span><span class="sxs-lookup"><span data-stu-id="22506-165">Other payment connectors can be supported via the [Commerce software development kit (SDK) for payments](./dev-itpro/end-to-end-payment-extension.md).</span></span> |
    | <span data-ttu-id="22506-166">PIN 小键盘</span><span class="sxs-lookup"><span data-stu-id="22506-166">PIN pad</span></span> | <span data-ttu-id="22506-167">网络</span><span class="sxs-lookup"><span data-stu-id="22506-167">Network</span></span> | <span data-ttu-id="22506-168">**MicrosoftAdyenDeviceV001**</span><span class="sxs-lookup"><span data-stu-id="22506-168">**MicrosoftAdyenDeviceV001**</span></span> | <span data-ttu-id="22506-169">无。</span><span class="sxs-lookup"><span data-stu-id="22506-169">None.</span></span> |

5. <span data-ttu-id="22506-170">在 Dynamics 365 Commerce 中，搜索 **收银机**。</span><span class="sxs-lookup"><span data-stu-id="22506-170">In Dynamics 365 Commerce, search for **Registers**.</span></span>
6. <span data-ttu-id="22506-171">通过选择收银机编号选择一个收银机，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="22506-171">Select a register by selecting the register number, and then select **Edit**.</span></span>
7. <span data-ttu-id="22506-172">将刚才创建的硬件配置文件分配给应该使用专用付款终端的收银机。</span><span class="sxs-lookup"><span data-stu-id="22506-172">Assign the hardware profile that you just created to the register that should use a dedicated payment terminal.</span></span> <span data-ttu-id="22506-173">映射到此收银机的设备必须使用适用于 Windows 的 Modern POS 应用程序或适用于 Android 的 Modern POS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="22506-173">The device that is mapped to this register must use either the Modern POS for Windows application or the Modern POS for Android application.</span></span>
8. <span data-ttu-id="22506-174">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="22506-174">Select **Save**.</span></span>
9. <span data-ttu-id="22506-175">在“操作”窗格上的 **收银机** 选项卡中，选择 **配置 IP 地址**。</span><span class="sxs-lookup"><span data-stu-id="22506-175">On the Action Pane, on the **Registers** tab, select **Configure IP addresses**.</span></span>
10. <span data-ttu-id="22506-176">在 **PIN 小键盘** 快速选项卡上，输入付款终端的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="22506-176">On the **PIN pad** FastTab, enter the IP address of the payment terminal.</span></span> <span data-ttu-id="22506-177">有关如何使用 Adyen 连接器获取付款终端 IP 地址的信息，请参阅[适用于 Adyen 的 Dynamics 365 Payment Connector](./dev-itpro/adyen-connector.md?tabs=8-1-3)。</span><span class="sxs-lookup"><span data-stu-id="22506-177">For information about how to get the IP address of the payment terminal by using the Adyen connector, see [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).</span></span>
11. <span data-ttu-id="22506-178">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="22506-178">Select **Save**.</span></span>

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a><span data-ttu-id="22506-179">设置收据打印机和银箱的硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="22506-179">Set up a hardware profile for the receipt printer and cash drawer</span></span>

<span data-ttu-id="22506-180">要设置用于将网络收据打印机和银箱分组的硬件配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="22506-180">To set up the hardware profile that is used to group the network receipt printer and cash drawer, follow these steps.</span></span>

1. <span data-ttu-id="22506-181">在 Dynamics 365 Commerce 中，搜索 **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="22506-181">In Dynamics 365 Commerce, search for **Hardware profile**.</span></span>
2. <span data-ttu-id="22506-182">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="22506-182">Select **New**.</span></span>
3. <span data-ttu-id="22506-183">分配硬件配置文件编号，然后输入描述。</span><span class="sxs-lookup"><span data-stu-id="22506-183">Assign a hardware profile number, and then enter a description.</span></span> <span data-ttu-id="22506-184">此硬件配置文件将用于对收据打印机和银箱进行分组。</span><span class="sxs-lookup"><span data-stu-id="22506-184">This hardware profile will be used to group the receipt printer and cash drawer.</span></span> <span data-ttu-id="22506-185">因此，诸如 **网络打印机和银箱** 这样的描述就可以。</span><span class="sxs-lookup"><span data-stu-id="22506-185">Therefore, a description such as **Network printer and cash drawer** will suffice.</span></span>
4. <span data-ttu-id="22506-186">在不同设备类型的快速选项卡上，设置以下设备类型。</span><span class="sxs-lookup"><span data-stu-id="22506-186">On the FastTabs for different device types, set up the following device types.</span></span>

    | <span data-ttu-id="22506-187">设备</span><span class="sxs-lookup"><span data-stu-id="22506-187">Device</span></span> | <span data-ttu-id="22506-188">类型</span><span class="sxs-lookup"><span data-stu-id="22506-188">Type</span></span> | <span data-ttu-id="22506-189">说明</span><span class="sxs-lookup"><span data-stu-id="22506-189">Description</span></span> | <span data-ttu-id="22506-190">其他详细信息</span><span class="sxs-lookup"><span data-stu-id="22506-190">Additional details</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="22506-191">打印机</span><span class="sxs-lookup"><span data-stu-id="22506-191">Printer</span></span> | <span data-ttu-id="22506-192">网络</span><span class="sxs-lookup"><span data-stu-id="22506-192">Network</span></span> | <span data-ttu-id="22506-193">**Epson** 或 **Star**</span><span class="sxs-lookup"><span data-stu-id="22506-193">**Epson** or **Star**</span></span> | <span data-ttu-id="22506-194">设备名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="22506-194">The device name is case-sensitive.</span></span> <span data-ttu-id="22506-195">**收据模板 ID** 应该与映射到打印机的 **收据模板 ID** 相同，打印机在分配给收银机的硬件配置文件中设置。</span><span class="sxs-lookup"><span data-stu-id="22506-195">The **Receipt profile ID** should be the same as the **Receipt profile ID** that is mapped to the printer that is set up in the hardware profile that is assigned to the register.</span></span> |
    | <span data-ttu-id="22506-196">银箱</span><span class="sxs-lookup"><span data-stu-id="22506-196">Cash drawer</span></span> | <span data-ttu-id="22506-197">回退</span><span class="sxs-lookup"><span data-stu-id="22506-197">Fallback</span></span> | <span data-ttu-id="22506-198">**Epson** 或 **Star**</span><span class="sxs-lookup"><span data-stu-id="22506-198">**Epson** or **Star**</span></span> | <span data-ttu-id="22506-199">设备名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="22506-199">The device name is case-sensitive.</span></span> <span data-ttu-id="22506-200">将 **使用共享班次** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="22506-200">set the **Use shared shift** option to **Yes**.</span></span> |

5. <span data-ttu-id="22506-201">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="22506-201">Select **Save**.</span></span>

### <a name="set-up-hardware-stations"></a><span data-ttu-id="22506-202">设置硬件工作站</span><span class="sxs-lookup"><span data-stu-id="22506-202">Set up hardware stations</span></span>

<span data-ttu-id="22506-203">您必须有两个硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="22506-203">You must have two hardware stations.</span></span> <span data-ttu-id="22506-204">第一个将映射到收银机。</span><span class="sxs-lookup"><span data-stu-id="22506-204">The first will be mapped to the register.</span></span> <span data-ttu-id="22506-205">每当必须打印收据或必须打开银箱时，将根据需要选择第二个。</span><span class="sxs-lookup"><span data-stu-id="22506-205">The second will be selected as it's required, whenever a receipt must be printed or a cash drawer must be opened.</span></span>

#### <a name="register-a-hardware-station"></a><span data-ttu-id="22506-206">登记硬件工作站</span><span class="sxs-lookup"><span data-stu-id="22506-206">Register a hardware station</span></span>

1. <span data-ttu-id="22506-207">在 Dynamics 365 Commerce 中，搜索 **所有商店**。</span><span class="sxs-lookup"><span data-stu-id="22506-207">In Dynamics 365 Commerce, search for **All stores**.</span></span>
2. <span data-ttu-id="22506-208">通过选择商店的 **零售渠道 ID** 值，然后选择 **编辑** 来选择商店。</span><span class="sxs-lookup"><span data-stu-id="22506-208">Select a store by selecting its **Retail Channel Id** values, and then select **Edit**.</span></span>
3. <span data-ttu-id="22506-209">在 **硬件工作站** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="22506-209">On the **Hardware stations** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="22506-210">将 **硬件工作站类型** 设置为 **专用**。</span><span class="sxs-lookup"><span data-stu-id="22506-210">Set the **Hardware station type** field to **Dedicated**.</span></span>
5. <span data-ttu-id="22506-211">输入描述，但不要为此硬件工作站设置任何其他值。</span><span class="sxs-lookup"><span data-stu-id="22506-211">Enter a description, but don't set any other values for this hardware station.</span></span> <span data-ttu-id="22506-212">此硬件工作站将始终用于收银机。</span><span class="sxs-lookup"><span data-stu-id="22506-212">This hardware station will be used for the register at all times.</span></span> 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a><span data-ttu-id="22506-213">设置收据打印机和银箱的硬件工作站</span><span class="sxs-lookup"><span data-stu-id="22506-213">Set up a hardware station for the receipt printer and cash drawer</span></span>

1. <span data-ttu-id="22506-214">在 Dynamics 365 Commerce 中，搜索 **所有商店**。</span><span class="sxs-lookup"><span data-stu-id="22506-214">In Dynamics 365 Commerce, search for **All stores**.</span></span>
2. <span data-ttu-id="22506-215">通过选择商店的 **零售渠道 ID** 值，然后选择 **编辑** 来选择商店。</span><span class="sxs-lookup"><span data-stu-id="22506-215">Select a store by selecting its **Retail Channel Id** values, and then select **Edit**.</span></span>
3. <span data-ttu-id="22506-216">在 **硬件工作站** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="22506-216">On the **Hardware stations** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="22506-217">将 **硬件工作站类型** 设置为 **专用**。</span><span class="sxs-lookup"><span data-stu-id="22506-217">Set the **Hardware station type** field to **Dedicated**.</span></span>
5. <span data-ttu-id="22506-218">输入描述。</span><span class="sxs-lookup"><span data-stu-id="22506-218">Enter a description.</span></span> <span data-ttu-id="22506-219">此硬件工作站将用于收据打印机和银箱。</span><span class="sxs-lookup"><span data-stu-id="22506-219">This hardware station will be used for the receipt printer and cash drawer.</span></span>
6. <span data-ttu-id="22506-220">在 **硬件配置文件** 字段中，选择您先前为收据打印机和银箱创建的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="22506-220">In the **Hardware profile** field, select the hardware profile that you previously created for the receipt printer and cash drawer.</span></span>
7. <span data-ttu-id="22506-221">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="22506-221">Select **Save**.</span></span>
8. <span data-ttu-id="22506-222">在仍然选择了收据打印机和银箱的硬件工作站时，选择 **配置 IP 地址**。</span><span class="sxs-lookup"><span data-stu-id="22506-222">While the hardware station for the receipt printer and cash drawer is still selected, select **Configure IP addresses**.</span></span>
9. <span data-ttu-id="22506-223">获取打印机的 IP 地址，并将其输入为收据打印机和银箱的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="22506-223">Obtain the IP address for the printer, and enter it as the IP address for both the receipt printer and the cash drawer.</span></span>
10. <span data-ttu-id="22506-224">选择 **保存**</span><span class="sxs-lookup"><span data-stu-id="22506-224">Select **Save**</span></span>
11. <span data-ttu-id="22506-225">搜索 **分配计划**。</span><span class="sxs-lookup"><span data-stu-id="22506-225">Search for **Distribution schedules**.</span></span>
12. <span data-ttu-id="22506-226">选择分配计划 **1090**，然后选择 **立即运行**。</span><span class="sxs-lookup"><span data-stu-id="22506-226">Select distribution schedule **1090**, and then select **Run now**.</span></span>
13. <span data-ttu-id="22506-227">选择分配计划 **1070**，然后选择 **立即运行**。</span><span class="sxs-lookup"><span data-stu-id="22506-227">Select distribution schedule **1070**, and then select **Run now**.</span></span>

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a><span data-ttu-id="22506-228">设置系统以根据需要提示选择收据打印机和银箱</span><span class="sxs-lookup"><span data-stu-id="22506-228">Set up the system to prompt for receipt printer and cash drawer selection as it's required</span></span>

1. <span data-ttu-id="22506-229">在支持的 POS 客户端，如果某个班次已打开，关闭当前班次。</span><span class="sxs-lookup"><span data-stu-id="22506-229">In a supported POS client, close the current shift, if a shift is open.</span></span>
2. <span data-ttu-id="22506-230">登录，然后选择 **非银箱银箱工序**。</span><span class="sxs-lookup"><span data-stu-id="22506-230">Sign in, and then select **Non-drawer drawer operations**.</span></span>
3. <span data-ttu-id="22506-231">使用 **管理硬件工作站** 操作打开一个硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="22506-231">Use the **Manage hardware stations** operation to turn on a hardware station.</span></span>
4. <span data-ttu-id="22506-232">选择您为收银机创建的硬件工作站以将其激活。</span><span class="sxs-lookup"><span data-stu-id="22506-232">Select the hardware station that you created for the register to make it active.</span></span>
5. <span data-ttu-id="22506-233">注销 POS，重新登录，然后打开一个班次。</span><span class="sxs-lookup"><span data-stu-id="22506-233">Sign out of the POS, sign back in, and open a shift.</span></span>

<span data-ttu-id="22506-234">现在，分配给硬件配置文件的付款终端将始终处于活动状态，系统会在需要收据打印机或银箱时提示您。</span><span class="sxs-lookup"><span data-stu-id="22506-234">The payment terminal that is assigned to the hardware profile will now always be active, and you will be prompted if a receipt printer or cash drawer is required.</span></span>

<span data-ttu-id="22506-235">许多要求此功能的商家都希望通过提供电子邮件收据和鼓励电子付款来减少浪费。</span><span class="sxs-lookup"><span data-stu-id="22506-235">Many merchants who requested this feature are interested in reducing waste by providing email receipts and encouraging electronic payments.</span></span> <span data-ttu-id="22506-236">根据 POS 的配置，仅当客户需要实体收据或要用现金支付时，系统才会提示商店员工选择收据打印机或银箱。</span><span class="sxs-lookup"><span data-stu-id="22506-236">Depending on the configuration of the POS, store associates are prompted to select a receipt printer or cash drawer only when a customer wants a physical receipt or wants to pay with cash.</span></span>

<span data-ttu-id="22506-237">每次交易仅提示商店员工选择硬件工作站一次，除非必须打印收据并且使用现金付款，否则最初选择的硬件配置文件不会同时包括这两种设备。</span><span class="sxs-lookup"><span data-stu-id="22506-237">Store associates are prompted to select a hardware station only one time per transaction, unless a receipt must be printed and cash is used for payment, but the hardware profile that was originally selected doesn't include both devices.</span></span> <span data-ttu-id="22506-238">在这种情况下，将再次提示商店员工选择可用于完成交易的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="22506-238">In that case, the store associate will be prompted again to select a hardware station that can be used to complete the transaction.</span></span>

## <a name="related-articles"></a><span data-ttu-id="22506-239">相关文章</span><span class="sxs-lookup"><span data-stu-id="22506-239">Related articles</span></span>

- [<span data-ttu-id="22506-240">在 Android 和 iOS 中安装 POS Hybrid 应用</span><span class="sxs-lookup"><span data-stu-id="22506-240">Set up POS hybrid app on Android and iOS</span></span>](./dev-itpro/hybridapp.md)
- [<span data-ttu-id="22506-241">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="22506-241">Dynamics 365 Payment Connector for Adyen</span></span>](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [<span data-ttu-id="22506-242">网络外围设备支持概述</span><span class="sxs-lookup"><span data-stu-id="22506-242">Network peripheral support overview</span></span>](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
