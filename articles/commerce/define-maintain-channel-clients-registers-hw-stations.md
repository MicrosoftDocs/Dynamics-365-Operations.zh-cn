---
title: 将外设连接到销售点 (POS)
description: 此主题介绍如何将外设连接到 Retail POS。
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ec64cb8a7c490c6798a897fd20a56e5af5c8be3a
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057929"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a><span data-ttu-id="9e450-103">将外设连接到销售点 (POS)</span><span class="sxs-lookup"><span data-stu-id="9e450-103">Connect peripherals to the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e450-104">此主题介绍如何将外设连接到 Retail POS。</span><span class="sxs-lookup"><span data-stu-id="9e450-104">This topic covers how to connect peripherals to your Retail POS.</span></span>

> [!NOTE]
> <span data-ttu-id="9e450-105">要获取特定的安装说明，请参阅[配置并安装 Retail Hardware Station](retail-hardware-station-configuration-installation.md) 和[配置、安装和激活 Modern POS (MPOS)](retail-modern-pos-device-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="9e450-105">For specific installation instructions, see [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) and [Configure, install, and activate Modern POS (MPOS)](retail-modern-pos-device-activation.md).</span></span>

## <a name="key-components"></a><span data-ttu-id="9e450-106">重要组件</span><span class="sxs-lookup"><span data-stu-id="9e450-106">Key components</span></span>

<span data-ttu-id="9e450-107">有几个组件用于定义商店、销售点 (POS) 收银机或商店内渠道，以及这些收银机或渠道用于处理交易的外设之间的关系。</span><span class="sxs-lookup"><span data-stu-id="9e450-107">Several components are used to define the relationships among a store, the point-of-sale (POS) registers or channels within the store, and the peripherals that those registers or channels use to process transactions.</span></span> <span data-ttu-id="9e450-108">此部分介绍每个组件，并说明它在商店部署中的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9e450-108">This section describes each component and explains how it should be used in a store deployment.</span></span>

### <a name="pos-registers"></a><span data-ttu-id="9e450-109">POS 收银机</span><span class="sxs-lookup"><span data-stu-id="9e450-109">POS registers</span></span>

<span data-ttu-id="9e450-110">导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="9e450-110">Navigation: Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>

<span data-ttu-id="9e450-111">POS 收银机是用来定义特定 POS 实例的特征的实体。</span><span class="sxs-lookup"><span data-stu-id="9e450-111">The POS register is an entity that is used to define the characteristics of a specific instance of the POS.</span></span> <span data-ttu-id="9e450-112">这些特征包括外设的硬件配置文件或设置，它们将被用于收银机、收银机映射到的商店，以及登录该收银机的用户的视觉体验。</span><span class="sxs-lookup"><span data-stu-id="9e450-112">These characteristics include the hardware profile or setup for peripherals that will be used at the register, the store that the register is mapped to, and the visual experience for the user who logs on to that register.</span></span>

### <a name="devices"></a><span data-ttu-id="9e450-113">设备</span><span class="sxs-lookup"><span data-stu-id="9e450-113">Devices</span></span>

<span data-ttu-id="9e450-114">导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **设备**。</span><span class="sxs-lookup"><span data-stu-id="9e450-114">Navigation: Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**.</span></span>

<span data-ttu-id="9e450-115">设备是表示映射到 POS 收银机的设备的物理实例的实体。</span><span class="sxs-lookup"><span data-stu-id="9e450-115">A device is an entity that represents a physical instance of a device that is mapped to a POS register.</span></span> <span data-ttu-id="9e450-116">当创建一个设备时，它被映射到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="9e450-116">When a device is created, it's mapped to a POS register.</span></span> <span data-ttu-id="9e450-117">设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。</span><span class="sxs-lookup"><span data-stu-id="9e450-117">The device entity tracks information about when a POS register is activated, the type of client that is being used, and the application package that has been deployed to a specific device.</span></span> <span data-ttu-id="9e450-118">设备可以有两种类型︰**Retail modern POS** (MPOS) 或 **Retail Cloud POS** (Cloud POS)。</span><span class="sxs-lookup"><span data-stu-id="9e450-118">Devices can be of two types: **Retail modern POS** (MPOS) or **Retail Cloud POS** (Cloud POS).</span></span>

#### <a name="mpos"></a><span data-ttu-id="9e450-119">MPOS</span><span class="sxs-lookup"><span data-stu-id="9e450-119">MPOS</span></span>

<span data-ttu-id="9e450-120">MPO 是安装在 Windows 8.1 或基于 PC 的更高版本的操作系统上的 POS 客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="9e450-120">MPOS is a POS client application that is installed on Windows 8.1 or a later PC-based operating system.</span></span> <span data-ttu-id="9e450-121">如果 **Retail modern POS** 应用程序类型映射到设备，可以为特定设备指定下载包。</span><span class="sxs-lookup"><span data-stu-id="9e450-121">If the **Retail modern POS** application type is mapped to a device, the download package can be specified for a particular device.</span></span> <span data-ttu-id="9e450-122">可以自定义下载包以包括不同版本的安装程序包。</span><span class="sxs-lookup"><span data-stu-id="9e450-122">The download package can be customized to include different versions of the installation package.</span></span> <span data-ttu-id="9e450-123">部署不同的程序包的能力提供了灵活性，满足了不同收银机可能需要不同集成的情况的需求。</span><span class="sxs-lookup"><span data-stu-id="9e450-123">The ability to deploy different packages provides flexibility in cases where different POS registers might need different integrations.</span></span> <span data-ttu-id="9e450-124">MPOS 与内置的硬件工作站一同部署。</span><span class="sxs-lookup"><span data-stu-id="9e450-124">MPOS is deployed together with a built-in hardware station.</span></span>

#### <a name="cloud-pos"></a><span data-ttu-id="9e450-125">云 POS</span><span class="sxs-lookup"><span data-stu-id="9e450-125">Cloud POS</span></span>

<span data-ttu-id="9e450-126">Cloud POS 是基于浏览器的 POS。</span><span class="sxs-lookup"><span data-stu-id="9e450-126">Cloud POS is a browser-based POS.</span></span> <span data-ttu-id="9e450-127">因为在浏览器中运行，Cloud POS 不需要 Windows 8.1 或基于 PC 的更高版本的操作系统。</span><span class="sxs-lookup"><span data-stu-id="9e450-127">Because it runs in the browser, Cloud POS doesn't require Windows 8.1 or a later PC-based operating system.</span></span> <span data-ttu-id="9e450-128">如果 **Retail Cloud POS** 应用程序类型映射到“总部”中的特定设备，该设备可通过浏览器使用，不需要下载或安装程序包。</span><span class="sxs-lookup"><span data-stu-id="9e450-128">If the **Retail Cloud POS** application type is mapped to a specific device in Headquarters, that device can be used through the browser with no need to download or install a package.</span></span> <span data-ttu-id="9e450-129">Cloud POS 需要硬件工作站使用除基于键盘口的条码扫描以外的硬件。</span><span class="sxs-lookup"><span data-stu-id="9e450-129">Cloud POS requires a hardware station to use hardware beyond keyboard wedge based bar code scanning.</span></span>

### <a name="hardware-profile"></a><span data-ttu-id="9e450-130">硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-130">Hardware profile</span></span>

<span data-ttu-id="9e450-131">导航︰单击**商业** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="9e450-131">Navigation: Click **Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>

<span data-ttu-id="9e450-132">硬件配置文件确定连接到 POS 收银机或硬件工作站的硬件。</span><span class="sxs-lookup"><span data-stu-id="9e450-132">A hardware profile identifies the hardware that is connected to a POS register or a hardware station.</span></span> <span data-ttu-id="9e450-133">硬件配置文件还用于指定应在与付款软件开发套件 (SDK) 通信过程中使用的付款处理器参数。</span><span class="sxs-lookup"><span data-stu-id="9e450-133">The hardware profile is also used to specify the payment processor parameters that should be used during communication with the payment software development kit (SDK).</span></span> <span data-ttu-id="9e450-134">（付款 SDK 部署为硬件工作站的一部分。）</span><span class="sxs-lookup"><span data-stu-id="9e450-134">(The payment SDK is deployed as part of the hardware station.)</span></span>

### <a name="hardware-station"></a><span data-ttu-id="9e450-135">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="9e450-135">Hardware station</span></span>

<span data-ttu-id="9e450-136">导航：单击 **Retail 和 Commerce** &gt; **渠道** &gt; **商店** &gt; **所有商店**。</span><span class="sxs-lookup"><span data-stu-id="9e450-136">Navigation: Click **Retail and Commerce** &gt; **Channels** &gt; **Stores** &gt; **All stores**.</span></span> <span data-ttu-id="9e450-137">选择一个商店，然后单击**硬件工作站**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="9e450-137">Select a store, and then click the **Hardware stations** FastTab.</span></span>

<span data-ttu-id="9e450-138">硬件工作站是驱动 POS 外设的业务逻辑的一个实例。</span><span class="sxs-lookup"><span data-stu-id="9e450-138">A hardware station is an instance of business logic that drives POS peripherals.</span></span> <span data-ttu-id="9e450-139">硬件工作站与 MPOS 一同自动安装。</span><span class="sxs-lookup"><span data-stu-id="9e450-139">A hardware station is automatically installed together with MPOS.</span></span> <span data-ttu-id="9e450-140">或者，硬件工作站可以作为独立的组件安装，然后通过 Web 服务由 MPOS 或 Cloud POS 访问。</span><span class="sxs-lookup"><span data-stu-id="9e450-140">Alternatively, the hardware station can be installed as a stand-alone component, and then accessed by MPOS or Cloud POS through a web service.</span></span> <span data-ttu-id="9e450-141">必须在渠道级别定义硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-141">The hardware station must be defined at the channel level.</span></span>

### <a name="hardware-station-profile"></a><span data-ttu-id="9e450-142">硬件工作站配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-142">Hardware station profile</span></span>

<span data-ttu-id="9e450-143">导航︰单击**商业** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件工作站配置文件**。</span><span class="sxs-lookup"><span data-stu-id="9e450-143">Navigation: Click **Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware station profiles**.</span></span>

<span data-ttu-id="9e450-144">由于硬件工作站本身在渠道级别指定，其包括实例特定信息，如硬件工作站的 URL，硬件工作站配置文件包括可以是静态的跨多个硬件工作站共享的信息。</span><span class="sxs-lookup"><span data-stu-id="9e450-144">Whereas the hardware station itself is specified at the channel level includes instance-specific information, such as the URL for the hardware station, the hardware station profile includes information that can be static or shared across multiple hardware stations.</span></span> <span data-ttu-id="9e450-145">静态信息包括应使用的端口、硬件工作站包和硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-145">The static information includes the port that should be used, the hardware station package, and the hardware profile.</span></span> <span data-ttu-id="9e450-146">静态信息还包括部署的硬件工作站的类型的描述，如**结帐**或**退货**，具体取决于每个特定硬件工作站所需的硬件。</span><span class="sxs-lookup"><span data-stu-id="9e450-146">The static information also includes a description of the type of hardware station that is being deployed, such as **Checkout** or **Returns**, depending on the hardware that is required for each specific hardware station.</span></span>

## <a name="scenarios"></a><span data-ttu-id="9e450-147">方案</span><span class="sxs-lookup"><span data-stu-id="9e450-147">Scenarios</span></span>

### <a name="mpos-with-connected-peripheral-devices"></a><span data-ttu-id="9e450-148">具有连接的外设的 MPOS</span><span class="sxs-lookup"><span data-stu-id="9e450-148">MPOS with connected peripheral devices</span></span>

<span data-ttu-id="9e450-149">[![传统的固定销售点](./media/traditional-300x279.png)](./media/traditional.png)</span><span class="sxs-lookup"><span data-stu-id="9e450-149">[![Traditional, fixed point of sale](./media/traditional-300x279.png)](./media/traditional.png)</span></span>

<span data-ttu-id="9e450-150">若要在传统的固定 POS 情景中将 MPOS 连接到 POS 外设，首先导航到收银机本身，并为其分配一个硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-150">To connect MPOS to POS peripherals in a traditional, fixed POS scenario, first navigate to the register itself, and assign a hardware profile to it.</span></span> <span data-ttu-id="9e450-151">您可以在 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**中找到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="9e450-151">You can find the POS registers at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> 

<span data-ttu-id="9e450-152">分配硬件配置文件后，通过使用**收银机**分配计划同步对渠道数据库的更改。</span><span class="sxs-lookup"><span data-stu-id="9e450-152">After you've assigned the hardware profile, sync changes to the channel database by using the **Registers** distribution schedule.</span></span> <span data-ttu-id="9e450-153">您可以在 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划**中找到分配计划。</span><span class="sxs-lookup"><span data-stu-id="9e450-153">You can find the distribution schedules at **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span> 

<span data-ttu-id="9e450-154">接下来，设置渠道中的“本地”硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-154">Next, set up a "local" hardware station on the channel.</span></span> <span data-ttu-id="9e450-155">单击 **Retail 和 Commerce** &gt; **渠道** &gt; **商店** &gt; **所有商店**，然后选择一个商店。</span><span class="sxs-lookup"><span data-stu-id="9e450-155">Click **Retail and Commerce** &gt; **Channels** &gt; **Stores** &gt; **All stores**, and select a store.</span></span> 

<span data-ttu-id="9e450-156">然后，在**硬件工作站**快速选项卡上，单击**添加**添加硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-156">Then, on the **Hardware stations** FastTab, click **Add** to add a hardware station.</span></span> <span data-ttu-id="9e450-157">输入描述，输入 **localhost** 作为主机名，然后通过使用**渠道配置**分配计划同步对渠道的更改。</span><span class="sxs-lookup"><span data-stu-id="9e450-157">Enter a description, enter **localhost** as the host name, and then sync the changes to the channel by using the **Channel configuration** distribution schedule.</span></span> <span data-ttu-id="9e450-158">您可以在 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划**中找到分配计划。</span><span class="sxs-lookup"><span data-stu-id="9e450-158">You can find the distribution schedules at **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span> 

<span data-ttu-id="9e450-159">最后，在 MPOS，使用**选择硬件工作站**操作来选择 **localhost** 硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-159">Finally, in MPOS, use the **Select hardware station** operation to select the **localhost** hardware station.</span></span> <span data-ttu-id="9e450-160">设置硬件工作站为**有效**。</span><span class="sxs-lookup"><span data-stu-id="9e450-160">Set the hardware station to **Active**.</span></span> <span data-ttu-id="9e450-161">在此情景中使用的硬件配置文件应来自 POS 收银机本身。</span><span class="sxs-lookup"><span data-stu-id="9e450-161">The hardware profile that is used in this scenario should come from the POS register itself.</span></span> <span data-ttu-id="9e450-162">此情况不需要硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-162">A hardware station profile isn't required for this scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="9e450-163">某些硬件配置文件的更改（如对银箱的更改）需要在与渠道同步更改后打开新班次。</span><span class="sxs-lookup"><span data-stu-id="9e450-163">Some hardware profile changes, such as changes to cash drawers, require that a new shift be opened after the changes have been synced to the channel.</span></span>
>
> <span data-ttu-id="9e450-164">Cloud POS 必须使用独立的硬件工作站来与外设通信。</span><span class="sxs-lookup"><span data-stu-id="9e450-164">Cloud POS must use the stand-alone hardware station to communicate with peripherals.</span></span>

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a><span data-ttu-id="9e450-165">具有独立硬件工作站的 MPOS 或 Cloud POS</span><span class="sxs-lookup"><span data-stu-id="9e450-165">MPOS or Cloud POS with a stand-alone hardware station</span></span>

<span data-ttu-id="9e450-166">[![共享外设](./media/shared-300x254.png)](./media/shared.png)</span><span class="sxs-lookup"><span data-stu-id="9e450-166">[![Shared peripherals](./media/shared-300x254.png)](./media/shared.png)</span></span>

<span data-ttu-id="9e450-167">在这种情况下，独立硬件工作站在 MPOS 和 Cloud POS 客户端之间共享。</span><span class="sxs-lookup"><span data-stu-id="9e450-167">In this scenario, a stand-alone hardware station is shared among MPOS and Cloud POS clients.</span></span> <span data-ttu-id="9e450-168">这种情况要求您创建硬件工作站配置文件以指定下载包、端口和硬件工作站使用的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-168">This scenario requires that you create a hardware station profile to specify the download package, port, and hardware profile that the hardware station uses.</span></span> <span data-ttu-id="9e450-169">您可以在 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件工作站配置文件**中找到硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-169">You can find the hardware station profile at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware station profiles**.</span></span> 

<span data-ttu-id="9e450-170">创建了硬件工作站配置文件后，导航到特定渠道（**Retail 和 Commerce** &gt; **渠道** &gt; **商店** &gt; **所有商店**），添加新的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-170">After you've created the hardware station profile, navigate to the specific channel (**Retail and Commerce** &gt; **Channels** &gt; **Stores** &gt; **All stores**), and add a new hardware station.</span></span> <span data-ttu-id="9e450-171">将此新硬件工作站映射到以前创建的硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-171">Map this new hardware station to the hardware station profile that was previously created.</span></span> 

<span data-ttu-id="9e450-172">接下来，提供有助于出纳识别硬件工作站的描述。</span><span class="sxs-lookup"><span data-stu-id="9e450-172">Next, provide a description that will help the cashier identify the hardware station.</span></span> <span data-ttu-id="9e450-173">在**主机名**字段中，以下面的格式输入主机计算机 URL：`https://<MachineName:Port>/HardwareStation`。</span><span class="sxs-lookup"><span data-stu-id="9e450-173">In the **Host name** field, enter the host machine URL in the following format: `https://<MachineName:Port>/HardwareStation`.</span></span> <span data-ttu-id="9e450-174">（将 **&lt;MachineName:Port&gt;** 替换为在硬件工作站配置文件中指定的硬件工作站和端口的实际计算机名称。）对于独立硬件工作站，则还应指定电子资金转帐 (EFT) 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="9e450-174">(Replace **&lt;MachineName:Port&gt;** with the actual machine name of the hardware station and the port that is specified in the hardware station profile.) For a stand-alone hardware station, you should also specify the electronic funds transfer (EFT) terminal ID.</span></span> <span data-ttu-id="9e450-175">此值标识当付款连接器与付款提供商通信时，连接到硬件工作站的 EFT 终端。</span><span class="sxs-lookup"><span data-stu-id="9e450-175">This value identifies the EFT terminal that is connected to the hardware station when the payment connector communicates with the payment provider.</span></span> 

<span data-ttu-id="9e450-176">下一步，从实际硬件工作站计算机，导航到渠道，然后选择硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-176">Next, from the actual hardware station machine, navigate to the channel, and select the hardware station.</span></span> <span data-ttu-id="9e450-177">然后单击**下载**，并安装硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-177">Then click **Download**, and install the hardware station.</span></span> 

<span data-ttu-id="9e450-178">接下来，从 MPOS 或 Cloud POS，使用**选择硬件工作站**操作来选择以前已安装的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="9e450-178">Next, from MPOS or Cloud POS, use the **Select hardware station** operation to select the hardware station that was previously installed.</span></span> <span data-ttu-id="9e450-179">选择**配对**在 POS 和硬件工作站之间建立安全关系。</span><span class="sxs-lookup"><span data-stu-id="9e450-179">Select **Pair** to establish a secure relationship between the POS and the hardware station.</span></span> <span data-ttu-id="9e450-180">必须为每个 POS 和硬件工作站完成一次此步骤。</span><span class="sxs-lookup"><span data-stu-id="9e450-180">This step must be completed once for every combination of a POS and a hardware station.</span></span> 

<span data-ttu-id="9e450-181">配对硬件工作站后，使用相同的操作使硬件工作站在使用时有效。</span><span class="sxs-lookup"><span data-stu-id="9e450-181">After the hardware station is paired, the same operation is used to make the hardware station active while it's used.</span></span> <span data-ttu-id="9e450-182">这种情况下，应将硬件配置文件分配到硬件工作站配置文件，而不是收银机本身。</span><span class="sxs-lookup"><span data-stu-id="9e450-182">For this scenario, the hardware profile should be assigned to the hardware station profile rather than the register itself.</span></span> <span data-ttu-id="9e450-183">如果由于某种原因硬件工作站没有直接分配的硬件配置文件，则将使用分配给收银机的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-183">If for some reason a hardware station does not have a hardware profile directly assigned, then the hardware profile assigned to the register is used.</span></span>

## <a name="client-maintenance"></a><span data-ttu-id="9e450-184">客户端维护</span><span class="sxs-lookup"><span data-stu-id="9e450-184">Client maintenance</span></span>

### <a name="registers"></a><span data-ttu-id="9e450-185">收银机</span><span class="sxs-lookup"><span data-stu-id="9e450-185">Registers</span></span>

<span data-ttu-id="9e450-186">POS 收银机主要通过收银机本身管理，同时还通过分配到收银机的配置文件管理。</span><span class="sxs-lookup"><span data-stu-id="9e450-186">POS registers are managed primarily through the registers themselves, and also through the profiles that are assigned to registers.</span></span> <span data-ttu-id="9e450-187">特定于单个收银机的属性在收银机级别管理。</span><span class="sxs-lookup"><span data-stu-id="9e450-187">Attributes that are specific to an individual register are managed at the register level.</span></span> <span data-ttu-id="9e450-188">这些属性包括使用收银机的商店、收银机编号、描述和特定于收银机本身的 EFT 终端 ID。</span><span class="sxs-lookup"><span data-stu-id="9e450-188">These attributes include the store where the register is used, the register number, the description, and the EFT terminal ID that is specific to the register itself.</span></span>

### <a name="pos-profiles"></a><span data-ttu-id="9e450-189">POS 配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-189">POS profiles</span></span>

<span data-ttu-id="9e450-190">您可以在 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件**中找到 POS 配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-190">You can find the POS profiles at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles**.</span></span> <span data-ttu-id="9e450-191">对于通过配置文件管理收银机的很多方面非常有用，因为可以在多个收银机之间共享配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-191">It's useful to manage many aspects of a register through profiles, because the profiles can be shared among many registers.</span></span> <span data-ttu-id="9e450-192">配置文件可映射到单个收银机或商店（如果配置文件在商店范围内有效）。</span><span class="sxs-lookup"><span data-stu-id="9e450-192">Profiles can be mapped either to an individual register or, if a profile is effective on a store-wide basis, to the store.</span></span> <span data-ttu-id="9e450-193">以下各部分描述了 POS 配置文件以及如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="9e450-193">The following sections describe the POS profiles and how they are used.</span></span>

#### <a name="offline-profile"></a><span data-ttu-id="9e450-194">脱机配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-194">Offline profile</span></span>

<span data-ttu-id="9e450-195">脱机配置文件在商店级别设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-195">The offline profile is set at the store level.</span></span> <span data-ttu-id="9e450-196">它用于指定在 POS 收银机（该收银机未连接到渠道数据库）执行的交易的上载设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-196">It's used to specify the upload settings for transactions that are performed on a POS register while that register isn't connected to the channel database.</span></span>

#### <a name="functionality-profile"></a><span data-ttu-id="9e450-197">功能配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-197">Functionality profile</span></span>

<span data-ttu-id="9e450-198">功能配置文件在商店级别设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-198">The functionality profile is set at the store level.</span></span> <span data-ttu-id="9e450-199">它用于指定可在 POS 执行的功能的商店范围设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-199">It's used to specify store-wide settings about the functions that can be performed at the POS.</span></span> <span data-ttu-id="9e450-200">以下功能通过功能配置文件进行管理。</span><span class="sxs-lookup"><span data-stu-id="9e450-200">The following capabilities are managed through the functionality profile.</span></span> <span data-ttu-id="9e450-201">这些功能按快速选项卡排列。</span><span class="sxs-lookup"><span data-stu-id="9e450-201">These capabilities are arranged by FastTab.</span></span>

- <span data-ttu-id="9e450-202">**常规**快速选项卡：</span><span class="sxs-lookup"><span data-stu-id="9e450-202">**General** FastTab:</span></span>

    - <span data-ttu-id="9e450-203">国际标准化组织 (ISO)。</span><span class="sxs-lookup"><span data-stu-id="9e450-203">International Organization for Standardization (ISO).</span></span>
    - <span data-ttu-id="9e450-204">在脱机模式下创建客户。</span><span class="sxs-lookup"><span data-stu-id="9e450-204">Create a customer in offline mode.</span></span>
    - <span data-ttu-id="9e450-205">通过电子邮件发送收据模板。</span><span class="sxs-lookup"><span data-stu-id="9e450-205">Email receipt profile.</span></span>
    - <span data-ttu-id="9e450-206">集中职员登录身份验证。</span><span class="sxs-lookup"><span data-stu-id="9e450-206">Central staff logon authentication.</span></span>

- <span data-ttu-id="9e450-207">**功能**快速选项卡︰</span><span class="sxs-lookup"><span data-stu-id="9e450-207">**Functions** FastTab:</span></span>

    - <span data-ttu-id="9e450-208">登录和扩展登录管理。</span><span class="sxs-lookup"><span data-stu-id="9e450-208">Management of logon and extended logon.</span></span>
    - <span data-ttu-id="9e450-209">POS 的财务和货币相关方面，如键入价格以及次要币种是否需要小数的能力。</span><span class="sxs-lookup"><span data-stu-id="9e450-209">Financial and currency-related aspects of the POS, such as the ability to key in prices and whether decimals are required for minor currency.</span></span>
    - <span data-ttu-id="9e450-210">通过 POS 启用时间登记。</span><span class="sxs-lookup"><span data-stu-id="9e450-210">Enabling time registration through the POS.</span></span>
    - <span data-ttu-id="9e450-211">产品和付款在 POS 和收据上的显示方式。</span><span class="sxs-lookup"><span data-stu-id="9e450-211">How products and payments appear in the POS and on receipts.</span></span>
    - <span data-ttu-id="9e450-212">日结管理。</span><span class="sxs-lookup"><span data-stu-id="9e450-212">End-of-day management.</span></span>
    - <span data-ttu-id="9e450-213">渠道数据库交易记录保留参数。</span><span class="sxs-lookup"><span data-stu-id="9e450-213">Channel database transaction retention parameters.</span></span>
    - <span data-ttu-id="9e450-214">如何从 POS 查找和创建客户。</span><span class="sxs-lookup"><span data-stu-id="9e450-214">How customers are looked up and created from the POS.</span></span>
    - <span data-ttu-id="9e450-215">如何计算折扣。</span><span class="sxs-lookup"><span data-stu-id="9e450-215">How discounts are calculated.</span></span>

- <span data-ttu-id="9e450-216">**金额**快速选项卡︰</span><span class="sxs-lookup"><span data-stu-id="9e450-216">**Amount** FastTab:</span></span>

    - <span data-ttu-id="9e450-217">允许的最大和最小价格。</span><span class="sxs-lookup"><span data-stu-id="9e450-217">Maximum and minimum prices that are allowed.</span></span>
    - <span data-ttu-id="9e450-218">折扣应用和计算。</span><span class="sxs-lookup"><span data-stu-id="9e450-218">Discount application and calculation.</span></span>

- <span data-ttu-id="9e450-219">**信息代码**快速选项卡：</span><span class="sxs-lookup"><span data-stu-id="9e450-219">**Info codes** FastTab:</span></span>

    - <span data-ttu-id="9e450-220">如何在 POS 管理信息代码的所有方面。</span><span class="sxs-lookup"><span data-stu-id="9e450-220">All aspects of how info codes are managed at the POS.</span></span> <span data-ttu-id="9e450-221">有关详细信息，请参阅[信息代码和信息代码组](info-codes-retail.md)。</span><span class="sxs-lookup"><span data-stu-id="9e450-221">For details, see [Info codes and info code groups](info-codes-retail.md).</span></span>

- <span data-ttu-id="9e450-222">**收据编号**快速选项卡：</span><span class="sxs-lookup"><span data-stu-id="9e450-222">**Receipt numbering** FastTab:</span></span>

    - <span data-ttu-id="9e450-223">指定收据编号掩码，其中可能包括商店编号段、终端编号段、常量段，以及销售、退货、销售订单和报价单是否以单独顺序打印，或它们是否都按照相同的顺序。</span><span class="sxs-lookup"><span data-stu-id="9e450-223">Specify receipt numbering masks, which might include segments for the store number, terminal number, constants, and whether sales, returns, sales orders, and quotations are printed in separate sequences, or whether they all following the same sequence.</span></span>

#### <a name="receipt-profiles"></a><span data-ttu-id="9e450-224">收据模板</span><span class="sxs-lookup"><span data-stu-id="9e450-224">Receipt profiles</span></span>

<span data-ttu-id="9e450-225">收据模板在硬件配置文件内分配到打印机。</span><span class="sxs-lookup"><span data-stu-id="9e450-225">Receipts profiles are assigned to printers within the hardware profile.</span></span> <span data-ttu-id="9e450-226">它们用来指定在特定打印机上打印的收据类型。</span><span class="sxs-lookup"><span data-stu-id="9e450-226">They are used to specify the receipt types that are printed at a specific printer.</span></span> <span data-ttu-id="9e450-227">配置文件包括收据格式的设置，以及确定是否始终打印收据，或是否提示出纳决定是否必须打印收据的设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-227">The profiles include settings for the receipt formats, and settings that determine whether the receipt is always printed, or whether the cashier is prompted to decide whether the receipt must be printed.</span></span> <span data-ttu-id="9e450-228">不同的打印机也可能使用不同的收据模板。</span><span class="sxs-lookup"><span data-stu-id="9e450-228">Different printers might also use different receipt profiles.</span></span> <span data-ttu-id="9e450-229">例如，打印机 1 是标准的热敏收据打印机，因此具有较小的收据格式。</span><span class="sxs-lookup"><span data-stu-id="9e450-229">For example, printer 1 is a standard thermal receipt printer, and therefore has smaller receipt formats.</span></span> <span data-ttu-id="9e450-230">但是，打印机 2 是全尺寸收据打印机，仅用于打印客户订单收据，这需要更多的空间。</span><span class="sxs-lookup"><span data-stu-id="9e450-230">However, printer 2 is a full-size receipt printer that is used to print only customer order receipts, which require more space.</span></span>

#### <a name="hardware-profiles"></a><span data-ttu-id="9e450-231">硬件配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-231">Hardware profiles</span></span>

<span data-ttu-id="9e450-232">硬件配置文件作为本文前面介绍的客户端设置的组件介绍。</span><span class="sxs-lookup"><span data-stu-id="9e450-232">Hardware profiles are explained as a component for client setup earlier in this article.</span></span> <span data-ttu-id="9e450-233">直接向 POS 收银机或硬件工作站配置文件分配硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-233">Hardware profiles are assigned directly to the POS register or to a hardware station profile.</span></span> <span data-ttu-id="9e450-234">它们用来指定 POS 收银机或硬件工作站使用的设备类型。</span><span class="sxs-lookup"><span data-stu-id="9e450-234">They are used to specify the types of devices a specific POS register or hardware station uses.</span></span> <span data-ttu-id="9e450-235">硬件配置文件还用于指定用于与付款 SDK 通信的 EFT 设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-235">Hardware profiles are also used to specify the EFT settings that are used to communicate with the payment SDK.</span></span>

#### <a name="visual-profiles"></a><span data-ttu-id="9e450-236">可视化配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-236">Visual profiles</span></span>

<span data-ttu-id="9e450-237">可视化配置文件在收银机级别分配。</span><span class="sxs-lookup"><span data-stu-id="9e450-237">Visual profiles are assigned at the register level.</span></span> <span data-ttu-id="9e450-238">它们用来指定特定收银机的主题。</span><span class="sxs-lookup"><span data-stu-id="9e450-238">They are used to specify the theme for a specific register.</span></span> <span data-ttu-id="9e450-239">配置文件包含使用的应用程序类型（MPOS 或 Cloud POS）、个性色和主题、字体方案、登录背景以及 POS 背景的设置。</span><span class="sxs-lookup"><span data-stu-id="9e450-239">The profiles include settings for the type of application that is used (MPOS or Cloud POS), the accent color and theme, the font scheme, the logon background, and the POS background.</span></span>

### <a name="custom-fields"></a><span data-ttu-id="9e450-240">自定义字段</span><span class="sxs-lookup"><span data-stu-id="9e450-240">Custom fields</span></span>

<span data-ttu-id="9e450-241">您可以创建自定义字段以添加未现成提供的字段到 POS。</span><span class="sxs-lookup"><span data-stu-id="9e450-241">You can create custom fields to add fields that aren't provided out of the box to the POS.</span></span> <span data-ttu-id="9e450-242">有关如何使用自定义字段的详细信息，请参阅[使用自定义字段博客文章](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/)。</span><span class="sxs-lookup"><span data-stu-id="9e450-242">For more information about how to use custom fields, see the [Working with custom fields blog post](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).</span></span>

### <a name="language-text"></a><span data-ttu-id="9e450-243">语言文本</span><span class="sxs-lookup"><span data-stu-id="9e450-243">Language text</span></span>

<span data-ttu-id="9e450-244">您可以通过使用语言文本条目覆盖 POS 中的默认字符串。</span><span class="sxs-lookup"><span data-stu-id="9e450-244">You can override default strings in the POS by using language text entries.</span></span> <span data-ttu-id="9e450-245">若要覆盖 POS 中的字符串，添加新的语言文本行。</span><span class="sxs-lookup"><span data-stu-id="9e450-245">To override a string in the POS, add a new language text line.</span></span> <span data-ttu-id="9e450-246">然后指定 ID，应覆盖的默认字符串，以及应在 POS 而不是默认字符串显示的文本。</span><span class="sxs-lookup"><span data-stu-id="9e450-246">Then specify an ID, the default string that should be overridden, and the text that should be shown at the POS instead of the default string.</span></span>

### <a name="hardware-station-profiles"></a><span data-ttu-id="9e450-247">硬件工作站配置文件</span><span class="sxs-lookup"><span data-stu-id="9e450-247">Hardware station profiles</span></span>

<span data-ttu-id="9e450-248">在本文前面介绍了硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="9e450-248">Hardware station profiles are explained earlier in this article.</span></span> <span data-ttu-id="9e450-249">它们被用来向硬件工作站分配非实例特定信息。</span><span class="sxs-lookup"><span data-stu-id="9e450-249">They are used to assign non-instance-specific information to hardware stations.</span></span>

### <a name="channel-reports-configuration"></a><span data-ttu-id="9e450-250">渠道报告配置</span><span class="sxs-lookup"><span data-stu-id="9e450-250">Channel reports configuration</span></span>

<span data-ttu-id="9e450-251">您在**渠道报表配置**页设置可在零售渠道使用的报表。</span><span class="sxs-lookup"><span data-stu-id="9e450-251">You set up the reports that are available at the channel on the **Channel reports configuration** page.</span></span> <span data-ttu-id="9e450-252">您可以通过在 POS 提供报表的 XML 定义并将报表分配给特定权限组来创建新报表。</span><span class="sxs-lookup"><span data-stu-id="9e450-252">You can create new reports by providing the XML definition of the report and assigning the report to a specific permission group at the POS.</span></span>

### <a name="devices"></a><span data-ttu-id="9e450-253">设备</span><span class="sxs-lookup"><span data-stu-id="9e450-253">Devices</span></span>

<span data-ttu-id="9e450-254">在本文前面介绍了设备。</span><span class="sxs-lookup"><span data-stu-id="9e450-254">Devices are explained earlier in this article.</span></span> <span data-ttu-id="9e450-255">它们用来管理特定 POS 收银机的启用。</span><span class="sxs-lookup"><span data-stu-id="9e450-255">They are used to manage the activation of a specific POS register.</span></span> <span data-ttu-id="9e450-256">设备还用于指定用于特定收银机和安装程序包（应用于安装 MPOS 客户端）的应用程序。</span><span class="sxs-lookup"><span data-stu-id="9e450-256">Devices are also used to specify the application that is used for a specific register and the installation package that should be used to install the MPOS client.</span></span> <span data-ttu-id="9e450-257">下面是设备启用状态︰</span><span class="sxs-lookup"><span data-stu-id="9e450-257">Here are the device activation states:</span></span>

- <span data-ttu-id="9e450-258">**挂起** – 设备准备好被启用。</span><span class="sxs-lookup"><span data-stu-id="9e450-258">**Pending** – The device is ready to be activated.</span></span>
- <span data-ttu-id="9e450-259">**已启用** – 该设备已被启用。</span><span class="sxs-lookup"><span data-stu-id="9e450-259">**Activated** – The device has been activated.</span></span>
- <span data-ttu-id="9e450-260">**停用** – 已在“总部”或通过 POS 停用设备。</span><span class="sxs-lookup"><span data-stu-id="9e450-260">**Deactivated** – The device has been deactivated either in Headquarters or through the POS.</span></span>
- <span data-ttu-id="9e450-261">**禁用** – 该设备已被禁用。</span><span class="sxs-lookup"><span data-stu-id="9e450-261">**Disabled** – The device has been disabled.</span></span>

<span data-ttu-id="9e450-262">与启用相关的其他信息包括更改设备启用状态的工作人员、启用时间戳，以及设备配置是否已经过验证。</span><span class="sxs-lookup"><span data-stu-id="9e450-262">Additional activation-related information includes the worker who changed the activation status for the device, a time stamp for the activation, and whether the device configuration has been validated.</span></span>

### <a name="client-data-synchronization"></a><span data-ttu-id="9e450-263">客户端数据同步</span><span class="sxs-lookup"><span data-stu-id="9e450-263">Client data synchronization</span></span>

<span data-ttu-id="9e450-264">对 POS 客户端的所有更改（除设备启用状态的更改），均必须与渠道数据库同步以使其生效。</span><span class="sxs-lookup"><span data-stu-id="9e450-264">All changes to a POS client, except changes in the device activation status, must be synced to the channel database to take effect.</span></span> <span data-ttu-id="9e450-265">要同步对渠道数据库的更改，请导航到 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **配送计划**，并运行所需的配送计划。</span><span class="sxs-lookup"><span data-stu-id="9e450-265">To sync changes to the channel database, navigate to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**, and run the required distribution schedule.</span></span> <span data-ttu-id="9e450-266">对于客户端更改，应运行**收银机**和**渠道配置**配送计划。</span><span class="sxs-lookup"><span data-stu-id="9e450-266">For client changes, you should run the **Registers** and **Channel configuration** distribution schedules.</span></span>