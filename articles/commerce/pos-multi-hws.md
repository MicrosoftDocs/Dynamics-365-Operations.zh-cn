---
title: 打印机和银箱的专用的付款终端和提示
description: 本主题提供有关使用专用付款终端以及提示用户选择银箱和收据打印机的功能的信息。
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 41b0faa7ef24bdae229f7e6760d22357cb87eb0d
ms.sourcegitcommit: 7b7cc93c0f78c6bfc7a3ea66a74a29ba0f218553
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/04/2020
ms.locfileid: "3658350"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>打印机和银箱的专用的付款终端和提示

[!include [banner](includes/banner.md)]

本主题提供有关使用专用付款终端以及提示用户选择银箱和收据打印机的功能的信息。

## <a name="overview"></a>概览

现代零售商正在寻找简化店内结帐体验的方法。 通过电子付款进行无纸化结帐的最新趋势不仅有助于使购买体验更加顺畅，还可以减少为每个商店员工提供全套外围设备的需求。

Microsoft Dynamics 365 Commerce 通过实现以下方案来支持这些趋势：销售点 (POS) 设备始终会有分配给它的专用付款终端，但没有自己的收据打印机或银箱。 当员工必须打印收据或接收现金付款时，系统会提示他们选择已配置这些设备的硬件工作站。

## <a name="key-terms"></a>重要术语

| 条款 | 说明 |
|---|---|
| 登记簿 | 用于配置 POS 收银机实例的实体。 |
| 设备 | POS 收银机和分配给它的 Modern POS 应用程序的物理实例的表示形式。 |
| 专用硬件工作站 | 内置在适用于 Windows 的 Modern POS 和适用于 Android 的 Modern POS 应用程序中的硬件工作站业务逻辑。 |
| 银箱弹出 (d/k) 端口 | 将银箱连接到收据打印机的传统方法。 |
| 网络外设 | 对网络支持的付款终端、收据打印机和银箱的内置支持。 |

## <a name="supported-pos-clients-and-devices"></a>支持的 POS 客户端和设备

本主题中介绍的功能由适用于 Windows 的 Modern POS 和适用于 Android的 Modern POS 的 POS 客户端支持。

此功能支持网络支持的付款终端和收据打印机。 您可以通过 d/k 端口将银箱连接到网络支持的收据打印机，以此来提供银箱支持。

此功能的现成支持由[适用于 Adyen 的 Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3) 提供。 但是，可以通过 Commerce 付款软件开发套件 (SDK) 支持其他付款连接器。 支持的收据打印机包括 Star Micronics 和 Epson 的网络支持的收据打印机。

要设置 Star Micronics 收据打印机，请使用 Star Micronics 打印机实用程序配置设备，以可以通过网络上使用它。 此实用程序还会提供设备的 IP 地址。

要设置 Epson 收据打印机，请使用 Epson ePOS-Print 实用程序将设备设置为使用网络协议。

有关如何设置网络外围设备的详细信息，请参阅[网络外围设备支持概述](https://go.microsoft.com/fwlink/?linkid=2129965)。

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>为打印机和银箱设置专用付款终端和提示

### <a name="set-up-hardware-profiles"></a>设置硬件配置文件

您必须有两种类型的硬件配置文件。 第一种分配给收银机。 第二种分配给商店级别的硬件工作站，用于对网络收据打印机和银箱进行逻辑分组。

#### <a name="set-up-a-hardware-profile-for-the-register"></a>设置收银机的硬件配置文件

要设置分配给收银机的硬件配置文件，请按照下列步骤操作。

1. 在 Dynamics 365 Commerce 中，搜索**硬件配置文件**。
2. 选择**新建**。
3. 分配硬件配置文件编号，然后输入描述。 此硬件配置文件将分配给收银机本身。 因此，诸如**专用与后备**这样的描述就可以。
4. 在不同设备类型的快速选项卡上，设置以下设备类型。

    | 设备 | 类型 | 设备名称 | 其他详细信息 |
    |---|---|---|---|
    | 打印机 | 回退 | **Epson** 或 **Star** | 设备名称区分大小写。 **收据模板 ID** 应该与映射到网络打印机的**收据模板 ID** 相同，网络打印机在渠道级别分配给硬件工作站的硬件配置文件中设置。 |
    | 银箱 | 回退 | **Epson** 或 **Star** | 设备名称区分大小写。 将**使用共享班次**选项设置为**是**。 |
    | EFT 服务 | Adyen | 不适用 | 有关如何设置现成的 Adyen 连接器的信息，请参阅[适用于 Adyen 的 Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)。 可以通过 [Commerce 付款软件开发套件 (SDK)](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension) 支持其他付款连接器。 |
    | PIN 小键盘 | 网络 | **MicrosoftAdyenDeviceV001** | 无。 |

5. 在 Dynamics 365 Commerce 中，搜索**收银机**。
6. 通过选择收银机编号选择一个收银机，然后选择**编辑**。
7. 将刚才创建的硬件配置文件分配给应该使用专用付款终端的收银机。 映射到此收银机的设备必须使用适用于 Windows 的 Modern POS 应用程序或适用于 Android 的 Modern POS 应用程序。
8. 选择**保存**。
9. 在“操作”窗格上的**收银机**选项卡中，选择**配置 IP 地址**。
10. 在 **PIN 小键盘**快速选项卡上，输入付款终端的 IP 地址。 有关如何使用 Adyen 连接器获取付款终端 IP 地址的信息，请参阅[适用于 Adyen 的 Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)。
11. 选择**保存**。

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>设置收据打印机和银箱的硬件配置文件

要设置用于将网络收据打印机和银箱分组的硬件配置文件，请按照下列步骤操作。

1. 在 Dynamics 365 Commerce 中，搜索**硬件配置文件**。
2. 选择**新建**。
3. 分配硬件配置文件编号，然后输入描述。 此硬件配置文件将用于对收据打印机和银箱进行分组。 因此，诸如**网络打印机和银箱**这样的描述就可以。
4. 在不同设备类型的快速选项卡上，设置以下设备类型。

    | 设备 | 类型 | 说明 | 其他详细信息 |
    |---|---|---|---|
    | 打印机 | 网络 | **Epson** 或 **Star** | 设备名称区分大小写。 **收据模板 ID** 应该与映射到打印机的**收据模板 ID** 相同，打印机在分配给收银机的硬件配置文件中设置。 |
    | 银箱 | 回退 | **Epson** 或 **Star** | 设备名称区分大小写。 将**使用共享班次**选项设置为**是**。 |

5. 选择**保存**。

### <a name="set-up-hardware-stations"></a>设置硬件工作站

您必须有两个硬件工作站。 第一个将映射到收银机。 每当必须打印收据或必须打开银箱时，将根据需要选择第二个。

#### <a name="register-a-hardware-station"></a>登记硬件工作站

1. 在 Dynamics 365 Commerce 中，搜索**所有商店**。
2. 通过选择商店的**零售渠道 ID** 值，然后选择**编辑**来选择商店。
3. 在**硬件工作站**快速选项卡上，选择**添加**。
4. 将**硬件工作站类型**设置为**专用**。
5. 输入描述，但不要为此硬件工作站设置任何其他值。 此硬件工作站将始终用于收银机。 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>设置收据打印机和银箱的硬件工作站

1. 在 Dynamics 365 Commerce 中，搜索**所有商店**。
2. 通过选择商店的**零售渠道 ID** 值，然后选择**编辑**来选择商店。
3. 在**硬件工作站**快速选项卡上，选择**添加**。
4. 将**硬件工作站类型**设置为**专用**。
5. 输入描述。 此硬件工作站将用于收据打印机和银箱。
6. 在**硬件配置文件**字段中，选择您先前为收据打印机和银箱创建的硬件配置文件。
7. 选择**保存**。
8. 在仍然选择了收据打印机和银箱的硬件工作站时，选择**配置 IP 地址**。
9. 获取打印机的 IP 地址，并将其输入为收据打印机和银箱的 IP 地址。
10. 选择**保存**
11. 搜索**分配计划**。
12. 选择分配计划 **1090**，然后选择**立即运行**。
13. 选择分配计划 **1070**，然后选择**立即运行**。

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>设置系统以根据需要提示选择收据打印机和银箱

1. 在支持的 POS 客户端，如果某个班次已打开，关闭当前班次。
2. 登录，然后选择**非银箱银箱工序**。
3. 使用**管理硬件工作站**操作打开一个硬件工作站。
4. 选择您为收银机创建的硬件工作站以将其激活。
5. 注销 POS，重新登录，然后打开一个班次。

现在，分配给硬件配置文件的付款终端将始终处于活动状态，系统会在需要收据打印机或银箱时提示您。

许多要求此功能的商家都希望通过提供电子邮件收据和鼓励电子付款来减少浪费。 根据 POS 的配置，仅当客户需要实体收据或要用现金支付时，系统才会提示商店员工选择收据打印机或银箱。

每次交易仅提示商店员工选择硬件工作站一次，除非必须打印收据并且使用现金付款，否则最初选择的硬件配置文件不会同时包括这两种设备。 在这种情况下，将再次提示商店员工选择可用于完成交易的硬件工作站。

## <a name="related-articles"></a>相关文章

- [在 Android 和 iOS 中安装 POS Hybrid 应用](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [适用于 Adyen 的 Dynamics 365 付款连接器](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [网络外围设备支持概述](https://go.microsoft.com/fwlink/?linkid=2129965)
