---
title: 选择 Store Commerce 或 Cloud POS
description: 本文介绍了 Store Commerce 和 Cloud POS 之间的主要差异，并介绍了实现 Dynamics 365 Commerce 的零售商应考虑的各种因素，以帮助他们根据自己的要求做出最佳选择。
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: bbb5f3d4c61907243bed404f3ab7bea05c78b1c0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276446"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>选择 Store Commerce 或 Cloud POS

[!include [banner](includes/banner.md)]

本文介绍了 Store Commerce 和 Cloud POS 之间的主要差异，并介绍了实现 Dynamics 365 Commerce 的零售商应考虑的各种因素，以帮助他们根据自己的要求做出最佳选择。 此主题还为实施人员提供在部署 Dynamics 365 Commerce 时应该考虑的因素的其他背景、建议和指南。 通过查看并在部署过程中遵循此指导，实施人员可以避免可能会影响用户满意度或性能的问题。

## <a name="insights"></a>见解

Commerce 提供多种部署和拓扑选项。 因此，零售商可以选择最满足其业务和技术要求的组件和配置。 需要仔细考虑的一个实现方面是平台的选择和销售点 (POS) 组件的窗体因子。

### <a name="pos-platform-and-form-factor-considerations"></a>POS 平台和窗体因子考虑事项

Commerce 支持以下 POS 选项：

- 适用于 Microsoft Windows 的 Store Commerce
- 适用于 iOS 和 Android 的 Store Commerce
- Cloud POS (CPOS) 支持 Microsoft Edge 和 Google Chrome 浏览器
- 适用于 Microsoft Windows 的 Modern POS (MPOS)（将于 2023 年 10 月弃用 MPOS。） 

在任何情况下，POS（Store Commerce 和 CPOS）都共享同一个核心应用程序代码。 由于以下原因这一点很重要：

- 用户界面 (UI) 是一致的，不管平台或窗体因子如何。
- 大多数功能能力是相同的，无论平台或窗体因子如何。 不过，也存在某些重要差异。 这些差异在本文中有说明。
- 在每个商店中，POS 差异可以合并，并可以同时运行。 例如，对于其主要收银机，零售商可以在运行 Windows 的计算机上使用 Store Commerce。 但是，零售商可以使用基于浏览器的终端或移动设备补充这些收银机。
- 自定义和扩展可以跨平台和窗体因子轻松使用。 由于核心应用程序代码被共享，大多数自定义可以实施一次，而不是多次。

### <a name="store-commerce-vs-cpos"></a>Store Commerce 与 CPOS

尽管 Store Commerce 和 CPOS 大部分是相同的，但您必须了解某些重要的差异。

#### <a name="store-commerce"></a>Store Commerce

Store Commerce 是一个在设备上安装和服务的桌面应用程序。

- **Windows** – 适用于 Windows 的 Store Commerce 应用程序包含所有应用程序代码、Commerce Runtime (CRT) 和硬件工作站 (HWS)。
- **iOS/Android** – 在这些平台上，此应用程序充当 CPOS 应用程序代码的主机。 换言之，应用程序代码来自 Commerce Scale Unit 上托管的 CPOS 服务器。 有关详细信息，请参阅 [Commerce Scale Unit 概述](dev-itpro/retail-store-system-begin.md)。

#### <a name="cpos"></a>CPOS

由于 CPOS 在浏览器中运行，应用程序不在设备上安装。 浏览器改从 CPOS 服务器访问应用程序代码。 因此，CPOS 不能直接访问 POS 硬件或在脱机状态下工作。

### <a name="store-deployment-considerations"></a>商店部署注意事项

除了平台和窗体因子外，零售商还必须在商店选择部署选项。 下表显示每个 POS 选项可用的配置。

| POS 应用程序            | Commerce Scale Unit | 脱机可用 | 本地 HWS 支持 |
|----------------------------|---------------------|-------------------|-------------------|
| 适用于 Windows 的 Store Commerce | 云或 RSSU       | 是               | 是               |
| 适用于 Android 的 Store Commerce | 云或 RSSU       | 否                | 是               |
| 适用于 iOS 的 Store Commerce     | 云或 RSSU       | 否                | 否                |
| 云 POS                  | 云或 RSSU       | 否                | 否                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit 是承载 CRT 的组件。 CRT 包含 POS 使用的所有业务逻辑，并提供对渠道数据库的访问。 当在线时，商店中的所有 POS 客户端均使用 Commerce Scale Unit。 Commerce Scale Unit 可以在云或商店中部署。

#### <a name="offline-mode"></a>脱机模式

适用于 Windows 的 Store Commerce 支持脱机模式。 在脱机模式下，POS 可以继续处理销售，即使它从 Commerce Scale Unit 断开。 在恢复连接时，它可以与渠道数据库同步。 Store Commerce 使用其自己的嵌入 CRT 实例，并暂时使用其自己的本地数据源（脱机 SQL Server 数据库）。 有关脱机功能的详细信息，请参阅 [POS 脱机功能](pos-offline-functionality.md)。

### <a name="pos-peripheralhardware-considerations"></a>POS 外设/硬件注意事项

零售商还必须考虑 POS 如何访问打印机、银箱和付款终端等设备和外设。 硬件工作站可专用于 POS 收银机或在商店中的收银机之间共用。

| POS 应用程序            | 本地 HWS OPOS | 网络外设 | 共享的 HWS 支持 |
|----------------------------|----------------|---------------------|--------------------|
| 适用于 Windows 的 Store Commerce | 是            | 是                 | 是                |
| 适用于 Android 的 Store Commerce | 否             | 是                 | 是                |
| 适用于 iOS 的 Store Commerce     | 否             | 否                  | 是                |
| 云 POS                  | 否             | 否                  | 是                |

有关硬件工作站的详细信息，请参阅[配置和安装 Retail 硬件工作站](retail-hardware-station-configuration-installation.md)。

## <a name="implementation-considerations"></a>实施注意事项

在您规划商店的 POS 实现时请考虑以下信息：

- **功能要求** – 核心业务流程和功能是相同的，不论平台、窗体因子或部署拓扑如何。 因此，大多数零售商在规划其实现时不必考虑功能要求。
- **连接** – 网络可用性（广域网 \[WAN\] 和局域网 \[LAN\]）是需要仔细考虑的一个主要因素。 如果系统不可用于业务关键型流程，那么零占地的云托管解决方案在成本和简化方面带来的任何优势都将消失。

    除非特定设备的连接非常可靠和灵活，或者零售商可以接受一定的停机时间，否则我们建议以下选项之一：

    - 在 Windows 中使用 Store Commerce，并启用脱机模式。
    - 部署本地 Commerce Scale Unit。

    这两个选项不彼此排斥。 对于最可靠的拓扑，零售商可以部署本地 RSSU 以减少对互联网连接与 Azure 可用性的依赖，如果本地服务器或网络有问题，他们还可以部署启用脱机模式的 POS 收银机。

- **硬件设备/外设** – Retail POS 系统的一个重要方面是它能够使用 POS 外设，如打印机、银箱和付款终端。 虽然所有可用 POS 选项均可以使用外设，但只有适用于 Windows 的 Store Commerce 直接支持它们。 对于所有其他应用程序，均需要一个或多个硬件工作站。 虽然此方法增加了灵活性，但必须部署、配置和服务其他组件。
- **系统要求** – POS 应用程序的系统要求会发生变化。 在您进行选择前，请确保检查最新信息。 例如，因为 CPOS 在浏览器中运行，它支持各种操作系统。 有关系统要求的详细信息，请参阅[云部署的系统要求](../fin-ops-core/fin-ops/get-started/system-requirements.md)。
- **部署和服务** – 部署和服务要求的复杂程度可能因应用程序和部署选择的更改而改变。 例如，对于云托管的 CPOS 部署，您不必在每台设备上安装和更新。 因此，此方法将极大地减少复杂性和成本。 但是，如果您在每个收银机上部署 Store Commerce 并启用脱机模式，而且您还部署了共享的硬件工作站，这会大大增加必须管理的终结点数量。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
