---
title: 将外设连接到销售点 (POS)
description: 本文介绍如何将外设连接到 Retail POS。
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ffee75e1713c7c9d31b1d023cd055c2f1a3fc43d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897100"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>将外设连接到销售点 (POS)

[!include [banner](includes/banner.md)]

本文介绍如何将外设连接到 Retail POS。

> [!NOTE]
> 要获取特定的安装说明，请参阅[配置并安装 Retail Hardware Station](retail-hardware-station-configuration-installation.md) 和[配置、安装和激活 Modern POS (MPOS)](retail-modern-pos-device-activation.md)。

## <a name="key-components"></a>重要组件

有几个组件用于定义商店、销售点 (POS) 收银机或商店内渠道，以及这些收银机或渠道用于处理交易的外设之间的关系。 此部分介绍每个组件，并说明它在商店部署中的使用方式。

### <a name="pos-registers"></a>POS 收银机

导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。

POS 收银机是用来定义特定 POS 实例的特征的实体。 这些特征包括外设的硬件配置文件或设置，它们将被用于收银机、收银机映射到的商店，以及登录该收银机的用户的视觉体验。

### <a name="devices"></a>设备

导航：单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **设备**。

设备是表示映射到 POS 收银机的设备的物理实例的实体。 当创建一个设备时，它被映射到 POS 收银机。 设备实体跟踪 POS 收银机何时被激活，正在使用的客户端的类型，以及已经部署到特定设备应用程序包的信息。 设备可以有两种类型︰**Retail modern POS** (MPOS) 或 **Retail Cloud POS** (Cloud POS)。

#### <a name="mpos"></a>MPOS

MPO 是安装在 Windows 8.1 或基于 PC 的更高版本的操作系统上的 POS 客户端应用程序。 如果 **Retail modern POS** 应用程序类型映射到设备，可以为特定设备指定下载包。 可以自定义下载包以包括不同版本的安装程序包。 部署不同的程序包的能力提供了灵活性，满足了不同收银机可能需要不同集成的情况的需求。 MPOS 与内置的硬件工作站一同部署。

#### <a name="cloud-pos"></a>云 POS

Cloud POS 是基于浏览器的 POS。 因为在浏览器中运行，Cloud POS 不需要 Windows 8.1 或基于 PC 的更高版本的操作系统。 如果 **Retail Cloud POS** 应用程序类型映射到“总部”中的特定设备，该设备可通过浏览器使用，不需要下载或安装程序包。 Cloud POS 需要硬件工作站使用除基于键盘口的条码扫描以外的硬件。

### <a name="hardware-profile"></a>硬件配置文件

导航：转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 硬件配置文件**。

硬件配置文件确定通过集成或共享硬件工作站连接到 POS 收银机的硬件。 硬件配置文件还用于指定应在与付款软件开发套件 (SDK) 通信过程中使用的付款处理器参数。 付款 SDK 部署为硬件工作站的一部分。

### <a name="hardware-station"></a>硬件工作站

导航：转到 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**，选择商店，然后选择 **硬件工作站** 快速选项卡。

硬件工作站是驱动 POS 外设的业务逻辑的一个实例。 硬件工作站与 MPOS 一同自动安装。 或者，硬件工作站可以作为独立的组件安装，然后通过 Web 服务由 MPOS 或 Cloud POS 访问。 必须在渠道级别定义硬件工作站。

## <a name="scenarios"></a>方案

### <a name="mpos-with-connected-peripheral-devices"></a>具有连接的外设的 MPOS

[![传统的固定销售点。](./media/traditional-300x279.png)](./media/traditional.png)

若要在传统的固定 POS 情景中将 MPOS 连接到 POS 外设，首先导航到收银机本身，并为其分配一个硬件配置文件。 您可以在 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机** 中找到 POS 收银机。 

分配硬件配置文件后，通过使用 **收银机** 分配计划同步对渠道数据库的更改。 您可以在 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划** 中找到分配计划。 

接下来，在渠道中设置专用硬件工作站。 转到 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**，选择商店。 

然后，在 **硬件工作站** 快速选项卡上，选择 **添加** 添加硬件工作站。 选择 **专用** 作为硬件工作站类型，然后输入说明。 **硬件配置文件** 字段可以留空，因为在此场景中使用的硬件配置文件来自 POS 收银机本身。 然后使用 **渠道配置** 配送计划将更改同步到渠道。 您可以在 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划** 中找到配送计划。 

最后，在 MPOS 中，使用 **选择硬件工作站** 操作选择与您之前为说明输入的值匹配的硬件工作站，并将此硬件工作站设置为 **可用**。 

> [!NOTE]
> - 某些硬件配置文件的更改（如对银箱的更改）需要在与渠道同步更改后打开新班次。
> - Cloud POS 必须使用独立的硬件工作站来与外设通信。

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>具有独立硬件工作站的 MPOS 或 Cloud POS

[![共享外设。](./media/shared-300x254.png)](./media/shared.png)

在这种情况下，独立硬件工作站在 MPOS 和 Cloud POS 客户端之间共享。 这种情况要求您创建共享硬件工作站并指定下载包、端口和硬件工作站使用的硬件配置文件。 您可以通过在特定渠道中选择 **硬件工作站** 快速选项卡（**Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**），然后添加新的 **共享** 类型的新硬件工作站来定义一个新的硬件工作站。 

接下来，提供有助于出纳识别硬件工作站的描述。 在 **主机名** 字段中，以下面的格式输入主机计算机 URL：`https://<MachineName:Port>/HardwareStation`。 （将 **&lt;MachineName:Port&gt;** 替换为硬件工作站的实际计算机名称。）对于独立硬件工作站，则还应指定电子资金转帐 (EFT) 终端 ID。 此值标识当付款连接器与付款提供商通信时，连接到硬件工作站的 EFT 终端。 

接下来，从将托管硬件工作站的计算机，转到 Headquarters 中的渠道，选择该硬件工作站。 然后选择 **下载** 下载硬件工作站安装程序，安装硬件工作站。 有关如何安装硬件工作站的详细信息，请参阅[配置和安装 Retail 硬件工作站](retail-hardware-station-configuration-installation.md)。 

接下来，从 MPOS 或 Cloud POS，使用 **选择硬件工作站** 操作来选择以前已安装的硬件工作站。 选择 **配对** 在 POS 和硬件工作站之间建立安全关系。 必须为每个 POS 和硬件工作站完成一次此步骤。 

配对硬件工作站后，使用相同的操作使硬件工作站在使用时有效。 这种情况下，应将硬件配置文件分配到共享硬件工作站，而不是收银机本身。 如果由于某种原因没有将硬件配置文件直接分配给硬件工作站，将使用分配给收银机的硬件配置文件。

## <a name="client-maintenance"></a>客户端维护

### <a name="registers"></a>收银机

POS 收银机主要通过收银机本身管理，同时还通过分配到收银机的配置文件管理。 特定于单个收银机的属性在收银机级别管理。 这些属性包括使用收银机的商店、收银机编号、描述和特定于收银机本身的 EFT 终端 ID。

### <a name="pos-profiles"></a>POS 配置文件

您可以在 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** 中找到 POS 配置文件。 对于通过配置文件管理收银机的很多方面非常有用，因为可以在多个收银机之间共享配置文件。 配置文件可映射到单个收银机或商店（如果配置文件在商店范围内有效）。 以下各部分描述了 POS 配置文件以及如何使用它们。

#### <a name="offline-profile"></a>脱机配置文件

脱机配置文件在商店级别设置。 它用于指定在 POS 收银机（该收银机未连接到渠道数据库）执行的交易的上载设置。

#### <a name="functionality-profile"></a>功能配置文件

功能配置文件在商店级别设置。 它用于指定可在 POS 执行的功能的商店范围设置。 以下功能通过功能配置文件进行管理。 这些功能按快速选项卡排列。

- **常规** 快速选项卡：

    - 国际标准化组织 (ISO)。
    - 在脱机模式下创建客户。
    - 通过电子邮件发送收据模板。
    - 集中职员登录身份验证。

- **功能** 快速选项卡︰

    - 登录和扩展登录管理。
    - POS 的财务和货币相关方面，如键入价格以及次要币种是否需要小数的能力。
    - 通过 POS 启用时间登记。
    - 产品和付款在 POS 和收据上的显示方式。
    - 日结管理。
    - 渠道数据库交易记录保留参数。
    - 如何从 POS 查找和创建客户。
    - 如何计算折扣。

- **金额** 快速选项卡︰

    - 允许的最大和最小价格。
    - 折扣应用和计算。

- **信息代码** 快速选项卡：

    - 如何在 POS 管理信息代码的所有方面。 有关详细信息，请参阅[信息代码和信息代码组](info-codes-retail.md)。

- **收据编号** 快速选项卡：

    - 指定收据编号掩码，其中可能包括商店编号段、终端编号段、常量段，以及销售、退货、销售订单和报价单是否以单独顺序打印，或它们是否都按照相同的顺序。

#### <a name="receipt-profiles"></a>收据模板

收据模板在硬件配置文件内分配到打印机。 它们用来指定在特定打印机上打印的收据类型。 配置文件包括收据格式的设置，以及确定是否始终打印收据，或是否提示出纳决定是否必须打印收据的设置。 不同的打印机也可能使用不同的收据模板。 例如，打印机 1 是标准的热敏收据打印机，因此具有较小的收据格式。 但是，打印机 2 是全尺寸收据打印机，仅用于打印客户订单收据，这需要更多的空间。 有关详细信息，请参阅[配置收据模板](configure-emailed-receipt-formats.md#configure-a-receipt-profile)。

#### <a name="hardware-profiles"></a>硬件配置文件

硬件配置文件作为本文前面介绍的客户端设置的组件介绍。 硬件配置文件将被直接分配给 POS 收银机或共享硬件工作站，用于指定特定 POS 收银机或硬件工作站使用的设备类型。 硬件配置文件还用于指定用于与付款 SDK 通信的 EFT 设置。

#### <a name="visual-profiles"></a>可视化配置文件

视觉配置文件用于指定特定收银机的主题，在收银机级别分配。 配置文件包含使用的应用程序类型（MPOS 或 Cloud POS）、个性色和主题、字体方案、登录页面背景以及 POS 背景的设置。 有关详细信息，请参阅[创建销售点 (POS) 视觉配置文件](tasks/create-pos-visual-profile-2016-02.md)。 

### <a name="custom-fields"></a>自定义字段

您可以创建自定义字段以添加未现成提供的字段到 POS。 有关如何使用自定义字段的详细信息，请参阅[使用自定义字段博客文章](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/)。

### <a name="language-text"></a>语言文本

您可以通过使用语言文本条目覆盖 POS 中的默认字符串。 若要覆盖 POS 中的字符串，添加新的语言文本行。 然后指定 ID，应覆盖的默认字符串，以及应在 POS 而不是默认字符串显示的文本。

### <a name="channel-reports-configuration"></a>渠道报告配置

您在 **渠道报表配置** 页设置可在零售渠道使用的报表。 您可以通过在 POS 提供报表的 XML 定义并将报表分配给特定权限组来创建新报表。

### <a name="devices"></a>设备

在本文前面介绍了设备。 它们用来管理特定 POS 收银机的启用。 设备还用于指定用于特定收银机和安装程序包（应用于安装 MPOS 客户端）的应用程序。 下面是设备启用状态︰

- **挂起** – 设备准备好被启用。
- **已启用** – 该设备已被启用。
- **停用** – 已在“总部”或通过 POS 停用设备。
- **禁用** – 该设备已被禁用。

与启用相关的其他信息包括更改设备启用状态的工作人员、启用时间戳，以及设备配置是否已经过验证。

### <a name="client-data-synchronization"></a>客户端数据同步

对 POS 客户端的所有更改（除设备启用状态的更改），均必须与渠道数据库同步以使其生效。 要同步对渠道数据库的更改，请导航到 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **配送计划**，并运行所需的配送计划。 对于客户端更改，应运行 **收银机** 和 **渠道配置** 配送计划。

## <a name="additional-resources"></a>其他资源

[配置并安装 Retail Hardware Station](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
