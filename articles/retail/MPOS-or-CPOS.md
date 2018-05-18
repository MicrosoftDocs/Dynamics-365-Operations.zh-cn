---
title: "在 Modern POS 和 Cloud POS 之间选择"
description: "本主题说明 Retail Modern POS 和 Cloud POS 之间的主要差别。 它还描述实现 Microsoft Dynamics 365 for Retail 的零售商应考虑的以帮助他们作出满足自己要求的最佳选择的各个因素。"
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7eb15f9f73f4773d98160e1b0ec5ce74c159cdea
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---

# <a name="choose-between-modern-pos-and-cloud-pos"></a>在 Modern POS 和 Cloud POS 之间选择

[!include [banner](includes/banner.md)]

此主题为实施人员提供在部署 Microsoft Dynamics 365 for Retail 时应该考虑的因素的其他背景、建议和指南。 通过查看并在部署过程中遵循此指导，实施人员可以避免可能会影响用户满意度或性能的问题。

## <a name="insights"></a>洞察力
Retail 提供多种部署和拓扑选项。 因此，零售商可以选择最满足其业务和技术要求的组件和配置。 需要仔细考虑的一个实现方面是平台的选择和销售点 (POS) 组件的窗体因子。

### <a name="pos-platform-and-form-factor-considerations"></a>POS 平台和窗体因子考虑事项
Retail 支持以下 POS 选项：

- 适用于 Microsoft Windows 的 Retail Modern POS (MPOS)
- 适用于 Microsoft Windows Phone 的 MPOS
- 适用于 Apple iPad 或 Google Android 平板电脑的 MPOS
- Cloud POS (CPOS) 支持 Microsoft Edge、Internet Explorer 和 Google Chrome 浏览器

在任何情况下，POS（MPOS 和 CPOS）都共享同一个核心应用程序代码。 由于以下原因这一点很重要：

- 用户界面 (UI) 是一致的，不管平台或窗体因子如何。
- 大多数功能能力是相同的，无论平台或窗体因子如何。 不过，也存在某些重要差异。 这些差异在本主题中有说明。
- 在指定商店中，POS 差异可以合并，并可以同时运行。 例如，对于其主要收银机，零售商可以在运行 Windows 的计算机上使用 MPOS。 但是，零售商可以使用基于浏览器的终端或移动设备补充这些收银机。
- 自定义和扩展可以跨平台和窗体因子轻松使用。 由于核心应用程序代码被共享，大多数自定义可以实施一次，而不是多次。

### <a name="mpos-vs-cpos"></a>MPOS 与 CPOS
尽管 MPOS 和 CPOS 大部分是相同的，但您必须了解某些重要的差异。

#### <a name="mpos"></a>MPOS

Windows、iOS 或 Android 设备上的 MPOS 是在该设备上打包、安装和服务的应用程序。

- **Windows** – Windows 应用程序的 MPOS 包含所有应用程序代码和嵌入的 Commerce Runtime (CRT)。 
- **iOS/Android** – 在这些平台上，此应用程序充当 CPOS 应用程序代码的主机。 换言之，应用程序代码来自 Microsoft Azure 或零售商店扩展单位 (RSSU) 上的 CPOS 服务器。 有关详细信息，请参阅[零售商店扩展单位概览](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin)。

#### <a name="cpos"></a>CPOS

由于 CPOS 在浏览器中运行，应用程序不在设备上安装。 浏览器改从 CPOS 服务器访问应用程序代码。 因此，CPOS 不能直接访问 POS 硬件或在脱机状态下工作。

### <a name="store-deployment-considerations"></a>商店部署注意事项
除了平台和窗体因子外，零售商还必须在商店选择部署选项。 下表显示每个 POS 选项可用的配置。

| POS 应用程序         | Retail Server | 脱机可用 |
|-------------------------|---------------|-------------------|
| 适用于 Windows 的 MPOS        | 云或 RSSU | 是               |
| 适用于 iOS 或 Android 的 MPOS | 云或 RSSU | 无                |
| 云 POS               | 云或 RSSU | 无                |

#### <a name="retail-server"></a>Retail Server

Retail 服务器是承载 CRT 的组件。 CRT 包含 POS 使用的所有业务逻辑，并提供对渠道数据库的访问。 当在线时，商店中的所有 POS 客户端均使用 Retail 服务器。 Retail 服务器可以在云或商店 (RSSU) 中部署。

#### <a name="offline-mode"></a>脱机模式

适用于 Windows 的 MPOS 支持脱机模式。 在脱机模式下，POS 可以继续处理销售，即使它从 Retail 服务器断开。 在恢复连接时，它可以与渠道数据库同步。 MPOS 使用其自己的嵌入 CRT 实例，并暂时使用其自己的本地数据源（脱机 SQL Server 数据库）。 有关脱机功能的详细信息，请参阅 [POS 脱机功能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality)。

### <a name="pos-peripheralhardware-considerations"></a>POS 外设/硬件注意事项
零售商还必须考虑 POS 如何访问打印机、银箱和付款终端等设备和外设。 仅适用于 Windows 的 MPOS 支持与这些设备的直接通信。 适用于 Windows Phone、iOS 或 Android 的 MPOS 和 Cloud POS 需要硬件工作站来访问这些设备。 硬件工作站可专用于 POS 收银机或在商店中的收银机之间共用。 有关硬件工作站的详细信息，请参阅[配置和安装 Retail 硬件工作站](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation)。

## <a name="implementation-considerations"></a>实施注意事项
在您规划零售店的 POS 实现时请考虑以下信息：

- **功能要求** – 核心业务流程和功能是相同的，不论平台、窗体因子或部署拓扑如何。 因此，大多数零售商在规划其实现时不必考虑功能要求。
- **连接** - 网络可用性（广域网 \[WAN\] 和局域网 \[LAN\]）是需要仔细考虑的一个主要因素。 如果系统不可用于业务关键型流程，那么零占地的云托管解决方案在成本和简化方面带来的任何优势都将消失。

    除非特定设备的连接非常可靠和灵活，或者零售商可以接受一定的停机时间，否则我们建议以下选项之一：

  - 在 Windows 中使用 MPOS，并启用脱机模式。
  - 部署本地 RSSU。

    这两个选项不彼此排斥。 对于最可靠的拓扑，零售商可以部署本地 RSSU 以减少对互联网连接与 Azure 可用性的依赖，如果本地服务器或网络有问题，他们还可以部署启用脱机模式的 POS 收银机。

- **硬件设备/外设** – Retail POS 系统的一个重要方面是它能够使用 POS 外设，如打印机、银箱和付款终端。 虽然所有可用 POS 选项均可以使用外设，但只有适用于 Windows 的 MPOS 直接支持它们。 对于所有其他应用程序，均需要一个或多个硬件工作站。 虽然此方法增加了灵活性，但必须部署、配置和服务其他组件。
- **系统要求** – POS 应用程序的系统要求会发生变化。 在您进行选择前，请确保检查最新信息。 例如，因为 CPOS 在浏览器中运行，它支持各种操作系统。 有关系统要求的详细信息，请参阅[云部署的系统要求](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements)。
- **部署和服务** – 部署和服务要求的复杂程度可能因应用程序和部署选择的更改而改变。 例如，对于云托管的 CPOS 部署，您不必在每台设备上安装和更新。 因此，此方法将极大地减少复杂性和成本。 但是，如果您在每个收银机上部署 MPOS 并启用脱机模式，而且您还部署了共享的硬件工作站，这会大大增加必须管理的终结点数量。

