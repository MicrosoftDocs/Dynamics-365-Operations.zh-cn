---
title: POS 外围设备和服务的运行状况检查
description: 此主题概述销售点 (POS) 中的运行状况检查操作。
author: BrianShook
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: cd4e97b8dbfc4faf336d4ea927342fd4fa3cc7cd
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779864"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>POS 外围设备和服务的运行状况检查

[!include [banner](includes/banner.md)]

此主题介绍销售点 (POS) 中的运行状况检查操作。

## <a name="overview"></a>概览

零售商店可以是使用大量应用程序和设备的复杂环境。 随着经营规模扩大，可能很难确保经营始终平稳开展，例如，因为依赖的外围设备可能在一天内损坏或被意外拔下。 对于较大规模的商家来说，诊断与设备和服务有关的问题可能成本很高，而对于较小规模的经营来说，同样会让人烦心。

Microsoft Dynamics 365 Commerce 版本 10.0.10 及更高版本中有一项运行状况检查操作，可帮助部分避免这样的成本和烦恼。 此操作提供在正常经营外直接从 POS 测试设备的方法。 因此，可以帮助零售商提前检测问题。

## <a name="key-terms"></a>重要术语

| 术语 | 说明 |
|---|---|
| 外围设备 | POS 应用程序用于促成交易和商店中的其他操作的任何设备。 例如，收银箱、条形码扫描仪和付款终端。 |
| 服务 | 在此主题中，服务是 POS 应用程序用于执行交易和日常经营的辅助应用程序。 例如，帮助计算税或装运费用的应用。 |

## <a name="health-check-operation"></a>运行状况检查操作

运行状况检查操作是 Commerce Headquarters 中 **POS 操作** 页内的操作 717。 其可在 POS 处于非银箱模式时使用。 但是，必须有一个硬件工作站处于活动状态。

默认情况下，运行状况检查经测试收银机的当前活动硬件工作站的硬件配置文件中配置的设备。 如果收银机在一天内使用多个硬件工作站，若要对所有这些硬件工作站执行运行状况检查，该收银机同时只能连接到一个硬件工作站。 不存在商店级运行状况检查。 但是，可以通过 Commerce Server 扩展执行这种检查。

### <a name="out-of-box-health-checks"></a>自带运行状况检查

| 类型 | 连接 | 明细 |
|---|---|---|
| 打印机 | OPOS | 此项检查测试 POS (OPOS) 功能的链接和嵌入。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| 行显示内容 | OPOS | 此项检查测试基本 OPOS 功能。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| 双显示器 | 窗口 | 此项检查确保操作系统检测第二个 Windows 显示器。 | 
| MSR | OPOS | 此项检查测试基本 OPOS 功能。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| 银箱 | OPOS | 此项检查测试基本 OPOS 功能。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| 扫描仪 | OPOS | 此项检查测试基本 OPOS 功能。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| 比例 | OPOS | 此项检查测试基本 OPOS 功能。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| PIN 小键盘 | OPOS | 此项检查测试基本 OPOS 功能。 下面举了一些示例加以说明：<ul><li>打开：**Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>关闭：**DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| 付款终端 | 付款 SDK | 此项检查测试付款 SDK 提供的基本付款终端功能。 <ul><li>锁定</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>期结</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>在 POS 中使用运行状况检查操作

在 POS 中启动运行状况检查操作之后，右侧的窗格将列出配置的设备，并显示各设备的状态。 若要对一个设备执行运行状况检查，请选择该设备，然后选择 **测试选定设备**。 若要对所有设备执行运行状况检查，请选择 **全部测试**。 **全部测试** 功能一次一个测试所有设备，并更新 **状态** 列中各设备的状态。

**上次检查** 列 显示上次对每个设备执行运行状况检查的时间。

如果通过了某个设备的运行状况检查（即未遇到任何错误），该设备的状态将为 **正常**。 如果运行状况检查失败，则状态将指示存在错误。 在此情况下，右侧的窗格提供与错误有关的详细信息，或指示用户联系系统管理员。

某些设备（如 OPOS 键锁）没有自带运行状况检查测试。 如果没有为使用的任何设备检测到运行状况检查测试，状态将为 **不支持**。

### <a name="extending-health-checks"></a>扩展运行状况检查

自带运行状况检查测试被配置为为典型错误提供一些用户容易明白的消息。 但是，并未涵盖所有方案。 通过扩展，商家可以将用户容易明白的消息映射到可能特定于其环境的错误。

也可以创建自定义的运行状况检查来测试自带不支持的设备，或测试 POS 依赖的服务。

## <a name="related-articles"></a>相关文章

[Modern POS (MPOS) 触发器和打印](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]